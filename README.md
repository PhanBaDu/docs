# Test Case Template - Quản lý đơn hàng (Admin)

## Module Code
**Giao lộ 19: Họcl6c (Admin)**

## Test Requirement
1. Hiển thị danh sách đơn hàng
2. Xem chi tiết đơn hàng
3. Cập nhật trạng thái đơn hàng
4. Xác nhận đơn hàng
5. Hủy đơn hàng
6. In đơn hàng

---

## Test Summary

### Người lớp Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 25 |
| **Fail** | 0 |
| **Untested** | 0 |
| **N/A** | 0 |
| **Number of Test cases** | 25 |

---

## Test Cases

### Function: Hiển thị danh sách đơn hàng

#### Check GUI: Hiển thị danh sách đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DSDH-01** | Kiểm tra tiêu đề trang | 1. Đăng nhập Admin<br>2. Truy cập /admin/orders<br>3. Kiểm tra tiêu đề | Hiển thị tiêu đề "Quản lý đơn hàng" với class text-3xl font-bold, mô tả "Xử lý và theo dõi tất cả đơn hàng" với class text-muted-foreground, nằm trong div flex items-center justify-between | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSDH-02** | Kiểm tra thống kê đơn hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/orders<br>3. Kiểm tra thống kê | Hiển thị grid grid-cols-1 md:grid-cols-5 gap-4 với 5 Card: Card "Chờ xác nhận" với icon Package trong vòng tròn bg-primary/10, Card "Đã xác nhận" với icon CheckCircle, Card "Đang giao" với icon Truck, Card "Đã giao" với icon CheckCircle, Card "Đã hủy" với icon XCircle. Mỗi card có CardContent p-4 với text-sm text-muted-foreground cho label và text-2xl font-bold cho số (count) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSDH-03** | Kiểm tra các nút header | 1. Đăng nhập Admin<br>2. Truy cập /admin/orders<br>3. Kiểm tra nút | Hiển thị div flex items-center gap-2 bên phải tiêu đề với Button variant="outline" "In báo cáo" có icon Printer h-4 w-4 mr-2, Button variant="outline" "Bộ lọc nâng cao" có icon Filter h-4 w-4 mr-2 | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSDH-04** | Kiểm tra card Bộ lọc | 1. Đăng nhập Admin<br>2. Truy cập /admin/orders<br>3. Kiểm tra card bộ lọc | Hiển thị Card với CardContent p-4, có div flex items-center gap-4 chứa: Input tìm kiếm với icon Search absolute left-3, placeholder="Tìm kiếm đơn hàng, khách hàng...", Select Trạng thái w-40 với các option có count trong ngoặc, Select Phương thức thanh toán w-40, 2 Input type="date" cho khoảng thời gian, Button variant="outline" "Áp dụng" có icon Filter | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSDH-05** | Kiểm tra card Danh sách đơn hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/orders<br>3. Kiểm tra card | Hiển thị Card với CardHeader có CardTitle "Danh sách đơn hàng", CardDescription "Quản lý và xử lý tất cả đơn hàng", CardContent chứa Table | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSDH-06** | Kiểm tra bảng danh sách đơn hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/orders<br>3. Kiểm tra bảng | Hiển thị Table với TableHeader có các TableHead: "Mã đơn hàng", "Khách hàng", "Sản phẩm", "Tổng tiền", "Thanh toán", "Trạng thái", "Ngày tạo", "Thao tác" (w-24). TableBody có các TableRow với TableCell tương ứng | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSDH-07** | Kiểm tra cột Mã đơn hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/orders<br>3. Kiểm tra cột | Mỗi hàng có TableCell chứa div với p font-medium (mã đơn hàng, VD: ORD001) và p text-sm text-muted-foreground (ngày tạo) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSDH-08** | Kiểm tra cột Khách hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/orders<br>3. Kiểm tra cột | Mỗi hàng có TableCell chứa div với p font-medium (tên khách hàng), p text-sm text-muted-foreground (email), p text-sm text-muted-foreground (số điện thoại) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSDH-09** | Kiểm tra cột Sản phẩm | 1. Đăng nhập Admin<br>2. Truy cập /admin/orders<br>3. Kiểm tra cột | Mỗi hàng có TableCell chứa div với p font-medium "[số] sản phẩm" và p text-sm text-muted-foreground (địa chỉ giao hàng) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSDH-10** | Kiểm tra cột Trạng thái | 1. Đăng nhập Admin<br>2. Truy cập /admin/orders<br>3. Kiểm tra cột | Mỗi hàng có TableCell chứa Badge với variant tương ứng (destructive cho pending "Chờ xác nhận" với icon Package, default cho confirmed "Đã xác nhận" với icon CheckCircle, secondary cho shipping "Đang giao" với icon Truck, outline cho delivered "Đã giao" với icon CheckCircle, destructive cho cancelled "Đã hủy" với icon XCircle), bên trong có div flex items-center gap-1 với icon và label | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSDH-11** | Kiểm tra các nút thao tác | 1. Đăng nhập Admin<br>2. Truy cập /admin/orders<br>3. Kiểm tra nút thao tác | Mỗi hàng có TableCell "Thao tác" với div flex items-center gap-1 chứa: Button variant="ghost" size="sm" với Link href="/admin/orders/[id]" và icon Eye, Button variant="ghost" size="sm" với Link href="/admin/orders/[id]/update-status" và icon Edit, Button variant="ghost" size="sm" với icon Printer onClick mở modal, Button variant="ghost" size="sm" với icon AlertTriangle màu đỏ onClick mở modal hủy (chỉ hiển thị nếu status không phải cancelled và delivered) | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Hiển thị danh sách đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DSDH-01** | Xem danh sách đơn hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/orders | Hiển thị đầy đủ: thống kê 5 card (Chờ xác nhận: 12, Đã xác nhận: 8, Đang giao: 15, Đã giao: 120, Đã hủy: 1) với số liệu và icon, card Bộ lọc với ô tìm kiếm, 2 dropdown (Trạng thái, Phương thức thanh toán), 2 input date, nút Áp dụng, card Danh sách đơn hàng với Table hiển thị các đơn hàng, mỗi hàng có Mã đơn hàng (với ngày tạo), Khách hàng (tên, email, SĐT), Sản phẩm (số lượng + địa chỉ), Tổng tiền (toLocaleString), Thanh toán (Badge), Trạng thái (Badge với icon), Ngày tạo, các nút thao tác, phân trang | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSDH-02** | Tìm kiếm đơn hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/orders<br>3. Nhập từ khóa tìm kiếm vào ô "Tìm kiếm đơn hàng, khách hàng..."<br>4. Click nút "Áp dụng" | Danh sách đơn hàng được lọc theo từ khóa (mã đơn hàng, tên khách hàng, email, số điện thoại), bảng cập nhật với các đơn hàng phù hợp | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSDH-03** | Lọc đơn hàng theo trạng thái | 1. Đăng nhập Admin<br>2. Truy cập /admin/orders<br>3. Chọn trạng thái từ dropdown (VD: "Chờ xác nhận")<br>4. Click nút "Áp dụng" | Danh sách đơn hàng được lọc theo trạng thái đã chọn, bảng chỉ hiển thị đơn hàng có trạng thái tương ứng, thống kê có thể cập nhật | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSDH-04** | Lọc đơn hàng theo phương thức thanh toán | 1. Đăng nhập Admin<br>2. Truy cập /admin/orders<br>3. Chọn phương thức thanh toán từ dropdown (VD: "COD")<br>4. Click nút "Áp dụng" | Danh sách đơn hàng được lọc theo phương thức thanh toán đã chọn, bảng chỉ hiển thị đơn hàng có phương thức thanh toán tương ứng | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSDH-05** | Lọc đơn hàng theo khoảng thời gian | 1. Đăng nhập Admin<br>2. Truy cập /admin/orders<br>3. Chọn ngày bắt đầu và ngày kết thúc<br>4. Click nút "Áp dụng" | Danh sách đơn hàng được lọc theo khoảng thời gian tạo đơn hàng, bảng chỉ hiển thị đơn hàng được tạo trong khoảng thời gian đã chọn | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSDH-06** | Kết hợp nhiều bộ lọc | 1. Đăng nhập Admin<br>2. Truy cập /admin/orders<br>3. Chọn trạng thái "Chờ xác nhận"<br>4. Chọn phương thức thanh toán "COD"<br>5. Nhập từ khóa tìm kiếm<br>6. Click nút "Áp dụng" | Danh sách đơn hàng được lọc theo tất cả các tiêu chí đã chọn, bảng chỉ hiển thị đơn hàng thỏa mãn tất cả điều kiện | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Xem chi tiết đơn hàng

#### Check GUI: Xem chi tiết đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CTDH-01** | Kiểm tra tiêu đề trang | 1. Đăng nhập Admin<br>2. Truy cập /admin/orders/[id]<br>3. Kiểm tra tiêu đề | Hiển thị tiêu đề "Chi tiết đơn hàng - [Mã đơn hàng]" hoặc "Chi tiết đơn hàng - ORD001" với class text-2xl font-bold, layout tương tự trang chi tiết nhân viên | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-CTDH-02** | Kiểm tra thông tin đơn hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/orders/[id]<br>3. Kiểm tra thông tin | Hiển thị Card với CardHeader có CardTitle "Thông tin đơn hàng", CardContent có grid layout, hiển thị các trường: Mã đơn hàng, Ngày tạo, Ngày cập nhật, Trạng thái (Badge với icon), Phương thức thanh toán (Badge), Tổng tiền | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-CTDH-03** | Kiểm tra thông tin khách hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/orders/[id]<br>3. Kiểm tra thông tin | Hiển thị Card với CardHeader có CardTitle "Thông tin khách hàng", CardContent hiển thị các trường: Tên khách hàng, Email, Số điện thoại, Link đến trang chi tiết khách hàng | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-CTDH-04** | Kiểm tra danh sách sản phẩm | 1. Đăng nhập Admin<br>2. Truy cập /admin/orders/[id]<br>3. Kiểm tra danh sách | Hiển thị Card với CardHeader có CardTitle "Danh sách sản phẩm", CardContent có Table với các cột: Tên sản phẩm, Số lượng, Đơn giá, Thành tiền | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-CTDH-05** | Kiểm tra thông tin giao hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/orders/[id]<br>3. Kiểm tra thông tin | Hiển thị Card với CardHeader có CardTitle "Thông tin giao hàng", CardContent hiển thị các trường: Địa chỉ giao hàng, Phương thức vận chuyển, Mã vận đơn (trackingNumber), Trạng thái vận chuyển | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Xem chi tiết đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CTDH-01** | Xem chi tiết đơn hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/orders<br>3. Click nút Eye icon hoặc Link href="/admin/orders/[id]" | Hiển thị đầy đủ thông tin: tiêu đề "Chi tiết đơn hàng - [Mã]", card Thông tin đơn hàng với đầy đủ các trường (Mã đơn hàng, Ngày tạo, Ngày cập nhật, Trạng thái với Badge và icon, Phương thức thanh toán, Tổng tiền), card Thông tin khách hàng, card Danh sách sản phẩm với Table, card Thông tin giao hàng, các nút thao tác (Cập nhật trạng thái, In đơn hàng, Hủy đơn hàng nếu có thể) | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Cập nhật trạng thái đơn hàng

#### Check FUNC: Cập nhật trạng thái đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-STDH-01** | Cập nhật trạng thái đơn hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/orders/[id]/update-status<br>3. Chọn trạng thái mới từ Select<br>4. Nhập ghi chú (nếu có)<br>5. Click "Lưu" | Hiển thị form hoặc Dialog với Select trạng thái (pending, confirmed, shipping, delivered, cancelled), có thể có Textarea ghi chú. Sau khi lưu: trạng thái đơn hàng được cập nhật thành công, hiển thị thông báo thành công (toast success), Badge trạng thái được cập nhật với icon và màu tương ứng, thông báo được gửi cho khách hàng qua email/SMS về việc thay đổi trạng thái, lịch sử thay đổi được ghi nhận | FUNC-DN-02, FUNC-CTDH-01 | Pass | 11/15/2015 | |
| **FUNC-STDH-02** | Cập nhật trạng thái không hợp lệ | 1. Đăng nhập Admin<br>2. Truy cập /admin/orders/[id]/update-status<br>3. Chọn trạng thái không hợp lệ (VD: từ "delivered" về "pending")<br>4. Click "Lưu" | Hiển thị thông báo lỗi "Không thể chuyển từ trạng thái [trạng thái cũ] sang [trạng thái mới]" (toast error), không cập nhật trạng thái | FUNC-DN-02, FUNC-CTDH-01 | Pass | 11/15/2015 | |

---

### Function: Xác nhận đơn hàng

#### Check FUNC: Xác nhận đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XNDH-01** | Xác nhận đơn hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/orders/[id]<br>3. Click nút "Xác nhận đơn hàng" hoặc cập nhật trạng thái sang "confirmed"<br>4. Xác nhận | Đơn hàng được xác nhận thành công, hiển thị thông báo thành công (toast success), trạng thái cập nhật thành "Đã xác nhận" với Badge variant="default" và icon CheckCircle, thông báo được gửi cho khách hàng qua email/SMS về việc đơn hàng đã được xác nhận, tồn kho có thể được trừ (nếu cần), lịch sử được ghi nhận | FUNC-DN-02, FUNC-CTDH-01 | Pass | 11/15/2015 | |

---

### Function: Hủy đơn hàng

#### Check FUNC: Hủy đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-HDH-01** | Hủy đơn hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/orders<br>3. Click nút AlertTriangle icon (màu đỏ) trên một đơn hàng có thể hủy<br>4. Nhập lý do hủy vào Textarea<br>5. Click "Xác nhận hủy" | Hiển thị CancelOrderModal với DialogTitle "Hủy đơn hàng", có Textarea placeholder="Nhập lý do hủy đơn hàng..." required, có nút "Hủy" và "Xác nhận hủy" variant="destructive". Sau khi xác nhận: đơn hàng được hủy thành công, hiển thị thông báo thành công (toast success), trạng thái cập nhật thành "Đã hủy" với Badge variant="destructive" và icon XCircle, thông báo được gửi cho khách hàng qua email/SMS về việc đơn hàng bị hủy và lý do, hoàn tiền (nếu đã thanh toán qua Banking/Credit Card/E-wallet), tồn kho được hoàn trả (nếu đã trừ), modal đóng, bảng được refresh | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-HDH-02** | Hủy đơn hàng thiếu lý do | 1. Đăng nhập Admin<br>2. Truy cập /admin/orders<br>3. Click nút AlertTriangle icon<br>4. Để trống lý do hủy<br>5. Click "Xác nhận hủy" | Hiển thị thông báo lỗi "Vui lòng nhập lý do hủy đơn hàng" (toast error), không hủy đơn hàng, modal vẫn mở | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-HDH-03** | Hủy đơn hàng đã giao | 1. Đăng nhập Admin<br>2. Truy cập /admin/orders<br>3. Tìm đơn hàng có trạng thái "delivered"<br>4. Kiểm tra nút hủy | Nút AlertTriangle icon không hiển thị hoặc disabled, không thể hủy đơn hàng đã giao | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-HDH-04** | Hủy hủy đơn hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/orders<br>3. Click nút AlertTriangle icon<br>4. Nhập lý do<br>5. Click "Hủy" trong modal | Modal đóng lại, không hủy đơn hàng, trạng thái không thay đổi | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: In đơn hàng

#### Check FUNC: In đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-IDH-01** | In đơn hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/orders<br>3. Click nút Printer icon trên một đơn hàng<br>4. Click "In" trong modal | Hiển thị PrintOrderModal với DialogTitle "In đơn hàng", có preview đơn hàng với đầy đủ thông tin: Mã đơn hàng, Thông tin khách hàng, Danh sách sản phẩm, Tổng tiền, Phương thức thanh toán, Địa chỉ giao hàng, Trạng thái, Ngày tạo. Có nút "In" và "Hủy". Sau khi click "In": mở dialog in của trình duyệt, có thể in ra giấy hoặc lưu PDF, modal đóng sau khi in | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-IDH-02** | Hủy in đơn hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/orders<br>3. Click nút Printer icon<br>4. Click "Hủy" trong modal | Modal đóng lại, không in đơn hàng | FUNC-DN-02 | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn MDX để dễ dàng quản lý và cập nhật test cases.*
