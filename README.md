# Test Case Template - Quản lý khách hàng (Nhân viên)

## Module Code
**Giao lộ 19: Họcl6c (Nhân viên)**

## Test Requirement
1. Tìm kiếm thông tin khách hàng
2. Hiển thị kết quả khách hàng
3. Xem lịch sử mua hàng

---

## Test Summary

### Người lớp Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 30 |
| **Fail** | 0 |
| **Untested** | 0 |
| **N/A** | 0 |
| **Number of Test cases** | 30 |

---

## Test Cases

### Function: Tìm kiếm thông tin khách hàng

#### Check GUI: Tìm kiếm thông tin khách hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-TKKH-01** | Kiểm tra tiêu đề trang | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/customers<br>3. Kiểm tra tiêu đề | Hiển thị div space-y-6 với h1 "Tìm kiếm khách hàng" class text-2xl font-bold, p "Tra cứu thông tin khách hàng để hỗ trợ bán hàng" class text-sm text-muted-foreground | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-TKKH-02** | Kiểm tra card Tìm kiếm nhanh | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/customers<br>3. Kiểm tra card | Hiển thị Card với CardHeader có CardTitle "Tìm kiếm nhanh", CardDescription "Nhập số điện thoại, email hoặc tên", CardContent className="grid gap-3 md:grid-cols-6" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-TKKH-03** | Kiểm tra form Tìm kiếm nhanh | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/customers<br>3. Kiểm tra form | Hiển thị div md:col-span-4 với Input value={query} onChange placeholder="SĐT, email, tên...", div flex gap-2 với Button className="shrink-0" "Tìm kiếm", Button variant="outline" className="shrink-0" "Xóa" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-TKKH-04** | Kiểm tra card Tìm kiếm nâng cao | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/customers<br>3. Kiểm tra card | Hiển thị Card với CardHeader có CardTitle "Tìm kiếm nâng cao", CardDescription "Bộ lọc chi tiết theo mô tả", CardContent className="grid gap-3 md:grid-cols-6" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-TKKH-05** | Kiểm tra các trường tìm kiếm nâng cao | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/customers<br>3. Kiểm tra các trường | Hiển thị: div grid gap-1 với Label "Số điện thoại", Input placeholder="0123456789". div grid gap-1 với Label "Email", Input type="email" placeholder="email@domain.com". div grid gap-1 với Label "Họ và tên", Input placeholder="Nguyễn Văn A". div grid gap-1 với Label "Mã khách hàng", Input placeholder="CUS-001". div grid gap-1 với Label "Địa chỉ", Input placeholder="Địa chỉ". div grid gap-1 với Label "Khu vực", Select với SelectTrigger SelectValue placeholder="Tất cả", SelectContent có SelectItem (Tất cả, TP.HCM, Hà Nội, Đà Nẵng, Khác). div grid gap-1 với Label "Hạng khách hàng", Select (Tất cả, Vàng, Bạc, Đồng, Thành viên mới). div grid gap-1 với Label "Trạng thái", Select (Tất cả, Hoạt động, Tạm khóa, Đã xóa). div md:col-span-2 flex items-end gap-2 với Button className="shrink-0" "Tìm kiếm", Button variant="outline" className="shrink-0" "Lưu bộ lọc" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-TKKH-06** | Kiểm tra card Kết quả tìm kiếm | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/customers<br>3. Kiểm tra card | Hiển thị Card với CardHeader có CardTitle "Kết quả tìm kiếm", CardDescription "Số kết quả: X khách hàng", CardContent className="space-y-3 text-sm" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-TKKH-07** | Kiểm tra item kết quả tìm kiếm | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/customers<br>3. Kiểm tra item | Mỗi item có div p-3 border rounded với div flex items-center justify-between chứa div có div font-medium (tên khách hàng), div text-muted-foreground (phone + " • " + email), Button asChild variant="outline" Link href="/nhanvien/customers/[id]" "Xem chi tiết" | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Tìm kiếm thông tin khách hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TKKH-01** | Tìm kiếm nhanh khách hàng | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/customers<br>3. Nhập từ khóa vào Input (VD: số điện thoại, email, tên)<br>4. Click "Tìm kiếm" | Danh sách khách hàng được lọc theo từ khóa, chỉ hiển thị các khách hàng có số điện thoại, email, hoặc tên chứa từ khóa, tìm kiếm không phân biệt hoa thường, hỗ trợ tìm kiếm một phần từ khóa, card "Kết quả tìm kiếm" hiển thị với số lượng kết quả, các item khách hàng được hiển thị với thông tin cơ bản (tên, phone, email), có nút "Xem chi tiết" cho mỗi khách hàng | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TKKH-02** | Tìm kiếm nhanh không có kết quả | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/customers<br>3. Nhập từ khóa không tồn tại (VD: "xyz123")<br>4. Click "Tìm kiếm" | Hiển thị thông báo "Không tìm thấy khách hàng nào phù hợp", card "Kết quả tìm kiếm" hiển thị "Số kết quả: 0 khách hàng", CardContent trống hoặc hiển thị thông báo không có kết quả | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TKKH-03** | Xóa tìm kiếm nhanh | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/customers<br>3. Nhập từ khóa<br>4. Click "Xóa" | Input được xóa trống, danh sách khách hàng hiển thị lại tất cả hoặc reset về trạng thái ban đầu | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TKKH-04** | Tìm kiếm nâng cao theo số điện thoại | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/customers<br>3. Nhập số điện thoại vào Input "Số điện thoại"<br>4. Click "Tìm kiếm" | Danh sách khách hàng được lọc theo số điện thoại đã nhập, chỉ hiển thị khách hàng có số điện thoại khớp, card "Kết quả tìm kiếm" hiển thị số lượng kết quả | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TKKH-05** | Tìm kiếm nâng cao theo email | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/customers<br>3. Nhập email vào Input "Email"<br>4. Click "Tìm kiếm" | Danh sách khách hàng được lọc theo email đã nhập, chỉ hiển thị khách hàng có email khớp | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TKKH-06** | Tìm kiếm nâng cao theo hạng khách hàng | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/customers<br>3. Chọn hạng khách hàng từ Select (VD: "Vàng")<br>4. Click "Tìm kiếm" | Danh sách khách hàng được lọc theo hạng đã chọn, chỉ hiển thị các khách hàng có hạng "Vàng" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TKKH-07** | Tìm kiếm nâng cao theo trạng thái | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/customers<br>3. Chọn trạng thái từ Select (VD: "Hoạt động")<br>4. Click "Tìm kiếm" | Danh sách khách hàng được lọc theo trạng thái đã chọn, chỉ hiển thị các khách hàng có trạng thái "Hoạt động" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TKKH-08** | Tìm kiếm nâng cao kết hợp nhiều tiêu chí | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/customers<br>3. Nhập số điện thoại, chọn hạng "Vàng", chọn trạng thái "Hoạt động"<br>4. Click "Tìm kiếm" | Danh sách khách hàng được lọc theo tất cả các tiêu chí đã chọn, chỉ hiển thị các khách hàng thỏa mãn tất cả điều kiện (số điện thoại AND hạng Vàng AND trạng thái Hoạt động) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TKKH-09** | Lưu bộ lọc | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/customers<br>3. Thiết lập các bộ lọc<br>4. Click "Lưu bộ lọc" | Bộ lọc được lưu thành công, hiển thị thông báo thành công "Đã lưu bộ lọc" (toast success), bộ lọc có thể được sử dụng lại sau này | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TKKH-10** | Xem chi tiết khách hàng từ kết quả | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/customers<br>3. Tìm kiếm khách hàng<br>4. Click nút "Xem chi tiết" trên một khách hàng | Chuyển đến trang /nhanvien/customers/[id], hiển thị chi tiết khách hàng với đầy đủ thông tin | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Hiển thị kết quả khách hàng

#### Check GUI: Hiển thị kết quả khách hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-HTKH-01** | Kiểm tra layout trang chi tiết | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/customers/[id]<br>3. Kiểm tra layout | Hiển thị div grid gap-6 lg:grid-cols-2 với các Card | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-HTKH-02** | Kiểm tra card Thông tin khách hàng | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/customers/[id]<br>3. Kiểm tra card | Hiển thị Card với CardHeader có CardTitle "Thông tin khách hàng", CardDescription "Chi tiết hồ sơ khách hàng", CardContent className="grid grid-cols-2 gap-4 text-sm" với các div có div text-muted-foreground (label) và div font-medium (value) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-HTKH-03** | Kiểm tra thông tin cơ bản | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/customers/[id]<br>3. Kiểm tra thông tin | Hiển thị: "Họ và tên" với giá trị, "Số điện thoại" với giá trị, "Email" với giá trị, "Địa chỉ" với giá trị, "Hạng khách hàng" với Badge, "Trạng thái" với Badge variant="default", "Mã khách hàng" với giá trị, "Ngày đăng ký" với giá trị | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-HTKH-04** | Kiểm tra card Thống kê mua hàng | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/customers/[id]<br>3. Kiểm tra card | Hiển thị Card với CardHeader có CardTitle "Thống kê mua hàng", CardDescription "Tổng quan hành vi mua hàng", CardContent className="space-y-2 text-sm" với các div chứa thông tin (Đơn hàng gần nhất, Giá trị đơn hàng TB, Sản phẩm yêu thích, Tần suất mua hàng), div pt-2 với Button asChild variant="outline" Link href="/nhanvien/customers/[id]/history" "Xem lịch sử mua hàng" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-HTKH-05** | Kiểm tra card Ghi chú khách hàng | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/customers/[id]<br>3. Kiểm tra card | Hiển thị Card className="lg:col-span-2" với CardHeader có CardTitle "Ghi chú khách hàng", CardDescription "Lịch sử ghi chú", CardContent className="space-y-2 text-sm" với các div chứa ghi chú (thời gian, người ghi chú, nội dung), div pt-2 flex gap-2 với Button variant="outline" "Thêm ghi chú", Button variant="outline" "Gửi tin nhắn", Button variant="outline" "Cập nhật thông tin" | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Hiển thị kết quả khách hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-HTKH-01** | Xem thông tin khách hàng | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/customers/[id] | Hiển thị đầy đủ: card Thông tin khách hàng với thông tin cơ bản (Họ và tên, Số điện thoại, Email, Địa chỉ, Hạng khách hàng Badge, Trạng thái Badge variant="default", Mã khách hàng, Ngày đăng ký), card Thống kê mua hàng với thông tin (Đơn hàng gần nhất, Giá trị đơn hàng TB, Sản phẩm yêu thích, Tần suất mua hàng), nút "Xem lịch sử mua hàng", card Ghi chú khách hàng với lịch sử ghi chú, các nút thao tác (Thêm ghi chú, Gửi tin nhắn, Cập nhật thông tin) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-HTKH-02** | Thêm ghi chú khách hàng | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/customers/[id]<br>3. Click nút "Thêm ghi chú"<br>4. Nhập nội dung ghi chú<br>5. Click "Lưu" | Hiển thị Dialog hoặc form với Textarea để nhập ghi chú, sau khi lưu: ghi chú được thêm thành công, hiển thị thông báo thành công "Đã thêm ghi chú" (toast success), ghi chú xuất hiện trong lịch sử ghi chú với thông tin (thời gian, tên nhân viên, nội dung), lịch sử ghi chú được cập nhật | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-HTKH-03** | Gửi tin nhắn cho khách hàng | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/customers/[id]<br>3. Click nút "Gửi tin nhắn"<br>4. Nhập nội dung tin nhắn<br>5. Chọn phương thức gửi (SMS/Email)<br>6. Click "Gửi" | Hiển thị Dialog hoặc form với Textarea để nhập nội dung, Select để chọn phương thức gửi, thông tin liên hệ khách hàng được điền tự động, sau khi gửi: tin nhắn được gửi thành công, hiển thị thông báo thành công "Đã gửi tin nhắn" (toast success), khách hàng nhận được tin nhắn qua SMS hoặc email, lịch sử tin nhắn được lưu | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-HTKH-04** | Cập nhật thông tin khách hàng | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/customers/[id]<br>3. Click nút "Cập nhật thông tin"<br>4. Sửa thông tin (VD: địa chỉ, số điện thoại, email)<br>5. Click "Lưu" | Hiển thị Dialog hoặc form với các Input có thể chỉnh sửa (địa chỉ, số điện thoại, email), một số thông tin có thể chỉ đọc (họ tên, mã khách hàng), sau khi lưu: thông tin được cập nhật thành công, hiển thị thông báo thành công "Đã cập nhật thông tin" (toast success), thông tin trong card "Thông tin khách hàng" được cập nhật, lịch sử thay đổi được ghi lại, khách hàng nhận được thông báo về việc thay đổi (nếu có email) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-HTKH-05** | Xem lịch sử mua hàng | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/customers/[id]<br>3. Click nút "Xem lịch sử mua hàng" | Chuyển đến trang /nhanvien/customers/[id]/history, hiển thị lịch sử mua hàng với đầy đủ thông tin | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Xem lịch sử mua hàng

#### Check GUI: Xem lịch sử mua hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-LSMH-01** | Kiểm tra tiêu đề trang | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/customers/[id]/history<br>3. Kiểm tra tiêu đề | Hiển thị tiêu đề "Lịch sử mua hàng - [Tên khách hàng]" hoặc "Lịch sử mua hàng" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-LSMH-02** | Kiểm tra thống kê tổng quan | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/customers/[id]/history<br>3. Kiểm tra thống kê | Hiển thị div grid grid-cols-2 md:grid-cols-4 gap-4 với 4 Card: Card "Tổng đơn hàng" với số liệu, Card "Đơn hàng thành công" với số liệu, Card "Đơn hàng đã hủy" với số liệu, Card "Tổng chi tiêu" với số liệu format VNĐ | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-LSMH-03** | Kiểm tra bộ lọc lịch sử | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/customers/[id]/history<br>3. Kiểm tra bộ lọc | Hiển thị Card với CardHeader có CardTitle "Bộ lọc lịch sử", CardContent chứa: Input type="date" hoặc DateRange cho "Khoảng thời gian", Select "Trạng thái đơn hàng" (Tất cả, Thành công, Đã hủy, Đang xử lý), Select "Phương thức thanh toán" (Tất cả, Tiền mặt, Thẻ, Chuyển khoản, Ví điện tử), Slider hoặc Input cho "Khoảng giá", Button "Áp dụng", Button "Xóa bộ lọc" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-LSMH-04** | Kiểm tra bảng danh sách đơn hàng | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/customers/[id]/history<br>3. Kiểm tra bảng | Hiển thị Table với TableHeader có các TableHead: "Mã đơn hàng" (Link), "Ngày đặt", "Sản phẩm", "Tổng tiền", "Trạng thái" (Badge), "Phương thức thanh toán", "Thao tác". TableBody có các TableRow với TableCell tương ứng | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-LSMH-05** | Kiểm tra các nút thao tác | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/customers/[id]/history<br>3. Kiểm tra nút | Mỗi hàng có TableCell "Thao tác" chứa Button "Xem chi tiết", Button "Tạo đơn hàng tương tự", Button "In hóa đơn" | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Xem lịch sử mua hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-LSMH-01** | Xem lịch sử mua hàng | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/customers/[id]/history | Hiển thị đầy đủ: tiêu đề "Lịch sử mua hàng", thống kê tổng quan 4 card (Tổng đơn hàng, Đơn hàng thành công, Đơn hàng đã hủy, Tổng chi tiêu), bộ lọc lịch sử với đầy đủ các bộ lọc, bảng danh sách đơn hàng với các đơn hàng, mỗi hàng có Mã đơn hàng (Link), Ngày đặt, Sản phẩm (danh sách), Tổng tiền (format VNĐ), Trạng thái (Badge), Phương thức thanh toán, các nút thao tác (Xem chi tiết, Tạo đơn hàng tương tự, In hóa đơn), đơn hàng được sắp xếp theo thời gian đặt (mới nhất trước) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-LSMH-02** | Lọc lịch sử theo khoảng thời gian | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/customers/[id]/history<br>3. Chọn khoảng thời gian<br>4. Click "Áp dụng" | Danh sách đơn hàng được lọc theo khoảng thời gian đã chọn, chỉ hiển thị các đơn hàng có ngày đặt trong khoảng thời gian đó, thống kê được cập nhật theo kết quả lọc | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-LSMH-03** | Lọc lịch sử theo trạng thái đơn hàng | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/customers/[id]/history<br>3. Chọn trạng thái từ Select (VD: "Thành công")<br>4. Click "Áp dụng" | Danh sách đơn hàng được lọc theo trạng thái đã chọn, chỉ hiển thị các đơn hàng có trạng thái "Thành công", Badge màu xanh | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-LSMH-04** | Lọc lịch sử theo phương thức thanh toán | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/customers/[id]/history<br>3. Chọn phương thức thanh toán từ Select (VD: "Tiền mặt")<br>4. Click "Áp dụng" | Danh sách đơn hàng được lọc theo phương thức thanh toán đã chọn, chỉ hiển thị các đơn hàng có phương thức thanh toán "Tiền mặt" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-LSMH-05** | Lọc lịch sử theo khoảng giá | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/customers/[id]/history<br>3. Điều chỉnh khoảng giá (VD: 100,000 - 1,000,000đ)<br>4. Click "Áp dụng" | Danh sách đơn hàng được lọc theo khoảng giá đã chọn, chỉ hiển thị các đơn hàng có tổng tiền trong khoảng giá đó | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-LSMH-06** | Xem chi tiết đơn hàng từ lịch sử | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/customers/[id]/history<br>3. Click Link "Mã đơn hàng" hoặc nút "Xem chi tiết" | Hiển thị Dialog hoặc chuyển đến trang chi tiết đơn hàng với đầy đủ thông tin: thông tin đơn hàng (mã, ngày đặt, trạng thái, phương thức thanh toán, tổng tiền), danh sách sản phẩm Table (tên sản phẩm, số lượng, đơn giá, thành tiền), thông tin thanh toán, lịch sử xử lý Timeline | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-LSMH-07** | Tạo đơn hàng tương tự | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/customers/[id]/history<br>3. Click nút "Tạo đơn hàng tương tự" trên một đơn hàng | Đơn hàng mới được tạo dựa trên đơn hàng trong lịch sử, thông tin khách hàng được điền tự động, danh sách sản phẩm được điền tự động, cho phép chỉnh sửa số lượng sản phẩm và thêm/bớt sản phẩm, tổng tiền đơn hàng được tính lại, hiển thị thông báo thành công "Đã tạo đơn hàng tương tự" (toast success), chuyển đến trang tạo đơn hàng hoặc trang chi tiết đơn hàng mới | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-LSMH-08** | In hóa đơn từ lịch sử | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/customers/[id]/history<br>3. Click nút "In hóa đơn" trên một đơn hàng | Hóa đơn được mở trong dialog in hoặc chuyển đến trang in, hóa đơn bao gồm đầy đủ thông tin (cửa hàng, đơn hàng, khách hàng, sản phẩm, tổng kết), có thể in trực tiếp hoặc lưu PDF | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-LSMH-09** | Xuất báo cáo lịch sử | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/customers/[id]/history<br>3. Click nút "Xuất báo cáo" | Báo cáo lịch sử mua hàng được tạo dưới dạng PDF hoặc Excel, báo cáo bao gồm thông tin chi tiết về các đơn hàng, thống kê tổng quan, có thể có biểu đồ phân tích, file được tải xuống hoặc lưu vào thư mục, tên file theo tên khách hàng và ngày xuất, hiển thị thông báo thành công "Đã xuất báo cáo" (toast success) | FUNC-DN-02 | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn MDX để dễ dàng quản lý và cập nhật test cases.*

