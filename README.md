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
| **Pass** | 99 |
| **Fail** | 0 |
| **Untested** | 22 |
| **N/A** | 0 |
| **Number of Test cases** | 121 |

---

## Test Cases

### Function: Hiển thị danh sách đơn hàng

#### Check GUI: Hiển thị danh sách đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DSDH-01** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/orders<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Quản lý đơn hàng" | | Pass | 11/15/2015 | |
| **GUI-DSDH-02** | Kiểm tra mô tả trang | 1. Truy cập /admin/orders<br>2. Kiểm tra mô tả | Hiển thị mô tả "Xử lý và theo dõi tất cả đơn hàng" | | Pass | 11/15/2015 | |
| **GUI-DSDH-03** | Kiểm tra nút In báo cáo | 1. Truy cập /admin/orders<br>2. Kiểm tra nút In báo cáo | Hiển thị nút "In báo cáo" với icon Printer | | Pass | 11/15/2015 | |
| **GUI-DSDH-04** | Kiểm tra nút Bộ lọc nâng cao | 1. Truy cập /admin/orders<br>2. Kiểm tra nút Bộ lọc nâng cao | Hiển thị nút "Bộ lọc nâng cao" với icon Filter | | Pass | 11/15/2015 | |
| **GUI-DSDH-05** | Kiểm tra thẻ thống kê trạng thái | 1. Truy cập /admin/orders<br>2. Kiểm tra các thẻ thống kê | Hiển thị 5 thẻ thống kê: Chờ xác nhận, Đã xác nhận, Đang giao, Đã giao, Đã hủy, mỗi thẻ có icon và số lượng tương ứng | | Pass | 11/15/2015 | |
| **GUI-DSDH-06** | Kiểm tra ô tìm kiếm | 1. Truy cập /admin/orders<br>2. Kiểm tra ô tìm kiếm | Hiển thị ô tìm kiếm với icon Search bên trái, placeholder "Tìm kiếm đơn hàng, khách hàng..." | | Pass | 11/15/2015 | |
| **GUI-DSDH-07** | Kiểm tra dropdown lọc trạng thái | 1. Truy cập /admin/orders<br>2. Kiểm tra dropdown lọc trạng thái | Hiển thị dropdown Select với các tùy chọn: Tất cả, Chờ xác nhận, Đã xác nhận, Đang giao, Đã giao, Đã hủy, mỗi tùy chọn có số lượng trong ngoặc | | Pass | 11/15/2015 | |
| **GUI-DSDH-08** | Kiểm tra dropdown lọc phương thức thanh toán | 1. Truy cập /admin/orders<br>2. Kiểm tra dropdown lọc thanh toán | Hiển thị dropdown Select với các tùy chọn: Tất cả, COD, Banking, Credit Card, E-wallet | | Pass | 11/15/2015 | |
| **GUI-DSDH-09** | Kiểm tra bộ lọc ngày tháng | 1. Truy cập /admin/orders<br>2. Kiểm tra bộ lọc ngày | Hiển thị 2 input date với text "đến" ở giữa | | Pass | 11/15/2015 | |
| **GUI-DSDH-10** | Kiểm tra nút Áp dụng bộ lọc | 1. Truy cập /admin/orders<br>2. Kiểm tra nút Áp dụng | Hiển thị nút "Áp dụng" với icon Filter | | Pass | 11/15/2015 | |
| **GUI-DSDH-11** | Kiểm tra bảng danh sách đơn hàng | 1. Truy cập /admin/orders<br>2. Kiểm tra bảng | Hiển thị bảng với các cột: Mã đơn hàng, Khách hàng, Sản phẩm, Tổng tiền, Thanh toán, Trạng thái, Ngày tạo, Thao tác | | Pass | 11/15/2015 | |
| **GUI-DSDH-12** | Kiểm tra badge trạng thái đơn hàng | 1. Truy cập /admin/orders<br>2. Kiểm tra badge trạng thái | Mỗi đơn hàng hiển thị badge trạng thái với icon và text tương ứng (Chờ xác nhận, Đã xác nhận, Đang giao, Đã giao, Đã hủy) | | Pass | 11/15/2015 | |
| **GUI-DSDH-13** | Kiểm tra nút Xem chi tiết | 1. Truy cập /admin/orders<br>2. Kiểm tra nút Xem | Mỗi hàng có nút với icon Eye để xem chi tiết | | Pass | 11/15/2015 | |
| **GUI-DSDH-14** | Kiểm tra nút Cập nhật trạng thái | 1. Truy cập /admin/orders<br>2. Kiểm tra nút Cập nhật | Mỗi hàng có nút với icon Edit để cập nhật trạng thái | | Pass | 11/15/2015 | |
| **GUI-DSDH-15** | Kiểm tra nút In đơn hàng | 1. Truy cập /admin/orders<br>2. Kiểm tra nút In | Mỗi hàng có nút với icon Printer để in đơn hàng | | Pass | 11/15/2015 | |
| **GUI-DSDH-16** | Kiểm tra nút Hủy đơn hàng | 1. Truy cập /admin/orders<br>2. Kiểm tra nút Hủy | Các đơn hàng chưa giao hoặc chưa hủy có nút với icon AlertTriangle để hủy đơn hàng | | Pass | 11/15/2015 | |
| **GUI-DSDH-17** | Kiểm tra phân trang | 1. Truy cập /admin/orders<br>2. Kiểm tra phân trang | Hiển thị thông tin "Hiển thị 1-5 trong 156 đơn hàng", các nút Trước, số trang, nút Sau | | Pass | 11/15/2015 | |

---

### Check FUNC: Hiển thị danh sách đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DSDH-01** | Mở trang danh sách đơn hàng | 1. Truy cập /admin/orders | Hiển thị trang với tiêu đề, mô tả, thẻ thống kê, bộ lọc, bảng danh sách đơn hàng, phân trang | | Pass | 11/15/2015 | |
| **FUNC-DSDH-02** | Tìm kiếm đơn hàng theo mã | 1. Truy cập /admin/orders<br>2. Nhập mã đơn hàng vào ô tìm kiếm<br>3. Nhấn Enter hoặc click Áp dụng | Bảng hiển thị các đơn hàng có mã khớp với từ khóa tìm kiếm | | Untested | 11/15/2015 | |
| **FUNC-DSDH-03** | Tìm kiếm đơn hàng theo tên khách hàng | 1. Truy cập /admin/orders<br>2. Nhập tên khách hàng vào ô tìm kiếm<br>3. Nhấn Enter hoặc click Áp dụng | Bảng hiển thị các đơn hàng của khách hàng có tên khớp với từ khóa | | Untested | 11/15/2015 | |
| **FUNC-DSDH-04** | Lọc đơn hàng theo trạng thái | 1. Truy cập /admin/orders<br>2. Chọn trạng thái từ dropdown<br>3. Nhấn Áp dụng | Bảng chỉ hiển thị các đơn hàng có trạng thái đã chọn | | Pass | 11/15/2015 | |
| **FUNC-DSDH-05** | Lọc đơn hàng theo phương thức thanh toán | 1. Truy cập /admin/orders<br>2. Chọn phương thức thanh toán từ dropdown<br>3. Nhấn Áp dụng | Bảng chỉ hiển thị các đơn hàng có phương thức thanh toán đã chọn | | Pass | 11/15/2015 | |
| **FUNC-DSDH-06** | Lọc đơn hàng theo khoảng thời gian | 1. Truy cập /admin/orders<br>2. Chọn ngày bắt đầu và ngày kết thúc<br>3. Nhấn Áp dụng | Bảng chỉ hiển thị các đơn hàng được tạo trong khoảng thời gian đã chọn | | Pass | 11/15/2015 | |
| **FUNC-DSDH-07** | Click nút Xem chi tiết | 1. Truy cập /admin/orders<br>2. Click nút Eye trên một đơn hàng | Chuyển đến trang chi tiết đơn hàng /admin/orders/[id] | | Pass | 11/15/2015 | |
| **FUNC-DSDH-08** | Click nút Cập nhật trạng thái | 1. Truy cập /admin/orders<br>2. Click nút Edit trên một đơn hàng | Chuyển đến trang /admin/orders/[id]/update-status | | Pass | 11/15/2015 | |
| **FUNC-DSDH-09** | Click nút In đơn hàng | 1. Truy cập /admin/orders<br>2. Click nút Printer trên một đơn hàng | Mở modal in đơn hàng với thông tin đơn hàng | | Pass | 11/15/2015 | |
| **FUNC-DSDH-10** | Phân trang - Chuyển trang | 1. Truy cập /admin/orders<br>2. Click nút số trang hoặc nút Sau | Bảng hiển thị các đơn hàng của trang tiếp theo | | Untested | 11/15/2015 | |
| **FUNC-DSDH-11** | Phân trang - Quay lại trang trước | 1. Truy cập /admin/orders<br>2. Đang ở trang 2<br>3. Click nút Trước | Bảng hiển thị các đơn hàng của trang trước | | Untested | 11/15/2015 | |
| **FUNC-DSDH-12** | Hiển thị số lượng đơn hàng theo trạng thái | 1. Truy cập /admin/orders<br>2. Kiểm tra các thẻ thống kê | Các thẻ thống kê hiển thị số lượng chính xác đơn hàng theo từng trạng thái | | Untested | 11/15/2015 | |
| **FUNC-DSDH-13** | Sắp xếp đơn hàng | 1. Truy cập /admin/orders<br>2. Click vào header cột để sắp xếp | Bảng sắp xếp đơn hàng theo cột đã chọn (tăng dần/giảm dần) | | Untested | 11/15/2015 | |

---

### Function: Xem chi tiết đơn hàng

#### Check GUI: Xem chi tiết đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XCTDH-01** | Kiểm tra nút Quay lại | 1. Truy cập /admin/orders/[id]<br>2. Kiểm tra nút Quay lại | Hiển thị nút "Quay lại" với icon ArrowLeft | | Pass | 11/15/2015 | |
| **GUI-XCTDH-02** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/orders/[id]<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Chi tiết đơn hàng" và mã đơn hàng | | Pass | 11/15/2015 | |
| **GUI-XCTDH-03** | Kiểm tra nút Xác nhận đơn hàng | 1. Truy cập /admin/orders/[id]<br>2. Kiểm tra nút Xác nhận | Nếu đơn hàng ở trạng thái pending, hiển thị nút "Xác nhận đơn hàng" với icon CheckCircle | | Pass | 11/15/2015 | |
| **GUI-XCTDH-04** | Kiểm tra nút Cập nhật trạng thái | 1. Truy cập /admin/orders/[id]<br>2. Kiểm tra nút Cập nhật | Hiển thị nút "Cập nhật trạng thái" với icon Edit | | Pass | 11/15/2015 | |
| **GUI-XCTDH-05** | Kiểm tra nút In đơn hàng | 1. Truy cập /admin/orders/[id]<br>2. Kiểm tra nút In | Hiển thị nút "In đơn hàng" với icon Printer | | Pass | 11/15/2015 | |
| **GUI-XCTDH-06** | Kiểm tra nút Hủy đơn hàng | 1. Truy cập /admin/orders/[id]<br>2. Kiểm tra nút Hủy | Nếu đơn hàng chưa giao và chưa hủy, hiển thị nút "Hủy đơn hàng" với icon XCircle | | Pass | 11/15/2015 | |
| **GUI-XCTDH-07** | Kiểm tra card Thông tin đơn hàng | 1. Truy cập /admin/orders/[id]<br>2. Kiểm tra card Thông tin đơn hàng | Hiển thị card với tiêu đề "Thông tin đơn hàng", các thông tin: Mã đơn hàng, Ngày tạo, Trạng thái, Tổng tiền | | Pass | 11/15/2015 | |
| **GUI-XCTDH-08** | Kiểm tra card Thông tin khách hàng | 1. Truy cập /admin/orders/[id]<br>2. Kiểm tra card Thông tin khách hàng | Hiển thị card với tiêu đề "Thông tin khách hàng", các thông tin: Tên, Email, Số điện thoại, Địa chỉ giao hàng | | Pass | 11/15/2015 | |
| **GUI-XCTDH-09** | Kiểm tra card Danh sách sản phẩm | 1. Truy cập /admin/orders/[id]<br>2. Kiểm tra card Danh sách sản phẩm | Hiển thị card với tiêu đề "Danh sách sản phẩm", bảng với các cột: Sản phẩm, Số lượng, Đơn giá, Thành tiền, tổng cộng ở cuối | | Pass | 11/15/2015 | |
| **GUI-XCTDH-10** | Kiểm tra card Lịch sử cập nhật | 1. Truy cập /admin/orders/[id]<br>2. Kiểm tra card Lịch sử | Hiển thị card với tiêu đề "Lịch sử cập nhật", danh sách các mốc thời gian với mô tả và người thực hiện | | Pass | 11/15/2015 | |
| **GUI-XCTDH-11** | Kiểm tra card Thông tin thanh toán | 1. Truy cập /admin/orders/[id]<br>2. Kiểm tra card Thông tin thanh toán | Hiển thị card với tiêu đề "Thông tin thanh toán", các thông tin: Phương thức thanh toán, Trạng thái thanh toán | | Pass | 11/15/2015 | |
| **GUI-XCTDH-12** | Kiểm tra card Thông tin vận chuyển | 1. Truy cập /admin/orders/[id]<br>2. Kiểm tra card Thông tin vận chuyển | Hiển thị card với tiêu đề "Thông tin vận chuyển", các thông tin: Đơn vị vận chuyển, Mã vận đơn, Dự kiến giao hàng | | Pass | 11/15/2015 | |
| **GUI-XCTDH-13** | Kiểm tra card Ghi chú | 1. Truy cập /admin/orders/[id]<br>2. Kiểm tra card Ghi chú | Nếu có ghi chú, hiển thị card với tiêu đề "Ghi chú" và nội dung ghi chú | | Pass | 11/15/2015 | |

---

### Check FUNC: Xem chi tiết đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XCTDH-01** | Mở trang chi tiết đơn hàng | 1. Truy cập /admin/orders/[id] | Hiển thị đầy đủ thông tin đơn hàng: thông tin đơn hàng, khách hàng, danh sách sản phẩm, lịch sử cập nhật, thông tin thanh toán, vận chuyển | | Pass | 11/15/2015 | |
| **FUNC-XCTDH-02** | Click nút Quay lại | 1. Truy cập /admin/orders/[id]<br>2. Click nút "Quay lại" | Chuyển về trang /admin/orders | | Pass | 11/15/2015 | |
| **FUNC-XCTDH-03** | Xác nhận đơn hàng thành công | 1. Truy cập /admin/orders/[id]<br>2. Đơn hàng ở trạng thái pending<br>3. Click "Xác nhận đơn hàng" | Hiển thị thông báo "Xác nhận đơn hàng thành công", trạng thái đơn hàng chuyển sang "Đã xác nhận" | | Untested | 11/15/2015 | |
| **FUNC-XCTDH-04** | Click nút Cập nhật trạng thái | 1. Truy cập /admin/orders/[id]<br>2. Click "Cập nhật trạng thái" | Chuyển đến trang /admin/orders/[id]/update-status | | Pass | 11/15/2015 | |
| **FUNC-XCTDH-05** | Click nút In đơn hàng | 1. Truy cập /admin/orders/[id]<br>2. Click "In đơn hàng" | Hiển thị thông báo "Đã gửi lệnh in", mở cửa sổ in hoặc tải file PDF | | Untested | 11/15/2015 | |
| **FUNC-XCTDH-06** | Hủy đơn hàng - Mở dialog | 1. Truy cập /admin/orders/[id]<br>2. Click "Hủy đơn hàng" | Mở Dialog với tiêu đề "Xác nhận hủy đơn hàng", mô tả, trường nhập lý do hủy, 2 nút (Hủy, Xác nhận hủy) | | Pass | 11/15/2015 | |
| **FUNC-XCTDH-07** | Hủy đơn hàng - Thiếu lý do | 1. Truy cập /admin/orders/[id]<br>2. Click "Hủy đơn hàng"<br>3. Để trống lý do<br>4. Click "Xác nhận hủy" | Hiển thị thông báo lỗi "Vui lòng nhập lý do hủy đơn hàng" | | Pass | 11/15/2015 | |
| **FUNC-XCTDH-08** | Hủy đơn hàng thành công | 1. Truy cập /admin/orders/[id]<br>2. Click "Hủy đơn hàng"<br>3. Nhập lý do hủy<br>4. Click "Xác nhận hủy" | Hiển thị thông báo "Hủy đơn hàng thành công", chuyển về trang /admin/orders, trạng thái đơn hàng chuyển sang "Đã hủy" | | Untested | 11/15/2015 | |
| **FUNC-XCTDH-09** | Hủy dialog hủy đơn hàng | 1. Truy cập /admin/orders/[id]<br>2. Click "Hủy đơn hàng"<br>3. Click nút "Hủy" trong dialog | Dialog đóng, không hủy đơn hàng | | Pass | 11/15/2015 | |
| **FUNC-XCTDH-10** | Hiển thị hình ảnh sản phẩm | 1. Truy cập /admin/orders/[id]<br>2. Kiểm tra danh sách sản phẩm | Mỗi sản phẩm hiển thị hình ảnh thumbnail, tên sản phẩm | | Pass | 11/15/2015 | |
| **FUNC-XCTDH-11** | Tính tổng tiền đơn hàng | 1. Truy cập /admin/orders/[id]<br>2. Kiểm tra tổng tiền | Tổng tiền được tính đúng bằng tổng thành tiền của tất cả sản phẩm | | Pass | 11/15/2015 | |

---

### Function: Cập nhật đơn hàng

#### Check GUI: Cập nhật đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CNDH-01** | Kiểm tra nút Quay lại | 1. Truy cập /admin/orders/[id]/update-status<br>2. Kiểm tra nút Quay lại | Hiển thị nút "Quay lại" với icon ArrowLeft | | Pass | 11/15/2015 | |
| **GUI-CNDH-02** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/orders/[id]/update-status<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Cập nhật trạng thái đơn hàng" và mã đơn hàng | | Pass | 11/15/2015 | |
| **GUI-CNDH-03** | Kiểm tra card Thông tin đơn hàng | 1. Truy cập /admin/orders/[id]/update-status<br>2. Kiểm tra card Thông tin đơn hàng | Hiển thị card với tiêu đề "Thông tin đơn hàng", các thông tin: Mã đơn hàng, Khách hàng, Tổng tiền, Ngày tạo | | Pass | 11/15/2015 | |
| **GUI-CNDH-04** | Kiểm tra card Trạng thái hiện tại | 1. Truy cập /admin/orders/[id]/update-status<br>2. Kiểm tra card Trạng thái hiện tại | Hiển thị card với tiêu đề "Trạng thái hiện tại", badge trạng thái với icon, text trạng thái, thời gian cập nhật lần cuối | | Pass | 11/15/2015 | |
| **GUI-CNDH-05** | Kiểm tra dropdown chọn trạng thái mới | 1. Truy cập /admin/orders/[id]/update-status<br>2. Kiểm tra dropdown | Hiển thị Select với placeholder "Chọn trạng thái mới...", các tùy chọn trạng thái (loại trừ trạng thái hiện tại) | | Pass | 11/15/2015 | |
| **GUI-CNDH-06** | Kiểm tra preview trạng thái mới | 1. Truy cập /admin/orders/[id]/update-status<br>2. Chọn trạng thái mới<br>3. Kiểm tra preview | Hiển thị alert với badge trạng thái mới và text "Trạng thái mới sẽ được áp dụng" | | Pass | 11/15/2015 | |
| **GUI-CNDH-07** | Kiểm tra trường Lý do thay đổi | 1. Truy cập /admin/orders/[id]/update-status<br>2. Kiểm tra trường Lý do | Hiển thị card với tiêu đề "Lý do thay đổi", textarea với placeholder "Nhập lý do thay đổi trạng thái..." | | Pass | 11/15/2015 | |
| **GUI-CNDH-08** | Kiểm tra card Thời gian cập nhật | 1. Truy cập /admin/orders/[id]/update-status<br>2. Kiểm tra card Thời gian | Hiển thị card với tiêu đề "Thời gian cập nhật", icon Clock, thời gian thực hiện thay đổi | | Pass | 11/15/2015 | |
| **GUI-CNDH-09** | Kiểm tra card Thông tin khách hàng | 1. Truy cập /admin/orders/[id]/update-status<br>2. Kiểm tra card Thông tin khách hàng | Hiển thị card với tiêu đề "Thông tin khách hàng", các thông tin: Tên, Email, Số điện thoại | | Pass | 11/15/2015 | |
| **GUI-CNDH-10** | Kiểm tra checkbox Thông báo khách hàng | 1. Truy cập /admin/orders/[id]/update-status<br>2. Kiểm tra checkbox | Hiển thị checkbox "Gửi thông báo cho khách hàng" với mô tả, mặc định được tích | | Pass | 11/15/2015 | |
| **GUI-CNDH-11** | Kiểm tra nút Cập nhật trạng thái | 1. Truy cập /admin/orders/[id]/update-status<br>2. Kiểm tra nút Cập nhật | Hiển thị nút "Cập nhật trạng thái" với icon Save, bị disable khi chưa chọn trạng thái hoặc chưa nhập lý do | | Pass | 11/15/2015 | |
| **GUI-CNDH-12** | Kiểm tra nút Hủy | 1. Truy cập /admin/orders/[id]/update-status<br>2. Kiểm tra nút Hủy | Hiển thị nút "Hủy" với icon X | | Pass | 11/15/2015 | |
| **GUI-CNDH-13** | Kiểm tra card Lưu ý | 1. Truy cập /admin/orders/[id]/update-status<br>2. Kiểm tra card Lưu ý | Hiển thị card với tiêu đề "Lưu ý", danh sách các lưu ý về thay đổi trạng thái | | Pass | 11/15/2015 | |

---

### Check FUNC: Cập nhật đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CNDH-01** | Mở trang cập nhật trạng thái | 1. Truy cập /admin/orders/[id]/update-status | Hiển thị trang với thông tin đơn hàng, trạng thái hiện tại, form chọn trạng thái mới, nhập lý do | | Pass | 11/15/2015 | |
| **FUNC-CNDH-02** | Chọn trạng thái mới | 1. Truy cập /admin/orders/[id]/update-status<br>2. Click dropdown chọn trạng thái<br>3. Chọn một trạng thái | Dropdown hiển thị trạng thái đã chọn, hiển thị preview trạng thái mới | | Pass | 11/15/2015 | |
| **FUNC-CNDH-03** | Cập nhật trạng thái - Thiếu trạng thái | 1. Truy cập /admin/orders/[id]/update-status<br>2. Nhập lý do<br>3. Click "Cập nhật trạng thái" | Hiển thị thông báo lỗi "Vui lòng chọn trạng thái mới", nút Cập nhật bị disable | | Pass | 11/15/2015 | |
| **FUNC-CNDH-04** | Cập nhật trạng thái - Thiếu lý do | 1. Truy cập /admin/orders/[id]/update-status<br>2. Chọn trạng thái mới<br>3. Để trống lý do<br>4. Click "Cập nhật trạng thái" | Hiển thị thông báo lỗi "Vui lòng nhập lý do thay đổi trạng thái", nút Cập nhật bị disable | | Pass | 11/15/2015 | |
| **FUNC-CNDH-05** | Cập nhật trạng thái thành công | 1. Truy cập /admin/orders/[id]/update-status<br>2. Chọn trạng thái mới<br>3. Nhập lý do<br>4. Click "Cập nhật trạng thái" | Hiển thị thông báo "Cập nhật trạng thái thành công", nếu có tích checkbox thông báo thì hiển thị "Đã gửi thông báo cho khách hàng", chuyển về trang chi tiết đơn hàng | | Untested | 11/15/2015 | |
| **FUNC-CNDH-06** | Cập nhật trạng thái với thông báo khách hàng | 1. Truy cập /admin/orders/[id]/update-status<br>2. Chọn trạng thái mới<br>3. Nhập lý do<br>4. Tích checkbox thông báo<br>5. Click "Cập nhật trạng thái" | Cập nhật thành công, gửi email và SMS thông báo cho khách hàng về thay đổi trạng thái | | Untested | 11/15/2015 | |
| **FUNC-CNDH-07** | Cập nhật trạng thái không thông báo khách hàng | 1. Truy cập /admin/orders/[id]/update-status<br>2. Chọn trạng thái mới<br>3. Nhập lý do<br>4. Bỏ tích checkbox thông báo<br>5. Click "Cập nhật trạng thái" | Cập nhật thành công, không gửi thông báo cho khách hàng | | Untested | 11/15/2015 | |
| **FUNC-CNDH-08** | Click nút Hủy | 1. Truy cập /admin/orders/[id]/update-status<br>2. Click nút "Hủy" | Chuyển về trang chi tiết đơn hàng, không lưu thay đổi | | Pass | 11/15/2015 | |
| **FUNC-CNDH-09** | Click nút Quay lại | 1. Truy cập /admin/orders/[id]/update-status<br>2. Click nút "Quay lại" | Chuyển về trang chi tiết đơn hàng | | Pass | 11/15/2015 | |
| **FUNC-CNDH-10** | Lọc trạng thái không hiển thị trạng thái hiện tại | 1. Truy cập /admin/orders/[id]/update-status<br>2. Kiểm tra dropdown trạng thái | Dropdown chỉ hiển thị các trạng thái khác trạng thái hiện tại | | Pass | 11/15/2015 | |
| **FUNC-CNDH-11** | Ghi nhận lịch sử thay đổi | 1. Truy cập /admin/orders/[id]/update-status<br>2. Cập nhật trạng thái thành công<br>3. Xem trang chi tiết đơn hàng | Lịch sử cập nhật ghi nhận thay đổi trạng thái với thời gian, lý do, người thực hiện | | Untested | 11/15/2015 | |

---

### Function: Xóa đơn hàng

#### Check GUI: Xóa đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XDH-01** | Kiểm tra nút Hủy đơn hàng trong danh sách | 1. Truy cập /admin/orders<br>2. Kiểm tra nút Hủy | Các đơn hàng chưa giao và chưa hủy có nút với icon AlertTriangle | | Pass | 11/15/2015 | |
| **GUI-XDH-02** | Kiểm tra modal xác nhận hủy đơn hàng | 1. Truy cập /admin/orders<br>2. Click nút Hủy đơn hàng<br>3. Kiểm tra modal | Hiển thị modal với tiêu đề xác nhận, mô tả, trường nhập lý do hủy, 2 nút (Hủy, Xác nhận hủy) | | Pass | 11/15/2015 | |

---

### Check FUNC: Xóa đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XDH-01** | Hủy đơn hàng từ danh sách | 1. Truy cập /admin/orders<br>2. Click nút Hủy trên một đơn hàng<br>3. Nhập lý do hủy<br>4. Click "Xác nhận hủy" | Hiển thị thông báo "Hủy đơn hàng thành công", đơn hàng biến mất khỏi danh sách hoặc chuyển sang trạng thái "Đã hủy" | | Untested | 11/15/2015 | |
| **FUNC-XDH-02** | Hủy đơn hàng từ chi tiết | 1. Truy cập /admin/orders/[id]<br>2. Click "Hủy đơn hàng"<br>3. Nhập lý do<br>4. Click "Xác nhận hủy" | Hiển thị thông báo "Hủy đơn hàng thành công", chuyển về trang danh sách, đơn hàng chuyển sang trạng thái "Đã hủy" | | Untested | 11/15/2015 | |
| **FUNC-XDH-03** | Hủy đơn hàng - Thiếu lý do | 1. Truy cập /admin/orders<br>2. Click nút Hủy<br>3. Để trống lý do<br>4. Click "Xác nhận hủy" | Hiển thị thông báo lỗi "Vui lòng nhập lý do hủy đơn hàng" | | Pass | 11/15/2015 | |
| **FUNC-XDH-04** | Hủy dialog hủy đơn hàng | 1. Truy cập /admin/orders<br>2. Click nút Hủy<br>3. Click nút "Hủy" trong modal | Modal đóng, không hủy đơn hàng | | Pass | 11/15/2015 | |
| **FUNC-XDH-05** | Không hiển thị nút Hủy cho đơn đã giao | 1. Truy cập /admin/orders<br>2. Tìm đơn hàng đã giao<br>3. Kiểm tra nút Hủy | Đơn hàng đã giao không có nút Hủy | | Pass | 11/15/2015 | |
| **FUNC-XDH-06** | Không hiển thị nút Hủy cho đơn đã hủy | 1. Truy cập /admin/orders<br>2. Tìm đơn hàng đã hủy<br>3. Kiểm tra nút Hủy | Đơn hàng đã hủy không có nút Hủy | | Pass | 11/15/2015 | |

---

### Function: Xác nhận đơn hàng

#### Check GUI: Xác nhận đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XNDH-01** | Kiểm tra nút Xác nhận đơn hàng | 1. Truy cập /admin/orders/[id]<br>2. Kiểm tra nút Xác nhận | Nếu đơn hàng ở trạng thái pending, hiển thị nút "Xác nhận đơn hàng" với icon CheckCircle | | Pass | 11/15/2015 | |

---

### Check FUNC: Xác nhận đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XNDH-01** | Xác nhận đơn hàng thành công | 1. Truy cập /admin/orders/[id]<br>2. Đơn hàng ở trạng thái pending<br>3. Click "Xác nhận đơn hàng" | Hiển thị thông báo "Xác nhận đơn hàng thành công", trạng thái đơn hàng chuyển sang "Đã xác nhận", nút Xác nhận biến mất | | Untested | 11/15/2015 | |
| **FUNC-XNDH-02** | Không hiển thị nút Xác nhận cho đơn đã xác nhận | 1. Truy cập /admin/orders/[id]<br>2. Đơn hàng đã xác nhận<br>3. Kiểm tra nút Xác nhận | Không hiển thị nút "Xác nhận đơn hàng" | | Pass | 11/15/2015 | |
| **FUNC-XNDH-03** | Ghi nhận lịch sử xác nhận | 1. Truy cập /admin/orders/[id]<br>2. Xác nhận đơn hàng thành công<br>3. Kiểm tra lịch sử | Lịch sử cập nhật ghi nhận "Đơn hàng được xác nhận" với thời gian và người thực hiện | | Untested | 11/15/2015 | |

---

### Function: In đơn hàng

#### Check GUI: In đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-IDH-01** | Kiểm tra nút In đơn hàng trong danh sách | 1. Truy cập /admin/orders<br>2. Kiểm tra nút In | Mỗi hàng có nút với icon Printer | | Pass | 11/15/2015 | |
| **GUI-IDH-02** | Kiểm tra nút In đơn hàng trong chi tiết | 1. Truy cập /admin/orders/[id]<br>2. Kiểm tra nút In | Hiển thị nút "In đơn hàng" với icon Printer | | Pass | 11/15/2015 | |
| **GUI-IDH-03** | Kiểm tra modal in đơn hàng | 1. Truy cập /admin/orders<br>2. Click nút In<br>3. Kiểm tra modal | Hiển thị modal với thông tin đơn hàng để in | | Pass | 11/15/2015 | |

---

### Check FUNC: In đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-IDH-01** | In đơn hàng từ danh sách | 1. Truy cập /admin/orders<br>2. Click nút Printer trên một đơn hàng | Mở modal in đơn hàng với đầy đủ thông tin, có thể in hoặc tải PDF | | Untested | 11/15/2015 | |
| **FUNC-IDH-02** | In đơn hàng từ chi tiết | 1. Truy cập /admin/orders/[id]<br>2. Click "In đơn hàng" | Hiển thị thông báo "Đã gửi lệnh in", mở cửa sổ in hoặc tải file PDF | | Untested | 11/15/2015 | |
| **FUNC-IDH-03** | Đóng modal in đơn hàng | 1. Truy cập /admin/orders<br>2. Click nút In<br>3. Click nút đóng modal | Modal đóng, không in đơn hàng | | Pass | 11/15/2015 | |

---

### Function: Tạo đơn hàng mới

#### Check GUI: Tạo đơn hàng mới

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-TDHM-01** | Kiểm tra nút Quay lại | 1. Truy cập /admin/orders/new<br>2. Kiểm tra nút Quay lại | Hiển thị nút "Quay lại" với icon ArrowLeft | | Pass | 11/15/2015 | |
| **GUI-TDHM-02** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/orders/new<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Đơn hàng mới" và mô tả "Xử lý các đơn hàng mới cần được xác nhận" | | Pass | 11/15/2015 | |
| **GUI-TDHM-03** | Kiểm tra thẻ thống kê | 1. Truy cập /admin/orders/new<br>2. Kiểm tra các thẻ | Hiển thị 4 thẻ: Tổng đơn hàng mới, Ưu tiên cao, Ưu tiên trung bình, Ưu tiên thấp, mỗi thẻ có icon và số lượng | | Pass | 11/15/2015 | |
| **GUI-TDHM-04** | Kiểm tra bộ lọc ưu tiên | 1. Truy cập /admin/orders/new<br>2. Kiểm tra dropdown ưu tiên | Hiển thị Select với các tùy chọn: Tất cả, Cao, Trung bình, Thấp | | Pass | 11/15/2015 | |
| **GUI-TDHM-05** | Kiểm tra bộ lọc thời gian | 1. Truy cập /admin/orders/new<br>2. Kiểm tra dropdown thời gian | Hiển thị Select với các tùy chọn: Hôm nay, 3 ngày qua, 1 tuần qua, 1 tháng qua | | Pass | 11/15/2015 | |
| **GUI-TDHM-06** | Kiểm tra nút Sắp xếp theo ưu tiên | 1. Truy cập /admin/orders/new<br>2. Kiểm tra nút Sắp xếp | Hiển thị nút "Sắp xếp theo ưu tiên" với icon Package | | Pass | 11/15/2015 | |
| **GUI-TDHM-07** | Kiểm tra nút Xác nhận hàng loạt | 1. Truy cập /admin/orders/new<br>2. Kiểm tra nút Xác nhận | Hiển thị nút "Xác nhận hàng loạt" với icon CheckCircle và số lượng đơn đã chọn | | Pass | 11/15/2015 | |
| **GUI-TDHM-08** | Kiểm tra checkbox chọn đơn hàng | 1. Truy cập /admin/orders/new<br>2. Kiểm tra checkbox | Mỗi hàng có checkbox để chọn đơn hàng, header có checkbox để chọn tất cả | | Pass | 11/15/2015 | |
| **GUI-TDHM-09** | Kiểm tra bảng đơn hàng mới | 1. Truy cập /admin/orders/new<br>2. Kiểm tra bảng | Hiển thị bảng với các cột: Checkbox, Mã đơn hàng, Khách hàng, Tổng tiền, Thời gian tạo, Ưu tiên, Thời gian chờ, Thao tác | | Pass | 11/15/2015 | |
| **GUI-TDHM-10** | Kiểm tra badge ưu tiên | 1. Truy cập /admin/orders/new<br>2. Kiểm tra badge ưu tiên | Mỗi đơn hàng hiển thị badge ưu tiên với icon và text (Cao, Trung bình, Thấp) | | Pass | 11/15/2015 | |
| **GUI-TDHM-11** | Kiểm tra nút Xem chi tiết | 1. Truy cập /admin/orders/new<br>2. Kiểm tra nút Xem | Mỗi hàng có nút với icon Eye để xem chi tiết | | Pass | 11/15/2015 | |
| **GUI-TDHM-12** | Kiểm tra nút Đánh dấu đã xem | 1. Truy cập /admin/orders/new<br>2. Kiểm tra nút Đánh dấu | Mỗi hàng có nút với icon CheckCircle để đánh dấu đã xem | | Pass | 11/15/2015 | |

---

### Check FUNC: Tạo đơn hàng mới

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TDHM-01** | Mở trang đơn hàng mới | 1. Truy cập /admin/orders/new | Hiển thị trang với tiêu đề, thẻ thống kê, bộ lọc, bảng danh sách đơn hàng mới | | Pass | 11/15/2015 | |
| **FUNC-TDHM-02** | Lọc đơn hàng theo ưu tiên | 1. Truy cập /admin/orders/new<br>2. Chọn mức ưu tiên từ dropdown<br>3. Kiểm tra bảng | Bảng chỉ hiển thị các đơn hàng có mức ưu tiên đã chọn | | Pass | 11/15/2015 | |
| **FUNC-TDHM-03** | Lọc đơn hàng theo thời gian | 1. Truy cập /admin/orders/new<br>2. Chọn khoảng thời gian từ dropdown<br>3. Kiểm tra bảng | Bảng chỉ hiển thị các đơn hàng trong khoảng thời gian đã chọn | | Pass | 11/15/2015 | |
| **FUNC-TDHM-04** | Chọn một đơn hàng | 1. Truy cập /admin/orders/new<br>2. Tích checkbox một đơn hàng | Checkbox được tích, nút Xác nhận hàng loạt hiển thị số lượng (1) | | Pass | 11/15/2015 | |
| **FUNC-TDHM-05** | Chọn tất cả đơn hàng | 1. Truy cập /admin/orders/new<br>2. Tích checkbox ở header | Tất cả checkbox được tích, nút Xác nhận hàng loạt hiển thị số lượng tất cả | | Pass | 11/15/2015 | |
| **FUNC-TDHM-06** | Bỏ chọn tất cả đơn hàng | 1. Truy cập /admin/orders/new<br>2. Đã chọn tất cả<br>3. Bỏ tích checkbox ở header | Tất cả checkbox bị bỏ tích, nút Xác nhận hàng loạt bị disable | | Pass | 11/15/2015 | |
| **FUNC-TDHM-07** | Xác nhận hàng loạt - Chưa chọn đơn | 1. Truy cập /admin/orders/new<br>2. Không chọn đơn hàng nào<br>3. Click "Xác nhận hàng loạt" | Hiển thị thông báo lỗi "Vui lòng chọn ít nhất một đơn hàng", nút bị disable | | Pass | 11/15/2015 | |
| **FUNC-TDHM-08** | Xác nhận hàng loạt thành công | 1. Truy cập /admin/orders/new<br>2. Chọn một hoặc nhiều đơn hàng<br>3. Click "Xác nhận hàng loạt" | Hiển thị thông báo "Xác nhận hàng loạt thành công cho X đơn hàng", các đơn hàng đã chọn biến mất khỏi danh sách | | Untested | 11/15/2015 | |
| **FUNC-TDHM-09** | Đánh dấu đơn hàng đã xem | 1. Truy cập /admin/orders/new<br>2. Click nút CheckCircle trên một đơn hàng | Hiển thị thông báo "Đã đánh dấu đơn hàng đã xem", đơn hàng có thể thay đổi trạng thái hiển thị | | Untested | 11/15/2015 | |
| **FUNC-TDHM-10** | Sắp xếp theo ưu tiên | 1. Truy cập /admin/orders/new<br>2. Click "Sắp xếp theo ưu tiên" | Hiển thị thông báo "Đã sắp xếp theo mức độ ưu tiên", bảng sắp xếp đơn hàng theo thứ tự ưu tiên (Cao -> Trung bình -> Thấp) | | Untested | 11/15/2015 | |
| **FUNC-TDHM-11** | Click nút Xem chi tiết | 1. Truy cập /admin/orders/new<br>2. Click nút Eye trên một đơn hàng | Chuyển đến trang chi tiết đơn hàng /admin/orders/[id] | | Pass | 11/15/2015 | |
| **FUNC-TDHM-12** | Click nút Quay lại | 1. Truy cập /admin/orders/new<br>2. Click nút "Quay lại" | Chuyển về trang /admin/orders | | Pass | 11/15/2015 | |
| **FUNC-TDHM-13** | Hiển thị thời gian chờ | 1. Truy cập /admin/orders/new<br>2. Kiểm tra cột Thời gian chờ | Mỗi đơn hàng hiển thị thời gian chờ từ lúc tạo đến hiện tại (VD: "2 giờ 15 phút") | | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn Markdown để dễ dàng quản lý và cập nhật test cases.*

