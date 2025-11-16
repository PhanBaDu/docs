# Test Case Template - Báo cáo và thống kê (Admin)

## Module Code
**Model Management Store: Báo cáo và thống kê Admin**

## Test Requirement
1. Xem báo cáo doanh thu
2. Xem báo cáo chi phí
3. Xem báo cáo lợi nhuận
4. Xem sản phẩm bán chạy
5. Xem thống kê khách hàng
6. Xem báo cáo tồn kho
7. Tạo báo cáo tùy chỉnh

---

## Test Summary

### Người thực hiện Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 57 |
| **Fail** | 0 |
| **Untested** | 55 |
| **N/A** | 0 |
| **Number of Test cases** | 112 |

---

## Test Cases

### Function: Xem báo cáo doanh thu

#### Check GUI: Xem báo cáo doanh thu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-BCDT-01** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/reports/revenue<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Báo cáo doanh thu" với kích thước text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-BCDT-02** | Kiểm tra mô tả chức năng | 1. Truy cập /admin/reports/revenue<br>2. Kiểm tra mô tả | Hiển thị mô tả "Theo dõi doanh thu theo ngày/tháng/năm" màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-BCDT-03** | Kiểm tra Select Bộ lọc thời gian | 1. Truy cập /admin/reports/revenue<br>2. Kiểm tra Select | Hiển thị Select với placeholder "Khoảng thời gian", có các option: Hôm nay, Tuần này, Tháng này, Năm nay, Tùy chỉnh | | Pass | 11/15/2015 | |
| **GUI-BCDT-04** | Kiểm tra Date Range (khi chọn Tùy chỉnh) | 1. Truy cập /admin/reports/revenue<br>2. Chọn "Tùy chỉnh"<br>3. Kiểm tra Date Range | Hiển thị 2 input date với text "đến" ở giữa | | Pass | 11/15/2015 | |
| **GUI-BCDT-05** | Kiểm tra Select Bộ lọc kênh | 1. Truy cập /admin/reports/revenue<br>2. Kiểm tra Select | Hiển thị Select với placeholder "Kênh thanh toán", có các option: Tất cả, COD, Banking, E-wallet | | Pass | 11/15/2015 | |
| **GUI-BCDT-06** | Kiểm tra Card Tổng doanh thu | 1. Truy cập /admin/reports/revenue<br>2. Kiểm tra Card | Hiển thị Card "Tổng doanh thu" với số tiền VNĐ (text-3xl font-bold), icon DollarSign | | Pass | 11/15/2015 | |
| **GUI-BCDT-07** | Kiểm tra Chart Biểu đồ doanh thu | 1. Truy cập /admin/reports/revenue<br>2. Kiểm tra Chart | Hiển thị Chart Line/Bar "Biểu đồ doanh thu" với trục X (thời gian), trục Y (số tiền), có thể zoom, hover để xem chi tiết | | Pass | 11/15/2015 | |
| **GUI-BCDT-08** | Kiểm tra Table Bảng chi tiết | 1. Truy cập /admin/reports/revenue<br>2. Kiểm tra Table | Hiển thị Table với các cột: Ngày, Số đơn, Doanh thu, Trung bình đơn, Tỷ lệ hoàn | | Pass | 11/15/2015 | |
| **GUI-BCDT-09** | Kiểm tra nút Export | 1. Truy cập /admin/reports/revenue<br>2. Kiểm tra nút | Hiển thị nút "Export" với icon Download variant outline | | Pass | 11/15/2015 | |

---

### Check FUNC: Xem báo cáo doanh thu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-BCDT-01** | Mở trang báo cáo doanh thu | 1. Truy cập /admin/reports/revenue | Hiển thị trang với tiêu đề, mô tả, Select Bộ lọc thời gian, Select Bộ lọc kênh, Card Tổng doanh thu, Chart Biểu đồ doanh thu, Table Bảng chi tiết, nút Export | | Pass | 11/15/2015 | |
| **FUNC-BCDT-02** | Hiển thị báo cáo doanh thu mặc định | 1. Truy cập /admin/reports/revenue | Hiển thị báo cáo doanh thu theo khoảng thời gian mặc định (VD: Tháng này), số liệu chính xác, biểu đồ trực quan, bảng chi tiết đầy đủ | | Pass | 11/15/2015 | |
| **FUNC-BCDT-03** | Lọc theo thời gian - Hôm nay | 1. Truy cập /admin/reports/revenue<br>2. Chọn "Hôm nay" | Hiển thị báo cáo doanh thu của ngày hôm nay, Card Tổng doanh thu, Chart, Table được cập nhật | | Untested | 11/15/2015 | |
| **FUNC-BCDT-04** | Lọc theo thời gian - Tùy chỉnh | 1. Truy cập /admin/reports/revenue<br>2. Chọn "Tùy chỉnh"<br>3. Chọn khoảng ngày<br>4. Click "Áp dụng" | Hiển thị báo cáo doanh thu trong khoảng ngày đã chọn, Card, Chart, Table được cập nhật | | Untested | 11/15/2015 | |
| **FUNC-BCDT-05** | Lọc theo kênh thanh toán | 1. Truy cập /admin/reports/revenue<br>2. Chọn kênh thanh toán (VD: COD)<br>3. Kiểm tra báo cáo | Hiển thị báo cáo doanh thu theo kênh đã chọn, Card, Chart, Table được cập nhật | | Untested | 11/15/2015 | |
| **FUNC-BCDT-06** | Export báo cáo doanh thu | 1. Truy cập /admin/reports/revenue<br>2. Click nút "Export"<br>3. Chọn định dạng (CSV/XLSX/PDF) | Tải về file báo cáo doanh thu với đầy đủ dữ liệu, file có định dạng đúng | | Untested | 11/15/2015 | |
| **FUNC-BCDT-07** | Xử lý khi không có dữ liệu | 1. Truy cập /admin/reports/revenue<br>2. Chọn khoảng thời gian không có dữ liệu | Hiển thị thông báo "Không có dữ liệu trong khoảng thời gian đã chọn", Chart và Table trống | | Untested | 11/15/2015 | |
| **FUNC-BCDT-08** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/reports/revenue<br>2. Tắt kết nối mạng | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại" | | Untested | 11/15/2015 | |
| **FUNC-BCDT-09** | Xử lý khi server lỗi | 1. Truy cập /admin/reports/revenue<br>2. Server trả về lỗi 500 | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau" | | Untested | 11/15/2015 | |

---

### Function: Xem báo cáo chi phí

#### Check GUI: Xem báo cáo chi phí

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-BCCP-01** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/reports/expenses<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Báo cáo chi phí" với kích thước text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-BCCP-02** | Kiểm tra mô tả chức năng | 1. Truy cập /admin/reports/expenses<br>2. Kiểm tra mô tả | Hiển thị mô tả "Theo dõi chi phí vận hành và quản lý" màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-BCCP-03** | Kiểm tra Select Bộ lọc thời gian | 1. Truy cập /admin/reports/expenses<br>2. Kiểm tra Select | Hiển thị Select với placeholder "Khoảng thời gian", có các option: Tháng này, Quý này, Năm nay, Tùy chỉnh | | Pass | 11/15/2015 | |
| **GUI-BCCP-04** | Kiểm tra Select Bộ lọc loại chi phí | 1. Truy cập /admin/reports/expenses<br>2. Kiểm tra Select | Hiển thị Select với placeholder "Loại chi phí", có các option: Tất cả, Vận chuyển, Nhập hàng, Marketing, Nhân sự, Khác | | Pass | 11/15/2015 | |
| **GUI-BCCP-05** | Kiểm tra Card Tổng chi phí | 1. Truy cập /admin/reports/expenses<br>2. Kiểm tra Card | Hiển thị Card "Tổng chi phí" với số tiền VNĐ (text-3xl font-bold), icon TrendingDown | | Pass | 11/15/2015 | |
| **GUI-BCCP-06** | Kiểm tra Chart Biểu đồ chi phí | 1. Truy cập /admin/reports/expenses<br>2. Kiểm tra Chart | Hiển thị Chart Bar/Line "Biểu đồ chi phí" với trục X (thời gian), trục Y (số tiền), phân loại theo loại chi phí | | Pass | 11/15/2015 | |
| **GUI-BCCP-07** | Kiểm tra Table Bảng chi tiết | 1. Truy cập /admin/reports/expenses<br>2. Kiểm tra Table | Hiển thị Table với các cột: Ngày, Loại chi phí, Mô tả, Số tiền, Người tạo | | Pass | 11/15/2015 | |
| **GUI-BCCP-08** | Kiểm tra nút Export | 1. Truy cập /admin/reports/expenses<br>2. Kiểm tra nút | Hiển thị nút "Export" với icon Download variant outline | | Pass | 11/15/2015 | |

---

### Check FUNC: Xem báo cáo chi phí

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-BCCP-01** | Mở trang báo cáo chi phí | 1. Truy cập /admin/reports/expenses | Hiển thị trang với tiêu đề, mô tả, Select Bộ lọc thời gian, Select Bộ lọc loại chi phí, Card Tổng chi phí, Chart Biểu đồ chi phí, Table Bảng chi tiết, nút Export | | Pass | 11/15/2015 | |
| **FUNC-BCCP-02** | Hiển thị báo cáo chi phí mặc định | 1. Truy cập /admin/reports/expenses | Hiển thị báo cáo chi phí theo khoảng thời gian mặc định, số liệu chính xác, biểu đồ trực quan, bảng chi tiết đầy đủ | | Pass | 11/15/2015 | |
| **FUNC-BCCP-03** | Lọc theo thời gian | 1. Truy cập /admin/reports/expenses<br>2. Chọn khoảng thời gian<br>3. Kiểm tra báo cáo | Hiển thị báo cáo chi phí trong khoảng thời gian đã chọn, Card, Chart, Table được cập nhật | | Untested | 11/15/2015 | |
| **FUNC-BCCP-04** | Lọc theo loại chi phí | 1. Truy cập /admin/reports/expenses<br>2. Chọn loại chi phí (VD: Vận chuyển)<br>3. Kiểm tra báo cáo | Hiển thị báo cáo chi phí theo loại đã chọn, Card, Chart, Table được cập nhật | | Untested | 11/15/2015 | |
| **FUNC-BCCP-05** | Export báo cáo chi phí | 1. Truy cập /admin/reports/expenses<br>2. Click nút "Export"<br>3. Chọn định dạng | Tải về file báo cáo chi phí với đầy đủ dữ liệu, file có định dạng đúng | | Untested | 11/15/2015 | |
| **FUNC-BCCP-06** | Xử lý khi không có dữ liệu | 1. Truy cập /admin/reports/expenses<br>2. Chọn khoảng thời gian không có dữ liệu | Hiển thị thông báo "Không có dữ liệu trong khoảng thời gian đã chọn", Chart và Table trống | | Untested | 11/15/2015 | |
| **FUNC-BCCP-07** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/reports/expenses<br>2. Tắt kết nối mạng | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại" | | Untested | 11/15/2015 | |
| **FUNC-BCCP-08** | Xử lý khi server lỗi | 1. Truy cập /admin/reports/expenses<br>2. Server trả về lỗi 500 | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau" | | Untested | 11/15/2015 | |

---

### Function: Xem báo cáo lợi nhuận

#### Check GUI: Xem báo cáo lợi nhuận

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-BCLN-01** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/reports/profit<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Báo cáo lợi nhuận" với kích thước text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-BCLN-02** | Kiểm tra mô tả chức năng | 1. Truy cập /admin/reports/profit<br>2. Kiểm tra mô tả | Hiển thị mô tả "Tính chi phí - doanh thu = lãi" màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-BCLN-03** | Kiểm tra Select Bộ lọc thời gian | 1. Truy cập /admin/reports/profit<br>2. Kiểm tra Select | Hiển thị Select với placeholder "Khoảng thời gian", có các option: Tháng này, Quý này, Năm nay, Tùy chỉnh | | Pass | 11/15/2015 | |
| **GUI-BCLN-04** | Kiểm tra Card Tổng lợi nhuận | 1. Truy cập /admin/reports/profit<br>2. Kiểm tra Card | Hiển thị Card "Tổng lợi nhuận" với số tiền VNĐ (text-3xl font-bold), icon TrendingUp màu xanh lá | | Pass | 11/15/2015 | |
| **GUI-BCLN-05** | Kiểm tra Card Doanh thu | 1. Truy cập /admin/reports/profit<br>2. Kiểm tra Card | Hiển thị Card "Doanh thu" với số tiền VNĐ, icon DollarSign | | Pass | 11/15/2015 | |
| **GUI-BCLN-06** | Kiểm tra Card Chi phí | 1. Truy cập /admin/reports/profit<br>2. Kiểm tra Card | Hiển thị Card "Chi phí" với số tiền VNĐ, icon TrendingDown màu đỏ | | Pass | 11/15/2015 | |
| **GUI-BCLN-07** | Kiểm tra Chart Biểu đồ lợi nhuận | 1. Truy cập /admin/reports/profit<br>2. Kiểm tra Chart | Hiển thị Chart Bar/Line "Biểu đồ lợi nhuận" với trục X (thời gian), trục Y (số tiền), hiển thị Doanh thu, Chi phí, Lợi nhuận | | Pass | 11/15/2015 | |
| **GUI-BCLN-08** | Kiểm tra Table Bảng chi tiết | 1. Truy cập /admin/reports/profit<br>2. Kiểm tra Table | Hiển thị Table với các cột: Thời gian, Doanh thu, Giá vốn, Chi phí, Lợi nhuận, Tỷ lệ lợi nhuận (%) | | Pass | 11/15/2015 | |
| **GUI-BCLN-09** | Kiểm tra nút Export | 1. Truy cập /admin/reports/profit<br>2. Kiểm tra nút | Hiển thị nút "Export" với icon Download variant outline | | Pass | 11/15/2015 | |

---

### Check FUNC: Xem báo cáo lợi nhuận

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-BCLN-01** | Mở trang báo cáo lợi nhuận | 1. Truy cập /admin/reports/profit | Hiển thị trang với tiêu đề, mô tả, Select Bộ lọc thời gian, Card Tổng lợi nhuận, Card Doanh thu, Card Chi phí, Chart Biểu đồ lợi nhuận, Table Bảng chi tiết, nút Export | | Pass | 11/15/2015 | |
| **FUNC-BCLN-02** | Hiển thị báo cáo lợi nhuận mặc định | 1. Truy cập /admin/reports/profit | Hiển thị báo cáo lợi nhuận theo khoảng thời gian mặc định, số liệu đúng (Doanh thu - Chi phí = Lợi nhuận), biểu đồ trình bày rõ ràng, bảng chi tiết đầy đủ | | Pass | 11/15/2015 | |
| **FUNC-BCLN-03** | Lọc theo thời gian | 1. Truy cập /admin/reports/profit<br>2. Chọn khoảng thời gian<br>3. Kiểm tra báo cáo | Hiển thị báo cáo lợi nhuận trong khoảng thời gian đã chọn, các Card, Chart, Table được cập nhật | | Untested | 11/15/2015 | |
| **FUNC-BCLN-04** | Export báo cáo lợi nhuận | 1. Truy cập /admin/reports/profit<br>2. Click nút "Export"<br>3. Chọn định dạng | Tải về file báo cáo lợi nhuận với đầy đủ dữ liệu, file có định dạng đúng | | Untested | 11/15/2015 | |
| **FUNC-BCLN-05** | Xử lý khi không có dữ liệu | 1. Truy cập /admin/reports/profit<br>2. Chọn khoảng thời gian không có dữ liệu | Hiển thị thông báo "Không có dữ liệu trong khoảng thời gian đã chọn", Chart và Table trống | | Untested | 11/15/2015 | |
| **FUNC-BCLN-06** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/reports/profit<br>2. Tắt kết nối mạng | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại" | | Untested | 11/15/2015 | |
| **FUNC-BCLN-07** | Xử lý khi server lỗi | 1. Truy cập /admin/reports/profit<br>2. Server trả về lỗi 500 | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau" | | Untested | 11/15/2015 | |

---

### Function: Xem sản phẩm bán chạy

#### Check GUI: Xem sản phẩm bán chạy

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-SPBC-01** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/reports/top-products<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Sản phẩm bán chạy" với kích thước text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-SPBC-02** | Kiểm tra mô tả chức năng | 1. Truy cập /admin/reports/top-products<br>2. Kiểm tra mô tả | Hiển thị mô tả "Top sản phẩm có doanh số cao" màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-SPBC-03** | Kiểm tra Select Khoảng thời gian | 1. Truy cập /admin/reports/top-products<br>2. Kiểm tra Select | Hiển thị Select với placeholder "Khoảng thời gian", có các option: Hôm nay, Tuần này, Tháng này, Năm nay, Tùy chỉnh | | Pass | 11/15/2015 | |
| **GUI-SPBC-04** | Kiểm tra Table Bảng xếp hạng | 1. Truy cập /admin/reports/top-products<br>2. Kiểm tra Table | Hiển thị Table với các cột: Hạng, Sản phẩm, Số lượng bán, Doanh thu, Tỷ trọng (%) | | Pass | 11/15/2015 | |
| **GUI-SPBC-05** | Kiểm tra Chart Biểu đồ tỉ trọng | 1. Truy cập /admin/reports/top-products<br>2. Kiểm tra Chart | Hiển thị Chart Pie/Donut "Biểu đồ tỉ trọng doanh thu" với các phần tương ứng với từng sản phẩm | | Pass | 11/15/2015 | |
| **GUI-SPBC-06** | Kiểm tra nút Export | 1. Truy cập /admin/reports/top-products<br>2. Kiểm tra nút | Hiển thị nút "Export" với icon Download variant outline | | Pass | 11/15/2015 | |

---

### Check FUNC: Xem sản phẩm bán chạy

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-SPBC-01** | Mở trang sản phẩm bán chạy | 1. Truy cập /admin/reports/top-products | Hiển thị trang với tiêu đề, mô tả, Select Khoảng thời gian, Table Bảng xếp hạng, Chart Biểu đồ tỉ trọng, nút Export | | Pass | 11/15/2015 | |
| **FUNC-SPBC-02** | Hiển thị bảng xếp hạng mặc định | 1. Truy cập /admin/reports/top-products | Hiển thị bảng xếp hạng top sản phẩm theo doanh thu/số lượng, danh sách xếp hạng chính xác, biểu đồ tỉ trọng hiển thị đúng | | Pass | 11/15/2015 | |
| **FUNC-SPBC-03** | Lọc theo thời gian | 1. Truy cập /admin/reports/top-products<br>2. Chọn khoảng thời gian<br>3. Kiểm tra bảng xếp hạng | Hiển thị bảng xếp hạng sản phẩm bán chạy trong khoảng thời gian đã chọn, Table và Chart được cập nhật | | Untested | 11/15/2015 | |
| **FUNC-SPBC-04** | Export báo cáo sản phẩm bán chạy | 1. Truy cập /admin/reports/top-products<br>2. Click nút "Export"<br>3. Chọn định dạng | Tải về file báo cáo sản phẩm bán chạy với đầy đủ dữ liệu, file có định dạng đúng | | Untested | 11/15/2015 | |
| **FUNC-SPBC-05** | Xử lý khi không có dữ liệu | 1. Truy cập /admin/reports/top-products<br>2. Chọn khoảng thời gian không có dữ liệu | Hiển thị thông báo "Không có dữ liệu trong khoảng thời gian đã chọn", Table và Chart trống | | Untested | 11/15/2015 | |
| **FUNC-SPBC-06** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/reports/top-products<br>2. Tắt kết nối mạng | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại" | | Untested | 11/15/2015 | |
| **FUNC-SPBC-07** | Xử lý khi server lỗi | 1. Truy cập /admin/reports/top-products<br>2. Server trả về lỗi 500 | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau" | | Untested | 11/15/2015 | |

---

### Function: Xem thống kê khách hàng

#### Check GUI: Xem thống kê khách hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-TKKH-01** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/reports/customers<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Thống kê khách hàng" với kích thước text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-TKKH-02** | Kiểm tra mô tả chức năng | 1. Truy cập /admin/reports/customers<br>2. Kiểm tra mô tả | Hiển thị mô tả "Khách mới, VIP, tần suất mua hàng" màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-TKKH-03** | Kiểm tra Select Bộ lọc thời gian | 1. Truy cập /admin/reports/customers<br>2. Kiểm tra Select | Hiển thị Select với placeholder "Khoảng thời gian", có các option: Tuần này, Tháng này, Quý này, Năm nay, Tùy chỉnh | | Pass | 11/15/2015 | |
| **GUI-TKKH-04** | Kiểm tra Card Khách mới | 1. Truy cập /admin/reports/customers<br>2. Kiểm tra Card | Hiển thị Card "Khách mới" với số lượng (text-2xl font-bold), icon UserPlus | | Pass | 11/15/2015 | |
| **GUI-TKKH-05** | Kiểm tra Card Khách VIP | 1. Truy cập /admin/reports/customers<br>2. Kiểm tra Card | Hiển thị Card "Khách VIP" với số lượng (text-2xl font-bold), icon Crown | | Pass | 11/15/2015 | |
| **GUI-TKKH-06** | Kiểm tra Card AOV (Average Order Value) | 1. Truy cập /admin/reports/customers<br>2. Kiểm tra Card | Hiển thị Card "AOV" với số tiền VNĐ (text-2xl font-bold), icon DollarSign | | Pass | 11/15/2015 | |
| **GUI-TKKH-07** | Kiểm tra Card Tần suất mua | 1. Truy cập /admin/reports/customers<br>2. Kiểm tra Card | Hiển thị Card "Tần suất mua" với số lần (text-2xl font-bold), icon ShoppingCart | | Pass | 11/15/2015 | |
| **GUI-TKKH-08** | Kiểm tra Table Bảng khách hàng | 1. Truy cập /admin/reports/customers<br>2. Kiểm tra Table | Hiển thị Table với các cột: Tên, Email, Số đơn, Tổng chi tiêu, Hạng | | Pass | 11/15/2015 | |
| **GUI-TKKH-09** | Kiểm tra nút Export | 1. Truy cập /admin/reports/customers<br>2. Kiểm tra nút | Hiển thị nút "Export" với icon Download variant outline | | Pass | 11/15/2015 | |

---

### Check FUNC: Xem thống kê khách hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TKKH-01** | Mở trang thống kê khách hàng | 1. Truy cập /admin/reports/customers | Hiển thị trang với tiêu đề, mô tả, Select Bộ lọc thời gian, Card Khách mới, Card Khách VIP, Card AOV, Card Tần suất mua, Table Bảng khách hàng, nút Export | | Pass | 11/15/2015 | |
| **FUNC-TKKH-02** | Hiển thị thống kê khách hàng mặc định | 1. Truy cập /admin/reports/customers | Hiển thị thống kê khách hàng theo khoảng thời gian mặc định, KPI hiển thị đúng (Khách mới, Khách VIP, AOV, Tần suất mua), bảng khách hàng đầy đủ | | Pass | 11/15/2015 | |
| **FUNC-TKKH-03** | Lọc theo thời gian | 1. Truy cập /admin/reports/customers<br>2. Chọn khoảng thời gian<br>3. Kiểm tra thống kê | Hiển thị thống kê khách hàng trong khoảng thời gian đã chọn, các Card KPI và Table được cập nhật | | Untested | 11/15/2015 | |
| **FUNC-TKKH-04** | Export thống kê khách hàng | 1. Truy cập /admin/reports/customers<br>2. Click nút "Export"<br>3. Chọn định dạng | Tải về file thống kê khách hàng với đầy đủ dữ liệu, file có định dạng đúng | | Untested | 11/15/2015 | |
| **FUNC-TKKH-05** | Xử lý khi không có dữ liệu | 1. Truy cập /admin/reports/customers<br>2. Chọn khoảng thời gian không có dữ liệu | Hiển thị thông báo "Không có dữ liệu trong khoảng thời gian đã chọn", Table trống, các Card KPI hiển thị 0 | | Untested | 11/15/2015 | |
| **FUNC-TKKH-06** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/reports/customers<br>2. Tắt kết nối mạng | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại" | | Untested | 11/15/2015 | |
| **FUNC-TKKH-07** | Xử lý khi server lỗi | 1. Truy cập /admin/reports/customers<br>2. Server trả về lỗi 500 | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau" | | Untested | 11/15/2015 | |

---

### Function: Xem báo cáo tồn kho

#### Check GUI: Xem báo cáo tồn kho

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-BCTK-01** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/reports/inventory<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Báo cáo tồn kho" với kích thước text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-BCTK-02** | Kiểm tra mô tả chức năng | 1. Truy cập /admin/reports/inventory<br>2. Kiểm tra mô tả | Hiển thị mô tả "Tình trạng hàng hóa, sản phẩm sắp hết" màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-BCTK-03** | Kiểm tra Input Ngưỡng cảnh báo | 1. Truy cập /admin/reports/inventory<br>2. Kiểm tra Input | Hiển thị label "Ngưỡng cảnh báo", input type number với placeholder "Nhập số lượng sắp hết (VD: 5)", có giá trị mặc định | | Pass | 11/15/2015 | |
| **GUI-BCTK-04** | Kiểm tra nút Áp dụng ngưỡng | 1. Truy cập /admin/reports/inventory<br>2. Kiểm tra nút | Hiển thị nút "Áp dụng ngưỡng" variant outline | | Pass | 11/15/2015 | |
| **GUI-BCTK-05** | Kiểm tra Table Bảng tồn kho | 1. Truy cập /admin/reports/inventory<br>2. Kiểm tra Table | Hiển thị Table với các cột: Sản phẩm, SKU, Tồn hiện tại, Ngưỡng, Trạng thái | | Pass | 11/15/2015 | |
| **GUI-BCTK-06** | Kiểm tra Badge Trạng thái trong bảng | 1. Truy cập /admin/reports/inventory<br>2. Kiểm tra Badge | Hiển thị Badge trạng thái: "Đủ hàng" (outline), "Sắp hết" (secondary), "Hết hàng" (destructive) | | Pass | 11/15/2015 | |
| **GUI-BCTK-07** | Kiểm tra Form Bộ lọc nâng cao | 1. Truy cập /admin/reports/inventory<br>2. Kiểm tra Form | Hiển thị Form "Bộ lọc nâng cao" với các trường: Danh mục, Thương hiệu, Trạng thái, có nút "Áp dụng lọc" | | Pass | 11/15/2015 | |
| **GUI-BCTK-08** | Kiểm tra Checkbox Chọn trường export | 1. Truy cập /admin/reports/inventory<br>2. Kiểm tra Checkbox | Hiển thị Checkbox "Chọn trường export" với danh sách các trường: Sản phẩm, SKU, Tồn hiện tại, Ngưỡng, Trạng thái, có thể chọn nhiều | | Pass | 11/15/2015 | |
| **GUI-BCTK-09** | Kiểm tra nút Lưu mẫu export | 1. Truy cập /admin/reports/inventory<br>2. Kiểm tra nút | Hiển thị nút "Lưu mẫu export" variant outline | | Pass | 11/15/2015 | |
| **GUI-BCTK-10** | Kiểm tra nút Export | 1. Truy cập /admin/reports/inventory<br>2. Kiểm tra nút | Hiển thị nút "Export" với icon Download variant outline, có Select định dạng (CSV/XLSX) | | Pass | 11/15/2015 | |

---

### Check FUNC: Xem báo cáo tồn kho

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-BCTK-01** | Mở trang báo cáo tồn kho | 1. Truy cập /admin/reports/inventory | Hiển thị trang với tiêu đề, mô tả, Input Ngưỡng cảnh báo, nút Áp dụng ngưỡng, Table Bảng tồn kho, Form Bộ lọc nâng cao, Checkbox Chọn trường export, nút Lưu mẫu export, nút Export | | Pass | 11/15/2015 | |
| **FUNC-BCTK-02** | Hiển thị báo cáo tồn kho mặc định | 1. Truy cập /admin/reports/inventory | Hiển thị báo cáo tồn kho với danh sách sản phẩm, trạng thái tồn kho, sản phẩm sắp hết được đánh dấu rõ ràng | | Pass | 11/15/2015 | |
| **FUNC-BCTK-03** | Áp dụng ngưỡng cảnh báo | 1. Truy cập /admin/reports/inventory<br>2. Nhập ngưỡng cảnh báo (VD: 5)<br>3. Click "Áp dụng ngưỡng" | Danh sách sản phẩm dưới ngưỡng được liệt kê, cảnh báo rõ ràng, gợi ý nhập hàng, Table được cập nhật | | Untested | 11/15/2015 | |
| **FUNC-BCTK-04** | Lọc nâng cao | 1. Truy cập /admin/reports/inventory<br>2. Chọn danh mục, thương hiệu, trạng thái<br>3. Click "Áp dụng lọc" | Table hiển thị sản phẩm phù hợp với bộ lọc đã chọn | | Untested | 11/15/2015 | |
| **FUNC-BCTK-05** | Export dữ liệu tùy chỉnh | 1. Truy cập /admin/reports/inventory<br>2. Chọn các trường cần export<br>3. Áp dụng bộ lọc (nếu có)<br>4. Chọn định dạng (CSV/XLSX)<br>5. Click "Export" | Tải về file báo cáo tồn kho với các trường đã chọn, file có định dạng đúng | | Untested | 11/15/2015 | |
| **FUNC-BCTK-06** | Lưu mẫu export | 1. Truy cập /admin/reports/inventory<br>2. Chọn các trường export<br>3. Áp dụng bộ lọc<br>4. Click "Lưu mẫu export"<br>5. Nhập tên mẫu | Hiển thị thông báo "Lưu mẫu export thành công", mẫu được lưu và có thể sử dụng lại | | Untested | 11/15/2015 | |
| **FUNC-BCTK-07** | Export - Không chọn trường | 1. Truy cập /admin/reports/inventory<br>2. Không chọn trường export<br>3. Click "Export" | Hiển thị thông báo lỗi "Vui lòng chọn ít nhất một trường để export", không export | | Pass | 11/15/2015 | |
| **FUNC-BCTK-08** | Xử lý khi không có dữ liệu | 1. Truy cập /admin/reports/inventory<br>2. Lọc để không có sản phẩm nào | Hiển thị thông báo "Không tìm thấy sản phẩm nào", Table trống | | Untested | 11/15/2015 | |
| **FUNC-BCTK-09** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/reports/inventory<br>2. Tắt kết nối mạng | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại" | | Untested | 11/15/2015 | |
| **FUNC-BCTK-10** | Xử lý khi server lỗi | 1. Truy cập /admin/reports/inventory<br>2. Server trả về lỗi 500 | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau" | | Untested | 11/15/2015 | |

---

### Function: Tạo báo cáo tùy chỉnh

#### Check GUI: Tạo báo cáo tùy chỉnh

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-BCTC-01** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/reports/advanced<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Báo cáo nâng cao" với kích thước text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-BCTC-02** | Kiểm tra mô tả chức năng | 1. Truy cập /admin/reports/advanced<br>2. Kiểm tra mô tả | Hiển thị mô tả "Phân tích hiệu quả khuyến mãi, hành vi mua" màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-BCTC-03** | Kiểm tra Card Phân tích khuyến mãi | 1. Truy cập /admin/reports/advanced<br>2. Kiểm tra Card | Hiển thị Card "Phân tích khuyến mãi" với: Tỉ lệ sử dụng mã (%), Doanh thu do khuyến mãi (VNĐ), Biểu đồ hiệu quả chiến dịch | | Pass | 11/15/2015 | |
| **GUI-BCTC-04** | Kiểm tra Card Phân tích hành vi | 1. Truy cập /admin/reports/advanced<br>2. Kiểm tra Card | Hiển thị Card "Phân tích hành vi" với: Tần suất mua, Tỷ lệ quay lại (%), Phễu chuyển đổi, Biểu đồ hành vi khách hàng | | Pass | 11/15/2015 | |
| **GUI-BCTC-05** | Kiểm tra Select Bộ lọc thời gian | 1. Truy cập /admin/reports/advanced<br>2. Kiểm tra Select | Hiển thị Select với placeholder "Khoảng thời gian", có các option: Tuần này, Tháng này, Quý này, Năm nay, Tùy chỉnh | | Pass | 11/15/2015 | |
| **GUI-BCTC-06** | Kiểm tra nút Export | 1. Truy cập /admin/reports/advanced<br>2. Kiểm tra nút | Hiển thị nút "Export" với icon Download variant outline | | Pass | 11/15/2015 | |

---

### Check FUNC: Tạo báo cáo tùy chỉnh

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-BCTC-01** | Mở trang báo cáo nâng cao | 1. Truy cập /admin/reports/advanced | Hiển thị trang với tiêu đề, mô tả, Select Bộ lọc thời gian, Card Phân tích khuyến mãi, Card Phân tích hành vi, nút Export | | Pass | 11/15/2015 | |
| **FUNC-BCTC-02** | Hiển thị báo cáo nâng cao mặc định | 1. Truy cập /admin/reports/advanced | Hiển thị báo cáo nâng cao với chỉ số hiển thị đúng (Tỉ lệ sử dụng mã, Doanh thu do khuyến mãi, Tần suất mua, Tỷ lệ quay lại, Phễu chuyển đổi), biểu đồ trực quan | | Pass | 11/15/2015 | |
| **FUNC-BCTC-03** | Lọc theo thời gian | 1. Truy cập /admin/reports/advanced<br>2. Chọn khoảng thời gian<br>3. Kiểm tra báo cáo | Hiển thị báo cáo nâng cao trong khoảng thời gian đã chọn, các Card và biểu đồ được cập nhật | | Untested | 11/15/2015 | |
| **FUNC-BCTC-04** | Export báo cáo nâng cao | 1. Truy cập /admin/reports/advanced<br>2. Click nút "Export"<br>3. Chọn định dạng | Tải về file báo cáo nâng cao với đầy đủ dữ liệu, file có định dạng đúng | | Untested | 11/15/2015 | |
| **FUNC-BCTC-05** | Xử lý khi không có dữ liệu | 1. Truy cập /admin/reports/advanced<br>2. Chọn khoảng thời gian không có dữ liệu | Hiển thị thông báo "Không có dữ liệu trong khoảng thời gian đã chọn", các Card và biểu đồ trống | | Untested | 11/15/2015 | |
| **FUNC-BCTC-06** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/reports/advanced<br>2. Tắt kết nối mạng | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại" | | Untested | 11/15/2015 | |
| **FUNC-BCTC-07** | Xử lý khi server lỗi | 1. Truy cập /admin/reports/advanced<br>2. Server trả về lỗi 500 | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau" | | Untested | 11/15/2015 | |

---

**Người tạo:** Testing Team  
**Ngày cập nhật:** 11/15/2015  
**Phiên bản:** 1.0

