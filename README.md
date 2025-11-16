# Test Case Template - Bảo mật (Admin)

## Module Code
**Model Management Store: Bảo mật Admin**

## Test Requirement
1. Xem lịch sử đăng nhập
2. Quản lý phiên đăng nhập
3. Phát hiện đăng nhập lạ
4. Auto logout khi hết hạn

---

## Test Summary

### Người thực hiện Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 30 |
| **Fail** | 0 |
| **Untested** | 31 |
| **N/A** | 0 |
| **Number of Test cases** | 61 |

---

## Test Cases

### Function: Xem lịch sử đăng nhập

#### Check GUI: Xem lịch sử đăng nhập

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XLSDN-01** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/security/login-history<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Lịch sử đăng nhập" với kích thước text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-XLSDN-02** | Kiểm tra mô tả chức năng | 1. Truy cập /admin/security/login-history<br>2. Kiểm tra mô tả | Hiển thị mô tả "Xem các lần đăng nhập gần đây" màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-XLSDN-03** | Kiểm tra Select Bộ lọc thời gian | 1. Truy cập /admin/security/login-history<br>2. Kiểm tra Select | Hiển thị Select "Thời gian" với placeholder "Chọn thời gian", có các option: Tất cả, Tuần này, Tháng này, 3 tháng gần đây | | Pass | 11/15/2015 | |
| **GUI-XLSDN-04** | Kiểm tra Select Bộ lọc thiết bị | 1. Truy cập /admin/security/login-history<br>2. Kiểm tra Select | Hiển thị Select "Thiết bị" với placeholder "Chọn thiết bị", có các option: Tất cả, Desktop, Mobile, Tablet | | Pass | 11/15/2015 | |
| **GUI-XLSDN-05** | Kiểm tra Select Bộ lọc trạng thái | 1. Truy cập /admin/security/login-history<br>2. Kiểm tra Select | Hiển thị Select "Trạng thái" với placeholder "Chọn trạng thái", có các option: Tất cả, Thành công, Thất bại | | Pass | 11/15/2015 | |
| **GUI-XLSDN-06** | Kiểm tra Table lịch sử đăng nhập | 1. Truy cập /admin/security/login-history<br>2. Kiểm tra Table | Hiển thị Table với các cột: STT, Thời gian, IP, Thiết bị, OS, Trình duyệt, Vị trí, Trạng thái | | Pass | 11/15/2015 | |
| **GUI-XLSDN-07** | Kiểm tra Badge trạng thái Thành công | 1. Truy cập /admin/security/login-history<br>2. Kiểm tra Badge | Hiển thị Badge "Thành công" màu green với icon CheckCircle | | Pass | 11/15/2015 | |
| **GUI-XLSDN-08** | Kiểm tra Badge trạng thái Thất bại | 1. Truy cập /admin/security/login-history<br>2. Kiểm tra Badge | Hiển thị Badge "Thất bại" màu red với icon XCircle | | Pass | 11/15/2015 | |
| **GUI-XLSDN-09** | Kiểm tra Badge đăng nhập lạ | 1. Truy cập /admin/security/login-history<br>2. Kiểm tra Badge | Hiển thị Badge "Đăng nhập lạ" màu orange với icon AlertTriangle cho các đăng nhập từ thiết bị mới hoặc vị trí mới | | Pass | 11/15/2015 | |
| **GUI-XLSDN-10** | Kiểm tra Pagination | 1. Truy cập /admin/security/login-history<br>2. Kiểm tra Pagination | Hiển thị Pagination với nút Previous, Next, số trang, số bản ghi mỗi trang | | Pass | 11/15/2015 | |

---

### Check FUNC: Xem lịch sử đăng nhập

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XLSDN-01** | Mở trang lịch sử đăng nhập | 1. Truy cập /admin/security/login-history | Hiển thị danh sách lịch sử đăng nhập với đầy đủ thông tin: thời gian, IP, thiết bị, OS, trình duyệt, vị trí, trạng thái, các bộ lọc | | Pass | 11/15/2015 | |
| **FUNC-XLSDN-02** | Hiển thị danh sách khi có dữ liệu | 1. Truy cập /admin/security/login-history<br>2. Có dữ liệu lịch sử | Hiển thị danh sách lịch sử đăng nhập trong Table, mỗi dòng hiển thị đầy đủ thông tin | | Pass | 11/15/2015 | |
| **FUNC-XLSDN-03** | Hiển thị khi không có dữ liệu | 1. Truy cập /admin/security/login-history<br>2. Không có dữ liệu | Hiển thị thông báo "Chưa có lịch sử đăng nhập nào", Table rỗng | | Pass | 11/15/2015 | |
| **FUNC-XLSDN-04** | Lọc theo thời gian | 1. Truy cập /admin/security/login-history<br>2. Chọn "Tuần này" từ Select "Thời gian" | Danh sách được cập nhật, chỉ hiển thị các đăng nhập trong tuần này | | Pass | 11/15/2015 | |
| **FUNC-XLSDN-05** | Lọc theo thiết bị | 1. Truy cập /admin/security/login-history<br>2. Chọn "Mobile" từ Select "Thiết bị" | Danh sách được cập nhật, chỉ hiển thị các đăng nhập từ thiết bị Mobile | | Pass | 11/15/2015 | |
| **FUNC-XLSDN-06** | Lọc theo trạng thái | 1. Truy cập /admin/security/login-history<br>2. Chọn "Thất bại" từ Select "Trạng thái" | Danh sách được cập nhật, chỉ hiển thị các đăng nhập thất bại | | Pass | 11/15/2015 | |
| **FUNC-XLSDN-07** | Kết hợp nhiều bộ lọc | 1. Truy cập /admin/security/login-history<br>2. Chọn thời gian, thiết bị, trạng thái | Danh sách được cập nhật theo tất cả các tiêu chí đã chọn | | Pass | 11/15/2015 | |
| **FUNC-XLSDN-08** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/security/login-history<br>2. Tắt kết nối mạng | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại" | | Untested | 11/15/2015 | |
| **FUNC-XLSDN-09** | Xử lý khi server lỗi | 1. Truy cập /admin/security/login-history<br>2. Server trả về lỗi 500 | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau" | | Untested | 11/15/2015 | |

---

### Function: Quản lý phiên đăng nhập

#### Check GUI: Quản lý phiên đăng nhập

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-QLPDN-01** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/security/sessions<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Quản lý phiên đăng nhập" với kích thước text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-QLPDN-02** | Kiểm tra mô tả chức năng | 1. Truy cập /admin/security/sessions<br>2. Kiểm tra mô tả | Hiển thị mô tả "Xóa/đăng xuất các phiên trên thiết bị" màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-QLPDN-03** | Kiểm tra Card Phiên hiện tại | 1. Truy cập /admin/security/sessions<br>2. Kiểm tra Card | Hiển thị Card "Phiên hiện tại" với: Thiết bị, Thời gian, IP, Vị trí, Badge "Phiên hiện tại" | | Pass | 11/15/2015 | |
| **GUI-QLPDN-04** | Kiểm tra Danh sách phiên khác | 1. Truy cập /admin/security/sessions<br>2. Kiểm tra danh sách | Hiển thị danh sách các phiên khác với: Thiết bị, OS, Trình duyệt, Hoạt động cuối, Trạng thái, nút Xóa phiên | | Pass | 11/15/2015 | |
| **GUI-QLPDN-05** | Kiểm tra nút Xóa phiên | 1. Truy cập /admin/security/sessions<br>2. Kiểm tra nút | Mỗi phiên (trừ phiên hiện tại) có nút "Xóa phiên" với icon Trash2, màu destructive | | Pass | 11/15/2015 | |
| **GUI-QLPDN-06** | Kiểm tra nút Đăng xuất tất cả | 1. Truy cập /admin/security/sessions<br>2. Kiểm tra nút | Hiển thị nút "Đăng xuất tất cả thiết bị" variant destructive, ở đầu trang | | Pass | 11/15/2015 | |
| **GUI-QLPDN-07** | Kiểm tra Modal xác nhận xóa | 1. Click "Xóa phiên"<br>2. Kiểm tra Modal | Hiển thị Modal "Xác nhận xóa phiên" với: tiêu đề, nội dung cảnh báo, nút "Hủy", nút "Xác nhận xóa" | | Pass | 11/15/2015 | |
| **GUI-QLPDN-08** | Kiểm tra Modal xác nhận đăng xuất tất cả | 1. Click "Đăng xuất tất cả thiết bị"<br>2. Kiểm tra Modal | Hiển thị Modal "Xác nhận đăng xuất tất cả" với: tiêu đề, nội dung cảnh báo, nút "Hủy", nút "Xác nhận" | | Pass | 11/15/2015 | |

---

### Check FUNC: Quản lý phiên đăng nhập

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-QLPDN-01** | Mở trang quản lý phiên đăng nhập | 1. Truy cập /admin/security/sessions | Hiển thị trang với Card Phiên hiện tại, danh sách phiên khác, nút Đăng xuất tất cả | | Pass | 11/15/2015 | |
| **FUNC-QLPDN-02** | Xóa phiên đăng nhập thành công | 1. Truy cập /admin/security/sessions<br>2. Click "Xóa phiên" trên một phiên<br>3. Click "Xác nhận xóa" trong Modal | Hiển thị thông báo "Xóa phiên thành công", phiên bị xóa khỏi danh sách, thiết bị bị đăng xuất, log bảo mật được ghi nhận | | Untested | 11/15/2015 | |
| **FUNC-QLPDN-03** | Hủy xóa phiên | 1. Truy cập /admin/security/sessions<br>2. Click "Xóa phiên"<br>3. Click "Hủy" trong Modal | Modal đóng, phiên không bị xóa | | Pass | 11/15/2015 | |
| **FUNC-QLPDN-04** | Đăng xuất tất cả thiết bị thành công | 1. Truy cập /admin/security/sessions<br>2. Click "Đăng xuất tất cả thiết bị"<br>3. Click "Xác nhận" trong Modal | Hiển thị thông báo "Đăng xuất tất cả thiết bị thành công", tất cả phiên (trừ phiên hiện tại) bị vô hiệu hóa, thông báo được gửi đến các thiết bị | | Untested | 11/15/2015 | |
| **FUNC-QLPDN-05** | Hủy đăng xuất tất cả | 1. Truy cập /admin/security/sessions<br>2. Click "Đăng xuất tất cả thiết bị"<br>3. Click "Hủy" trong Modal | Modal đóng, không có phiên nào bị vô hiệu hóa | | Pass | 11/15/2015 | |
| **FUNC-QLPDN-06** | Không thể xóa phiên hiện tại | 1. Truy cập /admin/security/sessions<br>2. Kiểm tra phiên hiện tại | Phiên hiện tại không có nút "Xóa phiên", chỉ hiển thị Badge "Phiên hiện tại" | | Pass | 11/15/2015 | |
| **FUNC-QLPDN-07** | Hiển thị khi không có phiên khác | 1. Truy cập /admin/security/sessions<br>2. Chỉ có phiên hiện tại | Hiển thị thông báo "Không có phiên đăng nhập nào khác", chỉ hiển thị Card Phiên hiện tại | | Pass | 11/15/2015 | |
| **FUNC-QLPDN-08** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/security/sessions<br>2. Click "Xóa phiên"<br>3. Tắt kết nối mạng<br>4. Click "Xác nhận xóa" | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", phiên không bị xóa | | Untested | 11/15/2015 | |
| **FUNC-QLPDN-09** | Xử lý khi server lỗi | 1. Truy cập /admin/security/sessions<br>2. Click "Xóa phiên"<br>3. Server trả về lỗi 500<br>4. Click "Xác nhận xóa" | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau", phiên không bị xóa | | Untested | 11/15/2015 | |

---

### Function: Phát hiện đăng nhập lạ

#### Check GUI: Phát hiện đăng nhập lạ

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-PHDNL-01** | Kiểm tra Badge đăng nhập lạ trong lịch sử | 1. Truy cập /admin/security/login-history<br>2. Kiểm tra Badge | Hiển thị Badge "Đăng nhập lạ" màu orange với icon AlertTriangle cho các đăng nhập từ thiết bị mới hoặc vị trí mới | | Pass | 11/15/2015 | |
| **GUI-PHDNL-02** | Kiểm tra thông báo cảnh báo | 1. Có đăng nhập lạ xảy ra<br>2. Kiểm tra thông báo | Hiển thị thông báo cảnh báo "Phát hiện đăng nhập lạ" với thông tin thiết bị, vị trí, thời gian | | Pass | 11/15/2015 | |
| **GUI-PHDNL-03** | Kiểm tra email cảnh báo | 1. Có đăng nhập lạ xảy ra<br>2. Kiểm tra email | Email cảnh báo được gửi với tiêu đề "Cảnh báo: Phát hiện đăng nhập lạ" | | Pass | 11/15/2015 | |

---

### Check FUNC: Phát hiện đăng nhập lạ

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-PHDNL-01** | Phát hiện đăng nhập từ thiết bị mới | 1. Đăng nhập từ thiết bị chưa từng sử dụng<br>2. Kiểm tra hệ thống | Hệ thống phát hiện và đánh dấu đăng nhập lạ, hiển thị Badge "Đăng nhập lạ" trong lịch sử, gửi thông báo qua email/SMS | | Untested | 11/15/2015 | |
| **FUNC-PHDNL-02** | Phát hiện đăng nhập từ vị trí mới | 1. Đăng nhập từ vị trí địa lý mới<br>2. Kiểm tra hệ thống | Hệ thống phát hiện và đánh dấu đăng nhập lạ, hiển thị Badge "Đăng nhập lạ" trong lịch sử, gửi thông báo qua email/SMS | | Untested | 11/15/2015 | |
| **FUNC-PHDNL-03** | Phát hiện đăng nhập từ IP mới | 1. Đăng nhập từ IP chưa từng sử dụng<br>2. Kiểm tra hệ thống | Hệ thống phát hiện và đánh dấu đăng nhập lạ, hiển thị Badge "Đăng nhập lạ" trong lịch sử, gửi thông báo qua email/SMS | | Untested | 11/15/2015 | |
| **FUNC-PHDNL-04** | Gửi thông báo email cảnh báo | 1. Có đăng nhập lạ xảy ra<br>2. Kiểm tra email | Email cảnh báo được gửi đến admin với thông tin: thiết bị, vị trí, IP, thời gian đăng nhập | | Untested | 11/15/2015 | |
| **FUNC-PHDNL-05** | Gửi thông báo SMS cảnh báo | 1. Có đăng nhập lạ xảy ra<br>2. Kiểm tra SMS | SMS cảnh báo được gửi đến số điện thoại admin với thông tin đăng nhập lạ | | Untested | 11/15/2015 | |
| **FUNC-PHDNL-06** | Không phát hiện đăng nhập từ thiết bị quen thuộc | 1. Đăng nhập từ thiết bị đã từng sử dụng<br>2. Kiểm tra hệ thống | Hệ thống không đánh dấu đăng nhập lạ, không gửi thông báo cảnh báo | | Pass | 11/15/2015 | |
| **FUNC-PHDNL-07** | Không phát hiện đăng nhập từ vị trí quen thuộc | 1. Đăng nhập từ vị trí đã từng sử dụng<br>2. Kiểm tra hệ thống | Hệ thống không đánh dấu đăng nhập lạ, không gửi thông báo cảnh báo | | Pass | 11/15/2015 | |

---

### Function: Auto logout khi hết hạn

#### Check GUI: Auto logout khi hết hạn

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-ALHT-01** | Kiểm tra thông báo cảnh báo trước khi hết hạn | 1. Phiên đăng nhập sắp hết hạn<br>2. Kiểm tra thông báo | Hiển thị thông báo cảnh báo "Phiên đăng nhập của bạn sắp hết hạn trong X phút" với nút "Gia hạn" | | Pass | 11/15/2015 | |
| **GUI-ALHT-02** | Kiểm tra Modal xác nhận auto logout | 1. Phiên đăng nhập hết hạn<br>2. Kiểm tra Modal | Hiển thị Modal "Phiên đăng nhập đã hết hạn" với nút "Đăng nhập lại" | | Pass | 11/15/2015 | |

---

### Check FUNC: Auto logout khi hết hạn

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-ALHT-01** | Cảnh báo trước khi hết hạn | 1. Phiên đăng nhập còn 5 phút<br>2. Kiểm tra hệ thống | Hiển thị thông báo cảnh báo "Phiên đăng nhập của bạn sắp hết hạn trong 5 phút" với nút "Gia hạn" | | Untested | 11/15/2015 | |
| **FUNC-ALHT-02** | Gia hạn phiên đăng nhập | 1. Click "Gia hạn" trong thông báo cảnh báo<br>2. Kiểm tra hệ thống | Phiên đăng nhập được gia hạn, thông báo cảnh báo biến mất, thời gian hết hạn được cập nhật | | Untested | 11/15/2015 | |
| **FUNC-ALHT-03** | Auto logout khi hết hạn | 1. Phiên đăng nhập hết hạn<br>2. Kiểm tra hệ thống | Hệ thống tự động đăng xuất, hiển thị Modal "Phiên đăng nhập đã hết hạn", redirect về trang đăng nhập | | Untested | 11/15/2015 | |
| **FUNC-ALHT-04** | Đăng nhập lại sau khi hết hạn | 1. Phiên đăng nhập hết hạn<br>2. Click "Đăng nhập lại"<br>3. Đăng nhập lại | Redirect về trang đăng nhập, có thể đăng nhập lại thành công | | Pass | 11/15/2015 | |
| **FUNC-ALHT-05** | Không gia hạn - phiên hết hạn | 1. Hiển thị thông báo cảnh báo<br>2. Không click "Gia hạn"<br>3. Chờ phiên hết hạn | Hệ thống tự động đăng xuất khi hết hạn, hiển thị Modal "Phiên đăng nhập đã hết hạn" | | Untested | 11/15/2015 | |
| **FUNC-ALHT-06** | Auto logout các phiên hết hạn trong quản lý phiên | 1. Truy cập /admin/security/sessions<br>2. Có phiên hết hạn<br>3. Kiểm tra danh sách | Các phiên hết hạn tự động bị xóa khỏi danh sách, chỉ hiển thị các phiên còn hiệu lực | | Untested | 11/15/2015 | |

---

### Function: Layout - Bảo mật

#### Check GUI: Layout - Bảo mật

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-LAYOUT-BM-01** | Kiểm tra Header | 1. Truy cập /admin/security<br>2. Kiểm tra Header | Hiển thị Header với logo, menu navigation, thông tin admin | | Pass | 11/15/2015 | |
| **GUI-LAYOUT-BM-02** | Kiểm tra Sidebar | 1. Truy cập /admin/security<br>2. Kiểm tra Sidebar | Hiển thị Sidebar với menu Admin, có item "Bảo mật" được highlight | | Pass | 11/15/2015 | |
| **GUI-LAYOUT-BM-03** | Kiểm tra Tabs | 1. Truy cập /admin/security<br>2. Kiểm tra Tabs | Hiển thị Tabs với các tab: Lịch sử đăng nhập, Quản lý phiên đăng nhập | | Pass | 11/15/2015 | |
| **GUI-LAYOUT-BM-04** | Kiểm tra Breadcrumb | 1. Truy cập /admin/security<br>2. Kiểm tra Breadcrumb | Hiển thị Breadcrumb: Trang chủ > Bảo mật | | Pass | 11/15/2015 | |
| **GUI-LAYOUT-BM-05** | Kiểm tra Footer | 1. Truy cập /admin/security<br>2. Kiểm tra Footer | Hiển thị Footer với thông tin copyright, liên kết | | Pass | 11/15/2015 | |
| **GUI-LAYOUT-BM-06** | Kiểm tra Responsive trên mobile | 1. Truy cập /admin/security trên mobile<br>2. Kiểm tra layout | Layout hiển thị đúng trên mobile, Sidebar có thể thu gọn, Table có thể scroll ngang | | Pass | 11/15/2015 | |
| **GUI-LAYOUT-BM-07** | Kiểm tra Responsive trên tablet | 1. Truy cập /admin/security trên tablet<br>2. Kiểm tra layout | Layout hiển thị đúng trên tablet, các thành phần được sắp xếp hợp lý | | Pass | 11/15/2015 | |

---

**Người tạo:** Testing Team  
**Ngày cập nhật:** 11/15/2015  
**Phiên bản:** 1.0

