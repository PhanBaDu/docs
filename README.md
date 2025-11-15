# BLACKBOX TEST CASE - QUẢN LÝ TÀI KHOẢN (USER)

## HEADER SECTION

**Module Code:** Quản lý tài khoản User

**Test requirement:**
1. Đăng nhập
2. Đăng ký
3. Đổi mật khẩu
4. Cập nhật thông tin cá nhân
5. Quản lý thông tin cá nhân (Layout)
6. Khôi phục mật khẩu
7. Quản lý địa chỉ
8. Quản lý thanh toán
9. Xem hạng thành viên

**Tester:** [Tên tester]

**Summary Statistics:**

| Pass | Fail | Untested | N/A | Number of Test cases |
|------|------|----------|-----|---------------------|
| 0 | 0 | 123 | 0 | 123 |

---

## TEST CASE TABLE

| ID | Test Case Description | Test Case Procedure | Expected Output | Test-case rate | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|----------------|--------|-----------|------|
| **Function: Đăng nhập** |
| **Check GUI: Đăng nhập** |
| GUI-DangNhap-01 | Check [Email] Input | 1. Truy cập `/user/auth/login`<br>2. Kiểm tra ô [Email] | Status: visible, enable, Type: email | | Pass | 11/15/2025 | |
| GUI-DangNhap-02 | Check [Mật khẩu] Input | 1. Truy cập `/user/auth/login`<br>2. Kiểm tra ô [Mật khẩu] | Status: visible, enable, Type: password | | Pass | 11/15/2025 | |
| GUI-DangNhap-03 | Check [Ghi nhớ đăng nhập] Checkbox | 1. Truy cập `/user/auth/login`<br>2. Kiểm tra checkbox [Ghi nhớ đăng nhập] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-DangNhap-04 | Check [Quên mật khẩu] Link | 1. Truy cập `/user/auth/login`<br>2. Kiểm tra link [Quên mật khẩu] | Status: visible, enable, Link to: `/user/auth/forgot-password` | | Pass | 11/15/2025 | |
| GUI-DangNhap-05 | Check [Đăng nhập] Button | 1. Truy cập `/user/auth/login`<br>2. Kiểm tra nút [Đăng nhập] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-DangNhap-06 | Check [Hủy] Button | 1. Truy cập `/user/auth/login`<br>2. Kiểm tra nút [Hủy] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-DangNhap-07 | Check [Chưa có tài khoản? Đăng ký] Link | 1. Truy cập `/user/auth/login`<br>2. Kiểm tra link [Đăng ký] | Status: visible, enable, Link to: `/user/auth/register` | | Pass | 11/15/2025 | |
| GUI-DangNhap-08 | Check [Đăng nhập xã hội] Buttons | 1. Truy cập `/user/auth/login`<br>2. Kiểm tra nút [Google], [Facebook] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-DangNhap-09 | Check [Captcha] (sau 3 lần sai) | 1. Truy cập `/user/auth/login`<br>2. Đăng nhập sai 3 lần<br>3. Kiểm tra captcha | Status: visible, enable | | Pass | 11/15/2025 | |
| **Check FUNC: Đăng nhập** |
| FUNC-DangNhap-01 | Mở màn hình đăng nhập | 1. Truy cập `/user/auth/login` hoặc click [Đăng nhập] | Hiển thị màn hình đăng nhập với form trống | | Pass | 11/15/2025 | |
| FUNC-DangNhap-02 | Đăng nhập thiếu Email | 1. Truy cập `/user/auth/login`<br>2. Không nhập Email<br>3. Click [Đăng nhập] | Hiển thị thông báo lỗi: "Email là bắt buộc" | | Pass | 11/15/2025 | |
| FUNC-DangNhap-03 | Đăng nhập thiếu Mật khẩu | 1. Truy cập `/user/auth/login`<br>2. Nhập Email<br>3. Không nhập Mật khẩu<br>4. Click [Đăng nhập] | Hiển thị thông báo lỗi: "Mật khẩu là bắt buộc" | | Pass | 11/15/2025 | |
| FUNC-DangNhap-04 | Đăng nhập Email không đúng định dạng | 1. Truy cập `/user/auth/login`<br>2. Nhập Email = "invalid-email"<br>3. Click [Đăng nhập] | Hiển thị thông báo lỗi: "Email không đúng định dạng" | | Pass | 11/15/2025 | |
| FUNC-DangNhap-05 | Đăng nhập Email không tồn tại | 1. Truy cập `/user/auth/login`<br>2. Nhập Email không tồn tại<br>3. Nhập Mật khẩu<br>4. Click [Đăng nhập] | Hiển thị thông báo lỗi: "Email hoặc mật khẩu không đúng" | | Pass | 11/15/2025 | |
| FUNC-DangNhap-06 | Đăng nhập Mật khẩu sai | 1. Truy cập `/user/auth/login`<br>2. Nhập Email hợp lệ<br>3. Nhập Mật khẩu sai<br>4. Click [Đăng nhập] | Hiển thị thông báo lỗi: "Email hoặc mật khẩu không đúng" | | Pass | 11/15/2025 | |
| FUNC-DangNhap-07 | Đăng nhập thành công | 1. Truy cập `/user/auth/login`<br>2. Nhập Email và Mật khẩu hợp lệ<br>3. Click [Đăng nhập] | Đăng nhập thành công, chuyển đến trang chủ | | Pass | 11/15/2025 | |
| FUNC-DangNhap-08 | Đăng nhập với Ghi nhớ đăng nhập | 1. Truy cập `/user/auth/login`<br>2. Nhập thông tin đăng nhập<br>3. Check [Ghi nhớ đăng nhập]<br>4. Click [Đăng nhập] | Đăng nhập thành công, phiên đăng nhập được lưu lâu hơn | | Pass | 11/15/2025 | |
| FUNC-DangNhap-09 | Đăng nhập sai 3 lần - hiển thị Captcha | 1. Truy cập `/user/auth/login`<br>2. Đăng nhập sai 3 lần liên tiếp | Hiển thị captcha, yêu cầu nhập captcha để tiếp tục | | Pass | 11/15/2025 | |
| FUNC-DangNhap-10 | Đăng nhập tài khoản bị khóa | 1. Truy cập `/user/auth/login`<br>2. Nhập thông tin tài khoản bị khóa<br>3. Click [Đăng nhập] | Hiển thị thông báo lỗi: "Tài khoản đã bị khóa" | | Pass | 11/15/2025 | |
| FUNC-DangNhap-11 | Đăng nhập tài khoản chưa kích hoạt | 1. Truy cập `/user/auth/login`<br>2. Nhập thông tin tài khoản chưa kích hoạt<br>3. Click [Đăng nhập] | Hiển thị thông báo lỗi: "Tài khoản chưa được kích hoạt" | | Pass | 11/15/2025 | |
| FUNC-DangNhap-12 | Click link Quên mật khẩu | 1. Truy cập `/user/auth/login`<br>2. Click [Quên mật khẩu] | Chuyển đến trang khôi phục mật khẩu | | Pass | 11/15/2025 | |
| FUNC-DangNhap-13 | Click link Đăng ký | 1. Truy cập `/user/auth/login`<br>2. Click [Chưa có tài khoản? Đăng ký] | Chuyển đến trang đăng ký | | Pass | 11/15/2025 | |
| FUNC-DangNhap-14 | Click nút Hủy | 1. Truy cập `/user/auth/login`<br>2. Nhập một số thông tin<br>3. Click [Hủy] | Form được reset, quay về trang trước | | Pass | 11/15/2025 | |
| **Function: Đăng ký** |
| **Check GUI: Đăng ký** |
| GUI-DangKy-01 | Check [Họ và tên] Input | 1. Truy cập `/user/auth/register`<br>2. Kiểm tra ô [Họ và tên] | Status: visible, enable, Type: text, Max length: 100 | | Pass | 11/15/2025 | |
| GUI-DangKy-02 | Check [Email] Input | 1. Truy cập `/user/auth/register`<br>2. Kiểm tra ô [Email] | Status: visible, enable, Type: email | | Pass | 11/15/2025 | |
| GUI-DangKy-03 | Check [Số điện thoại] Input | 1. Truy cập `/user/auth/register`<br>2. Kiểm tra ô [Số điện thoại] | Status: visible, enable, Type: tel | | Pass | 11/15/2025 | |
| GUI-DangKy-04 | Check [Mật khẩu] Input | 1. Truy cập `/user/auth/register`<br>2. Kiểm tra ô [Mật khẩu] | Status: visible, enable, Type: password | | Pass | 11/15/2025 | |
| GUI-DangKy-05 | Check [Xác nhận mật khẩu] Input | 1. Truy cập `/user/auth/register`<br>2. Kiểm tra ô [Xác nhận mật khẩu] | Status: visible, enable, Type: password | | Pass | 11/15/2025 | |
| GUI-DangKy-06 | Check [Địa chỉ] Textarea | 1. Truy cập `/user/auth/register`<br>2. Kiểm tra ô [Địa chỉ] | Status: visible, enable, Type: textarea | | Pass | 11/15/2025 | |
| GUI-DangKy-07 | Check [Điều khoản sử dụng] Checkbox | 1. Truy cập `/user/auth/register`<br>2. Kiểm tra checkbox [Điều khoản sử dụng] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-DangKy-08 | Check [Đăng ký] Button | 1. Truy cập `/user/auth/register`<br>2. Kiểm tra nút [Đăng ký] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-DangKy-09 | Check [Hủy] Button | 1. Truy cập `/user/auth/register`<br>2. Kiểm tra nút [Hủy] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-DangKy-10 | Check [Đã có tài khoản? Đăng nhập] Link | 1. Truy cập `/user/auth/register`<br>2. Kiểm tra link [Đăng nhập] | Status: visible, enable, Link to: `/user/auth/login` | | Pass | 11/15/2025 | |
| **Check FUNC: Đăng ký** |
| FUNC-DangKy-01 | Mở màn hình đăng ký | 1. Truy cập `/user/auth/register` hoặc click [Đăng ký] | Hiển thị màn hình đăng ký với form trống | | Pass | 11/15/2025 | |
| FUNC-DangKy-02 | Đăng ký thiếu Họ và tên | 1. Truy cập `/user/auth/register`<br>2. Không nhập Họ và tên<br>3. Điền các trường khác<br>4. Click [Đăng ký] | Hiển thị thông báo lỗi: "Họ và tên là bắt buộc" | | Pass | 11/15/2025 | |
| FUNC-DangKy-03 | Đăng ký thiếu Email | 1. Truy cập `/user/auth/register`<br>2. Không nhập Email<br>3. Điền các trường khác<br>4. Click [Đăng ký] | Hiển thị thông báo lỗi: "Email là bắt buộc" | | Pass | 11/15/2025 | |
| FUNC-DangKy-04 | Đăng ký thiếu Số điện thoại | 1. Truy cập `/user/auth/register`<br>2. Không nhập Số điện thoại<br>3. Điền các trường khác<br>4. Click [Đăng ký] | Hiển thị thông báo lỗi: "Số điện thoại là bắt buộc" | | Pass | 11/15/2025 | |
| FUNC-DangKy-05 | Đăng ký thiếu Mật khẩu | 1. Truy cập `/user/auth/register`<br>2. Không nhập Mật khẩu<br>3. Điền các trường khác<br>4. Click [Đăng ký] | Hiển thị thông báo lỗi: "Mật khẩu là bắt buộc" | | Pass | 11/15/2025 | |
| FUNC-DangKy-06 | Đăng ký Email không đúng định dạng | 1. Truy cập `/user/auth/register`<br>2. Nhập Email = "invalid-email"<br>3. Điền các trường khác<br>4. Click [Đăng ký] | Hiển thị thông báo lỗi: "Email không đúng định dạng" | | Pass | 11/15/2025 | |
| FUNC-DangKy-07 | Đăng ký Email đã tồn tại (real-time check) | 1. Truy cập `/user/auth/register`<br>2. Nhập Email đã tồn tại<br>3. Kiểm tra validation real-time | Hiển thị cảnh báo ngay khi nhập: "Email đã tồn tại" | | Pass | 11/15/2025 | |
| FUNC-DangKy-08 | Đăng ký Mật khẩu < 8 ký tự | 1. Truy cập `/user/auth/register`<br>2. Nhập Mật khẩu = "1234567"<br>3. Điền các trường khác<br>4. Click [Đăng ký] | Hiển thị thông báo lỗi: "Mật khẩu phải có ít nhất 8 ký tự" | | Pass | 11/15/2025 | |
| FUNC-DangKy-09 | Đăng ký Mật khẩu không đủ mạnh (thiếu chữ hoa) | 1. Truy cập `/user/auth/register`<br>2. Nhập Mật khẩu = "password123"<br>3. Điền các trường khác<br>4. Click [Đăng ký] | Hiển thị thông báo lỗi: "Mật khẩu phải có chữ hoa, chữ thường và số" | | Pass | 11/15/2025 | |
| FUNC-DangKy-10 | Đăng ký Mật khẩu và Xác nhận không khớp | 1. Truy cập `/user/auth/register`<br>2. Nhập Mật khẩu = "Password123"<br>3. Nhập Xác nhận mật khẩu = "Password456"<br>4. Click [Đăng ký] | Hiển thị thông báo lỗi: "Mật khẩu xác nhận không khớp" | | Pass | 11/15/2025 | |
| FUNC-DangKy-11 | Đăng ký Số điện thoại không đúng định dạng | 1. Truy cập `/user/auth/register`<br>2. Nhập Số điện thoại = "123"<br>3. Điền các trường khác<br>4. Click [Đăng ký] | Hiển thị thông báo lỗi: "Số điện thoại không đúng định dạng" | | Pass | 11/15/2025 | |
| FUNC-DangKy-12 | Đăng ký không đồng ý Điều khoản sử dụng | 1. Truy cập `/user/auth/register`<br>2. Điền đầy đủ thông tin<br>3. Không check [Điều khoản sử dụng]<br>4. Click [Đăng ký] | Hiển thị thông báo lỗi: "Vui lòng đồng ý với điều khoản sử dụng" | | Pass | 11/15/2025 | |
| FUNC-DangKy-13 | Đăng ký với thông tin hợp lệ | 1. Truy cập `/user/auth/register`<br>2. Điền đầy đủ thông tin hợp lệ<br>3. Check [Điều khoản sử dụng]<br>4. Click [Đăng ký] | Đăng ký thành công, chuyển đến trang đăng nhập hoặc trang chủ, email xác nhận được gửi | | Pass | 11/15/2025 | |
| FUNC-DangKy-14 | Click link Đăng nhập | 1. Truy cập `/user/auth/register`<br>2. Click [Đã có tài khoản? Đăng nhập] | Chuyển đến trang đăng nhập | | Pass | 11/15/2025 | |
| FUNC-DangKy-15 | Click nút Hủy | 1. Truy cập `/user/auth/register`<br>2. Điền một số thông tin<br>3. Click [Hủy] | Form được reset, quay về trang trước | | Pass | 11/15/2025 | |
| **Function: Đổi mật khẩu** |
| **Check GUI: Đổi mật khẩu** |
| GUI-DoiMK-01 | Check [Mật khẩu hiện tại] Input | 1. Truy cập `/user/account`<br>2. Click tab [Bảo mật] hoặc [Đổi mật khẩu]<br>3. Kiểm tra ô [Mật khẩu hiện tại] | Status: visible, enable, Type: password | | Pass | 11/15/2025 | |
| GUI-DoiMK-02 | Check [Mật khẩu mới] Input | 1. Truy cập `/user/account`<br>2. Click tab [Bảo mật]<br>3. Kiểm tra ô [Mật khẩu mới] | Status: visible, enable, Type: password | | Pass | 11/15/2025 | |
| GUI-DoiMK-03 | Check [Xác nhận mật khẩu mới] Input | 1. Truy cập `/user/account`<br>2. Click tab [Bảo mật]<br>3. Kiểm tra ô [Xác nhận mật khẩu mới] | Status: visible, enable, Type: password | | Pass | 11/15/2025 | |
| GUI-DoiMK-04 | Check [Hiển thị mật khẩu] Checkbox | 1. Truy cập `/user/account`<br>2. Click tab [Bảo mật]<br>3. Kiểm tra checkbox [Hiển thị mật khẩu] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-DoiMK-05 | Check [Xác thực 2 bước] Checkbox | 1. Truy cập `/user/account`<br>2. Click tab [Bảo mật]<br>3. Kiểm tra checkbox [Xác thực 2 bước] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-DoiMK-06 | Check [Đổi mật khẩu] Button | 1. Truy cập `/user/account`<br>2. Click tab [Bảo mật]<br>3. Kiểm tra nút [Đổi mật khẩu] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-DoiMK-07 | Check [Hủy] Button | 1. Truy cập `/user/account`<br>2. Click tab [Bảo mật]<br>3. Kiểm tra nút [Hủy] | Status: visible, enable | | Pass | 11/15/2025 | |
| **Check FUNC: Đổi mật khẩu** |
| FUNC-DoiMK-01 | Mở màn hình đổi mật khẩu | 1. Truy cập `/user/account`<br>2. Click tab [Bảo mật] hoặc [Đổi mật khẩu] | Hiển thị màn hình đổi mật khẩu với form trống | | Pass | 11/15/2025 | |
| FUNC-DoiMK-02 | Đổi mật khẩu thiếu Mật khẩu hiện tại | 1. Truy cập `/user/account`<br>2. Click tab [Bảo mật]<br>3. Không nhập Mật khẩu hiện tại<br>4. Click [Đổi mật khẩu] | Hiển thị thông báo lỗi: "Mật khẩu hiện tại là bắt buộc" | | Pass | 11/15/2025 | |
| FUNC-DoiMK-03 | Đổi mật khẩu Mật khẩu hiện tại sai | 1. Truy cập `/user/account`<br>2. Click tab [Bảo mật]<br>3. Nhập Mật khẩu hiện tại sai<br>4. Click [Đổi mật khẩu] | Hiển thị thông báo lỗi: "Mật khẩu hiện tại không đúng" | | Pass | 11/15/2025 | |
| FUNC-DoiMK-04 | Đổi mật khẩu Mật khẩu mới < 8 ký tự | 1. Truy cập `/user/account`<br>2. Click tab [Bảo mật]<br>3. Nhập Mật khẩu mới = "1234567"<br>4. Click [Đổi mật khẩu] | Hiển thị thông báo lỗi: "Mật khẩu phải có ít nhất 8 ký tự" | | Pass | 11/15/2025 | |
| FUNC-DoiMK-05 | Đổi mật khẩu Mật khẩu mới không đủ mạnh | 1. Truy cập `/user/account`<br>2. Click tab [Bảo mật]<br>3. Nhập Mật khẩu mới = "password123"<br>4. Click [Đổi mật khẩu] | Hiển thị thông báo lỗi: "Mật khẩu phải có chữ hoa, chữ thường và số" | | Pass | 11/15/2025 | |
| FUNC-DoiMK-06 | Đổi mật khẩu Mật khẩu mới trùng với mật khẩu hiện tại | 1. Truy cập `/user/account`<br>2. Click tab [Bảo mật]<br>3. Nhập Mật khẩu mới = mật khẩu hiện tại<br>4. Click [Đổi mật khẩu] | Hiển thị thông báo lỗi: "Mật khẩu mới không được trùng với mật khẩu hiện tại" | | Pass | 11/15/2025 | |
| FUNC-DoiMK-07 | Đổi mật khẩu Xác nhận không khớp | 1. Truy cập `/user/account`<br>2. Click tab [Bảo mật]<br>3. Nhập Mật khẩu mới và Xác nhận không khớp<br>4. Click [Đổi mật khẩu] | Hiển thị thông báo lỗi: "Mật khẩu xác nhận không khớp" | | Pass | 11/15/2025 | |
| FUNC-DoiMK-08 | Đổi mật khẩu với 2FA - thiếu OTP | 1. Truy cập `/user/account`<br>2. Click tab [Bảo mật]<br>3. Bật [Xác thực 2 bước]<br>4. Nhập thông tin nhưng không nhập OTP<br>5. Click [Đổi mật khẩu] | Hiển thị thông báo lỗi: "Vui lòng nhập mã OTP" | | Pass | 11/15/2025 | |
| FUNC-DoiMK-09 | Đổi mật khẩu với 2FA - OTP sai | 1. Truy cập `/user/account`<br>2. Click tab [Bảo mật]<br>3. Bật [Xác thực 2 bước]<br>4. Nhập OTP sai<br>5. Click [Đổi mật khẩu] | Hiển thị thông báo lỗi: "Mã OTP không đúng hoặc đã hết hạn" | | Pass | 11/15/2025 | |
| FUNC-DoiMK-10 | Đổi mật khẩu thành công | 1. Truy cập `/user/account`<br>2. Click tab [Bảo mật]<br>3. Nhập đầy đủ thông tin hợp lệ<br>4. Click [Đổi mật khẩu] | Đổi mật khẩu thành công, tất cả phiên đăng nhập cũ bị vô hiệu hóa, yêu cầu đăng nhập lại | | Pass | 11/15/2025 | |
| FUNC-DoiMK-11 | Hiển thị mật khẩu | 1. Truy cập `/user/account`<br>2. Click tab [Bảo mật]<br>3. Nhập mật khẩu<br>4. Check [Hiển thị mật khẩu] | Mật khẩu hiển thị dạng text | | Pass | 11/15/2025 | |
| FUNC-DoiMK-12 | Click nút Hủy | 1. Truy cập `/user/account`<br>2. Click tab [Bảo mật]<br>3. Nhập một số thông tin<br>4. Click [Hủy] | Form được reset về trạng thái ban đầu | | Pass | 11/15/2025 | |
| **Function: Cập nhật thông tin cá nhân** |
| **Check GUI: Cập nhật thông tin cá nhân** |
| GUI-CapNhatTT-01 | Check [Họ và tên] Input | 1. Truy cập `/user/account`<br>2. Kiểm tra ô [Họ và tên] | Status: visible, enable, Type: text, Default: [giá trị hiện tại] | | Pass | 11/15/2025 | |
| GUI-CapNhatTT-02 | Check [Email] Input | 1. Truy cập `/user/account`<br>2. Kiểm tra ô [Email] | Status: visible, enable, Type: email, Read-only: true | | Pass | 11/15/2025 | |
| GUI-CapNhatTT-03 | Check [Số điện thoại] Input | 1. Truy cập `/user/account`<br>2. Kiểm tra ô [Số điện thoại] | Status: visible, enable, Type: tel, Default: [giá trị hiện tại] | | Pass | 11/15/2025 | |
| GUI-CapNhatTT-04 | Check [Ngày sinh] Datepicker | 1. Truy cập `/user/account`<br>2. Kiểm tra ô [Ngày sinh] | Status: visible, enable, Type: date, Default: [giá trị hiện tại] | | Pass | 11/15/2025 | |
| GUI-CapNhatTT-05 | Check [Giới tính] Select | 1. Truy cập `/user/account`<br>2. Kiểm tra dropdown [Giới tính] | Status: visible, enable, Options: Nam, Nữ, Khác | | Pass | 11/15/2025 | |
| GUI-CapNhatTT-06 | Check [Địa chỉ] Textarea | 1. Truy cập `/user/account`<br>2. Kiểm tra ô [Địa chỉ] | Status: visible, enable, Type: textarea, Default: [giá trị hiện tại] | | Pass | 11/15/2025 | |
| GUI-CapNhatTT-07 | Check [Thành phố] Select | 1. Truy cập `/user/account`<br>2. Kiểm tra dropdown [Thành phố] | Status: visible, enable, Options: Hà Nội, TP.HCM, Đà Nẵng, ... | | Pass | 11/15/2025 | |
| GUI-CapNhatTT-08 | Check [Quận/Huyện] Select | 1. Truy cập `/user/account`<br>2. Kiểm tra dropdown [Quận/Huyện] | Status: visible, enable, Depends on: Thành phố | | Pass | 11/15/2025 | |
| GUI-CapNhatTT-09 | Check [Phường/Xã] Select | 1. Truy cập `/user/account`<br>2. Kiểm tra dropdown [Phường/Xã] | Status: visible, enable, Depends on: Quận/Huyện | | Pass | 11/15/2025 | |
| GUI-CapNhatTT-10 | Check [Đổi ảnh đại diện] Button | 1. Truy cập `/user/account`<br>2. Kiểm tra nút [Đổi ảnh đại diện] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-CapNhatTT-11 | Check [Lưu] Button | 1. Truy cập `/user/account`<br>2. Kiểm tra nút [Lưu] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-CapNhatTT-12 | Check [Hủy] Button | 1. Truy cập `/user/account`<br>2. Kiểm tra nút [Hủy] | Status: visible, enable | | Pass | 11/15/2025 | |
| **Check FUNC: Cập nhật thông tin cá nhân** |
| FUNC-CapNhatTT-01 | Mở màn hình cập nhật thông tin | 1. Truy cập `/user/account` hoặc click vào avatar | Hiển thị màn hình với thông tin hiện tại đã điền sẵn | | Pass | 11/15/2025 | |
| FUNC-CapNhatTT-02 | Cập nhật thiếu Họ và tên | 1. Truy cập `/user/account`<br>2. Xóa Họ và tên<br>3. Click [Lưu] | Hiển thị thông báo lỗi: "Họ và tên là bắt buộc" | | Pass | 11/15/2025 | |
| FUNC-CapNhatTT-03 | Cập nhật Số điện thoại không đúng định dạng | 1. Truy cập `/user/account`<br>2. Nhập Số điện thoại = "123"<br>3. Click [Lưu] | Hiển thị thông báo lỗi: "Số điện thoại không đúng định dạng" | | Pass | 11/15/2025 | |
| FUNC-CapNhatTT-04 | Cập nhật Số điện thoại đã được sử dụng | 1. Truy cập `/user/account`<br>2. Nhập Số điện thoại đã được sử dụng bởi tài khoản khác<br>3. Click [Lưu] | Hiển thị thông báo lỗi: "Số điện thoại đã được sử dụng" | | Pass | 11/15/2025 | |
| FUNC-CapNhatTT-05 | Cập nhật Ngày sinh là tương lai | 1. Truy cập `/user/account`<br>2. Chọn Ngày sinh > ngày hiện tại<br>3. Click [Lưu] | Hiển thị thông báo lỗi: "Ngày sinh không được là tương lai" | | Pass | 11/15/2025 | |
| FUNC-CapNhatTT-06 | Cập nhật Quận/Huyện phụ thuộc Thành phố | 1. Truy cập `/user/account`<br>2. Chọn Thành phố<br>3. Kiểm tra dropdown Quận/Huyện | Danh sách Quận/Huyện được cập nhật theo Thành phố đã chọn | | Pass | 11/15/2025 | |
| FUNC-CapNhatTT-07 | Cập nhật Phường/Xã phụ thuộc Quận/Huyện | 1. Truy cập `/user/account`<br>2. Chọn Quận/Huyện<br>3. Kiểm tra dropdown Phường/Xã | Danh sách Phường/Xã được cập nhật theo Quận/Huyện đã chọn | | Pass | 11/15/2025 | |
| FUNC-CapNhatTT-08 | Đổi ảnh đại diện - file không đúng định dạng | 1. Truy cập `/user/account`<br>2. Click [Đổi ảnh đại diện]<br>3. Chọn file không phải ảnh (.txt, .pdf)<br>4. Click [Lưu] | Hiển thị thông báo lỗi: "File phải là định dạng ảnh (jpg, png, gif)" | | Pass | 11/15/2025 | |
| FUNC-CapNhatTT-09 | Đổi ảnh đại diện - file quá lớn | 1. Truy cập `/user/account`<br>2. Click [Đổi ảnh đại diện]<br>3. Chọn file ảnh > 5MB<br>4. Click [Lưu] | Hiển thị thông báo lỗi: "Kích thước file không được vượt quá 5MB" | | Pass | 11/15/2025 | |
| FUNC-CapNhatTT-10 | Đổi ảnh đại diện thành công | 1. Truy cập `/user/account`<br>2. Click [Đổi ảnh đại diện]<br>3. Chọn file ảnh hợp lệ<br>4. Click [Lưu] | Ảnh đại diện được cập nhật thành công, hiển thị ảnh mới | | Pass | 11/15/2025 | |
| FUNC-CapNhatTT-11 | Cập nhật thông tin thành công | 1. Truy cập `/user/account`<br>2. Điền đầy đủ thông tin hợp lệ<br>3. Click [Lưu] | Cập nhật thành công, thông tin mới được hiển thị | | Pass | 11/15/2025 | |
| FUNC-CapNhatTT-12 | Xem thông tin thống kê | 1. Truy cập `/user/account` | Hiển thị: Ngày tham gia, Hạng thành viên, Tổng đơn hàng, Tổng chi tiêu | | Pass | 11/15/2025 | |
| FUNC-CapNhatTT-13 | Click nút Hủy | 1. Truy cập `/user/account`<br>2. Thay đổi một số thông tin<br>3. Click [Hủy] | Form được reset về giá trị ban đầu, không lưu thay đổi | | Pass | 11/15/2025 | |
| **Function: Khôi phục mật khẩu** |
| **Check GUI: Khôi phục mật khẩu** |
| GUI-KhoiPhucMK-01 | Check [Email] Input | 1. Truy cập `/user/auth/forgot-password`<br>2. Kiểm tra ô [Email] | Status: visible, enable, Type: email | | Pass | 11/15/2025 | |
| GUI-KhoiPhucMK-02 | Check [Gửi mã khôi phục] Button | 1. Truy cập `/user/auth/forgot-password`<br>2. Kiểm tra nút [Gửi mã khôi phục] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-KhoiPhucMK-03 | Check [Mã OTP] Input | 1. Truy cập `/user/auth/forgot-password`<br>2. Nhập Email và click [Gửi mã khôi phục]<br>3. Kiểm tra ô [Mã OTP] | Status: visible, enable, Type: text | | Pass | 11/15/2025 | |
| GUI-KhoiPhucMK-04 | Check [Mật khẩu mới] Input | 1. Truy cập `/user/auth/forgot-password`<br>2. Nhập OTP<br>3. Kiểm tra ô [Mật khẩu mới] | Status: visible, enable, Type: password | | Pass | 11/15/2025 | |
| GUI-KhoiPhucMK-05 | Check [Xác nhận mật khẩu mới] Input | 1. Truy cập `/user/auth/forgot-password`<br>2. Nhập OTP<br>3. Kiểm tra ô [Xác nhận mật khẩu mới] | Status: visible, enable, Type: password | | Pass | 11/15/2025 | |
| **Check FUNC: Khôi phục mật khẩu** |
| FUNC-KhoiPhucMK-01 | Mở màn hình khôi phục mật khẩu | 1. Truy cập `/user/auth/login`<br>2. Click [Quên mật khẩu] hoặc truy cập `/user/auth/forgot-password` | Hiển thị màn hình khôi phục mật khẩu | | Pass | 11/15/2025 | |
| FUNC-KhoiPhucMK-02 | Khôi phục mật khẩu - Email không tồn tại | 1. Truy cập `/user/auth/forgot-password`<br>2. Nhập Email không tồn tại<br>3. Click [Gửi mã khôi phục] | Hiển thị thông báo lỗi: "Email không tồn tại trong hệ thống" | | Pass | 11/15/2025 | |
| FUNC-KhoiPhucMK-03 | Khôi phục mật khẩu - Email không đúng định dạng | 1. Truy cập `/user/auth/forgot-password`<br>2. Nhập Email = "invalid-email"<br>3. Click [Gửi mã khôi phục] | Hiển thị thông báo lỗi: "Email không đúng định dạng" | | Pass | 11/15/2025 | |
| FUNC-KhoiPhucMK-04 | Khôi phục mật khẩu - Gửi mã OTP thành công | 1. Truy cập `/user/auth/forgot-password`<br>2. Nhập Email hợp lệ<br>3. Click [Gửi mã khôi phục] | Mã OTP được gửi đến email, hiển thị form nhập OTP | | Pass | 11/15/2025 | |
| FUNC-KhoiPhucMK-05 | Khôi phục mật khẩu - OTP sai | 1. Truy cập `/user/auth/forgot-password`<br>2. Nhập Email và nhận OTP<br>3. Nhập OTP sai<br>4. Click [Xác nhận] | Hiển thị thông báo lỗi: "Mã OTP không đúng" | | Pass | 11/15/2025 | |
| FUNC-KhoiPhucMK-06 | Khôi phục mật khẩu - OTP hết hạn | 1. Truy cập `/user/auth/forgot-password`<br>2. Nhập Email và nhận OTP<br>3. Đợi OTP hết hạn<br>4. Nhập OTP<br>5. Click [Xác nhận] | Hiển thị thông báo lỗi: "Mã OTP đã hết hạn" | | Pass | 11/15/2025 | |
| FUNC-KhoiPhucMK-07 | Khôi phục mật khẩu - Mật khẩu mới không đủ mạnh | 1. Truy cập `/user/auth/forgot-password`<br>2. Nhập OTP đúng<br>3. Nhập Mật khẩu mới = "1234567"<br>4. Click [Xác nhận] | Hiển thị thông báo lỗi: "Mật khẩu phải có ít nhất 8 ký tự" | | Pass | 11/15/2025 | |
| FUNC-KhoiPhucMK-08 | Khôi phục mật khẩu thành công | 1. Truy cập `/user/auth/forgot-password`<br>2. Nhập Email hợp lệ<br>3. Nhập OTP đúng<br>4. Nhập Mật khẩu mới hợp lệ<br>5. Click [Xác nhận] | Khôi phục mật khẩu thành công, chuyển đến trang đăng nhập | | Pass | 11/15/2025 | |
| **Function: Quản lý địa chỉ** |
| **Check GUI: Quản lý địa chỉ** |
| GUI-QLDiaChi-01 | Check danh sách địa chỉ | 1. Truy cập `/user/account/addresses` | Status: visible, hiển thị danh sách địa chỉ đã lưu | | Pass | 11/15/2025 | |
| GUI-QLDiaChi-02 | Check [Thêm địa chỉ] Button | 1. Truy cập `/user/account/addresses`<br>2. Kiểm tra nút [Thêm địa chỉ] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-QLDiaChi-03 | Check [Chỉnh sửa] Button | 1. Truy cập `/user/account/addresses`<br>2. Kiểm tra nút [Chỉnh sửa] trên mỗi địa chỉ | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-QLDiaChi-04 | Check [Xóa] Button | 1. Truy cập `/user/account/addresses`<br>2. Kiểm tra nút [Xóa] trên mỗi địa chỉ | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-QLDiaChi-05 | Check [Đặt làm mặc định] Button | 1. Truy cập `/user/account/addresses`<br>2. Kiểm tra nút [Đặt làm mặc định] | Status: visible, enable | | Pass | 11/15/2025 | |
| **Check FUNC: Quản lý địa chỉ** |
| FUNC-QLDiaChi-01 | Mở màn hình quản lý địa chỉ | 1. Truy cập `/user/account/addresses` | Hiển thị danh sách địa chỉ đã lưu | | Pass | 11/15/2025 | |
| FUNC-QLDiaChi-02 | Thêm địa chỉ mới | 1. Truy cập `/user/account/addresses`<br>2. Click [Thêm địa chỉ]<br>3. Điền thông tin địa chỉ<br>4. Click [Lưu] | Thêm địa chỉ thành công, hiển thị trong danh sách | | Pass | 11/15/2025 | |
| FUNC-QLDiaChi-03 | Chỉnh sửa địa chỉ | 1. Truy cập `/user/account/addresses`<br>2. Click [Chỉnh sửa] trên một địa chỉ<br>3. Sửa thông tin<br>4. Click [Lưu] | Cập nhật địa chỉ thành công | | Pass | 11/15/2025 | |
| FUNC-QLDiaChi-04 | Xóa địa chỉ | 1. Truy cập `/user/account/addresses`<br>2. Click [Xóa] trên một địa chỉ<br>3. Xác nhận xóa | Xóa địa chỉ thành công, địa chỉ bị xóa khỏi danh sách | | Pass | 11/15/2025 | |
| FUNC-QLDiaChi-05 | Đặt địa chỉ làm mặc định | 1. Truy cập `/user/account/addresses`<br>2. Click [Đặt làm mặc định] trên một địa chỉ | Địa chỉ được đặt làm mặc định, hiển thị badge "Mặc định" | | Pass | 11/15/2025 | |
| **Function: Quản lý thanh toán** |
| **Check GUI: Quản lý thanh toán** |
| GUI-QLThanhToan-01 | Check danh sách phương thức thanh toán | 1. Truy cập `/user/account/payments` | Status: visible, hiển thị danh sách phương thức thanh toán đã lưu | | Pass | 11/15/2025 | |
| GUI-QLThanhToan-02 | Check [Thêm phương thức] Button | 1. Truy cập `/user/account/payments`<br>2. Kiểm tra nút [Thêm phương thức] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-QLThanhToan-03 | Check [Xóa] Button | 1. Truy cập `/user/account/payments`<br>2. Kiểm tra nút [Xóa] trên mỗi phương thức | Status: visible, enable | | Pass | 11/15/2025 | |
| **Check FUNC: Quản lý thanh toán** |
| FUNC-QLThanhToan-01 | Mở màn hình quản lý thanh toán | 1. Truy cập `/user/account/payments` | Hiển thị danh sách phương thức thanh toán đã lưu | | Pass | 11/15/2025 | |
| FUNC-QLThanhToan-02 | Thêm phương thức thanh toán mới | 1. Truy cập `/user/account/payments`<br>2. Click [Thêm phương thức]<br>3. Điền thông tin<br>4. Click [Lưu] | Thêm phương thức thanh toán thành công | | Pass | 11/15/2025 | |
| FUNC-QLThanhToan-03 | Xóa phương thức thanh toán | 1. Truy cập `/user/account/payments`<br>2. Click [Xóa] trên một phương thức<br>3. Xác nhận xóa | Xóa phương thức thanh toán thành công | | Pass | 11/15/2025 | |
| **Function: Xem hạng thành viên** |
| **Check GUI: Xem hạng thành viên** |
| GUI-XemHangTV-01 | Check thông tin hạng thành viên | 1. Truy cập `/user/account/rank` | Status: visible, hiển thị hạng thành viên hiện tại, điểm tích lũy, quyền lợi | | Pass | 11/15/2025 | |
| **Check FUNC: Xem hạng thành viên** |
| FUNC-XemHangTV-01 | Mở màn hình xem hạng thành viên | 1. Truy cập `/user/account/rank` | Hiển thị thông tin: Hạng hiện tại, Điểm tích lũy, Quyền lợi, Điểm cần để lên hạng tiếp theo | | Pass | 11/15/2025 | |

---

## GHI CHÚ

- Tất cả test cases cần được thực hiện trên môi trường test
- Routes động (có `[id]`) cần thay thế bằng ID thực tế khi test
- Các test case GUI kiểm tra giao diện và trạng thái của các thành phần
- Các test case FUNC kiểm tra chức năng và logic nghiệp vụ
- Cần cập nhật cột Result, Test date sau khi thực hiện test

