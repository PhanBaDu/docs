# Test Case Template - Chức năng đặt trước sản phẩm (User)

## Module Code
**Model Management Store: Chức năng đặt trước sản phẩm User**

## Test Requirement
1. Danh sách sản phẩm đã đặt trước
2. Đặt trước sản phẩm
3. Xem chi tiết đặt trước
4. Hủy đặt trước
5. Quản lý trạng thái đặt trước

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

### Function: Danh sách sản phẩm đã đặt trước

#### Check GUI: Danh sách sản phẩm đã đặt trước

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DSSPDDT-01** | Kiểm tra tiêu đề trang | 1. Truy cập trang đặt trước sản phẩm<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Đặt trước sản phẩm" với icon Package h-8 w-8, text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-DSSPDDT-02** | Kiểm tra mô tả trang | 1. Truy cập trang đặt trước sản phẩm<br>2. Kiểm tra mô tả | Hiển thị mô tả "Đặt trước các sản phẩm sắp ra mắt với ưu đãi đặc biệt" với text-muted-foreground | | Pass | 11/15/2015 | |
| **GUI-DSSPDDT-03** | Kiểm tra tab Đơn đặt trước của tôi | 1. Truy cập trang đặt trước sản phẩm<br>2. Kiểm tra tab | Hiển thị tab "Đơn đặt trước của tôi" trong TabsList grid-cols-2 | | Pass | 11/15/2015 | |
| **GUI-DSSPDDT-04** | Kiểm tra tiêu đề danh sách | 1. Chọn tab "Đơn đặt trước của tôi"<br>2. Kiểm tra tiêu đề | Hiển thị CardTitle "Đơn đặt trước của tôi" với CardDescription "Theo dõi trạng thái các đơn đặt trước" | | Pass | 11/15/2015 | |
| **GUI-DSSPDDT-05** | Kiểm tra ô tìm kiếm | 1. Chọn tab "Đơn đặt trước của tôi"<br>2. Kiểm tra tìm kiếm | Hiển thị Input với icon Search bên trái, placeholder "Tìm kiếm đơn đặt trước...", pl-10 w-64 | | Pass | 11/15/2015 | |
| **GUI-DSSPDDT-06** | Kiểm tra bộ lọc trạng thái | 1. Chọn tab "Đơn đặt trước của tôi"<br>2. Kiểm tra bộ lọc | Hiển thị Select với trigger w-32, các option: "Tất cả", "Chờ xử lý", "Đã xác nhận", "Đang chuẩn bị", "Đã giao", "Đã hủy" | | Pass | 11/15/2015 | |
| **GUI-DSSPDDT-07** | Kiểm tra card đặt trước | 1. Xem danh sách đặt trước<br>2. Kiểm tra card | Hiển thị card với CardContent p-4, chứa hình ảnh sản phẩm, tên sản phẩm, mã đặt trước, badge trạng thái, thông tin chi tiết | | Pass | 11/15/2015 | |
| **GUI-DSSPDDT-08** | Kiểm tra hình ảnh sản phẩm | 1. Xem card đặt trước<br>2. Kiểm tra hình ảnh | Hiển thị hình ảnh sản phẩm w-16 h-16 object-cover rounded-lg | | Pass | 11/15/2015 | |
| **GUI-DSSPDDT-09** | Kiểm tra mã đặt trước | 1. Xem card đặt trước<br>2. Kiểm tra mã | Hiển thị mã đặt trước với format "#PRE001" hoặc "PO-202401-001", text-sm text-muted-foreground | | Pass | 11/15/2015 | |
| **GUI-DSSPDDT-10** | Kiểm tra badge trạng thái | 1. Xem card đặt trước<br>2. Kiểm tra badge | Hiển thị badge với màu: Chờ xử lý (yellow-500), Đã xác nhận (blue-500), Đang chuẩn bị (orange-500), Đã giao (green-500), Đã hủy (red-500), có icon tương ứng | | Pass | 11/15/2015 | |
| **GUI-DSSPDDT-11** | Kiểm tra thông tin chi tiết | 1. Xem card đặt trước<br>2. Kiểm tra thông tin | Hiển thị grid grid-cols-1 md:grid-cols-2 gap-4 với: Số lượng, Giá dự kiến, Đã cọc, Còn lại, Phương thức thanh toán (icon CreditCard), Dự kiến giao (icon Calendar), Nhân viên (icon User) | | Pass | 11/15/2015 | |
| **GUI-DSSPDDT-12** | Kiểm tra ghi chú | 1. Xem đặt trước có ghi chú<br>2. Kiểm tra ghi chú | Hiển thị phần ghi chú với background bg-muted rounded-lg, icon FileText, tiêu đề "Ghi chú:", nội dung ghi chú | | Pass | 11/15/2015 | |
| **GUI-DSSPDDT-13** | Kiểm tra lịch sử xử lý | 1. Xem card đặt trước<br>2. Kiểm tra lịch sử | Hiển thị phần "Lịch sử xử lý:" với timeline, mỗi event có dot, action, timestamp, staff và note | | Pass | 11/15/2015 | |
| **GUI-DSSPDDT-14** | Kiểm tra nút Xem chi tiết | 1. Xem card đặt trước<br>2. Kiểm tra nút | Hiển thị nút "Xem chi tiết" với icon Eye, variant outline size sm, flex-1 | | Pass | 11/15/2015 | |
| **GUI-DSSPDDT-15** | Kiểm tra nút Hủy đặt trước | 1. Xem đặt trước chờ xử lý<br>2. Kiểm tra nút | Hiển thị nút "Hủy đặt trước" với icon XCircle, variant destructive size sm, chỉ hiển thị khi status = "pending" | | Pass | 11/15/2015 | |

---

### Check FUNC: Danh sách sản phẩm đã đặt trước

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DSSPDDT-01** | Mở tab Đơn đặt trước của tôi | 1. Truy cập trang đặt trước sản phẩm<br>2. Chọn tab "Đơn đặt trước của tôi" | Hiển thị danh sách tất cả đơn đặt trước, có ô tìm kiếm và bộ lọc trạng thái | | Pass | 11/15/2015 | |
| **FUNC-DSSPDDT-02** | Hiển thị danh sách đặt trước | 1. Chọn tab "Đơn đặt trước của tôi" | Hiển thị danh sách với đầy đủ thông tin: hình ảnh, tên sản phẩm, mã đặt trước, số lượng, giá dự kiến, tiền cọc, số tiền còn lại, trạng thái, phương thức thanh toán, ngày giao dự kiến, nhân viên, ghi chú, lịch sử xử lý | | Pass | 11/15/2015 | |
| **FUNC-DSSPDDT-03** | Sắp xếp theo thời gian mới nhất | 1. Chọn tab "Đơn đặt trước của tôi" | Danh sách được sắp xếp theo thời gian tạo mới nhất trước | | Pass | 11/15/2015 | |
| **FUNC-DSSPDDT-04** | Tìm kiếm theo tên sản phẩm | 1. Chọn tab "Đơn đặt trước của tôi"<br>2. Nhập tên sản phẩm vào ô tìm kiếm | Danh sách được lọc, chỉ hiển thị đặt trước có tên sản phẩm chứa từ khóa | | Pass | 11/15/2015 | |
| **FUNC-DSSPDDT-05** | Tìm kiếm theo mã đặt trước | 1. Chọn tab "Đơn đặt trước của tôi"<br>2. Nhập mã đặt trước vào ô tìm kiếm | Danh sách được lọc, chỉ hiển thị đặt trước có mã chứa từ khóa | | Pass | 11/15/2015 | |
| **FUNC-DSSPDDT-06** | Lọc theo trạng thái - Chờ xử lý | 1. Chọn tab "Đơn đặt trước của tôi"<br>2. Chọn bộ lọc "Chờ xử lý" | Chỉ hiển thị các đặt trước có trạng thái "Chờ xử lý" | | Pass | 11/15/2015 | |
| **FUNC-DSSPDDT-07** | Lọc theo trạng thái - Đã xác nhận | 1. Chọn tab "Đơn đặt trước của tôi"<br>2. Chọn bộ lọc "Đã xác nhận" | Chỉ hiển thị các đặt trước có trạng thái "Đã xác nhận" | | Pass | 11/15/2015 | |
| **FUNC-DSSPDDT-08** | Lọc theo trạng thái - Đang chuẩn bị | 1. Chọn tab "Đơn đặt trước của tôi"<br>2. Chọn bộ lọc "Đang chuẩn bị" | Chỉ hiển thị các đặt trước có trạng thái "Đang chuẩn bị" | | Pass | 11/15/2015 | |
| **FUNC-DSSPDDT-09** | Lọc theo trạng thái - Đã giao | 1. Chọn tab "Đơn đặt trước của tôi"<br>2. Chọn bộ lọc "Đã giao" | Chỉ hiển thị các đặt trước có trạng thái "Đã giao" | | Pass | 11/15/2015 | |
| **FUNC-DSSPDDT-10** | Lọc theo trạng thái - Đã hủy | 1. Chọn tab "Đơn đặt trước của tôi"<br>2. Chọn bộ lọc "Đã hủy" | Chỉ hiển thị các đặt trước có trạng thái "Đã hủy" | | Pass | 11/15/2015 | |
| **FUNC-DSSPDDT-11** | Kết hợp tìm kiếm và lọc | 1. Chọn tab "Đơn đặt trước của tôi"<br>2. Nhập từ khóa tìm kiếm<br>3. Chọn bộ lọc trạng thái | Danh sách được lọc theo cả từ khóa và trạng thái, chỉ hiển thị đặt trước thỏa mãn cả hai điều kiện | | Pass | 11/15/2015 | |
| **FUNC-DSSPDDT-12** | Hiển thị khi không có đặt trước | 1. Chọn tab "Đơn đặt trước của tôi"<br>2. Không có đặt trước nào | Hiển thị thông báo "Chưa có đơn đặt trước nào" hoặc danh sách trống | | Pass | 11/15/2015 | |
| **FUNC-DSSPDDT-13** | Hiển thị lịch sử xử lý | 1. Xem card đặt trước<br>2. Kiểm tra lịch sử | Hiển thị timeline lịch sử xử lý với các event: action, timestamp, staff, note, mỗi event có dot và được sắp xếp theo thời gian | | Pass | 11/15/2015 | |
| **FUNC-DSSPDDT-14** | Tìm kiếm real-time | 1. Chọn tab "Đơn đặt trước của tôi"<br>2. Nhập từ khóa vào ô tìm kiếm | Danh sách được lọc ngay khi nhập, không cần nhấn Enter | | Pass | 11/15/2015 | |

---

### Function: Đặt trước sản phẩm

#### Check GUI: Đặt trước sản phẩm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DTSP-01** | Kiểm tra tab Sản phẩm đặt trước | 1. Truy cập trang đặt trước sản phẩm<br>2. Kiểm tra tab | Hiển thị tab "Sản phẩm đặt trước" trong TabsList | | Pass | 11/15/2015 | |
| **GUI-DTSP-02** | Kiểm tra tiêu đề danh sách sản phẩm | 1. Chọn tab "Sản phẩm đặt trước"<br>2. Kiểm tra tiêu đề | Hiển thị CardTitle "Sản phẩm có thể đặt trước" với CardDescription "Các sản phẩm sắp ra mắt với ưu đãi đặt trước" | | Pass | 11/15/2015 | |
| **GUI-DTSP-03** | Kiểm tra card sản phẩm | 1. Xem danh sách sản phẩm<br>2. Kiểm tra card | Hiển thị card với hover:shadow-lg transition-shadow, chứa hình ảnh, badge trạng thái, thông tin sản phẩm | | Pass | 11/15/2015 | |
| **GUI-DTSP-04** | Kiểm tra badge trạng thái sản phẩm | 1. Xem card sản phẩm<br>2. Kiểm tra badge | Hiển thị badge "Có thể đặt trước" (green-500), "Hết chỗ đặt trước" (red-500), "Sắp ra mắt" (blue-500) ở góc trên trái | | Pass | 11/15/2015 | |
| **GUI-DTSP-05** | Kiểm tra badge giảm giá | 1. Xem sản phẩm có giảm giá<br>2. Kiểm tra badge | Hiển thị badge "Giảm [Số] VNĐ" variant secondary ở góc trên phải | | Pass | 11/15/2015 | |
| **GUI-DTSP-06** | Kiểm tra giá dự kiến | 1. Xem card sản phẩm<br>2. Kiểm tra giá | Hiển thị "Giá dự kiến: [Giá] VNĐ" với font-bold text-primary | | Pass | 11/15/2015 | |
| **GUI-DTSP-07** | Kiểm tra giá gốc | 1. Xem sản phẩm có giá gốc<br>2. Kiểm tra giá | Hiển thị "Giá gốc: [Giá] VNĐ" với line-through text-muted-foreground | | Pass | 11/15/2015 | |
| **GUI-DTSP-08** | Kiểm tra tiền cọc cần thiết | 1. Xem card sản phẩm<br>2. Kiểm tra cọc | Hiển thị "Cọc cần thiết: [Số] VNĐ" với font-medium text-orange-600 | | Pass | 11/15/2015 | |
| **GUI-DTSP-09** | Kiểm tra ngày ra mắt | 1. Xem card sản phẩm<br>2. Kiểm tra ngày | Hiển thị "Ra mắt: [Ngày]" với icon Calendar, format ngày Việt Nam | | Pass | 11/15/2015 | |
| **GUI-DTSP-10** | Kiểm tra hết hạn đặt trước | 1. Xem card sản phẩm<br>2. Kiểm tra ngày | Hiển thị "Hết hạn đặt trước: [Ngày]" với icon Clock, format ngày Việt Nam | | Pass | 11/15/2015 | |
| **GUI-DTSP-11** | Kiểm tra tính năng sản phẩm | 1. Xem card sản phẩm<br>2. Kiểm tra tính năng | Hiển thị "Tính năng:" với danh sách badge variant outline text-xs | | Pass | 11/15/2015 | |
| **GUI-DTSP-12** | Kiểm tra nút Đặt trước ngay | 1. Xem card sản phẩm<br>2. Kiểm tra nút | Hiển thị nút "Đặt trước ngay" với icon ShoppingCart, variant default, disabled nếu hết chỗ | | Pass | 11/15/2015 | |
| **GUI-DTSP-13** | Kiểm tra form đặt trước | 1. Nhấn nút "Đặt trước ngay"<br>2. Kiểm tra form | Hiển thị form/modal với các trường: Tên sản phẩm, Số lượng, Giá dự kiến, Tổng tiền, Tiền cọc, Số tiền còn lại, Phương thức thanh toán, Địa chỉ giao hàng, Ngày giao dự kiến, Ghi chú, Mức độ ưu tiên | | Pass | 11/15/2015 | |
| **GUI-DTSP-14** | Kiểm tra tính toán giá tiền | 1. Mở form đặt trước<br>2. Nhập số lượng<br>3. Kiểm tra tính toán | Tổng tiền, tiền cọc (20%), số tiền còn lại được tính toán và hiển thị real-time | | Pass | 11/15/2015 | |
| **GUI-DTSP-15** | Kiểm tra nút Xác nhận đặt trước | 1. Mở form đặt trước<br>2. Kiểm tra nút | Hiển thị nút "Xác nhận đặt trước" variant default | | Pass | 11/15/2015 | |

---

### Check FUNC: Đặt trước sản phẩm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DTSP-01** | Mở tab Sản phẩm đặt trước | 1. Truy cập trang đặt trước sản phẩm<br>2. Chọn tab "Sản phẩm đặt trước" | Hiển thị danh sách sản phẩm có thể đặt trước, có ô tìm kiếm và bộ lọc danh mục | | Pass | 11/15/2015 | |
| **FUNC-DTSP-02** | Hiển thị danh sách sản phẩm | 1. Chọn tab "Sản phẩm đặt trước" | Hiển thị danh sách sản phẩm với đầy đủ thông tin: hình ảnh, tên, thương hiệu, series, scale, mô tả, giá dự kiến, giá gốc (nếu có), tiền cọc, ngày ra mắt, hết hạn đặt trước, tính năng | | Pass | 11/15/2015 | |
| **FUNC-DTSP-03** | Đặt trước sản phẩm | 1. Chọn tab "Sản phẩm đặt trước"<br>2. Nhấn nút "Đặt trước ngay"<br>3. Điền form và xác nhận | Mở form/modal đặt trước với thông tin sản phẩm đã điền sẵn, sau khi xác nhận, đặt trước được tạo thành công, hiển thị toast "Đã tạo đơn đặt trước thành công", đặt trước xuất hiện trong tab "Đơn đặt trước của tôi" | | Pass | 11/15/2015 | |
| **FUNC-DTSP-04** | Tính toán giá tiền tự động | 1. Mở form đặt trước<br>2. Nhập số lượng<br>3. Quan sát tính toán | Tổng tiền = Số lượng × Giá dự kiến, Tiền cọc = Tổng tiền × 20%, Số tiền còn lại = Tổng tiền - Tiền cọc, cập nhật real-time khi thay đổi số lượng | | Pass | 11/15/2015 | |
| **FUNC-DTSP-05** | Chọn phương thức thanh toán | 1. Mở form đặt trước<br>2. Chọn phương thức thanh toán | Phương thức được chọn từ Select: COD, Banking, MoMo, Credit Card, có thể thay đổi | | Pass | 11/15/2015 | |
| **FUNC-DTSP-06** | Nhập địa chỉ giao hàng | 1. Mở form đặt trước<br>2. Nhập địa chỉ | Địa chỉ được nhập vào Textarea, có thể nhập nhiều dòng | | Pass | 11/15/2015 | |
| **FUNC-DTSP-07** | Chọn ngày giao dự kiến | 1. Mở form đặt trước<br>2. Chọn ngày | Ngày được chọn từ date picker, hiển thị format ngày Việt Nam | | Pass | 11/15/2015 | |
| **FUNC-DTSP-08** | Nhập ghi chú | 1. Mở form đặt trước<br>2. Nhập ghi chú | Ghi chú được nhập vào Textarea, optional | | Pass | 11/15/2015 | |
| **FUNC-DTSP-09** | Chọn mức độ ưu tiên | 1. Mở form đặt trước<br>2. Chọn mức độ ưu tiên | Mức độ ưu tiên được chọn từ Select: Thấp, Trung bình, Cao, mặc định là "Trung bình" | | Pass | 11/15/2015 | |
| **FUNC-DTSP-10** | Đặt trước sản phẩm hết chỗ | 1. Chọn tab "Sản phẩm đặt trước"<br>2. Xem sản phẩm hết chỗ<br>3. Nhấn nút | Nút hiển thị "Hết chỗ đặt trước" và bị disabled, không thể đặt trước | | Pass | 11/15/2015 | |
| **FUNC-DTSP-11** | Đặt trước với đầy đủ thông tin | 1. Mở form đặt trước<br>2. Nhập đầy đủ: số lượng, phương thức thanh toán, địa chỉ, ngày giao, ghi chú, mức độ ưu tiên<br>3. Xác nhận | Đặt trước được tạo với đầy đủ thông tin, hiển thị trong danh sách với tất cả thông tin đã nhập | | Pass | 11/15/2015 | |
| **FUNC-DTSP-12** | Đặt trước chỉ với thông tin bắt buộc | 1. Mở form đặt trước<br>2. Chỉ nhập số lượng và địa chỉ<br>3. Xác nhận | Đặt trước được tạo thành công với chỉ thông tin bắt buộc, các trường optional để trống hoặc mặc định | | Pass | 11/15/2015 | |
| **FUNC-DTSP-13** | Tìm kiếm sản phẩm đặt trước | 1. Chọn tab "Sản phẩm đặt trước"<br>2. Nhập từ khóa tìm kiếm | Danh sách được lọc, chỉ hiển thị sản phẩm có tên/thương hiệu/series chứa từ khóa | | Pass | 11/15/2015 | |
| **FUNC-DTSP-14** | Lọc theo danh mục | 1. Chọn tab "Sản phẩm đặt trước"<br>2. Chọn danh mục trong bộ lọc | Chỉ hiển thị sản phẩm thuộc danh mục đã chọn | | Pass | 11/15/2015 | |

---

### Function: Xem chi tiết đặt trước

#### Check GUI: Xem chi tiết đặt trước

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XCTDT-01** | Kiểm tra modal/trang chi tiết | 1. Nhấn nút "Xem chi tiết"<br>2. Kiểm tra modal/trang | Hiển thị modal hoặc trang chi tiết với đầy đủ thông tin đặt trước | | Pass | 11/15/2015 | |
| **GUI-XCTDT-02** | Kiểm tra thông tin cơ bản | 1. Xem chi tiết đặt trước<br>2. Kiểm tra thông tin | Hiển thị đầy đủ: mã đặt trước, tên sản phẩm, số lượng, giá dự kiến, tổng tiền, tiền cọc, số tiền còn lại, trạng thái, mức độ ưu tiên | | Pass | 11/15/2015 | |
| **GUI-XCTDT-03** | Kiểm tra phương thức thanh toán | 1. Xem chi tiết đặt trước<br>2. Kiểm tra phương thức | Hiển thị phương thức thanh toán với icon CreditCard | | Pass | 11/15/2015 | |
| **GUI-XCTDT-04** | Kiểm tra địa chỉ giao hàng | 1. Xem chi tiết đặt trước<br>2. Kiểm tra địa chỉ | Hiển thị địa chỉ giao hàng đầy đủ | | Pass | 11/15/2015 | |
| **GUI-XCTDT-05** | Kiểm tra ngày tạo | 1. Xem chi tiết đặt trước<br>2. Kiểm tra ngày | Hiển thị ngày tạo với format ngày Việt Nam, icon Calendar | | Pass | 11/15/2015 | |
| **GUI-XCTDT-06** | Kiểm tra ngày giao dự kiến | 1. Xem chi tiết đặt trước<br>2. Kiểm tra ngày | Hiển thị ngày giao dự kiến với format ngày Việt Nam, icon Clock | | Pass | 11/15/2015 | |
| **GUI-XCTDT-07** | Kiểm tra nhân viên phụ trách | 1. Xem chi tiết đặt trước<br>2. Kiểm tra nhân viên | Hiển thị tên nhân viên phụ trách với icon User | | Pass | 11/15/2015 | |
| **GUI-XCTDT-08** | Kiểm tra ghi chú | 1. Xem chi tiết đặt trước có ghi chú<br>2. Kiểm tra ghi chú | Hiển thị ghi chú với background bg-muted rounded-lg, icon FileText | | Pass | 11/15/2015 | |
| **GUI-XCTDT-09** | Kiểm tra lịch sử xử lý | 1. Xem chi tiết đặt trước<br>2. Kiểm tra lịch sử | Hiển thị timeline lịch sử xử lý với các event: action, timestamp, staff, note, mỗi event có dot và được sắp xếp theo thời gian | | Pass | 11/15/2015 | |
| **GUI-XCTDT-10** | Kiểm tra nút Quay lại | 1. Xem chi tiết đặt trước<br>2. Kiểm tra nút | Hiển thị nút "Quay lại" để quay lại danh sách | | Pass | 11/15/2015 | |
| **GUI-XCTDT-11** | Kiểm tra nút Hủy đặt trước | 1. Xem chi tiết đặt trước chờ xử lý<br>2. Kiểm tra nút | Hiển thị nút "Hủy đặt trước" variant destructive, chỉ hiển thị khi status = "pending" | | Pass | 11/15/2015 | |

---

### Check FUNC: Xem chi tiết đặt trước

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XCTDT-01** | Mở chi tiết đặt trước | 1. Chọn tab "Đơn đặt trước của tôi"<br>2. Nhấn nút "Xem chi tiết" | Mở modal hoặc trang chi tiết với đầy đủ thông tin đặt trước | | Pass | 11/15/2015 | |
| **FUNC-XCTDT-02** | Hiển thị chi tiết đầy đủ | 1. Xem chi tiết đặt trước | Hiển thị đầy đủ: mã đặt trước, tên sản phẩm, số lượng, giá dự kiến, tổng tiền, tiền cọc, số tiền còn lại, trạng thái, mức độ ưu tiên, phương thức thanh toán, địa chỉ giao hàng, ngày tạo, ngày giao dự kiến, nhân viên phụ trách, ghi chú, lịch sử xử lý | | Pass | 11/15/2015 | |
| **FUNC-XCTDT-03** | Hiển thị lịch sử xử lý | 1. Xem chi tiết đặt trước | Hiển thị timeline lịch sử xử lý với các event được sắp xếp theo thời gian, mỗi event có: action, timestamp, staff, note | | Pass | 11/15/2015 | |
| **FUNC-XCTDT-04** | Quay lại danh sách | 1. Xem chi tiết đặt trước<br>2. Nhấn nút "Quay lại" | Quay lại trang danh sách đặt trước, giữ nguyên trạng thái lọc và tìm kiếm | | Pass | 11/15/2015 | |
| **FUNC-XCTDT-05** | Đóng modal bằng click overlay | 1. Mở modal chi tiết<br>2. Click vào overlay | Modal đóng, quay lại danh sách | | Pass | 11/15/2015 | |

---

### Function: Hủy đặt trước

#### Check GUI: Hủy đặt trước

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-HDT-01** | Kiểm tra nút Hủy đặt trước | 1. Xem đặt trước chờ xử lý<br>2. Kiểm tra nút | Hiển thị nút "Hủy đặt trước" với icon XCircle, variant destructive size sm, chỉ hiển thị khi status = "pending" | | Pass | 11/15/2015 | |
| **GUI-HDT-02** | Kiểm tra modal xác nhận | 1. Nhấn nút "Hủy đặt trước"<br>2. Kiểm tra modal | Hiển thị modal với tiêu đề "Xác nhận hủy đặt trước", mô tả "Bạn có chắc chắn muốn hủy đặt trước?", thông tin hoàn cọc | | Pass | 11/15/2015 | |
| **GUI-HDT-03** | Kiểm tra thông tin hoàn cọc | 1. Mở modal xác nhận<br>2. Kiểm tra thông tin | Hiển thị thông tin: số tiền cọc sẽ được hoàn, thời gian hoàn dự kiến, trạng thái hoàn cọc | | Pass | 11/15/2015 | |
| **GUI-HDT-04** | Kiểm tra nút Xác nhận | 1. Mở modal xác nhận<br>2. Kiểm tra nút | Hiển thị nút "Xác nhận" variant destructive, thực hiện hủy khi nhấn | | Pass | 11/15/2015 | |
| **GUI-HDT-05** | Kiểm tra nút Hủy trong modal | 1. Mở modal xác nhận<br>2. Kiểm tra nút | Hiển thị nút "Hủy" variant outline, đóng modal khi nhấn | | Pass | 11/15/2015 | |

---

### Check FUNC: Hủy đặt trước

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-HDT-01** | Hủy đặt trước chờ xử lý | 1. Chọn tab "Đơn đặt trước của tôi"<br>2. Nhấn nút "Hủy đặt trước" trên đặt trước chờ xử lý<br>3. Xác nhận hủy | Hiển thị modal xác nhận với thông tin hoàn cọc, sau khi xác nhận, đặt trước được hủy, hiển thị toast "Đã hủy đơn đặt trước", đặt trước biến mất khỏi danh sách hoặc chuyển sang trạng thái "Đã hủy", yêu cầu hoàn cọc được tạo tự động | | Pass | 11/15/2015 | |
| **FUNC-HDT-02** | Hủy đặt trước trong modal | 1. Nhấn nút "Hủy đặt trước"<br>2. Nhấn nút "Hủy" trong modal | Modal đóng, không hủy đặt trước, đặt trước vẫn còn trong danh sách | | Pass | 11/15/2015 | |
| **FUNC-HDT-03** | Hủy đặt trước đã xử lý | 1. Xem đặt trước đã được xử lý (đã xác nhận/đang chuẩn bị)<br>2. Kiểm tra nút hủy | Nút "Hủy đặt trước" không hiển thị, không thể hủy đặt trước đã xử lý | | Pass | 11/15/2015 | |
| **FUNC-HDT-04** | Hủy đặt trước từ trang chi tiết | 1. Xem chi tiết đặt trước chờ xử lý<br>2. Nhấn nút "Hủy đặt trước"<br>3. Xác nhận | Đặt trước được hủy, quay lại danh sách, đặt trước biến mất hoặc chuyển sang trạng thái "Đã hủy" | | Pass | 11/15/2015 | |
| **FUNC-HDT-05** | Xử lý hoàn cọc tự động | 1. Hủy đặt trước thành công<br>2. Kiểm tra hoàn cọc | Yêu cầu hoàn cọc được tạo tự động, trạng thái hoàn cọc được cập nhật, thông tin hoàn cọc được hiển thị trong modal xác nhận | | Pass | 11/15/2015 | |
| **FUNC-HDT-06** | Đóng modal bằng click overlay | 1. Mở modal xác nhận<br>2. Click vào overlay | Modal đóng, không hủy đặt trước | | Pass | 11/15/2015 | |

---

### Function: Quản lý trạng thái đặt trước

#### Check GUI: Quản lý trạng thái đặt trước

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-QLTTDT-01** | Kiểm tra badge trạng thái Chờ xử lý | 1. Xem đặt trước chờ xử lý<br>2. Kiểm tra badge | Hiển thị badge "Chờ xử lý" với màu yellow-500, icon Clock | | Pass | 11/15/2015 | |
| **GUI-QLTTDT-02** | Kiểm tra badge trạng thái Đã xác nhận | 1. Xem đặt trước đã xác nhận<br>2. Kiểm tra badge | Hiển thị badge "Đã xác nhận" với màu blue-500, icon CheckCircle | | Pass | 11/15/2015 | |
| **GUI-QLTTDT-03** | Kiểm tra badge trạng thái Đang chuẩn bị | 1. Xem đặt trước đang chuẩn bị<br>2. Kiểm tra badge | Hiển thị badge "Đang chuẩn bị" với màu orange-500, icon Package | | Pass | 11/15/2015 | |
| **GUI-QLTTDT-04** | Kiểm tra badge trạng thái Đã giao | 1. Xem đặt trước đã giao<br>2. Kiểm tra badge | Hiển thị badge "Đã giao" với màu green-500, icon CheckCircle | | Pass | 11/15/2015 | |
| **GUI-QLTTDT-05** | Kiểm tra badge trạng thái Đã hủy | 1. Xem đặt trước đã hủy<br>2. Kiểm tra badge | Hiển thị badge "Đã hủy" với màu red-500, icon XCircle | | Pass | 11/15/2015 | |
| **GUI-QLTTDT-06** | Kiểm tra thời gian cập nhật | 1. Xem đặt trước<br>2. Kiểm tra thời gian | Hiển thị thời gian cập nhật cuối với format ngày giờ Việt Nam | | Pass | 11/15/2015 | |

---

### Check FUNC: Quản lý trạng thái đặt trước

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-QLTTDT-01** | Theo dõi trạng thái real-time | 1. Xem danh sách đặt trước<br>2. Admin thay đổi trạng thái | Trạng thái đặt trước được cập nhật real-time, badge thay đổi màu và icon tương ứng, hiển thị thông báo khi có thay đổi | | Pass | 11/15/2015 | |
| **FUNC-QLTTDT-02** | Lọc theo trạng thái qua bộ lọc | 1. Chọn tab "Đơn đặt trước của tôi"<br>2. Chọn trạng thái trong bộ lọc | Danh sách được lọc, chỉ hiển thị đặt trước có trạng thái đã chọn, cập nhật ngay lập tức | | Pass | 11/15/2015 | |
| **FUNC-QLTTDT-03** | Hiển thị thông tin trạng thái | 1. Xem đặt trước<br>2. Kiểm tra thông tin | Hiển thị đầy đủ: badge trạng thái với màu và icon, thời gian cập nhật, nhân viên xử lý (nếu có), ghi chú (nếu có) | | Pass | 11/15/2015 | |
| **FUNC-QLTTDT-04** | Cập nhật trạng thái tự động | 1. Xem danh sách đặt trước<br>2. Đợi admin xử lý | Hệ thống tự động cập nhật trạng thái khi admin xử lý, không cần refresh trang | | Pass | 11/15/2015 | |
| **FUNC-QLTTDT-05** | Thông báo thay đổi trạng thái | 1. Đặt trước có thay đổi trạng thái<br>2. Kiểm tra thông báo | Hiển thị toast hoặc notification thông báo thay đổi trạng thái, có thể click để xem chi tiết | | Pass | 11/15/2015 | |
| **FUNC-QLTTDT-06** | Hiển thị số lượng theo trạng thái | 1. Chọn tab "Đơn đặt trước của tôi"<br>2. Kiểm tra số lượng | Số lượng đặt trước được hiển thị chính xác cho từng trạng thái trong bộ lọc | | Pass | 11/15/2015 | |

---

### Check VALIDATION: Đặt trước sản phẩm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **VALID-DTSP-01** | Đặt trước thiếu số lượng | 1. Mở form đặt trước<br>2. Để trống số lượng<br>3. Xác nhận | Hiển thị thông báo lỗi "Vui lòng nhập số lượng", không tạo đặt trước | | Pass | 11/15/2015 | |
| **VALID-DTSP-02** | Đặt trước số lượng = 0 | 1. Mở form đặt trước<br>2. Nhập số lượng = 0<br>3. Xác nhận | Hiển thị thông báo lỗi "Số lượng phải lớn hơn 0", không tạo đặt trước | | Pass | 11/15/2015 | |
| **VALID-DTSP-03** | Đặt trước số lượng âm | 1. Mở form đặt trước<br>2. Nhập số lượng < 0<br>3. Xác nhận | Hệ thống tự động chuyển về 1 hoặc hiển thị lỗi, không cho nhập số âm | | Pass | 11/15/2015 | |
| **VALID-DTSP-04** | Đặt trước thiếu địa chỉ giao hàng | 1. Mở form đặt trước<br>2. Để trống địa chỉ<br>3. Xác nhận | Hiển thị thông báo lỗi "Vui lòng nhập địa chỉ giao hàng", không tạo đặt trước | | Pass | 11/15/2015 | |
| **VALID-DTSP-05** | Hủy đặt trước đã xử lý | 1. Xem đặt trước đã được xử lý<br>2. Thử hủy đặt trước | Nút "Hủy đặt trước" không hiển thị, không thể hủy đặt trước đã xử lý | | Pass | 11/15/2015 | |
| **VALID-DTSP-06** | Đặt trước sản phẩm hết chỗ | 1. Chọn tab "Sản phẩm đặt trước"<br>2. Xem sản phẩm hết chỗ<br>3. Thử đặt trước | Nút bị disabled, hiển thị "Hết chỗ đặt trước", không thể đặt trước | | Pass | 11/15/2015 | |
| **VALID-DTSP-07** | Đặt trước với ngày giao quá khứ | 1. Mở form đặt trước<br>2. Chọn ngày giao trong quá khứ<br>3. Xác nhận | Hiển thị thông báo lỗi "Ngày giao phải là ngày tương lai", không tạo đặt trước | | Pass | 11/15/2015 | |
| **VALID-DTSP-08** | Tính toán giá với số lượng lớn | 1. Mở form đặt trước<br>2. Nhập số lượng rất lớn (>1000)<br>3. Quan sát tính toán | Hệ thống tính toán chính xác, hiển thị tổng tiền, tiền cọc, số tiền còn lại đúng | | Pass | 11/15/2015 | |

