# Test Case Template - Xử lý đặt trước (Admin)

## Module Code
**Model Management Store: Xử lý đặt trước Admin**

## Test Requirement
1. Hiển thị danh sách đặt trước
2. Xem chi tiết đặt trước
3. Xử lý đặt trước
4. Cập nhật trạng thái đặt trước
5. Thông báo có hàng

---

## Test Summary

### Người thực hiện Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 60 |
| **Fail** | 0 |
| **Untested** | 50 |
| **N/A** | 0 |
| **Number of Test cases** | 110 |

---

## Test Cases

### Function: Hiển thị danh sách đặt trước

#### Check GUI: Hiển thị danh sách đặt trước

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DSDT-01** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/pre-orders<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Xử lý đặt trước" với kích thước text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-DSDT-02** | Kiểm tra mô tả chức năng | 1. Truy cập /admin/pre-orders<br>2. Kiểm tra mô tả | Hiển thị mô tả "Quản lý và xử lý các đơn hàng đặt trước từ khách hàng" màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-DSDT-03** | Kiểm tra Stats Cards | 1. Truy cập /admin/pre-orders<br>2. Kiểm tra Stats Cards | Hiển thị 5 card thống kê: Tổng đơn đặt trước, Chờ xử lý, Đã xác nhận, Đang chuẩn bị, Đã giao, Tổng giá trị | | Pass | 11/15/2015 | |
| **GUI-DSDT-04** | Kiểm tra trường Tìm kiếm | 1. Truy cập /admin/pre-orders<br>2. Kiểm tra trường tìm kiếm | Hiển thị input với icon Search bên trái, placeholder "Tìm kiếm đơn hàng đặt trước theo ID, tên khách hàng, hoặc tên sản phẩm...", có thể nhập và nhấn Enter để tìm | | Pass | 11/15/2015 | |
| **GUI-DSDT-05** | Kiểm tra Select Trạng thái | 1. Truy cập /admin/pre-orders<br>2. Kiểm tra Select Trạng thái | Hiển thị Select với placeholder "Trạng thái", width w-40, có các option: Tất cả, Chờ xử lý, Đã xác nhận, Đang chuẩn bị, Đã giao, Đã hủy | | Pass | 11/15/2015 | |
| **GUI-DSDT-06** | Kiểm tra Select Loại sản phẩm | 1. Truy cập /admin/pre-orders<br>2. Kiểm tra Select | Hiển thị Select với placeholder "Loại sản phẩm", width w-40, có các option: Tất cả, Gundam, Figure, Mô hình xe, Máy bay, Khác | | Pass | 11/15/2015 | |
| **GUI-DSDT-07** | Kiểm tra Date Range | 1. Truy cập /admin/pre-orders<br>2. Kiểm tra Date Range | Hiển thị 2 input date với text "đến" ở giữa, width w-40 mỗi input | | Pass | 11/15/2015 | |
| **GUI-DSDT-08** | Kiểm tra nút Bộ lọc | 1. Truy cập /admin/pre-orders<br>2. Kiểm tra nút | Hiển thị nút "Bộ lọc" với icon Filter variant outline | | Pass | 11/15/2015 | |
| **GUI-DSDT-09** | Kiểm tra bảng danh sách đặt trước | 1. Truy cập /admin/pre-orders<br>2. Kiểm tra bảng | Hiển thị Table với các cột: ID đơn hàng, Khách hàng, Sản phẩm, Tổng giá trị, Trạng thái, Ngày tạo, Thao tác | | Pass | 11/15/2015 | |
| **GUI-DSDT-10** | Kiểm tra cột ID đơn hàng trong bảng | 1. Truy cập /admin/pre-orders<br>2. Kiểm tra cột ID đơn hàng | Mỗi dòng hiển thị ID đơn hàng (font-medium, VD: #PRE001) kèm Badge trạng thái | | Pass | 11/15/2015 | |
| **GUI-DSDT-11** | Kiểm tra cột Khách hàng trong bảng | 1. Truy cập /admin/pre-orders<br>2. Kiểm tra cột Khách hàng | Hiển thị tên khách hàng (font-medium), email (text-sm muted-foreground), SĐT (text-sm muted-foreground), Hạng (Badge) | | Pass | 11/15/2015 | |
| **GUI-DSDT-12** | Kiểm tra cột Sản phẩm trong bảng | 1. Truy cập /admin/pre-orders<br>2. Kiểm tra cột Sản phẩm | Hiển thị danh sách sản phẩm với tên và số lượng (VD: Gundam RX-78-2 (x1), Figure Saber (x2)) | | Pass | 11/15/2015 | |
| **GUI-DSDT-13** | Kiểm tra cột Tổng giá trị trong bảng | 1. Truy cập /admin/pre-orders<br>2. Kiểm tra cột Tổng giá trị | Hiển thị tổng giá trị dự kiến (VD: 15.000.000 VNĐ) | | Pass | 11/15/2015 | |
| **GUI-DSDT-14** | Kiểm tra cột Trạng thái trong bảng | 1. Truy cập /admin/pre-orders<br>2. Kiểm tra cột Trạng thái | Hiển thị Badge với icon và màu tương ứng: Chờ xử lý (Clock icon màu vàng, secondary), Đã xác nhận (CheckCircle icon màu xanh, default), Đang chuẩn bị (Package icon màu xanh dương, outline), Đã giao (Truck icon màu xanh lá, outline), Đã hủy (XCircle icon màu đỏ, destructive) | | Pass | 11/15/2015 | |
| **GUI-DSDT-15** | Kiểm tra cột Ngày tạo trong bảng | 1. Truy cập /admin/pre-orders<br>2. Kiểm tra cột Ngày tạo | Hiển thị ngày tạo đơn hàng (text-sm, VD: 2023-10-26 10:30) | | Pass | 11/15/2015 | |
| **GUI-DSDT-16** | Kiểm tra cột Thao tác trong bảng | 1. Truy cập /admin/pre-orders<br>2. Kiểm tra cột Thao tác | Hiển thị các nút: Xem (icon Eye link đến /admin/pre-orders/[id]), Cập nhật trạng thái (icon CheckCircle), Xử lý (icon Package), Thông báo có hàng (icon Bell), tất cả variant ghost size sm | | Pass | 11/15/2015 | |
| **GUI-DSDT-17** | Kiểm tra Pagination | 1. Truy cập /admin/pre-orders<br>2. Kiểm tra Pagination | Hiển thị text "Hiển thị 1-X trong Y đơn đặt trước", các nút phân trang: Trước (disabled), số trang, Sau | | Pass | 11/15/2015 | |
| **GUI-DSDT-18** | Kiểm tra Sidebar | 1. Truy cập /admin/pre-orders<br>2. Kiểm tra Sidebar | Hiển thị Sidebar với: Hành động nhanh (nút Tạo đơn đặt trước mới), Tóm tắt trạng thái (Chart Doughnut), Hoạt động gần đây (List) | | Pass | 11/15/2015 | |

---

### Check FUNC: Hiển thị danh sách đặt trước

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DSDT-01** | Mở trang danh sách đặt trước | 1. Truy cập /admin/pre-orders | Hiển thị trang với tiêu đề, mô tả, 5 Stats Cards, bộ lọc (tìm kiếm, trạng thái, loại sản phẩm, date range, nút Bộ lọc), bảng danh sách đặt trước, pagination, sidebar | | Pass | 11/15/2015 | |
| **FUNC-DSDT-02** | Hiển thị danh sách đặt trước mặc định | 1. Truy cập /admin/pre-orders | Hiển thị tất cả đơn đặt trước trong bảng, mỗi đơn có đầy đủ thông tin: ID đơn hàng, khách hàng, sản phẩm, tổng giá trị, trạng thái, ngày tạo, các nút thao tác | | Pass | 11/15/2015 | |
| **FUNC-DSDT-03** | Click nút Xem (icon Eye) | 1. Truy cập /admin/pre-orders<br>2. Click nút Xem của một đơn đặt trước | Chuyển đến trang chi tiết đơn đặt trước /admin/pre-orders/[id] | | Pass | 11/15/2015 | |
| **FUNC-DSDT-04** | Click nút Cập nhật trạng thái (icon CheckCircle) | 1. Truy cập /admin/pre-orders<br>2. Click nút Cập nhật trạng thái của một đơn | Mở modal cập nhật trạng thái đơn đặt trước | | Pass | 11/15/2015 | |
| **FUNC-DSDT-05** | Click nút Xử lý (icon Package) | 1. Truy cập /admin/pre-orders<br>2. Click nút Xử lý của một đơn | Mở modal xử lý đơn đặt trước | | Pass | 11/15/2015 | |
| **FUNC-DSDT-06** | Click nút Thông báo có hàng (icon Bell) | 1. Truy cập /admin/pre-orders<br>2. Click nút Thông báo có hàng của một đơn | Mở modal thông báo có hàng | | Pass | 11/15/2015 | |
| **FUNC-DSDT-07** | Lọc theo Trạng thái | 1. Truy cập /admin/pre-orders<br>2. Chọn trạng thái (VD: Chờ xử lý)<br>3. Click "Bộ lọc" | Hiển thị danh sách đơn đặt trước có trạng thái đã chọn, Stats Cards được cập nhật | | Untested | 11/15/2015 | |
| **FUNC-DSDT-08** | Lọc theo Loại sản phẩm | 1. Truy cập /admin/pre-orders<br>2. Chọn loại sản phẩm (VD: Gundam)<br>3. Click "Bộ lọc" | Hiển thị danh sách đơn đặt trước có loại sản phẩm đã chọn | | Untested | 11/15/2015 | |
| **FUNC-DSDT-09** | Lọc theo Date Range | 1. Truy cập /admin/pre-orders<br>2. Chọn khoảng ngày tạo<br>3. Click "Bộ lọc" | Hiển thị danh sách đơn đặt trước tạo trong khoảng ngày đã chọn | | Untested | 11/15/2015 | |
| **FUNC-DSDT-10** | Tìm kiếm đơn đặt trước | 1. Truy cập /admin/pre-orders<br>2. Nhập từ khóa tìm kiếm (ID, tên khách hàng hoặc tên sản phẩm)<br>3. Nhấn Enter hoặc click "Bộ lọc" | Hiển thị danh sách đơn đặt trước phù hợp với từ khóa tìm kiếm | | Untested | 11/15/2015 | |
| **FUNC-DSDT-11** | Xử lý khi không có đơn đặt trước | 1. Truy cập /admin/pre-orders<br>2. Lọc để không có đơn nào | Hiển thị thông báo "Không tìm thấy đơn đặt trước nào" hoặc bảng trống | | Untested | 11/15/2015 | |
| **FUNC-DSDT-12** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/pre-orders<br>2. Tắt kết nối mạng | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại" | | Untested | 11/15/2015 | |
| **FUNC-DSDT-13** | Xử lý khi server lỗi | 1. Truy cập /admin/pre-orders<br>2. Server trả về lỗi 500 | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau" | | Untested | 11/15/2015 | |

---

### Function: Xem chi tiết đặt trước

#### Check GUI: Xem chi tiết đặt trước

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CTDT-01** | Kiểm tra nút Quay lại | 1. Truy cập /admin/pre-orders/[id]<br>2. Kiểm tra nút Quay lại | Hiển thị nút "Quay lại" với icon ArrowLeft variant outline size sm, link đến /admin/pre-orders | | Pass | 11/15/2015 | |
| **GUI-CTDT-02** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/pre-orders/[id]<br>2. Kiểm tra tiêu đề | Hiển thị "Đơn đặt trước #[id]" với kích thước text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-CTDT-03** | Kiểm tra mô tả trang | 1. Truy cập /admin/pre-orders/[id]<br>2. Kiểm tra mô tả | Hiển thị "Chi tiết đơn hàng đặt trước" màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-CTDT-04** | Kiểm tra Badge trạng thái | 1. Truy cập /admin/pre-orders/[id]<br>2. Kiểm tra Badge | Hiển thị Badge trạng thái với icon và màu tương ứng: Chờ xử lý (Clock icon màu vàng, secondary), Đã xác nhận (CheckCircle icon màu xanh, default), Đang chuẩn bị (Package icon màu xanh dương, outline), Đã giao (Truck icon màu xanh lá, outline), Đã hủy (XCircle icon màu đỏ, destructive) | | Pass | 11/15/2015 | |
| **GUI-CTDT-05** | Kiểm tra Badge mức ưu tiên | 1. Truy cập /admin/pre-orders/[id]<br>2. Kiểm tra Badge | Hiển thị Badge mức ưu tiên với icon và màu tương ứng: Cao (AlertTriangle icon màu đỏ, destructive), Trung bình (Clock icon màu vàng, secondary), Thấp (CheckCircle icon màu xanh lá, outline) | | Pass | 11/15/2015 | |
| **GUI-CTDT-06** | Kiểm tra nút Cập nhật trạng thái | 1. Truy cập /admin/pre-orders/[id]<br>2. Kiểm tra nút | Hiển thị nút "Cập nhật trạng thái" với icon CheckCircle variant outline | | Pass | 11/15/2015 | |
| **GUI-CTDT-07** | Kiểm tra nút Gửi thông báo | 1. Truy cập /admin/pre-orders/[id]<br>2. Kiểm tra nút | Hiển thị nút "Gửi thông báo" với icon Bell variant secondary | | Pass | 11/15/2015 | |
| **GUI-CTDT-08** | Kiểm tra nút Xử lý | 1. Truy cập /admin/pre-orders/[id]<br>2. Kiểm tra nút | Hiển thị nút "Xử lý" với icon Package variant outline | | Pass | 11/15/2015 | |
| **GUI-CTDT-09** | Kiểm tra card Thông tin cơ bản | 1. Truy cập /admin/pre-orders/[id]<br>2. Kiểm tra card | Hiển thị card "Thông tin cơ bản" với: Mã đặt trước, Ngày tạo (icon Calendar), Trạng thái (Badge), Mức ưu tiên (Badge) | | Pass | 11/15/2015 | |
| **GUI-CTDT-10** | Kiểm tra card Khách hàng | 1. Truy cập /admin/pre-orders/[id]<br>2. Kiểm tra card | Hiển thị card "Khách hàng" với: Họ tên (icon User), SĐT (icon Phone), Email (icon Mail), Hạng (Badge) | | Pass | 11/15/2015 | |
| **GUI-CTDT-11** | Kiểm tra card Sản phẩm | 1. Truy cập /admin/pre-orders/[id]<br>2. Kiểm tra card | Hiển thị card "Sản phẩm" với danh sách sản phẩm: Tên, Số lượng, Giá dự kiến, Tổng, Tiền cọc, Còn lại (icon Package) | | Pass | 11/15/2015 | |
| **GUI-CTDT-12** | Kiểm tra card Địa chỉ giao hàng | 1. Truy cập /admin/pre-orders/[id]<br>2. Kiểm tra card | Hiển thị card "Địa chỉ giao hàng" với: Địa chỉ, Thành phố, Quận/Huyện, Phường/Xã (icon MapPin) | | Pass | 11/15/2015 | |
| **GUI-CTDT-13** | Kiểm tra card Phương thức thanh toán | 1. Truy cập /admin/pre-orders/[id]<br>2. Kiểm tra card | Hiển thị card "Phương thức thanh toán" với: COD / Banking / MoMo / ZaloPay / Viettel Money (icon CreditCard) | | Pass | 11/15/2015 | |
| **GUI-CTDT-14** | Kiểm tra card Lịch sử xử lý | 1. Truy cập /admin/pre-orders/[id]<br>2. Kiểm tra card | Hiển thị card "Lịch sử xử lý" với Timeline hiển thị các mốc: Thời gian, Hành động, Người xử lý, Ghi chú | | Pass | 11/15/2015 | |
| **GUI-CTDT-15** | Kiểm tra trường Ghi chú nội bộ | 1. Truy cập /admin/pre-orders/[id]<br>2. Kiểm tra trường | Hiển thị Textarea "Ghi chú nội bộ" với placeholder "Nhập ghi chú xử lý...", nút "Thêm ghi chú" hoặc "Cập nhật ghi chú" | | Pass | 11/15/2015 | |

---

### Check FUNC: Xem chi tiết đặt trước

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CTDT-01** | Mở trang chi tiết đặt trước | 1. Truy cập /admin/pre-orders/[id] | Hiển thị trang với nút Quay lại, tiêu đề "Đơn đặt trước #[id]", mô tả, Badge trạng thái, Badge mức ưu tiên, các nút thao tác, card Thông tin cơ bản, card Khách hàng, card Sản phẩm, card Địa chỉ giao hàng, card Phương thức thanh toán, card Lịch sử xử lý, trường Ghi chú nội bộ | | Pass | 11/15/2015 | |
| **FUNC-CTDT-02** | Hiển thị đầy đủ thông tin đặt trước | 1. Truy cập /admin/pre-orders/[id] | Hiển thị đầy đủ thông tin: mã đặt trước, ngày tạo, trạng thái, mức ưu tiên, thông tin khách hàng, danh sách sản phẩm, địa chỉ giao hàng, phương thức thanh toán, lịch sử xử lý, ghi chú nội bộ | | Pass | 11/15/2015 | |
| **FUNC-CTDT-03** | Click nút Quay lại | 1. Truy cập /admin/pre-orders/[id]<br>2. Click nút "Quay lại" | Chuyển về trang /admin/pre-orders | | Pass | 11/15/2015 | |
| **FUNC-CTDT-04** | Click nút Cập nhật trạng thái | 1. Truy cập /admin/pre-orders/[id]<br>2. Click nút "Cập nhật trạng thái" | Mở modal cập nhật trạng thái đơn đặt trước | | Pass | 11/15/2015 | |
| **FUNC-CTDT-05** | Click nút Gửi thông báo | 1. Truy cập /admin/pre-orders/[id]<br>2. Click nút "Gửi thông báo" | Mở modal gửi thông báo cho khách hàng | | Pass | 11/15/2015 | |
| **FUNC-CTDT-06** | Click nút Xử lý | 1. Truy cập /admin/pre-orders/[id]<br>2. Click nút "Xử lý" | Mở modal xử lý đơn đặt trước | | Pass | 11/15/2015 | |
| **FUNC-CTDT-07** | Thêm ghi chú nội bộ thành công | 1. Truy cập /admin/pre-orders/[id]<br>2. Nhập ghi chú vào Textarea<br>3. Click "Thêm ghi chú" hoặc "Cập nhật ghi chú" | Hiển thị thông báo "Thêm ghi chú thành công" hoặc "Cập nhật ghi chú thành công", ghi chú được lưu và hiển thị trong Timeline | | Untested | 11/15/2015 | |
| **FUNC-CTDT-08** | Xử lý khi đơn đặt trước không tồn tại | 1. Truy cập /admin/pre-orders/[id không tồn tại] | Hiển thị thông báo lỗi "Đơn đặt trước không tồn tại" hoặc chuyển về trang danh sách | | Untested | 11/15/2015 | |
| **FUNC-CTDT-09** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/pre-orders/[id]<br>2. Tắt kết nối mạng | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại" | | Untested | 11/15/2015 | |
| **FUNC-CTDT-10** | Xử lý khi server lỗi | 1. Truy cập /admin/pre-orders/[id]<br>2. Server trả về lỗi 500 | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau" | | Untested | 11/15/2015 | |

---

### Function: Xử lý đặt trước

#### Check GUI: Xử lý đặt trước

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XLDT-01** | Kiểm tra modal Xử lý đặt trước | 1. Truy cập /admin/pre-orders<br>2. Click nút Xử lý (icon Package) của một đơn<br>3. Kiểm tra modal | Hiển thị Dialog với tiêu đề "Xử lý đơn đặt trước", mô tả "Xử lý đơn đặt trước #[id]" | | Pass | 11/15/2015 | |
| **GUI-XLDT-02** | Kiểm tra trường Tồn kho khả dụng | 1. Truy cập /admin/pre-orders<br>2. Click nút Xử lý<br>3. Kiểm tra trường | Hiển thị label "Tồn kho khả dụng", Display hiển thị số lượng hiện có (icon Package) | | Pass | 11/15/2015 | |
| **GUI-XLDT-03** | Kiểm tra Select Đề xuất phương án | 1. Truy cập /admin/pre-orders<br>2. Click nút Xử lý<br>3. Kiểm tra Select | Hiển thị label "Đề xuất phương án *", Select với placeholder "Chọn phương án xử lý", có các option: Chờ thêm hàng, Giao 1 phần, Hủy theo yêu cầu | | Pass | 11/15/2015 | |
| **GUI-XLDT-04** | Kiểm tra trường Nhân viên phụ trách | 1. Truy cập /admin/pre-orders<br>2. Click nút Xử lý<br>3. Kiểm tra trường | Hiển thị label "Nhân viên phụ trách", Select với placeholder "Chọn nhân viên...", có danh sách nhân viên | | Pass | 11/15/2015 | |
| **GUI-XLDT-05** | Kiểm tra trường Ghi chú | 1. Truy cập /admin/pre-orders<br>2. Click nút Xử lý<br>3. Kiểm tra trường | Hiển thị label "Ghi chú", Textarea với placeholder "Nhập ghi chú xử lý..." | | Pass | 11/15/2015 | |
| **GUI-XLDT-06** | Kiểm tra checkbox Gửi thông báo cho khách hàng | 1. Truy cập /admin/pre-orders<br>2. Click nút Xử lý<br>3. Kiểm tra checkbox | Hiển thị checkbox với label "Gửi thông báo cho khách hàng về phương án xử lý", mặc định checked | | Pass | 11/15/2015 | |
| **GUI-XLDT-07** | Kiểm tra nút Hủy | 1. Truy cập /admin/pre-orders<br>2. Click nút Xử lý<br>3. Kiểm tra nút | Hiển thị nút "Hủy" variant outline | | Pass | 11/15/2015 | |
| **GUI-XLDT-08** | Kiểm tra nút Xác nhận xử lý | 1. Truy cập /admin/pre-orders<br>2. Click nút Xử lý<br>3. Kiểm tra nút | Hiển thị nút "Xác nhận xử lý" type submit | | Pass | 11/15/2015 | |

---

### Check FUNC: Xử lý đặt trước

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XLDT-01** | Mở modal xử lý đặt trước | 1. Truy cập /admin/pre-orders<br>2. Click nút "Xử lý" của một đơn đặt trước | Hiển thị Dialog với tiêu đề "Xử lý đơn đặt trước", mô tả, trường Tồn kho khả dụng, Select Đề xuất phương án, Select Nhân viên phụ trách, Textarea Ghi chú, checkbox Gửi thông báo cho khách hàng, nút Hủy, nút Xác nhận xử lý | | Pass | 11/15/2015 | |
| **FUNC-XLDT-02** | Xử lý đặt trước thành công - Chờ thêm hàng | 1. Truy cập /admin/pre-orders<br>2. Click nút "Xử lý"<br>3. Chọn phương án "Chờ thêm hàng"<br>4. Chọn nhân viên phụ trách<br>5. Nhập ghi chú<br>6. Tích checkbox Gửi thông báo<br>7. Click "Xác nhận xử lý" | Hiển thị thông báo "Xử lý đơn đặt trước thành công", gửi thông báo cho khách hàng (nếu được chọn), nhân viên được gán, ghi chú được lưu, lịch sử xử lý được ghi nhận, modal đóng | | Untested | 11/15/2015 | |
| **FUNC-XLDT-03** | Xử lý đặt trước thành công - Giao 1 phần | 1. Truy cập /admin/pre-orders<br>2. Click nút "Xử lý"<br>3. Chọn phương án "Giao 1 phần"<br>4. Chọn nhân viên phụ trách<br>5. Nhập ghi chú<br>6. Tích checkbox Gửi thông báo<br>7. Click "Xác nhận xử lý" | Hiển thị thông báo "Xử lý đơn đặt trước thành công", gửi thông báo cho khách hàng, cập nhật số lượng sản phẩm còn lại, lịch sử xử lý được ghi nhận, modal đóng | | Untested | 11/15/2015 | |
| **FUNC-XLDT-04** | Xử lý đặt trước thành công - Hủy theo yêu cầu | 1. Truy cập /admin/pre-orders<br>2. Click nút "Xử lý"<br>3. Chọn phương án "Hủy theo yêu cầu"<br>4. Chọn nhân viên phụ trách<br>5. Nhập ghi chú<br>6. Tích checkbox Gửi thông báo<br>7. Click "Xác nhận xử lý" | Hiển thị thông báo "Xử lý đơn đặt trước thành công", trạng thái đơn chuyển thành "Đã hủy", gửi thông báo cho khách hàng, hoàn tiền cọc (nếu có), lịch sử xử lý được ghi nhận, modal đóng | | Untested | 11/15/2015 | |
| **FUNC-XLDT-05** | Xử lý - Thiếu Đề xuất phương án | 1. Truy cập /admin/pre-orders<br>2. Click nút "Xử lý"<br>3. Không chọn phương án<br>4. Click "Xác nhận xử lý" | Hiển thị thông báo lỗi "Vui lòng chọn phương án xử lý", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-XLDT-06** | Click nút Hủy | 1. Truy cập /admin/pre-orders<br>2. Click nút "Xử lý"<br>3. Click "Hủy" | Modal đóng, không xử lý đơn đặt trước | | Pass | 11/15/2015 | |
| **FUNC-XLDT-07** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/pre-orders<br>2. Click nút "Xử lý"<br>3. Điền đầy đủ thông tin<br>4. Tắt kết nối mạng<br>5. Click "Xác nhận xử lý" | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", form không được gửi | | Untested | 11/15/2015 | |
| **FUNC-XLDT-08** | Xử lý khi server lỗi | 1. Truy cập /admin/pre-orders<br>2. Click nút "Xử lý"<br>3. Điền đầy đủ thông tin<br>4. Server trả về lỗi 500<br>5. Click "Xác nhận xử lý" | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau", form không được gửi | | Untested | 11/15/2015 | |

---

### Function: Cập nhật trạng thái đặt trước

#### Check GUI: Cập nhật trạng thái đặt trước

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CNTTDT-01** | Kiểm tra modal Cập nhật trạng thái | 1. Truy cập /admin/pre-orders<br>2. Click nút Cập nhật trạng thái (icon CheckCircle) của một đơn<br>3. Kiểm tra modal | Hiển thị Dialog với tiêu đề "Cập nhật trạng thái đơn đặt trước", mô tả "Thay đổi trạng thái xử lý đơn đặt trước #[id]" | | Pass | 11/15/2015 | |
| **GUI-CNTTDT-02** | Kiểm tra trường Trạng thái hiện tại | 1. Truy cập /admin/pre-orders<br>2. Click nút Cập nhật trạng thái<br>3. Kiểm tra trường | Hiển thị label "Trạng thái hiện tại", Display hiển thị trạng thái hiện tại với Badge và icon | | Pass | 11/15/2015 | |
| **GUI-CNTTDT-03** | Kiểm tra Select Trạng thái mới | 1. Truy cập /admin/pre-orders<br>2. Click nút Cập nhật trạng thái<br>3. Kiểm tra Select | Hiển thị label "Trạng thái mới *", Select với placeholder "Chọn trạng thái mới", có các option: Chờ xử lý, Đã xác nhận, Đang chuẩn bị, Đã giao, Đã hủy | | Pass | 11/15/2015 | |
| **GUI-CNTTDT-04** | Kiểm tra trường Người xử lý | 1. Truy cập /admin/pre-orders<br>2. Click nút Cập nhật trạng thái<br>3. Kiểm tra trường | Hiển thị label "Người xử lý", Select với placeholder "Chọn người xử lý...", có danh sách nhân viên | | Pass | 11/15/2015 | |
| **GUI-CNTTDT-05** | Kiểm tra trường Ghi chú | 1. Truy cập /admin/pre-orders<br>2. Click nút Cập nhật trạng thái<br>3. Kiểm tra trường | Hiển thị label "Ghi chú", Textarea với placeholder "Nhập ghi chú thay đổi trạng thái (tùy chọn)" | | Pass | 11/15/2015 | |
| **GUI-CNTTDT-06** | Kiểm tra Toggle Thông báo khách hàng | 1. Truy cập /admin/pre-orders<br>2. Click nút Cập nhật trạng thái<br>3. Kiểm tra Toggle | Hiển thị Toggle với label "Gửi thông báo cho khách hàng về thay đổi trạng thái", mặc định bật | | Pass | 11/15/2015 | |
| **GUI-CNTTDT-07** | Kiểm tra Card Bảng quy ước trạng thái | 1. Truy cập /admin/pre-orders<br>2. Click nút Cập nhật trạng thái<br>3. Kiểm tra Card | Hiển thị Card "Bảng quy ước trạng thái" với các trạng thái: Chờ xử lý / Đã xác nhận / Đang chuẩn bị / Đã giao / Đã hủy và mô tả từng trạng thái | | Pass | 11/15/2015 | |
| **GUI-CNTTDT-08** | Kiểm tra nút Hủy | 1. Truy cập /admin/pre-orders<br>2. Click nút Cập nhật trạng thái<br>3. Kiểm tra nút | Hiển thị nút "Hủy" variant outline | | Pass | 11/15/2015 | |
| **GUI-CNTTDT-09** | Kiểm tra nút Cập nhật trạng thái | 1. Truy cập /admin/pre-orders<br>2. Click nút Cập nhật trạng thái<br>3. Kiểm tra nút | Hiển thị nút "Cập nhật trạng thái" type submit | | Pass | 11/15/2015 | |

---

### Check FUNC: Cập nhật trạng thái đặt trước

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CNTTDT-01** | Mở modal cập nhật trạng thái | 1. Truy cập /admin/pre-orders<br>2. Click nút "Cập nhật trạng thái" của một đơn đặt trước | Hiển thị Dialog với tiêu đề "Cập nhật trạng thái đơn đặt trước", mô tả, trường Trạng thái hiện tại, Select Trạng thái mới, Select Người xử lý, Textarea Ghi chú, Toggle Thông báo khách hàng, Card Bảng quy ước trạng thái, nút Hủy, nút Cập nhật trạng thái | | Pass | 11/15/2015 | |
| **FUNC-CNTTDT-02** | Cập nhật trạng thái thành công | 1. Truy cập /admin/pre-orders<br>2. Click nút "Cập nhật trạng thái"<br>3. Chọn trạng thái mới<br>4. Chọn người xử lý<br>5. Nhập ghi chú (tùy chọn)<br>6. Bật Toggle Thông báo khách hàng<br>7. Click "Cập nhật trạng thái" | Hiển thị thông báo "Cập nhật trạng thái thành công", trạng thái đơn được cập nhật, gửi thông báo cho khách hàng (nếu được bật), lịch sử xử lý được ghi nhận, modal đóng | | Untested | 11/15/2015 | |
| **FUNC-CNTTDT-03** | Cập nhật - Thiếu Trạng thái mới | 1. Truy cập /admin/pre-orders<br>2. Click nút "Cập nhật trạng thái"<br>3. Không chọn trạng thái mới<br>4. Click "Cập nhật trạng thái" | Hiển thị thông báo lỗi "Vui lòng chọn trạng thái mới", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-CNTTDT-04** | Cập nhật - Chọn trạng thái giống hiện tại | 1. Truy cập /admin/pre-orders<br>2. Click nút "Cập nhật trạng thái"<br>3. Chọn trạng thái mới giống trạng thái hiện tại<br>4. Click "Cập nhật trạng thái" | Hiển thị thông báo lỗi "Trạng thái mới phải khác trạng thái hiện tại", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-CNTTDT-05** | Cập nhật - Không gửi thông báo | 1. Truy cập /admin/pre-orders<br>2. Click nút "Cập nhật trạng thái"<br>3. Chọn trạng thái mới<br>4. Tắt Toggle Thông báo khách hàng<br>5. Click "Cập nhật trạng thái" | Hiển thị thông báo "Cập nhật trạng thái thành công", trạng thái được cập nhật, không gửi thông báo cho khách hàng | | Untested | 11/15/2015 | |
| **FUNC-CNTTDT-06** | Hủy đơn đặt trước | 1. Truy cập /admin/pre-orders<br>2. Click nút "Cập nhật trạng thái"<br>3. Chọn trạng thái "Đã hủy"<br>4. Nhập lý do hủy<br>5. Click "Cập nhật trạng thái" | Hiển thị thông báo "Cập nhật trạng thái thành công", trạng thái chuyển thành "Đã hủy", hoàn tiền cọc (nếu có), gửi thông báo cho khách hàng, lịch sử xử lý được ghi nhận | | Untested | 11/15/2015 | |
| **FUNC-CNTTDT-07** | Click nút Hủy | 1. Truy cập /admin/pre-orders<br>2. Click nút "Cập nhật trạng thái"<br>3. Click "Hủy" | Modal đóng, trạng thái không được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-CNTTDT-08** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/pre-orders<br>2. Click nút "Cập nhật trạng thái"<br>3. Chọn trạng thái mới<br>4. Tắt kết nối mạng<br>5. Click "Cập nhật trạng thái" | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", form không được gửi | | Untested | 11/15/2015 | |
| **FUNC-CNTTDT-09** | Xử lý khi server lỗi | 1. Truy cập /admin/pre-orders<br>2. Click nút "Cập nhật trạng thái"<br>3. Chọn trạng thái mới<br>4. Server trả về lỗi 500<br>5. Click "Cập nhật trạng thái" | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau", form không được gửi | | Untested | 11/15/2015 | |

---

### Function: Thông báo có hàng

#### Check GUI: Thông báo có hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-TBCH-01** | Kiểm tra modal Thông báo có hàng | 1. Truy cập /admin/pre-orders<br>2. Click nút Thông báo có hàng (icon Bell) của một đơn<br>3. Kiểm tra modal | Hiển thị Dialog với tiêu đề "Thông báo có hàng", mô tả "Gửi thông báo đến khách đã đặt trước khi hàng về" | | Pass | 11/15/2015 | |
| **GUI-TBCH-02** | Kiểm tra trường Tiêu đề | 1. Truy cập /admin/pre-orders<br>2. Click nút Thông báo có hàng<br>3. Kiểm tra trường | Hiển thị label "Tiêu đề *", input type text với placeholder "Nhập tiêu đề thông báo...", có giá trị mặc định "Sản phẩm đã có hàng" | | Pass | 11/15/2015 | |
| **GUI-TBCH-03** | Kiểm tra trường Nội dung | 1. Truy cập /admin/pre-orders<br>2. Click nút Thông báo có hàng<br>3. Kiểm tra trường | Hiển thị label "Nội dung *", Textarea với placeholder "Nhập nội dung thông báo...", có template mặc định | | Pass | 11/15/2015 | |
| **GUI-TBCH-04** | Kiểm tra trường Sản phẩm | 1. Truy cập /admin/pre-orders<br>2. Click nút Thông báo có hàng<br>3. Kiểm tra trường | Hiển thị label "Sản phẩm", Display hiển thị tên sản phẩm đã đặt trước (icon Package) | | Pass | 11/15/2015 | |
| **GUI-TBCH-05** | Kiểm tra trường Giá | 1. Truy cập /admin/pre-orders<br>2. Click nút Thông báo có hàng<br>3. Kiểm tra trường | Hiển thị label "Giá", Display hiển thị giá sản phẩm (icon DollarSign) | | Pass | 11/15/2015 | |
| **GUI-TBCH-06** | Kiểm tra trường Thời gian | 1. Truy cập /admin/pre-orders<br>2. Click nút Thông báo có hàng<br>3. Kiểm tra trường | Hiển thị label "Thời gian dự kiến giao hàng", input type date hoặc datetime-local | | Pass | 11/15/2015 | |
| **GUI-TBCH-07** | Kiểm tra Select Kênh gửi | 1. Truy cập /admin/pre-orders<br>2. Click nút Thông báo có hàng<br>3. Kiểm tra Select | Hiển thị label "Kênh gửi *", Select với placeholder "Chọn kênh gửi", có các option: Email, Push, SMS, có thể chọn nhiều | | Pass | 11/15/2015 | |
| **GUI-TBCH-08** | Kiểm tra Select Đối tượng nhận | 1. Truy cập /admin/pre-orders<br>2. Click nút Thông báo có hàng<br>3. Kiểm tra Select | Hiển thị label "Đối tượng nhận *", Select với placeholder "Chọn đối tượng nhận", có các option: Theo đơn đặt trước, Theo sản phẩm | | Pass | 11/15/2015 | |
| **GUI-TBCH-09** | Kiểm tra nút Hủy | 1. Truy cập /admin/pre-orders<br>2. Click nút Thông báo có hàng<br>3. Kiểm tra nút | Hiển thị nút "Hủy" variant outline | | Pass | 11/15/2015 | |
| **GUI-TBCH-10** | Kiểm tra nút Gửi thông báo | 1. Truy cập /admin/pre-orders<br>2. Click nút Thông báo có hàng<br>3. Kiểm tra nút | Hiển thị nút "Gửi thông báo" type submit | | Pass | 11/15/2015 | |

---

### Check FUNC: Thông báo có hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TBCH-01** | Mở modal thông báo có hàng | 1. Truy cập /admin/pre-orders<br>2. Click nút "Thông báo có hàng" của một đơn đặt trước | Hiển thị Dialog với tiêu đề "Thông báo có hàng", mô tả, trường Tiêu đề (có giá trị mặc định), trường Nội dung (có template mặc định), trường Sản phẩm, trường Giá, trường Thời gian, Select Kênh gửi, Select Đối tượng nhận, nút Hủy, nút Gửi thông báo | | Pass | 11/15/2015 | |
| **FUNC-TBCH-02** | Gửi thông báo có hàng thành công - Theo đơn đặt trước | 1. Truy cập /admin/pre-orders<br>2. Click nút "Thông báo có hàng"<br>3. Điều chỉnh tiêu đề và nội dung<br>4. Chọn kênh gửi (Email, Push, SMS)<br>5. Chọn đối tượng "Theo đơn đặt trước"<br>6. Click "Gửi thông báo" | Hiển thị thông báo "Gửi thông báo có hàng thành công", thông báo được gửi đến khách hàng của đơn đặt trước qua các kênh đã chọn, ghi nhận tỉ lệ mở (nếu có), modal đóng | | Untested | 11/15/2015 | |
| **FUNC-TBCH-03** | Gửi thông báo có hàng thành công - Theo sản phẩm | 1. Truy cập /admin/pre-orders<br>2. Click nút "Thông báo có hàng"<br>3. Điều chỉnh tiêu đề và nội dung<br>4. Chọn kênh gửi<br>5. Chọn đối tượng "Theo sản phẩm"<br>6. Click "Gửi thông báo" | Hiển thị thông báo "Gửi thông báo có hàng thành công", thông báo được gửi đến tất cả khách hàng đã đặt trước sản phẩm này qua các kênh đã chọn, ghi nhận tỉ lệ mở, modal đóng | | Untested | 11/15/2015 | |
| **FUNC-TBCH-04** | Gửi thông báo - Thiếu Tiêu đề | 1. Truy cập /admin/pre-orders<br>2. Click nút "Thông báo có hàng"<br>3. Xóa tiêu đề<br>4. Click "Gửi thông báo" | Hiển thị thông báo lỗi "Tiêu đề không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-TBCH-05** | Gửi thông báo - Thiếu Nội dung | 1. Truy cập /admin/pre-orders<br>2. Click nút "Thông báo có hàng"<br>3. Xóa nội dung<br>4. Click "Gửi thông báo" | Hiển thị thông báo lỗi "Nội dung không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-TBCH-06** | Gửi thông báo - Thiếu Kênh gửi | 1. Truy cập /admin/pre-orders<br>2. Click nút "Thông báo có hàng"<br>3. Không chọn kênh gửi<br>4. Click "Gửi thông báo" | Hiển thị thông báo lỗi "Vui lòng chọn ít nhất một kênh gửi", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-TBCH-07** | Gửi thông báo - Thiếu Đối tượng nhận | 1. Truy cập /admin/pre-orders<br>2. Click nút "Thông báo có hàng"<br>3. Không chọn đối tượng nhận<br>4. Click "Gửi thông báo" | Hiển thị thông báo lỗi "Vui lòng chọn đối tượng nhận", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-TBCH-08** | Click nút Hủy | 1. Truy cập /admin/pre-orders<br>2. Click nút "Thông báo có hàng"<br>3. Click "Hủy" | Modal đóng, không gửi thông báo | | Pass | 11/15/2015 | |
| **FUNC-TBCH-09** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/pre-orders<br>2. Click nút "Thông báo có hàng"<br>3. Điền đầy đủ thông tin<br>4. Tắt kết nối mạng<br>5. Click "Gửi thông báo" | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", form không được gửi | | Untested | 11/15/2015 | |
| **FUNC-TBCH-10** | Xử lý khi server lỗi | 1. Truy cập /admin/pre-orders<br>2. Click nút "Thông báo có hàng"<br>3. Điền đầy đủ thông tin<br>4. Server trả về lỗi 500<br>5. Click "Gửi thông báo" | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau", form không được gửi | | Untested | 11/15/2015 | |

---

**Người tạo:** Testing Team  
**Ngày cập nhật:** 11/15/2015  
**Phiên bản:** 1.0

