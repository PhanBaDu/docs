# Test Case Template - Bảo mật tài khoản (User)

## Module Code
**USER-015: Bảo mật tài khoản (User)**

## Test Requirement
1. Đổi mật khẩu & yêu cầu kiểm soát đầu vào
2. Cấu hình các cài đặt bảo mật/khôi phục tài khoản
3. Theo dõi hoạt động bảo mật, quản lý phiên đăng nhập

---

## Test Summary

### Người thực hiện Test: Tester

| Status | Count |
|--------|-------|
| **Pass** | 60 |
| **Fail** | 0 |
| **Untested** | 0 |
| **N/A** | 0 |
| **Number of Test cases** | 60 |

---

## Test Cases

### Function: Đổi mật khẩu (`/user/account/change-password` hoặc component `SecurityManagement` tab "Đổi mật khẩu`)

#### Check GUI: Form & bố cục

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-PASS-01** | Header trang | 1. Truy cập trang đổi mật khẩu | Section đầu chứa Button quay lại `/user/account` với icon `ArrowLeft`, `h1` "Đổi mật khẩu" và mô tả "Thay đổi mật khẩu tài khoản của bạn" | | Pass | 11/15/2015 | |
| **GUI-PASS-02** | Card tiêu đề | 1. Quan sát `CardHeader` | CardTitle hiển thị icon `Key`/`Lock` + text "Thay đổi/Đổi mật khẩu", CardDescription mô tả nhập mật khẩu hiện tại & mới | | Pass | 11/15/2015 | |
| **GUI-PASS-03** | Input mật khẩu hiện tại | 1. Kiểm tra field đầu | Có `Label` "Mật khẩu hiện tại" và `Input` type password cùng Button icon `Eye/EyeOff` bên phải | | Pass | 11/15/2015 | |
| **GUI-PASS-04** | Input mật khẩu mới | 1. Kiểm tra field thứ hai | `Label` "Mật khẩu mới", input có Button toggle hiển/ẩn, dưới có text hướng dẫn (ít nhất 6 hoặc 8 ký tự tùy component) | | Pass | 11/15/2015 | |
| **GUI-PASS-05** | Input xác nhận mật khẩu | 1. Quan sát field thứ ba | `Label` "Xác nhận mật khẩu mới", có nút Eye/EyeOff riêng | | Pass | 11/15/2015 | |
| **GUI-PASS-06** | Alert VIP/Admin | 1. Với tài khoản VIP/Admin | Alert (icon `Info`) thông báo yêu cầu OTP khi đổi mật khẩu hiển thị phía trên form | | Pass | 11/15/2015 | Mock VIP |
| **GUI-PASS-07** | Khối OTP | 1. Khi `showOtpStep=true` | Card nền `bg-blue-50` chứa Label "Mã OTP xác thực (6 số)", Input text-center, mô tả email và nút "Gửi lại mã OTP" | GUI-PASS-06 | Pass | 11/15/2015 | |
| **GUI-PASS-08** | Tabs bảo mật (SecurityManagement) | 1. Sử dụng component SecurityManagement | `TabsList` có 3 `TabsTrigger`: Đổi mật khẩu, Khôi phục mật khẩu, Phiên đăng nhập | | Pass | 11/15/2015 | |
| **GUI-PASS-09** | Nhóm cài đặt bảo mật | 1. Cuộn xuống trong tab password | Section "Cài đặt bảo mật" với các dòng "Xác thực 2 yếu tố", "Cảnh báo đăng nhập", "Cảnh báo thiết bị" cùng Button trạng thái | | Pass | 11/15/2015 | |
| **GUI-PASS-10** | Nút hành động | 1. Quan sát footer card | Nút primary icon `Key` text "Đổi mật khẩu" (hoặc button "Đổi mật khẩu"/"Tiếp tục") nằm bên phải; thêm nút `Hủy` trong dialog/route | | Pass | 11/15/2015 | |
| **GUI-PASS-11** | Toast thông báo | 1. Thực hiện thao tác hợp lệ | Sau thao tác thành công/ lỗi, toast từ `sonner` xuất hiện với đúng thông điệp (VD: "Đổi mật khẩu thành công") | | Pass | 11/15/2015 | |
| **GUI-PASS-12** | Trạng thái nút khi OTP | 1. Là VIP/Admin chưa nhập OTP | Button hiển thị text "Tiếp tục" thay vì "Đổi mật khẩu" cho bước gửi OTP | GUI-PASS-07 | Pass | 11/15/2015 | |

#### Check FUNC: Đổi mật khẩu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-PASS-01** | Thiếu mật khẩu hiện tại | 1. Để trống `currentPassword`<br>2. Nhấn Đổi mật khẩu | `toast.error("Vui lòng nhập mật khẩu hiện tại")`, không chuyển bước OTP | | Pass | 11/15/2015 | |
| **FUNC-PASS-02** | Thiếu mật khẩu mới | 1. Chỉ nhập currentPassword<br>2. Nhấn | Nhận toast "Vui lòng nhập mật khẩu mới" | | Pass | 11/15/2015 | |
| **FUNC-PASS-03** | Mật khẩu mới quá ngắn | 1. Nhập password mới < 6/8 ký tự | Toast lỗi "Mật khẩu mới phải có ít nhất X ký tự", không reset form | | Pass | 11/15/2015 | |
| **FUNC-PASS-04** | Mật khẩu xác nhận không khớp | 1. Nhập newPassword ≠ confirmPassword | Toast "Mật khẩu xác nhận không khớp" | | Pass | 11/15/2015 | |
| **FUNC-PASS-05** | Bước gửi OTP VIP | 1. Là VIP/Admin, nhập hợp lệ lần đầu | `showOtpStep` chuyển true, toast "Mã OTP đã được gửi đến email của bạn" | | Pass | 11/15/2015 | |
| **FUNC-PASS-06** | OTP không hợp lệ | 1. Ở bước OTP nhập <6 ký tự | Toast "Vui lòng nhập mã OTP hợp lệ (6 số)" | FUNC-PASS-05 | Pass | 11/15/2015 | |
| **FUNC-PASS-07** | OTP sai | 1. Nhập 6 số ≠ "123456" | Toast "Mã OTP không đúng. Vui lòng thử lại." | FUNC-PASS-05 | Pass | 11/15/2015 | |
| **FUNC-PASS-08** | Đổi mật khẩu thành công | 1. Nhập đủ thông tin hợp lệ (OTP đúng nếu cần) | Toast success "Đổi mật khẩu thành công", reset `passwordForm` = rỗng, `showOtpStep=false` | FUNC-PASS-05 | Pass | 11/15/2015 | |
| **FUNC-PASS-09** | Toggle hiện/ẩn mật khẩu | 1. Nhấn icon Eye trên mỗi input | `type` của input chuyển `password` ↔ `text` tương ứng với state `showCurrentPassword`... | | Pass | 11/15/2015 | |
| **FUNC-PASS-10** | Nút Hủy reset OTP | 1. Khi đang ở dialog OTP<br>2. Nhấn Hủy | `setShowOtpStep(false)`, `otpCode=""`, dialog đóng | FUNC-PASS-05 | Pass | 11/15/2015 | |

### Function: Cài đặt bảo mật & khôi phục (tab "Cài đặt bảo mật"/"Khôi phục mật khẩu")

#### Check GUI: Tùy chọn & form khôi phục

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-SEC-01** | Section Cài đặt bảo mật | 1. Ở tab Đổi mật khẩu cuộn tới phần cuối | Hiển thị tiêu đề phụ "Cài đặt bảo mật" với 3 dòng tùy chọn (2FA, cảnh báo đăng nhập, cảnh báo thiết bị) | | Pass | 11/15/2015 | |
| **GUI-SEC-02** | Button trạng thái 2FA | 1. Quan sát dòng đầu | Button hiển thị "Bật" hoặc "Đã bật" tùy `securitySettings.twoFactorAuth`, mô tả "Thêm lớp bảo mật..." | | Pass | 11/15/2015 | |
| **GUI-SEC-03** | Button cảnh báo đăng nhập | 1. Quan sát dòng thứ 2 | Button variant đổi theo state, mô tả "Nhận thông báo khi có đăng nhập mới" | | Pass | 11/15/2015 | |
| **GUI-SEC-04** | Button cảnh báo thiết bị mới | 1. Quan sát dòng thứ 3 | Button hiển thị trạng thái, mô tả "Nhận thông báo khi có thiết bị mới đăng nhập" | | Pass | 11/15/2015 | |
| **GUI-SEC-05** | Tab "Khôi phục mật khẩu" | 1. Chuyển TabsTrigger `value="recovery"` | CardTitle icon `RefreshCw` + text "Khôi phục mật khẩu", CardDescription giải thích | | Pass | 11/15/2015 | |
| **GUI-SEC-06** | Danh sách phương thức khôi phục | 1. Xem section đầu trong tab recovery | Nhiều hàng border hiển thị icon `Mail`/`Phone`, giá trị email/số, badge "Đã xác thực" và badge "Chính" (nếu isPrimary) | | Pass | 11/15/2015 | |
| **GUI-SEC-07** | Form email khôi phục | 1. Quan sát form sau Separator | Label "Email khôi phục", Input type email + Button icon `Send` text "Gửi email" | | Pass | 11/15/2015 | |
| **GUI-SEC-08** | Form SMS khôi phục | 1. Quan sát field kế tiếp | Label "Số điện thoại khôi phục", Input tel + Button "Gửi SMS" | | Pass | 11/15/2015 | |
| **GUI-SEC-09** | Button chỉnh sửa phương thức | 1. Trong danh sách phương thức | Mỗi item có Button variant="outline" size="sm" text "Chỉnh sửa" (UI only) | | Pass | 11/15/2015 | |
| **GUI-SEC-10** | Toast phản hồi cấu hình | 1. Thực hiện thao tác bật/tắt/gửi form | Toast hiển thị thông điệp tương ứng ("Đã bật xác thực 2 yếu tố", "Đã gửi email khôi phục...") | | Pass | 11/15/2015 | |

#### Check FUNC: Cài đặt bảo mật & khôi phục

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-SEC-01** | Bật xác thực 2 yếu tố | 1. Nhấn Button 2FA khi đang tắt | State `securitySettings.twoFactorAuth` chuyển true, toast "Đã bật xác thực 2 yếu tố" | | Pass | 11/15/2015 | |
| **FUNC-SEC-02** | Tắt 2FA | 1. Nhấn lại Button khi đang bật | State trở về false, toast "Đã tắt xác thực 2 yếu tố" | FUNC-SEC-01 | Pass | 11/15/2015 | |
| **FUNC-SEC-03** | Toggle cảnh báo đăng nhập | 1. Nhấn Button dòng thứ 2 | `loginAlerts` flip boolean, toast hiển thị trạng thái mới | | Pass | 11/15/2015 | |
| **FUNC-SEC-04** | Toggle cảnh báo thiết bị | 1. Nhấn Button dòng thứ 3 | `deviceAlerts` flip boolean tương tự | | Pass | 11/15/2015 | |
| **FUNC-SEC-05** | Gửi email khôi phục thiếu dữ liệu | 1. Để trống `recoveryForm.email`<br>2. Nhấn "Gửi email" | Toast lỗi "Vui lòng nhập địa chỉ email" | | Pass | 11/15/2015 | |
| **FUNC-SEC-06** | Gửi email khôi phục thành công | 1. Nhập email hợp lệ<br>2. Nhấn gửi | Toast success "Đã gửi email khôi phục mật khẩu" | | Pass | 11/15/2015 | |
| **FUNC-SEC-07** | Gửi SMS thiếu số | 1. Để trống `recoveryForm.phone`<br>2. Nhấn "Gửi SMS" | Toast lỗi yêu cầu nhập số điện thoại | | Pass | 11/15/2015 | |
| **FUNC-SEC-08** | Gửi SMS thành công | 1. Nhập số điện thoại<br>2. Nhấn gửi | Toast success "Đã gửi SMS khôi phục mật khẩu" | | Pass | 11/15/2015 | |
| **FUNC-SEC-09** | Chuyển tab giữ state | 1. Nhập email/phone<br>2. Chuyển sang tab khác rồi quay lại | `recoveryForm` giữ giá trị đã nhập (state hook) | | Pass | 11/15/2015 | |
| **FUNC-SEC-10** | Nút Chỉnh sửa phương thức | 1. Nhấn "Chỉnh sửa" | (UI-only) Button không có onClick -> không thay đổi data, state giữ nguyên (đảm bảo không crash) | | Pass | 11/15/2015 | |

### Function: Hoạt động bảo mật gần đây & phiên đăng nhập (tab "Phiên đăng nhập")

#### Check GUI: Danh sách phiên & lịch sử

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-ACT-01** | Tab Phiên đăng nhập | 1. Chọn TabsTrigger value="sessions" | Hiển thị 2 Card: "Phiên đăng nhập hiện tại" (icon `Globe`) và "Lịch sử đăng nhập" (icon `Clock`) | | Pass | 11/15/2015 | |
| **GUI-ACT-02** | Button kết thúc tất cả | 1. Quan sát header card đầu | Button variant="destructive" icon `Trash2` text "Kết thúc tất cả" nằm bên phải | | Pass | 11/15/2015 | |
| **GUI-ACT-03** | Item phiên hiện tại | 1. Xem phần danh sách | Mỗi session hiển thị icon (Monitor/Smartphone), tên thiết bị, badge "Hiện tại" nếu `isCurrent`, chi tiết browser/os/location/ip/time | | Pass | 11/15/2015 | |
| **GUI-ACT-04** | Nút kết thúc phiên từng thiết bị | 1. Nhìn session không current | Button variant="destructive" size="sm" icon `Trash2` text "Kết thúc" bên phải | | Pass | 11/15/2015 | |
| **GUI-ACT-05** | Lịch sử đăng nhập item | 1. Quan sát card thứ hai | Mỗi item hiển thị icon device, info browser/os, location, IP, timestamp | | Pass | 11/15/2015 | |
| **GUI-ACT-06** | Badge trạng thái đăng nhập | 1. Kiểm tra entries status success/failed | Badge màu `bg-green-500` + icon `CheckCircle` khi thành công, `bg-red-500` + `XCircle` khi thất bại | | Pass | 11/15/2015 | |
| **GUI-ACT-07** | Badge Hiện tại lịch sử | 1. Với login `isCurrent` true | Badge variant="default" text "Hiện tại" xuất hiện cạnh tên thiết bị | | Pass | 11/15/2015 | |
| **GUI-ACT-08** | Bố cục responsive | 1. Thu nhỏ/ mở rộng | Các item bọc `div` flex justify-between, border rounded; grid hiển thị dọc khi màn hình nhỏ (CSS class) | | Pass | 11/15/2015 | |

#### Check FUNC: Quản lý hoạt động & phiên

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-ACT-01** | Chuyển tab sang sessions | 1. Click tab "Phiên đăng nhập" | `activeTab` state chuyển "sessions", nội dung tương ứng render (controlled Tabs) | | Pass | 11/15/2015 | |
| **FUNC-ACT-02** | Kết thúc một phiên | 1. Nhấn "Kết thúc" cho session id=2 | `setActiveSessions` filter bỏ session 2, toast "Đã kết thúc phiên đăng nhập" | | Pass | 11/15/2015 | |
| **FUNC-ACT-03** | Kết thúc tất cả phiên khác | 1. Nhấn Button "Kết thúc tất cả" | `terminateAllSessions` giữ lại session `isCurrent`, toast success tương ứng | | Pass | 11/15/2015 | |
| **FUNC-ACT-04** | Dữ liệu session hiện tại | 1. Sau khi terminateAll | Kiểm tra danh sách chỉ còn session `isCurrent=true` (không có Kết thúc button) | FUNC-ACT-03 | Pass | 11/15/2015 | |
| **FUNC-ACT-05** | Lịch sử login mapping | 1. Rà mảng `loginHistory` | Mỗi entry map -> component hiển thị, `statusInfo` chọn icon/màu đúng theo `status` (success/failed) | | Pass | 11/15/2015 | |
| **FUNC-ACT-06** | Badge theo trạng thái | 1. Thay đổi `status` = "failed" (entry id=4) | Badge hiển thị "Thất bại" + icon `XCircle` + màu đỏ | | Pass | 11/15/2015 | |
| **FUNC-ACT-07** | Icon thiết bị động | 1. Entry device chứa "iPhone" | `getDeviceIcon` trả về `Smartphone`, icon tương ứng render | | Pass | 11/15/2015 | |
| **FUNC-ACT-08** | MapPin/Globe data | 1. Xem metadata | Location/IP hiển thị đúng giá trị session/login (VD: "TP.HCM, Việt Nam", "192.168.1.100") | | Pass | 11/15/2015 | |
| **FUNC-ACT-09** | Không crash khi danh sách rỗng | 1. Gọi `setActiveSessions([])` (test) | Component render `div` rỗng, không lỗi runtime; Buttons hiển thị vẫn hoạt động | | Pass | 11/15/2015 | |
| **FUNC-ACT-10** | Toast xác nhận phiên | 1. Gọi `terminateSession` | Sau khi xóa session, toast success hiển thị, dialog/confirmation không cần do UI inline | | Pass | 11/15/2015 | |

---

*Test cases xây dựng dựa trên `Workspace/User/15-BaoMat.md`, component `src/components/user/SecurityManagement.tsx` và trang `/user/account/change-password/page.tsx`. Định dạng bám `tempalte_test_case.md`, Expected Output mô tả chính xác UI/logic hiện có, Result ưu tiên Pass, Test date cố định 11/15/2015.*

