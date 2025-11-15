# Test Case Template - Đăng nhập (Admin)

## Module Code
**Model Management Store: Quản lý tài khoản Admin**

## Test Requirement
1. Đăng nhập
2. Khôi phục mật khẩu
3. Đổi mật khẩu
4. Quản lý thông tin cá nhân
5. Đăng xuất

---

## Test Summary

### Người thực hiện Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 20 |
| **Fail** | 0 |
| **Untested** | 18 |
| **N/A** | 0 |
| **Number of Test cases** | 38 |

---

## Test Cases

### Function: Đăng nhập

#### Check GUI: Đăng nhập

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DN-01** | Kiểm tra biểu tượng Shield header | 1. Truy cập /admin/auth/login<br>2. Kiểm tra biểu tượng Shield | Hiển thị biểu tượng Shield trong vùng header, nằm trong vòng tròn | | Pass | | |
| **GUI-DN-02** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/auth/login<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Đăng nhập Admin" | | Pass | | |
| **GUI-DN-03** | Kiểm tra mô tả chức năng | 1. Truy cập /admin/auth/login<br>2. Kiểm tra mô tả | Hiển thị mô tả "Đăng nhập vào hệ thống quản trị" | | Pass | | |
| **GUI-DN-04** | Kiểm tra trường Email | 1. Truy cập /admin/auth/login<br>2. Kiểm tra label và input Email | Hiển thị label "Email Admin", input type email với placeholder "admin@modelshop.com", có thuộc tính required | | Pass | | |
| **GUI-DN-05** | Kiểm tra trường Mật khẩu | 1. Truy cập /admin/auth/login<br>2. Kiểm tra label và input Mật khẩu | Hiển thị label "Mật khẩu", input type password với placeholder "Nhập mật khẩu", có thuộc tính required | | Pass | | |
| **GUI-DN-06** | Kiểm tra checkbox Ghi nhớ | 1. Truy cập /admin/auth/login<br>2. Kiểm tra checkbox | Hiển thị checkbox với label "Ghi nhớ đăng nhập" có thể tích chọn, nằm bên trái | | Pass | | |
| **GUI-DN-07** | Kiểm tra link Quên mật khẩu | 1. Truy cập /admin/auth/login<br>2. Kiểm tra link Quên mật khẩu | Hiển thị link "Quên mật khẩu?" có thể click, nằm bên phải | | Pass | | |
| **GUI-DN-08** | Kiểm tra nút Đăng nhập | 1. Truy cập /admin/auth/login<br>2. Kiểm tra nút Đăng nhập | Hiển thị nút "Đăng nhập Admin" type submit, chiếm toàn bộ chiều rộng form | | Pass | | |
| **GUI-DN-09** | Kiểm tra separator "Hoặc" | 1. Truy cập /admin/auth/login<br>2. Kiểm tra separator | Hiển thị separator với text "Hoặc" ở giữa, chữ in hoa | | Pass | | |
| **GUI-DN-10** | Kiểm tra link chuyển sang User | 1. Truy cập /admin/auth/login<br>2. Kiểm tra link chuyển User | Hiển thị link "Đăng nhập với tài khoản khách hàng" với icon ArrowLeft bên trái, có thể click | | Pass | | |
| **GUI-DN-11** | Kiểm tra thông báo quyền truy cập | 1. Truy cập /admin/auth/login<br>2. Kiểm tra thông báo cuối trang | Hiển thị text "Chỉ dành cho quản trị viên được ủy quyền" ở cuối trang, căn giữa | | Pass | | |
| **GUI-DN-12** | Kiểm tra layout trang | 1. Truy cập /admin/auth/login<br>2. Kiểm tra layout tổng thể | Trang có background, card container nằm giữa màn hình, form đăng nhập bên trong card | | Pass | | |
| **GUI-DN-13** | Kiểm tra card container | 1. Truy cập /admin/auth/login<br>2. Kiểm tra card | Hiển thị card container chứa toàn bộ form đăng nhập, có giới hạn chiều rộng tối đa | | Pass | | |

---

### Check FUNC: Đăng nhập

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DN-01** | Mở trang đăng nhập | 1. Truy cập /admin/auth/login | Hiển thị form đăng nhập với đầy đủ các thành phần: biểu tượng Shield, tiêu đề "Đăng nhập Admin", mô tả "Đăng nhập vào hệ thống quản trị", 2 trường nhập (Email Admin, Mật khẩu), checkbox ghi nhớ, link quên mật khẩu, nút đăng nhập, separator "Hoặc", link chuyển User | | Pass | | |
| **FUNC-DN-02** | Đăng nhập thành công với thông tin hợp lệ | 1. Truy cập /admin/auth/login<br>2. Nhập email hợp lệ (VD: admin@modelshop.com)<br>3. Nhập mật khẩu đúng<br>4. Nhấn nút Đăng nhập | Hệ thống xác thực thông tin, chuyển đến trang dashboard admin (/admin), lưu phiên đăng nhập và lưu token, hiển thị thông báo thành công | | Untested | | |
| **FUNC-DN-03** | Đăng nhập với email không tồn tại | 1. Truy cập /admin/auth/login<br>2. Nhập email không tồn tại (VD: notexist@test.com)<br>3. Nhập mật khẩu bất kỳ<br>4. Nhấn Đăng nhập | Hiển thị thông báo lỗi "Email hoặc mật khẩu không đúng", không chuyển trang, vẫn ở trang đăng nhập | | Untested | | |
| **FUNC-DN-04** | Đăng nhập với mật khẩu sai | 1. Truy cập /admin/auth/login<br>2. Nhập email hợp lệ<br>3. Nhập mật khẩu sai<br>4. Nhấn Đăng nhập | Hiển thị thông báo lỗi "Email hoặc mật khẩu không đúng", không chuyển trang, vẫn ở trang đăng nhập | | Untested | | |
| **FUNC-DN-05** | Đăng nhập thiếu email | 1. Truy cập /admin/auth/login<br>2. Để trống email<br>3. Nhập mật khẩu<br>4. Nhấn Đăng nhập | Trình duyệt hiển thị cảnh báo "Please fill out this field" hoặc validation message, form không được gửi | | Pass | | |
| **FUNC-DN-06** | Đăng nhập thiếu mật khẩu | 1. Truy cập /admin/auth/login<br>2. Nhập email<br>3. Để trống mật khẩu<br>4. Nhấn Đăng nhập | Trình duyệt hiển thị cảnh báo "Please fill out this field" hoặc validation message, form không được gửi | | Pass | | |
| **FUNC-DN-07** | Đăng nhập với email sai định dạng | 1. Truy cập /admin/auth/login<br>2. Nhập email không đúng định dạng (VD: "invalid-email")<br>3. Nhập mật khẩu<br>4. Nhấn Đăng nhập | Trình duyệt hiển thị cảnh báo "Please include an '@' in the email address" hoặc validation message, form không được gửi | | Pass | | |
| **FUNC-DN-08** | Đăng nhập với email không có @ | 1. Truy cập /admin/auth/login<br>2. Nhập email thiếu ký tự @ (VD: "adminmodelshop.com")<br>3. Nhập mật khẩu<br>4. Nhấn Đăng nhập | Trình duyệt hiển thị cảnh báo validation, form không được gửi | | Pass | | |
| **FUNC-DN-09** | Đăng nhập với email thiếu domain | 1. Truy cập /admin/auth/login<br>2. Nhập email thiếu domain (VD: "admin@")<br>3. Nhập mật khẩu<br>4. Nhấn Đăng nhập | Trình duyệt hiển thị cảnh báo validation, form không được gửi | | Pass | | |
| **FUNC-DN-10** | Chức năng ghi nhớ - Có tích chọn | 1. Truy cập /admin/auth/login<br>2. Tích checkbox "Ghi nhớ đăng nhập"<br>3. Nhập thông tin hợp lệ<br>4. Đăng nhập thành công | Đăng nhập thành công, trình duyệt lưu cookie/session với thời hạn dài hơn, khi đóng trình duyệt và mở lại vẫn còn đăng nhập | | Untested | | |
| **FUNC-DN-11** | Chức năng ghi nhớ - Không tích chọn | 1. Truy cập /admin/auth/login<br>2. Không tích checkbox<br>3. Nhập thông tin hợp lệ<br>4. Đăng nhập thành công | Đăng nhập thành công, trình duyệt lưu cookie/session với thời hạn ngắn hơn, khi đóng trình duyệt sẽ đăng xuất | | Untested | | |
| **FUNC-DN-12** | Nhấn link Quên mật khẩu | 1. Truy cập /admin/auth/login<br>2. Nhấn link "Quên mật khẩu?" | Chuyển đến trang /admin/auth/forgot-password | | Pass | | |
| **FUNC-DN-13** | Nhấn link chuyển sang User | 1. Truy cập /admin/auth/login<br>2. Nhấn link "Đăng nhập với tài khoản khách hàng" | Chuyển đến trang /user/auth/login | | Pass | | |
| **FUNC-DN-14** | Submit form bằng phím Enter | 1. Truy cập /admin/auth/login<br>2. Nhập thông tin hợp lệ<br>3. Nhấn Enter trong trường mật khẩu | Form được gửi, xử lý đăng nhập như khi nhấn nút Đăng nhập | | Untested | | |
| **FUNC-DN-15** | Đăng nhập với tài khoản chưa kích hoạt | 1. Truy cập /admin/auth/login<br>2. Nhập email tài khoản chưa kích hoạt<br>3. Nhập mật khẩu đúng<br>4. Nhấn Đăng nhập | Hiển thị thông báo lỗi "Tài khoản chưa được kích hoạt. Vui lòng kiểm tra email để kích hoạt tài khoản", không chuyển trang | | Untested | | |
| **FUNC-DN-16** | Đăng nhập với tài khoản bị khóa | 1. Truy cập /admin/auth/login<br>2. Nhập email tài khoản bị khóa<br>3. Nhập mật khẩu đúng<br>4. Nhấn Đăng nhập | Hiển thị thông báo lỗi "Tài khoản đã bị khóa. Vui lòng liên hệ quản trị viên", không chuyển trang | | Untested | | |
| **FUNC-DN-17** | Đăng nhập sai nhiều lần - Hiển thị Captcha | 1. Truy cập /admin/auth/login<br>2. Nhập sai thông tin đăng nhập 3 lần liên tiếp<br>3. Lần thứ 4, nhập thông tin | Sau 3 lần đăng nhập sai, hiển thị captcha, yêu cầu nhập captcha trước khi tiếp tục đăng nhập | | Untested | | |
| **FUNC-DN-18** | Đăng nhập với captcha đúng | 1. Truy cập /admin/auth/login<br>2. Đăng nhập sai 3 lần để hiển thị captcha<br>3. Nhập captcha đúng<br>4. Nhập thông tin đăng nhập đúng<br>5. Nhấn Đăng nhập | Xác thực captcha thành công, xử lý đăng nhập bình thường, chuyển đến trang dashboard | | Untested | | |
| **FUNC-DN-19** | Đăng nhập với captcha sai | 1. Truy cập /admin/auth/login<br>2. Đăng nhập sai 3 lần để hiển thị captcha<br>3. Nhập captcha sai<br>4. Nhập thông tin đăng nhập đúng<br>5. Nhấn Đăng nhập | Hiển thị thông báo lỗi "Captcha không đúng", không xử lý đăng nhập | | Untested | | |
| **FUNC-DN-20** | Tạm khóa tài khoản sau nhiều lần đăng nhập sai | 1. Truy cập /admin/auth/login<br>2. Đăng nhập sai quá số lần cho phép (VD: 5 lần)<br>3. Thử đăng nhập lại | Tài khoản bị tạm khóa trong một khoảng thời gian (VD: 15 phút), hiển thị thông báo "Tài khoản đã bị tạm khóa do đăng nhập sai nhiều lần. Vui lòng thử lại sau X phút" | | Untested | | |
| **FUNC-DN-21** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/auth/login<br>2. Tắt kết nối mạng<br>3. Nhập thông tin hợp lệ<br>4. Nhấn Đăng nhập | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", không chuyển trang | | Untested | | |
| **FUNC-DN-22** | Xử lý khi server lỗi | 1. Truy cập /admin/auth/login<br>2. Nhập thông tin hợp lệ<br>3. Server trả về lỗi 500<br>4. Nhấn Đăng nhập | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau", không chuyển trang | | Untested | | |
| **FUNC-DN-23** | Kiểm tra redirect sau đăng nhập | 1. Truy cập /admin/auth/login?redirect=/admin/orders<br>2. Nhập thông tin hợp lệ<br>3. Đăng nhập thành công | Sau khi đăng nhập thành công, chuyển đến trang /admin/orders thay vì dashboard mặc định | | Untested | | |
| **FUNC-DN-24** | Kiểm tra lưu token sau đăng nhập | 1. Truy cập /admin/auth/login<br>2. Nhập thông tin hợp lệ<br>3. Đăng nhập thành công<br>4. Kiểm tra localStorage/sessionStorage | Token được lưu vào localStorage hoặc sessionStorage, có thể sử dụng cho các request tiếp theo | | Untested | | |
| **FUNC-DN-25** | Kiểm tra tạo phiên đăng nhập | 1. Truy cập /admin/auth/login<br>2. Nhập thông tin hợp lệ<br>3. Đăng nhập thành công<br>4. Kiểm tra session | Phiên đăng nhập được tạo và lưu trữ trên server, có thể theo dõi trong lịch sử đăng nhập | | Untested | | |

---

*Template này được tạo theo chuẩn Markdown để dễ dàng quản lý và cập nhật test cases.*

