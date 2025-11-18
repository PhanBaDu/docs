# Test Case Template - Quản lý tài khoản (Nhân viên kho)

## Module Code
**Giao lộ 19: Họcl6c (Nhân viên kho)**

## Test Requirement
1. Đăng nhập hệ thống `/nhanvienkho/auth/login`
2. Khôi phục mật khẩu `/nhanvienkho/auth/forgot-password`
3. Quản lý thông tin cá nhân `/nhanvienkho/account`
4. Đổi mật khẩu `/nhanvienkho/account/change-password`
5. Đăng xuất hệ thống `/nhanvienkho/logout`

---

## Test Summary

### Người lớp Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 25 |
| **Fail** | 0 |
| **Untested** | 0 |
| **N/A** | 0 |
| **Number of Test cases** | 25 |

---

## Test Cases

### Function: Đăng nhập hệ thống

#### Check GUI: `/nhanvienkho/auth/login`

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-KW-LOGIN-01** | Kiểm tra bố cục form đăng nhập | 1. Mở `/nhanvienkho/auth/login` | Card trung tâm max-w-md với header chứa logo avatar chữ `K`, `CardTitle` “Đăng nhập - Nhân viên kho”, `CardDescription` “Truy cập hệ thống quản lý kho”; form gồm Input `Tên đăng nhập hoặc Email`, Input password với placeholder `••••••••`, checkbox `Ghi nhớ đăng nhập`, link `Quên mật khẩu?`, nút `Đăng nhập` full width | FUNC-KW-LOGIN-01 | Pass | 11/15/2015 | |
| **GUI-KW-LOGIN-02** | Kiểm tra vùng thông báo | 1. Nhập sai để trigger lỗi | Sau submit hiển thị `Alert variant="destructive"` chứa thông báo lỗi; khi thành công hiển thị `Alert` thường với text “Đăng nhập thành công” | FUNC-KW-LOGIN-02 | Pass | 11/15/2015 | |

---

#### Check FUNC: Đăng nhập

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-KW-LOGIN-01** | Đăng nhập hợp lệ | 1. Nhập username hợp lệ<br>2. Nhập mật khẩu đúng<br>3. Click `Đăng nhập` | Form submit thành công, alert “Đăng nhập thành công”, chuyển hướng dashboard `/nhanvienkho` trong vòng 2s, lưu log đăng nhập (thời gian + IP) | None | Pass | 11/15/2015 | |
| **FUNC-KW-LOGIN-02** | Sai thông tin đăng nhập | 1. Nhập mật khẩu sai | Hiển thị alert đỏ “Tên đăng nhập hoặc mật khẩu không đúng”, reset trường mật khẩu, không chuyển trang | None | Pass | 11/15/2015 | |
| **FUNC-KW-LOGIN-03** | Bật Ghi nhớ đăng nhập | 1. Tick checkbox `Ghi nhớ đăng nhập`<br>2. Đăng nhập thành công | Token refresh lưu 30 ngày, lần sau tự điền, hiển thị thông báo “Đã bật ghi nhớ đăng nhập trên thiết bị này” | FUNC-KW-LOGIN-01 | Pass | 11/15/2015 | |

---

### Function: Khôi phục mật khẩu

#### Check GUI: `/nhanvienkho/auth/forgot-password`

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-KW-FP-01** | Kiểm tra layout trang khôi phục | 1. Mở `/nhanvienkho/auth/forgot-password` | Card max-w-lg, `CardTitle` “Khôi phục mật khẩu”, `CardDescription` hướng dẫn nhập email/SĐT, form có Input `Email hoặc Số điện thoại`, RadioGroup `Gửi qua Email/SMS`, 2 buttons `Gửi link khôi phục` (primary) và `Hủy` (outline), alert trạng thái | FUNC-KW-FP-01 | Pass | 11/15/2015 | |
| **GUI-KW-FP-02** | Kiểm tra Radio phương thức xác thực | 1. Click từng radio | RadioGroup thay đổi highlight, label cập nhật, giữ layout flex items-center | FUNC-KW-FP-02 | Pass | 11/15/2015 | |

---

#### Check FUNC: Khôi phục mật khẩu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-KW-FP-01** | Gửi link qua email | 1. Nhập email hợp lệ<br>2. Chọn `Gửi qua Email`<br>3. Click gửi | Alert hiển thị “Link khôi phục đã được gửi...”, hệ thống tạo token 15 phút, email chứa link reset | FUNC-KW-LOGIN-01 | Pass | 11/15/2015 | |
| **FUNC-KW-FP-02** | Gửi OTP qua SMS | 1. Nhập số điện thoại hợp lệ<br>2. Chọn `Gửi qua SMS` | Hệ thống gửi OTP 6 số, hiển thị hướng dẫn nhập OTP ở bước kế, ghi log kênh SMS | FUNC-KW-FP-01 | Pass | 11/15/2015 | |
| **FUNC-KW-FP-03** | Nhập thông tin không hợp lệ | 1. Để trống email/SĐT<br>2. Gửi | Hiển thị lỗi `Vui lòng nhập email hoặc số điện thoại hợp lệ`, không gọi API | None | Pass | 11/15/2015 | |

---

### Function: Quản lý thông tin cá nhân

#### Check GUI: `/nhanvienkho/account`

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-KW-ACC-01** | Kiểm tra tiêu đề trang | 1. Mở `/nhanvienkho/account` | Hiển thị `h1` “Thông tin cá nhân” (text-2xl font-bold) và mô tả “Quản lý thông tin nhân viên kho” | FUNC-KW-ACC-01 | Pass | 11/15/2015 | |
| **GUI-KW-ACC-02** | Kiểm tra card Hồ sơ | 1. Quan sát card đầu | CardTitle `Hồ sơ`, Thumbnail avatar chữ `K`, button `Tải lên ảnh mới`, thông tin `Chức vụ`, `Trạng thái tài khoản` với `Badge Hoạt động` | FUNC-KW-ACC-01 | Pass | 11/15/2015 | |
| **GUI-KW-ACC-03** | Kiểm tra form thông tin liên hệ | 1. Quan sát card thứ hai | Grid md:grid-cols-2: các Input `Họ và tên`, `Số điện thoại`, `Email`, Textarea `Địa chỉ`, Input date `Ngày sinh`, Input `Giới tính`; buttons cuối trang “Lưu thay đổi”, “Hủy” | FUNC-KW-ACC-02 | Pass | 11/15/2015 | |

---

#### Check FUNC: Thông tin cá nhân

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-KW-ACC-01** | Xem thông tin cá nhân | 1. Đăng nhập<br>2. Truy cập `/nhanvienkho/account` | Dữ liệu hiển thị đúng profile DB (tên, sđt, email, địa chỉ, ngày sinh, giới tính, chức vụ, trạng thái), avatar placeholder nếu chưa có ảnh | FUNC-KW-LOGIN-01 | Pass | 11/15/2015 | |
| **FUNC-KW-ACC-02** | Cập nhật thông tin hợp lệ | 1. Sửa SĐT, địa chỉ<br>2. Click `Lưu thay đổi` | Validate thành công, hiển thị toast success “Đã lưu thông tin”, DB cập nhật, lịch sử thay đổi được log | FUNC-KW-ACC-01 | Pass | 11/15/2015 | |
| **FUNC-KW-ACC-03** | Validation email sai định dạng | 1. Nhập email `abc`<br>2. Lưu | Hiển thị lỗi tại field email “Email không hợp lệ”, không lưu | FUNC-KW-ACC-01 | Pass | 11/15/2015 | |

---

### Function: Đổi mật khẩu

#### Check GUI: `/nhanvienkho/account/change-password`

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-KW-PW-01** | Kiểm tra bố cục | 1. Mở trang | Hiển thị `h1` “Đổi mật khẩu”, mô tả yêu cầu độ mạnh, Card với form gồm 3 Input password (current/new/confirm) và button pair `Đổi mật khẩu` & `Hủy`, Alert hiển thị trạng thái | FUNC-KW-PW-01 | Pass | 11/15/2015 | |
| **GUI-KW-PW-02** | Kiểm tra thông báo | 1. Submit thành công<br>2. Submit lỗi | Sau thành công hiển thị Alert thường “Đổi mật khẩu thành công”; khi lỗi hiển thị Alert đỏ với message tương ứng | FUNC-KW-PW-01 | Pass | 11/15/2015 | |

---

#### Check FUNC: Đổi mật khẩu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-KW-PW-01** | Đổi mật khẩu thành công | 1. Nhập mật khẩu hiện tại đúng<br>2. Nhập mật khẩu mới hợp lệ<br>3. Submit | Hệ thống xác thực, cập nhật mật khẩu, logout các thiết bị khác, Alert success, ghi log bảo mật | FUNC-KW-LOGIN-01 | Pass | 11/15/2015 | |
| **FUNC-KW-PW-02** | Sai mật khẩu hiện tại | 1. Nhập mật khẩu hiện tại sai | Hiển thị lỗi “Mật khẩu hiện tại không đúng”, không lưu | FUNC-KW-PW-01 | Pass | 11/15/2015 | |
| **FUNC-KW-PW-03** | Mật khẩu mới không đạt yêu cầu | 1. Nhập mật khẩu mới < 8 ký tự | Hiển thị lỗi “Mật khẩu phải có ít nhất 8 ký tự...”, highlight field | FUNC-KW-PW-01 | Pass | 11/15/2015 | |
| **FUNC-KW-PW-04** | Hủy thao tác đổi mật khẩu | 1. Click `Hủy` | Form reset, không lưu thay đổi, điều hướng về `/nhanvienkho/account` | FUNC-KW-PW-01 | Pass | 11/15/2015 | |

---

### Function: Đăng xuất hệ thống

#### Check GUI: `/nhanvienkho/logout`

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-KW-LOGOUT-01** | Kiểm tra modal đăng xuất | 1. Đăng nhập rồi truy cập `/nhanvienkho/logout` | Card giữa màn hình với `CardTitle` “Đăng xuất hệ thống”, `CardDescription` hỏi xác nhận, 2 nút `Có, đăng xuất` (primary) và `Hủy` (outline) | FUNC-KW-LOGOUT-01 | Pass | 11/15/2015 | |

---

#### Check FUNC: Đăng xuất

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-KW-LOGOUT-01** | Đăng xuất thành công | 1. Click `Có, đăng xuất` | Phiên hiện tại bị revoke, cookie/token xóa, chuyển hướng `/nhanvienkho/auth/login`, hiển thị toast “Đã đăng xuất thành công” | FUNC-KW-LOGIN-01 | Pass | 11/15/2015 | |
| **FUNC-KW-LOGOUT-02** | Hủy đăng xuất | 1. Click `Hủy` | Quay lại trang trước (dashboard), phiên vẫn hoạt động, ghi log “Cancel logout” | FUNC-KW-LOGIN-01 | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn MDX để dễ dàng quản lý và cập nhật test cases.*

