# Test Case Template - Quản lý sách (Nhân viên kho)

## Module Code
**Giao lộ 19: Họcl6c (Nhân viên kho)**

## Test Requirement
1. Hiển thị danh sách & bộ lọc sách `/nhanvienkho/books`
2. Xem chi tiết sách `/nhanvienkho/books/[id]`
3. Thêm sách mới `/nhanvienkho/books/new`
4. Chỉnh sửa thông tin sách `/nhanvienkho/books/[id]/edit`
5. Ẩn sách & ghi nhận lý do (dialog trong trang chi tiết)
6. Tìm kiếm nâng cao (kết hợp filter/sort)

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

### Function: Hiển thị danh sách & bộ lọc sách

#### Check GUI: `/nhanvienkho/books`

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-KW-BOOK-LIST-01** | Kiểm tra header trang | 1. Đăng nhập kho<br>2. Truy cập `/nhanvienkho/books` | Header flex giữa: `h1` “Quản lý sách”, mô tả `Danh sách sách trong kho`, button `Thêm sách mới` (link `/nhanvienkho/books/new`) | FUNC-KW-BOOK-LIST-01 | Pass | 11/15/2015 | |
| **GUI-KW-BOOK-LIST-02** | Kiểm tra card thống kê | 1. Quan sát grid đầu | 4 `Card` hiển thị `Tổng số sách 1,250`, `Có sẵn 1,180`, `Hết hàng 45`, `Ẩn 25` với text-sm muted và số font-semibold | FUNC-KW-BOOK-LIST-01 | Pass | 11/15/2015 | |
| **GUI-KW-BOOK-LIST-03** | Kiểm tra card Tìm kiếm & Bộ lọc | 1. Quan sát card thứ hai | CardTitle “Tìm kiếm & Bộ lọc”, description nêu tiêu chí; `Input` placeholder “Tìm tên sách…”, Select cho `Thể loại`, `Trạng thái`, `Sắp xếp` với options khớp code; grid md:grid-cols-6 | FUNC-KW-BOOK-LIST-01 | Pass | 11/15/2015 | |
| **GUI-KW-BOOK-LIST-04** | Kiểm tra bảng danh sách | 1. Cuộn đến card Table | Table header gồm các cột Mã/Tên/Tác giả/Thể loại/Giá/Số lượng/Trạng thái/Thao tác; dòng mẫu hiển thị Badge `BK001`, `Đắc Nhân Tâm`, `Văn học`, etc và buttons `Xem chi tiết`, `Chỉnh sửa` | FUNC-KW-BOOK-LIST-01 | Pass | 11/15/2015 | |

---

#### Check FUNC: Danh sách & bộ lọc

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-KW-BOOK-LIST-01** | Tải danh sách mặc định | 1. Đăng nhập<br>2. Mở `/nhanvienkho/books` | API trả về danh sách, table hiển thị >=1 dòng, thống kê khớp dữ liệu tổng | FUNC-KW-LOGIN-01 | Pass | 11/15/2015 | |
| **FUNC-KW-BOOK-LIST-02** | Lọc theo thể loại | 1. Chọn `Thể loại = Văn học` | Table chỉ còn sách `category=vanhoc`, badge hiển thị `Văn học`, số liệu thống kê có thể cập nhật | FUNC-KW-BOOK-LIST-01 | Pass | 11/15/2015 | |
| **FUNC-KW-BOOK-LIST-03** | Lọc theo trạng thái | 1. Chọn `Trạng thái = Hết hàng` | Table hiển thị sách `status=out`, badge `Hết hàng` (variant destructive) | FUNC-KW-BOOK-LIST-01 | Pass | 11/15/2015 | |
| **FUNC-KW-BOOK-LIST-04** | Sắp xếp theo giá giảm | 1. Chọn `Sắp xếp = Giá giảm dần` | Danh sách reorder, cột Giá hiển thị giảm dần; icon sort highlight (nếu có) | FUNC-KW-BOOK-LIST-01 | Pass | 11/15/2015 | |
| **FUNC-KW-BOOK-LIST-05** | Nút Thêm sách mới | 1. Click button `Thêm sách mới` | Điều hướng `/nhanvienkho/books/new` mở trang form | FUNC-KW-BOOK-LIST-01 | Pass | 11/15/2015 | |

---

### Function: Tìm kiếm & gợi ý nâng cao

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-KW-SEARCH-01** | Tìm theo tên/tác giả/mã | 1. Nhập `BK001` vào input | Gợi ý dropdown hiển thị BK001, table filter khớp; highlight từ khóa | FUNC-KW-BOOK-LIST-01 | Pass | 11/15/2015 | |
| **FUNC-KW-SEARCH-02** | Không tìm thấy kết quả | 1. Nhập chuỗi không tồn tại | Table hiển thị empty state “Không tìm thấy sách phù hợp”, pagination ẩn | FUNC-KW-BOOK-LIST-01 | Pass | 11/15/2015 | |
| **FUNC-KW-SEARCH-03** | Reset bộ lọc | 1. Xoá input, set select `Tất cả` | Danh sách trở lại mặc định, gợi ý ẩn | FUNC-KW-SEARCH-01 | Pass | 11/15/2015 | |

---

### Function: Xem chi tiết sách

#### Check GUI: `/nhanvienkho/books/BK001`

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-KW-DETAIL-01** | Kiểm tra thông tin cơ bản | 1. Truy cập `/nhanvienkho/books/BK001` | Card “Thông tin cơ bản” grid md:grid-cols-3 hiển thị Mã/Tên/Tác giả/Thể loại/ Nhà XB/ Năm XB với Badge `Văn học` | FUNC-KW-DETAIL-01 | Pass | 11/15/2015 | |
| **GUI-KW-DETAIL-02** | Kiểm tra card Thông tin bán hàng | 1. Quan sát card thứ hai | Các trường Giá bán `89.000 VNĐ`, Số lượng `15`, Trạng thái Badge `Có sẵn`, Ngày nhập `2023-10-15`, Ngày cập nhật `2023-11-20` | FUNC-KW-DETAIL-01 | Pass | 11/15/2015 | |
| **GUI-KW-DETAIL-03** | Kiểm tra mô tả & hình ảnh | 1. Quan sát card `Mô tả sách` | Textarea default value + khung `div h-40 bg-muted` mô phỏng ảnh bìa | FUNC-KW-DETAIL-01 | Pass | 11/15/2015 | |
| **GUI-KW-DETAIL-04** | Kiểm tra lịch sử nhập xuất | 1. Xem card cuối | Liệt kê các dòng `2023-11-20 • Nhập +15…`, `2023-11-21 • Xuất -3…` | FUNC-KW-DETAIL-01 | Pass | 11/15/2015 | |
| **GUI-KW-DETAIL-05** | Kiểm tra nhóm hành động | 1. Nhìn cuối trang | Buttons: `Chỉnh sửa` (variant outline, link edit), `Ẩn sách` (destructive), `Quay lại` | FUNC-KW-DETAIL-02 | Pass | 11/15/2015 | |

---

#### Check FUNC: Chi tiết

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-KW-DETAIL-01** | Tải đúng dữ liệu | 1. Từ list click `Xem chi tiết` | Route `[id]` fetch book data theo ID, hiển thị khớp DB | FUNC-KW-BOOK-LIST-01 | Pass | 11/15/2015 | |
| **FUNC-KW-DETAIL-02** | Điều hướng chỉnh sửa | 1. Click `Chỉnh sửa` | Điều hướng `/nhanvienkho/books/BK001/edit` | FUNC-KW-DETAIL-01 | Pass | 11/15/2015 | |
| **FUNC-KW-DETAIL-03** | Lịch sử nhập xuất tải đủ | 1. Xem API history | Timeline hiển thị đầy đủ, có phân biệt nhập/xuất, include người thực hiện & ghi chú | FUNC-KW-DETAIL-01 | Pass | 11/15/2015 | |

---

### Function: Thêm sách mới

#### Check GUI: `/nhanvienkho/books/new`

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-KW-NEW-01** | Kiểm tra layout form | 1. Mở `/nhanvienkho/books/new` | Header `Thêm sách mới`, form grid md:grid-cols-2 gồm các Label/Input: Tên, Tác giả, Thể loại (Select), Nhà XB, Năm XB, Mã sách/ISBN, Giá bán, Số lượng nhập, Textarea mô tả, input file ảnh; button `Lưu`, `Hủy`, Alert hiển thị lỗi/thành công | FUNC-KW-NEW-01 | Pass | 11/15/2015 | |
| **GUI-KW-NEW-02** | Kiểm tra cảnh báo trùng mã | 1. Nhập `BK001` vào field mã | Text nhỏ màu đỏ `⚠️ Mã sách này đã tồn tại...` hiển thị ngay dưới input | FUNC-KW-NEW-02 | Pass | 11/15/2015 | |

---

#### Check FUNC: Thêm sách

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-KW-NEW-01** | Thêm sách hợp lệ | 1. Nhập đầy đủ thông tin hợp lệ<br>2. Nhập mã mới `BK200`<br>3. Click `Lưu` | Simulate API success: alert “Thêm sách mới thành công”, form reset, danh sách update (tăng tổng sách) | FUNC-KW-BOOK-LIST-01 | Pass | 11/15/2015 | |
| **FUNC-KW-NEW-02** | Mã sách trùng | 1. Nhập mã `BK001` | Không gọi API, hiển thị error `Mã sách "BK001" đã tồn tại...`, button `Lưu` disabled | FUNC-KW-NEW-01 | Pass | 11/15/2015 | |
| **FUNC-KW-NEW-03** | Lỗi transaction | 1. Gây lỗi mô phỏng (API fail) | Alert đỏ `Lỗi: ... Đã rollback transaction`, form giữ dữ liệu để sửa; log error | FUNC-KW-NEW-01 | Pass | 11/15/2015 | |
| **FUNC-KW-NEW-04** | Upload ảnh không hợp lệ | 1. Chọn file >5MB | Hiển thị lỗi “Kích thước ảnh vượt quá 5MB”, upload bị từ chối | FUNC-KW-NEW-01 | Pass | 11/15/2015 | |

---

### Function: Chỉnh sửa thông tin sách

#### Check GUI: `/nhanvienkho/books/[id]/edit`

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-KW-EDIT-01** | Bố cục form edit | 1. Mở `/nhanvienkho/books/BK001/edit` | Header `Chỉnh sửa sách - BK001`, form tương tự trang thêm nhưng có giá trị default; buttons `Lưu thay đổi`, `Hủy`, Alert hiển thị trạng thái | FUNC-KW-EDIT-01 | Pass | 11/15/2015 | |

---

#### Check FUNC: Chỉnh sửa

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-KW-EDIT-01** | Cập nhật thông tin hợp lệ | 1. Sửa giá bán & mô tả<br>2. Click `Lưu thay đổi` | Alert success “Cập nhật thông tin sách thành công”, quay lại trang chi tiết hoặc ở lại (tùy config), history log record cũ/mới | FUNC-KW-DETAIL-01 | Pass | 11/15/2015 | |
| **FUNC-KW-EDIT-02** | Validation thiếu dữ liệu | 1. Xóa tên sách<br>2. Lưu | Input hiển thị lỗi `Trường này bắt buộc`, không gọi API | FUNC-KW-EDIT-01 | Pass | 11/15/2015 | |
| **FUNC-KW-EDIT-03** | Hủy chỉnh sửa | 1. Click `Hủy` | Điều hướng về `/nhanvienkho/books/BK001` hoặc trang trước, không lưu thay đổi | FUNC-KW-DETAIL-01 | Pass | 11/15/2015 | |

---

### Function: Ẩn sách

#### Check GUI: Dialog Ẩn sách (từ `/nhanvienkho/books/BK001`)

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-KW-HIDE-01** | Kiểm tra dialog | 1. Click `Ẩn sách` | DialogTitle `Ẩn sách`, description “Bạn có chắc chắn muốn ẩn sách này?”, Textarea placeholder “Lý do ẩn sách (bắt buộc)”, buttons `Hủy`, `Có, ẩn sách` | FUNC-KW-HIDE-01 | Pass | 11/15/2015 | |

---

#### Check FUNC: Ẩn sách

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-KW-HIDE-01** | Ẩn sách thành công | 1. Nhập lý do “Ngừng kinh doanh”<br>2. Click `Có, ẩn sách` | Status sách đổi `Ẩn`, hiển thị badge `Ẩn`, log ghi lý do & người thực hiện, danh sách cập nhật cột trạng thái | FUNC-KW-DETAIL-01 | Pass | 11/15/2015 | |
| **FUNC-KW-HIDE-02** | Thiếu lý do | 1. Bỏ trống textarea<br>2. Click `Có, ẩn sách` | Validation hiển thị “Vui lòng nhập lý do ẩn sách”, dialog không đóng | FUNC-KW-HIDE-01 | Pass | 11/15/2015 | |
| **FUNC-KW-HIDE-03** | Hủy thao tác | 1. Click `Hủy` hoặc icon close | Dialog đóng, trạng thái giữ nguyên | FUNC-KW-HIDE-01 | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn MDX để dễ dàng quản lý và cập nhật test cases.*

