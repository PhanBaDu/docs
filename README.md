# Test Case Template - Báo cáo kho (Nhân viên kho)

## Module Code
**Giao lộ 19: Họcl6c (Nhân viên kho)**

## Test Requirement
1. Trang lựa chọn báo cáo `/nhanvienkho/reports`
2. Báo cáo sách sắp hết hàng `/nhanvienkho/reports/low-stock`
3. Báo cáo tồn kho tổng quan `/nhanvienkho/reports/inventory`
4. Lịch sử nhập/xuất kho `/nhanvienkho/reports/history`

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

### Function: Trang lựa chọn báo cáo

#### Check GUI: `/nhanvienkho/reports`

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-KW-REPORTS-01** | Kiểm tra bố cục tổng quan | 1. Đăng nhập kho<br>2. Mở `/nhanvienkho/reports` | Header `Báo cáo kho` + mô tả, grid 3 card link: `Sách sắp hết hàng`, `Báo cáo tồn kho`, `Lịch sử nhập xuất` (CardTitle + CardDescription đúng như code) | FUNC-KW-REPORTS-01 | Pass | 11/15/2015 | |

#### Check FUNC

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-KW-REPORTS-01** | Điều hướng Low-stock | 1. Click card `Sách sắp hết hàng` | Điều hướng đến `/nhanvienkho/reports/low-stock` | None | Pass | 11/15/2015 | |
| **FUNC-KW-REPORTS-02** | Điều hướng Báo cáo tồn kho | 1. Click card `Báo cáo tồn kho` | Điều hướng đến `/nhanvienkho/reports/inventory` | None | Pass | 11/15/2015 | |
| **FUNC-KW-REPORTS-03** | Điều hướng Lịch sử | 1. Click card `Lịch sử nhập xuất` | Điều hướng đến `/nhanvienkho/reports/history` | None | Pass | 11/15/2015 | |

---

### Function: Báo cáo sách sắp hết hàng

#### Check GUI: `/nhanvienkho/reports/low-stock`

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-KW-LOW-01** | Thẻ thống kê cảnh báo | 1. Mở trang | Grid thống kê 4 card: `Sắp hết 25`, `Hết hàng 8`, `Cần nhập gấp 5`, `Tổng cảnh báo 38` với text-sm muted và số font-semibold | FUNC-KW-LOW-01 | Pass | 11/15/2015 | |
| **GUI-KW-LOW-02** | Bộ lọc cảnh báo | 1. Quan sát card “Bộ lọc” | Select `Mức độ`, `Thể loại`, `Sắp xếp`, row action buttons `Tạo yêu cầu nhập hàng`, `Xuất báo cáo` | FUNC-KW-LOW-02 | Pass | 11/15/2015 | |
| **GUI-KW-LOW-03** | Bảng sách sắp hết | 1. Quan sát table | Cột Mã/Tên/Thể loại/Số lượng/Ngưỡng/Mức độ/Thao tác, badge `BK001`, `Văn học`, `Mức độ` highlight, buttons `Tạo yêu cầu nhập`, `Cập nhật ngưỡng` | FUNC-KW-LOW-01 | Pass | 11/15/2015 | |

#### Check FUNC: Lọc & thao tác

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-KW-LOW-01** | Lọc theo mức độ | 1. Chọn `Mức độ = Hết hàng` | Danh sách chỉ hiển thị những sách badge `Hết hàng`; thống kê có thể cập nhật | None | Pass | 11/15/2015 | |
| **FUNC-KW-LOW-02** | Lọc theo thể loại | 1. Chọn `Thể loại = Khoa học` | Table chỉ hiện sách khoa học, badge thay đổi | None | Pass | 11/15/2015 | |
| **FUNC-KW-LOW-03** | Sắp xếp số lượng tăng dần | 1. Chọn `Sắp xếp = Số lượng tăng dần` | Danh sách reorder theo số lượng hiện tại | None | Pass | 11/15/2015 | |
| **FUNC-KW-LOW-04** | Tạo yêu cầu nhập cho từng sách | 1. Bấm `Tạo yêu cầu nhập` tại BK001 | Mở flow tạo yêu cầu (modal / trang) với mã sách auto fill, cho phép nhập số lượng đề xuất; submission log “Yêu cầu nhập BK001” | None | Pass | 11/15/2015 | |
| **FUNC-KW-LOW-05** | Cập nhật ngưỡng tối thiểu | 1. Click `Cập nhật ngưỡng`<br>2. Nhập ngưỡng mới | Sau khi lưu, ngưỡng hiển thị trong table update, badge mức độ recalculated | None | Pass | 11/15/2015 | |
| **FUNC-KW-LOW-06** | Tạo yêu cầu nhập hàng loạt | 1. Chọn nhiều sách (checkbox) -> `Tạo yêu cầu nhập hàng` | Modal liệt kê sách đã chọn, nhập số lượng/ghi chú chung; sau khi Submit, tạo batch request và hiển thị toast success | FUNC-KW-LOW-04 | Pass | 11/15/2015 | |
| **FUNC-KW-LOW-07** | Xuất báo cáo cảnh báo | 1. Click `Xuất báo cáo` | File PDF/Excel tải xuống gồm thống kê + danh sách; log `low-stock-report` | None | Pass | 11/15/2015 | |

---

### Function: Báo cáo tồn kho

#### Check GUI: `/nhanvienkho/reports/inventory`

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-KW-INVREP-01** | Kiểm tra bộ lọc | 1. Mở trang | Form gồm Input `Từ ngày/Đến ngày`, Select `Khoảng thời gian`, Select `Thể loại`, layout md:grid-cols-5 | FUNC-KW-INVREP-01 | Pass | 11/15/2015 | |
| **GUI-KW-INVREP-02** | Kiểm tra thẻ thống kê | 1. Quan sát grid 4 card | Hiển thị `Tổng sách 1,250`, `Giá trị tồn 125M VNĐ`, `Có sẵn 1,180`, `Hết hàng 45` | FUNC-KW-INVREP-01 | Pass | 11/15/2015 | |
| **GUI-KW-INVREP-03** | Biểu đồ tồn kho | 1. Quan sát card “Biểu đồ tồn kho” | Placeholder `div h-48 bg-muted` xuất hiện, mô tả `Số lượng theo thể loại` | FUNC-KW-INVREP-01 | Pass | 11/15/2015 | |
| **GUI-KW-INVREP-04** | Bảng danh sách sách | 1. Quan sát table | Cột Mã/Tên/Thể loại/Số lượng/Giá trị/Trạng thái/Ngày cập nhật, button group `Tạo báo cáo`, `Xuất báo cáo`, `Gửi báo cáo` | FUNC-KW-INVREP-01 | Pass | 11/15/2015 | |

#### Check FUNC: Lọc & xuất báo cáo

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-KW-INVREP-01** | Tạo báo cáo theo tháng | 1. Set `Khoảng thời gian = Tháng này`<br>2. Click `Tạo báo cáo` | Dữ liệu thống kê, biểu đồ, table refresh theo tháng hiện tại; toast `Đã tạo báo cáo tồn kho (Tháng này)` | None | Pass | 11/15/2015 | |
| **FUNC-KW-INVREP-02** | Lọc đa thể loại | 1. Chọn `Thể loại = Văn học` | Table chỉ hiển thị sách loại văn học; biểu đồ highlight dataset tương ứng | None | Pass | 11/15/2015 | |
| **FUNC-KW-INVREP-03** | Xuất báo cáo tồn kho | 1. Click `Xuất báo cáo` | Hệ thống tạo file PDF/Excel chứa thẻ thống kê + biểu đồ + bảng chi tiết | FUNC-KW-INVREP-01 | Pass | 11/15/2015 | |
| **FUNC-KW-INVREP-04** | Gửi báo cáo | 1. Click `Gửi báo cáo`<br>2. Chọn người nhận | Báo cáo gắn file được gửi qua email/app, log `report_sent`, toast success | FUNC-KW-INVREP-03 | Pass | 11/15/2015 | |
| **FUNC-KW-INVREP-05** | Validation ngày không hợp lệ | 1. Chọn `Từ ngày` > `Đến ngày`<br>2. Tạo báo cáo | Hiển thị lỗi `Khoảng ngày không hợp lệ`, không gọi API | None | Pass | 11/15/2015 | |

---

### Function: Lịch sử nhập/xuất

#### Check GUI: `/nhanvienkho/reports/history`

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-KW-HIST-01** | Bộ lọc lịch sử | 1. Mở trang | Form gồm `Từ ngày`, `Đến ngày`, Select `Loại giao dịch`, Input `Mã sách`; layout md:grid-cols-5 | FUNC-KW-HIST-01 | Pass | 11/15/2015 | |
| **GUI-KW-HIST-02** | Thẻ thống kê nhập/xuất | 1. Quan sát grid card | Thẻ hiển thị `Tổng nhập 1,250`, `Tổng xuất 980`, `Chênh lệch +270`, `Giá trị nhập 125M VNĐ` | FUNC-KW-HIST-01 | Pass | 11/15/2015 | |
| **GUI-KW-HIST-03** | Bảng giao dịch | 1. Quan sát card danh sách | Table cột Ngày giờ, Loại, Mã sách, Tên sách, Số lượng, Giá trị, Người thực hiện, Ghi chú; row mẫu `2023-11-20 14:30` | FUNC-KW-HIST-01 | Pass | 11/15/2015 | |
| **GUI-KW-HIST-04** | Buttons hành động | 1. Quan sát cuối card | Buttons `Xuất lịch sử`, `Gửi báo cáo` hiển thị | FUNC-KW-HIST-01 | Pass | 11/15/2015 | |

#### Check FUNC: Lọc & báo cáo lịch sử

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-KW-HIST-01** | Lọc theo loại giao dịch | 1. Chọn `Loại giao dịch = Nhập hàng` | Table chỉ hiển thị dòng badge Nhập hàng, thống kê cập nhật `Tổng nhập` | None | Pass | 11/15/2015 | |
| **FUNC-KW-HIST-02** | Lọc theo mã sách | 1. Nhập `BK001` vào ô Mã sách | Hiển thị giao dịch liên quan BK001, gợi ý auto highlight | None | Pass | 11/15/2015 | |
| **FUNC-KW-HIST-03** | Xuất lịch sử giao dịch | 1. Thiết lập bộ lọc<br>2. Click `Xuất lịch sử` | Tệp Excel/PDF chứa bảng theo bộ lọc; log `history_export` | FUNC-KW-HIST-01 | Pass | 11/15/2015 | |
| **FUNC-KW-HIST-04** | Gửi báo cáo lịch sử | 1. Click `Gửi báo cáo`<br>2. Chọn người nhận | Gửi email/app notification đính kèm file; toast success | FUNC-KW-HIST-03 | Pass | 11/15/2015 | |
| **FUNC-KW-HIST-05** | Xem chi tiết giao dịch | 1. Click vào dòng giao dịch | Modal hiển thị đầy đủ thông tin (thời gian, loại, số lượng, ghi chú) | FUNC-KW-HIST-01 | Pass | 11/15/2015 | |
| **FUNC-KW-HIST-06** | Kiểm tra chênh lệch thống kê | 1. Chọn khoảng thời gian tùy chỉnh | Thẻ `Chênh lệch` cập nhật = Tổng nhập - Tổng xuất; hiển thị dấu + hoặc - theo số | FUNC-KW-HIST-01 | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn MDX để dễ dàng quản lý và cập nhật test cases.*

