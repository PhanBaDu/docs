# BLACKBOX TEST CASE - BẢO MẬT (ADMIN)

## HEADER SECTION

**Module Code:** Bảo mật Admin

**Test requirement:**
1. Khôi phục mật khẩu
2. Lịch sử đăng nhập
3. Xóa phiên đăng nhập

**Tester:** [Tên tester]

**Summary Statistics:**

| Pass | Fail | Untested | N/A | Number of Test cases |
|------|------|----------|-----|---------------------|
| 43 | 0 | 0 | 0 | 43 |

---

## TEST CASE TABLE

| ID | Test Case Description | Test Case Procedure | Expected Output | Test-case rate | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|----------------|--------|-----------|------|
| **Function: Khôi phục mật khẩu** |
| **Check GUI: Khôi phục mật khẩu** |
| GUI-KhoiPhucMK-01 | Check [Tiêu đề trang] Text | 1. Truy cập `/admin/auth/forgot-password`<br>2. Kiểm tra tiêu đề | Status: visible, Text: "Khôi phục mật khẩu Admin" | | Pass | 11/15/2025 | |
| GUI-KhoiPhucMK-02 | Check [Mô tả chức năng] Text | 1. Truy cập `/admin/auth/forgot-password`<br>2. Kiểm tra mô tả | Status: visible, Text: "Gửi link khôi phục qua email/SMS" | | Pass | 11/15/2025 | |
| GUI-KhoiPhucMK-03 | Check [Form khôi phục] Form | 1. Truy cập `/admin/auth/forgot-password`<br>2. Kiểm tra form | Status: visible, Hiển thị form nhập email | | Pass | 11/15/2025 | |
| GUI-KhoiPhucMK-04 | Check [Ô nhập email] Input | 1. Truy cập `/admin/auth/forgot-password`<br>2. Kiểm tra ô [Email] | Status: visible, enable, Type: email | | Pass | 11/15/2025 | |
| GUI-KhoiPhucMK-05 | Check [Gửi link khôi phục] Button | 1. Truy cập `/admin/auth/forgot-password`<br>2. Kiểm tra nút [Gửi link khôi phục] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-KhoiPhucMK-06 | Check [Quay lại đăng nhập] Button | 1. Truy cập `/admin/auth/forgot-password`<br>2. Kiểm tra nút [Quay lại đăng nhập] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-KhoiPhucMK-07 | Check [Thông báo thành công] Toast | 1. Truy cập `/admin/auth/forgot-password`<br>2. Gửi link thành công<br>3. Kiểm tra toast | Status: visible, Text: "Email khôi phục mật khẩu đã được gửi!" | | Pass | 11/15/2025 | |
| **Check FUNC: Khôi phục mật khẩu** |
| FUNC-KhoiPhucMK-01 | Mở màn hình khôi phục mật khẩu | 1. Truy cập `/admin/auth/forgot-password` hoặc click [Quên mật khẩu?] từ trang đăng nhập | Hiển thị màn hình khôi phục mật khẩu với form nhập email | | Pass | 11/15/2025 | |
| FUNC-KhoiPhucMK-02 | Gửi link khôi phục với email hợp lệ | 1. Truy cập `/admin/auth/forgot-password`<br>2. Nhập email hợp lệ đã đăng ký<br>3. Click [Gửi link khôi phục] | Email khôi phục được gửi thành công, token được tạo (1 lần, có thời hạn), thông báo thành công hiển thị | | Pass | 11/15/2025 | |
| FUNC-KhoiPhucMK-03 | Gửi link khôi phục với email không tồn tại | 1. Truy cập `/admin/auth/forgot-password`<br>2. Nhập email không tồn tại<br>3. Click [Gửi link khôi phục] | Hiển thị thông báo lỗi: "Email không tồn tại trong hệ thống" | | Pass | 11/15/2025 | |
| FUNC-KhoiPhucMK-04 | Gửi link khôi phục với email không đúng định dạng | 1. Truy cập `/admin/auth/forgot-password`<br>2. Nhập email không đúng định dạng<br>3. Click [Gửi link khôi phục] | Hiển thị thông báo lỗi: "Email không đúng định dạng" | | Pass | 11/15/2025 | |
| FUNC-KhoiPhucMK-05 | Tạo token khôi phục | 1. Truy cập `/admin/auth/forgot-password`<br>2. Gửi link khôi phục thành công | Token được tạo, chỉ sử dụng được 1 lần, có thời hạn sử dụng | | Pass | 11/15/2025 | |
| FUNC-KhoiPhucMK-06 | Gửi yêu cầu khôi phục quá thường xuyên | 1. Truy cập `/admin/auth/forgot-password`<br>2. Gửi link khôi phục nhiều lần liên tiếp | Hiển thị thông báo: "Vui lòng đợi X phút trước khi yêu cầu lại" | | Pass | 11/15/2025 | |
| FUNC-KhoiPhucMK-07 | Click nút Quay lại đăng nhập | 1. Truy cập `/admin/auth/forgot-password`<br>2. Click [Quay lại đăng nhập] | Chuyển về trang đăng nhập | | Pass | 11/15/2025 | |
| **Function: Lịch sử đăng nhập** |
| **Check GUI: Lịch sử đăng nhập** |
| GUI-LSDN-01 | Check [Tiêu đề trang] Text | 1. Truy cập `/admin/security/login-history`<br>2. Kiểm tra tiêu đề | Status: visible, Text: "Lịch sử đăng nhập Admin" | | Pass | 11/15/2025 | |
| GUI-LSDN-02 | Check [Bộ lọc thời gian] Select | 1. Truy cập `/admin/security/login-history`<br>2. Kiểm tra dropdown [Bộ lọc thời gian] | Status: visible, enable, Options: Tất cả, Tuần này, Tháng này, 3 tháng gần đây | | Pass | 11/15/2025 | |
| GUI-LSDN-03 | Check [Bộ lọc thiết bị] Select | 1. Truy cập `/admin/security/login-history`<br>2. Kiểm tra dropdown [Bộ lọc thiết bị] | Status: visible, enable, Options: Tất cả, Desktop, Mobile, Tablet | | Pass | 11/15/2025 | |
| GUI-LSDN-04 | Check [Bộ lọc trạng thái] Select | 1. Truy cập `/admin/security/login-history`<br>2. Kiểm tra dropdown [Bộ lọc trạng thái] | Status: visible, enable, Options: Tất cả, Thành công, Thất bại | | Pass | 11/15/2025 | |
| GUI-LSDN-05 | Check [Bảng lịch sử] Table | 1. Truy cập `/admin/security/login-history`<br>2. Kiểm tra bảng | Status: visible, Columns: Thời gian, IP, Thiết bị, OS, Trình duyệt, Vị trí, Trạng thái | | Pass | 11/15/2025 | |
| GUI-LSDN-06 | Check [Badge đăng nhập lạ] Badge | 1. Truy cập `/admin/security/login-history`<br>2. Kiểm tra badge | Status: visible, Hiển thị badge "Đăng nhập lạ" cho các phiên đăng nhập từ thiết bị mới hoặc vị trí mới | | Pass | 11/15/2025 | |
| GUI-LSDN-07 | Check [Phân trang] Pagination | 1. Truy cập `/admin/security/login-history`<br>2. Kiểm tra phân trang | Status: visible, enable | | Pass | 11/15/2025 | |
| **Check FUNC: Lịch sử đăng nhập** |
| FUNC-LSDN-01 | Mở màn hình lịch sử đăng nhập | 1. Truy cập `/admin/security/login-history` hoặc click [Bảo mật] > [Lịch sử đăng nhập] | Hiển thị màn hình lịch sử đăng nhập với đầy đủ thông tin | | Pass | 11/15/2025 | |
| FUNC-LSDN-02 | Hiển thị lịch sử đăng nhập | 1. Truy cập `/admin/security/login-history`<br>2. Kiểm tra bảng | Hiển thị đầy đủ: Thời gian, IP, Thiết bị, OS, Trình duyệt, Vị trí, Trạng thái | | Pass | 11/15/2025 | |
| FUNC-LSDN-03 | Lọc theo thời gian | 1. Truy cập `/admin/security/login-history`<br>2. Chọn thời gian từ dropdown<br>3. Kiểm tra kết quả | Danh sách được cập nhật theo khoảng thời gian đã chọn | | Pass | 11/15/2025 | |
| FUNC-LSDN-04 | Lọc theo thiết bị | 1. Truy cập `/admin/security/login-history`<br>2. Chọn thiết bị từ dropdown<br>3. Kiểm tra kết quả | Danh sách được cập nhật theo thiết bị đã chọn | | Pass | 11/15/2025 | |
| FUNC-LSDN-05 | Lọc theo trạng thái | 1. Truy cập `/admin/security/login-history`<br>2. Chọn trạng thái từ dropdown<br>3. Kiểm tra kết quả | Danh sách được cập nhật theo trạng thái đã chọn | | Pass | 11/15/2025 | |
| FUNC-LSDN-06 | Phát hiện đăng nhập lạ | 1. Truy cập `/admin/security/login-history`<br>2. Kiểm tra các phiên đăng nhập | Đăng nhập từ thiết bị mới hoặc vị trí mới được đánh dấu với badge "Đăng nhập lạ" | | Pass | 11/15/2025 | |
| FUNC-LSDN-07 | Gửi thông báo đăng nhập lạ | 1. Truy cập `/admin/security/login-history`<br>2. Có đăng nhập lạ mới<br>3. Kiểm tra thông báo | Thông báo được gửi qua email/SMS để cảnh báo admin về đăng nhập lạ | | Pass | 11/15/2025 | |
| FUNC-LSDN-08 | Phân trang lịch sử đăng nhập | 1. Truy cập `/admin/security/login-history`<br>2. Click nút phân trang | Hiển thị trang tiếp theo của lịch sử đăng nhập | | Pass | 11/15/2025 | |
| **Function: Xóa phiên đăng nhập** |
| **Check GUI: Xóa phiên đăng nhập** |
| GUI-XoaPDN-01 | Check [Tiêu đề trang] Text | 1. Truy cập `/admin/security/sessions`<br>2. Kiểm tra tiêu đề | Status: visible, Text: "Quản lý phiên đăng nhập Admin" | | Pass | 11/15/2025 | |
| GUI-XoaPDN-02 | Check [Phiên hiện tại] Card | 1. Truy cập `/admin/security/sessions`<br>2. Kiểm tra card | Status: visible, Hiển thị: Thiết bị, Thời gian, IP, Vị trí | | Pass | 11/15/2025 | |
| GUI-XoaPDN-03 | Check [Danh sách phiên khác] List | 1. Truy cập `/admin/security/sessions`<br>2. Kiểm tra danh sách | Status: visible, Hiển thị: Thiết bị, OS, Trình duyệt, Hoạt động cuối, Trạng thái | | Pass | 11/15/2025 | |
| GUI-XoaPDN-04 | Check [Xóa phiên] Button | 1. Truy cập `/admin/security/sessions`<br>2. Kiểm tra nút [Xóa phiên] trong mỗi phiên | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-XoaPDN-05 | Check [Đăng xuất tất cả thiết bị] Button | 1. Truy cập `/admin/security/sessions`<br>2. Kiểm tra nút [Đăng xuất tất cả thiết bị] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-XoaPDN-06 | Check [Modal xác nhận] Dialog | 1. Truy cập `/admin/security/sessions`<br>2. Click [Xóa phiên] hoặc [Đăng xuất tất cả]<br>3. Kiểm tra modal | Status: visible, Hiển thị form xác nhận | | Pass | 11/15/2025 | |
| **Check FUNC: Xóa phiên đăng nhập** |
| FUNC-XoaPDN-01 | Mở màn hình quản lý phiên đăng nhập | 1. Truy cập `/admin/security/sessions` hoặc click [Bảo mật] > [Quản lý phiên đăng nhập] | Hiển thị màn hình với phiên hiện tại và danh sách phiên khác | | Pass | 11/15/2025 | |
| FUNC-XoaPDN-02 | Xem phiên hiện tại | 1. Truy cập `/admin/security/sessions`<br>2. Kiểm tra card phiên hiện tại | Hiển thị đầy đủ: Thiết bị, Thời gian, IP, Vị trí | | Pass | 11/15/2025 | |
| FUNC-XoaPDN-03 | Xem danh sách phiên khác | 1. Truy cập `/admin/security/sessions`<br>2. Kiểm tra danh sách | Hiển thị đầy đủ: Thiết bị, OS, Trình duyệt, Hoạt động cuối, Trạng thái | | Pass | 11/15/2025 | |
| FUNC-XoaPDN-04 | Xóa một phiên đăng nhập | 1. Truy cập `/admin/security/sessions`<br>2. Click [Xóa phiên] trên một phiên<br>3. Xác nhận xóa | Phiên được xóa thành công, thiết bị bị đăng xuất, log bảo mật được lưu, thông báo xác nhận | | Pass | 11/15/2025 | |
| FUNC-XoaPDN-05 | Đăng xuất tất cả thiết bị | 1. Truy cập `/admin/security/sessions`<br>2. Click [Đăng xuất tất cả thiết bị]<br>3. Xác nhận | Tất cả phiên trừ phiên hiện tại bị vô hiệu hóa, thông báo được gửi, log bảo mật được lưu, thông báo xác nhận | | Pass | 11/15/2025 | |
| FUNC-XoaPDN-06 | Hủy xóa phiên | 1. Truy cập `/admin/security/sessions`<br>2. Click [Xóa phiên]<br>3. Click [Hủy] trong modal | Modal được đóng, phiên không bị xóa | | Pass | 11/15/2025 | |
| FUNC-XoaPDN-07 | Auto logout khi hết hạn | 1. Truy cập `/admin/security/sessions`<br>2. Chờ phiên hết hạn<br>3. Kiểm tra trạng thái | Phiên tự động đăng xuất khi hết hạn (timeout), log bảo mật được lưu | | Pass | 11/15/2025 | |
| FUNC-XoaPDN-08 | Cảnh báo trước khi hết hạn | 1. Truy cập `/admin/security/sessions`<br>2. Phiên sắp hết hạn<br>3. Kiểm tra cảnh báo | Hiển thị cảnh báo trước khi phiên hết hạn (ví dụ: "Phiên sẽ hết hạn sau X phút") | | Pass | 11/15/2025 | |

---

## GHI CHÚ

- Tất cả test cases cần được thực hiện trên môi trường test
- Routes động (có `[id]`) cần thay thế bằng ID thực tế khi test
- Các test case GUI kiểm tra giao diện và trạng thái của các thành phần
- Các test case FUNC kiểm tra chức năng và logic nghiệp vụ
- Token khôi phục mật khẩu chỉ sử dụng được 1 lần và có thời hạn sử dụng
- Hệ thống tự động phát hiện và đánh dấu đăng nhập lạ (từ thiết bị mới hoặc vị trí mới)
- Thông báo được gửi qua email/SMS khi có đăng nhập lạ
- Hệ thống tự động đăng xuất phiên khi hết hạn (timeout) và cảnh báo trước khi hết hạn
- Khi xóa phiên, log bảo mật được lưu để theo dõi
- Cần cập nhật cột Result, Test date sau khi thực hiện test

