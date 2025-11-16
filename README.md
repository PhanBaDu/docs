# Test Case Template - Quản lý người dùng (Admin)

## Module Code
**Model Management Store: Quản lý người dùng Admin**

## Test Requirement
1. Tạo người dùng
2. Hiển thị danh sách người dùng
3. Xem chi tiết người dùng
4. Xóa người dùng
5. Cập nhật người dùng

---

## Test Summary

### Người thực hiện Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 51 |
| **Fail** | 0 |
| **Untested** | 53 |
| **N/A** | 0 |
| **Number of Test cases** | 104 |

---

## Test Cases

### Function: Hiển thị danh sách người dùng

#### Check GUI: Hiển thị danh sách người dùng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DSND-01** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/customers<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Quản lý khách hàng" với kích thước text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-DSND-02** | Kiểm tra mô tả chức năng | 1. Truy cập /admin/customers<br>2. Kiểm tra mô tả | Hiển thị mô tả "Hiển thị tất cả khách hàng đã đăng ký trong hệ thống" màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-DSND-03** | Kiểm tra Stats Cards | 1. Truy cập /admin/customers<br>2. Kiểm tra Stats Cards | Hiển thị 4 card thống kê: Tổng khách hàng, Hoạt động, Tạm khóa, Chưa xác thực | | Pass | 11/15/2015 | |
| **GUI-DSND-04** | Kiểm tra trường Tìm kiếm | 1. Truy cập /admin/customers<br>2. Kiểm tra trường tìm kiếm | Hiển thị input với icon Search bên trái, placeholder "Tìm kiếm khách hàng theo tên, email, số điện thoại...", có thể nhập và nhấn Enter để tìm | | Pass | 11/15/2015 | |
| **GUI-DSND-05** | Kiểm tra Select Trạng thái | 1. Truy cập /admin/customers<br>2. Kiểm tra Select Trạng thái | Hiển thị Select với placeholder "Trạng thái", width w-40, có các option: Tất cả, Hoạt động, Tạm khóa, Chưa xác thực | | Pass | 11/15/2015 | |
| **GUI-DSND-06** | Kiểm tra Select Loại khách hàng | 1. Truy cập /admin/customers<br>2. Kiểm tra Select | Hiển thị Select với placeholder "Loại khách hàng", width w-40, có các option: Tất cả, VIP, Thường, Mới | | Pass | 11/15/2015 | |
| **GUI-DSND-07** | Kiểm tra Date Range | 1. Truy cập /admin/customers<br>2. Kiểm tra Date Range | Hiển thị 2 input date với text "đến" ở giữa, width w-40 mỗi input | | Pass | 11/15/2015 | |
| **GUI-DSND-08** | Kiểm tra nút Bộ lọc | 1. Truy cập /admin/customers<br>2. Kiểm tra nút | Hiển thị nút "Bộ lọc" với icon Filter variant outline | | Pass | 11/15/2015 | |
| **GUI-DSND-09** | Kiểm tra bảng danh sách người dùng | 1. Truy cập /admin/customers<br>2. Kiểm tra bảng | Hiển thị Table với các cột: Avatar, Tên, Email, SĐT, Trạng thái, Ngày đăng ký, Tổng đơn hàng, Phân loại, Thao tác | | Pass | 11/15/2015 | |
| **GUI-DSND-10** | Kiểm tra cột Avatar trong bảng | 1. Truy cập /admin/customers<br>2. Kiểm tra cột Avatar | Mỗi dòng hiển thị avatar (w-10 h-10 rounded-full) hoặc AvatarFallback | | Pass | 11/15/2015 | |
| **GUI-DSND-11** | Kiểm tra cột Tên trong bảng | 1. Truy cập /admin/customers<br>2. Kiểm tra cột Tên | Hiển thị tên khách hàng (font-medium) và ID (text-sm muted-foreground) | | Pass | 11/15/2015 | |
| **GUI-DSND-12** | Kiểm tra cột Email trong bảng | 1. Truy cập /admin/customers<br>2. Kiểm tra cột Email | Hiển thị email (text-sm) | | Pass | 11/15/2015 | |
| **GUI-DSND-13** | Kiểm tra cột SĐT trong bảng | 1. Truy cập /admin/customers<br>2. Kiểm tra cột SĐT | Hiển thị số điện thoại (text-sm) | | Pass | 11/15/2015 | |
| **GUI-DSND-14** | Kiểm tra cột Trạng thái trong bảng | 1. Truy cập /admin/customers<br>2. Kiểm tra cột Trạng thái | Hiển thị Badge với icon và màu tương ứng: Hoạt động (User icon màu xanh, default), Tạm khóa (Lock icon màu đỏ, destructive), Chưa xác thực (AlertCircle icon màu vàng, secondary) | | Pass | 11/15/2015 | |
| **GUI-DSND-15** | Kiểm tra cột Ngày đăng ký trong bảng | 1. Truy cập /admin/customers<br>2. Kiểm tra cột Ngày đăng ký | Hiển thị icon Calendar và ngày đăng ký (text-sm) | | Pass | 11/15/2015 | |
| **GUI-DSND-16** | Kiểm tra cột Tổng đơn hàng trong bảng | 1. Truy cập /admin/customers<br>2. Kiểm tra cột Tổng đơn hàng | Hiển thị số lượng đơn hàng (font-medium) và tổng tiền đã mua (text-sm muted-foreground) định dạng vi-VN | | Pass | 11/15/2015 | |
| **GUI-DSND-17** | Kiểm tra cột Phân loại trong bảng | 1. Truy cập /admin/customers<br>2. Kiểm tra cột Phân loại | Hiển thị Badge với icon và màu tương ứng: VIP (Crown icon màu vàng, default), Thường (User icon màu xanh, outline), Mới (Star icon màu xanh lá, secondary) | | Pass | 11/15/2015 | |
| **GUI-DSND-18** | Kiểm tra cột Thao tác trong bảng | 1. Truy cập /admin/customers<br>2. Kiểm tra cột Thao tác | Hiển thị 4 nút: Xem (icon Eye link đến /admin/customers/[id]), Chỉnh sửa (icon Edit), Khóa/Mở khóa (icon Lock/Unlock), Gửi email (icon Mail), tất cả variant ghost size sm | | Pass | 11/15/2015 | |
| **GUI-DSND-19** | Kiểm tra Pagination | 1. Truy cập /admin/customers<br>2. Kiểm tra Pagination | Hiển thị text "Hiển thị 1-X trong Y khách hàng", các nút phân trang: Trước (disabled), số trang, Sau | | Pass | 11/15/2015 | |

---

### Check FUNC: Hiển thị danh sách người dùng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DSND-01** | Mở trang danh sách người dùng | 1. Truy cập /admin/customers | Hiển thị trang với tiêu đề, mô tả, 4 Stats Cards, bộ lọc (tìm kiếm, trạng thái, loại khách hàng, date range, nút Bộ lọc), bảng danh sách người dùng, pagination | | Pass | 11/15/2015 | |
| **FUNC-DSND-02** | Hiển thị danh sách người dùng mặc định | 1. Truy cập /admin/customers | Hiển thị tất cả người dùng trong bảng, mỗi người dùng có đầy đủ thông tin: avatar, tên, email, SĐT, trạng thái, ngày đăng ký, tổng đơn hàng, phân loại, các nút thao tác | | Pass | 11/15/2015 | |
| **FUNC-DSND-03** | Click nút Xem (icon Eye) | 1. Truy cập /admin/customers<br>2. Click nút Xem của một người dùng | Chuyển đến trang chi tiết người dùng /admin/customers/[id] | | Pass | 11/15/2015 | |
| **FUNC-DSND-04** | Click nút Chỉnh sửa (icon Edit) | 1. Truy cập /admin/customers<br>2. Click nút Chỉnh sửa của một người dùng | Mở modal chỉnh sửa thông tin người dùng | | Pass | 11/15/2015 | |
| **FUNC-DSND-05** | Click nút Khóa (icon Lock) | 1. Truy cập /admin/customers<br>2. Click nút Khóa của một người dùng đang hoạt động | Hiển thị thông báo "Đã khóa tài khoản [tên]", trạng thái người dùng chuyển thành "Tạm khóa", nút chuyển thành Unlock | | Untested | 11/15/2015 | |
| **FUNC-DSND-06** | Click nút Mở khóa (icon Unlock) | 1. Truy cập /admin/customers<br>2. Click nút Mở khóa của một người dùng đang bị khóa | Hiển thị thông báo "Đã mở khóa tài khoản [tên]", trạng thái người dùng chuyển thành "Hoạt động", nút chuyển thành Lock | | Untested | 11/15/2015 | |
| **FUNC-DSND-07** | Click nút Gửi email (icon Mail) | 1. Truy cập /admin/customers<br>2. Click nút Gửi email của một người dùng | Hiển thị thông báo "Đã gửi email cho [tên]" hoặc mở modal gửi email | | Untested | 11/15/2015 | |
| **FUNC-DSND-08** | Lọc theo Trạng thái | 1. Truy cập /admin/customers<br>2. Chọn trạng thái (VD: Hoạt động)<br>3. Click "Bộ lọc" | Hiển thị danh sách người dùng có trạng thái đã chọn, Stats Cards được cập nhật | | Untested | 11/15/2015 | |
| **FUNC-DSND-09** | Lọc theo Loại khách hàng | 1. Truy cập /admin/customers<br>2. Chọn loại khách hàng (VD: VIP)<br>3. Click "Bộ lọc" | Hiển thị danh sách người dùng có loại khách hàng đã chọn | | Untested | 11/15/2015 | |
| **FUNC-DSND-10** | Lọc theo Date Range | 1. Truy cập /admin/customers<br>2. Chọn khoảng ngày đăng ký<br>3. Click "Bộ lọc" | Hiển thị danh sách người dùng đăng ký trong khoảng ngày đã chọn | | Untested | 11/15/2015 | |
| **FUNC-DSND-11** | Tìm kiếm người dùng | 1. Truy cập /admin/customers<br>2. Nhập từ khóa tìm kiếm (tên, email hoặc số điện thoại)<br>3. Nhấn Enter hoặc click "Bộ lọc" | Hiển thị danh sách người dùng phù hợp với từ khóa tìm kiếm | | Untested | 11/15/2015 | |
| **FUNC-DSND-12** | Xử lý khi không có người dùng | 1. Truy cập /admin/customers<br>2. Lọc để không có người dùng nào | Hiển thị thông báo "Không tìm thấy khách hàng nào" hoặc bảng trống | | Untested | 11/15/2015 | |
| **FUNC-DSND-13** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/customers<br>2. Tắt kết nối mạng | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại" | | Untested | 11/15/2015 | |
| **FUNC-DSND-14** | Xử lý khi server lỗi | 1. Truy cập /admin/customers<br>2. Server trả về lỗi 500 | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau" | | Untested | 11/15/2015 | |

---

### Function: Xem chi tiết người dùng

#### Check GUI: Xem chi tiết người dùng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CTND-01** | Kiểm tra nút Quay lại | 1. Truy cập /admin/customers/[id]<br>2. Kiểm tra nút Quay lại | Hiển thị nút "Quay lại" với icon ArrowLeft variant outline size sm, link đến /admin/customers | | Pass | 11/15/2015 | |
| **GUI-CTND-02** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/customers/[id]<br>2. Kiểm tra tiêu đề | Hiển thị tên khách hàng với kích thước text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-CTND-03** | Kiểm tra mô tả trang | 1. Truy cập /admin/customers/[id]<br>2. Kiểm tra mô tả | Hiển thị "Chi tiết khách hàng - ID: [id]" màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-CTND-04** | Kiểm tra nút Chỉnh sửa | 1. Truy cập /admin/customers/[id]<br>2. Kiểm tra nút Chỉnh sửa | Hiển thị nút "Chỉnh sửa" với icon Edit variant outline | | Pass | 11/15/2015 | |
| **GUI-CTND-05** | Kiểm tra nút Khóa/Mở khóa | 1. Truy cập /admin/customers/[id]<br>2. Kiểm tra nút | Hiển thị nút "Khóa tài khoản" (icon Lock) hoặc "Mở khóa" (icon Unlock) tùy theo trạng thái | | Pass | 11/15/2015 | |
| **GUI-CTND-06** | Kiểm tra nút Gửi thông báo | 1. Truy cập /admin/customers/[id]<br>2. Kiểm tra nút | Hiển thị nút "Gửi thông báo" với icon Bell variant secondary | | Pass | 11/15/2015 | |
| **GUI-CTND-07** | Kiểm tra nút Xuất báo cáo | 1. Truy cập /admin/customers/[id]<br>2. Kiểm tra nút | Hiển thị nút "Xuất báo cáo" với icon Download variant outline | | Pass | 11/15/2015 | |
| **GUI-CTND-08** | Kiểm tra card Thông tin cá nhân | 1. Truy cập /admin/customers/[id]<br>2. Kiểm tra card | Hiển thị card "Thông tin cá nhân" với: Avatar (w-20 h-20), Tên khách hàng (text-2xl font-bold), Email (icon Mail), Số điện thoại (icon Phone), Ngày sinh (icon Calendar), Giới tính, Địa chỉ (icon MapPin) | | Pass | 11/15/2015 | |
| **GUI-CTND-09** | Kiểm tra card Thông tin tài khoản | 1. Truy cập /admin/customers/[id]<br>2. Kiểm tra card | Hiển thị card "Thông tin tài khoản" với: Trạng thái (Badge), Ngày đăng ký (icon Calendar), Lần đăng nhập cuối (icon Clock), Phân loại (Badge với icon Crown/Star/User) | | Pass | 11/15/2015 | |
| **GUI-CTND-10** | Kiểm tra card Thống kê mua hàng | 1. Truy cập /admin/customers/[id]<br>2. Kiểm tra card | Hiển thị card "Thống kê mua hàng" với: Tổng đơn hàng (icon Package), Tổng tiền đã mua (icon DollarSign), Đơn hàng trung bình (icon BarChart3), Sản phẩm yêu thích (icon Heart) | | Pass | 11/15/2015 | |
| **GUI-CTND-11** | Kiểm tra card Lịch sử đơn hàng | 1. Truy cập /admin/customers/[id]<br>2. Kiểm tra card | Hiển thị card "Lịch sử đơn hàng" với Table hiển thị các cột: Mã đơn hàng, Ngày mua, Sản phẩm, Số lượng, Tổng tiền, Trạng thái | | Pass | 11/15/2015 | |
| **GUI-CTND-12** | Kiểm tra card Địa chỉ giao hàng | 1. Truy cập /admin/customers/[id]<br>2. Kiểm tra card | Hiển thị card "Địa chỉ giao hàng" với danh sách các địa chỉ: Tên địa chỉ, Địa chỉ, Số điện thoại, Badge "Mặc định" nếu là địa chỉ mặc định | | Pass | 11/15/2015 | |
| **GUI-CTND-13** | Kiểm tra card Ghi chú khách hàng | 1. Truy cập /admin/customers/[id]<br>2. Kiểm tra card | Hiển thị card "Ghi chú khách hàng" với Textarea hiển thị ghi chú hiện tại, nút "Thêm ghi chú" hoặc "Cập nhật ghi chú" | | Pass | 11/15/2015 | |
| **GUI-CTND-14** | Kiểm tra card Lịch sử hoạt động | 1. Truy cập /admin/customers/[id]<br>2. Kiểm tra card | Hiển thị card "Lịch sử hoạt động" với Timeline hiển thị các mốc: Thời gian, Loại hoạt động (icon tương ứng), Mô tả | | Pass | 11/15/2015 | |

---

### Check FUNC: Xem chi tiết người dùng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CTND-01** | Mở trang chi tiết người dùng | 1. Truy cập /admin/customers/[id] | Hiển thị trang với nút Quay lại, tiêu đề (tên khách hàng), mô tả, các nút thao tác, card Thông tin cá nhân, card Thông tin tài khoản, card Thống kê mua hàng, card Lịch sử đơn hàng, card Địa chỉ giao hàng, card Ghi chú khách hàng, card Lịch sử hoạt động | | Pass | 11/15/2015 | |
| **FUNC-CTND-02** | Hiển thị đầy đủ thông tin người dùng | 1. Truy cập /admin/customers/[id] | Hiển thị đầy đủ thông tin: avatar, tên, email, SĐT, ngày sinh, giới tính, địa chỉ, trạng thái, ngày đăng ký, lần đăng nhập cuối, phân loại, tổng đơn hàng, tổng tiền đã mua, đơn hàng trung bình, sản phẩm yêu thích, lịch sử đơn hàng, địa chỉ giao hàng, ghi chú, lịch sử hoạt động | | Pass | 11/15/2015 | |
| **FUNC-CTND-03** | Click nút Quay lại | 1. Truy cập /admin/customers/[id]<br>2. Click nút "Quay lại" | Chuyển về trang /admin/customers | | Pass | 11/15/2015 | |
| **FUNC-CTND-04** | Click nút Chỉnh sửa | 1. Truy cập /admin/customers/[id]<br>2. Click nút "Chỉnh sửa" | Mở modal chỉnh sửa thông tin người dùng | | Pass | 11/15/2015 | |
| **FUNC-CTND-05** | Khóa tài khoản thành công | 1. Truy cập /admin/customers/[id]<br>2. Click nút "Khóa tài khoản" | Hiển thị thông báo "Đã khóa tài khoản", trạng thái người dùng chuyển thành "Tạm khóa", nút chuyển thành "Mở khóa" | | Untested | 11/15/2015 | |
| **FUNC-CTND-06** | Mở khóa tài khoản thành công | 1. Truy cập /admin/customers/[id]<br>2. Click nút "Mở khóa" | Hiển thị thông báo "Đã mở khóa tài khoản", trạng thái người dùng chuyển thành "Hoạt động", nút chuyển thành "Khóa tài khoản" | | Untested | 11/15/2015 | |
| **FUNC-CTND-07** | Gửi thông báo thành công | 1. Truy cập /admin/customers/[id]<br>2. Click nút "Gửi thông báo" | Mở modal gửi thông báo hoặc hiển thị thông báo "Gửi thông báo thành công" | | Untested | 11/15/2015 | |
| **FUNC-CTND-08** | Xuất báo cáo thành công | 1. Truy cập /admin/customers/[id]<br>2. Click nút "Xuất báo cáo" | Tải về file PDF báo cáo chi tiết khách hàng với đầy đủ thông tin | | Untested | 11/15/2015 | |
| **FUNC-CTND-09** | Thêm ghi chú thành công | 1. Truy cập /admin/customers/[id]<br>2. Nhập ghi chú vào Textarea<br>3. Click "Thêm ghi chú" hoặc "Cập nhật ghi chú" | Hiển thị thông báo "Thêm ghi chú thành công" hoặc "Cập nhật ghi chú thành công", ghi chú được lưu và hiển thị | | Untested | 11/15/2015 | |
| **FUNC-CTND-10** | Xử lý khi người dùng không tồn tại | 1. Truy cập /admin/customers/[id không tồn tại] | Hiển thị thông báo lỗi "Khách hàng không tồn tại" hoặc chuyển về trang danh sách | | Untested | 11/15/2015 | |
| **FUNC-CTND-11** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/customers/[id]<br>2. Tắt kết nối mạng | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại" | | Untested | 11/15/2015 | |
| **FUNC-CTND-12** | Xử lý khi server lỗi | 1. Truy cập /admin/customers/[id]<br>2. Server trả về lỗi 500 | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau" | | Untested | 11/15/2015 | |

---

### Function: Cập nhật người dùng

#### Check GUI: Cập nhật người dùng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CNND-01** | Kiểm tra modal Chỉnh sửa | 1. Truy cập /admin/customers<br>2. Click nút Chỉnh sửa của một người dùng<br>3. Kiểm tra modal | Hiển thị Dialog với tiêu đề "Chỉnh sửa thông tin khách hàng", mô tả "Cập nhật thông tin cho khách hàng [tên]" | | Pass | 11/15/2015 | |
| **GUI-CNND-02** | Kiểm tra trường Tên khách hàng | 1. Truy cập /admin/customers<br>2. Click nút Chỉnh sửa<br>3. Kiểm tra trường | Hiển thị label "Tên khách hàng", input type text với giá trị mặc định là tên hiện tại | | Pass | 11/15/2015 | |
| **GUI-CNND-03** | Kiểm tra trường Email | 1. Truy cập /admin/customers<br>2. Click nút Chỉnh sửa<br>3. Kiểm tra trường | Hiển thị label "Email", input type email với giá trị mặc định là email hiện tại | | Pass | 11/15/2015 | |
| **GUI-CNND-04** | Kiểm tra trường Số điện thoại | 1. Truy cập /admin/customers<br>2. Click nút Chỉnh sửa<br>3. Kiểm tra trường | Hiển thị label "Số điện thoại", input type text với giá trị mặc định là số điện thoại hiện tại | | Pass | 11/15/2015 | |
| **GUI-CNND-05** | Kiểm tra nút Hủy | 1. Truy cập /admin/customers<br>2. Click nút Chỉnh sửa<br>3. Kiểm tra nút | Hiển thị nút "Hủy" variant outline | | Pass | 11/15/2015 | |
| **GUI-CNND-06** | Kiểm tra nút Lưu thay đổi | 1. Truy cập /admin/customers<br>2. Click nút Chỉnh sửa<br>3. Kiểm tra nút | Hiển thị nút "Lưu thay đổi" type submit | | Pass | 11/15/2015 | |

---

### Check FUNC: Cập nhật người dùng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CNND-01** | Mở modal chỉnh sửa | 1. Truy cập /admin/customers<br>2. Click nút "Chỉnh sửa" của một người dùng | Hiển thị Dialog với tiêu đề "Chỉnh sửa thông tin khách hàng", mô tả, các trường: Tên khách hàng, Email, Số điện thoại (đã được điền sẵn giá trị hiện tại), nút Hủy, nút Lưu thay đổi | | Pass | 11/15/2015 | |
| **FUNC-CNND-02** | Cập nhật người dùng thành công | 1. Truy cập /admin/customers<br>2. Click nút "Chỉnh sửa"<br>3. Sửa thông tin (Tên, Email, SĐT)<br>4. Click "Lưu thay đổi" | Hiển thị thông báo "Cập nhật thông tin khách hàng thành công", modal đóng, thông tin người dùng được cập nhật trong bảng và trang chi tiết | | Untested | 11/15/2015 | |
| **FUNC-CNND-03** | Cập nhật - Thiếu Tên khách hàng | 1. Truy cập /admin/customers<br>2. Click nút "Chỉnh sửa"<br>3. Xóa tên khách hàng<br>4. Click "Lưu thay đổi" | Hiển thị thông báo lỗi "Tên khách hàng không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-CNND-04** | Cập nhật - Thiếu Email | 1. Truy cập /admin/customers<br>2. Click nút "Chỉnh sửa"<br>3. Xóa email<br>4. Click "Lưu thay đổi" | Hiển thị thông báo lỗi "Email không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-CNND-05** | Cập nhật - Email không hợp lệ | 1. Truy cập /admin/customers<br>2. Click nút "Chỉnh sửa"<br>3. Nhập email không đúng định dạng<br>4. Click "Lưu thay đổi" | Trình duyệt hiển thị cảnh báo validation hoặc thông báo lỗi "Email không hợp lệ", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-CNND-06** | Cập nhật - Email đã tồn tại | 1. Truy cập /admin/customers<br>2. Click nút "Chỉnh sửa"<br>3. Nhập email đã tồn tại của người dùng khác<br>4. Click "Lưu thay đổi" | Hiển thị thông báo lỗi "Email đã tồn tại trong hệ thống", form không được gửi | | Untested | 11/15/2015 | |
| **FUNC-CNND-07** | Click nút Hủy | 1. Truy cập /admin/customers<br>2. Click nút "Chỉnh sửa"<br>3. Sửa thông tin<br>4. Click "Hủy" | Modal đóng, thông tin không được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-CNND-08** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/customers<br>2. Click nút "Chỉnh sửa"<br>3. Sửa thông tin<br>4. Tắt kết nối mạng<br>5. Click "Lưu thay đổi" | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", form không được gửi | | Untested | 11/15/2015 | |
| **FUNC-CNND-09** | Xử lý khi server lỗi | 1. Truy cập /admin/customers<br>2. Click nút "Chỉnh sửa"<br>3. Sửa thông tin<br>4. Server trả về lỗi 500<br>5. Click "Lưu thay đổi" | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau", form không được gửi | | Untested | 11/15/2015 | |

---

### Function: Xóa người dùng

#### Check GUI: Xóa người dùng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XND-01** | Kiểm tra Dialog xác nhận xóa | 1. Truy cập /admin/customers<br>2. Click nút Xóa của một người dùng (nếu có)<br>3. Kiểm tra dialog | Hiển thị Dialog với tiêu đề "Xác nhận xóa khách hàng", mô tả "Bạn có chắc chắn muốn xóa khách hàng này? Hành động này không thể hoàn tác", textarea "Lý do xóa", nút "Hủy" variant outline, nút "Xóa vĩnh viễn" variant destructive | | Pass | 11/15/2015 | |

---

### Check FUNC: Xóa người dùng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XND-01** | Xóa người dùng thành công | 1. Truy cập /admin/customers<br>2. Click nút Xóa của một người dùng<br>3. Nhập lý do xóa<br>4. Click "Xóa vĩnh viễn" | Hiển thị thông báo "Đã xóa khách hàng", người dùng bị xóa khỏi danh sách, cập nhật lại bảng | | Untested | 11/15/2015 | |
| **FUNC-XND-02** | Hủy xóa người dùng | 1. Truy cập /admin/customers<br>2. Click nút Xóa<br>3. Click "Hủy" trong dialog | Dialog đóng, người dùng không bị xóa, vẫn ở trang danh sách | | Pass | 11/15/2015 | |
| **FUNC-XND-03** | Xóa người dùng - Người dùng đang có đơn hàng | 1. Truy cập /admin/customers<br>2. Click nút Xóa của người dùng đang có đơn hàng<br>3. Click "Xóa vĩnh viễn" | Hiển thị thông báo lỗi "Không thể xóa khách hàng đang có đơn hàng", người dùng không bị xóa | | Untested | 11/15/2015 | |
| **FUNC-XND-04** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/customers<br>2. Click nút Xóa<br>3. Nhập lý do<br>4. Tắt kết nối mạng<br>5. Click "Xóa vĩnh viễn" | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", người dùng không bị xóa | | Untested | 11/15/2015 | |
| **FUNC-XND-05** | Xử lý khi server lỗi | 1. Truy cập /admin/customers<br>2. Click nút Xóa<br>3. Nhập lý do<br>4. Server trả về lỗi 500<br>5. Click "Xóa vĩnh viễn" | Hiển thị thông báo lỗi "Lỗi xóa khách hàng", người dùng không bị xóa | | Untested | 11/15/2015 | |

---

### Function: Tạo người dùng

#### Check GUI: Tạo người dùng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-TND-01** | Kiểm tra nút Tạo người dùng | 1. Truy cập /admin/customers<br>2. Kiểm tra nút Tạo người dùng | Hiển thị nút "Tạo người dùng" với icon Plus ở header, link đến /admin/customers/new hoặc mở modal | | Pass | 11/15/2015 | |
| **GUI-TND-02** | Kiểm tra modal/trang Tạo người dùng | 1. Truy cập /admin/customers<br>2. Click nút "Tạo người dùng"<br>3. Kiểm tra modal/trang | Hiển thị Dialog hoặc trang với tiêu đề "Tạo người dùng mới", mô tả "Thêm khách hàng mới vào hệ thống" | | Pass | 11/15/2015 | |
| **GUI-TND-03** | Kiểm tra trường Họ và tên | 1. Truy cập /admin/customers<br>2. Click nút "Tạo người dùng"<br>3. Kiểm tra trường | Hiển thị label "Họ và tên *", input type text với placeholder "Nhập họ và tên", có thuộc tính required | | Pass | 11/15/2015 | |
| **GUI-TND-04** | Kiểm tra trường Email | 1. Truy cập /admin/customers<br>2. Click nút "Tạo người dùng"<br>3. Kiểm tra trường | Hiển thị label "Email *", input type email với placeholder "Nhập email", có thuộc tính required | | Pass | 11/15/2015 | |
| **GUI-TND-05** | Kiểm tra trường Số điện thoại | 1. Truy cập /admin/customers<br>2. Click nút "Tạo người dùng"<br>3. Kiểm tra trường | Hiển thị label "Số điện thoại *", input type tel với placeholder "Nhập số điện thoại", có thuộc tính required | | Pass | 11/15/2015 | |
| **GUI-TND-06** | Kiểm tra trường Mật khẩu | 1. Truy cập /admin/customers<br>2. Click nút "Tạo người dùng"<br>3. Kiểm tra trường | Hiển thị label "Mật khẩu *", input type password với placeholder "Nhập mật khẩu", có nút icon Eye/EyeOff để hiển thị/ẩn mật khẩu, có thuộc tính required | | Pass | 11/15/2015 | |
| **GUI-TND-07** | Kiểm tra trường Ngày sinh | 1. Truy cập /admin/customers<br>2. Click nút "Tạo người dùng"<br>3. Kiểm tra trường | Hiển thị label "Ngày sinh", input type date | | Pass | 11/15/2015 | |
| **GUI-TND-08** | Kiểm tra trường Giới tính | 1. Truy cập /admin/customers<br>2. Click nút "Tạo người dùng"<br>3. Kiểm tra trường | Hiển thị label "Giới tính", Select với placeholder "Chọn giới tính", có các option: Nam, Nữ, Khác | | Pass | 11/15/2015 | |
| **GUI-TND-09** | Kiểm tra trường Địa chỉ | 1. Truy cập /admin/customers<br>2. Click nút "Tạo người dùng"<br>3. Kiểm tra trường | Hiển thị label "Địa chỉ", Textarea với placeholder "Nhập địa chỉ" | | Pass | 11/15/2015 | |
| **GUI-TND-10** | Kiểm tra nút Hủy | 1. Truy cập /admin/customers<br>2. Click nút "Tạo người dùng"<br>3. Kiểm tra nút | Hiển thị nút "Hủy" variant outline | | Pass | 11/15/2015 | |
| **GUI-TND-11** | Kiểm tra nút Tạo người dùng | 1. Truy cập /admin/customers<br>2. Click nút "Tạo người dùng"<br>3. Kiểm tra nút | Hiển thị nút "Tạo người dùng" type submit | | Pass | 11/15/2015 | |

---

### Check FUNC: Tạo người dùng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TND-01** | Mở modal/trang tạo người dùng | 1. Truy cập /admin/customers<br>2. Click nút "Tạo người dùng" | Hiển thị Dialog hoặc trang với tiêu đề "Tạo người dùng mới", mô tả, form với các trường: Họ và tên, Email, Số điện thoại, Mật khẩu, Ngày sinh, Giới tính, Địa chỉ, nút Hủy, nút Tạo người dùng | | Pass | 11/15/2015 | |
| **FUNC-TND-02** | Tạo người dùng thành công | 1. Truy cập /admin/customers<br>2. Click nút "Tạo người dùng"<br>3. Điền đầy đủ thông tin bắt buộc (Họ tên, Email, SĐT, Mật khẩu)<br>4. Nhấn "Tạo người dùng" | Hiển thị thông báo "Tạo người dùng thành công", modal/trang đóng, chuyển về trang danh sách, người dùng mới được thêm vào danh sách | | Untested | 11/15/2015 | |
| **FUNC-TND-03** | Tạo người dùng - Thiếu Họ tên | 1. Truy cập /admin/customers<br>2. Click nút "Tạo người dùng"<br>3. Để trống Họ tên<br>4. Điền các trường khác<br>5. Nhấn "Tạo người dùng" | Hiển thị thông báo lỗi "Họ tên không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-TND-04** | Tạo người dùng - Thiếu Email | 1. Truy cập /admin/customers<br>2. Click nút "Tạo người dùng"<br>3. Để trống Email<br>4. Điền các trường khác<br>5. Nhấn "Tạo người dùng" | Hiển thị thông báo lỗi "Email không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-TND-05** | Tạo người dùng - Email không hợp lệ | 1. Truy cập /admin/customers<br>2. Click nút "Tạo người dùng"<br>3. Nhập email không có @<br>4. Điền các trường khác<br>5. Nhấn "Tạo người dùng" | Hiển thị thông báo lỗi "Email không hợp lệ", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-TND-06** | Tạo người dùng - Email đã tồn tại | 1. Truy cập /admin/customers<br>2. Click nút "Tạo người dùng"<br>3. Nhập email đã tồn tại trong hệ thống<br>4. Điền các trường khác<br>5. Nhấn "Tạo người dùng" | Hiển thị thông báo lỗi "Email đã tồn tại trong hệ thống", form không được gửi | | Untested | 11/15/2015 | |
| **FUNC-TND-07** | Tạo người dùng - Thiếu Số điện thoại | 1. Truy cập /admin/customers<br>2. Click nút "Tạo người dùng"<br>3. Để trống Số điện thoại<br>4. Điền các trường khác<br>5. Nhấn "Tạo người dùng" | Hiển thị thông báo lỗi "Số điện thoại không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-TND-08** | Tạo người dùng - Thiếu Mật khẩu | 1. Truy cập /admin/customers<br>2. Click nút "Tạo người dùng"<br>3. Để trống Mật khẩu<br>4. Điền các trường khác<br>5. Nhấn "Tạo người dùng" | Hiển thị thông báo lỗi "Mật khẩu không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-TND-09** | Tạo người dùng - Mật khẩu quá ngắn | 1. Truy cập /admin/customers<br>2. Click nút "Tạo người dùng"<br>3. Nhập mật khẩu < 6 ký tự<br>4. Điền các trường khác<br>5. Nhấn "Tạo người dùng" | Hiển thị thông báo lỗi "Mật khẩu phải có ít nhất 6 ký tự", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-TND-10** | Hiển thị/ẩn mật khẩu | 1. Truy cập /admin/customers<br>2. Click nút "Tạo người dùng"<br>3. Nhập mật khẩu<br>4. Click icon Eye | Input chuyển từ type password sang type text, hiển thị mật khẩu, icon chuyển thành EyeOff | | Pass | 11/15/2015 | |
| **FUNC-TND-11** | Click nút Hủy | 1. Truy cập /admin/customers<br>2. Click nút "Tạo người dùng"<br>3. Click nút "Hủy" | Modal/trang đóng, không tạo người dùng, chuyển về trang danh sách | | Pass | 11/15/2015 | |
| **FUNC-TND-12** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/customers<br>2. Click nút "Tạo người dùng"<br>3. Điền đầy đủ thông tin<br>4. Tắt kết nối mạng<br>5. Nhấn "Tạo người dùng" | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", form không được gửi | | Untested | 11/15/2015 | |
| **FUNC-TND-13** | Xử lý khi server lỗi | 1. Truy cập /admin/customers<br>2. Click nút "Tạo người dùng"<br>3. Điền đầy đủ thông tin<br>4. Server trả về lỗi 500<br>5. Nhấn "Tạo người dùng" | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau", form không được gửi | | Untested | 11/15/2015 | |

---

**Người tạo:** Testing Team  
**Ngày cập nhật:** 11/15/2015  
**Phiên bản:** 1.0

