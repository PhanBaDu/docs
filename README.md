# Test Case Template - Xử lý yêu cầu (Nhân viên kho)

## Module Code
**Giao lộ 19: Họcl6c (Nhân viên kho)**

## Test Requirement
1. Danh sách yêu cầu `/nhanvienkho/requests`
2. Xử lý yêu cầu nhập hàng `/nhanvienkho/requests/import`
3. Xử lý yêu cầu xuất hàng `/nhanvienkho/requests/export`
4. Theo dõi trạng thái & báo cáo yêu cầu `/nhanvienkho/requests/tracking`

---

## Test Summary

### Người lớp Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 34 |
| **Fail** | 0 |
| **Untested** | 0 |
| **N/A** | 0 |
| **Number of Test cases** | 34 |

---

## Test Cases

### Function: Danh sách yêu cầu

#### Check GUI: `/nhanvienkho/requests`

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-KW-REQ-LIST-01** | Thẻ thống kê đầu trang | 1. Đăng nhập kho<br>2. Truy cập `/nhanvienkho/requests` | Grid 4 `Card`: `Yêu cầu mới 15`, `Đang xử lý 8`, `Hoàn thành 45`, `Chờ phê duyệt 3` đúng typography trong UI | FUNC-KW-REQ-LIST-01 | Pass | 11/15/2015 | |
| **GUI-KW-REQ-LIST-02** | Bộ lọc | 1. Quan sát card `Bộ lọc` | 4 Select: Loại (all/import/export/audit/adjust), Trạng thái, Ưu tiên, Sắp xếp (time-desc/time-asc/priority/code) hiển thị đúng label | FUNC-KW-REQ-LIST-02 | Pass | 11/15/2015 | |
| **GUI-KW-REQ-LIST-03** | Bảng danh sách | 1. Quan sát `Table` | Cột Mã yêu cầu, Loại, Mô tả, Người tạo, Thời gian, Ưu tiên, Trạng thái, Thao tác; row mẫu hiển thị `REQ001`, badge `Nhập hàng`, `Mới`, buttons `Xem chi tiết`, `Xử lý` | FUNC-KW-REQ-LIST-01 | Pass | 11/15/2015 | |

#### Check FUNC: Lọc, sắp xếp, thao tác

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-KW-REQ-LIST-01** | Tải danh sách mặc định | 1. Mở trang | API trả danh sách, table >=1 row, thống kê khớp database | None | Pass | 11/15/2015 | |
| **FUNC-KW-REQ-LIST-02** | Lọc theo loại | 1. Chọn `Loại = Xuất hàng` | Table chỉ hiển thị yêu cầu `export`, badge loại cập nhật | FUNC-KW-REQ-LIST-01 | Pass | 11/15/2015 | |
| **FUNC-KW-REQ-LIST-03** | Lọc theo trạng thái | 1. Chọn `Trạng thái = Đang xử lý` | Danh sách chỉ còn badge `Đang xử lý`; thẻ “Đang xử lý” highlight | FUNC-KW-REQ-LIST-01 | Pass | 11/15/2015 | |
| **FUNC-KW-REQ-LIST-04** | Lọc theo ưu tiên | 1. Chọn `Ưu tiên = Cao` | Table hiển thị badge `Cao`; cột `Ưu tiên` highlight | FUNC-KW-REQ-LIST-01 | Pass | 11/15/2015 | |
| **FUNC-KW-REQ-LIST-05** | Sắp xếp thời gian | 1. Chọn `Sắp xếp = Thời gian tạo cũ nhất` | Danh sách được sắp xếp ascending theo `Thời gian` | FUNC-KW-REQ-LIST-01 | Pass | 11/15/2015 | |
| **FUNC-KW-REQ-LIST-06** | Xem chi tiết yêu cầu | 1. Click `Xem chi tiết` trên REQ001 | Điều hướng/toggle detail view hiển thị đầy đủ info + hành động xử lý tương ứng | FUNC-KW-REQ-LIST-01 | Pass | 11/15/2015 | |
| **FUNC-KW-REQ-LIST-07** | Mở trang xử lý | 1. Click `Xử lý` trên yêu cầu import | Điều hướng tới `/nhanvienkho/requests/import` với query ID | FUNC-KW-REQ-LIST-06 | Pass | 11/15/2015 | |

---

### Function: Xử lý yêu cầu nhập hàng

#### Check GUI: `/nhanvienkho/requests/import`

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-KW-REQ-IMPORT-01** | Thông tin yêu cầu | 1. Mở trang | Card hiển thị `Mã yêu cầu`, `Người tạo`, `Thời gian`, `Mô tả` dạng grid 4 cột | FUNC-KW-REQ-IMPORT-01 | Pass | 11/15/2015 | |
| **GUI-KW-REQ-IMPORT-02** | Bảng sách yêu cầu | 1. Quan sát table | Cột Mã sách, Tên sách, Số lượng yêu cầu/có sẵn, Trạng thái (Badge), Thao tác (buttons Xác nhận/Từ chối/Điều chỉnh) | FUNC-KW-REQ-IMPORT-01 | Pass | 11/15/2015 | |
| **GUI-KW-REQ-IMPORT-03** | Khối ghi chú xử lý | 1. Quan sát card cuối | Textarea placeholder “Ghi chú…”, các button `Xác nhận tất cả`, `Từ chối yêu cầu`, `Lưu xử lý` | FUNC-KW-REQ-IMPORT-01 | Pass | 11/15/2015 | |

#### Check FUNC: Xử lý yêu cầu nhập

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-KW-REQ-IMPORT-01** | Xác nhận từng sách | 1. Click `Xác nhận` tại BK001<br>2. Nhập ghi chú | Trạng thái item chuyển “Đã xác nhận”, badge cập nhật, log ghi lý do; tooltip/alert success | FUNC-KW-REQ-LIST-07 | Pass | 11/15/2015 | |
| **FUNC-KW-REQ-IMPORT-02** | Từ chối từng sách | 1. Click `Từ chối`<br>2. Nhập lý do | Badge đổi `Từ chối`, trạng thái yêu cầu partial; notify người tạo | FUNC-KW-REQ-IMPORT-01 | Pass | 11/15/2015 | |
| **FUNC-KW-REQ-IMPORT-03** | Điều chỉnh số lượng | 1. Click `Điều chỉnh`<br>2. Nhập số lượng mới 30 | UI ghi nhận số mới (hiển thị 30/100), log `Điều chỉnh`, hiển thị note | FUNC-KW-REQ-IMPORT-01 | Pass | 11/15/2015 | |
| **FUNC-KW-REQ-IMPORT-04** | Xác nhận tất cả | 1. Click `Xác nhận tất cả` | Tất cả book rows set to `Đã xác nhận`, trạng thái yêu cầu -> `Đã xác nhận`, alert success | FUNC-KW-REQ-IMPORT-01 | Pass | 11/15/2015 | |
| **FUNC-KW-REQ-IMPORT-05** | Từ chối toàn bộ | 1. Click `Từ chối yêu cầu`<br>2. Nhập lý do | Request status -> `Từ chối`, send notification to requester, log reason | FUNC-KW-REQ-IMPORT-01 | Pass | 11/15/2015 | |
| **FUNC-KW-REQ-IMPORT-06** | Lưu xử lý | 1. Click `Lưu xử lý` | Ghi lại trạng thái từng sách + ghi chú xuống DB, toast `Đã lưu xử lý yêu cầu` | FUNC-KW-REQ-IMPORT-01 | Pass | 11/15/2015 | |
| **FUNC-KW-REQ-IMPORT-07** | Validation ghi chú bắt buộc khi từ chối | 1. Click `Từ chối yêu cầu` mà không nhập ghi chú | Alert lỗi “Vui lòng nhập lý do từ chối”, không thay đổi trạng thái | FUNC-KW-REQ-IMPORT-05 | Pass | 11/15/2015 | |

---

### Function: Xử lý yêu cầu xuất hàng

#### Check GUI: `/nhanvienkho/requests/export`

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-KW-REQ-EXPORT-01** | Card thông tin yêu cầu | 1. Mở trang | Card grid hiển thị `REQ002`, người tạo, thời gian, mô tả | FUNC-KW-REQ-EXPORT-01 | Pass | 11/15/2015 | |
| **GUI-KW-REQ-EXPORT-02** | Card thông tin đơn hàng | 1. Quan sát card thứ hai | Fields `Mã đơn hàng ORD001`, `Khách hàng`, `Thời gian giao` | FUNC-KW-REQ-EXPORT-01 | Pass | 11/15/2015 | |
| **GUI-KW-REQ-EXPORT-03** | Bảng sách xuất & ghi chú | 1. Quan sát table + card `Ghi chú xử lý` | Table như trang import (Số lượng yêu cầu/có sẵn, badges). Card ghi chú có buttons `Xác nhận tất cả`, `Từ chối yêu cầu`, `Lưu xử lý` | FUNC-KW-REQ-EXPORT-01 | Pass | 11/15/2015 | |

#### Check FUNC: Xử lý yêu cầu xuất

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-KW-REQ-EXPORT-01** | Kiểm tra tồn kho trước xuất | 1. Click `Xác nhận` khi `Số lượng có sẵn` < yêu cầu | Nếu không đủ: hiển thị cảnh báo, cho phép điều chỉnh hoặc từ chối; không cập nhật kho | FUNC-KW-REQ-LIST-07 | Pass | 11/15/2015 | |
| **FUNC-KW-REQ-EXPORT-02** | Xác nhận đủ hàng | 1. Click `Xác nhận` khi đủ hàng | Trạng thái item `Sẵn sàng xuất`, giảm tạm số lượng trong session, log cho ORD001 | FUNC-KW-REQ-EXPORT-01 | Pass | 11/15/2015 | |
| **FUNC-KW-REQ-EXPORT-03** | Từ chối yêu cầu | 1. Click `Từ chối yêu cầu` + ghi chú | Request status -> `Từ chối`, notify sales team | FUNC-KW-REQ-EXPORT-01 | Pass | 11/15/2015 | |
| **FUNC-KW-REQ-EXPORT-04** | Điều chỉnh thay thế sách | 1. Click `Điều chỉnh` -> chọn sách khác | UI cho phép chọn sản phẩm thay thế, update table & ghi chú | FUNC-KW-REQ-EXPORT-01 | Pass | 11/15/2015 | |
| **FUNC-KW-REQ-EXPORT-05** | Lưu xử lý | 1. Click `Lưu xử lý` | Ghi log, cập nhật trạng thái, gửi thông báo, hiển thị alert success | FUNC-KW-REQ-EXPORT-02 | Pass | 11/15/2015 | |

---

### Function: Theo dõi trạng thái yêu cầu

#### Check GUI: `/nhanvienkho/requests/tracking`

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-KW-REQ-TRACK-01** | Bộ lọc theo thời gian & trạng thái | 1. Mở trang tracking | Form với Input `Từ ngày`, `Đến ngày`, Select `Trạng thái`, `Loại yêu cầu` (layout md:grid-cols-5) | FUNC-KW-REQ-TRACK-01 | Pass | 11/15/2015 | |
| **GUI-KW-REQ-TRACK-02** | Thẻ thống kê & biểu đồ | 1. Quan sát grid & card | Grid 4 card (Tổng, Hoàn thành, Đang xử lý, Từ chối) + card `Biểu đồ trạng thái` (div h-48 bg-muted) | FUNC-KW-REQ-TRACK-01 | Pass | 11/15/2015 | |
| **GUI-KW-REQ-TRACK-03** | Bảng yêu cầu theo dõi | 1. Quan sát table | Cột Mã, Loại, Mô tả, Trạng thái, Thời gian tạo/xử lý, Người xử lý, Thao tác (Xem chi tiết, Cập nhật trạng thái) | FUNC-KW-REQ-TRACK-01 | Pass | 11/15/2015 | |

#### Check FUNC: Theo dõi & cập nhật

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-KW-REQ-TRACK-01** | Lọc theo trạng thái | 1. Set `Trạng thái = Chờ phê duyệt` | Card thống kê cập nhật, table chỉ hiển thị yêu cầu pending | None | Pass | 11/15/2015 | |
| **FUNC-KW-REQ-TRACK-02** | Lọc theo loại yêu cầu | 1. Set `Loại = Điều chỉnh` | Table hiển thị req adjust, badge `Điều chỉnh` | None | Pass | 11/15/2015 | |
| **FUNC-KW-REQ-TRACK-03** | Xem chi tiết từ tracking | 1. Click `Xem chi tiết` | Mở modal / điều hướng detail page hiển thị timeline xử lý | FUNC-KW-REQ-TRACK-01 | Pass | 11/15/2015 | |
| **FUNC-KW-REQ-TRACK-04** | Cập nhật trạng thái | 1. Click `Cập nhật trạng thái` -> chọn `Hoàn thành` | Trạng thái thay đổi, log `status_change`, gửi thông báo cho requester | FUNC-KW-REQ-TRACK-03 | Pass | 11/15/2015 | |
| **FUNC-KW-REQ-TRACK-05** | Xem lịch sử xử lý | 1. Trong modal detail, mở tab `Lịch sử` | Hiển thị timeline entries (thời gian, người xử lý, ghi chú) | FUNC-KW-REQ-TRACK-03 | Pass | 11/15/2015 | |
| **FUNC-KW-REQ-TRACK-06** | Xuất báo cáo theo dõi | 1. Từ trang tracking, click `Xuất báo cáo` | Tạo file PDF/Excel gồm thống kê + biểu đồ + bảng theo bộ lọc | FUNC-KW-REQ-TRACK-01 | Pass | 11/15/2015 | |
| **FUNC-KW-REQ-TRACK-07** | Gửi báo cáo theo dõi | 1. Sau khi xuất, chọn `Gửi báo cáo` | Báo cáo gửi qua email/app cho quản lý, toast success | FUNC-KW-REQ-TRACK-06 | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn MDX để dễ dàng quản lý và cập nhật test cases.*


