# BLACKBOX TEST CASE - BÁO CÁO VÀ THỐNG KÊ (ADMIN)

## HEADER SECTION

**Module Code:** Báo cáo và thống kê Admin

**Test requirement:**
1. Xem báo cáo doanh thu
2. Xem báo cáo chi phí
3. Xem báo cáo lợi nhuận
4. Xem sản phẩm bán chạy
5. Xem thống kê khách hàng
6. Xem báo cáo tồn kho
7. Tạo báo cáo tùy chỉnh

**Tester:** [Tên tester]

**Summary Statistics:**
- Pass: 0
- Failed: 0
- Untested: [Số lượng test cases]
- N/A: 0
- Number of Test cases: [Tổng số test cases]

---

## TEST CASE TABLE

| ID | Test Case Description | Test Case Procedure | Expected Output | Test-case rate | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|----------------|--------|-----------|------|
| **Function: Xem báo cáo doanh thu** |
| **Check GUI: Xem báo cáo doanh thu** |
| GUI-BaoCaoDT-01 | Check [Tiêu đề trang] Text | 1. Truy cập `/admin/reports/revenue`<br>2. Kiểm tra tiêu đề | Status: visible, Text: "Báo cáo doanh thu" | | | | |
| GUI-BaoCaoDT-02 | Check [Bộ lọc thời gian] Select | 1. Truy cập `/admin/reports/revenue`<br>2. Kiểm tra dropdown [Bộ lọc thời gian] | Status: visible, enable, Options: Hôm nay, Tuần này, Tháng này, Năm nay, Tùy chỉnh | | | | |
| GUI-BaoCaoDT-03 | Check [Bộ lọc kênh] Select | 1. Truy cập `/admin/reports/revenue`<br>2. Kiểm tra dropdown [Bộ lọc kênh] | Status: visible, enable, Options: Tất cả, COD, Banking, E-wallet | | | | |
| GUI-BaoCaoDT-04 | Check [Biểu đồ doanh thu] Chart | 1. Truy cập `/admin/reports/revenue`<br>2. Kiểm tra biểu đồ | Status: visible, Type: Line/Bar, Hiển thị xu hướng doanh thu | | | | |
| GUI-BaoCaoDT-05 | Check [Tổng doanh thu] Card | 1. Truy cập `/admin/reports/revenue`<br>2. Kiểm tra card | Status: visible, Hiển thị số tiền VNĐ | | | | |
| GUI-BaoCaoDT-06 | Check [Bảng chi tiết] Table | 1. Truy cập `/admin/reports/revenue`<br>2. Kiểm tra bảng | Status: visible, Columns: Ngày, Số đơn, Doanh thu, Trung bình đơn, Tỷ lệ hoàn | | | | |
| GUI-BaoCaoDT-07 | Check [Export] Button | 1. Truy cập `/admin/reports/revenue`<br>2. Kiểm tra nút [Export] | Status: visible, enable | | | | |
| **Check FUNC: Xem báo cáo doanh thu** |
| FUNC-BaoCaoDT-01 | Mở màn hình báo cáo doanh thu | 1. Truy cập `/admin/reports/revenue` hoặc click [Báo cáo & Thống kê] > [Xem doanh thu] | Hiển thị màn hình báo cáo doanh thu với đầy đủ thông tin | | | | |
| FUNC-BaoCaoDT-02 | Lọc báo cáo theo thời gian | 1. Truy cập `/admin/reports/revenue`<br>2. Chọn thời gian từ dropdown<br>3. Kiểm tra kết quả | Biểu đồ và bảng được cập nhật theo khoảng thời gian đã chọn | | | | |
| FUNC-BaoCaoDT-03 | Lọc báo cáo theo kênh thanh toán | 1. Truy cập `/admin/reports/revenue`<br>2. Chọn kênh từ dropdown<br>3. Kiểm tra kết quả | Biểu đồ và bảng được cập nhật theo kênh đã chọn | | | | |
| FUNC-BaoCaoDT-04 | Lọc báo cáo theo thời gian tùy chỉnh | 1. Truy cập `/admin/reports/revenue`<br>2. Chọn "Tùy chỉnh"<br>3. Chọn khoảng ngày<br>4. Kiểm tra kết quả | Biểu đồ và bảng được cập nhật theo khoảng ngày đã chọn | | | | |
| FUNC-BaoCaoDT-05 | Hiển thị biểu đồ doanh thu | 1. Truy cập `/admin/reports/revenue`<br>2. Kiểm tra biểu đồ | Biểu đồ hiển thị xu hướng doanh thu chính xác, trực quan | | | | |
| FUNC-BaoCaoDT-06 | Hiển thị tổng doanh thu | 1. Truy cập `/admin/reports/revenue`<br>2. Kiểm tra card tổng doanh thu | Hiển thị tổng doanh thu chính xác theo bộ lọc | | | | |
| FUNC-BaoCaoDT-07 | Hiển thị bảng chi tiết | 1. Truy cập `/admin/reports/revenue`<br>2. Kiểm tra bảng | Hiển thị đầy đủ: Ngày, Số đơn, Doanh thu, Trung bình đơn, Tỷ lệ hoàn | | | | |
| FUNC-BaoCaoDT-08 | Export báo cáo doanh thu | 1. Truy cập `/admin/reports/revenue`<br>2. Click [Export] | File Excel/PDF được tải xuống với báo cáo doanh thu | | | | |
| **Function: Xem báo cáo chi phí** |
| **Check GUI: Xem báo cáo chi phí** |
| GUI-BaoCaoCP-01 | Check [Tiêu đề trang] Text | 1. Truy cập `/admin/reports/expenses`<br>2. Kiểm tra tiêu đề | Status: visible, Text: "Báo cáo chi phí" | | | | |
| GUI-BaoCaoCP-02 | Check [Bộ lọc thời gian] Select | 1. Truy cập `/admin/reports/expenses`<br>2. Kiểm tra dropdown [Bộ lọc thời gian] | Status: visible, enable, Options: Hôm nay, Tuần này, Tháng này, Năm nay, Tùy chỉnh | | | | |
| GUI-BaoCaoCP-03 | Check [Bộ lọc loại chi phí] Select | 1. Truy cập `/admin/reports/expenses`<br>2. Kiểm tra dropdown [Bộ lọc loại chi phí] | Status: visible, enable, Options: Tất cả, Nhập hàng, Vận chuyển, Marketing, Khác | | | | |
| GUI-BaoCaoCP-04 | Check [Biểu đồ chi phí] Chart | 1. Truy cập `/admin/reports/expenses`<br>2. Kiểm tra biểu đồ | Status: visible, Type: Line/Bar, Hiển thị xu hướng chi phí | | | | |
| GUI-BaoCaoCP-05 | Check [Tổng chi phí] Card | 1. Truy cập `/admin/reports/expenses`<br>2. Kiểm tra card | Status: visible, Hiển thị số tiền VNĐ | | | | |
| GUI-BaoCaoCP-06 | Check [Bảng chi tiết] Table | 1. Truy cập `/admin/reports/expenses`<br>2. Kiểm tra bảng | Status: visible, Columns: Ngày, Loại chi phí, Số tiền, Mô tả | | | | |
| **Check FUNC: Xem báo cáo chi phí** |
| FUNC-BaoCaoCP-01 | Mở màn hình báo cáo chi phí | 1. Truy cập `/admin/reports/expenses` hoặc click [Báo cáo & Thống kê] > [Xem chi phí] | Hiển thị màn hình báo cáo chi phí với đầy đủ thông tin | | | | |
| FUNC-BaoCaoCP-02 | Lọc báo cáo theo thời gian | 1. Truy cập `/admin/reports/expenses`<br>2. Chọn thời gian từ dropdown<br>3. Kiểm tra kết quả | Biểu đồ và bảng được cập nhật theo khoảng thời gian đã chọn | | | | |
| FUNC-BaoCaoCP-03 | Lọc báo cáo theo loại chi phí | 1. Truy cập `/admin/reports/expenses`<br>2. Chọn loại chi phí từ dropdown<br>3. Kiểm tra kết quả | Biểu đồ và bảng được cập nhật theo loại chi phí đã chọn | | | | |
| FUNC-BaoCaoCP-04 | Hiển thị biểu đồ chi phí | 1. Truy cập `/admin/reports/expenses`<br>2. Kiểm tra biểu đồ | Biểu đồ hiển thị xu hướng chi phí chính xác, trực quan | | | | |
| FUNC-BaoCaoCP-05 | Hiển thị tổng chi phí | 1. Truy cập `/admin/reports/expenses`<br>2. Kiểm tra card tổng chi phí | Hiển thị tổng chi phí chính xác theo bộ lọc | | | | |
| FUNC-BaoCaoCP-06 | Hiển thị bảng chi tiết | 1. Truy cập `/admin/reports/expenses`<br>2. Kiểm tra bảng | Hiển thị đầy đủ: Ngày, Loại chi phí, Số tiền, Mô tả | | | | |
| **Function: Xem báo cáo lợi nhuận** |
| **Check GUI: Xem báo cáo lợi nhuận** |
| GUI-BaoCaoLN-01 | Check [Tiêu đề trang] Text | 1. Truy cập `/admin/reports/profit`<br>2. Kiểm tra tiêu đề | Status: visible, Text: "Báo cáo lợi nhuận" | | | | |
| GUI-BaoCaoLN-02 | Check [Bộ lọc thời gian] Select | 1. Truy cập `/admin/reports/profit`<br>2. Kiểm tra dropdown [Bộ lọc thời gian] | Status: visible, enable, Options: Hôm nay, Tuần này, Tháng này, Năm nay, Tùy chỉnh | | | | |
| GUI-BaoCaoLN-03 | Check [Biểu đồ lợi nhuận] Chart | 1. Truy cập `/admin/reports/profit`<br>2. Kiểm tra biểu đồ | Status: visible, Type: Line/Bar, Hiển thị xu hướng lợi nhuận | | | | |
| GUI-BaoCaoLN-04 | Check [Tổng lợi nhuận] Card | 1. Truy cập `/admin/reports/profit`<br>2. Kiểm tra card | Status: visible, Hiển thị số tiền VNĐ | | | | |
| GUI-BaoCaoLN-05 | Check [Tổng doanh thu] Card | 1. Truy cập `/admin/reports/profit`<br>2. Kiểm tra card | Status: visible, Hiển thị số tiền VNĐ | | | | |
| GUI-BaoCaoLN-06 | Check [Tổng chi phí] Card | 1. Truy cập `/admin/reports/profit`<br>2. Kiểm tra card | Status: visible, Hiển thị số tiền VNĐ | | | | | |
| GUI-BaoCaoLN-07 | Check [Bảng chi tiết] Table | 1. Truy cập `/admin/reports/profit`<br>2. Kiểm tra bảng | Status: visible, Columns: Ngày, Doanh thu, Chi phí, Lợi nhuận, Tỷ suất lợi nhuận | | | | |
| **Check FUNC: Xem báo cáo lợi nhuận** |
| FUNC-BaoCaoLN-01 | Mở màn hình báo cáo lợi nhuận | 1. Truy cập `/admin/reports/profit` hoặc click [Báo cáo & Thống kê] > [Xem lợi nhuận] | Hiển thị màn hình báo cáo lợi nhuận với đầy đủ thông tin | | | | |
| FUNC-BaoCaoLN-02 | Lọc báo cáo theo thời gian | 1. Truy cập `/admin/reports/profit`<br>2. Chọn thời gian từ dropdown<br>3. Kiểm tra kết quả | Biểu đồ và bảng được cập nhật theo khoảng thời gian đã chọn | | | | |
| FUNC-BaoCaoLN-03 | Hiển thị biểu đồ lợi nhuận | 1. Truy cập `/admin/reports/profit`<br>2. Kiểm tra biểu đồ | Biểu đồ hiển thị xu hướng lợi nhuận chính xác, trực quan | | | | |
| FUNC-BaoCaoLN-04 | Tính toán lợi nhuận | 1. Truy cập `/admin/reports/profit`<br>2. Kiểm tra tổng lợi nhuận | Tổng lợi nhuận = Tổng doanh thu - Tổng chi phí (tính toán chính xác) | | | | |
| FUNC-BaoCaoLN-05 | Hiển thị tổng doanh thu và chi phí | 1. Truy cập `/admin/reports/profit`<br>2. Kiểm tra các card | Hiển thị tổng doanh thu và tổng chi phí chính xác theo bộ lọc | | | | |
| FUNC-BaoCaoLN-06 | Hiển thị bảng chi tiết | 1. Truy cập `/admin/reports/profit`<br>2. Kiểm tra bảng | Hiển thị đầy đủ: Ngày, Doanh thu, Chi phí, Lợi nhuận, Tỷ suất lợi nhuận | | | | |
| **Function: Xem sản phẩm bán chạy** |
| **Check GUI: Xem sản phẩm bán chạy** |
| GUI-SPBC-01 | Check [Tiêu đề trang] Text | 1. Truy cập `/admin/reports/top-products`<br>2. Kiểm tra tiêu đề | Status: visible, Text: "Sản phẩm bán chạy" | | | | |
| GUI-SPBC-02 | Check [Khoảng thời gian] Select | 1. Truy cập `/admin/reports/top-products`<br>2. Kiểm tra dropdown [Khoảng thời gian] | Status: visible, enable, Options: Hôm nay, Tuần, Tháng, Năm | | | | |
| GUI-SPBC-03 | Check [Bảng xếp hạng] Table | 1. Truy cập `/admin/reports/top-products`<br>2. Kiểm tra bảng | Status: visible, Columns: Sản phẩm, SL bán, Doanh thu, Tỷ trọng | | | | |
| GUI-SPBC-04 | Check [Biểu đồ tỉ trọng] Chart | 1. Truy cập `/admin/reports/top-products`<br>2. Kiểm tra biểu đồ | Status: visible, Type: Pie/Donut, Hiển thị tỷ trọng doanh thu | | | | |
| **Check FUNC: Xem sản phẩm bán chạy** |
| FUNC-SPBC-01 | Mở màn hình sản phẩm bán chạy | 1. Truy cập `/admin/reports/top-products` hoặc click [Báo cáo & Thống kê] > [Sản phẩm bán chạy] | Hiển thị màn hình sản phẩm bán chạy với đầy đủ thông tin | | | | |
| FUNC-SPBC-02 | Lọc theo khoảng thời gian | 1. Truy cập `/admin/reports/top-products`<br>2. Chọn khoảng thời gian từ dropdown<br>3. Kiểm tra kết quả | Bảng xếp hạng và biểu đồ được cập nhật theo khoảng thời gian đã chọn | | | | |
| FUNC-SPBC-03 | Hiển thị bảng xếp hạng | 1. Truy cập `/admin/reports/top-products`<br>2. Kiểm tra bảng | Hiển thị đầy đủ: Sản phẩm, SL bán, Doanh thu, Tỷ trọng, xếp hạng theo doanh số | | | | |
| FUNC-SPBC-04 | Hiển thị biểu đồ tỉ trọng | 1. Truy cập `/admin/reports/top-products`<br>2. Kiểm tra biểu đồ | Biểu đồ hiển thị tỷ trọng doanh thu của từng sản phẩm chính xác, trực quan | | | | |
| FUNC-SPBC-05 | Xếp hạng theo doanh thu | 1. Truy cập `/admin/reports/top-products`<br>2. Kiểm tra bảng | Sản phẩm được xếp hạng theo doanh thu từ cao xuống thấp | | | | |
| FUNC-SPBC-06 | Xếp hạng theo số lượng | 1. Truy cập `/admin/reports/top-products`<br>2. Kiểm tra bảng | Sản phẩm được xếp hạng theo số lượng bán từ cao xuống thấp | | | | |
| **Function: Xem thống kê khách hàng** |
| **Check GUI: Xem thống kê khách hàng** |
| GUI-TKKH-01 | Check [Tiêu đề trang] Text | 1. Truy cập `/admin/reports/customers`<br>2. Kiểm tra tiêu đề | Status: visible, Text: "Thống kê khách hàng" | | | | |
| GUI-TKKH-02 | Check [Bộ lọc thời gian] Select | 1. Truy cập `/admin/reports/customers`<br>2. Kiểm tra dropdown [Bộ lọc thời gian] | Status: visible, enable, Options: Tuần, Tháng, Quý, Năm | | | | |
| GUI-TKKH-03 | Check [Chỉ số tổng quan] Cards | 1. Truy cập `/admin/reports/customers`<br>2. Kiểm tra cards | Status: visible, Hiển thị: Khách mới, Khách VIP, AOV, Tần suất mua | | | | |
| GUI-TKKH-04 | Check [Bảng khách hàng] Table | 1. Truy cập `/admin/reports/customers`<br>2. Kiểm tra bảng | Status: visible, Columns: Tên, Email, Số đơn, Tổng chi tiêu, Hạng | | | | |
| **Check FUNC: Xem thống kê khách hàng** |
| FUNC-TKKH-01 | Mở màn hình thống kê khách hàng | 1. Truy cập `/admin/reports/customers` hoặc click [Báo cáo & Thống kê] > [Thống kê khách hàng] | Hiển thị màn hình thống kê khách hàng với đầy đủ thông tin | | | | |
| FUNC-TKKH-02 | Lọc theo thời gian | 1. Truy cập `/admin/reports/customers`<br>2. Chọn thời gian từ dropdown<br>3. Kiểm tra kết quả | Chỉ số tổng quan và bảng được cập nhật theo khoảng thời gian đã chọn | | | | |
| FUNC-TKKH-03 | Hiển thị chỉ số tổng quan | 1. Truy cập `/admin/reports/customers`<br>2. Kiểm tra cards | Hiển thị đầy đủ: Khách mới, Khách VIP, AOV (Average Order Value), Tần suất mua, tính toán chính xác | | | | |
| FUNC-TKKH-04 | Hiển thị bảng khách hàng | 1. Truy cập `/admin/reports/customers`<br>2. Kiểm tra bảng | Hiển thị đầy đủ: Tên, Email, Số đơn, Tổng chi tiêu, Hạng thành viên | | | | |
| FUNC-TKKH-05 | Tính toán KPI khách hàng | 1. Truy cập `/admin/reports/customers`<br>2. Kiểm tra chỉ số | KPI được tính toán chính xác theo bộ lọc: Khách mới, Khách VIP, AOV, Tần suất mua | | | | |
| **Function: Xem báo cáo tồn kho** |
| **Check GUI: Xem báo cáo tồn kho** |
| GUI-BaoCaoTK-01 | Check [Tiêu đề trang] Text | 1. Truy cập `/admin/reports/inventory`<br>2. Kiểm tra tiêu đề | Status: visible, Text: "Báo cáo tồn kho" | | | | |
| GUI-BaoCaoTK-02 | Check [Bộ lọc thời gian] Select | 1. Truy cập `/admin/reports/inventory`<br>2. Kiểm tra dropdown [Bộ lọc thời gian] | Status: visible, enable, Options: Hôm nay, Tuần này, Tháng này, Năm nay, Tùy chỉnh | | | | |
| GUI-BaoCaoTK-03 | Check [Bộ lọc trạng thái] Select | 1. Truy cập `/admin/reports/inventory`<br>2. Kiểm tra dropdown [Bộ lọc trạng thái] | Status: visible, enable, Options: Tất cả, Còn hàng, Sắp hết, Hết hàng | | | | |
| GUI-BaoCaoTK-04 | Check [Bảng báo cáo] Table | 1. Truy cập `/admin/reports/inventory`<br>2. Kiểm tra bảng | Status: visible, Columns: Sản phẩm, Tồn kho hiện tại, Tồn kho tối thiểu, Trạng thái, Cảnh báo | | | | |
| GUI-BaoCaoTK-05 | Check [Biểu đồ tồn kho] Chart | 1. Truy cập `/admin/reports/inventory`<br>2. Kiểm tra biểu đồ | Status: visible, Type: Bar, Hiển thị tình trạng tồn kho | | | | |
| **Check FUNC: Xem báo cáo tồn kho** |
| FUNC-BaoCaoTK-01 | Mở màn hình báo cáo tồn kho | 1. Truy cập `/admin/reports/inventory` hoặc click [Báo cáo & Thống kê] > [Báo cáo tồn kho] | Hiển thị màn hình báo cáo tồn kho với đầy đủ thông tin | | | | |
| FUNC-BaoCaoTK-02 | Lọc theo thời gian | 1. Truy cập `/admin/reports/inventory`<br>2. Chọn thời gian từ dropdown<br>3. Kiểm tra kết quả | Bảng và biểu đồ được cập nhật theo khoảng thời gian đã chọn | | | | |
| FUNC-BaoCaoTK-03 | Lọc theo trạng thái | 1. Truy cập `/admin/reports/inventory`<br>2. Chọn trạng thái từ dropdown<br>3. Kiểm tra kết quả | Bảng được cập nhật theo trạng thái đã chọn | | | | |
| FUNC-BaoCaoTK-04 | Hiển thị bảng báo cáo | 1. Truy cập `/admin/reports/inventory`<br>2. Kiểm tra bảng | Hiển thị đầy đủ: Sản phẩm, Tồn kho hiện tại, Tồn kho tối thiểu, Trạng thái, Cảnh báo | | | | |
| FUNC-BaoCaoTK-05 | Hiển thị cảnh báo sản phẩm sắp hết | 1. Truy cập `/admin/reports/inventory`<br>2. Kiểm tra bảng | Sản phẩm sắp hết được đánh dấu và cảnh báo rõ ràng | | | | |
| FUNC-BaoCaoTK-06 | Hiển thị biểu đồ tồn kho | 1. Truy cập `/admin/reports/inventory`<br>2. Kiểm tra biểu đồ | Biểu đồ hiển thị tình trạng tồn kho chính xác, trực quan | | | | |
| **Function: Tạo báo cáo tùy chỉnh** |
| **Check GUI: Tạo báo cáo tùy chỉnh** |
| GUI-BaoCaoTC-01 | Check [Tiêu đề trang] Text | 1. Truy cập `/admin/reports/advanced`<br>2. Kiểm tra tiêu đề | Status: visible, Text: "Báo cáo nâng cao" | | | | |
| GUI-BaoCaoTC-02 | Check [Form tạo báo cáo] Form | 1. Truy cập `/admin/reports/advanced`<br>2. Kiểm tra form | Status: visible, Hiển thị form tạo báo cáo tùy chỉnh | | | | |
| GUI-BaoCaoTC-03 | Check [Loại báo cáo] Select | 1. Truy cập `/admin/reports/advanced`<br>2. Kiểm tra dropdown | Status: visible, enable, Options: Doanh thu, Chi phí, Lợi nhuận, Sản phẩm, Khách hàng, Tồn kho | | | | |
| GUI-BaoCaoTC-04 | Check [Khoảng thời gian] Date Range | 1. Truy cập `/admin/reports/advanced`<br>2. Kiểm tra date range | Status: visible, enable, Type: date range | | | | |
| GUI-BaoCaoTC-05 | Check [Bộ lọc bổ sung] Checkbox Group | 1. Truy cập `/admin/reports/advanced`<br>2. Kiểm tra checkbox group | Status: visible, enable, Options: Theo sản phẩm, Theo khách hàng, Theo kênh thanh toán | | | | |
| GUI-BaoCaoTC-06 | Check [Định dạng xuất] Select | 1. Truy cập `/admin/reports/advanced`<br>2. Kiểm tra dropdown | Status: visible, enable, Options: Excel, PDF, CSV | | | | |
| GUI-BaoCaoTC-07 | Check [Tạo báo cáo] Button | 1. Truy cập `/admin/reports/advanced`<br>2. Kiểm tra nút [Tạo báo cáo] | Status: visible, enable | | | | |
| GUI-BaoCaoTC-08 | Check [Hủy] Button | 1. Truy cập `/admin/reports/advanced`<br>2. Kiểm tra nút [Hủy] | Status: visible, enable | | | | |
| **Check FUNC: Tạo báo cáo tùy chỉnh** |
| FUNC-BaoCaoTC-01 | Mở màn hình tạo báo cáo tùy chỉnh | 1. Truy cập `/admin/reports/advanced` hoặc click [Báo cáo & Thống kê] > [Báo cáo nâng cao] | Hiển thị form tạo báo cáo tùy chỉnh với các trường trống | | | | |
| FUNC-BaoCaoTC-02 | Tạo báo cáo tùy chỉnh thành công | 1. Truy cập `/admin/reports/advanced`<br>2. Chọn loại báo cáo<br>3. Chọn khoảng thời gian<br>4. Chọn bộ lọc bổ sung (nếu có)<br>5. Chọn định dạng xuất<br>6. Click [Tạo báo cáo] | Báo cáo được tạo thành công, file được tải xuống với định dạng đã chọn, thông báo xác nhận | | | | | |
| FUNC-BaoCaoTC-03 | Tạo báo cáo không chọn loại báo cáo | 1. Truy cập `/admin/reports/advanced`<br>2. Không chọn loại báo cáo<br>3. Click [Tạo báo cáo] | Hiển thị thông báo lỗi: "Vui lòng chọn loại báo cáo" | | | | |
| FUNC-BaoCaoTC-04 | Tạo báo cáo không chọn khoảng thời gian | 1. Truy cập `/admin/reports/advanced`<br>2. Không chọn khoảng thời gian<br>3. Click [Tạo báo cáo] | Hiển thị thông báo lỗi: "Vui lòng chọn khoảng thời gian" | | | | |
| FUNC-BaoCaoTC-05 | Tạo báo cáo với bộ lọc bổ sung | 1. Truy cập `/admin/reports/advanced`<br>2. Chọn bộ lọc bổ sung<br>3. Click [Tạo báo cáo] | Báo cáo được tạo với bộ lọc bổ sung đã chọn | | | | |
| FUNC-BaoCaoTC-06 | Export báo cáo Excel | 1. Truy cập `/admin/reports/advanced`<br>2. Chọn định dạng Excel<br>3. Click [Tạo báo cáo] | File Excel được tải xuống với báo cáo đầy đủ | | | | |
| FUNC-BaoCaoTC-07 | Export báo cáo PDF | 1. Truy cập `/admin/reports/advanced`<br>2. Chọn định dạng PDF<br>3. Click [Tạo báo cáo] | File PDF được tải xuống với báo cáo đầy đủ | | | | |
| FUNC-BaoCaoTC-08 | Click nút Hủy | 1. Truy cập `/admin/reports/advanced`<br>2. Điền một số thông tin<br>3. Click [Hủy] | Form được reset, không tạo báo cáo | | | | |

---

## GHI CHÚ

- Tất cả test cases cần được thực hiện trên môi trường test
- Routes động (có `[id]`) cần thay thế bằng ID thực tế khi test
- Các test case GUI kiểm tra giao diện và trạng thái của các thành phần
- Các test case FUNC kiểm tra chức năng và logic nghiệp vụ
- Tất cả báo cáo có thể được export ra file Excel, PDF, hoặc CSV
- Biểu đồ được hiển thị dưới dạng Line, Bar, Pie, hoặc Donut tùy theo loại báo cáo
- Số liệu được tính toán theo thời gian thực từ dữ liệu trong hệ thống
- Cần cập nhật cột Result, Test date sau khi thực hiện test

