# Test Case Template - Chức năng bảo mật (Nhân viên)

## Module Code
**Giao lộ 19: Họcl6c (Nhân viên)**

## Test Requirement
1. Khôi phục mật khẩu (quên mật khẩu + đặt lại)
2. Lịch sử đăng nhập & cảnh báo bất thường
3. Quản lý và xóa phiên đăng nhập

---

## Test Summary

### Người lớp Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 29 |
| **Fail** | 0 |
| **Untested** | 0 |
| **N/A** | 0 |
| **Number of Test cases** | 29 |

---

## Test Cases

### Function: Khôi phục mật khẩu

#### Check GUI: `/nhanvien/auth/forgot-password`

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-BM-FP-01** | Kiểm tra layout trang khôi phục | 1. Từ trang đăng nhập click `Quên mật khẩu` | Trang hiển thị Card với CardHeader (Title `Khôi phục mật khẩu`, Description “Nhập email...”), Alert hướng dẫn, Input `Email`, Button `Gửi liên kết đặt lại mật khẩu` (full width) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-BM-FP-02** | Kiểm tra label & placeholder | 1. Quan sát Input | Label `Email`, placeholder `nhanvien@bookstore.com`, input type email với border mặc định | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-BM-FP-03** | Kiểm tra thông báo trạng thái | 1. Gửi form (mock) | Alert text `Đang gửi link khôi phục...` hoặc `Link đã được gửi thành công` hiển thị bên dưới | FUNC-BM-FP-01 | Pass | 11/15/2015 | |
| **GUI-BM-FP-04** | Kiểm tra Radio phương thức xác thực (tài liệu) | 1. Kiểm tra phần `Phương thức xác thực` (theo tài liệu) | Các tùy chọn Email/SMS hiển thị radio button, mô tả “Hệ thống sẽ gửi link qua phương thức đã chọn” | FUNC-BM-FP-02 | Pass | 11/15/2015 | |
| **GUI-BM-FP-05** | Kiểm tra khối OTP & câu hỏi bảo mật | 1. Chọn phương thức OTP/câu hỏi bảo mật | Hiển thị input nhập OTP 6 số, dropdown câu hỏi bảo mật, input trả lời, Button `Tạo mã OTP` | FUNC-BM-FP-03 | Pass | 11/15/2015 | |

---

#### Check FUNC: Khôi phục mật khẩu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-BM-FP-01** | Gửi link khôi phục hợp lệ | 1. Nhập email hợp lệ `nv@example.com`<br>2. Chọn phương thức Email<br>3. Nhấn `Gửi` | Hiển thị toast success, Alert “Link đã được gửi”, hệ thống tạo token và ghi log khôi phục | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-BM-FP-02** | Chọn phương thức SMS | 1. Chọn radio `Gửi qua SMS`<br>2. Nhập số điện thoại hợp lệ | Hệ thống gửi OTP/link qua SMS, hiển thị thông báo “Đã gửi OTP tới SĐT...” | FUNC-BM-FP-01 | Pass | 11/15/2015 | |
| **FUNC-BM-FP-03** | Xác thực OTP đúng | 1. Nhấn `Tạo mã OTP`<br>2. Nhập mã hợp lệ trong ô OTP<br>3. Submit | Chấp nhận OTP, chuyển sang màn đặt mật khẩu mới | FUNC-BM-FP-02 | Pass | 11/15/2015 | |
| **FUNC-BM-FP-04** | OTP sai hoặc hết hạn | 1. Nhập mã sai/ quá 15 phút<br>2. Submit | Hiển thị lỗi `OTP không chính xác hoặc đã hết hạn`, cho phép yêu cầu lại | FUNC-BM-FP-03 | Pass | 11/15/2015 | |
| **FUNC-BM-FP-05** | Câu hỏi bảo mật sai | 1. Chọn câu hỏi bảo mật<br>2. Nhập sai câu trả lời 3 lần | Khóa chức năng 5 phút, thông báo `Bạn đã nhập sai quá số lần cho phép` | FUNC-BM-FP-01 | Pass | 11/15/2015 | |
| **FUNC-BM-FP-06** | Đặt lại mật khẩu mới hợp lệ | 1. Sau khi vào trang đặt mật khẩu, nhập mật khẩu mới (>=8 ký tự, hoa/thường/số/ký tự đặc biệt)<br>2. Confirm khớp | Hiển thị success `Mật khẩu đã được đặt lại`, mật khẩu cũ vô hiệu, tự chuyển về màn đăng nhập | FUNC-BM-FP-03 | Pass | 11/15/2015 | |
| **FUNC-BM-FP-07** | Đặt lại mật khẩu không đạt chuẩn | 1. Nhập mật khẩu <8 ký tự hoặc thiếu ký tự đặc biệt | Validation hiển thị `Mật khẩu phải có ...`, không cho lưu | FUNC-BM-FP-06 | Pass | 11/15/2015 | |

---

### Function: Lịch sử đăng nhập & cảnh báo

#### Check GUI: `/nhanvien/security/login-history`

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-BM-LH-01** | Kiểm tra Card tiêu đề | 1. Truy cập `/nhanvien/security/login-history` | CardTitle `Lịch sử đăng nhập`, CardDescription “Thời gian, địa chỉ IP, thiết bị, vị trí và trạng thái` | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-BM-LH-02** | Kiểm tra Alert cảnh báo | 1. Quan sát Alert đầu trang | Alert text “Chúng tôi nhận thấy các đăng nhập bất thường...” hiển thị icon + nền `bg-muted` | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-BM-LH-03** | Kiểm tra bộ lọc thời gian & trạng thái | 1. Kiểm tra grid bộ lọc | Hai Select với Label `Khoảng thời gian`, `Trạng thái`, options `Tất cả/Tuần này/...` và `Thành công/Thất bại` | FUNC-BM-LH-01 | Pass | 11/15/2015 | |
| **GUI-BM-LH-04** | Kiểm tra card danh sách log | 1. Cuộn xuống danh sách | Mỗi log hiển thị Card border-dashed, grid 5 cột (time+IP, device+OS, browser+location, Badge trạng thái, ID) | FUNC-BM-LH-01 | Pass | 11/15/2015 | |
| **GUI-BM-LH-05** | Kiểm tra badge trạng thái | 1. So sánh log thành công và thất bại | Thành công dùng Badge variant secondary `THÀNH CÔNG`, thất bại variant destructive `THẤT BẠI` | FUNC-BM-LH-01 | Pass | 11/15/2015 | |

---

#### Check FUNC: Lịch sử đăng nhập

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-BM-LH-01** | Tải danh sách log | 1. Truy cập trang | Hệ thống gọi API lịch sử, hiển thị dữ liệu theo thời gian giảm dần | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-BM-LH-02** | Lọc theo trạng thái thành công | 1. Chọn `Trạng thái = Thành công` | Danh sách chỉ còn log `status = success` (badge xanh), card thất bại ẩn | FUNC-BM-LH-01 | Pass | 11/15/2015 | |
| **FUNC-BM-LH-03** | Lọc theo trạng thái thất bại | 1. Chọn `Thất bại` | Chỉ hiển thị log thất bại, Alert gợi ý đổi mật khẩu | FUNC-BM-LH-01 | Pass | 11/15/2015 | |
| **FUNC-BM-LH-04** | Lọc theo khoảng thời gian | 1. Chọn `Tuần này` | Chỉ hiển thị log trong 7 ngày gần nhất, nếu không có data hiển thị empty state | FUNC-BM-LH-01 | Pass | 11/15/2015 | |
| **FUNC-BM-LH-05** | Gửi cảnh báo đăng nhập bất thường | 1. Hệ thống phát hiện IP/thiết bị lạ | Tự động gửi email/app notification cho nhân viên, ghi log “Cảnh báo đã gửi”, hiển thị Alert trên trang | FUNC-BM-LH-01 | Pass | 11/15/2015 | |

---

### Function: Quản lý phiên đăng nhập

#### Check GUI: `/nhanvien/security/sessions`

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-BM-SE-01** | Kiểm tra Card tiêu đề | 1. Truy cập `/nhanvien/security/sessions` | CardTitle `Bảo mật - Phiên đăng nhập`, mô tả “Quản lý và xóa phiên đăng nhập`, Alert cảnh báo | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-BM-SE-02** | Kiểm tra thông tin phiên | 1. Quan sát nội dung | Text hiển thị `Phiên hiện tại` với thiết bị, IP, thời gian; `Phiên khác` liệt kê iPhone Safari... | FUNC-BM-SE-01 | Pass | 11/15/2015 | |
| **GUI-BM-SE-03** | Kiểm tra Dialog đăng xuất | 1. Click nút `Đăng xuất` | DialogTitle `Xác nhận đăng xuất`, radio chọn phạm vi, Textarea ghi chú, Buttons `Hủy`, `Đăng xuất` | FUNC-BM-SE-02 | Pass | 11/15/2015 | |

---

#### Check FUNC: Quản lý & xóa phiên

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-BM-SE-01** | Đăng xuất phiên hiện tại | 1. Mở dialog<br>2. Chọn `Đăng xuất chỉ phiên hiện tại`<br>3. Confirm | Phiên hiện tại bị revoke, user chuyển về `/nhanvien/auth/login`, lịch sử ghi `logout current session` | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-BM-SE-02** | Đăng xuất tất cả phiên khác | 1. Chọn radio `Đăng xuất tất cả phiên khác` | Chỉ giữ phiên hiện tại, các refresh token khác bị hủy, hiển thị toast success | FUNC-BM-SE-01 | Pass | 11/15/2015 | |
| **FUNC-BM-SE-03** | Đăng xuất tất cả phiên | 1. Chọn `Đăng xuất tất cả các phiên` | User bị logout khỏi mọi thiết bị, yêu cầu đăng nhập lại, hiển thị cảnh báo “Đã đăng xuất tất cả phiên” | FUNC-BM-SE-01 | Pass | 11/15/2015 | |
| **FUNC-BM-SE-04** | Ghi chú đăng xuất | 1. Nhập ghi chú vào textarea trước khi confirm | Ghi chú lưu kèm log logout để quản trị tra cứu, hiển thị trong lịch sử bảo mật | FUNC-BM-SE-01 | Pass | 11/15/2015 | |
| **FUNC-BM-SE-05** | Hủy dialog | 1. Click `Hủy` | Dialog đóng, không thay đổi trạng thái phiên | FUNC-BM-SE-01 | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn MDX để dễ dàng quản lý và cập nhật test cases.*

