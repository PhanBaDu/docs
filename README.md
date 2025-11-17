# Test Case Template - Xử lý đổi trả sách (Nhân viên)

## Module Code
**Giao lộ 19: Họcl6c (Nhân viên)**

## Test Requirement
1. Hiển thị danh sách đổi trả
2. Xem chi tiết yêu cầu đổi trả
3. Liên hệ đổi trả

---

## Test Summary

### Người lớp Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 36 |
| **Fail** | 0 |
| **Untested** | 0 |
| **N/A** | 0 |
| **Number of Test cases** | 36 |

---

## Test Cases

### Function: Hiển thị danh sách đổi trả

#### Check GUI: Hiển thị danh sách đổi trả

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DSDT-01** | Kiểm tra tiêu đề trang | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/returns<br>3. Kiểm tra tiêu đề | Hiển thị div space-y-6 với h1 `Xử lý đổi trả sách` class text-2xl font-bold, p `Quản lý yêu cầu đổi trả cần xử lý` class text-sm text-muted-foreground | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSDT-02** | Kiểm tra thống kê tổng quan | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/returns<br>3. Kiểm tra thống kê | Hiển thị grid grid-cols-2 md:grid-cols-5 gap-4 với các Card chứa CardContent p-4: `Tổng yêu cầu 15`, `Chờ xử lý 8`, `Đã xử lý 5`, `Đã từ chối 2`, Card cuối class col-span-2 md:col-span-1 hiển thị `Tổng giá trị 2.500.000 VNĐ` | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSDT-03** | Kiểm tra card Bộ lọc yêu cầu | 1. Truy cập /nhanvien/returns<br>2. Quan sát card | Hiển thị Card với CardHeader (CardTitle `Bộ lọc yêu cầu`, CardDescription `Trạng thái, loại, thời gian, ưu tiên, tìm kiếm`), CardContent class grid md:grid-cols-6 gap-3 chứa các control | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSDT-04** | Kiểm tra bộ lọc Trạng thái | 1. Truy cập /nhanvien/returns<br>2. Mở dropdown Trạng thái | Hiển thị SelectTrigger với SelectValue placeholder `Tất cả`, SelectContent chứa SelectItem: `Tất cả`, `Chờ xử lý`, `Đang xử lý`, `Đã xử lý`, `Đã từ chối`, `Đã hủy` | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSDT-05** | Kiểm tra bộ lọc Loại yêu cầu | 1. Truy cập /nhanvien/returns<br>2. Mở dropdown Loại yêu cầu | Hiển thị Select với các option: `Tất cả`, `Đổi sách`, `Trả sách`, `Đổi sách khác`, `Hoàn tiền` | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSDT-06** | Kiểm tra bộ lọc Khoảng thời gian | 1. Truy cập /nhanvien/returns<br>2. Kiểm tra phần Khoảng thời gian | Hiển thị grid grid-cols-2 gap-2 với hai Input type="date" (Từ ngày, Đến ngày) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSDT-07** | Kiểm tra bộ lọc Mức độ ưu tiên | 1. Truy cập /nhanvien/returns<br>2. Mở dropdown Mức độ ưu tiên | Hiển thị Select có các option: `Tất cả`, `Cao`, `Trung bình`, `Thấp` | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSDT-08** | Kiểm tra ô tìm kiếm | 1. Truy cập /nhanvien/returns<br>2. Quan sát ô tìm kiếm | Input placeholder `ID, tên, số điện thoại...` hiển thị trong grid | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSDT-09** | Kiểm tra bảng danh sách yêu cầu | 1. Truy cập /nhanvien/returns<br>2. cuộn tới bảng | Hiển thị Card (CardTitle `Danh sách yêu cầu`, CardDescription `Các yêu cầu đổi trả cần xử lý`), TableHeader có các cột: `ID yêu cầu`, `Khách hàng`, `Loại`, `Sản phẩm`, `Lý do`, `Trạng thái`, `Ngày tạo`, `Thao tác`. TableBody hiển thị hàng với dữ liệu mẫu (#RT-001, Nguyễn Văn A, Badge `Đổi sách`, …) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSDT-10** | Kiểm tra cột Thao tác | 1. Truy cập /nhanvien/returns<br>2. Quan sát cột Thao tác | Mỗi hàng có Button size="sm" variant="outline" asChild Link tới `/nhanvien/returns/RT-001` (Xem chi tiết) và Button size="sm" `Xử lý yêu cầu` | FUNC-DN-02 | Pass | 11/15/2015 | |

---

#### Check FUNC: Hiển thị danh sách đổi trả

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DSDT-01** | Xem danh sách yêu cầu đổi trả | 1. Đăng nhập Nhân viên<br>2. Truy cập /nhanvien/returns | Trang hiển thị đầy đủ: tiêu đề, thống kê 5 card, card bộ lọc với các control (Select Trạng thái/Loại, Input date range, Select ưu tiên, Input tìm kiếm), card danh sách với bảng hiển thị yêu cầu, cột Thao tác có nút `Xem chi tiết` & `Xử lý yêu cầu` | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSDT-02** | Lọc yêu cầu theo trạng thái | 1. Truy cập /nhanvien/returns<br>2. Chọn Trạng thái = `Chờ xử lý` | Bảng chỉ hiển thị các yêu cầu có trạng thái `Chờ xử lý`, Badge variant="destructive" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSDT-03** | Lọc theo loại yêu cầu | 1. Truy cập /nhanvien/returns<br>2. Chọn Loại yêu cầu = `Hoàn tiền` | Danh sách chỉ còn các yêu cầu Hoàn tiền (Badge `Hoàn tiền`), thống kê cập nhật | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSDT-04** | Lọc theo khoảng thời gian | 1. Truy cập /nhanvien/returns<br>2. Chọn Từ ngày & Đến ngày<br>3. Áp dụng | Danh sách yêu cầu cập nhật chỉ bao gồm các yêu cầu tạo trong khoảng thời gian, cột Ngày tạo phù hợp | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSDT-05** | Lọc theo mức độ ưu tiên | 1. Truy cập /nhanvien/returns<br>2. Chọn ưu tiên = `Cao` | Danh sách hiển thị các yêu cầu ưu tiên cao, Badge `Cao`, cột Thao tác vẫn hoạt động | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSDT-06** | Tìm kiếm yêu cầu | 1. Truy cập /nhanvien/returns<br>2. Nhập `RT-001` vào ô tìm kiếm | Bảng hiển thị yêu cầu #RT-001, nếu không có hiển thị thông báo “Không tìm thấy yêu cầu nào” | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSDT-07** | Sắp xếp theo ngày tạo mới nhất | 1. Truy cập /nhanvien/returns<br>2. Chọn sắp xếp = `Ngày tạo (mới nhất)` | Danh sách yêu cầu hiển thị theo thứ tự ngày tạo giảm dần, hàng đầu tiên là yêu cầu mới nhất | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSDT-08** | Xem chi tiết yêu cầu | 1. Truy cập /nhanvien/returns<br>2. Click nút `Xem chi tiết` | Điều hướng đến `/nhanvien/returns/RT-001` hiển thị chi tiết yêu cầu | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSDT-09** | Xử lý yêu cầu | 1. Truy cập /nhanvien/returns<br>2. Click cbutton `Xử lý yêu cầu` | Hiển thị dialog/form xử lý (hoặc điều hướng), cho phép cập nhật trạng thái/ghi chú, hiển thị thông báo thành công | FUNC-DSDT-08 | Pass | 11/15/2015 | |

---

### Function: Xem chi tiết yêu cầu đổi trả

#### Check GUI: Xem chi tiết yêu cầu đổi trả

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CTDT-01** | Kiểm tra tiêu đề trang | 1. Truy cập /nhanvien/returns/RT-001 | Hiển thị h1 `Chi tiết yêu cầu đổi trả #RT-001` class text-2xl font-bold | FUNC-DSDT-08 | Pass | 11/15/2015 | |
| **GUI-CTDT-02** | Kiểm tra card Thông tin chung | 1. Truy cập chi tiết yêu cầu<br>2. Quan sát card đầu | CardTitle `Thông tin chung`, CardDescription, CardContent grid grid-cols-2 md:grid-cols-3 gap-4 hiển thị ID, Trạng thái (Badge variant destructive), Loại (Badge default), Mức độ ưu tiên (Badge), Ngày tạo, Ngày cập nhật, Người xử lý | FUNC-DSDT-08 | Pass | 11/15/2015 | |
| **GUI-CTDT-03** | Kiểm tra card Thông tin khách hàng | 1. Truy cập chi tiết yêu cầu | CardTitle `Thông tin khách hàng`, grid grid-cols-2 md:grid-cols-3 hiển thị tên, số điện thoại, email, địa chỉ (md:col-span-3), Hạng khách hàng (Badge Vàng) | FUNC-DSDT-08 | Pass | 11/15/2015 | |
| **GUI-CTDT-04** | Kiểm tra card Thông tin sản phẩm | 1. Truy cập chi tiết yêu cầu | CardTitle `Thông tin sản phẩm`, CardContent có hình ảnh (Image fill `/1.png`), grid hiển thị Tên SP, Mã SP, Số lượng, Giá bán, Ngày mua, Link đơn hàng gốc `/nhanvien/orders/#ORD-001` | FUNC-DSDT-08 | Pass | 11/15/2015 | |
| **GUI-CTDT-05** | Kiểm tra card Lý do đổi trả | 1. Truy cập chi tiết yêu cầu | CardTitle `Lý do đổi trả`, hiển thị Lý do chính, Mô tả chi tiết, grid hình ảnh minh chứng (3 div h-24 bg-muted), Yêu cầu bồi thường | FUNC-DSDT-08 | Pass | 11/15/2015 | |
| **GUI-CTDT-06** | Kiểm tra card Lịch sử xử lý | 1. Truy cập chi tiết yêu cầu | CardTitle `Lịch sử xử lý`, CardContent space-y-2 text-sm hiển thị các mục `thời gian • trạng thái • người xử lý • ghi chú` | FUNC-DSDT-08 | Pass | 11/15/2015 | |
| **GUI-CTDT-07** | Kiểm tra card Ghi chú nội bộ | 1. Truy cập chi tiết yêu cầu | CardTitle `Ghi chú nội bộ`, CardContent có Label, Textarea placeholder `Nhập ghi chú nội bộ...`, Buttons `Thêm ghi chú`, `Cập nhật trạng thái`, `Liên hệ khách hàng` (Link /nhanvien/returns/RT-001/contact) | FUNC-DSDT-08 | Pass | 11/15/2015 | |

---

#### Check FUNC: Xem chi tiết yêu cầu đổi trả

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CTDT-01** | Xem thông tin chi tiết yêu cầu | 1. Truy cập /nhanvien/returns/RT-001 | Hiển thị đầy đủ tất cả card: Thông tin chung (ID, trạng thái, loại, ưu tiên, thời gian, người xử lý), Thông tin khách hàng, Thông tin sản phẩm (ảnh bìa, mã SP, link đơn hàng gốc), Lý do đổi trả (lý do chính, mô tả, hình ảnh, yêu cầu bồi thường), Lịch sử xử lý, Ghi chú nội bộ, Buttons xử lý | FUNC-DSDT-08 | Pass | 11/15/2015 | |
| **FUNC-CTDT-02** | Thêm ghi chú nội bộ | 1. Truy cập chi tiết<br>2. Nhập ghi chú vào Textarea<br>3. Click `Thêm ghi chú` | Ghi chú nội bộ được lưu, hiển thị thông báo thành công (toast success), ghi chú xuất hiện trong danh sách (nếu UI hiển thị), ghi log | FUNC-CTDT-01 | Pass | 11/15/2015 | |
| **FUNC-CTDT-03** | Cập nhật trạng thái yêu cầu | 1. Truy cập chi tiết<br>2. Click `Cập nhật trạng thái`<br>3. Chọn trạng thái mới | Hiển thị dialog hoặc form, cho phép chọn trạng thái (ví dụ: Đang xử lý, Đã xử lý, Đã từ chối), sau khi lưu: badge trạng thái cập nhật, lịch sử xử lý bổ sung dòng mới, thông báo thành công | FUNC-CTDT-01 | Pass | 11/15/2015 | |
| **FUNC-CTDT-04** | Mở trang liên hệ khách hàng | 1. Truy cập chi tiết<br>2. Click `Liên hệ khách hàng` | Điều hướng đến `/nhanvien/returns/RT-001/contact` | FUNC-CTDT-01 | Pass | 11/15/2015 | |
| **FUNC-CTDT-05** | Xem lịch sử xử lý | 1. Truy cập chi tiết<br>2. Quan sát card `Lịch sử xử lý` | Danh sách timeline hiển thị đúng thứ tự thời gian với thông tin `thời gian • trạng thái • người xử lý • ghi chú`, dữ liệu khớp với backend | FUNC-CTDT-01 | Pass | 11/15/2015 | |

---

### Function: Liên hệ đổi trả

#### Check GUI: Liên hệ đổi trả

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-LHDT-01** | Kiểm tra tiêu đề trang | 1. Truy cập /nhanvien/returns/RT-001/contact | Hiển thị h1 `Liên hệ đổi trả - #RT-001` | FUNC-CTDT-04 | Pass | 11/15/2015 | |
| **GUI-LHDT-02** | Kiểm tra card Thông tin khách hàng | 1. Truy cập contact page | CardTitle `Thông tin khách hàng`, CardContent grid md:grid-cols-4 hiển thị tên, số điện thoại, email, thời gian liên hệ | FUNC-CTDT-04 | Pass | 11/15/2015 | |
| **GUI-LHDT-03** | Kiểm tra card Thông tin yêu cầu | 1. Truy cập contact page | CardTitle `Thông tin yêu cầu`, hiển thị Loại (Badge), Sản phẩm, Lý do, Yêu cầu bồi thường | FUNC-CTDT-04 | Pass | 11/15/2015 | |
| **GUI-LHDT-04** | Kiểm tra khối Gọi điện thoại | 1. Truy cập contact page | Trong card `Phương thức liên hệ`, cột trái hiển thị Label `Số điện thoại`, Input defaultValue `0123456789`, Input `Thời gian gọi` type datetime-local, Textarea `Ghi chú cuộc gọi`, Select `Kết quả cuộc gọi` (Thành công, Không nghe máy, Máy bận, Không liên lạc được), Button `Xác nhận gọi` | FUNC-CTDT-04 | Pass | 11/15/2015 | |
| **GUI-LHDT-05** | Kiểm tra khối Gửi email | 1. Truy cập contact page | CardContent cột phải hiển thị section `Gửi email` với Input email, Input tiêu đề, Textarea nội dung, Button `Gửi email` | FUNC-CTDT-04 | Pass | 11/15/2015 | |
| **GUI-LHDT-06** | Kiểm tra khối Gửi SMS | 1. Truy cập contact page | Section `Gửi SMS` có Input số điện thoại, Textarea nội dung, Button `Gửi SMS` | FUNC-CTDT-04 | Pass | 11/15/2015 | |
| **GUI-LHDT-07** | Kiểm tra khối Chat trực tuyến | 1. Truy cập contact page | Section `Chat trực tuyến` hiển thị Select `Tin nhắn mẫu` với các option (Chào bạn…, Chúng tôi đã nhận…, Cảm ơn bạn…), Button `Mở chat`, Button `Gửi tin nhắn` | FUNC-CTDT-04 | Pass | 11/15/2015 | |
| **GUI-LHDT-08** | Kiểm tra card Lịch sử liên hệ | 1. Truy cập contact page | CardTitle `Lịch sử liên hệ`, CardContent space-y-2 text-sm hiển thị các dòng `thời gian • phương thức • nội dung • kết quả • nhân viên` | FUNC-CTDT-04 | Pass | 11/15/2015 | |
| **GUI-LHDT-09** | Kiểm tra card Cập nhật trạng thái | 1. Truy cập contact page | CardTitle `Cập nhật trạng thái yêu cầu`, CardContent flex gap-2 hiển thị Buttons `Đã liên hệ`, `Đang xử lý`, `Hoàn thành`, `Hủy yêu cầu` | FUNC-CTDT-04 | Pass | 11/15/2015 | |

---

#### Check FUNC: Liên hệ đổi trả

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-LHDT-01** | Ghi nhận cuộc gọi thành công | 1. Truy cập /nhanvien/returns/RT-001/contact<br>2. Nhập thời gian gọi, ghi chú, chọn kết quả `Thành công`<br>3. Click `Xác nhận gọi` | Cuộc gọi được ghi nhận, hiển thị thông báo thành công (toast success), lịch sử liên hệ thêm dòng `Gọi điện thoại … Thành công`, trạng thái yêu cầu có thể cập nhật thành `Đã liên hệ` | FUNC-CTDT-04 | Pass | 11/15/2015 | |
| **FUNC-LHDT-02** | Gửi email hướng dẫn đổi trả | 1. Truy cập contact page<br>2. Nhập tiêu đề, nội dung<br>3. Click `Gửi email` | Email gửi thành công, hiển thị thông báo `Đã gửi email`, email được ghi trong lịch sử liên hệ với kết quả `Thành công`, khách hàng nhận được email | FUNC-CTDT-04 | Pass | 11/15/2015 | |
| **FUNC-LHDT-03** | Gửi SMS cho khách hàng | 1. Truy cập contact page<br>2. Nhập nội dung SMS<br>3. Click `Gửi SMS` | Tin nhắn được gửi, lịch sử liên hệ bổ sung dòng `SMS • nội dung • Thành công`, trạng thái yêu cầu cập nhật | FUNC-CTDT-04 | Pass | 11/15/2015 | |
| **FUNC-LHDT-04** | Gửi tin nhắn chat trực tuyến | 1. Truy cập contact page<br>2. Chọn tin nhắn mẫu<br>3. Click `Mở chat` rồi `Gửi tin nhắn` | Cửa sổ chat mở (UI placeholder), tin nhắn được gửi, ghi lại vào lịch sử, hiển thị thông báo thành công | FUNC-CTDT-04 | Pass | 11/15/2015 | |
| **FUNC-LHDT-05** | Cập nhật trạng thái `Đã liên hệ` | 1. Truy cập contact page<br>2. Click button `Đã liên hệ` | Trạng thái yêu cầu cập nhật (Badge trong trang chi tiết thay đổi, hoặc hiển thị toast `Đã cập nhật trạng thái`), lịch sử xử lý bổ sung dòng mới | FUNC-CTDT-04 | Pass | 11/15/2015 | |
| **FUNC-LHDT-06** | Cập nhật trạng thái `Hoàn thành` | 1. Truy cập contact page<br>2. Click button `Hoàn thành` | Yêu cầu đổi trả chuyển sang trạng thái `Hoàn thành`, bảng danh sách cập nhật, hiển thị thông báo thành công, khách hàng nhận thông báo đóng yêu cầu | FUNC-CTDT-04 | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn MDX để dễ dàng quản lý và cập nhật test cases.*

