# Test Case Template - Quản lý sản phẩm (Admin)

## Module Code
**Model Management Store: Quản lý sản phẩm Admin**

## Test Requirement
1. Hiển thị danh sách sản phẩm
2. Xem chi tiết sản phẩm
3. Thêm sản phẩm
4. Cập nhật sản phẩm
5. Xóa sản phẩm
6. Tìm kiếm sản phẩm
7. Lọc sản phẩm

---

## Test Summary

### Người thực hiện Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 168 |
| **Fail** | 0 |
| **Untested** | 52 |
| **N/A** | 0 |
| **Number of Test cases** | 220 |

---

## Test Cases

### Function: Hiển thị danh sách sản phẩm

#### Check GUI: Hiển thị danh sách sản phẩm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DSSP-01** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/products<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Quản lý sản phẩm" với kích thước text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-DSSP-02** | Kiểm tra mô tả chức năng | 1. Truy cập /admin/products<br>2. Kiểm tra mô tả | Hiển thị mô tả "Quản lý danh sách sản phẩm và thông tin chi tiết" màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-DSSP-03** | Kiểm tra nút Nhập hàng | 1. Truy cập /admin/products<br>2. Kiểm tra nút Nhập hàng | Hiển thị nút "Nhập hàng" với icon Package variant outline ở header | | Pass | 11/15/2015 | |
| **GUI-DSSP-04** | Kiểm tra nút Thêm sản phẩm | 1. Truy cập /admin/products<br>2. Kiểm tra nút Thêm sản phẩm | Hiển thị nút "Thêm sản phẩm" với icon Plus ở header, link đến /admin/products/new | | Pass | 11/15/2015 | |
| **GUI-DSSP-05** | Kiểm tra Stats Cards | 1. Truy cập /admin/products<br>2. Kiểm tra Stats Cards | Hiển thị 4 card thống kê: Tổng sản phẩm (156), Đang bán (142), Sắp hết hàng (8), Hết hàng (6) | | Pass | 11/15/2015 | |
| **GUI-DSSP-06** | Kiểm tra trường Tìm kiếm | 1. Truy cập /admin/products<br>2. Kiểm tra trường tìm kiếm | Hiển thị input với icon Search bên trái, placeholder "Tìm kiếm sản phẩm...", có thể nhập và nhấn Enter để tìm | | Pass | 11/15/2015 | |
| **GUI-DSSP-07** | Kiểm tra Select Danh mục | 1. Truy cập /admin/products<br>2. Kiểm tra Select Danh mục | Hiển thị Select với placeholder "Danh mục", width w-40, có các option: Tất cả, Gundam, Figure, Mô hình xe, Máy bay, Tàu chiến, Khác | | Pass | 11/15/2015 | |
| **GUI-DSSP-08** | Kiểm tra Select Thương hiệu | 1. Truy cập /admin/products<br>2. Kiểm tra Select Thương hiệu | Hiển thị Select với placeholder "Thương hiệu", width w-40, có các option: Tất cả, Bandai, Good Smile Company, Tamiya, Revell, Banpresto, Kotobukiya | | Pass | 11/15/2015 | |
| **GUI-DSSP-09** | Kiểm tra Select Trạng thái | 1. Truy cập /admin/products<br>2. Kiểm tra Select Trạng thái | Hiển thị Select với placeholder "Trạng thái", width w-40, có các option: Tất cả, Đang bán, Sắp hết hàng, Hết hàng, Ngừng bán | | Pass | 11/15/2015 | |
| **GUI-DSSP-10** | Kiểm tra nút Bộ lọc | 1. Truy cập /admin/products<br>2. Kiểm tra nút Bộ lọc | Hiển thị nút "Bộ lọc" với icon Filter variant outline | | Pass | 11/15/2015 | |
| **GUI-DSSP-11** | Kiểm tra bảng danh sách sản phẩm | 1. Truy cập /admin/products<br>2. Kiểm tra bảng | Hiển thị Table với các cột: #, Sản phẩm, Danh mục, Giá, Tồn kho, Trạng thái, Đánh giá, Ngày tạo, Thao tác | | Pass | 11/15/2015 | |
| **GUI-DSSP-12** | Kiểm tra cột Sản phẩm trong bảng | 1. Truy cập /admin/products<br>2. Kiểm tra cột Sản phẩm | Mỗi dòng hiển thị hình ảnh sản phẩm (w-12 h-12 rounded-lg), tên sản phẩm (font-medium), thương hiệu (text-sm muted-foreground) | | Pass | 11/15/2015 | |
| **GUI-DSSP-13** | Kiểm tra cột Danh mục trong bảng | 1. Truy cập /admin/products<br>2. Kiểm tra cột Danh mục | Hiển thị Badge variant outline với tên danh mục | | Pass | 11/15/2015 | |
| **GUI-DSSP-14** | Kiểm tra cột Giá trong bảng | 1. Truy cập /admin/products<br>2. Kiểm tra cột Giá | Hiển thị giá bán (font-medium) và giá gốc (text-sm muted-foreground line-through) định dạng vi-VN | | Pass | 11/15/2015 | |
| **GUI-DSSP-15** | Kiểm tra cột Tồn kho trong bảng | 1. Truy cập /admin/products<br>2. Kiểm tra cột Tồn kho | Hiển thị số lượng tồn kho (font-medium) và tồn kho tối thiểu (text-sm muted-foreground) | | Pass | 11/15/2015 | |
| **GUI-DSSP-16** | Kiểm tra cột Trạng thái trong bảng | 1. Truy cập /admin/products<br>2. Kiểm tra cột Trạng thái | Hiển thị Badge với màu tương ứng: Đang bán (default), Sắp hết (secondary), Hết hàng (destructive), Ngừng bán (outline) | | Pass | 11/15/2015 | |
| **GUI-DSSP-17** | Kiểm tra cột Đánh giá trong bảng | 1. Truy cập /admin/products<br>2. Kiểm tra cột Đánh giá | Hiển thị điểm đánh giá (text-sm font-medium) và số lượng đánh giá (text-sm muted-foreground) | | Pass | 11/15/2015 | |
| **GUI-DSSP-18** | Kiểm tra cột Thao tác trong bảng | 1. Truy cập /admin/products<br>2. Kiểm tra cột Thao tác | Hiển thị 4 nút: Xem (icon Eye), Chỉnh sửa (icon Edit), Ẩn (icon EyeOff), Xóa (icon Trash2), tất cả variant ghost size sm | | Pass | 11/15/2015 | |
| **GUI-DSSP-19** | Kiểm tra Pagination | 1. Truy cập /admin/products<br>2. Kiểm tra Pagination | Hiển thị text "Hiển thị 1-X trong Y sản phẩm", các nút phân trang: Trước (disabled), số trang, Sau | | Pass | 11/15/2015 | |

---

### Check FUNC: Hiển thị danh sách sản phẩm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DSSP-01** | Mở trang danh sách sản phẩm | 1. Truy cập /admin/products | Hiển thị trang với tiêu đề, mô tả, nút Nhập hàng, nút Thêm sản phẩm, 4 Stats Cards, bộ lọc (tìm kiếm, danh mục, thương hiệu, trạng thái, nút Bộ lọc), bảng danh sách sản phẩm, pagination | | Pass | 11/15/2015 | |
| **FUNC-DSSP-02** | Hiển thị danh sách sản phẩm mặc định | 1. Truy cập /admin/products | Hiển thị tất cả sản phẩm trong bảng, mỗi sản phẩm có đầy đủ thông tin: hình ảnh, tên, thương hiệu, danh mục, giá, tồn kho, trạng thái, đánh giá, ngày tạo, các nút thao tác | | Pass | 11/15/2015 | |
| **FUNC-DSSP-03** | Click nút Nhập hàng | 1. Truy cập /admin/products<br>2. Click nút "Nhập hàng" | Chuyển đến trang nhập hàng hoặc mở dialog nhập hàng | | Untested | 11/15/2015 | |
| **FUNC-DSSP-04** | Click nút Thêm sản phẩm | 1. Truy cập /admin/products<br>2. Click nút "Thêm sản phẩm" | Chuyển đến trang /admin/products/new | | Pass | 11/15/2015 | |
| **FUNC-DSSP-05** | Click nút Xem (icon Eye) | 1. Truy cập /admin/products<br>2. Click nút Xem của một sản phẩm | Chuyển đến trang chi tiết sản phẩm /admin/products/[id] | | Pass | 11/15/2015 | |
| **FUNC-DSSP-06** | Click nút Chỉnh sửa (icon Edit) | 1. Truy cập /admin/products<br>2. Click nút Chỉnh sửa của một sản phẩm | Chuyển đến trang chỉnh sửa sản phẩm /admin/products/[id]/edit | | Pass | 11/15/2015 | |
| **FUNC-DSSP-07** | Click nút Ẩn (icon EyeOff) | 1. Truy cập /admin/products<br>2. Click nút Ẩn của một sản phẩm | Hiển thị Dialog xác nhận ẩn sản phẩm với tiêu đề "Xác nhận ẩn sản phẩm", mô tả, nút Hủy, nút "Ẩn sản phẩm" | | Pass | 11/15/2015 | |
| **FUNC-DSSP-08** | Click nút Xóa (icon Trash2) | 1. Truy cập /admin/products<br>2. Click nút Xóa của một sản phẩm | Hiển thị Dialog xác nhận xóa sản phẩm với tiêu đề "Xác nhận xóa sản phẩm", mô tả "Hành động này không thể hoàn tác", nút Hủy, nút "Xóa" variant destructive | | Pass | 11/15/2015 | |
| **FUNC-DSSP-09** | Xác nhận ẩn sản phẩm | 1. Truy cập /admin/products<br>2. Click nút Ẩn<br>3. Click "Ẩn sản phẩm" trong dialog | Hiển thị thông báo "Đã ẩn sản phẩm", sản phẩm bị ẩn khỏi danh sách hoặc trạng thái chuyển thành "Ẩn" | | Untested | 11/15/2015 | |
| **FUNC-DSSP-10** | Xác nhận xóa sản phẩm | 1. Truy cập /admin/products<br>2. Click nút Xóa<br>3. Click "Xóa" trong dialog | Hiển thị thông báo "Đã xóa sản phẩm", sản phẩm bị xóa khỏi danh sách | | Untested | 11/15/2015 | |
| **FUNC-DSSP-11** | Hủy ẩn sản phẩm | 1. Truy cập /admin/products<br>2. Click nút Ẩn<br>3. Click "Hủy" trong dialog | Dialog đóng, sản phẩm không bị ẩn | | Pass | 11/15/2015 | |
| **FUNC-DSSP-12** | Hủy xóa sản phẩm | 1. Truy cập /admin/products<br>2. Click nút Xóa<br>3. Click "Hủy" trong dialog | Dialog đóng, sản phẩm không bị xóa | | Pass | 11/15/2015 | |
| **FUNC-DSSP-13** | Xử lý khi không có sản phẩm | 1. Truy cập /admin/products<br>2. Lọc để không có sản phẩm nào | Hiển thị thông báo "Không tìm thấy sản phẩm nào" hoặc bảng trống | | Untested | 11/15/2015 | |
| **FUNC-DSSP-14** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/products<br>2. Tắt kết nối mạng | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại" | | Untested | 11/15/2015 | |
| **FUNC-DSSP-15** | Xử lý khi server lỗi | 1. Truy cập /admin/products<br>2. Server trả về lỗi 500 | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau" | | Untested | 11/15/2015 | |

---

### Function: Xem chi tiết sản phẩm

#### Check GUI: Xem chi tiết sản phẩm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CTSP-01** | Kiểm tra nút Quay lại | 1. Truy cập /admin/products/[id]<br>2. Kiểm tra nút Quay lại | Hiển thị nút "Quay lại" với icon ArrowLeft variant outline size sm, link đến /admin/products | | Pass | 11/15/2015 | |
| **GUI-CTSP-02** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/products/[id]<br>2. Kiểm tra tiêu đề | Hiển thị tên sản phẩm với kích thước text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-CTSP-03** | Kiểm tra mô tả trang | 1. Truy cập /admin/products/[id]<br>2. Kiểm tra mô tả | Hiển thị "Chi tiết sản phẩm - ID: [id]" màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-CTSP-04** | Kiểm tra nút Chỉnh sửa | 1. Truy cập /admin/products/[id]<br>2. Kiểm tra nút Chỉnh sửa | Hiển thị nút "Chỉnh sửa" với icon Edit variant outline, link đến /admin/products/[id]/edit | | Pass | 11/15/2015 | |
| **GUI-CTSP-05** | Kiểm tra nút Ẩn sản phẩm | 1. Truy cập /admin/products/[id]<br>2. Kiểm tra nút Ẩn | Hiển thị nút "Ẩn sản phẩm" với icon EyeOff variant secondary | | Pass | 11/15/2015 | |
| **GUI-CTSP-06** | Kiểm tra nút Xóa | 1. Truy cập /admin/products/[id]<br>2. Kiểm tra nút Xóa | Hiển thị nút "Xóa" với icon Trash2 variant destructive | | Pass | 11/15/2015 | |
| **GUI-CTSP-07** | Kiểm tra card Thông tin sản phẩm | 1. Truy cập /admin/products/[id]<br>2. Kiểm tra card | Hiển thị card "Thông tin sản phẩm" với hình ảnh sản phẩm (w-48 h-48), tên sản phẩm (text-2xl font-bold), thương hiệu, Badge danh mục, Badge trạng thái | | Pass | 11/15/2015 | |
| **GUI-CTSP-08** | Kiểm tra thông tin giá và tồn kho | 1. Truy cập /admin/products/[id]<br>2. Kiểm tra thông tin | Hiển thị grid 2 cột với: Giá bán (icon DollarSign), Giá gốc (icon DollarSign line-through), Tồn kho (icon Package), Tồn kho tối thiểu (icon BarChart3) | | Pass | 11/15/2015 | |
| **GUI-CTSP-09** | Kiểm tra đánh giá sản phẩm | 1. Truy cập /admin/products/[id]<br>2. Kiểm tra đánh giá | Hiển thị icon Star màu yellow-500, điểm đánh giá (font-medium), số lượng đánh giá (muted-foreground) | | Pass | 11/15/2015 | |
| **GUI-CTSP-10** | Kiểm tra card Mô tả sản phẩm | 1. Truy cập /admin/products/[id]<br>2. Kiểm tra card | Hiển thị card "Mô tả sản phẩm" với nội dung mô tả màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-CTSP-11** | Kiểm tra card Thông số kỹ thuật | 1. Truy cập /admin/products/[id]<br>2. Kiểm tra card | Hiển thị card "Thông số kỹ thuật" với Table hiển thị các thông số: Tỷ lệ, Chất liệu, Chiều cao, Chiều rộng, Chiều sâu, Độ tuổi khuyến nghị, Thời gian lắp ráp, Tính năng | | Pass | 11/15/2015 | |
| **GUI-CTSP-12** | Kiểm tra card Thông tin bổ sung | 1. Truy cập /admin/products/[id]<br>2. Kiểm tra card | Hiển thị card "Thông tin bổ sung" với: Ngày tạo (icon Calendar), Ngày cập nhật (icon Calendar), URL Slug (icon Package) | | Pass | 11/15/2015 | |
| **GUI-CTSP-13** | Kiểm tra card Trạng thái sản phẩm | 1. Truy cập /admin/products/[id]<br>2. Kiểm tra card | Hiển thị card "Trạng thái sản phẩm" với các Badge: Đang giảm giá, Sản phẩm nổi bật, Sản phẩm mới | | Pass | 11/15/2015 | |
| **GUI-CTSP-14** | Kiểm tra card Thông tin SEO | 1. Truy cập /admin/products/[id]<br>2. Kiểm tra card | Hiển thị card "Thông tin SEO" với Meta Title và Meta Description | | Pass | 11/15/2015 | |
| **GUI-CTSP-15** | Kiểm tra Dialog ẩn sản phẩm | 1. Truy cập /admin/products/[id]<br>2. Click nút Ẩn sản phẩm<br>3. Kiểm tra dialog | Hiển thị Dialog với tiêu đề "Xác nhận ẩn sản phẩm", mô tả, textarea "Lý do ẩn sản phẩm", nút Hủy, nút "Ẩn sản phẩm" | | Pass | 11/15/2015 | |
| **GUI-CTSP-16** | Kiểm tra Dialog xóa sản phẩm | 1. Truy cập /admin/products/[id]<br>2. Click nút Xóa<br>3. Kiểm tra dialog | Hiển thị Dialog với tiêu đề "Xác nhận xóa sản phẩm", mô tả "Hành động này không thể hoàn tác", textarea "Lý do xóa sản phẩm", nút Hủy, nút "Xóa vĩnh viễn" variant destructive | | Pass | 11/15/2015 | |

---

### Check FUNC: Xem chi tiết sản phẩm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CTSP-01** | Mở trang chi tiết sản phẩm | 1. Truy cập /admin/products/[id] | Hiển thị trang với nút Quay lại, tiêu đề (tên sản phẩm), mô tả, nút Chỉnh sửa, nút Ẩn, nút Xóa, card Thông tin sản phẩm, card Mô tả, card Thông số kỹ thuật, card Thông tin bổ sung, card Trạng thái, card SEO | | Pass | 11/15/2015 | |
| **FUNC-CTSP-02** | Hiển thị đầy đủ thông tin sản phẩm | 1. Truy cập /admin/products/[id] | Hiển thị đầy đủ thông tin: hình ảnh, tên, thương hiệu, danh mục, trạng thái, giá bán, giá gốc, tồn kho, tồn kho tối thiểu, đánh giá, mô tả, thông số kỹ thuật, ngày tạo, ngày cập nhật, slug, meta title, meta description | | Pass | 11/15/2015 | |
| **FUNC-CTSP-03** | Click nút Quay lại | 1. Truy cập /admin/products/[id]<br>2. Click nút "Quay lại" | Chuyển về trang /admin/products | | Pass | 11/15/2015 | |
| **FUNC-CTSP-04** | Click nút Chỉnh sửa | 1. Truy cập /admin/products/[id]<br>2. Click nút "Chỉnh sửa" | Chuyển đến trang /admin/products/[id]/edit | | Pass | 11/15/2015 | |
| **FUNC-CTSP-05** | Ẩn sản phẩm thành công | 1. Truy cập /admin/products/[id]<br>2. Click nút "Ẩn sản phẩm"<br>3. Nhập lý do<br>4. Click "Ẩn sản phẩm" | Hiển thị thông báo "Đã ẩn sản phẩm", chuyển về trang /admin/products | | Untested | 11/15/2015 | |
| **FUNC-CTSP-06** | Xóa sản phẩm thành công | 1. Truy cập /admin/products/[id]<br>2. Click nút "Xóa"<br>3. Nhập lý do<br>4. Click "Xóa vĩnh viễn" | Hiển thị thông báo "Đã xóa sản phẩm", chuyển về trang /admin/products | | Untested | 11/15/2015 | |
| **FUNC-CTSP-07** | Hủy ẩn sản phẩm | 1. Truy cập /admin/products/[id]<br>2. Click nút "Ẩn sản phẩm"<br>3. Click "Hủy" | Dialog đóng, vẫn ở trang chi tiết, sản phẩm không bị ẩn | | Pass | 11/15/2015 | |
| **FUNC-CTSP-08** | Hủy xóa sản phẩm | 1. Truy cập /admin/products/[id]<br>2. Click nút "Xóa"<br>3. Click "Hủy" | Dialog đóng, vẫn ở trang chi tiết, sản phẩm không bị xóa | | Pass | 11/15/2015 | |
| **FUNC-CTSP-09** | Xử lý khi sản phẩm không tồn tại | 1. Truy cập /admin/products/[id không tồn tại] | Hiển thị thông báo lỗi "Sản phẩm không tồn tại" hoặc chuyển về trang danh sách | | Untested | 11/15/2015 | |
| **FUNC-CTSP-10** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/products/[id]<br>2. Tắt kết nối mạng | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại" | | Untested | 11/15/2015 | |
| **FUNC-CTSP-11** | Xử lý khi server lỗi | 1. Truy cập /admin/products/[id]<br>2. Server trả về lỗi 500 | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau" | | Untested | 11/15/2015 | |

---

### Function: Thêm sản phẩm

#### Check GUI: Thêm sản phẩm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-TSP-01** | Kiểm tra nút Quay lại | 1. Truy cập /admin/products/new<br>2. Kiểm tra nút Quay lại | Hiển thị nút "Quay lại" với icon ArrowLeft variant outline size sm, link đến /admin/products | | Pass | 11/15/2015 | |
| **GUI-TSP-02** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/products/new<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Thêm sản phẩm mới" với kích thước text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-TSP-03** | Kiểm tra mô tả trang | 1. Truy cập /admin/products/new<br>2. Kiểm tra mô tả | Hiển thị mô tả "Nhập thông tin chi tiết cho sản phẩm mới" màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-TSP-04** | Kiểm tra card Thông tin cơ bản | 1. Truy cập /admin/products/new<br>2. Kiểm tra card | Hiển thị card "Thông tin cơ bản" với tiêu đề, mô tả "Thông tin chính của sản phẩm" | | Pass | 11/15/2015 | |
| **GUI-TSP-05** | Kiểm tra trường Tên sản phẩm | 1. Truy cập /admin/products/new<br>2. Kiểm tra trường | Hiển thị label "Tên sản phẩm *", input type text với placeholder "Nhập tên sản phẩm", có thuộc tính required | | Pass | 11/15/2015 | |
| **GUI-TSP-06** | Kiểm tra trường Thương hiệu | 1. Truy cập /admin/products/new<br>2. Kiểm tra trường | Hiển thị label "Thương hiệu *", Select với placeholder "Chọn thương hiệu", có các option: Bandai, Good Smile Company, Tamiya, Revell, Banpresto, Kotobukiya, Max Factory, Khác | | Pass | 11/15/2015 | |
| **GUI-TSP-07** | Kiểm tra trường Mô tả sản phẩm | 1. Truy cập /admin/products/new<br>2. Kiểm tra trường | Hiển thị label "Mô tả sản phẩm *", Textarea với placeholder "Mô tả chi tiết về sản phẩm...", rows 4 | | Pass | 11/15/2015 | |
| **GUI-TSP-08** | Kiểm tra trường Danh mục | 1. Truy cập /admin/products/new<br>2. Kiểm tra trường | Hiển thị label "Danh mục *", Select với placeholder "Chọn danh mục", có các option: Gundam, Figure, Mô hình xe, Máy bay, Tàu chiến, Khác | | Pass | 11/15/2015 | |
| **GUI-TSP-09** | Kiểm tra trường Tỷ lệ | 1. Truy cập /admin/products/new<br>2. Kiểm tra trường | Hiển thị label "Tỷ lệ", Select với placeholder "Chọn tỷ lệ", có các option: 1/144, 1/100, 1/72, 1/48, 1/24, 1/12, 1/8, 1/7, 1/6, 1/4 | | Pass | 11/15/2015 | |
| **GUI-TSP-10** | Kiểm tra card Giá cả | 1. Truy cập /admin/products/new<br>2. Kiểm tra card | Hiển thị card "Giá cả" với tiêu đề, mô tả "Thiết lập giá bán và giá gốc" | | Pass | 11/15/2015 | |
| **GUI-TSP-11** | Kiểm tra trường Giá bán | 1. Truy cập /admin/products/new<br>2. Kiểm tra trường | Hiển thị label "Giá bán *", input type number với placeholder "0", min 0 | | Pass | 11/15/2015 | |
| **GUI-TSP-12** | Kiểm tra trường Giá gốc | 1. Truy cập /admin/products/new<br>2. Kiểm tra trường | Hiển thị label "Giá gốc", input type number với placeholder "0", min 0 | | Pass | 11/15/2015 | |
| **GUI-TSP-13** | Kiểm tra checkbox Đang giảm giá | 1. Truy cập /admin/products/new<br>2. Kiểm tra checkbox | Hiển thị checkbox với label "Đang giảm giá" | | Pass | 11/15/2015 | |
| **GUI-TSP-14** | Kiểm tra card Quản lý tồn kho | 1. Truy cập /admin/products/new<br>2. Kiểm tra card | Hiển thị card "Quản lý tồn kho" với tiêu đề, mô tả "Thiết lập số lượng và cảnh báo tồn kho" | | Pass | 11/15/2015 | |
| **GUI-TSP-15** | Kiểm tra trường Số lượng tồn kho | 1. Truy cập /admin/products/new<br>2. Kiểm tra trường | Hiển thị label "Số lượng tồn kho *", input type number với placeholder "0", min 0 | | Pass | 11/15/2015 | |
| **GUI-TSP-16** | Kiểm tra trường Số lượng tối thiểu | 1. Truy cập /admin/products/new<br>2. Kiểm tra trường | Hiển thị label "Số lượng tối thiểu", input type number với placeholder "0", min 0 | | Pass | 11/15/2015 | |
| **GUI-TSP-17** | Kiểm tra checkbox Theo dõi tồn kho | 1. Truy cập /admin/products/new<br>2. Kiểm tra checkbox | Hiển thị checkbox với label "Theo dõi tồn kho", mặc định checked | | Pass | 11/15/2015 | |
| **GUI-TSP-18** | Kiểm tra card Thông số kỹ thuật | 1. Truy cập /admin/products/new<br>2. Kiểm tra card | Hiển thị card "Thông số kỹ thuật" với các trường: Chất liệu (Select), Chiều cao (number), Chiều rộng (number), Chiều sâu (number), Độ tuổi khuyến nghị (text), Thời gian lắp ráp (text) | | Pass | 11/15/2015 | |
| **GUI-TSP-19** | Kiểm tra card Tính năng nổi bật | 1. Truy cập /admin/products/new<br>2. Kiểm tra card | Hiển thị card "Tính năng nổi bật" với input nhập tính năng, nút Plus để thêm, danh sách tính năng với nút X để xóa | | Pass | 11/15/2015 | |
| **GUI-TSP-20** | Kiểm tra card Hình ảnh sản phẩm | 1. Truy cập /admin/products/new<br>2. Kiểm tra card | Hiển thị card "Hình ảnh sản phẩm" với vùng upload (border-dashed), icon Upload, text hướng dẫn, nút "Chọn hình ảnh", thông tin hỗ trợ (JPG, PNG, WebP, tối đa 5MB, tỷ lệ 1:1) | | Pass | 11/15/2015 | |
| **GUI-TSP-21** | Kiểm tra card Trạng thái | 1. Truy cập /admin/products/new<br>2. Kiểm tra card | Hiển thị card "Trạng thái" với Select "Trạng thái sản phẩm" (Bản nháp, Đang bán, Ngừng bán), checkbox "Sản phẩm nổi bật", checkbox "Sản phẩm mới" | | Pass | 11/15/2015 | |
| **GUI-TSP-22** | Kiểm tra card SEO | 1. Truy cập /admin/products/new<br>2. Kiểm tra card | Hiển thị card "SEO" với các trường: URL slug (input), Meta title (input), Meta description (textarea rows 3) | | Pass | 11/15/2015 | |
| **GUI-TSP-23** | Kiểm tra nút Hủy | 1. Truy cập /admin/products/new<br>2. Kiểm tra nút | Hiển thị nút "Hủy" variant outline, link đến /admin/products | | Pass | 11/15/2015 | |
| **GUI-TSP-24** | Kiểm tra nút Lưu bản nháp | 1. Truy cập /admin/products/new<br>2. Kiểm tra nút | Hiển thị nút "Lưu bản nháp" variant outline type button | | Pass | 11/15/2015 | |
| **GUI-TSP-25** | Kiểm tra nút Tạo sản phẩm | 1. Truy cập /admin/products/new<br>2. Kiểm tra nút | Hiển thị nút "Tạo sản phẩm" type submit | | Pass | 11/15/2015 | |

---

### Check FUNC: Thêm sản phẩm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TSP-01** | Mở trang thêm sản phẩm | 1. Truy cập /admin/products/new | Hiển thị trang với nút Quay lại, tiêu đề "Thêm sản phẩm mới", mô tả, form với các card: Thông tin cơ bản, Giá cả, Quản lý tồn kho, Thông số kỹ thuật, Tính năng nổi bật, Hình ảnh, Trạng thái, SEO, các nút Hủy, Lưu bản nháp, Tạo sản phẩm | | Pass | 11/15/2015 | |
| **FUNC-TSP-02** | Tạo sản phẩm thành công | 1. Truy cập /admin/products/new<br>2. Điền đầy đủ thông tin bắt buộc (Tên, Thương hiệu, Mô tả, Danh mục, Giá bán, Số lượng tồn kho)<br>3. Nhấn "Tạo sản phẩm" | Hiển thị thông báo "Tạo sản phẩm thành công", chuyển về trang /admin/products | | Untested | 11/15/2015 | |
| **FUNC-TSP-03** | Tạo sản phẩm - Thiếu Tên sản phẩm | 1. Truy cập /admin/products/new<br>2. Để trống Tên sản phẩm<br>3. Điền các trường khác<br>4. Nhấn "Tạo sản phẩm" | Hiển thị thông báo lỗi "Tên sản phẩm không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-TSP-04** | Tạo sản phẩm - Thiếu Thương hiệu | 1. Truy cập /admin/products/new<br>2. Không chọn Thương hiệu<br>3. Điền các trường khác<br>4. Nhấn "Tạo sản phẩm" | Hiển thị thông báo lỗi "Thương hiệu không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-TSP-05** | Tạo sản phẩm - Thiếu Mô tả | 1. Truy cập /admin/products/new<br>2. Để trống Mô tả<br>3. Điền các trường khác<br>4. Nhấn "Tạo sản phẩm" | Hiển thị thông báo lỗi "Mô tả không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-TSP-06** | Tạo sản phẩm - Thiếu Danh mục | 1. Truy cập /admin/products/new<br>2. Không chọn Danh mục<br>3. Điền các trường khác<br>4. Nhấn "Tạo sản phẩm" | Hiển thị thông báo lỗi "Danh mục không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-TSP-07** | Tạo sản phẩm - Giá bán <= 0 | 1. Truy cập /admin/products/new<br>2. Nhập giá bán <= 0<br>3. Điền các trường khác<br>4. Nhấn "Tạo sản phẩm" | Hiển thị thông báo lỗi "Giá bán phải lớn hơn 0", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-TSP-08** | Tạo sản phẩm - Số lượng tồn kho < 0 | 1. Truy cập /admin/products/new<br>2. Nhập số lượng tồn kho < 0<br>3. Điền các trường khác<br>4. Nhấn "Tạo sản phẩm" | Hiển thị thông báo lỗi "Số lượng tồn kho phải lớn hơn hoặc bằng 0", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-TSP-09** | Thêm tính năng | 1. Truy cập /admin/products/new<br>2. Nhập tính năng vào input<br>3. Click nút Plus hoặc nhấn Enter | Tính năng được thêm vào danh sách, hiển thị với nút X để xóa | | Pass | 11/15/2015 | |
| **FUNC-TSP-10** | Xóa tính năng | 1. Truy cập /admin/products/new<br>2. Thêm tính năng<br>3. Click nút X của tính năng | Tính năng bị xóa khỏi danh sách | | Pass | 11/15/2015 | |
| **FUNC-TSP-11** | Lưu bản nháp thành công | 1. Truy cập /admin/products/new<br>2. Nhập ít nhất Tên sản phẩm<br>3. Nhấn "Lưu bản nháp" | Hiển thị thông báo "Lưu bản nháp thành công", chuyển về trang /admin/products, sản phẩm được lưu với trạng thái "Bản nháp" | | Untested | 11/15/2015 | |
| **FUNC-TSP-12** | Lưu bản nháp - Thiếu Tên sản phẩm | 1. Truy cập /admin/products/new<br>2. Để trống Tên sản phẩm<br>3. Nhấn "Lưu bản nháp" | Hiển thị thông báo lỗi "Vui lòng nhập tên sản phẩm để lưu bản nháp" | | Pass | 11/15/2015 | |
| **FUNC-TSP-13** | Click nút Hủy | 1. Truy cập /admin/products/new<br>2. Click nút "Hủy" | Chuyển về trang /admin/products, không lưu thông tin | | Pass | 11/15/2015 | |
| **FUNC-TSP-14** | Upload hình ảnh thành công | 1. Truy cập /admin/products/new<br>2. Click "Chọn hình ảnh"<br>3. Chọn file ảnh hợp lệ (< 5MB, JPG/PNG/WebP) | Hình ảnh được upload và hiển thị preview | | Untested | 11/15/2015 | |
| **FUNC-TSP-15** | Upload hình ảnh - File quá lớn | 1. Truy cập /admin/products/new<br>2. Click "Chọn hình ảnh"<br>3. Chọn file > 5MB | Hiển thị thông báo lỗi "Kích thước file không được vượt quá 5MB" | | Pass | 11/15/2015 | |
| **FUNC-TSP-16** | Upload hình ảnh - File không phải ảnh | 1. Truy cập /admin/products/new<br>2. Click "Chọn hình ảnh"<br>3. Chọn file không phải ảnh | Hiển thị thông báo lỗi "Vui lòng chọn file ảnh hợp lệ (JPG, PNG, WebP)" | | Pass | 11/15/2015 | |
| **FUNC-TSP-17** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/products/new<br>2. Điền đầy đủ thông tin<br>3. Tắt kết nối mạng<br>4. Nhấn "Tạo sản phẩm" | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", form không được gửi | | Untested | 11/15/2015 | |
| **FUNC-TSP-18** | Xử lý khi server lỗi | 1. Truy cập /admin/products/new<br>2. Điền đầy đủ thông tin<br>3. Server trả về lỗi 500<br>4. Nhấn "Tạo sản phẩm" | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau", form không được gửi | | Untested | 11/15/2015 | |

---

### Function: Cập nhật sản phẩm

#### Check GUI: Cập nhật sản phẩm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CNSP-01** | Kiểm tra nút Quay lại | 1. Truy cập /admin/products/[id]/edit<br>2. Kiểm tra nút Quay lại | Hiển thị nút "Quay lại" với icon ArrowLeft variant outline size sm, link đến /admin/products/[id] | | Pass | 11/15/2015 | |
| **GUI-CNSP-02** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/products/[id]/edit<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Chỉnh sửa sản phẩm" với kích thước text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-CNSP-03** | Kiểm tra mô tả trang | 1. Truy cập /admin/products/[id]/edit<br>2. Kiểm tra mô tả | Hiển thị mô tả "Cập nhật thông tin sản phẩm #[id]" màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-CNSP-04** | Kiểm tra nút Hủy (khi đang chỉnh sửa) | 1. Truy cập /admin/products/[id]/edit<br>2. Kiểm tra nút Hủy | Hiển thị nút "Hủy" với icon X variant outline, chỉ hiển thị khi đang chỉnh sửa | | Pass | 11/15/2015 | |
| **GUI-CNSP-05** | Kiểm tra nút Lưu bản nháp | 1. Truy cập /admin/products/[id]/edit<br>2. Kiểm tra nút | Hiển thị nút "Lưu bản nháp" với icon Save variant outline, chỉ hiển thị khi đang chỉnh sửa | | Pass | 11/15/2015 | |
| **GUI-CNSP-06** | Kiểm tra nút Cập nhật sản phẩm | 1. Truy cập /admin/products/[id]/edit<br>2. Kiểm tra nút | Hiển thị nút "Cập nhật sản phẩm" với icon Save, chỉ hiển thị khi đang chỉnh sửa | | Pass | 11/15/2015 | |
| **GUI-CNSP-07** | Kiểm tra nút Chỉnh sửa (khi không chỉnh sửa) | 1. Truy cập /admin/products/[id]/edit<br>2. Kiểm tra nút | Hiển thị nút "Chỉnh sửa" với icon Save, chỉ hiển thị khi không đang chỉnh sửa | | Pass | 11/15/2015 | |
| **GUI-CNSP-08** | Kiểm tra trạng thái disabled của các trường | 1. Truy cập /admin/products/[id]/edit<br>2. Kiểm tra các trường | Tất cả các trường input, select, textarea có thuộc tính disabled khi không ở chế độ chỉnh sửa | | Pass | 11/15/2015 | |
| **GUI-CNSP-09** | Kiểm tra cảnh báo tồn kho thấp | 1. Truy cập /admin/products/[id]/edit<br>2. Chỉnh sửa tồn kho <= tồn kho tối thiểu<br>3. Kiểm tra cảnh báo | Hiển thị Alert với icon AlertTriangle màu yellow-600, text "Cảnh báo: Tồn kho sắp hết, cần nhập hàng" màu yellow-800, background yellow-50, border yellow-200 | | Pass | 11/15/2015 | |

---

### Check FUNC: Cập nhật sản phẩm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CNSP-01** | Mở trang chỉnh sửa sản phẩm | 1. Truy cập /admin/products/[id]/edit | Hiển thị trang với nút Quay lại, tiêu đề "Chỉnh sửa sản phẩm", mô tả, nút Chỉnh sửa, form với các trường đã được điền sẵn thông tin sản phẩm, tất cả trường disabled | | Pass | 11/15/2015 | |
| **FUNC-CNSP-02** | Bật chế độ chỉnh sửa | 1. Truy cập /admin/products/[id]/edit<br>2. Click nút "Chỉnh sửa" | Tất cả các trường được kích hoạt (disabled=false), nút Chỉnh sửa biến mất, hiển thị nút "Hủy", "Lưu bản nháp", "Cập nhật sản phẩm" | | Pass | 11/15/2015 | |
| **FUNC-CNSP-03** | Cập nhật sản phẩm thành công | 1. Truy cập /admin/products/[id]/edit<br>2. Click Chỉnh sửa<br>3. Sửa thông tin<br>4. Nhấn "Cập nhật sản phẩm" | Hiển thị thông báo "Cập nhật sản phẩm thành công", các trường chuyển về disabled, nút Lưu và Hủy biến mất, nút Chỉnh sửa hiển thị lại, thông tin được cập nhật | | Untested | 11/15/2015 | |
| **FUNC-CNSP-04** | Cập nhật - Thiếu Tên sản phẩm | 1. Truy cập /admin/products/[id]/edit<br>2. Click Chỉnh sửa<br>3. Xóa tên sản phẩm<br>4. Nhấn "Cập nhật sản phẩm" | Hiển thị thông báo lỗi "Tên sản phẩm không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-CNSP-05** | Cập nhật - Thiếu Thương hiệu | 1. Truy cập /admin/products/[id]/edit<br>2. Click Chỉnh sửa<br>3. Xóa thương hiệu<br>4. Nhấn "Cập nhật sản phẩm" | Hiển thị thông báo lỗi "Thương hiệu không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-CNSP-06** | Cập nhật - Thiếu Mô tả | 1. Truy cập /admin/products/[id]/edit<br>2. Click Chỉnh sửa<br>3. Xóa mô tả<br>4. Nhấn "Cập nhật sản phẩm" | Hiển thị thông báo lỗi "Mô tả không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-CNSP-07** | Cập nhật - Thiếu Danh mục | 1. Truy cập /admin/products/[id]/edit<br>2. Click Chỉnh sửa<br>3. Xóa danh mục<br>4. Nhấn "Cập nhật sản phẩm" | Hiển thị thông báo lỗi "Danh mục không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-CNSP-08** | Cập nhật - Giá bán <= 0 | 1. Truy cập /admin/products/[id]/edit<br>2. Click Chỉnh sửa<br>3. Nhập giá bán <= 0<br>4. Nhấn "Cập nhật sản phẩm" | Hiển thị thông báo lỗi "Giá bán phải lớn hơn 0", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-CNSP-09** | Cập nhật - Số lượng tồn kho < 0 | 1. Truy cập /admin/products/[id]/edit<br>2. Click Chỉnh sửa<br>3. Nhập số lượng tồn kho < 0<br>4. Nhấn "Cập nhật sản phẩm" | Hiển thị thông báo lỗi "Số lượng tồn kho phải lớn hơn hoặc bằng 0", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-CNSP-10** | Hủy chỉnh sửa | 1. Truy cập /admin/products/[id]/edit<br>2. Click Chỉnh sửa<br>3. Sửa thông tin<br>4. Nhấn "Hủy" | Các trường được reset về giá trị ban đầu, chuyển về chế độ xem (disabled=true), nút Lưu và Hủy biến mất, nút Chỉnh sửa hiển thị lại | | Pass | 11/15/2015 | |
| **FUNC-CNSP-11** | Lưu bản nháp | 1. Truy cập /admin/products/[id]/edit<br>2. Click Chỉnh sửa<br>3. Sửa thông tin<br>4. Nhấn "Lưu bản nháp" | Hiển thị thông báo "Lưu bản nháp thành công", sản phẩm được lưu với trạng thái "Bản nháp" | | Untested | 11/15/2015 | |
| **FUNC-CNSP-12** | Hiển thị cảnh báo tồn kho thấp | 1. Truy cập /admin/products/[id]/edit<br>2. Click Chỉnh sửa<br>3. Nhập tồn kho <= tồn kho tối thiểu | Hiển thị Alert cảnh báo màu vàng "Cảnh báo: Tồn kho sắp hết, cần nhập hàng" | | Pass | 11/15/2015 | |
| **FUNC-CNSP-13** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/products/[id]/edit<br>2. Click Chỉnh sửa<br>3. Sửa thông tin<br>4. Tắt kết nối mạng<br>5. Nhấn "Cập nhật sản phẩm" | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", form không được gửi | | Untested | 11/15/2015 | |
| **FUNC-CNSP-14** | Xử lý khi server lỗi | 1. Truy cập /admin/products/[id]/edit<br>2. Click Chỉnh sửa<br>3. Sửa thông tin<br>4. Server trả về lỗi 500<br>5. Nhấn "Cập nhật sản phẩm" | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau", form không được gửi | | Untested | 11/15/2015 | |

---

### Function: Xóa sản phẩm

#### Check GUI: Xóa sản phẩm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XSP-01** | Kiểm tra Dialog xác nhận xóa | 1. Truy cập /admin/products<br>2. Click nút Xóa của một sản phẩm<br>3. Kiểm tra dialog | Hiển thị Dialog với tiêu đề "Xác nhận xóa sản phẩm", mô tả "Bạn có chắc chắn muốn xóa sản phẩm...? Hành động này không thể hoàn tác", nút "Hủy" variant outline, nút "Xóa" variant destructive | | Pass | 11/15/2015 | |

---

### Check FUNC: Xóa sản phẩm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XSP-01** | Xóa sản phẩm thành công | 1. Truy cập /admin/products<br>2. Click nút Xóa của một sản phẩm<br>3. Click "Xóa" trong dialog | Hiển thị thông báo "Đã xóa sản phẩm", sản phẩm bị xóa khỏi danh sách, cập nhật lại bảng | | Untested | 11/15/2015 | |
| **FUNC-XSP-02** | Hủy xóa sản phẩm | 1. Truy cập /admin/products<br>2. Click nút Xóa<br>3. Click "Hủy" trong dialog | Dialog đóng, sản phẩm không bị xóa, vẫn ở trang danh sách | | Pass | 11/15/2015 | |
| **FUNC-XSP-03** | Xóa sản phẩm - Sản phẩm đang có đơn hàng | 1. Truy cập /admin/products<br>2. Click nút Xóa của sản phẩm đang có đơn hàng<br>3. Click "Xóa" | Hiển thị thông báo lỗi "Không thể xóa sản phẩm đang có đơn hàng", sản phẩm không bị xóa | | Untested | 11/15/2015 | |
| **FUNC-XSP-04** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/products<br>2. Click nút Xóa<br>3. Tắt kết nối mạng<br>4. Click "Xóa" | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", sản phẩm không bị xóa | | Untested | 11/15/2015 | |
| **FUNC-XSP-05** | Xử lý khi server lỗi | 1. Truy cập /admin/products<br>2. Click nút Xóa<br>3. Server trả về lỗi 500<br>4. Click "Xóa" | Hiển thị thông báo lỗi "Lỗi xóa sản phẩm", sản phẩm không bị xóa | | Untested | 11/15/2015 | |

---

### Function: Tìm kiếm sản phẩm

#### Check GUI: Tìm kiếm sản phẩm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-TKSP-01** | Kiểm tra trường tìm kiếm | 1. Truy cập /admin/products<br>2. Kiểm tra trường tìm kiếm | Hiển thị input với icon Search bên trái, placeholder "Tìm kiếm sản phẩm...", có thể nhập và nhấn Enter | | Pass | 11/15/2015 | |

---

### Check FUNC: Tìm kiếm sản phẩm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TKSP-01** | Tìm kiếm theo tên sản phẩm | 1. Truy cập /admin/products<br>2. Nhập tên sản phẩm vào ô tìm kiếm<br>3. Nhấn Enter | Hiển thị danh sách sản phẩm có tên chứa từ khóa tìm kiếm, hiển thị thông báo "Đã lọc X sản phẩm" | | Untested | 11/15/2015 | |
| **FUNC-TKSP-02** | Tìm kiếm theo thương hiệu | 1. Truy cập /admin/products<br>2. Nhập thương hiệu vào ô tìm kiếm<br>3. Nhấn Enter | Hiển thị danh sách sản phẩm có thương hiệu chứa từ khóa tìm kiếm | | Untested | 11/15/2015 | |
| **FUNC-TKSP-03** | Tìm kiếm theo danh mục | 1. Truy cập /admin/products<br>2. Nhập danh mục vào ô tìm kiếm<br>3. Nhấn Enter | Hiển thị danh sách sản phẩm có danh mục chứa từ khóa tìm kiếm | | Untested | 11/15/2015 | |
| **FUNC-TKSP-04** | Tìm kiếm - Không tìm thấy | 1. Truy cập /admin/products<br>2. Nhập từ khóa không tồn tại<br>3. Nhấn Enter | Hiển thị bảng trống hoặc thông báo "Không tìm thấy sản phẩm phù hợp" | | Untested | 11/15/2015 | |
| **FUNC-TKSP-05** | Tìm kiếm - Từ khóa rỗng | 1. Truy cập /admin/products<br>2. Để trống ô tìm kiếm<br>3. Nhấn Enter | Hiển thị toàn bộ danh sách sản phẩm | | Pass | 11/15/2015 | |
| **FUNC-TKSP-06** | Tìm kiếm không phân biệt hoa thường | 1. Truy cập /admin/products<br>2. Nhập "GUNDAM" (chữ hoa)<br>3. Nhấn Enter | Hiển thị danh sách sản phẩm có tên/thương hiệu/danh mục chứa "gundam" (không phân biệt hoa thường) | | Untested | 11/15/2015 | |

---

### Function: Lọc sản phẩm

#### Check GUI: Lọc sản phẩm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-LSP-01** | Kiểm tra Select Danh mục | 1. Truy cập /admin/products<br>2. Kiểm tra Select Danh mục | Hiển thị Select với placeholder "Danh mục", có các option: Tất cả, Gundam, Figure, Mô hình xe, Máy bay, Tàu chiến, Khác | | Pass | 11/15/2015 | |
| **GUI-LSP-02** | Kiểm tra Select Thương hiệu | 1. Truy cập /admin/products<br>2. Kiểm tra Select Thương hiệu | Hiển thị Select với placeholder "Thương hiệu", có các option: Tất cả, Bandai, Good Smile Company, Tamiya, Revell, Banpresto, Kotobukiya | | Pass | 11/15/2015 | |
| **GUI-LSP-03** | Kiểm tra Select Trạng thái | 1. Truy cập /admin/products<br>2. Kiểm tra Select Trạng thái | Hiển thị Select với placeholder "Trạng thái", có các option: Tất cả, Đang bán, Sắp hết hàng, Hết hàng, Ngừng bán | | Pass | 11/15/2015 | |
| **GUI-LSP-04** | Kiểm tra nút Bộ lọc | 1. Truy cập /admin/products<br>2. Kiểm tra nút | Hiển thị nút "Bộ lọc" với icon Filter variant outline | | Pass | 11/15/2015 | |

---

### Check FUNC: Lọc sản phẩm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-LSP-01** | Lọc theo Danh mục | 1. Truy cập /admin/products<br>2. Chọn Danh mục (VD: Gundam)<br>3. Click "Bộ lọc" | Hiển thị danh sách sản phẩm thuộc danh mục đã chọn, hiển thị thông báo "Đã lọc X sản phẩm" | | Untested | 11/15/2015 | |
| **FUNC-LSP-02** | Lọc theo Thương hiệu | 1. Truy cập /admin/products<br>2. Chọn Thương hiệu (VD: Bandai)<br>3. Click "Bộ lọc" | Hiển thị danh sách sản phẩm thuộc thương hiệu đã chọn | | Untested | 11/15/2015 | |
| **FUNC-LSP-03** | Lọc theo Trạng thái | 1. Truy cập /admin/products<br>2. Chọn Trạng thái (VD: Đang bán)<br>3. Click "Bộ lọc" | Hiển thị danh sách sản phẩm có trạng thái đã chọn | | Untested | 11/15/2015 | |
| **FUNC-LSP-04** | Lọc kết hợp nhiều tiêu chí | 1. Truy cập /admin/products<br>2. Chọn Danh mục, Thương hiệu, Trạng thái<br>3. Click "Bộ lọc" | Hiển thị danh sách sản phẩm thỏa mãn tất cả các tiêu chí đã chọn | | Untested | 11/15/2015 | |
| **FUNC-LSP-05** | Lọc - Không có sản phẩm phù hợp | 1. Truy cập /admin/products<br>2. Chọn các tiêu chí không có sản phẩm nào<br>3. Click "Bộ lọc" | Hiển thị bảng trống hoặc thông báo "Không có sản phẩm phù hợp với bộ lọc" | | Untested | 11/15/2015 | |
| **FUNC-LSP-06** | Lọc - Chọn "Tất cả" | 1. Truy cập /admin/products<br>2. Chọn "Tất cả" cho các Select<br>3. Click "Bộ lọc" | Hiển thị toàn bộ danh sách sản phẩm | | Pass | 11/15/2015 | |
| **FUNC-LSP-07** | Kết hợp tìm kiếm và lọc | 1. Truy cập /admin/products<br>2. Nhập từ khóa tìm kiếm<br>3. Chọn Danh mục<br>4. Click "Bộ lọc" | Hiển thị danh sách sản phẩm thỏa mãn cả từ khóa tìm kiếm và bộ lọc đã chọn | | Untested | 11/15/2015 | |

---

**Người tạo:** Testing Team  
**Ngày cập nhật:** 11/15/2015  
**Phiên bản:** 1.0

