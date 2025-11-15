# Test Case Template - Quản lý tài khoản (Admin)

## Module Code
**Model Management Store: Quản lý tài khoản Admin**

## Test Requirement
1. Đăng nhập
2. Đăng ký
3. Khôi phục mật khẩu
4. Đổi mật khẩu
5. Cập nhật thông tin cá nhân
6. Đăng xuất

---

## Test Summary

### Người thực hiện Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 142 |
| **Fail** | 0 |
| **Untested** | 38 |
| **N/A** | 0 |
| **Number of Test cases** | 180 |

---

## Test Cases

### Function: Đăng nhập

#### Check GUI: Đăng nhập

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DN-01** | Kiểm tra icon Shield header | 1. Truy cập /admin/auth/login<br>2. Kiểm tra icon Shield | Hiển thị icon Shield trong vòng tròn ở header, màu primary | | Pass | 11/15/2015 | |
| **GUI-DN-02** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/auth/login<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Đăng nhập Admin" | | Pass | 11/15/2015 | |
| **GUI-DN-03** | Kiểm tra mô tả chức năng | 1. Truy cập /admin/auth/login<br>2. Kiểm tra mô tả | Hiển thị mô tả "Đăng nhập vào hệ thống quản trị" | | Pass | 11/15/2015 | |
| **GUI-DN-04** | Kiểm tra trường Email Admin | 1. Truy cập /admin/auth/login<br>2. Kiểm tra label và input Email | Hiển thị label "Email Admin", input type email với placeholder "admin@modelshop.com", có thuộc tính required | | Pass | 11/15/2015 | |
| **GUI-DN-05** | Kiểm tra trường Mật khẩu | 1. Truy cập /admin/auth/login<br>2. Kiểm tra label và input Mật khẩu | Hiển thị label "Mật khẩu", input type password với placeholder "Nhập mật khẩu", có thuộc tính required | | Pass | 11/15/2015 | |
| **GUI-DN-06** | Kiểm tra checkbox Ghi nhớ | 1. Truy cập /admin/auth/login<br>2. Kiểm tra checkbox | Hiển thị checkbox với label "Ghi nhớ đăng nhập" có thể tích chọn, nằm bên trái | | Pass | 11/15/2015 | |
| **GUI-DN-07** | Kiểm tra link Quên mật khẩu | 1. Truy cập /admin/auth/login<br>2. Kiểm tra link Quên mật khẩu | Hiển thị link "Quên mật khẩu?" có thể click, nằm bên phải, màu primary | | Pass | 11/15/2015 | |
| **GUI-DN-08** | Kiểm tra nút Đăng nhập Admin | 1. Truy cập /admin/auth/login<br>2. Kiểm tra nút Đăng nhập | Hiển thị nút "Đăng nhập Admin" type submit, chiếm toàn bộ chiều rộng form | | Pass | 11/15/2015 | |
| **GUI-DN-09** | Kiểm tra separator "Hoặc" | 1. Truy cập /admin/auth/login<br>2. Kiểm tra separator | Hiển thị separator với text "Hoặc" ở giữa, chữ in hoa, màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-DN-10** | Kiểm tra link Đăng nhập với tài khoản khách hàng | 1. Truy cập /admin/auth/login<br>2. Kiểm tra link | Hiển thị link "Đăng nhập với tài khoản khách hàng" với icon ArrowLeft, màu primary, có thể click | | Pass | 11/15/2015 | |
| **GUI-DN-11** | Kiểm tra thông báo cảnh báo | 1. Truy cập /admin/auth/login<br>2. Kiểm tra thông báo | Hiển thị text "Chỉ dành cho quản trị viên được ủy quyền" màu muted-foreground, kích thước text-sm | | Pass | 11/15/2015 | |
| **GUI-DN-12** | Kiểm tra layout trang | 1. Truy cập /admin/auth/login<br>2. Kiểm tra layout tổng thể | Trang có background gradient từ primary/5 đến secondary/5, card container nằm giữa màn hình với max-width-md, form đăng nhập bên trong card | | Pass | 11/15/2015 | |
| **GUI-DN-13** | Kiểm tra card container | 1. Truy cập /admin/auth/login<br>2. Kiểm tra card | Hiển thị card container chứa toàn bộ form đăng nhập, có giới hạn chiều rộng tối đa (max-w-md), có padding | | Pass | 11/15/2015 | |

---

### Check FUNC: Đăng nhập

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DN-01** | Mở trang đăng nhập | 1. Truy cập /admin/auth/login | Hiển thị form đăng nhập với đầy đủ các thành phần: icon Shield, tiêu đề "Đăng nhập Admin", mô tả "Đăng nhập vào hệ thống quản trị", 2 trường nhập (Email Admin, Mật khẩu), checkbox ghi nhớ, link quên mật khẩu, nút đăng nhập Admin, separator "Hoặc", link đăng nhập với tài khoản khách hàng, thông báo cảnh báo | | Pass | 11/15/2015 | |
| **FUNC-DN-02** | Đăng nhập thành công với thông tin hợp lệ | 1. Truy cập /admin/auth/login<br>2. Nhập email hợp lệ (VD: admin@modelshop.com)<br>3. Nhập mật khẩu đúng<br>4. Nhấn nút Đăng nhập Admin | Hệ thống xác thực thông tin, chuyển đến dashboard Admin (/admin), lưu phiên đăng nhập và lưu token, hiển thị thông báo thành công | | Untested | 11/15/2015 | |
| **FUNC-DN-03** | Đăng nhập với email không tồn tại | 1. Truy cập /admin/auth/login<br>2. Nhập email không tồn tại (VD: notexist@test.com)<br>3. Nhập mật khẩu bất kỳ<br>4. Nhấn Đăng nhập Admin | Hiển thị thông báo lỗi "Tài khoản hoặc mật khẩu không đúng", không chuyển trang, vẫn ở trang đăng nhập | | Untested | 11/15/2015 | |
| **FUNC-DN-04** | Đăng nhập với mật khẩu sai | 1. Truy cập /admin/auth/login<br>2. Nhập email hợp lệ<br>3. Nhập mật khẩu sai<br>4. Nhấn Đăng nhập Admin | Hiển thị thông báo lỗi "Tài khoản hoặc mật khẩu không đúng", không chuyển trang, vẫn ở trang đăng nhập | | Untested | 11/15/2015 | |
| **FUNC-DN-05** | Đăng nhập thiếu email | 1. Truy cập /admin/auth/login<br>2. Để trống email<br>3. Nhập mật khẩu<br>4. Nhấn Đăng nhập Admin | Trình duyệt hiển thị cảnh báo "Please fill out this field" hoặc validation message "Trường này là bắt buộc", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-DN-06** | Đăng nhập thiếu mật khẩu | 1. Truy cập /admin/auth/login<br>2. Nhập email<br>3. Để trống mật khẩu<br>4. Nhấn Đăng nhập Admin | Trình duyệt hiển thị cảnh báo "Please fill out this field" hoặc validation message "Trường này là bắt buộc", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-DN-07** | Đăng nhập với email sai định dạng | 1. Truy cập /admin/auth/login<br>2. Nhập email không đúng định dạng (VD: "invalid-email")<br>3. Nhập mật khẩu<br>4. Nhấn Đăng nhập Admin | Trình duyệt hiển thị cảnh báo "Please include an '@' in the email address" hoặc validation message "Dữ liệu không hợp lệ", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-DN-08** | Chức năng ghi nhớ - Có tích chọn | 1. Truy cập /admin/auth/login<br>2. Tích checkbox "Ghi nhớ đăng nhập"<br>3. Nhập thông tin hợp lệ<br>4. Đăng nhập thành công | Đăng nhập thành công, trình duyệt lưu cookie/session với thời hạn dài hơn, khi đóng trình duyệt và mở lại vẫn còn đăng nhập | | Untested | 11/15/2015 | |
| **FUNC-DN-09** | Chức năng ghi nhớ - Không tích chọn | 1. Truy cập /admin/auth/login<br>2. Không tích checkbox<br>3. Nhập thông tin hợp lệ<br>4. Đăng nhập thành công | Đăng nhập thành công, trình duyệt lưu cookie/session với thời hạn ngắn hơn, khi đóng trình duyệt sẽ đăng xuất | | Untested | 11/15/2015 | |
| **FUNC-DN-10** | Nhấn link Quên mật khẩu | 1. Truy cập /admin/auth/login<br>2. Nhấn link "Quên mật khẩu?" | Chuyển đến trang /admin/auth/forgot-password | | Pass | 11/15/2015 | |
| **FUNC-DN-11** | Nhấn link Đăng nhập với tài khoản khách hàng | 1. Truy cập /admin/auth/login<br>2. Nhấn link "Đăng nhập với tài khoản khách hàng" | Chuyển đến trang /user/auth/login | | Pass | 11/15/2015 | |
| **FUNC-DN-12** | Submit form bằng phím Enter | 1. Truy cập /admin/auth/login<br>2. Nhập thông tin hợp lệ<br>3. Nhấn Enter trong trường mật khẩu | Form được gửi, xử lý đăng nhập như khi nhấn nút Đăng nhập Admin | | Untested | 11/15/2015 | |
| **FUNC-DN-13** | Đăng nhập với tài khoản chưa kích hoạt | 1. Truy cập /admin/auth/login<br>2. Nhập email tài khoản chưa kích hoạt<br>3. Nhập mật khẩu đúng<br>4. Nhấn Đăng nhập Admin | Hiển thị thông báo lỗi "Tài khoản chưa được kích hoạt. Vui lòng liên hệ quản trị viên cấp cao", không chuyển trang | | Untested | 11/15/2015 | |
| **FUNC-DN-14** | Đăng nhập với tài khoản bị khóa | 1. Truy cập /admin/auth/login<br>2. Nhập email tài khoản bị khóa<br>3. Nhập mật khẩu đúng<br>4. Nhấn Đăng nhập Admin | Hiển thị thông báo lỗi "Tài khoản đã bị khóa. Vui lòng liên hệ quản trị viên", không chuyển trang | | Untested | 11/15/2015 | |
| **FUNC-DN-15** | Đăng nhập sai nhiều lần - Hiển thị Captcha | 1. Truy cập /admin/auth/login<br>2. Nhập sai thông tin đăng nhập 3 lần liên tiếp<br>3. Lần thứ 4, nhập thông tin | Sau 3 lần đăng nhập sai, hiển thị captcha, yêu cầu nhập captcha trước khi tiếp tục đăng nhập | | Untested | 11/15/2015 | |
| **FUNC-DN-16** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/auth/login<br>2. Tắt kết nối mạng<br>3. Nhập thông tin hợp lệ<br>4. Nhấn Đăng nhập Admin | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", không chuyển trang | | Untested | 11/15/2015 | |
| **FUNC-DN-17** | Xử lý khi server lỗi | 1. Truy cập /admin/auth/login<br>2. Nhập thông tin hợp lệ<br>3. Server trả về lỗi 500<br>4. Nhấn Đăng nhập Admin | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau", không chuyển trang | | Untested | 11/15/2015 | |
| **FUNC-DN-18** | Kiểm tra redirect sau đăng nhập | 1. Truy cập /admin/auth/login?redirect=/admin/products<br>2. Nhập thông tin hợp lệ<br>3. Đăng nhập thành công | Sau khi đăng nhập thành công, chuyển đến trang /admin/products thay vì dashboard mặc định | | Untested | 11/15/2015 | |
| **FUNC-DN-19** | Kiểm tra lưu token sau đăng nhập | 1. Truy cập /admin/auth/login<br>2. Nhập thông tin hợp lệ<br>3. Đăng nhập thành công<br>4. Kiểm tra localStorage/sessionStorage | Token được lưu vào localStorage hoặc sessionStorage, có thể sử dụng cho các request tiếp theo | | Untested | 11/15/2015 | |
| **FUNC-DN-20** | Kiểm tra tạo phiên đăng nhập | 1. Truy cập /admin/auth/login<br>2. Nhập thông tin hợp lệ<br>3. Đăng nhập thành công<br>4. Kiểm tra session | Phiên đăng nhập được tạo và lưu trữ trên server, có thể theo dõi trong lịch sử đăng nhập | | Untested | 11/15/2015 | |

---

### Function: Đăng ký

#### Check GUI: Đăng ký

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DK-01** | Kiểm tra icon Shield header | 1. Truy cập /admin/auth/register<br>2. Kiểm tra icon Shield | Hiển thị icon Shield trong vòng tròn ở header, màu primary | | Pass | 11/15/2015 | |
| **GUI-DK-02** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/auth/register<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Đăng ký tài khoản Admin" | | Pass | 11/15/2015 | |
| **GUI-DK-03** | Kiểm tra mô tả chức năng | 1. Truy cập /admin/auth/register<br>2. Kiểm tra mô tả | Hiển thị mô tả "Tạo tài khoản quản trị viên mới cho hệ thống Model Shop" | | Pass | 11/15/2015 | |
| **GUI-DK-04** | Kiểm tra trường Họ và tên | 1. Truy cập /admin/auth/register<br>2. Kiểm tra trường Họ và tên | Hiển thị label "Họ và tên *" với icon User, input type text với placeholder "Nhập họ và tên", có thuộc tính required | | Pass | 11/15/2015 | |
| **GUI-DK-05** | Kiểm tra trường Email công ty | 1. Truy cập /admin/auth/register<br>2. Kiểm tra trường Email | Hiển thị label "Email công ty *" với icon Mail, input type email với placeholder "admin@modelshop.com", có thuộc tính required | | Pass | 11/15/2015 | |
| **GUI-DK-06** | Kiểm tra trường Số điện thoại | 1. Truy cập /admin/auth/register<br>2. Kiểm tra trường Số điện thoại | Hiển thị label "Số điện thoại *" với icon Phone, input type tel với placeholder "Nhập số điện thoại", có thuộc tính required | | Pass | 11/15/2015 | |
| **GUI-DK-07** | Kiểm tra trường Mã nhân viên | 1. Truy cập /admin/auth/register<br>2. Kiểm tra trường Mã nhân viên | Hiển thị label "Mã nhân viên *" với icon Key, input type text với placeholder "EMP001", có thuộc tính required | | Pass | 11/15/2015 | |
| **GUI-DK-08** | Kiểm tra trường Phòng ban | 1. Truy cập /admin/auth/register<br>2. Kiểm tra trường Phòng ban | Hiển thị label "Phòng ban *" với icon Building, Select với placeholder "Chọn phòng ban", có các option: Ban Giám đốc, Phòng Kinh doanh, Phòng Marketing, Phòng Kho, Phòng Chăm sóc khách hàng, Phòng IT, Phòng Nhân sự, Phòng Tài chính | | Pass | 11/15/2015 | |
| **GUI-DK-09** | Kiểm tra trường Chức vụ | 1. Truy cập /admin/auth/register<br>2. Kiểm tra trường Chức vụ | Hiển thị label "Chức vụ *" với icon Shield, input type text với placeholder "Nhập chức vụ", có thuộc tính required | | Pass | 11/15/2015 | |
| **GUI-DK-10** | Kiểm tra trường Mật khẩu | 1. Truy cập /admin/auth/register<br>2. Kiểm tra trường Mật khẩu | Hiển thị label "Mật khẩu *", input type password với placeholder "Nhập mật khẩu", có nút icon Eye/EyeOff để hiển thị/ẩn mật khẩu, có thuộc tính required, có text hướng dẫn "Mật khẩu phải có ít nhất 8 ký tự, bao gồm chữ hoa, chữ thường và số" | | Pass | 11/15/2015 | |
| **GUI-DK-11** | Kiểm tra trường Xác nhận mật khẩu | 1. Truy cập /admin/auth/register<br>2. Kiểm tra trường Xác nhận mật khẩu | Hiển thị label "Xác nhận mật khẩu *", input type password với placeholder "Nhập lại mật khẩu", có nút icon Eye/EyeOff để hiển thị/ẩn mật khẩu, có thuộc tính required | | Pass | 11/15/2015 | |
| **GUI-DK-12** | Kiểm tra checkbox Điều khoản | 1. Truy cập /admin/auth/register<br>2. Kiểm tra checkbox | Hiển thị checkbox với label "Tôi đồng ý với Điều khoản sử dụng Admin và Chính sách bảo mật", có link đến trang điều khoản và chính sách | | Pass | 11/15/2015 | |
| **GUI-DK-13** | Kiểm tra nút Đăng ký | 1. Truy cập /admin/auth/register<br>2. Kiểm tra nút Đăng ký | Hiển thị nút "Đăng ký tài khoản Admin" type submit, chiếm toàn bộ chiều rộng, có thể disabled khi đang loading | | Pass | 11/15/2015 | |
| **GUI-DK-14** | Kiểm tra separator "Hoặc" | 1. Truy cập /admin/auth/register<br>2. Kiểm tra separator | Hiển thị separator với text "Hoặc" ở giữa, chữ in hoa | | Pass | 11/15/2015 | |
| **GUI-DK-15** | Kiểm tra link Đăng nhập với tài khoản admin hiện có | 1. Truy cập /admin/auth/register<br>2. Kiểm tra link | Hiển thị link "Đăng nhập với tài khoản admin hiện có" với icon Shield, màu primary | | Pass | 11/15/2015 | |
| **GUI-DK-16** | Kiểm tra link Đăng ký tài khoản khách hàng | 1. Truy cập /admin/auth/register<br>2. Kiểm tra link | Hiển thị text "Chưa có tài khoản khách hàng? " với link "Đăng ký tài khoản khách hàng" có thể click | | Pass | 11/15/2015 | |
| **GUI-DK-17** | Kiểm tra thông báo cảnh báo | 1. Truy cập /admin/auth/register<br>2. Kiểm tra thông báo | Hiển thị text "⚠️ Chỉ dành cho nhân viên được ủy quyền" và "Tài khoản admin cần được xác thực bởi quản trị viên cấp cao", màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-DK-18** | Kiểm tra layout trang | 1. Truy cập /admin/auth/register<br>2. Kiểm tra layout tổng thể | Trang có background gradient từ primary/5 đến secondary/5, card container nằm giữa màn hình với max-width-2xl, form đăng ký bên trong card, có scroll nếu nội dung dài | | Pass | 11/15/2015 | |

---

### Check FUNC: Đăng ký

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DK-01** | Mở trang đăng ký | 1. Truy cập /admin/auth/register | Hiển thị form đăng ký với đầy đủ các thành phần: icon Shield, tiêu đề "Đăng ký tài khoản Admin", mô tả, các trường nhập (Họ tên, Email công ty, SĐT, Mã nhân viên, Phòng ban, Chức vụ, Mật khẩu, Xác nhận mật khẩu), checkbox điều khoản, nút đăng ký, separator, link đăng nhập admin, link đăng ký khách hàng, thông báo cảnh báo | | Pass | 11/15/2015 | |
| **FUNC-DK-02** | Đăng ký thành công với thông tin hợp lệ | 1. Truy cập /admin/auth/register<br>2. Điền đầy đủ thông tin hợp lệ<br>3. Tích checkbox điều khoản<br>4. Nhấn Đăng ký | Hiển thị thông báo "Đăng ký tài khoản admin thành công!", chuyển đến trang /admin/auth/login, tài khoản cần được xác thực bởi quản trị viên cấp cao | | Untested | 11/15/2015 | |
| **FUNC-DK-03** | Đăng ký thiếu Họ tên | 1. Truy cập /admin/auth/register<br>2. Để trống Họ tên<br>3. Điền các trường khác<br>4. Nhấn Đăng ký | Hiển thị thông báo lỗi "Họ tên không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-DK-04** | Đăng ký thiếu Email | 1. Truy cập /admin/auth/register<br>2. Để trống Email<br>3. Điền các trường khác<br>4. Nhấn Đăng ký | Hiển thị thông báo lỗi "Email không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-DK-05** | Đăng ký với Email không hợp lệ | 1. Truy cập /admin/auth/register<br>2. Nhập email không có @<br>3. Điền các trường khác<br>4. Nhấn Đăng ký | Hiển thị thông báo lỗi "Email không hợp lệ", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-DK-06** | Đăng ký với Email đã tồn tại | 1. Truy cập /admin/auth/register<br>2. Nhập email đã tồn tại trong hệ thống<br>3. Điền các trường khác<br>4. Nhấn Đăng ký | Hiển thị thông báo lỗi "Email đã tồn tại trong hệ thống", form không được gửi | | Untested | 11/15/2015 | |
| **FUNC-DK-07** | Đăng ký thiếu Số điện thoại | 1. Truy cập /admin/auth/register<br>2. Để trống Số điện thoại<br>3. Điền các trường khác<br>4. Nhấn Đăng ký | Hiển thị thông báo lỗi "Số điện thoại không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-DK-08** | Đăng ký thiếu Mã nhân viên | 1. Truy cập /admin/auth/register<br>2. Để trống Mã nhân viên<br>3. Điền các trường khác<br>4. Nhấn Đăng ký | Hiển thị thông báo lỗi "Mã nhân viên không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-DK-09** | Đăng ký thiếu Phòng ban | 1. Truy cập /admin/auth/register<br>2. Không chọn Phòng ban<br>3. Điền các trường khác<br>4. Nhấn Đăng ký | Hiển thị thông báo lỗi "Vui lòng chọn phòng ban", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-DK-10** | Đăng ký thiếu Chức vụ | 1. Truy cập /admin/auth/register<br>2. Để trống Chức vụ<br>3. Điền các trường khác<br>4. Nhấn Đăng ký | Hiển thị thông báo lỗi "Chức vụ không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-DK-11** | Đăng ký thiếu Mật khẩu | 1. Truy cập /admin/auth/register<br>2. Để trống Mật khẩu<br>3. Điền các trường khác<br>4. Nhấn Đăng ký | Hiển thị thông báo lỗi "Mật khẩu không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-DK-12** | Đăng ký với Mật khẩu quá ngắn | 1. Truy cập /admin/auth/register<br>2. Nhập mật khẩu < 8 ký tự<br>3. Điền các trường khác<br>4. Nhấn Đăng ký | Hiển thị thông báo lỗi "Mật khẩu phải có ít nhất 8 ký tự", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-DK-13** | Đăng ký với Mật khẩu không đủ yêu cầu | 1. Truy cập /admin/auth/register<br>2. Nhập mật khẩu không có chữ hoa, chữ thường và số<br>3. Điền các trường khác<br>4. Nhấn Đăng ký | Hiển thị thông báo lỗi "Mật khẩu phải chứa ít nhất 1 chữ hoa, 1 chữ thường và 1 số", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-DK-14** | Đăng ký với Mật khẩu xác nhận không khớp | 1. Truy cập /admin/auth/register<br>2. Nhập mật khẩu<br>3. Nhập xác nhận mật khẩu khác<br>4. Nhấn Đăng ký | Hiển thị thông báo lỗi "Mật khẩu xác nhận không khớp", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-DK-15** | Đăng ký không tích checkbox điều khoản | 1. Truy cập /admin/auth/register<br>2. Điền đầy đủ thông tin<br>3. Không tích checkbox điều khoản<br>4. Nhấn Đăng ký | Hiển thị thông báo lỗi "Vui lòng đồng ý với điều khoản sử dụng", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-DK-16** | Hiển thị/ẩn mật khẩu | 1. Truy cập /admin/auth/register<br>2. Nhập mật khẩu<br>3. Click icon Eye | Input chuyển từ type password sang type text, hiển thị mật khẩu, icon chuyển thành EyeOff | | Pass | 11/15/2015 | |
| **FUNC-DK-17** | Hiển thị/ẩn xác nhận mật khẩu | 1. Truy cập /admin/auth/register<br>2. Nhập xác nhận mật khẩu<br>3. Click icon Eye | Input chuyển từ type password sang type text, hiển thị mật khẩu, icon chuyển thành EyeOff | | Pass | 11/15/2015 | |
| **FUNC-DK-18** | Nhấn link Đăng nhập với tài khoản admin hiện có | 1. Truy cập /admin/auth/register<br>2. Nhấn link "Đăng nhập với tài khoản admin hiện có" | Chuyển đến trang /admin/auth/login | | Pass | 11/15/2015 | |
| **FUNC-DK-19** | Nhấn link Đăng ký tài khoản khách hàng | 1. Truy cập /admin/auth/register<br>2. Nhấn link "Đăng ký tài khoản khách hàng" | Chuyển đến trang /user/auth/register | | Pass | 11/15/2015 | |
| **FUNC-DK-20** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/auth/register<br>2. Điền đầy đủ thông tin<br>3. Tắt kết nối mạng<br>4. Nhấn Đăng ký | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", form không được gửi | | Untested | 11/15/2015 | |
| **FUNC-DK-21** | Xử lý khi server lỗi | 1. Truy cập /admin/auth/register<br>2. Điền đầy đủ thông tin<br>3. Server trả về lỗi 500<br>4. Nhấn Đăng ký | Hiển thị thông báo lỗi "Có lỗi xảy ra, vui lòng thử lại", form không được gửi | | Untested | 11/15/2015 | |

---

### Function: Khôi phục mật khẩu

#### Check GUI: Khôi phục mật khẩu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-KPMK-01** | Kiểm tra icon Shield header | 1. Truy cập /admin/auth/forgot-password<br>2. Kiểm tra icon Shield | Hiển thị icon Shield trong vòng tròn màu xanh ở header | | Pass | 11/15/2015 | |
| **GUI-KPMK-02** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/auth/forgot-password<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Khôi phục mật khẩu" | | Pass | 11/15/2015 | |
| **GUI-KPMK-03** | Kiểm tra mô tả chức năng | 1. Truy cập /admin/auth/forgot-password<br>2. Kiểm tra mô tả | Hiển thị mô tả "Chọn phương thức khôi phục mật khẩu của bạn" | | Pass | 11/15/2015 | |
| **GUI-KPMK-04** | Kiểm tra phương thức Email | 1. Truy cập /admin/auth/forgot-password<br>2. Kiểm tra phương thức Email | Hiển thị radio button với icon Mail, label "Email", mô tả "Gửi mã xác thực qua email", có thể chọn | | Pass | 11/15/2015 | |
| **GUI-KPMK-05** | Kiểm tra phương thức SMS | 1. Truy cập /admin/auth/forgot-password<br>2. Kiểm tra phương thức SMS | Hiển thị radio button với icon Phone, label "SMS", mô tả "Gửi mã xác thực qua SMS", có thể chọn | | Pass | 11/15/2015 | |
| **GUI-KPMK-06** | Kiểm tra phương thức Câu hỏi bảo mật | 1. Truy cập /admin/auth/forgot-password<br>2. Kiểm tra phương thức Câu hỏi bảo mật | Hiển thị radio button với icon MessageSquare, label "Câu hỏi bảo mật", mô tả "Trả lời câu hỏi bảo mật", có thể chọn | | Pass | 11/15/2015 | |
| **GUI-KPMK-07** | Kiểm tra trường nhập Email (khi chọn Email) | 1. Truy cập /admin/auth/forgot-password<br>2. Chọn phương thức Email<br>3. Kiểm tra trường nhập | Hiển thị label "Email", input type email với placeholder "Nhập email của bạn" | | Pass | 11/15/2015 | |
| **GUI-KPMK-08** | Kiểm tra trường nhập Số điện thoại (khi chọn SMS) | 1. Truy cập /admin/auth/forgot-password<br>2. Chọn phương thức SMS<br>3. Kiểm tra trường nhập | Hiển thị label "Số điện thoại", input type tel với placeholder "Nhập số điện thoại của bạn" | | Pass | 11/15/2015 | |
| **GUI-KPMK-09** | Kiểm tra câu hỏi bảo mật (khi chọn Câu hỏi bảo mật) | 1. Truy cập /admin/auth/forgot-password<br>2. Chọn phương thức Câu hỏi bảo mật<br>3. Kiểm tra câu hỏi | Hiển thị 3 câu hỏi bảo mật với các trường nhập câu trả lời | | Pass | 11/15/2015 | |
| **GUI-KPMK-10** | Kiểm tra nút Tiếp tục | 1. Truy cập /admin/auth/forgot-password<br>2. Kiểm tra nút | Hiển thị nút "Tiếp tục" với icon Key, chiếm toàn bộ chiều rộng, có thể disabled khi đang loading | | Pass | 11/15/2015 | |
| **GUI-KPMK-11** | Kiểm tra màn hình nhập mã xác thực | 1. Truy cập /admin/auth/forgot-password<br>2. Gửi mã xác thực thành công<br>3. Kiểm tra màn hình | Hiển thị Alert với icon Mail, mô tả "Mã xác thực đã được gửi đến email/số điện thoại của bạn", trường nhập mã xác thực 6 chữ số, nút "Xác thực" với icon CheckCircle, link "Quay lại" với icon ArrowLeft | | Pass | 11/15/2015 | |
| **GUI-KPMK-12** | Kiểm tra màn hình đặt mật khẩu mới | 1. Truy cập /admin/auth/forgot-password<br>2. Xác thực mã thành công<br>3. Kiểm tra màn hình | Hiển thị Alert với icon CheckCircle, mô tả "Mã xác thực hợp lệ. Vui lòng đặt mật khẩu mới cho tài khoản của bạn", trường Mật khẩu mới, trường Xác nhận mật khẩu, thanh hiển thị độ mạnh mật khẩu, danh sách yêu cầu mật khẩu, nút "Đặt lại mật khẩu" với icon Lock, link "Quay lại" | | Pass | 11/15/2015 | |
| **GUI-KPMK-13** | Kiểm tra màn hình hoàn thành | 1. Truy cập /admin/auth/forgot-password<br>2. Đặt lại mật khẩu thành công<br>3. Kiểm tra màn hình | Hiển thị icon CheckCircle trong vòng tròn xanh, tiêu đề "Khôi phục mật khẩu thành công", mô tả, nút "Đăng nhập ngay" với icon User, nút "Quay về trang chủ" với icon ArrowLeft | | Pass | 11/15/2015 | |
| **GUI-KPMK-14** | Kiểm tra link Đăng nhập | 1. Truy cập /admin/auth/forgot-password<br>2. Kiểm tra link | Hiển thị text "Bạn có tài khoản? " với link "Đăng nhập" có thể click | | Pass | 11/15/2015 | |

---

### Check FUNC: Khôi phục mật khẩu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-KPMK-01** | Mở trang khôi phục mật khẩu | 1. Truy cập /admin/auth/forgot-password | Hiển thị trang với icon Shield, tiêu đề "Khôi phục mật khẩu", mô tả, 3 phương thức khôi phục (Email, SMS, Câu hỏi bảo mật), nút "Tiếp tục", link đăng nhập | | Pass | 11/15/2015 | |
| **FUNC-KPMK-02** | Chọn phương thức Email | 1. Truy cập /admin/auth/forgot-password<br>2. Click chọn phương thức Email | Hiển thị trường nhập Email, radio button Email được chọn (có dấu chấm trắng trong vòng tròn xanh) | | Pass | 11/15/2015 | |
| **FUNC-KPMK-03** | Chọn phương thức SMS | 1. Truy cập /admin/auth/forgot-password<br>2. Click chọn phương thức SMS | Hiển thị trường nhập Số điện thoại, radio button SMS được chọn | | Pass | 11/15/2015 | |
| **FUNC-KPMK-04** | Chọn phương thức Câu hỏi bảo mật | 1. Truy cập /admin/auth/forgot-password<br>2. Click chọn phương thức Câu hỏi bảo mật | Hiển thị 3 câu hỏi bảo mật với các trường nhập câu trả lời, radio button Câu hỏi bảo mật được chọn | | Pass | 11/15/2015 | |
| **FUNC-KPMK-05** | Gửi mã xác thực qua Email thành công | 1. Truy cập /admin/auth/forgot-password<br>2. Chọn phương thức Email<br>3. Nhập email hợp lệ<br>4. Nhấn "Tiếp tục" | Hiển thị thông báo "Mã xác thực đã được gửi", chuyển sang màn hình nhập mã xác thực | | Untested | 11/15/2015 | |
| **FUNC-KPMK-06** | Gửi mã xác thực qua SMS thành công | 1. Truy cập /admin/auth/forgot-password<br>2. Chọn phương thức SMS<br>3. Nhập số điện thoại hợp lệ<br>4. Nhấn "Tiếp tục" | Hiển thị thông báo "Mã xác thực đã được gửi", chuyển sang màn hình nhập mã xác thực | | Untested | 11/15/2015 | |
| **FUNC-KPMK-07** | Trả lời câu hỏi bảo mật thành công | 1. Truy cập /admin/auth/forgot-password<br>2. Chọn phương thức Câu hỏi bảo mật<br>3. Nhập đúng câu trả lời cho 3 câu hỏi<br>4. Nhấn "Tiếp tục" | Hiển thị thông báo "Xác thực thành công", chuyển sang màn hình đặt mật khẩu mới | | Untested | 11/15/2015 | |
| **FUNC-KPMK-08** | Gửi mã - Email không tồn tại | 1. Truy cập /admin/auth/forgot-password<br>2. Chọn Email<br>3. Nhập email không tồn tại<br>4. Nhấn "Tiếp tục" | Hiển thị thông báo lỗi "Email không tồn tại trong hệ thống" | | Untested | 11/15/2015 | |
| **FUNC-KPMK-09** | Gửi mã - Thiếu email | 1. Truy cập /admin/auth/forgot-password<br>2. Chọn Email<br>3. Để trống email<br>4. Nhấn "Tiếp tục" | Hiển thị thông báo lỗi "Vui lòng nhập email", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-KPMK-10** | Xác thực mã thành công | 1. Truy cập /admin/auth/forgot-password<br>2. Gửi mã xác thực<br>3. Nhập mã xác thực đúng<br>4. Nhấn "Xác thực" | Hiển thị thông báo "Mã xác thực hợp lệ", chuyển sang màn hình đặt mật khẩu mới | | Untested | 11/15/2015 | |
| **FUNC-KPMK-11** | Xác thực mã - Mã sai | 1. Truy cập /admin/auth/forgot-password<br>2. Gửi mã xác thực<br>3. Nhập mã xác thực sai<br>4. Nhấn "Xác thực" | Hiển thị thông báo lỗi "Mã xác thực không đúng" | | Untested | 11/15/2015 | |
| **FUNC-KPMK-12** | Đặt lại mật khẩu thành công | 1. Truy cập /admin/auth/forgot-password<br>2. Xác thực mã thành công<br>3. Nhập mật khẩu mới hợp lệ (≥8 ký tự, có chữ hoa, số)<br>4. Nhập xác nhận mật khẩu khớp<br>5. Nhấn "Đặt lại mật khẩu" | Hiển thị thông báo "Mật khẩu đã được đặt lại thành công", chuyển sang màn hình hoàn thành | | Untested | 11/15/2015 | |
| **FUNC-KPMK-13** | Đặt lại mật khẩu - Mật khẩu quá ngắn | 1. Truy cập /admin/auth/forgot-password<br>2. Xác thực mã thành công<br>3. Nhập mật khẩu < 8 ký tự<br>4. Nhấn "Đặt lại mật khẩu" | Hiển thị thông báo lỗi "Mật khẩu phải có ít nhất 8 ký tự", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-KPMK-14** | Đặt lại mật khẩu - Mật khẩu xác nhận không khớp | 1. Truy cập /admin/auth/forgot-password<br>2. Xác thực mã thành công<br>3. Nhập mật khẩu mới<br>4. Nhập xác nhận mật khẩu khác<br>5. Nhấn "Đặt lại mật khẩu" | Hiển thị Alert với icon AlertCircle, mô tả "Mật khẩu xác nhận không khớp", nút "Đặt lại mật khẩu" bị disabled | | Pass | 11/15/2015 | |
| **FUNC-KPMK-15** | Hiển thị độ mạnh mật khẩu | 1. Truy cập /admin/auth/forgot-password<br>2. Xác thực mã thành công<br>3. Nhập mật khẩu mới | Hiển thị thanh progress và label độ mạnh mật khẩu (Yếu/Trung bình/Mạnh) với màu tương ứng (đỏ/vàng/xanh) | | Pass | 11/15/2015 | |
| **FUNC-KPMK-16** | Hiển thị yêu cầu mật khẩu | 1. Truy cập /admin/auth/forgot-password<br>2. Xác thực mã thành công<br>3. Nhập mật khẩu mới | Hiển thị danh sách yêu cầu mật khẩu với các dấu chấm màu xanh khi đạt yêu cầu, màu xám khi chưa đạt: "Ít nhất 8 ký tự", "Có ít nhất 1 chữ hoa", "Có ít nhất 1 chữ số", "Có ít nhất 1 ký tự đặc biệt" | | Pass | 11/15/2015 | |
| **FUNC-KPMK-17** | Nhấn nút Đăng nhập ngay | 1. Truy cập /admin/auth/forgot-password<br>2. Hoàn thành khôi phục mật khẩu<br>3. Nhấn "Đăng nhập ngay" | Chuyển đến trang /admin/auth/login | | Pass | 11/15/2015 | |
| **FUNC-KPMK-18** | Nhấn link Quay lại | 1. Truy cập /admin/auth/forgot-password<br>2. Ở màn hình nhập mã xác thực<br>3. Nhấn "Quay lại" | Quay lại màn hình chọn phương thức khôi phục | | Pass | 11/15/2015 | |
| **FUNC-KPMK-19** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/auth/forgot-password<br>2. Chọn phương thức và nhập thông tin<br>3. Tắt kết nối mạng<br>4. Nhấn "Tiếp tục" | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại" | | Untested | 11/15/2015 | |
| **FUNC-KPMK-20** | Xử lý khi server lỗi | 1. Truy cập /admin/auth/forgot-password<br>2. Chọn phương thức và nhập thông tin<br>3. Server trả về lỗi 500<br>4. Nhấn "Tiếp tục" | Hiển thị thông báo lỗi "Có lỗi xảy ra khi gửi mã xác thực" | | Untested | 11/15/2015 | |

---

### Function: Đổi mật khẩu

#### Check GUI: Đổi mật khẩu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DMK-01** | Kiểm tra nút Đổi mật khẩu | 1. Truy cập /admin/account<br>2. Kiểm tra nút Đổi mật khẩu | Hiển thị nút "Đổi mật khẩu" với icon Key trong card "Thông tin tài khoản", variant outline, chiếm toàn bộ chiều rộng | | Pass | 11/15/2015 | |
| **GUI-DMK-02** | Kiểm tra modal Đổi mật khẩu | 1. Truy cập /admin/account<br>2. Nhấn nút Đổi mật khẩu<br>3. Kiểm tra modal | Hiển thị Dialog với tiêu đề "Đổi mật khẩu", mô tả "Nhập mật khẩu hiện tại và mật khẩu mới để thay đổi" | | Pass | 11/15/2015 | |
| **GUI-DMK-03** | Kiểm tra trường Mật khẩu hiện tại | 1. Truy cập /admin/account<br>2. Mở modal Đổi mật khẩu<br>3. Kiểm tra trường Mật khẩu hiện tại | Hiển thị label "Mật khẩu hiện tại", input type password, có nút icon Eye/EyeOff để hiển thị/ẩn mật khẩu ở bên phải | | Pass | 11/15/2015 | |
| **GUI-DMK-04** | Kiểm tra trường Mật khẩu mới | 1. Truy cập /admin/account<br>2. Mở modal Đổi mật khẩu<br>3. Kiểm tra trường Mật khẩu mới | Hiển thị label "Mật khẩu mới", input type password, có nút icon Eye/EyeOff để hiển thị/ẩn mật khẩu ở bên phải | | Pass | 11/15/2015 | |
| **GUI-DMK-05** | Kiểm tra trường Xác nhận mật khẩu mới | 1. Truy cập /admin/account<br>2. Mở modal Đổi mật khẩu<br>3. Kiểm tra trường Xác nhận mật khẩu | Hiển thị label "Xác nhận mật khẩu mới", input type password, có nút icon Eye/EyeOff để hiển thị/ẩn mật khẩu ở bên phải | | Pass | 11/15/2015 | |
| **GUI-DMK-06** | Kiểm tra nút Hủy | 1. Truy cập /admin/account<br>2. Mở modal Đổi mật khẩu<br>3. Kiểm tra nút Hủy | Hiển thị nút "Hủy" variant outline | | Pass | 11/15/2015 | |
| **GUI-DMK-07** | Kiểm tra nút Đổi mật khẩu trong modal | 1. Truy cập /admin/account<br>2. Mở modal Đổi mật khẩu<br>3. Kiểm tra nút Đổi mật khẩu | Hiển thị nút "Đổi mật khẩu" | | Pass | 11/15/2015 | |

---

### Check FUNC: Đổi mật khẩu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DMK-01** | Mở modal đổi mật khẩu | 1. Truy cập /admin/account<br>2. Nhấn nút "Đổi mật khẩu" | Hiển thị Dialog với tiêu đề "Đổi mật khẩu", mô tả, 3 trường nhập (Mật khẩu hiện tại, Mật khẩu mới, Xác nhận mật khẩu mới), nút Hủy, nút Đổi mật khẩu | | Pass | 11/15/2015 | |
| **FUNC-DMK-02** | Đổi mật khẩu thành công | 1. Truy cập /admin/account<br>2. Mở modal Đổi mật khẩu<br>3. Nhập mật khẩu hiện tại đúng<br>4. Nhập mật khẩu mới hợp lệ (≥6 ký tự)<br>5. Nhập xác nhận mật khẩu khớp<br>6. Nhấn "Đổi mật khẩu" | Hiển thị thông báo "Đổi mật khẩu thành công", modal đóng, form được reset | | Untested | 11/15/2015 | |
| **FUNC-DMK-03** | Đổi mật khẩu - Thiếu mật khẩu hiện tại | 1. Truy cập /admin/account<br>2. Mở modal Đổi mật khẩu<br>3. Để trống mật khẩu hiện tại<br>4. Nhập mật khẩu mới<br>5. Nhấn "Đổi mật khẩu" | Hiển thị thông báo lỗi "Vui lòng nhập mật khẩu hiện tại", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-DMK-04** | Đổi mật khẩu - Mật khẩu hiện tại sai | 1. Truy cập /admin/account<br>2. Mở modal Đổi mật khẩu<br>3. Nhập mật khẩu hiện tại sai<br>4. Nhập mật khẩu mới<br>5. Nhấn "Đổi mật khẩu" | Hiển thị thông báo lỗi "Mật khẩu hiện tại không đúng", form không được gửi | | Untested | 11/15/2015 | |
| **FUNC-DMK-05** | Đổi mật khẩu - Thiếu mật khẩu mới | 1. Truy cập /admin/account<br>2. Mở modal Đổi mật khẩu<br>3. Nhập mật khẩu hiện tại<br>4. Để trống mật khẩu mới<br>5. Nhấn "Đổi mật khẩu" | Hiển thị thông báo lỗi "Vui lòng nhập mật khẩu mới", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-DMK-06** | Đổi mật khẩu - Mật khẩu mới quá ngắn | 1. Truy cập /admin/account<br>2. Mở modal Đổi mật khẩu<br>3. Nhập mật khẩu hiện tại<br>4. Nhập mật khẩu mới < 6 ký tự<br>5. Nhấn "Đổi mật khẩu" | Hiển thị thông báo lỗi "Mật khẩu mới phải có ít nhất 6 ký tự", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-DMK-07** | Đổi mật khẩu - Mật khẩu xác nhận không khớp | 1. Truy cập /admin/account<br>2. Mở modal Đổi mật khẩu<br>3. Nhập mật khẩu hiện tại<br>4. Nhập mật khẩu mới<br>5. Nhập xác nhận mật khẩu khác<br>6. Nhấn "Đổi mật khẩu" | Hiển thị thông báo lỗi "Mật khẩu xác nhận không khớp", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-DMK-08** | Hiển thị/ẩn mật khẩu hiện tại | 1. Truy cập /admin/account<br>2. Mở modal Đổi mật khẩu<br>3. Nhập mật khẩu hiện tại<br>4. Click icon Eye | Input chuyển từ type password sang type text, hiển thị mật khẩu, icon chuyển thành EyeOff | | Pass | 11/15/2015 | |
| **FUNC-DMK-09** | Hiển thị/ẩn mật khẩu mới | 1. Truy cập /admin/account<br>2. Mở modal Đổi mật khẩu<br>3. Nhập mật khẩu mới<br>4. Click icon Eye | Input chuyển từ type password sang type text, hiển thị mật khẩu, icon chuyển thành EyeOff | | Pass | 11/15/2015 | |
| **FUNC-DMK-10** | Hiển thị/ẩn xác nhận mật khẩu | 1. Truy cập /admin/account<br>2. Mở modal Đổi mật khẩu<br>3. Nhập xác nhận mật khẩu<br>4. Click icon Eye | Input chuyển từ type password sang type text, hiển thị mật khẩu, icon chuyển thành EyeOff | | Pass | 11/15/2015 | |
| **FUNC-DMK-11** | Nhấn nút Hủy | 1. Truy cập /admin/account<br>2. Mở modal Đổi mật khẩu<br>3. Nhấn nút "Hủy" | Modal đóng, form được reset về trạng thái ban đầu | | Pass | 11/15/2015 | |
| **FUNC-DMK-12** | Đóng modal bằng cách click bên ngoài | 1. Truy cập /admin/account<br>2. Mở modal Đổi mật khẩu<br>3. Click bên ngoài modal | Modal đóng, form được reset | | Pass | 11/15/2015 | |
| **FUNC-DMK-13** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/account<br>2. Mở modal Đổi mật khẩu<br>3. Nhập đầy đủ thông tin<br>4. Tắt kết nối mạng<br>5. Nhấn "Đổi mật khẩu" | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", form không được gửi | | Untested | 11/15/2015 | |
| **FUNC-DMK-14** | Xử lý khi server lỗi | 1. Truy cập /admin/account<br>2. Mở modal Đổi mật khẩu<br>3. Nhập đầy đủ thông tin<br>4. Server trả về lỗi 500<br>5. Nhấn "Đổi mật khẩu" | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau", form không được gửi | | Untested | 11/15/2015 | |

---

### Function: Cập nhật thông tin cá nhân

#### Check GUI: Cập nhật thông tin cá nhân

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CTTCN-01** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/account<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Quản lý tài khoản" với kích thước text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-CTTCN-02** | Kiểm tra mô tả chức năng | 1. Truy cập /admin/account<br>2. Kiểm tra mô tả | Hiển thị mô tả "Quản lý thông tin cá nhân và cài đặt tài khoản" màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-CTTCN-03** | Kiểm tra nút Chỉnh sửa | 1. Truy cập /admin/account<br>2. Kiểm tra nút Chỉnh sửa | Hiển thị nút "Chỉnh sửa" với icon Edit ở header, chỉ hiển thị khi không ở chế độ chỉnh sửa | | Pass | 11/15/2015 | |
| **GUI-CTTCN-04** | Kiểm tra nút Lưu thay đổi | 1. Truy cập /admin/account<br>2. Nhấn Chỉnh sửa<br>3. Kiểm tra nút Lưu | Hiển thị nút "Lưu thay đổi" với icon Save ở header, chỉ hiển thị khi ở chế độ chỉnh sửa | | Pass | 11/15/2015 | |
| **GUI-CTTCN-05** | Kiểm tra nút Hủy | 1. Truy cập /admin/account<br>2. Nhấn Chỉnh sửa<br>3. Kiểm tra nút Hủy | Hiển thị nút "Hủy" với icon X variant outline ở header, chỉ hiển thị khi ở chế độ chỉnh sửa | | Pass | 11/15/2015 | |
| **GUI-CTTCN-06** | Kiểm tra card Thông tin cá nhân | 1. Truy cập /admin/account<br>2. Kiểm tra card | Hiển thị card "Thông tin cá nhân" với icon User, tiêu đề "Thông tin cá nhân", mô tả "Thông tin cơ bản của tài khoản quản trị" | | Pass | 11/15/2015 | |
| **GUI-CTTCN-07** | Kiểm tra Avatar | 1. Truy cập /admin/account<br>2. Kiểm tra Avatar | Hiển thị Avatar với kích thước h-20 w-20, có AvatarImage hoặc AvatarFallback hiển thị chữ cái đầu của họ tên | | Pass | 11/15/2015 | |
| **GUI-CTTCN-08** | Kiểm tra Badge Role | 1. Truy cập /admin/account<br>2. Kiểm tra Badge | Hiển thị Badge với icon Shield, text hiển thị role (VD: "Super Admin"), variant secondary | | Pass | 11/15/2015 | |
| **GUI-CTTCN-09** | Kiểm tra trường Họ và tên | 1. Truy cập /admin/account<br>2. Kiểm tra trường Họ và tên | Hiển thị label "Họ và tên", input type text, có thể disabled khi không ở chế độ chỉnh sửa | | Pass | 11/15/2015 | |
| **GUI-CTTCN-10** | Kiểm tra trường Email | 1. Truy cập /admin/account<br>2. Kiểm tra trường Email | Hiển thị label "Email", input type email, có thể disabled khi không ở chế độ chỉnh sửa | | Pass | 11/15/2015 | |
| **GUI-CTTCN-11** | Kiểm tra trường Số điện thoại | 1. Truy cập /admin/account<br>2. Kiểm tra trường Số điện thoại | Hiển thị label "Số điện thoại", input type text, có thể disabled khi không ở chế độ chỉnh sửa | | Pass | 11/15/2015 | |
| **GUI-CTTCN-12** | Kiểm tra trường Địa chỉ | 1. Truy cập /admin/account<br>2. Kiểm tra trường Địa chỉ | Hiển thị label "Địa chỉ", input type text, có thể disabled khi không ở chế độ chỉnh sửa | | Pass | 11/15/2015 | |
| **GUI-CTTCN-13** | Kiểm tra trường Ngày sinh | 1. Truy cập /admin/account<br>2. Kiểm tra trường Ngày sinh | Hiển thị label "Ngày sinh", input type date, có thể disabled khi không ở chế độ chỉnh sửa | | Pass | 11/15/2015 | |
| **GUI-CTTCN-14** | Kiểm tra card Thông tin tài khoản | 1. Truy cập /admin/account<br>2. Kiểm tra card | Hiển thị card "Thông tin tài khoản" với icon Shield, tiêu đề "Thông tin tài khoản", mô tả "Thông tin bảo mật và hoạt động tài khoản" | | Pass | 11/15/2015 | |
| **GUI-CTTCN-15** | Kiểm tra thông tin Email đăng nhập | 1. Truy cập /admin/account<br>2. Kiểm tra thông tin Email | Hiển thị icon Mail, label "Email đăng nhập", hiển thị email hiện tại màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-CTTCN-16** | Kiểm tra thông tin Ngày tạo tài khoản | 1. Truy cập /admin/account<br>2. Kiểm tra thông tin | Hiển thị icon Calendar, label "Ngày tạo tài khoản", hiển thị ngày tạo định dạng vi-VN | | Pass | 11/15/2015 | |
| **GUI-CTTCN-17** | Kiểm tra thông tin Lần đăng nhập cuối | 1. Truy cập /admin/account<br>2. Kiểm tra thông tin | Hiển thị icon Calendar, label "Lần đăng nhập cuối", hiển thị thời gian đăng nhập cuối định dạng vi-VN | | Pass | 11/15/2015 | |
| **GUI-CTTCN-18** | Kiểm tra Separator | 1. Truy cập /admin/account<br>2. Kiểm tra Separator | Hiển thị Separator giữa các phần thông tin trong card | | Pass | 11/15/2015 | |

---

### Check FUNC: Cập nhật thông tin cá nhân

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CTTCN-01** | Mở trang quản lý tài khoản | 1. Truy cập /admin/account | Hiển thị trang với tiêu đề "Quản lý tài khoản", mô tả, nút Chỉnh sửa, 2 card (Thông tin cá nhân, Thông tin tài khoản), các trường thông tin được điền sẵn, nút Đổi mật khẩu, nút Đăng xuất | | Pass | 11/15/2015 | |
| **FUNC-CTTCN-02** | Bật chế độ chỉnh sửa | 1. Truy cập /admin/account<br>2. Nhấn nút "Chỉnh sửa" | Các trường trong card "Thông tin cá nhân" (Họ tên, Email, SĐT, Địa chỉ, Ngày sinh) được kích hoạt (disabled=false), nút Chỉnh sửa biến mất, hiển thị nút "Lưu thay đổi" và nút "Hủy" | | Pass | 11/15/2015 | |
| **FUNC-CTTCN-03** | Cập nhật thông tin thành công | 1. Truy cập /admin/account<br>2. Nhấn Chỉnh sửa<br>3. Sửa thông tin (Họ tên, Email, SĐT, Địa chỉ, Ngày sinh)<br>4. Nhấn "Lưu thay đổi" | Hiển thị thông báo "Cập nhật thông tin thành công", các trường chuyển về chế độ disabled, nút Lưu và Hủy biến mất, nút Chỉnh sửa hiển thị lại, thông tin được cập nhật | | Untested | 11/15/2015 | |
| **FUNC-CTTCN-04** | Cập nhật - Thiếu Họ tên | 1. Truy cập /admin/account<br>2. Nhấn Chỉnh sửa<br>3. Xóa họ tên<br>4. Nhấn "Lưu thay đổi" | Hiển thị thông báo lỗi "Họ tên không được để trống", form không được gửi, vẫn ở chế độ chỉnh sửa | | Pass | 11/15/2015 | |
| **FUNC-CTTCN-05** | Cập nhật - Thiếu Email | 1. Truy cập /admin/account<br>2. Nhấn Chỉnh sửa<br>3. Xóa email<br>4. Nhấn "Lưu thay đổi" | Hiển thị thông báo lỗi "Email không được để trống", form không được gửi, vẫn ở chế độ chỉnh sửa | | Pass | 11/15/2015 | |
| **FUNC-CTTCN-06** | Cập nhật - Thiếu Số điện thoại | 1. Truy cập /admin/account<br>2. Nhấn Chỉnh sửa<br>3. Xóa số điện thoại<br>4. Nhấn "Lưu thay đổi" | Hiển thị thông báo lỗi "Số điện thoại không được để trống", form không được gửi, vẫn ở chế độ chỉnh sửa | | Pass | 11/15/2015 | |
| **FUNC-CTTCN-07** | Cập nhật - Email không hợp lệ | 1. Truy cập /admin/account<br>2. Nhấn Chỉnh sửa<br>3. Nhập email không đúng định dạng<br>4. Nhấn "Lưu thay đổi" | Trình duyệt hiển thị cảnh báo validation hoặc thông báo lỗi "Email không hợp lệ", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-CTTCN-08** | Hủy chỉnh sửa | 1. Truy cập /admin/account<br>2. Nhấn Chỉnh sửa<br>3. Sửa thông tin<br>4. Nhấn "Hủy" | Các trường được reset về giá trị ban đầu, chuyển về chế độ xem (disabled=true), nút Lưu và Hủy biến mất, nút Chỉnh sửa hiển thị lại | | Pass | 11/15/2015 | |
| **FUNC-CTTCN-09** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/account<br>2. Nhấn Chỉnh sửa<br>3. Sửa thông tin<br>4. Tắt kết nối mạng<br>5. Nhấn "Lưu thay đổi" | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", form không được gửi | | Untested | 11/15/2015 | |
| **FUNC-CTTCN-10** | Xử lý khi server lỗi | 1. Truy cập /admin/account<br>2. Nhấn Chỉnh sửa<br>3. Sửa thông tin<br>4. Server trả về lỗi 500<br>5. Nhấn "Lưu thay đổi" | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau", form không được gửi | | Untested | 11/15/2015 | |

---

### Function: Đăng xuất

#### Check GUI: Đăng xuất

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DX-01** | Kiểm tra nút Đăng xuất | 1. Truy cập /admin/account<br>2. Kiểm tra nút Đăng xuất | Hiển thị nút "Đăng xuất" với icon LogOut trong card "Thông tin tài khoản", variant destructive, chiếm toàn bộ chiều rộng | | Pass | 11/15/2015 | |
| **GUI-DX-02** | Kiểm tra AlertDialog xác nhận | 1. Truy cập /admin/account<br>2. Nhấn nút Đăng xuất<br>3. Kiểm tra dialog | Hiển thị AlertDialog với tiêu đề "Xác nhận đăng xuất", mô tả "Bạn có chắc chắn muốn đăng xuất khỏi hệ thống? Bạn sẽ cần đăng nhập lại để tiếp tục sử dụng.", nút "Hủy" và nút "Đăng xuất" | | Pass | 11/15/2015 | |

---

### Check FUNC: Đăng xuất

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DX-01** | Mở dialog xác nhận đăng xuất | 1. Truy cập /admin/account<br>2. Nhấn nút "Đăng xuất" | Hiển thị AlertDialog với tiêu đề "Xác nhận đăng xuất", mô tả, nút "Hủy" (AlertDialogCancel), nút "Đăng xuất" (AlertDialogAction) | | Pass | 11/15/2015 | |
| **FUNC-DX-02** | Đăng xuất thành công | 1. Truy cập /admin/account<br>2. Nhấn nút "Đăng xuất"<br>3. Nhấn "Đăng xuất" trong dialog | Hiển thị thông báo "Đăng xuất thành công", chuyển đến trang /admin/auth/login, token và session bị xóa | | Untested | 11/15/2015 | |
| **FUNC-DX-03** | Hủy đăng xuất | 1. Truy cập /admin/account<br>2. Nhấn nút "Đăng xuất"<br>3. Nhấn "Hủy" trong dialog | Dialog đóng, vẫn ở trang /admin/account, không đăng xuất | | Pass | 11/15/2015 | |
| **FUNC-DX-04** | Đóng dialog bằng cách click bên ngoài | 1. Truy cập /admin/account<br>2. Nhấn nút "Đăng xuất"<br>3. Click bên ngoài dialog | Dialog đóng, vẫn ở trang /admin/account, không đăng xuất | | Pass | 11/15/2015 | |
| **FUNC-DX-05** | Kiểm tra xóa token sau đăng xuất | 1. Truy cập /admin/account<br>2. Đăng xuất thành công<br>3. Kiểm tra localStorage/sessionStorage | Token bị xóa khỏi localStorage/sessionStorage | | Untested | 11/15/2015 | |
| **FUNC-DX-06** | Kiểm tra xóa session sau đăng xuất | 1. Truy cập /admin/account<br>2. Đăng xuất thành công<br>3. Kiểm tra session | Session bị xóa trên server | | Untested | 11/15/2015 | |
| **FUNC-DX-07** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/account<br>2. Nhấn nút "Đăng xuất"<br>3. Tắt kết nối mạng<br>4. Nhấn "Đăng xuất" trong dialog | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", có thể vẫn đăng xuất ở phía client | | Untested | 11/15/2015 | |
| **FUNC-DX-08** | Xử lý khi server lỗi | 1. Truy cập /admin/account<br>2. Nhấn nút "Đăng xuất"<br>3. Server trả về lỗi 500<br>4. Nhấn "Đăng xuất" trong dialog | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau", có thể vẫn đăng xuất ở phía client | | Untested | 11/15/2015 | |

---

**Người tạo:** Testing Team  
**Ngày cập nhật:** 11/15/2015  
**Phiên bản:** 1.0

