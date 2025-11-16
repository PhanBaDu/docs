# Test Case Template - Quản lý tồn kho (Admin)

## Module Code
**Model Management Store: Quản lý tồn kho Admin**

## Test Requirement
1. Hiển thị danh sách tồn kho
2. Xem chi tiết tồn kho
3. Cập nhật tồn kho
4. Nhập hàng mới
5. Cảnh báo tồn kho thấp
6. Kiểm kê tồn kho
7. Nhập kho

---

## Test Summary

### Người thực hiện Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 71 |
| **Fail** | 0 |
| **Untested** | 72 |
| **N/A** | 0 |
| **Number of Test cases** | 143 |

---

## Test Cases

### Function: Hiển thị danh sách tồn kho

#### Check GUI: Hiển thị danh sách tồn kho

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DSTK-01** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/inventory<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Quản lý tồn kho" với kích thước text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-DSTK-02** | Kiểm tra mô tả chức năng | 1. Truy cập /admin/inventory<br>2. Kiểm tra mô tả | Hiển thị mô tả "Theo dõi và quản lý tồn kho sản phẩm" màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-DSTK-03** | Kiểm tra nút Nhập hàng | 1. Truy cập /admin/inventory<br>2. Kiểm tra nút Nhập hàng | Hiển thị nút "Nhập hàng" với icon Upload variant outline ở header | | Pass | 11/15/2015 | |
| **GUI-DSTK-04** | Kiểm tra nút Kiểm kê | 1. Truy cập /admin/inventory<br>2. Kiểm tra nút Kiểm kê | Hiển thị nút "Kiểm kê" với icon ClipboardList variant outline ở header | | Pass | 11/15/2015 | |
| **GUI-DSTK-05** | Kiểm tra nút Thêm sản phẩm | 1. Truy cập /admin/inventory<br>2. Kiểm tra nút Thêm sản phẩm | Hiển thị nút "Thêm sản phẩm" với icon Plus ở header, link đến /admin/inventory/new | | Pass | 11/15/2015 | |
| **GUI-DSTK-06** | Kiểm tra Stats Cards | 1. Truy cập /admin/inventory<br>2. Kiểm tra Stats Cards | Hiển thị 4 card thống kê: Tổng sản phẩm (156), Đủ hàng (142), Sắp hết (8), Hết hàng (6) | | Pass | 11/15/2015 | |
| **GUI-DSTK-07** | Kiểm tra trường Tìm kiếm | 1. Truy cập /admin/inventory<br>2. Kiểm tra trường tìm kiếm | Hiển thị input với icon Search bên trái, placeholder "Tìm kiếm sản phẩm...", có thể nhập và nhấn Enter để tìm | | Pass | 11/15/2015 | |
| **GUI-DSTK-08** | Kiểm tra Select Danh mục | 1. Truy cập /admin/inventory<br>2. Kiểm tra Select Danh mục | Hiển thị Select với placeholder "Danh mục", width w-40, có các option: Tất cả, Gundam, Figure, Mô hình xe, Máy bay, Tàu chiến, Khác | | Pass | 11/15/2015 | |
| **GUI-DSTK-09** | Kiểm tra Select Trạng thái tồn kho | 1. Truy cập /admin/inventory<br>2. Kiểm tra Select Trạng thái | Hiển thị Select với placeholder "Trạng thái", width w-40, có các option: Tất cả, Đủ hàng, Sắp hết, Nguy hiểm, Hết hàng | | Pass | 11/15/2015 | |
| **GUI-DSTK-10** | Kiểm tra nút Bộ lọc | 1. Truy cập /admin/inventory<br>2. Kiểm tra nút Bộ lọc | Hiển thị nút "Bộ lọc" với icon Filter variant outline | | Pass | 11/15/2015 | |
| **GUI-DSTK-11** | Kiểm tra bảng danh sách tồn kho | 1. Truy cập /admin/inventory<br>2. Kiểm tra bảng | Hiển thị Table với các cột: Mã SP, Tên SP, Danh mục, Tồn kho hiện tại, Ngưỡng cảnh báo, Trạng thái, Thao tác | | Pass | 11/15/2015 | |
| **GUI-DSTK-12** | Kiểm tra cột Mã SP trong bảng | 1. Truy cập /admin/inventory<br>2. Kiểm tra cột Mã SP | Mỗi dòng hiển thị mã sản phẩm (VD: SP001) với font-medium | | Pass | 11/15/2015 | |
| **GUI-DSTK-13** | Kiểm tra cột Tên SP trong bảng | 1. Truy cập /admin/inventory<br>2. Kiểm tra cột Tên SP | Mỗi dòng hiển thị hình ảnh sản phẩm (w-12 h-12 rounded-lg), tên sản phẩm (font-medium), thương hiệu (text-sm muted-foreground) | | Pass | 11/15/2015 | |
| **GUI-DSTK-14** | Kiểm tra cột Danh mục trong bảng | 1. Truy cập /admin/inventory<br>2. Kiểm tra cột Danh mục | Hiển thị Badge variant outline với tên danh mục | | Pass | 11/15/2015 | |
| **GUI-DSTK-15** | Kiểm tra cột Tồn kho hiện tại trong bảng | 1. Truy cập /admin/inventory<br>2. Kiểm tra cột Tồn kho | Hiển thị số lượng tồn kho (font-medium) và Progress bar hiển thị tỷ lệ tồn kho so với maxStock | | Pass | 11/15/2015 | |
| **GUI-DSTK-16** | Kiểm tra cột Ngưỡng cảnh báo trong bảng | 1. Truy cập /admin/inventory<br>2. Kiểm tra cột Ngưỡng cảnh báo | Hiển thị số lượng ngưỡng cảnh báo (text-sm) | | Pass | 11/15/2015 | |
| **GUI-DSTK-17** | Kiểm tra cột Trạng thái trong bảng | 1. Truy cập /admin/inventory<br>2. Kiểm tra cột Trạng thái | Hiển thị Badge với icon và màu tương ứng: Đủ hàng (CheckCircle màu xanh, default), Sắp hết (AlertTriangle màu vàng, secondary), Nguy hiểm (AlertTriangle màu cam, destructive), Hết hàng (AlertTriangle màu đỏ, destructive) | | Pass | 11/15/2015 | |
| **GUI-DSTK-18** | Kiểm tra cột Thao tác trong bảng | 1. Truy cập /admin/inventory<br>2. Kiểm tra cột Thao tác | Hiển thị 3 nút: Xem (icon Edit link đến /admin/inventory/[id]), Chỉnh sửa (icon Edit link đến /admin/inventory/[id]/edit), Nhập hàng (icon Upload), tất cả variant ghost size sm | | Pass | 11/15/2015 | |
| **GUI-DSTK-19** | Kiểm tra Pagination | 1. Truy cập /admin/inventory<br>2. Kiểm tra Pagination | Hiển thị text "Hiển thị 1-X trong Y sản phẩm", các nút phân trang: Trước (disabled), số trang, Sau | | Pass | 11/15/2015 | |

---

### Check FUNC: Hiển thị danh sách tồn kho

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DSTK-01** | Mở trang danh sách tồn kho | 1. Truy cập /admin/inventory | Hiển thị trang với tiêu đề, mô tả, nút Nhập hàng, nút Kiểm kê, nút Thêm sản phẩm, 4 Stats Cards, bộ lọc (tìm kiếm, danh mục, trạng thái, nút Bộ lọc), bảng danh sách tồn kho, pagination | | Pass | 11/15/2015 | |
| **FUNC-DSTK-02** | Hiển thị danh sách tồn kho mặc định | 1. Truy cập /admin/inventory | Hiển thị tất cả sản phẩm trong bảng, mỗi sản phẩm có đầy đủ thông tin: mã SP, hình ảnh, tên, thương hiệu, danh mục, tồn kho hiện tại (kèm progress bar), ngưỡng cảnh báo, trạng thái (kèm icon và màu), các nút thao tác | | Pass | 11/15/2015 | |
| **FUNC-DSTK-03** | Click nút Nhập hàng | 1. Truy cập /admin/inventory<br>2. Click nút "Nhập hàng" | Mở modal nhập hàng hoặc chuyển đến trang nhập hàng | | Untested | 11/15/2015 | |
| **FUNC-DSTK-04** | Click nút Kiểm kê | 1. Truy cập /admin/inventory<br>2. Click nút "Kiểm kê" | Mở modal kiểm kê tồn kho | | Untested | 11/15/2015 | |
| **FUNC-DSTK-05** | Click nút Thêm sản phẩm | 1. Truy cập /admin/inventory<br>2. Click nút "Thêm sản phẩm" | Chuyển đến trang /admin/inventory/new | | Pass | 11/15/2015 | |
| **FUNC-DSTK-06** | Click nút Xem (icon Edit đầu tiên) | 1. Truy cập /admin/inventory<br>2. Click nút Xem của một sản phẩm | Chuyển đến trang chi tiết tồn kho /admin/inventory/[id] | | Pass | 11/15/2015 | |
| **FUNC-DSTK-07** | Click nút Chỉnh sửa (icon Edit thứ hai) | 1. Truy cập /admin/inventory<br>2. Click nút Chỉnh sửa của một sản phẩm | Chuyển đến trang chỉnh sửa tồn kho /admin/inventory/[id]/edit | | Pass | 11/15/2015 | |
| **FUNC-DSTK-08** | Click nút Nhập hàng (icon Upload) | 1. Truy cập /admin/inventory<br>2. Click nút Nhập hàng của một sản phẩm | Mở modal nhập hàng với sản phẩm đã chọn | | Untested | 11/15/2015 | |
| **FUNC-DSTK-09** | Xử lý khi không có sản phẩm | 1. Truy cập /admin/inventory<br>2. Lọc để không có sản phẩm nào | Hiển thị thông báo "Không tìm thấy sản phẩm nào" hoặc bảng trống | | Untested | 11/15/2015 | |
| **FUNC-DSTK-10** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/inventory<br>2. Tắt kết nối mạng | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại" | | Untested | 11/15/2015 | |
| **FUNC-DSTK-11** | Xử lý khi server lỗi | 1. Truy cập /admin/inventory<br>2. Server trả về lỗi 500 | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau" | | Untested | 11/15/2015 | |

---

### Function: Xem chi tiết tồn kho

#### Check GUI: Xem chi tiết tồn kho

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CTTK-01** | Kiểm tra nút Quay lại | 1. Truy cập /admin/inventory/[id]<br>2. Kiểm tra nút Quay lại | Hiển thị nút "Quay lại" với icon ArrowLeft variant outline size sm, link đến /admin/inventory | | Pass | 11/15/2015 | |
| **GUI-CTTK-02** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/inventory/[id]<br>2. Kiểm tra tiêu đề | Hiển thị tên sản phẩm với kích thước text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-CTTK-03** | Kiểm tra mô tả trang | 1. Truy cập /admin/inventory/[id]<br>2. Kiểm tra mô tả | Hiển thị "Chi tiết tồn kho - Mã: [productCode]" màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-CTTK-04** | Kiểm tra nút Chỉnh sửa | 1. Truy cập /admin/inventory/[id]<br>2. Kiểm tra nút Chỉnh sửa | Hiển thị nút "Chỉnh sửa" với icon Edit variant outline, link đến /admin/inventory/[id]/edit | | Pass | 11/15/2015 | |
| **GUI-CTTK-05** | Kiểm tra nút Nhập hàng | 1. Truy cập /admin/inventory/[id]<br>2. Kiểm tra nút Nhập hàng | Hiển thị nút "Nhập hàng" với icon Upload variant secondary | | Pass | 11/15/2015 | |
| **GUI-CTTK-06** | Kiểm tra nút Xóa | 1. Truy cập /admin/inventory/[id]<br>2. Kiểm tra nút Xóa | Hiển thị nút "Xóa" với icon Trash2 variant destructive | | Pass | 11/15/2015 | |
| **GUI-CTTK-07** | Kiểm tra card Thông tin sản phẩm | 1. Truy cập /admin/inventory/[id]<br>2. Kiểm tra card | Hiển thị card "Thông tin sản phẩm" với hình ảnh sản phẩm (w-48 h-48), tên sản phẩm (text-2xl font-bold), thương hiệu, Badge danh mục, Badge trạng thái | | Pass | 11/15/2015 | |
| **GUI-CTTK-08** | Kiểm tra thông tin tồn kho | 1. Truy cập /admin/inventory/[id]<br>2. Kiểm tra thông tin | Hiển thị grid với: Tồn kho hiện tại (icon Package), Ngưỡng cảnh báo (icon AlertTriangle), Tồn kho tối đa (icon BarChart3), Trạng thái (icon CheckCircle/AlertTriangle) | | Pass | 11/15/2015 | |
| **GUI-CTTK-09** | Kiểm tra thông tin giá | 1. Truy cập /admin/inventory/[id]<br>2. Kiểm tra thông tin | Hiển thị: Giá nhập (icon DollarSign), Giá bán (icon DollarSign) | | Pass | 11/15/2015 | |
| **GUI-CTTK-10** | Kiểm tra card Lịch sử nhập hàng | 1. Truy cập /admin/inventory/[id]<br>2. Kiểm tra card | Hiển thị card "Lịch sử nhập hàng" với Table hiển thị các cột: Ngày nhập, Số lượng, Giá nhập, Nhà cung cấp, Ghi chú | | Pass | 11/15/2015 | |
| **GUI-CTTK-11** | Kiểm tra card Lịch sử xuất hàng | 1. Truy cập /admin/inventory/[id]<br>2. Kiểm tra card | Hiển thị card "Lịch sử xuất hàng" với Table hiển thị các cột: Ngày xuất, Số lượng, Lý do, Người thực hiện | | Pass | 11/15/2015 | |
| **GUI-CTTK-12** | Kiểm tra card Thông tin bổ sung | 1. Truy cập /admin/inventory/[id]<br>2. Kiểm tra card | Hiển thị card "Thông tin bổ sung" với: Nhà cung cấp (icon User), Ngày tạo (icon Calendar), Ngày cập nhật (icon Calendar), Ghi chú (icon FileText) | | Pass | 11/15/2015 | |
| **GUI-CTTK-13** | Kiểm tra Dialog xóa sản phẩm | 1. Truy cập /admin/inventory/[id]<br>2. Click nút Xóa<br>3. Kiểm tra dialog | Hiển thị Dialog với tiêu đề "Xác nhận xóa sản phẩm", mô tả "Hành động này không thể hoàn tác", textarea "Lý do xóa sản phẩm", nút Hủy, nút "Xóa vĩnh viễn" variant destructive | | Pass | 11/15/2015 | |

---

### Check FUNC: Xem chi tiết tồn kho

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CTTK-01** | Mở trang chi tiết tồn kho | 1. Truy cập /admin/inventory/[id] | Hiển thị trang với nút Quay lại, tiêu đề (tên sản phẩm), mô tả, nút Chỉnh sửa, nút Nhập hàng, nút Xóa, card Thông tin sản phẩm, card Thông tin tồn kho, card Lịch sử nhập hàng, card Lịch sử xuất hàng, card Thông tin bổ sung | | Pass | 11/15/2015 | |
| **FUNC-CTTK-02** | Hiển thị đầy đủ thông tin tồn kho | 1. Truy cập /admin/inventory/[id] | Hiển thị đầy đủ thông tin: hình ảnh, tên, thương hiệu, danh mục, trạng thái, tồn kho hiện tại, ngưỡng cảnh báo, tồn kho tối đa, giá nhập, giá bán, nhà cung cấp, ngày tạo, ngày cập nhật, ghi chú, lịch sử nhập hàng, lịch sử xuất hàng | | Pass | 11/15/2015 | |
| **FUNC-CTTK-03** | Click nút Quay lại | 1. Truy cập /admin/inventory/[id]<br>2. Click nút "Quay lại" | Chuyển về trang /admin/inventory | | Pass | 11/15/2015 | |
| **FUNC-CTTK-04** | Click nút Chỉnh sửa | 1. Truy cập /admin/inventory/[id]<br>2. Click nút "Chỉnh sửa" | Chuyển đến trang /admin/inventory/[id]/edit | | Pass | 11/15/2015 | |
| **FUNC-CTTK-05** | Click nút Nhập hàng | 1. Truy cập /admin/inventory/[id]<br>2. Click nút "Nhập hàng" | Mở modal nhập hàng với sản phẩm đã chọn | | Untested | 11/15/2015 | |
| **FUNC-CTTK-06** | Xóa sản phẩm thành công | 1. Truy cập /admin/inventory/[id]<br>2. Click nút "Xóa"<br>3. Nhập lý do<br>4. Click "Xóa vĩnh viễn" | Hiển thị thông báo "Đã xóa sản phẩm", chuyển về trang /admin/inventory | | Untested | 11/15/2015 | |
| **FUNC-CTTK-07** | Hủy xóa sản phẩm | 1. Truy cập /admin/inventory/[id]<br>2. Click nút "Xóa"<br>3. Click "Hủy" | Dialog đóng, vẫn ở trang chi tiết, sản phẩm không bị xóa | | Pass | 11/15/2015 | |
| **FUNC-CTTK-08** | Xử lý khi sản phẩm không tồn tại | 1. Truy cập /admin/inventory/[id không tồn tại] | Hiển thị thông báo lỗi "Sản phẩm không tồn tại" hoặc chuyển về trang danh sách | | Untested | 11/15/2015 | |
| **FUNC-CTTK-09** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/inventory/[id]<br>2. Tắt kết nối mạng | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại" | | Untested | 11/15/2015 | |
| **FUNC-CTTK-10** | Xử lý khi server lỗi | 1. Truy cập /admin/inventory/[id]<br>2. Server trả về lỗi 500 | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau" | | Untested | 11/15/2015 | |

---

### Function: Cập nhật tồn kho

#### Check GUI: Cập nhật tồn kho

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CNTK-01** | Kiểm tra nút Quay lại | 1. Truy cập /admin/inventory/[id]/edit<br>2. Kiểm tra nút Quay lại | Hiển thị nút "Quay lại" với icon ArrowLeft variant outline size sm, link đến /admin/inventory/[id] | | Pass | 11/15/2015 | |
| **GUI-CNTK-02** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/inventory/[id]/edit<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Chỉnh sửa tồn kho" với kích thước text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-CNTK-03** | Kiểm tra mô tả trang | 1. Truy cập /admin/inventory/[id]/edit<br>2. Kiểm tra mô tả | Hiển thị mô tả "Cập nhật thông tin tồn kho sản phẩm #[id]" màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-CNTK-04** | Kiểm tra card Thông tin cơ bản | 1. Truy cập /admin/inventory/[id]/edit<br>2. Kiểm tra card | Hiển thị card "Thông tin cơ bản" với các trường: Tên sản phẩm (input), Mã sản phẩm (input readonly), Danh mục (Select), Thương hiệu (Select), Mô tả (Textarea) | | Pass | 11/15/2015 | |
| **GUI-CNTK-05** | Kiểm tra card Quản lý tồn kho | 1. Truy cập /admin/inventory/[id]/edit<br>2. Kiểm tra card | Hiển thị card "Quản lý tồn kho" với các trường: Số lượng hiện tại (number input), Ngưỡng cảnh báo (number input) | | Pass | 11/15/2015 | |
| **GUI-CNTK-06** | Kiểm tra card Thông tin nhập hàng | 1. Truy cập /admin/inventory/[id]/edit<br>2. Kiểm tra card | Hiển thị card "Thông tin nhập hàng" với các trường: Giá nhập (number input), Nhà cung cấp (input), Ghi chú (Textarea) | | Pass | 11/15/2015 | |
| **GUI-CNTK-07** | Kiểm tra nút Hủy | 1. Truy cập /admin/inventory/[id]/edit<br>2. Kiểm tra nút | Hiển thị nút "Hủy" variant outline, link đến /admin/inventory/[id] | | Pass | 11/15/2015 | |
| **GUI-CNTK-08** | Kiểm tra nút Lưu thay đổi | 1. Truy cập /admin/inventory/[id]/edit<br>2. Kiểm tra nút | Hiển thị nút "Lưu thay đổi" với icon Save type submit | | Pass | 11/15/2015 | |
| **GUI-CNTK-09** | Kiểm tra cảnh báo tồn kho thấp | 1. Truy cập /admin/inventory/[id]/edit<br>2. Nhập tồn kho <= ngưỡng cảnh báo<br>3. Kiểm tra cảnh báo | Hiển thị Alert với icon AlertTriangle màu yellow-600, text "Cảnh báo: Tồn kho sắp hết, cần nhập hàng" màu yellow-800, background yellow-50, border yellow-200 | | Pass | 11/15/2015 | |

---

### Check FUNC: Cập nhật tồn kho

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CNTK-01** | Mở trang chỉnh sửa tồn kho | 1. Truy cập /admin/inventory/[id]/edit | Hiển thị trang với nút Quay lại, tiêu đề "Chỉnh sửa tồn kho", mô tả, form với các card: Thông tin cơ bản, Quản lý tồn kho, Thông tin nhập hàng, các trường đã được điền sẵn thông tin sản phẩm, nút Hủy, nút Lưu thay đổi | | Pass | 11/15/2015 | |
| **FUNC-CNTK-02** | Cập nhật tồn kho thành công | 1. Truy cập /admin/inventory/[id]/edit<br>2. Sửa thông tin (Tên, Danh mục, Thương hiệu, Số lượng, Ngưỡng cảnh báo, Giá nhập, Nhà cung cấp, Ghi chú)<br>3. Nhấn "Lưu thay đổi" | Hiển thị thông báo "Cập nhật tồn kho thành công", chuyển về trang /admin/inventory/[id], thông tin được cập nhật | | Untested | 11/15/2015 | |
| **FUNC-CNTK-03** | Cập nhật - Thiếu Tên sản phẩm | 1. Truy cập /admin/inventory/[id]/edit<br>2. Xóa tên sản phẩm<br>3. Nhấn "Lưu thay đổi" | Hiển thị thông báo lỗi "Tên sản phẩm không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-CNTK-04** | Cập nhật - Thiếu Danh mục | 1. Truy cập /admin/inventory/[id]/edit<br>2. Xóa danh mục<br>3. Nhấn "Lưu thay đổi" | Hiển thị thông báo lỗi "Danh mục không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-CNTK-05** | Cập nhật - Thiếu Thương hiệu | 1. Truy cập /admin/inventory/[id]/edit<br>2. Xóa thương hiệu<br>3. Nhấn "Lưu thay đổi" | Hiển thị thông báo lỗi "Thương hiệu không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-CNTK-06** | Cập nhật - Số lượng hiện tại < 0 | 1. Truy cập /admin/inventory/[id]/edit<br>2. Nhập số lượng hiện tại < 0<br>3. Nhấn "Lưu thay đổi" | Hiển thị thông báo lỗi "Số lượng hiện tại phải lớn hơn hoặc bằng 0", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-CNTK-07** | Cập nhật - Ngưỡng cảnh báo < 0 | 1. Truy cập /admin/inventory/[id]/edit<br>2. Nhập ngưỡng cảnh báo < 0<br>3. Nhấn "Lưu thay đổi" | Hiển thị thông báo lỗi "Ngưỡng cảnh báo phải lớn hơn hoặc bằng 0", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-CNTK-08** | Hiển thị cảnh báo tồn kho thấp | 1. Truy cập /admin/inventory/[id]/edit<br>2. Nhập tồn kho <= ngưỡng cảnh báo | Hiển thị Alert cảnh báo màu vàng "Cảnh báo: Tồn kho sắp hết, cần nhập hàng" | | Pass | 11/15/2015 | |
| **FUNC-CNTK-09** | Click nút Hủy | 1. Truy cập /admin/inventory/[id]/edit<br>2. Click nút "Hủy" | Chuyển về trang /admin/inventory/[id], không lưu thông tin | | Pass | 11/15/2015 | |
| **FUNC-CNTK-10** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/inventory/[id]/edit<br>2. Sửa thông tin<br>3. Tắt kết nối mạng<br>4. Nhấn "Lưu thay đổi" | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", form không được gửi | | Untested | 11/15/2015 | |
| **FUNC-CNTK-11** | Xử lý khi server lỗi | 1. Truy cập /admin/inventory/[id]/edit<br>2. Sửa thông tin<br>3. Server trả về lỗi 500<br>4. Nhấn "Lưu thay đổi" | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau", form không được gửi | | Untested | 11/15/2015 | |

---

### Function: Nhập hàng mới

#### Check GUI: Nhập hàng mới

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-NHM-01** | Kiểm tra nút Quay lại | 1. Truy cập /admin/inventory/new<br>2. Kiểm tra nút Quay lại | Hiển thị nút "Quay lại" với icon ArrowLeft variant outline size sm, link đến /admin/inventory | | Pass | 11/15/2015 | |
| **GUI-NHM-02** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/inventory/new<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Thêm sản phẩm mới" với kích thước text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-NHM-03** | Kiểm tra mô tả trang | 1. Truy cập /admin/inventory/new<br>2. Kiểm tra mô tả | Hiển thị mô tả "Nhập thông tin sản phẩm mới vào kho" màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-NHM-04** | Kiểm tra card Thông tin cơ bản | 1. Truy cập /admin/inventory/new<br>2. Kiểm tra card | Hiển thị card "Thông tin cơ bản" với các trường: Tên sản phẩm * (input), Mã sản phẩm * (input), Danh mục * (Select), Thương hiệu * (Select), Mô tả (Textarea) | | Pass | 11/15/2015 | |
| **GUI-NHM-05** | Kiểm tra card Quản lý tồn kho | 1. Truy cập /admin/inventory/new<br>2. Kiểm tra card | Hiển thị card "Quản lý tồn kho" với các trường: Số lượng ban đầu * (number input), Ngưỡng cảnh báo * (number input) | | Pass | 11/15/2015 | |
| **GUI-NHM-06** | Kiểm tra card Thông tin nhập hàng | 1. Truy cập /admin/inventory/new<br>2. Kiểm tra card | Hiển thị card "Thông tin nhập hàng" với các trường: Giá nhập (number input), Nhà cung cấp (input), Ghi chú (Textarea) | | Pass | 11/15/2015 | |
| **GUI-NHM-07** | Kiểm tra nút Hủy | 1. Truy cập /admin/inventory/new<br>2. Kiểm tra nút | Hiển thị nút "Hủy" variant outline, link đến /admin/inventory | | Pass | 11/15/2015 | |
| **GUI-NHM-08** | Kiểm tra nút Lưu bản nháp | 1. Truy cập /admin/inventory/new<br>2. Kiểm tra nút | Hiển thị nút "Lưu bản nháp" với icon FileText variant outline type button | | Pass | 11/15/2015 | |
| **GUI-NHM-09** | Kiểm tra nút Tạo sản phẩm | 1. Truy cập /admin/inventory/new<br>2. Kiểm tra nút | Hiển thị nút "Tạo sản phẩm" với icon Save type submit | | Pass | 11/15/2015 | |

---

### Check FUNC: Nhập hàng mới

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-NHM-01** | Mở trang thêm sản phẩm mới | 1. Truy cập /admin/inventory/new | Hiển thị trang với nút Quay lại, tiêu đề "Thêm sản phẩm mới", mô tả, form với các card: Thông tin cơ bản, Quản lý tồn kho, Thông tin nhập hàng, các nút Hủy, Lưu bản nháp, Tạo sản phẩm | | Pass | 11/15/2015 | |
| **FUNC-NHM-02** | Tạo sản phẩm thành công | 1. Truy cập /admin/inventory/new<br>2. Điền đầy đủ thông tin bắt buộc (Tên, Mã SP, Danh mục, Thương hiệu, Số lượng ban đầu, Ngưỡng cảnh báo)<br>3. Nhấn "Tạo sản phẩm" | Hiển thị thông báo "Thêm sản phẩm thành công", chuyển về trang /admin/inventory | | Untested | 11/15/2015 | |
| **FUNC-NHM-03** | Tạo sản phẩm - Thiếu Tên sản phẩm | 1. Truy cập /admin/inventory/new<br>2. Để trống Tên sản phẩm<br>3. Điền các trường khác<br>4. Nhấn "Tạo sản phẩm" | Hiển thị thông báo lỗi "Tên sản phẩm không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-NHM-04** | Tạo sản phẩm - Thiếu Mã sản phẩm | 1. Truy cập /admin/inventory/new<br>2. Để trống Mã sản phẩm<br>3. Điền các trường khác<br>4. Nhấn "Tạo sản phẩm" | Hiển thị thông báo lỗi "Mã sản phẩm không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-NHM-05** | Tạo sản phẩm - Thiếu Danh mục | 1. Truy cập /admin/inventory/new<br>2. Không chọn Danh mục<br>3. Điền các trường khác<br>4. Nhấn "Tạo sản phẩm" | Hiển thị thông báo lỗi "Danh mục không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-NHM-06** | Tạo sản phẩm - Thiếu Thương hiệu | 1. Truy cập /admin/inventory/new<br>2. Không chọn Thương hiệu<br>3. Điền các trường khác<br>4. Nhấn "Tạo sản phẩm" | Hiển thị thông báo lỗi "Thương hiệu không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-NHM-07** | Tạo sản phẩm - Số lượng ban đầu < 0 | 1. Truy cập /admin/inventory/new<br>2. Nhập số lượng ban đầu < 0<br>3. Điền các trường khác<br>4. Nhấn "Tạo sản phẩm" | Hiển thị thông báo lỗi "Số lượng ban đầu phải lớn hơn hoặc bằng 0", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-NHM-08** | Tạo sản phẩm - Ngưỡng cảnh báo < 0 | 1. Truy cập /admin/inventory/new<br>2. Nhập ngưỡng cảnh báo < 0<br>3. Điền các trường khác<br>4. Nhấn "Tạo sản phẩm" | Hiển thị thông báo lỗi "Ngưỡng cảnh báo phải lớn hơn hoặc bằng 0", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-NHM-09** | Lưu bản nháp thành công | 1. Truy cập /admin/inventory/new<br>2. Nhập ít nhất Tên sản phẩm và Mã sản phẩm<br>3. Nhấn "Lưu bản nháp" | Hiển thị thông báo "Lưu bản nháp thành công", chuyển về trang /admin/inventory, sản phẩm được lưu với trạng thái "Bản nháp" | | Untested | 11/15/2015 | |
| **FUNC-NHM-10** | Lưu bản nháp - Thiếu Tên sản phẩm | 1. Truy cập /admin/inventory/new<br>2. Để trống Tên sản phẩm<br>3. Nhấn "Lưu bản nháp" | Hiển thị thông báo lỗi "Vui lòng nhập tên sản phẩm để lưu bản nháp" | | Pass | 11/15/2015 | |
| **FUNC-NHM-11** | Click nút Hủy | 1. Truy cập /admin/inventory/new<br>2. Click nút "Hủy" | Chuyển về trang /admin/inventory, không lưu thông tin | | Pass | 11/15/2015 | |
| **FUNC-NHM-12** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/inventory/new<br>2. Điền đầy đủ thông tin<br>3. Tắt kết nối mạng<br>4. Nhấn "Tạo sản phẩm" | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", form không được gửi | | Untested | 11/15/2015 | |
| **FUNC-NHM-13** | Xử lý khi server lỗi | 1. Truy cập /admin/inventory/new<br>2. Điền đầy đủ thông tin<br>3. Server trả về lỗi 500<br>4. Nhấn "Tạo sản phẩm" | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau", form không được gửi | | Untested | 11/15/2015 | |

---

### Function: Cảnh báo tồn kho thấp

#### Check GUI: Cảnh báo tồn kho thấp

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CBTK-01** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/inventory/alerts<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Cảnh báo tồn kho" với kích thước text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-CBTK-02** | Kiểm tra mô tả chức năng | 1. Truy cập /admin/inventory/alerts<br>2. Kiểm tra mô tả | Hiển thị mô tả "Danh sách sản phẩm có tồn kho thấp cần nhập hàng" màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-CBTK-03** | Kiểm tra bộ lọc | 1. Truy cập /admin/inventory/alerts<br>2. Kiểm tra bộ lọc | Hiển thị Select với các option: Tất cả, Sắp hết, Nguy hiểm, Hết hàng | | Pass | 11/15/2015 | |
| **GUI-CBTK-04** | Kiểm tra bảng cảnh báo | 1. Truy cập /admin/inventory/alerts<br>2. Kiểm tra bảng | Hiển thị Table với các cột: Mã SP, Tên SP, Tồn kho hiện tại, Ngưỡng cảnh báo, Trạng thái, Thao tác | | Pass | 11/15/2015 | |
| **GUI-CBTK-05** | Kiểm tra Badge trạng thái cảnh báo | 1. Truy cập /admin/inventory/alerts<br>2. Kiểm tra Badge | Hiển thị Badge với màu tương ứng: Sắp hết (secondary màu vàng), Nguy hiểm (destructive màu cam), Hết hàng (destructive màu đỏ) | | Pass | 11/15/2015 | |

---

### Check FUNC: Cảnh báo tồn kho thấp

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CBTK-01** | Mở trang cảnh báo tồn kho | 1. Truy cập /admin/inventory/alerts | Hiển thị trang với tiêu đề, mô tả, bộ lọc, bảng danh sách sản phẩm có tồn kho thấp | | Pass | 11/15/2015 | |
| **FUNC-CBTK-02** | Hiển thị danh sách cảnh báo | 1. Truy cập /admin/inventory/alerts | Hiển thị danh sách sản phẩm có tồn kho <= ngưỡng cảnh báo, mỗi sản phẩm hiển thị đầy đủ thông tin và trạng thái cảnh báo | | Pass | 11/15/2015 | |
| **FUNC-CBTK-03** | Lọc theo trạng thái cảnh báo | 1. Truy cập /admin/inventory/alerts<br>2. Chọn trạng thái cảnh báo (VD: Sắp hết)<br>3. Click "Bộ lọc" | Hiển thị danh sách sản phẩm có trạng thái cảnh báo đã chọn | | Untested | 11/15/2015 | |
| **FUNC-CBTK-04** | Click nút Nhập hàng từ cảnh báo | 1. Truy cập /admin/inventory/alerts<br>2. Click nút Nhập hàng của một sản phẩm | Mở modal nhập hàng với sản phẩm đã chọn | | Untested | 11/15/2015 | |
| **FUNC-CBTK-05** | Xử lý khi không có cảnh báo | 1. Truy cập /admin/inventory/alerts<br>2. Lọc để không có sản phẩm nào | Hiển thị thông báo "Không có sản phẩm nào cần cảnh báo" hoặc bảng trống | | Untested | 11/15/2015 | |
| **FUNC-CBTK-06** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/inventory/alerts<br>2. Tắt kết nối mạng | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại" | | Untested | 11/15/2015 | |
| **FUNC-CBTK-07** | Xử lý khi server lỗi | 1. Truy cập /admin/inventory/alerts<br>2. Server trả về lỗi 500 | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau" | | Untested | 11/15/2015 | |

---

### Function: Kiểm kê tồn kho

#### Check GUI: Kiểm kê tồn kho

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-KKTK-01** | Kiểm tra modal Kiểm kê | 1. Truy cập /admin/inventory<br>2. Click nút "Kiểm kê"<br>3. Kiểm tra modal | Hiển thị Dialog với tiêu đề "Kiểm kê tồn kho", mô tả "Đối chiếu tồn kho thực tế với hệ thống" | | Pass | 11/15/2015 | |
| **GUI-KKTK-02** | Kiểm tra bảng kiểm kê | 1. Truy cập /admin/inventory<br>2. Click nút "Kiểm kê"<br>3. Kiểm tra bảng | Hiển thị Table với các cột: Mã SP, Tên SP, Tồn kho hệ thống, Số lượng thực tế, Chênh lệch, Trạng thái | | Pass | 11/15/2015 | |
| **GUI-KKTK-03** | Kiểm tra trường Số lượng thực tế | 1. Truy cập /admin/inventory<br>2. Click nút "Kiểm kê"<br>3. Kiểm tra trường | Hiển thị input number cho mỗi sản phẩm để nhập số lượng thực tế | | Pass | 11/15/2015 | |
| **GUI-KKTK-04** | Kiểm tra Badge trạng thái kiểm kê | 1. Truy cập /admin/inventory<br>2. Click nút "Kiểm kê"<br>3. Kiểm tra Badge | Hiển thị Badge với màu: Khớp (default màu xanh), Chênh lệch (destructive màu đỏ) | | Pass | 11/15/2015 | |
| **GUI-KKTK-05** | Kiểm tra nút Lưu kiểm kê | 1. Truy cập /admin/inventory<br>2. Click nút "Kiểm kê"<br>3. Kiểm tra nút | Hiển thị nút "Lưu kiểm kê" variant outline | | Pass | 11/15/2015 | |
| **GUI-KKTK-06** | Kiểm tra nút Đối chiếu & Cập nhật | 1. Truy cập /admin/inventory<br>2. Click nút "Kiểm kê"<br>3. Kiểm tra nút | Hiển thị nút "Đối chiếu & Cập nhật" type submit | | Pass | 11/15/2015 | |
| **GUI-KKTK-07** | Kiểm tra nút Xuất báo cáo | 1. Truy cập /admin/inventory<br>2. Click nút "Kiểm kê"<br>3. Kiểm tra nút | Hiển thị nút "Xuất báo cáo" variant outline | | Pass | 11/15/2015 | |

---

### Check FUNC: Kiểm kê tồn kho

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-KKTK-01** | Mở modal kiểm kê | 1. Truy cập /admin/inventory<br>2. Click nút "Kiểm kê" | Hiển thị Dialog với tiêu đề "Kiểm kê tồn kho", mô tả, bảng danh sách sản phẩm với các trường để nhập số lượng thực tế, các nút Lưu kiểm kê, Đối chiếu & Cập nhật, Xuất báo cáo | | Pass | 11/15/2015 | |
| **FUNC-KKTK-02** | Nhập số lượng thực tế | 1. Truy cập /admin/inventory<br>2. Click nút "Kiểm kê"<br>3. Nhập số lượng thực tế cho các sản phẩm | Số lượng thực tế được nhập vào input, hệ thống tự động tính chênh lệch và hiển thị trạng thái (Khớp/Chênh lệch) | | Pass | 11/15/2015 | |
| **FUNC-KKTK-03** | Lưu kiểm kê thành công | 1. Truy cập /admin/inventory<br>2. Click nút "Kiểm kê"<br>3. Nhập số lượng thực tế<br>4. Click "Lưu kiểm kê" | Hiển thị thông báo "Lưu kiểm kê thành công", dữ liệu kiểm kê được lưu tạm thời | | Untested | 11/15/2015 | |
| **FUNC-KKTK-04** | Đối chiếu & Cập nhật thành công | 1. Truy cập /admin/inventory<br>2. Click nút "Kiểm kê"<br>3. Nhập số lượng thực tế<br>4. Click "Đối chiếu & Cập nhật" | Hiển thị thông báo "Cập nhật tồn kho thành công", tồn kho hệ thống được cập nhật theo số lượng thực tế, modal đóng | | Untested | 11/15/2015 | |
| **FUNC-KKTK-05** | Xuất báo cáo kiểm kê | 1. Truy cập /admin/inventory<br>2. Click nút "Kiểm kê"<br>3. Nhập số lượng thực tế<br>4. Click "Xuất báo cáo" | Tải về file Excel/PDF báo cáo kiểm kê với đầy đủ thông tin: Mã SP, Tên SP, Tồn kho hệ thống, Số lượng thực tế, Chênh lệch, Trạng thái | | Untested | 11/15/2015 | |
| **FUNC-KKTK-06** | Hiển thị chênh lệch tự động | 1. Truy cập /admin/inventory<br>2. Click nút "Kiểm kê"<br>3. Nhập số lượng thực tế khác với tồn kho hệ thống | Hiển thị chênh lệch (số lượng thực tế - tồn kho hệ thống), Badge trạng thái chuyển thành "Chênh lệch" màu đỏ | | Pass | 11/15/2015 | |
| **FUNC-KKTK-07** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/inventory<br>2. Click nút "Kiểm kê"<br>3. Nhập số lượng thực tế<br>4. Tắt kết nối mạng<br>5. Click "Đối chiếu & Cập nhật" | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", không cập nhật tồn kho | | Untested | 11/15/2015 | |
| **FUNC-KKTK-08** | Xử lý khi server lỗi | 1. Truy cập /admin/inventory<br>2. Click nút "Kiểm kê"<br>3. Nhập số lượng thực tế<br>4. Server trả về lỗi 500<br>5. Click "Đối chiếu & Cập nhật" | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau", không cập nhật tồn kho | | Untested | 11/15/2015 | |

---

### Function: Nhập kho

#### Check GUI: Nhập kho

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-NK-01** | Kiểm tra modal Nhập hàng | 1. Truy cập /admin/inventory<br>2. Click nút "Nhập hàng" hoặc icon Upload<br>3. Kiểm tra modal | Hiển thị Dialog với tiêu đề "Nhập hàng", mô tả "Ghi nhận việc nhập sản phẩm mới vào kho" | | Pass | 11/15/2015 | |
| **GUI-NK-02** | Kiểm tra trường Sản phẩm | 1. Truy cập /admin/inventory<br>2. Click nút "Nhập hàng"<br>3. Kiểm tra trường | Hiển thị Select/Dropdown với placeholder "Chọn sản phẩm" hoặc input tìm kiếm sản phẩm, nếu click từ sản phẩm cụ thể thì sản phẩm đã được chọn sẵn | | Pass | 11/15/2015 | |
| **GUI-NK-03** | Kiểm tra trường Số lượng nhập | 1. Truy cập /admin/inventory<br>2. Click nút "Nhập hàng"<br>3. Kiểm tra trường | Hiển thị label "Số lượng nhập *", input type number với placeholder "0", min 0, có thuộc tính required | | Pass | 11/15/2015 | |
| **GUI-NK-04** | Kiểm tra trường Giá nhập | 1. Truy cập /admin/inventory<br>2. Click nút "Nhập hàng"<br>3. Kiểm tra trường | Hiển thị label "Giá nhập", input type number với placeholder "0", min 0 | | Pass | 11/15/2015 | |
| **GUI-NK-05** | Kiểm tra trường Nhà cung cấp | 1. Truy cập /admin/inventory<br>2. Click nút "Nhập hàng"<br>3. Kiểm tra trường | Hiển thị label "Nhà cung cấp", Select/Dropdown với placeholder "Chọn nhà cung cấp" hoặc input text | | Pass | 11/15/2015 | |
| **GUI-NK-06** | Kiểm tra trường Ngày nhập | 1. Truy cập /admin/inventory<br>2. Click nút "Nhập hàng"<br>3. Kiểm tra trường | Hiển thị label "Ngày nhập", DatePicker với giá trị mặc định là ngày hiện tại | | Pass | 11/15/2015 | |
| **GUI-NK-07** | Kiểm tra trường Ghi chú | 1. Truy cập /admin/inventory<br>2. Click nút "Nhập hàng"<br>3. Kiểm tra trường | Hiển thị label "Ghi chú", Textarea với placeholder "Ghi chú thêm về lô hàng nhập (tùy chọn)" | | Pass | 11/15/2015 | |
| **GUI-NK-08** | Kiểm tra nút Hủy | 1. Truy cập /admin/inventory<br>2. Click nút "Nhập hàng"<br>3. Kiểm tra nút | Hiển thị nút "Hủy" variant outline | | Pass | 11/15/2015 | |
| **GUI-NK-09** | Kiểm tra nút Lưu | 1. Truy cập /admin/inventory<br>2. Click nút "Nhập hàng"<br>3. Kiểm tra nút | Hiển thị nút "Lưu" type submit | | Pass | 11/15/2015 | |

---

### Check FUNC: Nhập kho

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-NK-01** | Mở modal nhập hàng | 1. Truy cập /admin/inventory<br>2. Click nút "Nhập hàng" | Hiển thị Dialog với tiêu đề "Nhập hàng", mô tả, các trường: Sản phẩm, Số lượng nhập, Giá nhập, Nhà cung cấp, Ngày nhập, Ghi chú, nút Hủy, nút Lưu | | Pass | 11/15/2015 | |
| **FUNC-NK-02** | Mở modal nhập hàng từ sản phẩm cụ thể | 1. Truy cập /admin/inventory<br>2. Click icon Upload của một sản phẩm | Hiển thị Dialog với sản phẩm đã được chọn sẵn trong trường Sản phẩm | | Pass | 11/15/2015 | |
| **FUNC-NK-03** | Nhập hàng thành công | 1. Truy cập /admin/inventory<br>2. Click nút "Nhập hàng"<br>3. Chọn sản phẩm<br>4. Nhập số lượng nhập > 0<br>5. Nhập giá nhập (tùy chọn)<br>6. Chọn nhà cung cấp (tùy chọn)<br>7. Chọn ngày nhập<br>8. Nhập ghi chú (tùy chọn)<br>9. Click "Lưu" | Hiển thị thông báo "Nhập hàng thành công", tồn kho sản phẩm được cập nhật (tăng thêm số lượng nhập), lịch sử nhập hàng được ghi nhận, modal đóng | | Untested | 11/15/2015 | |
| **FUNC-NK-04** | Nhập hàng - Thiếu Sản phẩm | 1. Truy cập /admin/inventory<br>2. Click nút "Nhập hàng"<br>3. Không chọn sản phẩm<br>4. Nhập số lượng<br>5. Click "Lưu" | Hiển thị thông báo lỗi "Vui lòng chọn sản phẩm", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-NK-05** | Nhập hàng - Thiếu Số lượng nhập | 1. Truy cập /admin/inventory<br>2. Click nút "Nhập hàng"<br>3. Chọn sản phẩm<br>4. Để trống số lượng nhập<br>5. Click "Lưu" | Hiển thị thông báo lỗi "Số lượng nhập không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-NK-06** | Nhập hàng - Số lượng nhập <= 0 | 1. Truy cập /admin/inventory<br>2. Click nút "Nhập hàng"<br>3. Chọn sản phẩm<br>4. Nhập số lượng <= 0<br>5. Click "Lưu" | Hiển thị thông báo lỗi "Số lượng nhập phải lớn hơn 0", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-NK-07** | Nhập hàng - Giá nhập < 0 | 1. Truy cập /admin/inventory<br>2. Click nút "Nhập hàng"<br>3. Chọn sản phẩm<br>4. Nhập giá nhập < 0<br>5. Click "Lưu" | Hiển thị thông báo lỗi "Giá nhập phải lớn hơn hoặc bằng 0", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-NK-08** | Click nút Hủy | 1. Truy cập /admin/inventory<br>2. Click nút "Nhập hàng"<br>3. Click "Hủy" | Modal đóng, không lưu thông tin | | Pass | 11/15/2015 | |
| **FUNC-NK-09** | Cập nhật tồn kho sau nhập hàng | 1. Truy cập /admin/inventory<br>2. Click nút "Nhập hàng"<br>3. Chọn sản phẩm có tồn kho = 10<br>4. Nhập số lượng = 5<br>5. Click "Lưu"<br>6. Kiểm tra tồn kho | Tồn kho sản phẩm được cập nhật thành 15 (10 + 5), hiển thị trong bảng danh sách tồn kho | | Untested | 11/15/2015 | |
| **FUNC-NK-10** | Ghi nhận lịch sử nhập hàng | 1. Truy cập /admin/inventory<br>2. Click nút "Nhập hàng"<br>3. Nhập hàng thành công<br>4. Xem chi tiết sản phẩm | Lịch sử nhập hàng được ghi nhận với đầy đủ thông tin: Ngày nhập, Số lượng, Giá nhập, Nhà cung cấp, Ghi chú | | Untested | 11/15/2015 | |
| **FUNC-NK-11** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/inventory<br>2. Click nút "Nhập hàng"<br>3. Điền đầy đủ thông tin<br>4. Tắt kết nối mạng<br>5. Click "Lưu" | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", form không được gửi | | Untested | 11/15/2015 | |
| **FUNC-NK-12** | Xử lý khi server lỗi | 1. Truy cập /admin/inventory<br>2. Click nút "Nhập hàng"<br>3. Điền đầy đủ thông tin<br>4. Server trả về lỗi 500<br>5. Click "Lưu" | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau", form không được gửi | | Untested | 11/15/2015 | |

---

**Người tạo:** Testing Team  
**Ngày cập nhật:** 11/15/2015  
**Phiên bản:** 1.0

