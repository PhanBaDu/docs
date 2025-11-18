# Test Case Template - Báo cáo và thống kê (Admin)

## Module Code
**Giao lộ 19: Họcl6c (Admin)**

## Test Requirement
1. Hiển thị báo cáo và thống kê tổng quan
2. Xem chi tiết báo cáo
3. Xem báo cáo doanh thu
4. Xem thống kê bán hàng
5. Xem báo cáo khách hàng
6. Xem báo cáo tồn kho

---

## Test Summary

### Người lớp Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 24 |
| **Fail** | 0 |
| **Untested** | 0 |
| **N/A** | 0 |
| **Number of Test cases** | 24 |

---

## Test Cases

### Function: Hiển thị báo cáo và thống kê tổng quan

#### Check GUI: Hiển thị báo cáo và thống kê

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-BC-01** | Kiểm tra tiêu đề trang | 1. Đăng nhập Admin<br>2. Truy cập /admin/reports<br>3. Kiểm tra tiêu đề | Hiển thị tiêu đề "Báo cáo & Thống kê" với class text-3xl font-bold, mô tả "Theo dõi hiệu suất kinh doanh và phân tích dữ liệu" với class text-muted-foreground, nằm trong div flex items-center justify-between | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-BC-02** | Kiểm tra các nút header | 1. Đăng nhập Admin<br>2. Truy cập /admin/reports<br>3. Kiểm tra nút | Hiển thị div flex items-center gap-2 bên phải tiêu đề với Select defaultValue="6months" w-40 có các option: "7 ngày qua", "30 ngày qua", "3 tháng qua", "6 tháng qua", "1 năm qua", Button variant="outline" "Xuất báo cáo" có icon Download h-4 w-4 mr-2 | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-BC-03** | Kiểm tra thống kê tổng quan | 1. Đăng nhập Admin<br>2. Truy cập /admin/reports<br>3. Kiểm tra thống kê | Hiển thị grid grid-cols-1 md:grid-cols-4 gap-4 với 4 Card: Card 1 "Doanh thu tháng" với icon DollarSign h-8 w-8 text-primary, số "22.5M đ", div flex items-center gap-1 với icon TrendingUp màu xanh và text "+22%", Card 2 "Đơn hàng tháng" với icon ShoppingCart, số "85", growth "+18%", Card 3 "Khách hàng mới" với icon Users, số "23", growth "+28%", Card 4 "Sản phẩm bán" với icon Package, số "342", growth "+15%". Mỗi card có CardContent p-4 với text-sm text-muted-foreground cho label và text-2xl font-bold cho số | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-BC-04** | Kiểm tra Tabs | 1. Đăng nhập Admin<br>2. Truy cập /admin/reports<br>3. Kiểm tra tabs | Hiển thị Tabs defaultValue="revenue" với TabsList className="grid w-full grid-cols-4" có 4 TabsTrigger: "Doanh thu", "Sản phẩm", "Khách hàng", "Tồn kho" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-BC-05** | Kiểm tra Tab Doanh thu | 1. Đăng nhập Admin<br>2. Truy cập /admin/reports<br>3. Click tab "Doanh thu" | Hiển thị TabsContent value="revenue" với space-y-6 chứa: Card "Biểu đồ doanh thu" với CardDescription "Doanh thu theo tháng trong 6 tháng qua", CardContent có div h-80 border-2 border-dashed với icon BarChart3 và text "Biểu đồ doanh thu sẽ được hiển thị ở đây", Card "Chi tiết doanh thu" với CardContent có danh sách các tháng với doanh thu, số đơn hàng, và growth % | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-BC-06** | Kiểm tra Tab Sản phẩm | 1. Đăng nhập Admin<br>2. Truy cập /admin/reports<br>3. Click tab "Sản phẩm" | Hiển thị TabsContent value="products" với Card "Sản phẩm bán chạy" có CardDescription "Top sản phẩm có doanh số cao nhất", CardContent có danh sách sản phẩm với số thứ tự (#1, #2...), tên sản phẩm, số lượng đã bán, doanh thu, growth % | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-BC-07** | Kiểm tra Tab Khách hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/reports<br>3. Click tab "Khách hàng" | Hiển thị TabsContent value="customers" với grid grid-cols-1 md:grid-cols-2 gap-4 chứa các Card thống kê: "Khách hàng mới", "Khách VIP", "Tỷ lệ quay lại", "Giá trị đơn hàng TB", mỗi card có số liệu và growth % | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-BC-08** | Kiểm tra Tab Tồn kho | 1. Đăng nhập Admin<br>2. Truy cập /admin/reports<br>3. Click tab "Tồn kho" | Hiển thị TabsContent value="inventory" với Card "Cảnh báo tồn kho" có CardDescription "Sản phẩm sắp hết hàng cần nhập thêm", CardContent có danh sách sản phẩm với tên, số lượng hiện tại, số lượng tối thiểu, Badge trạng thái (Nguy hiểm/Cảnh báo/Hết hàng) | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Hiển thị báo cáo và thống kê

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-BC-01** | Xem danh sách báo cáo | 1. Đăng nhập Admin<br>2. Truy cập /admin/reports | Hiển thị đầy đủ: tiêu đề và mô tả, Select khoảng thời gian và nút Xuất báo cáo, thống kê tổng quan 4 card (Doanh thu tháng: 22.5M đ +22%, Đơn hàng tháng: 85 +18%, Khách hàng mới: 23 +28%, Sản phẩm bán: 342 +15%), Tabs với 4 tab (Doanh thu, Sản phẩm, Khách hàng, Tồn kho), Tab Doanh thu hiển thị biểu đồ và chi tiết doanh thu theo tháng | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-BC-02** | Chọn khoảng thời gian | 1. Đăng nhập Admin<br>2. Truy cập /admin/reports<br>3. Chọn khoảng thời gian từ Select (VD: "30 ngày qua") | Dữ liệu báo cáo được cập nhật theo khoảng thời gian đã chọn, thống kê tổng quan được tính lại, biểu đồ và danh sách chi tiết được refresh với dữ liệu mới | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-BC-03** | Chuyển đổi giữa các tab | 1. Đăng nhập Admin<br>2. Truy cập /admin/reports<br>3. Click tab "Sản phẩm" | Tab "Sản phẩm" được kích hoạt, hiển thị Card "Sản phẩm bán chạy" với danh sách top sản phẩm, mỗi sản phẩm có số thứ tự (#1, #2...), tên, số lượng đã bán, doanh thu (toLocaleString), growth % với icon TrendingUp màu xanh | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-BC-04** | Xem thống kê khách hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/reports<br>3. Click tab "Khách hàng" | Tab "Khách hàng" được kích hoạt, hiển thị grid với 4 Card: "Khách hàng mới" (23, +28%), "Khách VIP" (12, +50%), "Tỷ lệ quay lại" (68%, +10%), "Giá trị đơn hàng TB" (1.3M đ, +14%), mỗi card có icon Users và growth với icon TrendingUp màu xanh | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-BC-05** | Xem cảnh báo tồn kho | 1. Đăng nhập Admin<br>2. Truy cập /admin/reports<br>3. Click tab "Tồn kho" | Tab "Tồn kho" được kích hoạt, hiển thị Card "Cảnh báo tồn kho" với danh sách sản phẩm sắp hết, mỗi sản phẩm có tên, thông tin "Còn [số] sản phẩm (Tối thiểu: [số])", Badge trạng thái với variant tương ứng (destructive cho "Nguy hiểm", secondary cho "Cảnh báo", outline cho "Hết hàng") | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-BC-06** | Xuất báo cáo | 1. Đăng nhập Admin<br>2. Truy cập /admin/reports<br>3. Click nút "Xuất báo cáo" | Hiển thị Dialog hoặc menu cho phép chọn định dạng (PDF, Excel), sau khi chọn: báo cáo được xuất thành công, file được tải xuống với tên file chứa ngày tháng, hiển thị thông báo thành công (toast success) | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Xem chi tiết báo cáo

#### Check FUNC: Xem chi tiết báo cáo

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CTBC-01** | Xem chi tiết doanh thu theo tháng | 1. Đăng nhập Admin<br>2. Truy cập /admin/reports<br>3. Xem tab "Doanh thu"<br>4. Xem chi tiết một tháng | Hiển thị Card "Chi tiết doanh thu" với danh sách các tháng, mỗi tháng có: tên tháng (VD: "Tháng 1"), số đơn hàng (VD: "45 đơn hàng"), doanh thu (toLocaleString("vi-VN")đ), growth % với icon TrendingUp (màu xanh) nếu > 0 hoặc TrendingDown (màu đỏ) nếu < 0, text màu xanh/đỏ tương ứng | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-CTBC-02** | Tải xuống báo cáo | 1. Đăng nhập Admin<br>2. Truy cập /admin/reports<br>3. Click nút "Xuất báo cáo"<br>4. Chọn định dạng (PDF hoặc Excel)<br>5. Click "Tải xuống" | Báo cáo được tải xuống thành công dưới dạng PDF hoặc Excel, file có tên chứa ngày tháng (VD: "BaoCao_2024-01-20.pdf"), file chứa đầy đủ thông tin: thống kê tổng quan, biểu đồ (nếu PDF), bảng dữ liệu chi tiết, hiển thị thông báo thành công (toast success) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-CTBC-03** | In báo cáo | 1. Đăng nhập Admin<br>2. Truy cập /admin/reports<br>3. Click nút "In báo cáo" (nếu có) hoặc Ctrl+P | Hiển thị dialog in của trình duyệt với preview báo cáo, có thể in ra giấy hoặc lưu PDF, preview hiển thị đầy đủ thông tin: tiêu đề, thống kê, biểu đồ, bảng dữ liệu | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Xem báo cáo doanh thu

#### Check GUI: Báo cáo doanh thu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DT-01** | Kiểm tra tab Doanh thu | 1. Đăng nhập Admin<br>2. Truy cập /admin/reports<br>3. Click tab "Doanh thu" | Hiển thị TabsContent value="revenue" với Card "Biểu đồ doanh thu" có CardTitle và CardDescription, CardContent có placeholder biểu đồ với icon BarChart3 và text "Biểu đồ doanh thu sẽ được hiển thị ở đây", Card "Chi tiết doanh thu" với danh sách các tháng | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DT-02** | Kiểm tra biểu đồ doanh thu | 1. Đăng nhập Admin<br>2. Truy cập /admin/reports<br>3. Xem tab "Doanh thu"<br>4. Kiểm tra biểu đồ | Hiển thị div h-80 flex items-center justify-center border-2 border-dashed border-muted-foreground/25 rounded-lg với icon BarChart3 h-12 w-12 mx-auto mb-4 text-muted-foreground và text "Biểu đồ doanh thu sẽ được hiển thị ở đây" (placeholder, trong thực tế sẽ có biểu đồ thực) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DT-03** | Kiểm tra chi tiết doanh thu | 1. Đăng nhập Admin<br>2. Truy cập /admin/reports<br>3. Xem tab "Doanh thu"<br>4. Kiểm tra chi tiết | Hiển thị Card "Chi tiết doanh thu" với CardContent có space-y-4 chứa các div flex items-center justify-between p-4 border rounded-lg, mỗi div có: tên tháng (font-medium), số đơn hàng (text-sm text-muted-foreground), doanh thu (font-medium, toLocaleString), growth % với icon và màu tương ứng | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Xem báo cáo doanh thu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DT-01** | Xem báo cáo doanh thu | 1. Đăng nhập Admin<br>2. Truy cập /admin/reports<br>3. Click tab "Doanh thu" | Hiển thị báo cáo doanh thu với: Card "Biểu đồ doanh thu" (placeholder hoặc biểu đồ thực), Card "Chi tiết doanh thu" với danh sách các tháng trong khoảng thời gian đã chọn, mỗi tháng hiển thị: tên tháng, số đơn hàng, doanh thu (toLocaleString), growth % với icon TrendingUp (xanh) nếu tăng hoặc TrendingDown (đỏ) nếu giảm | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DT-02** | Xuất báo cáo doanh thu | 1. Đăng nhập Admin<br>2. Truy cập /admin/reports<br>3. Click tab "Doanh thu"<br>4. Click nút "Xuất báo cáo" | Báo cáo doanh thu được xuất thành công dưới dạng PDF hoặc Excel, file chứa: biểu đồ doanh thu (nếu PDF), bảng chi tiết doanh thu theo tháng, thống kê tổng quan, hiển thị thông báo thành công (toast success) | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Xem thống kê bán hàng

#### Check FUNC: Xem thống kê bán hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TKBH-01** | Xem thống kê bán hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/reports<br>3. Click tab "Sản phẩm" | Hiển thị thống kê bán hàng: Card "Sản phẩm bán chạy" với CardDescription "Top sản phẩm có doanh số cao nhất", CardContent có danh sách sản phẩm được sắp xếp theo doanh số, mỗi sản phẩm có: số thứ tự (#1, #2...) trong vòng tròn bg-primary/10, tên sản phẩm (font-medium), số lượng đã bán (text-sm text-muted-foreground), doanh thu (font-medium, toLocaleString), growth % với icon TrendingUp màu xanh | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TKBH-02** | Xem sách bán chạy | 1. Đăng nhập Admin<br>2. Truy cập /admin/reports<br>3. Click tab "Sản phẩm"<br>4. Xem danh sách sách bán chạy | Hiển thị danh sách sách bán chạy với xếp hạng (từ #1 đến #5 hoặc nhiều hơn), mỗi sách có: số thứ tự trong vòng tròn, tên sách, số lượng đã bán (VD: "156 sản phẩm đã bán"), doanh thu (VD: "187,200,000đ"), growth % (VD: "+15%"), các sách được sắp xếp theo doanh số từ cao xuống thấp | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Xem báo cáo khách hàng

#### Check FUNC: Xem báo cáo khách hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-BCKH-01** | Xem báo cáo khách hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/reports<br>3. Click tab "Khách hàng" | Hiển thị báo cáo khách hàng: grid grid-cols-1 md:grid-cols-2 gap-4 với 4 Card: Card "Khách hàng mới" (23, +28%), Card "Khách VIP" (12, +50%), Card "Tỷ lệ quay lại" (68%, +10%), Card "Giá trị đơn hàng TB" (1.3M đ, +14%). Mỗi card có: label (text-sm text-muted-foreground), số liệu (text-2xl font-bold, format đặc biệt cho số lớn), growth % với icon TrendingUp màu xanh, icon Users h-8 w-8 text-primary | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-BCKH-02** | Xuất báo cáo khách hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/reports<br>3. Click tab "Khách hàng"<br>4. Click nút "Xuất báo cáo" | Báo cáo khách hàng được xuất thành công dưới dạng PDF hoặc Excel, file chứa: thống kê khách hàng mới, VIP, tỷ lệ quay lại, giá trị đơn hàng TB, có thể có biểu đồ phân bố khách hàng, hiển thị thông báo thành công (toast success) | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Xem báo cáo tồn kho

#### Check FUNC: Xem báo cáo tồn kho

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-BCTK-01** | Xem báo cáo tồn kho | 1. Đăng nhập Admin<br>2. Truy cập /admin/reports<br>3. Click tab "Tồn kho" | Hiển thị báo cáo tồn kho: Card "Cảnh báo tồn kho" với CardDescription "Sản phẩm sắp hết hàng cần nhập thêm", CardContent có danh sách sản phẩm với: tên sản phẩm (font-medium), thông tin "Còn [số] sản phẩm (Tối thiểu: [số])" (text-sm text-muted-foreground), Badge trạng thái với variant tương ứng (destructive cho "Nguy hiểm", secondary cho "Cảnh báo", outline cho "Hết hàng"), các sản phẩm được sắp xếp theo mức độ nguy hiểm | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-BCTK-02** | Xuất báo cáo tồn kho | 1. Đăng nhập Admin<br>2. Truy cập /admin/reports<br>3. Click tab "Tồn kho"<br>4. Click nút "Xuất báo cáo" | Báo cáo tồn kho được xuất thành công dưới dạng PDF hoặc Excel, file chứa: tổng quan tình trạng kho, danh sách sản phẩm sắp hết/hết hàng với số lượng hiện tại và tối thiểu, trạng thái, có thể có biểu đồ phân bố tồn kho, hiển thị thông báo thành công (toast success) | FUNC-DN-02 | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn MDX để dễ dàng quản lý và cập nhật test cases.*
