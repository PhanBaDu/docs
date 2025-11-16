# Test Case Template - Quản lý đơn hàng (Admin)

## Module Code
**Model Management Store: Quản lý đơn hàng Admin**

## Test Requirement
1. Hiển thị danh sách đơn hàng
2. Xem chi tiết đơn hàng
3. Cập nhật đơn hàng
4. Xóa đơn hàng
5. Xác nhận đơn hàng
6. In đơn hàng
7. Tạo đơn hàng mới

---

## Test Summary

### Người thực hiện Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 63 |
| **Fail** | 0 |
| **Untested** | 69 |
| **N/A** | 0 |
| **Number of Test cases** | 132 |

---

## Test Cases

### Function: Hiển thị danh sách đơn hàng

#### Check GUI: Hiển thị danh sách đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DSDH-01** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/orders<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Quản lý đơn hàng" với kích thước text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-DSDH-02** | Kiểm tra mô tả chức năng | 1. Truy cập /admin/orders<br>2. Kiểm tra mô tả | Hiển thị mô tả "Xử lý và theo dõi tất cả đơn hàng" màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-DSDH-03** | Kiểm tra nút In báo cáo | 1. Truy cập /admin/orders<br>2. Kiểm tra nút | Hiển thị nút "In báo cáo" với icon Printer variant outline ở header | | Pass | 11/15/2015 | |
| **GUI-DSDH-04** | Kiểm tra nút Bộ lọc nâng cao | 1. Truy cập /admin/orders<br>2. Kiểm tra nút | Hiển thị nút "Bộ lọc nâng cao" với icon Filter variant outline ở header | | Pass | 11/15/2015 | |
| **GUI-DSDH-05** | Kiểm tra Stats Cards | 1. Truy cập /admin/orders<br>2. Kiểm tra Stats Cards | Hiển thị 5 card thống kê: Chờ xác nhận (12), Đã xác nhận (8), Đang giao (15), Đã giao (120), Đã hủy (1) | | Pass | 11/15/2015 | |
| **GUI-DSDH-06** | Kiểm tra trường Tìm kiếm | 1. Truy cập /admin/orders<br>2. Kiểm tra trường tìm kiếm | Hiển thị input với icon Search bên trái, placeholder "Tìm kiếm đơn hàng, khách hàng...", có thể nhập và nhấn Enter để tìm | | Pass | 11/15/2015 | |
| **GUI-DSDH-07** | Kiểm tra Select Trạng thái | 1. Truy cập /admin/orders<br>2. Kiểm tra Select Trạng thái | Hiển thị Select với placeholder "Trạng thái", width w-40, có các option: Tất cả (156), Chờ xác nhận (12), Đã xác nhận (8), Đang giao (15), Đã giao (120), Đã hủy (1) | | Pass | 11/15/2015 | |
| **GUI-DSDH-08** | Kiểm tra Select Phương thức thanh toán | 1. Truy cập /admin/orders<br>2. Kiểm tra Select | Hiển thị Select với placeholder "Phương thức thanh toán", width w-40, có các option: Tất cả, COD, Banking, Credit Card, E-wallet | | Pass | 11/15/2015 | |
| **GUI-DSDH-09** | Kiểm tra Date Range | 1. Truy cập /admin/orders<br>2. Kiểm tra Date Range | Hiển thị 2 input date với text "đến" ở giữa, width w-40 mỗi input | | Pass | 11/15/2015 | |
| **GUI-DSDH-10** | Kiểm tra nút Áp dụng | 1. Truy cập /admin/orders<br>2. Kiểm tra nút | Hiển thị nút "Áp dụng" với icon Filter variant outline | | Pass | 11/15/2015 | |
| **GUI-DSDH-11** | Kiểm tra bảng danh sách đơn hàng | 1. Truy cập /admin/orders<br>2. Kiểm tra bảng | Hiển thị Table với các cột: Mã đơn hàng, Khách hàng, Sản phẩm, Tổng tiền, Thanh toán, Trạng thái, Ngày tạo, Thao tác | | Pass | 11/15/2015 | |
| **GUI-DSDH-12** | Kiểm tra cột Mã đơn hàng trong bảng | 1. Truy cập /admin/orders<br>2. Kiểm tra cột Mã đơn hàng | Mỗi dòng hiển thị mã đơn hàng (font-medium) và ngày tạo (text-sm muted-foreground) | | Pass | 11/15/2015 | |
| **GUI-DSDH-13** | Kiểm tra cột Khách hàng trong bảng | 1. Truy cập /admin/orders<br>2. Kiểm tra cột Khách hàng | Hiển thị tên khách hàng (font-medium), email (text-sm muted-foreground), số điện thoại (text-sm muted-foreground) | | Pass | 11/15/2015 | |
| **GUI-DSDH-14** | Kiểm tra cột Sản phẩm trong bảng | 1. Truy cập /admin/orders<br>2. Kiểm tra cột Sản phẩm | Hiển thị số lượng sản phẩm (font-medium) và địa chỉ giao hàng (text-sm muted-foreground) | | Pass | 11/15/2015 | |
| **GUI-DSDH-15** | Kiểm tra cột Tổng tiền trong bảng | 1. Truy cập /admin/orders<br>2. Kiểm tra cột Tổng tiền | Hiển thị tổng tiền định dạng vi-VN (font-medium) | | Pass | 11/15/2015 | |
| **GUI-DSDH-16** | Kiểm tra cột Thanh toán trong bảng | 1. Truy cập /admin/orders<br>2. Kiểm tra cột Thanh toán | Hiển thị Badge variant outline với phương thức thanh toán (COD, Banking, Credit Card, E-wallet) | | Pass | 11/15/2015 | |
| **GUI-DSDH-17** | Kiểm tra cột Trạng thái trong bảng | 1. Truy cập /admin/orders<br>2. Kiểm tra cột Trạng thái | Hiển thị Badge với icon và màu tương ứng: Chờ xác nhận (Package icon, destructive), Đã xác nhận (CheckCircle icon, default), Đang giao (Truck icon, secondary), Đã giao (CheckCircle icon, outline), Đã hủy (XCircle icon, destructive) | | Pass | 11/15/2015 | |
| **GUI-DSDH-18** | Kiểm tra cột Thao tác trong bảng | 1. Truy cập /admin/orders<br>2. Kiểm tra cột Thao tác | Hiển thị 4 nút: Xem (icon Eye link đến /admin/orders/[id]), Cập nhật trạng thái (icon Edit link đến /admin/orders/[id]/update-status), In (icon Printer), Hủy (icon AlertTriangle chỉ hiển thị khi trạng thái không phải cancelled/delivered), tất cả variant ghost size sm | | Pass | 11/15/2015 | |
| **GUI-DSDH-19** | Kiểm tra Pagination | 1. Truy cập /admin/orders<br>2. Kiểm tra Pagination | Hiển thị text "Hiển thị 1-X trong Y đơn hàng", các nút phân trang: Trước (disabled), số trang, Sau | | Pass | 11/15/2015 | |

---

### Check FUNC: Hiển thị danh sách đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DSDH-01** | Mở trang danh sách đơn hàng | 1. Truy cập /admin/orders | Hiển thị trang với tiêu đề, mô tả, nút In báo cáo, nút Bộ lọc nâng cao, 5 Stats Cards, bộ lọc (tìm kiếm, trạng thái, phương thức thanh toán, date range, nút Áp dụng), bảng danh sách đơn hàng, pagination | | Pass | 11/15/2015 | |
| **FUNC-DSDH-02** | Hiển thị danh sách đơn hàng mặc định | 1. Truy cập /admin/orders | Hiển thị tất cả đơn hàng trong bảng, mỗi đơn hàng có đầy đủ thông tin: mã đơn hàng, khách hàng, sản phẩm, tổng tiền, phương thức thanh toán, trạng thái, ngày tạo, các nút thao tác | | Pass | 11/15/2015 | |
| **FUNC-DSDH-03** | Click nút In báo cáo | 1. Truy cập /admin/orders<br>2. Click nút "In báo cáo" | Tải về file PDF/Excel báo cáo đơn hàng hoặc mở dialog in báo cáo | | Untested | 11/15/2015 | |
| **FUNC-DSDH-04** | Click nút Bộ lọc nâng cao | 1. Truy cập /admin/orders<br>2. Click nút "Bộ lọc nâng cao" | Mở dialog/modal với các bộ lọc nâng cao (khoảng giá, loại khách hàng, v.v.) | | Untested | 11/15/2015 | |
| **FUNC-DSDH-05** | Click nút Xem (icon Eye) | 1. Truy cập /admin/orders<br>2. Click nút Xem của một đơn hàng | Chuyển đến trang chi tiết đơn hàng /admin/orders/[id] | | Pass | 11/15/2015 | |
| **FUNC-DSDH-06** | Click nút Cập nhật trạng thái (icon Edit) | 1. Truy cập /admin/orders<br>2. Click nút Cập nhật trạng thái của một đơn hàng | Chuyển đến trang cập nhật trạng thái /admin/orders/[id]/update-status | | Pass | 11/15/2015 | |
| **FUNC-DSDH-07** | Click nút In (icon Printer) | 1. Truy cập /admin/orders<br>2. Click nút In của một đơn hàng | Mở modal in đơn hàng với các tùy chọn in | | Pass | 11/15/2015 | |
| **FUNC-DSDH-08** | Click nút Hủy (icon AlertTriangle) | 1. Truy cập /admin/orders<br>2. Click nút Hủy của một đơn hàng | Mở dialog xác nhận hủy đơn hàng | | Pass | 11/15/2015 | |
| **FUNC-DSDH-09** | Lọc theo Trạng thái | 1. Truy cập /admin/orders<br>2. Chọn trạng thái (VD: Chờ xác nhận)<br>3. Click "Áp dụng" | Hiển thị danh sách đơn hàng có trạng thái đã chọn, Stats Cards được cập nhật | | Untested | 11/15/2015 | |
| **FUNC-DSDH-10** | Lọc theo Phương thức thanh toán | 1. Truy cập /admin/orders<br>2. Chọn phương thức thanh toán (VD: COD)<br>3. Click "Áp dụng" | Hiển thị danh sách đơn hàng có phương thức thanh toán đã chọn | | Untested | 11/15/2015 | |
| **FUNC-DSDH-11** | Lọc theo Date Range | 1. Truy cập /admin/orders<br>2. Chọn khoảng ngày<br>3. Click "Áp dụng" | Hiển thị danh sách đơn hàng trong khoảng ngày đã chọn | | Untested | 11/15/2015 | |
| **FUNC-DSDH-12** | Tìm kiếm đơn hàng | 1. Truy cập /admin/orders<br>2. Nhập từ khóa tìm kiếm (mã đơn hàng hoặc tên khách hàng)<br>3. Nhấn Enter hoặc click "Áp dụng" | Hiển thị danh sách đơn hàng phù hợp với từ khóa tìm kiếm | | Untested | 11/15/2015 | |
| **FUNC-DSDH-13** | Xử lý khi không có đơn hàng | 1. Truy cập /admin/orders<br>2. Lọc để không có đơn hàng nào | Hiển thị thông báo "Không tìm thấy đơn hàng nào" hoặc bảng trống | | Untested | 11/15/2015 | |
| **FUNC-DSDH-14** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/orders<br>2. Tắt kết nối mạng | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại" | | Untested | 11/15/2015 | |
| **FUNC-DSDH-15** | Xử lý khi server lỗi | 1. Truy cập /admin/orders<br>2. Server trả về lỗi 500 | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau" | | Untested | 11/15/2015 | |

---

### Function: Xem chi tiết đơn hàng

#### Check GUI: Xem chi tiết đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CTDH-01** | Kiểm tra nút Quay lại | 1. Truy cập /admin/orders/[id]<br>2. Kiểm tra nút Quay lại | Hiển thị nút "Quay lại" với icon ArrowLeft variant outline size sm, link đến /admin/orders | | Pass | 11/15/2015 | |
| **GUI-CTDH-02** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/orders/[id]<br>2. Kiểm tra tiêu đề | Hiển thị "Đơn hàng #[id]" với kích thước text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-CTDH-03** | Kiểm tra mô tả trang | 1. Truy cập /admin/orders/[id]<br>2. Kiểm tra mô tả | Hiển thị "Chi tiết đơn hàng" màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-CTDH-04** | Kiểm tra Badge trạng thái | 1. Truy cập /admin/orders/[id]<br>2. Kiểm tra Badge | Hiển thị Badge trạng thái với màu tương ứng: Chờ xác nhận (bg-yellow-500), Đã xác nhận (bg-blue-500), Đang giao (bg-purple-500), Đã giao (bg-green-500), Đã hủy (bg-red-500) | | Pass | 11/15/2015 | |
| **GUI-CTDH-05** | Kiểm tra nút Xác nhận đơn hàng | 1. Truy cập /admin/orders/[id]<br>2. Kiểm tra nút | Hiển thị nút "Xác nhận đơn hàng" với icon CheckCircle, chỉ hiển thị khi trạng thái là "pending" | | Pass | 11/15/2015 | |
| **GUI-CTDH-06** | Kiểm tra nút Cập nhật trạng thái | 1. Truy cập /admin/orders/[id]<br>2. Kiểm tra nút | Hiển thị nút "Cập nhật trạng thái" với icon Edit variant outline, link đến /admin/orders/[id]/update-status | | Pass | 11/15/2015 | |
| **GUI-CTDH-07** | Kiểm tra nút In đơn hàng | 1. Truy cập /admin/orders/[id]<br>2. Kiểm tra nút | Hiển thị nút "In đơn hàng" với icon Printer variant outline | | Pass | 11/15/2015 | |
| **GUI-CTDH-08** | Kiểm tra nút Hủy đơn hàng | 1. Truy cập /admin/orders/[id]<br>2. Kiểm tra nút | Hiển thị nút "Hủy đơn hàng" với icon XCircle variant destructive, chỉ hiển thị khi trạng thái không phải cancelled/delivered | | Pass | 11/15/2015 | |
| **GUI-CTDH-09** | Kiểm tra card Thông tin đơn hàng | 1. Truy cập /admin/orders/[id]<br>2. Kiểm tra card | Hiển thị card "Thông tin đơn hàng" với: Mã đơn hàng, Ngày tạo (icon Clock), Trạng thái, Tổng tiền (icon DollarSign), Phương thức thanh toán (icon CreditCard), Trạng thái thanh toán | | Pass | 11/15/2015 | |
| **GUI-CTDH-10** | Kiểm tra card Thông tin khách hàng | 1. Truy cập /admin/orders/[id]<br>2. Kiểm tra card | Hiển thị card "Thông tin khách hàng" với: Tên khách hàng (icon User), Email, Số điện thoại, Địa chỉ (icon MapPin) | | Pass | 11/15/2015 | |
| **GUI-CTDH-11** | Kiểm tra card Danh sách sản phẩm | 1. Truy cập /admin/orders/[id]<br>2. Kiểm tra card | Hiển thị card "Danh sách sản phẩm" với Table hiển thị các cột: Hình ảnh, Tên sản phẩm, Số lượng, Đơn giá, Thành tiền | | Pass | 11/15/2015 | |
| **GUI-CTDH-12** | Kiểm tra card Thông tin vận chuyển | 1. Truy cập /admin/orders/[id]<br>2. Kiểm tra card | Hiển thị card "Thông tin vận chuyển" với: Địa chỉ giao hàng (icon MapPin), Phương thức vận chuyển (icon Truck), Mã vận đơn, Ngày dự kiến giao hàng (icon Clock) | | Pass | 11/15/2015 | |
| **GUI-CTDH-13** | Kiểm tra card Lịch sử cập nhật | 1. Truy cập /admin/orders/[id]<br>2. Kiểm tra card | Hiển thị card "Lịch sử cập nhật" với Timeline hiển thị các mốc thời gian: Thời gian, Trạng thái, Mô tả, Người xử lý | | Pass | 11/15/2015 | |
| **GUI-CTDH-14** | Kiểm tra Dialog hủy đơn hàng | 1. Truy cập /admin/orders/[id]<br>2. Click nút Hủy đơn hàng<br>3. Kiểm tra dialog | Hiển thị Dialog với tiêu đề "Xác nhận hủy đơn hàng", textarea "Lý do hủy", nút Hủy, nút "Xác nhận hủy" variant destructive | | Pass | 11/15/2015 | |

---

### Check FUNC: Xem chi tiết đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CTDH-01** | Mở trang chi tiết đơn hàng | 1. Truy cập /admin/orders/[id] | Hiển thị trang với nút Quay lại, tiêu đề "Đơn hàng #[id]", mô tả, Badge trạng thái, các nút thao tác, card Thông tin đơn hàng, card Thông tin khách hàng, card Danh sách sản phẩm, card Thông tin vận chuyển, card Lịch sử cập nhật | | Pass | 11/15/2015 | |
| **FUNC-CTDH-02** | Hiển thị đầy đủ thông tin đơn hàng | 1. Truy cập /admin/orders/[id] | Hiển thị đầy đủ thông tin: mã đơn hàng, ngày tạo, trạng thái, tổng tiền, phương thức thanh toán, trạng thái thanh toán, thông tin khách hàng, danh sách sản phẩm, thông tin vận chuyển, lịch sử cập nhật | | Pass | 11/15/2015 | |
| **FUNC-CTDH-03** | Click nút Quay lại | 1. Truy cập /admin/orders/[id]<br>2. Click nút "Quay lại" | Chuyển về trang /admin/orders | | Pass | 11/15/2015 | |
| **FUNC-CTDH-04** | Xác nhận đơn hàng thành công | 1. Truy cập /admin/orders/[id]<br>2. Click nút "Xác nhận đơn hàng" | Hiển thị thông báo "Xác nhận đơn hàng thành công", trạng thái đơn hàng chuyển thành "Đã xác nhận", nút Xác nhận biến mất, lịch sử cập nhật được ghi nhận | | Untested | 11/15/2015 | |
| **FUNC-CTDH-05** | Click nút Cập nhật trạng thái | 1. Truy cập /admin/orders/[id]<br>2. Click nút "Cập nhật trạng thái" | Chuyển đến trang /admin/orders/[id]/update-status | | Pass | 11/15/2015 | |
| **FUNC-CTDH-06** | Click nút In đơn hàng | 1. Truy cập /admin/orders/[id]<br>2. Click nút "In đơn hàng" | Mở modal in đơn hàng với các tùy chọn in | | Pass | 11/15/2015 | |
| **FUNC-CTDH-07** | Hủy đơn hàng thành công | 1. Truy cập /admin/orders/[id]<br>2. Click nút "Hủy đơn hàng"<br>3. Nhập lý do hủy<br>4. Click "Xác nhận hủy" | Hiển thị thông báo "Hủy đơn hàng thành công", trạng thái đơn hàng chuyển thành "Đã hủy", chuyển về trang /admin/orders | | Untested | 11/15/2015 | |
| **FUNC-CTDH-08** | Hủy đơn hàng - Thiếu lý do | 1. Truy cập /admin/orders/[id]<br>2. Click nút "Hủy đơn hàng"<br>3. Để trống lý do<br>4. Click "Xác nhận hủy" | Hiển thị thông báo lỗi "Vui lòng nhập lý do hủy đơn hàng", dialog không đóng | | Pass | 11/15/2015 | |
| **FUNC-CTDH-09** | Hủy hủy đơn hàng | 1. Truy cập /admin/orders/[id]<br>2. Click nút "Hủy đơn hàng"<br>3. Click "Hủy" trong dialog | Dialog đóng, vẫn ở trang chi tiết, đơn hàng không bị hủy | | Pass | 11/15/2015 | |
| **FUNC-CTDH-10** | Xử lý khi đơn hàng không tồn tại | 1. Truy cập /admin/orders/[id không tồn tại] | Hiển thị thông báo lỗi "Đơn hàng không tồn tại" hoặc chuyển về trang danh sách | | Untested | 11/15/2015 | |
| **FUNC-CTDH-11** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/orders/[id]<br>2. Tắt kết nối mạng | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại" | | Untested | 11/15/2015 | |
| **FUNC-CTDH-12** | Xử lý khi server lỗi | 1. Truy cập /admin/orders/[id]<br>2. Server trả về lỗi 500 | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau" | | Untested | 11/15/2015 | |

---

### Function: Cập nhật đơn hàng

#### Check GUI: Cập nhật đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CNDH-01** | Kiểm tra nút Quay lại | 1. Truy cập /admin/orders/[id]/update-status<br>2. Kiểm tra nút Quay lại | Hiển thị nút "Quay lại" với icon ArrowLeft variant outline size sm, link đến /admin/orders/[id] | | Pass | 11/15/2015 | |
| **GUI-CNDH-02** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/orders/[id]/update-status<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Cập nhật trạng thái đơn hàng" với kích thước text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-CNDH-03** | Kiểm tra mô tả trang | 1. Truy cập /admin/orders/[id]/update-status<br>2. Kiểm tra mô tả | Hiển thị mô tả "Thay đổi trạng thái đơn hàng #[id]" màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-CNDH-04** | Kiểm tra card Thông tin đơn hàng | 1. Truy cập /admin/orders/[id]/update-status<br>2. Kiểm tra card | Hiển thị card "Thông tin đơn hàng" với: Mã đơn hàng, Khách hàng, Tổng tiền, Trạng thái hiện tại (Badge với icon và màu) | | Pass | 11/15/2015 | |
| **GUI-CNDH-05** | Kiểm tra trường Trạng thái mới | 1. Truy cập /admin/orders/[id]/update-status<br>2. Kiểm tra trường | Hiển thị label "Trạng thái mới *", Select với placeholder "Chọn trạng thái mới", có các option: Đã xác nhận, Đang giao, Đã giao, Đã hủy | | Pass | 11/15/2015 | |
| **GUI-CNDH-06** | Kiểm tra trường Lý do thay đổi | 1. Truy cập /admin/orders/[id]/update-status<br>2. Kiểm tra trường | Hiển thị label "Lý do thay đổi", Textarea với placeholder "Nhập lý do thay đổi trạng thái (tùy chọn)" | | Pass | 11/15/2015 | |
| **GUI-CNDH-07** | Kiểm tra checkbox Thông báo khách hàng | 1. Truy cập /admin/orders/[id]/update-status<br>2. Kiểm tra checkbox | Hiển thị checkbox với label "Gửi thông báo cho khách hàng về thay đổi trạng thái", mặc định checked | | Pass | 11/15/2015 | |
| **GUI-CNDH-08** | Kiểm tra nút Hủy | 1. Truy cập /admin/orders/[id]/update-status<br>2. Kiểm tra nút | Hiển thị nút "Hủy" variant outline, link đến /admin/orders/[id] | | Pass | 11/15/2015 | |
| **GUI-CNDH-09** | Kiểm tra nút Cập nhật trạng thái | 1. Truy cập /admin/orders/[id]/update-status<br>2. Kiểm tra nút | Hiển thị nút "Cập nhật trạng thái" với icon Save type submit | | Pass | 11/15/2015 | |

---

### Check FUNC: Cập nhật đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CNDH-01** | Mở trang cập nhật trạng thái | 1. Truy cập /admin/orders/[id]/update-status | Hiển thị trang với nút Quay lại, tiêu đề "Cập nhật trạng thái đơn hàng", mô tả, card Thông tin đơn hàng, form với trường Trạng thái mới, Lý do thay đổi, checkbox Thông báo khách hàng, nút Hủy, nút Cập nhật trạng thái | | Pass | 11/15/2015 | |
| **FUNC-CNDH-02** | Cập nhật trạng thái thành công | 1. Truy cập /admin/orders/[id]/update-status<br>2. Chọn trạng thái mới<br>3. Nhập lý do (tùy chọn)<br>4. Tích checkbox Thông báo khách hàng<br>5. Nhấn "Cập nhật trạng thái" | Hiển thị thông báo "Cập nhật trạng thái thành công", gửi thông báo cho khách hàng (nếu được chọn), chuyển về trang chi tiết đơn hàng, trạng thái được cập nhật, lịch sử cập nhật được ghi nhận | | Untested | 11/15/2015 | |
| **FUNC-CNDH-03** | Cập nhật - Thiếu Trạng thái mới | 1. Truy cập /admin/orders/[id]/update-status<br>2. Không chọn trạng thái mới<br>3. Nhấn "Cập nhật trạng thái" | Hiển thị thông báo lỗi "Vui lòng chọn trạng thái mới", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-CNDH-04** | Cập nhật - Chọn trạng thái giống hiện tại | 1. Truy cập /admin/orders/[id]/update-status<br>2. Chọn trạng thái mới giống trạng thái hiện tại<br>3. Nhấn "Cập nhật trạng thái" | Hiển thị thông báo lỗi "Trạng thái mới phải khác trạng thái hiện tại", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-CNDH-05** | Cập nhật - Không gửi thông báo | 1. Truy cập /admin/orders/[id]/update-status<br>2. Chọn trạng thái mới<br>3. Bỏ tích checkbox Thông báo khách hàng<br>4. Nhấn "Cập nhật trạng thái" | Hiển thị thông báo "Cập nhật trạng thái thành công", không gửi thông báo cho khách hàng, trạng thái được cập nhật | | Untested | 11/15/2015 | |
| **FUNC-CNDH-06** | Click nút Hủy | 1. Truy cập /admin/orders/[id]/update-status<br>2. Click nút "Hủy" | Chuyển về trang /admin/orders/[id], không lưu thông tin | | Pass | 11/15/2015 | |
| **FUNC-CNDH-07** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/orders/[id]/update-status<br>2. Chọn trạng thái mới<br>3. Tắt kết nối mạng<br>4. Nhấn "Cập nhật trạng thái" | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", form không được gửi | | Untested | 11/15/2015 | |
| **FUNC-CNDH-08** | Xử lý khi server lỗi | 1. Truy cập /admin/orders/[id]/update-status<br>2. Chọn trạng thái mới<br>3. Server trả về lỗi 500<br>4. Nhấn "Cập nhật trạng thái" | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau", form không được gửi | | Untested | 11/15/2015 | |

---

### Function: Xóa đơn hàng

#### Check GUI: Xóa đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XDH-01** | Kiểm tra Dialog xác nhận xóa | 1. Truy cập /admin/orders<br>2. Click nút Hủy (icon AlertTriangle) của một đơn hàng<br>3. Kiểm tra dialog | Hiển thị Dialog với tiêu đề "Xác nhận hủy đơn hàng", mô tả "Bạn có chắc chắn muốn hủy đơn hàng này?", textarea "Lý do hủy", nút "Hủy" variant outline, nút "Xác nhận hủy" variant destructive | | Pass | 11/15/2015 | |

---

### Check FUNC: Xóa đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XDH-01** | Hủy đơn hàng thành công | 1. Truy cập /admin/orders<br>2. Click nút Hủy của một đơn hàng<br>3. Nhập lý do hủy<br>4. Click "Xác nhận hủy" | Hiển thị thông báo "Hủy đơn hàng thành công", trạng thái đơn hàng chuyển thành "Đã hủy", đơn hàng bị ẩn hoặc cập nhật trong danh sách | | Untested | 11/15/2015 | |
| **FUNC-XDH-02** | Hủy đơn hàng - Thiếu lý do | 1. Truy cập /admin/orders<br>2. Click nút Hủy<br>3. Để trống lý do<br>4. Click "Xác nhận hủy" | Hiển thị thông báo lỗi "Vui lòng nhập lý do hủy đơn hàng", dialog không đóng | | Pass | 11/15/2015 | |
| **FUNC-XDH-03** | Hủy hủy đơn hàng | 1. Truy cập /admin/orders<br>2. Click nút Hủy<br>3. Click "Hủy" trong dialog | Dialog đóng, đơn hàng không bị hủy, vẫn ở trang danh sách | | Pass | 11/15/2015 | |
| **FUNC-XDH-04** | Hủy đơn hàng - Đơn hàng đã giao | 1. Truy cập /admin/orders<br>2. Click nút Hủy của đơn hàng đã giao | Nút Hủy không hiển thị hoặc hiển thị thông báo lỗi "Không thể hủy đơn hàng đã giao" | | Pass | 11/15/2015 | |
| **FUNC-XDH-05** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/orders<br>2. Click nút Hủy<br>3. Nhập lý do<br>4. Tắt kết nối mạng<br>5. Click "Xác nhận hủy" | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", đơn hàng không bị hủy | | Untested | 11/15/2015 | |
| **FUNC-XDH-06** | Xử lý khi server lỗi | 1. Truy cập /admin/orders<br>2. Click nút Hủy<br>3. Nhập lý do<br>4. Server trả về lỗi 500<br>5. Click "Xác nhận hủy" | Hiển thị thông báo lỗi "Lỗi hủy đơn hàng", đơn hàng không bị hủy | | Untested | 11/15/2015 | |

---

### Function: Xác nhận đơn hàng

#### Check GUI: Xác nhận đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XNDH-01** | Kiểm tra nút Xác nhận đơn hàng | 1. Truy cập /admin/orders/[id]<br>2. Kiểm tra nút | Hiển thị nút "Xác nhận đơn hàng" với icon CheckCircle, chỉ hiển thị khi trạng thái là "pending" | | Pass | 11/15/2015 | |
| **GUI-XNDH-02** | Kiểm tra Dialog xác nhận | 1. Truy cập /admin/orders/[id]/confirm<br>2. Kiểm tra dialog | Hiển thị Dialog với tiêu đề "Xác nhận đơn hàng", mô tả, card Kiểm tra tồn kho, checkbox "Xác nhận thông tin khách hàng và địa chỉ giao hàng", textarea "Ghi chú xác nhận", nút Hủy, nút "Xác nhận đơn hàng" | | Pass | 11/15/2015 | |

---

### Check FUNC: Xác nhận đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XNDH-01** | Xác nhận đơn hàng thành công | 1. Truy cập /admin/orders/[id]<br>2. Click nút "Xác nhận đơn hàng"<br>3. Kiểm tra tồn kho đủ<br>4. Tích checkbox xác nhận thông tin<br>5. Nhập ghi chú (tùy chọn)<br>6. Click "Xác nhận đơn hàng" | Hiển thị thông báo "Xác nhận đơn hàng thành công", trạng thái đơn hàng chuyển thành "Đã xác nhận", nút Xác nhận biến mất, lịch sử cập nhật được ghi nhận | | Untested | 11/15/2015 | |
| **FUNC-XNDH-02** | Xác nhận - Tồn kho không đủ | 1. Truy cập /admin/orders/[id]<br>2. Click nút "Xác nhận đơn hàng"<br>3. Kiểm tra tồn kho không đủ<br>4. Click "Xác nhận đơn hàng" | Hiển thị thông báo lỗi "Tồn kho không đủ để xác nhận đơn hàng", đơn hàng không được xác nhận | | Untested | 11/15/2015 | |
| **FUNC-XNDH-03** | Xác nhận - Không tích checkbox | 1. Truy cập /admin/orders/[id]<br>2. Click nút "Xác nhận đơn hàng"<br>3. Không tích checkbox xác nhận thông tin<br>4. Click "Xác nhận đơn hàng" | Hiển thị thông báo lỗi "Vui lòng xác nhận thông tin khách hàng và địa chỉ giao hàng", đơn hàng không được xác nhận | | Pass | 11/15/2015 | |
| **FUNC-XNDH-04** | Từ chối đơn hàng | 1. Truy cập /admin/orders/[id]<br>2. Click nút "Xác nhận đơn hàng"<br>3. Click "Từ chối đơn hàng" | Hiển thị thông báo "Từ chối đơn hàng thành công", trạng thái đơn hàng chuyển thành "Đã hủy" | | Untested | 11/15/2015 | |
| **FUNC-XNDH-05** | Hủy xác nhận | 1. Truy cập /admin/orders/[id]<br>2. Click nút "Xác nhận đơn hàng"<br>3. Click "Hủy" | Dialog đóng, vẫn ở trang chi tiết, đơn hàng không được xác nhận | | Pass | 11/15/2015 | |
| **FUNC-XNDH-06** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/orders/[id]<br>2. Click nút "Xác nhận đơn hàng"<br>3. Tắt kết nối mạng<br>4. Click "Xác nhận đơn hàng" | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", đơn hàng không được xác nhận | | Untested | 11/15/2015 | |
| **FUNC-XNDH-07** | Xử lý khi server lỗi | 1. Truy cập /admin/orders/[id]<br>2. Click nút "Xác nhận đơn hàng"<br>3. Server trả về lỗi 500<br>4. Click "Xác nhận đơn hàng" | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau", đơn hàng không được xác nhận | | Untested | 11/15/2015 | |

---

### Function: In đơn hàng

#### Check GUI: In đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-IDH-01** | Kiểm tra modal In đơn hàng | 1. Truy cập /admin/orders<br>2. Click nút In (icon Printer) của một đơn hàng<br>3. Kiểm tra modal | Hiển thị Dialog với tiêu đề "In đơn hàng", mô tả "Xuất thông tin đơn hàng để in" | | Pass | 11/15/2015 | |
| **GUI-IDH-02** | Kiểm tra Radio Group Loại tài liệu | 1. Truy cập /admin/orders<br>2. Click nút In<br>3. Kiểm tra Radio Group | Hiển thị Radio Group với các option: Phiếu giao hàng, Hóa đơn, Phiếu xuất kho | | Pass | 11/15/2015 | |
| **GUI-IDH-03** | Kiểm tra Preview tài liệu | 1. Truy cập /admin/orders<br>2. Click nút In<br>3. Kiểm tra Preview | Hiển thị preview tài liệu với đầy đủ thông tin: Thông tin đơn hàng, Thông tin khách hàng, Danh sách sản phẩm, Thông tin vận chuyển | | Pass | 11/15/2015 | |
| **GUI-IDH-04** | Kiểm tra textarea Ghi chú in | 1. Truy cập /admin/orders<br>2. Click nút In<br>3. Kiểm tra textarea | Hiển thị label "Ghi chú in", Textarea với placeholder "Ghi chú thêm cho tài liệu in (tùy chọn)" | | Pass | 11/15/2015 | |
| **GUI-IDH-05** | Kiểm tra nút Xem trước | 1. Truy cập /admin/orders<br>2. Click nút In<br>3. Kiểm tra nút | Hiển thị nút "Xem trước" variant outline | | Pass | 11/15/2015 | |
| **GUI-IDH-06** | Kiểm tra nút Xuất PDF | 1. Truy cập /admin/orders<br>2. Click nút In<br>3. Kiểm tra nút | Hiển thị nút "Xuất PDF" variant outline | | Pass | 11/15/2015 | |
| **GUI-IDH-07** | Kiểm tra nút In trực tiếp | 1. Truy cập /admin/orders<br>2. Click nút In<br>3. Kiểm tra nút | Hiển thị nút "In trực tiếp" type submit | | Pass | 11/15/2015 | |
| **GUI-IDH-08** | Kiểm tra nút Hủy | 1. Truy cập /admin/orders<br>2. Click nút In<br>3. Kiểm tra nút | Hiển thị nút "Hủy" variant outline | | Pass | 11/15/2015 | |

---

### Check FUNC: In đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-IDH-01** | Mở modal in đơn hàng | 1. Truy cập /admin/orders<br>2. Click nút In của một đơn hàng | Hiển thị Dialog với tiêu đề "In đơn hàng", Radio Group Loại tài liệu, Preview tài liệu, textarea Ghi chú in, các nút Xem trước, Xuất PDF, In trực tiếp, Hủy | | Pass | 11/15/2015 | |
| **FUNC-IDH-02** | Chọn loại tài liệu | 1. Truy cập /admin/orders<br>2. Click nút In<br>3. Chọn loại tài liệu (VD: Hóa đơn) | Preview tài liệu được cập nhật theo loại tài liệu đã chọn | | Pass | 11/15/2015 | |
| **FUNC-IDH-03** | Xuất PDF thành công | 1. Truy cập /admin/orders<br>2. Click nút In<br>3. Chọn loại tài liệu<br>4. Click "Xuất PDF" | Tải về file PDF đơn hàng với đầy đủ thông tin, định dạng chuẩn | | Untested | 11/15/2015 | |
| **FUNC-IDH-04** | In trực tiếp thành công | 1. Truy cập /admin/orders<br>2. Click nút In<br>3. Chọn loại tài liệu<br>4. Click "In trực tiếp" | Hiển thị thông báo "Đã gửi lệnh in", lệnh in được gửi đến máy in | | Untested | 11/15/2015 | |
| **FUNC-IDH-05** | Xem trước tài liệu | 1. Truy cập /admin/orders<br>2. Click nút In<br>3. Click "Xem trước" | Hiển thị preview tài liệu với đầy đủ thông tin, có thể zoom in/out | | Pass | 11/15/2015 | |
| **FUNC-IDH-06** | Click nút Hủy | 1. Truy cập /admin/orders<br>2. Click nút In<br>3. Click "Hủy" | Modal đóng, không in tài liệu | | Pass | 11/15/2015 | |
| **FUNC-IDH-07** | Xuất PDF - Lỗi tạo file | 1. Truy cập /admin/orders<br>2. Click nút In<br>3. Click "Xuất PDF"<br>4. Server lỗi khi tạo PDF | Hiển thị thông báo lỗi "Không thể tạo file PDF. Vui lòng thử lại sau" | | Untested | 11/15/2015 | |
| **FUNC-IDH-08** | In trực tiếp - Không có máy in | 1. Truy cập /admin/orders<br>2. Click nút In<br>3. Click "In trực tiếp"<br>4. Không có máy in được kết nối | Hiển thị thông báo lỗi "Không tìm thấy máy in. Vui lòng kiểm tra kết nối máy in" | | Untested | 11/15/2015 | |
| **FUNC-IDH-09** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/orders<br>2. Click nút In<br>3. Tắt kết nối mạng<br>4. Click "Xuất PDF" | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại" | | Untested | 11/15/2015 | |
| **FUNC-IDH-10** | Xử lý khi server lỗi | 1. Truy cập /admin/orders<br>2. Click nút In<br>3. Server trả về lỗi 500<br>4. Click "Xuất PDF" | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau" | | Untested | 11/15/2015 | |

---

### Function: Tạo đơn hàng mới

#### Check GUI: Tạo đơn hàng mới

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-TDHM-01** | Kiểm tra nút Quay lại | 1. Truy cập /admin/orders/new<br>2. Kiểm tra nút Quay lại | Hiển thị nút "Quay lại" với icon ArrowLeft variant outline size sm, link đến /admin/orders | | Pass | 11/15/2015 | |
| **GUI-TDHM-02** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/orders/new<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Tạo đơn hàng mới" với kích thước text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-TDHM-03** | Kiểm tra mô tả trang | 1. Truy cập /admin/orders/new<br>2. Kiểm tra mô tả | Hiển thị mô tả "Tạo đơn hàng mới cho khách hàng" màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-TDHM-04** | Kiểm tra card Thông tin khách hàng | 1. Truy cập /admin/orders/new<br>2. Kiểm tra card | Hiển thị card "Thông tin khách hàng" với các trường: Chọn khách hàng (Select/Dropdown), Tên khách hàng (input), Email (input), Số điện thoại (input), Địa chỉ giao hàng (Textarea) | | Pass | 11/15/2015 | |
| **GUI-TDHM-05** | Kiểm tra card Danh sách sản phẩm | 1. Truy cập /admin/orders/new<br>2. Kiểm tra card | Hiển thị card "Danh sách sản phẩm" với nút "Thêm sản phẩm", Table hiển thị các cột: Sản phẩm, Số lượng, Đơn giá, Thành tiền, Thao tác | | Pass | 11/15/2015 | |
| **GUI-TDHM-06** | Kiểm tra card Thông tin thanh toán | 1. Truy cập /admin/orders/new<br>2. Kiểm tra card | Hiển thị card "Thông tin thanh toán" với các trường: Phương thức thanh toán (Select), Trạng thái thanh toán (Select), Ghi chú (Textarea) | | Pass | 11/15/2015 | |
| **GUI-TDHM-07** | Kiểm tra card Thông tin vận chuyển | 1. Truy cập /admin/orders/new<br>2. Kiểm tra card | Hiển thị card "Thông tin vận chuyển" với các trường: Phương thức vận chuyển (Select), Phí vận chuyển (number input), Ngày dự kiến giao hàng (DatePicker) | | Pass | 11/15/2015 | |
| **GUI-TDHM-08** | Kiểm tra card Tổng kết | 1. Truy cập /admin/orders/new<br>2. Kiểm tra card | Hiển thị card "Tổng kết" với: Tổng tiền sản phẩm, Phí vận chuyển, Tổng cộng (font-bold text-lg) | | Pass | 11/15/2015 | |
| **GUI-TDHM-09** | Kiểm tra nút Hủy | 1. Truy cập /admin/orders/new<br>2. Kiểm tra nút | Hiển thị nút "Hủy" variant outline, link đến /admin/orders | | Pass | 11/15/2015 | |
| **GUI-TDHM-10** | Kiểm tra nút Tạo đơn hàng | 1. Truy cập /admin/orders/new<br>2. Kiểm tra nút | Hiển thị nút "Tạo đơn hàng" type submit | | Pass | 11/15/2015 | |

---

### Check FUNC: Tạo đơn hàng mới

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TDHM-01** | Mở trang tạo đơn hàng mới | 1. Truy cập /admin/orders/new | Hiển thị trang với nút Quay lại, tiêu đề "Tạo đơn hàng mới", mô tả, form với các card: Thông tin khách hàng, Danh sách sản phẩm, Thông tin thanh toán, Thông tin vận chuyển, Tổng kết, các nút Hủy, Tạo đơn hàng | | Pass | 11/15/2015 | |
| **FUNC-TDHM-02** | Tạo đơn hàng thành công | 1. Truy cập /admin/orders/new<br>2. Chọn khách hàng hoặc nhập thông tin khách hàng<br>3. Thêm sản phẩm vào đơn hàng<br>4. Chọn phương thức thanh toán<br>5. Chọn phương thức vận chuyển<br>6. Nhấn "Tạo đơn hàng" | Hiển thị thông báo "Tạo đơn hàng thành công", chuyển về trang /admin/orders, đơn hàng được tạo với trạng thái "Chờ xác nhận" | | Untested | 11/15/2015 | |
| **FUNC-TDHM-03** | Tạo đơn hàng - Thiếu thông tin khách hàng | 1. Truy cập /admin/orders/new<br>2. Không chọn/nhập thông tin khách hàng<br>3. Thêm sản phẩm<br>4. Nhấn "Tạo đơn hàng" | Hiển thị thông báo lỗi "Vui lòng chọn hoặc nhập thông tin khách hàng", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-TDHM-04** | Tạo đơn hàng - Chưa thêm sản phẩm | 1. Truy cập /admin/orders/new<br>2. Chọn khách hàng<br>3. Không thêm sản phẩm<br>4. Nhấn "Tạo đơn hàng" | Hiển thị thông báo lỗi "Vui lòng thêm ít nhất một sản phẩm vào đơn hàng", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-TDHM-05** | Thêm sản phẩm vào đơn hàng | 1. Truy cập /admin/orders/new<br>2. Click nút "Thêm sản phẩm"<br>3. Chọn sản phẩm và số lượng<br>4. Click "Thêm" | Sản phẩm được thêm vào bảng danh sách sản phẩm, tổng kết được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-TDHM-06** | Xóa sản phẩm khỏi đơn hàng | 1. Truy cập /admin/orders/new<br>2. Thêm sản phẩm<br>3. Click nút Xóa của sản phẩm | Sản phẩm bị xóa khỏi danh sách, tổng kết được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-TDHM-07** | Cập nhật số lượng sản phẩm | 1. Truy cập /admin/orders/new<br>2. Thêm sản phẩm<br>3. Thay đổi số lượng | Tổng kết được cập nhật tự động theo số lượng mới | | Pass | 11/15/2015 | |
| **FUNC-TDHM-08** | Tính tổng kết tự động | 1. Truy cập /admin/orders/new<br>2. Thêm sản phẩm<br>3. Nhập phí vận chuyển | Tổng kết được tính tự động: Tổng tiền sản phẩm + Phí vận chuyển = Tổng cộng | | Pass | 11/15/2015 | |
| **FUNC-TDHM-09** | Click nút Hủy | 1. Truy cập /admin/orders/new<br>2. Click nút "Hủy" | Chuyển về trang /admin/orders, không lưu thông tin | | Pass | 11/15/2015 | |
| **FUNC-TDHM-10** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/orders/new<br>2. Điền đầy đủ thông tin<br>3. Tắt kết nối mạng<br>4. Nhấn "Tạo đơn hàng" | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", form không được gửi | | Untested | 11/15/2015 | |
| **FUNC-TDHM-11** | Xử lý khi server lỗi | 1. Truy cập /admin/orders/new<br>2. Điền đầy đủ thông tin<br>3. Server trả về lỗi 500<br>4. Nhấn "Tạo đơn hàng" | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau", form không được gửi | | Untested | 11/15/2015 | |

---

**Người tạo:** Testing Team  
**Ngày cập nhật:** 11/15/2015  
**Phiên bản:** 1.0

