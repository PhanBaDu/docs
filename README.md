# Test Case Template - Quản lý tài khoản (Nhân viên)

## Module Code
**Giao lộ 19: Họcl6c (Nhân viên)**

## Test Requirement
1. Đăng nhập hệ thống
2. Thông tin cá nhân
3. Đổi mật khẩu
4. Khôi phục mật khẩu
5. Đăng xuất

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

### Function: Đăng nhập hệ thống

#### Check GUI: Đăng nhập hệ thống

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DN-01** | Kiểm tra tiêu đề trang | 1. Truy cập /nhanvien/auth/login<br>2. Kiểm tra tiêu đề | Hiển thị div max-w-md mx-auto w-full với Card, CardHeader có CardTitle "Đăng nhập hệ thống", CardDescription "Đăng nhập vào hệ thống quản lý bán hàng với tài khoản nhân viên" | | Pass | 11/15/2015 | |
| **GUI-DN-02** | Kiểm tra trường Tên đăng nhập | 1. Truy cập /nhanvien/auth/login<br>2. Kiểm tra trường | Hiển thị div space-y-2 với Label htmlFor="username" "Tên đăng nhập hoặc email", Input id="username" placeholder="nhanvien@bookstore.com" | | Pass | 11/15/2015 | |
| **GUI-DN-03** | Kiểm tra trường Mật khẩu | 1. Truy cập /nhanvien/auth/login<br>2. Kiểm tra trường | Hiển thị div space-y-2 với Label htmlFor="password" "Mật khẩu", Input id="password" type="password" placeholder="••••••••" | | Pass | 11/15/2015 | |
| **GUI-DN-04** | Kiểm tra checkbox Ghi nhớ | 1. Truy cập /nhanvien/auth/login<br>2. Kiểm tra checkbox | Hiển thị div flex items-center justify-between với div flex items-center gap-2 chứa Checkbox id="remember", Label htmlFor="remember" className="text-sm" "Ghi nhớ đăng nhập" | | Pass | 11/15/2015 | |
| **GUI-DN-05** | Kiểm tra link Quên mật khẩu | 1. Truy cập /nhanvien/auth/login<br>2. Kiểm tra link | Hiển thị Link href="/nhanvien/auth/forgot-password" className="text-sm text-primary hover:underline" "Quên mật khẩu" | | Pass | 11/15/2015 | |
| **GUI-DN-06** | Kiểm tra nút Đăng nhập | 1. Truy cập /nhanvien/auth/login<br>2. Kiểm tra nút | Hiển thị Button className="w-full" "Đăng nhập" | | Pass | 11/15/2015 | |

---

### Check FUNC: Đăng nhập hệ thống

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DN-01** | Mở trang đăng nhập | 1. Truy cập /nhanvien/auth/login | Hiển thị đầy đủ form đăng nhập với Card, CardHeader có CardTitle "Đăng nhập hệ thống", CardDescription, CardContent space-y-4 chứa: Input "Tên đăng nhập hoặc email" placeholder="nhanvien@bookstore.com", Input type="password" "Mật khẩu" placeholder="••••••••", Checkbox "Ghi nhớ đăng nhập", Link "Quên mật khẩu" href="/nhanvien/auth/forgot-password", Button "Đăng nhập" className="w-full" | | Pass | 11/15/2015 | |
| **FUNC-DN-02** | Đăng nhập thành công | 1. Truy cập /nhanvien/auth/login<br>2. Nhập tên đăng nhập hoặc email hợp lệ (VD: "nhanvien@bookstore.com")<br>3. Nhập mật khẩu đúng<br>4. Nhấn nút "Đăng nhập" | Hệ thống xác thực thông tin đăng nhập, đăng nhập thành công, hiển thị thông báo thành công "Đăng nhập thành công" (toast success), chuyển đến trang dashboard nhân viên (/nhanvien), lưu phiên đăng nhập và token, hiển thị header với thông tin nhân viên (tên, email, role) | | Pass | 11/15/2015 | |
| **FUNC-DN-03** | Đăng nhập với tên đăng nhập không tồn tại | 1. Truy cập /nhanvien/auth/login<br>2. Nhập tên đăng nhập hoặc email không tồn tại<br>3. Nhập mật khẩu<br>4. Nhấn "Đăng nhập" | Hiển thị thông báo lỗi "Tên đăng nhập hoặc mật khẩu không đúng" (toast error), không chuyển trang, vẫn ở trang đăng nhập | | Pass | 11/15/2015 | |
| **FUNC-DN-04** | Đăng nhập với mật khẩu sai | 1. Truy cập /nhanvien/auth/login<br>2. Nhập tên đăng nhập hoặc email hợp lệ<br>3. Nhập mật khẩu sai<br>4. Nhấn "Đăng nhập" | Hiển thị thông báo lỗi "Tên đăng nhập hoặc mật khẩu không đúng" (toast error), không chuyển trang | | Pass | 11/15/2015 | |
| **FUNC-DN-05** | Đăng nhập thiếu tên đăng nhập | 1. Truy cập /nhanvien/auth/login<br>2. Để trống tên đăng nhập<br>3. Nhập mật khẩu<br>4. Nhấn "Đăng nhập" | Trình duyệt hiển thị cảnh báo "Please fill out this field" trên trường Input username, form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-DN-06** | Đăng nhập thiếu mật khẩu | 1. Truy cập /nhanvien/auth/login<br>2. Nhập tên đăng nhập<br>3. Để trống mật khẩu<br>4. Nhấn "Đăng nhập" | Trình duyệt hiển thị cảnh báo "Please fill out this field" trên trường Input password, form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-DN-07** | Đăng nhập với tài khoản bị khóa | 1. Truy cập /nhanvien/auth/login<br>2. Nhập tên đăng nhập của tài khoản bị khóa<br>3. Nhập mật khẩu<br>4. Nhấn "Đăng nhập" | Hiển thị thông báo lỗi "Tài khoản đã bị khóa" (toast error), không chuyển trang | | Pass | 11/15/2015 | |
| **FUNC-DN-08** | Chức năng ghi nhớ - Có tích chọn | 1. Truy cập /nhanvien/auth/login<br>2. Tích checkbox "Ghi nhớ đăng nhập"<br>3. Nhập thông tin hợp lệ<br>4. Đăng nhập | Đăng nhập thành công, trình duyệt lưu cookie với thời hạn dài hơn (VD: 30 ngày), lần sau truy cập tự động điền thông tin đăng nhập | | Pass | 11/15/2015 | |
| **FUNC-DN-09** | Chức năng ghi nhớ - Không tích chọn | 1. Truy cập /nhanvien/auth/login<br>2. Không tích checkbox<br>3. Nhập thông tin hợp lệ<br>4. Đăng nhập | Đăng nhập thành công, trình duyệt lưu cookie với thời hạn ngắn hơn (VD: session), lần sau truy cập không tự động điền thông tin | | Pass | 11/15/2015 | |
| **FUNC-DN-10** | Nhấn link Quên mật khẩu | 1. Truy cập /nhanvien/auth/login<br>2. Nhấn link "Quên mật khẩu" | Chuyển đến trang /nhanvien/auth/forgot-password | | Pass | 11/15/2015 | |
| **FUNC-DN-11** | Submit form bằng phím Enter | 1. Truy cập /nhanvien/auth/login<br>2. Nhập thông tin hợp lệ<br>3. Nhấn Enter trong trường mật khẩu | Form được gửi, xử lý đăng nhập như khi nhấn nút "Đăng nhập" | | Pass | 11/15/2015 | |

---

### Function: Thông tin cá nhân

#### Check GUI: Thông tin cá nhân

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-TTCN-01** | Kiểm tra tiêu đề trang | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/account<br>3. Kiểm tra tiêu đề | Hiển thị div grid gap-6 lg:grid-cols-2 với Card, CardHeader có CardTitle "Thông tin cá nhân", CardDescription "Quản lý và cập nhật thông tin của bạn" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-TTCN-02** | Kiểm tra thông tin cơ bản | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/account<br>3. Kiểm tra thông tin | Hiển thị CardContent space-y-4 với div grid grid-cols-2 gap-4 chứa: div với div text-sm text-muted-foreground "Họ và tên", div font-medium (tên nhân viên), div với div text-sm text-muted-foreground "Email", div font-medium (email), div với div text-sm text-muted-foreground "Số điện thoại", div font-medium (số điện thoại), div với div text-sm text-muted-foreground "Chức vụ", div font-medium với Badge (chức vụ), div với div text-sm text-muted-foreground "Ngày vào làm", div font-medium (ngày), div với div text-sm text-muted-foreground "Trạng thái", div font-medium với Badge variant="default" (trạng thái) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-TTCN-03** | Kiểm tra form Cập nhật thông tin | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/account<br>3. Kiểm tra form | Hiển thị div pt-2 với div text-sm font-medium mb-2 "Cập nhật thông tin", div grid gap-3 chứa: div grid gap-1 với Label htmlFor="phone" "Số điện thoại", Input id="phone" defaultValue, div grid gap-1 với Label htmlFor="address" "Địa chỉ", Input id="address" placeholder="Số nhà, đường, quận/huyện, tỉnh/thành", Button className="w-fit" "Lưu thay đổi" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-TTCN-04** | Kiểm tra card Lịch sử hoạt động | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/account<br>3. Kiểm tra card | Hiển thị Card với CardHeader có CardTitle "Lịch sử hoạt động gần đây", CardDescription "Theo dõi đăng nhập và thao tác", CardContent space-y-3 với các div text-sm chứa thông tin hoạt động (thời gian, hoạt động, IP) | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Thông tin cá nhân

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TTCN-01** | Xem thông tin cá nhân | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/account | Hiển thị đầy đủ: card Thông tin cá nhân với thông tin cơ bản (Họ và tên, Email, Số điện thoại, Chức vụ với Badge, Ngày vào làm, Trạng thái với Badge variant="default"), form Cập nhật thông tin với Input số điện thoại và địa chỉ, nút "Lưu thay đổi", card Lịch sử hoạt động gần đây với các hoạt động (thời gian, loại hoạt động, IP) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TTCN-02** | Cập nhật số điện thoại | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/account<br>3. Sửa số điện thoại trong Input<br>4. Click "Lưu thay đổi" | Số điện thoại được cập nhật thành công, hiển thị thông báo thành công "Cập nhật thông tin thành công" (toast success), thông tin trong card "Thông tin cơ bản" được cập nhật, lịch sử hoạt động ghi nhận "Cập nhật thông tin cá nhân" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TTCN-03** | Cập nhật địa chỉ | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/account<br>3. Nhập địa chỉ vào Input<br>4. Click "Lưu thay đổi" | Địa chỉ được cập nhật thành công, hiển thị thông báo thành công (toast success), lịch sử hoạt động ghi nhận | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TTCN-04** | Cập nhật với số điện thoại không hợp lệ | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/account<br>3. Nhập số điện thoại không hợp lệ (VD: "123")<br>4. Click "Lưu thay đổi" | Hiển thị thông báo lỗi "Số điện thoại không hợp lệ" (toast error), không cập nhật thông tin | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TTCN-05** | Xem lịch sử hoạt động | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/account<br>3. Xem card Lịch sử hoạt động | Hiển thị danh sách các hoạt động gần đây với format "YYYY-MM-DD HH:mm • [Hoạt động] • IP [IP Address]" hoặc "YYYY-MM-DD HH:mm • [Hoạt động]", các hoạt động được sắp xếp từ mới đến cũ, có thể có nhiều hoạt động (Đăng nhập, Tạo đơn hàng, Cập nhật tồn kho, v.v.) | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Đổi mật khẩu

#### Check GUI: Đổi mật khẩu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DMK-01** | Kiểm tra tiêu đề trang | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/account/change-password<br>3. Kiểm tra tiêu đề | Hiển thị div max-w-md mx-auto w-full với Card, CardHeader có CardTitle "Đổi mật khẩu", CardDescription "Mật khẩu phải có ít nhất 8 ký tự, gồm chữ hoa, chữ thường, số và ký tự đặc biệt" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DMK-02** | Kiểm tra trường Mật khẩu hiện tại | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/account/change-password<br>3. Kiểm tra trường | Hiển thị div space-y-2 với Label htmlFor="current" "Mật khẩu hiện tại", Input id="current" type="password" placeholder="••••••••" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DMK-03** | Kiểm tra trường Mật khẩu mới | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/account/change-password<br>3. Kiểm tra trường | Hiển thị div space-y-2 với Label htmlFor="new" "Mật khẩu mới", Input id="new" type="password" placeholder="••••••••" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DMK-04** | Kiểm tra trường Xác nhận mật khẩu mới | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/account/change-password<br>3. Kiểm tra trường | Hiển thị div space-y-2 với Label htmlFor="confirm" "Xác nhận mật khẩu mới", Input id="confirm" type="password" placeholder="••••••••" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DMK-05** | Kiểm tra các nút | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/account/change-password<br>3. Kiểm tra nút | Hiển thị div flex gap-2 với Button "Đổi mật khẩu", Button variant="outline" "Hủy" | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Đổi mật khẩu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DMK-01** | Đổi mật khẩu thành công | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/account/change-password<br>3. Nhập mật khẩu hiện tại đúng<br>4. Nhập mật khẩu mới đủ mạnh (>= 8 ký tự, có chữ hoa, chữ thường, số, ký tự đặc biệt)<br>5. Xác nhận mật khẩu mới (khớp với mật khẩu mới)<br>6. Click "Đổi mật khẩu" | Mật khẩu được đổi thành công, hiển thị thông báo thành công "Đổi mật khẩu thành công" (toast success), tự động đăng xuất khỏi tất cả các phiên đăng nhập khác để bảo mật, gửi thông báo xác nhận qua email (nếu được cấu hình), lịch sử thay đổi mật khẩu được ghi lại, chuyển về trang đăng nhập hoặc trang tài khoản | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DMK-02** | Đổi mật khẩu với mật khẩu hiện tại sai | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/account/change-password<br>3. Nhập mật khẩu hiện tại sai<br>4. Nhập mật khẩu mới<br>5. Click "Đổi mật khẩu" | Hiển thị thông báo lỗi "Mật khẩu hiện tại không đúng" (toast error), không đổi mật khẩu | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DMK-03** | Đổi mật khẩu với mật khẩu mới không đủ mạnh | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/account/change-password<br>3. Nhập mật khẩu hiện tại đúng<br>4. Nhập mật khẩu mới yếu (VD: "123456")<br>5. Click "Đổi mật khẩu" | Hiển thị thông báo lỗi "Mật khẩu mới không đủ mạnh. Mật khẩu phải có ít nhất 8 ký tự, gồm chữ hoa, chữ thường, số và ký tự đặc biệt" (toast error), không đổi mật khẩu | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DMK-04** | Đổi mật khẩu với xác nhận không khớp | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/account/change-password<br>3. Nhập mật khẩu hiện tại đúng<br>4. Nhập mật khẩu mới "Password123!"<br>5. Xác nhận mật khẩu mới "Password456!" (không khớp)<br>6. Click "Đổi mật khẩu" | Hiển thị thông báo lỗi "Xác nhận mật khẩu không khớp" (toast error), không đổi mật khẩu | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DMK-05** | Hủy đổi mật khẩu | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/account/change-password<br>3. Nhập thông tin<br>4. Click "Hủy" | Chuyển về trang /nhanvien/account, không đổi mật khẩu, form được reset | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Khôi phục mật khẩu

#### Check GUI: Khôi phục mật khẩu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-KPMK-01** | Kiểm tra tiêu đề trang | 1. Truy cập /nhanvien/auth/forgot-password<br>2. Kiểm tra tiêu đề | Hiển thị div max-w-md mx-auto w-full với Card, CardHeader có CardTitle "Khôi phục mật khẩu", CardDescription "Nhập email để nhận liên kết đặt lại mật khẩu (liên kết có thời hạn)" | | Pass | 11/15/2015 | |
| **GUI-KPMK-02** | Kiểm tra form khôi phục | 1. Truy cập /nhanvien/auth/forgot-password<br>2. Kiểm tra form | Hiển thị CardContent space-y-4 với div space-y-2 chứa Label htmlFor="email" "Email", Input id="email" type="email" placeholder="nhanvien@bookstore.com", Button className="w-full" "Gửi liên kết đặt lại mật khẩu" | | Pass | 11/15/2015 | |

---

### Check FUNC: Khôi phục mật khẩu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-KPMK-01** | Gửi liên kết đặt lại mật khẩu thành công | 1. Truy cập /nhanvien/auth/forgot-password<br>2. Nhập email đã đăng ký (VD: "nhanvien@bookstore.com")<br>3. Nhấn "Gửi liên kết đặt lại mật khẩu" | Email chứa liên kết đặt lại mật khẩu được gửi thành công, hiển thị thông báo thành công "Liên kết đặt lại mật khẩu đã được gửi đến email của bạn" (toast success), liên kết có thời hạn sử dụng (VD: 1 giờ), có thể có countdown timer | | Pass | 11/15/2015 | |
| **FUNC-KPMK-02** | Gửi với email không tồn tại | 1. Truy cập /nhanvien/auth/forgot-password<br>2. Nhập email không tồn tại<br>3. Nhấn "Gửi liên kết đặt lại mật khẩu" | Hiển thị thông báo lỗi "Email không tồn tại trong hệ thống" (toast error), không gửi email | | Pass | 11/15/2015 | |
| **FUNC-KPMK-03** | Gửi với email sai định dạng | 1. Truy cập /nhanvien/auth/forgot-password<br>2. Nhập email sai định dạng (VD: "invalid-email")<br>3. Nhấn "Gửi liên kết đặt lại mật khẩu" | Trình duyệt hiển thị cảnh báo "Please include an '@' in the email address", form không được gửi | | Pass | 11/15/2015 | |

---

### Function: Đăng xuất

#### Check FUNC: Đăng xuất

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DX-01** | Đăng xuất thành công | 1. Đăng nhập Nhân viên<br>2. Click "Đăng xuất" từ menu hoặc truy cập /nhanvien/logout<br>3. Xác nhận đăng xuất (nếu có Dialog) | Hiển thị Dialog xác nhận (nếu có) với DialogTitle "Xác nhận đăng xuất", DialogDescription "Bạn có chắc chắn muốn đăng xuất khỏi hệ thống?", nút "Hủy" và "Có, đăng xuất". Sau khi xác nhận: đăng xuất thành công, kết thúc phiên đăng nhập hiện tại, xóa thông tin phiên đăng nhập khỏi hệ thống, ghi lại lịch sử đăng xuất với thời gian và địa chỉ IP, chuyển hướng về trang đăng nhập (/nhanvien/auth/login), hiển thị thông báo xác nhận "Đăng xuất thành công" (toast success), tất cả dữ liệu nhạy cảm được xóa khỏi bộ nhớ tạm thời của trình duyệt | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DX-02** | Hủy đăng xuất | 1. Đăng nhập Nhân viên<br>2. Click "Đăng xuất"<br>3. Click "Hủy" trong Dialog | Dialog đóng lại, không đăng xuất, vẫn ở trang hiện tại | FUNC-DN-02 | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn MDX để dễ dàng quản lý và cập nhật test cases.*

