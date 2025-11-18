# Test Case Template - Quản lý đánh giá (Nhân viên)

## Module Code
**Giao lộ 19: Họcl6c (Nhân viên)**

## Test Requirement
1. Hiển thị danh sách đánh giá
2. Xem chi tiết đánh giá
3. Quản lý và theo dõi đánh giá từ khách hàng

---

## Test Summary

### Người lớp Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 42 |
| **Fail** | 0 |
| **Untested** | 0 |
| **N/A** | 0 |
| **Number of Test cases** | 42 |

---

## Test Cases

### Function: Hiển thị danh sách đánh giá (Nhân viên)

#### Check GUI: `/nhanvien/reviews`

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DG-LIST-01** | Kiểm tra tiêu đề trang | 1. Đăng nhập Nhân viên<br>2. Truy cập `/nhanvien/reviews` | Hiển thị h1 `Quản lý đánh giá` class text-2xl font-bold & mô tả `Xem và quản lý đánh giá từ khách hàng` class text-sm text-muted-foreground | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DG-LIST-02** | Kiểm tra thống kê đánh giá | 1. Ở `/nhanvien/reviews` quan sát grid đầu | Grid `grid-cols-2 md:grid-cols-4` gồm Card `Tổng đánh giá 156`, `5 sao 89`, `4 sao 45`, `3 sao 12`, `2 sao 7`, `1 sao 3` với Badge màu tương ứng | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DG-LIST-03** | Kiểm tra card Tìm kiếm & Bộ lọc | 1. Quan sát card tiếp theo | CardTitle `Tìm kiếm & Bộ lọc`, mô tả `Tìm theo tên sách, khách hàng; lọc theo điểm đánh giá & trạng thái`, grid md:grid-cols-6 có Input placeholder "Tên sách, khách hàng...", Select `Điểm đánh giá` (Tất cả, 5 sao, 4 sao, 3 sao, 2 sao, 1 sao), Select `Trạng thái` (Tất cả, Đã duyệt, Chờ duyệt, Đã ẩn), Button `Tìm kiếm`, Button variant="outline" `Xóa bộ lọc` | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DG-LIST-04** | Kiểm tra bảng danh sách đánh giá | 1. Quan sát card `Danh sách đánh giá` | TableHeader có các cột STT, Sách, Khách hàng, Điểm đánh giá, Nhận xét, Ngày đánh giá, Trạng thái, Thao tác. TableBody hiển thị hàng mẫu với Image sách, tên sách, tên khách hàng, div flex gap-1 với 5 icon Star (h-4 w-4) màu vàng/xám, p text-sm line-clamp-2 nhận xét, thời gian, Badge trạng thái, nút `Xem chi tiết` | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DG-LIST-05** | Kiểm tra phân trang | 1. Cuộn xuống cuối bảng | Hiển thị div flex justify-between items-center với text "Hiển thị 1-10 của 156 đánh giá", div flex gap-2 với Button variant="outline" size="sm" "Trước", Button variant="outline" size="sm" "Sau", Select số items/trang | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DG-LIST-06** | Kiểm tra sidebar panels | 1. Quan sát grid 3 card bên phải | Card `Đánh giá mới nhất` liệt kê 5 đánh giá gần nhất với Image, tên sách, tên khách, điểm sao; Card `Thống kê theo sách` có placeholder chart `h-40 bg-muted`; Card `Hoạt động gần đây` liệt kê các hoạt động duyệt/ẩn đánh giá | FUNC-DN-02 | Pass | 11/15/2015 | |

---

#### Check FUNC: Hiển thị danh sách đánh giá

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DG-LIST-01** | Xem danh sách đánh giá | 1. Đăng nhập<br>2. Truy cập `/nhanvien/reviews` | Trang hiển thị thống kê, bộ lọc, bảng danh sách đánh giá, sidebar như GUI tests; dữ liệu khớp mock reviews | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DG-LIST-02** | Tìm kiếm đánh giá theo từ khóa | 1. Nhập `Sách hay` vào Input tìm kiếm<br>2. Click `Tìm kiếm` | Bảng chỉ hiển thị đánh giá có tên sách hoặc tên khách hàng khớp; nếu không có hiển thị thông báo "Không tìm thấy đánh giá" | FUNC-DG-LIST-01 | Pass | 11/15/2015 | |
| **FUNC-DG-LIST-03** | Lọc theo điểm đánh giá | 1. Chọn Điểm đánh giá = `5 sao`<br>2. Click `Tìm kiếm` | Bảng chỉ hiển thị các đánh giá 5 sao (5 icon Star màu vàng) | FUNC-DG-LIST-01 | Pass | 11/15/2015 | |
| **FUNC-DG-LIST-04** | Lọc theo trạng thái | 1. Chọn Trạng thái = `Chờ duyệt`<br>2. Click `Tìm kiếm` | Bảng chỉ hiển thị các đánh giá có status `Chờ duyệt` (Badge variant warning) | FUNC-DG-LIST-01 | Pass | 11/15/2015 | |
| **FUNC-DG-LIST-05** | Kết hợp tìm kiếm và lọc | 1. Nhập `Nguyễn Văn A` vào Input<br>2. Chọn Điểm = `4 sao`, Trạng thái = `Đã duyệt`<br>3. Click `Tìm kiếm` | Bảng hiển thị đánh giá của khách hàng "Nguyễn Văn A" có 4 sao và đã duyệt | FUNC-DG-LIST-01 | Pass | 11/15/2015 | |
| **FUNC-DG-LIST-06** | Xóa bộ lọc | 1. Đã có bộ lọc đang áp dụng<br>2. Click `Xóa bộ lọc` | Input và Select về giá trị mặc định (rỗng/Tất cả), bảng hiển thị toàn bộ đánh giá | FUNC-DG-LIST-01 | Pass | 11/15/2015 | |
| **FUNC-DG-LIST-07** | Phân trang - Chuyển trang | 1. Click nút `Sau` | Bảng hiển thị trang tiếp theo (items 11-20), nút `Trước` được enable | FUNC-DG-LIST-01 | Pass | 11/15/2015 | |
| **FUNC-DG-LIST-08** | Phân trang - Thay đổi số items/trang | 1. Chọn Select số items = `20` | Bảng hiển thị 20 items/trang, tổng số trang giảm, text cập nhật "Hiển thị 1-20 của 156 đánh giá" | FUNC-DG-LIST-01 | Pass | 11/15/2015 | |
| **FUNC-DG-LIST-09** | Click Xem chi tiết | 1. Click nút `Xem chi tiết` ở một đánh giá | Chuyển đến trang `/nhanvien/reviews/[id]` hiển thị chi tiết đánh giá | FUNC-DG-LIST-01 | Pass | 11/15/2015 | |
| **FUNC-DG-LIST-10** | Cập nhật thống kê real-time | 1. Thực hiện thao tác duyệt/ẩn đánh giá<br>2. Quay lại danh sách | Thống kê ở đầu trang cập nhật số lượng đánh giá theo từng mức điểm | FUNC-DG-LIST-01 | Pass | 11/15/2015 | |

---

### Function: Xem chi tiết đánh giá (Nhân viên)

#### Check GUI: `/nhanvien/reviews/[id]`

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DG-DETAIL-01** | Kiểm tra tiêu đề trang | 1. Đăng nhập Nhân viên<br>2. Truy cập `/nhanvien/reviews/[id]` | Hiển thị h1 `Chi tiết đánh giá` class text-2xl font-bold & mô tả `Thông tin chi tiết về đánh giá từ khách hàng` | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DG-DETAIL-02** | Kiểm tra nút Quay lại | 1. Ở `/nhanvien/reviews/[id]` quan sát | Hiển thị Button variant="ghost" asChild với Link href="/nhanvien/reviews", icon ArrowLeft (h-4 w-4 mr-2) và text "Quay lại danh sách" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DG-DETAIL-03** | Kiểm tra card Thông tin đánh giá | 1. Quan sát card đầu tiên | CardTitle `Thông tin đánh giá`, CardContent có grid md:grid-cols-2 với: div flex gap-4 (Image sách w-24 h-32, div có h3 tên sách, p tác giả), div space-y-2 (Label "Khách hàng" + p tên khách, Label "Điểm đánh giá" + div flex gap-1 5 icon Star, Label "Ngày đánh giá" + p thời gian, Label "Trạng thái" + Badge) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DG-DETAIL-04** | Kiểm tra card Nội dung đánh giá | 1. Quan sát card tiếp theo | CardTitle `Nội dung đánh giá`, CardContent có div space-y-2 với Label "Nhận xét" + Textarea readOnly value={review.comment} rows={6}, Label "Đã mua sách" + p "Có" hoặc "Không", Label "Đã đọc sách" + p "Có" hoặc "Không" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DG-DETAIL-05** | Kiểm tra card Thông tin đơn hàng | 1. Quan sát card tiếp theo | CardTitle `Thông tin đơn hàng`, CardContent có div space-y-2 với Label "Mã đơn hàng" + Link href="/nhanvien/orders/[orderId]" text "#ORD001", Label "Ngày mua" + p thời gian, Label "Số lượng" + p "1 cuốn" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DG-DETAIL-06** | Kiểm tra card Thao tác | 1. Quan sát card cuối | CardTitle `Thao tác`, CardContent có div flex gap-2 với Button variant="default" "Duyệt đánh giá" (nếu status Chờ duyệt), Button variant="destructive" "Ẩn đánh giá" (nếu status Đã duyệt), Button variant="outline" "Xóa đánh giá" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DG-DETAIL-07** | Kiểm tra Modal xác nhận | 1. Click nút "Duyệt" hoặc "Ẩn"<br>2. Quan sát Modal | Hiển thị Dialog với DialogTitle "Xác nhận", DialogDescription "Bạn có chắc chắn muốn [duyệt/ẩn] đánh giá này?", DialogFooter có Button variant="outline" "Hủy", Button variant="default" "Xác nhận" | FUNC-DN-02 | Pass | 11/15/2015 | |

---

#### Check FUNC: Xem chi tiết đánh giá

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DG-DETAIL-01** | Xem chi tiết đánh giá | 1. Đăng nhập<br>2. Truy cập `/nhanvien/reviews/[id]` | Trang hiển thị đầy đủ thông tin đánh giá: thông tin sách, khách hàng, điểm đánh giá, nội dung, đơn hàng như GUI tests; dữ liệu khớp với ID | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DG-DETAIL-02** | Click Quay lại danh sách | 1. Click nút `Quay lại danh sách` | Chuyển về trang `/nhanvien/reviews`, giữ nguyên bộ lọc và phân trang trước đó | FUNC-DG-DETAIL-01 | Pass | 11/15/2015 | |
| **FUNC-DG-DETAIL-03** | Duyệt đánh giá | 1. Đánh giá có status `Chờ duyệt`<br>2. Click `Duyệt đánh giá`<br>3. Xác nhận trong Modal | Hiển thị toast "Đã duyệt đánh giá thành công", Badge trạng thái chuyển sang `Đã duyệt` (variant default), nút "Duyệt" biến mất, nút "Ẩn đánh giá" xuất hiện | FUNC-DG-DETAIL-01 | Pass | 11/15/2015 | |
| **FUNC-DG-DETAIL-04** | Ẩn đánh giá | 1. Đánh giá có status `Đã duyệt`<br>2. Click `Ẩn đánh giá`<br>3. Xác nhận trong Modal | Hiển thị toast "Đã ẩn đánh giá thành công", Badge trạng thái chuyển sang `Đã ẩn` (variant secondary), nút "Ẩn" biến mất | FUNC-DG-DETAIL-01 | Pass | 11/15/2015 | |
| **FUNC-DG-DETAIL-05** | Hủy thao tác trong Modal | 1. Click nút thao tác (Duyệt/Ẩn)<br>2. Click `Hủy` trong Modal | Modal đóng, không có thay đổi nào, trạng thái đánh giá giữ nguyên | FUNC-DG-DETAIL-01 | Pass | 11/15/2015 | |
| **FUNC-DG-DETAIL-06** | Click link Mã đơn hàng | 1. Click link "#ORD001" | Chuyển đến trang `/nhanvien/orders/[orderId]` hiển thị chi tiết đơn hàng | FUNC-DG-DETAIL-01 | Pass | 11/15/2015 | |
| **FUNC-DG-DETAIL-07** | Xử lý đánh giá không tồn tại | 1. Truy cập `/nhanvien/reviews/invalid-id` | Hiển thị thông báo lỗi "Không tìm thấy đánh giá", nút "Quay lại danh sách" để quay về | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DG-DETAIL-08** | Cập nhật trạng thái real-time | 1. Duyệt/ẩn đánh giá<br>2. Quay lại danh sách | Đánh giá trong danh sách cập nhật trạng thái mới, thống kê cập nhật | FUNC-DG-DETAIL-03, FUNC-DG-DETAIL-04 | Pass | 11/15/2015 | |

---

### Function: Layout - Quản lý đánh giá (Nhân viên)

#### Check GUI: Layout tổng quan trang quản lý đánh giá

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DG-LAYOUT-01** | Kiểm tra layout tổng thể trang danh sách | 1. Đăng nhập Nhân viên<br>2. Truy cập `/nhanvien/reviews` | Trang có layout container max-w-7xl mx-auto p-6 space-y-6, header với tiêu đề và mô tả, grid md:grid-cols-4 thống kê, card Tìm kiếm & Bộ lọc, card Danh sách đánh giá với bảng, grid md:grid-cols-3 sidebar bên phải | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DG-LAYOUT-02** | Kiểm tra responsive trên mobile | 1. Thu nhỏ màn hình < 768px<br>2. Quan sát layout | Grid thống kê chuyển thành 2 cột, sidebar chuyển xuống dưới, bảng có scroll ngang, các card xếp dọc | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DG-LAYOUT-03** | Kiểm tra layout trang chi tiết | 1. Truy cập `/nhanvien/reviews/[id]` | Trang có layout container max-w-4xl mx-auto p-6 space-y-6, header với nút Quay lại, các card thông tin xếp dọc, card Thao tác ở cuối | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DG-LAYOUT-04** | Kiểm tra navigation breadcrumb | 1. Quan sát header trang | Hiển thị Breadcrumb với links: "Trang chủ" > "Quản lý đánh giá" (trang danh sách) hoặc "Trang chủ" > "Quản lý đánh giá" > "Chi tiết" (trang chi tiết) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DG-LAYOUT-05** | Kiểm tra màu sắc và theme | 1. Quan sát toàn bộ trang | Sử dụng màu sắc nhất quán với theme hệ thống, Badge có màu phù hợp với trạng thái (default cho Đã duyệt, warning cho Chờ duyệt, secondary cho Đã ẩn), icon Star màu vàng cho điểm đánh giá | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DG-LAYOUT-06** | Kiểm tra loading state | 1. Reload trang<br>2. Quan sát khi đang tải | Hiển thị Skeleton loader cho bảng, cards, sidebar trong khi đang fetch dữ liệu | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DG-LAYOUT-07** | Kiểm tra empty state | 1. Áp dụng bộ lọc không có kết quả<br>2. Quan sát | Hiển thị div flex flex-col items-center justify-center p-12 với icon Inbox (h-12 w-12 text-muted-foreground), text "Không tìm thấy đánh giá", Button "Xóa bộ lọc" | FUNC-DG-LIST-01 | Pass | 11/15/2015 | |

---

