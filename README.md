# Test Case Template - Tìm kiếm sách và hiển thị (Nhân viên)

## Module Code
**Giao lộ 19: Họcl6c (Nhân viên)**

## Test Requirement
1. Hiển thị danh sách sách
2. Tìm kiếm sách
3. Kiểm tra tồn kho

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

### Function: Hiển thị danh sách sách

#### Check GUI: Hiển thị danh sách sách

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-HDS-01** | Kiểm tra tiêu đề trang | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/products<br>3. Kiểm tra tiêu đề | Hiển thị div space-y-6 với h1 "Danh sách sách" class text-2xl font-bold, p "Quản lý và hiển thị thông tin các sách hiện đang bán trong cửa hàng" class text-sm text-muted-foreground | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-HDS-02** | Kiểm tra thống kê tổng quan | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/products<br>3. Kiểm tra thống kê | Hiển thị div grid grid-cols-2 md:grid-cols-5 gap-4 với 5 Card: Card "Tổng số sách" với CardContent p-4 có div text-sm text-muted-foreground "Tổng số sách", div text-xl font-semibold "1,250". Card "Đang bán" với "1,180". Card "Tạm ngừng" với "45". Card "Sắp hết hàng" với "25". Card "Tổng giá trị" className="col-span-2 md:col-span-1" với "2.5 tỷ VNĐ" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-HDS-03** | Kiểm tra card Bộ lọc sách | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/products<br>3. Kiểm tra card | Hiển thị Card với CardHeader có CardTitle "Bộ lọc sách", CardDescription "Lọc theo thể loại, NXB, giá, trạng thái, năm", CardContent className="grid gap-4 md:grid-cols-6" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-HDS-04** | Kiểm tra các bộ lọc | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/products<br>3. Kiểm tra bộ lọc | Hiển thị: div grid gap-2 với Label "Thể loại", Select với SelectTrigger SelectValue placeholder="Tất cả", SelectContent có SelectItem (Tất cả, Khoa học, Văn học, Kinh tế, Lịch sử, Thiếu nhi). div grid gap-2 với Label "Nhà xuất bản", Select với các option (Tất cả, NXB Trẻ, NXB Kim Đồng, NXB Giáo dục, NXB Thế giới). div grid gap-2 md:col-span-2 với Label "Khoảng giá", Slider min={0} max={1000000} step={10000}, div text-xs text-muted-foreground hiển thị giá trị. div grid gap-2 với Label "Trạng thái", Select (Tất cả, Đang bán, Tạm ngừng, Sắp hết hàng, Hết hàng). div grid gap-2 với Label "Năm xuất bản", Select (Tất cả, 2024, 2023, 2022, 2021, Trước 2021). div grid gap-2 md:col-span-2 với Label "Tìm kiếm", Input placeholder="Tìm theo tên sách, tác giả, mã sách...". div grid gap-2 với Label "Sắp xếp", Select (Mặc định, Tên A-Z, Tên Z-A, Giá tăng dần, Giá giảm dần, Mới nhất, Bán chạy nhất). div flex items-end gap-2 với Button "Áp dụng" className="shrink-0", Button variant="outline" "Xóa bộ lọc" className="shrink-0" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-HDS-05** | Kiểm tra chuyển đổi view | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/products<br>3. Kiểm tra view switch | Hiển thị div flex items-center justify-between với Tabs value={view} onValueChange, TabsList có TabsTrigger value="grid" "Lưới", TabsTrigger value="list" "Danh sách", div text-sm text-muted-foreground "Hiển thị 25 sách/trang" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-HDS-06** | Kiểm tra danh sách sách dạng lưới | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/products<br>3. Chọn view "Lưới"<br>4. Kiểm tra danh sách | Hiển thị div grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4 với các Card className="overflow-hidden" chứa: div aspect-[3/2] relative bg-muted với Image src={book.cover} alt={book.title} fill className="object-cover", CardContent className="p-4 space-y-2" với div flex items-start justify-between gap-2 có div font-semibold line-clamp-2 (title), div text-sm text-muted-foreground (author), Badge với variant tương ứng status, div flex items-center justify-between text-sm với span font-medium (price), span text-muted-foreground (stock), div flex gap-2 với Button variant="outline" asChild Link href="/nhanvien/products/[id]" "Xem chi tiết", Button variant="outline" asChild Link href="/nhanvien/products/[id]/inventory" "Kiểm tra tồn kho", Button "Thêm vào đơn" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-HDS-07** | Kiểm tra danh sách sách dạng danh sách | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/products<br>3. Chọn view "Danh sách"<br>4. Kiểm tra danh sách | Hiển thị div space-y-2 với các Card có CardContent className="p-4 flex items-center gap-4" chứa: div relative w-20 h-14 bg-muted overflow-hidden rounded với Image, div flex-1 min-w-0 có div flex items-center justify-between gap-2 với div min-w-0 có div font-medium truncate (title), div text-sm text-muted-foreground truncate (author), Badge, div text-sm text-muted-foreground (publisher, category, year), div text-right có div font-semibold (price), div text-sm text-muted-foreground (stock), div flex gap-2 với các Button | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-HDS-08** | Kiểm tra phân trang | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/products<br>3. Kiểm tra phân trang | Hiển thị div flex justify-center với Pagination, PaginationContent có PaginationItem với PaginationLink href="#" isActive "1", PaginationLink "2", PaginationLink "3" | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Hiển thị danh sách sách

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-HDS-01** | Xem danh sách sách | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/products | Hiển thị đầy đủ: tiêu đề "Danh sách sách" và mô tả, thống kê 5 card (Tổng số sách: 1,250, Đang bán: 1,180, Tạm ngừng: 45, Sắp hết hàng: 25, Tổng giá trị: 2.5 tỷ VNĐ), card Bộ lọc sách với đầy đủ các bộ lọc (Thể loại, Nhà xuất bản, Khoảng giá với Slider, Trạng thái, Năm xuất bản, Tìm kiếm, Sắp xếp), nút "Áp dụng" và "Xóa bộ lọc", Tabs chuyển đổi view (Lưới/Danh sách), danh sách sách với đầy đủ thông tin (ảnh bìa, tên sách, tác giả, giá bán, tồn kho, trạng thái Badge), các nút thao tác (Xem chi tiết, Kiểm tra tồn kho, Thêm vào đơn), phân trang | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-HDS-02** | Lọc sách theo thể loại | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/products<br>3. Chọn thể loại từ Select (VD: "Khoa học")<br>4. Click "Áp dụng" | Danh sách sách được lọc theo thể loại đã chọn, chỉ hiển thị các sách thuộc thể loại "Khoa học", thống kê được cập nhật theo kết quả lọc, số lượng kết quả được hiển thị | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-HDS-03** | Lọc sách theo nhà xuất bản | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/products<br>3. Chọn nhà xuất bản từ Select (VD: "NXB Trẻ")<br>4. Click "Áp dụng" | Danh sách sách được lọc theo nhà xuất bản đã chọn, chỉ hiển thị các sách của "NXB Trẻ", thống kê được cập nhật | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-HDS-04** | Lọc sách theo khoảng giá | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/products<br>3. Điều chỉnh Slider khoảng giá (VD: 100,000 - 500,000đ)<br>4. Click "Áp dụng" | Danh sách sách được lọc theo khoảng giá đã chọn, chỉ hiển thị các sách có giá trong khoảng 100,000 - 500,000đ, giá trị khoảng giá được hiển thị dưới Slider với format "100,000đ - 500,000đ", thống kê được cập nhật | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-HDS-05** | Lọc sách theo trạng thái | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/products<br>3. Chọn trạng thái từ Select (VD: "Sắp hết hàng")<br>4. Click "Áp dụng" | Danh sách sách được lọc theo trạng thái đã chọn, chỉ hiển thị các sách có trạng thái "Sắp hết hàng", Badge màu secondary, thống kê được cập nhật | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-HDS-06** | Lọc sách theo năm xuất bản | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/products<br>3. Chọn năm xuất bản từ Select (VD: "2024")<br>4. Click "Áp dụng" | Danh sách sách được lọc theo năm xuất bản đã chọn, chỉ hiển thị các sách xuất bản năm 2024, thống kê được cập nhật | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-HDS-07** | Lọc kết hợp nhiều tiêu chí | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/products<br>3. Chọn thể loại "Khoa học", nhà xuất bản "NXB Trẻ", trạng thái "Đang bán"<br>4. Click "Áp dụng" | Danh sách sách được lọc theo tất cả các tiêu chí đã chọn, chỉ hiển thị các sách thỏa mãn tất cả điều kiện (thể loại Khoa học AND nhà xuất bản NXB Trẻ AND trạng thái Đang bán), thống kê được cập nhật | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-HDS-08** | Xóa bộ lọc | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/products<br>3. Áp dụng các bộ lọc<br>4. Click "Xóa bộ lọc" | Tất cả các bộ lọc được reset về giá trị mặc định (Tất cả), danh sách sách hiển thị lại tất cả sách, thống kê được cập nhật về giá trị ban đầu | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-HDS-09** | Sắp xếp danh sách sách | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/products<br>3. Chọn tiêu chí sắp xếp từ Select (VD: "Giá tăng dần")<br>4. Click "Áp dụng" | Danh sách sách được sắp xếp theo tiêu chí đã chọn, các sách được hiển thị theo thứ tự giá tăng dần, thứ tự được cập nhật ngay lập tức, duy trì trạng thái sắp xếp khi chuyển trang | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-HDS-10** | Chuyển đổi view Lưới/Danh sách | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/products<br>3. Click TabsTrigger "Danh sách" | View chuyển từ "Lưới" sang "Danh sách", danh sách sách được hiển thị dạng danh sách với layout khác (ảnh nhỏ hơn, thông tin nằm ngang), TabsTrigger "Danh sách" được active | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-HDS-11** | Xem chi tiết sách | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/products<br>3. Click nút "Xem chi tiết" trên một sách | Chuyển đến trang /nhanvien/products/[id], hiển thị thông tin chi tiết của sách | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-HDS-12** | Thêm sách vào đơn hàng | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/products<br>3. Click nút "Thêm vào đơn" trên một sách | Sách được thêm vào đơn hàng hiện tại (nếu đang tạo đơn) hoặc tạo đơn hàng mới, hiển thị thông báo thành công "Đã thêm sách vào đơn hàng" (toast success), có thể hiển thị số lượng sách trong đơn hàng ở header | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-HDS-13** | Chuyển trang phân trang | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/products<br>3. Click PaginationLink "2" | Chuyển sang trang 2, danh sách sách được cập nhật với các sách của trang 2, PaginationLink "2" được active (isActive), duy trì các bộ lọc và sắp xếp đã chọn | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Tìm kiếm sách

#### Check FUNC: Tìm kiếm sách

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TKS-01** | Tìm kiếm sách theo tên | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/products<br>3. Nhập từ khóa tìm kiếm vào Input (VD: "React")<br>4. Click "Áp dụng" | Danh sách sách được lọc theo từ khóa "React", chỉ hiển thị các sách có tên chứa "React", tìm kiếm không phân biệt hoa thường, có thể hiển thị số lượng kết quả tìm được, thống kê được cập nhật | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TKS-02** | Tìm kiếm sách theo tác giả | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/products<br>3. Nhập tên tác giả vào Input (VD: "Nguyễn Văn A")<br>4. Click "Áp dụng" | Danh sách sách được lọc theo tác giả, chỉ hiển thị các sách của tác giả "Nguyễn Văn A", thống kê được cập nhật | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TKS-03** | Tìm kiếm sách theo mã sách | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/products<br>3. Nhập mã sách vào Input (VD: "BK-001")<br>4. Click "Áp dụng" | Danh sách sách được lọc theo mã sách, chỉ hiển thị sách có mã "BK-001", có thể hiển thị 1 kết quả hoặc không có kết quả nếu mã không tồn tại | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TKS-04** | Tìm kiếm không có kết quả | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/products<br>3. Nhập từ khóa không tồn tại (VD: "xyz123")<br>4. Click "Áp dụng" | Hiển thị thông báo "Không tìm thấy sách nào phù hợp với từ khóa 'xyz123'", danh sách sách trống, thống kê hiển thị 0 cho tất cả các chỉ số | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TKS-05** | Tìm kiếm kết hợp với bộ lọc | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/products<br>3. Nhập từ khóa "React"<br>4. Chọn thể loại "Công nghệ"<br>5. Click "Áp dụng" | Danh sách sách được lọc theo cả từ khóa "React" và thể loại "Công nghệ", chỉ hiển thị các sách có tên chứa "React" VÀ thuộc thể loại "Công nghệ", thống kê được cập nhật | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Kiểm tra tồn kho

#### Check GUI: Kiểm tra tồn kho

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-KTK-01** | Kiểm tra tiêu đề trang | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/products/[id]/inventory<br>3. Kiểm tra tiêu đề | Hiển thị tiêu đề "Kiểm tra tồn kho" hoặc tên sách với thông tin tồn kho | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-KTK-02** | Kiểm tra thông tin sách | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/products/[id]/inventory<br>3. Kiểm tra thông tin | Hiển thị Card với thông tin sách: Tên sách, Mã sách, Tác giả, Thể loại (Badge), Nhà xuất bản | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-KTK-03** | Kiểm tra thông tin tồn kho | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/products/[id]/inventory<br>3. Kiểm tra thông tin | Hiển thị Card với: Số lượng hiện có, Số lượng đã bán, Số lượng đặt trước, Trạng thái (Badge: Đủ hàng/Sắp hết hàng/Hết hàng), Cập nhật lần cuối | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-KTK-04** | Kiểm tra lịch sử nhập xuất | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/products/[id]/inventory<br>3. Kiểm tra bảng | Hiển thị Table với TableHeader có các TableHead: "Thời gian", "Loại giao dịch" (Badge), "Số lượng" (+/-), "Ghi chú", "Người thực hiện". TableBody có các TableRow với TableCell tương ứng | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-KTK-05** | Kiểm tra cảnh báo tồn kho | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/products/[id]/inventory với sách sắp hết hàng<br>3. Kiểm tra cảnh báo | Hiển thị Alert với icon AlertCircle và AlertDescription "Sách sắp hết hàng (dưới 10 cuốn)" hoặc "Sách đã hết hàng" hoặc "Cần nhập thêm hàng" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-KTK-06** | Kiểm tra các nút thao tác | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/products/[id]/inventory<br>3. Kiểm tra nút | Hiển thị div flex gap-2 với Button "Cập nhật tồn kho", Button "Yêu cầu nhập hàng", Button "In báo cáo", Button "Xem chi tiết" | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Kiểm tra tồn kho

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-KTK-01** | Xem thông tin tồn kho | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/products/[id]/inventory | Hiển thị đầy đủ: thông tin sách (Tên sách, Mã sách, Tác giả, Thể loại Badge, Nhà xuất bản), thông tin tồn kho (Số lượng hiện có, Số lượng đã bán, Số lượng đặt trước, Trạng thái Badge, Cập nhật lần cuối), lịch sử nhập xuất Table với các giao dịch (Thời gian, Loại giao dịch Badge, Số lượng +/- với màu xanh/đỏ, Ghi chú, Người thực hiện), cảnh báo tồn kho (nếu có), các nút thao tác | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-KTK-02** | Xem cảnh báo tồn kho thấp | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/products/[id]/inventory với sách có số lượng < 10 | Hiển thị Alert với variant="destructive" hoặc "warning" "Sách sắp hết hàng (dưới 10 cuốn)", Badge trạng thái "Sắp hết hàng" màu secondary hoặc warning, số lượng hiện có được highlight màu vàng hoặc đỏ | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-KTK-03** | Xem cảnh báo hết hàng | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/products/[id]/inventory với sách có số lượng = 0 | Hiển thị Alert với variant="destructive" "Sách đã hết hàng", Badge trạng thái "Hết hàng" màu destructive, số lượng hiện có = 0 được highlight màu đỏ | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-KTK-04** | Yêu cầu nhập hàng | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/products/[id]/inventory<br>3. Click nút "Yêu cầu nhập hàng"<br>4. Nhập số lượng yêu cầu và ghi chú<br>5. Xác nhận | Hiển thị Dialog với DialogTitle "Yêu cầu nhập hàng", DialogDescription, Input "Số lượng yêu cầu" type="number", Textarea "Ghi chú ưu tiên", nút "Hủy" và "Gửi yêu cầu". Sau khi xác nhận: yêu cầu được gửi thành công, hiển thị thông báo thành công "Yêu cầu nhập hàng đã được gửi đến nhân viên kho" (toast success), nhân viên kho nhận được thông báo, trạng thái yêu cầu được theo dõi (chờ xử lý), dialog đóng lại | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-KTK-05** | In báo cáo tồn kho | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/products/[id]/inventory<br>3. Click nút "In báo cáo" | Báo cáo tồn kho được tạo và mở dialog in hoặc chuyển đến trang in, báo cáo bao gồm: thông tin sách, số lượng hiện có, lịch sử nhập xuất gần đây, định dạng dễ đọc và chuyên nghiệp, có thể in hoặc xuất PDF | FUNC-DN-02 | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn MDX để dễ dàng quản lý và cập nhật test cases.*

