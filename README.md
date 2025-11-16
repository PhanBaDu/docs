# Test Case Template - Quản lý bài viết (Admin)

## Module Code
**Model Management Store: Quản lý bài viết Admin**

## Test Requirement
1. Hiển thị danh sách bài viết
2. Xem chi tiết bài viết
3. Xóa bài viết
4. Chỉnh sửa bài viết
5. Xóa bình luận
6. Khóa tài khoản đăng bài
7. Tìm kiếm và lọc bài viết

---

## Test Summary

### Người thực hiện Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 53 |
| **Fail** | 0 |
| **Untested** | 50 |
| **N/A** | 0 |
| **Number of Test cases** | 103 |

---

## Test Cases

### Function: Hiển thị danh sách bài viết

#### Check GUI: Hiển thị danh sách bài viết

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-HDSLBV-01** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/posts<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Quản lý bài viết" với kích thước text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-HDSLBV-02** | Kiểm tra mô tả chức năng | 1. Truy cập /admin/posts<br>2. Kiểm tra mô tả | Hiển thị mô tả "Admin xem toàn bộ bài viết đã đăng" màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-HDSLBV-03** | Kiểm tra Select Bộ lọc danh mục | 1. Truy cập /admin/posts<br>2. Kiểm tra Select | Hiển thị Select "Danh mục" với placeholder "Tất cả danh mục", có các option: Gundam, Figure, Mô hình xe, Máy bay, Khác, Tất cả | | Pass | 11/15/2015 | |
| **GUI-HDSLBV-04** | Kiểm tra Select Bộ lọc thời gian | 1. Truy cập /admin/posts<br>2. Kiểm tra Select | Hiển thị Select "Thời gian" với placeholder "Chọn thời gian", có các option: Hôm nay, Tuần này, Tháng này, Tất cả | | Pass | 11/15/2015 | |
| **GUI-HDSLBV-05** | Kiểm tra Select Bộ lọc trạng thái | 1. Truy cập /admin/posts<br>2. Kiểm tra Select | Hiển thị Select "Trạng thái" với placeholder "Chọn trạng thái", có các option: Hiển thị, Ẩn, Vi phạm, Tất cả | | Pass | 11/15/2015 | |
| **GUI-HDSLBV-06** | Kiểm tra Input Tìm kiếm | 1. Truy cập /admin/posts<br>2. Kiểm tra Input | Hiển thị Input "Tìm kiếm" với placeholder "Tìm theo tiêu đề, nội dung, người đăng...", có icon Search | | Pass | 11/15/2015 | |
| **GUI-HDSLBV-07** | Kiểm tra Table danh sách bài viết | 1. Truy cập /admin/posts<br>2. Kiểm tra Table | Hiển thị Table với các cột: STT, Tiêu đề, Người đăng, Danh mục, Thời gian, Like, Comment, Trạng thái, Thao tác | | Pass | 11/15/2015 | |
| **GUI-HDSLBV-08** | Kiểm tra nút Xem chi tiết | 1. Truy cập /admin/posts<br>2. Kiểm tra nút trong Table | Mỗi dòng có nút "Xem chi tiết" với icon Eye | | Pass | 11/15/2015 | |
| **GUI-HDSLBV-09** | Kiểm tra Pagination | 1. Truy cập /admin/posts<br>2. Kiểm tra Pagination | Hiển thị Pagination với nút Previous, Next, số trang, số bài viết mỗi trang | | Pass | 11/15/2015 | |

---

### Check FUNC: Hiển thị danh sách bài viết

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-HDSLBV-01** | Mở trang danh sách bài viết | 1. Truy cập /admin/posts | Hiển thị danh sách bài viết với đầy đủ thông tin: tiêu đề, người đăng, danh mục, thời gian, like, comment, trạng thái, các bộ lọc và tìm kiếm | | Pass | 11/15/2015 | |
| **FUNC-HDSLBV-02** | Hiển thị danh sách khi có dữ liệu | 1. Truy cập /admin/posts<br>2. Có dữ liệu bài viết | Hiển thị danh sách bài viết trong Table, mỗi dòng hiển thị đầy đủ thông tin, có nút Xem chi tiết | | Pass | 11/15/2015 | |
| **FUNC-HDSLBV-03** | Hiển thị khi không có dữ liệu | 1. Truy cập /admin/posts<br>2. Không có dữ liệu bài viết | Hiển thị thông báo "Không có bài viết nào" hoặc "Chưa có bài viết", Table rỗng | | Pass | 11/15/2015 | |
| **FUNC-HDSLBV-04** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/posts<br>2. Tắt kết nối mạng | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại" | | Untested | 11/15/2015 | |
| **FUNC-HDSLBV-05** | Xử lý khi server lỗi | 1. Truy cập /admin/posts<br>2. Server trả về lỗi 500 | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau" | | Untested | 11/15/2015 | |

---

### Function: Xem chi tiết bài viết

#### Check GUI: Xem chi tiết bài viết

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XCTBV-01** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/posts/[id]<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Chi tiết bài viết" với kích thước text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-XCTBV-02** | Kiểm tra Card Thông tin tác giả | 1. Truy cập /admin/posts/[id]<br>2. Kiểm tra Card | Hiển thị Card "Thông tin tác giả" với: Avatar, Tên, Số bài viết, Rank | | Pass | 11/15/2015 | |
| **GUI-XCTBV-03** | Kiểm tra Nội dung bài viết | 1. Truy cập /admin/posts/[id]<br>2. Kiểm tra nội dung | Hiển thị tiêu đề bài viết, nội dung đầy đủ, thời gian đăng | | Pass | 11/15/2015 | |
| **GUI-XCTBV-04** | Kiểm tra Gallery Hình ảnh | 1. Truy cập /admin/posts/[id]<br>2. Kiểm tra Gallery | Hiển thị Gallery hình ảnh với các ảnh của bài viết, có thể xem phóng to | | Pass | 11/15/2015 | |
| **GUI-XCTBV-05** | Kiểm tra Video | 1. Truy cập /admin/posts/[id]<br>2. Kiểm tra Video | Hiển thị Video player nếu bài viết có video | | Pass | 11/15/2015 | |
| **GUI-XCTBV-06** | Kiểm tra Card Thông tin tương tác | 1. Truy cập /admin/posts/[id]<br>2. Kiểm tra Card | Hiển thị Card với: số Like, số Comment, số Share, số View | | Pass | 11/15/2015 | |
| **GUI-XCTBV-07** | Kiểm tra Danh sách bình luận | 1. Truy cập /admin/posts/[id]<br>2. Kiểm tra danh sách | Hiển thị danh sách bình luận với: Avatar người bình luận, Tên, Nội dung, Thời gian, nút Xóa bình luận | | Pass | 11/15/2015 | |
| **GUI-XCTBV-08** | Kiểm tra nút Chỉnh sửa | 1. Truy cập /admin/posts/[id]<br>2. Kiểm tra nút | Hiển thị nút "Chỉnh sửa" với icon Edit | | Pass | 11/15/2015 | |
| **GUI-XCTBV-09** | Kiểm tra nút Xóa bài viết | 1. Truy cập /admin/posts/[id]<br>2. Kiểm tra nút | Hiển thị nút "Xóa bài viết" với icon Trash2, màu destructive | | Pass | 11/15/2015 | |
| **GUI-XCTBV-10** | Kiểm tra nút Khóa tài khoản | 1. Truy cập /admin/posts/[id]<br>2. Kiểm tra nút | Hiển thị nút "Khóa tài khoản" với icon Flag | | Pass | 11/15/2015 | |
| **GUI-XCTBV-11** | Kiểm tra nút Quay lại | 1. Truy cập /admin/posts/[id]<br>2. Kiểm tra nút | Hiển thị nút "Quay lại" để quay về danh sách | | Pass | 11/15/2015 | |

---

### Check FUNC: Xem chi tiết bài viết

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XCTBV-01** | Mở trang chi tiết bài viết | 1. Truy cập /admin/posts<br>2. Click "Xem chi tiết" trên một bài viết | Hiển thị trang chi tiết với đầy đủ thông tin: thông tin tác giả, nội dung bài viết, hình ảnh/video, thông tin tương tác, danh sách bình luận | | Pass | 11/15/2015 | |
| **FUNC-XCTBV-02** | Hiển thị đầy đủ thông tin bài viết | 1. Truy cập /admin/posts/[id]<br>2. Kiểm tra thông tin | Hiển thị đầy đủ: tiêu đề, nội dung, tác giả, thời gian, like, comment, share, view, hình ảnh/video | | Pass | 11/15/2015 | |
| **FUNC-XCTBV-03** | Hiển thị danh sách bình luận | 1. Truy cập /admin/posts/[id]<br>2. Kiểm tra bình luận | Hiển thị danh sách bình luận với đầy đủ thông tin: người bình luận, nội dung, thời gian | | Pass | 11/15/2015 | |
| **FUNC-XCTBV-04** | Hiển thị khi không có bình luận | 1. Truy cập /admin/posts/[id]<br>2. Bài viết không có bình luận | Hiển thị thông báo "Chưa có bình luận nào" | | Pass | 11/15/2015 | |
| **FUNC-XCTBV-05** | Xử lý khi bài viết không tồn tại | 1. Truy cập /admin/posts/[id không tồn tại] | Hiển thị thông báo lỗi "Bài viết không tồn tại" hoặc redirect về danh sách | | Pass | 11/15/2015 | |
| **FUNC-XCTBV-06** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/posts/[id]<br>2. Tắt kết nối mạng | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại" | | Untested | 11/15/2015 | |
| **FUNC-XCTBV-07** | Xử lý khi server lỗi | 1. Truy cập /admin/posts/[id]<br>2. Server trả về lỗi 500 | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau" | | Untested | 11/15/2015 | |

---

### Function: Xóa bài viết

#### Check GUI: Xóa bài viết

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XBV-01** | Kiểm tra Modal xác nhận xóa | 1. Truy cập /admin/posts/[id]<br>2. Click "Xóa bài viết"<br>3. Kiểm tra Modal | Hiển thị Modal "Xác nhận xóa bài viết" với: tiêu đề, nội dung cảnh báo, Input lý do xóa, nút "Hủy", nút "Xác nhận xóa" | | Pass | 11/15/2015 | |
| **GUI-XBV-02** | Kiểm tra Input Lý do xóa | 1. Mở Modal xóa<br>2. Kiểm tra Input | Hiển thị label "Lý do xóa *", Textarea với placeholder "Nhập lý do xóa bài viết..." | | Pass | 11/15/2015 | |
| **GUI-XBV-03** | Kiểm tra nút Hủy | 1. Mở Modal xóa<br>2. Kiểm tra nút | Hiển thị nút "Hủy" variant outline, đóng Modal khi click | | Pass | 11/15/2015 | |
| **GUI-XBV-04** | Kiểm tra nút Xác nhận xóa | 1. Mở Modal xóa<br>2. Kiểm tra nút | Hiển thị nút "Xác nhận xóa" variant destructive | | Pass | 11/15/2015 | |

---

### Check FUNC: Xóa bài viết

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XBV-01** | Xóa bài viết thành công | 1. Truy cập /admin/posts/[id]<br>2. Click "Xóa bài viết"<br>3. Nhập lý do xóa<br>4. Click "Xác nhận xóa" | Hiển thị thông báo "Xóa bài viết thành công", bài viết bị xóa, redirect về danh sách, dữ liệu liên quan được dọn dẹp | | Untested | 11/15/2015 | |
| **FUNC-XBV-02** | Xóa - Thiếu lý do | 1. Truy cập /admin/posts/[id]<br>2. Click "Xóa bài viết"<br>3. Để trống lý do<br>4. Click "Xác nhận xóa" | Hiển thị thông báo lỗi "Vui lòng nhập lý do xóa", Modal không đóng, bài viết không bị xóa | | Pass | 11/15/2015 | |
| **FUNC-XBV-03** | Hủy xóa bài viết | 1. Truy cập /admin/posts/[id]<br>2. Click "Xóa bài viết"<br>3. Click "Hủy" | Modal đóng, bài viết không bị xóa, vẫn ở trang chi tiết | | Pass | 11/15/2015 | |
| **FUNC-XBV-04** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/posts/[id]<br>2. Click "Xóa bài viết"<br>3. Nhập lý do<br>4. Tắt kết nối mạng<br>5. Click "Xác nhận xóa" | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", bài viết không bị xóa | | Untested | 11/15/2015 | |
| **FUNC-XBV-05** | Xử lý khi server lỗi | 1. Truy cập /admin/posts/[id]<br>2. Click "Xóa bài viết"<br>3. Nhập lý do<br>4. Server trả về lỗi 500<br>5. Click "Xác nhận xóa" | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau", bài viết không bị xóa | | Untested | 11/15/2015 | |

---

### Function: Chỉnh sửa bài viết

#### Check GUI: Chỉnh sửa bài viết

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CSBV-01** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/posts/[id]<br>2. Click "Chỉnh sửa"<br>3. Kiểm tra tiêu đề | Hiển thị tiêu đề "Chỉnh sửa bài viết" với kích thước text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-CSBV-02** | Kiểm tra Form chỉnh sửa | 1. Mở form chỉnh sửa<br>2. Kiểm tra Form | Hiển thị Form với: Input "Tiêu đề *", Textarea "Nội dung *", Select "Danh mục", Select "Trạng thái", Upload hình ảnh, Upload video | | Pass | 11/15/2015 | |
| **GUI-CSBV-03** | Kiểm tra Input Tiêu đề | 1. Mở form chỉnh sửa<br>2. Kiểm tra Input | Hiển thị label "Tiêu đề *", input type text với giá trị hiện tại của bài viết | | Pass | 11/15/2015 | |
| **GUI-CSBV-04** | Kiểm tra Textarea Nội dung | 1. Mở form chỉnh sửa<br>2. Kiểm tra Textarea | Hiển thị label "Nội dung *", Textarea với giá trị hiện tại của bài viết | | Pass | 11/15/2015 | |
| **GUI-CSBV-05** | Kiểm tra Select Danh mục | 1. Mở form chỉnh sửa<br>2. Kiểm tra Select | Hiển thị label "Danh mục", Select với giá trị hiện tại, có các option: Gundam, Figure, Mô hình xe, Máy bay, Khác | | Pass | 11/15/2015 | |
| **GUI-CSBV-06** | Kiểm tra Select Trạng thái | 1. Mở form chỉnh sửa<br>2. Kiểm tra Select | Hiển thị label "Trạng thái", Select với giá trị hiện tại, có các option: Hiển thị, Ẩn, Vi phạm | | Pass | 11/15/2015 | |
| **GUI-CSBV-07** | Kiểm tra Upload hình ảnh | 1. Mở form chỉnh sửa<br>2. Kiểm tra Upload | Hiển thị label "Hình ảnh", Upload button, hiển thị danh sách hình ảnh hiện có, có thể xóa hoặc thêm mới | | Pass | 11/15/2015 | |
| **GUI-CSBV-08** | Kiểm tra Upload video | 1. Mở form chỉnh sửa<br>2. Kiểm tra Upload | Hiển thị label "Video", Upload button, hiển thị video hiện có (nếu có), có thể xóa hoặc thay thế | | Pass | 11/15/2015 | |
| **GUI-CSBV-09** | Kiểm tra nút Lưu thay đổi | 1. Mở form chỉnh sửa<br>2. Kiểm tra nút | Hiển thị nút "Lưu thay đổi" type submit | | Pass | 11/15/2015 | |
| **GUI-CSBV-10** | Kiểm tra nút Hủy | 1. Mở form chỉnh sửa<br>2. Kiểm tra nút | Hiển thị nút "Hủy" variant outline | | Pass | 11/15/2015 | |

---

### Check FUNC: Chỉnh sửa bài viết

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CSBV-01** | Mở form chỉnh sửa bài viết | 1. Truy cập /admin/posts/[id]<br>2. Click "Chỉnh sửa" | Hiển thị form chỉnh sửa với đầy đủ thông tin hiện tại của bài viết được điền sẵn | | Pass | 11/15/2015 | |
| **FUNC-CSBV-02** | Chỉnh sửa bài viết thành công | 1. Mở form chỉnh sửa<br>2. Sửa tiêu đề, nội dung, danh mục, trạng thái<br>3. Click "Lưu thay đổi" | Hiển thị thông báo "Cập nhật bài viết thành công", bài viết được cập nhật, hiển thị tức thì, redirect về chi tiết bài viết | | Untested | 11/15/2015 | |
| **FUNC-CSBV-03** | Chỉnh sửa - Thiếu tiêu đề | 1. Mở form chỉnh sửa<br>2. Xóa tiêu đề<br>3. Click "Lưu thay đổi" | Hiển thị thông báo lỗi "Tiêu đề không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-CSBV-04** | Chỉnh sửa - Thiếu nội dung | 1. Mở form chỉnh sửa<br>2. Xóa nội dung<br>3. Click "Lưu thay đổi" | Hiển thị thông báo lỗi "Nội dung không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-CSBV-05** | Chỉnh sửa - Thay đổi hình ảnh | 1. Mở form chỉnh sửa<br>2. Xóa hình ảnh cũ, upload hình ảnh mới<br>3. Click "Lưu thay đổi" | Hiển thị thông báo "Cập nhật bài viết thành công", hình ảnh mới được lưu và hiển thị | | Untested | 11/15/2015 | |
| **FUNC-CSBV-06** | Chỉnh sửa - Thay đổi video | 1. Mở form chỉnh sửa<br>2. Xóa video cũ, upload video mới<br>3. Click "Lưu thay đổi" | Hiển thị thông báo "Cập nhật bài viết thành công", video mới được lưu và hiển thị | | Untested | 11/15/2015 | |
| **FUNC-CSBV-07** | Click nút Hủy | 1. Mở form chỉnh sửa<br>2. Sửa thông tin<br>3. Click "Hủy" | Form đóng, quay về trang chi tiết, thay đổi không được lưu | | Pass | 11/15/2015 | |
| **FUNC-CSBV-08** | Xử lý khi mất kết nối mạng | 1. Mở form chỉnh sửa<br>2. Sửa thông tin<br>3. Tắt kết nối mạng<br>4. Click "Lưu thay đổi" | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", form không được gửi | | Untested | 11/15/2015 | |
| **FUNC-CSBV-09** | Xử lý khi server lỗi | 1. Mở form chỉnh sửa<br>2. Sửa thông tin<br>3. Server trả về lỗi 500<br>4. Click "Lưu thay đổi" | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau", form không được gửi | | Untested | 11/15/2015 | |

---

### Function: Xóa bình luận

#### Check GUI: Xóa bình luận

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XBL-01** | Kiểm tra nút Xóa bình luận | 1. Truy cập /admin/posts/[id]<br>2. Kiểm tra nút trong danh sách bình luận | Mỗi bình luận có nút "Xóa" với icon Trash2, màu destructive | | Pass | 11/15/2015 | |
| **GUI-XBL-02** | Kiểm tra Modal xác nhận xóa | 1. Click "Xóa" trên một bình luận<br>2. Kiểm tra Modal | Hiển thị Modal "Xác nhận xóa bình luận" với: tiêu đề, nội dung cảnh báo, Input lý do xóa, nút "Hủy", nút "Xác nhận xóa" | | Pass | 11/15/2015 | |
| **GUI-XBL-03** | Kiểm tra Input Lý do xóa | 1. Mở Modal xóa<br>2. Kiểm tra Input | Hiển thị label "Lý do xóa *", Textarea với placeholder "Nhập lý do xóa bình luận..." | | Pass | 11/15/2015 | |

---

### Check FUNC: Xóa bình luận

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XBL-01** | Xóa bình luận thành công | 1. Truy cập /admin/posts/[id]<br>2. Click "Xóa" trên một bình luận<br>3. Nhập lý do xóa<br>4. Click "Xác nhận xóa" | Hiển thị thông báo "Xóa bình luận thành công", bình luận bị xóa khỏi danh sách, lịch sử ghi nhận | | Untested | 11/15/2015 | |
| **FUNC-XBL-02** | Xóa - Thiếu lý do | 1. Truy cập /admin/posts/[id]<br>2. Click "Xóa" trên một bình luận<br>3. Để trống lý do<br>4. Click "Xác nhận xóa" | Hiển thị thông báo lỗi "Vui lòng nhập lý do xóa", Modal không đóng, bình luận không bị xóa | | Pass | 11/15/2015 | |
| **FUNC-XBL-03** | Hủy xóa bình luận | 1. Truy cập /admin/posts/[id]<br>2. Click "Xóa" trên một bình luận<br>3. Click "Hủy" | Modal đóng, bình luận không bị xóa | | Pass | 11/15/2015 | |
| **FUNC-XBL-04** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/posts/[id]<br>2. Click "Xóa" trên một bình luận<br>3. Nhập lý do<br>4. Tắt kết nối mạng<br>5. Click "Xác nhận xóa" | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", bình luận không bị xóa | | Untested | 11/15/2015 | |
| **FUNC-XBL-05** | Xử lý khi server lỗi | 1. Truy cập /admin/posts/[id]<br>2. Click "Xóa" trên một bình luận<br>3. Nhập lý do<br>4. Server trả về lỗi 500<br>5. Click "Xác nhận xóa" | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau", bình luận không bị xóa | | Untested | 11/15/2015 | |

---

### Function: Khóa tài khoản đăng bài

#### Check GUI: Khóa tài khoản đăng bài

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-KTTKDB-01** | Kiểm tra nút Khóa tài khoản | 1. Truy cập /admin/posts/[id]<br>2. Kiểm tra nút | Hiển thị nút "Khóa tài khoản" với icon Flag | | Pass | 11/15/2015 | |
| **GUI-KTTKDB-02** | Kiểm tra Modal khóa tài khoản | 1. Click "Khóa tài khoản"<br>2. Kiểm tra Modal | Hiển thị Modal "Khóa quyền đăng bài" với: tiêu đề, Form khóa, nút "Hủy", nút "Xác nhận khóa" | | Pass | 11/15/2015 | |
| **GUI-KTTKDB-03** | Kiểm tra Form khóa | 1. Mở Modal khóa<br>2. Kiểm tra Form | Hiển thị Form với: Select "Thời hạn *", Input "Lý do *", Textarea "Ghi chú" | | Pass | 11/15/2015 | |
| **GUI-KTTKDB-04** | Kiểm tra Select Thời hạn | 1. Mở Modal khóa<br>2. Kiểm tra Select | Hiển thị label "Thời hạn *", Select với placeholder "Chọn thời hạn", có các option: 1 ngày, 3 ngày, 7 ngày, 30 ngày, Vĩnh viễn | | Pass | 11/15/2015 | |
| **GUI-KTTKDB-05** | Kiểm tra Input Lý do | 1. Mở Modal khóa<br>2. Kiểm tra Input | Hiển thị label "Lý do *", Textarea với placeholder "Nhập lý do khóa quyền đăng bài..." | | Pass | 11/15/2015 | |
| **GUI-KTTKDB-06** | Kiểm tra nút Xác nhận khóa | 1. Mở Modal khóa<br>2. Kiểm tra nút | Hiển thị nút "Xác nhận khóa" variant destructive | | Pass | 11/15/2015 | |

---

### Check FUNC: Khóa tài khoản đăng bài

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-KTTKDB-01** | Khóa tài khoản đăng bài thành công | 1. Truy cập /admin/posts/[id]<br>2. Click "Khóa tài khoản"<br>3. Chọn thời hạn<br>4. Nhập lý do<br>5. Click "Xác nhận khóa" | Hiển thị thông báo "Khóa quyền đăng bài thành công", quyền đăng bài bị khóa, log sự kiện ghi nhận, tài khoản không thể đăng bài trong thời hạn đã chọn | | Untested | 11/15/2015 | |
| **FUNC-KTTKDB-02** | Khóa - Thiếu thời hạn | 1. Truy cập /admin/posts/[id]<br>2. Click "Khóa tài khoản"<br>3. Không chọn thời hạn<br>4. Nhập lý do<br>5. Click "Xác nhận khóa" | Hiển thị thông báo lỗi "Vui lòng chọn thời hạn", Modal không đóng, không khóa tài khoản | | Pass | 11/15/2015 | |
| **FUNC-KTTKDB-03** | Khóa - Thiếu lý do | 1. Truy cập /admin/posts/[id]<br>2. Click "Khóa tài khoản"<br>3. Chọn thời hạn<br>4. Để trống lý do<br>5. Click "Xác nhận khóa" | Hiển thị thông báo lỗi "Vui lòng nhập lý do", Modal không đóng, không khóa tài khoản | | Pass | 11/15/2015 | |
| **FUNC-KTTKDB-04** | Hủy khóa tài khoản | 1. Truy cập /admin/posts/[id]<br>2. Click "Khóa tài khoản"<br>3. Click "Hủy" | Modal đóng, tài khoản không bị khóa | | Pass | 11/15/2015 | |
| **FUNC-KTTKDB-05** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/posts/[id]<br>2. Click "Khóa tài khoản"<br>3. Điền đầy đủ thông tin<br>4. Tắt kết nối mạng<br>5. Click "Xác nhận khóa" | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", không khóa tài khoản | | Untested | 11/15/2015 | |
| **FUNC-KTTKDB-06** | Xử lý khi server lỗi | 1. Truy cập /admin/posts/[id]<br>2. Click "Khóa tài khoản"<br>3. Điền đầy đủ thông tin<br>4. Server trả về lỗi 500<br>5. Click "Xác nhận khóa" | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau", không khóa tài khoản | | Untested | 11/15/2015 | |

---

### Function: Tìm kiếm và lọc bài viết

#### Check GUI: Tìm kiếm và lọc bài viết

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-TKFLBV-01** | Kiểm tra Input Tìm kiếm | 1. Truy cập /admin/posts<br>2. Kiểm tra Input | Hiển thị Input "Tìm kiếm" với placeholder "Tìm theo tiêu đề, nội dung, người đăng...", có icon Search | | Pass | 11/15/2015 | |
| **GUI-TKFLBV-02** | Kiểm tra Select Lọc người dùng | 1. Truy cập /admin/posts<br>2. Kiểm tra Select | Hiển thị Select "Người đăng" với placeholder "Tất cả người dùng", có thể tìm kiếm và chọn người dùng | | Pass | 11/15/2015 | |
| **GUI-TKFLBV-03** | Kiểm tra Select Sắp xếp | 1. Truy cập /admin/posts<br>2. Kiểm tra Select | Hiển thị Select "Sắp xếp" với placeholder "Chọn sắp xếp", có các option: Mới nhất, Nhiều like, Nhiều bình luận | | Pass | 11/15/2015 | |
| **GUI-TKFLBV-04** | Kiểm tra nút Làm mới | 1. Truy cập /admin/posts<br>2. Kiểm tra nút | Hiển thị nút "Làm mới" với icon Refresh để reset bộ lọc | | Pass | 11/15/2015 | |

---

### Check FUNC: Tìm kiếm và lọc bài viết

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TKFLBV-01** | Tìm kiếm bài viết theo tiêu đề | 1. Truy cập /admin/posts<br>2. Nhập từ khóa vào ô tìm kiếm<br>3. Nhấn Enter hoặc click icon Search | Danh sách bài viết được cập nhật, chỉ hiển thị các bài viết có tiêu đề chứa từ khóa | | Pass | 11/15/2015 | |
| **FUNC-TKFLBV-02** | Tìm kiếm bài viết theo người đăng | 1. Truy cập /admin/posts<br>2. Nhập tên người đăng vào ô tìm kiếm<br>3. Nhấn Enter | Danh sách bài viết được cập nhật, chỉ hiển thị các bài viết của người đăng đó | | Pass | 11/15/2015 | |
| **FUNC-TKFLBV-03** | Lọc theo danh mục | 1. Truy cập /admin/posts<br>2. Chọn danh mục từ Select "Danh mục" | Danh sách bài viết được cập nhật, chỉ hiển thị các bài viết thuộc danh mục đã chọn | | Pass | 11/15/2015 | |
| **FUNC-TKFLBV-04** | Lọc theo thời gian | 1. Truy cập /admin/posts<br>2. Chọn thời gian từ Select "Thời gian" | Danh sách bài viết được cập nhật, chỉ hiển thị các bài viết trong khoảng thời gian đã chọn | | Pass | 11/15/2015 | |
| **FUNC-TKFLBV-05** | Lọc theo trạng thái | 1. Truy cập /admin/posts<br>2. Chọn trạng thái từ Select "Trạng thái" | Danh sách bài viết được cập nhật, chỉ hiển thị các bài viết có trạng thái đã chọn | | Pass | 11/15/2015 | |
| **FUNC-TKFLBV-06** | Lọc theo người dùng | 1. Truy cập /admin/posts<br>2. Chọn người dùng từ Select "Người đăng" | Danh sách bài viết được cập nhật, chỉ hiển thị các bài viết của người dùng đã chọn | | Pass | 11/15/2015 | |
| **FUNC-TKFLBV-07** | Sắp xếp theo Mới nhất | 1. Truy cập /admin/posts<br>2. Chọn "Mới nhất" từ Select "Sắp xếp" | Danh sách bài viết được sắp xếp theo thời gian đăng mới nhất | | Pass | 11/15/2015 | |
| **FUNC-TKFLBV-08** | Sắp xếp theo Nhiều like | 1. Truy cập /admin/posts<br>2. Chọn "Nhiều like" từ Select "Sắp xếp" | Danh sách bài viết được sắp xếp theo số lượng like giảm dần | | Pass | 11/15/2015 | |
| **FUNC-TKFLBV-09** | Sắp xếp theo Nhiều bình luận | 1. Truy cập /admin/posts<br>2. Chọn "Nhiều bình luận" từ Select "Sắp xếp" | Danh sách bài viết được sắp xếp theo số lượng bình luận giảm dần | | Pass | 11/15/2015 | |
| **FUNC-TKFLBV-10** | Kết hợp nhiều bộ lọc | 1. Truy cập /admin/posts<br>2. Chọn danh mục, thời gian, trạng thái, người dùng<br>3. Nhập từ khóa tìm kiếm<br>4. Chọn sắp xếp | Danh sách bài viết được cập nhật theo tất cả các tiêu chí đã chọn | | Pass | 11/15/2015 | |
| **FUNC-TKFLBV-11** | Tìm kiếm không có kết quả | 1. Truy cập /admin/posts<br>2. Nhập từ khóa không tồn tại<br>3. Nhấn Enter | Hiển thị thông báo "Không tìm thấy bài viết nào", Table rỗng | | Pass | 11/15/2015 | |
| **FUNC-TKFLBV-12** | Click nút Làm mới | 1. Truy cập /admin/posts<br>2. Áp dụng các bộ lọc<br>3. Click "Làm mới" | Tất cả bộ lọc được reset về mặc định, danh sách hiển thị tất cả bài viết | | Pass | 11/15/2015 | |
| **FUNC-TKFLBV-13** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/posts<br>2. Áp dụng bộ lọc<br>3. Tắt kết nối mạng | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại" | | Untested | 11/15/2015 | |

---

### Function: Layout - Quản lý bài viết

#### Check GUI: Layout - Quản lý bài viết

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-LAYOUT-BV-01** | Kiểm tra Header | 1. Truy cập /admin/posts<br>2. Kiểm tra Header | Hiển thị Header với logo, menu navigation, thông tin admin | | Pass | 11/15/2015 | |
| **GUI-LAYOUT-BV-02** | Kiểm tra Sidebar | 1. Truy cập /admin/posts<br>2. Kiểm tra Sidebar | Hiển thị Sidebar với menu Admin, có item "Quản lý bài viết" được highlight | | Pass | 11/15/2015 | |
| **GUI-LAYOUT-BV-03** | Kiểm tra Breadcrumb | 1. Truy cập /admin/posts<br>2. Kiểm tra Breadcrumb | Hiển thị Breadcrumb: Trang chủ > Quản lý bài viết | | Pass | 11/15/2015 | |
| **GUI-LAYOUT-BV-04** | Kiểm tra Footer | 1. Truy cập /admin/posts<br>2. Kiểm tra Footer | Hiển thị Footer với thông tin copyright, liên kết | | Pass | 11/15/2015 | |
| **GUI-LAYOUT-BV-05** | Kiểm tra Responsive trên mobile | 1. Truy cập /admin/posts trên mobile<br>2. Kiểm tra layout | Layout hiển thị đúng trên mobile, Sidebar có thể thu gọn, Table có thể scroll ngang | | Pass | 11/15/2015 | |
| **GUI-LAYOUT-BV-06** | Kiểm tra Responsive trên tablet | 1. Truy cập /admin/posts trên tablet<br>2. Kiểm tra layout | Layout hiển thị đúng trên tablet, các thành phần được sắp xếp hợp lý | | Pass | 11/15/2015 | |

---

**Người tạo:** Testing Team  
**Ngày cập nhật:** 11/15/2015  
**Phiên bản:** 1.0

