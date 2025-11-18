# Test Case Template - Quản lý vận chuyển (Admin)

## Module Code
**Giao lộ 19: Họcl6c (Admin)**

## Test Requirement
1. Hiển thị danh sách đơn vận chuyển
2. Xem chi tiết đơn vận chuyển
3. Cập nhật trạng thái vận chuyển
4. Quản lý nhà vận chuyển
5. Theo dõi vận chuyển

---

## Test Summary

### Người lớp Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 20 |
| **Fail** | 0 |
| **Untested** | 0 |
| **N/A** | 0 |
| **Number of Test cases** | 20 |

---

## Test Cases

### Function: Hiển thị danh sách đơn vận chuyển

#### Check GUI: Hiển thị danh sách đơn vận chuyển

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DSVC-01** | Kiểm tra tiêu đề trang | 1. Đăng nhập Admin<br>2. Truy cập /admin/shipping<br>3. Kiểm tra tiêu đề | Hiển thị Card với CardHeader có CardTitle "Quản lý vận chuyển" với class text-2xl font-bold, layout trong div space-y-6 | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSVC-02** | Kiểm tra card Bộ lọc | 1. Đăng nhập Admin<br>2. Truy cập /admin/shipping<br>3. Kiểm tra card bộ lọc | Hiển thị Card với CardContent có grid gap-4 md:grid-cols-5 chứa: Select "Trạng thái" với placeholder, Select "Nhà vận chuyển" với placeholder, Select "Khoảng thời gian" với placeholder, Input placeholder="Tìm mã đơn vận/đơn hàng", div flex justify-end với Button variant="outline" "Xuất báo cáo" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSVC-03** | Kiểm tra dropdown Trạng thái | 1. Đăng nhập Admin<br>2. Truy cập /admin/shipping<br>3. Kiểm tra dropdown | Hiển thị Select với SelectTrigger, SelectValue placeholder="Trạng thái", SelectContent có các option: "Chờ lấy hàng", "Đang giao", "Đã giao", "Trả về", "Hủy" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSVC-04** | Kiểm tra dropdown Nhà vận chuyển | 1. Đăng nhập Admin<br>2. Truy cập /admin/shipping<br>3. Kiểm tra dropdown | Hiển thị Select với SelectTrigger, SelectValue placeholder="Nhà vận chuyển", SelectContent có các option: "Giao Hàng Nhanh", "Viettel Post", "J&T Express", "Ninja Van" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSVC-05** | Kiểm tra card Danh sách đơn vận chuyển | 1. Đăng nhập Admin<br>2. Truy cập /admin/shipping<br>3. Kiểm tra card | Hiển thị Card với CardContent chứa Table | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSVC-06** | Kiểm tra bảng danh sách đơn vận chuyển | 1. Đăng nhập Admin<br>2. Truy cập /admin/shipping<br>3. Kiểm tra bảng | Hiển thị Table với TableHeader có các TableHead: "Mã đơn vận", "Mã đơn hàng", "Khách hàng", "Nhà vận chuyển", "Trạng thái", "Ngày tạo", "Thao tác". TableBody có các TableRow với TableCell tương ứng | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSVC-07** | Kiểm tra cột Mã đơn vận | 1. Đăng nhập Admin<br>2. Truy cập /admin/shipping<br>3. Kiểm tra cột | Mỗi hàng có TableCell chứa div flex items-center gap-2 với span (mã đơn vận, VD: VC001) và Badge với variant="default" nếu status="Đang giao" hoặc variant="secondary" nếu khác, hiển thị trạng thái | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSVC-08** | Kiểm tra cột Mã đơn hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/shipping<br>3. Kiểm tra cột | Mỗi hàng có TableCell chứa Link href="/admin/orders/[orderId]" với text là mã đơn hàng (VD: DH001), có thể click để xem chi tiết đơn hàng | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSVC-09** | Kiểm tra các nút thao tác | 1. Đăng nhập Admin<br>2. Truy cập /admin/shipping<br>3. Kiểm tra nút thao tác | Mỗi hàng có TableCell "Thao tác" với class space-x-2 chứa: Button size="sm" variant="outline" "Xem chi tiết" với Link href="/admin/shipping/[id]", Button size="sm" variant="outline" "Cập nhật trạng thái", Button size="sm" variant="outline" "Theo dõi", Button size="sm" variant="outline" "Hủy đơn" | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Hiển thị danh sách đơn vận chuyển

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DSVC-01** | Xem danh sách đơn vận chuyển | 1. Đăng nhập Admin<br>2. Truy cập /admin/shipping | Hiển thị đầy đủ: card Bộ lọc với 3 Select (Trạng thái, Nhà vận chuyển, Khoảng thời gian), 1 Input tìm kiếm, nút Xuất báo cáo, card Danh sách đơn vận chuyển với Table hiển thị các đơn vận chuyển, mỗi hàng có Mã đơn vận (với Badge trạng thái), Mã đơn hàng (Link), Khách hàng, Nhà vận chuyển, Trạng thái, Ngày tạo, các nút thao tác | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSVC-02** | Tìm kiếm đơn vận chuyển | 1. Đăng nhập Admin<br>2. Truy cập /admin/shipping<br>3. Nhập từ khóa tìm kiếm vào ô "Tìm mã đơn vận/đơn hàng" | Danh sách đơn vận chuyển được lọc theo từ khóa (mã đơn vận, mã đơn hàng), bảng cập nhật ngay lập tức (real-time filtering), hiển thị các đơn vận chuyển có mã chứa từ khóa (case-insensitive) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSVC-03** | Lọc đơn vận chuyển theo trạng thái | 1. Đăng nhập Admin<br>2. Truy cập /admin/shipping<br>3. Chọn trạng thái từ dropdown (VD: "Đang giao") | Danh sách đơn vận chuyển được lọc theo trạng thái đã chọn, bảng chỉ hiển thị đơn vận chuyển có trạng thái tương ứng, cập nhật ngay lập tức | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSVC-04** | Lọc đơn vận chuyển theo nhà vận chuyển | 1. Đăng nhập Admin<br>2. Truy cập /admin/shipping<br>3. Chọn nhà vận chuyển từ dropdown (VD: "Giao Hàng Nhanh") | Danh sách đơn vận chuyển được lọc theo nhà vận chuyển đã chọn, bảng chỉ hiển thị đơn vận chuyển có nhà vận chuyển tương ứng, cập nhật ngay lập tức | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSVC-05** | Lọc đơn vận chuyển theo khoảng thời gian | 1. Đăng nhập Admin<br>2. Truy cập /admin/shipping<br>3. Chọn khoảng thời gian từ dropdown (VD: "Tuần này") | Danh sách đơn vận chuyển được lọc theo khoảng thời gian đã chọn, bảng chỉ hiển thị đơn vận chuyển được tạo trong khoảng thời gian tương ứng, cập nhật ngay lập tức | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSVC-06** | Kết hợp nhiều bộ lọc | 1. Đăng nhập Admin<br>2. Truy cập /admin/shipping<br>3. Chọn trạng thái "Đang giao"<br>4. Chọn nhà vận chuyển "Giao Hàng Nhanh"<br>5. Nhập từ khóa tìm kiếm | Danh sách đơn vận chuyển được lọc theo tất cả các tiêu chí đã chọn, bảng chỉ hiển thị đơn vận chuyển thỏa mãn tất cả điều kiện, cập nhật ngay lập tức | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSVC-07** | Click vào mã đơn hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/shipping<br>3. Click vào Link mã đơn hàng (VD: DH001) | Chuyển đến trang chi tiết đơn hàng (/admin/orders/[orderId]), URL thay đổi, trang mới được load với thông tin đơn hàng | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Xem chi tiết đơn vận chuyển

#### Check GUI: Xem chi tiết đơn vận chuyển

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CTVC-01** | Kiểm tra tiêu đề trang | 1. Đăng nhập Admin<br>2. Truy cập /admin/shipping/[id]<br>3. Kiểm tra tiêu đề | Hiển thị tiêu đề "Chi tiết đơn vận chuyển - [Mã đơn vận]" hoặc "Chi tiết đơn vận chuyển - VC001" với class text-2xl font-bold, layout tương tự trang chi tiết nhân viên | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-CTVC-02** | Kiểm tra card Thông tin đơn vận chuyển | 1. Đăng nhập Admin<br>2. Truy cập /admin/shipping/[id]<br>3. Kiểm tra card | Hiển thị Card với CardHeader có CardTitle "Thông tin đơn vận chuyển", CardContent có grid layout, hiển thị các trường: Mã đơn vận, Mã đơn hàng (Link), Khách hàng, Nhà vận chuyển, Trạng thái (Badge), Ngày tạo, Mã vận đơn (trackingNumber) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-CTVC-03** | Kiểm tra card Địa chỉ giao hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/shipping/[id]<br>3. Kiểm tra card | Hiển thị Card với CardHeader có CardTitle "Địa chỉ giao hàng", CardContent hiển thị các trường: Tên người nhận, Số điện thoại, Địa chỉ chi tiết, Ghi chú (nếu có) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-CTVC-04** | Kiểm tra card Lịch sử vận chuyển | 1. Đăng nhập Admin<br>2. Truy cập /admin/shipping/[id]<br>3. Kiểm tra card | Hiển thị Card với CardHeader có CardTitle "Lịch sử vận chuyển", CardContent có Table hoặc timeline hiển thị các sự kiện: Thời gian, Trạng thái, Vị trí, Ghi chú, Người cập nhật | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Xem chi tiết đơn vận chuyển

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CTVC-01** | Xem chi tiết đơn vận chuyển | 1. Đăng nhập Admin<br>2. Truy cập /admin/shipping<br>3. Click nút "Xem chi tiết" hoặc Link href="/admin/shipping/[id]" | Hiển thị đầy đủ thông tin: tiêu đề "Chi tiết đơn vận chuyển - [Mã]", card Thông tin đơn vận chuyển với đầy đủ các trường (Mã đơn vận, Mã đơn hàng với Link, Khách hàng, Nhà vận chuyển, Trạng thái với Badge, Ngày tạo, Mã vận đơn), card Địa chỉ giao hàng, card Lịch sử vận chuyển với Table/timeline, các nút thao tác (Cập nhật trạng thái, Theo dõi, Hủy đơn) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-CTVC-02** | Xem lịch sử vận chuyển | 1. Đăng nhập Admin<br>2. Truy cập /admin/shipping/[id]<br>3. Xem card Lịch sử vận chuyển | Hiển thị lịch sử vận chuyển theo dòng thời gian từ cũ đến mới, mỗi sự kiện có: Thời gian, Trạng thái (Chờ lấy hàng, Đang giao, Đã giao, Trả về, Hủy), Vị trí (nếu có), Ghi chú, Người cập nhật | FUNC-DN-02, FUNC-CTVC-01 | Pass | 11/15/2015 | |

---

### Function: Cập nhật trạng thái vận chuyển

#### Check FUNC: Cập nhật trạng thái vận chuyển

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-STVC-01** | Cập nhật trạng thái vận chuyển | 1. Đăng nhập Admin<br>2. Truy cập /admin/shipping<br>3. Click nút "Cập nhật trạng thái" trên một đơn vận chuyển<br>4. Chọn trạng thái mới từ Select<br>5. Nhập mô tả/vị trí vào Textarea (nếu có)<br>6. Click "Lưu" | Hiển thị Dialog hoặc form cập nhật với Select trạng thái (các option: Chờ lấy hàng, Đang giao, Đã giao, Trả về, Hủy), có thể có Textarea "Mô tả" hoặc "Vị trí hiện tại", Input "Mã vận đơn" (nếu cần). Sau khi lưu: trạng thái vận chuyển được cập nhật thành công, hiển thị thông báo thành công (toast success), Badge trạng thái được cập nhật, thông báo được gửi cho khách hàng qua email/SMS về việc thay đổi trạng thái vận chuyển, lịch sử vận chuyển được ghi nhận với hành động "Cập nhật trạng thái", dialog/form đóng, bảng được refresh | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-STVC-02** | Cập nhật trạng thái không hợp lệ | 1. Đăng nhập Admin<br>2. Truy cập /admin/shipping<br>3. Click "Cập nhật trạng thái"<br>4. Chọn trạng thái không hợp lệ (VD: từ "Đã giao" về "Chờ lấy hàng")<br>5. Click "Lưu" | Hiển thị thông báo cảnh báo "Không thể chuyển từ trạng thái [trạng thái cũ] sang [trạng thái mới]" (toast warning), không cập nhật trạng thái | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-STVC-03** | Hủy cập nhật trạng thái | 1. Đăng nhập Admin<br>2. Truy cập /admin/shipping<br>3. Click "Cập nhật trạng thái"<br>4. Chọn trạng thái mới<br>5. Click "Hủy" trong dialog | Dialog đóng lại, không cập nhật trạng thái, trạng thái không thay đổi | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Quản lý nhà vận chuyển

#### Check FUNC: Quản lý nhà vận chuyển

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-QLNVC-01** | Xem danh sách nhà vận chuyển | 1. Đăng nhập Admin<br>2. Truy cập /admin/shipping/carriers<br>3. Xem danh sách | Hiển thị Card với Table có các cột: Tên nhà vận chuyển, Loại dịch vụ, Trạng thái (Badge), Phí vận chuyển, Thời gian giao hàng, Thao tác. Mỗi hàng có các nút: Chỉnh sửa, Xóa, Kích hoạt/Vô hiệu hóa | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-QLNVC-02** | Thêm nhà vận chuyển mới | 1. Đăng nhập Admin<br>2. Truy cập /admin/shipping/carriers<br>3. Click nút "Thêm nhà vận chuyển mới"<br>4. Nhập thông tin (Tên, Loại dịch vụ, Phí vận chuyển, Thời gian giao hàng, API key nếu có)<br>5. Click "Lưu" | Hiển thị Dialog hoặc form thêm mới với các trường: Tên nhà vận chuyển (Input required), Loại dịch vụ (Select), Phí vận chuyển (Input type="number"), Thời gian giao hàng (Input), API key (Input, nếu cần), Trạng thái (Toggle). Sau khi lưu: nhà vận chuyển mới được thêm thành công, hiển thị thông báo thành công (toast success), nhà vận chuyển mới hiển thị trong bảng, có thể được chọn trong dropdown khi tạo đơn vận chuyển | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-QLNVC-03** | Chỉnh sửa nhà vận chuyển | 1. Đăng nhập Admin<br>2. Truy cập /admin/shipping/carriers<br>3. Click nút "Chỉnh sửa" trên một nhà vận chuyển<br>4. Cập nhật thông tin (VD: Phí vận chuyển, Thời gian giao hàng)<br>5. Click "Lưu" | Hiển thị Dialog hoặc form chỉnh sửa với các trường đã điền sẵn. Sau khi lưu: thông tin nhà vận chuyển được cập nhật thành công, hiển thị thông báo thành công, bảng được cập nhật, các đơn vận chuyển đang sử dụng nhà vận chuyển này có thể được thông báo về thay đổi | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-QLNVC-04** | Xóa nhà vận chuyển | 1. Đăng nhập Admin<br>2. Truy cập /admin/shipping/carriers<br>3. Click nút "Xóa" trên một nhà vận chuyển<br>4. Xác nhận xóa | Hiển thị Dialog xác nhận "Bạn có chắc chắn muốn xóa nhà vận chuyển này?". Sau khi xác nhận: nhà vận chuyển được xóa thành công, hiển thị thông báo thành công, nhà vận chuyển biến mất khỏi bảng, không thể chọn trong dropdown khi tạo đơn vận chuyển mới, các đơn vận chuyển đang sử dụng nhà vận chuyển này vẫn giữ nguyên thông tin | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-QLNVC-05** | Kích hoạt/Vô hiệu hóa nhà vận chuyển | 1. Đăng nhập Admin<br>2. Truy cập /admin/shipping/carriers<br>3. Click nút "Vô hiệu hóa" hoặc "Kích hoạt" trên một nhà vận chuyển<br>4. Xác nhận | Trạng thái nhà vận chuyển được thay đổi (Kích hoạt/Vô hiệu hóa), hiển thị thông báo thành công, Badge trạng thái được cập nhật, nhà vận chuyển bị vô hiệu hóa không thể chọn trong dropdown khi tạo đơn vận chuyển mới | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Theo dõi vận chuyển

#### Check FUNC: Theo dõi vận chuyển

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TDVC-01** | Xem theo dõi vận chuyển | 1. Đăng nhập Admin<br>2. Truy cập /admin/shipping<br>3. Click nút "Theo dõi" trên một đơn vận chuyển | Hiển thị Dialog hoặc trang theo dõi với thông tin: Mã đơn vận, Mã vận đơn, Trạng thái hiện tại (Badge), Timeline hoặc bảng lịch sử vận chuyển với các mốc: Chờ lấy hàng, Đang lấy hàng, Đang vận chuyển, Đang giao hàng, Đã giao hàng (hoặc Trả về), mỗi mốc có thời gian, vị trí (nếu có), ghi chú, có thể có bản đồ hiển thị vị trí hiện tại (nếu có API) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TDVC-02** | Cập nhật tiến độ vận chuyển | 1. Đăng nhập Admin<br>2. Truy cập /admin/shipping/[id]<br>3. Click "Cập nhật tiến độ" hoặc "Cập nhật trạng thái"<br>4. Chọn trạng thái mới<br>5. Nhập vị trí hiện tại (nếu có)<br>6. Nhập ghi chú<br>7. Click "Lưu" | Tiến độ vận chuyển được cập nhật thành công, hiển thị thông báo thành công (toast success), timeline được cập nhật với mốc mới, thông báo được gửi cho khách hàng về tiến độ vận chuyển, lịch sử vận chuyển được ghi nhận | FUNC-DN-02, FUNC-CTVC-01 | Pass | 11/15/2015 | |
| **FUNC-TDVC-03** | Hủy đơn vận chuyển | 1. Đăng nhập Admin<br>2. Truy cập /admin/shipping<br>3. Click nút "Hủy đơn" trên một đơn vận chuyển<br>4. Nhập lý do hủy<br>5. Xác nhận | Hiển thị Dialog xác nhận với Textarea "Lý do hủy" required. Sau khi xác nhận: đơn vận chuyển được hủy thành công, hiển thị thông báo thành công, trạng thái cập nhật thành "Hủy" với Badge variant="destructive", thông báo được gửi cho khách hàng về việc đơn vận chuyển bị hủy và lý do, lịch sử vận chuyển được ghi nhận, dialog đóng, bảng được refresh | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TDVC-04** | Xuất báo cáo vận chuyển | 1. Đăng nhập Admin<br>2. Truy cập /admin/shipping<br>3. Click nút "Xuất báo cáo" | Hiển thị Dialog hoặc menu cho phép chọn định dạng (PDF, Excel) và khoảng thời gian. Sau khi chọn: báo cáo vận chuyển được xuất thành công, file được tải xuống với tên file chứa ngày tháng, file chứa: danh sách đơn vận chuyển, thống kê tổng quan, hiển thị thông báo thành công (toast success) | FUNC-DN-02 | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn MDX để dễ dàng quản lý và cập nhật test cases.*
