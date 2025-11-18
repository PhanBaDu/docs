# Test Case Template - Quản lý khách hàng (Admin)

## Module Code
**Giao lộ 19: Họcl6c (Admin)**

## Test Requirement
1. Hiển thị danh sách khách hàng
2. Xem chi tiết thông tin khách hàng
3. Quản lý rank khách hàng
4. Cập nhật thông tin khách hàng
5. Khóa/Mở khóa tài khoản khách hàng

---

## Test Summary

### Người lớp Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 28 |
| **Fail** | 0 |
| **Untested** | 0 |
| **N/A** | 0 |
| **Number of Test cases** | 28 |

---

## Test Cases

### Function: Hiển thị danh sách khách hàng

#### Check GUI: Hiển thị danh sách khách hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DSKH-01** | Kiểm tra tiêu đề trang | 1. Đăng nhập Admin<br>2. Truy cập /admin/customers<br>3. Kiểm tra tiêu đề | Hiển thị tiêu đề "Quản lý khách hàng" với class text-3xl font-bold, mô tả "Hiển thị tất cả khách hàng đã đăng ký trong hệ thống" với class text-muted-foreground, nằm trong div flex items-center justify-between | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSKH-02** | Kiểm tra thống kê khách hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/customers<br>3. Kiểm tra thống kê | Hiển thị grid grid-cols-1 md:grid-cols-4 gap-4 với 4 Card: Card 1 "Tổng khách hàng" với icon User h-8 w-8 text-primary, Card 2 "Hoạt động" với icon User trong vòng tròn bg-green-100 text-green-500, Card 3 "Tạm khóa" với icon Lock trong vòng tròn bg-red-100 text-red-500, Card 4 "Chưa xác thực" với icon AlertCircle trong vòng tròn bg-yellow-100 text-yellow-500. Mỗi card có CardContent p-4 với text-sm text-muted-foreground cho label và text-2xl font-bold cho số | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSKH-03** | Kiểm tra card Bộ lọc | 1. Đăng nhập Admin<br>2. Truy cập /admin/customers<br>3. Kiểm tra card bộ lọc | Hiển thị Card với CardContent p-4, có div flex items-center gap-4 chứa: Input tìm kiếm với icon Search absolute left-3, Select Trạng thái w-40, Select Phân loại w-40, 2 Input type="date" cho khoảng thời gian, Button variant="outline" "Bộ lọc" với icon Filter | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSKH-04** | Kiểm tra ô Tìm kiếm | 1. Đăng nhập Admin<br>2. Truy cập /admin/customers<br>3. Kiểm tra ô tìm kiếm | Hiển thị Input với icon Search absolute left-3 top-1/2, placeholder="Tìm kiếm khách hàng theo tên, email, số điện thoại...", class pl-10, flex-1 relative | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSKH-05** | Kiểm tra dropdown Trạng thái | 1. Đăng nhập Admin<br>2. Truy cập /admin/customers<br>3. Kiểm tra dropdown | Hiển thị Select với SelectTrigger w-40, SelectContent có các option: "Tất cả", "Hoạt động", "Tạm khóa", "Chưa xác thực" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSKH-06** | Kiểm tra dropdown Phân loại | 1. Đăng nhập Admin<br>2. Truy cập /admin/customers<br>3. Kiểm tra dropdown | Hiển thị Select với SelectTrigger w-40, SelectContent có các option: "Tất cả", "VIP", "Thường", "Mới" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSKH-07** | Kiểm tra card Danh sách khách hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/customers<br>3. Kiểm tra card | Hiển thị Card với CardHeader có CardTitle "Danh sách khách hàng", CardDescription "Quản lý thông tin và trạng thái tài khoản khách hàng", CardContent chứa Table | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSKH-08** | Kiểm tra bảng danh sách khách hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/customers<br>3. Kiểm tra bảng | Hiển thị Table với TableHeader có các TableHead: "Avatar", "Tên", "Email", "SĐT", "Trạng thái", "Ngày đăng ký", "Tổng đơn hàng", "Phân loại", "Thao tác" (w-24). TableBody có các TableRow với TableCell tương ứng | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSKH-09** | Kiểm tra cột Avatar | 1. Đăng nhập Admin<br>2. Truy cập /admin/customers<br>3. Kiểm tra cột Avatar | Mỗi hàng có TableCell chứa div w-10 h-10 rounded-full overflow-hidden với img w-full h-full object-cover | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSKH-10** | Kiểm tra cột Trạng thái | 1. Đăng nhập Admin<br>2. Truy cập /admin/customers<br>3. Kiểm tra cột Trạng thái | Mỗi hàng có TableCell chứa Badge với variant tương ứng (default cho active, destructive cho locked, secondary cho unverified), bên trong có div flex items-center gap-1 với icon (User/Lock/AlertCircle) và label | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSKH-11** | Kiểm tra cột Phân loại | 1. Đăng nhập Admin<br>2. Truy cập /admin/customers<br>3. Kiểm tra cột Phân loại | Mỗi hàng có TableCell chứa Badge với variant tương ứng (default cho vip, outline cho regular, secondary cho new), bên trong có div flex items-center gap-1 với icon (Crown/User/Star) và label (VIP/Thường/Mới) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSKH-12** | Kiểm tra các nút thao tác | 1. Đăng nhập Admin<br>2. Truy cập /admin/customers<br>3. Kiểm tra nút thao tác | Mỗi hàng có TableCell "Thao tác" với div flex items-center gap-1 chứa: Button variant="ghost" size="sm" với Link href="/admin/customers/[id]" và icon Eye, Button variant="ghost" size="sm" với icon Edit onClick mở dialog, Button variant="ghost" size="sm" với icon Lock/Unlock (màu đỏ/xanh) onClick, Button variant="ghost" size="sm" với icon Mail onClick | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSKH-13** | Kiểm tra phân trang | 1. Đăng nhập Admin<br>2. Truy cập /admin/customers<br>3. Kiểm tra phân trang | Hiển thị div flex items-center justify-between với text-sm text-muted-foreground "Hiển thị 1-5 trong [số] khách hàng" và div flex items-center gap-2 với các Button variant="outline" size="sm": "Trước" (disabled), "1", "2", "3", "...", "10", "Sau" | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Hiển thị danh sách khách hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DSKH-01** | Xem danh sách khách hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/customers | Hiển thị đầy đủ: thống kê 4 card (Tổng khách hàng, Hoạt động, Tạm khóa, Chưa xác thực) với số liệu và icon, card Bộ lọc với ô tìm kiếm, 2 dropdown, 2 input date, nút Bộ lọc, card Danh sách khách hàng với Table hiển thị các khách hàng, mỗi hàng có Avatar, Tên (với ID), Email, SĐT, Trạng thái (Badge với icon), Ngày đăng ký (với icon Calendar), Tổng đơn hàng (số đơn và tổng tiền), Phân loại (Badge với icon), các nút thao tác, phân trang | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSKH-02** | Tìm kiếm khách hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/customers<br>3. Nhập từ khóa tìm kiếm vào ô "Tìm kiếm khách hàng theo tên, email, số điện thoại..." | Danh sách khách hàng được lọc theo từ khóa (tên, email, số điện thoại), bảng cập nhật ngay lập tức (real-time), hiển thị các khách hàng phù hợp | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSKH-03** | Lọc khách hàng theo trạng thái | 1. Đăng nhập Admin<br>2. Truy cập /admin/customers<br>3. Chọn trạng thái từ dropdown (VD: "Hoạt động") | Danh sách khách hàng được lọc theo trạng thái đã chọn, bảng chỉ hiển thị khách hàng có trạng thái tương ứng, thống kê có thể cập nhật | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSKH-04** | Lọc khách hàng theo phân loại | 1. Đăng nhập Admin<br>2. Truy cập /admin/customers<br>3. Chọn phân loại từ dropdown (VD: "VIP") | Danh sách khách hàng được lọc theo phân loại đã chọn, bảng chỉ hiển thị khách hàng có phân loại tương ứng | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSKH-05** | Lọc khách hàng theo khoảng thời gian | 1. Đăng nhập Admin<br>2. Truy cập /admin/customers<br>3. Chọn ngày bắt đầu và ngày kết thúc | Danh sách khách hàng được lọc theo khoảng thời gian đăng ký, bảng chỉ hiển thị khách hàng đăng ký trong khoảng thời gian đã chọn | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSKH-06** | Kết hợp nhiều bộ lọc | 1. Đăng nhập Admin<br>2. Truy cập /admin/customers<br>3. Chọn trạng thái "Hoạt động"<br>4. Chọn phân loại "VIP"<br>5. Nhập từ khóa tìm kiếm | Danh sách khách hàng được lọc theo tất cả các tiêu chí đã chọn, bảng chỉ hiển thị khách hàng thỏa mãn tất cả điều kiện | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSKH-07** | Phân trang danh sách | 1. Đăng nhập Admin<br>2. Truy cập /admin/customers<br>3. Click số trang hoặc nút "Sau" | Danh sách chuyển sang trang tiếp theo, hiển thị các khách hàng của trang đó, text "Hiển thị X-Y trong [số] khách hàng" được cập nhật | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Xem chi tiết thông tin khách hàng

#### Check GUI: Xem chi tiết khách hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CTKH-01** | Kiểm tra tiêu đề trang | 1. Đăng nhập Admin<br>2. Truy cập /admin/customers/[id]<br>3. Kiểm tra tiêu đề | Hiển thị tiêu đề "Chi tiết khách hàng - [Mã khách hàng]" với class text-2xl font-bold, layout tương tự trang chi tiết nhân viên | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-CTKH-02** | Kiểm tra card Thông tin cá nhân | 1. Đăng nhập Admin<br>2. Truy cập /admin/customers/[id]<br>3. Kiểm tra card | Hiển thị Card với CardHeader có CardTitle "Thông tin cá nhân", CardContent có grid layout, hiển thị các trường: Mã khách hàng, Họ tên, Email, Số điện thoại, Địa chỉ, Ngày sinh, Giới tính | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-CTKH-03** | Kiểm tra card Thông tin thành viên | 1. Đăng nhập Admin<br>2. Truy cập /admin/customers/[id]<br>3. Kiểm tra card | Hiển thị Card với CardHeader có CardTitle "Thông tin thành viên", CardContent hiển thị các trường: Rank (Badge), Điểm tích lũy, Tổng chi tiêu, Ngày đăng ký, Trạng thái (Badge), % giảm giá | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-CTKH-04** | Kiểm tra card Lịch sử mua hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/customers/[id]<br>3. Kiểm tra card | Hiển thị Card với CardHeader có CardTitle "Lịch sử mua hàng", CardContent có Table với các cột: Mã đơn hàng, Ngày mua, Số lượng sách, Tổng tiền, Trạng thái, Thao tác | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Xem chi tiết khách hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CTKH-01** | Xem chi tiết khách hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/customers<br>3. Click nút Eye icon hoặc Link href="/admin/customers/[id]" | Hiển thị đầy đủ thông tin: tiêu đề "Chi tiết khách hàng - [Mã]", card Thông tin cá nhân với đầy đủ các trường, card Thông tin thành viên với đầy đủ các trường, card Lịch sử mua hàng với Table, các nút thao tác | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-CTKH-02** | Xem lịch sử mua hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/customers/[id]<br>3. Xem card Lịch sử mua hàng | Hiển thị lịch sử mua hàng theo dòng thời gian từ cũ đến mới, mỗi đơn hàng có Mã đơn hàng, Ngày mua, Số lượng sách, Tổng tiền, Trạng thái, nút Xem chi tiết đơn hàng | FUNC-DN-02, FUNC-CTKH-01 | Pass | 11/15/2015 | |
| **FUNC-CTKH-03** | Xem chi tiết đơn hàng từ lịch sử | 1. Đăng nhập Admin<br>2. Truy cập /admin/customers/[id]<br>3. Click [Xem chi tiết đơn hàng] trên một đơn hàng | Chuyển đến trang chi tiết đơn hàng (/admin/orders/[id]), URL thay đổi, trang mới được load | FUNC-DN-02, FUNC-CTKH-01 | Pass | 11/15/2015 | |

---

### Function: Quản lý rank khách hàng

#### Check GUI: Quản lý rank khách hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-RANK-01** | Kiểm tra tiêu đề trang | 1. Đăng nhập Admin<br>2. Truy cập /admin/customers/ranks<br>3. Kiểm tra tiêu đề | Hiển thị tiêu đề "Quản lý rank khách hàng" với layout tương tự các trang quản lý khác | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-RANK-02** | Kiểm tra thống kê rank | 1. Đăng nhập Admin<br>2. Truy cập /admin/customers/ranks<br>3. Kiểm tra thống kê | Hiển thị thống kê phân bố khách hàng theo rank dạng Card hoặc biểu đồ, hiển thị số lượng khách hàng ở mỗi rank | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-RANK-03** | Kiểm tra bảng cấu hình rank | 1. Đăng nhập Admin<br>2. Truy cập /admin/customers/ranks<br>3. Kiểm tra bảng | Hiển thị Card với Table có các cột: Rank, Điểm tối thiểu, % giảm giá, Ưu đãi đặc biệt, Mô tả, Thao tác. Mỗi hàng có các nút: Chỉnh sửa, Xóa | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Quản lý rank khách hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-RANK-01** | Xem cấu hình rank | 1. Đăng nhập Admin<br>2. Truy cập /admin/customers/ranks | Hiển thị bảng cấu hình các rank (Đồng, Bạc, Vàng, Bạch kim, Kim cương), mỗi rank có thông tin: Điểm tối thiểu, % giảm giá, Ưu đãi đặc biệt, Mô tả, thống kê phân bố khách hàng theo rank | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-RANK-02** | Chỉnh sửa rank | 1. Đăng nhập Admin<br>2. Truy cập /admin/customers/ranks<br>3. Click [Chỉnh sửa] trên một rank<br>4. Cập nhật thông tin (VD: Điểm tối thiểu, % giảm giá)<br>5. Lưu | Hiển thị Dialog hoặc form chỉnh sửa với các trường đã điền sẵn. Sau khi lưu: thông tin rank được cập nhật thành công, hiển thị thông báo thành công (toast success), các khách hàng bị ảnh hưởng được cập nhật rank tự động dựa trên điểm tích lũy mới | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-RANK-03** | Thêm rank mới | 1. Đăng nhập Admin<br>2. Truy cập /admin/customers/ranks<br>3. Click [Thêm rank mới]<br>4. Nhập thông tin (Tên rank, Điểm tối thiểu, % giảm giá, Ưu đãi, Mô tả)<br>5. Lưu | Hiển thị Dialog hoặc form thêm mới. Sau khi lưu: rank mới được tạo thành công, hiển thị thông báo thành công, rank mới hiển thị trong bảng, các khách hàng đủ điều kiện được cập nhật rank tự động | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-RANK-04** | Xóa rank | 1. Đăng nhập Admin<br>2. Truy cập /admin/customers/ranks<br>3. Click [Xóa] trên một rank<br>4. Xác nhận xóa | Hiển thị Dialog xác nhận "Bạn có chắc chắn muốn xóa rank này?". Sau khi xác nhận: rank được xóa thành công, hiển thị thông báo thành công, khách hàng có rank bị xóa được chuyển về rank thấp hơn (hoặc rank mặc định), rank biến mất khỏi bảng | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Cập nhật thông tin khách hàng

#### Check FUNC: Cập nhật thông tin khách hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-SKH-01** | Cập nhật thông tin khách hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/customers<br>3. Click nút Edit icon trên một khách hàng<br>4. Cập nhật thông tin (Tên, Email, Số điện thoại)<br>5. Click "Lưu thay đổi" | Hiển thị Dialog với DialogTitle "Chỉnh sửa thông tin khách hàng", DialogDescription "Cập nhật thông tin cho khách hàng [Tên]", có các Input với giá trị mặc định. Sau khi lưu: thông tin được cập nhật thành công, hiển thị thông báo "Cập nhật thông tin khách hàng thành công" (toast success), dialog đóng, bảng được cập nhật với thông tin mới | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-SKH-02** | Hủy cập nhật thông tin | 1. Đăng nhập Admin<br>2. Truy cập /admin/customers<br>3. Click nút Edit icon<br>4. Thay đổi thông tin<br>5. Click "Hủy" | Dialog đóng lại, không cập nhật thông tin, bảng vẫn giữ nguyên thông tin cũ | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-SKH-03** | Thay đổi rank khách hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/customers/[id]<br>3. Click [Thay đổi rank]<br>4. Chọn rank mới từ Select<br>5. Lưu | Rank được thay đổi thành công, hiển thị thông báo thành công, thông tin thành viên được cập nhật, thông báo được gửi cho khách hàng qua email về việc thay đổi rank và các ưu đãi mới | FUNC-DN-02, FUNC-CTKH-01 | Pass | 11/15/2015 | |

---

### Function: Khóa/Mở khóa tài khoản khách hàng

#### Check FUNC: Khóa/Mở khóa tài khoản

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-KKH-01** | Khóa tài khoản khách hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/customers<br>3. Click nút Lock icon (màu đỏ) trên một khách hàng đang hoạt động<br>4. Xác nhận (nếu có dialog) | Tài khoản được khóa thành công, hiển thị thông báo "Đã khóa tài khoản [Tên khách hàng]" (toast success), trạng thái cập nhật thành "Tạm khóa" với Badge variant="destructive" và icon Lock, thông báo được gửi cho khách hàng qua email về việc tài khoản bị khóa | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-KKH-02** | Mở khóa tài khoản khách hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/customers<br>3. Click nút Unlock icon (màu xanh) trên một khách hàng đã khóa<br>4. Xác nhận (nếu có dialog) | Tài khoản được mở khóa thành công, hiển thị thông báo "Đã mở khóa tài khoản [Tên khách hàng]" (toast success), trạng thái cập nhật thành "Hoạt động" với Badge variant="default" và icon User, thông báo được gửi cho khách hàng qua email về việc tài khoản đã được mở khóa | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-KKH-03** | Gửi email cho khách hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/customers<br>3. Click nút Mail icon trên một khách hàng | Hiển thị Dialog hoặc form gửi email, có thể chọn template email hoặc soạn thư tùy chỉnh. Sau khi gửi: hiển thị thông báo "Đã gửi email cho [Tên khách hàng]" (toast success) | FUNC-DN-02 | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn MDX để dễ dàng quản lý và cập nhật test cases.*
