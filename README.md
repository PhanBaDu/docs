# Test Case Template - Thông báo (Admin)

## Module Code
**Model Management Store: Thông báo Admin**

## Test Requirement
1. Quản lý thông báo

---

## Test Summary

### Người thực hiện Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 23 |
| **Fail** | 0 |
| **Untested** | 21 |
| **N/A** | 0 |
| **Number of Test cases** | 44 |

---

## Test Cases

### Function: Quản lý thông báo

#### Check GUI: Quản lý thông báo

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-QLTB-01** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/notifications<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Quản lý thông báo" với kích thước text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-QLTB-02** | Kiểm tra mô tả chức năng | 1. Truy cập /admin/notifications<br>2. Kiểm tra mô tả | Hiển thị mô tả "Quản lý và xem tất cả thông báo hệ thống" màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-QLTB-03** | Kiểm tra Input Tìm kiếm | 1. Truy cập /admin/notifications<br>2. Kiểm tra Input | Hiển thị Input "Tìm kiếm" với placeholder "Tìm kiếm thông báo...", có icon Search | | Pass | 11/15/2015 | |
| **GUI-QLTB-04** | Kiểm tra Select Lọc loại | 1. Truy cập /admin/notifications<br>2. Kiểm tra Select | Hiển thị Select "Loại" với placeholder "Tất cả loại", có các option: Tất cả, Đơn hàng, Khuyến mãi, Yêu thích, Đánh giá, Hệ thống, Hỗ trợ | | Pass | 11/15/2015 | |
| **GUI-QLTB-05** | Kiểm tra Select Lọc mức độ ưu tiên | 1. Truy cập /admin/notifications<br>2. Kiểm tra Select | Hiển thị Select "Mức độ ưu tiên" với placeholder "Tất cả mức độ", có các option: Tất cả, Cao, Trung bình, Thấp | | Pass | 11/15/2015 | |
| **GUI-QLTB-06** | Kiểm tra Select Lọc trạng thái | 1. Truy cập /admin/notifications<br>2. Kiểm tra Select | Hiển thị Select "Trạng thái" với placeholder "Tất cả trạng thái", có các option: Tất cả, Chưa đọc, Đã đọc | | Pass | 11/15/2015 | |
| **GUI-QLTB-07** | Kiểm tra nút Đánh dấu tất cả đã đọc | 1. Truy cập /admin/notifications<br>2. Kiểm tra nút | Hiển thị nút "Đánh dấu tất cả đã đọc" với icon CheckCircle | | Pass | 11/15/2015 | |
| **GUI-QLTB-08** | Kiểm tra nút Xóa tất cả | 1. Truy cập /admin/notifications<br>2. Kiểm tra nút | Hiển thị nút "Xóa tất cả" với icon Trash2, màu destructive | | Pass | 11/15/2015 | |
| **GUI-QLTB-09** | Kiểm tra Card thông báo | 1. Truy cập /admin/notifications<br>2. Kiểm tra Card | Mỗi thông báo hiển thị trong Card với: Icon loại thông báo, Tiêu đề, Nội dung, Thời gian, Badge mức độ ưu tiên, Badge trạng thái, nút Đánh dấu đã đọc, nút Xóa | | Pass | 11/15/2015 | |
| **GUI-QLTB-10** | Kiểm tra Icon loại thông báo | 1. Truy cập /admin/notifications<br>2. Kiểm tra Icon | Mỗi loại thông báo có icon tương ứng: Package (Đơn hàng), Tag (Khuyến mãi), Heart (Yêu thích), Star (Đánh giá), Settings (Hệ thống), MessageSquare (Hỗ trợ) | | Pass | 11/15/2015 | |
| **GUI-QLTB-11** | Kiểm tra Badge mức độ ưu tiên | 1. Truy cập /admin/notifications<br>2. Kiểm tra Badge | Badge mức độ ưu tiên: "Cao" màu red, "Trung bình" màu yellow, "Thấp" màu green | | Pass | 11/15/2015 | |
| **GUI-QLTB-12** | Kiểm tra Badge trạng thái | 1. Truy cập /admin/notifications<br>2. Kiểm tra Badge | Badge trạng thái: "Chưa đọc" màu blue, "Đã đọc" màu gray | | Pass | 11/15/2015 | |
| **GUI-QLTB-13** | Kiểm tra nút Đánh dấu đã đọc | 1. Truy cập /admin/notifications<br>2. Kiểm tra nút | Mỗi thông báo chưa đọc có nút "Đánh dấu đã đọc" với icon CheckCircle | | Pass | 11/15/2015 | |
| **GUI-QLTB-14** | Kiểm tra nút Xóa thông báo | 1. Truy cập /admin/notifications<br>2. Kiểm tra nút | Mỗi thông báo có nút "Xóa" với icon Trash2, màu destructive | | Pass | 11/15/2015 | |
| **GUI-QLTB-15** | Kiểm tra Pagination | 1. Truy cập /admin/notifications<br>2. Kiểm tra Pagination | Hiển thị Pagination với nút Previous, Next, số trang, số thông báo mỗi trang | | Pass | 11/15/2015 | |
| **GUI-QLTB-16** | Kiểm tra hiển thị khi không có thông báo | 1. Truy cập /admin/notifications<br>2. Không có thông báo | Hiển thị thông báo "Không có thông báo nào" với icon Bell, text-center | | Pass | 11/15/2015 | |

---

### Check FUNC: Quản lý thông báo

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-QLTB-01** | Mở trang quản lý thông báo | 1. Truy cập /admin/notifications | Hiển thị danh sách thông báo với đầy đủ thông tin: tiêu đề, nội dung, thời gian, loại, mức độ ưu tiên, trạng thái, các bộ lọc và tìm kiếm | | Pass | 11/15/2015 | |
| **FUNC-QLTB-02** | Hiển thị danh sách khi có dữ liệu | 1. Truy cập /admin/notifications<br>2. Có dữ liệu thông báo | Hiển thị danh sách thông báo trong các Card, mỗi Card hiển thị đầy đủ thông tin | | Pass | 11/15/2015 | |
| **FUNC-QLTB-03** | Hiển thị khi không có dữ liệu | 1. Truy cập /admin/notifications<br>2. Không có dữ liệu thông báo | Hiển thị thông báo "Không có thông báo nào", không có Card nào được hiển thị | | Pass | 11/15/2015 | |
| **FUNC-QLTB-04** | Tìm kiếm thông báo theo tiêu đề | 1. Truy cập /admin/notifications<br>2. Nhập từ khóa vào ô tìm kiếm<br>3. Nhấn Enter hoặc click icon Search | Danh sách thông báo được cập nhật, chỉ hiển thị các thông báo có tiêu đề chứa từ khóa | | Pass | 11/15/2015 | |
| **FUNC-QLTB-05** | Tìm kiếm thông báo theo nội dung | 1. Truy cập /admin/notifications<br>2. Nhập từ khóa vào ô tìm kiếm<br>3. Nhấn Enter | Danh sách thông báo được cập nhật, chỉ hiển thị các thông báo có nội dung chứa từ khóa | | Pass | 11/15/2015 | |
| **FUNC-QLTB-06** | Lọc theo loại thông báo | 1. Truy cập /admin/notifications<br>2. Chọn "Đơn hàng" từ Select "Loại" | Danh sách thông báo được cập nhật, chỉ hiển thị các thông báo loại "Đơn hàng" | | Pass | 11/15/2015 | |
| **FUNC-QLTB-07** | Lọc theo mức độ ưu tiên | 1. Truy cập /admin/notifications<br>2. Chọn "Cao" từ Select "Mức độ ưu tiên" | Danh sách thông báo được cập nhật, chỉ hiển thị các thông báo có mức độ ưu tiên "Cao" | | Pass | 11/15/2015 | |
| **FUNC-QLTB-08** | Lọc theo trạng thái | 1. Truy cập /admin/notifications<br>2. Chọn "Chưa đọc" từ Select "Trạng thái" | Danh sách thông báo được cập nhật, chỉ hiển thị các thông báo chưa đọc | | Pass | 11/15/2015 | |
| **FUNC-QLTB-09** | Kết hợp nhiều bộ lọc | 1. Truy cập /admin/notifications<br>2. Chọn loại, mức độ ưu tiên, trạng thái<br>3. Nhập từ khóa tìm kiếm | Danh sách thông báo được cập nhật theo tất cả các tiêu chí đã chọn | | Pass | 11/15/2015 | |
| **FUNC-QLTB-10** | Đánh dấu đã đọc một thông báo | 1. Truy cập /admin/notifications<br>2. Click "Đánh dấu đã đọc" trên một thông báo | Hiển thị thông báo "Đã đánh dấu là đã đọc", Badge trạng thái chuyển từ "Chưa đọc" sang "Đã đọc", nút "Đánh dấu đã đọc" biến mất | | Untested | 11/15/2015 | |
| **FUNC-QLTB-11** | Đánh dấu tất cả đã đọc | 1. Truy cập /admin/notifications<br>2. Có thông báo chưa đọc<br>3. Click "Đánh dấu tất cả đã đọc" | Hiển thị thông báo "Đã đánh dấu tất cả là đã đọc", tất cả thông báo chuyển sang trạng thái "Đã đọc", các nút "Đánh dấu đã đọc" biến mất | | Untested | 11/15/2015 | |
| **FUNC-QLTB-12** | Xóa một thông báo | 1. Truy cập /admin/notifications<br>2. Click "Xóa" trên một thông báo<br>3. Xác nhận xóa trong Modal (nếu có) | Hiển thị thông báo "Đã xóa thông báo", thông báo bị xóa khỏi danh sách | | Untested | 11/15/2015 | |
| **FUNC-QLTB-13** | Xóa tất cả thông báo | 1. Truy cập /admin/notifications<br>2. Có thông báo<br>3. Click "Xóa tất cả"<br>4. Xác nhận xóa trong Modal | Hiển thị thông báo "Đã xóa tất cả thông báo", tất cả thông báo bị xóa, hiển thị "Không có thông báo nào" | | Untested | 11/15/2015 | |
| **FUNC-QLTB-14** | Hủy xóa tất cả | 1. Truy cập /admin/notifications<br>2. Click "Xóa tất cả"<br>3. Click "Hủy" trong Modal | Modal đóng, không có thông báo nào bị xóa | | Pass | 11/15/2015 | |
| **FUNC-QLTB-15** | Click vào thông báo để xem chi tiết | 1. Truy cập /admin/notifications<br>2. Click vào một thông báo có actionUrl | Chuyển đến trang chi tiết tương ứng (nếu có actionUrl), thông báo được đánh dấu đã đọc | | Pass | 11/15/2015 | |
| **FUNC-QLTB-16** | Click vào thông báo không có actionUrl | 1. Truy cập /admin/notifications<br>2. Click vào một thông báo không có actionUrl | Thông báo được đánh dấu đã đọc, không chuyển trang | | Pass | 11/15/2015 | |
| **FUNC-QLTB-17** | Tìm kiếm không có kết quả | 1. Truy cập /admin/notifications<br>2. Nhập từ khóa không tồn tại<br>3. Nhấn Enter | Hiển thị thông báo "Không tìm thấy thông báo nào", không có Card nào được hiển thị | | Pass | 11/15/2015 | |
| **FUNC-QLTB-18** | Lọc không có kết quả | 1. Truy cập /admin/notifications<br>2. Chọn bộ lọc không có dữ liệu tương ứng | Hiển thị thông báo "Không có thông báo nào phù hợp", không có Card nào được hiển thị | | Pass | 11/15/2015 | |
| **FUNC-QLTB-19** | Pagination - Chuyển trang | 1. Truy cập /admin/notifications<br>2. Có nhiều trang<br>3. Click "Next" hoặc số trang | Danh sách thông báo được cập nhật, hiển thị thông báo của trang đã chọn | | Pass | 11/15/2015 | |
| **FUNC-QLTB-20** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/notifications<br>2. Tắt kết nối mạng<br>3. Thực hiện thao tác (đánh dấu đã đọc, xóa) | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", thao tác không được thực hiện | | Untested | 11/15/2015 | |
| **FUNC-QLTB-21** | Xử lý khi server lỗi | 1. Truy cập /admin/notifications<br>2. Server trả về lỗi 500<br>3. Thực hiện thao tác | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau", thao tác không được thực hiện | | Untested | 11/15/2015 | |

---

### Function: Layout - Thông báo

#### Check GUI: Layout - Thông báo

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-LAYOUT-TB-01** | Kiểm tra Header | 1. Truy cập /admin/notifications<br>2. Kiểm tra Header | Hiển thị Header với logo, menu navigation, thông tin admin, icon thông báo với Badge số lượng chưa đọc | | Pass | 11/15/2015 | |
| **GUI-LAYOUT-TB-02** | Kiểm tra Sidebar | 1. Truy cập /admin/notifications<br>2. Kiểm tra Sidebar | Hiển thị Sidebar với menu Admin, có item "Quản lý thông báo" được highlight | | Pass | 11/15/2015 | |
| **GUI-LAYOUT-TB-03** | Kiểm tra Breadcrumb | 1. Truy cập /admin/notifications<br>2. Kiểm tra Breadcrumb | Hiển thị Breadcrumb: Trang chủ > Quản lý thông báo | | Pass | 11/15/2015 | |
| **GUI-LAYOUT-TB-04** | Kiểm tra Footer | 1. Truy cập /admin/notifications<br>2. Kiểm tra Footer | Hiển thị Footer với thông tin copyright, liên kết | | Pass | 11/15/2015 | |
| **GUI-LAYOUT-TB-05** | Kiểm tra Badge số lượng chưa đọc trong Header | 1. Truy cập /admin/notifications<br>2. Có thông báo chưa đọc<br>3. Kiểm tra Badge | Hiển thị Badge số lượng thông báo chưa đọc trên icon Bell trong Header, màu red | | Pass | 11/15/2015 | |
| **GUI-LAYOUT-TB-06** | Kiểm tra Responsive trên mobile | 1. Truy cập /admin/notifications trên mobile<br>2. Kiểm tra layout | Layout hiển thị đúng trên mobile, Sidebar có thể thu gọn, Card thông báo hiển thị đầy đủ | | Pass | 11/15/2015 | |
| **GUI-LAYOUT-TB-07** | Kiểm tra Responsive trên tablet | 1. Truy cập /admin/notifications trên tablet<br>2. Kiểm tra layout | Layout hiển thị đúng trên tablet, các thành phần được sắp xếp hợp lý | | Pass | 11/15/2015 | |

---

**Người tạo:** Testing Team  
**Ngày cập nhật:** 11/15/2015  
**Phiên bản:** 1.0

