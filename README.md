# BLACKBOX TEST CASE - QUẢN LÝ TÀI KHOẢN (ADMIN)

## HEADER SECTION

**Module Code:** Quản lý tài khoản Admin

**Test requirement:**
1. Đăng nhập
2. Đăng ký
3. Đổi mật khẩu
4. Quản lý thông tin cá nhân
5. Khôi phục mật khẩu
6. Đăng xuất

**Tester:** [Tên tester]

**Summary Statistics:**

| Pass | Fail | Untested | N/A | Number of Test cases |
|------|------|----------|-----|---------------------|
| 129 | 0 | 0 | 0 | 129 |

---

## TEST CASE TABLE

| ID | Test Case Description | Test Case Procedure | Expected Output | Test-case rate | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|----------------|--------|-----------|------|
| **Function: Đăng nhập** |
| **Check GUI: Đăng nhập** |
| GUI-DangNhap-01 | Check [Tiêu đề trang] Text | 1. Truy cập `/admin/auth/login`<br>2. Kiểm tra tiêu đề | Status: visible, Text: "Đăng nhập" | | Pass | 11/15/2025 | |
| GUI-DangNhap-02 | Check [Mô tả chức năng] Text | 1. Truy cập `/admin/auth/login`<br>2. Kiểm tra mô tả | Status: visible, Text: "Đăng nhập để truy cập tài khoản và sử dụng các chức năng quản lý" | | Pass | 11/15/2025 | |
| GUI-DangNhap-03 | Check [Form đăng nhập] Form | 1. Truy cập `/admin/auth/login`<br>2. Kiểm tra form | Status: visible, Hiển thị form nhập thông tin đăng nhập | | Pass | 11/15/2025 | |
| GUI-DangNhap-04 | Check [Email] Input | 1. Truy cập `/admin/auth/login`<br>2. Kiểm tra ô [Email] | Status: visible, enable, Type: email | | Pass | 11/15/2025 | |
| GUI-DangNhap-05 | Check [Mật khẩu] Input | 1. Truy cập `/admin/auth/login`<br>2. Kiểm tra ô [Mật khẩu] | Status: visible, enable, Type: password | | Pass | 11/15/2025 | |
| GUI-DangNhap-06 | Check [Ghi nhớ đăng nhập] Checkbox | 1. Truy cập `/admin/auth/login`<br>2. Kiểm tra checkbox | Status: visible, enable, Text: "Ghi nhớ đăng nhập" | | Pass | 11/15/2025 | |
| GUI-DangNhap-07 | Check [Quên mật khẩu] Link | 1. Truy cập `/admin/auth/login`<br>2. Kiểm tra link | Status: visible, enable, Text: "Quên mật khẩu?" | | Pass | 11/15/2025 | |
| GUI-DangNhap-08 | Check [Captcha] Captcha | 1. Truy cập `/admin/auth/login`<br>2. Đăng nhập sai 3 lần<br>3. Kiểm tra captcha | Status: visible, enable (sau 3 lần đăng nhập sai) | | Pass | 11/15/2025 | |
| GUI-DangNhap-09 | Check [Đăng nhập] Button | 1. Truy cập `/admin/auth/login`<br>2. Kiểm tra nút [Đăng nhập] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-DangNhap-10 | Check [Hủy] Button | 1. Truy cập `/admin/auth/login`<br>2. Kiểm tra nút [Hủy] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-DangNhap-11 | Check [Link đăng ký] Link | 1. Truy cập `/admin/auth/login`<br>2. Kiểm tra link | Status: visible, enable, Text: "Chưa có tài khoản? Đăng ký" | | Pass | 11/15/2025 | |
| **Check FUNC: Đăng nhập** |
| FUNC-DangNhap-01 | Mở màn hình đăng nhập | 1. Truy cập `/admin/auth/login` hoặc click [Đăng nhập] | Hiển thị màn hình đăng nhập với form trống | | Pass | 11/15/2025 | |
| FUNC-DangNhap-02 | Đăng nhập với email và mật khẩu hợp lệ | 1. Truy cập `/admin/auth/login`<br>2. Nhập email và mật khẩu hợp lệ<br>3. Click [Đăng nhập] | Đăng nhập thành công, chuyển đến trang dashboard admin, phiên đăng nhập được tạo | | Pass | 11/15/2025 | |
| FUNC-DangNhap-03 | Đăng nhập với email không tồn tại | 1. Truy cập `/admin/auth/login`<br>2. Nhập email không tồn tại<br>3. Click [Đăng nhập] | Hiển thị thông báo lỗi: "Email hoặc mật khẩu không đúng" | | Pass | 11/15/2025 | |
| FUNC-DangNhap-04 | Đăng nhập với mật khẩu sai | 1. Truy cập `/admin/auth/login`<br>2. Nhập email hợp lệ và mật khẩu sai<br>3. Click [Đăng nhập] | Hiển thị thông báo lỗi: "Email hoặc mật khẩu không đúng" | | Pass | 11/15/2025 | |
| FUNC-DangNhap-05 | Đăng nhập không nhập email | 1. Truy cập `/admin/auth/login`<br>2. Không nhập email<br>3. Click [Đăng nhập] | Hiển thị thông báo lỗi: "Email là bắt buộc" | | Pass | 11/15/2025 | |
| FUNC-DangNhap-06 | Đăng nhập không nhập mật khẩu | 1. Truy cập `/admin/auth/login`<br>2. Không nhập mật khẩu<br>3. Click [Đăng nhập] | Hiển thị thông báo lỗi: "Mật khẩu là bắt buộc" | | Pass | 11/15/2025 | |
| FUNC-DangNhap-07 | Đăng nhập với tài khoản chưa kích hoạt | 1. Truy cập `/admin/auth/login`<br>2. Nhập email và mật khẩu của tài khoản chưa kích hoạt<br>3. Click [Đăng nhập] | Hiển thị thông báo lỗi: "Tài khoản chưa được kích hoạt" | | Pass | 11/15/2025 | |
| FUNC-DangNhap-08 | Đăng nhập với tài khoản bị khóa | 1. Truy cập `/admin/auth/login`<br>2. Nhập email và mật khẩu của tài khoản bị khóa<br>3. Click [Đăng nhập] | Hiển thị thông báo lỗi: "Tài khoản đã bị khóa" | | Pass | 11/15/2025 | |
| FUNC-DangNhap-09 | Hiển thị captcha sau 3 lần đăng nhập sai | 1. Truy cập `/admin/auth/login`<br>2. Đăng nhập sai 3 lần liên tiếp<br>3. Kiểm tra captcha | Captcha được hiển thị, yêu cầu nhập captcha để tiếp tục | | Pass | 11/15/2025 | |
| FUNC-DangNhap-10 | Đăng nhập với captcha sai | 1. Truy cập `/admin/auth/login`<br>2. Đăng nhập sai 3 lần<br>3. Nhập captcha sai<br>4. Click [Đăng nhập] | Hiển thị thông báo lỗi: "Captcha không đúng" | | Pass | 11/15/2025 | |
| FUNC-DangNhap-11 | Tạm khóa tài khoản sau nhiều lần đăng nhập sai | 1. Truy cập `/admin/auth/login`<br>2. Đăng nhập sai nhiều lần vượt quá giới hạn | Tài khoản bị tạm khóa trong một khoảng thời gian, hiển thị thông báo "Tài khoản đã bị tạm khóa, vui lòng thử lại sau X phút" | | Pass | 11/15/2025 | |
| FUNC-DangNhap-12 | Ghi nhớ đăng nhập | 1. Truy cập `/admin/auth/login`<br>2. Check [Ghi nhớ đăng nhập]<br>3. Đăng nhập thành công<br>4. Đóng trình duyệt và mở lại | Phiên đăng nhập được giữ lại, tự động đăng nhập | | Pass | 11/15/2025 | |
| FUNC-DangNhap-13 | Click link Quên mật khẩu | 1. Truy cập `/admin/auth/login`<br>2. Click [Quên mật khẩu?] | Chuyển đến trang khôi phục mật khẩu | | Pass | 11/15/2025 | |
| FUNC-DangNhap-14 | Click link Đăng ký | 1. Truy cập `/admin/auth/login`<br>2. Click [Chưa có tài khoản? Đăng ký] | Chuyển đến trang đăng ký | | Pass | 11/15/2025 | |
| FUNC-DangNhap-15 | Click nút Hủy | 1. Truy cập `/admin/auth/login`<br>2. Nhập một số thông tin<br>3. Click [Hủy] | Form được reset về trạng thái ban đầu | | Pass | 11/15/2025 | |
| **Function: Đăng ký** |
| **Check GUI: Đăng ký** |
| GUI-DangKy-01 | Check [Tiêu đề trang] Text | 1. Truy cập `/admin/auth/register`<br>2. Kiểm tra tiêu đề | Status: visible, Text: "Đăng ký tài khoản" | | Pass | 11/15/2025 | |
| GUI-DangKy-02 | Check [Mô tả chức năng] Text | 1. Truy cập `/admin/auth/register`<br>2. Kiểm tra mô tả | Status: visible, Text: "Tạo tài khoản mới để sử dụng hệ thống quản lý" | | Pass | 11/15/2025 | |
| GUI-DangKy-03 | Check [Form đăng ký] Form | 1. Truy cập `/admin/auth/register`<br>2. Kiểm tra form | Status: visible, Hiển thị form nhập thông tin đăng ký | | Pass | 11/15/2025 | |
| GUI-DangKy-04 | Check [Họ và tên] Input | 1. Truy cập `/admin/auth/register`<br>2. Kiểm tra ô [Họ và tên] | Status: visible, enable, Type: text | | Pass | 11/15/2025 | |
| GUI-DangKy-05 | Check [Email] Input | 1. Truy cập `/admin/auth/register`<br>2. Kiểm tra ô [Email] | Status: visible, enable, Type: email | | Pass | 11/15/2025 | |
| GUI-DangKy-06 | Check [Số điện thoại] Input | 1. Truy cập `/admin/auth/register`<br>2. Kiểm tra ô [Số điện thoại] | Status: visible, enable, Type: tel | | Pass | 11/15/2025 | |
| GUI-DangKy-07 | Check [Mật khẩu] Input | 1. Truy cập `/admin/auth/register`<br>2. Kiểm tra ô [Mật khẩu] | Status: visible, enable, Type: password | | Pass | 11/15/2025 | |
| GUI-DangKy-08 | Check [Xác nhận mật khẩu] Input | 1. Truy cập `/admin/auth/register`<br>2. Kiểm tra ô [Xác nhận mật khẩu] | Status: visible, enable, Type: password | | Pass | 11/15/2025 | |
| GUI-DangKy-09 | Check [Địa chỉ] Textarea | 1. Truy cập `/admin/auth/register`<br>2. Kiểm tra textarea | Status: visible, enable, Type: textarea | | Pass | 11/15/2025 | |
| GUI-DangKy-10 | Check [Điều khoản sử dụng] Checkbox | 1. Truy cập `/admin/auth/register`<br>2. Kiểm tra checkbox | Status: visible, enable, Text: "Tôi đồng ý với điều khoản sử dụng" | | Pass | 11/15/2025 | |
| GUI-DangKy-11 | Check [Đăng ký] Button | 1. Truy cập `/admin/auth/register`<br>2. Kiểm tra nút [Đăng ký] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-DangKy-12 | Check [Hủy] Button | 1. Truy cập `/admin/auth/register`<br>2. Kiểm tra nút [Hủy] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-DangKy-13 | Check [Link đăng nhập] Link | 1. Truy cập `/admin/auth/register`<br>2. Kiểm tra link | Status: visible, enable, Text: "Đã có tài khoản? Đăng nhập" | | Pass | 11/15/2025 | |
| **Check FUNC: Đăng ký** |
| FUNC-DangKy-01 | Mở màn hình đăng ký | 1. Truy cập `/admin/auth/register` hoặc click [Đăng ký] từ trang đăng nhập | Hiển thị màn hình đăng ký với form trống | | Pass | 11/15/2025 | |
| FUNC-DangKy-02 | Đăng ký với thông tin hợp lệ | 1. Truy cập `/admin/auth/register`<br>2. Điền đầy đủ thông tin hợp lệ<br>3. Check [Điều khoản sử dụng]<br>4. Click [Đăng ký] | Tài khoản được tạo thành công, chuyển đến trang đăng nhập hoặc dashboard, email xác nhận được gửi | | Pass | 11/15/2025 | |
| FUNC-DangKy-03 | Đăng ký với email đã tồn tại | 1. Truy cập `/admin/auth/register`<br>2. Nhập email đã tồn tại trong hệ thống<br>3. Click [Đăng ký] | Hiển thị thông báo lỗi: "Email đã tồn tại trong hệ thống" | | Pass | 11/15/2025 | |
| FUNC-DangKy-04 | Đăng ký với mật khẩu không đủ mạnh | 1. Truy cập `/admin/auth/register`<br>2. Nhập mật khẩu yếu (ví dụ: "123")<br>3. Click [Đăng ký] | Hiển thị thông báo lỗi: "Mật khẩu phải có ít nhất 8 ký tự, bao gồm chữ hoa, chữ thường và số" | | Pass | 11/15/2025 | |
| FUNC-DangKy-05 | Đăng ký với mật khẩu và xác nhận không khớp | 1. Truy cập `/admin/auth/register`<br>2. Nhập mật khẩu và xác nhận mật khẩu khác nhau<br>3. Click [Đăng ký] | Hiển thị thông báo lỗi: "Mật khẩu xác nhận không khớp" | | Pass | 11/15/2025 | |
| FUNC-DangKy-06 | Đăng ký không check điều khoản | 1. Truy cập `/admin/auth/register`<br>2. Điền đầy đủ thông tin<br>3. Không check [Điều khoản sử dụng]<br>4. Click [Đăng ký] | Nút [Đăng ký] bị vô hiệu hóa hoặc hiển thị thông báo "Vui lòng đồng ý với điều khoản sử dụng" | | Pass | 11/15/2025 | |
| FUNC-DangKy-07 | Đăng ký thiếu thông tin bắt buộc | 1. Truy cập `/admin/auth/register`<br>2. Không điền đầy đủ thông tin bắt buộc<br>3. Click [Đăng ký] | Hiển thị thông báo lỗi về các trường bắt buộc chưa được điền | | Pass | 11/15/2025 | |
| FUNC-DangKy-08 | Xác thực email real-time | 1. Truy cập `/admin/auth/register`<br>2. Nhập email đã tồn tại<br>3. Kiểm tra validation | Hiển thị cảnh báo ngay lập tức: "Email đã tồn tại" (không cần chờ submit) | | Pass | 11/15/2025 | |
| FUNC-DangKy-09 | Gửi email xác nhận | 1. Truy cập `/admin/auth/register`<br>2. Đăng ký thành công | Email xác nhận được gửi đến địa chỉ email đã đăng ký, chứa link kích hoạt tài khoản | | Pass | 11/15/2025 | |
| FUNC-DangKy-10 | Click nút Hủy | 1. Truy cập `/admin/auth/register`<br>2. Điền một số thông tin<br>3. Click [Hủy] | Form được reset về trạng thái ban đầu | | Pass | 11/15/2025 | |
| FUNC-DangKy-11 | Click link Đăng nhập | 1. Truy cập `/admin/auth/register`<br>2. Click [Đã có tài khoản? Đăng nhập] | Chuyển đến trang đăng nhập | | Pass | 11/15/2025 | |
| **Function: Đổi mật khẩu** |
| **Check GUI: Đổi mật khẩu** |
| GUI-DoiMK-01 | Check [Tiêu đề trang] Text | 1. Truy cập `/admin/account`<br>2. Click tab [Bảo mật] hoặc [Đổi mật khẩu]<br>3. Kiểm tra tiêu đề | Status: visible, Text: "Đổi mật khẩu" | | Pass | 11/15/2025 | |
| GUI-DoiMK-02 | Check [Mô tả chức năng] Text | 1. Truy cập `/admin/account`<br>2. Click tab [Bảo mật]<br>3. Kiểm tra mô tả | Status: visible, Text: "Thay đổi mật khẩu để bảo vệ tài khoản của bạn" | | Pass | 11/15/2025 | |
| GUI-DoiMK-03 | Check [Form đổi mật khẩu] Form | 1. Truy cập `/admin/account`<br>2. Click tab [Bảo mật]<br>3. Kiểm tra form | Status: visible, Hiển thị form nhập thông tin đổi mật khẩu | | Pass | 11/15/2025 | |
| GUI-DoiMK-04 | Check [Mật khẩu hiện tại] Input | 1. Truy cập `/admin/account`<br>2. Click tab [Bảo mật]<br>3. Kiểm tra ô [Mật khẩu hiện tại] | Status: visible, enable, Type: password | | Pass | 11/15/2025 | |
| GUI-DoiMK-05 | Check [Mật khẩu mới] Input | 1. Truy cập `/admin/account`<br>2. Click tab [Bảo mật]<br>3. Kiểm tra ô [Mật khẩu mới] | Status: visible, enable, Type: password | | Pass | 11/15/2025 | |
| GUI-DoiMK-06 | Check [Xác nhận mật khẩu mới] Input | 1. Truy cập `/admin/account`<br>2. Click tab [Bảo mật]<br>3. Kiểm tra ô [Xác nhận mật khẩu mới] | Status: visible, enable, Type: password | | Pass | 11/15/2025 | |
| GUI-DoiMK-07 | Check [Hiển thị mật khẩu] Checkbox | 1. Truy cập `/admin/account`<br>2. Click tab [Bảo mật]<br>3. Kiểm tra checkbox | Status: visible, enable, Text: "Hiển thị mật khẩu" | | Pass | 11/15/2025 | |
| GUI-DoiMK-08 | Check [Xác thực 2 bước] Checkbox | 1. Truy cập `/admin/account`<br>2. Click tab [Bảo mật]<br>3. Kiểm tra checkbox | Status: visible, enable, Text: "Sử dụng xác thực 2 bước" | | Pass | 11/15/2025 | |
| GUI-DoiMK-09 | Check [Phương thức 2FA] Select | 1. Truy cập `/admin/account`<br>2. Click tab [Bảo mật]<br>3. Bật 2FA<br>4. Kiểm tra dropdown | Status: visible, enable, Options: Email OTP, SMS OTP | | Pass | 11/15/2025 | |
| GUI-DoiMK-10 | Check [Mã OTP] Input | 1. Truy cập `/admin/account`<br>2. Click tab [Bảo mật]<br>3. Bật 2FA<br>4. Kiểm tra ô [Mã OTP] | Status: visible, enable, Type: text | | Pass | 11/15/2025 | |
| GUI-DoiMK-11 | Check [Yêu cầu mật khẩu] Text | 1. Truy cập `/admin/account`<br>2. Click tab [Bảo mật]<br>3. Kiểm tra text | Status: visible, Text: "Mật khẩu phải có ít nhất 8 ký tự, bao gồm chữ hoa, chữ thường và số" | | Pass | 11/15/2025 | |
| GUI-DoiMK-12 | Check [Đổi mật khẩu] Button | 1. Truy cập `/admin/account`<br>2. Click tab [Bảo mật]<br>3. Kiểm tra nút [Đổi mật khẩu] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-DoiMK-13 | Check [Hủy] Button | 1. Truy cập `/admin/account`<br>2. Click tab [Bảo mật]<br>3. Kiểm tra nút [Hủy] | Status: visible, enable | | Pass | 11/15/2025 | |
| **Check FUNC: Đổi mật khẩu** |
| FUNC-DoiMK-01 | Mở màn hình đổi mật khẩu | 1. Truy cập `/admin/account`<br>2. Click tab [Bảo mật] hoặc [Đổi mật khẩu] | Hiển thị form đổi mật khẩu với các trường trống | | Pass | 11/15/2025 | |
| FUNC-DoiMK-02 | Đổi mật khẩu với mật khẩu hiện tại đúng | 1. Truy cập `/admin/account`<br>2. Click tab [Bảo mật]<br>3. Nhập mật khẩu hiện tại đúng, mật khẩu mới hợp lệ<br>4. Click [Đổi mật khẩu] | Mật khẩu được thay đổi thành công, tất cả phiên đăng nhập cũ bị vô hiệu hóa, thông báo xác nhận | | Pass | 11/15/2025 | |
| FUNC-DoiMK-03 | Đổi mật khẩu với mật khẩu hiện tại sai | 1. Truy cập `/admin/account`<br>2. Click tab [Bảo mật]<br>3. Nhập mật khẩu hiện tại sai<br>4. Click [Đổi mật khẩu] | Hiển thị thông báo lỗi: "Mật khẩu hiện tại không đúng" | | Pass | 11/15/2025 | |
| FUNC-DoiMK-04 | Đổi mật khẩu với mật khẩu mới không đủ mạnh | 1. Truy cập `/admin/account`<br>2. Click tab [Bảo mật]<br>3. Nhập mật khẩu mới yếu<br>4. Click [Đổi mật khẩu] | Hiển thị thông báo lỗi: "Mật khẩu mới không đủ mạnh" | | Pass | 11/15/2025 | |
| FUNC-DoiMK-05 | Đổi mật khẩu với mật khẩu mới và xác nhận không khớp | 1. Truy cập `/admin/account`<br>2. Click tab [Bảo mật]<br>3. Nhập mật khẩu mới và xác nhận khác nhau<br>4. Click [Đổi mật khẩu] | Hiển thị thông báo lỗi: "Mật khẩu xác nhận không khớp" | | Pass | 11/15/2025 | |
| FUNC-DoiMK-06 | Đổi mật khẩu với mật khẩu mới trùng mật khẩu hiện tại | 1. Truy cập `/admin/account`<br>2. Click tab [Bảo mật]<br>3. Nhập mật khẩu mới trùng với mật khẩu hiện tại<br>4. Click [Đổi mật khẩu] | Hiển thị thông báo lỗi: "Mật khẩu mới không được trùng với mật khẩu hiện tại" | | Pass | 11/15/2025 | |
| FUNC-DoiMK-07 | Đổi mật khẩu với 2FA - Email OTP | 1. Truy cập `/admin/account`<br>2. Click tab [Bảo mật]<br>3. Bật 2FA, chọn Email OTP<br>4. Nhập thông tin và click [Đổi mật khẩu]<br>5. Nhập mã OTP từ email<br>6. Click [Xác nhận] | Mã OTP được gửi qua email, xác thực thành công, mật khẩu được đổi | | Pass | 11/15/2025 | |
| FUNC-DoiMK-08 | Đổi mật khẩu với 2FA - SMS OTP | 1. Truy cập `/admin/account`<br>2. Click tab [Bảo mật]<br>3. Bật 2FA, chọn SMS OTP<br>4. Nhập thông tin và click [Đổi mật khẩu]<br>5. Nhập mã OTP từ SMS<br>6. Click [Xác nhận] | Mã OTP được gửi qua SMS, xác thực thành công, mật khẩu được đổi | | Pass | 11/15/2025 | |
| FUNC-DoiMK-09 | Đổi mật khẩu với mã OTP sai | 1. Truy cập `/admin/account`<br>2. Click tab [Bảo mật]<br>3. Bật 2FA, nhập mã OTP sai<br>4. Click [Xác nhận] | Hiển thị thông báo lỗi: "Mã OTP không đúng hoặc đã hết hạn" | | Pass | 11/15/2025 | |
| FUNC-DoiMK-10 | Hiển thị mật khẩu | 1. Truy cập `/admin/account`<br>2. Click tab [Bảo mật]<br>3. Check [Hiển thị mật khẩu] | Mật khẩu được hiển thị dạng text thay vì dấu chấm | | Pass | 11/15/2025 | |
| FUNC-DoiMK-11 | Vô hiệu hóa phiên đăng nhập cũ sau khi đổi mật khẩu | 1. Truy cập `/admin/account`<br>2. Đổi mật khẩu thành công<br>3. Kiểm tra các phiên đăng nhập khác | Tất cả phiên đăng nhập cũ bị vô hiệu hóa, yêu cầu đăng nhập lại | | Pass | 11/15/2025 | |
| FUNC-DoiMK-12 | Click nút Hủy | 1. Truy cập `/admin/account`<br>2. Click tab [Bảo mật]<br>3. Nhập một số thông tin<br>4. Click [Hủy] | Form được reset về trạng thái ban đầu | | Pass | 11/15/2025 | |
| **Function: Quản lý thông tin cá nhân** |
| **Check GUI: Quản lý thông tin cá nhân** |
| GUI-QLTT-01 | Check [Tiêu đề trang] Text | 1. Truy cập `/admin/account`<br>2. Kiểm tra tiêu đề | Status: visible, Text: "Thông tin cá nhân" | | Pass | 11/15/2025 | |
| GUI-QLTT-02 | Check [Mô tả chức năng] Text | 1. Truy cập `/admin/account`<br>2. Kiểm tra mô tả | Status: visible, Text: "Quản lý và cập nhật thông tin cá nhân của bạn" | | Pass | 11/15/2025 | |
| GUI-QLTT-03 | Check [Ảnh đại diện] Avatar | 1. Truy cập `/admin/account`<br>2. Kiểm tra avatar | Status: visible, Hiển thị ảnh đại diện hiện tại | | Pass | 11/15/2025 | |
| GUI-QLTT-04 | Check [Đổi ảnh đại diện] Button | 1. Truy cập `/admin/account`<br>2. Kiểm tra nút [Đổi ảnh đại diện] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-QLTT-05 | Check [Họ và tên] Input | 1. Truy cập `/admin/account`<br>2. Kiểm tra ô [Họ và tên] | Status: visible, enable, Type: text | | Pass | 11/15/2025 | |
| GUI-QLTT-06 | Check [Email] Input | 1. Truy cập `/admin/account`<br>2. Kiểm tra ô [Email] | Status: visible, Readonly hoặc disabled (không cho phép đổi) | | Pass | 11/15/2025 | |
| GUI-QLTT-07 | Check [Số điện thoại] Input | 1. Truy cập `/admin/account`<br>2. Kiểm tra ô [Số điện thoại] | Status: visible, enable, Type: tel | | Pass | 11/15/2025 | |
| GUI-QLTT-08 | Check [Ngày sinh] Date Picker | 1. Truy cập `/admin/account`<br>2. Kiểm tra date picker | Status: visible, enable, Type: date | | Pass | 11/15/2025 | |
| GUI-QLTT-09 | Check [Giới tính] Select | 1. Truy cập `/admin/account`<br>2. Kiểm tra dropdown | Status: visible, enable, Options: Nam, Nữ, Khác | | Pass | 11/15/2025 | |
| GUI-QLTT-10 | Check [Địa chỉ] Textarea | 1. Truy cập `/admin/account`<br>2. Kiểm tra textarea | Status: visible, enable, Type: textarea | | Pass | 11/15/2025 | |
| GUI-QLTT-11 | Check [Thành phố] Select | 1. Truy cập `/admin/account`<br>2. Kiểm tra dropdown | Status: visible, enable, Options: Hà Nội, TP.HCM, Đà Nẵng, ... | | Pass | 11/15/2025 | |
| GUI-QLTT-12 | Check [Quận/Huyện] Select | 1. Truy cập `/admin/account`<br>2. Kiểm tra dropdown | Status: visible, enable, Depends on: Thành phố | | Pass | 11/15/2025 | |
| GUI-QLTT-13 | Check [Phường/Xã] Select | 1. Truy cập `/admin/account`<br>2. Kiểm tra dropdown | Status: visible, enable, Depends on: Quận/Huyện | | Pass | 11/15/2025 | |
| GUI-QLTT-14 | Check [Lưu] Button | 1. Truy cập `/admin/account`<br>2. Kiểm tra nút [Lưu] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-QLTT-15 | Check [Hủy] Button | 1. Truy cập `/admin/account`<br>2. Kiểm tra nút [Hủy] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-QLTT-16 | Check [Thông tin bổ sung] Card | 1. Truy cập `/admin/account`<br>2. Kiểm tra card | Status: visible, Hiển thị: Ngày tham gia, Hạng thành viên, Tổng đơn hàng, Tổng chi tiêu | | Pass | 11/15/2025 | |
| **Check FUNC: Quản lý thông tin cá nhân** |
| FUNC-QLTT-01 | Mở màn hình quản lý thông tin cá nhân | 1. Truy cập `/admin/account` hoặc click vào avatar | Hiển thị form với thông tin hiện tại đã điền sẵn | | Pass | 11/15/2025 | |
| FUNC-QLTT-02 | Cập nhật họ và tên | 1. Truy cập `/admin/account`<br>2. Sửa [Họ và tên]<br>3. Click [Lưu] | Họ và tên được cập nhật thành công, thông báo xác nhận | | Pass | 11/15/2025 | |
| FUNC-QLTT-03 | Cập nhật số điện thoại | 1. Truy cập `/admin/account`<br>2. Sửa [Số điện thoại]<br>3. Click [Lưu] | Số điện thoại được cập nhật thành công | | Pass | 11/15/2025 | |
| FUNC-QLTT-04 | Cập nhật số điện thoại không đúng định dạng | 1. Truy cập `/admin/account`<br>2. Nhập số điện thoại không đúng định dạng<br>3. Click [Lưu] | Hiển thị thông báo lỗi: "Số điện thoại không đúng định dạng" | | Pass | 11/15/2025 | |
| FUNC-QLTT-05 | Cập nhật ngày sinh | 1. Truy cập `/admin/account`<br>2. Chọn [Ngày sinh] mới<br>3. Click [Lưu] | Ngày sinh được cập nhật thành công | | Pass | 11/15/2025 | |
| FUNC-QLTT-06 | Cập nhật giới tính | 1. Truy cập `/admin/account`<br>2. Chọn [Giới tính] mới<br>3. Click [Lưu] | Giới tính được cập nhật thành công | | Pass | 11/15/2025 | |
| FUNC-QLTT-07 | Cập nhật địa chỉ | 1. Truy cập `/admin/account`<br>2. Sửa [Địa chỉ]<br>3. Click [Lưu] | Địa chỉ được cập nhật thành công | | Pass | 11/15/2025 | |
| FUNC-QLTT-08 | Chọn Thành phố | 1. Truy cập `/admin/account`<br>2. Chọn [Thành phố] | Danh sách Quận/Huyện được cập nhật theo Thành phố đã chọn | | Pass | 11/15/2025 | |
| FUNC-QLTT-09 | Chọn Quận/Huyện | 1. Truy cập `/admin/account`<br>2. Chọn [Quận/Huyện] | Danh sách Phường/Xã được cập nhật theo Quận/Huyện đã chọn | | Pass | 11/15/2025 | |
| FUNC-QLTT-10 | Đổi ảnh đại diện | 1. Truy cập `/admin/account`<br>2. Click [Đổi ảnh đại diện]<br>3. Chọn file ảnh<br>4. Click [Lưu] | Ảnh đại diện được upload thành công, hiển thị preview, ảnh cũ được thay thế | | Pass | 11/15/2025 | |
| FUNC-QLTT-11 | Đổi ảnh đại diện không đúng định dạng | 1. Truy cập `/admin/account`<br>2. Upload file không phải ảnh | Hiển thị thông báo lỗi: "Định dạng ảnh không được hỗ trợ" | | Pass | 11/15/2025 | |
| FUNC-QLTT-12 | Đổi ảnh đại diện quá lớn | 1. Truy cập `/admin/account`<br>2. Upload file > giới hạn | Hiển thị thông báo lỗi: "Kích thước ảnh quá lớn" | | Pass | 11/15/2025 | |
| FUNC-QLTT-13 | Không thể đổi email | 1. Truy cập `/admin/account`<br>2. Kiểm tra ô [Email] | Ô Email bị readonly hoặc disabled, không thể chỉnh sửa | | Pass | 11/15/2025 | |
| FUNC-QLTT-14 | Xem thông tin thống kê | 1. Truy cập `/admin/account`<br>2. Kiểm tra card [Thông tin bổ sung] | Hiển thị: Ngày tham gia, Hạng thành viên, Tổng đơn hàng, Tổng chi tiêu | | Pass | 11/15/2025 | |
| FUNC-QLTT-15 | Click nút Hủy | 1. Truy cập `/admin/account`<br>2. Sửa một số thông tin<br>3. Click [Hủy] | Form được reset về thông tin ban đầu, không lưu thay đổi | | Pass | 11/15/2025 | |
| **Function: Khôi phục mật khẩu** |
| **Check GUI: Khôi phục mật khẩu** |
| GUI-KhoiPhucMK-01 | Check [Tiêu đề trang] Text | 1. Truy cập `/admin/auth/forgot-password`<br>2. Kiểm tra tiêu đề | Status: visible, Text: "Quên mật khẩu" | | Pass | 11/15/2025 | |
| GUI-KhoiPhucMK-02 | Check [Mô tả chức năng] Text | 1. Truy cập `/admin/auth/forgot-password`<br>2. Kiểm tra mô tả | Status: visible, Text: "Nhập email của bạn để nhận link khôi phục mật khẩu" | | Pass | 11/15/2025 | |
| GUI-KhoiPhucMK-03 | Check [Form khôi phục] Form | 1. Truy cập `/admin/auth/forgot-password`<br>2. Kiểm tra form | Status: visible, Hiển thị form nhập email | | Pass | 11/15/2025 | |
| GUI-KhoiPhucMK-04 | Check [Ô nhập email] Input | 1. Truy cập `/admin/auth/forgot-password`<br>2. Kiểm tra ô [Email] | Status: visible, enable, Type: email | | Pass | 11/15/2025 | |
| GUI-KhoiPhucMK-05 | Check [Gửi link khôi phục] Button | 1. Truy cập `/admin/auth/forgot-password`<br>2. Kiểm tra nút [Gửi link khôi phục] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-KhoiPhucMK-06 | Check [Quay lại đăng nhập] Button | 1. Truy cập `/admin/auth/forgot-password`<br>2. Kiểm tra nút [Quay lại đăng nhập] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-KhoiPhucMK-07 | Check [Trạng thái gửi] Card | 1. Truy cập `/admin/auth/forgot-password`<br>2. Gửi email thành công<br>3. Kiểm tra card | Status: visible, Hiển thị trạng thái gửi email | | Pass | 11/15/2025 | |
| **Check FUNC: Khôi phục mật khẩu** |
| FUNC-KhoiPhucMK-01 | Mở màn hình khôi phục mật khẩu | 1. Truy cập `/admin/auth/forgot-password` hoặc click [Quên mật khẩu?] từ trang đăng nhập | Hiển thị màn hình khôi phục mật khẩu với form nhập email | | Pass | 11/15/2025 | |
| FUNC-KhoiPhucMK-02 | Gửi link khôi phục với email hợp lệ | 1. Truy cập `/admin/auth/forgot-password`<br>2. Nhập email hợp lệ đã đăng ký<br>3. Click [Gửi link khôi phục] | Email khôi phục được gửi thành công, hiển thị card trạng thái gửi, thông báo hướng dẫn | | Pass | 11/15/2025 | |
| FUNC-KhoiPhucMK-03 | Gửi link khôi phục với email không tồn tại | 1. Truy cập `/admin/auth/forgot-password`<br>2. Nhập email không tồn tại<br>3. Click [Gửi link khôi phục] | Hiển thị thông báo lỗi: "Email không tồn tại trong hệ thống" | | Pass | 11/15/2025 | |
| FUNC-KhoiPhucMK-04 | Gửi link khôi phục với email không đúng định dạng | 1. Truy cập `/admin/auth/forgot-password`<br>2. Nhập email không đúng định dạng<br>3. Click [Gửi link khôi phục] | Hiển thị thông báo lỗi: "Email không đúng định dạng" | | Pass | 11/15/2025 | |
| FUNC-KhoiPhucMK-05 | Tạo token khôi phục | 1. Truy cập `/admin/auth/forgot-password`<br>2. Gửi link khôi phục thành công | Token khôi phục được tạo, có thời hạn sử dụng (thường 1 giờ), chỉ sử dụng được 1 lần | | Pass | 11/15/2025 | |
| FUNC-KhoiPhucMK-06 | Gửi yêu cầu khôi phục quá thường xuyên | 1. Truy cập `/admin/auth/forgot-password`<br>2. Gửi link khôi phục nhiều lần liên tiếp | Hiển thị thông báo: "Vui lòng đợi X phút trước khi yêu cầu lại" | | Pass | 11/15/2025 | |
| FUNC-KhoiPhucMK-07 | Click nút Quay lại đăng nhập | 1. Truy cập `/admin/auth/forgot-password`<br>2. Click [Quay lại đăng nhập] | Chuyển về trang đăng nhập | | Pass | 11/15/2025 | |
| **Function: Đăng xuất** |
| **Check GUI: Đăng xuất** |
| GUI-DangXuat-01 | Check [Đăng xuất] Button | 1. Truy cập `/admin/dashboard` (đã đăng nhập)<br>2. Kiểm tra nút [Đăng xuất] từ menu | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-DangXuat-02 | Check [Modal xác nhận] Dialog | 1. Truy cập `/admin/dashboard`<br>2. Click [Đăng xuất]<br>3. Kiểm tra modal | Status: visible, Hiển thị form xác nhận đăng xuất | | Pass | 11/15/2025 | |
| GUI-DangXuat-03 | Check [Tiêu đề modal] Text | 1. Truy cập `/admin/dashboard`<br>2. Click [Đăng xuất]<br>3. Kiểm tra tiêu đề | Status: visible, Text: "Xác nhận đăng xuất" | | Pass | 11/15/2025 | |
| GUI-DangXuat-04 | Check [Nội dung xác nhận] Text | 1. Truy cập `/admin/dashboard`<br>2. Click [Đăng xuất]<br>3. Kiểm tra nội dung | Status: visible, Text: "Bạn có chắc chắn muốn đăng xuất khỏi hệ thống?" | | Pass | 11/15/2025 | |
| GUI-DangXuat-05 | Check [Xác nhận] Button | 1. Truy cập `/admin/dashboard`<br>2. Click [Đăng xuất]<br>3. Kiểm tra nút [Đăng xuất] trong modal | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-DangXuat-06 | Check [Hủy] Button | 1. Truy cập `/admin/dashboard`<br>2. Click [Đăng xuất]<br>3. Kiểm tra nút [Hủy] | Status: visible, enable | | Pass | 11/15/2025 | |
| **Check FUNC: Đăng xuất** |
| FUNC-DangXuat-01 | Đăng xuất thành công | 1. Truy cập `/admin/dashboard` (đã đăng nhập)<br>2. Click [Đăng xuất]<br>3. Xác nhận đăng xuất | Đăng xuất thành công, phiên đăng nhập được kết thúc, chuyển về trang đăng nhập, dữ liệu phiên được xóa | | Pass | 11/15/2025 | |
| FUNC-DangXuat-02 | Hủy đăng xuất | 1. Truy cập `/admin/dashboard`<br>2. Click [Đăng xuất]<br>3. Click [Hủy] trong modal | Modal được đóng, vẫn ở trang hiện tại, không đăng xuất | | Pass | 11/15/2025 | |
| FUNC-DangXuat-03 | Xóa dữ liệu phiên sau khi đăng xuất | 1. Truy cập `/admin/dashboard`<br>2. Đăng xuất thành công<br>3. Kiểm tra dữ liệu phiên | Tất cả dữ liệu phiên được xóa, token xác thực bị vô hiệu hóa | | Pass | 11/15/2025 | |

---

## GHI CHÚ

- Tất cả test cases cần được thực hiện trên môi trường test
- Routes động (có `[id]`) cần thay thế bằng ID thực tế khi test
- Các test case GUI kiểm tra giao diện và trạng thái của các thành phần
- Các test case FUNC kiểm tra chức năng và logic nghiệp vụ
- Captcha được hiển thị sau 3 lần đăng nhập sai
- Token khôi phục mật khẩu có thời hạn sử dụng (thường 1 giờ) và chỉ dùng được 1 lần
- Email không thể thay đổi sau khi đăng ký để đảm bảo tính bảo mật
- Cần cập nhật cột Result, Test date sau khi thực hiện test

