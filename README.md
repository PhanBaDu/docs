# Test Case Template - Cập nhật đơn hàng online (Nhân viên)

## Module Code
**Giao lộ 19: Họcl6c (Nhân viên)**

## Test Requirement
1. Danh sách & chi tiết đơn hàng online
2. Cập nhật trạng thái
3. Xác nhận đơn hàng (kiểm kho)
4. Hủy đơn hàng

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

### Function: Danh sách & chi tiết đơn hàng online

#### Check GUI: `/nhanvien/orders`

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DH-LIST-01** | Kiểm tra layout danh sách | 1. Đăng nhập<br>2. Truy cập `/nhanvien/orders` | Hiển thị trang với tiêu đề, mô tả, thống kê (từ trang orders page), card bộ lọc, bảng danh sách đơn (chờ xác nhận, tổng tiền, phương thức, trạng thái, ngày đặt, thao tác) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DH-DETAIL-01** | Kiểm tra layout chi tiết | 1. Truy cập `/nhanvien/orders/ORD001` | Hiển thị h1 `Chi tiết đơn hàng online`, mô tả, grid tổng quan (ID, Trạng thái, PT thanh toán, Ngày đặt, Nhân viên xử lý) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DH-DETAIL-02** | Kiểm tra card Khách hàng & giao hàng | 1. Ở trang chi tiết | CardTitle `Khách hàng & Giao hàng`, hiển thị tên, email, SĐT, hạng, địa chỉ giao | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DH-DETAIL-03** | Kiểm tra bảng sản phẩm đặt | 1. Ở trang chi tiết | CardTitle `Sản phẩm đặt`, Table columns `Tên sách`, `SL yêu cầu`, `Tồn kho hiện tại`, `Cần nhập thêm` với Badge (Không/Có) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DH-DETAIL-04** | Kiểm tra nhóm hành động | 1. Quan sát các button | Buttons: `Cập nhật trạng thái`, `Xác nhận đơn hàng`, `Hủy đơn hàng`, `Xử lý thanh toán`, `In hóa đơn` | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DH-DETAIL-05** | Kiểm tra card Lịch sử thay đổi | 1. Cuộn xuống cuối trang | CardTitle `Lịch sử thay đổi`, liệt kê các thay đổi `thời gian • nhân viên • ghi chú` | FUNC-DN-02 | Pass | 11/15/2015 | |

---

#### Check FUNC: Danh sách & chi tiết

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DH-LIST-01** | Tìm kiếm đơn hàng | 1. Ở `/nhanvien/orders` nhập `ORD001` vào ô tìm kiếm | Danh sách chỉ hiển thị đơn #ORD001; nếu không có hiển thị “Không tìm thấy đơn hàng” | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DH-LIST-02** | Lọc theo trạng thái | 1. Chọn trạng thái `Đang giao` | Danh sách chỉ hiển thị đơn trạng thái `Đang giao`, Badge màu phù hợp | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DH-LIST-03** | Lọc theo phương thức thanh toán | 1. Chọn `MoMo` | Danh sách chỉ hiển thị đơn thanh toán MoMo | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DH-LIST-04** | Xem chi tiết đơn từ danh sách | 1. Click `Xem chi tiết` | Điều hướng `/nhanvien/orders/[id]`, hiển thị trang chi tiết | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DH-DETAIL-01** | Xem chi tiết | 1. Truy cập `/nhanvien/orders/ORD001` | Hiển thị đầy đủ thông tin: khách, sản phẩm, tình trạng tồn kho, lịch sử | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Cập nhật trạng thái đơn hàng

#### Check GUI (Modal `Cập nhật trạng thái`)

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DH-STATUS-01** | Kiểm tra modal | 1. Tại trang chi tiết, click `Cập nhật trạng thái` | Dialog hiển thị tiêu đề `Cập nhật trạng thái đơn hàng #ORD001`, Badge trạng thái hiện tại, RadioGroup trạng thái mới, Textarea lý do hủy, Textarea ghi chú, Select gửi thông báo, Buttons `Hủy`, `Lưu` | FUNC-DN-02 | Pass | 11/15/2015 | |

---

#### Check FUNC: Cập nhật trạng thái

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DH-STATUS-01** | Chuyển từ Chờ xác nhận → Đang chuẩn bị | 1. Trong modal chọn `Đang chuẩn bị`<br>2. Nhập ghi chú nếu cần<br>3. Chọn Gửi thông báo = Có<br>4. Click `Lưu` | Trạng thái đơn cập nhật thành `Đang chuẩn bị`, Badge đổi màu, lịch sử bổ sung dòng mới, thông báo gửi cho khách hàng, toast success | FUNC-DH-DETAIL-01 | Pass | 11/15/2015 | |
| **FUNC-DH-STATUS-02** | Cập nhật thành `Đang giao` | 1. Chọn `Đang giao`, ghi chú `Bàn giao cho shipper A` | Đơn hiển thị badge `Đang giao`, lịch sử cập nhật, thông báo shipper (nếu logic), toast success | FUNC-DH-STATUS-01 | Pass | 11/15/2015 | |
| **FUNC-DH-STATUS-03** | Cập nhật thành `Đã giao` | 1. Chọn `Đã giao`<br>2. Tick gửi thông báo | Đơn chuyển `Đã giao`, thông báo “Đơn hàng của bạn đã được giao thành công” gửi cho khách | FUNC-DH-STATUS-01 | Pass | 11/15/2015 | |
| **FUNC-DH-STATUS-04** | Cập nhật thành `Đã hủy` không nhập lý do | 1. Chọn `Đã hủy`<br>2. Để trống Lý do | Modal báo lỗi `Vui lòng nhập lý do hủy`, không lưu | FUNC-DH-STATUS-01 | Pass | 11/15/2015 | |
| **FUNC-DH-STATUS-05** | Hủy cập nhật | 1. Click `Hủy` trong modal | Modal đóng, không thay đổi dữ liệu | FUNC-DH-STATUS-01 | Pass | 11/15/2015 | |

---

### Function: Xác nhận đơn hàng (kiểm kho)

#### Check GUI (Modal `Xác nhận đơn hàng`)

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DH-CONFIRM-01** | Kiểm tra modal xác nhận | 1. Click `Xác nhận đơn hàng` | Dialog hiển thị thông tin khách, PT thanh toán, địa chỉ giao, bảng sản phẩm (Tên, SL yêu cầu, Tồn kho), Textarea `Lý do từ chối`, Buttons `Hủy`, `Từ chối`, `Xác nhận` | FUNC-DN-02 | Pass | 11/15/2015 | |

---

#### Check FUNC: Xác nhận đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DH-CONFIRM-01** | Xác nhận đủ hàng | 1. Trong modal, kiểm tra tồn kho<br>2. Click `Xác nhận` | Nếu tất cả sản phẩm đủ kho: trạng thái đơn → `Đang chuẩn bị`, tồn kho trừ tương ứng, lịch sử thêm dòng “Xác nhận đơn hàng”, khách nhận thông báo | FUNC-DH-DETAIL-01 | Pass | 11/15/2015 | |
| **FUNC-DH-CONFIRM-02** | Từ chối do thiếu hàng | 1. Nếu sản phẩm `Toán học 12` thiếu (10 yêu cầu, 5 tồn)<br>2. Nhập lý do “Không đủ tồn kho”<br>3. Click `Từ chối` | Đơn chuyển trạng thái `Đã hủy` hoặc `Chờ xử lý lại`, thông báo gửi cho khách, gợi ý chọn sản phẩm khác | FUNC-DH-DETAIL-01 | Pass | 11/15/2015 | |
| **FUNC-DH-CONFIRM-03** | Hủy modal xác nhận | 1. Click `Hủy` | Modal đóng, không thay đổi | FUNC-DH-DETAIL-01 | Pass | 11/15/2015 | |

---

### Function: Hủy đơn hàng

#### Check GUI (Modal `Hủy đơn hàng`)

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DH-CANCEL-01** | Kiểm tra modal hủy | 1. Click `Hủy đơn hàng` | Dialog hiển thị tiêu đề `Hủy đơn hàng #ORD001`, RadioGroup lý do, Textarea mô tả, Select hoàn tiền, Textarea giải pháp, Textarea thông báo khách hàng, Buttons `Đóng`, `Xác nhận hủy` | FUNC-DN-02 | Pass | 11/15/2015 | |

---

#### Check FUNC: Hủy đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DH-CANCEL-01** | Hủy do không thể vận chuyển | 1. Chọn lý do `Không thể vận chuyển (địa chỉ lỗi)`<br>2. Nhập mô tả, chọn hoàn tiền nếu cần, nhập giải pháp, soạn thông báo<br>3. Click `Xác nhận hủy` | Đơn chuyển trạng thái `Đã hủy`, khách nhận thông báo, lịch sử ghi nhận lý do, hoàn tiền xử lý (nếu chọn) | FUNC-DH-DETAIL-01 | Pass | 11/15/2015 | |
| **FUNC-DH-CANCEL-02** | Hủy do khách yêu cầu | 1. Chọn `Khách hàng yêu cầu`<br>2. Nhập mô tả + thông báo | Đơn hủy thành công, khách nhận xác nhận, không hoàn tiền nếu chưa thanh toán | FUNC-DH-DETAIL-01 | Pass | 11/15/2015 | |
| **FUNC-DH-CANCEL-03** | Hủy modal | 1. Click `Đóng` | Modal đóng, không thay đổi | FUNC-DH-DETAIL-01 | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn MDX để dễ dàng quản lý và cập nhật test cases.*

