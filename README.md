# Test Case Template - Bảo mật (Nhân viên kho)

## Module Code
**Giao lộ 19: Họcl6c (Nhân viên kho)**

## Test Requirement
1. Quản lý phiên đăng nhập `/nhanvienkho/security/sessions`
2. Theo dõi hoạt động hệ thống `/nhanvienkho/security/activity` *(theo tài liệu @NhanVienKho/7-BaoMat.md)*
3. Báo cáo bảo mật `/nhanvienkho/security/reports`
4. Cảnh báo bảo mật `/nhanvienkho/security/alerts`

---

## Test Summary

### Người lớp Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 32 |
| **Fail** | 0 |
| **Untested** | 0 |
| **N/A** | 0 |
| **Number of Test cases** | 32 |

---

## Test Cases

### Function: Quản lý phiên đăng nhập

#### Check GUI: `/nhanvienkho/security/sessions`

| ID | Test Case Description | Test Case Procedure | Expected Output | Dependence | Result | Test date | Note |
|----|----------------------|---------------------|----------------|------------|--------|-----------|------|
| **GUI-KW-SEC-SESS-01** | Card phiên hiện tại | 1. Đăng nhập kho<br>2. Mở `/security/sessions` | Card hiển thị `Mã phiên SESS001`, `Thời gian đăng nhập 2023-11-20 08:30`, `IP 192.168.1.100`, `Trạng thái Badge Hoạt động` | None | Pass | 11/15/2015 | |
| **GUI-KW-SEC-SESS-02** | Bộ lọc phiên | 1. Quan sát card `Bộ lọc phiên đăng nhập` | Inputs `Từ ngày`, `Đến ngày`, Select `Trạng thái` (Tất cả/Hoạt động/Đã kết thúc/Bị khóa/Bất thường), Input `IP` | None | Pass | 11/15/2015 | |
| **GUI-KW-SEC-SESS-03** | Bảng phiên đăng nhập | 1. Quan sát table | Cột Mã phiên, Thời gian đăng nhập, Địa chỉ IP, Thiết bị, Trạng thái, Thao tác (buttons Xem chi tiết/Kết thúc/Khóa) | None | Pass | 11/15/2015 | |
| **GUI-KW-SEC-SESS-04** | Dialog xóa lịch sử | 1. Click `Xóa lịch sử` (Kết thúc tất cả) | `DialogTitle Xóa lịch sử phiên đăng nhập`, mô tả `Hành động không thể hoàn tác`, buttons `Hủy`, `Xóa` | None | Pass | 11/15/2015 | |

#### Check FUNC

| ID | Test Case Description | Test Case Procedure | Expected Output | Dependence | Result | Test date | Note |
|----|----------------------|---------------------|----------------|------------|--------|-----------|------|
| **FUNC-KW-SEC-SESS-01** | Lọc theo trạng thái hoạt động | 1. Set filter `Trạng thái = Hoạt động` | Bảng chỉ hiển thị các phiên active, badge green | None | Pass | 11/15/2015 | |
| **FUNC-KW-SEC-SESS-02** | Kết thúc phiên đơn lẻ | 1. Click `Kết thúc` trên SESS001 | Phiên chuyển `Đã kết thúc`, người dùng bị đăng xuất, log action | None | Pass | 11/15/2015 | |
| **FUNC-KW-SEC-SESS-03** | Khóa phiên bất thường | 1. Chọn phiên suspicious -> `Khóa phiên` | Trạng thái Badge `Bị khóa`, notification gửi tới user + admin | None | Pass | 11/15/2015 | |
| **FUNC-KW-SEC-SESS-04** | Kết thúc tất cả phiên khác | 1. Click button `Kết thúc tất cả` | Tất cả phiên ngoại trừ hiện tại bị revoke, toast success | None | Pass | 11/15/2015 | |
| **FUNC-KW-SEC-SESS-05** | Xóa lịch sử phiên | 1. Trong dialog, click `Xóa` | Phiên đã kết thúc được xóa khỏi bảng, log `history_delete` | None | Pass | 11/15/2015 | |

---

### Function: Theo dõi hoạt động hệ thống *(được mô tả tại tài liệu @NhanVienKho/7-BaoMat.md)*

#### Check GUI: `/nhanvienkho/security/activity`

| ID | Test Case Description | Test Case Procedure | Expected Output | Dependence | Result | Test date | Note |
|----|----------------------|---------------------|----------------|------------|--------|-----------|------|
| **GUI-KW-SEC-ACT-01** | Bộ lọc hoạt động | 1. Mở `/security/activity` | Form gồm Inputs `Từ ngày`, `Đến ngày`, Select `Loại hoạt động`, Input `Người thực hiện`, Select `Mức độ` | None | Pass | 11/15/2015 | |
| **GUI-KW-SEC-ACT-02** | Thống kê & biểu đồ | 1. Quan sát đầu trang | Card group `Tổng hoạt động 1,250`, `Thành công 1,180`, `Lỗi 45`, `Cảnh báo 25`; card Biểu đồ đường (h-48 bg-muted) | None | Pass | 11/15/2015 | |
| **GUI-KW-SEC-ACT-03** | Bảng hoạt động | 1. Quan sát table | Cột Thời gian, Loại (Badge), Mô tả, Người thực hiện, IP, Mức độ, Kết quả, Thao tác (Xem chi tiết/Xuất log/Báo cáo lỗi) | None | Pass | 11/15/2015 | |

#### Check FUNC

| ID | Test Case Description | Test Case Procedure | Expected Output | Dependence | Result | Test date | Note |
|----|----------------------|---------------------|----------------|------------|--------|-----------|------|
| **FUNC-KW-SEC-ACT-01** | Lọc theo loại hoạt động | 1. Set `Loại = Thao tác dữ liệu` | Bảng chỉ hiển thị entries with data ops badge; thống kê cập nhật | None | Pass | 11/15/2015 | |
| **FUNC-KW-SEC-ACT-02** | Lọc theo mức độ nghiêm trọng | 1. Set `Mức độ = Nghiêm trọng` | Table highlight entries severity high; cards updated | None | Pass | 11/15/2015 | |
| **FUNC-KW-SEC-ACT-03** | Xem chi tiết hoạt động | 1. Click `Xem chi tiết` | Modal hiển thị log chi tiết (thời gian, request id, payload) | FUNC-KW-SEC-ACT-01 | Pass | 11/15/2015 | |
| **FUNC-KW-SEC-ACT-04** | Xuất log | 1. Click `Xuất log` | Download file CSV/TXT chứa hoạt động theo bộ lọc | FUNC-KW-SEC-ACT-01 | Pass | 11/15/2015 | |
| **FUNC-KW-SEC-ACT-05** | Báo cáo lỗi | 1. Với hoạt động `Kết quả = Lỗi`, click `Báo cáo lỗi` | Form gửi tới admin, status entry -> `Đang xử lý`, toast success | FUNC-KW-SEC-ACT-03 | Pass | 11/15/2015 | |

---

### Function: Báo cáo bảo mật

#### Check GUI: `/nhanvienkho/security/reports`

| ID | Test Case Description | Test Case Procedure | Expected Output | Dependence | Result | Test date | Note |
|----|----------------------|---------------------|----------------|------------|--------|-----------|------|
| **GUI-KW-SEC-REP-01** | Bộ lọc báo cáo | 1. Mở trang | Form `Từ ngày`, `Đến ngày`, Select `Loại báo cáo`, Select `Mức độ ưu tiên` | None | Pass | 11/15/2015 | |
| **GUI-KW-SEC-REP-02** | Thống kê & biểu đồ | 1. Quan sát thẻ | Card group `Tổng đăng nhập 1,250`, `Đăng nhập thành công 1,180`, `Thất bại 45`, `Hoạt động bất thường 8`; card `Biểu đồ bảo mật` (cột) | None | Pass | 11/15/2015 | |
| **GUI-KW-SEC-REP-03** | Bảng sự kiện bảo mật | 1. Quan sát table | Cột Thời gian, Loại, Mô tả, Mức độ, Trạng thái, Người thực hiện, Thao tác (Xem/Xử lý/Bỏ qua/Báo cáo) | None | Pass | 11/15/2015 | |

#### Check FUNC

| ID | Test Case Description | Test Case Procedure | Expected Output | Dependence | Result | Test date | Note |
|----|----------------------|---------------------|----------------|------------|--------|-----------|------|
| **FUNC-KW-SEC-REP-01** | Tạo báo cáo theo thời gian | 1. Chọn khoảng ngày + loại `Đăng nhập` -> click `Tạo báo cáo` | Dashboard refresh theo filter, toast “Đã tạo báo cáo bảo mật” | None | Pass | 11/15/2015 | |
| **FUNC-KW-SEC-REP-02** | Lọc theo mức độ ưu tiên | 1. Set `Mức độ = Cao` | Table hiển thị events severity high, statistics adjust | FUNC-KW-SEC-REP-01 | Pass | 11/15/2015 | |
| **FUNC-KW-SEC-REP-03** | Xử lý sự kiện bảo mật | 1. Click `Xử lý` -> chọn trạng thái `Đang xử lý` + note | Event status badge update, timeline entry added, notify admin | FUNC-KW-SEC-REP-01 | Pass | 11/15/2015 | |
| **FUNC-KW-SEC-REP-04** | Xuất báo cáo | 1. Click `Xuất báo cáo` | PDF/Excel file generated with stats + chart + table | FUNC-KW-SEC-REP-01 | Pass | 11/15/2015 | |
| **FUNC-KW-SEC-REP-05** | Gửi báo cáo | 1. Click `Gửi báo cáo` -> chọn recipients | Email/internal message sent, history log, toast success | FUNC-KW-SEC-REP-04 | Pass | 11/15/2015 | |

---

### Function: Cảnh báo bảo mật

#### Check GUI: `/nhanvienkho/security/alerts`

| ID | Test Case Description | Test Case Procedure | Expected Output | Dependence | Result | Test date | Note |
|----|----------------------|---------------------|----------------|------------|--------|-----------|------|
| **GUI-KW-SEC-ALT-01** | Thẻ thống kê cảnh báo | 1. Mở trang | Card group `Cảnh báo mới 5`, `Đang xử lý 3`, `Đã xử lý 45`, `Nghiêm trọng 2` | None | Pass | 11/15/2015 | |
| **GUI-KW-SEC-ALT-02** | Bộ lọc cảnh báo | 1. Quan sát form | Select `Mức độ`, Select `Trạng thái`, Select `Loại cảnh báo`, Input `Thời gian` | None | Pass | 11/15/2015 | |
| **GUI-KW-SEC-ALT-03** | Bảng cảnh báo | 1. Quan sát table | Cột Thời gian, Loại, Mô tả, Mức độ, Trạng thái, Người xử lý, Thao tác (Xem/Xử lý/Bỏ qua/Báo cáo) | None | Pass | 11/15/2015 | |

#### Check FUNC

| ID | Test Case Description | Test Case Procedure | Expected Output | Dependence | Result | Test date | Note |
|----|----------------------|---------------------|----------------|------------|--------|-----------|------|
| **FUNC-KW-SEC-ALT-01** | Lọc theo mức độ | 1. Set `Mức độ = Nghiêm trọng` | Table hiển thị alerts severity critical; stats highlight | None | Pass | 11/15/2015 | |
| **FUNC-KW-SEC-ALT-02** | Xử lý cảnh báo | 1. Click `Xử lý` -> cập nhật trạng thái `Đang xử lý`, thêm ghi chú | Badge update, log entry, notify admin | FUNC-KW-SEC-ALT-01 | Pass | 11/15/2015 | |
| **FUNC-KW-SEC-ALT-03** | Đánh dấu đã xử lý | 1. Sau khi xử lý, click `Đã xử lý` | Alert moves to resolved list, stats update, toast success | FUNC-KW-SEC-ALT-02 | Pass | 11/15/2015 | |
| **FUNC-KW-SEC-ALT-04** | Bỏ qua cảnh báo | 1. Click `Bỏ qua` + nhập lý do | Status -> `Bỏ qua`, note saved, audit log entry | FUNC-KW-SEC-ALT-01 | Pass | 11/15/2015 | |
| **FUNC-KW-SEC-ALT-05** | Xử lý hàng loạt | 1. Chọn nhiều alerts -> `Xử lý hàng loạt` -> chọn `Đã xử lý` | Tất cả alerts update status, log batch action, toast | FUNC-KW-SEC-ALT-01 | Pass | 11/15/2015 | |
| **FUNC-KW-SEC-ALT-06** | Báo cáo cảnh báo | 1. Click `Báo cáo` trên alert nghiêm trọng | Report sent to security admin, state flagged, history recorded | FUNC-KW-SEC-ALT-02 | Pass | 11/15/2015 | |
| **FUNC-KW-SEC-ALT-07** | Xuất báo cáo cảnh báo | 1. Click `Xuất báo cáo` | File summary of alerts generated (CSV/PDF) | FUNC-KW-SEC-ALT-01 | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn MDX để dễ dàng quản lý và cập nhật test cases.*


