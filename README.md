# Test Case Template - Xử lý đơn hàng (Nhân viên)

## Module Code
**Giao lộ 19: Họcl6c (Nhân viên)**

## Test Requirement
1. Tạo đơn hàng trực tiếp
2. Xử lý đơn hàng online
3. Tính toán giá
4. Xử lý thanh toán
5. In hóa đơn

---

## Test Summary

### Người lớp Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 45 |
| **Fail** | 0 |
| **Untested** | 0 |
| **N/A** | 0 |
| **Number of Test cases** | 45 |

---

## Test Cases

### Function: Xử lý đơn hàng online

#### Check GUI: Xử lý đơn hàng online

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XLDH-01** | Kiểm tra tiêu đề trang | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders<br>3. Kiểm tra tiêu đề | Hiển thị div space-y-6 với div flex items-center justify-between có h1 "Xử lý đơn hàng online" class text-2xl font-bold, p "Lọc, xem chi tiết và cập nhật trạng thái đơn" class text-sm text-muted-foreground, Button asChild Link href="/nhanvien/orders/new" "Tạo đơn hàng trực tiếp" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-XLDH-02** | Kiểm tra Alert lỗi | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders<br>3. Kiểm tra Alert | Hiển thị Alert variant="destructive" (nếu có lỗi) với icon AlertCircle h-4 w-4, AlertDescription chứa thông báo lỗi | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-XLDH-03** | Kiểm tra card Bộ lọc đơn hàng | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders<br>3. Kiểm tra card | Hiển thị Card với CardHeader có CardTitle "Bộ lọc đơn hàng", CardDescription "Trạng thái, thời gian, phương thức thanh toán, tìm kiếm", CardContent className="grid gap-4 md:grid-cols-6" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-XLDH-04** | Kiểm tra các bộ lọc | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders<br>3. Kiểm tra bộ lọc | Hiển thị: div grid gap-2 với Label "Trạng thái", Select value={status} onValueChange với SelectTrigger SelectValue placeholder="Tất cả", SelectContent có SelectItem (Tất cả, Chờ xác nhận, Đã xác nhận, Đang chuẩn bị, Đã giao, Đã hủy). div grid gap-2 với Label "Khoảng thời gian", Popover với PopoverTrigger là Button variant="outline" có icon CalendarIcon mr-2 h-4 w-4, PopoverContent với Calendar mode="range". div grid gap-2 với Label "Phương thức thanh toán", Select (Tất cả, COD, Banking, MoMo, ZaloPay, Viettel Money). div grid gap-2 md:col-span-2 với Label "Tìm kiếm", Input value={query} onChange placeholder="ID, tên, số điện thoại..." | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-XLDH-05** | Kiểm tra card Danh sách đơn hàng | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders<br>3. Kiểm tra card | Hiển thị Card với CardHeader có CardTitle "Danh sách đơn hàng", CardDescription "Các đơn đặt online", CardContent chứa Table | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-XLDH-06** | Kiểm tra bảng danh sách đơn hàng | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders<br>3. Kiểm tra bảng | Hiển thị Table với TableHeader có các TableHead: "ID đơn", "Khách hàng", "Sản phẩm", "Tổng tiền", "Trạng thái", "Ngày đặt", "Thao tác". TableBody có các TableRow với TableCell tương ứng | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-XLDH-07** | Kiểm tra cột ID đơn hàng | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders<br>3. Kiểm tra cột | Mỗi hàng có TableCell chứa Link href="/nhanvien/orders/[id]" className="text-primary hover:underline" (order.id) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-XLDH-08** | Kiểm tra cột Khách hàng | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders<br>3. Kiểm tra cột | Mỗi hàng có TableCell chứa div text-sm font-medium (customer.name), div text-xs text-muted-foreground (customer.phone + " • " + customer.email) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-XLDH-09** | Kiểm tra cột Trạng thái | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders<br>3. Kiểm tra cột | Mỗi hàng có TableCell chứa Badge với variant="destructive" nếu status="Chờ xác nhận", variant="default" nếu status="Đã xác nhận", variant="outline" cho các trạng thái khác | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-XLDH-10** | Kiểm tra cột Thao tác | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders<br>3. Kiểm tra cột | Mỗi hàng có TableCell className="space-x-2" chứa Button size="sm" variant="outline" asChild Link href="/nhanvien/orders/[id]" "Xem chi tiết", Button size="sm" onClick={handleConfirmOrder} disabled={isProcessing} "Xác nhận" hoặc "Đang xử lý...", Button size="sm" variant="destructive" onClick={handleCancelOrder} disabled={isProcessing} "Hủy" | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Xử lý đơn hàng online

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XLDH-01** | Xem danh sách đơn hàng online | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders | Hiển thị đầy đủ: tiêu đề "Xử lý đơn hàng online" và mô tả, nút "Tạo đơn hàng trực tiếp", Alert lỗi (nếu có), card Bộ lọc đơn hàng với đầy đủ các bộ lọc (Trạng thái, Khoảng thời gian với Calendar, Phương thức thanh toán, Tìm kiếm), card Danh sách đơn hàng với Table hiển thị các đơn hàng, mỗi hàng có ID đơn (Link), Khách hàng (tên, phone, email), Sản phẩm (danh sách items), Tổng tiền (format VNĐ), Trạng thái (Badge), Ngày đặt, các nút thao tác (Xem chi tiết, Xác nhận, Hủy) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-XLDH-02** | Lọc đơn hàng theo trạng thái | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders<br>3. Chọn trạng thái từ Select (VD: "Chờ xác nhận") | Danh sách đơn hàng được lọc theo trạng thái đã chọn, chỉ hiển thị các đơn hàng có trạng thái "Chờ xác nhận", Badge màu đỏ (variant="destructive") | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-XLDH-03** | Lọc đơn hàng theo khoảng thời gian | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders<br>3. Click Button "Khoảng thời gian"<br>4. Chọn ngày bắt đầu và ngày kết thúc trong Calendar<br>5. Đóng Popover | Danh sách đơn hàng được lọc theo khoảng thời gian đã chọn, chỉ hiển thị các đơn hàng có ngày đặt trong khoảng thời gian đó, Button hiển thị "DD/MM/YYYY - DD/MM/YYYY" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-XLDH-04** | Lọc đơn hàng theo phương thức thanh toán | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders<br>3. Chọn phương thức thanh toán từ Select (VD: "COD") | Danh sách đơn hàng được lọc theo phương thức thanh toán đã chọn, chỉ hiển thị các đơn hàng có phương thức thanh toán "COD" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-XLDH-05** | Tìm kiếm đơn hàng | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders<br>3. Nhập từ khóa vào Input (VD: ID đơn hàng, tên khách hàng, số điện thoại) | Danh sách đơn hàng được lọc theo từ khóa, chỉ hiển thị các đơn hàng có ID, tên khách hàng, hoặc số điện thoại chứa từ khóa, tìm kiếm không phân biệt hoa thường | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-XLDH-06** | Xem chi tiết đơn hàng | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders<br>3. Click Link ID đơn hàng hoặc nút "Xem chi tiết" | Chuyển đến trang /nhanvien/orders/[id], hiển thị chi tiết đơn hàng với đầy đủ thông tin | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-XLDH-07** | Xác nhận đơn hàng thành công | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders<br>3. Click nút "Xác nhận" trên một đơn hàng có trạng thái "Chờ xác nhận" | Hiển thị thông báo thành công "Đã xác nhận đơn hàng [orderId]" (toast success), trạng thái đơn hàng cập nhật thành "Đã xác nhận" với Badge màu xanh (variant="default"), nút "Xác nhận" có thể bị ẩn hoặc disabled, lịch sử xử lý được ghi lại, khách hàng nhận được thông báo xác nhận | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-XLDH-08** | Xác nhận đơn hàng thất bại | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders<br>3. Click nút "Xác nhận"<br>4. Giả lập lỗi (VD: không đủ tồn kho) | Hiển thị Alert variant="destructive" với thông báo lỗi (VD: "Lỗi database. Không thể cập nhật đơn hàng."), hiển thị toast error, trạng thái đơn hàng không thay đổi, nút "Xác nhận" vẫn hoạt động | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-XLDH-09** | Hủy đơn hàng thành công | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders<br>3. Click nút "Hủy" trên một đơn hàng<br>4. Xác nhận hủy trong Dialog | Hiển thị Dialog hủy đơn hàng (xem chi tiết ở FUNC-XLDH-10), sau khi xác nhận: hiển thị thông báo thành công "Đã hủy đơn hàng [orderId]" (toast success), trạng thái đơn hàng cập nhật thành "Đã hủy" với Badge màu xám (variant="outline"), hoàn tiền cho khách hàng nếu đã thanh toán, khách hàng nhận được thông báo hủy đơn hàng | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-XLDH-10** | Dialog hủy đơn hàng | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders/[id]<br>3. Click nút "Hủy đơn hàng" | Hiển thị Dialog với DialogTitle "Hủy đơn hàng #[id]", DialogDescription, RadioGroup "Lý do hủy" với các option (Không thể vận chuyển, Kho không đủ hàng, Phương thức TT không khả dụng, Sản phẩm hết hàng/ngừng kinh doanh, Khách hàng yêu cầu, Khách hàng không phản hồi, Khác), Textarea "Mô tả chi tiết", Select "Hoàn tiền", Textarea "Giải pháp đề xuất", Textarea "Thông báo khách hàng", DialogFooter có Button "Đóng" và Button variant="destructive" "Xác nhận hủy" | FUNC-DN-02, FUNC-XLDH-06 | Pass | 11/15/2015 | |
| **FUNC-XLDH-11** | Tạo đơn hàng trực tiếp | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders<br>3. Click nút "Tạo đơn hàng trực tiếp" | Chuyển đến trang /nhanvien/orders/new, hiển thị form tạo đơn hàng trực tiếp | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Chi tiết đơn hàng online

#### Check GUI: Chi tiết đơn hàng online

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CTDH-01** | Kiểm tra tiêu đề trang | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders/[id]<br>3. Kiểm tra tiêu đề | Hiển thị div space-y-6 với h1 "Chi tiết đơn hàng online" class text-2xl font-bold, p "Xem và cập nhật trạng thái các đơn hàng online đã đặt từ khách hàng" class text-sm text-muted-foreground | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-CTDH-02** | Kiểm tra tổng quan nhanh | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders/[id]<br>3. Kiểm tra tổng quan | Hiển thị div grid grid-cols-2 md:grid-cols-5 gap-4 với 5 Card: Card "ID đơn hàng" với CardContent p-4 có div text-sm text-muted-foreground "ID đơn hàng", div text-xl font-semibold "#ORD001". Card "Trạng thái" với Badge variant="destructive" "Chờ xác nhận". Card "PT thanh toán" với "COD". Card "Ngày đặt" với "2023-10-26 10:30". Card "Nhân viên xử lý" với "Nhân viên B" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-CTDH-03** | Kiểm tra card Khách hàng & Giao hàng | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders/[id]<br>3. Kiểm tra card | Hiển thị Card với CardHeader có CardTitle "Khách hàng & Giao hàng", CardDescription "Thông tin người đặt và địa chỉ nhận", CardContent className="grid md:grid-cols-2 gap-4 text-sm" với div font-medium (tên khách hàng), div text-muted-foreground (email), div text-muted-foreground (phone + " • Hạng: " + rank), div font-medium "Địa chỉ giao", div text-muted-foreground (địa chỉ) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-CTDH-04** | Kiểm tra card Sản phẩm đặt | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders/[id]<br>3. Kiểm tra card | Hiển thị Card với CardHeader có CardTitle "Sản phẩm đặt", CardDescription "Danh sách sách và tồn kho", CardContent chứa Table với TableHeader có TableHead: "Tên sách", "SL yêu cầu" className="text-right", "Tồn kho hiện tại" className="text-right", "Cần nhập thêm" className="text-right" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-CTDH-05** | Kiểm tra các nút hành động | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders/[id]<br>3. Kiểm tra nút | Hiển thị div flex flex-wrap gap-2 với Button variant="outline" onClick "Cập nhật trạng thái", Button onClick "Xác nhận đơn hàng", Button variant="destructive" onClick "Hủy đơn hàng", Button variant="outline" asChild Link href="/nhanvien/orders/[id]/payment" "Xử lý thanh toán", Button variant="outline" asChild Link href="/nhanvien/orders/[id]/invoice" "In hóa đơn" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-CTDH-06** | Kiểm tra card Lịch sử thay đổi | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders/[id]<br>3. Kiểm tra card | Hiển thị Card với CardHeader có CardTitle "Lịch sử thay đổi", CardContent className="space-y-2 text-sm" với các div chứa thông tin (thời gian, người xử lý, ghi chú) | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Chi tiết đơn hàng online

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CTDH-01** | Xem chi tiết đơn hàng | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders/[id] | Hiển thị đầy đủ: tiêu đề "Chi tiết đơn hàng online" và mô tả, tổng quan nhanh 5 card (ID đơn hàng, Trạng thái Badge, PT thanh toán, Ngày đặt, Nhân viên xử lý), card Khách hàng & Giao hàng với thông tin khách hàng (tên, email, phone, hạng) và địa chỉ giao, card Sản phẩm đặt với Table hiển thị tên sách, số lượng yêu cầu, tồn kho hiện tại, Badge "Cần nhập thêm" (variant="destructive" nếu cần, variant="secondary" nếu không), các nút hành động, card Lịch sử thay đổi với các thay đổi trạng thái | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-CTDH-02** | Cập nhật trạng thái đơn hàng | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders/[id]<br>3. Click nút "Cập nhật trạng thái"<br>4. Chọn trạng thái mới trong Dialog<br>5. Nhập lý do và ghi chú<br>6. Click "Lưu" | Hiển thị Dialog với DialogTitle "Cập nhật trạng thái đơn hàng #[id]", DialogDescription, Badge "Trạng thái hiện tại", RadioGroup "Trạng thái mới" với các option (Chờ xác nhận, Đang chuẩn bị, Đang giao, Đã giao, Đã hủy), Textarea "Lý do thay đổi (bắt buộc nếu hủy)", Textarea "Ghi chú nội bộ", Select "Gửi thông báo" (Có/Không), DialogFooter có Button "Hủy" và "Lưu". Sau khi lưu: trạng thái đơn hàng được cập nhật, Badge trong tổng quan nhanh được cập nhật, lịch sử thay đổi được ghi lại, khách hàng nhận được thông báo (nếu chọn "Có"), dialog đóng lại | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-CTDH-03** | Xác nhận đơn hàng từ chi tiết | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders/[id]<br>3. Click nút "Xác nhận đơn hàng"<br>4. Kiểm tra tồn kho trong Dialog<br>5. Click "Xác nhận" | Hiển thị Dialog với DialogTitle "Xác nhận đơn hàng #[id]", DialogDescription "Kiểm tra tồn kho và xác nhận", thông tin khách hàng và PT thanh toán, địa chỉ giao hàng, bảng sản phẩm với cột (Tên sách, Yêu cầu, Tồn kho), Textarea "Lý do từ chối (nếu cần)", DialogFooter có Button "Hủy", Button variant="destructive" "Từ chối", Button "Xác nhận". Sau khi xác nhận: đơn hàng được xác nhận thành công, trạng thái cập nhật thành "Đã xác nhận", khách hàng nhận được thông báo, dialog đóng lại | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-CTDH-04** | Từ chối đơn hàng | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders/[id]<br>3. Click nút "Xác nhận đơn hàng"<br>4. Nhập lý do từ chối vào Textarea<br>5. Click "Từ chối" | Đơn hàng bị từ chối, hiển thị thông báo thành công (toast success), trạng thái có thể cập nhật thành "Đã hủy" hoặc "Từ chối", khách hàng nhận được thông báo từ chối với lý do, dialog đóng lại | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-CTDH-05** | Xử lý thanh toán | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders/[id]<br>3. Click nút "Xử lý thanh toán" | Chuyển đến trang /nhanvien/orders/[id]/payment, hiển thị form xử lý thanh toán | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-CTDH-06** | In hóa đơn | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders/[id]<br>3. Click nút "In hóa đơn" | Chuyển đến trang /nhanvien/orders/[id]/invoice, hiển thị hóa đơn với đầy đủ thông tin, có thể in hoặc lưu PDF | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Tạo đơn hàng trực tiếp

#### Check FUNC: Tạo đơn hàng trực tiếp

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TDH-01** | Tạo đơn hàng trực tiếp thành công | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders/new<br>3. Nhập thông tin khách hàng (họ tên, số điện thoại, email, địa chỉ)<br>4. Tìm kiếm và thêm sản phẩm vào đơn hàng<br>5. Cập nhật số lượng sản phẩm<br>6. Chọn phương thức thanh toán<br>7. Nhập ghi chú (nếu có)<br>8. Click "Tạo đơn hàng" | Đơn hàng được tạo thành công, hiển thị thông báo thành công "Đã tạo đơn hàng thành công" (toast success), thông tin khách hàng được lưu trữ, tồn kho được cập nhật, hóa đơn được tạo, chuyển đến trang chi tiết đơn hàng hoặc trang thanh toán | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TDH-02** | Thêm sản phẩm vào đơn hàng | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders/new<br>3. Tìm kiếm sản phẩm theo tên, tác giả hoặc mã sách<br>4. Click "Thêm vào đơn hàng" | Sản phẩm được thêm vào đơn hàng, tồn kho được kiểm tra trước khi thêm, hiển thị cảnh báo nếu sản phẩm hết hàng hoặc sắp hết hàng, tổng tiền đơn hàng được cập nhật, sản phẩm xuất hiện trong danh sách sản phẩm của đơn hàng | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TDH-03** | Cập nhật số lượng sản phẩm | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders/new<br>3. Thay đổi số lượng sản phẩm trong đơn hàng<br>4. Kiểm tra tồn kho | Số lượng sản phẩm được cập nhật, kiểm tra tồn kho khi tăng số lượng, hiển thị cảnh báo nếu số lượng vượt quá tồn kho, thành tiền của sản phẩm được tính lại (Giá × Số lượng), tổng tiền đơn hàng được cập nhật | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TDH-04** | Xóa sản phẩm khỏi đơn hàng | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders/new<br>3. Click nút "Xóa" trên một sản phẩm<br>4. Xác nhận xóa | Hiển thị Dialog xác nhận xóa, sau khi xác nhận: sản phẩm được xóa khỏi đơn hàng, tổng tiền đơn hàng được cập nhật, hiển thị thông báo xác nhận (toast success) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TDH-05** | Tính toán giá đơn hàng | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders/new<br>3. Thêm sản phẩm vào đơn hàng<br>4. Áp dụng giảm giá (nếu có) | Tổng tiền đơn hàng được tính tự động: Tạm tính = tổng giá sản phẩm, Giảm giá = giảm giá sản phẩm + giảm giá đơn hàng + giảm giá theo rank khách hàng + mã giảm giá, Thuế VAT = 10% × (Tạm tính - Giảm giá), Tổng cộng = Tạm tính - Giảm giá + Thuế VAT, chi tiết tính toán được hiển thị trong bảng, cập nhật real-time khi thay đổi | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TDH-06** | Áp dụng mã giảm giá | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders/new<br>3. Nhập mã giảm giá vào Input<br>4. Click "Áp dụng mã giảm giá" | Mã giảm giá được kiểm tra tính hợp lệ, kiểm tra điều kiện áp dụng mã, giảm giá được áp dụng theo quy định của mã, tổng tiền đơn hàng được cập nhật, hiển thị thông báo thành công "Đã áp dụng mã giảm giá" (toast success) hoặc lỗi "Mã giảm giá không hợp lệ" (toast error) | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Xử lý thanh toán

#### Check FUNC: Xử lý thanh toán

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TT-01** | Thanh toán tiền mặt | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders/[id]/payment<br>3. Chọn "Tiền mặt"<br>4. Nhập số tiền khách hàng đưa<br>5. Click "Xác nhận thanh toán" | Số tiền thối lại được tính tự động (Số tiền nhận - Tổng cộng), hiển thị số tiền thối trong Text hoặc Alert, thanh toán được xác nhận thành công, hiển thị thông báo thành công (toast success), hóa đơn được tạo, trạng thái đơn hàng cập nhật thành "Đã thanh toán", lịch sử thanh toán được ghi lại | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TT-02** | Thanh toán tiền mặt thiếu tiền | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders/[id]/payment<br>3. Chọn "Tiền mặt"<br>4. Nhập số tiền nhỏ hơn tổng cộng<br>5. Click "Xác nhận thanh toán" | Hiển thị thông báo lỗi "Số tiền nhận không đủ. Còn thiếu [số tiền] VNĐ" (toast error), không xác nhận thanh toán, số tiền thối hiển thị màu đỏ hoặc cảnh báo | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TT-03** | Thanh toán thẻ | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders/[id]/payment<br>3. Chọn "Thẻ"<br>4. Chọn loại thẻ từ Dropdown<br>5. Nhập 4 số cuối của thẻ<br>6. Nhập ngày hết hạn<br>7. Click "Xác nhận thanh toán" | Kết nối với hệ thống thanh toán, thanh toán được xử lý thành công, hiển thị thông báo thành công (toast success), hóa đơn được tạo, trạng thái đơn hàng cập nhật, lịch sử thanh toán được ghi lại | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TT-04** | Thanh toán chuyển khoản | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders/[id]/payment<br>3. Chọn "Chuyển khoản"<br>4. Xem thông tin tài khoản nhận tiền<br>5. Xác nhận đã nhận được tiền<br>6. Click "Xác nhận chuyển khoản" | Hiển thị thông tin tài khoản nhận tiền (số tài khoản, tên ngân hàng, số tiền, nội dung chuyển khoản), sau khi xác nhận: thanh toán được ghi nhận, hiển thị thông báo thành công (toast success), trạng thái đơn hàng cập nhật, lịch sử thanh toán được ghi lại | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TT-05** | Thanh toán ví điện tử | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders/[id]/payment<br>3. Chọn loại ví từ Dropdown (VD: "MoMo")<br>4. Xem mã QR thanh toán<br>5. Xác nhận thanh toán thành công<br>6. Click "Xác nhận thanh toán" | Hiển thị mã QR thanh toán (Image), sau khi xác nhận: thanh toán được ghi nhận, hiển thị thông báo thành công (toast success), trạng thái đơn hàng cập nhật, lịch sử thanh toán được ghi lại | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: In hóa đơn

#### Check FUNC: In hóa đơn

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-HD-01** | In hóa đơn | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders/[id]/invoice<br>3. Click nút "In hóa đơn" | Hóa đơn được in thành công, hiển thị đầy đủ thông tin: thông tin cửa hàng (tên, địa chỉ, số điện thoại, email, mã số thuế), thông tin đơn hàng (số hóa đơn, ngày bán, nhân viên bán, phương thức thanh toán), thông tin khách hàng (tên, số điện thoại, email, địa chỉ), chi tiết sản phẩm Table (STT, tên sản phẩm, số lượng, đơn giá, thành tiền), tổng kết hóa đơn (Tạm tính, Giảm giá, Thuế VAT, Tổng cộng), định dạng chuyên nghiệp và dễ đọc, bản sao hóa đơn được lưu trong hệ thống | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-HD-02** | Lưu hóa đơn PDF | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders/[id]/invoice<br>3. Click nút "Lưu PDF" | File PDF hóa đơn được tạo thành công, tên file theo số hóa đơn (VD: "INV-001.pdf"), file được lưu vào thư mục quy định hoặc tải xuống, hóa đơn PDF được gửi qua email cho khách hàng (nếu có email), hiển thị thông báo thành công "Đã lưu hóa đơn PDF" (toast success) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-HD-03** | Gửi hóa đơn qua email | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/orders/[id]/invoice<br>3. Click nút "Gửi email" | Email hóa đơn được gửi thành công, địa chỉ email khách hàng được điền tự động, file PDF hóa đơn được đính kèm, email có nội dung chuyên nghiệp, hiển thị thông báo thành công "Đã gửi hóa đơn qua email" (toast success), khách hàng nhận được email | FUNC-DN-02 | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn MDX để dễ dàng quản lý và cập nhật test cases.*

