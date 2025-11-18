# Test Case Template - Quản lý tài khoản (User)

## Module Code
**USER-001: Quản lý tài khoản (User)**

## Test Requirement
1. Đăng ký tài khoản
2. Đăng nhập hệ thống
3. Quên mật khẩu / Khôi phục mật khẩu
4. Quản lý thông tin cá nhân
5. Đổi mật khẩu
6. Xem điểm tích lũy và hạng thành viên
7. Đăng xuất hệ thống

---

## Test Summary

### Người thực hiện Test: Tester

| Status | Count |
|--------|-------|
| **Pass** | 78 |
| **Fail** | 0 |
| **Untested** | 0 |
| **N/A** | 0 |
| **Number of Test cases** | 78 |

---

## Test Cases

### Function: Đăng ký tài khoản

#### Check GUI: Đăng ký tài khoản

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DK-01** | Kiểm tra tiêu đề trang đăng ký | 1. Truy cập /user/auth/register<br>2. Kiểm tra tiêu đề | Hiển thị Card với CardHeader, CardTitle "Đăng ký tài khoản" (text-xl font-bold), CardDescription "Tạo tài khoản mới để bắt đầu mua sắm tại Book Store" | | Pass | 11/15/2015 | |
| **GUI-DK-02** | Kiểm tra phần upload ảnh đại diện | 1. Truy cập /user/auth/register<br>2. Kiểm tra phần avatar | Hiển thị Avatar component (h-16 w-16) ở giữa, có nút Camera (h-6 w-6) ở góc dưới bên phải, AvatarFallback hiển thị icon User2 | | Pass | 11/15/2015 | |
| **GUI-DK-03** | Kiểm tra trường Họ và tên | 1. Truy cập /user/auth/register<br>2. Kiểm tra trường Họ và tên | Hiển thị Label với icon User (h-3 w-3) và text "Họ và tên *", Input type text với placeholder "Nhập họ và tên", required, className h-9 | | Pass | 11/15/2015 | |
| **GUI-DK-04** | Kiểm tra trường Email | 1. Truy cập /user/auth/register<br>2. Kiểm tra trường Email | Hiển thị Label với icon Mail (h-3 w-3) và text "Email *", Input type email với placeholder "Nhập email", required, className h-9 | | Pass | 11/15/2015 | |
| **GUI-DK-05** | Kiểm tra trường Số điện thoại | 1. Truy cập /user/auth/register<br>2. Kiểm tra trường Số điện thoại | Hiển thị Label với icon Phone (h-3 w-3) và text "Số điện thoại *", Input type tel với placeholder "Nhập số điện thoại", required, className h-9 | | Pass | 11/15/2015 | |
| **GUI-DK-06** | Kiểm tra trường Giới tính | 1. Truy cập /user/auth/register<br>2. Kiểm tra trường Giới tính | Hiển thị Label với icon User2 (h-3 w-3) và text "Giới tính", Select component với SelectTrigger (h-9), SelectValue placeholder "Chọn giới tính", SelectContent có 3 options: Nam, Nữ, Khác | | Pass | 11/15/2015 | |
| **GUI-DK-07** | Kiểm tra trường Ngày sinh | 1. Truy cập /user/auth/register<br>2. Kiểm tra trường Ngày sinh | Hiển thị Label với icon Calendar (h-3 w-3) và text "Ngày sinh", Input type date, className h-9 w-full | | Pass | 11/15/2015 | |
| **GUI-DK-08** | Kiểm tra trường Địa chỉ | 1. Truy cập /user/auth/register<br>2. Kiểm tra trường Địa chỉ | Hiển thị Label với icon MapPin (h-3 w-3) và text "Địa chỉ", Input type text với placeholder "Nhập địa chỉ", className h-9 w-full | | Pass | 11/15/2015 | |
| **GUI-DK-09** | Kiểm tra trường Mật khẩu | 1. Truy cập /user/auth/register<br>2. Kiểm tra trường Mật khẩu | Hiển thị Label "Mật khẩu *", Input type password với placeholder "Nhập mật khẩu", required, className h-9 pr-10, có nút Eye/EyeOff ở bên phải để hiện/ẩn mật khẩu | | Pass | 11/15/2015 | |
| **GUI-DK-10** | Kiểm tra trường Xác nhận mật khẩu | 1. Truy cập /user/auth/register<br>2. Kiểm tra trường Xác nhận mật khẩu | Hiển thị Label "Xác nhận mật khẩu *", Input type password với placeholder "Nhập lại mật khẩu", required, className h-9 pr-10, có nút Eye/EyeOff ở bên phải | | Pass | 11/15/2015 | |
| **GUI-DK-11** | Kiểm tra checkbox Điều khoản | 1. Truy cập /user/auth/register<br>2. Kiểm tra checkbox | Hiển thị Checkbox với Label "Tôi đồng ý với Điều khoản sử dụng và Chính sách bảo mật", có link đến /terms và /privacy | | Pass | 11/15/2015 | |
| **GUI-DK-12** | Kiểm tra thông báo yêu cầu bảo mật | 1. Truy cập /user/auth/register<br>2. Kiểm tra phần thông báo | Hiển thị div với className "bg-blue-50 border border-blue-200 rounded-lg p-3", chứa thông tin về yêu cầu bảo mật: mật khẩu, email, số điện thoại, họ tên, địa chỉ | | Pass | 11/15/2015 | |
| **GUI-DK-13** | Kiểm tra nút Đăng ký | 1. Truy cập /user/auth/register<br>2. Kiểm tra nút đăng ký | Hiển thị Button với text "Đăng ký tài khoản" hoặc "Đang tạo tài khoản..." khi isLoading, className w-full, type submit | | Pass | 11/15/2015 | |
| **GUI-DK-14** | Kiểm tra nút đăng nhập xã hội | 1. Truy cập /user/auth/register<br>2. Kiểm tra phần đăng nhập xã hội | Hiển thị Separator với text "Hoặc", có 2 Button variant outline: "Đăng ký với Google" và "Đăng ký với Facebook", className w-full h-9 text-sm | | Pass | 11/15/2015 | |
| **GUI-DK-15** | Kiểm tra link đăng nhập | 1. Truy cập /user/auth/register<br>2. Kiểm tra link đăng nhập | Hiển thị text "Đã có tài khoản? " và Link đến /user/auth/login với text "Đăng nhập ngay" | | Pass | 11/15/2015 | |

#### Check FUNC: Đăng ký tài khoản

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DK-01** | Mở trang đăng ký | 1. Truy cập /user/auth/register | Hiển thị form đăng ký với Card component, các trường: avatar upload, họ tên, email, số điện thoại, giới tính, ngày sinh, địa chỉ, mật khẩu, xác nhận mật khẩu, checkbox điều khoản, nút đăng ký, các nút đăng nhập xã hội, link đăng nhập | | Pass | 11/15/2015 | |
| **FUNC-DK-02** | Đăng ký thành công với thông tin hợp lệ | 1. Truy cập /user/auth/register<br>2. Nhập đầy đủ thông tin hợp lệ<br>3. Tích checkbox điều khoản<br>4. Nhấn nút Đăng ký | Hiển thị toast.success "Đăng ký tài khoản thành công!", sau đó redirect đến /user/auth/login. Email xác nhận được gửi thành công | | Pass | 11/15/2015 | |
| **FUNC-DK-03** | Đăng ký thiếu họ tên | 1. Truy cập /user/auth/register<br>2. Để trống họ tên<br>3. Nhập các trường khác<br>4. Nhấn Đăng ký | Hiển thị toast.error "Họ tên không được để trống", form không được submit | | Pass | 11/15/2015 | |
| **FUNC-DK-04** | Đăng ký với họ tên quá ngắn | 1. Truy cập /user/auth/register<br>2. Nhập họ tên chỉ 1 ký tự<br>3. Nhập các trường khác hợp lệ<br>4. Nhấn Đăng ký | Hiển thị toast.error "Họ tên phải từ 2 đến 100 ký tự", form không được submit | | Pass | 11/15/2015 | |
| **FUNC-DK-05** | Đăng ký với email không hợp lệ | 1. Truy cập /user/auth/register<br>2. Nhập email không đúng định dạng RFC 5322<br>3. Nhập các trường khác hợp lệ<br>4. Nhấn Đăng ký | Hiển thị toast.error "Email không hợp lệ (theo chuẩn RFC 5322)", form không được submit | | Pass | 11/15/2015 | |
| **FUNC-DK-06** | Đăng ký với số điện thoại không hợp lệ | 1. Truy cập /user/auth/register<br>2. Nhập số điện thoại không đúng định dạng Việt Nam<br>3. Nhập các trường khác hợp lệ<br>4. Nhấn Đăng ký | Hiển thị toast.error "Số điện thoại không hợp lệ (định dạng: 0xxxxxxxxx hoặc +84xxxxxxxxx)", form không được submit | | Pass | 11/15/2015 | |
| **FUNC-DK-07** | Đăng ký với mật khẩu yếu | 1. Truy cập /user/auth/register<br>2. Nhập mật khẩu không đủ 8 ký tự<br>3. Nhập các trường khác hợp lệ<br>4. Nhấn Đăng ký | Hiển thị toast.error "Mật khẩu phải có ít nhất 8 ký tự", form không được submit | | Pass | 11/15/2015 | |
| **FUNC-DK-08** | Đăng ký với mật khẩu thiếu chữ hoa | 1. Truy cập /user/auth/register<br>2. Nhập mật khẩu không có chữ hoa<br>3. Nhập các trường khác hợp lệ<br>4. Nhấn Đăng ký | Hiển thị toast.error "Mật khẩu phải có ít nhất 1 chữ hoa", form không được submit | | Pass | 11/15/2015 | |
| **FUNC-DK-09** | Đăng ký với mật khẩu xác nhận không khớp | 1. Truy cập /user/auth/register<br>2. Nhập mật khẩu và mật khẩu xác nhận khác nhau<br>3. Nhập các trường khác hợp lệ<br>4. Nhấn Đăng ký | Hiển thị toast.error "Mật khẩu xác nhận không khớp", form không được submit | | Pass | 11/15/2015 | |
| **FUNC-DK-10** | Đăng ký không tích checkbox điều khoản | 1. Truy cập /user/auth/register<br>2. Nhập đầy đủ thông tin hợp lệ<br>3. Không tích checkbox điều khoản<br>4. Nhấn Đăng ký | Hiển thị toast.error "Vui lòng đồng ý với điều khoản sử dụng", form không được submit | | Pass | 11/15/2015 | |
| **FUNC-DK-11** | Upload ảnh đại diện quá lớn | 1. Truy cập /user/auth/register<br>2. Click nút Camera<br>3. Chọn file ảnh > 5MB<br>4. Xác nhận | Hiển thị toast.error "Kích thước ảnh không được vượt quá 5MB", file không được chấp nhận | | Pass | 11/15/2015 | |
| **FUNC-DK-12** | Upload file không phải ảnh | 1. Truy cập /user/auth/register<br>2. Click nút Camera<br>3. Chọn file không phải ảnh<br>4. Xác nhận | Hiển thị toast.error "Vui lòng chọn file ảnh hợp lệ", file không được chấp nhận | | Pass | 11/15/2015 | |
| **FUNC-DK-13** | Hiện/Ẩn mật khẩu | 1. Truy cập /user/auth/register<br>2. Nhập mật khẩu<br>3. Click nút Eye | Input type chuyển từ password sang text, icon chuyển từ Eye sang EyeOff | | Pass | 11/15/2015 | |
| **FUNC-DK-14** | Gửi email xác nhận với retry mechanism | 1. Truy cập /user/auth/register<br>2. Nhập đầy đủ thông tin hợp lệ<br>3. Nhấn Đăng ký<br>4. Giả lập lỗi gửi email lần đầu | Hệ thống tự động retry gửi email tối đa 3 lần, mỗi lần cách nhau 30 giây. Nếu vẫn lỗi, hiển thị toast.warning "Không thể gửi email xác nhận. Vui lòng liên hệ admin để kích hoạt tài khoản." | | Pass | 11/15/2015 | |
| **FUNC-DK-15** | Xử lý lỗi mạng khi đăng ký | 1. Truy cập /user/auth/register<br>2. Nhập đầy đủ thông tin hợp lệ<br>3. Giả lập lỗi mạng<br>4. Nhấn Đăng ký | Hệ thống tự động retry tối đa 3 lần, mỗi lần cách nhau 2 giây. Hiển thị toast.warning "Lỗi kết nối. Đang thử lại... (x/3)". Nếu vẫn lỗi, hiển thị toast.error "Có lỗi xảy ra, vui lòng thử lại sau" | | Pass | 11/15/2015 | |

### Function: Đăng nhập hệ thống

#### Check GUI: Đăng nhập

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DN-01** | Kiểm tra tiêu đề trang đăng nhập | 1. Truy cập /user/auth/login<br>2. Kiểm tra tiêu đề | Hiển thị Card với CardHeader, CardTitle "Đăng nhập" (text-2xl font-bold), CardDescription "Đăng nhập vào tài khoản của bạn để tiếp tục mua sắm" | | Pass | 11/15/2015 | |
| **GUI-DN-02** | Kiểm tra trường Email | 1. Truy cập /user/auth/login<br>2. Kiểm tra trường Email | Hiển thị Label "Email", Input type email với placeholder "Nhập email của bạn", required, disabled khi isLocked | | Pass | 11/15/2015 | |
| **GUI-DN-03** | Kiểm tra trường Mật khẩu | 1. Truy cập /user/auth/login<br>2. Kiểm tra trường Mật khẩu | Hiển thị Label "Mật khẩu", Input type password với placeholder "Nhập mật khẩu", required, className pr-10, có nút Eye/EyeOff ở bên phải, disabled khi isLocked | | Pass | 11/15/2015 | |
| **GUI-DN-04** | Kiểm tra checkbox Ghi nhớ | 1. Truy cập /user/auth/login<br>2. Kiểm tra checkbox | Hiển thị Checkbox với Label "Ghi nhớ đăng nhập" (text-sm) | | Pass | 11/15/2015 | |
| **GUI-DN-05** | Kiểm tra link Quên mật khẩu | 1. Truy cập /user/auth/login<br>2. Kiểm tra link | Hiển thị Link đến /user/auth/forgot-password với text "Quên mật khẩu?" (text-sm text-primary hover:underline) | | Pass | 11/15/2015 | |
| **GUI-DN-06** | Kiểm tra nút Đăng nhập | 1. Truy cập /user/auth/login<br>2. Kiểm tra nút | Hiển thị Button với text "Đăng nhập" hoặc "Đang đăng nhập..." khi isLoading, className w-full, type submit, disabled khi isLoading hoặc isLocked | | Pass | 11/15/2015 | |
| **GUI-DN-07** | Kiểm tra cảnh báo tài khoản bị khóa | 1. Truy cập /user/auth/login<br>2. Đăng nhập sai 5 lần<br>3. Kiểm tra cảnh báo | Hiển thị Alert variant destructive với icon AlertCircle, AlertDescription hiển thị "Tài khoản bị khóa do quá nhiều lần đăng nhập sai. Vui lòng thử lại sau X phút." | | Pass | 11/15/2015 | |
| **GUI-DN-08** | Kiểm tra cảnh báo CAPTCHA | 1. Truy cập /user/auth/login<br>2. Đăng nhập sai 3 lần<br>3. Kiểm tra cảnh báo | Hiển thị Alert với icon Shield, AlertDescription "Đã có X lần đăng nhập sai. Vui lòng nhập CAPTCHA để tiếp tục." | | Pass | 11/15/2015 | |
| **GUI-DN-09** | Kiểm tra phần CAPTCHA | 1. Truy cập /user/auth/login<br>2. Đăng nhập sai 3 lần<br>3. Kiểm tra phần CAPTCHA | Hiển thị div với className "space-y-2 p-4 bg-muted rounded-lg", có Label "Nhập CAPTCHA để tiếp tục", div hiển thị phép tính (font-mono text-lg), Input để nhập kết quả (w-24), Button "Làm mới" | | Pass | 11/15/2015 | |
| **GUI-DN-10** | Kiểm tra nút đăng nhập xã hội | 1. Truy cập /user/auth/login<br>2. Kiểm tra phần đăng nhập xã hội | Hiển thị Separator với text "Hoặc", có 2 Button variant outline: "Đăng nhập với Google" và "Đăng nhập với Facebook", className w-full | | Pass | 11/15/2015 | |
| **GUI-DN-11** | Kiểm tra link đăng ký | 1. Truy cập /user/auth/login<br>2. Kiểm tra link | Hiển thị text "Chưa có tài khoản? " và Link đến /user/auth/register với text "Đăng ký ngay" | | Pass | 11/15/2015 | |

#### Check FUNC: Đăng nhập

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DN-01** | Mở trang đăng nhập | 1. Truy cập /user/auth/login | Hiển thị form đăng nhập với Card component, các trường: email, mật khẩu, checkbox ghi nhớ, link quên mật khẩu, nút đăng nhập, các nút đăng nhập xã hội, link đăng ký | | Pass | 11/15/2015 | |
| **FUNC-DN-02** | Đăng nhập thành công | 1. Truy cập /user/auth/login<br>2. Nhập email hợp lệ<br>3. Nhập mật khẩu đúng<br>4. Nhấn nút Đăng nhập | Hiển thị toast.success "Đăng nhập thành công!", sau đó redirect đến /user. Phiên đăng nhập được tạo và lưu trữ | | Pass | 11/15/2015 | |
| **FUNC-DN-03** | Đăng nhập với email không tồn tại | 1. Truy cập /user/auth/login<br>2. Nhập email "wrong@example.com"<br>3. Nhập mật khẩu<br>4. Nhấn Đăng nhập | Hiển thị toast.error "Sai email hoặc mật khẩu. Còn X lần thử.", failedAttempts tăng lên 1, không chuyển trang | | Pass | 11/15/2015 | |
| **FUNC-DN-04** | Đăng nhập với mật khẩu sai | 1. Truy cập /user/auth/login<br>2. Nhập email hợp lệ<br>3. Nhập mật khẩu "wrong"<br>4. Nhấn Đăng nhập | Hiển thị toast.error "Sai email hoặc mật khẩu. Còn X lần thử.", failedAttempts tăng lên 1, không chuyển trang | | Pass | 11/15/2015 | |
| **FUNC-DN-05** | Đăng nhập thiếu email | 1. Truy cập /user/auth/login<br>2. Để trống email<br>3. Nhập mật khẩu<br>4. Nhấn Đăng nhập | Trình duyệt hiển thị cảnh báo "Please fill out this field", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-DN-06** | Đăng nhập thiếu mật khẩu | 1. Truy cập /user/auth/login<br>2. Nhập email<br>3. Để trống mật khẩu<br>4. Nhấn Đăng nhập | Trình duyệt hiển thị cảnh báo "Please fill out this field", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-DN-07** | Đăng nhập với email sai định dạng | 1. Truy cập /user/auth/login<br>2. Nhập email không đúng định dạng<br>3. Nhập mật khẩu<br>4. Nhấn Đăng nhập | Trình duyệt hiển thị cảnh báo "Please include an '@' in the email address", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-DN-08** | Hiện/Ẩn mật khẩu | 1. Truy cập /user/auth/login<br>2. Nhập mật khẩu<br>3. Click nút Eye | Input type chuyển từ password sang text, icon chuyển từ Eye sang EyeOff | | Pass | 11/15/2015 | |
| **FUNC-DN-09** | Chức năng ghi nhớ - Có tích chọn | 1. Truy cập /user/auth/login<br>2. Tích checkbox "Ghi nhớ đăng nhập"<br>3. Nhập thông tin hợp lệ<br>4. Đăng nhập | Đăng nhập thành công, thông tin đăng nhập được lưu với thời hạn dài hơn | | Pass | 11/15/2015 | |
| **FUNC-DN-10** | Chức năng ghi nhớ - Không tích chọn | 1. Truy cập /user/auth/login<br>2. Không tích checkbox<br>3. Nhập thông tin hợp lệ<br>4. Đăng nhập | Đăng nhập thành công, thông tin đăng nhập được lưu với thời hạn ngắn hơn | | Pass | 11/15/2015 | |
| **FUNC-DN-11** | Hiển thị CAPTCHA sau 3 lần đăng nhập sai | 1. Truy cập /user/auth/login<br>2. Đăng nhập sai 3 lần | Hiển thị Alert cảnh báo, phần CAPTCHA xuất hiện với phép tính ngẫu nhiên, Input để nhập kết quả, Button "Làm mới" | | Pass | 11/15/2015 | |
| **FUNC-DN-12** | Đăng nhập với CAPTCHA đúng | 1. Truy cập /user/auth/login<br>2. Đăng nhập sai 3 lần<br>3. Nhập CAPTCHA đúng<br>4. Nhập thông tin đăng nhập đúng<br>5. Nhấn Đăng nhập | Đăng nhập thành công, chuyển đến /user | | Pass | 11/15/2015 | |
| **FUNC-DN-13** | Đăng nhập với CAPTCHA sai | 1. Truy cập /user/auth/login<br>2. Đăng nhập sai 3 lần<br>3. Nhập CAPTCHA sai<br>4. Nhấn Đăng nhập | Hiển thị toast.error "Mã CAPTCHA không đúng", CAPTCHA được tạo lại, Input CAPTCHA được xóa | | Pass | 11/15/2015 | |
| **FUNC-DN-14** | Khóa tài khoản sau 5 lần đăng nhập sai | 1. Truy cập /user/auth/login<br>2. Đăng nhập sai 5 lần | Hiển thị Alert variant destructive "Tài khoản bị khóa do quá nhiều lần đăng nhập sai. Vui lòng thử lại sau 30 phút.", isLocked = true, lockUntil được set 30 phút sau, các trường input bị disabled | | Pass | 11/15/2015 | |
| **FUNC-DN-15** | Tự động mở khóa sau 30 phút | 1. Truy cập /user/auth/login<br>2. Đăng nhập sai 5 lần<br>3. Đợi 30 phút | isLocked = false, lockUntil = null, failedAttempts = 0, showCaptcha = false, các trường input được enable lại, localStorage được xóa | | Pass | 11/15/2015 | |
| **FUNC-DN-16** | Nhấn link Quên mật khẩu | 1. Truy cập /user/auth/login<br>2. Nhấn link "Quên mật khẩu?" | Chuyển đến trang /user/auth/forgot-password | | Pass | 11/15/2015 | |
| **FUNC-DN-17** | Nhấn link Đăng ký | 1. Truy cập /user/auth/login<br>2. Nhấn link "Đăng ký ngay" | Chuyển đến trang /user/auth/register | | Pass | 11/15/2015 | |
| **FUNC-DN-18** | Submit form bằng phím Enter | 1. Truy cập /user/auth/login<br>2. Nhập thông tin hợp lệ<br>3. Nhấn Enter trong trường mật khẩu | Form được gửi, xử lý đăng nhập như khi nhấn nút | | Pass | 11/15/2015 | |

### Function: Quên mật khẩu / Khôi phục mật khẩu

#### Check GUI: Quên mật khẩu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-QM-01** | Kiểm tra tiêu đề trang quên mật khẩu | 1. Truy cập /user/auth/forgot-password<br>2. Kiểm tra tiêu đề | Hiển thị Card với CardHeader, có icon Mail trong div (h-12 w-12 rounded-full bg-primary/10), CardTitle "Quên mật khẩu" (text-2xl font-bold), CardDescription "Nhập email của bạn để nhận link khôi phục mật khẩu" | | Pass | 11/15/2015 | |
| **GUI-QM-02** | Kiểm tra trường Email | 1. Truy cập /user/auth/forgot-password<br>2. Kiểm tra trường Email | Hiển thị Label "Email", Input type email với placeholder "Nhập email của bạn", required | | Pass | 11/15/2015 | |
| **GUI-QM-03** | Kiểm tra nút Gửi link khôi phục | 1. Truy cập /user/auth/forgot-password<br>2. Kiểm tra nút | Hiển thị Button với text "Gửi link khôi phục" hoặc "Đang gửi..." khi isLoading, className w-full, type submit | | Pass | 11/15/2015 | |
| **GUI-QM-04** | Kiểm tra link quay lại đăng nhập | 1. Truy cập /user/auth/forgot-password<br>2. Kiểm tra link | Hiển thị Link đến /user/auth/login với icon ArrowLeft và text "Quay lại đăng nhập" (text-sm text-primary hover:underline) | | Pass | 11/15/2015 | |
| **GUI-QM-05** | Kiểm tra link đăng ký | 1. Truy cập /user/auth/forgot-password<br>2. Kiểm tra link | Hiển thị text "Chưa có tài khoản? " và Link đến /user/auth/register với text "Đăng ký ngay" | | Pass | 11/15/2015 | |
| **GUI-QM-06** | Kiểm tra màn hình xác nhận email đã gửi | 1. Truy cập /user/auth/forgot-password<br>2. Nhập email và gửi thành công<br>3. Kiểm tra màn hình | Hiển thị Card với icon CheckCircle (h-6 w-6 text-green-600) trong div (h-12 w-12 rounded-full bg-green-100), CardTitle "Email đã được gửi" (text-2xl font-bold), CardDescription "Chúng tôi đã gửi link khôi phục mật khẩu đến email của bạn" | | Pass | 11/15/2015 | |
| **GUI-QM-07** | Kiểm tra nút Gửi lại email | 1. Truy cập /user/auth/forgot-password<br>2. Gửi email thành công<br>3. Kiểm tra nút | Hiển thị Button variant outline "Gửi lại email", className w-full | | Pass | 11/15/2015 | |

#### Check FUNC: Quên mật khẩu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-QM-01** | Mở trang quên mật khẩu | 1. Truy cập /user/auth/forgot-password | Hiển thị form quên mật khẩu với Card component, trường email, nút gửi link, link quay lại đăng nhập, link đăng ký | | Pass | 11/15/2015 | |
| **FUNC-QM-02** | Gửi link khôi phục thành công | 1. Truy cập /user/auth/forgot-password<br>2. Nhập email hợp lệ<br>3. Nhấn nút Gửi link khôi phục | Hiển thị toast.success "Email khôi phục mật khẩu đã được gửi!", chuyển sang màn hình xác nhận với icon CheckCircle, thông báo "Chúng tôi đã gửi link khôi phục mật khẩu đến email của bạn" | | Pass | 11/15/2015 | |
| **FUNC-QM-03** | Gửi link với email trống | 1. Truy cập /user/auth/forgot-password<br>2. Để trống email<br>3. Nhấn nút Gửi | Hiển thị toast.error "Vui lòng nhập email", form không được submit | | Pass | 11/15/2015 | |
| **FUNC-QM-04** | Gửi lại email | 1. Truy cập /user/auth/forgot-password<br>2. Gửi email thành công<br>3. Nhấn nút "Gửi lại email" | Chuyển về màn hình form ban đầu, có thể nhập email và gửi lại | | Pass | 11/15/2015 | |
| **FUNC-QM-05** | Nhấn link quay lại đăng nhập | 1. Truy cập /user/auth/forgot-password<br>2. Nhấn link "Quay lại đăng nhập" | Chuyển đến trang /user/auth/login | | Pass | 11/15/2015 | |
| **FUNC-QM-06** | Xử lý lỗi khi gửi email | 1. Truy cập /user/auth/forgot-password<br>2. Nhập email hợp lệ<br>3. Giả lập lỗi gửi email<br>4. Nhấn nút Gửi | Hiển thị toast.error "Có lỗi xảy ra, vui lòng thử lại", form vẫn hiển thị để người dùng thử lại | | Pass | 11/15/2015 | |

### Function: Quản lý thông tin cá nhân

#### Check GUI: Quản lý thông tin cá nhân

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-TT-01** | Kiểm tra tiêu đề trang | 1. Truy cập /user/account<br>2. Kiểm tra tiêu đề | Hiển thị h1 "Tài khoản của tôi" (text-3xl font-bold), p "Quản lý thông tin cá nhân và theo dõi hoạt động" (text-muted-foreground) | | Pass | 11/15/2015 | |
| **GUI-TT-02** | Kiểm tra nút Chỉnh sửa/Lưu | 1. Truy cập /user/account<br>2. Kiểm tra nút | Hiển thị Button "Chỉnh sửa" với icon Edit khi không editing, hoặc Button "Hủy" (variant outline) và Button "Lưu thay đổi" với icon Save khi editing | | Pass | 11/15/2015 | |
| **GUI-TT-03** | Kiểm tra phần Avatar và hạng | 1. Truy cập /user/account<br>2. Kiểm tra phần avatar | Hiển thị Avatar (h-20 w-20) với AvatarImage hoặc AvatarFallback, h3 với tên người dùng (text-lg font-semibold), Badge hiển thị hạng với icon Crown | | Pass | 11/15/2015 | |
| **GUI-TT-04** | Kiểm tra các trường thông tin | 1. Truy cập /user/account<br>2. Kiểm tra các trường | Hiển thị grid md:grid-cols-2 với các Label và Input: Họ và tên, Email, Số điện thoại, Ngày sinh, Địa chỉ. Các Input disabled khi không editing | | Pass | 11/15/2015 | |
| **GUI-TT-05** | Kiểm tra phần thống kê hoạt động | 1. Truy cập /user/account<br>2. Kiểm tra phần thống kê | Hiển thị Card với CardTitle "Thống kê hoạt động" (icon Star), grid md:grid-cols-3 với 3 div: Đơn hàng (icon ShoppingBag), Sách yêu thích (icon Heart), Điểm tích lũy (icon Crown) | | Pass | 11/15/2015 | |
| **GUI-TT-06** | Kiểm tra sidebar thông tin tài khoản | 1. Truy cập /user/account<br>2. Kiểm tra sidebar | Hiển thị Card với CardTitle "Thông tin tài khoản" (icon Crown), các thông tin: Email đăng nhập (icon Mail), Thành viên từ (icon Calendar), Lần đăng nhập cuối (icon Calendar) | | Pass | 11/15/2015 | |
| **GUI-TT-07** | Kiểm tra nút Đổi mật khẩu | 1. Truy cập /user/account<br>2. Kiểm tra nút | Hiển thị Button variant outline với icon Key và text "Đổi mật khẩu", className w-full justify-start | | Pass | 11/15/2015 | |
| **GUI-TT-08** | Kiểm tra nút Đăng xuất | 1. Truy cập /user/account<br>2. Kiểm tra nút | Hiển thị AlertDialogTrigger với Button variant destructive, icon LogOut và text "Đăng xuất", className w-full justify-start | | Pass | 11/15/2015 | |
| **GUI-TT-09** | Kiểm tra phần thông tin thành viên | 1. Truy cập /user/account<br>2. Kiểm tra phần thành viên | Hiển thị Card với CardTitle "Thông tin thành viên" (icon Crown), Badge hiển thị hạng, text "Giảm giá X%", các thông tin: Tổng chi tiêu, Điểm tích lũy, Button "Xem lịch sử giao dịch" | | Pass | 11/15/2015 | |

#### Check FUNC: Quản lý thông tin cá nhân

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TT-01** | Mở trang quản lý tài khoản | 1. Truy cập /user/account | Hiển thị trang với tiêu đề, nút chỉnh sửa, Card thông tin cá nhân, Card thống kê hoạt động, sidebar với thông tin tài khoản và các nút chức năng | | Pass | 11/15/2015 | |
| **FUNC-TT-02** | Chỉnh sửa thông tin cá nhân | 1. Truy cập /user/account<br>2. Nhấn nút "Chỉnh sửa"<br>3. Sửa các trường thông tin<br>4. Nhấn "Lưu thay đổi" | Các Input được enable, có thể chỉnh sửa. Sau khi lưu, hiển thị toast.success "Cập nhật thông tin thành công", các Input được disable lại, thông tin được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-TT-03** | Hủy chỉnh sửa | 1. Truy cập /user/account<br>2. Nhấn nút "Chỉnh sửa"<br>3. Sửa thông tin<br>4. Nhấn "Hủy" | Form được reset về giá trị ban đầu, các Input được disable lại, nút chuyển về "Chỉnh sửa" | | Pass | 11/15/2015 | |
| **FUNC-TT-04** | Lưu thông tin thiếu họ tên | 1. Truy cập /user/account<br>2. Nhấn "Chỉnh sửa"<br>3. Xóa họ tên<br>4. Nhấn "Lưu thay đổi" | Hiển thị toast.error "Họ tên không được để trống", thông tin không được lưu | | Pass | 11/15/2015 | |
| **FUNC-TT-05** | Lưu thông tin thiếu email | 1. Truy cập /user/account<br>2. Nhấn "Chỉnh sửa"<br>3. Xóa email<br>4. Nhấn "Lưu thay đổi" | Hiển thị toast.error "Email không được để trống", thông tin không được lưu | | Pass | 11/15/2015 | |
| **FUNC-TT-06** | Lưu thông tin thiếu số điện thoại | 1. Truy cập /user/account<br>2. Nhấn "Chỉnh sửa"<br>3. Xóa số điện thoại<br>4. Nhấn "Lưu thay đổi" | Hiển thị toast.error "Số điện thoại không được để trống", thông tin không được lưu | | Pass | 11/15/2015 | |

### Function: Đổi mật khẩu

#### Check GUI: Đổi mật khẩu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DM-01** | Kiểm tra Dialog đổi mật khẩu | 1. Truy cập /user/account<br>2. Nhấn nút "Đổi mật khẩu" | Hiển thị Dialog với DialogHeader, DialogTitle "Đổi mật khẩu", DialogDescription "Nhập mật khẩu hiện tại và mật khẩu mới để thay đổi" | | Pass | 11/15/2015 | |
| **GUI-DM-02** | Kiểm tra trường Mật khẩu hiện tại | 1. Truy cập /user/account<br>2. Mở Dialog đổi mật khẩu<br>3. Kiểm tra trường | Hiển thị Label "Mật khẩu hiện tại *", Input type password với nút Eye/EyeOff ở bên phải | | Pass | 11/15/2015 | |
| **GUI-DM-03** | Kiểm tra trường Mật khẩu mới | 1. Truy cập /user/account<br>2. Mở Dialog đổi mật khẩu<br>3. Kiểm tra trường | Hiển thị Label "Mật khẩu mới *", Input type password với nút Eye/EyeOff ở bên phải, text "Mật khẩu phải có ít nhất 6 ký tự" (text-xs text-muted-foreground) | | Pass | 11/15/2015 | |
| **GUI-DM-04** | Kiểm tra trường Xác nhận mật khẩu | 1. Truy cập /user/account<br>2. Mở Dialog đổi mật khẩu<br>3. Kiểm tra trường | Hiển thị Label "Xác nhận mật khẩu mới *", Input type password với nút Eye/EyeOff ở bên phải | | Pass | 11/15/2015 | |
| **GUI-DM-05** | Kiểm tra phần OTP cho VIP/Admin | 1. Truy cập /user/account<br>2. Mở Dialog đổi mật khẩu (tài khoản VIP/Admin)<br>3. Nhấn "Tiếp tục"<br>4. Kiểm tra phần OTP | Hiển thị Alert với icon Info, AlertDescription về yêu cầu OTP. Sau khi nhấn "Tiếp tục", hiển thị div với className "space-y-2 p-4 bg-blue-50 rounded-lg border border-blue-200", có Label "Mã OTP xác thực (6 số) *", Input để nhập OTP (text-center text-lg tracking-widest), text hướng dẫn, Button "Gửi lại mã OTP" | | Pass | 11/15/2015 | |
| **GUI-DM-06** | Kiểm tra nút Hủy và Đổi mật khẩu | 1. Truy cập /user/account<br>2. Mở Dialog đổi mật khẩu<br>3. Kiểm tra nút | Hiển thị Button variant outline "Hủy" và Button "Đổi mật khẩu" hoặc "Tiếp tục" (nếu VIP/Admin và chưa nhập OTP) | | Pass | 11/15/2015 | |

#### Check FUNC: Đổi mật khẩu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DM-01** | Mở Dialog đổi mật khẩu | 1. Truy cập /user/account<br>2. Nhấn nút "Đổi mật khẩu" | Hiển thị Dialog với form đổi mật khẩu, các trường: mật khẩu hiện tại, mật khẩu mới, xác nhận mật khẩu, các nút Hủy và Đổi mật khẩu | | Pass | 11/15/2015 | |
| **FUNC-DM-02** | Đổi mật khẩu thành công (tài khoản thường) | 1. Truy cập /user/account<br>2. Mở Dialog đổi mật khẩu<br>3. Nhập mật khẩu hiện tại đúng<br>4. Nhập mật khẩu mới hợp lệ (>= 6 ký tự)<br>5. Nhập xác nhận mật khẩu khớp<br>6. Nhấn "Đổi mật khẩu" | Hiển thị toast.success "Đổi mật khẩu thành công", Dialog đóng, form được reset | | Pass | 11/15/2015 | |
| **FUNC-DM-03** | Đổi mật khẩu với mật khẩu hiện tại sai | 1. Truy cập /user/account<br>2. Mở Dialog đổi mật khẩu<br>3. Nhập mật khẩu hiện tại sai<br>4. Nhập mật khẩu mới<br>5. Nhấn "Đổi mật khẩu" | Hiển thị toast.error "Mật khẩu hiện tại không đúng", mật khẩu không được đổi | | Pass | 11/15/2015 | |
| **FUNC-DM-04** | Đổi mật khẩu với mật khẩu mới quá ngắn | 1. Truy cập /user/account<br>2. Mở Dialog đổi mật khẩu<br>3. Nhập mật khẩu hiện tại đúng<br>4. Nhập mật khẩu mới < 6 ký tự<br>5. Nhấn "Đổi mật khẩu" | Hiển thị toast.error "Mật khẩu mới phải có ít nhất 6 ký tự", mật khẩu không được đổi | | Pass | 11/15/2015 | |
| **FUNC-DM-05** | Đổi mật khẩu với xác nhận không khớp | 1. Truy cập /user/account<br>2. Mở Dialog đổi mật khẩu<br>3. Nhập mật khẩu hiện tại đúng<br>4. Nhập mật khẩu mới<br>5. Nhập xác nhận mật khẩu khác<br>6. Nhấn "Đổi mật khẩu" | Hiển thị toast.error "Mật khẩu xác nhận không khớp", mật khẩu không được đổi | | Pass | 11/15/2015 | |
| **FUNC-DM-06** | Đổi mật khẩu cho tài khoản VIP/Admin - Gửi OTP | 1. Truy cập /user/account (tài khoản VIP/Admin)<br>2. Mở Dialog đổi mật khẩu<br>3. Nhập đầy đủ thông tin hợp lệ<br>4. Nhấn "Tiếp tục" | Hiển thị toast.success "Mã OTP đã được gửi đến email của bạn", phần OTP xuất hiện, nút chuyển thành "Đổi mật khẩu" | | Pass | 11/15/2015 | |
| **FUNC-DM-07** | Đổi mật khẩu cho tài khoản VIP/Admin - Nhập OTP đúng | 1. Truy cập /user/account (tài khoản VIP/Admin)<br>2. Mở Dialog đổi mật khẩu<br>3. Nhập đầy đủ thông tin và nhấn "Tiếp tục"<br>4. Nhập OTP đúng (123456)<br>5. Nhấn "Đổi mật khẩu" | Hiển thị toast.success "Đổi mật khẩu thành công", Dialog đóng, form được reset | | Pass | 11/15/2015 | |
| **FUNC-DM-08** | Đổi mật khẩu cho tài khoản VIP/Admin - Nhập OTP sai | 1. Truy cập /user/account (tài khoản VIP/Admin)<br>2. Mở Dialog đổi mật khẩu<br>3. Nhập đầy đủ thông tin và nhấn "Tiếp tục"<br>4. Nhập OTP sai<br>5. Nhấn "Đổi mật khẩu" | Hiển thị toast.error "Mã OTP không đúng. Vui lòng thử lại.", OTP không được chấp nhận | | Pass | 11/15/2015 | |
| **FUNC-DM-09** | Gửi lại mã OTP | 1. Truy cập /user/account (tài khoản VIP/Admin)<br>2. Mở Dialog đổi mật khẩu<br>3. Nhập đầy đủ thông tin và nhấn "Tiếp tục"<br>4. Nhấn "Gửi lại mã OTP" | Hiển thị toast.success "Đã gửi lại mã OTP", mã OTP mới được gửi đến email | | Pass | 11/15/2015 | |
| **FUNC-DM-10** | Hiện/Ẩn mật khẩu | 1. Truy cập /user/account<br>2. Mở Dialog đổi mật khẩu<br>3. Nhập mật khẩu<br>4. Click nút Eye | Input type chuyển từ password sang text, icon chuyển từ Eye sang EyeOff | | Pass | 11/15/2015 | |
| **FUNC-DM-11** | Hủy đổi mật khẩu | 1. Truy cập /user/account<br>2. Mở Dialog đổi mật khẩu<br>3. Nhập thông tin<br>4. Nhấn "Hủy" | Dialog đóng, form được reset, không có thay đổi nào được lưu | | Pass | 11/15/2015 | |

### Function: Xem điểm tích lũy và hạng thành viên

#### Check GUI: Điểm tích lũy và hạng thành viên

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DT-01** | Kiểm tra tiêu đề trang | 1. Truy cập /user/account/rank<br>2. Kiểm tra tiêu đề | Hiển thị h1 "Điểm tích lũy và hạng thành viên" (text-2xl font-bold), p "Theo dõi hạng hiện tại, tổng chi tiêu và ưu đãi" (text-muted-foreground) | | Pass | 11/15/2015 | |
| **GUI-DT-02** | Kiểm tra Card thông tin hạng | 1. Truy cập /user/account/rank<br>2. Kiểm tra Card | Hiển thị Card với CardHeader có CardTitle "Thông tin hạng" (icon Crown text-yellow-500), CardDescription "Hạng hiện tại, điểm và chi tiêu", Badge "ID: user_001" | | Pass | 11/15/2015 | |
| **GUI-DT-03** | Kiểm tra thông tin hạng hiện tại | 1. Truy cập /user/account/rank<br>2. Kiểm tra thông tin | Hiển thị grid md:grid-cols-2 với: Hạng hiện tại (Badge), Điểm tích lũy (toLocaleString), Tổng chi tiêu (toLocaleString VNĐ), Phần trăm giảm giá (%) | | Pass | 11/15/2015 | |
| **GUI-DT-04** | Kiểm tra thanh tiến độ hạng tiếp theo | 1. Truy cập /user/account/rank<br>2. Kiểm tra thanh tiến độ | Hiển thị text "Tiến độ hạng tiếp theo", Progress component với value tính từ currentPoints/nextRankTarget, text "{currentPoints}/{nextRankTarget} điểm", text-xs "Quy tắc nâng hạng có thể dựa trên điểm hoặc tổng chi tiêu" | | Pass | 11/15/2015 | |
| **GUI-DT-05** | Kiểm tra Card quyền lợi hạng | 1. Truy cập /user/account/rank<br>2. Kiểm tra Card | Hiển thị Card với CardTitle "Quyền lợi hạng", CardDescription "Giảm giá và ưu đãi theo hạng", grid md:grid-cols-4 với 4 div: Bronze (0%), Silver (3%), Gold (5%), Kim cương (8%) | | Pass | 11/15/2015 | |
| **GUI-DT-06** | Kiểm tra bảng lịch sử tích điểm | 1. Truy cập /user/account/rank<br>2. Kiểm tra bảng | Hiển thị Card với CardTitle "Lịch sử tích điểm", CardDescription "Ngày, Mô tả, Điểm tích, Điểm sử dụng, Số dư", Table với TableHeader: Ngày, Mô tả, Điểm tích (text-right), Điểm sử dụng (text-right), Số dư (text-right) | | Pass | 11/15/2015 | |
| **GUI-DT-07** | Kiểm tra nút Xem lịch sử giao dịch | 1. Truy cập /user/account/rank<br>2. Kiểm tra nút | Hiển thị Button variant outline size sm với link đến /user/account/orders, text "Xem lịch sử giao dịch", className w-full | | Pass | 11/15/2015 | |

#### Check FUNC: Điểm tích lũy và hạng thành viên

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DT-01** | Mở trang điểm tích lũy | 1. Truy cập /user/account/rank | Hiển thị trang với tiêu đề, Card thông tin hạng (hạng hiện tại, điểm, chi tiêu, giảm giá, tiến độ), Card quyền lợi hạng, Card lịch sử tích điểm với bảng dữ liệu | | Pass | 11/15/2015 | |
| **FUNC-DT-02** | Hiển thị lịch sử tích điểm | 1. Truy cập /user/account/rank<br>2. Kiểm tra bảng lịch sử | Hiển thị Table với các dòng dữ liệu: Ngày (toLocaleDateString), Mô tả, Điểm tích (+X hoặc -), Điểm sử dụng (-X hoặc -), Số dư | | Pass | 11/15/2015 | |
| **FUNC-DT-03** | Tính toán tiến độ hạng tiếp theo | 1. Truy cập /user/account/rank<br>2. Kiểm tra thanh tiến độ | Progress value = Math.min(100, Math.round((currentPoints / nextRankTarget) * 100)), hiển thị đúng phần trăm và số điểm | | Pass | 11/15/2015 | |
| **FUNC-DT-04** | Nhấn nút Xem lịch sử giao dịch | 1. Truy cập /user/account/rank<br>2. Nhấn nút "Xem lịch sử giao dịch" | Chuyển đến trang /user/account/orders | | Pass | 11/15/2015 | |

### Function: Đăng xuất hệ thống

#### Check GUI: Đăng xuất

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DX-01** | Kiểm tra nút Đăng xuất | 1. Truy cập /user/account<br>2. Kiểm tra nút | Hiển thị AlertDialogTrigger với Button variant destructive, icon LogOut và text "Đăng xuất", className w-full justify-start | | Pass | 11/15/2015 | |
| **GUI-DX-02** | Kiểm tra Dialog xác nhận đăng xuất | 1. Truy cập /user/account<br>2. Nhấn nút "Đăng xuất" | Hiển thị AlertDialog với AlertDialogHeader, AlertDialogTitle "Xác nhận đăng xuất", AlertDialogDescription "Bạn có chắc chắn muốn đăng xuất khỏi hệ thống? Bạn sẽ cần đăng nhập lại để tiếp tục sử dụng." | | Pass | 11/15/2015 | |
| **GUI-DX-03** | Kiểm tra nút Hủy và Xác nhận | 1. Truy cập /user/account<br>2. Mở Dialog đăng xuất<br>3. Kiểm tra nút | Hiển thị AlertDialogFooter với AlertDialogCancel "Hủy" và AlertDialogAction "Đăng xuất" | | Pass | 11/15/2015 | |

#### Check FUNC: Đăng xuất

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DX-01** | Mở Dialog xác nhận đăng xuất | 1. Truy cập /user/account<br>2. Nhấn nút "Đăng xuất" | Hiển thị AlertDialog với tiêu đề, mô tả, nút Hủy và nút Xác nhận | | Pass | 11/15/2015 | |
| **FUNC-DX-02** | Đăng xuất thành công | 1. Truy cập /user/account<br>2. Nhấn nút "Đăng xuất"<br>3. Nhấn "Đăng xuất" trong Dialog | Hiển thị toast.success "Đăng xuất thành công", redirect đến /user/auth/login, phiên đăng nhập được kết thúc, token được xóa | | Pass | 11/15/2015 | |
| **FUNC-DX-03** | Hủy đăng xuất | 1. Truy cập /user/account<br>2. Nhấn nút "Đăng xuất"<br>3. Nhấn "Hủy" | Dialog đóng, vẫn ở trang /user/account, không có thay đổi nào | | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn MDX để dễ dàng quản lý và cập nhật test cases.*

