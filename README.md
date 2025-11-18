# Test Case Template - Quản lý sách và kho (Admin)

## Module Code
**Giao lộ 19: Họcl6c (Admin)**

## Test Requirement
1. Hiển thị toàn bộ sách
2. Xem chi tiết sách
3. Toàn quyền quản lý sách (Thêm, Sửa, Xóa, Ẩn/Hiện)
4. Quản lý danh mục sách
5. Thiết lập giá sách

---

## Test Summary

### Người lớp Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 35 |
| **Fail** | 0 |
| **Untested** | 0 |
| **N/A** | 0 |
| **Number of Test cases** | 35 |

---

## Test Cases

### Function: Hiển thị toàn bộ sách

#### Check GUI: Hiển thị danh sách sách

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DSS-01** | Kiểm tra tiêu đề trang | 1. Đăng nhập Admin<br>2. Truy cập /admin/products<br>3. Kiểm tra tiêu đề | Hiển thị tiêu đề "Quản lý sản phẩm" với class text-3xl font-bold, mô tả "Quản lý danh sách sản phẩm và thông tin chi tiết" với class text-muted-foreground, nằm trong div flex items-center justify-between | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSS-02** | Kiểm tra thống kê sách | 1. Đăng nhập Admin<br>2. Truy cập /admin/products<br>3. Kiểm tra thống kê | Hiển thị grid grid-cols-1 md:grid-cols-4 gap-4 với 4 Card: Card 1 "Tổng sản phẩm" với icon Package h-8 w-8 text-primary, Card 2 "Đang bán" với vòng tròn bg-green-100 và dot bg-green-500, Card 3 "Sắp hết hàng" với vòng tròn bg-yellow-100 và dot bg-yellow-500, Card 4 "Hết hàng" với vòng tròn bg-red-100 và dot bg-red-500. Mỗi card có CardContent p-4 với text-sm text-muted-foreground cho label và text-2xl font-bold cho số | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSS-03** | Kiểm tra nút Nhập hàng và Thêm sản phẩm | 1. Đăng nhập Admin<br>2. Truy cập /admin/products<br>3. Kiểm tra nút | Hiển thị div flex items-center gap-2 bên phải tiêu đề với Button variant="outline" "Nhập hàng" có icon Package h-4 w-4 mr-2, Button "Thêm sản phẩm" có icon Plus h-4 w-4 mr-2 với Link href="/admin/products/new" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSS-04** | Kiểm tra card Bộ lọc | 1. Đăng nhập Admin<br>2. Truy cập /admin/products<br>3. Kiểm tra card bộ lọc | Hiển thị Card với CardContent p-4, có div flex items-center gap-4 chứa: Input tìm kiếm với icon Search absolute left-3, Select Danh mục w-40, Select Thương hiệu w-40, Select Trạng thái w-40, Button variant="outline" "Bộ lọc" với icon Filter | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSS-05** | Kiểm tra ô Tìm kiếm | 1. Đăng nhập Admin<br>2. Truy cập /admin/products<br>3. Kiểm tra ô tìm kiếm | Hiển thị Input với icon Search absolute left-3 top-1/2 transform -translate-y-1/2, placeholder="Tìm kiếm sản phẩm...", class pl-10, flex-1 relative, có onKeyPress Enter để lọc | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSS-06** | Kiểm tra dropdown Danh mục | 1. Đăng nhập Admin<br>2. Truy cập /admin/products<br>3. Kiểm tra dropdown | Hiển thị Select với SelectTrigger w-40, placeholder="Danh mục", SelectContent có các option: "Tất cả", "Gundam", "Figure", "Mô hình xe", "Máy bay", "Tàu chiến", "Khác" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSS-07** | Kiểm tra dropdown Thương hiệu | 1. Đăng nhập Admin<br>2. Truy cập /admin/products<br>3. Kiểm tra dropdown | Hiển thị Select với SelectTrigger w-40, placeholder="Thương hiệu", SelectContent có các option: "Tất cả", "Bandai", "Good Smile Company", "Tamiya", "Revell", "Banpresto", "Kotobukiya" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSS-08** | Kiểm tra dropdown Trạng thái | 1. Đăng nhập Admin<br>2. Truy cập /admin/products<br>3. Kiểm tra dropdown | Hiển thị Select với SelectTrigger w-40, placeholder="Trạng thái", SelectContent có các option: "Tất cả", "Đang bán", "Sắp hết hàng", "Hết hàng", "Ngừng bán" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSS-09** | Kiểm tra card Danh sách sản phẩm | 1. Đăng nhập Admin<br>2. Truy cập /admin/products<br>3. Kiểm tra card | Hiển thị Card với CardHeader có CardTitle "Danh sách sản phẩm", CardDescription "Quản lý tất cả sản phẩm trong hệ thống", CardContent chứa Table | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSS-10** | Kiểm tra bảng danh sách sản phẩm | 1. Đăng nhập Admin<br>2. Truy cập /admin/products<br>3. Kiểm tra bảng | Hiển thị Table với TableHeader có các TableHead: "#" (w-12), "Sản phẩm", "Danh mục", "Giá", "Tồn kho", "Trạng thái", "Đánh giá", "Ngày tạo", "Thao tác" (w-24). TableBody có các TableRow với TableCell tương ứng | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSS-11** | Kiểm tra cột Sản phẩm | 1. Đăng nhập Admin<br>2. Truy cập /admin/products<br>3. Kiểm tra cột Sản phẩm | Mỗi hàng có TableCell chứa div flex items-center gap-3 với: div w-12 h-12 rounded-lg overflow-hidden chứa Image (width={48} height={48}), div chứa p font-medium (tên sản phẩm) và p text-sm text-muted-foreground (thương hiệu) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSS-12** | Kiểm tra cột Giá | 1. Đăng nhập Admin<br>2. Truy cập /admin/products<br>3. Kiểm tra cột Giá | Mỗi hàng có TableCell chứa div với p font-medium (giá hiện tại với toLocaleString("vi-VN")đ) và p text-sm text-muted-foreground line-through (giá gốc) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSS-13** | Kiểm tra cột Tồn kho | 1. Đăng nhập Admin<br>2. Truy cập /admin/products<br>3. Kiểm tra cột Tồn kho | Mỗi hàng có TableCell chứa div với p font-medium (số lượng tồn kho) và p text-sm text-muted-foreground "Tối thiểu: [số]" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSS-14** | Kiểm tra cột Trạng thái | 1. Đăng nhập Admin<br>2. Truy cập /admin/products<br>3. Kiểm tra cột Trạng thái | Mỗi hàng có TableCell chứa Badge với variant tương ứng (default cho active "Đang bán", secondary cho low_stock "Sắp hết", destructive cho out_of_stock "Hết hàng", outline cho inactive "Ngừng bán") | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSS-15** | Kiểm tra cột Đánh giá | 1. Đăng nhập Admin<br>2. Truy cập /admin/products<br>3. Kiểm tra cột Đánh giá | Mỗi hàng có TableCell chứa div flex items-center gap-1 với span text-sm font-medium (rating) và span text-sm text-muted-foreground (số reviews trong ngoặc) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSS-16** | Kiểm tra các nút thao tác | 1. Đăng nhập Admin<br>2. Truy cập /admin/products<br>3. Kiểm tra nút thao tác | Mỗi hàng có TableCell "Thao tác" với div flex items-center gap-1 chứa: Button variant="ghost" size="sm" với Link href="/admin/products/[id]" và icon Eye, Button variant="ghost" size="sm" với Link href="/admin/products/[id]/edit" và icon Edit, Dialog với DialogTrigger là Button variant="ghost" size="sm" có icon EyeOff, Dialog với DialogTrigger là Button variant="ghost" size="sm" có icon Trash2 | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSS-17** | Kiểm tra phân trang | 1. Đăng nhập Admin<br>2. Truy cập /admin/products<br>3. Kiểm tra phân trang | Hiển thị div flex items-center justify-between với text-sm text-muted-foreground "Hiển thị 1-[số] trong [số] sản phẩm" và div flex items-center gap-2 với các Button variant="outline" size="sm": "Trước" (disabled), "1", "2", "3", "...", "32", "Sau" | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Hiển thị danh sách sách

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DSS-01** | Xem danh sách sách | 1. Đăng nhập Admin<br>2. Truy cập /admin/products | Hiển thị đầy đủ: thống kê 4 card (Tổng sản phẩm: 156, Đang bán: 142, Sắp hết hàng: 8, Hết hàng: 6) với số liệu và icon/indicator, card Bộ lọc với ô tìm kiếm, 3 dropdown (Danh mục, Thương hiệu, Trạng thái), nút Bộ lọc, card Danh sách sản phẩm với Table hiển thị các sản phẩm, mỗi hàng có #, Sản phẩm (ảnh + tên + thương hiệu), Danh mục (Badge), Giá (giá hiện tại + giá gốc gạch ngang), Tồn kho (số lượng + tối thiểu), Trạng thái (Badge), Đánh giá (rating + reviews), Ngày tạo, các nút thao tác, phân trang | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSS-02** | Tìm kiếm sách | 1. Đăng nhập Admin<br>2. Truy cập /admin/products<br>3. Nhập từ khóa tìm kiếm vào ô "Tìm kiếm sản phẩm..."<br>4. Nhấn Enter hoặc click nút "Bộ lọc" | Danh sách sản phẩm được lọc theo từ khóa (tên sản phẩm, thương hiệu, danh mục), hiển thị thông báo "Đã lọc [số] sản phẩm" (toast success), bảng cập nhật với các sản phẩm phù hợp | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSS-03** | Lọc sách theo danh mục | 1. Đăng nhập Admin<br>2. Truy cập /admin/products<br>3. Chọn danh mục từ dropdown (VD: "Gundam")<br>4. Click nút "Bộ lọc" | Danh sách sản phẩm được lọc theo danh mục đã chọn, hiển thị thông báo "Đã lọc [số] sản phẩm" (toast success), bảng chỉ hiển thị sản phẩm có danh mục tương ứng | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSS-04** | Lọc sách theo thương hiệu | 1. Đăng nhập Admin<br>2. Truy cập /admin/products<br>3. Chọn thương hiệu từ dropdown (VD: "Bandai")<br>4. Click nút "Bộ lọc" | Danh sách sản phẩm được lọc theo thương hiệu đã chọn, hiển thị thông báo "Đã lọc [số] sản phẩm" (toast success), bảng chỉ hiển thị sản phẩm có thương hiệu tương ứng | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSS-05** | Lọc sách theo trạng thái | 1. Đăng nhập Admin<br>2. Truy cập /admin/products<br>3. Chọn trạng thái từ dropdown (VD: "Đang bán")<br>4. Click nút "Bộ lọc" | Danh sách sản phẩm được lọc theo trạng thái đã chọn, hiển thị thông báo "Đã lọc [số] sản phẩm" (toast success), bảng chỉ hiển thị sản phẩm có trạng thái tương ứng | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSS-06** | Kết hợp nhiều bộ lọc | 1. Đăng nhập Admin<br>2. Truy cập /admin/products<br>3. Chọn danh mục "Gundam"<br>4. Chọn thương hiệu "Bandai"<br>5. Chọn trạng thái "Đang bán"<br>6. Nhập từ khóa tìm kiếm<br>7. Click nút "Bộ lọc" | Danh sách sản phẩm được lọc theo tất cả các tiêu chí đã chọn, hiển thị thông báo "Đã lọc [số] sản phẩm" (toast success), bảng chỉ hiển thị sản phẩm thỏa mãn tất cả điều kiện | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSS-07** | Phân trang danh sách | 1. Đăng nhập Admin<br>2. Truy cập /admin/products<br>3. Click số trang hoặc nút "Sau" | Danh sách chuyển sang trang tiếp theo, hiển thị các sản phẩm của trang đó, text "Hiển thị X-Y trong [số] sản phẩm" được cập nhật | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Xem chi tiết sách

#### Check GUI: Xem chi tiết sách

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CTS-01** | Kiểm tra tiêu đề trang | 1. Đăng nhập Admin<br>2. Truy cập /admin/products/[id]<br>3. Kiểm tra tiêu đề | Hiển thị tiêu đề "Chi tiết sách - [Mã sách]" hoặc "Chi tiết sản phẩm - [ID]" với class text-2xl font-bold, layout tương tự trang chi tiết nhân viên | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-CTS-02** | Kiểm tra thông tin cơ bản | 1. Đăng nhập Admin<br>2. Truy cập /admin/products/[id]<br>3. Kiểm tra thông tin | Hiển thị Card với CardHeader có CardTitle "Thông tin cơ bản", CardContent có grid layout, hiển thị các trường: Mã sách (hoặc ID), Tên sách, Tác giả (hoặc Thương hiệu), Nhà xuất bản, Năm xuất bản, ISBN, Danh mục (Badge), Ảnh sản phẩm | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-CTS-03** | Kiểm tra thông tin bán hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/products/[id]<br>3. Kiểm tra thông tin | Hiển thị Card với CardHeader có CardTitle "Thông tin bán hàng", CardContent hiển thị các trường: Giá bán, Giá nhập (hoặc Giá gốc), Lợi nhuận (tính toán), Tồn kho, Tồn kho tối thiểu, Trạng thái (Badge), Đánh giá (rating + reviews), Ngày tạo, Ngày cập nhật | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Xem chi tiết sách

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CTS-01** | Xem chi tiết sách | 1. Đăng nhập Admin<br>2. Truy cập /admin/products<br>3. Click nút Eye icon hoặc Link href="/admin/products/[id]" | Hiển thị đầy đủ thông tin: tiêu đề "Chi tiết sản phẩm - [ID]", card Thông tin cơ bản với đầy đủ các trường (ID, Tên, Thương hiệu, Danh mục, Ảnh), card Thông tin bán hàng với đầy đủ các trường (Giá, Giá gốc, Tồn kho, Trạng thái, Đánh giá, Ngày tạo, Ngày cập nhật), các nút thao tác (Chỉnh sửa, Ẩn, Xóa) | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Thêm sách mới

#### Check GUI: Thêm sách mới

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-TS-01** | Kiểm tra tiêu đề trang | 1. Đăng nhập Admin<br>2. Truy cập /admin/products/new<br>3. Kiểm tra tiêu đề | Hiển thị tiêu đề "Thêm sản phẩm mới" hoặc "Thêm sách mới" với class text-2xl font-bold, layout tương tự trang thêm nhân viên | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-TS-02** | Kiểm tra form thêm sách | 1. Đăng nhập Admin<br>2. Truy cập /admin/products/new<br>3. Kiểm tra form | Hiển thị Card với CardHeader có CardTitle "Thông tin sản phẩm", CardContent chứa form với grid layout, có các trường: Tên sách (Input required), Tác giả/Thương hiệu (Input hoặc Select), Nhà xuất bản, Năm xuất bản (Input type="date"), ISBN (Input), Danh mục (Select), Giá bán (Input type="number"), Giá nhập (Input type="number"), Tồn kho ban đầu (Input type="number"), Tồn kho tối thiểu (Input type="number"), Mô tả (Textarea), Ảnh sản phẩm (File upload), nút "Lưu" và "Hủy" | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Thêm sách mới

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TS-01** | Thêm sách thành công | 1. Đăng nhập Admin<br>2. Truy cập /admin/products/new<br>3. Nhập đầy đủ thông tin hợp lệ (Tên sách, Tác giả/Thương hiệu, Nhà xuất bản, Năm xuất bản, ISBN, Danh mục, Giá bán, Giá nhập, Tồn kho, Mô tả, Upload ảnh)<br>4. Nhấn Lưu | Sách được thêm thành công, mã sách được tạo tự động (hoặc ID được tạo), hiển thị thông báo thành công (toast success), chuyển về danh sách sách (/admin/products) hoặc ở lại trang để thêm tiếp | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TS-02** | Thêm sách thiếu thông tin bắt buộc | 1. Đăng nhập Admin<br>2. Truy cập /admin/products/new<br>3. Để trống các trường bắt buộc (Tên sách)<br>4. Nhấn Lưu | Trình duyệt hiển thị cảnh báo "Please fill out this field" trên các trường bắt buộc, form không được gửi, không có request đến server | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TS-03** | Thêm sách với ISBN trùng | 1. Đăng nhập Admin<br>2. Truy cập /admin/products/new<br>3. Nhập ISBN đã tồn tại<br>4. Nhập các thông tin khác hợp lệ<br>5. Nhấn Lưu | Hiển thị thông báo lỗi "ISBN đã tồn tại" (toast error), không tạo sách, vẫn ở trang thêm sách, các trường input vẫn giữ giá trị đã nhập | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TS-04** | Hủy thêm sách | 1. Đăng nhập Admin<br>2. Truy cập /admin/products/new<br>3. Nhập một số thông tin<br>4. Nhấn Hủy | Đóng form, quay về danh sách sách (/admin/products), không lưu thông tin đã nhập | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Cập nhật thông tin sách

#### Check GUI: Chỉnh sửa sách

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-SS-01** | Kiểm tra tiêu đề trang | 1. Đăng nhập Admin<br>2. Truy cập /admin/products/[id]/edit<br>3. Kiểm tra tiêu đề | Hiển thị tiêu đề "Chỉnh sửa sản phẩm - [ID]" hoặc "Chỉnh sửa sách - [Mã sách]" với layout tương tự trang thêm sách | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-SS-02** | Kiểm tra form đã điền sẵn | 1. Đăng nhập Admin<br>2. Truy cập /admin/products/[id]/edit<br>3. Kiểm tra form | Form hiển thị với thông tin hiện tại của sách đã được điền sẵn vào các trường input, select, textarea, file upload tương ứng | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Cập nhật thông tin sách

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-SS-01** | Cập nhật thông tin sách thành công | 1. Đăng nhập Admin<br>2. Truy cập /admin/products/[id]/edit<br>3. Cập nhật thông tin (VD: Tên sách, Giá bán, Tồn kho, Mô tả)<br>4. Nhấn Lưu | Thông tin được cập nhật thành công, hiển thị thông báo thành công (toast success), lịch sử thay đổi được ghi nhận, có thể chuyển về chi tiết sách hoặc danh sách | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-SS-02** | Cập nhật với ISBN trùng (sách khác) | 1. Đăng nhập Admin<br>2. Truy cập /admin/products/[id]/edit<br>3. Đổi ISBN thành ISBN đã tồn tại của sách khác<br>4. Nhấn Lưu | Hiển thị thông báo lỗi "ISBN đã tồn tại" (toast error), không cập nhật, vẫn ở trang chỉnh sửa | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-SS-03** | Hủy chỉnh sửa | 1. Đăng nhập Admin<br>2. Truy cập /admin/products/[id]/edit<br>3. Thay đổi thông tin<br>4. Nhấn Hủy | Đóng form, quay về chi tiết sách (/admin/products/[id]) hoặc danh sách, không lưu thay đổi, thông tin vẫn giữ nguyên như ban đầu | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Xóa sách

#### Check FUNC: Xóa sách

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XS-01** | Xóa sách | 1. Đăng nhập Admin<br>2. Truy cập /admin/products<br>3. Click nút Trash2 icon trên một sản phẩm<br>4. Xác nhận xóa trong Dialog | Hiển thị Dialog với DialogTitle "Xác nhận xóa sản phẩm", DialogDescription "Bạn có chắc chắn muốn xóa sản phẩm "[Tên]"? Hành động này không thể hoàn tác.", có nút "Hủy" và "Xóa" variant="destructive". Sau khi xác nhận: sách được xóa thành công, hiển thị thông báo "Đã xóa sản phẩm "[Tên]"" (toast success), dialog đóng, bảng được cập nhật, sản phẩm biến mất khỏi danh sách | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-XS-02** | Hủy xóa sách | 1. Đăng nhập Admin<br>2. Truy cập /admin/products<br>3. Click nút Trash2 icon<br>4. Click nút "Hủy" trong Dialog | Dialog đóng lại, không xóa sách, vẫn ở trang danh sách, sản phẩm vẫn hiển thị trong bảng | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Ẩn/Hiện sách

#### Check FUNC: Ẩn/Hiện sách

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-AHS-01** | Ẩn sách | 1. Đăng nhập Admin<br>2. Truy cập /admin/products<br>3. Click nút EyeOff icon trên một sản phẩm<br>4. Xác nhận ẩn trong Dialog | Hiển thị Dialog với DialogTitle "Xác nhận ẩn sản phẩm", DialogDescription "Bạn có chắc chắn muốn ẩn sản phẩm "[Tên]"? Sản phẩm sẽ không hiển thị cho khách hàng nhưng vẫn tồn tại trong hệ thống.", có nút "Hủy" và "Ẩn sản phẩm" variant="secondary". Sau khi xác nhận: sách được ẩn thành công, hiển thị thông báo "Đã ẩn sản phẩm "[Tên]"" (toast success), dialog đóng, trạng thái cập nhật thành "Ngừng bán" hoặc "Ẩn", sách không hiển thị cho người dùng trên trang user | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-AHS-02** | Hủy ẩn sách | 1. Đăng nhập Admin<br>2. Truy cập /admin/products<br>3. Click nút EyeOff icon<br>4. Click nút "Hủy" trong Dialog | Dialog đóng lại, không ẩn sách, trạng thái không thay đổi | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-AHS-03** | Hiện sách | 1. Đăng nhập Admin<br>2. Truy cập /admin/products/[id] (sách đã ẩn)<br>3. Click [Hiện] hoặc thay đổi trạng thái<br>4. Xác nhận | Sách được hiện thành công, hiển thị thông báo thành công (toast success), trạng thái cập nhật thành "Đang bán", sách hiển thị cho người dùng trên trang user | FUNC-DN-02, FUNC-CTS-01 | Pass | 11/15/2015 | |

---

### Function: Quản lý danh mục sách

#### Check GUI: Quản lý danh mục sách

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DM-01** | Kiểm tra tiêu đề trang | 1. Đăng nhập Admin<br>2. Truy cập /admin/products/categories<br>3. Kiểm tra tiêu đề | Hiển thị tiêu đề "Quản lý danh mục sách" hoặc "Quản lý danh mục sản phẩm" với layout tương tự các trang quản lý khác | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DM-02** | Kiểm tra danh sách danh mục | 1. Đăng nhập Admin<br>2. Truy cập /admin/products/categories<br>3. Kiểm tra bảng | Hiển thị Card với Table có các cột: Mã danh mục, Tên danh mục, Mô tả, Số sách (số lượng sản phẩm trong danh mục), Trạng thái (Badge), Thao tác. Có nút "Thêm danh mục mới" | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Quản lý danh mục sách

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DM-01** | Xem danh sách danh mục | 1. Đăng nhập Admin<br>2. Truy cập /admin/products/categories | Hiển thị danh sách tất cả danh mục sách với đầy đủ thông tin: Mã danh mục, Tên danh mục, Mô tả, Số sách (số lượng sản phẩm), Trạng thái, các nút thao tác (Chỉnh sửa, Xóa) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DM-02** | Thêm danh mục mới | 1. Đăng nhập Admin<br>2. Truy cập /admin/products/categories<br>3. Click [Thêm danh mục mới]<br>4. Nhập thông tin (Tên danh mục, Mô tả)<br>5. Lưu | Hiển thị Dialog hoặc form thêm mới. Sau khi lưu: danh mục mới được tạo thành công, hiển thị thông báo thành công (toast success), mã danh mục được tạo tự động, danh mục mới hiển thị trong bảng | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DM-03** | Chỉnh sửa danh mục | 1. Đăng nhập Admin<br>2. Truy cập /admin/products/categories<br>3. Click [Chỉnh sửa] trên một danh mục<br>4. Cập nhật thông tin (Tên danh mục, Mô tả)<br>5. Lưu | Hiển thị Dialog hoặc form chỉnh sửa với các trường đã điền sẵn. Sau khi lưu: thông tin danh mục được cập nhật thành công, hiển thị thông báo thành công, bảng được cập nhật | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DM-04** | Xóa danh mục | 1. Đăng nhập Admin<br>2. Truy cập /admin/products/categories<br>3. Click [Xóa] trên một danh mục<br>4. Xác nhận xóa | Hiển thị Dialog xác nhận "Bạn có chắc chắn muốn xóa danh mục này? Sách trong danh mục sẽ được chuyển về danh mục khác.". Sau khi xác nhận: danh mục được xóa thành công, hiển thị thông báo thành công, sách trong danh mục được chuyển về danh mục mặc định hoặc danh mục khác, danh mục biến mất khỏi bảng | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Thiết lập giá sách

#### Check GUI: Thiết lập giá sách

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-GS-01** | Kiểm tra tiêu đề trang | 1. Đăng nhập Admin<br>2. Truy cập /admin/products/pricing<br>3. Kiểm tra tiêu đề | Hiển thị tiêu đề "Thiết lập giá sách" hoặc "Thiết lập giá sản phẩm" với layout tương tự các trang quản lý khác | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-GS-02** | Kiểm tra danh sách sách | 1. Đăng nhập Admin<br>2. Truy cập /admin/products/pricing<br>3. Kiểm tra bảng | Hiển thị Card với Table có các cột: Mã sách, Tên sách, Giá hiện tại, Giá mới (Input type="number"), Thay đổi (tính toán %), Thao tác. Có nút "Lưu tất cả" và "Khôi phục" | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Thiết lập giá sách

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-GS-01** | Xem danh sách sách để thiết lập giá | 1. Đăng nhập Admin<br>2. Truy cập /admin/products/pricing | Hiển thị danh sách sách với giá hiện tại và ô nhập giá mới cho mỗi sách, có thể thấy mức thay đổi (tăng/giảm %) khi nhập giá mới | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-GS-02** | Thay đổi giá sách | 1. Đăng nhập Admin<br>2. Truy cập /admin/products/pricing<br>3. Nhập giá mới cho một sách<br>4. Click [Lưu giá] trên sách đó | Giá sách được thay đổi thành công, hiển thị thông báo thành công (toast success), mức thay đổi được hiển thị (tăng/giảm %), lịch sử thay đổi giá được ghi nhận vào PriceHistory với thông tin: oldPrice, newPrice, changedBy, changedAt, reason (nếu có) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-GS-03** | Lưu tất cả thay đổi giá | 1. Đăng nhập Admin<br>2. Truy cập /admin/products/pricing<br>3. Thay đổi giá cho nhiều sách<br>4. Click [Lưu tất cả] | Tất cả thay đổi giá được lưu thành công, hiển thị thông báo thành công "Đã cập nhật giá cho [số] sản phẩm" (toast success), tất cả giá mới được áp dụng, lịch sử thay đổi được ghi nhận cho từng sách | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-GS-04** | Khôi phục thay đổi giá | 1. Đăng nhập Admin<br>2. Truy cập /admin/products/pricing<br>3. Thay đổi giá cho một hoặc nhiều sách<br>4. Click [Khôi phục] | Thay đổi giá được khôi phục về giá ban đầu, các ô Input "Giá mới" được reset về giá hiện tại, mức thay đổi về 0%, không có thay đổi nào được lưu | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-GS-05** | Thay đổi giá với giá âm | 1. Đăng nhập Admin<br>2. Truy cập /admin/products/pricing<br>3. Nhập giá mới < 0<br>4. Click [Lưu giá] | Hiển thị thông báo lỗi "Giá không được âm" (toast error), không lưu giá, giá vẫn giữ nguyên | FUNC-DN-02 | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn MDX để dễ dàng quản lý và cập nhật test cases.*
