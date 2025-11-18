# Test Case Template - Quản lý yêu cầu (Nhân viên)

## Module Code
**Giao lộ 19: Họcl6c (Nhân viên)**

## Test Requirement
1. Danh sách yêu cầu nhập sách
2. Chi tiết yêu cầu
3. Chuyển tiếp lên kho
4. Gửi phản hồi/Thông báo khách hàng

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

### Function: Danh sách yêu cầu nhập sách

#### Check GUI: `/nhanvien/requests`

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-YC-LIST-01** | Kiểm tra tiêu đề trang | 1. Đăng nhập Nhân viên<br>2. Truy cập `/nhanvien/requests` | Hiển thị h1 `Quản lý yêu cầu từ khách hàng` class text-2xl font-bold & mô tả `Yêu cầu nhập sách từ khách hàng` | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-YC-LIST-02** | Kiểm tra thống kê | 1. Ở `/nhanvien/requests` quan sát grid đầu | Grid `grid-cols-2 md:grid-cols-5` gồm Card `Tổng yêu cầu 78`, `Chờ xử lý 15`, `Đang xử lý 12`, `Đã hoàn thành 45`, Card cuối `Đã từ chối 6` (col-span-2 md:col-span-1) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-YC-LIST-03** | Kiểm tra card Tìm kiếm & Bộ lọc | 1. Quan sát card tiếp theo | CardTitle `Tìm kiếm & Bộ lọc`, mô tả `Tìm theo ID, tên KH, tên sách; lọc Trạng thái & Loại yêu cầu`, grid md:grid-cols-6 có Input, Select Trạng thái, Select Loại yêu cầu | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-YC-LIST-04** | Kiểm tra bảng yêu cầu | 1. Quan sát card `Danh sách yêu cầu` | TableHeader có các cột ID, Khách hàng, Loại yêu cầu, Sản phẩm, Tình trạng, Ngày tạo, Thao tác. TableBody hiển thị hàng mẫu (#REQ001) với Badge, info khách, mô tả loại, list sản phẩm, Badge trạng thái, thời gian, nút `Xem chi tiết` | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-YC-LIST-05** | Kiểm tra sidebar panels | 1. Cuộn xuống grid 3 card | Card `Yêu cầu mới` chứa Button `Tạo yêu cầu nhập sách mới`; Card `Tóm tắt trạng thái` có placeholder chart `h-40 bg-muted`; Card `Hoạt động gần đây` liệt kê các hoạt động | FUNC-DN-02 | Pass | 11/15/2015 | |

---

#### Check FUNC: Danh sách yêu cầu nhập sách

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-YC-LIST-01** | Xem danh sách yêu cầu | 1. Đăng nhập<br>2. Truy cập `/nhanvien/requests` | Trang hiển thị thống kê, bộ lọc, bảng, sidebar như GUI tests; dữ liệu khớp mock | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-YC-LIST-02** | Tìm kiếm yêu cầu theo từ khóa | 1. Nhập `REQ001` vào Input tìm kiếm | Bảng chỉ hiển thị yêu cầu có ID/khách hàng/sản phẩm khớp; nếu không có hiển thị thông báo “Không tìm thấy yêu cầu” | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-YC-LIST-03** | Lọc theo trạng thái | 1. Chọn Trạng thái = `Chờ xử lý` | Bảng chỉ hiển thị các yêu cầu status `Chờ xử lý` (Badge variant destructive) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-YC-LIST-04** | Lọc theo loại yêu cầu | 1. Chọn Loại = `Nhập sách hết hàng` | Danh sách cập nhật chỉ các yêu cầu cùng loại; cột “Loại yêu cầu” hiển thị mô tả & số lượng | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-YC-LIST-05** | Xem chi tiết yêu cầu | 1. Click nút `Xem chi tiết` của #REQ001 | Điều hướng `/nhanvien/requests/REQ001` | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-YC-LIST-06** | Tạo yêu cầu mới | 1. Click `Tạo yêu cầu nhập sách mới` | Mở form/modal tạo yêu cầu mới (theo tài liệu). Cho phép nhập thông tin sản phẩm & lý do. Sau khi lưu hiển thị toast success | FUNC-DN-02 | Pass | 11/15/2015 | *(Mock flow)* |

---

### Function: Chi tiết yêu cầu

#### Check GUI: `/nhanvien/requests/[id]`

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-YC-DETAIL-01** | Kiểm tra tiêu đề trang | 1. Mở `/nhanvien/requests/REQ001` | Tiêu đề `Chi tiết yêu cầu #REQ001` | FUNC-YC-LIST-05 | Pass | 11/15/2015 | |
| **GUI-YC-DETAIL-02** | Kiểm tra card Thông tin chung | 1. Quan sát card đầu | CardTitle `Thông tin chung`, CardDescription, grid md:grid-cols-3 hiển thị ID, Trạng thái (Badge), Loại, Ngày tạo, Ngày cập nhật, Mức độ ưu tiên (Badge), Khách hàng (email/sđt/hạng), Nhân viên phụ trách | FUNC-YC-LIST-05 | Pass | 11/15/2015 | |
| **GUI-YC-DETAIL-03** | Kiểm tra card Chi tiết sản phẩm | 1. Quan sát card thứ hai | CardTitle `Chi tiết sản phẩm yêu cầu`, CardContent liệt kê từng sách: tên, số lượng, lý do, phản hồi kho | FUNC-YC-LIST-05 | Pass | 11/15/2015 | |
| **GUI-YC-DETAIL-04** | Kiểm tra card Lịch sử xử lý | 1. Quan sát card `Lịch sử xử lý` | CardContent hiển thị các dòng `thời gian • người xử lý • hành động • nội dung` | FUNC-YC-LIST-05 | Pass | 11/15/2015 | |
| **GUI-YC-DETAIL-05** | Kiểm tra card Ghi chú cá nhân | 1. Quan sát card cuối | CardTitle `Ghi chú cá nhân`, Label + Textarea, Button group `Chuyển tiếp lên kho`, `Cập nhật trạng thái`, `Gửi phản hồi`, `Hoàn thành yêu cầu` | FUNC-YC-LIST-05 | Pass | 11/15/2015 | |

---

#### Check FUNC: Chi tiết yêu cầu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-YC-DETAIL-01** | Xem thông tin yêu cầu | 1. Truy cập `/nhanvien/requests/REQ001` | Tất cả card hiển thị đúng dữ liệu: thổng tin chung, sản phẩm, lịch sử, ghi chú | FUNC-YC-LIST-05 | Pass | 11/15/2015 | |
| **FUNC-YC-DETAIL-02** | Thêm ghi chú cá nhân | 1. Nhập nội dung ghi chú<br>2. Click `Ghi chú cá nhân` (hành động) | Ghi chú được lưu, hiển thị toast success, lịch sử ghi chú cập nhật | FUNC-YC-DETAIL-01 | Pass | 11/15/2015 | |
| **FUNC-YC-DETAIL-03** | Cập nhật trạng thái yêu cầu | 1. Click `Cập nhật trạng thái`<br>2. Chọn trạng thái mới<br>3. Xác nhận | Yêu cầu chuyển trạng thái (Badge & bảng), timeline thêm dòng, hiển thị toast success | FUNC-YC-DETAIL-01 | Pass | 11/15/2015 | |
| **FUNC-YC-DETAIL-04** | Hoàn thành yêu cầu | 1. Click `Hoàn thành yêu cầu` | Trạng thái => `Đã hoàn thành`, các nút hành động ẩn/disable tùy logic, hiển thị toast success, danh sách tổng quan update | FUNC-YC-DETAIL-03 | Pass | 11/15/2015 | |
| **FUNC-YC-DETAIL-05** | Gửi phản hồi khách hàng | 1. Click `Gửi phản hồi` -> mở modal | Cho phép chọn loại phản hồi (dropdown), nhập tiêu đề, nội dung, phương thức gửi, template, tệp đính kèm, thời gian gửi. Khi click `Gửi`, thông báo được gửi (email/SMS/push), hiển thị toast success, log vào lịch sử xử lý | FUNC-YC-DETAIL-01 | Pass | 11/15/2015 | |

---

### Function: Chuyển tiếp lên kho

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-YC-KHO-01** | Mở modal chuyển tiếp | 1. Tại `/nhanvien/requests/REQ001`, click `Chuyển tiếp lên kho` | Modal hiển thị thông tin yêu cầu (ID, KH, loại), danh sách sách, lý do, radio ưu tiên, textarea ghi chú cho kho, DatePicker thời hạn, checkbox “Thông báo cho khách hàng”, Buttons `Hủy` & `Xác nhận` | FUNC-YC-DETAIL-01 | Pass | 11/15/2015 | |
| **FUNC-YC-KHO-02** | Chuyển tiếp thành công | 1. Trong modal, chọn ưu tiên, nhập ghi chú, chọn thời hạn, tick thông báo<br>2. Click `Xác nhận` | Yêu cầu chuyển trạng thái `Chuyển kho`, Nhân viên kho nhận thông báo, timeline cập nhật hành động, khách hàng nhận thông báo (nếu chọn), toast success | FUNC-YC-KHO-01 | Pass | 11/15/2015 | |
| **FUNC-YC-KHO-03** | Thiếu thông tin chuyển tiếp | 1. Mở modal<br>2. Không nhập ghi chú hoặc thời hạn<br>3. Click `Xác nhận` | Hiển thị validation `Vui lòng nhập ghi chú/ thời hạn`, không chuyển trạng thái, modal vẫn mở | FUNC-YC-KHO-01 | Pass | 11/15/2015 | |

---

### Function: Thông báo khách hàng / phản hồi

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-YC-TB-01** | Gửi thông báo cập nhật | 1. Tại chi tiết yêu cầu, click `Gửi phản hồi`<br>2. Chọn `Loại phản hồi = Cập nhật tiến độ`<br>3. Nhập tiêu đề, nội dung, chọn gửi email & app, tick “Lưu vào lịch sử”<br>4. Click `Gửi` | Thông báo gửi qua email & app, khách hàng nhận nội dung, lịch sử yêu cầu thêm dòng, toast success | FUNC-YC-DETAIL-01 | Pass | 11/15/2015 | |
| **FUNC-YC-TB-02** | Gửi thông báo hoàn thành | 1. Loại phản hồi `Hoàn thành yêu cầu`<br>2. Nhập nội dung<br>3. Chọn `Gửi ngay` | Yêu cầu đánh dấu `Đã hoàn thành`, thông báo gửi ngay, log kèm nội dung | FUNC-YC-DETAIL-04 | Pass | 11/15/2015 | |
| **FUNC-YC-TB-03** | Lên lịch gửi thông báo | 1. Trong modal, chọn `Gửi tại thời gian cụ thể`, đặt ngày/giờ | Thông báo được xếp lịch (ghi chú trong lịch sử), khi đến thời gian sẽ gửi tự động, hiển thị toast `Đã lên lịch gửi thông báo` | FUNC-YC-TB-01 | Pass | 11/15/2015 | |
| **FUNC-YC-TB-04** | Sử dụng mẫu phản hồi | 1. Chọn mẫu `Mẫu cảm ơn`<br>2. Chỉnh nội dung<br>3. Gửi | Textarea được điền nội dung mẫu, có thể chỉnh sửa, sau khi gửi log “Sử dụng mẫu” | FUNC-YC-TB-01 | Pass | 11/15/2015 | |
| **FUNC-YC-TB-05** | Gửi thông báo thất bại | 1. Ngắt kết nối/ mô phỏng lỗi, click `Gửi` | Hiển thị toast error `Không thể gửi thông báo`, log lỗi, yêu cầu giữ trạng thái cũ, cho phép thử lại | FUNC-YC-TB-01 | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn MDX để dễ dàng quản lý và cập nhật test cases.*

