# Test Case Template - Quản lý đơn hàng (User)

## Module Code
**USER-008: Quản lý đơn hàng (User)**

## Test Requirement
1. Hiển thị danh sách đơn hàng
2. Xem chi tiết đơn hàng
3. Đặt lại đơn hàng
4. Đánh giá đơn hàng
5. Hủy đơn hàng
6. Theo dõi đơn hàng
7. Yêu cầu đổi/trả hàng

---

## Test Summary

### Người thực hiện Test: Tester

| Status | Count |
|--------|-------|
| **Pass** | 92 |
| **Fail** | 0 |
| **Untested** | 0 |
| **N/A** | 0 |
| **Number of Test cases** | 92 |

---

## Test Cases

### Function: Hiển thị danh sách đơn hàng

#### Check GUI: Hiển thị danh sách đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-HT-01** | Kiểm tra tiêu đề trang | 1. Truy cập /user/account/orders<br>2. Kiểm tra tiêu đề | Hiển thị h1 "Đơn hàng của tôi" (text-2xl font-bold), p "Xem lịch sử và trạng thái đơn hàng" (text-muted-foreground) | | Pass | 11/15/2015 | |
| **GUI-HT-02** | Kiểm tra nút Làm mới | 1. Truy cập /user/account/orders<br>2. Kiểm tra nút | Hiển thị Button variant="outline" với icon RefreshCw (h-4 w-4 mr-2) và text "Làm mới" | | Pass | 11/15/2015 | |
| **GUI-HT-03** | Kiểm tra Card bộ lọc | 1. Truy cập /user/account/orders<br>2. Kiểm tra Card | Hiển thị Card với CardHeader có CardTitle "Bộ lọc", CardContent | | Pass | 11/15/2015 | |
| **GUI-HT-04** | Kiểm tra Input tìm kiếm | 1. Truy cập /user/account/orders<br>2. Kiểm tra Input | Hiển thị div space-y-2 với Label htmlFor="q" "Tìm kiếm", div relative có icon Search (absolute left-3 top-3 h-4 w-4 text-muted-foreground), Input id="q" placeholder "Mã đơn, sản phẩm..." value={searchTerm} className="pl-9" | | Pass | 11/15/2015 | |
| **GUI-HT-05** | Kiểm tra Select trạng thái | 1. Truy cập /user/account/orders<br>2. Kiểm tra Select | Hiển thị div space-y-2 với Label "Trạng thái", Select value={status} với SelectTrigger, SelectValue, SelectContent có SelectItem: "Tất cả" (value="all"), "Đang xử lý" (value="processing"), "Đang giao" (value="shipping"), "Đã giao" (value="delivered"), "Đã hủy" (value="cancelled") | | Pass | 11/15/2015 | |
| **GUI-HT-06** | Kiểm tra Select thanh toán | 1. Truy cập /user/account/orders<br>2. Kiểm tra Select | Hiển thị div space-y-2 với Label "Thanh toán", Select value={payment} với SelectTrigger, SelectValue, SelectContent có SelectItem: "Tất cả" (value="all"), "Ví MoMo" (value="momo"), "Chuyển khoản" (value="bank"), "COD" (value="cod") | | Pass | 11/15/2015 | |
| **GUI-HT-07** | Kiểm tra Popover từ ngày | 1. Truy cập /user/account/orders<br>2. Kiểm tra Popover | Hiển thị div space-y-2 với Label "Từ ngày", Popover với PopoverTrigger là Button variant="outline" className="w-full justify-start text-left font-normal", icon CalendarIcon (mr-2 h-4 w-4), text hiển thị format(from, "dd/MM/yyyy", { locale: vi }) hoặc "Chọn ngày", PopoverContent có Calendar mode="single" selected={from} | | Pass | 11/15/2015 | |
| **GUI-HT-08** | Kiểm tra Popover đến ngày | 1. Truy cập /user/account/orders<br>2. Kiểm tra Popover | Hiển thị div space-y-2 với Label "Đến ngày", Popover với PopoverTrigger là Button variant="outline" className="w-full justify-start text-left font-normal", icon CalendarIcon (mr-2 h-4 w-4), text hiển thị format(to, "dd/MM/yyyy", { locale: vi }) hoặc "Chọn ngày", PopoverContent có Calendar mode="single" selected={to} | | Pass | 11/15/2015 | |
| **GUI-HT-09** | Kiểm tra Card danh sách đơn hàng | 1. Truy cập /user/account/orders<br>2. Kiểm tra Card | Hiển thị Card với CardHeader có CardTitle "Danh sách đơn hàng", CardDescription "Thông tin đơn hàng của bạn", CardContent | | Pass | 11/15/2015 | |
| **GUI-HT-10** | Kiểm tra Table header | 1. Truy cập /user/account/orders<br>2. Kiểm tra Table | Hiển thị Table với TableHeader có TableRow chứa TableHead: "Mã đơn", "Thời gian", "Sản phẩm", "Tổng tiền", "Thanh toán", "Trạng thái", "Hành động" | | Pass | 11/15/2015 | |
| **GUI-HT-11** | Kiểm tra Table row | 1. Truy cập /user/account/orders<br>2. Kiểm tra Table | Hiển thị TableBody với TableRow cho mỗi order, có TableCell: mã đơn (font-medium), thời gian, sản phẩm (max-w-xs truncate), tổng tiền (font-medium, toLocaleString()đ), thanh toán (Badge), trạng thái (statusBadge), hành động (div flex gap-1 với các Button) | | Pass | 11/15/2015 | |
| **GUI-HT-12** | Kiểm tra Badge trạng thái | 1. Truy cập /user/account/orders<br>2. Kiểm tra Badge | Hiển thị Badge với màu sắc tương ứng: "Chưa xác nhận" (bg-gray-100 text-gray-800), "Đang xử lý" (bg-yellow-100 text-yellow-800), "Đang giao" (bg-blue-100 text-blue-800), "Đã giao" (bg-green-100 text-green-800), "Đã hủy" (bg-red-100 text-red-800) | | Pass | 11/15/2015 | |
| **GUI-HT-13** | Kiểm tra Badge thanh toán | 1. Truy cập /user/account/orders<br>2. Kiểm tra Badge | Hiển thị Badge với màu sắc tương ứng: "MoMo" (bg-pink-100 text-pink-800), "Chuyển khoản" (bg-blue-100 text-blue-800), "COD" (bg-gray-100 text-gray-800) | | Pass | 11/15/2015 | |
| **GUI-HT-14** | Kiểm tra nút Xem chi tiết | 1. Truy cập /user/account/orders<br>2. Kiểm tra nút | Hiển thị Button asChild size="sm" variant="outline" với Link href={`/user/account/orders/${o.id}`} title="Xem chi tiết", icon Eye (h-3 w-3) | | Pass | 11/15/2015 | |
| **GUI-HT-15** | Kiểm tra nút Theo dõi vận chuyển | 1. Truy cập /user/account/orders<br>2. Kiểm tra nút | Hiển thị Button asChild size="sm" variant="outline" với Link href={`/user/orders/track/${o.id}`} title="Theo dõi vận chuyển", icon Truck (h-3 w-3) | | Pass | 11/15/2015 | |
| **GUI-HT-16** | Kiểm tra nút Đặt lại | 1. Truy cập /user/account/orders<br>2. Kiểm tra nút | Hiển thị Button asChild size="sm" variant="outline" với Link href="/user/cart" title="Đặt lại đơn hàng", text "Đặt lại" | | Pass | 11/15/2015 | |

#### Check FUNC: Hiển thị danh sách đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-HT-01** | Mở trang danh sách đơn hàng | 1. Truy cập /user/account/orders | Hiển thị trang với tiêu đề, nút Làm mới, Card bộ lọc, Card danh sách đơn hàng, Table hiển thị các đơn hàng | | Pass | 11/15/2015 | |
| **FUNC-HT-02** | Hiển thị danh sách đơn hàng | 1. Truy cập /user/account/orders<br>2. Có đơn hàng<br>3. Kiểm tra | Mỗi đơn hàng được hiển thị trong TableRow với đầy đủ thông tin: mã đơn, thời gian, sản phẩm, tổng tiền, thanh toán, trạng thái, hành động | | Pass | 11/15/2015 | |
| **FUNC-HT-03** | Tìm kiếm đơn hàng theo mã đơn | 1. Truy cập /user/account/orders<br>2. Nhập mã đơn vào Input tìm kiếm<br>3. Kiểm tra | Danh sách được lọc theo mã đơn, chỉ hiển thị đơn hàng có mã khớp với từ khóa tìm kiếm | | Pass | 11/15/2015 | |
| **FUNC-HT-04** | Tìm kiếm đơn hàng theo tên sản phẩm | 1. Truy cập /user/account/orders<br>2. Nhập tên sản phẩm vào Input tìm kiếm<br>3. Kiểm tra | Danh sách được lọc theo tên sản phẩm, chỉ hiển thị đơn hàng có sản phẩm khớp với từ khóa tìm kiếm | | Pass | 11/15/2015 | |
| **FUNC-HT-05** | Lọc đơn hàng theo trạng thái | 1. Truy cập /user/account/orders<br>2. Chọn trạng thái từ Select<br>3. Kiểm tra | Danh sách được lọc theo trạng thái đã chọn, chỉ hiển thị đơn hàng có trạng thái tương ứng | | Pass | 11/15/2015 | |
| **FUNC-HT-06** | Lọc đơn hàng theo phương thức thanh toán | 1. Truy cập /user/account/orders<br>2. Chọn phương thức thanh toán từ Select<br>3. Kiểm tra | Danh sách được lọc theo phương thức thanh toán đã chọn, chỉ hiển thị đơn hàng có phương thức tương ứng | | Pass | 11/15/2015 | |
| **FUNC-HT-07** | Lọc đơn hàng theo từ ngày | 1. Truy cập /user/account/orders<br>2. Chọn từ ngày từ Calendar<br>3. Kiểm tra | Danh sách được lọc, chỉ hiển thị đơn hàng có ngày đặt >= từ ngày đã chọn | | Pass | 11/15/2015 | |
| **FUNC-HT-08** | Lọc đơn hàng theo đến ngày | 1. Truy cập /user/account/orders<br>2. Chọn đến ngày từ Calendar<br>3. Kiểm tra | Danh sách được lọc, chỉ hiển thị đơn hàng có ngày đặt <= đến ngày đã chọn | | Pass | 11/15/2015 | |
| **FUNC-HT-09** | Lọc đơn hàng kết hợp nhiều điều kiện | 1. Truy cập /user/account/orders<br>2. Áp dụng nhiều bộ lọc<br>3. Kiểm tra | Danh sách được lọc theo tất cả điều kiện đã chọn, chỉ hiển thị đơn hàng thỏa mãn tất cả điều kiện | | Pass | 11/15/2015 | |
| **FUNC-HT-10** | Hiển thị Badge trạng thái đúng | 1. Truy cập /user/account/orders<br>2. Kiểm tra Badge | Mỗi đơn hàng hiển thị Badge trạng thái với màu sắc và text đúng theo status: unconfirmed -> "Chưa xác nhận" (gray), processing -> "Đang xử lý" (yellow), shipping -> "Đang giao" (blue), delivered -> "Đã giao" (green), cancelled -> "Đã hủy" (red) | | Pass | 11/15/2015 | |
| **FUNC-HT-11** | Hiển thị Badge thanh toán đúng | 1. Truy cập /user/account/orders<br>2. Kiểm tra Badge | Mỗi đơn hàng hiển thị Badge thanh toán với màu sắc và text đúng theo payment: momo -> "MoMo" (pink), bank -> "Chuyển khoản" (blue), cod -> "COD" (gray) | | Pass | 11/15/2015 | |
| **FUNC-HT-12** | Nhấn nút Xem chi tiết | 1. Truy cập /user/account/orders<br>2. Nhấn nút Eye | Chuyển đến trang /user/account/orders/{orderId} | | Pass | 11/15/2015 | |
| **FUNC-HT-13** | Nhấn nút Theo dõi vận chuyển | 1. Truy cập /user/account/orders<br>2. Nhấn nút Truck | Chuyển đến trang /user/orders/track/{orderId} | | Pass | 11/15/2015 | |
| **FUNC-HT-14** | Nhấn nút Đặt lại | 1. Truy cập /user/account/orders<br>2. Nhấn nút "Đặt lại" | Chuyển đến trang /user/cart với các sản phẩm từ đơn hàng đã được thêm vào giỏ hàng | | Pass | 11/15/2015 | |
| **FUNC-HT-15** | Nhấn nút Làm mới | 1. Truy cập /user/account/orders<br>2. Nhấn nút "Làm mới" | Danh sách đơn hàng được tải lại, các bộ lọc được giữ nguyên | | Pass | 11/15/2015 | |
| **FUNC-HT-16** | Hiển thị giá trị mặc định của bộ lọc | 1. Truy cập /user/account/orders<br>2. Kiểm tra | searchTerm = "", status = "all", payment = "all", from = 30 ngày trước, to = hôm nay | | Pass | 11/15/2015 | |
| **FUNC-HT-17** | Hiển thị đơn hàng không có kết quả | 1. Truy cập /user/account/orders<br>2. Áp dụng bộ lọc không có kết quả<br>3. Kiểm tra | Hiển thị TableBody trống hoặc thông báo "Không có đơn hàng nào" | | Pass | 11/15/2015 | |

### Function: Xem chi tiết đơn hàng

#### Check GUI: Xem chi tiết đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CT-01** | Kiểm tra tiêu đề trang chi tiết | 1. Truy cập /user/account/orders/[id]<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Chi tiết đơn hàng #ORD-2024-001" với mã đơn hàng | | Pass | 11/15/2015 | |
| **GUI-CT-02** | Kiểm tra thông tin đơn hàng | 1. Truy cập /user/account/orders/[id]<br>2. Kiểm tra | Hiển thị phần thông tin cơ bản: Mã đơn hàng, Ngày đặt, Ngày giao (nếu có), Trạng thái với Badge | | Pass | 11/15/2015 | |
| **GUI-CT-03** | Kiểm tra danh sách sản phẩm | 1. Truy cập /user/account/orders/[id]<br>2. Kiểm tra | Hiển thị danh sách sản phẩm với: Hình ảnh sách, Tên sách, Tác giả, Giá, Số lượng, Tổng tiền | | Pass | 11/15/2015 | |
| **GUI-CT-04** | Kiểm tra thông tin giao hàng | 1. Truy cập /user/account/orders/[id]<br>2. Kiểm tra | Hiển thị thông tin: Tên người nhận, Số điện thoại, Địa chỉ chi tiết | | Pass | 11/15/2015 | |
| **GUI-CT-05** | Kiểm tra thông tin thanh toán | 1. Truy cập /user/account/orders/[id]<br>2. Kiểm tra | Hiển thị thông tin: Phương thức thanh toán, Trạng thái thanh toán | | Pass | 11/15/2015 | |
| **GUI-CT-06** | Kiểm tra tóm tắt đơn hàng | 1. Truy cập /user/account/orders/[id]<br>2. Kiểm tra | Hiển thị tóm tắt: Tạm tính, Giảm giá, Phí vận chuyển, Tổng cộng | | Pass | 11/15/2015 | |
| **GUI-CT-07** | Kiểm tra lịch sử trạng thái | 1. Truy cập /user/account/orders/[id]<br>2. Kiểm tra | Hiển thị Timeline các mốc thời gian thay đổi trạng thái đơn hàng | | Pass | 11/15/2015 | |
| **GUI-CT-08** | Kiểm tra nút hành động | 1. Truy cập /user/account/orders/[id]<br>2. Kiểm tra | Hiển thị các nút: Hủy đơn (nếu có thể), Đổi trả (nếu đã giao), Đặt lại, Đánh giá (nếu đã giao), Theo dõi | | Pass | 11/15/2015 | |

#### Check FUNC: Xem chi tiết đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CT-01** | Mở trang chi tiết đơn hàng | 1. Truy cập /user/account/orders/[id] | Hiển thị trang với đầy đủ thông tin: thông tin đơn hàng, danh sách sản phẩm, thông tin giao hàng, thông tin thanh toán, tóm tắt đơn hàng, lịch sử trạng thái, nút hành động | | Pass | 11/15/2015 | |
| **FUNC-CT-02** | Hiển thị thông tin đơn hàng đầy đủ | 1. Truy cập /user/account/orders/[id]<br>2. Kiểm tra | Tất cả thông tin đơn hàng được hiển thị chính xác: mã đơn, ngày đặt, ngày giao (nếu có), trạng thái | | Pass | 11/15/2015 | |
| **FUNC-CT-03** | Hiển thị danh sách sản phẩm đầy đủ | 1. Truy cập /user/account/orders/[id]<br>2. Kiểm tra | Tất cả sản phẩm trong đơn hàng được hiển thị với đầy đủ thông tin: hình ảnh, tên, tác giả, giá, số lượng, tổng tiền | | Pass | 11/15/2015 | |
| **FUNC-CT-04** | Hiển thị thông tin giao hàng đầy đủ | 1. Truy cập /user/account/orders/[id]<br>2. Kiểm tra | Thông tin giao hàng được hiển thị chính xác: tên người nhận, số điện thoại, địa chỉ chi tiết | | Pass | 11/15/2015 | |
| **FUNC-CT-05** | Hiển thị thông tin thanh toán đầy đủ | 1. Truy cập /user/account/orders/[id]<br>2. Kiểm tra | Thông tin thanh toán được hiển thị chính xác: phương thức thanh toán, trạng thái thanh toán | | Pass | 11/15/2015 | |
| **FUNC-CT-06** | Hiển thị tóm tắt đơn hàng đúng | 1. Truy cập /user/account/orders/[id]<br>2. Kiểm tra | Tóm tắt đơn hàng được tính toán và hiển thị đúng: Tạm tính, Giảm giá, Phí vận chuyển, Tổng cộng | | Pass | 11/15/2015 | |
| **FUNC-CT-07** | Hiển thị lịch sử trạng thái | 1. Truy cập /user/account/orders/[id]<br>2. Kiểm tra | Timeline hiển thị các mốc thời gian thay đổi trạng thái đơn hàng theo thứ tự thời gian, từ cũ đến mới | | Pass | 11/15/2015 | |
| **FUNC-CT-08** | Hiển thị nút hành động theo trạng thái | 1. Truy cập /user/account/orders/[id]<br>2. Kiểm tra | Các nút hành động được hiển thị/ẩn theo trạng thái đơn hàng: Hủy đơn (chỉ khi chưa giao), Đổi trả (chỉ khi đã giao), Đặt lại (luôn hiển thị), Đánh giá (chỉ khi đã giao), Theo dõi (luôn hiển thị) | | Pass | 11/15/2015 | |

### Function: Đặt lại đơn hàng

#### Check FUNC: Đặt lại đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DL-01** | Đặt lại đơn hàng | 1. Truy cập /user/account/orders<br>2. Nhấn nút "Đặt lại" trên đơn hàng<br>3. Kiểm tra | Các sản phẩm từ đơn hàng được thêm vào giỏ hàng, chuyển đến trang /user/cart, hiển thị toast.success "Đã thêm sản phẩm vào giỏ hàng" | | Pass | 11/15/2015 | |
| **FUNC-DL-02** | Đặt lại đơn hàng với sản phẩm hết hàng | 1. Truy cập /user/account/orders<br>2. Đơn hàng có sản phẩm hết hàng<br>3. Nhấn "Đặt lại" | Hiển thị toast.warning "Một số sản phẩm đã hết hàng", chỉ các sản phẩm còn hàng được thêm vào giỏ hàng | | Pass | 11/15/2015 | |
| **FUNC-DL-03** | Đặt lại đơn hàng với giá đã thay đổi | 1. Truy cập /user/account/orders<br>2. Đơn hàng có sản phẩm giá đã thay đổi<br>3. Nhấn "Đặt lại" | Sản phẩm được thêm vào giỏ hàng với giá hiện tại, hiển thị thông báo về sự thay đổi giá (nếu có) | | Pass | 11/15/2015 | |
| **FUNC-DL-04** | Đặt lại đơn hàng từ trang chi tiết | 1. Truy cập /user/account/orders/[id]<br>2. Nhấn nút "Đặt lại" | Các sản phẩm từ đơn hàng được thêm vào giỏ hàng, chuyển đến trang /user/cart | | Pass | 11/15/2015 | |

### Function: Đánh giá đơn hàng

#### Check FUNC: Đánh giá đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DG-01** | Mở form đánh giá | 1. Truy cập /user/account/orders/[id]<br>2. Đơn hàng đã giao<br>3. Nhấn nút "Đánh giá" | Hiển thị Dialog/Modal với form đánh giá, có Star Rating cho mỗi sản phẩm, Textarea để viết nhận xét, Button "Gửi đánh giá" | | Pass | 11/15/2015 | |
| **FUNC-DG-02** | Đánh giá sản phẩm | 1. Mở form đánh giá<br>2. Chọn số sao cho sản phẩm<br>3. Viết nhận xét<br>4. Nhấn "Gửi đánh giá" | Hiển thị toast.success "Đánh giá đã được gửi thành công", đánh giá được lưu trữ, Dialog đóng lại | | Pass | 11/15/2015 | |
| **FUNC-DG-03** | Đánh giá nhiều sản phẩm | 1. Mở form đánh giá<br>2. Đơn hàng có nhiều sản phẩm<br>3. Đánh giá từng sản phẩm<br>4. Nhấn "Gửi đánh giá" | Tất cả đánh giá được lưu trữ, mỗi sản phẩm có đánh giá riêng | | Pass | 11/15/2015 | |
| **FUNC-DG-04** | Đánh giá dịch vụ | 1. Mở form đánh giá<br>2. Đánh giá tổng thể về dịch vụ<br>3. Nhấn "Gửi đánh giá" | Đánh giá dịch vụ được lưu trữ, phản hồi được gửi đến bộ phận liên quan | | Pass | 11/15/2015 | |
| **FUNC-DG-05** | Cập nhật điểm đánh giá sản phẩm | 1. Gửi đánh giá sản phẩm<br>2. Kiểm tra trang sản phẩm | Điểm đánh giá trung bình của sản phẩm được cập nhật, đánh giá được hiển thị trên trang sản phẩm | | Pass | 11/15/2015 | |

### Function: Hủy đơn hàng

#### Check FUNC: Hủy đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-HD-01** | Mở dialog hủy đơn hàng | 1. Truy cập /user/account/orders/[id]<br>2. Đơn hàng chưa giao<br>3. Nhấn nút "Hủy đơn" | Hiển thị Dialog với tiêu đề "Bạn có chắc chắn muốn hủy đơn hàng này?", Select chọn lý do hủy, Textarea ghi chú, Button "Xác nhận hủy đơn", Button "Hủy bỏ" | | Pass | 11/15/2015 | |
| **FUNC-HD-02** | Hủy đơn hàng thành công | 1. Mở dialog hủy đơn<br>2. Chọn lý do hủy<br>3. Nhập ghi chú (tùy chọn)<br>4. Nhấn "Xác nhận hủy đơn" | Hiển thị toast.success "Đơn hàng đã được hủy thành công", trạng thái đơn hàng được cập nhật thành "Đã hủy", Dialog đóng lại, nếu đã thanh toán thì hiển thị thông tin hoàn tiền | | Pass | 11/15/2015 | |
| **FUNC-HD-03** | Hủy đơn hàng đã giao | 1. Truy cập /user/account/orders/[id]<br>2. Đơn hàng đã giao<br>3. Kiểm tra nút "Hủy đơn" | Nút "Hủy đơn" bị ẩn hoặc disabled, không thể hủy đơn hàng đã giao | | Pass | 11/15/2015 | |
| **FUNC-HD-04** | Hủy đơn hàng đang giao | 1. Truy cập /user/account/orders/[id]<br>2. Đơn hàng đang giao<br>3. Kiểm tra nút "Hủy đơn" | Nút "Hủy đơn" bị ẩn hoặc disabled, hiển thị thông báo "Không thể hủy đơn hàng đang giao" | | Pass | 11/15/2015 | |
| **FUNC-HD-05** | Xử lý hoàn tiền khi hủy | 1. Hủy đơn hàng đã thanh toán<br>2. Kiểm tra | Hiển thị thông tin hoàn tiền: phương thức hoàn tiền, thời gian hoàn tiền dự kiến, hiển thị toast.info "Tiền sẽ được hoàn trong 3-5 ngày làm việc" | | Pass | 11/15/2015 | |
| **FUNC-HD-06** | Hủy bỏ dialog hủy đơn | 1. Mở dialog hủy đơn<br>2. Nhấn nút "Hủy bỏ" | Dialog đóng lại, đơn hàng không bị hủy, trạng thái không thay đổi | | Pass | 11/15/2015 | |

### Function: Theo dõi đơn hàng

#### Check FUNC: Theo dõi đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TD-01** | Mở trang theo dõi đơn hàng | 1. Truy cập /user/orders/track/[id] | Hiển thị trang với Timeline trạng thái, Trạng thái hiện tại, Vị trí hiện tại (nếu đang giao), Thời gian dự kiến, Thông tin vận chuyển, Bản đồ theo dõi (nếu có), Lịch sử cập nhật | | Pass | 11/15/2015 | |
| **FUNC-TD-02** | Hiển thị Timeline trạng thái | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra | Timeline hiển thị các mốc thời gian thay đổi trạng thái: Đặt hàng, Xác nhận, Đóng gói, Giao hàng, Đã giao, với icon và màu sắc tương ứng | | Pass | 11/15/2015 | |
| **FUNC-TD-03** | Hiển thị trạng thái hiện tại | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra | Hiển thị Badge trạng thái hiện tại của đơn hàng với màu sắc và text đúng | | Pass | 11/15/2015 | |
| **FUNC-TD-04** | Hiển thị vị trí hiện tại | 1. Truy cập /user/orders/track/[id]<br>2. Đơn hàng đang giao<br>3. Kiểm tra | Hiển thị vị trí hiện tại của đơn hàng (nếu đơn vị vận chuyển hỗ trợ), bản đồ hiển thị vị trí | | Pass | 11/15/2015 | |
| **FUNC-TD-05** | Hiển thị thời gian dự kiến | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra | Hiển thị thời gian dự kiến giao hàng dựa trên đơn vị vận chuyển và địa chỉ giao hàng | | Pass | 11/15/2015 | |
| **FUNC-TD-06** | Hiển thị thông tin vận chuyển | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra | Hiển thị thông tin: Đơn vị vận chuyển, Mã vận đơn, Số điện thoại liên hệ | | Pass | 11/15/2015 | |
| **FUNC-TD-07** | Cập nhật thời gian thực | 1. Truy cập /user/orders/track/[id]<br>2. Đợi cập nhật<br>3. Kiểm tra | Thông tin đơn hàng được cập nhật tự động theo thời gian thực, Timeline được cập nhật khi có thay đổi trạng thái | | Pass | 11/15/2015 | |
| **FUNC-TD-08** | Thông báo cập nhật | 1. Truy cập /user/orders/track/[id]<br>2. Có cập nhật mới<br>3. Kiểm tra | Hiển thị toast.info hoặc notification khi có cập nhật mới về trạng thái đơn hàng | | Pass | 11/15/2015 | |

### Function: Yêu cầu đổi/trả hàng

#### Check FUNC: Yêu cầu đổi/trả hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DT-01** | Mở form yêu cầu đổi trả | 1. Truy cập /user/account/orders/[id]<br>2. Đơn hàng đã giao<br>3. Nhấn nút "Đổi trả" | Hiển thị Dialog/Modal với form yêu cầu đổi trả, có Radio Group chọn loại yêu cầu (Đổi hàng, Trả hàng), Select chọn lý do, Textarea mô tả chi tiết, File Upload hình ảnh minh chứng, Input thông tin liên hệ, Button "Gửi yêu cầu đổi trả" | | Pass | 11/15/2015 | |
| **FUNC-DT-02** | Gửi yêu cầu đổi trả thành công | 1. Mở form yêu cầu đổi trả<br>2. Chọn loại yêu cầu<br>3. Chọn lý do<br>4. Nhập mô tả<br>5. Upload hình ảnh (tùy chọn)<br>6. Nhấn "Gửi yêu cầu đổi trả" | Hiển thị toast.success "Yêu cầu đổi trả đã được gửi thành công", Dialog đóng lại, yêu cầu được lưu trữ, nhân viên nhận được thông báo | | Pass | 11/15/2015 | |
| **FUNC-DT-03** | Kiểm tra điều kiện đổi trả | 1. Truy cập /user/account/orders/[id]<br>2. Đơn hàng chưa giao<br>3. Kiểm tra nút "Đổi trả" | Nút "Đổi trả" bị ẩn hoặc disabled, hiển thị thông báo "Chỉ có thể đổi trả đơn hàng đã giao" | | Pass | 11/15/2015 | |
| **FUNC-DT-04** | Kiểm tra thời gian đổi trả | 1. Truy cập /user/account/orders/[id]<br>2. Đơn hàng đã giao quá 30 ngày<br>3. Kiểm tra | Hiển thị thông báo "Đã quá thời hạn đổi trả (30 ngày)", nút "Đổi trả" bị disabled | | Pass | 11/15/2015 | |
| **FUNC-DT-05** | Chọn loại yêu cầu đổi hàng | 1. Mở form yêu cầu đổi trả<br>2. Chọn radio "Đổi hàng" | Form hiển thị các trường phù hợp với yêu cầu đổi hàng, có thể chọn sản phẩm muốn đổi | | Pass | 11/15/2015 | |
| **FUNC-DT-06** | Chọn loại yêu cầu trả hàng | 1. Mở form yêu cầu đổi trả<br>2. Chọn radio "Trả hàng" | Form hiển thị các trường phù hợp với yêu cầu trả hàng, có thể chọn sản phẩm muốn trả | | Pass | 11/15/2015 | |
| **FUNC-DT-07** | Upload hình ảnh minh chứng | 1. Mở form yêu cầu đổi trả<br>2. Click File Upload<br>3. Chọn hình ảnh | Hình ảnh được upload thành công, hiển thị preview hình ảnh, có thể xóa hình ảnh đã upload | | Pass | 11/15/2015 | |
| **FUNC-DT-08** | Gửi yêu cầu thiếu thông tin | 1. Mở form yêu cầu đổi trả<br>2. Không điền đầy đủ thông tin<br>3. Nhấn "Gửi yêu cầu đổi trả" | Hiển thị toast.error "Vui lòng điền đầy đủ thông tin", các trường bắt buộc được đánh dấu lỗi | | Pass | 11/15/2015 | |
| **FUNC-DT-09** | Theo dõi tiến trình đổi trả | 1. Gửi yêu cầu đổi trả<br>2. Truy cập trang theo dõi<br>3. Kiểm tra | Hiển thị tiến trình xử lý yêu cầu: Đã gửi, Đang xử lý, Đã chấp nhận/Từ chối, Đang xử lý đổi trả, Hoàn thành | | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn MDX để dễ dàng quản lý và cập nhật test cases.*

