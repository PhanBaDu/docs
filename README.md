# Test Case Template - Hỗ trợ bán hàng (Nhân viên kho)

## Module Code
**Giao lộ 19: Họcl6c (Nhân viên kho)**

## Test Requirement
1. Trang chọn thao tác hỗ trợ `/nhanvienkho/support`
2. Kiểm tra tồn kho cho đơn hàng `/nhanvienkho/support/check-order`
3. Xác nhận khả năng giao hàng `/nhanvienkho/support/confirm`
4. Cập nhật trạng thái đơn hàng `/nhanvienkho/support/update-status`
5. Xử lý đơn hàng đặc biệt `/nhanvienkho/support/special-orders`

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

### Function: Trang hỗ trợ bán hàng (landing)

#### Check GUI: `/nhanvienkho/support`

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-KW-SUP-LAND-01** | Kiểm tra bố cục thẻ điều hướng | 1. Đăng nhập kho<br>2. mở `/nhanvienkho/support` | Header `Hỗ trợ bán hàng`, mô tả; grid 4 card link tới `check-order`, `confirm`, `update-status`, `special-orders` với CardTitle/CardDescription khớp code | FUNC-KW-SUP-LAND-01 | Pass | 11/15/2015 | |

#### Check FUNC

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-KW-SUP-LAND-01** | Điều hướng kiểm tra đơn | 1. Click card `Kiểm tra tồn kho cho đơn hàng` | Điều hướng tới `/nhanvienkho/support/check-order` | None | Pass | 11/15/2015 | |
| **FUNC-KW-SUP-LAND-02** | Điều hướng xác nhận giao hàng | 1. Click card `Xác nhận khả năng giao hàng` | Điều hướng tới `/nhanvienkho/support/confirm` | None | Pass | 11/15/2015 | |
| **FUNC-KW-SUP-LAND-03** | Điều hướng cập nhật trạng thái | 1. Click card `Cập nhật trạng thái đơn hàng` | Điều hướng tới `/nhanvienkho/support/update-status` | None | Pass | 11/15/2015 | |
| **FUNC-KW-SUP-LAND-04** | Điều hướng đơn đặc biệt | 1. Click card `Đơn hàng đặc biệt` | Điều hướng tới `/nhanvienkho/support/special-orders` | None | Pass | 11/15/2015 | |

---

### Function: Kiểm tra tồn kho cho đơn hàng

#### Check GUI: `/nhanvienkho/support/check-order`

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-KW-CHECK-01** | Form tìm kiếm đơn hàng | 1. Mở trang | Card với Label/Input `Mã đơn hàng`, `Mã khách hàng`, `Ngày tạo đơn`, button `Tìm kiếm` | FUNC-KW-CHECK-01 | Pass | 11/15/2015 | |
| **GUI-KW-CHECK-02** | Thông tin đơn hàng | 1. Quan sát card thứ hai | Grid text-sm hiển thị `Mã đơn`, `Khách hàng`, `Ngày tạo`, `Tổng tiền` | FUNC-KW-CHECK-01 | Pass | 11/15/2015 | |
| **GUI-KW-CHECK-03** | Bảng danh sách sách | 1. Quan sát Table | Cột Mã sách, Tên sách, `Số lượng yêu cầu/có sẵn`, `Trạng thái` (Badge), `Ghi chú` | FUNC-KW-CHECK-01 | Pass | 11/15/2015 | |
| **GUI-KW-CHECK-04** | Tổng kết kiểm tra | 1. Quan sát card cuối | Các dòng `Tổng sách`, `Có sẵn`, `Hết hàng` + buttons `Xác nhận giao hàng`, `Từ chối giao hàng`, `Đề xuất thay thế` | FUNC-KW-CHECK-01 | Pass | 11/15/2015 | |

#### Check FUNC

| ID | Test Case Description | Test Case Procedure | Expected Output | Dependence | Result | Test date | Note |
|----|----------------------|---------------------|----------------|------------|--------|-----------|------|
| **FUNC-KW-CHECK-01** | Tìm kiếm đơn hàng hợp lệ | 1. Nhập mã ORD001<br>2. Click `Tìm kiếm` | Thông tin đơn và danh sách sách được tải, hiển thị summary | None | Pass | 11/15/2015 | |
| **FUNC-KW-CHECK-02** | Tính trạng thái từng sách | 1. Kiểm tra row `Số lượng có sẵn =0` | Badge chuyển `Hết hàng`, ghi chú “Cần đề xuất thay thế” | FUNC-KW-CHECK-01 | Pass | 11/15/2015 | |
| **FUNC-KW-CHECK-03** | Xác nhận giao hàng | 1. Sau khi đảm bảo đủ hàng, click `Xác nhận giao hàng` | Alert success “Đơn hàng có thể giao”, log confirmation, notify sales | FUNC-KW-CHECK-01 | Pass | 11/15/2015 | |
| **FUNC-KW-CHECK-04** | Từ chối giao hàng | 1. Khi thiếu hàng, click `Từ chối giao hàng` + nhập lý do | Trạng thái đơn -> `Từ chối`, send notification, prompt to create import request | FUNC-KW-CHECK-02 | Pass | 11/15/2015 | |
| **FUNC-KW-CHECK-05** | Đề xuất thay thế | 1. Click `Đề xuất thay thế` trên sách hết hàng | Modal gợi ý sách tương tự (theo category/author), cho phép chọn & gửi note | FUNC-KW-CHECK-02 | Pass | 11/15/2015 | |

---

### Function: Xác nhận khả năng giao hàng

#### Check GUI: `/nhanvienkho/support/confirm`

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-KW-CONFIRM-01** | Bộ lọc đơn hàng | 1. Mở trang | Form 4 cột: Select `Trạng thái`, Input `Ngày tạo`, Input `Mã khách hàng`, Select `Ưu tiên` | FUNC-KW-CONFIRM-01 | Pass | 11/15/2015 | |
| **GUI-KW-CONFIRM-02** | Bảng đơn hàng cần xác nhận | 1. Quan sát table | Cột Mã, Khách hàng, Ngày tạo, Tổng tiền, Trạng thái, Ưu tiên, Thao tác; buttons `Xem chi tiết`, `Xác nhận`, `Từ chối`, `Đề xuất thay thế`; buttons `Xác nhận hàng loạt`, `Xuất báo cáo` phía trên | FUNC-KW-CONFIRM-01 | Pass | 11/15/2015 | |

#### Check FUNC

| ID | Test Case Description | Test Case Procedure | Expected Output | Dependence | Result | Test date | Note |
|----|----------------------|---------------------|----------------|-----------|--------|-----------|------|
| **FUNC-KW-CONFIRM-01** | Lọc theo trạng thái | 1. Set `Trạng thái = Chờ xác nhận` | Table hiển thị đơn pending, badge `Chờ xác nhận` | None | Pass | 11/15/2015 | |
| **FUNC-KW-CONFIRM-02** | Xác nhận đơn | 1. Click `Xác nhận` trên ORD001 | Trạng thái -> `Đã xác nhận`, log timestamp, notify sales/customer | FUNC-KW-CONFIRM-01 | Pass | 11/15/2015 | |
| **FUNC-KW-CONFIRM-03** | Từ chối đơn | 1. Click `Từ chối` + nhập lý do | Đơn set `Từ chối`, gợi ý tạo yêu cầu nhập, email notification | FUNC-KW-CONFIRM-01 | Pass | 11/15/2015 | |
| **FUNC-KW-CONFIRM-04** | Đề xuất thay thế | 1. Click `Đề xuất thay thế` | Modal cho phép lựa chọn sách thay, gửi note cho sales | FUNC-KW-CONFIRM-01 | Pass | 11/15/2015 | |
| **FUNC-KW-CONFIRM-05** | Xác nhận hàng loạt | 1. Chọn nhiều đơn -> click `Xác nhận hàng loạt` | Selected orders update to confirmed, progress toast hiển thị; log batch id | FUNC-KW-CONFIRM-01 | Pass | 11/15/2015 | |
| **FUNC-KW-CONFIRM-06** | Xuất báo cáo | 1. Click `Xuất báo cáo` | Download file danh sách + trạng thái, kèm bộ lọc hiện tại | FUNC-KW-CONFIRM-01 | Pass | 11/15/2015 | |

---

### Function: Cập nhật trạng thái đơn hàng

#### Check GUI: `/nhanvienkho/support/update-status`

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-KW-UPD-01** | Bộ lọc | 1. Mở trang | Form với Input `Mã đơn hàng`, Select `Trạng thái hiện tại`, Input `Ngày cập nhật`, Input `Mã khách hàng` | FUNC-KW-UPD-01 | Pass | 11/15/2015 | |
| **GUI-KW-UPD-02** | Bảng đơn hàng | 1. Quan sát table | Cột Mã, Khách hàng, Trạng thái hiện tại, Ngày cập nhật, Ghi chú, Thao tác (button `Cập nhật trạng thái`) | FUNC-KW-UPD-01 | Pass | 11/15/2015 | |
| **GUI-KW-UPD-03** | Modal cập nhật trạng thái | 1. Click `Cập nhật trạng thái` | Dialog hiển thị Select `Trạng thái mới` (preparing/shipping/delivered/done/canceled), Textarea `Ghi chú`, Input `Ngày cập nhật`, Input readOnly `Người thực hiện`, buttons `Hủy`, `Lưu cập nhật` | FUNC-KW-UPD-02 | Pass | 11/15/2015 | |

#### Check FUNC

| ID | Test Case Description | Test Case Procedure | Expected Output | Dependence | Result | Test date | Note |
|----|----------------------|---------------------|----------------|-----------|--------|-----------|------|
| **FUNC-KW-UPD-01** | Lọc theo trạng thái | 1. Set filter `Trạng thái hiện tại = Đã xác nhận` | Table hiển thị các đơn matching | None | Pass | 11/15/2015 | |
| **FUNC-KW-UPD-02** | Cập nhật sang `Đang chuẩn bị` | 1. Click `Cập nhật trạng thái` -> chọn `Đang chuẩn bị` | Record updated, table row status text change, toast success | FUNC-KW-UPD-01 | Pass | 11/15/2015 | |
| **FUNC-KW-UPD-03** | Cập nhật sang `Đang giao` | 1. Chọn `Đang giao` + ghi chú | Thông báo gửi cho vận chuyển & khách hàng; history entry appended | FUNC-KW-UPD-02 | Pass | 11/15/2015 | |
| **FUNC-KW-UPD-04** | Cập nhật sang `Đã giao` | 1. Chọn `Đã giao` | Đơn được đánh dấu delivered, trigger `Đánh giá` email cho khách | FUNC-KW-UPD-02 | Pass | 11/15/2015 | |
| **FUNC-KW-UPD-05** | Hủy đơn | 1. Chọn `Hủy bỏ` + ghi chú lý do | Đơn set canceled, logs, refund process triggered (nếu cần) | FUNC-KW-UPD-02 | Pass | 11/15/2015 | |
| **FUNC-KW-UPD-06** | Validation ghi chú | 1. Chọn `Hủy bỏ` nhưng bỏ trống ghi chú | Modal hiển thị lỗi `Vui lòng nhập ghi chú`, không lưu | FUNC-KW-UPD-05 | Pass | 11/15/2015 | |

---

### Function: Đơn hàng đặc biệt

#### Check GUI: `/nhanvienkho/support/special-orders`

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-KW-SPECIAL-01** | Bộ lọc | 1. Mở trang | Form gồm Select `Loại đặc biệt`, `Ưu tiên`, `Trạng thái`, Input `Ngày tạo` | FUNC-KW-SPECIAL-01 | Pass | 11/15/2015 | |
| **GUI-KW-SPECIAL-02** | Bảng đơn hàng đặc biệt | 1. Quan sát table | Cột Mã đơn, Loại đặc biệt, Khách hàng, Mô tả, Ưu tiên, Trạng thái, Thao tác (buttons `Xem chi tiết`, `Xử lý`, `Chuyển tiếp`, `Ghi chú`) | FUNC-KW-SPECIAL-01 | Pass | 11/15/2015 | |
| **GUI-KW-SPECIAL-03** | Form xử lý đặc biệt | 1. Quan sát card cuối | Textarea `Phương án xử lý`, Input datetime `Thời gian dự kiến`, Select `Người phụ trách`, buttons `Lưu xử lý`, `Chuyển tiếp` | FUNC-KW-SPECIAL-02 | Pass | 11/15/2015 | |

#### Check FUNC

| ID | Test Case Description | Test Case Procedure | Expected Output | Dependence | Result | Test date | Note |
|----|----------------------|---------------------|----------------|-----------|--------|-----------|------|
| **FUNC-KW-SPECIAL-01** | Lọc theo loại đặc biệt | 1. Set `Loại đặc biệt = Giao hàng nhanh` | Table hiển thị các đơn express, badge `Giao hàng nhanh` | None | Pass | 11/15/2015 | |
| **FUNC-KW-SPECIAL-02** | Lưu phương án xử lý | 1. Nhập phương án + thời gian + người phụ trách, click `Lưu xử lý` | Plan saved, status -> `Đang xử lý`, notify stakeholders | FUNC-KW-SPECIAL-01 | Pass | 11/15/2015 | |
| **FUNC-KW-SPECIAL-03** | Chuyển tiếp đơn | 1. Click `Chuyển tiếp` + chọn bộ phận | Đơn status -> `Đã chuyển tiếp`, log reason, send notification | FUNC-KW-SPECIAL-01 | Pass | 11/15/2015 | |
| **FUNC-KW-SPECIAL-04** | Ghi chú bổ sung | 1. Click `Ghi chú` -> nhập note | Note appended to history, hiển thị trong detail | FUNC-KW-SPECIAL-01 | Pass | 11/15/2015 | |
| **FUNC-KW-SPECIAL-05** | Theo dõi tiến độ | 1. Sau khi lưu phương án, refresh tracking | Trang tracking hiển thị đơn trong danh mục “Đơn đặc biệt - đang xử lý” | FUNC-KW-REQ-TRACK-01 | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn MDX để dễ dàng quản lý và cập nhật test cases.*


