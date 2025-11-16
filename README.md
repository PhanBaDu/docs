# Test Case Template - Quản lý đánh giá (Admin)

## Module Code
**Model Management Store: Quản lý đánh giá Admin**

## Test Requirement
1. Xem đánh giá sản phẩm
2. Xem chi tiết đánh giá
3. Duyệt đánh giá
4. Từ chối đánh giá
5. Xóa đánh giá sản phẩm
6. Phản hồi đánh giá

---

## Test Summary

### Người thực hiện Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 33 |
| **Fail** | 0 |
| **Untested** | 43 |
| **N/A** | 0 |
| **Number of Test cases** | 76 |

---

## Test Cases

### Function: Xem đánh giá sản phẩm

#### Check GUI: Xem đánh giá sản phẩm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XDGSP-01** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/reviews<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Quản lý đánh giá" với kích thước text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-XDGSP-02** | Kiểm tra mô tả chức năng | 1. Truy cập /admin/reviews<br>2. Kiểm tra mô tả | Hiển thị mô tả "Xem toàn bộ đánh giá của khách hàng" màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-XDGSP-03** | Kiểm tra Select Bộ lọc sản phẩm | 1. Truy cập /admin/reviews<br>2. Kiểm tra Select | Hiển thị Select với placeholder "Sản phẩm", có danh sách tên sản phẩm | | Pass | 11/15/2015 | |
| **GUI-XDGSP-04** | Kiểm tra Select Bộ lọc điểm | 1. Truy cập /admin/reviews<br>2. Kiểm tra Select | Hiển thị Select với placeholder "Điểm", có các option: Tất cả, 5 sao, 4 sao, 3 sao, 2 sao, 1 sao | | Pass | 11/15/2015 | |
| **GUI-XDGSP-05** | Kiểm tra Select Bộ lọc trạng thái | 1. Truy cập /admin/reviews<br>2. Kiểm tra Select | Hiển thị Select với placeholder "Trạng thái", có các option: Tất cả, Chờ duyệt, Đã duyệt, Từ chối, Hiển thị, Ẩn, Vi phạm | | Pass | 11/15/2015 | |
| **GUI-XDGSP-06** | Kiểm tra trường Tìm kiếm | 1. Truy cập /admin/reviews<br>2. Kiểm tra trường tìm kiếm | Hiển thị input với icon Search bên trái, placeholder "Tìm theo nội dung/khách hàng...", có thể nhập và nhấn Enter để tìm | | Pass | 11/15/2015 | |
| **GUI-XDGSP-07** | Kiểm tra bảng đánh giá | 1. Truy cập /admin/reviews<br>2. Kiểm tra bảng | Hiển thị Table với các cột: Sản phẩm, Người đánh giá, Điểm, Nội dung, Trạng thái, Ngày, Thao tác | | Pass | 11/15/2015 | |
| **GUI-XDGSP-08** | Kiểm tra cột Sản phẩm trong bảng | 1. Truy cập /admin/reviews<br>2. Kiểm tra cột Sản phẩm | Hiển thị tên sản phẩm (font-medium), có thể có ảnh thumbnail | | Pass | 11/15/2015 | |
| **GUI-XDGSP-09** | Kiểm tra cột Người đánh giá trong bảng | 1. Truy cập /admin/reviews<br>2. Kiểm tra cột Người đánh giá | Hiển thị tên người đánh giá (font-medium), avatar (nếu có) | | Pass | 11/15/2015 | |
| **GUI-XDGSP-10** | Kiểm tra cột Điểm trong bảng | 1. Truy cập /admin/reviews<br>2. Kiểm tra cột Điểm | Hiển thị số sao (icon Star màu vàng), số điểm (VD: 4.5/5) | | Pass | 11/15/2015 | |
| **GUI-XDGSP-11** | Kiểm tra cột Nội dung trong bảng | 1. Truy cập /admin/reviews<br>2. Kiểm tra cột Nội dung | Hiển thị nội dung đánh giá (text-sm), có thể truncate nếu quá dài | | Pass | 11/15/2015 | |
| **GUI-XDGSP-12** | Kiểm tra cột Trạng thái trong bảng | 1. Truy cập /admin/reviews<br>2. Kiểm tra cột Trạng thái | Hiển thị Badge với màu tương ứng: Chờ duyệt (secondary), Đã duyệt (default), Từ chối (destructive), Hiển thị (outline), Ẩn (secondary), Vi phạm (destructive) | | Pass | 11/15/2015 | |
| **GUI-XDGSP-13** | Kiểm tra cột Thao tác trong bảng | 1. Truy cập /admin/reviews<br>2. Kiểm tra cột Thao tác | Hiển thị nút "Xem chi tiết" (icon Eye link đến /admin/reviews/[id]) | | Pass | 11/15/2015 | |
| **GUI-XDGSP-14** | Kiểm tra Pagination | 1. Truy cập /admin/reviews<br>2. Kiểm tra Pagination | Hiển thị text "Hiển thị 1-X trong Y đánh giá", các nút phân trang: Trước (disabled), số trang, Sau | | Pass | 11/15/2015 | |

---

### Check FUNC: Xem đánh giá sản phẩm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XDGSP-01** | Mở trang đánh giá sản phẩm | 1. Truy cập /admin/reviews | Hiển thị trang với tiêu đề, mô tả, bộ lọc sản phẩm, bộ lọc điểm, bộ lọc trạng thái, trường tìm kiếm, bảng đánh giá, pagination | | Pass | 11/15/2015 | |
| **FUNC-XDGSP-02** | Hiển thị danh sách đánh giá mặc định | 1. Truy cập /admin/reviews | Hiển thị tất cả đánh giá trong bảng, mỗi đánh giá có đầy đủ thông tin: sản phẩm, người đánh giá, điểm, nội dung, trạng thái, ngày, nút xem chi tiết | | Pass | 11/15/2015 | |
| **FUNC-XDGSP-03** | Lọc theo Sản phẩm | 1. Truy cập /admin/reviews<br>2. Chọn sản phẩm<br>3. Kiểm tra danh sách | Hiển thị danh sách đánh giá của sản phẩm đã chọn | | Untested | 11/15/2015 | |
| **FUNC-XDGSP-04** | Lọc theo Điểm | 1. Truy cập /admin/reviews<br>2. Chọn điểm (VD: 5 sao)<br>3. Kiểm tra danh sách | Hiển thị danh sách đánh giá có điểm đã chọn | | Untested | 11/15/2015 | |
| **FUNC-XDGSP-05** | Lọc theo Trạng thái | 1. Truy cập /admin/reviews<br>2. Chọn trạng thái (VD: Chờ duyệt)<br>3. Kiểm tra danh sách | Hiển thị danh sách đánh giá có trạng thái đã chọn | | Untested | 11/15/2015 | |
| **FUNC-XDGSP-06** | Tìm kiếm đánh giá | 1. Truy cập /admin/reviews<br>2. Nhập từ khóa tìm kiếm (nội dung hoặc tên khách hàng)<br>3. Nhấn Enter | Hiển thị danh sách đánh giá phù hợp với từ khóa tìm kiếm | | Untested | 11/15/2015 | |
| **FUNC-XDGSP-07** | Click nút Xem chi tiết | 1. Truy cập /admin/reviews<br>2. Click nút "Xem chi tiết" của một đánh giá | Chuyển đến trang chi tiết đánh giá /admin/reviews/[id] | | Pass | 11/15/2015 | |
| **FUNC-XDGSP-08** | Xử lý khi không có đánh giá | 1. Truy cập /admin/reviews<br>2. Lọc để không có đánh giá nào | Hiển thị thông báo "Không tìm thấy đánh giá nào" hoặc bảng trống | | Untested | 11/15/2015 | |
| **FUNC-XDGSP-09** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/reviews<br>2. Tắt kết nối mạng | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại" | | Untested | 11/15/2015 | |
| **FUNC-XDGSP-10** | Xử lý khi server lỗi | 1. Truy cập /admin/reviews<br>2. Server trả về lỗi 500 | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau" | | Untested | 11/15/2015 | |

---

### Function: Xem chi tiết đánh giá

#### Check GUI: Xem chi tiết đánh giá

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CTDG-01** | Kiểm tra nút Quay lại | 1. Truy cập /admin/reviews/[id]<br>2. Kiểm tra nút Quay lại | Hiển thị nút "Quay lại" với icon ArrowLeft variant outline size sm, link đến /admin/reviews | | Pass | 11/15/2015 | |
| **GUI-CTDG-02** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/reviews/[id]<br>2. Kiểm tra tiêu đề | Hiển thị "Chi tiết đánh giá #[id]" với kích thước text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-CTDG-03** | Kiểm tra card Thông tin sản phẩm | 1. Truy cập /admin/reviews/[id]<br>2. Kiểm tra card | Hiển thị card "Thông tin sản phẩm" với: Tên sản phẩm (icon Package), SKU, ảnh sản phẩm (nếu có) | | Pass | 11/15/2015 | |
| **GUI-CTDG-04** | Kiểm tra card Người đánh giá | 1. Truy cập /admin/reviews/[id]<br>2. Kiểm tra card | Hiển thị card "Người đánh giá" với: Tên (icon User), Email (icon Mail), Badge "Đã mua" (nếu đã mua sản phẩm) | | Pass | 11/15/2015 | |
| **GUI-CTDG-05** | Kiểm tra Badge Điểm đánh giá | 1. Truy cập /admin/reviews/[id]<br>2. Kiểm tra Badge | Hiển thị Badge "Điểm đánh giá" với số sao (icon Star màu vàng), số điểm (VD: 4.5/5) | | Pass | 11/15/2015 | |
| **GUI-CTDG-06** | Kiểm tra Text Nội dung | 1. Truy cập /admin/reviews/[id]<br>2. Kiểm tra Text | Hiển thị "Nội dung đánh giá" với nội dung chi tiết (text-sm) | | Pass | 11/15/2015 | |
| **GUI-CTDG-07** | Kiểm tra Gallery Ảnh/Video | 1. Truy cập /admin/reviews/[id]<br>2. Kiểm tra Gallery | Hiển thị Gallery "Ảnh/Video" với các media đính kèm, có thể xem preview hoặc phóng to | | Pass | 11/15/2015 | |
| **GUI-CTDG-08** | Kiểm tra Badge Trạng thái | 1. Truy cập /admin/reviews/[id]<br>2. Kiểm tra Badge | Hiển thị Badge trạng thái với màu tương ứng: Chờ duyệt (secondary), Đã duyệt (default), Từ chối (destructive), Hiển thị (outline), Ẩn (secondary), Vi phạm (destructive) | | Pass | 11/15/2015 | |
| **GUI-CTDG-09** | Kiểm tra nút Duyệt | 1. Truy cập /admin/reviews/[id]<br>2. Kiểm tra nút | Hiển thị nút "Duyệt" với icon CheckCircle variant default, chỉ hiển thị khi trạng thái là "Chờ duyệt" | | Pass | 11/15/2015 | |
| **GUI-CTDG-10** | Kiểm tra nút Từ chối | 1. Truy cập /admin/reviews/[id]<br>2. Kiểm tra nút | Hiển thị nút "Từ chối" với icon XCircle variant destructive, chỉ hiển thị khi trạng thái là "Chờ duyệt" | | Pass | 11/15/2015 | |
| **GUI-CTDG-11** | Kiểm tra nút Phản hồi | 1. Truy cập /admin/reviews/[id]<br>2. Kiểm tra nút | Hiển thị nút "Phản hồi" với icon Reply variant outline | | Pass | 11/15/2015 | |
| **GUI-CTDG-12** | Kiểm tra nút Ẩn/Xóa | 1. Truy cập /admin/reviews/[id]<br>2. Kiểm tra nút | Hiển thị nút "Ẩn" (icon EyeOff) hoặc "Xóa" (icon Trash2) variant destructive | | Pass | 11/15/2015 | |

---

### Check FUNC: Xem chi tiết đánh giá

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CTDG-01** | Mở trang chi tiết đánh giá | 1. Truy cập /admin/reviews/[id] | Hiển thị trang với nút Quay lại, tiêu đề, card Thông tin sản phẩm, card Người đánh giá, Badge Điểm đánh giá, Text Nội dung, Gallery Ảnh/Video, Badge Trạng thái, nút Duyệt, nút Từ chối, nút Phản hồi, nút Ẩn/Xóa | | Pass | 11/15/2015 | |
| **FUNC-CTDG-02** | Hiển thị đầy đủ thông tin đánh giá | 1. Truy cập /admin/reviews/[id] | Hiển thị đầy đủ nội dung, media, meta, trạng thái moderation được hiển thị rõ ràng | | Pass | 11/15/2015 | |
| **FUNC-CTDG-03** | Click nút Quay lại | 1. Truy cập /admin/reviews/[id]<br>2. Click nút "Quay lại" | Chuyển về trang /admin/reviews | | Pass | 11/15/2015 | |
| **FUNC-CTDG-04** | Xem ảnh/Video trong Gallery | 1. Truy cập /admin/reviews/[id]<br>2. Click vào ảnh/Video trong Gallery | Hiển thị preview hoặc phóng to ảnh/Video | | Pass | 11/15/2015 | |
| **FUNC-CTDG-05** | Click nút Duyệt | 1. Truy cập /admin/reviews/[id]<br>2. Click nút "Duyệt" | Mở dialog xác nhận duyệt hoặc duyệt trực tiếp | | Pass | 11/15/2015 | |
| **FUNC-CTDG-06** | Click nút Từ chối | 1. Truy cập /admin/reviews/[id]<br>2. Click nút "Từ chối" | Mở dialog xác nhận từ chối với lý do | | Pass | 11/15/2015 | |
| **FUNC-CTDG-07** | Click nút Phản hồi | 1. Truy cập /admin/reviews/[id]<br>2. Click nút "Phản hồi" | Mở modal phản hồi đánh giá | | Pass | 11/15/2015 | |
| **FUNC-CTDG-08** | Click nút Ẩn/Xóa | 1. Truy cập /admin/reviews/[id]<br>2. Click nút "Ẩn" hoặc "Xóa" | Mở dialog xác nhận ẩn/xóa với lý do | | Pass | 11/15/2015 | |
| **FUNC-CTDG-09** | Xử lý khi đánh giá không tồn tại | 1. Truy cập /admin/reviews/[id không tồn tại] | Hiển thị thông báo lỗi "Đánh giá không tồn tại" hoặc chuyển về trang danh sách | | Untested | 11/15/2015 | |
| **FUNC-CTDG-10** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/reviews/[id]<br>2. Tắt kết nối mạng | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại" | Untested | 11/15/2015 | |
| **FUNC-CTDG-11** | Xử lý khi server lỗi | 1. Truy cập /admin/reviews/[id]<br>2. Server trả về lỗi 500 | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau" | | Untested | 11/15/2015 | |

---

### Function: Duyệt đánh giá

#### Check GUI: Duyệt đánh giá

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DDG-01** | Kiểm tra dialog Xác nhận duyệt | 1. Truy cập /admin/reviews/[id]<br>2. Click nút "Duyệt"<br>3. Kiểm tra dialog | Hiển thị Dialog với tiêu đề "Xác nhận duyệt đánh giá", mô tả "Bạn có chắc chắn muốn duyệt đánh giá này? Đánh giá sẽ được hiển thị công khai", nút "Hủy" variant outline, nút "Duyệt" variant default | | Pass | 11/15/2015 | |

---

### Check FUNC: Duyệt đánh giá

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DDG-01** | Duyệt đánh giá thành công | 1. Truy cập /admin/reviews/[id]<br>2. Click nút "Duyệt"<br>3. Click "Duyệt" trong dialog | Hiển thị thông báo "Duyệt đánh giá thành công", trạng thái đánh giá chuyển thành "Đã duyệt", đánh giá được hiển thị công khai cho người dùng khác xem, nút Duyệt và Từ chối biến mất | | Untested | 11/15/2015 | |
| **FUNC-DDG-02** | Hủy duyệt đánh giá | 1. Truy cập /admin/reviews/[id]<br>2. Click nút "Duyệt"<br>3. Click "Hủy" trong dialog | Dialog đóng, đánh giá không được duyệt, trạng thái không thay đổi | | Pass | 11/15/2015 | |
| **FUNC-DDG-03** | Duyệt đánh giá - Trạng thái không phải Chờ duyệt | 1. Truy cập /admin/reviews/[id có trạng thái Đã duyệt]<br>2. Kiểm tra nút Duyệt | Nút "Duyệt" không hiển thị hoặc disabled | | Pass | 11/15/2015 | |
| **FUNC-DDG-04** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/reviews/[id]<br>2. Click nút "Duyệt"<br>3. Tắt kết nối mạng<br>4. Click "Duyệt" trong dialog | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", đánh giá không được duyệt | | Untested | 11/15/2015 | |
| **FUNC-DDG-05** | Xử lý khi server lỗi | 1. Truy cập /admin/reviews/[id]<br>2. Click nút "Duyệt"<br>3. Server trả về lỗi 500<br>4. Click "Duyệt" trong dialog | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau", đánh giá không được duyệt | | Untested | 11/15/2015 | |

---

### Function: Từ chối đánh giá

#### Check GUI: Từ chối đánh giá

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-TCDG-01** | Kiểm tra dialog Từ chối đánh giá | 1. Truy cập /admin/reviews/[id]<br>2. Click nút "Từ chối"<br>3. Kiểm tra dialog | Hiển thị Dialog với tiêu đề "Từ chối đánh giá", mô tả "Bạn có chắc chắn muốn từ chối đánh giá này? Đánh giá sẽ không được hiển thị công khai", Textarea "Lý do từ chối *", nút "Hủy" variant outline, nút "Từ chối" variant destructive | | Pass | 11/15/2015 | |

---

### Check FUNC: Từ chối đánh giá

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TCDG-01** | Từ chối đánh giá thành công | 1. Truy cập /admin/reviews/[id]<br>2. Click nút "Từ chối"<br>3. Nhập lý do từ chối<br>4. Click "Từ chối" trong dialog | Hiển thị thông báo "Từ chối đánh giá thành công", trạng thái đánh giá chuyển thành "Từ chối", đánh giá không được hiển thị công khai, nút Duyệt và Từ chối biến mất | | Untested | 11/15/2015 | |
| **FUNC-TCDG-02** | Từ chối - Thiếu Lý do từ chối | 1. Truy cập /admin/reviews/[id]<br>2. Click nút "Từ chối"<br>3. Để trống lý do<br>4. Click "Từ chối" trong dialog | Hiển thị thông báo lỗi "Lý do từ chối không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-TCDG-03** | Hủy từ chối đánh giá | 1. Truy cập /admin/reviews/[id]<br>2. Click nút "Từ chối"<br>3. Click "Hủy" trong dialog | Dialog đóng, đánh giá không bị từ chối, trạng thái không thay đổi | | Pass | 11/15/2015 | |
| **FUNC-TCDG-04** | Từ chối đánh giá - Trạng thái không phải Chờ duyệt | 1. Truy cập /admin/reviews/[id có trạng thái Đã duyệt]<br>2. Kiểm tra nút Từ chối | Nút "Từ chối" không hiển thị hoặc disabled | | Pass | 11/15/2015 | |
| **FUNC-TCDG-05** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/reviews/[id]<br>2. Click nút "Từ chối"<br>3. Nhập lý do<br>4. Tắt kết nối mạng<br>5. Click "Từ chối" trong dialog | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", đánh giá không bị từ chối | | Untested | 11/15/2015 | |
| **FUNC-TCDG-06** | Xử lý khi server lỗi | 1. Truy cập /admin/reviews/[id]<br>2. Click nút "Từ chối"<br>3. Nhập lý do<br>4. Server trả về lỗi 500<br>5. Click "Từ chối" trong dialog | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau", đánh giá không bị từ chối | | Untested | 11/15/2015 | |

---

### Function: Xóa đánh giá sản phẩm

#### Check GUI: Xóa đánh giá sản phẩm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XDG-01** | Kiểm tra dialog Xác nhận xóa | 1. Truy cập /admin/reviews/[id]<br>2. Click nút "Xóa"<br>3. Kiểm tra dialog | Hiển thị Dialog với tiêu đề "Xác nhận xóa đánh giá", mô tả "Bạn có chắc chắn muốn xóa đánh giá này? Hành động này không thể hoàn tác. Đánh giá vi phạm/spam sẽ bị xóa vĩnh viễn", Textarea "Lý do xóa *", nút "Hủy" variant outline, nút "Xóa vĩnh viễn" variant destructive | | Pass | 11/15/2015 | |

---

### Check FUNC: Xóa đánh giá sản phẩm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XDG-01** | Xóa đánh giá thành công | 1. Truy cập /admin/reviews/[id]<br>2. Click nút "Xóa"<br>3. Nhập lý do xóa<br>4. Click "Xóa vĩnh viễn" trong dialog | Hiển thị thông báo "Xóa đánh giá thành công", đánh giá bị xóa vĩnh viễn, lịch sử ghi nhận, chuyển về trang danh sách | | Untested | 11/15/2015 | |
| **FUNC-XDG-02** | Xóa - Thiếu Lý do xóa | 1. Truy cập /admin/reviews/[id]<br>2. Click nút "Xóa"<br>3. Để trống lý do<br>4. Click "Xóa vĩnh viễn" trong dialog | Hiển thị thông báo lỗi "Lý do xóa không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-XDG-03** | Hủy xóa đánh giá | 1. Truy cập /admin/reviews/[id]<br>2. Click nút "Xóa"<br>3. Click "Hủy" trong dialog | Dialog đóng, đánh giá không bị xóa, vẫn ở trang chi tiết | | Pass | 11/15/2015 | |
| **FUNC-XDG-04** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/reviews/[id]<br>2. Click nút "Xóa"<br>3. Nhập lý do<br>4. Tắt kết nối mạng<br>5. Click "Xóa vĩnh viễn" trong dialog | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", đánh giá không bị xóa | | Untested | 11/15/2015 | |
| **FUNC-XDG-05** | Xử lý khi server lỗi | 1. Truy cập /admin/reviews/[id]<br>2. Click nút "Xóa"<br>3. Nhập lý do<br>4. Server trả về lỗi 500<br>5. Click "Xóa vĩnh viễn" trong dialog | Hiển thị thông báo lỗi "Lỗi xóa đánh giá", đánh giá không bị xóa | | Untested | 11/15/2015 | |

---

### Function: Phản hồi đánh giá

#### Check GUI: Phản hồi đánh giá

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-PHDG-01** | Kiểm tra modal Phản hồi đánh giá | 1. Truy cập /admin/reviews/[id]<br>2. Click nút "Phản hồi"<br>3. Kiểm tra modal | Hiển thị Dialog với tiêu đề "Phản hồi đánh giá", mô tả "Admin phản hồi công khai dưới đánh giá" | | Pass | 11/15/2015 | |
| **GUI-PHDG-02** | Kiểm tra Textarea Nội dung phản hồi | 1. Truy cập /admin/reviews/[id]<br>2. Click nút "Phản hồi"<br>3. Kiểm tra Textarea | Hiển thị label "Nội dung phản hồi *", Textarea với placeholder "Nhập nội dung phản hồi...", rows 4 | | Pass | 11/15/2015 | |
| **GUI-PHDG-03** | Kiểm tra nút Hủy | 1. Truy cập /admin/reviews/[id]<br>2. Click nút "Phản hồi"<br>3. Kiểm tra nút | Hiển thị nút "Hủy" variant outline | | Pass | 11/15/2015 | |
| **GUI-PHDG-04** | Kiểm tra nút Gửi phản hồi | 1. Truy cập /admin/reviews/[id]<br>2. Click nút "Phản hồi"<br>3. Kiểm tra nút | Hiển thị nút "Gửi phản hồi" type submit | | Pass | 11/15/2015 | |

---

### Check FUNC: Phản hồi đánh giá

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-PHDG-01** | Mở modal phản hồi đánh giá | 1. Truy cập /admin/reviews/[id]<br>2. Click nút "Phản hồi" | Hiển thị Dialog với tiêu đề "Phản hồi đánh giá", mô tả, Textarea Nội dung phản hồi, nút Hủy, nút Gửi phản hồi | | Pass | 11/15/2015 | |
| **FUNC-PHDG-02** | Phản hồi đánh giá thành công | 1. Truy cập /admin/reviews/[id]<br>2. Click nút "Phản hồi"<br>3. Nhập nội dung phản hồi<br>4. Click "Gửi phản hồi" | Hiển thị thông báo "Gửi phản hồi thành công", phản hồi được đăng công khai dưới đánh giá, lưu thời gian và người phản hồi, modal đóng | | Untested | 11/15/2015 | |
| **FUNC-PHDG-03** | Phản hồi - Thiếu Nội dung phản hồi | 1. Truy cập /admin/reviews/[id]<br>2. Click nút "Phản hồi"<br>3. Để trống nội dung<br>4. Click "Gửi phản hồi" | Hiển thị thông báo lỗi "Nội dung phản hồi không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-PHDG-04** | Click nút Hủy | 1. Truy cập /admin/reviews/[id]<br>2. Click nút "Phản hồi"<br>3. Click "Hủy" | Modal đóng, không gửi phản hồi | | Pass | 11/15/2015 | |
| **FUNC-PHDG-05** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/reviews/[id]<br>2. Click nút "Phản hồi"<br>3. Nhập nội dung<br>4. Tắt kết nối mạng<br>5. Click "Gửi phản hồi" | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", form không được gửi | | Untested | 11/15/2015 | |
| **FUNC-PHDG-06** | Xử lý khi server lỗi | 1. Truy cập /admin/reviews/[id]<br>2. Click nút "Phản hồi"<br>3. Nhập nội dung<br>4. Server trả về lỗi 500<br>5. Click "Gửi phản hồi" | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau", form không được gửi | | Untested | 11/15/2015 | |

---

**Người tạo:** Testing Team  
**Ngày cập nhật:** 11/15/2015  
**Phiên bản:** 1.0

