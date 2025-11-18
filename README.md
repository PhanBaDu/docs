# Test Case Template - Quản lý nhân viên (Admin)

## Module Code
**Giao lộ 19: Họcl6c (Admin)**

## Test Requirement
1. Hiển thị danh sách nhân viên
2. Xem chi tiết nhân viên
3. Thêm nhân viên mới
4. Chỉnh sửa thông tin nhân viên
5. Khóa tài khoản nhân viên
6. Xóa nhân viên

---

## Test Summary

### Người lớp Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 38 |
| **Fail** | 0 |
| **Untested** | 0 |
| **N/A** | 0 |
| **Number of Test cases** | 38 |

---

## Test Cases

### Function: Hiển thị danh sách nhân viên

#### Check GUI: Hiển thị danh sách nhân viên

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DSNV-01** | Kiểm tra tiêu đề trang | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees<br>3. Kiểm tra tiêu đề | Hiển thị tiêu đề "Quản lý nhân viên" với class text-2xl font-bold, mô tả "Danh sách nhân viên" với class text-sm text-muted-foreground, nằm trong div flex items-center justify-between | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSNV-02** | Kiểm tra thống kê nhân viên | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees<br>3. Kiểm tra thống kê | Hiển thị grid grid-cols-2 md:grid-cols-4 gap-4 với 4 Card: Card 1 "Tổng nhân viên" hiển thị số 25, Card 2 "Bán hàng" hiển thị số 15, Card 3 "Kho" hiển thị số 8, Card 4 "Admin" hiển thị số 2. Mỗi card có CardContent p-4 với text-sm text-muted-foreground cho label và text-xl font-semibold cho số | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSNV-03** | Kiểm tra card Bộ lọc | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees<br>3. Kiểm tra card bộ lọc | Hiển thị Card với CardHeader có CardTitle "Bộ lọc", CardDescription "Vị trí, trạng thái, thời gian, tìm kiếm", CardContent có grid md:grid-cols-5 gap-3 | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSNV-04** | Kiểm tra dropdown Vị trí | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees<br>3. Kiểm tra dropdown Vị trí | Hiển thị Label "Vị trí", Select với SelectTrigger có placeholder "Tất cả", SelectContent có các option: "Tất cả", "Nhân viên bán hàng", "Nhân viên kho", "Admin" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSNV-05** | Kiểm tra dropdown Trạng thái | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees<br>3. Kiểm tra dropdown Trạng thái | Hiển thị Label "Trạng thái", Select với SelectTrigger có placeholder "Tất cả", SelectContent có các option: "Tất cả", "Hoạt động", "Khóa tài khoản", "Nghỉ việc" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSNV-06** | Kiểm tra dropdown Khoảng thời gian | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees<br>3. Kiểm tra dropdown Khoảng thời gian | Hiển thị Label "Khoảng thời gian", Select với SelectTrigger có placeholder "Tất cả", SelectContent có các option: "Tất cả", "Tuần này", "Tháng này", "Quý này", "Năm này" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSNV-07** | Kiểm tra ô Tìm kiếm | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees<br>3. Kiểm tra ô tìm kiếm | Hiển thị Label "Tìm kiếm", Input với placeholder "Tên hoặc email..." nằm trong grid gap-1 md:col-span-2 | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSNV-08** | Kiểm tra card Danh sách nhân viên | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees<br>3. Kiểm tra card danh sách | Hiển thị Card với CardHeader có CardTitle "Danh sách nhân viên", CardContent chứa Table | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSNV-09** | Kiểm tra bảng danh sách nhân viên | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees<br>3. Kiểm tra bảng | Hiển thị Table với TableHeader có các TableHead: "Mã NV", "Họ tên", "Vị trí", "Email", "Trạng thái", "Ngày tạo", "Thao tác". TableBody có các TableRow với TableCell tương ứng | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSNV-10** | Kiểm tra nút Thêm nhân viên | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees<br>3. Kiểm tra nút | Hiển thị Button "Thêm nhân viên" với asChild Link href="/admin/employees/new", nằm trong div flex gap-2 bên phải tiêu đề | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSNV-11** | Kiểm tra nút Xuất báo cáo | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees<br>3. Kiểm tra nút | Hiển thị Button variant="outline" "Xuất báo cáo" nằm cạnh nút Thêm nhân viên | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSNV-12** | Kiểm tra các nút thao tác trong bảng | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees<br>3. Kiểm tra nút thao tác | Mỗi hàng có TableCell "Thao tác" với class space-x-2 chứa: Button size="sm" variant="outline" "Xem chi tiết" với Link href="/admin/employees/[id]", Button size="sm" variant="outline" "Chỉnh sửa" với Link href="/admin/employees/[id]/edit", Button size="sm" variant="destructive" "Khóa tài khoản" | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Hiển thị danh sách nhân viên

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DSNV-01** | Xem danh sách nhân viên | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees | Hiển thị đầy đủ: thống kê 4 card (Tổng nhân viên: 25, Bán hàng: 15, Kho: 8, Admin: 2), card Bộ lọc với 4 dropdown và 1 input tìm kiếm, card Danh sách nhân viên với Table hiển thị các nhân viên, mỗi hàng có Mã NV (Badge variant="secondary"), Họ tên, Vị trí (Badge), Email, Trạng thái (Badge), Ngày tạo, các nút thao tác | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSNV-02** | Tìm kiếm nhân viên | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees<br>3. Nhập từ khóa tìm kiếm vào ô "Tên hoặc email..." | Danh sách nhân viên được lọc theo từ khóa (tên, email, mã nhân viên), bảng cập nhật ngay lập tức, hiển thị các nhân viên phù hợp | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSNV-03** | Lọc nhân viên theo vị trí | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees<br>3. Chọn vị trí từ dropdown (VD: "Nhân viên bán hàng") | Danh sách nhân viên được lọc theo vị trí đã chọn, bảng chỉ hiển thị nhân viên có vị trí tương ứng, thống kê có thể cập nhật | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSNV-04** | Lọc nhân viên theo trạng thái | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees<br>3. Chọn trạng thái từ dropdown (VD: "Hoạt động") | Danh sách nhân viên được lọc theo trạng thái đã chọn, bảng chỉ hiển thị nhân viên có trạng thái tương ứng | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSNV-05** | Lọc nhân viên theo khoảng thời gian | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees<br>3. Chọn khoảng thời gian từ dropdown (VD: "Tháng này") | Danh sách nhân viên được lọc theo khoảng thời gian tạo tài khoản, bảng chỉ hiển thị nhân viên được tạo trong khoảng thời gian đã chọn | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSNV-06** | Kết hợp nhiều bộ lọc | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees<br>3. Chọn vị trí "Nhân viên bán hàng"<br>4. Chọn trạng thái "Hoạt động"<br>5. Nhập từ khóa tìm kiếm | Danh sách nhân viên được lọc theo tất cả các tiêu chí đã chọn, bảng chỉ hiển thị nhân viên thỏa mãn tất cả điều kiện | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Xem chi tiết nhân viên

#### Check GUI: Xem chi tiết nhân viên

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CTNV-01** | Kiểm tra tiêu đề trang | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees/[id]<br>3. Kiểm tra tiêu đề | Hiển thị tiêu đề "Chi tiết nhân viên - NV001" với class text-2xl font-bold, nằm trong div | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-CTNV-02** | Kiểm tra card Thông tin cá nhân | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees/[id]<br>3. Kiểm tra card | Hiển thị Card với CardHeader có CardTitle "Thông tin cá nhân", CardContent có grid md:grid-cols-3 gap-3 text-sm, hiển thị các trường: Mã nhân viên (text-muted-foreground label, font-medium value), Họ tên, Email, Số điện thoại, Địa chỉ (md:col-span-2), Ngày sinh, Giới tính | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-CTNV-03** | Kiểm tra card Thông tin công việc | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees/[id]<br>3. Kiểm tra card | Hiển thị Card với CardHeader có CardTitle "Thông tin công việc", CardContent có grid md:grid-cols-3 gap-3 text-sm, hiển thị các trường: Vị trí (Badge), Phòng ban, Ngày bắt đầu, Lương cơ bản, Trạng thái (Badge), Quyền hạn | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-CTNV-04** | Kiểm tra card Lịch sử hoạt động | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees/[id]<br>3. Kiểm tra card | Hiển thị Card với CardHeader có CardTitle "Lịch sử hoạt động", CardContent có space-y-2 text-sm, hiển thị các hoạt động dạng text với format "Thời gian • Hành động • IP • Thiết bị" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-CTNV-05** | Kiểm tra card Audit Log | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees/[id]<br>3. Kiểm tra card | Hiển thị Card với CardHeader có CardTitle "Audit Log - Lịch sử thao tác nhạy cảm", CardDescription "Ghi nhận tất cả các thao tác khóa, mở khóa, xóa tài khoản", CardContent có Table với các cột: Thời gian, Hành động (Badge), Người thực hiện, Lý do, IP Address, Chi tiết (max-w-xs truncate) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-CTNV-06** | Kiểm tra các nút thao tác | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees/[id]<br>3. Kiểm tra nút | Hiển thị div flex flex-wrap gap-2 với các Button: "Chỉnh sửa" variant="outline" với Link href="/admin/employees/[id]/edit", "Khóa tài khoản" variant="destructive" onClick mở dialog, "Mở khóa tài khoản" variant="outline" onClick mở dialog, "Đặt lại mật khẩu" variant="outline", "Xóa tài khoản" variant="destructive" onClick mở dialog | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Xem chi tiết nhân viên

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CTNV-01** | Xem chi tiết nhân viên | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees<br>3. Click [Xem chi tiết] hoặc truy cập /admin/employees/[id] | Hiển thị đầy đủ thông tin: tiêu đề "Chi tiết nhân viên - NV001", card Thông tin cá nhân với đầy đủ các trường (Mã nhân viên, Họ tên, Email, Số điện thoại, Địa chỉ, Ngày sinh, Giới tính), card Thông tin công việc với đầy đủ các trường (Vị trí, Phòng ban, Ngày bắt đầu, Lương cơ bản, Trạng thái, Quyền hạn), card Lịch sử hoạt động, card Audit Log với Table, các nút thao tác | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-CTNV-02** | Xem lịch sử hoạt động | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees/[id]<br>3. Xem card Lịch sử hoạt động | Hiển thị lịch sử hoạt động theo dòng thời gian từ cũ đến mới, mỗi hoạt động có format "Thời gian • Hành động • IP Address • Thiết bị" (VD: "2023-11-20 14:30 • Đăng nhập hệ thống • IP 192.168.1.100 • Chrome/Windows 10") | FUNC-DN-02, FUNC-CTNV-01 | Pass | 11/15/2015 | |
| **FUNC-CTNV-03** | Xem Audit Log | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees/[id]<br>3. Xem card Audit Log | Hiển thị Table với các hàng audit log, mỗi hàng có: Thời gian, Hành động (Badge với variant destructive nếu là "Khóa tài khoản"), Người thực hiện, Lý do, IP Address, Chi tiết (truncate nếu quá dài) | FUNC-DN-02, FUNC-CTNV-01 | Pass | 11/15/2015 | |

---

### Function: Thêm nhân viên mới

#### Check GUI: Thêm nhân viên mới

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-TNV-01** | Kiểm tra tiêu đề trang | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees/new<br>3. Kiểm tra tiêu đề | Hiển thị tiêu đề "Thêm nhân viên mới" với class text-2xl font-bold, nằm trong div | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-TNV-02** | Kiểm tra card Thông tin cá nhân | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees/new<br>3. Kiểm tra card | Hiển thị Card với CardHeader có CardTitle "Thông tin cá nhân", CardContent chứa form với grid gap-4 md:grid-cols-2 | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-TNV-03** | Kiểm tra form thông tin cá nhân | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees/new<br>3. Kiểm tra form | Hiển thị form với các trường: Label "Họ tên" với Input placeholder="Nguyễn Văn A" required, Label "Email" với Input type="email" placeholder="email@bookstore.com" required, Label "Số điện thoại" với Input type="tel" placeholder="0901234567", Label "Địa chỉ" với Textarea placeholder="123 Đường ABC, Quận 1, TP.HCM" md:col-span-2, Label "Ngày sinh" với Input type="date", Label "Giới tính" với Select defaultValue="male" có options Nam/Nữ/Khác | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-TNV-04** | Kiểm tra form thông tin công việc | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees/new<br>3. Kiểm tra form | Hiển thị các trường: Label "Vị trí" với Select defaultValue="sales" có options "Nhân viên bán hàng", "Nhân viên kho", "Admin", Label "Phòng ban" với Input placeholder="Phòng bán hàng", Label "Lương cơ bản" với Input type="number" placeholder="8000000", Label "Quyền hạn" với grid grid-cols-2 gap-2 text-sm chứa các checkbox: "Xem sách", "Tạo đơn hàng", "Quản lý khách hàng", "Báo cáo ca làm", "Quản lý kho", "Nhập xuất hàng", Label "Mật khẩu tạm thời" với Input type="password" placeholder="••••••••" md:col-span-2 | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-TNV-05** | Kiểm tra nút Lưu và Hủy | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees/new<br>3. Kiểm tra nút | Hiển thị div flex gap-2 md:col-span-2 với Button type="submit" "Lưu" và Button type="button" variant="outline" "Hủy" | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Thêm nhân viên mới

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TNV-01** | Thêm nhân viên thành công | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees/new<br>3. Nhập đầy đủ thông tin hợp lệ (Họ tên, Email, Số điện thoại, Địa chỉ, Ngày sinh, Giới tính, Vị trí, Phòng ban, Lương cơ bản, chọn Quyền hạn, Mật khẩu tạm thời)<br>4. Nhấn Lưu | Tài khoản nhân viên được tạo thành công, hiển thị Alert với AlertDescription "Tạo tài khoản nhân viên thành công", email thông báo được gửi cho nhân viên với thông tin đăng nhập, có thể chuyển về danh sách nhân viên hoặc ở lại trang | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TNV-02** | Thêm nhân viên với email đã tồn tại | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees/new<br>3. Nhập email đã tồn tại<br>4. Nhập các thông tin khác hợp lệ<br>5. Nhấn Lưu | Hiển thị thông báo lỗi "Email đã tồn tại" (toast error), không tạo tài khoản, vẫn ở trang thêm nhân viên, các trường input vẫn giữ giá trị đã nhập | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TNV-03** | Thêm nhân viên thiếu thông tin bắt buộc | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees/new<br>3. Để trống các trường bắt buộc (Họ tên, Email)<br>4. Nhấn Lưu | Trình duyệt hiển thị cảnh báo "Please fill out this field" trên các trường bắt buộc, form không được gửi, không có request đến server | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TNV-04** | Hủy thêm nhân viên | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees/new<br>3. Nhập một số thông tin<br>4. Nhấn Hủy | Đóng form, quay về danh sách nhân viên (/admin/employees), không lưu thông tin đã nhập | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Chỉnh sửa thông tin nhân viên

#### Check GUI: Chỉnh sửa thông tin nhân viên

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-SNV-01** | Kiểm tra tiêu đề trang | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees/[id]/edit<br>3. Kiểm tra tiêu đề | Hiển thị tiêu đề "Chỉnh sửa thông tin nhân viên - [Mã nhân viên]" với layout tương tự trang thêm nhân viên | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-SNV-02** | Kiểm tra form đã điền sẵn | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees/[id]/edit<br>3. Kiểm tra form | Form hiển thị với thông tin hiện tại của nhân viên đã được điền sẵn vào các trường input, select, checkbox tương ứng | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Chỉnh sửa thông tin nhân viên

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-SNV-01** | Cập nhật thông tin nhân viên thành công | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees/[id]/edit<br>3. Cập nhật thông tin (VD: Số điện thoại, Địa chỉ, Lương cơ bản, Quyền hạn)<br>4. Nhấn Lưu | Thông tin được cập nhật thành công, hiển thị thông báo thành công (toast success), lịch sử thay đổi được ghi nhận vào Audit Log, có thể chuyển về chi tiết nhân viên hoặc danh sách | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-SNV-02** | Cập nhật với email đã tồn tại (khác nhân viên) | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees/[id]/edit<br>3. Đổi email thành email đã tồn tại của nhân viên khác<br>4. Nhấn Lưu | Hiển thị thông báo lỗi "Email đã tồn tại" (toast error), không cập nhật, vẫn ở trang chỉnh sửa | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-SNV-03** | Hủy chỉnh sửa | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees/[id]/edit<br>3. Thay đổi thông tin<br>4. Nhấn Hủy | Đóng form, quay về chi tiết nhân viên (/admin/employees/[id]), không lưu thay đổi, thông tin vẫn giữ nguyên như ban đầu | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Khóa tài khoản nhân viên

#### Check FUNC: Khóa tài khoản nhân viên

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-KTNV-01** | Khóa tài khoản nhân viên | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees/[id]<br>3. Click nút "Khóa tài khoản"<br>4. Nhập lý do khóa vào Textarea<br>5. Click "Xác nhận khóa" | Hiển thị Dialog với DialogTitle "Khóa tài khoản nhân viên", DialogDescription "Vui lòng nhập lý do khóa tài khoản. Hành động này sẽ được ghi vào audit log.", có Textarea placeholder="Nhập lý do khóa tài khoản..." required. Sau khi xác nhận: tài khoản được khóa thành công, hiển thị thông báo "Đã khóa tài khoản và ghi nhận audit log" (toast success), dialog đóng, trạng thái cập nhật, audit log được thêm vào bảng với Badge variant="destructive", thông báo được gửi cho nhân viên qua email | FUNC-DN-02, FUNC-CTNV-01 | Pass | 11/15/2015 | |
| **FUNC-KTNV-02** | Khóa tài khoản thiếu lý do | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees/[id]<br>3. Click "Khóa tài khoản"<br>4. Để trống lý do<br>5. Click "Xác nhận khóa" | Hiển thị thông báo lỗi "Vui lòng nhập lý do khóa tài khoản" (toast error), không khóa tài khoản, dialog vẫn mở | FUNC-DN-02, FUNC-CTNV-01 | Pass | 11/15/2015 | |
| **FUNC-KTNV-03** | Hủy khóa tài khoản | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees/[id]<br>3. Click "Khóa tài khoản"<br>4. Nhập lý do<br>5. Click "Hủy" | Dialog đóng lại, không khóa tài khoản, trạng thái không thay đổi | FUNC-DN-02, FUNC-CTNV-01 | Pass | 11/15/2015 | |
| **FUNC-KTNV-04** | Mở khóa tài khoản nhân viên | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees/[id] (nhân viên đã khóa)<br>3. Click nút "Mở khóa tài khoản"<br>4. Nhập lý do mở khóa vào Textarea<br>5. Click "Xác nhận mở khóa" | Hiển thị Dialog với DialogTitle "Mở khóa tài khoản nhân viên", DialogDescription "Vui lòng nhập lý do mở khóa tài khoản. Hành động này sẽ được ghi vào audit log.", có Textarea placeholder="Nhập lý do mở khóa tài khoản..." required. Sau khi xác nhận: tài khoản được mở khóa thành công, hiển thị thông báo "Đã mở khóa tài khoản và ghi nhận audit log" (toast success), dialog đóng, trạng thái cập nhật, audit log được thêm vào bảng, thông báo được gửi cho nhân viên | FUNC-DN-02, FUNC-CTNV-01 | Pass | 11/15/2015 | |

---

### Function: Xóa nhân viên

#### Check FUNC: Xóa nhân viên

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XNV-01** | Xóa nhân viên | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees/[id]<br>3. Click nút "Xóa tài khoản"<br>4. Nhập lý do xóa vào Textarea<br>5. Click "Xác nhận xóa" | Hiển thị Dialog với DialogTitle "Xóa tài khoản nhân viên", DialogDescription "Cảnh báo: Hành động này không thể hoàn tác. Vui lòng nhập lý do xóa tài khoản. Hành động này sẽ được ghi vào audit log.", có Textarea placeholder="Nhập lý do xóa tài khoản..." required. Sau khi xác nhận: nhân viên được xóa thành công, hiển thị thông báo "Đã xóa tài khoản và ghi nhận audit log" (toast success), dialog đóng, chuyển về danh sách nhân viên (/admin/employees), audit log được ghi nhận | FUNC-DN-02, FUNC-CTNV-01 | Pass | 11/15/2015 | |
| **FUNC-XNV-02** | Xóa nhân viên thiếu lý do | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees/[id]<br>3. Click "Xóa tài khoản"<br>4. Để trống lý do<br>5. Click "Xác nhận xóa" | Hiển thị thông báo lỗi "Vui lòng nhập lý do xóa tài khoản" (toast error), không xóa nhân viên, dialog vẫn mở | FUNC-DN-02, FUNC-CTNV-01 | Pass | 11/15/2015 | |
| **FUNC-XNV-03** | Hủy xóa nhân viên | 1. Đăng nhập Admin<br>2. Truy cập /admin/employees/[id]<br>3. Click "Xóa tài khoản"<br>4. Nhập lý do<br>5. Click "Hủy" | Dialog đóng lại, không xóa nhân viên, vẫn ở trang chi tiết nhân viên | FUNC-DN-02, FUNC-CTNV-01 | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn MDX để dễ dàng quản lý và cập nhật test cases.*
