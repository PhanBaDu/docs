# Test Case Template - Bảo mật (Admin)

## Module Code
**Giao lộ 19: Họcl6c (Admin)**

## Test Requirement
1. Khôi phục mật khẩu
2. Lịch sử đăng nhập
3. Xóa phiên đăng nhập
4. Phát hiện đăng nhập lạ

---

## Test Summary

### Người lớp Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 20 |
| **Fail** | 0 |
| **Untested** | 0 |
| **N/A** | 0 |
| **Number of Test cases** | 20 |

---

## Test Cases

### Function: Khôi phục mật khẩu

#### Check GUI: Khôi phục mật khẩu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-KPMK-01** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/auth/forgot-password<br>2. Kiểm tra tiêu đề | Hiển thị Card với CardHeader có CardTitle "Khôi phục mật khẩu Admin" với class text-2xl font-bold, CardDescription "Nhập email để nhận mã khôi phục", layout tương tự trang đăng nhập | | Pass | 11/15/2015 | |
| **GUI-KPMK-02** | Kiểm tra form khôi phục | 1. Truy cập /admin/auth/forgot-password<br>2. Kiểm tra form | Hiển thị CardContent với form chứa: Input type="email" placeholder="Email Admin" required, Button "Gửi mã khôi phục" type="submit", Link "Quay lại đăng nhập" href="/admin/auth/login" | | Pass | 11/15/2015 | |
| **GUI-KPMK-03** | Kiểm tra form nhập mã | 1. Gửi mã khôi phục thành công<br>2. Kiểm tra form | Hiển thị form nhập mã với: Input "Mã xác thực" required, Input type="password" "Mật khẩu mới" required, Input type="password" "Xác nhận mật khẩu mới" required, Button "Đặt lại mật khẩu" type="submit", Button "Hủy" variant="outline" | | Pass | 11/15/2015 | |

---

### Check FUNC: Khôi phục mật khẩu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-KPMK-01** | Gửi mã khôi phục qua email | 1. Truy cập /admin/auth/forgot-password<br>2. Nhập email đã đăng ký (VD: admin@bookstore.com)<br>3. Nhấn "Gửi mã khôi phục" | Mã khôi phục được gửi thành công qua email, hiển thị thông báo thành công "Mã khôi phục đã được gửi đến email của bạn" (toast success), form chuyển sang form nhập mã, có thể có countdown timer (VD: "Gửi lại mã sau 60 giây") | | Pass | 11/15/2015 | |
| **FUNC-KPMK-02** | Gửi mã với email không tồn tại | 1. Truy cập /admin/auth/forgot-password<br>2. Nhập email không tồn tại<br>3. Nhấn "Gửi mã khôi phục" | Hiển thị thông báo lỗi "Email không tồn tại trong hệ thống" (toast error), không gửi mã, vẫn ở form nhập email | | Pass | 11/15/2015 | |
| **FUNC-KPMK-03** | Đặt lại mật khẩu thành công | 1. Gửi mã khôi phục thành công<br>2. Nhập mã xác thực đúng (6 chữ số)<br>3. Nhập mật khẩu mới (>= 6 ký tự)<br>4. Xác nhận mật khẩu mới (khớp với mật khẩu mới)<br>5. Nhấn "Đặt lại mật khẩu" | Mật khẩu được đặt lại thành công, hiển thị thông báo thành công "Đặt lại mật khẩu thành công. Vui lòng đăng nhập lại." (toast success), chuyển đến trang đăng nhập (/admin/auth/login), có thể hiển thị thông báo "Vui lòng đăng nhập với mật khẩu mới" | FUNC-KPMK-01 | Pass | 11/15/2015 | |
| **FUNC-KPMK-04** | Đặt lại mật khẩu với mã sai | 1. Gửi mã khôi phục thành công<br>2. Nhập mã xác thực sai<br>3. Nhập mật khẩu mới<br>4. Nhấn "Đặt lại mật khẩu" | Hiển thị thông báo lỗi "Mã xác thực không đúng hoặc đã hết hạn" (toast error), không đặt lại mật khẩu, form vẫn ở trạng thái nhập mã, có thể có nút "Gửi lại mã" | FUNC-KPMK-01 | Pass | 11/15/2015 | |
| **FUNC-KPMK-05** | Đặt lại mật khẩu với mật khẩu không khớp | 1. Gửi mã khôi phục thành công<br>2. Nhập mã xác thực đúng<br>3. Nhập mật khẩu mới "password123"<br>4. Xác nhận mật khẩu mới "password456" (không khớp)<br>5. Nhấn "Đặt lại mật khẩu" | Hiển thị thông báo lỗi "Mật khẩu xác nhận không khớp" (toast error), không đặt lại mật khẩu, form vẫn ở trạng thái nhập mã | FUNC-KPMK-01 | Pass | 11/15/2015 | |
| **FUNC-KPMK-06** | Đặt lại mật khẩu với mật khẩu yếu | 1. Gửi mã khôi phục thành công<br>2. Nhập mã xác thực đúng<br>3. Nhập mật khẩu mới "123" (< 6 ký tự)<br>4. Nhấn "Đặt lại mật khẩu" | Hiển thị thông báo lỗi "Mật khẩu phải có ít nhất 6 ký tự" (toast error), không đặt lại mật khẩu | FUNC-KPMK-01 | Pass | 11/15/2015 | |

---

### Function: Lịch sử đăng nhập

#### Check GUI: Lịch sử đăng nhập

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-LSDN-01** | Kiểm tra tiêu đề trang | 1. Đăng nhập Admin<br>2. Truy cập /admin/security/login-history<br>3. Kiểm tra tiêu đề | Hiển thị tiêu đề "Lịch sử đăng nhập Admin" hoặc "Lịch sử đăng nhập" với class text-2xl font-bold, layout tương tự các trang quản lý khác | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-LSDN-02** | Kiểm tra thống kê đăng nhập | 1. Đăng nhập Admin<br>2. Truy cập /admin/security/login-history<br>3. Kiểm tra thống kê | Hiển thị grid grid-cols-1 md:grid-cols-4 gap-4 với 4 Card: Card "Tổng đăng nhập" với số liệu, Card "Hôm nay" với số liệu, Card "Tuần này" với số liệu, Card "Tháng này" với số liệu. Mỗi card có CardContent p-4 với text-sm text-muted-foreground cho label và text-xl font-semibold cho số | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-LSDN-03** | Kiểm tra card Bộ lọc | 1. Đăng nhập Admin<br>2. Truy cập /admin/security/login-history<br>3. Kiểm tra card bộ lọc | Hiển thị Card với CardContent chứa: Input tìm kiếm với icon Search, Select "Trạng thái" với các option (Tất cả, Thành công, Thất bại), 2 Input type="date" cho khoảng thời gian, Button "Áp dụng" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-LSDN-04** | Kiểm tra card Danh sách đăng nhập | 1. Đăng nhập Admin<br>2. Truy cập /admin/security/login-history<br>3. Kiểm tra card | Hiển thị Card với CardHeader có CardTitle "Danh sách đăng nhập", CardContent chứa Table | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-LSDN-05** | Kiểm tra bảng danh sách đăng nhập | 1. Đăng nhập Admin<br>2. Truy cập /admin/security/login-history<br>3. Kiểm tra bảng | Hiển thị Table với TableHeader có các TableHead: "Thời gian", "IP Address", "Trạng thái" (Badge), "Thiết bị", "Địa điểm", "Thao tác". TableBody có các TableRow với TableCell tương ứng | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Lịch sử đăng nhập

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-LSDN-01** | Xem lịch sử đăng nhập | 1. Đăng nhập Admin<br>2. Truy cập /admin/security/login-history | Hiển thị đầy đủ: thống kê 4 card (Tổng đăng nhập, Hôm nay, Tuần này, Tháng này) với số liệu, card Bộ lọc với ô tìm kiếm, dropdown Trạng thái, 2 input date, nút Áp dụng, card Danh sách đăng nhập với Table hiển thị các lần đăng nhập, mỗi hàng có Thời gian, IP Address, Trạng thái (Badge "Thành công" màu xanh hoặc "Thất bại" màu đỏ), Thiết bị (tên thiết bị + trình duyệt), Địa điểm, các nút thao tác (Xem chi tiết) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-LSDN-02** | Tìm kiếm lịch sử đăng nhập | 1. Đăng nhập Admin<br>2. Truy cập /admin/security/login-history<br>3. Nhập từ khóa tìm kiếm (VD: IP Address hoặc thiết bị)<br>4. Click nút "Áp dụng" | Danh sách đăng nhập được lọc theo từ khóa, bảng chỉ hiển thị các lần đăng nhập có IP Address, thiết bị, hoặc thông tin khác chứa từ khóa | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-LSDN-03** | Lọc lịch sử theo khoảng thời gian | 1. Đăng nhập Admin<br>2. Truy cập /admin/security/login-history<br>3. Chọn ngày bắt đầu và ngày kết thúc<br>4. Click nút "Áp dụng" | Danh sách đăng nhập được lọc theo khoảng thời gian đã chọn, bảng chỉ hiển thị các lần đăng nhập trong khoảng thời gian đó, thống kê có thể được cập nhật | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-LSDN-04** | Lọc lịch sử theo trạng thái | 1. Đăng nhập Admin<br>2. Truy cập /admin/security/login-history<br>3. Chọn trạng thái từ dropdown (VD: "Thất bại")<br>4. Click nút "Áp dụng" | Danh sách đăng nhập được lọc theo trạng thái đã chọn, bảng chỉ hiển thị các lần đăng nhập có trạng thái tương ứng (chỉ các lần đăng nhập thất bại) | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Xóa phiên đăng nhập

#### Check GUI: Xóa phiên đăng nhập

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XPDN-01** | Kiểm tra tiêu đề trang | 1. Đăng nhập Admin<br>2. Truy cập /admin/security/sessions<br>3. Kiểm tra tiêu đề | Hiển thị tiêu đề "Quản lý bảo mật" với class text-2xl font-bold, mô tả "Quản lý sessions và force logout khi phát hiện security risk" với class text-muted-foreground | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-XPDN-02** | Kiểm tra thống kê sessions | 1. Đăng nhập Admin<br>2. Truy cập /admin/security/sessions<br>3. Kiểm tra thống kê | Hiển thị grid grid-cols-1 md:grid-cols-4 gap-4 với 4 Card: Card "Tổng sessions" với số liệu, Card "Sessions đang hoạt động" với số liệu, Card "Sessions đã đóng" với số liệu, Card "Users đang online" với số liệu. Mỗi card có CardContent p-4 với text-sm text-muted-foreground cho label và text-xl font-semibold cho số | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-XPDN-03** | Kiểm tra card Force Logout Tất Cả | 1. Đăng nhập Admin<br>2. Truy cập /admin/security/sessions<br>3. Kiểm tra card | Hiển thị Card với CardHeader có CardTitle với icon Shield h-5 w-5 "Force Logout Tất Cả Sessions", CardDescription "Đóng tất cả sessions khi phát hiện security risk (đổi mật khẩu, suspicious activity)", CardContent có Alert với icon AlertCircle và AlertDescription cảnh báo, Dialog với DialogTrigger là Button variant="destructive" "Force Logout Tất Cả Sessions" có icon LogOut | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-XPDN-04** | Kiểm tra card Danh sách Sessions | 1. Đăng nhập Admin<br>2. Truy cập /admin/security/sessions<br>3. Kiểm tra card | Hiển thị Card với CardHeader có CardTitle "Danh sách Sessions", CardDescription "Quản lý và theo dõi các phiên đăng nhập", Select "Tất cả users" w-48, CardContent chứa Table | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-XPDN-05** | Kiểm tra bảng danh sách sessions | 1. Đăng nhập Admin<br>2. Truy cập /admin/security/sessions<br>3. Kiểm tra bảng | Hiển thị Table với TableHeader có các TableHead: "User", "Thiết bị", "IP Address", "Vị trí", "Hoạt động cuối", "Trạng thái", "Thao tác". TableBody có các TableRow với TableCell tương ứng | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-XPDN-06** | Kiểm tra cột User | 1. Đăng nhập Admin<br>2. Truy cập /admin/security/sessions<br>3. Kiểm tra cột | Mỗi hàng có TableCell chứa div flex items-center gap-2 với icon User h-4 w-4 text-muted-foreground, div với div font-medium (userName) và div text-xs text-muted-foreground (userId) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-XPDN-07** | Kiểm tra cột Thiết bị | 1. Đăng nhập Admin<br>2. Truy cập /admin/security/sessions<br>3. Kiểm tra cột | Mỗi hàng có TableCell chứa div flex items-center gap-2 với icon Monitor h-4 w-4 text-muted-foreground, div với div text-sm (device) và div text-xs text-muted-foreground (browser) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-XPDN-08** | Kiểm tra cột Trạng thái | 1. Đăng nhập Admin<br>2. Truy cập /admin/security/sessions<br>3. Kiểm tra cột | Mỗi hàng có TableCell chứa Badge với className="bg-green-100 text-green-800" nếu isActive=true "Đang hoạt động" hoặc className="bg-gray-100 text-gray-800" nếu isActive=false "Đã đóng" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-XPDN-09** | Kiểm tra các nút thao tác | 1. Đăng nhập Admin<br>2. Truy cập /admin/security/sessions<br>3. Kiểm tra nút thao tác | Mỗi hàng có TableCell "Thao tác" chứa Button variant="outline" size="sm" "Force Logout" có icon LogOut h-3 w-3 mr-1 onClick (chỉ hiển thị nếu isActive=true) | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Xóa phiên đăng nhập

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XPDN-01** | Xem danh sách phiên | 1. Đăng nhập Admin<br>2. Truy cập /admin/security/sessions | Hiển thị đầy đủ: thống kê 4 card (Tổng sessions, Sessions đang hoạt động, Sessions đã đóng, Users đang online) với số liệu, card Force Logout Tất Cả Sessions với Alert cảnh báo và Dialog, card Danh sách Sessions với Select lọc theo user, Table hiển thị các session, mỗi hàng có User (icon + tên + ID), Thiết bị (icon + device + browser), IP Address, Vị trí (icon + location), Hoạt động cuối (icon + lastActivity), Trạng thái (Badge), nút Force Logout (nếu đang hoạt động) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-XPDN-02** | Lọc sessions theo user | 1. Đăng nhập Admin<br>2. Truy cập /admin/security/sessions<br>3. Chọn user từ Select (VD: "Nguyễn Văn A (user-001)") | Danh sách sessions được lọc theo user đã chọn, bảng chỉ hiển thị sessions của user đó, thống kê có thể được cập nhật | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-XPDN-03** | Xóa phiên đăng nhập cụ thể | 1. Đăng nhập Admin<br>2. Truy cập /admin/security/sessions<br>3. Click nút "Force Logout" trên một session đang hoạt động<br>4. Nhập lý do vào Textarea<br>5. Click "Xác nhận Force Logout" | Hiển thị Dialog với DialogTitle "Xác nhận Force Logout", DialogDescription "Bạn có chắc chắn muốn force logout session này?", Textarea "Lý do force logout *" required placeholder="Nhập lý do...", nút "Hủy" và "Xác nhận Force Logout" variant="destructive". Sau khi xác nhận: session được force logout thành công, hiển thị thông báo thành công "Đã force logout tất cả sessions của user [userId]" (toast success), trạng thái session cập nhật thành "Đã đóng" với Badge màu xám, nút "Force Logout" biến mất, thông báo được gửi đến thiết bị bị ảnh hưởng (nếu có), dialog đóng, bảng được refresh | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-XPDN-04** | Force logout thiếu lý do | 1. Đăng nhập Admin<br>2. Truy cập /admin/security/sessions<br>3. Click nút "Force Logout"<br>4. Để trống lý do<br>5. Click "Xác nhận Force Logout" | Hiển thị thông báo lỗi "Vui lòng nhập lý do force logout" (toast error), không force logout, dialog vẫn mở | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-XPDN-05** | Đăng xuất tất cả phiên | 1. Đăng nhập Admin<br>2. Truy cập /admin/security/sessions<br>3. Click nút "Force Logout Tất Cả Sessions"<br>4. Nhập lý do vào Textarea<br>5. Click "Xác nhận Force Logout Tất Cả" | Hiển thị Dialog với DialogTitle "Xác nhận Force Logout", DialogDescription "Bạn có chắc chắn muốn force logout tất cả sessions? Tất cả users sẽ bị đăng xuất và cần đăng nhập lại.", Textarea "Lý do force logout *" required, nút "Hủy" và "Xác nhận Force Logout Tất Cả" variant="destructive". Sau khi xác nhận: tất cả sessions được force logout thành công, hiển thị thông báo thành công "Đã force logout tất cả sessions trong hệ thống" (toast success), tất cả trạng thái sessions cập nhật thành "Đã đóng", tất cả nút "Force Logout" biến mất, thống kê được cập nhật (Sessions đang hoạt động = 0, Users đang online = 0), thông báo được gửi đến tất cả thiết bị, yêu cầu đăng nhập lại, dialog đóng, bảng được refresh | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-XPDN-06** | Hủy force logout | 1. Đăng nhập Admin<br>2. Truy cập /admin/security/sessions<br>3. Click nút "Force Logout"<br>4. Nhập lý do<br>5. Click "Hủy" trong dialog | Dialog đóng lại, không force logout, trạng thái sessions không thay đổi | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Phát hiện đăng nhập lạ

#### Check FUNC: Phát hiện đăng nhập lạ

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-PHDL-01** | Hệ thống phát hiện đăng nhập lạ | 1. Đăng nhập Admin từ IP/thiết bị lạ (khác với các lần đăng nhập trước)<br>2. Truy cập /admin/security/sessions hoặc /admin/security/login-history | Hệ thống tự động phát hiện và đánh dấu đăng nhập lạ, hiển thị cảnh báo trong lịch sử đăng nhập với Badge "Đăng nhập lạ" variant="destructive" hoặc icon AlertCircle màu đỏ, có thể gửi thông báo email/SMS cho Admin về việc có đăng nhập lạ, session mới được tạo với flag "suspicious" hoặc "unusual", có thể yêu cầu xác thực 2FA bổ sung | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-PHDL-02** | Xem chi tiết đăng nhập lạ | 1. Đăng nhập Admin<br>2. Truy cập /admin/security/login-history<br>3. Click vào một đăng nhập lạ (có Badge "Đăng nhập lạ") | Hiển thị Dialog hoặc trang chi tiết với thông tin: IP Address (highlight màu đỏ), Thiết bị (highlight), Địa điểm (highlight), Thời gian, Badge "Đăng nhập lạ" variant="destructive", có thể có nút "Force Logout Session này" để đóng session nếu nghi ngờ, có thể có nút "Đánh dấu là an toàn" nếu xác nhận đây là đăng nhập hợp pháp | FUNC-DN-02, FUNC-LSDN-01 | Pass | 11/15/2015 | |
| **FUNC-PHDL-03** | Force logout session đăng nhập lạ | 1. Đăng nhập Admin<br>2. Truy cập /admin/security/sessions<br>3. Tìm session có flag "suspicious" hoặc "unusual"<br>4. Click nút "Force Logout"<br>5. Nhập lý do "Phát hiện đăng nhập lạ"<br>6. Xác nhận | Session đăng nhập lạ được force logout thành công, hiển thị thông báo thành công (toast success), trạng thái cập nhật thành "Đã đóng", thông báo được gửi đến thiết bị bị ảnh hưởng, lịch sử bảo mật được ghi nhận với hành động "Force logout session đăng nhập lạ" | FUNC-DN-02, FUNC-XPDN-03 | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn MDX để dễ dàng quản lý và cập nhật test cases.*
