# Test Case Template - Quản lý tồn kho (Admin)

## Module Code
**Giao lộ 19: Họcl6c (Admin)**

## Test Requirement
1. Hiển thị danh sách tồn kho
2. Xem chi tiết tồn kho
3. Cập nhật số lượng tồn kho
4. Nhập hàng
5. Kiểm kê tồn kho
6. Cảnh báo tồn kho thấp

---

## Test Summary

### Người lớp Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 28 |
| **Fail** | 0 |
| **Untested** | 0 |
| **N/A** | 0 |
| **Number of Test cases** | 28 |

---

## Test Cases

### Function: Hiển thị danh sách tồn kho

#### Check GUI: Hiển thị danh sách tồn kho

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DSTK-01** | Kiểm tra tiêu đề trang | 1. Đăng nhập Admin<br>2. Truy cập /admin/inventory<br>3. Kiểm tra tiêu đề | Hiển thị tiêu đề "Quản lý tồn kho" với class text-3xl font-bold, mô tả "Theo dõi và quản lý tồn kho sản phẩm" với class text-muted-foreground, nằm trong div flex items-center justify-between | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSTK-02** | Kiểm tra thống kê tồn kho | 1. Đăng nhập Admin<br>2. Truy cập /admin/inventory<br>3. Kiểm tra thống kê | Hiển thị grid grid-cols-1 md:grid-cols-4 gap-4 với 4 Card: Card 1 "Tổng sản phẩm" với icon Package h-8 w-8 text-primary, Card 2 "Đủ hàng" với icon CheckCircle trong vòng tròn bg-green-100 text-green-500, Card 3 "Sắp hết" với icon AlertTriangle trong vòng tròn bg-yellow-100 text-yellow-500, Card 4 "Hết hàng" với icon AlertTriangle trong vòng tròn bg-red-100 text-red-500. Mỗi card có CardContent p-4 với text-sm text-muted-foreground cho label và text-2xl font-bold cho số | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSTK-03** | Kiểm tra các nút thao tác header | 1. Đăng nhập Admin<br>2. Truy cập /admin/inventory<br>3. Kiểm tra nút | Hiển thị div flex items-center gap-2 bên phải tiêu đề với Button variant="outline" "Nhập hàng" có icon Upload h-4 w-4 mr-2 onClick mở modal, Button variant="outline" "Kiểm kê" có icon ClipboardList h-4 w-4 mr-2 onClick mở modal, Button "Thêm sản phẩm" có icon Plus h-4 w-4 mr-2 với Link href="/admin/inventory/new" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSTK-04** | Kiểm tra card Bộ lọc | 1. Đăng nhập Admin<br>2. Truy cập /admin/inventory<br>3. Kiểm tra card bộ lọc | Hiển thị Card với CardContent p-4, có div flex items-center gap-4 chứa: Input tìm kiếm với icon Search absolute left-3, placeholder="Tìm kiếm sản phẩm...", Select Danh mục w-40, Select Trạng thái w-40, Button variant="outline" "Bộ lọc" với icon Filter | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSTK-05** | Kiểm tra dropdown Trạng thái | 1. Đăng nhập Admin<br>2. Truy cập /admin/inventory<br>3. Kiểm tra dropdown | Hiển thị Select với SelectTrigger w-40, SelectContent có các option: "Tất cả", "Đủ hàng", "Sắp hết", "Nguy hiểm", "Hết hàng" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSTK-06** | Kiểm tra card Tồn kho sản phẩm | 1. Đăng nhập Admin<br>2. Truy cập /admin/inventory<br>3. Kiểm tra card | Hiển thị Card với CardHeader có CardTitle "Tồn kho sản phẩm", CardDescription "Quản lý số lượng tồn kho của tất cả sản phẩm", CardContent chứa Table | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSTK-07** | Kiểm tra bảng danh sách tồn kho | 1. Đăng nhập Admin<br>2. Truy cập /admin/inventory<br>3. Kiểm tra bảng | Hiển thị Table với TableHeader có các TableHead: "Mã SP", "Tên SP", "Danh mục", "Tồn kho hiện tại", "Ngưỡng cảnh báo", "Trạng thái", "Thao tác" (w-24). TableBody có các TableRow với TableCell tương ứng | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSTK-08** | Kiểm tra cột Tồn kho hiện tại | 1. Đăng nhập Admin<br>2. Truy cập /admin/inventory<br>3. Kiểm tra cột | Mỗi hàng có TableCell chứa div space-y-1 với p font-medium (số lượng tồn kho) và Progress component với value tính theo (currentStock / maxStock) * 100, class h-2 w-20 | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSTK-09** | Kiểm tra cột Trạng thái | 1. Đăng nhập Admin<br>2. Truy cập /admin/inventory<br>3. Kiểm tra cột | Mỗi hàng có TableCell chứa Badge với variant tương ứng (default cho good "Đủ hàng" với icon CheckCircle màu xanh, secondary cho low "Sắp hết" với icon AlertTriangle màu vàng, destructive cho critical "Nguy hiểm" với icon AlertTriangle màu cam, destructive cho out_of_stock "Hết hàng" với icon AlertTriangle màu đỏ), bên trong có div flex items-center gap-1 với icon và label | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSTK-10** | Kiểm tra các nút thao tác | 1. Đăng nhập Admin<br>2. Truy cập /admin/inventory<br>3. Kiểm tra nút thao tác | Mỗi hàng có TableCell "Thao tác" với div flex items-center gap-1 chứa: Button variant="ghost" size="sm" với Link href="/admin/inventory/[id]" và icon Edit, Button variant="ghost" size="sm" với Link href="/admin/inventory/[id]/edit" và icon Edit, Button variant="ghost" size="sm" với icon Upload onClick mở modal nhập hàng | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Hiển thị danh sách tồn kho

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DSTK-01** | Xem danh sách tồn kho | 1. Đăng nhập Admin<br>2. Truy cập /admin/inventory | Hiển thị đầy đủ: thống kê 4 card (Tổng sản phẩm: 156, Đủ hàng: 142, Sắp hết: 8, Hết hàng: 6) với số liệu và icon, card Bộ lọc với ô tìm kiếm, 2 dropdown (Danh mục, Trạng thái), nút Bộ lọc, card Tồn kho sản phẩm với Table hiển thị các sản phẩm, mỗi hàng có Mã SP (SP001, SP002...), Tên SP (ảnh + tên + thương hiệu), Danh mục (Badge), Tồn kho hiện tại (số lượng + Progress bar), Ngưỡng cảnh báo, Trạng thái (Badge với icon), các nút thao tác, phân trang | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSTK-02** | Tìm kiếm sản phẩm trong tồn kho | 1. Đăng nhập Admin<br>2. Truy cập /admin/inventory<br>3. Nhập từ khóa tìm kiếm vào ô "Tìm kiếm sản phẩm..."<br>4. Click nút "Bộ lọc" | Danh sách sản phẩm được lọc theo từ khóa (tên sản phẩm, thương hiệu, mã sản phẩm), bảng cập nhật với các sản phẩm phù hợp | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSTK-03** | Lọc tồn kho theo danh mục | 1. Đăng nhập Admin<br>2. Truy cập /admin/inventory<br>3. Chọn danh mục từ dropdown<br>4. Click nút "Bộ lọc" | Danh sách sản phẩm được lọc theo danh mục đã chọn, bảng chỉ hiển thị sản phẩm có danh mục tương ứng | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSTK-04** | Lọc tồn kho theo trạng thái | 1. Đăng nhập Admin<br>2. Truy cập /admin/inventory<br>3. Chọn trạng thái từ dropdown (VD: "Sắp hết")<br>4. Click nút "Bộ lọc" | Danh sách sản phẩm được lọc theo trạng thái đã chọn, bảng chỉ hiển thị sản phẩm có trạng thái tương ứng, thống kê có thể cập nhật | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSTK-05** | Xem sách sắp hết | 1. Đăng nhập Admin<br>2. Truy cập /admin/inventory<br>3. Chọn trạng thái "Sắp hết" hoặc "Nguy hiểm"<br>4. Click nút "Bộ lọc" | Hiển thị danh sách sách có tồn kho dưới ngưỡng tối thiểu, các sản phẩm có Badge màu vàng/cam/đỏ với icon AlertTriangle, Progress bar hiển thị mức tồn kho thấp | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Xem chi tiết tồn kho

#### Check GUI: Xem chi tiết tồn kho

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CTTK-01** | Kiểm tra tiêu đề trang | 1. Đăng nhập Admin<br>2. Truy cập /admin/inventory/[id]<br>3. Kiểm tra tiêu đề | Hiển thị tiêu đề "Chi tiết tồn kho - SP[ID]" hoặc "Chi tiết tồn kho - [Mã sách]" với class text-2xl font-bold, layout tương tự trang chi tiết nhân viên | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-CTTK-02** | Kiểm tra thông tin tồn kho | 1. Đăng nhập Admin<br>2. Truy cập /admin/inventory/[id]<br>3. Kiểm tra thông tin | Hiển thị Card với CardHeader có CardTitle "Thông tin tồn kho", CardContent có grid layout, hiển thị các trường: Mã sách, Tên sách, Ảnh sản phẩm, Tồn kho hiện tại, Tồn kho tối thiểu, Tồn kho tối đa, Trạng thái (Badge với icon), Giá nhập, Giá bán, Lần cập nhật cuối | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-CTTK-03** | Kiểm tra card Lịch sử nhập/xuất | 1. Đăng nhập Admin<br>2. Truy cập /admin/inventory/[id]<br>3. Kiểm tra card | Hiển thị Card với CardHeader có CardTitle "Lịch sử nhập/xuất", CardContent có Table với các cột: Thời gian, Loại (Nhập/Xuất), Số lượng, Giá, Người thực hiện, Ghi chú | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Xem chi tiết tồn kho

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CTTK-01** | Xem chi tiết tồn kho | 1. Đăng nhập Admin<br>2. Truy cập /admin/inventory<br>3. Click nút Edit icon đầu tiên hoặc Link href="/admin/inventory/[id]" | Hiển thị đầy đủ thông tin: tiêu đề "Chi tiết tồn kho - SP[ID]", card Thông tin tồn kho với đầy đủ các trường (Mã SP, Tên SP, Ảnh, Tồn kho hiện tại, Tồn kho tối thiểu, Tồn kho tối đa, Trạng thái với Badge và icon, Giá nhập, Giá bán, Lần cập nhật cuối), card Lịch sử nhập/xuất với Table hiển thị các giao dịch nhập/xuất theo thời gian | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-CTTK-02** | Xem lịch sử nhập/xuất | 1. Đăng nhập Admin<br>2. Truy cập /admin/inventory/[id]<br>3. Xem card Lịch sử nhập/xuất | Hiển thị lịch sử nhập/xuất theo dòng thời gian từ cũ đến mới, mỗi giao dịch có: Thời gian, Loại (Badge "Nhập" hoặc "Xuất"), Số lượng, Giá (nếu là nhập), Người thực hiện, Ghi chú | FUNC-DN-02, FUNC-CTTK-01 | Pass | 11/15/2015 | |

---

### Function: Cập nhật số lượng tồn kho

#### Check FUNC: Cập nhật số lượng tồn kho

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-STK-01** | Cập nhật số lượng tồn kho | 1. Đăng nhập Admin<br>2. Truy cập /admin/inventory/[id]/edit<br>3. Cập nhật số lượng tồn kho<br>4. Lưu | Hiển thị form chỉnh sửa với các trường đã điền sẵn. Sau khi lưu: số lượng tồn kho được cập nhật thành công, hiển thị thông báo thành công (toast success), trạng thái được cập nhật tự động dựa trên số lượng mới (good/low/critical/out_of_stock), lịch sử thay đổi được ghi nhận vào Lịch sử nhập/xuất với loại "Điều chỉnh", Progress bar được cập nhật | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-STK-02** | Cập nhật với số lượng âm | 1. Đăng nhập Admin<br>2. Truy cập /admin/inventory/[id]/edit<br>3. Nhập số lượng < 0<br>4. Lưu | Hiển thị thông báo lỗi "Số lượng không được âm" (toast error), không cập nhật, form vẫn giữ giá trị cũ | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-STK-03** | Cập nhật với số lượng vượt quá tối đa | 1. Đăng nhập Admin<br>2. Truy cập /admin/inventory/[id]/edit<br>3. Nhập số lượng > maxStock<br>4. Lưu | Hiển thị thông báo cảnh báo "Số lượng vượt quá tồn kho tối đa. Bạn có muốn tiếp tục?" hoặc tự động điều chỉnh về maxStock, hoặc hiển thị lỗi "Số lượng không được vượt quá [maxStock]" | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Nhập hàng

#### Check GUI: Nhập hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-NH-01** | Kiểm tra modal Nhập hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/inventory<br>3. Click nút "Nhập hàng" hoặc icon Upload trên một sản phẩm<br>4. Kiểm tra modal | Hiển thị ReceiveGoodsModal với DialogTitle "Nhập hàng", có form với các trường: Sản phẩm (Select hoặc Input, có thể đã chọn sẵn nếu click từ sản phẩm cụ thể), Số lượng (Input type="number" required), Giá nhập (Input type="number"), Nhà cung cấp (Input hoặc Select), Ghi chú (Textarea), nút "Hủy" và "Xác nhận nhập hàng" | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Nhập hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-NH-01** | Nhập hàng thành công | 1. Đăng nhập Admin<br>2. Truy cập /admin/inventory<br>3. Click nút "Nhập hàng" hoặc icon Upload<br>4. Chọn sản phẩm (hoặc đã chọn sẵn)<br>5. Nhập số lượng > 0<br>6. Nhập giá nhập (nếu có)<br>7. Nhập nhà cung cấp và ghi chú<br>8. Click "Xác nhận nhập hàng" | Hàng được nhập thành công, hiển thị thông báo thành công (toast success), modal đóng, tồn kho được cập nhật (currentStock tăng), trạng thái được cập nhật tự động, lịch sử nhập được ghi nhận vào Lịch sử nhập/xuất với loại "Nhập", bảng tồn kho được refresh | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-NH-02** | Nhập hàng với số lượng không hợp lệ | 1. Đăng nhập Admin<br>2. Truy cập /admin/inventory<br>3. Click "Nhập hàng"<br>4. Nhập số lượng <= 0<br>5. Click "Xác nhận nhập hàng" | Hiển thị thông báo lỗi "Số lượng phải lớn hơn 0" (toast error), không nhập hàng, modal vẫn mở | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-NH-03** | Nhập hàng thiếu thông tin bắt buộc | 1. Đăng nhập Admin<br>2. Truy cập /admin/inventory<br>3. Click "Nhập hàng"<br>4. Để trống Sản phẩm hoặc Số lượng<br>5. Click "Xác nhận nhập hàng" | Trình duyệt hiển thị cảnh báo "Please fill out this field" hoặc validation message, form không được gửi | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-NH-04** | Hủy nhập hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/inventory<br>3. Click "Nhập hàng"<br>4. Nhập một số thông tin<br>5. Click "Hủy" | Modal đóng lại, không nhập hàng, không có thay đổi nào được lưu | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-NH-05** | Nhập hàng từ sản phẩm cụ thể | 1. Đăng nhập Admin<br>2. Truy cập /admin/inventory<br>3. Click icon Upload trên một sản phẩm cụ thể<br>4. Kiểm tra modal | Modal hiển thị với sản phẩm đã được chọn sẵn, trường Sản phẩm đã điền và có thể disabled hoặc readonly, chỉ cần nhập số lượng và thông tin khác | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Kiểm kê tồn kho

#### Check GUI: Kiểm kê tồn kho

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-KK-01** | Kiểm tra modal Kiểm kê | 1. Đăng nhập Admin<br>2. Truy cập /admin/inventory<br>3. Click nút "Kiểm kê"<br>4. Kiểm tra modal | Hiển thị InventoryAuditModal với DialogTitle "Kiểm kê tồn kho", có Table hoặc form với danh sách sản phẩm, mỗi hàng có: Tên sản phẩm, Số lượng hệ thống (hiển thị), Số lượng thực tế (Input type="number" để nhập), Chênh lệch (tính toán tự động), nút "Lưu kiểm kê" và "Hủy" | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Kiểm kê tồn kho

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-KK-01** | Thực hiện kiểm kê | 1. Đăng nhập Admin<br>2. Truy cập /admin/inventory<br>3. Click nút "Kiểm kê"<br>4. Nhập số lượng thực tế cho các sản phẩm<br>5. Click "Lưu kiểm kê" | Kiểm kê được thực hiện, hiển thị thông báo thành công (toast success), modal đóng, chênh lệch được tính toán và hiển thị (số lượng thực tế - số lượng hệ thống), tồn kho được điều chỉnh theo số lượng thực tế, lịch sử kiểm kê được ghi nhận với thông tin: sản phẩm, số lượng cũ, số lượng mới, chênh lệch, người thực hiện, thời gian, bảng tồn kho được refresh | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-KK-02** | Kiểm kê với số lượng thực tế < 0 | 1. Đăng nhập Admin<br>2. Truy cập /admin/inventory<br>3. Click "Kiểm kê"<br>4. Nhập số lượng thực tế < 0<br>5. Click "Lưu kiểm kê" | Hiển thị thông báo lỗi "Số lượng thực tế không được âm" (toast error), không lưu kiểm kê | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-KK-03** | Hủy kiểm kê | 1. Đăng nhập Admin<br>2. Truy cập /admin/inventory<br>3. Click "Kiểm kê"<br>4. Nhập một số số lượng thực tế<br>5. Click "Hủy" | Modal đóng lại, không lưu kiểm kê, không có thay đổi nào được áp dụng | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Cảnh báo tồn kho thấp

#### Check GUI: Cảnh báo tồn kho thấp

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CB-01** | Kiểm tra cảnh báo trong danh sách | 1. Đăng nhập Admin<br>2. Truy cập /admin/inventory<br>3. Kiểm tra các sản phẩm có tồn kho thấp | Các sản phẩm có tồn kho dưới ngưỡng tối thiểu hiển thị với Badge variant="secondary" hoặc "destructive" (Sắp hết/Nguy hiểm/Hết hàng) với icon AlertTriangle màu vàng/cam/đỏ, Progress bar hiển thị mức thấp (màu vàng/cam/đỏ) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-CB-02** | Kiểm tra trang cảnh báo riêng | 1. Đăng nhập Admin<br>2. Truy cập /admin/inventory/alerts<br>3. Kiểm tra trang | Hiển thị tiêu đề "Cảnh báo tồn kho thấp", Card với Table hiển thị chỉ các sản phẩm có tồn kho dưới ngưỡng tối thiểu, mỗi hàng có: Mã SP, Tên SP, Tồn kho hiện tại, Ngưỡng tối thiểu, Trạng thái (Badge), nút "Nhập hàng" | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Cảnh báo tồn kho thấp

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CB-01** | Xem danh sách cảnh báo | 1. Đăng nhập Admin<br>2. Truy cập /admin/inventory<br>3. Lọc theo trạng thái "Sắp hết", "Nguy hiểm", "Hết hàng" | Hiển thị danh sách sách có tồn kho dưới ngưỡng tối thiểu, các sản phẩm có Badge màu vàng/cam/đỏ với icon AlertTriangle, Progress bar hiển thị mức tồn kho thấp, thống kê hiển thị số lượng sản phẩm sắp hết/hết hàng | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-CB-02** | Nhập hàng từ cảnh báo | 1. Đăng nhập Admin<br>2. Truy cập /admin/inventory<br>3. Click icon Upload trên một sản phẩm sắp hết<br>4. Thực hiện nhập hàng | Modal nhập hàng hiển thị với sản phẩm đã được chọn sẵn, có thể nhập số lượng ngay, sau khi nhập hàng thành công, trạng thái sản phẩm có thể chuyển từ "Sắp hết" sang "Đủ hàng" nếu số lượng mới >= minStock | FUNC-DN-02, FUNC-NH-01 | Pass | 11/15/2015 | |
| **FUNC-CB-03** | Xem trang cảnh báo riêng | 1. Đăng nhập Admin<br>2. Truy cập /admin/inventory/alerts | Hiển thị trang riêng chỉ các sản phẩm có tồn kho thấp, có thể có thống kê tổng quan về số lượng sản phẩm cần nhập hàng, có nút "Nhập hàng hàng loạt" hoặc nhập từng sản phẩm | FUNC-DN-02 | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn MDX để dễ dàng quản lý và cập nhật test cases.*
