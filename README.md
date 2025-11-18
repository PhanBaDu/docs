# Test Case Template - Thông báo (Admin)

## Module Code
**Giao lộ 19: Họcl6c (Admin)**

## Test Requirement
1. Quản lý thông báo
2. Xem danh sách thông báo
3. Đánh dấu đã đọc
4. Xóa thông báo

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

### Function: Quản lý thông báo

#### Check GUI: Quản lý thông báo

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-TB-01** | Kiểm tra tiêu đề trang | 1. Đăng nhập Admin<br>2. Truy cập /admin/notifications<br>3. Kiểm tra tiêu đề | Hiển thị div space-y-6 với header có h1 "Quản lý thông báo" class text-3xl font-bold, p "Gửi và quản lý thông báo cho khách hàng" class text-muted-foreground, Button "Tạo thông báo mới" có icon Plus h-4 w-4 mr-2 | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-TB-02** | Kiểm tra thống kê thông báo | 1. Đăng nhập Admin<br>2. Truy cập /admin/notifications<br>3. Kiểm tra thống kê | Hiển thị grid grid-cols-1 md:grid-cols-4 gap-4 với 4 Card: Card "Tổng thông báo" với icon Bell h-6 w-6 text-blue-600 trong div p-2 rounded-full bg-blue-100, số "24" text-2xl font-bold, label "Tổng thông báo" text-sm text-muted-foreground. Card "Đã gửi" với icon Send h-6 w-6 text-green-600 trong div p-2 rounded-full bg-green-100, số "18" text-2xl font-bold, label "Đã gửi" text-sm text-muted-foreground. Card "Đã lên lịch" với icon Clock h-6 w-6 text-yellow-600 trong div p-2 rounded-full bg-yellow-100, số "3" text-2xl font-bold, label "Đã lên lịch" text-sm text-muted-foreground. Card "Người nhận" với icon Users h-6 w-6 text-purple-600 trong div p-2 rounded-full bg-purple-100, số "1,250" text-2xl font-bold, label "Người nhận" text-sm text-muted-foreground | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-TB-03** | Kiểm tra card Danh sách thông báo | 1. Đăng nhập Admin<br>2. Truy cập /admin/notifications<br>3. Kiểm tra card | Hiển thị Card với CardHeader có CardTitle "Danh sách thông báo", div flex items-center justify-between với Input placeholder="Tìm kiếm..." className="pl-10 w-64" có icon Search absolute left-3 top-1/2 transform -translate-y-1/2 h-4 w-4 text-muted-foreground, Button variant="outline" "Lọc" có icon Filter h-4 w-4 mr-2, CardContent chứa div space-y-4 với danh sách thông báo | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-TB-04** | Kiểm tra item thông báo | 1. Đăng nhập Admin<br>2. Truy cập /admin/notifications<br>3. Kiểm tra item | Mỗi item thông báo có div border rounded-lg p-4 với: div flex items-start justify-between mb-3 chứa div flex-1 với h3 font-semibold (title), Badge với statusInfo.color (statusInfo.label), Badge variant="outline" với typeInfo.color (typeInfo.icon + typeInfo.label), p text-sm text-muted-foreground mb-2 (content), div flex items-center gap-4 text-xs text-muted-foreground với "Người nhận: {recipients}", "Gửi: {sentAt}" (nếu có), "Tỷ lệ mở: {openRate}%" (nếu > 0), div flex items-center gap-2 với Button variant="ghost" size="sm" có icon Eye h-4 w-4, Button variant="ghost" size="sm" có icon Edit h-4 w-4, Button variant="ghost" size="sm" className="text-destructive" có icon Trash2 h-4 w-4 | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-TB-05** | Kiểm tra card Tạo thông báo mới | 1. Đăng nhập Admin<br>2. Truy cập /admin/notifications<br>3. Kiểm tra card sidebar | Hiển thị Card với CardHeader có CardTitle "Tạo thông báo mới", CardContent space-y-4 với: label "Loại thông báo" text-sm font-medium mb-2 block, select w-full p-2 border rounded-md với các option (Khuyến mãi, Hệ thống, Đơn hàng, Cá nhân), label "Đối tượng nhận" text-sm font-medium mb-2 block, select w-full p-2 border rounded-md với các option từ targetGroups, label "Tiêu đề" text-sm font-medium mb-2 block, Input placeholder="Tiêu đề thông báo", label "Nội dung" text-sm font-medium mb-2 block, Textarea placeholder="Nội dung thông báo..." rows={4}, label "Thời gian gửi" text-sm font-medium mb-2 block, div flex gap-2 với Input type="datetime-local", Button variant="outline" size="sm" có icon Clock h-4 w-4, Button className="w-full" "Gửi thông báo" có icon Send h-4 w-4 mr-2 | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-TB-06** | Kiểm tra card Mẫu thông báo | 1. Đăng nhập Admin<br>2. Truy cập /admin/notifications<br>3. Kiểm tra card | Hiển thị Card với CardHeader có CardTitle "Mẫu thông báo", CardContent space-y-3 với các div border rounded-lg p-3 chứa: div flex items-center justify-between mb-2 với h4 font-medium text-sm (template.name), Button variant="ghost" size="sm" có icon Edit h-4 w-4, p text-xs text-muted-foreground mb-2 (template.subject), div flex flex-wrap gap-1 với các Badge variant="outline" className="text-xs" (template.variables) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-TB-07** | Kiểm tra card Nhóm đối tượng | 1. Đăng nhập Admin<br>2. Truy cập /admin/notifications<br>3. Kiểm tra card | Hiển thị Card với CardHeader có CardTitle "Nhóm đối tượng", CardContent space-y-3 với các div flex items-center justify-between p-2 rounded hover:bg-muted chứa span text-sm (group.name), Badge variant="secondary" (group.count) | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Quản lý thông báo

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TB-01** | Xem danh sách thông báo | 1. Đăng nhập Admin<br>2. Truy cập /admin/notifications | Hiển thị đầy đủ: header với tiêu đề "Quản lý thông báo" và mô tả, nút "Tạo thông báo mới", thống kê 4 card (Tổng thông báo: 24, Đã gửi: 18, Đã lên lịch: 3, Người nhận: 1,250), card Danh sách thông báo với Input tìm kiếm và nút Lọc, danh sách các thông báo với đầy đủ thông tin (title, status Badge, type Badge, content, recipients, sentAt, openRate), các nút thao tác (Eye, Edit, Trash2), card Tạo thông báo mới với form đầy đủ, card Mẫu thông báo với các template, card Nhóm đối tượng với các nhóm | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TB-02** | Tìm kiếm thông báo | 1. Đăng nhập Admin<br>2. Truy cập /admin/notifications<br>3. Nhập từ khóa tìm kiếm vào Input (VD: "khuyến mãi")<br>4. Nhấn Enter hoặc click icon Search | Danh sách thông báo được lọc theo từ khóa, chỉ hiển thị các thông báo có title hoặc content chứa từ khóa "khuyến mãi", các thông báo khác bị ẩn, có thể hiển thị thông báo "Không tìm thấy thông báo nào" nếu không có kết quả | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TB-03** | Lọc thông báo | 1. Đăng nhập Admin<br>2. Truy cập /admin/notifications<br>3. Click nút "Lọc"<br>4. Chọn các tiêu chí lọc (loại, trạng thái, khoảng thời gian)<br>5. Click "Áp dụng" | Hiển thị Dialog hoặc dropdown với các bộ lọc: Select "Loại thông báo" (Tất cả, Khuyến mãi, Hệ thống, Đơn hàng, Cá nhân, Tồn kho), Select "Trạng thái" (Tất cả, Bản nháp, Đã lên lịch, Đã gửi, Gửi thất bại), 2 Input type="date" cho khoảng thời gian, Button "Áp dụng" và "Hủy". Sau khi áp dụng: danh sách thông báo được lọc theo các tiêu chí đã chọn, chỉ hiển thị các thông báo phù hợp, dialog/dropdown đóng lại | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TB-04** | Xem chi tiết thông báo | 1. Đăng nhập Admin<br>2. Truy cập /admin/notifications<br>3. Click nút icon Eye trên một thông báo | Hiển thị Dialog hoặc trang chi tiết với thông tin đầy đủ: title, content, type (Badge), status (Badge), target (nhóm đối tượng), sentAt (nếu đã gửi), recipients, openRate (nếu > 0), clickRate (nếu > 0), có thể có nút "Đóng" hoặc "Quay lại" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TB-05** | Tạo thông báo mới | 1. Đăng nhập Admin<br>2. Truy cập /admin/notifications<br>3. Click nút "Tạo thông báo mới" hoặc điền form trong card sidebar<br>4. Chọn loại thông báo (VD: "Khuyến mãi")<br>5. Chọn đối tượng nhận (VD: "Tất cả người dùng (1250)")<br>6. Nhập tiêu đề (VD: "Khuyến mãi cuối tuần")<br>7. Nhập nội dung (VD: "Giảm 20% cho tất cả sản phẩm...")<br>8. Chọn thời gian gửi (hoặc để trống để gửi ngay)<br>9. Click "Gửi thông báo" | Thông báo được tạo thành công, hiển thị thông báo thành công "Tạo thông báo thành công" (toast success), nếu chọn thời gian gửi: status là "Đã lên lịch" với Badge màu vàng, nếu không chọn: status là "Đã gửi" với Badge màu xanh và thông báo được gửi ngay, thông báo mới xuất hiện ở đầu danh sách, form được reset về trạng thái ban đầu, thống kê được cập nhật (Tổng thông báo tăng, Đã gửi hoặc Đã lên lịch tăng) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TB-06** | Tạo thông báo thiếu thông tin | 1. Đăng nhập Admin<br>2. Truy cập /admin/notifications<br>3. Click nút "Tạo thông báo mới"<br>4. Để trống tiêu đề hoặc nội dung<br>5. Click "Gửi thông báo" | Hiển thị thông báo lỗi "Vui lòng điền đầy đủ thông tin" (toast error), không tạo thông báo, form vẫn ở trạng thái nhập liệu, các trường bắt buộc có thể được highlight màu đỏ | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TB-07** | Sửa thông báo | 1. Đăng nhập Admin<br>2. Truy cập /admin/notifications<br>3. Click nút icon Edit trên một thông báo (status là "Bản nháp" hoặc "Đã lên lịch")<br>4. Sửa tiêu đề, nội dung, hoặc các thông tin khác<br>5. Click "Lưu" | Hiển thị Dialog hoặc form chỉnh sửa với các trường đã được điền sẵn, sau khi lưu: thông báo được cập nhật thành công, hiển thị thông báo thành công "Cập nhật thông báo thành công" (toast success), thông tin thông báo trong danh sách được cập nhật, dialog/form đóng lại | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TB-08** | Xóa thông báo | 1. Đăng nhập Admin<br>2. Truy cập /admin/notifications<br>3. Click nút icon Trash2 trên một thông báo<br>4. Xác nhận xóa trong Dialog | Hiển thị Dialog với DialogTitle "Xác nhận xóa", DialogDescription "Bạn có chắc chắn muốn xóa thông báo này?", nút "Hủy" và "Xác nhận xóa" variant="destructive". Sau khi xác nhận: thông báo được xóa thành công, hiển thị thông báo thành công "Đã xóa thông báo" (toast success), thông báo biến mất khỏi danh sách, thống kê được cập nhật (Tổng thông báo giảm), dialog đóng lại | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TB-09** | Hủy xóa thông báo | 1. Đăng nhập Admin<br>2. Truy cập /admin/notifications<br>3. Click nút icon Trash2<br>4. Click "Hủy" trong Dialog | Dialog đóng lại, không xóa thông báo, thông báo vẫn còn trong danh sách | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TB-10** | Sử dụng mẫu thông báo | 1. Đăng nhập Admin<br>2. Truy cập /admin/notifications<br>3. Click vào một mẫu thông báo trong card "Mẫu thông báo" hoặc click icon Edit trên mẫu<br>4. Điền các biến (variables) vào form<br>5. Click "Gửi thông báo" | Form "Tạo thông báo mới" được điền sẵn với nội dung từ mẫu, các biến (VD: {customer_name}, {discount}) được thay thế bằng giá trị đã nhập, thông báo được tạo và gửi thành công, hiển thị thông báo thành công (toast success) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TB-11** | Gửi thông báo đã lên lịch | 1. Đăng nhập Admin<br>2. Truy cập /admin/notifications<br>3. Tìm thông báo có status "Đã lên lịch"<br>4. Click nút "Gửi ngay" (nếu có) hoặc chờ đến thời gian đã lên lịch | Nếu click "Gửi ngay": thông báo được gửi ngay lập tức, status cập nhật thành "Đã gửi" với Badge màu xanh, thống kê được cập nhật (Đã gửi tăng, Đã lên lịch giảm). Nếu chờ đến thời gian: hệ thống tự động gửi thông báo khi đến thời gian đã lên lịch, status cập nhật thành "Đã gửi", thông báo được gửi đến tất cả người nhận trong nhóm đối tượng đã chọn | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TB-12** | Xem thống kê thông báo | 1. Đăng nhập Admin<br>2. Truy cập /admin/notifications<br>3. Xem các card thống kê | Hiển thị đầy đủ 4 card thống kê với số liệu chính xác: Tổng thông báo (tổng số thông báo đã tạo), Đã gửi (số thông báo đã gửi thành công), Đã lên lịch (số thông báo đang chờ gửi), Người nhận (tổng số người nhận từ tất cả thông báo đã gửi). Các số liệu được cập nhật real-time khi có thay đổi | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TB-13** | Xem tỷ lệ mở và click | 1. Đăng nhập Admin<br>2. Truy cập /admin/notifications<br>3. Xem chi tiết một thông báo đã gửi (click icon Eye) | Hiển thị Dialog chi tiết với thông tin: Tỷ lệ mở (openRate) tính bằng phần trăm số người đã mở thông báo / tổng số người nhận, Tỷ lệ click (clickRate) tính bằng phần trăm số người đã click vào thông báo / tổng số người nhận, có thể có biểu đồ hoặc số liệu chi tiết hơn (số người mở, số người click, số người không mở) | FUNC-DN-02, FUNC-TB-04 | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn MDX để dễ dàng quản lý và cập nhật test cases.*
