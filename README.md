# Test Case Template - Quản lý tài khoản (Admin)

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
| **Pass** | 94 |
| **Fail** | 0 |
| **Untested** | 31 |
| **N/A** | 0 |
| **Number of Test cases** | 125 |

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

### Function: Khôi phục mật khẩu

#### Check GUI: Khôi phục mật khẩu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-KPMK-01** | Kiểm tra biểu tượng Shield header | 1. Truy cập /admin/auth/forgot-password<br>2. Kiểm tra biểu tượng Shield | Hiển thị biểu tượng Shield trong vòng tròn ở header | | Pass | | |
| **GUI-KPMK-02** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/auth/forgot-password<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Khôi phục mật khẩu" | | Pass | | |
| **GUI-KPMK-03** | Kiểm tra mô tả chức năng | 1. Truy cập /admin/auth/forgot-password<br>2. Kiểm tra mô tả | Hiển thị mô tả "Chọn phương thức khôi phục mật khẩu của bạn" | | Pass | | |
| **GUI-KPMK-04** | Kiểm tra phương thức Email | 1. Truy cập /admin/auth/forgot-password<br>2. Kiểm tra phương thức Email | Hiển thị radio button "Email" với mô tả "Gửi mã xác thực qua email", có icon Mail | | Pass | | |
| **GUI-KPMK-05** | Kiểm tra phương thức SMS | 1. Truy cập /admin/auth/forgot-password<br>2. Kiểm tra phương thức SMS | Hiển thị radio button "SMS" với mô tả "Gửi mã xác thực qua SMS", có icon Phone | | Pass | | |
| **GUI-KPMK-06** | Kiểm tra phương thức Câu hỏi bảo mật | 1. Truy cập /admin/auth/forgot-password<br>2. Kiểm tra phương thức Câu hỏi bảo mật | Hiển thị radio button "Câu hỏi bảo mật" với mô tả "Trả lời câu hỏi bảo mật", có icon MessageSquare | | Pass | | |
| **GUI-KPMK-07** | Kiểm tra trường nhập Email | 1. Truy cập /admin/auth/forgot-password<br>2. Chọn phương thức Email<br>3. Kiểm tra trường nhập | Hiển thị label "Email", input type email với placeholder "Nhập email của bạn" | | Pass | | |
| **GUI-KPMK-08** | Kiểm tra trường nhập Số điện thoại | 1. Truy cập /admin/auth/forgot-password<br>2. Chọn phương thức SMS<br>3. Kiểm tra trường nhập | Hiển thị label "Số điện thoại", input type tel với placeholder "Nhập số điện thoại của bạn" | | Pass | | |
| **GUI-KPMK-09** | Kiểm tra câu hỏi bảo mật | 1. Truy cập /admin/auth/forgot-password<br>2. Chọn phương thức Câu hỏi bảo mật<br>3. Kiểm tra câu hỏi | Hiển thị 3 câu hỏi bảo mật với các input để nhập câu trả lời | | Pass | | |
| **GUI-KPMK-10** | Kiểm tra nút Tiếp tục | 1. Truy cập /admin/auth/forgot-password<br>2. Kiểm tra nút Tiếp tục | Hiển thị nút "Tiếp tục" với icon Key, chiếm toàn bộ chiều rộng | | Pass | | |
| **GUI-KPMK-11** | Kiểm tra bước nhập mã xác thực | 1. Truy cập /admin/auth/forgot-password<br>2. Chọn phương thức và nhập thông tin<br>3. Nhấn Tiếp tục<br>4. Kiểm tra bước 2 | Hiển thị alert thông báo mã đã gửi, trường nhập "Mã xác thực" với placeholder "Nhập mã xác thực 6 chữ số", nút "Xác thực" với icon CheckCircle | | Pass | | |
| **GUI-KPMK-12** | Kiểm tra bước đặt mật khẩu mới | 1. Truy cập /admin/auth/forgot-password<br>2. Hoàn thành bước xác thực<br>3. Kiểm tra bước 3 | Hiển thị alert xác nhận, trường "Mật khẩu mới", trường "Xác nhận mật khẩu", progress bar độ mạnh mật khẩu, danh sách yêu cầu mật khẩu, nút "Đặt lại mật khẩu" | | Pass | | |
| **GUI-KPMK-13** | Kiểm tra bước hoàn thành | 1. Truy cập /admin/auth/forgot-password<br>2. Hoàn thành đặt mật khẩu mới<br>3. Kiểm tra bước 4 | Hiển thị icon CheckCircle trong vòng tròn xanh, tiêu đề "Khôi phục mật khẩu thành công", mô tả, nút "Đăng nhập ngay", nút "Quay về trang chủ" | | Pass | | |
| **GUI-KPMK-14** | Kiểm tra link Đăng nhập | 1. Truy cập /admin/auth/forgot-password<br>2. Kiểm tra link cuối trang | Hiển thị text "Bạn có tài khoản?" với link "Đăng nhập" | | Pass | | |

---

### Check FUNC: Khôi phục mật khẩu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-KPMK-01** | Mở trang khôi phục mật khẩu | 1. Truy cập /admin/auth/forgot-password | Hiển thị trang khôi phục mật khẩu với biểu tượng Shield, tiêu đề, mô tả, 3 phương thức khôi phục (Email, SMS, Câu hỏi bảo mật) | | Pass | | |
| **FUNC-KPMK-02** | Chọn phương thức Email | 1. Truy cập /admin/auth/forgot-password<br>2. Click vào phương thức Email | Radio button Email được chọn, hiển thị trường nhập Email | | Pass | | |
| **FUNC-KPMK-03** | Chọn phương thức SMS | 1. Truy cập /admin/auth/forgot-password<br>2. Click vào phương thức SMS | Radio button SMS được chọn, hiển thị trường nhập Số điện thoại | | Pass | | |
| **FUNC-KPMK-04** | Chọn phương thức Câu hỏi bảo mật | 1. Truy cập /admin/auth/forgot-password<br>2. Click vào phương thức Câu hỏi bảo mật | Radio button Câu hỏi bảo mật được chọn, hiển thị 3 câu hỏi bảo mật với các trường nhập | | Pass | | |
| **FUNC-KPMK-05** | Gửi mã xác thực qua Email - Thành công | 1. Truy cập /admin/auth/forgot-password<br>2. Chọn Email<br>3. Nhập email hợp lệ<br>4. Nhấn Tiếp tục | Hiển thị thông báo "Mã xác thực đã được gửi", chuyển sang bước 2 (nhập mã xác thực) | | Untested | | |
| **FUNC-KPMK-06** | Gửi mã xác thực qua Email - Email không tồn tại | 1. Truy cập /admin/auth/forgot-password<br>2. Chọn Email<br>3. Nhập email không tồn tại<br>4. Nhấn Tiếp tục | Hiển thị thông báo lỗi "Email không tồn tại trong hệ thống" | | Untested | | |
| **FUNC-KPMK-07** | Gửi mã xác thực - Thiếu email | 1. Truy cập /admin/auth/forgot-password<br>2. Chọn Email<br>3. Để trống email<br>4. Nhấn Tiếp tục | Hiển thị thông báo lỗi "Vui lòng nhập email" | | Pass | | |
| **FUNC-KPMK-08** | Xác thực mã OTP - Thành công | 1. Truy cập /admin/auth/forgot-password<br>2. Gửi mã xác thực thành công<br>3. Nhập mã OTP đúng<br>4. Nhấn Xác thực | Hiển thị thông báo "Mã xác thực hợp lệ", chuyển sang bước 3 (đặt mật khẩu mới) | | Untested | | |
| **FUNC-KPMK-09** | Xác thực mã OTP - Mã sai | 1. Truy cập /admin/auth/forgot-password<br>2. Gửi mã xác thực thành công<br>3. Nhập mã OTP sai<br>4. Nhấn Xác thực | Hiển thị thông báo lỗi "Mã xác thực không đúng" | | Untested | | |
| **FUNC-KPMK-10** | Xác thực mã OTP - Mã hết hạn | 1. Truy cập /admin/auth/forgot-password<br>2. Gửi mã xác thực<br>3. Đợi mã hết hạn<br>4. Nhập mã OTP<br>5. Nhấn Xác thực | Hiển thị thông báo lỗi "Mã xác thực đã hết hạn. Vui lòng yêu cầu mã mới" | | Untested | | |
| **FUNC-KPMK-11** | Trả lời câu hỏi bảo mật - Thành công | 1. Truy cập /admin/auth/forgot-password<br>2. Chọn Câu hỏi bảo mật<br>3. Nhập đúng câu trả lời cho 3 câu hỏi<br>4. Nhấn Tiếp tục | Hiển thị thông báo "Xác thực thành công", chuyển sang bước 3 (đặt mật khẩu mới) | | Untested | | |
| **FUNC-KPMK-12** | Trả lời câu hỏi bảo mật - Sai câu trả lời | 1. Truy cập /admin/auth/forgot-password<br>2. Chọn Câu hỏi bảo mật<br>3. Nhập sai câu trả lời<br>4. Nhấn Tiếp tục | Hiển thị thông báo lỗi "Câu trả lời không đúng" | | Untested | | |
| **FUNC-KPMK-13** | Trả lời câu hỏi bảo mật - Thiếu câu trả lời | 1. Truy cập /admin/auth/forgot-password<br>2. Chọn Câu hỏi bảo mật<br>3. Để trống một hoặc nhiều câu trả lời<br>4. Nhấn Tiếp tục | Hiển thị thông báo lỗi "Vui lòng trả lời đầy đủ các câu hỏi bảo mật" | | Pass | | |
| **FUNC-KPMK-14** | Đặt mật khẩu mới - Thành công | 1. Truy cập /admin/auth/forgot-password<br>2. Hoàn thành xác thực<br>3. Nhập mật khẩu mới hợp lệ (≥8 ký tự, có chữ hoa, số)<br>4. Nhập lại mật khẩu khớp<br>5. Nhấn Đặt lại mật khẩu | Hiển thị thông báo "Mật khẩu đã được đặt lại thành công", chuyển sang bước 4 (hoàn thành) | | Untested | | |
| **FUNC-KPMK-15** | Đặt mật khẩu mới - Mật khẩu quá ngắn | 1. Truy cập /admin/auth/forgot-password<br>2. Hoàn thành xác thực<br>3. Nhập mật khẩu < 8 ký tự<br>4. Nhấn Đặt lại mật khẩu | Hiển thị thông báo lỗi "Mật khẩu phải có ít nhất 8 ký tự" | | Pass | | |
| **FUNC-KPMK-16** | Đặt mật khẩu mới - Mật khẩu không khớp | 1. Truy cập /admin/auth/forgot-password<br>2. Hoàn thành xác thực<br>3. Nhập mật khẩu mới<br>4. Nhập xác nhận mật khẩu khác<br>5. Nhấn Đặt lại mật khẩu | Hiển thị alert "Mật khẩu xác nhận không khớp", nút Đặt lại mật khẩu bị disable | | Pass | | |
| **FUNC-KPMK-17** | Kiểm tra độ mạnh mật khẩu | 1. Truy cập /admin/auth/forgot-password<br>2. Hoàn thành xác thực<br>3. Nhập mật khẩu mới<br>4. Quan sát progress bar | Progress bar hiển thị độ mạnh mật khẩu (Yếu/Trung bình/Mạnh) với màu tương ứng, danh sách yêu cầu hiển thị trạng thái từng điều kiện | | Pass | | |
| **FUNC-KPMK-18** | Quay lại bước trước | 1. Truy cập /admin/auth/forgot-password<br>2. Đến bước 2 hoặc 3<br>3. Nhấn nút Quay lại | Quay lại bước trước đó, giữ nguyên thông tin đã nhập | | Pass | | |
| **FUNC-KPMK-19** | Nhấn nút Đăng nhập ngay | 1. Truy cập /admin/auth/forgot-password<br>2. Hoàn thành khôi phục mật khẩu<br>3. Nhấn "Đăng nhập ngay" | Chuyển đến trang /admin/auth/login | | Pass | | |
| **FUNC-KPMK-20** | Nhấn link Đăng nhập ở cuối trang | 1. Truy cập /admin/auth/forgot-password<br>2. Nhấn link "Đăng nhập" ở cuối trang | Chuyển đến trang /admin/auth/login | | Pass | | |

---

### Function: Đổi mật khẩu

#### Check GUI: Đổi mật khẩu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DMK-01** | Kiểm tra nút Đổi mật khẩu | 1. Truy cập /admin/account<br>2. Kiểm tra nút Đổi mật khẩu | Hiển thị nút "Đổi mật khẩu" với icon Key trong card "Thông tin tài khoản" | | Pass | | |
| **GUI-DMK-02** | Kiểm tra modal Đổi mật khẩu | 1. Truy cập /admin/account<br>2. Nhấn nút Đổi mật khẩu<br>3. Kiểm tra modal | Hiển thị modal với tiêu đề "Đổi mật khẩu", mô tả "Nhập mật khẩu hiện tại và mật khẩu mới để thay đổi" | | Pass | | |
| **GUI-DMK-03** | Kiểm tra trường Mật khẩu hiện tại | 1. Truy cập /admin/account<br>2. Mở modal Đổi mật khẩu<br>3. Kiểm tra trường Mật khẩu hiện tại | Hiển thị label "Mật khẩu hiện tại", input type password, có nút icon Eye/EyeOff để hiển thị/ẩn mật khẩu | | Pass | | |
| **GUI-DMK-04** | Kiểm tra trường Mật khẩu mới | 1. Truy cập /admin/account<br>2. Mở modal Đổi mật khẩu<br>3. Kiểm tra trường Mật khẩu mới | Hiển thị label "Mật khẩu mới", input type password, có nút icon Eye/EyeOff để hiển thị/ẩn mật khẩu | | Pass | | |
| **GUI-DMK-05** | Kiểm tra trường Xác nhận mật khẩu mới | 1. Truy cập /admin/account<br>2. Mở modal Đổi mật khẩu<br>3. Kiểm tra trường Xác nhận mật khẩu | Hiển thị label "Xác nhận mật khẩu mới", input type password, có nút icon Eye/EyeOff để hiển thị/ẩn mật khẩu | | Pass | | |
| **GUI-DMK-06** | Kiểm tra nút Hủy | 1. Truy cập /admin/account<br>2. Mở modal Đổi mật khẩu<br>3. Kiểm tra nút Hủy | Hiển thị nút "Hủy" variant outline | | Pass | | |
| **GUI-DMK-07** | Kiểm tra nút Đổi mật khẩu trong modal | 1. Truy cập /admin/account<br>2. Mở modal Đổi mật khẩu<br>3. Kiểm tra nút Đổi mật khẩu | Hiển thị nút "Đổi mật khẩu" | | Pass | | |

---

### Check FUNC: Đổi mật khẩu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DMK-01** | Mở modal Đổi mật khẩu | 1. Truy cập /admin/account<br>2. Nhấn nút "Đổi mật khẩu" | Modal Đổi mật khẩu mở ra, hiển thị 3 trường nhập (Mật khẩu hiện tại, Mật khẩu mới, Xác nhận mật khẩu mới), 2 nút (Hủy, Đổi mật khẩu) | | Pass | | |
| **FUNC-DMK-02** | Đổi mật khẩu thành công | 1. Truy cập /admin/account<br>2. Mở modal Đổi mật khẩu<br>3. Nhập mật khẩu hiện tại đúng<br>4. Nhập mật khẩu mới hợp lệ (≥6 ký tự)<br>5. Nhập lại mật khẩu mới khớp<br>6. Nhấn Đổi mật khẩu | Hiển thị thông báo "Đổi mật khẩu thành công", modal đóng, form được reset | | Untested | | |
| **FUNC-DMK-03** | Đổi mật khẩu - Mật khẩu hiện tại sai | 1. Truy cập /admin/account<br>2. Mở modal Đổi mật khẩu<br>3. Nhập mật khẩu hiện tại sai<br>4. Nhập mật khẩu mới<br>5. Nhấn Đổi mật khẩu | Hiển thị thông báo lỗi "Mật khẩu hiện tại không đúng", không đổi mật khẩu | | Untested | | |
| **FUNC-DMK-04** | Đổi mật khẩu - Thiếu mật khẩu hiện tại | 1. Truy cập /admin/account<br>2. Mở modal Đổi mật khẩu<br>3. Để trống mật khẩu hiện tại<br>4. Nhập mật khẩu mới<br>5. Nhấn Đổi mật khẩu | Hiển thị thông báo lỗi "Vui lòng nhập mật khẩu hiện tại" | | Pass | | |
| **FUNC-DMK-05** | Đổi mật khẩu - Thiếu mật khẩu mới | 1. Truy cập /admin/account<br>2. Mở modal Đổi mật khẩu<br>3. Nhập mật khẩu hiện tại<br>4. Để trống mật khẩu mới<br>5. Nhấn Đổi mật khẩu | Hiển thị thông báo lỗi "Vui lòng nhập mật khẩu mới" | | Pass | | |
| **FUNC-DMK-06** | Đổi mật khẩu - Mật khẩu mới quá ngắn | 1. Truy cập /admin/account<br>2. Mở modal Đổi mật khẩu<br>3. Nhập mật khẩu hiện tại<br>4. Nhập mật khẩu mới < 6 ký tự<br>5. Nhấn Đổi mật khẩu | Hiển thị thông báo lỗi "Mật khẩu mới phải có ít nhất 6 ký tự" | | Pass | | |
| **FUNC-DMK-07** | Đổi mật khẩu - Mật khẩu xác nhận không khớp | 1. Truy cập /admin/account<br>2. Mở modal Đổi mật khẩu<br>3. Nhập mật khẩu hiện tại<br>4. Nhập mật khẩu mới<br>5. Nhập xác nhận mật khẩu khác<br>6. Nhấn Đổi mật khẩu | Hiển thị thông báo lỗi "Mật khẩu xác nhận không khớp" | | Pass | | |
| **FUNC-DMK-08** | Hiển thị/ẩn mật khẩu hiện tại | 1. Truy cập /admin/account<br>2. Mở modal Đổi mật khẩu<br>3. Nhập mật khẩu hiện tại<br>4. Nhấn icon Eye | Input chuyển từ type password sang type text, hiển thị mật khẩu, icon chuyển thành EyeOff | | Pass | | |
| **FUNC-DMK-09** | Hiển thị/ẩn mật khẩu mới | 1. Truy cập /admin/account<br>2. Mở modal Đổi mật khẩu<br>3. Nhập mật khẩu mới<br>4. Nhấn icon Eye | Input chuyển từ type password sang type text, hiển thị mật khẩu, icon chuyển thành EyeOff | | Pass | | |
| **FUNC-DMK-10** | Hiển thị/ẩn xác nhận mật khẩu | 1. Truy cập /admin/account<br>2. Mở modal Đổi mật khẩu<br>3. Nhập xác nhận mật khẩu<br>4. Nhấn icon Eye | Input chuyển từ type password sang type text, hiển thị mật khẩu, icon chuyển thành EyeOff | | Pass | | |
| **FUNC-DMK-11** | Đóng modal bằng nút Hủy | 1. Truy cập /admin/account<br>2. Mở modal Đổi mật khẩu<br>3. Nhấn nút Hủy | Modal đóng, form được reset về trạng thái ban đầu | | Pass | | |
| **FUNC-DMK-12** | Đóng modal bằng click bên ngoài | 1. Truy cập /admin/account<br>2. Mở modal Đổi mật khẩu<br>3. Click bên ngoài modal | Modal đóng | | Pass | | |

---

### Function: Quản lý thông tin cá nhân

#### Check GUI: Quản lý thông tin cá nhân

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-QLTT-01** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/account<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Quản lý tài khoản" | | Pass | | |
| **GUI-QLTT-02** | Kiểm tra mô tả trang | 1. Truy cập /admin/account<br>2. Kiểm tra mô tả | Hiển thị mô tả "Quản lý thông tin cá nhân và cài đặt tài khoản" | | Pass | | |
| **GUI-QLTT-03** | Kiểm tra nút Chỉnh sửa | 1. Truy cập /admin/account<br>2. Kiểm tra nút Chỉnh sửa | Hiển thị nút "Chỉnh sửa" với icon Edit | | Pass | | |
| **GUI-QLTT-04** | Kiểm tra Avatar | 1. Truy cập /admin/account<br>2. Kiểm tra Avatar | Hiển thị Avatar với fallback là chữ cái đầu của họ tên, có badge role "Super Admin" với icon Shield | | Pass | | |
| **GUI-QLTT-05** | Kiểm tra card Thông tin cá nhân | 1. Truy cập /admin/account<br>2. Kiểm tra card Thông tin cá nhân | Hiển thị card "Thông tin cá nhân" với icon User, mô tả "Thông tin cơ bản của tài khoản quản trị" | | Pass | | |
| **GUI-QLTT-06** | Kiểm tra trường Họ và tên | 1. Truy cập /admin/account<br>2. Kiểm tra trường Họ và tên | Hiển thị label "Họ và tên", input text hiển thị giá trị hiện tại, disabled khi không ở chế độ chỉnh sửa | | Pass | | |
| **GUI-QLTT-07** | Kiểm tra trường Email | 1. Truy cập /admin/account<br>2. Kiểm tra trường Email | Hiển thị label "Email", input type email hiển thị giá trị hiện tại, disabled khi không ở chế độ chỉnh sửa | | Pass | | |
| **GUI-QLTT-08** | Kiểm tra trường Số điện thoại | 1. Truy cập /admin/account<br>2. Kiểm tra trường Số điện thoại | Hiển thị label "Số điện thoại", input text hiển thị giá trị hiện tại, disabled khi không ở chế độ chỉnh sửa | | Pass | | |
| **GUI-QLTT-09** | Kiểm tra trường Địa chỉ | 1. Truy cập /admin/account<br>2. Kiểm tra trường Địa chỉ | Hiển thị label "Địa chỉ", input text hiển thị giá trị hiện tại, disabled khi không ở chế độ chỉnh sửa | | Pass | | |
| **GUI-QLTT-10** | Kiểm tra trường Ngày sinh | 1. Truy cập /admin/account<br>2. Kiểm tra trường Ngày sinh | Hiển thị label "Ngày sinh", input type date hiển thị giá trị hiện tại, disabled khi không ở chế độ chỉnh sửa | | Pass | | |
| **GUI-QLTT-11** | Kiểm tra card Thông tin tài khoản | 1. Truy cập /admin/account<br>2. Kiểm tra card Thông tin tài khoản | Hiển thị card "Thông tin tài khoản" với icon Shield, mô tả "Thông tin bảo mật và hoạt động tài khoản" | | Pass | | |
| **GUI-QLTT-12** | Kiểm tra thông tin Email đăng nhập | 1. Truy cập /admin/account<br>2. Kiểm tra thông tin Email đăng nhập | Hiển thị icon Mail, label "Email đăng nhập", giá trị email hiện tại | | Pass | | |
| **GUI-QLTT-13** | Kiểm tra thông tin Ngày tạo tài khoản | 1. Truy cập /admin/account<br>2. Kiểm tra thông tin Ngày tạo | Hiển thị icon Calendar, label "Ngày tạo tài khoản", giá trị ngày tạo định dạng Việt Nam | | Pass | | |
| **GUI-QLTT-14** | Kiểm tra thông tin Lần đăng nhập cuối | 1. Truy cập /admin/account<br>2. Kiểm tra thông tin Lần đăng nhập cuối | Hiển thị icon Calendar, label "Lần đăng nhập cuối", giá trị thời gian định dạng Việt Nam | | Pass | | |
| **GUI-QLTT-15** | Kiểm tra nút Lưu thay đổi | 1. Truy cập /admin/account<br>2. Nhấn Chỉnh sửa<br>3. Kiểm tra nút Lưu | Hiển thị nút "Lưu thay đổi" với icon Save | | Pass | | |
| **GUI-QLTT-16** | Kiểm tra nút Hủy khi chỉnh sửa | 1. Truy cập /admin/account<br>2. Nhấn Chỉnh sửa<br>3. Kiểm tra nút Hủy | Hiển thị nút "Hủy" với icon X, variant outline | | Pass | | |

---

### Check FUNC: Quản lý thông tin cá nhân

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-QLTT-01** | Mở trang Quản lý tài khoản | 1. Truy cập /admin/account | Hiển thị trang với tiêu đề "Quản lý tài khoản", 2 card (Thông tin cá nhân, Thông tin tài khoản), nút Chỉnh sửa, nút Đổi mật khẩu, nút Đăng xuất | | Pass | | |
| **FUNC-QLTT-02** | Bật chế độ chỉnh sửa | 1. Truy cập /admin/account<br>2. Nhấn nút "Chỉnh sửa" | Tất cả các trường input trong card "Thông tin cá nhân" được enable, nút "Chỉnh sửa" biến thành "Hủy" và "Lưu thay đổi" | | Pass | | |
| **FUNC-QLTT-03** | Cập nhật thông tin thành công | 1. Truy cập /admin/account<br>2. Nhấn Chỉnh sửa<br>3. Sửa thông tin (Họ tên, SĐT, Địa chỉ, Ngày sinh)<br>4. Nhấn Lưu thay đổi | Hiển thị thông báo "Cập nhật thông tin thành công", các trường được disable lại, thông tin mới được hiển thị | | Untested | | |
| **FUNC-QLTT-04** | Cập nhật thông tin - Thiếu Họ tên | 1. Truy cập /admin/account<br>2. Nhấn Chỉnh sửa<br>3. Xóa họ tên<br>4. Nhấn Lưu thay đổi | Hiển thị thông báo lỗi "Họ tên không được để trống" | | Pass | | |
| **FUNC-QLTT-05** | Cập nhật thông tin - Thiếu Email | 1. Truy cập /admin/account<br>2. Nhấn Chỉnh sửa<br>3. Xóa email<br>4. Nhấn Lưu thay đổi | Hiển thị thông báo lỗi "Email không được để trống" | | Pass | | |
| **FUNC-QLTT-06** | Cập nhật thông tin - Thiếu Số điện thoại | 1. Truy cập /admin/account<br>2. Nhấn Chỉnh sửa<br>3. Xóa số điện thoại<br>4. Nhấn Lưu thay đổi | Hiển thị thông báo lỗi "Số điện thoại không được để trống" | | Pass | | |
| **FUNC-QLTT-07** | Hủy chỉnh sửa | 1. Truy cập /admin/account<br>2. Nhấn Chỉnh sửa<br>3. Sửa một số thông tin<br>4. Nhấn Hủy | Các trường quay về giá trị ban đầu, chế độ chỉnh sửa tắt, nút "Hủy" và "Lưu" biến thành "Chỉnh sửa" | | Pass | | |
| **FUNC-QLTT-08** | Xem thông tin tài khoản | 1. Truy cập /admin/account<br>2. Kiểm tra card Thông tin tài khoản | Hiển thị đầy đủ: Email đăng nhập, Ngày tạo tài khoản, Lần đăng nhập cuối | | Pass | | |

---

### Function: Đăng xuất

#### Check GUI: Đăng xuất

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DX-01** | Kiểm tra nút Đăng xuất | 1. Truy cập /admin/account<br>2. Kiểm tra nút Đăng xuất | Hiển thị nút "Đăng xuất" với icon LogOut, variant destructive, trong card "Thông tin tài khoản" | | Pass | | |
| **GUI-DX-02** | Kiểm tra modal xác nhận đăng xuất | 1. Truy cập /admin/account<br>2. Nhấn nút Đăng xuất<br>3. Kiểm tra modal | Hiển thị AlertDialog với tiêu đề "Xác nhận đăng xuất", mô tả "Bạn có chắc chắn muốn đăng xuất khỏi hệ thống? Bạn sẽ cần đăng nhập lại để tiếp tục sử dụng." | | Pass | | |
| **GUI-DX-03** | Kiểm tra nút Hủy trong modal | 1. Truy cập /admin/account<br>2. Mở modal đăng xuất<br>3. Kiểm tra nút Hủy | Hiển thị nút "Hủy" | | Pass | | |
| **GUI-DX-04** | Kiểm tra nút Đăng xuất trong modal | 1. Truy cập /admin/account<br>2. Mở modal đăng xuất<br>3. Kiểm tra nút Đăng xuất | Hiển thị nút "Đăng xuất" để xác nhận | | Pass | | |

---

### Check FUNC: Đăng xuất

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DX-01** | Mở modal xác nhận đăng xuất | 1. Truy cập /admin/account<br>2. Nhấn nút "Đăng xuất" | Modal AlertDialog hiển thị với tiêu đề "Xác nhận đăng xuất", mô tả, 2 nút (Hủy, Đăng xuất) | | Pass | | |
| **FUNC-DX-02** | Đăng xuất thành công | 1. Truy cập /admin/account<br>2. Nhấn nút Đăng xuất<br>3. Nhấn "Đăng xuất" trong modal | Hiển thị thông báo "Đăng xuất thành công", chuyển đến trang /admin/auth/login, phiên đăng nhập bị xóa | | Untested | | |
| **FUNC-DX-03** | Hủy đăng xuất | 1. Truy cập /admin/account<br>2. Nhấn nút Đăng xuất<br>3. Nhấn "Hủy" trong modal | Modal đóng, vẫn ở trang /admin/account, không đăng xuất | | Pass | | |
| **FUNC-DX-04** | Đóng modal bằng click bên ngoài | 1. Truy cập /admin/account<br>2. Nhấn nút Đăng xuất<br>3. Click bên ngoài modal | Modal đóng, không đăng xuất | | Pass | | |
| **FUNC-DX-05** | Kiểm tra xóa token sau đăng xuất | 1. Truy cập /admin/account<br>2. Đăng xuất thành công<br>3. Kiểm tra localStorage/sessionStorage | Token bị xóa khỏi localStorage/sessionStorage | | Untested | | |
| **FUNC-DX-06** | Kiểm tra xóa session sau đăng xuất | 1. Truy cập /admin/account<br>2. Đăng xuất thành công<br>3. Kiểm tra session | Session bị xóa trên server | | Untested | | |

---

*Template này được tạo theo chuẩn Markdown để dễ dàng quản lý và cập nhật test cases.*

