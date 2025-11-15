# Test Case Template - Chức năng thông báo (User)

## Module Code
**Model Management Store: Chức năng thông báo User**

## Test Requirement
1. Hiển thị danh sách thông báo
2. Thông báo giảm giá
3. Cập nhật đơn hàng
4. Thông báo có hàng
5. Quản lý trạng thái thông báo

---

## Test Summary

### Người thực hiện Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 130 |
| **Fail** | 0 |
| **Untested** | 40 |
| **N/A** | 0 |
| **Number of Test cases** | 170 |

---

## Test Cases

### Function: Hiển thị danh sách thông báo

#### Check GUI: Hiển thị danh sách thông báo

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-HTDS-TB-01** | Kiểm tra tiêu đề trang | 1. Truy cập trang thông báo<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Thông báo" với icon Bell h-8 w-8, text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-HTDS-TB-02** | Kiểm tra mô tả trang | 1. Truy cập trang thông báo<br>2. Kiểm tra mô tả | Hiển thị mô tả "[Số] thông báo chưa đọc" hoặc "Tất cả thông báo đã được đọc" với text-muted-foreground | | Pass | 11/15/2015 | |
| **GUI-HTDS-TB-03** | Kiểm tra số thông báo chưa đọc | 1. Truy cập trang thông báo<br>2. Kiểm tra badge | Hiển thị số thông báo chưa đọc trong header hoặc badge, cập nhật real-time | | Pass | 11/15/2015 | |
| **GUI-HTDS-TB-04** | Kiểm tra tab loại thông báo | 1. Truy cập trang thông báo<br>2. Kiểm tra tab | Hiển thị TabsList với các tab: "Tất cả", "Đơn hàng" (icon Package), "Khuyến mãi" (icon Percent), "Yêu thích" (icon Heart), "Đánh giá" (icon Star), "Hệ thống" (icon AlertCircle), "Hỗ trợ" (icon MessageSquare), mỗi tab hiển thị số lượng | | Pass | 11/15/2015 | |
| **GUI-HTDS-TB-05** | Kiểm tra ô tìm kiếm | 1. Truy cập trang thông báo<br>2. Kiểm tra tìm kiếm | Hiển thị Input với icon Search bên trái, placeholder "Tìm kiếm thông báo...", pl-10 | | Pass | 11/15/2015 | |
| **GUI-HTDS-TB-06** | Kiểm tra bộ lọc loại | 1. Truy cập trang thông báo<br>2. Kiểm tra bộ lọc | Hiển thị Select với trigger w-40, các option: "Tất cả loại", "Đơn hàng", "Khuyến mãi", "Yêu thích", "Đánh giá", "Hệ thống", "Hỗ trợ" | | Pass | 11/15/2015 | |
| **GUI-HTDS-TB-07** | Kiểm tra bộ lọc mức độ ưu tiên | 1. Truy cập trang thông báo<br>2. Kiểm tra bộ lọc | Hiển thị Select với trigger w-40, các option: "Tất cả mức độ", "Cao", "Trung bình", "Thấp" | | Pass | 11/15/2015 | |
| **GUI-HTDS-TB-08** | Kiểm tra nút Đánh dấu tất cả đã đọc | 1. Truy cập trang thông báo<br>2. Kiểm tra nút | Hiển thị nút "Đánh dấu tất cả đã đọc" với icon CheckCheck, variant outline, chỉ hiển thị khi có thông báo chưa đọc | | Pass | 11/15/2015 | |
| **GUI-HTDS-TB-09** | Kiểm tra nút Xóa đã đọc | 1. Truy cập trang thông báo<br>2. Kiểm tra nút | Hiển thị nút "Xóa đã đọc" với icon Trash2, variant outline | | Pass | 11/15/2015 | |
| **GUI-HTDS-TB-10** | Kiểm tra card thông báo | 1. Xem danh sách thông báo<br>2. Kiểm tra card | Hiển thị card với CardContent p-6, border-primary nếu chưa đọc, chứa icon loại, tiêu đề, nội dung, badge trạng thái, badge mức độ ưu tiên, thời gian | | Pass | 11/15/2015 | |
| **GUI-HTDS-TB-11** | Kiểm tra icon loại thông báo | 1. Xem card thông báo<br>2. Kiểm tra icon | Hiển thị icon loại trong div p-2 rounded-full bg-primary/10 (chưa đọc) hoặc bg-muted (đã đọc), icon Package/Tag/Heart/Star/AlertCircle/MessageSquare tùy loại | | Pass | 11/15/2015 | |
| **GUI-HTDS-TB-12** | Kiểm tra badge trạng thái đọc | 1. Xem card thông báo<br>2. Kiểm tra badge | Hiển thị dot w-2 h-2 bg-primary rounded-full nếu chưa đọc, không hiển thị nếu đã đọc | | Pass | 11/15/2015 | |
| **GUI-HTDS-TB-13** | Kiểm tra badge mức độ ưu tiên | 1. Xem card thông báo<br>2. Kiểm tra badge | Hiển thị badge với màu: Cao (red-500), Trung bình (yellow-500), Thấp (gray-500) | | Pass | 11/15/2015 | |
| **GUI-HTDS-TB-14** | Kiểm tra nút Đánh dấu đã đọc | 1. Xem thông báo chưa đọc<br>2. Kiểm tra nút | Hiển thị nút với icon CheckCircle, variant ghost size sm, chỉ hiển thị khi chưa đọc | | Pass | 11/15/2015 | |
| **GUI-HTDS-TB-15** | Kiểm tra nút Xóa thông báo | 1. Xem card thông báo<br>2. Kiểm tra nút | Hiển thị nút với icon XCircle, variant ghost size sm, text-red-600 hover:text-red-700 | | Pass | 11/15/2015 | |
| **GUI-HTDS-TB-16** | Kiểm tra nút hành động | 1. Xem thông báo có actionUrl<br>2. Kiểm tra nút | Hiển thị nút "Xem chi tiết"/"Mua ngay"/"Theo dõi" với variant outline size sm, link đến actionUrl | | Pass | 11/15/2015 | |
| **GUI-HTDS-TB-17** | Kiểm tra phân trang | 1. Xem danh sách thông báo<br>2. Kiểm tra phân trang | Hiển thị phân trang nếu có nhiều thông báo, có thể điều hướng giữa các trang | | Pass | 11/15/2015 | |

---

### Check FUNC: Hiển thị danh sách thông báo

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-HTDS-TB-01** | Mở trang thông báo | 1. Truy cập trang thông báo từ sidebar menu | Hiển thị danh sách tất cả thông báo, có tab loại, ô tìm kiếm, bộ lọc | | Pass | 11/15/2015 | |
| **FUNC-HTDS-TB-02** | Hiển thị danh sách thông báo | 1. Truy cập trang thông báo | Hiển thị danh sách với đầy đủ thông tin: icon loại, tiêu đề, nội dung, thời gian, trạng thái đọc, mức độ ưu tiên, nút hành động (nếu có) | | Pass | 11/15/2015 | |
| **FUNC-HTDS-TB-03** | Sắp xếp theo thời gian mới nhất | 1. Truy cập trang thông báo | Danh sách được sắp xếp theo thời gian mới nhất trước | | Pass | 11/15/2015 | |
| **FUNC-HTDS-TB-04** | Tìm kiếm theo tiêu đề | 1. Truy cập trang thông báo<br>2. Nhập từ khóa vào ô tìm kiếm | Danh sách được lọc, chỉ hiển thị thông báo có tiêu đề chứa từ khóa | | Pass | 11/15/2015 | |
| **FUNC-HTDS-TB-05** | Tìm kiếm theo nội dung | 1. Truy cập trang thông báo<br>2. Nhập từ khóa vào ô tìm kiếm | Danh sách được lọc, chỉ hiển thị thông báo có nội dung chứa từ khóa | | Pass | 11/15/2015 | |
| **FUNC-HTDS-TB-06** | Lọc theo loại - Đơn hàng | 1. Chọn tab "Đơn hàng" hoặc bộ lọc loại "Đơn hàng" | Chỉ hiển thị các thông báo loại "Đơn hàng" | | Pass | 11/15/2015 | |
| **FUNC-HTDS-TB-07** | Lọc theo loại - Khuyến mãi | 1. Chọn tab "Khuyến mãi" hoặc bộ lọc loại "Khuyến mãi" | Chỉ hiển thị các thông báo loại "Khuyến mãi" | | Pass | 11/15/2015 | |
| **FUNC-HTDS-TB-08** | Lọc theo loại - Yêu thích | 1. Chọn tab "Yêu thích" hoặc bộ lọc loại "Yêu thích" | Chỉ hiển thị các thông báo loại "Yêu thích" | | Pass | 11/15/2015 | |
| **FUNC-HTDS-TB-09** | Lọc theo loại - Đánh giá | 1. Chọn tab "Đánh giá" hoặc bộ lọc loại "Đánh giá" | Chỉ hiển thị các thông báo loại "Đánh giá" | | Pass | 11/15/2015 | |
| **FUNC-HTDS-TB-10** | Lọc theo loại - Hệ thống | 1. Chọn tab "Hệ thống" hoặc bộ lọc loại "Hệ thống" | Chỉ hiển thị các thông báo loại "Hệ thống" | | Pass | 11/15/2015 | |
| **FUNC-HTDS-TB-11** | Lọc theo loại - Hỗ trợ | 1. Chọn tab "Hỗ trợ" hoặc bộ lọc loại "Hỗ trợ" | Chỉ hiển thị các thông báo loại "Hỗ trợ" | | Pass | 11/15/2015 | |
| **FUNC-HTDS-TB-12** | Lọc theo mức độ ưu tiên - Cao | 1. Chọn bộ lọc mức độ ưu tiên "Cao" | Chỉ hiển thị các thông báo có mức độ ưu tiên "Cao" | | Pass | 11/15/2015 | |
| **FUNC-HTDS-TB-13** | Lọc theo mức độ ưu tiên - Trung bình | 1. Chọn bộ lọc mức độ ưu tiên "Trung bình" | Chỉ hiển thị các thông báo có mức độ ưu tiên "Trung bình" | | Pass | 11/15/2015 | |
| **FUNC-HTDS-TB-14** | Lọc theo mức độ ưu tiên - Thấp | 1. Chọn bộ lọc mức độ ưu tiên "Thấp" | Chỉ hiển thị các thông báo có mức độ ưu tiên "Thấp" | | Pass | 11/15/2015 | |
| **FUNC-HTDS-TB-15** | Kết hợp tìm kiếm và lọc | 1. Nhập từ khóa tìm kiếm<br>2. Chọn tab loại và bộ lọc mức độ ưu tiên | Danh sách được lọc theo cả từ khóa, loại và mức độ ưu tiên, chỉ hiển thị thông báo thỏa mãn tất cả điều kiện | | Pass | 11/15/2015 | |
| **FUNC-HTDS-TB-16** | Hiển thị khi không có thông báo | 1. Chọn tab loại không có thông báo<br>2. Kiểm tra hiển thị | Hiển thị thông báo "Không có thông báo nào" với icon Bell, tiêu đề và mô tả phù hợp | | Pass | 11/15/2015 | |
| **FUNC-HTDS-TB-17** | Tìm kiếm real-time | 1. Truy cập trang thông báo<br>2. Nhập từ khóa vào ô tìm kiếm | Danh sách được lọc ngay khi nhập, không cần nhấn Enter | | Pass | 11/15/2015 | |
| **FUNC-HTDS-TB-18** | Cập nhật số lượng trong tab | 1. Xem danh sách thông báo<br>2. Kiểm tra số lượng | Số lượng thông báo được hiển thị chính xác trong mỗi tab, cập nhật khi có thay đổi | | Pass | 11/15/2015 | |

---

### Function: Thông báo giảm giá

#### Check GUI: Thông báo giảm giá

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-TBGG-01** | Kiểm tra icon khuyến mãi | 1. Xem thông báo giảm giá<br>2. Kiểm tra icon | Hiển thị icon Percent hoặc Tag trong div p-2 rounded-full, màu green-500 | | Pass | 11/15/2015 | |
| **GUI-TBGG-02** | Kiểm tra tiêu đề khuyến mãi | 1. Xem thông báo giảm giá<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề thông báo khuyến mãi với font-semibold | | Pass | 11/15/2015 | |
| **GUI-TBGG-03** | Kiểm tra nội dung khuyến mãi | 1. Xem thông báo giảm giá<br>2. Kiểm tra nội dung | Hiển thị nội dung chi tiết khuyến mãi với text-sm text-muted-foreground | | Pass | 11/15/2015 | |
| **GUI-TBGG-04** | Kiểm tra phần trăm giảm giá | 1. Xem thông báo giảm giá<br>2. Kiểm tra phần trăm | Hiển thị phần trăm giảm giá trong metadata hoặc nội dung, format rõ ràng | | Pass | 11/15/2015 | |
| **GUI-TBGG-05** | Kiểm tra thời gian áp dụng | 1. Xem thông báo giảm giá<br>2. Kiểm tra thời gian | Hiển thị thời gian bắt đầu và kết thúc khuyến mãi trong nội dung | | Pass | 11/15/2015 | |
| **GUI-TBGG-06** | Kiểm tra ngày hết hạn | 1. Xem thông báo giảm giá<br>2. Kiểm tra ngày | Hiển thị ngày hết hạn với icon AlertCircle, format ngày Việt Nam | | Pass | 11/15/2015 | |
| **GUI-TBGG-07** | Kiểm tra nút Mua ngay | 1. Xem thông báo giảm giá<br>2. Kiểm tra nút | Hiển thị nút "Mua ngay" với variant outline size sm, link đến trang sản phẩm khuyến mãi | | Pass | 11/15/2015 | |
| **GUI-TBGG-08** | Kiểm tra nút Xem chi tiết | 1. Xem thông báo giảm giá<br>2. Kiểm tra nút | Hiển thị nút "Xem chi tiết" với variant outline size sm, link đến trang chi tiết khuyến mãi | | Pass | 11/15/2015 | |

---

### Check FUNC: Thông báo giảm giá

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TBGG-01** | Hiển thị thông báo khuyến mãi | 1. Chọn tab "Khuyến mãi"<br>2. Xem thông báo | Hiển thị thông báo khuyến mãi với đầy đủ thông tin: phần trăm giảm giá, thời gian áp dụng, danh sách sản phẩm (nếu có), ngày hết hạn | | Pass | 11/15/2015 | |
| **FUNC-TBGG-02** | Truy cập sản phẩm khuyến mãi | 1. Xem thông báo giảm giá<br>2. Nhấn nút "Mua ngay" | Chuyển hướng đến trang sản phẩm hoặc danh mục sản phẩm được áp dụng khuyến mãi, trang hiển thị đầy đủ thông tin khuyến mãi | | Pass | 11/15/2015 | |
| **FUNC-TBGG-03** | Xem chi tiết khuyến mãi | 1. Xem thông báo giảm giá<br>2. Nhấn nút "Xem chi tiết" | Chuyển hướng đến trang chi tiết khuyến mãi với đầy đủ thông tin: điều kiện, sản phẩm áp dụng, thời gian | | Pass | 11/15/2015 | |
| **FUNC-TBGG-04** | Theo dõi thời gian khuyến mãi | 1. Xem thông báo giảm giá<br>2. Kiểm tra thời gian | Hiển thị thời gian còn lại của khuyến mãi, cập nhật real-time, cảnh báo khi sắp hết hạn | | Pass | 11/15/2015 | |
| **FUNC-TBGG-05** | Hiển thị danh sách sản phẩm áp dụng | 1. Xem thông báo giảm giá có danh sách sản phẩm<br>2. Kiểm tra danh sách | Hiển thị danh sách sản phẩm được áp dụng khuyến mãi, có thể click để xem chi tiết | | Pass | 11/15/2015 | |

---

### Function: Cập nhật đơn hàng

#### Check GUI: Cập nhật đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CNDH-01** | Kiểm tra icon đơn hàng | 1. Xem thông báo cập nhật đơn hàng<br>2. Kiểm tra icon | Hiển thị icon Package trong div p-2 rounded-full, màu blue-500 | | Pass | 11/15/2015 | |
| **GUI-CNDH-02** | Kiểm tra tiêu đề cập nhật | 1. Xem thông báo cập nhật đơn hàng<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề thông báo đơn hàng với font-semibold, ví dụ "Đơn hàng đã được xác nhận" | | Pass | 11/15/2015 | |
| **GUI-CNDH-03** | Kiểm tra nội dung cập nhật | 1. Xem thông báo cập nhật đơn hàng<br>2. Kiểm tra nội dung | Hiển thị nội dung chi tiết cập nhật với mã đơn hàng, trạng thái mới | | Pass | 11/15/2015 | |
| **GUI-CNDH-04** | Kiểm tra mã đơn hàng | 1. Xem thông báo cập nhật đơn hàng<br>2. Kiểm tra mã | Hiển thị mã đơn hàng trong nội dung hoặc metadata, format rõ ràng | | Pass | 11/15/2015 | |
| **GUI-CNDH-05** | Kiểm tra badge trạng thái mới | 1. Xem thông báo cập nhật đơn hàng<br>2. Kiểm tra badge | Hiển thị badge trạng thái mới: "Xác nhận" (blue), "Đang giao" (orange), "Đã giao" (green) | | Pass | 11/15/2015 | |
| **GUI-CNDH-06** | Kiểm tra thời gian cập nhật | 1. Xem thông báo cập nhật đơn hàng<br>2. Kiểm tra thời gian | Hiển thị thời gian cập nhật trạng thái với icon Calendar, format ngày giờ Việt Nam | | Pass | 11/15/2015 | |
| **GUI-CNDH-07** | Kiểm tra nút Xem chi tiết đơn hàng | 1. Xem thông báo cập nhật đơn hàng<br>2. Kiểm tra nút | Hiển thị nút "Xem chi tiết" hoặc "Theo dõi" với variant outline size sm, link đến trang chi tiết đơn hàng | | Pass | 11/15/2015 | |

---

### Check FUNC: Cập nhật đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CNDH-01** | Hiển thị cập nhật đơn hàng | 1. Chọn tab "Đơn hàng"<br>2. Xem thông báo | Hiển thị thông báo cập nhật trạng thái đơn hàng với đầy đủ thông tin: mã đơn hàng, trạng thái mới, thời gian cập nhật, thông tin giao hàng (nếu có), dự kiến nhận hàng (nếu có) | | Pass | 11/15/2015 | |
| **FUNC-CNDH-02** | Truy cập chi tiết đơn hàng | 1. Xem thông báo cập nhật đơn hàng<br>2. Nhấn nút "Xem chi tiết" | Chuyển hướng đến trang chi tiết đơn hàng, trang hiển thị đầy đủ thông tin cập nhật | | Pass | 11/15/2015 | |
| **FUNC-CNDH-03** | Theo dõi đơn hàng | 1. Xem thông báo cập nhật đơn hàng<br>2. Nhấn nút "Theo dõi" | Chuyển hướng đến trang theo dõi đơn hàng với thông tin tiến độ giao hàng | | Pass | 11/15/2015 | |
| **FUNC-CNDH-04** | Theo dõi tiến độ giao hàng | 1. Xem thông báo đơn hàng đang giao<br>2. Kiểm tra thông tin | Hiển thị thông tin chi tiết về tiến độ giao hàng: vị trí hiện tại, thời gian dự kiến nhận hàng, thông tin liên hệ shipper, cập nhật real-time | | Pass | 11/15/2015 | |
| **FUNC-CNDH-05** | Thông báo đơn hàng đã giao | 1. Xem thông báo đơn hàng đã giao<br>2. Kiểm tra thông tin | Hiển thị thông báo "Đơn hàng đã giao" với thông tin: mã đơn hàng, thời gian giao, có thể đánh giá sản phẩm | | Pass | 11/15/2015 | |

---

### Function: Thông báo có hàng

#### Check GUI: Thông báo có hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-TBCH-01** | Kiểm tra icon có hàng | 1. Xem thông báo có hàng<br>2. Kiểm tra icon | Hiển thị icon Package hoặc Heart trong div p-2 rounded-full, màu red-500 (yêu thích) hoặc blue-500 (đặt trước) | | Pass | 11/15/2015 | |
| **GUI-TBCH-02** | Kiểm tra tiêu đề có hàng | 1. Xem thông báo có hàng<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề thông báo có hàng với font-semibold, ví dụ "Sản phẩm yêu thích đã có hàng" | | Pass | 11/15/2015 | |
| **GUI-TBCH-03** | Kiểm tra nội dung có hàng | 1. Xem thông báo có hàng<br>2. Kiểm tra nội dung | Hiển thị nội dung chi tiết có hàng với tên sản phẩm, loại thông báo | | Pass | 11/15/2015 | |
| **GUI-TBCH-04** | Kiểm tra tên sản phẩm | 1. Xem thông báo có hàng<br>2. Kiểm tra tên | Hiển thị tên sản phẩm trong nội dung hoặc metadata, format rõ ràng | | Pass | 11/15/2015 | |
| **GUI-TBCH-05** | Kiểm tra badge loại thông báo | 1. Xem thông báo có hàng<br>2. Kiểm tra badge | Hiển thị badge loại: "Đặt trước", "Yêu cầu", "Yêu thích" | | Pass | 11/15/2015 | |
| **GUI-TBCH-06** | Kiểm tra số lượng có sẵn | 1. Xem thông báo có hàng<br>2. Kiểm tra số lượng | Hiển thị số lượng sản phẩm có sẵn trong nội dung | | Pass | 11/15/2015 | |
| **GUI-TBCH-07** | Kiểm tra giá sản phẩm | 1. Xem thông báo có hàng<br>2. Kiểm tra giá | Hiển thị giá hiện tại của sản phẩm trong nội dung | | Pass | 11/15/2015 | |
| **GUI-TBCH-08** | Kiểm tra thời gian có hàng | 1. Xem thông báo có hàng<br>2. Kiểm tra thời gian | Hiển thị thời gian sản phẩm có hàng trở lại với icon Calendar, format ngày giờ Việt Nam | | Pass | 11/15/2015 | |
| **GUI-TBCH-09** | Kiểm tra nút Mua ngay | 1. Xem thông báo có hàng<br>2. Kiểm tra nút | Hiển thị nút "Mua ngay" với variant outline size sm, link đến trang sản phẩm | | Pass | 11/15/2015 | |
| **GUI-TBCH-10** | Kiểm tra nút Xem sản phẩm | 1. Xem thông báo có hàng<br>2. Kiểm tra nút | Hiển thị nút "Xem sản phẩm" với variant outline size sm, link đến trang chi tiết sản phẩm | | Pass | 11/15/2015 | |

---

### Check FUNC: Thông báo có hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TBCH-01** | Hiển thị thông báo có hàng | 1. Chọn tab "Yêu thích" hoặc "Hệ thống"<br>2. Xem thông báo | Hiển thị thông báo có hàng với đầy đủ thông tin: tên sản phẩm, loại thông báo, số lượng có sẵn, giá sản phẩm, thời gian có hàng | | Pass | 11/15/2015 | |
| **FUNC-TBCH-02** | Truy cập sản phẩm có hàng | 1. Xem thông báo có hàng<br>2. Nhấn nút "Mua ngay" hoặc "Xem sản phẩm" | Chuyển hướng đến trang sản phẩm, trang hiển thị đầy đủ thông tin và trạng thái "Có hàng" | | Pass | 11/15/2015 | |
| **FUNC-TBCH-03** | Cập nhật trạng thái sản phẩm | 1. Sản phẩm được nhập về<br>2. Kiểm tra thông báo | Trạng thái sản phẩm được cập nhật từ "Hết hàng" hoặc "Đặt trước" thành "Có hàng", thông báo được gửi đến tất cả người dùng quan tâm qua kênh đã chọn (push, email, SMS) | | Pass | 11/15/2015 | |
| **FUNC-TBCH-04** | Gửi thông báo qua kênh đã chọn | 1. Người dùng đã cài đặt kênh nhận thông báo<br>2. Sản phẩm có hàng | Thông báo được gửi qua kênh đã chọn (push notification, email, hoặc SMS), người dùng nhận được thông báo kịp thời | | Pass | 11/15/2015 | |
| **FUNC-TBCH-05** | Thông báo sản phẩm đặt trước có hàng | 1. Xem thông báo sản phẩm đặt trước có hàng<br>2. Kiểm tra thông tin | Hiển thị thông báo với loại "Đặt trước", thông tin sản phẩm, có thể mua ngay hoặc hoàn tất đơn đặt trước | | Pass | 11/15/2015 | |

---

### Function: Quản lý trạng thái thông báo

#### Check GUI: Quản lý trạng thái thông báo

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-QLTT-TB-01** | Kiểm tra số thông báo chưa đọc | 1. Truy cập trang thông báo<br>2. Kiểm tra badge | Hiển thị số lượng thông báo chưa đọc trong header, cập nhật real-time | | Pass | 11/15/2015 | |
| **GUI-QLTT-TB-02** | Kiểm tra nút Đánh dấu tất cả đã đọc | 1. Truy cập trang thông báo<br>2. Kiểm tra nút | Hiển thị nút "Đánh dấu tất cả đã đọc" với icon CheckCheck, variant outline, chỉ hiển thị khi có thông báo chưa đọc | | Pass | 11/15/2015 | |
| **GUI-QLTT-TB-03** | Kiểm tra nút Xóa tất cả | 1. Truy cập trang thông báo<br>2. Kiểm tra nút | Hiển thị nút "Xóa tất cả" hoặc "Xóa đã đọc" với icon Trash2, variant outline | | Pass | 11/15/2015 | |
| **GUI-QLTT-TB-04** | Kiểm tra nút Đánh dấu đã đọc | 1. Xem thông báo chưa đọc<br>2. Kiểm tra nút | Hiển thị nút với icon CheckCircle, variant ghost size sm, chỉ hiển thị khi chưa đọc | | Pass | 11/15/2015 | |
| **GUI-QLTT-TB-05** | Kiểm tra badge trạng thái đọc | 1. Xem card thông báo<br>2. Kiểm tra badge | Hiển thị dot w-2 h-2 bg-primary rounded-full nếu chưa đọc, không hiển thị nếu đã đọc, card có border-primary nếu chưa đọc | | Pass | 11/15/2015 | |

---

### Check FUNC: Quản lý trạng thái thông báo

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-QLTT-TB-01** | Đánh dấu thông báo đã đọc | 1. Xem thông báo chưa đọc<br>2. Nhấn nút "Đánh dấu đã đọc" | Trạng thái thông báo được cập nhật thành "Đã đọc", dot biến mất, border-primary biến mất, số lượng thông báo chưa đọc giảm, hiển thị toast "Đã đánh dấu là đã đọc" | | Pass | 11/15/2015 | |
| **FUNC-QLTT-TB-02** | Đánh dấu tất cả đã đọc | 1. Truy cập trang thông báo<br>2. Nhấn nút "Đánh dấu tất cả đã đọc" | Tất cả thông báo chưa đọc được đánh dấu là đã đọc, số lượng thông báo chưa đọc về 0, hiển thị toast "Đã đánh dấu tất cả thông báo là đã đọc" | | Pass | 11/15/2015 | |
| **FUNC-QLTT-TB-03** | Xóa thông báo | 1. Xem thông báo<br>2. Nhấn nút "Xóa" | Thông báo được xóa khỏi danh sách, danh sách được cập nhật, hiển thị toast "Đã xóa thông báo" | | Pass | 11/15/2015 | |
| **FUNC-QLTT-TB-04** | Xóa tất cả thông báo đã đọc | 1. Truy cập trang thông báo<br>2. Nhấn nút "Xóa đã đọc" | Tất cả thông báo đã đọc được xóa, chỉ còn lại thông báo chưa đọc, danh sách được cập nhật, hiển thị toast "Đã xóa tất cả thông báo đã đọc" | | Pass | 11/15/2015 | |
| **FUNC-QLTT-TB-05** | Cập nhật số lượng thông báo | 1. Có thông báo mới hoặc thay đổi trạng thái<br>2. Kiểm tra số lượng | Số lượng thông báo chưa đọc được cập nhật chính xác và hiển thị real-time, badge số lượng được cập nhật kịp thời | | Pass | 11/15/2015 | |
| **FUNC-QLTT-TB-06** | Tự động đánh dấu đã đọc khi xem | 1. Xem chi tiết thông báo<br>2. Kiểm tra trạng thái | Thông báo được tự động đánh dấu là đã đọc khi người dùng xem chi tiết (tùy cài đặt) | | Pass | 11/15/2015 | |
| **FUNC-QLTT-TB-07** | Cập nhật real-time khi có thông báo mới | 1. Đang ở trang thông báo<br>2. Có thông báo mới | Thông báo mới xuất hiện trong danh sách real-time, số lượng chưa đọc tăng, có thể có notification popup | | Pass | 11/15/2015 | |

---

### Check VALIDATION: Thông báo

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **VALID-TB-01** | Tìm kiếm với từ khóa đặc biệt | 1. Truy cập trang thông báo<br>2. Nhập từ khóa có ký tự đặc biệt | Hệ thống xử lý an toàn, không gây lỗi, lọc kết quả chính xác | | Pass | 11/15/2015 | |
| **VALID-TB-02** | Xóa thông báo không tồn tại | 1. Thử xóa thông báo đã bị xóa<br>2. Kiểm tra lỗi | Hệ thống xử lý an toàn, không gây lỗi, hiển thị thông báo phù hợp | | Pass | 11/15/2015 | |
| **VALID-TB-03** | Đánh dấu đã đọc thông báo đã đọc | 1. Xem thông báo đã đọc<br>2. Thử đánh dấu lại | Hệ thống xử lý an toàn, không gây lỗi, trạng thái không thay đổi | | Pass | 11/15/2015 | |
| **VALID-TB-04** | Hiển thị thông báo với nội dung dài | 1. Xem thông báo có nội dung rất dài<br>2. Kiểm tra hiển thị | Nội dung được hiển thị đầy đủ hoặc được cắt với "Xem thêm", không bị lỗi layout | | Pass | 11/15/2015 | |
| **VALID-TB-05** | Phân trang với số lượng lớn | 1. Có nhiều thông báo (>100)<br>2. Kiểm tra phân trang | Phân trang hoạt động chính xác, có thể điều hướng giữa các trang, hiển thị số trang chính xác | | Pass | 11/15/2015 | |

