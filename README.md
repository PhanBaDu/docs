# Test Case Template - Quản lý tài khoản (User)

## Module Code
**Model Management Store: Quản lý tài khoản User**

## Test Requirement
1. Đăng nhập
2. Đăng ký
3. Khôi phục mật khẩu
4. Đổi mật khẩu
5. Cập nhật thông tin cá nhân
6. Quản lý địa chỉ
7. Xem hạng thành viên
8. Đăng xuất

---

## Test Summary

### Người thực hiện Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 156 |
| **Fail** | 0 |
| **Untested** | 42 |
| **N/A** | 0 |
| **Number of Test cases** | 198 |

---

## Test Cases

### Function: Đăng nhập

#### Check GUI: Đăng nhập

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DN-01** | Kiểm tra tiêu đề trang | 1. Truy cập /user/auth/login<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Đăng nhập" | | Pass | 11/15/2015 | |
| **GUI-DN-02** | Kiểm tra mô tả chức năng | 1. Truy cập /user/auth/login<br>2. Kiểm tra mô tả | Hiển thị mô tả "Đăng nhập vào tài khoản của bạn để tiếp tục mua sắm" | | Pass | 11/15/2015 | |
| **GUI-DN-03** | Kiểm tra trường Email | 1. Truy cập /user/auth/login<br>2. Kiểm tra label và input Email | Hiển thị label "Email", input type email với placeholder "Nhập email của bạn", có thuộc tính required | | Pass | 11/15/2015 | |
| **GUI-DN-04** | Kiểm tra trường Mật khẩu | 1. Truy cập /user/auth/login<br>2. Kiểm tra label và input Mật khẩu | Hiển thị label "Mật khẩu", input type password với placeholder "Nhập mật khẩu", có thuộc tính required | | Pass | 11/15/2015 | |
| **GUI-DN-05** | Kiểm tra checkbox Ghi nhớ | 1. Truy cập /user/auth/login<br>2. Kiểm tra checkbox | Hiển thị checkbox với label "Ghi nhớ đăng nhập" có thể tích chọn, nằm bên trái | | Pass | 11/15/2015 | |
| **GUI-DN-06** | Kiểm tra link Quên mật khẩu | 1. Truy cập /user/auth/login<br>2. Kiểm tra link Quên mật khẩu | Hiển thị link "Quên mật khẩu?" có thể click, nằm bên phải | | Pass | 11/15/2015 | |
| **GUI-DN-07** | Kiểm tra nút Đăng nhập | 1. Truy cập /user/auth/login<br>2. Kiểm tra nút Đăng nhập | Hiển thị nút "Đăng nhập" type submit, chiếm toàn bộ chiều rộng form | | Pass | 11/15/2015 | |
| **GUI-DN-08** | Kiểm tra separator "Hoặc" | 1. Truy cập /user/auth/login<br>2. Kiểm tra separator | Hiển thị separator với text "Hoặc" ở giữa, chữ in hoa | | Pass | 11/15/2015 | |
| **GUI-DN-09** | Kiểm tra nút Đăng nhập với Google | 1. Truy cập /user/auth/login<br>2. Kiểm tra nút Google | Hiển thị nút "Đăng nhập với Google" variant outline, chiếm toàn bộ chiều rộng | | Pass | 11/15/2015 | |
| **GUI-DN-10** | Kiểm tra nút Đăng nhập với Facebook | 1. Truy cập /user/auth/login<br>2. Kiểm tra nút Facebook | Hiển thị nút "Đăng nhập với Facebook" variant outline, chiếm toàn bộ chiều rộng | | Pass | 11/15/2015 | |
| **GUI-DN-11** | Kiểm tra link Đăng ký | 1. Truy cập /user/auth/login<br>2. Kiểm tra link đăng ký | Hiển thị text "Chưa có tài khoản? " với link "Đăng ký ngay" có thể click | | Pass | 11/15/2015 | |
| **GUI-DN-12** | Kiểm tra layout trang | 1. Truy cập /user/auth/login<br>2. Kiểm tra layout tổng thể | Trang có background gradient, card container nằm giữa màn hình, form đăng nhập bên trong card | | Pass | 11/15/2015 | |
| **GUI-DN-13** | Kiểm tra card container | 1. Truy cập /user/auth/login<br>2. Kiểm tra card | Hiển thị card container chứa toàn bộ form đăng nhập, có giới hạn chiều rộng tối đa | | Pass | 11/15/2015 | |

---

### Check FUNC: Đăng nhập

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DN-01** | Mở trang đăng nhập | 1. Truy cập /user/auth/login | Hiển thị form đăng nhập với đầy đủ các thành phần: tiêu đề "Đăng nhập", mô tả "Đăng nhập vào tài khoản của bạn để tiếp tục mua sắm", 2 trường nhập (Email, Mật khẩu), checkbox ghi nhớ, link quên mật khẩu, nút đăng nhập, separator "Hoặc", nút đăng nhập Google/Facebook, link đăng ký | | Pass | 11/15/2015 | |
| **FUNC-DN-02** | Đăng nhập thành công với thông tin hợp lệ | 1. Truy cập /user/auth/login<br>2. Nhập email hợp lệ (VD: user@email.com)<br>3. Nhập mật khẩu đúng<br>4. Nhấn nút Đăng nhập | Hệ thống xác thực thông tin, chuyển đến trang chủ user (/user), lưu phiên đăng nhập và lưu token, hiển thị thông báo thành công | | Untested | 11/15/2015 | |
| **FUNC-DN-03** | Đăng nhập với email không tồn tại | 1. Truy cập /user/auth/login<br>2. Nhập email không tồn tại (VD: notexist@test.com)<br>3. Nhập mật khẩu bất kỳ<br>4. Nhấn Đăng nhập | Hiển thị thông báo lỗi "Email hoặc mật khẩu không đúng", không chuyển trang, vẫn ở trang đăng nhập | | Untested | 11/15/2015 | |
| **FUNC-DN-04** | Đăng nhập với mật khẩu sai | 1. Truy cập /user/auth/login<br>2. Nhập email hợp lệ<br>3. Nhập mật khẩu sai<br>4. Nhấn Đăng nhập | Hiển thị thông báo lỗi "Email hoặc mật khẩu không đúng", không chuyển trang, vẫn ở trang đăng nhập | | Untested | 11/15/2015 | |
| **FUNC-DN-05** | Đăng nhập thiếu email | 1. Truy cập /user/auth/login<br>2. Để trống email<br>3. Nhập mật khẩu<br>4. Nhấn Đăng nhập | Trình duyệt hiển thị cảnh báo "Please fill out this field" hoặc validation message, form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-DN-06** | Đăng nhập thiếu mật khẩu | 1. Truy cập /user/auth/login<br>2. Nhập email<br>3. Để trống mật khẩu<br>4. Nhấn Đăng nhập | Trình duyệt hiển thị cảnh báo "Please fill out this field" hoặc validation message, form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-DN-07** | Đăng nhập với email sai định dạng | 1. Truy cập /user/auth/login<br>2. Nhập email không đúng định dạng (VD: "invalid-email")<br>3. Nhập mật khẩu<br>4. Nhấn Đăng nhập | Trình duyệt hiển thị cảnh báo "Please include an '@' in the email address" hoặc validation message, form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-DN-08** | Chức năng ghi nhớ - Có tích chọn | 1. Truy cập /user/auth/login<br>2. Tích checkbox "Ghi nhớ đăng nhập"<br>3. Nhập thông tin hợp lệ<br>4. Đăng nhập thành công | Đăng nhập thành công, trình duyệt lưu cookie/session với thời hạn dài hơn, khi đóng trình duyệt và mở lại vẫn còn đăng nhập | | Untested | 11/15/2015 | |
| **FUNC-DN-09** | Chức năng ghi nhớ - Không tích chọn | 1. Truy cập /user/auth/login<br>2. Không tích checkbox<br>3. Nhập thông tin hợp lệ<br>4. Đăng nhập thành công | Đăng nhập thành công, trình duyệt lưu cookie/session với thời hạn ngắn hơn, khi đóng trình duyệt sẽ đăng xuất | | Untested | 11/15/2015 | |
| **FUNC-DN-10** | Nhấn link Quên mật khẩu | 1. Truy cập /user/auth/login<br>2. Nhấn link "Quên mật khẩu?" | Chuyển đến trang /user/auth/forgot-password | | Pass | 11/15/2015 | |
| **FUNC-DN-11** | Nhấn link Đăng ký | 1. Truy cập /user/auth/login<br>2. Nhấn link "Đăng ký ngay" | Chuyển đến trang /user/auth/register | | Pass | 11/15/2015 | |
| **FUNC-DN-12** | Submit form bằng phím Enter | 1. Truy cập /user/auth/login<br>2. Nhập thông tin hợp lệ<br>3. Nhấn Enter trong trường mật khẩu | Form được gửi, xử lý đăng nhập như khi nhấn nút Đăng nhập | | Untested | 11/15/2015 | |
| **FUNC-DN-13** | Đăng nhập với tài khoản chưa kích hoạt | 1. Truy cập /user/auth/login<br>2. Nhập email tài khoản chưa kích hoạt<br>3. Nhập mật khẩu đúng<br>4. Nhấn Đăng nhập | Hiển thị thông báo lỗi "Tài khoản chưa được kích hoạt. Vui lòng kiểm tra email để kích hoạt tài khoản", không chuyển trang | | Untested | 11/15/2015 | |
| **FUNC-DN-14** | Đăng nhập với tài khoản bị khóa | 1. Truy cập /user/auth/login<br>2. Nhập email tài khoản bị khóa<br>3. Nhập mật khẩu đúng<br>4. Nhấn Đăng nhập | Hiển thị thông báo lỗi "Tài khoản đã bị khóa. Vui lòng liên hệ quản trị viên", không chuyển trang | | Untested | 11/15/2015 | |
| **FUNC-DN-15** | Đăng nhập sai nhiều lần - Hiển thị Captcha | 1. Truy cập /user/auth/login<br>2. Nhập sai thông tin đăng nhập 3 lần liên tiếp<br>3. Lần thứ 4, nhập thông tin | Sau 3 lần đăng nhập sai, hiển thị captcha, yêu cầu nhập captcha trước khi tiếp tục đăng nhập | | Untested | 11/15/2015 | |
| **FUNC-DN-16** | Đăng nhập với captcha đúng | 1. Truy cập /user/auth/login<br>2. Đăng nhập sai 3 lần để hiển thị captcha<br>3. Nhập captcha đúng<br>4. Nhập thông tin đăng nhập đúng<br>5. Nhấn Đăng nhập | Xác thực captcha thành công, xử lý đăng nhập bình thường, chuyển đến trang chủ | | Untested | 11/15/2015 | |
| **FUNC-DN-17** | Đăng nhập với captcha sai | 1. Truy cập /user/auth/login<br>2. Đăng nhập sai 3 lần để hiển thị captcha<br>3. Nhập captcha sai<br>4. Nhập thông tin đăng nhập đúng<br>5. Nhấn Đăng nhập | Hiển thị thông báo lỗi "Captcha không đúng", không xử lý đăng nhập | | Untested | 11/15/2015 | |
| **FUNC-DN-18** | Tạm khóa tài khoản sau nhiều lần đăng nhập sai | 1. Truy cập /user/auth/login<br>2. Đăng nhập sai quá số lần cho phép (VD: 5 lần)<br>3. Thử đăng nhập lại | Tài khoản bị tạm khóa trong một khoảng thời gian (VD: 15 phút), hiển thị thông báo "Tài khoản đã bị tạm khóa do đăng nhập sai nhiều lần. Vui lòng thử lại sau X phút" | | Untested | 11/15/2015 | |
| **FUNC-DN-19** | Xử lý khi mất kết nối mạng | 1. Truy cập /user/auth/login<br>2. Tắt kết nối mạng<br>3. Nhập thông tin hợp lệ<br>4. Nhấn Đăng nhập | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", không chuyển trang | | Untested | 11/15/2015 | |
| **FUNC-DN-20** | Xử lý khi server lỗi | 1. Truy cập /user/auth/login<br>2. Nhập thông tin hợp lệ<br>3. Server trả về lỗi 500<br>4. Nhấn Đăng nhập | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau", không chuyển trang | | Untested | 11/15/2015 | |
| **FUNC-DN-21** | Kiểm tra redirect sau đăng nhập | 1. Truy cập /user/auth/login?redirect=/user/products<br>2. Nhập thông tin hợp lệ<br>3. Đăng nhập thành công | Sau khi đăng nhập thành công, chuyển đến trang /user/products thay vì trang chủ mặc định | | Untested | 11/15/2015 | |
| **FUNC-DN-22** | Kiểm tra lưu token sau đăng nhập | 1. Truy cập /user/auth/login<br>2. Nhập thông tin hợp lệ<br>3. Đăng nhập thành công<br>4. Kiểm tra localStorage/sessionStorage | Token được lưu vào localStorage hoặc sessionStorage, có thể sử dụng cho các request tiếp theo | | Untested | 11/15/2015 | |
| **FUNC-DN-23** | Kiểm tra tạo phiên đăng nhập | 1. Truy cập /user/auth/login<br>2. Nhập thông tin hợp lệ<br>3. Đăng nhập thành công<br>4. Kiểm tra session | Phiên đăng nhập được tạo và lưu trữ trên server, có thể theo dõi trong lịch sử đăng nhập | | Untested | 11/15/2015 | |
| **FUNC-DN-24** | Đăng nhập với Google | 1. Truy cập /user/auth/login<br>2. Nhấn nút "Đăng nhập với Google" | Mở popup hoặc chuyển hướng đến trang xác thực Google, sau khi xác thực thành công chuyển về trang chủ | | Untested | 11/15/2015 | |
| **FUNC-DN-25** | Đăng nhập với Facebook | 1. Truy cập /user/auth/login<br>2. Nhấn nút "Đăng nhập với Facebook" | Mở popup hoặc chuyển hướng đến trang xác thực Facebook, sau khi xác thực thành công chuyển về trang chủ | | Untested | 11/15/2015 | |

---

### Function: Đăng ký

#### Check GUI: Đăng ký

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DK-01** | Kiểm tra tiêu đề trang | 1. Truy cập /user/auth/register<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Đăng ký tài khoản" | | Pass | 11/15/2015 | |
| **GUI-DK-02** | Kiểm tra mô tả chức năng | 1. Truy cập /user/auth/register<br>2. Kiểm tra mô tả | Hiển thị mô tả "Tạo tài khoản mới để bắt đầu mua sắm tại Model Shop" | | Pass | 11/15/2015 | |
| **GUI-DK-03** | Kiểm tra Avatar upload | 1. Truy cập /user/auth/register<br>2. Kiểm tra Avatar | Hiển thị Avatar với icon User2 làm fallback, có nút Camera để upload ảnh | | Pass | 11/15/2015 | |
| **GUI-DK-04** | Kiểm tra trường Họ và tên | 1. Truy cập /user/auth/register<br>2. Kiểm tra trường Họ và tên | Hiển thị label "Họ và tên *" với icon User, input type text với placeholder "Nhập họ và tên", có thuộc tính required | | Pass | 11/15/2015 | |
| **GUI-DK-05** | Kiểm tra trường Email | 1. Truy cập /user/auth/register<br>2. Kiểm tra trường Email | Hiển thị label "Email *" với icon Mail, input type email với placeholder "Nhập email", có thuộc tính required | | Pass | 11/15/2015 | |
| **GUI-DK-06** | Kiểm tra trường Số điện thoại | 1. Truy cập /user/auth/register<br>2. Kiểm tra trường Số điện thoại | Hiển thị label "Số điện thoại *" với icon Phone, input type tel với placeholder "Nhập số điện thoại", có thuộc tính required | | Pass | 11/15/2015 | |
| **GUI-DK-07** | Kiểm tra trường Giới tính | 1. Truy cập /user/auth/register<br>2. Kiểm tra trường Giới tính | Hiển thị label "Giới tính" với icon User2, Select với placeholder "Chọn giới tính", có các option: Nam, Nữ, Khác | | Pass | 11/15/2015 | |
| **GUI-DK-08** | Kiểm tra trường Ngày sinh | 1. Truy cập /user/auth/register<br>2. Kiểm tra trường Ngày sinh | Hiển thị label "Ngày sinh" với icon Calendar, input type date | | Pass | 11/15/2015 | |
| **GUI-DK-09** | Kiểm tra trường Địa chỉ | 1. Truy cập /user/auth/register<br>2. Kiểm tra trường Địa chỉ | Hiển thị label "Địa chỉ" với icon MapPin, input type text với placeholder "Nhập địa chỉ" | | Pass | 11/15/2015 | |
| **GUI-DK-10** | Kiểm tra trường Mật khẩu | 1. Truy cập /user/auth/register<br>2. Kiểm tra trường Mật khẩu | Hiển thị label "Mật khẩu *", input type password với placeholder "Nhập mật khẩu", có nút icon Eye/EyeOff để hiển thị/ẩn mật khẩu, có thuộc tính required | | Pass | 11/15/2015 | |
| **GUI-DK-11** | Kiểm tra trường Xác nhận mật khẩu | 1. Truy cập /user/auth/register<br>2. Kiểm tra trường Xác nhận mật khẩu | Hiển thị label "Xác nhận mật khẩu *", input type password với placeholder "Nhập lại mật khẩu", có nút icon Eye/EyeOff để hiển thị/ẩn mật khẩu, có thuộc tính required | | Pass | 11/15/2015 | |
| **GUI-DK-12** | Kiểm tra checkbox Điều khoản | 1. Truy cập /user/auth/register<br>2. Kiểm tra checkbox | Hiển thị checkbox với label "Tôi đồng ý với Điều khoản sử dụng và Chính sách bảo mật", có link đến trang điều khoản | | Pass | 11/15/2015 | |
| **GUI-DK-13** | Kiểm tra thông tin bảo mật | 1. Truy cập /user/auth/register<br>2. Kiểm tra thông tin bảo mật | Hiển thị card thông tin bảo mật với icon ℹ, nội dung: "Mật khẩu phải có ít nhất 6 ký tự", "Thông tin cá nhân được bảo mật tuyệt đối", "Ảnh đại diện sẽ được hiển thị công khai" | | Pass | 11/15/2015 | |
| **GUI-DK-14** | Kiểm tra nút Đăng ký | 1. Truy cập /user/auth/register<br>2. Kiểm tra nút Đăng ký | Hiển thị nút "Đăng ký tài khoản" type submit, chiếm toàn bộ chiều rộng, có thể disabled khi đang loading | | Pass | 11/15/2015 | |
| **GUI-DK-15** | Kiểm tra separator "Hoặc" | 1. Truy cập /user/auth/register<br>2. Kiểm tra separator | Hiển thị separator với text "Hoặc" ở giữa, chữ in hoa | | Pass | 11/15/2015 | |
| **GUI-DK-16** | Kiểm tra nút Đăng ký với Google | 1. Truy cập /user/auth/register<br>2. Kiểm tra nút Google | Hiển thị nút "Đăng ký với Google" variant outline, chiếm toàn bộ chiều rộng | | Pass | 11/15/2015 | |
| **GUI-DK-17** | Kiểm tra nút Đăng ký với Facebook | 1. Truy cập /user/auth/register<br>2. Kiểm tra nút Facebook | Hiển thị nút "Đăng ký với Facebook" variant outline, chiếm toàn bộ chiều rộng | | Pass | 11/15/2015 | |
| **GUI-DK-18** | Kiểm tra link Đăng nhập | 1. Truy cập /user/auth/register<br>2. Kiểm tra link đăng nhập | Hiển thị text "Đã có tài khoản? " với link "Đăng nhập ngay" có thể click | | Pass | 11/15/2015 | |
| **GUI-DK-19** | Kiểm tra layout trang | 1. Truy cập /user/auth/register<br>2. Kiểm tra layout tổng thể | Trang có background gradient, card container nằm giữa màn hình, form đăng ký bên trong card, có scroll nếu nội dung dài | | Pass | 11/15/2015 | |

---

### Check FUNC: Đăng ký

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DK-01** | Mở trang đăng ký | 1. Truy cập /user/auth/register | Hiển thị form đăng ký với đầy đủ các thành phần: tiêu đề, mô tả, Avatar upload, các trường nhập (Họ tên, Email, SĐT, Giới tính, Ngày sinh, Địa chỉ, Mật khẩu, Xác nhận mật khẩu), checkbox điều khoản, thông tin bảo mật, nút đăng ký, separator, nút đăng ký Google/Facebook, link đăng nhập | | Pass | 11/15/2015 | |
| **FUNC-DK-02** | Đăng ký thành công với thông tin hợp lệ | 1. Truy cập /user/auth/register<br>2. Điền đầy đủ thông tin hợp lệ<br>3. Tích checkbox điều khoản<br>4. Nhấn Đăng ký | Hiển thị thông báo "Đăng ký tài khoản thành công!", chuyển đến trang /user/auth/login, email xác nhận được gửi (nếu có) | | Untested | 11/15/2015 | |
| **FUNC-DK-03** | Đăng ký thiếu Họ tên | 1. Truy cập /user/auth/register<br>2. Để trống Họ tên<br>3. Điền các trường khác<br>4. Nhấn Đăng ký | Hiển thị thông báo lỗi "Họ tên không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-DK-04** | Đăng ký thiếu Email | 1. Truy cập /user/auth/register<br>2. Để trống Email<br>3. Điền các trường khác<br>4. Nhấn Đăng ký | Hiển thị thông báo lỗi "Email không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-DK-05** | Đăng ký với Email không hợp lệ | 1. Truy cập /user/auth/register<br>2. Nhập email không có @<br>3. Điền các trường khác<br>4. Nhấn Đăng ký | Hiển thị thông báo lỗi "Email không hợp lệ", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-DK-06** | Đăng ký với Email đã tồn tại | 1. Truy cập /user/auth/register<br>2. Nhập email đã tồn tại trong hệ thống<br>3. Điền các trường khác<br>4. Nhấn Đăng ký | Hiển thị thông báo lỗi "Email đã tồn tại trong hệ thống", form không được gửi | | Untested | 11/15/2015 | |
| **FUNC-DK-07** | Đăng ký thiếu Số điện thoại | 1. Truy cập /user/auth/register<br>2. Để trống Số điện thoại<br>3. Điền các trường khác<br>4. Nhấn Đăng ký | Hiển thị thông báo lỗi "Số điện thoại không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-DK-08** | Đăng ký với Số điện thoại không hợp lệ | 1. Truy cập /user/auth/register<br>2. Nhập số điện thoại không đúng định dạng (VD: 123)<br>3. Điền các trường khác<br>4. Nhấn Đăng ký | Hiển thị thông báo lỗi "Số điện thoại không hợp lệ", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-DK-09** | Đăng ký thiếu Mật khẩu | 1. Truy cập /user/auth/register<br>2. Để trống Mật khẩu<br>3. Điền các trường khác<br>4. Nhấn Đăng ký | Hiển thị thông báo lỗi "Mật khẩu không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-DK-10** | Đăng ký với Mật khẩu quá ngắn | 1. Truy cập /user/auth/register<br>2. Nhập mật khẩu < 6 ký tự<br>3. Điền các trường khác<br>4. Nhấn Đăng ký | Hiển thị thông báo lỗi "Mật khẩu phải có ít nhất 6 ký tự", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-DK-11** | Đăng ký với Mật khẩu xác nhận không khớp | 1. Truy cập /user/auth/register<br>2. Nhập mật khẩu<br>3. Nhập xác nhận mật khẩu khác<br>4. Nhấn Đăng ký | Hiển thị thông báo lỗi "Mật khẩu xác nhận không khớp", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-DK-12** | Đăng ký không tích checkbox điều khoản | 1. Truy cập /user/auth/register<br>2. Điền đầy đủ thông tin<br>3. Không tích checkbox điều khoản<br>4. Nhấn Đăng ký | Hiển thị thông báo lỗi "Vui lòng đồng ý với điều khoản sử dụng", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-DK-13** | Upload Avatar thành công | 1. Truy cập /user/auth/register<br>2. Click nút Camera<br>3. Chọn file ảnh hợp lệ (< 5MB)<br>4. Kiểm tra preview | Avatar được hiển thị preview, file được lưu vào form data | | Pass | 11/15/2015 | |
| **FUNC-DK-14** | Upload Avatar quá lớn | 1. Truy cập /user/auth/register<br>2. Click nút Camera<br>3. Chọn file ảnh > 5MB | Hiển thị thông báo lỗi "Kích thước ảnh không được vượt quá 5MB" | | Pass | 11/15/2015 | |
| **FUNC-DK-15** | Upload Avatar không phải file ảnh | 1. Truy cập /user/auth/register<br>2. Click nút Camera<br>3. Chọn file không phải ảnh | Hiển thị thông báo lỗi "Vui lòng chọn file ảnh hợp lệ" | | Pass | 11/15/2015 | |
| **FUNC-DK-16** | Hiển thị/ẩn mật khẩu | 1. Truy cập /user/auth/register<br>2. Nhập mật khẩu<br>3. Click icon Eye | Input chuyển từ type password sang type text, hiển thị mật khẩu, icon chuyển thành EyeOff | | Pass | 11/15/2015 | |
| **FUNC-DK-17** | Hiển thị/ẩn xác nhận mật khẩu | 1. Truy cập /user/auth/register<br>2. Nhập xác nhận mật khẩu<br>3. Click icon Eye | Input chuyển từ type password sang type text, hiển thị mật khẩu, icon chuyển thành EyeOff | | Pass | 11/15/2015 | |
| **FUNC-DK-18** | Kiểm tra email trùng lặp real-time | 1. Truy cập /user/auth/register<br>2. Nhập email đã tồn tại<br>3. Rời khỏi trường email | Hiển thị cảnh báo ngay lập tức "Email đã tồn tại trong hệ thống" mà không cần submit form | | Untested | 11/15/2015 | |
| **FUNC-DK-19** | Nhấn link Đăng nhập | 1. Truy cập /user/auth/register<br>2. Nhấn link "Đăng nhập ngay" | Chuyển đến trang /user/auth/login | | Pass | 11/15/2015 | |
| **FUNC-DK-20** | Nhấn link Điều khoản sử dụng | 1. Truy cập /user/auth/register<br>2. Nhấn link "Điều khoản sử dụng" | Mở trang /terms trong tab mới hoặc chuyển đến trang điều khoản | | Pass | 11/15/2015 | |
| **FUNC-DK-21** | Nhấn link Chính sách bảo mật | 1. Truy cập /user/auth/register<br>2. Nhấn link "Chính sách bảo mật" | Mở trang /privacy trong tab mới hoặc chuyển đến trang chính sách | | Pass | 11/15/2015 | |
| **FUNC-DK-22** | Đăng ký với Google | 1. Truy cập /user/auth/register<br>2. Nhấn nút "Đăng ký với Google" | Mở popup hoặc chuyển hướng đến trang xác thực Google, sau khi xác thực thành công tạo tài khoản và chuyển về trang chủ | | Untested | 11/15/2015 | |
| **FUNC-DK-23** | Đăng ký với Facebook | 1. Truy cập /user/auth/register<br>2. Nhấn nút "Đăng ký với Facebook" | Mở popup hoặc chuyển hướng đến trang xác thực Facebook, sau khi xác thực thành công tạo tài khoản và chuyển về trang chủ | | Untested | 11/15/2015 | |
| **FUNC-DK-24** | Xử lý khi mất kết nối mạng | 1. Truy cập /user/auth/register<br>2. Điền đầy đủ thông tin<br>3. Tắt kết nối mạng<br>4. Nhấn Đăng ký | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", form không được gửi | | Untested | 11/15/2015 | |
| **FUNC-DK-25** | Xử lý khi server lỗi | 1. Truy cập /user/auth/register<br>2. Điền đầy đủ thông tin<br>3. Server trả về lỗi 500<br>4. Nhấn Đăng ký | Hiển thị thông báo lỗi "Có lỗi xảy ra, vui lòng thử lại", form không được gửi | | Untested | 11/15/2015 | |

---

### Function: Khôi phục mật khẩu

#### Check GUI: Khôi phục mật khẩu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-KPMK-01** | Kiểm tra icon Mail header | 1. Truy cập /user/auth/forgot-password<br>2. Kiểm tra icon Mail | Hiển thị icon Mail trong vòng tròn ở header | | Pass | 11/15/2015 | |
| **GUI-KPMK-02** | Kiểm tra tiêu đề trang | 1. Truy cập /user/auth/forgot-password<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Quên mật khẩu" | | Pass | 11/15/2015 | |
| **GUI-KPMK-03** | Kiểm tra mô tả chức năng | 1. Truy cập /user/auth/forgot-password<br>2. Kiểm tra mô tả | Hiển thị mô tả "Nhập email của bạn để nhận link khôi phục mật khẩu" | | Pass | 11/15/2015 | |
| **GUI-KPMK-04** | Kiểm tra trường nhập Email | 1. Truy cập /user/auth/forgot-password<br>2. Kiểm tra trường nhập | Hiển thị label "Email", input type email với placeholder "Nhập email của bạn" | | Pass | 11/15/2015 | |
| **GUI-KPMK-05** | Kiểm tra nút Gửi link khôi phục | 1. Truy cập /user/auth/forgot-password<br>2. Kiểm tra nút | Hiển thị nút "Gửi link khôi phục" type submit, chiếm toàn bộ chiều rộng, có thể disabled khi đang loading | | Pass | 11/15/2015 | |
| **GUI-KPMK-06** | Kiểm tra link Quay lại đăng nhập | 1. Truy cập /user/auth/forgot-password<br>2. Kiểm tra link | Hiển thị link "Quay lại đăng nhập" với icon ArrowLeft, có thể click | | Pass | 11/15/2015 | |
| **GUI-KPMK-07** | Kiểm tra link Đăng ký | 1. Truy cập /user/auth/forgot-password<br>2. Kiểm tra link đăng ký | Hiển thị text "Chưa có tài khoản? " với link "Đăng ký ngay" có thể click | | Pass | 11/15/2015 | |
| **GUI-KPMK-08** | Kiểm tra màn hình Email đã gửi | 1. Truy cập /user/auth/forgot-password<br>2. Gửi email thành công<br>3. Kiểm tra màn hình | Hiển thị icon CheckCircle trong vòng tròn xanh, tiêu đề "Email đã được gửi", mô tả "Chúng tôi đã gửi link khôi phục mật khẩu đến email của bạn", nút "Gửi lại email", nút "Quay lại đăng nhập" | | Pass | 11/15/2015 | |

---

### Check FUNC: Khôi phục mật khẩu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-KPMK-01** | Mở trang khôi phục mật khẩu | 1. Truy cập /user/auth/forgot-password | Hiển thị trang với icon Mail, tiêu đề "Quên mật khẩu", mô tả, trường nhập Email, nút "Gửi link khôi phục", link quay lại đăng nhập, link đăng ký | | Pass | 11/15/2015 | |
| **FUNC-KPMK-02** | Gửi email khôi phục thành công | 1. Truy cập /user/auth/forgot-password<br>2. Nhập email hợp lệ<br>3. Nhấn "Gửi link khôi phục" | Hiển thị thông báo "Email khôi phục mật khẩu đã được gửi!", chuyển sang màn hình "Email đã được gửi" | | Untested | 11/15/2015 | |
| **FUNC-KPMK-03** | Gửi email - Email không tồn tại | 1. Truy cập /user/auth/forgot-password<br>2. Nhập email không tồn tại<br>3. Nhấn "Gửi link khôi phục" | Hiển thị thông báo lỗi "Email không tồn tại trong hệ thống" | | Untested | 11/15/2015 | |
| **FUNC-KPMK-04** | Gửi email - Thiếu email | 1. Truy cập /user/auth/forgot-password<br>2. Để trống email<br>3. Nhấn "Gửi link khôi phục" | Hiển thị thông báo lỗi "Vui lòng nhập email", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-KPMK-05** | Gửi email - Email không hợp lệ | 1. Truy cập /user/auth/forgot-password<br>2. Nhập email không đúng định dạng<br>3. Nhấn "Gửi link khôi phục" | Trình duyệt hiển thị cảnh báo validation hoặc thông báo lỗi "Email không hợp lệ" | | Pass | 11/15/2015 | |
| **FUNC-KPMK-06** | Nhấn link Quay lại đăng nhập | 1. Truy cập /user/auth/forgot-password<br>2. Nhấn link "Quay lại đăng nhập" | Chuyển đến trang /user/auth/login | | Pass | 11/15/2015 | |
| **FUNC-KPMK-07** | Nhấn link Đăng ký | 1. Truy cập /user/auth/forgot-password<br>2. Nhấn link "Đăng ký ngay" | Chuyển đến trang /user/auth/register | | Pass | 11/15/2015 | |
| **FUNC-KPMK-08** | Gửi lại email | 1. Truy cập /user/auth/forgot-password<br>2. Gửi email thành công<br>3. Nhấn "Gửi lại email" | Quay lại màn hình nhập email, có thể gửi lại email khôi phục | | Pass | 11/15/2015 | |
| **FUNC-KPMK-09** | Xử lý khi mất kết nối mạng | 1. Truy cập /user/auth/forgot-password<br>2. Nhập email hợp lệ<br>3. Tắt kết nối mạng<br>4. Nhấn "Gửi link khôi phục" | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại" | | Untested | 11/15/2015 | |
| **FUNC-KPMK-10** | Xử lý khi server lỗi | 1. Truy cập /user/auth/forgot-password<br>2. Nhập email hợp lệ<br>3. Server trả về lỗi 500<br>4. Nhấn "Gửi link khôi phục" | Hiển thị thông báo lỗi "Có lỗi xảy ra, vui lòng thử lại" | | Untested | 11/15/2015 | |

---

### Function: Đổi mật khẩu

#### Check GUI: Đổi mật khẩu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DMK-01** | Kiểm tra nút Đổi mật khẩu | 1. Truy cập /user/account<br>2. Kiểm tra nút Đổi mật khẩu | Hiển thị nút "Đổi mật khẩu" với icon Key trong card "Thông tin tài khoản" | | Pass | 11/15/2015 | |
| **GUI-DMK-02** | Kiểm tra modal Đổi mật khẩu | 1. Truy cập /user/account<br>2. Nhấn nút Đổi mật khẩu<br>3. Kiểm tra modal | Hiển thị Dialog với tiêu đề "Đổi mật khẩu", mô tả "Nhập mật khẩu hiện tại và mật khẩu mới để thay đổi" | | Pass | 11/15/2015 | |
| **GUI-DMK-03** | Kiểm tra trường Mật khẩu hiện tại | 1. Truy cập /user/account<br>2. Mở modal Đổi mật khẩu<br>3. Kiểm tra trường Mật khẩu hiện tại | Hiển thị label "Mật khẩu hiện tại", input type password, có nút icon Eye/EyeOff để hiển thị/ẩn mật khẩu | | Pass | 11/15/2015 | |
| **GUI-DMK-04** | Kiểm tra trường Mật khẩu mới | 1. Truy cập /user/account<br>2. Mở modal Đổi mật khẩu<br>3. Kiểm tra trường Mật khẩu mới | Hiển thị label "Mật khẩu mới", input type password, có nút icon Eye/EyeOff để hiển thị/ẩn mật khẩu | | Pass | 11/15/2015 | |
| **GUI-DMK-05** | Kiểm tra trường Xác nhận mật khẩu mới | 1. Truy cập /user/account<br>2. Mở modal Đổi mật khẩu<br>3. Kiểm tra trường Xác nhận mật khẩu | Hiển thị label "Xác nhận mật khẩu mới", input type password, có nút icon Eye/EyeOff để hiển thị/ẩn mật khẩu | | Pass | 11/15/2015 | |
| **GUI-DMK-06** | Kiểm tra nút Hủy | 1. Truy cập /user/account<br>2. Mở modal Đổi mật khẩu<br>3. Kiểm tra nút Hủy | Hiển thị nút "Hủy" variant outline | | Pass | 11/15/2015 | |
| **GUI-DMK-07** | Kiểm tra nút Đổi mật khẩu trong modal | 1. Truy cập /user/account<br>2. Mở modal Đổi mật khẩu<br>3. Kiểm tra nút Đổi mật khẩu | Hiển thị nút "Đổi mật khẩu" | | Pass | 11/15/2015 | |

---

### Check FUNC: Đổi mật khẩu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DMK-01** | Mở modal Đổi mật khẩu | 1. Truy cập /user/account<br>2. Nhấn nút "Đổi mật khẩu" | Modal Dialog mở ra, hiển thị 3 trường nhập (Mật khẩu hiện tại, Mật khẩu mới, Xác nhận mật khẩu mới), 2 nút (Hủy, Đổi mật khẩu) | | Pass | 11/15/2015 | |
| **FUNC-DMK-02** | Đổi mật khẩu thành công | 1. Truy cập /user/account<br>2. Mở modal Đổi mật khẩu<br>3. Nhập mật khẩu hiện tại đúng<br>4. Nhập mật khẩu mới hợp lệ (≥6 ký tự)<br>5. Nhập lại mật khẩu mới khớp<br>6. Nhấn Đổi mật khẩu | Hiển thị thông báo "Đổi mật khẩu thành công", modal đóng, form được reset | | Untested | 11/15/2015 | |
| **FUNC-DMK-03** | Đổi mật khẩu - Mật khẩu hiện tại sai | 1. Truy cập /user/account<br>2. Mở modal Đổi mật khẩu<br>3. Nhập mật khẩu hiện tại sai<br>4. Nhập mật khẩu mới<br>5. Nhấn Đổi mật khẩu | Hiển thị thông báo lỗi "Mật khẩu hiện tại không đúng", không đổi mật khẩu | | Untested | 11/15/2015 | |
| **FUNC-DMK-04** | Đổi mật khẩu - Thiếu mật khẩu hiện tại | 1. Truy cập /user/account<br>2. Mở modal Đổi mật khẩu<br>3. Để trống mật khẩu hiện tại<br>4. Nhập mật khẩu mới<br>5. Nhấn Đổi mật khẩu | Hiển thị thông báo lỗi "Vui lòng nhập mật khẩu hiện tại" | | Pass | 11/15/2015 | |
| **FUNC-DMK-05** | Đổi mật khẩu - Thiếu mật khẩu mới | 1. Truy cập /user/account<br>2. Mở modal Đổi mật khẩu<br>3. Nhập mật khẩu hiện tại<br>4. Để trống mật khẩu mới<br>5. Nhấn Đổi mật khẩu | Hiển thị thông báo lỗi "Vui lòng nhập mật khẩu mới" | | Pass | 11/15/2015 | |
| **FUNC-DMK-06** | Đổi mật khẩu - Mật khẩu mới quá ngắn | 1. Truy cập /user/account<br>2. Mở modal Đổi mật khẩu<br>3. Nhập mật khẩu hiện tại<br>4. Nhập mật khẩu mới < 6 ký tự<br>5. Nhấn Đổi mật khẩu | Hiển thị thông báo lỗi "Mật khẩu mới phải có ít nhất 6 ký tự" | | Pass | 11/15/2015 | |
| **FUNC-DMK-07** | Đổi mật khẩu - Mật khẩu xác nhận không khớp | 1. Truy cập /user/account<br>2. Mở modal Đổi mật khẩu<br>3. Nhập mật khẩu hiện tại<br>4. Nhập mật khẩu mới<br>5. Nhập xác nhận mật khẩu khác<br>6. Nhấn Đổi mật khẩu | Hiển thị thông báo lỗi "Mật khẩu xác nhận không khớp" | | Pass | 11/15/2015 | |
| **FUNC-DMK-08** | Hiển thị/ẩn mật khẩu hiện tại | 1. Truy cập /user/account<br>2. Mở modal Đổi mật khẩu<br>3. Nhập mật khẩu hiện tại<br>4. Nhấn icon Eye | Input chuyển từ type password sang type text, hiển thị mật khẩu, icon chuyển thành EyeOff | | Pass | 11/15/2015 | |
| **FUNC-DMK-09** | Hiển thị/ẩn mật khẩu mới | 1. Truy cập /user/account<br>2. Mở modal Đổi mật khẩu<br>3. Nhập mật khẩu mới<br>4. Nhấn icon Eye | Input chuyển từ type password sang type text, hiển thị mật khẩu, icon chuyển thành EyeOff | | Pass | 11/15/2015 | |
| **FUNC-DMK-10** | Hiển thị/ẩn xác nhận mật khẩu | 1. Truy cập /user/account<br>2. Mở modal Đổi mật khẩu<br>3. Nhập xác nhận mật khẩu<br>4. Nhấn icon Eye | Input chuyển từ type password sang type text, hiển thị mật khẩu, icon chuyển thành EyeOff | | Pass | 11/15/2015 | |
| **FUNC-DMK-11** | Đóng modal bằng nút Hủy | 1. Truy cập /user/account<br>2. Mở modal Đổi mật khẩu<br>3. Nhấn nút Hủy | Modal đóng, form được reset về trạng thái ban đầu | | Pass | 11/15/2015 | |
| **FUNC-DMK-12** | Đóng modal bằng click bên ngoài | 1. Truy cập /user/account<br>2. Mở modal Đổi mật khẩu<br>3. Click bên ngoài modal | Modal đóng | | Pass | 11/15/2015 | |

---

### Function: Cập nhật thông tin cá nhân

#### Check GUI: Cập nhật thông tin cá nhân

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-QLTT-01** | Kiểm tra tiêu đề trang | 1. Truy cập /user/account<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Tài khoản của tôi" | | Pass | 11/15/2015 | |
| **GUI-QLTT-02** | Kiểm tra mô tả trang | 1. Truy cập /user/account<br>2. Kiểm tra mô tả | Hiển thị mô tả "Quản lý thông tin cá nhân và theo dõi hoạt động" | | Pass | 11/15/2015 | |
| **GUI-QLTT-03** | Kiểm tra nút Chỉnh sửa | 1. Truy cập /user/account<br>2. Kiểm tra nút Chỉnh sửa | Hiển thị nút "Chỉnh sửa" với icon Edit | | Pass | 11/15/2015 | |
| **GUI-QLTT-04** | Kiểm tra Avatar | 1. Truy cập /user/account<br>2. Kiểm tra Avatar | Hiển thị Avatar với fallback là chữ cái đầu của họ tên, có badge rank (VD: Gold) với icon Crown | | Pass | 11/15/2015 | |
| **GUI-QLTT-05** | Kiểm tra card Thông tin cá nhân | 1. Truy cập /user/account<br>2. Kiểm tra card Thông tin cá nhân | Hiển thị card "Thông tin cá nhân" với icon User, mô tả "Thông tin cơ bản của tài khoản" | | Pass | 11/15/2015 | |
| **GUI-QLTT-06** | Kiểm tra trường Họ và tên | 1. Truy cập /user/account<br>2. Kiểm tra trường Họ và tên | Hiển thị label "Họ và tên", input text hiển thị giá trị hiện tại, disabled khi không ở chế độ chỉnh sửa | | Pass | 11/15/2015 | |
| **GUI-QLTT-07** | Kiểm tra trường Email | 1. Truy cập /user/account<br>2. Kiểm tra trường Email | Hiển thị label "Email", input type email hiển thị giá trị hiện tại, disabled khi không ở chế độ chỉnh sửa | | Pass | 11/15/2015 | |
| **GUI-QLTT-08** | Kiểm tra trường Số điện thoại | 1. Truy cập /user/account<br>2. Kiểm tra trường Số điện thoại | Hiển thị label "Số điện thoại", input text hiển thị giá trị hiện tại, disabled khi không ở chế độ chỉnh sửa | | Pass | 11/15/2015 | |
| **GUI-QLTT-09** | Kiểm tra trường Ngày sinh | 1. Truy cập /user/account<br>2. Kiểm tra trường Ngày sinh | Hiển thị label "Ngày sinh", input type date hiển thị giá trị hiện tại, disabled khi không ở chế độ chỉnh sửa | | Pass | 11/15/2015 | |
| **GUI-QLTT-10** | Kiểm tra trường Địa chỉ | 1. Truy cập /user/account<br>2. Kiểm tra trường Địa chỉ | Hiển thị label "Địa chỉ", input text hiển thị giá trị hiện tại, disabled khi không ở chế độ chỉnh sửa | | Pass | 11/15/2015 | |
| **GUI-QLTT-11** | Kiểm tra card Thông tin tài khoản | 1. Truy cập /user/account<br>2. Kiểm tra card Thông tin tài khoản | Hiển thị card "Thông tin tài khoản" với icon Crown | | Pass | 11/15/2015 | |
| **GUI-QLTT-12** | Kiểm tra thông tin Email đăng nhập | 1. Truy cập /user/account<br>2. Kiểm tra thông tin Email đăng nhập | Hiển thị icon Mail, label "Email đăng nhập", giá trị email hiện tại | | Pass | 11/15/2015 | |
| **GUI-QLTT-13** | Kiểm tra thông tin Thành viên từ | 1. Truy cập /user/account<br>2. Kiểm tra thông tin Thành viên từ | Hiển thị icon Calendar, label "Thành viên từ", giá trị ngày tạo định dạng Việt Nam | | Pass | 11/15/2015 | |
| **GUI-QLTT-14** | Kiểm tra thông tin Lần đăng nhập cuối | 1. Truy cập /user/account<br>2. Kiểm tra thông tin Lần đăng nhập cuối | Hiển thị icon Calendar, label "Lần đăng nhập cuối", giá trị thời gian định dạng Việt Nam | | Pass | 11/15/2015 | |
| **GUI-QLTT-15** | Kiểm tra nút Lưu thay đổi | 1. Truy cập /user/account<br>2. Nhấn Chỉnh sửa<br>3. Kiểm tra nút Lưu | Hiển thị nút "Lưu thay đổi" với icon Save | | Pass | 11/15/2015 | |
| **GUI-QLTT-16** | Kiểm tra nút Hủy khi chỉnh sửa | 1. Truy cập /user/account<br>2. Nhấn Chỉnh sửa<br>3. Kiểm tra nút Hủy | Hiển thị nút "Hủy" với icon X | | Pass | 11/15/2015 | |
| **GUI-QLTT-17** | Kiểm tra card Thống kê hoạt động | 1. Truy cập /user/account<br>2. Kiểm tra card Thống kê | Hiển thị card "Thống kê hoạt động" với icon Star, mô tả "Tổng quan về hoạt động mua sắm của bạn" | | Pass | 11/15/2015 | |
| **GUI-QLTT-18** | Kiểm tra thống kê Đơn hàng | 1. Truy cập /user/account<br>2. Kiểm tra thống kê Đơn hàng | Hiển thị icon ShoppingBag, số lượng đơn hàng, text "Đơn hàng" | | Pass | 11/15/2015 | |
| **GUI-QLTT-19** | Kiểm tra thống kê Mô hình yêu thích | 1. Truy cập /user/account<br>2. Kiểm tra thống kê Yêu thích | Hiển thị icon Heart, số lượng mô hình yêu thích, text "Mô hình yêu thích" | | Pass | 11/15/2015 | |
| **GUI-QLTT-20** | Kiểm tra thống kê Điểm tích lũy | 1. Truy cập /user/account<br>2. Kiểm tra thống kê Điểm | Hiển thị icon Crown, số điểm tích lũy, text "Điểm tích lũy" | | Pass | 11/15/2015 | |
| **GUI-QLTT-21** | Kiểm tra card Thông tin thành viên | 1. Truy cập /user/account<br>2. Kiểm tra card Thành viên | Hiển thị card "Thông tin thành viên" với icon Crown | | Pass | 11/15/2015 | |
| **GUI-QLTT-22** | Kiểm tra badge Hạng thành viên | 1. Truy cập /user/account<br>2. Kiểm tra badge Rank | Hiển thị badge với hạng thành viên (VD: Gold) và icon Crown, có màu tương ứng với hạng | | Pass | 11/15/2015 | |
| **GUI-QLTT-23** | Kiểm tra thông tin Tổng chi tiêu | 1. Truy cập /user/account<br>2. Kiểm tra Tổng chi tiêu | Hiển thị label "Tổng chi tiêu:" với giá trị định dạng VNĐ | | Pass | 11/15/2015 | |
| **GUI-QLTT-24** | Kiểm tra thông tin Điểm tích lũy | 1. Truy cập /user/account<br>2. Kiểm tra Điểm tích lũy | Hiển thị label "Điểm tích lũy:" với giá trị số điểm | | Pass | 11/15/2015 | |

---

### Check FUNC: Cập nhật thông tin cá nhân

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-QLTT-01** | Mở trang Quản lý tài khoản | 1. Truy cập /user/account | Hiển thị trang với tiêu đề "Tài khoản của tôi", các card (Thông tin cá nhân, Thống kê hoạt động, Thông tin tài khoản, Thông tin thành viên), nút Chỉnh sửa, nút Đổi mật khẩu, nút Đăng xuất | | Pass | 11/15/2015 | |
| **FUNC-QLTT-02** | Bật chế độ chỉnh sửa | 1. Truy cập /user/account<br>2. Nhấn nút "Chỉnh sửa" | Tất cả các trường input trong card "Thông tin cá nhân" được enable, nút "Chỉnh sửa" biến thành "Hủy" và "Lưu thay đổi" | | Pass | 11/15/2015 | |
| **FUNC-QLTT-03** | Cập nhật thông tin thành công | 1. Truy cập /user/account<br>2. Nhấn Chỉnh sửa<br>3. Sửa thông tin (Họ tên, SĐT, Địa chỉ, Ngày sinh)<br>4. Nhấn Lưu thay đổi | Hiển thị thông báo "Cập nhật thông tin thành công", các trường được disable lại, thông tin mới được hiển thị | | Untested | 11/15/2015 | |
| **FUNC-QLTT-04** | Cập nhật thông tin - Thiếu Họ tên | 1. Truy cập /user/account<br>2. Nhấn Chỉnh sửa<br>3. Xóa họ tên<br>4. Nhấn Lưu thay đổi | Hiển thị thông báo lỗi "Họ tên không được để trống" | | Pass | 11/15/2015 | |
| **FUNC-QLTT-05** | Cập nhật thông tin - Thiếu Email | 1. Truy cập /user/account<br>2. Nhấn Chỉnh sửa<br>3. Xóa email<br>4. Nhấn Lưu thay đổi | Hiển thị thông báo lỗi "Email không được để trống" | | Pass | 11/15/2015 | |
| **FUNC-QLTT-06** | Cập nhật thông tin - Thiếu Số điện thoại | 1. Truy cập /user/account<br>2. Nhấn Chỉnh sửa<br>3. Xóa số điện thoại<br>4. Nhấn Lưu thay đổi | Hiển thị thông báo lỗi "Số điện thoại không được để trống" | | Pass | 11/15/2015 | |
| **FUNC-QLTT-07** | Hủy chỉnh sửa | 1. Truy cập /user/account<br>2. Nhấn Chỉnh sửa<br>3. Sửa một số thông tin<br>4. Nhấn Hủy | Các trường quay về giá trị ban đầu, chế độ chỉnh sửa tắt, nút "Hủy" và "Lưu" biến thành "Chỉnh sửa" | | Pass | 11/15/2015 | |
| **FUNC-QLTT-08** | Xem thông tin tài khoản | 1. Truy cập /user/account<br>2. Kiểm tra card Thông tin tài khoản | Hiển thị đầy đủ: Email đăng nhập, Thành viên từ, Lần đăng nhập cuối | | Pass | 11/15/2015 | |
| **FUNC-QLTT-09** | Xem thống kê hoạt động | 1. Truy cập /user/account<br>2. Kiểm tra card Thống kê hoạt động | Hiển thị đầy đủ: Số đơn hàng, Số mô hình yêu thích, Điểm tích lũy | | Pass | 11/15/2015 | |
| **FUNC-QLTT-10** | Xem thông tin thành viên | 1. Truy cập /user/account<br>2. Kiểm tra card Thông tin thành viên | Hiển thị đầy đủ: Hạng thành viên với badge, Giảm giá %, Tổng chi tiêu, Điểm tích lũy | | Pass | 11/15/2015 | |

---

### Function: Đăng xuất

#### Check GUI: Đăng xuất

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DX-01** | Kiểm tra nút Đăng xuất | 1. Truy cập /user/account<br>2. Kiểm tra nút Đăng xuất | Hiển thị nút "Đăng xuất" với icon LogOut variant destructive trong card "Thông tin tài khoản" | | Pass | 11/15/2015 | |
| **GUI-DX-02** | Kiểm tra modal xác nhận đăng xuất | 1. Truy cập /user/account<br>2. Nhấn nút Đăng xuất<br>3. Kiểm tra modal | Hiển thị AlertDialog với tiêu đề "Xác nhận đăng xuất", mô tả "Bạn có chắc chắn muốn đăng xuất khỏi hệ thống? Bạn sẽ cần đăng nhập lại để tiếp tục sử dụng." | | Pass | 11/15/2015 | |
| **GUI-DX-03** | Kiểm tra nút Hủy trong modal | 1. Truy cập /user/account<br>2. Mở modal đăng xuất<br>3. Kiểm tra nút Hủy | Hiển thị nút "Hủy" (AlertDialogCancel) | | Pass | 11/15/2015 | |
| **GUI-DX-04** | Kiểm tra nút Đăng xuất trong modal | 1. Truy cập /user/account<br>2. Mở modal đăng xuất<br>3. Kiểm tra nút Đăng xuất | Hiển thị nút "Đăng xuất" (AlertDialogAction) để xác nhận | | Pass | 11/15/2015 | |

---

### Check FUNC: Đăng xuất

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DX-01** | Mở modal xác nhận đăng xuất | 1. Truy cập /user/account<br>2. Nhấn nút "Đăng xuất" | Modal AlertDialog hiển thị với tiêu đề "Xác nhận đăng xuất", mô tả, 2 nút (Hủy, Đăng xuất) | | Pass | 11/15/2015 | |
| **FUNC-DX-02** | Đăng xuất thành công | 1. Truy cập /user/account<br>2. Nhấn nút Đăng xuất<br>3. Nhấn "Đăng xuất" trong modal | Hiển thị thông báo "Đăng xuất thành công", chuyển đến trang /user/auth/login, phiên đăng nhập bị xóa | | Untested | 11/15/2015 | |
| **FUNC-DX-03** | Hủy đăng xuất | 1. Truy cập /user/account<br>2. Nhấn nút Đăng xuất<br>3. Nhấn "Hủy" trong modal | Modal đóng, vẫn ở trang /user/account, không đăng xuất | | Pass | 11/15/2015 | |
| **FUNC-DX-04** | Đóng modal bằng click bên ngoài | 1. Truy cập /user/account<br>2. Nhấn nút Đăng xuất<br>3. Click bên ngoài modal | Modal đóng, không đăng xuất | | Pass | 11/15/2015 | |
| **FUNC-DX-05** | Kiểm tra xóa token sau đăng xuất | 1. Truy cập /user/account<br>2. Đăng xuất thành công<br>3. Kiểm tra localStorage/sessionStorage | Token bị xóa khỏi localStorage/sessionStorage | | Untested | 11/15/2015 | |
| **FUNC-DX-06** | Kiểm tra xóa session sau đăng xuất | 1. Truy cập /user/account<br>2. Đăng xuất thành công<br>3. Kiểm tra session | Session bị xóa trên server | | Untested | 11/15/2015 | |

---

*Template này được tạo theo chuẩn Markdown để dễ dàng quản lý và cập nhật test cases.*

