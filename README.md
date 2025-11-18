# Test Case Template - Báo cáo và thống kê (Nhân viên)

## Module Code
**Giao lộ 19: Họcl6c (Nhân viên)**

## Test Requirement
1. Báo cáo ca làm
2. Xem số lượng đơn hàng đã xử lý
3. Báo cáo cuối ca

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

### Function: Báo cáo và thống kê

#### Check GUI: Báo cáo và thống kê

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-BCTK-01** | Kiểm tra tiêu đề trang | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/reports<br>3. Kiểm tra tiêu đề | Hiển thị div space-y-6 với h1 "Báo cáo & Thống kê" class text-2xl font-bold, p "Chọn loại báo cáo để xem chi tiết" class text-sm text-muted-foreground | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-BCTK-02** | Kiểm tra card Doanh thu | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/reports<br>3. Kiểm tra card | Hiển thị div grid grid-cols-1 md:grid-cols-3 gap-4 với Card có CardHeader có CardTitle "Doanh thu", CardDescription "Báo cáo doanh thu theo thời gian", CardContent có Button asChild className="w-full" Link href="/nhanvien/reports/revenue" "Xem báo cáo" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-BCTK-03** | Kiểm tra card Lợi nhuận | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/reports<br>3. Kiểm tra card | Hiển thị Card có CardHeader có CardTitle "Lợi nhuận", CardDescription "Theo dõi lợi nhuận theo kỳ", CardContent có Button asChild className="w-full" Link href="/nhanvien/reports/profit" "Xem báo cáo" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-BCTK-04** | Kiểm tra card Tồn kho | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/reports<br>3. Kiểm tra card | Hiển thị Card có CardHeader có CardTitle "Tồn kho", CardDescription "Phân tích tồn kho, cảnh báo", CardContent có Button asChild className="w-full" Link href="/nhanvien/reports/inventory" "Xem báo cáo" | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Báo cáo và thống kê

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-BCTK-01** | Xem trang báo cáo và thống kê | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/reports | Hiển thị đầy đủ: tiêu đề "Báo cáo & Thống kê" và mô tả, grid 3 card: Card "Doanh thu" với mô tả "Báo cáo doanh thu theo thời gian", nút "Xem báo cáo" Link href="/nhanvien/reports/revenue". Card "Lợi nhuận" với mô tả "Theo dõi lợi nhuận theo kỳ", nút "Xem báo cáo" Link href="/nhanvien/reports/profit". Card "Tồn kho" với mô tả "Phân tích tồn kho, cảnh báo", nút "Xem báo cáo" Link href="/nhanvien/reports/inventory" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-BCTK-02** | Xem báo cáo doanh thu | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/reports<br>3. Click nút "Xem báo cáo" trên card "Doanh thu" | Chuyển đến trang /nhanvien/reports/revenue, hiển thị báo cáo doanh thu với đầy đủ thông tin | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-BCTK-03** | Xem báo cáo lợi nhuận | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/reports<br>3. Click nút "Xem báo cáo" trên card "Lợi nhuận" | Chuyển đến trang /nhanvien/reports/profit, hiển thị báo cáo lợi nhuận với đầy đủ thông tin | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-BCTK-04** | Xem báo cáo tồn kho | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/reports<br>3. Click nút "Xem báo cáo" trên card "Tồn kho" | Chuyển đến trang /nhanvien/reports/inventory, hiển thị báo cáo tồn kho với đầy đủ thông tin | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Báo cáo doanh thu

#### Check GUI: Báo cáo doanh thu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-BCDT-01** | Kiểm tra tiêu đề trang | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/reports/revenue<br>3. Kiểm tra tiêu đề | Hiển thị div space-y-6 với h1 "Báo cáo doanh thu" class text-2xl font-bold, p "Doanh thu theo ngày/tháng/quý/năm" class text-sm text-muted-foreground | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-BCDT-02** | Kiểm tra card Bộ lọc | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/reports/revenue<br>3. Kiểm tra card | Hiển thị Card với CardHeader có CardTitle "Bộ lọc", CardDescription "Khoảng thời gian và nhóm theo", CardContent className="grid md:grid-cols-4 gap-3" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-BCDT-03** | Kiểm tra các trường bộ lọc | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/reports/revenue<br>3. Kiểm tra trường | Hiển thị: div grid gap-1 với Label "Từ ngày", Input type="date". div grid gap-1 với Label "Đến ngày", Input type="date". div grid gap-1 với Label "Nhóm theo", Select với SelectTrigger SelectValue placeholder="Ngày", SelectContent có SelectItem (Ngày, Tháng, Quý, Năm) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-BCDT-04** | Kiểm tra card Biểu đồ doanh thu | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/reports/revenue<br>3. Kiểm tra card | Hiển thị Card với CardHeader có CardTitle "Biểu đồ doanh thu", CardDescription "Đường/ cột theo nhóm", CardContent có div h-64 bg-muted rounded (placeholder cho biểu đồ) | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Báo cáo doanh thu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-BCDT-01** | Xem báo cáo doanh thu | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/reports/revenue | Hiển thị đầy đủ: tiêu đề "Báo cáo doanh thu" và mô tả, card Bộ lọc với Input "Từ ngày" type="date", Input "Đến ngày" type="date", Select "Nhóm theo" (Ngày, Tháng, Quý, Năm), card Biểu đồ doanh thu với div placeholder cho biểu đồ (trong thực tế sẽ hiển thị biểu đồ đường hoặc cột), biểu đồ hiển thị doanh thu theo khoảng thời gian và nhóm đã chọn | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-BCDT-02** | Lọc báo cáo theo khoảng thời gian | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/reports/revenue<br>3. Chọn "Từ ngày" và "Đến ngày"<br>4. Chọn "Nhóm theo" (VD: "Ngày") | Báo cáo được lọc theo khoảng thời gian đã chọn, biểu đồ được cập nhật hiển thị doanh thu trong khoảng thời gian đó, dữ liệu được nhóm theo "Ngày" (mỗi ngày một điểm trên biểu đồ) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-BCDT-03** | Nhóm báo cáo theo tháng | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/reports/revenue<br>3. Chọn khoảng thời gian<br>4. Chọn "Nhóm theo" = "Tháng" | Biểu đồ được cập nhật, dữ liệu được nhóm theo tháng (mỗi tháng một điểm trên biểu đồ), doanh thu được tổng hợp theo từng tháng | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-BCDT-04** | Nhóm báo cáo theo quý | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/reports/revenue<br>3. Chọn khoảng thời gian<br>4. Chọn "Nhóm theo" = "Quý" | Biểu đồ được cập nhật, dữ liệu được nhóm theo quý (mỗi quý một điểm trên biểu đồ), doanh thu được tổng hợp theo từng quý | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-BCDT-05** | Nhóm báo cáo theo năm | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/reports/revenue<br>3. Chọn khoảng thời gian<br>4. Chọn "Nhóm theo" = "Năm" | Biểu đồ được cập nhật, dữ liệu được nhóm theo năm (mỗi năm một điểm trên biểu đồ), doanh thu được tổng hợp theo từng năm | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Báo cáo ca làm

#### Check FUNC: Báo cáo ca làm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-BCCL-01** | Xem báo cáo ca làm | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/reports/shift<br>3. Xem báo cáo | Hiển thị đầy đủ: tiêu đề "Báo cáo ca làm việc", card Thông tin ca làm với thông tin (Ngày làm việc, Ca làm việc, Nhân viên, Thời gian bắt đầu, Thời gian kết thúc, Trạng thái ca làm Badge), card Thống kê doanh thu với các chỉ số (Tổng doanh thu, Doanh thu tiền mặt với %, Doanh thu thẻ với %, Doanh thu chuyển khoản với %, Doanh thu ví điện tử với %), card Thống kê đơn hàng với các chỉ số (Tổng số đơn hàng, Đơn hàng thành công với %, Đơn hàng đã hủy với %, Đơn hàng trực tiếp với %, Đơn hàng online với %), card Thống kê sản phẩm với các chỉ số (Tổng số sản phẩm bán, Sản phẩm bán chạy nhất, Giá trị đơn hàng TB, Số khách hàng phục vụ), biểu đồ doanh thu theo giờ, biểu đồ doanh thu theo phương thức thanh toán, biểu đồ số lượng đơn hàng theo giờ, bảng chi tiết đơn hàng Table với các cột (Thời gian, Mã đơn hàng Link, Khách hàng, Sản phẩm, Tổng tiền, Phương thức thanh toán, Trạng thái Badge), các nút xuất báo cáo (Xuất PDF, Xuất Excel, In báo cáo, Chia sẻ báo cáo) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-BCCL-02** | Xuất báo cáo ca làm PDF | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/reports/shift<br>3. Click nút "Xuất báo cáo PDF" | File PDF báo cáo ca làm được tạo thành công, báo cáo bao gồm tất cả thông tin trong báo cáo ca làm, định dạng chuyên nghiệp và dễ đọc, tên file tự động đặt theo ngày và ca làm việc (VD: "BaoCaoCaLam_2024-01-22_CaSang.pdf"), file được lưu vào thư mục quy định hoặc tải xuống, hiển thị thông báo thành công "Đã xuất báo cáo PDF" (toast success) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-BCCL-03** | Xuất báo cáo ca làm Excel | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/reports/shift<br>3. Click nút "Xuất báo cáo Excel" | File Excel báo cáo ca làm được tạo thành công, báo cáo bao gồm tất cả dữ liệu chi tiết trong bảng tính, hỗ trợ phân tích dữ liệu với các công thức Excel, tên file tự động đặt theo ngày và ca làm việc (VD: "BaoCaoCaLam_2024-01-22_CaSang.xlsx"), file được lưu vào thư mục quy định hoặc tải xuống, hiển thị thông báo thành công "Đã xuất báo cáo Excel" (toast success) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-BCCL-04** | In báo cáo ca làm | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/reports/shift<br>3. Click nút "In báo cáo" | Bản xem trước báo cáo được hiển thị trước khi in, hỗ trợ tùy chỉnh kích thước và hướng in, báo cáo được in trực tiếp ra máy in, tự động lưu bản sao báo cáo trong hệ thống, hiển thị thông báo thành công "Đã in báo cáo" (toast success) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-BCCL-05** | Chia sẻ báo cáo ca làm | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/reports/shift<br>3. Click nút "Chia sẻ báo cáo" | Hiển thị Dialog hoặc form với các tùy chọn chia sẻ (Email, Link, v.v.), sau khi chia sẻ: báo cáo được chia sẻ thành công, hiển thị thông báo thành công "Đã chia sẻ báo cáo" (toast success) | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Xem số lượng đơn hàng đã xử lý

#### Check FUNC: Xem số lượng đơn hàng đã xử lý

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-SLDH-01** | Xem thống kê đơn hàng đã xử lý | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/reports/orders-processed<br>3. Xem thống kê | Hiển thị đầy đủ: tiêu đề "Thống kê đơn hàng đã xử lý", bộ lọc thời gian với Date Picker "Ngày", Week Picker "Tuần", Month Picker "Tháng", Date Range "Khoảng thời gian tùy chỉnh", card Thống kê tổng quan với các chỉ số (Tổng đơn hàng, Đơn hàng thành công với %, Đơn hàng đã hủy với %, Tỷ lệ thành công Progress Bar, Tổng doanh thu), card Thống kê theo loại với các chỉ số (Đơn hàng trực tiếp với %, Đơn hàng online với %, Đơn hàng COD với %, Đơn hàng thanh toán trước với %), card Thống kê theo giờ với các chỉ số (Giờ cao điểm, Giờ thấp điểm, Giờ trung bình, Phân bố đơn hàng Chart), bảng Top sản phẩm bán chạy Table với các cột (STT, Tên sản phẩm, Số lượng bán, Doanh thu, Tỷ lệ), bảng Top khách hàng Table với các cột (STT, Tên khách hàng, Số đơn hàng, Tổng chi tiêu, Hạng khách hàng Badge), biểu đồ phân tích Chart Group (Biểu đồ doanh thu theo ngày, Biểu đồ số lượng đơn hàng theo ngày, Biểu đồ tỷ lệ thành công theo ngày), các nút xuất báo cáo (Xuất PDF, Xuất Excel, In báo cáo, Gửi email) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-SLDH-02** | Lọc thống kê theo ngày | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/reports/orders-processed<br>3. Chọn ngày từ Date Picker<br>4. Click "Áp dụng" | Thống kê được lọc theo ngày đã chọn, tất cả dữ liệu thống kê được cập nhật chỉ hiển thị đơn hàng trong ngày đó, biểu đồ và bảng dữ liệu được cập nhật tương ứng | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-SLDH-03** | Lọc thống kê theo tuần | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/reports/orders-processed<br>3. Chọn tuần từ Week Picker<br>4. Click "Áp dụng" | Thống kê được lọc theo tuần đã chọn, tất cả dữ liệu thống kê được cập nhật chỉ hiển thị đơn hàng trong tuần đó, biểu đồ và bảng dữ liệu được cập nhật tương ứng | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-SLDH-04** | Lọc thống kê theo tháng | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/reports/orders-processed<br>3. Chọn tháng từ Month Picker<br>4. Click "Áp dụng" | Thống kê được lọc theo tháng đã chọn, tất cả dữ liệu thống kê được cập nhật chỉ hiển thị đơn hàng trong tháng đó, biểu đồ và bảng dữ liệu được cập nhật tương ứng | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-SLDH-05** | Lọc thống kê theo khoảng thời gian tùy chỉnh | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/reports/orders-processed<br>3. Chọn khoảng thời gian từ Date Range<br>4. Click "Áp dụng" | Thống kê được lọc theo khoảng thời gian đã chọn, tất cả dữ liệu thống kê được cập nhật chỉ hiển thị đơn hàng trong khoảng thời gian đó, biểu đồ và bảng dữ liệu được cập nhật tương ứng | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-SLDH-06** | Xem top sản phẩm bán chạy | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/reports/orders-processed<br>3. Xem bảng Top sản phẩm bán chạy | Hiển thị danh sách các sản phẩm bán chạy nhất với thông tin chi tiết: STT (số thứ tự xếp hạng), Tên sản phẩm, Số lượng bán, Doanh thu (format VNĐ), Tỷ lệ (%), sản phẩm được sắp xếp theo số lượng bán hoặc doanh thu từ cao xuống thấp, có thể có biểu đồ trực quan hóa dữ liệu | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-SLDH-07** | Xem top khách hàng | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/reports/orders-processed<br>3. Xem bảng Top khách hàng | Hiển thị danh sách các khách hàng mua nhiều nhất với thông tin chi tiết: STT (số thứ tự xếp hạng), Tên khách hàng, Số đơn hàng, Tổng chi tiêu (format VNĐ), Hạng khách hàng Badge, khách hàng được sắp xếp theo tổng chi tiêu hoặc số đơn hàng từ cao xuống thấp, có thể có biểu đồ trực quan hóa dữ liệu | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-SLDH-08** | Xuất báo cáo PDF | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/reports/orders-processed<br>3. Click nút "Xuất PDF" | File PDF báo cáo được tạo thành công, báo cáo bao gồm tất cả thông tin thống kê, file được tải xuống hoặc lưu vào thư mục, hiển thị thông báo thành công "Đã xuất báo cáo PDF" (toast success) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-SLDH-09** | Xuất báo cáo Excel | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/reports/orders-processed<br>3. Click nút "Xuất Excel" | File Excel báo cáo được tạo thành công, báo cáo bao gồm tất cả dữ liệu chi tiết trong bảng tính, file được tải xuống hoặc lưu vào thư mục, hiển thị thông báo thành công "Đã xuất báo cáo Excel" (toast success) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-SLDH-10** | Gửi email báo cáo | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/reports/orders-processed<br>3. Click nút "Gửi email"<br>4. Nhập email người nhận<br>5. Click "Gửi" | Hiển thị Dialog hoặc form với Input email người nhận, sau khi gửi: email báo cáo được gửi thành công, file PDF hoặc Excel được đính kèm, hiển thị thông báo thành công "Đã gửi email báo cáo" (toast success), người nhận nhận được email | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Báo cáo cuối ca

#### Check FUNC: Báo cáo cuối ca

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-BCCC-01** | Xem báo cáo cuối ca | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/reports/end-of-shift<br>3. Xem báo cáo | Hiển thị đầy đủ: tiêu đề "Báo cáo cuối ca làm việc", card Thông tin ca làm với thông tin (Ngày làm việc, Ca làm việc, Nhân viên, Thời gian bắt đầu, Thời gian kết thúc, Thời gian làm việc), card Tổng kết doanh thu với các chỉ số (Tổng doanh thu, Doanh thu tiền mặt với %, Doanh thu thẻ với %, Doanh thu chuyển khoản với %, Doanh thu ví điện tử với %), card Tổng kết đơn hàng với các chỉ số (Tổng số đơn hàng, Đơn hàng thành công với %, Đơn hàng đã hủy với %, Đơn hàng trực tiếp với %, Đơn hàng online với %), card Tổng kết sản phẩm với các chỉ số (Tổng số sản phẩm bán, Sản phẩm bán chạy nhất, Giá trị đơn hàng TB, Số khách hàng phục vụ), card Đánh giá hiệu suất với các chỉ số (Điểm hiệu suất, So sánh với ca trước, So sánh với trung bình, Ghi chú đánh giá Textarea), bảng chi tiết đơn hàng Table với các cột (Thời gian, Mã đơn hàng Link, Khách hàng, Sản phẩm, Tổng tiền, Phương thức thanh toán, Trạng thái Badge), biểu đồ tổng kết Chart Group (Biểu đồ doanh thu theo giờ, Biểu đồ doanh thu theo phương thức thanh toán, Biểu đồ số lượng đơn hàng theo giờ), các nút xác nhận (Xác nhận hoàn thành ca, Lưu báo cáo, Gửi báo cáo cho quản lý, In báo cáo) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-BCCC-02** | Xác nhận hoàn thành ca | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/reports/end-of-shift<br>3. Xem báo cáo<br>4. Click nút "Xác nhận hoàn thành ca"<br>5. Xác nhận trong Dialog | Hiển thị Dialog xác nhận với DialogTitle "Xác nhận hoàn thành ca làm việc", DialogDescription, nút "Hủy" và "Xác nhận". Sau khi xác nhận: ca làm việc được xác nhận hoàn thành, thông tin ca làm việc được lưu trữ vào hệ thống, trạng thái ca làm việc cập nhật thành "Đã hoàn thành", thông báo được gửi cho quản lý về việc hoàn thành ca làm việc, các chỉ số hiệu suất được tính toán tự động, hiển thị thông báo thành công "Đã xác nhận hoàn thành ca làm việc" (toast success), dialog đóng lại | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-BCCC-03** | Lưu báo cáo cuối ca | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/reports/end-of-shift<br>3. Click nút "Lưu báo cáo" | Báo cáo cuối ca được lưu vào hệ thống, tên file tự động đặt theo ngày và ca làm việc (VD: "BaoCaoCuoiCa_2024-01-22_CaSang.pdf"), file được lưu vào thư mục quy định, bản sao lưu trữ được tạo cho quản lý, lịch sử tạo báo cáo được ghi lại, hiển thị thông báo thành công "Đã lưu báo cáo cuối ca" (toast success) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-BCCC-04** | Gửi báo cáo cho quản lý | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/reports/end-of-shift<br>3. Click nút "Gửi báo cáo cho quản lý"<br>4. Xác nhận gửi | Email báo cáo cuối ca được gửi cho quản lý, thông tin quản lý được điền tự động, file PDF báo cáo được đính kèm, email có nội dung chuyên nghiệp, hiển thị thông báo thành công "Đã gửi báo cáo cho quản lý" (toast success), quản lý nhận được email, file đính kèm chính xác | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-BCCC-05** | In báo cáo cuối ca | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/reports/end-of-shift<br>3. Click nút "In báo cáo" | Bản xem trước báo cáo được hiển thị trước khi in, hỗ trợ tùy chỉnh kích thước và hướng in, báo cáo được in trực tiếp ra máy in, tự động lưu bản sao báo cáo trong hệ thống, hiển thị thông báo thành công "Đã in báo cáo" (toast success) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-BCCC-06** | Thêm ghi chú đánh giá | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/reports/end-of-shift<br>3. Nhập ghi chú vào Textarea "Ghi chú đánh giá"<br>4. Click "Lưu" | Ghi chú đánh giá được lưu thành công, hiển thị thông báo thành công "Đã lưu ghi chú" (toast success), ghi chú được hiển thị trong card "Đánh giá hiệu suất" | FUNC-DN-02 | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn MDX để dễ dàng quản lý và cập nhật test cases.*

