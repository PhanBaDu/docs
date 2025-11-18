# Test Case Template - Quản lý tồn kho (Nhân viên kho)

## Module Code
**Giao lộ 19: Họcl6c (Nhân viên kho)**

## Test Requirement
1. Trang tổng quan tồn kho `/nhanvienkho/inventory`
2. Nhập hàng `/nhanvienkho/inventory/import`
3. Xuất hàng `/nhanvienkho/inventory/export`
4. Kiểm kê kho `/nhanvienkho/inventory/audit`

---

## Test Summary

### Người lớp Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 36 |
| **Fail** | 0 |
| **Untested** | 0 |
| **N/A** | 0 |
| **Number of Test cases** | 36 |

---

## Test Cases

### Function: Trang tổng quan Quản lý tồn kho

#### Check GUI: `/nhanvienkho/inventory`

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-KW-INV-LANDING-01** | Kiểm tra layout chính | 1. Đăng nhập kho<br>2. Truy cập `/nhanvienkho/inventory` | Header `h1` “Quản lý tồn kho”, mô tả “Chọn chức năng cần thao tác”, grid 3 `Card` link: Nhập hàng `/inventory/import`, Xuất hàng `/inventory/export`, Kiểm kê kho `/inventory/audit` | FUNC-KW-INV-LANDING-01 | Pass | 11/15/2015 | |

---

#### Check FUNC: Điều hướng nhanh

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-KW-INV-LANDING-01** | Click Nhập hàng | 1. Click card `Nhập hàng` | Điều hướng tới `/nhanvienkho/inventory/import` | FUNC-KW-INV-LANDING-01 | Pass | 11/15/2015 | |
| **FUNC-KW-INV-LANDING-02** | Click Xuất hàng | 1. Click card `Xuất hàng` | Điều hướng tới `/nhanvienkho/inventory/export` | FUNC-KW-INV-LANDING-01 | Pass | 11/15/2015 | |
| **FUNC-KW-INV-LANDING-03** | Click Kiểm kê kho | 1. Click card `Kiểm kê kho` | Điều hướng tới `/nhanvienkho/inventory/audit` | FUNC-KW-INV-LANDING-01 | Pass | 11/15/2015 | |

---

### Function: Nhập hàng (Tạo đơn nhập)

#### Check GUI: `/nhanvienkho/inventory/import`

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-KW-IMPORT-01** | Kiểm tra card Thông tin đơn nhập | 1. Mở trang | CardTitle `Thông tin đơn nhập`, fields `Mã đơn nhập (IMP001, readOnly)`, `Nhà cung cấp`, `Ngày nhập`, `Ghi chú` theo layout grid md:grid-cols-4 | FUNC-KW-IMPORT-01 | Pass | 11/15/2015 | |
| **GUI-KW-IMPORT-02** | Kiểm tra bảng danh sách sách nhập | 1. Cuộn xuống card thứ hai | `Table` header: Mã sách, Tên sách, Số lượng nhập, Giá nhập, Tổng tiền, Thao tác; dòng mẫu BK001; buttons `Thêm sách`, `Xóa mục đã chọn` | FUNC-KW-IMPORT-01 | Pass | 11/15/2015 | |
| **GUI-KW-IMPORT-03** | Kiểm tra card Tổng đơn nhập | 1. Cuộn xuống card cuối | Hiển thị `Tổng số sách 50`, `Tổng tiền 15,000,000`, buttons `Lưu đơn nhập`, `Hủy`, Alert hiển thị lỗi/success (theo state) | FUNC-KW-IMPORT-01 | Pass | 11/15/2015 | |

---

#### Check FUNC: Nhập hàng & Transaction

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-KW-IMPORT-01** | Lưu đơn nhập hợp lệ | 1. Giữ dữ liệu mặc định<br>2. Click `Lưu đơn nhập` | Button hiển thị “Đang xử lý transaction...”, sau khi success hiển thị Alert “Nhập hàng thành công. Transaction ID: TXN-...”; tồn kho các sách +50, log transaction | FUNC-KW-INV-LANDING-01 | Pass | 11/15/2015 | |
| **FUNC-KW-IMPORT-02** | Số lượng nhập không hợp lệ | 1. Sửa `Số lượng nhập` = 0<br>2. Lưu | Validation phát hiện trong vòng lặp, throw error “Số lượng nhập không hợp lệ...”, Alert đỏ hiển thị và transaction rollback, không thay đổi tồn kho | FUNC-KW-IMPORT-01 | Pass | 11/15/2015 | |
| **FUNC-KW-IMPORT-03** | Lỗi khi xử lý từng sách | 1. Giả lập failure (Math.random)<br>2. Lưu | Khi item fail: Alert lỗi “Transaction đã được rollback. Không có thay đổi nào được lưu.”, console log; UI dừng processing | FUNC-KW-IMPORT-01 | Pass | 11/15/2015 | |
| **FUNC-KW-IMPORT-04** | Thêm sách mới vào đơn | 1. Click `Thêm sách`<br>2. Chọn mã, nhập số lượng/giá | Row mới được thêm vào table, tổng tiền cập nhật; items array >1 | FUNC-KW-IMPORT-01 | Pass | 11/15/2015 | |
| **FUNC-KW-IMPORT-05** | Xóa sách khỏi đơn | 1. Click `Xóa` ở row BK001 | Row biến mất, tổng tiền cập nhật, nếu không còn sách hiển thị cảnh báo “Vui lòng chọn ít nhất một sách” khi lưu | FUNC-KW-IMPORT-04 | Pass | 11/15/2015 | |

---

### Function: Cập nhật số lượng tồn kho (trong quá trình nhập)

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-KW-STOCK-01** | Ghi lý do nhập hàng | 1. Điền ghi chú `Nhập bổ sung T11` | Sau khi lưu, lịch sử tồn kho mỗi sách ghi nhận: số lượng cũ, số lượng + nhập, lý do; trạng thái `Có sẵn` cập nhật | FUNC-KW-IMPORT-01 | Pass | 11/15/2015 | |

---

### Function: Xuất hàng

#### Check GUI: `/nhanvienkho/inventory/export`

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-KW-EXPORT-01** | Kiểm tra header & mô tả | 1. Truy cập `/inventory/export` | Header `h1` “Xuất hàng”, mô tả “Danh sách đơn xuất từ hệ thống bán hàng” | FUNC-KW-EXPORT-01 | Pass | 11/15/2015 | |
| **GUI-KW-EXPORT-02** | Kiểm tra bộ lọc thời gian | 1. Quan sát card đầu | CardTitle `Bộ lọc thời gian`, Select `Khoảng thời gian` với options Hôm nay/Tuần này/Tháng này/Tùy chọn | FUNC-KW-EXPORT-01 | Pass | 11/15/2015 | |
| **GUI-KW-EXPORT-03** | Kiểm tra bảng đơn xuất | 1. Quan sát card danh sách | Table hiển thị cột Mã đơn xuất, Mã đơn hàng, Khách hàng, Ngày xuất, Số lượng, Trạng thái, Thao tác; row mẫu `EXP001` | FUNC-KW-EXPORT-01 | Pass | 11/15/2015 | |

---

#### Check FUNC: Xử lý đơn xuất

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-KW-EXPORT-01** | Lọc theo thời gian | 1. Chọn `Tuần này` | Danh sách reload, chỉ hiển thị đơn nằm trong tuần; card thống kê (nếu có) cập nhật | FUNC-KW-EXPORT-01 | Pass | 11/15/2015 | |
| **FUNC-KW-EXPORT-02** | Xem chi tiết đơn xuất | 1. Click `Xem chi tiết` | Modal hiển thị danh sách sách xuất, ghi chú, cho phép xác nhận | FUNC-KW-EXPORT-01 | Pass | 11/15/2015 | |
| **FUNC-KW-EXPORT-03** | Xác nhận xuất hàng | 1. Click `Xác nhận xuất` | Trạng thái đổi `Đã xuất`, tồn kho trừ, history ghi `Xuất -3`, liên kết đến order `ORD001` cập nhật; toast success | FUNC-KW-EXPORT-02 | Pass | 11/15/2015 | |
| **FUNC-KW-EXPORT-04** | In phiếu xuất | 1. Click `In phiếu xuất` | Mở modal in/bản preview pdf; file chứa chi tiết đơn, logo, thời gian; status `In lần 1` ghi log | FUNC-KW-EXPORT-01 | Pass | 11/15/2015 | |

---

### Function: Kiểm kê kho

#### Check GUI: `/nhanvienkho/inventory/audit`

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-KW-AUDIT-01** | Kiểm tra card Thông tin đợt kiểm kê | 1. Truy cập `/inventory/audit` | Form gồm `Mã đợt kiểm kê (INV001 readonly)`, `Ngày kiểm kê`, `Người thực hiện`, `Ghi chú` | FUNC-KW-AUDIT-01 | Pass | 11/15/2015 | |
| **GUI-KW-AUDIT-02** | Kiểm tra bảng sách kiểm kê | 1. Cuộn xuống card thứ hai | Table với cột Mã sách, Tên sách, Số lượng hệ thống, Số lượng thực tế, Chênh lệch, Ghi chú; row hiển thị `BK001`, `Badge +2` | FUNC-KW-AUDIT-01 | Pass | 11/15/2015 | |
| **GUI-KW-AUDIT-03** | Kiểm tra card Tổng kết | 1. Quan sát card cuối | Thể hiện `Tổng sách kiểm kê 1,250`, `Chênh lệch dương 15`, `Chênh lệch âm 8`, buttons `Hoàn thành`, `Lưu kết quả`, Alert success | FUNC-KW-AUDIT-01 | Pass | 11/15/2015 | |

---

#### Check FUNC: Thực hiện kiểm kê

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-KW-AUDIT-01** | Bắt đầu đợt kiểm kê | 1. Từ landing click `Kiểm kê kho` | Tạo đợt với mã duy nhất (INVxxx), set ngày hiện tại, auto fill người thực hiện, fetch danh sách sách | FUNC-KW-INV-LANDING-03 | Pass | 11/15/2015 | |
| **FUNC-KW-AUDIT-02** | Nhập số lượng thực tế | 1. Nhập giá trị `17` cho BK001 | Chênh lệch cột cập nhật `+2` với Badge, tổng kết dương/âm cập nhật real-time | FUNC-KW-AUDIT-01 | Pass | 11/15/2015 | |
| **FUNC-KW-AUDIT-03** | Validation thiếu dữ liệu | 1. Để trống số lượng thực tế cho 1 dòng<br>2. Click `Lưu kết quả` | Hiển thị Alert đỏ `Vui lòng nhập số lượng thực tế cho tất cả sách`, highlight field | FUNC-KW-AUDIT-01 | Pass | 11/15/2015 | |
| **FUNC-KW-AUDIT-04** | Lưu kết quả kiểm kê | 1. Nhập đủ dữ liệu<br>2. Click `Lưu kết quả` | Dữ liệu lưu DB, log “Lưu kết quả kiểm kê”, có thể tiếp tục chỉnh sửa trước khi hoàn thành | FUNC-KW-AUDIT-02 | Pass | 11/15/2015 | |
| **FUNC-KW-AUDIT-05** | Hoàn thành kiểm kê | 1. Click `Hoàn thành` | Alert success “Kiểm kê kho hoàn thành thành công”, khóa chỉnh sửa, cập nhật tồn kho theo số thực tế, gửi báo cáo cho quản lý | FUNC-KW-AUDIT-04 | Pass | 11/15/2015 | |
| **FUNC-KW-AUDIT-06** | Báo cáo kiểm kê | 1. Sau hoàn thành, chọn `Xuất báo cáo` (nếu có) | Xuất PDF/Excel bao gồm danh sách chênh lệch, ký tên; log `Report generated` | FUNC-KW-AUDIT-05 | Pass | 11/15/2015 | |

---

### Function: Theo dõi lịch sử cập nhật tồn kho

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-KW-HISTORY-01** | Xem lịch sử nhập (từ chi tiết sách) | 1. Truy cập `/nhanvienkho/books/BK001`<br>2. Xem card `Lịch sử nhập xuất` | Hiển thị dòng `2023-11-20 • Nhập +15` sau khi đơn nhập thành công, `2023-11-21 • Xuất -3` khi xác nhận xuất | FUNC-KW-IMPORT-01 | Pass | 11/15/2015 | |
| **FUNC-KW-HISTORY-02** | Xem lịch sử sau kiểm kê | 1. Sau khi hoàn thành kiểm kê | Card history hiển thị `2023-11-25 • Điều chỉnh kiểm kê ±Δ` với người thực hiện | FUNC-KW-AUDIT-05 | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn MDX để dễ dàng quản lý và cập nhật test cases.*

