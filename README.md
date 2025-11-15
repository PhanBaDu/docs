# BLACKBOX TEST CASE - QUẢN LÝ TÀI KHOẢN ADMIN

## THÔNG TIN CHUNG

**Module:** Quản lý tài khoản Admin

**Các chức năng kiểm thử:**
1. Đăng nhập
2. Đăng ký
3. Đổi mật khẩu
4. Quản lý thông tin cá nhân
5. Khôi phục mật khẩu
6. Đăng xuất

**Người kiểm thử:** [Tên tester]

**Thống kê:**

| Pass | Fail | Untested | N/A | Tổng số test case |
|------|------|----------|-----|-------------------|
| 163  | 0    | 0        | 0   | 163               |

---

## 1. CHỨC NĂNG ĐĂNG NHẬP

### 1.1. Kiểm thử giao diện

| ID | Mô tả | Các bước thực hiện | Kết quả mong đợi | Mức độ | Kết quả | Ngày test | Ghi chú |
|----|-------|-------------------|------------------|--------|---------|-----------|---------|
| GUI-DN-01 | Kiểm tra biểu tượng header | 1. Truy cập `/admin/auth/login`<br>2. Kiểm tra biểu tượng Shield | Hiển thị biểu tượng Shield trong vòng tròn | Pass | Pass | 11/15/2025 | |
| GUI-DN-02 | Kiểm tra tiêu đề trang | 1. Truy cập `/admin/auth/login`<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Đăng nhập Admin" | Pass | Pass | 11/15/2025 | |
| GUI-DN-03 | Kiểm tra mô tả chức năng | 1. Truy cập `/admin/auth/login`<br>2. Kiểm tra mô tả | Hiển thị mô tả "Đăng nhập vào hệ thống quản trị" | Pass | Pass | 11/15/2025 | |
| GUI-DN-04 | Kiểm tra trường Email | 1. Truy cập `/admin/auth/login`<br>2. Kiểm tra label và input Email | Hiển thị label "Email Admin", input type email với placeholder "admin@modelshop.com", bắt buộc nhập | Pass | Pass | 11/15/2025 | |
| GUI-DN-05 | Kiểm tra trường Mật khẩu | 1. Truy cập `/admin/auth/login`<br>2. Kiểm tra label và input Mật khẩu | Hiển thị label "Mật khẩu", input type password với placeholder "Nhập mật khẩu", bắt buộc nhập | Pass | Pass | 11/15/2025 | |
| GUI-DN-06 | Kiểm tra checkbox Ghi nhớ | 1. Truy cập `/admin/auth/login`<br>2. Kiểm tra checkbox | Hiển thị checkbox "Ghi nhớ đăng nhập" có thể tích chọn | Pass | Pass | 11/15/2025 | |
| GUI-DN-07 | Kiểm tra link Quên mật khẩu | 1. Truy cập `/admin/auth/login`<br>2. Kiểm tra link | Hiển thị link "Quên mật khẩu?" dẫn đến `/admin/auth/forgot-password` | Pass | Pass | 11/15/2025 | |
| GUI-DN-08 | Kiểm tra nút Đăng nhập | 1. Truy cập `/admin/auth/login`<br>2. Kiểm tra nút submit | Hiển thị nút "Đăng nhập Admin" có thể nhấn | Pass | Pass | 11/15/2025 | |
| GUI-DN-09 | Kiểm tra dấu phân cách | 1. Truy cập `/admin/auth/login`<br>2. Kiểm tra separator | Hiển thị dấu phân cách với chữ "Hoặc" | Pass | Pass | 11/15/2025 | |
| GUI-DN-10 | Kiểm tra link chuyển đổi | 1. Truy cập `/admin/auth/login`<br>2. Kiểm tra link | Hiển thị link "Đăng nhập với tài khoản khách hàng" có icon mũi tên, dẫn đến `/user/auth/login` | Pass | Pass | 11/15/2025 | |
| GUI-DN-11 | Kiểm tra văn bản footer | 1. Truy cập `/admin/auth/login`<br>2. Kiểm tra text footer | Hiển thị "Chỉ dành cho quản trị viên được ủy quyền" | Pass | Pass | 11/15/2025 | |
| GUI-DN-12 | Kiểm tra bố cục trang | 1. Truy cập `/admin/auth/login`<br>2. Kiểm tra layout | Form được căn giữa màn hình với nền gradient, card có độ rộng tối đa | Pass | Pass | 11/15/2025 | |

### 1.2. Kiểm thử chức năng

| ID | Mô tả | Các bước thực hiện | Kết quả mong đợi | Mức độ | Kết quả | Ngày test | Ghi chú |
|----|-------|-------------------|------------------|--------|---------|-----------|---------|
| FUNC-DN-01 | Mở trang đăng nhập | 1. Truy cập `/admin/auth/login` | Hiển thị form đăng nhập với đầy đủ các thành phần: icon, tiêu đề, 2 trường nhập (Email, Mật khẩu), checkbox ghi nhớ, link quên mật khẩu, nút đăng nhập | Pass | Pass | 11/15/2025 | |
| FUNC-DN-02 | Đăng nhập thành công | 1. Truy cập `/admin/auth/login`<br>2. Nhập email hợp lệ<br>3. Nhập mật khẩu đúng<br>4. Nhấn nút Đăng nhập | Hệ thống xác thực thông tin, chuyển đến trang dashboard admin, tạo phiên đăng nhập và lưu token | Pass | Pass | 11/15/2025 | |
| FUNC-DN-03 | Đăng nhập với email không tồn tại | 1. Truy cập `/admin/auth/login`<br>2. Nhập email không tồn tại<br>3. Nhập mật khẩu<br>4. Nhấn Đăng nhập | Hiển thị thông báo lỗi "Email hoặc mật khẩu không đúng", không chuyển trang | Pass | Pass | 11/15/2025 | |
| FUNC-DN-04 | Đăng nhập với mật khẩu sai | 1. Truy cập `/admin/auth/login`<br>2. Nhập email hợp lệ<br>3. Nhập mật khẩu sai<br>4. Nhấn Đăng nhập | Hiển thị thông báo lỗi "Email hoặc mật khẩu không đúng", không chuyển trang | Pass | Pass | 11/15/2025 | |
| FUNC-DN-05 | Đăng nhập thiếu email | 1. Truy cập `/admin/auth/login`<br>2. Để trống email<br>3. Nhập mật khẩu<br>4. Nhấn Đăng nhập | Trình duyệt hiển thị cảnh báo "Please fill out this field", form không được gửi | Pass | Pass | 11/15/2025 | |
| FUNC-DN-06 | Đăng nhập thiếu mật khẩu | 1. Truy cập `/admin/auth/login`<br>2. Nhập email<br>3. Để trống mật khẩu<br>4. Nhấn Đăng nhập | Trình duyệt hiển thị cảnh báo "Please fill out this field", form không được gửi | Pass | Pass | 11/15/2025 | |
| FUNC-DN-07 | Đăng nhập với email sai định dạng | 1. Truy cập `/admin/auth/login`<br>2. Nhập email không đúng định dạng (VD: "invalid-email")<br>3. Nhập mật khẩu<br>4. Nhấn Đăng nhập | Trình duyệt hiển thị cảnh báo "Please include an '@' in the email address", form không được gửi | Pass | Pass | 11/15/2025 | |
| FUNC-DN-08 | Chức năng ghi nhớ - Có tích chọn | 1. Truy cập `/admin/auth/login`<br>2. Tích checkbox "Ghi nhớ đăng nhập"<br>3. Nhập thông tin hợp lệ<br>4. Đăng nhập | Đăng nhập thành công, token được lưu với thời hạn dài hơn | Pass | Pass | 11/15/2025 | |
| FUNC-DN-09 | Chức năng ghi nhớ - Không tích chọn | 1. Truy cập `/admin/auth/login`<br>2. Không tích checkbox<br>3. Nhập thông tin hợp lệ<br>4. Đăng nhập | Đăng nhập thành công, token được lưu với thời hạn ngắn hơn | Pass | Pass | 11/15/2025 | |
| FUNC-DN-10 | Nhấn link Quên mật khẩu | 1. Truy cập `/admin/auth/login`<br>2. Nhấn link "Quên mật khẩu?" | Chuyển đến trang `/admin/auth/forgot-password` | Pass | Pass | 11/15/2025 | |
| FUNC-DN-11 | Nhấn link chuyển sang User | 1. Truy cập `/admin/auth/login`<br>2. Nhấn "Đăng nhập với tài khoản khách hàng" | Chuyển đến trang `/user/auth/login` | Pass | Pass | 11/15/2025 | |
| FUNC-DN-12 | Submit form bằng phím Enter | 1. Truy cập `/admin/auth/login`<br>2. Nhập thông tin<br>3. Nhấn Enter trong trường mật khẩu | Form được gửi, xử lý đăng nhập như khi nhấn nút | Pass | Pass | 11/15/2025 | |

---

## 2. CHỨC NĂNG ĐĂNG KÝ

### 2.1. Kiểm thử giao diện

| ID | Mô tả | Các bước thực hiện | Kết quả mong đợi | Mức độ | Kết quả | Ngày test | Ghi chú |
|----|-------|-------------------|------------------|--------|---------|-----------|---------|
| GUI-DK-01 | Kiểm tra biểu tượng header | 1. Truy cập `/admin/auth/register`<br>2. Kiểm tra icon | Hiển thị biểu tượng Shield | Pass | Pass | 11/15/2025 | |
| GUI-DK-02 | Kiểm tra tiêu đề | 1. Truy cập `/admin/auth/register`<br>2. Kiểm tra tiêu đề | Hiển thị "Đăng ký tài khoản Admin" | Pass | Pass | 11/15/2025 | |
| GUI-DK-03 | Kiểm tra mô tả | 1. Truy cập `/admin/auth/register`<br>2. Kiểm tra mô tả | Hiển thị "Tạo tài khoản quản trị viên mới cho hệ thống Model Shop" | Pass | Pass | 11/15/2025 | |
| GUI-DK-04 | Kiểm tra trường Họ và tên | 1. Truy cập `/admin/auth/register`<br>2. Kiểm tra input | Hiển thị label "Họ và tên *" với icon User, input text có placeholder, bắt buộc nhập | Pass | Pass | 11/15/2025 | |
| GUI-DK-05 | Kiểm tra trường Email | 1. Truy cập `/admin/auth/register`<br>2. Kiểm tra input | Hiển thị label "Email công ty *" với icon Mail, input email có placeholder, bắt buộc nhập | Pass | Pass | 11/15/2025 | |
| GUI-DK-06 | Kiểm tra trường Số điện thoại | 1. Truy cập `/admin/auth/register`<br>2. Kiểm tra input | Hiển thị label "Số điện thoại *" với icon Phone, input tel có placeholder, bắt buộc nhập | Pass | Pass | 11/15/2025 | |
| GUI-DK-07 | Kiểm tra trường Mã nhân viên | 1. Truy cập `/admin/auth/register`<br>2. Kiểm tra input | Hiển thị label "Mã nhân viên *" với icon Key, input text có placeholder "EMP001", bắt buộc nhập | Pass | Pass | 11/15/2025 | |
| GUI-DK-08 | Kiểm tra dropdown Phòng ban | 1. Truy cập `/admin/auth/register`<br>2. Kiểm tra select | Hiển thị label "Phòng ban *" với icon Building, select có các lựa chọn: Ban Giám đốc, Phòng Kinh doanh, Phòng Marketing, Phòng Kho, Phòng Chăm sóc khách hàng, Phòng IT, Phòng Nhân sự, Phòng Tài chính | Pass | Pass | 11/15/2025 | |
| GUI-DK-09 | Kiểm tra trường Chức vụ | 1. Truy cập `/admin/auth/register`<br>2. Kiểm tra input | Hiển thị label "Chức vụ *" với icon Shield, input text có placeholder, bắt buộc nhập | Pass | Pass | 11/15/2025 | |
| GUI-DK-10 | Kiểm tra trường Mật khẩu | 1. Truy cập `/admin/auth/register`<br>2. Kiểm tra input | Hiển thị label "Mật khẩu *", input password có nút hiện/ẩn, gợi ý "Mật khẩu phải có ít nhất 8 ký tự, bao gồm chữ hoa, chữ thường và số" | Pass | Pass | 11/15/2025 | |
| GUI-DK-11 | Kiểm tra trường Xác nhận mật khẩu | 1. Truy cập `/admin/auth/register`<br>2. Kiểm tra input | Hiển thị label "Xác nhận mật khẩu *", input password có nút hiện/ẩn, bắt buộc nhập | Pass | Pass | 11/15/2025 | |
| GUI-DK-12 | Kiểm tra checkbox Điều khoản | 1. Truy cập `/admin/auth/register`<br>2. Kiểm tra checkbox | Hiển thị checkbox với label "Tôi đồng ý với Điều khoản sử dụng Admin và Chính sách bảo mật" (có links) | Pass | Pass | 11/15/2025 | |
| GUI-DK-13 | Kiểm tra nút Đăng ký | 1. Truy cập `/admin/auth/register`<br>2. Kiểm tra nút | Hiển thị nút "Đăng ký tài khoản Admin", khi đang xử lý hiển thị "Đang tạo tài khoản..." | Pass | Pass | 11/15/2025 | |
| GUI-DK-14 | Kiểm tra separator | 1. Truy cập `/admin/auth/register`<br>2. Kiểm tra separator | Hiển thị dấu phân cách với chữ "Hoặc" | Pass | Pass | 11/15/2025 | |
| GUI-DK-15 | Kiểm tra link Đăng nhập Admin | 1. Truy cập `/admin/auth/register`<br>2. Kiểm tra link | Hiển thị link "Đăng nhập với tài khoản admin hiện có" với icon Shield, dẫn đến `/admin/auth/login` | Pass | Pass | 11/15/2025 | |
| GUI-DK-16 | Kiểm tra link Đăng ký User | 1. Truy cập `/admin/auth/register`<br>2. Kiểm tra link | Hiển thị "Chưa có tài khoản khách hàng? Đăng ký tài khoản khách hàng", dẫn đến `/user/auth/register` | Pass | Pass | 11/15/2025 | |
| GUI-DK-17 | Kiểm tra cảnh báo footer | 1. Truy cập `/admin/auth/register`<br>2. Kiểm tra footer | Hiển thị "⚠️ Chỉ dành cho nhân viên được ủy quyền" và "Tài khoản admin cần được xác thực bởi quản trị viên cấp cao" | Pass | Pass | 11/15/2025 | |
| GUI-DK-18 | Kiểm tra bố cục | 1. Truy cập `/admin/auth/register`<br>2. Kiểm tra layout | Form được căn giữa với nền gradient, card có độ rộng tối đa | Pass | Pass | 11/15/2025 | |

### 2.2. Kiểm thử chức năng

| ID | Mô tả | Các bước thực hiện | Kết quả mong đợi | Mức độ | Kết quả | Ngày test | Ghi chú |
|----|-------|-------------------|------------------|--------|---------|-----------|---------|
| FUNC-DK-01 | Mở trang đăng ký | 1. Truy cập `/admin/auth/register` | Hiển thị form đăng ký với đầy đủ các trường: Họ tên, Email, SĐT, Mã NV, Phòng ban, Chức vụ, Mật khẩu, Xác nhận MK, Checkbox điều khoản | Pass | Pass | 11/15/2025 | |
| FUNC-DK-02 | Đăng ký thành công | 1. Điền đầy đủ thông tin hợp lệ<br>2. Mật khẩu ≥8 ký tự, có chữ hoa, thường, số<br>3. Xác nhận mật khẩu khớp<br>4. Tích checkbox điều khoản<br>5. Nhấn Đăng ký | Nút hiển thị "Đang tạo tài khoản...", sau đó thông báo "Đăng ký tài khoản admin thành công!", chuyển đến trang đăng nhập | Pass | Pass | 11/15/2025 | |
| FUNC-DK-03 | Đăng ký thiếu Họ và tên | 1. Để trống Họ và tên<br>2. Điền các trường khác<br>3. Nhấn Đăng ký | Hiển thị lỗi "Họ tên không được để trống", không gửi form | Pass | Pass | 11/15/2025 | |
| FUNC-DK-04 | Đăng ký thiếu Email | 1. Để trống Email<br>2. Điền các trường khác<br>3. Nhấn Đăng ký | Hiển thị lỗi "Email không được để trống", không gửi form | Pass | Pass | 11/15/2025 | |
| FUNC-DK-05 | Email không hợp lệ | 1. Nhập email không có @ (VD: "invalid-email")<br>2. Điền các trường khác<br>3. Nhấn Đăng ký | Hiển thị lỗi "Email không hợp lệ", không gửi form | Pass | Pass | 11/15/2025 | |
| FUNC-DK-06 | Đăng ký thiếu SĐT | 1. Để trống Số điện thoại<br>2. Điền các trường khác<br>3. Nhấn Đăng ký | Hiển thị lỗi "Số điện thoại không được để trống", không gửi form | Pass | Pass | 11/15/2025 | |
| FUNC-DK-07 | Đăng ký thiếu Phòng ban | 1. Không chọn Phòng ban<br>2. Điền các trường khác<br>3. Nhấn Đăng ký | Hiển thị lỗi "Vui lòng chọn phòng ban", không gửi form | Pass | Pass | 11/15/2025 | |
| FUNC-DK-08 | Đăng ký thiếu Chức vụ | 1. Để trống Chức vụ<br>2. Điền các trường khác<br>3. Nhấn Đăng ký | Hiển thị lỗi "Chức vụ không được để trống", không gửi form | Pass | Pass | 11/15/2025 | |
| FUNC-DK-09 | Đăng ký thiếu Mã nhân viên | 1. Để trống Mã nhân viên<br>2. Điền các trường khác<br>3. Nhấn Đăng ký | Hiển thị lỗi "Mã nhân viên không được để trống", không gửi form | Pass | Pass | 11/15/2025 | |
| FUNC-DK-10 | Mật khẩu quá ngắn | 1. Nhập mật khẩu <8 ký tự (VD: "1234567")<br>2. Điền các trường khác<br>3. Nhấn Đăng ký | Hiển thị lỗi "Mật khẩu phải có ít nhất 8 ký tự", không gửi form | Pass | Pass | 11/15/2025 | |
| FUNC-DK-11 | Mật khẩu không đủ điều kiện | 1. Nhập mật khẩu không có chữ hoa/thường/số (VD: "12345678")<br>2. Điền các trường khác<br>3. Nhấn Đăng ký | Hiển thị lỗi "Mật khẩu phải chứa ít nhất 1 chữ hoa, 1 chữ thường và 1 số", không gửi form | Pass | Pass | 11/15/2025 | |
| FUNC-DK-12 | Xác nhận mật khẩu không khớp | 1. Nhập mật khẩu và xác nhận khác nhau<br>2. Điền các trường khác<br>3. Nhấn Đăng ký | Hiển thị lỗi "Mật khẩu xác nhận không khớp", không gửi form | Pass | Pass | 11/15/2025 | |
| FUNC-DK-13 | Không đồng ý điều khoản | 1. Điền đầy đủ thông tin hợp lệ<br>2. Không tích checkbox điều khoản<br>3. Nhấn Đăng ký | Hiển thị lỗi "Vui lòng đồng ý với điều khoản sử dụng", không gửi form | Pass | Pass | 11/15/2025 | |
| FUNC-DK-14 | Hiện/ẩn mật khẩu | 1. Nhập mật khẩu<br>2. Nhấn nút con mắt trong trường Mật khẩu | Mật khẩu chuyển từ ẩn sang hiện, icon chuyển từ Eye sang EyeOff | Pass | Pass | 11/15/2025 | |
| FUNC-DK-15 | Hiện/ẩn xác nhận mật khẩu | 1. Nhập xác nhận mật khẩu<br>2. Nhấn nút con mắt | Mật khẩu chuyển từ ẩn sang hiện, icon thay đổi | Pass | Pass | 11/15/2025 | |
| FUNC-DK-16 | Nhấn link Đăng nhập Admin | 1. Nhấn "Đăng nhập với tài khoản admin hiện có" | Chuyển đến `/admin/auth/login` | Pass | Pass | 11/15/2025 | |
| FUNC-DK-17 | Nhấn link Đăng ký User | 1. Nhấn "Đăng ký tài khoản khách hàng" | Chuyển đến `/user/auth/register` | Pass | Pass | 11/15/2025 | |
| FUNC-DK-18 | Nhấn link Điều khoản | 1. Nhấn "Điều khoản sử dụng Admin" | Mở trang `/admin/terms` | Pass | Pass | 11/15/2025 | |
| FUNC-DK-19 | Nhấn link Chính sách | 1. Nhấn "Chính sách bảo mật" | Mở trang `/admin/privacy` | Pass | Pass | 11/15/2025 | |
| FUNC-DK-20 | Trạng thái loading | 1. Điền thông tin hợp lệ<br>2. Nhấn Đăng ký<br>3. Quan sát nút | Nút hiển thị "Đang tạo tài khoản..." với icon loading, nút bị vô hiệu hóa | Pass | Pass | 11/15/2025 | |

---

## 3. CHỨC NĂNG ĐỔI MẬT KHẨU

### 3.1. Kiểm thử giao diện

| ID | Mô tả | Các bước thực hiện | Kết quả mong đợi | Mức độ | Kết quả | Ngày test | Ghi chú |
|----|-------|-------------------|------------------|--------|---------|-----------|---------|
| GUI-DMK-01 | Kiểm tra Card Thông tin tài khoản | 1. Truy cập `/admin/account`<br>2. Kiểm tra card | Hiển thị card "Thông tin tài khoản" với icon Shield và mô tả | Pass | Pass | 11/15/2025 | |
| GUI-DMK-02 | Kiểm tra nút Đổi mật khẩu | 1. Truy cập `/admin/account`<br>2. Kiểm tra nút trong card | Hiển thị nút "Đổi mật khẩu" với icon Key, full width | Pass | Pass | 11/15/2025 | |
| GUI-DMK-03 | Kiểm tra Dialog | 1. Nhấn nút Đổi mật khẩu<br>2. Kiểm tra dialog | Hiển thị dialog với tiêu đề "Đổi mật khẩu" và mô tả hướng dẫn | Pass | Pass | 11/15/2025 | |
| GUI-DMK-04 | Kiểm tra trường Mật khẩu hiện tại | 1. Mở dialog<br>2. Kiểm tra input | Hiển thị label "Mật khẩu hiện tại", input password có nút hiện/ẩn | Pass | Pass | 11/15/2025 | |
| GUI-DMK-05 | Kiểm tra trường Mật khẩu mới | 1. Mở dialog<br>2. Kiểm tra input | Hiển thị label "Mật khẩu mới", input password có nút hiện/ẩn | Pass | Pass | 11/15/2025 | |
| GUI-DMK-06 | Kiểm tra trường Xác nhận MK mới | 1. Mở dialog<br>2. Kiểm tra input | Hiển thị label "Xác nhận mật khẩu mới", input password có nút hiện/ẩn | Pass | Pass | 11/15/2025 | |
| GUI-DMK-07 | Kiểm tra nút Hủy | 1. Mở dialog<br>2. Kiểm tra nút | Hiển thị nút "Hủy", có thể nhấn để đóng dialog | Pass | Pass | 11/15/2025 | |
| GUI-DMK-08 | Kiểm tra nút Đổi mật khẩu | 1. Mở dialog<br>2. Kiểm tra nút submit | Hiển thị nút "Đổi mật khẩu", có thể nhấn để xử lý | Pass | Pass | 11/15/2025 | |
| GUI-DMK-09 | Kiểm tra nút hiện/ẩn MK hiện tại | 1. Mở dialog<br>2. Kiểm tra nút con mắt | Hiển thị nút với icon Eye/EyeOff ở góc phải trường MK hiện tại | Pass | Pass | 11/15/2025 | |
| GUI-DMK-10 | Kiểm tra nút hiện/ẩn MK mới | 1. Mở dialog<br>2. Kiểm tra nút | Hiển thị nút với icon Eye/EyeOff ở góc phải trường MK mới | Pass | Pass | 11/15/2025 | |
| GUI-DMK-11 | Kiểm tra nút hiện/ẩn Xác nhận MK | 1. Mở dialog<br>2. Kiểm tra nút | Hiển thị nút với icon Eye/EyeOff ở góc phải trường Xác nhận MK | Pass | Pass | 11/15/2025 | |

### 3.2. Kiểm thử chức năng

| ID | Mô tả | Các bước thực hiện | Kết quả mong đợi | Mức độ | Kết quả | Ngày test | Ghi chú |
|----|-------|-------------------|------------------|--------|---------|-----------|---------|
| FUNC-DMK-01 | Mở dialog đổi mật khẩu | 1. Truy cập `/admin/account`<br>2. Nhấn nút Đổi mật khẩu | Hiển thị dialog với 3 trường nhập trống, nút Hủy và Đổi mật khẩu | Pass | Pass | 11/15/2025 | |
| FUNC-DMK-02 | Đổi mật khẩu thành công | 1. Mở dialog<br>2. Nhập mật khẩu hiện tại đúng<br>3. Nhập mật khẩu mới ≥6 ký tự<br>4. Nhập xác nhận khớp<br>5. Nhấn Đổi mật khẩu | Form được reset, dialog đóng, thông báo "Đổi mật khẩu thành công" | Pass | Pass | 11/15/2025 | |
| FUNC-DMK-03 | Thiếu mật khẩu hiện tại | 1. Mở dialog<br>2. Để trống MK hiện tại<br>3. Nhập MK mới và xác nhận<br>4. Nhấn Đổi mật khẩu | Hiển thị lỗi "Vui lòng nhập mật khẩu hiện tại", không gửi form | Pass | Pass | 11/15/2025 | |
| FUNC-DMK-04 | Thiếu mật khẩu mới | 1. Mở dialog<br>2. Nhập MK hiện tại<br>3. Để trống MK mới<br>4. Nhấn Đổi mật khẩu | Hiển thị lỗi "Vui lòng nhập mật khẩu mới", không gửi form | Pass | Pass | 11/15/2025 | |
| FUNC-DMK-05 | Mật khẩu mới quá ngắn | 1. Mở dialog<br>2. Nhập MK hiện tại<br>3. Nhập MK mới <6 ký tự<br>4. Nhấn Đổi mật khẩu | Hiển thị lỗi "Mật khẩu mới phải có ít nhất 6 ký tự", không gửi form | Pass | Pass | 11/15/2025 | |
| FUNC-DMK-06 | Xác nhận không khớp | 1. Mở dialog<br>2. Nhập MK hiện tại<br>3. Nhập MK mới<br>4. Nhập xác nhận khác<br>5. Nhấn Đổi mật khẩu | Hiển thị lỗi "Mật khẩu xác nhận không khớp", không gửi form | Pass | Pass | 11/15/2025 | |
| FUNC-DMK-07 | Hiện/ẩn MK hiện tại | 1. Mở dialog<br>2. Nhập MK hiện tại<br>3. Nhấn nút con mắt | Input chuyển từ ẩn sang hiện, icon thay đổi | Pass | Pass | 11/15/2025 | |
| FUNC-DMK-08 | Hiện/ẩn MK mới | 1. Mở dialog<br>2. Nhập MK mới<br>3. Nhấn nút con mắt | Input chuyển từ ẩn sang hiện, icon thay đổi | Pass | Pass | 11/15/2025 | |
| FUNC-DMK-09 | Hiện/ẩn Xác nhận MK | 1. Mở dialog<br>2. Nhập xác nhận MK<br>3. Nhấn nút con mắt | Input chuyển từ ẩn sang hiện, icon thay đổi | Pass | Pass | 11/15/2025 | |
| FUNC-DMK-10 | Nhấn nút Hủy | 1. Mở dialog<br>2. Nhập thông tin<br>3. Nhấn Hủy | Dialog đóng, thông tin không được lưu | Pass | Pass | 11/15/2025 | |
| FUNC-DMK-11 | Đóng dialog bằng click ngoài | 1. Mở dialog<br>2. Click bên ngoài dialog | Dialog đóng, không gửi form | Pass | Pass | 11/15/2025 | |
| FUNC-DMK-12 | Reset form sau khi thành công | 1. Đổi mật khẩu thành công<br>2. Mở lại dialog | Tất cả các trường đều trống | Pass | Pass | 11/15/2025 | |

---

## 4. CHỨC NĂNG QUẢN LÝ THÔNG TIN CÁ NHÂN

### 4.1. Kiểm thử giao diện

| ID | Mô tả | Các bước thực hiện | Kết quả mong đợi | Mức độ | Kết quả | Ngày test | Ghi chú |
|----|-------|-------------------|------------------|--------|---------|-----------|---------|
| GUI-QLTT-01 | Kiểm tra Header | 1. Truy cập `/admin/account`<br>2. Kiểm tra header | Hiển thị tiêu đề "Quản lý tài khoản" và mô tả | Pass | Pass | 11/15/2025 | |
| GUI-QLTT-02 | Kiểm tra nút Chỉnh sửa | 1. Truy cập `/admin/account`<br>2. Kiểm tra nút (chế độ xem) | Hiển thị nút "Chỉnh sửa" với icon Edit | Pass | Pass | 11/15/2025 | |
| GUI-QLTT-03 | Kiểm tra nút Hủy và Lưu | 1. Nhấn Chỉnh sửa<br>2. Kiểm tra các nút | Hiển thị nút "Hủy" với icon X và "Lưu thay đổi" với icon Save | Pass | Pass | 11/15/2025 | |
| GUI-QLTT-04 | Kiểm tra Card Thông tin cá nhân | 1. Truy cập `/admin/account`<br>2. Kiểm tra card | Hiển thị card với icon User, tiêu đề "Thông tin cá nhân" và mô tả | Pass | Pass | 11/15/2025 | |
| GUI-QLTT-05 | Kiểm tra Avatar và thông tin | 1. Truy cập `/admin/account`<br>2. Kiểm tra phần avatar | Hiển thị avatar (ảnh hoặc chữ cái đầu), họ tên, badge vai trò với icon Shield | Pass | Pass | 11/15/2025 | |
| GUI-QLTT-06 | Kiểm tra Separator | 1. Truy cập `/admin/account`<br>2. Kiểm tra | Hiển thị đường phân cách giữa avatar và form | Pass | Pass | 11/15/2025 | |
| GUI-QLTT-07 | Kiểm tra trường Họ và tên | 1. Truy cập `/admin/account`<br>2. Kiểm tra input | Hiển thị label "Họ và tên", input bị khóa khi không chỉnh sửa | Pass | Pass | 11/15/2025 | |
| GUI-QLTT-08 | Kiểm tra trường Email | 1. Truy cập `/admin/account`<br>2. Kiểm tra input | Hiển thị label "Email", input type email bị khóa khi không chỉnh sửa | Pass | Pass | 11/15/2025 | |
| GUI-QLTT-09 | Kiểm tra trường SĐT | 1. Truy cập `/admin/account`<br>2. Kiểm tra input | Hiển thị label "Số điện thoại", input bị khóa khi không chỉnh sửa | Pass | Pass | 11/15/2025 | |
| GUI-QLTT-10 | Kiểm tra trường Địa chỉ | 1. Truy cập `/admin/account`<br>2. Kiểm tra input | Hiển thị label "Địa chỉ", input bị khóa khi không chỉnh sửa | Pass | Pass | 11/15/2025 | |
| GUI-QLTT-11 | Kiểm tra trường Ngày sinh | 1. Truy cập `/admin/account`<br>2. Kiểm tra input | Hiển thị label "Ngày sinh", input date bị khóa khi không chỉnh sửa | Pass | Pass | 11/15/2025 | |
| GUI-QLTT-12 | Kiểm tra Card Thông tin tài khoản | 1. Truy cập `/admin/account`<br>2. Kiểm tra card | Hiển thị card với icon Shield, tiêu đề "Thông tin tài khoản" và mô tả | Pass | Pass | 11/15/2025 | |
| GUI-QLTT-13 | Kiểm tra Email đăng nhập | 1. Truy cập `/admin/account`<br>2. Kiểm tra thông tin | Hiển thị icon Mail, label "Email đăng nhập" và email | Pass | Pass | 11/15/2025 | |
| GUI-QLTT-14 | Kiểm tra Ngày tạo tài khoản | 1. Truy cập `/admin/account`<br>2. Kiểm tra thông tin | Hiển thị icon Calendar, label "Ngày tạo tài khoản" và ngày (định dạng tiếng Việt) | Pass | Pass | 11/15/2025 | |
| GUI-QLTT-15 | Kiểm tra Lần đăng nhập cuối | 1. Truy cập `/admin/account`<br>2. Kiểm tra thông tin | Hiển thị icon Calendar, label "Lần đăng nhập cuối" và thời gian (định dạng tiếng Việt) | Pass | Pass | 11/15/2025 | |
| GUI-QLTT-16 | Kiểm tra nút Đăng xuất | 1. Truy cập `/admin/account`<br>2. Kiểm tra nút | Hiển thị nút "Đăng xuất" với icon LogOut, màu đỏ, full width | Pass | Pass | 11/15/2025 | |

### 4.2. Kiểm thử chức năng

| ID | Mô tả | Các bước thực hiện | Kết quả mong đợi | Mức độ | Kết quả | Ngày test | Ghi chú |
|----|-------|-------------------|------------------|--------|---------|-----------|---------|
| FUNC-QLTT-01 | Mở trang quản lý tài khoản | 1. Truy cập `/admin/account` | Hiển thị 2 card, form với thông tin đã điền, các input bị khóa, nút Chỉnh sửa | Pass | Pass | 11/15/2025 | |
| FUNC-QLTT-02 | Nhấn nút Chỉnh sửa | 1. Truy cập `/admin/account`<br>2. Nhấn Chỉnh sửa | Các input được mở khóa, nút Chỉnh sửa ẩn, hiển thị nút Hủy và Lưu | Pass | Pass | 11/15/2025 | |
| FUNC-QLTT-03 | Cập nhật thành công | 1. Nhấn Chỉnh sửa<br>2. Sửa thông tin (tên, SĐT, địa chỉ, ngày sinh)<br>3. Nhấn Lưu thay đổi | Thông tin được cập nhật, các input bị khóa lại, thông báo "Cập nhật thông tin thành công" | Pass | Pass | 11/15/2025 | |
| FUNC-QLTT-04 | Cập nhật thiếu Họ và tên | 1. Nhấn Chỉnh sửa<br>2. Xóa Họ và tên<br>3. Nhấn Lưu | Hiển thị lỗi "Họ tên không được để trống", vẫn ở chế độ chỉnh sửa | Pass | Pass | 11/15/2025 | |
| FUNC-QLTT-05 | Cập nhật thiếu Email | 1. Nhấn Chỉnh sửa<br>2. Xóa Email<br>3. Nhấn Lưu | Hiển thị lỗi "Email không được để trống", vẫn ở chế độ chỉnh sửa | Pass | Pass | 11/15/2025 | |
| FUNC-QLTT-06 | Cập nhật thiếu SĐT | 1. Nhấn Chỉnh sửa<br>2. Xóa SĐT<br>3. Nhấn Lưu | Hiển thị lỗi "Số điện thoại không được để trống", vẫn ở chế độ chỉnh sửa | Pass | Pass | 11/15/2025 | |
| FUNC-QLTT-07 | Cập nhật Họ và tên | 1. Nhấn Chỉnh sửa<br>2. Sửa Họ và tên<br>3. Nhấn Lưu | Họ tên được cập nhật, avatar cập nhật chữ cái đầu, thông báo thành công | Pass | Pass | 11/15/2025 | |
| FUNC-QLTT-08 | Cập nhật SĐT | 1. Nhấn Chỉnh sửa<br>2. Sửa SĐT<br>3. Nhấn Lưu | SĐT được cập nhật, thông báo thành công | Pass | Pass | 11/15/2025 | |
| FUNC-QLTT-09 | Cập nhật Địa chỉ | 1. Nhấn Chỉnh sửa<br>2. Sửa Địa chỉ<br>3. Nhấn Lưu | Địa chỉ được cập nhật, thông báo thành công | Pass | Pass | 11/15/2025 | |
| FUNC-QLTT-10 | Cập nhật Ngày sinh | 1. Nhấn Chỉnh sửa<br>2. Chọn Ngày sinh mới<br>3. Nhấn Lưu | Ngày sinh được cập nhật, thông báo thành công | Pass | Pass | 11/15/2025 | |
| FUNC-QLTT-11 | Nhấn nút Hủy | 1. Nhấn Chỉnh sửa<br>2. Sửa thông tin<br>3. Nhấn Hủy | Thông tin khôi phục về ban đầu, các input bị khóa, nút Chỉnh sửa hiển thị lại | Pass | Pass | 11/15/2025 | |
| FUNC-QLTT-12 | Input khóa khi không chỉnh sửa | 1. Truy cập `/admin/account`<br>2. Kiểm tra các input | Tất cả input bị khóa, không thể nhập | Pass | Pass | 11/15/2025 | |
| FUNC-QLTT-13 | Input mở khi chỉnh sửa | 1. Nhấn Chỉnh sửa<br>2. Kiểm tra các input | Tất cả input được mở, có thể nhập liệu | Pass | Pass | 11/15/2025 | |
| FUNC-QLTT-14 | Hiển thị thông tin tài khoản | 1. Truy cập `/admin/account`<br>2. Xem card Thông tin tài khoản | Hiển thị Email, Ngày tạo, Lần đăng nhập cuối (định dạng tiếng Việt), không thể sửa | Pass | Pass | 11/15/2025 | |
| FUNC-QLTT-15 | Avatar hiển thị | 1. Truy cập `/admin/account`<br>2. Kiểm tra avatar | Nếu có ảnh: hiển thị ảnh, nếu không: hiển thị chữ cái đầu của tên | Pass | Pass | 11/15/2025 | |

---

## 5. CHỨC NĂNG KHÔI PHỤC MẬT KHẨU

### 5.1. Kiểm thử giao diện

| ID | Mô tả | Các bước thực hiện | Kết quả mong đợi | Mức độ | Kết quả | Ngày test | Ghi chú |
|----|-------|-------------------|------------------|--------|---------|-----------|---------|
| GUI-KPMK-01 | Kiểm tra Header | 1. Truy cập `/admin/auth/forgot-password`<br>2. Kiểm tra header | Hiển thị icon Shield, tiêu đề "Khôi phục mật khẩu", mô tả "Chọn phương thức khôi phục mật khẩu của bạn" | Pass | Pass | 11/15/2025 | |
| GUI-KPMK-02 | Kiểm tra Card | 1. Truy cập `/admin/auth/forgot-password`<br>2. Kiểm tra card | Hiển thị card với icon Lock, tiêu đề "Khôi phục mật khẩu", mô tả thay đổi theo bước | Pass | Pass | 11/15/2025 | |
| GUI-KPMK-03 | Kiểm tra phương thức Email | 1. Vào trang khôi phục<br>2. Xem phương thức Email | Hiển thị radio button, icon Mail, text "Email" và "Gửi mã xác thực qua email", input Email khi chọn | Pass | Pass | 11/15/2025 | |
| GUI-KPMK-04 | Kiểm tra phương thức SMS | 1. Vào trang khôi phục<br>2. Xem phương thức SMS | Hiển thị radio button, icon Phone, text "SMS" và "Gửi mã xác thực qua SMS", input SĐT khi chọn | Pass | Pass | 11/15/2025 | |
| GUI-KPMK-05 | Kiểm tra phương thức Câu hỏi | 1. Vào trang khôi phục<br>2. Xem phương thức Câu hỏi bảo mật | Hiển thị radio button, icon MessageSquare, text "Câu hỏi bảo mật" và "Trả lời câu hỏi bảo mật", 3 input câu hỏi khi chọn | Pass | Pass | 11/15/2025 | |
| GUI-KPMK-06 | Kiểm tra nút Tiếp tục (Bước 1) | 1. Ở bước 1<br>2. Kiểm tra nút | Hiển thị nút "Tiếp tục" với icon Key (hoặc Loader2 khi loading), full width | Pass | Pass | 11/15/2025 | |
| GUI-KPMK-07 | Kiểm tra Alert và Input OTP (Bước 2) | 1. Chuyển sang bước 2<br>2. Kiểm tra | Hiển thị Alert với icon Mail, input "Mã xác thực" với placeholder "Nhập mã xác thực 6 chữ số", maxLength=6 | Pass | Pass | 11/15/2025 | |
| GUI-KPMK-08 | Kiểm tra nút Xác thực (Bước 2) | 1. Ở bước 2<br>2. Kiểm tra nút | Hiển thị nút "Xác thực" với icon CheckCircle (hoặc Loader2), full width | Pass | Pass | 11/15/2025 | |
| GUI-KPMK-09 | Kiểm tra nút Quay lại (Bước 2) | 1. Ở bước 2<br>2. Kiểm tra nút | Hiển thị nút "Quay lại" với icon ArrowLeft | Pass | Pass | 11/15/2025 | |
| GUI-KPMK-10 | Kiểm tra Form MK mới (Bước 3) | 1. Chuyển sang bước 3<br>2. Kiểm tra | Hiển thị Alert thành công, input "Mật khẩu mới" và "Xác nhận mật khẩu" type password | Pass | Pass | 11/15/2025 | |
| GUI-KPMK-11 | Kiểm tra thanh Độ mạnh MK | 1. Ở bước 3<br>2. Nhập mật khẩu<br>3. Kiểm tra thanh | Hiển thị thanh progress màu thay đổi (đỏ/vàng/xanh), label "Yếu"/"Trung bình"/"Mạnh" | Pass | Pass | 11/15/2025 | |
| GUI-KPMK-12 | Kiểm tra Yêu cầu mật khẩu | 1. Ở bước 3<br>2. Kiểm tra danh sách | Hiển thị label "Yêu cầu mật khẩu", danh sách: "Ít nhất 8 ký tự", "Có ít nhất 1 chữ hoa", "Có ít nhất 1 chữ số", "Có ít nhất 1 ký tự đặc biệt", mỗi item có chấm màu (xanh khi đạt) | Pass | Pass | 11/15/2025 | |
| GUI-KPMK-13 | Kiểm tra nút Đặt lại MK (Bước 3) | 1. Ở bước 3<br>2. Kiểm tra nút | Hiển thị nút "Đặt lại mật khẩu" với icon Lock (hoặc Loader2), full width, khóa khi chưa hợp lệ | Pass | Pass | 11/15/2025 | |
| GUI-KPMK-14 | Kiểm tra màn hình Thành công (Bước 4) | 1. Chuyển sang bước 4<br>2. Kiểm tra | Hiển thị icon CheckCircle lớn, tiêu đề "Khôi phục mật khẩu thành công", mô tả, nút "Đăng nhập ngay" (icon User) và "Quay về trang chủ" (icon ArrowLeft) | Pass | Pass | 11/15/2025 | |
| GUI-KPMK-15 | Kiểm tra link Footer | 1. Truy cập trang<br>2. Kiểm tra footer | Hiển thị "Bạn có tài khoản? Đăng nhập" | Pass | Pass | 11/15/2025 | |

### 5.2. Kiểm thử chức năng

| ID | Mô tả | Các bước thực hiện | Kết quả mong đợi | Mức độ | Kết quả | Ngày test | Ghi chú |
|----|-------|-------------------|------------------|--------|---------|-----------|---------|
| FUNC-KPMK-01 | Mở trang khôi phục | 1. Truy cập `/admin/auth/forgot-password` | Hiển thị màn hình bước 1 với 3 phương thức: Email, SMS, Câu hỏi bảo mật | Pass | Pass | 11/15/2025 | |
| FUNC-KPMK-02 | Chọn phương thức Email | 1. Nhấn vào phương thức Email | Radio button Email được chọn, hiển thị input Email | Pass | Pass | 11/15/2025 | |
| FUNC-KPMK-03 | Chọn phương thức SMS | 1. Nhấn vào phương thức SMS | Radio button SMS được chọn, hiển thị input SĐT | Pass | Pass | 11/15/2025 | |
| FUNC-KPMK-04 | Chọn phương thức Câu hỏi | 1. Nhấn vào phương thức Câu hỏi bảo mật | Radio button được chọn, hiển thị 3 input câu hỏi | Pass | Pass | 11/15/2025 | |
| FUNC-KPMK-05 | Gửi mã qua Email | 1. Chọn Email<br>2. Nhập email hợp lệ<br>3. Nhấn Tiếp tục | Nút hiển thị "Đang xử lý...", sau 2s thông báo "Mã xác thực đã được gửi", chuyển sang bước 2 | Pass | Pass | 11/15/2025 | |
| FUNC-KPMK-06 | Gửi mã thiếu email | 1. Chọn Email<br>2. Không nhập email<br>3. Nhấn Tiếp tục | Hiển thị lỗi "Vui lòng nhập email", không chuyển bước | Pass | Pass | 11/15/2025 | |
| FUNC-KPMK-07 | Trả lời câu hỏi bảo mật | 1. Chọn Câu hỏi<br>2. Trả lời đầy đủ 3 câu<br>3. Nhấn Tiếp tục | Xử lý 2s, thông báo "Xác thực thành công", chuyển sang bước 3 | Pass | Pass | 11/15/2025 | |
| FUNC-KPMK-08 | Trả lời thiếu câu hỏi | 1. Chọn Câu hỏi<br>2. Không trả lời đầy đủ<br>3. Nhấn Tiếp tục | Hiển thị lỗi "Vui lòng trả lời đầy đủ các câu hỏi bảo mật", không chuyển bước | Pass | Pass |
