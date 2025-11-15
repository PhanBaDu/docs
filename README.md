# Test Case Template - Chức năng bảo mật (User)

## Module Code
**Model Management Store: Chức năng bảo mật User**

## Test Requirement
1. Khôi phục mật khẩu
2. Lịch sử đăng nhập
3. Xóa phiên đăng nhập

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

### Function: Khôi phục mật khẩu

#### Check GUI: Khôi phục mật khẩu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-KPMK-01** | Kiểm tra tiêu đề trang | 1. Truy cập /user/auth/forgot-password<br>2. Kiểm tra tiêu đề | Hiển thị CardTitle text-2xl font-bold "Quên mật khẩu" | | Pass | 11/15/2015 | |
| **GUI-KPMK-02** | Kiểm tra icon Mail | 1. Truy cập trang khôi phục<br>2. Kiểm tra icon | Hiển thị icon Mail h-6 w-6 text-primary trong div h-12 w-12 rounded-full bg-primary/10 | | Pass | 11/15/2015 | |
| **GUI-KPMK-03** | Kiểm tra mô tả chức năng | 1. Truy cập trang khôi phục<br>2. Kiểm tra mô tả | Hiển thị CardDescription "Nhập email của bạn để nhận link khôi phục mật khẩu" | | Pass | 11/15/2015 | |
| **GUI-KPMK-04** | Kiểm tra form khôi phục | 1. Truy cập trang khôi phục<br>2. Kiểm tra form | Hiển thị form với Label "Email", Input type="email" placeholder "Nhập email của bạn", required | | Pass | 11/15/2015 | |
| **GUI-KPMK-05** | Kiểm tra nút Gửi link khôi phục | 1. Truy cập trang khôi phục<br>2. Kiểm tra nút | Hiển thị nút "Gửi link khôi phục" type submit, className w-full, disabled khi isLoading | | Pass | 11/15/2015 | |
| **GUI-KPMK-06** | Kiểm tra nút Quay lại đăng nhập | 1. Truy cập trang khôi phục<br>2. Kiểm tra nút | Hiển thị link "Quay lại đăng nhập" với icon ArrowLeft h-4 w-4, href="/user/auth/login" | | Pass | 11/15/2015 | |
| **GUI-KPMK-07** | Kiểm tra card trạng thái gửi | 1. Gửi email thành công<br>2. Kiểm tra card | Hiển thị Card với CardHeader text-center, icon CheckCircle h-6 w-6 text-green-600 trong div bg-green-100, CardTitle "Email đã được gửi" | | Pass | 11/15/2015 | |
| **GUI-KPMK-08** | Kiểm tra thông báo gửi | 1. Gửi email thành công<br>2. Kiểm tra thông báo | Hiển thị CardDescription "Chúng tôi đã gửi link khôi phục mật khẩu đến email của bạn" | | Pass | 11/15/2015 | |
| **GUI-KPMK-09** | Kiểm tra hướng dẫn | 1. Gửi email thành công<br>2. Kiểm tra hướng dẫn | Hiển thị text-sm text-muted-foreground với hướng dẫn kiểm tra hộp thư và thư mục spam | | Pass | 11/15/2015 | |
| **GUI-KPMK-10** | Kiểm tra nút Gửi lại email | 1. Gửi email thành công<br>2. Kiểm tra nút | Hiển thị nút "Gửi lại email" variant outline className w-full | | Pass | 11/15/2015 | |
| **GUI-KPMK-11** | Kiểm tra nút Quay lại đăng nhập (sau khi gửi) | 1. Gửi email thành công<br>2. Kiểm tra nút | Hiển thị nút "Quay lại đăng nhập" với icon ArrowLeft h-4 w-4 mr-2, href="/user/auth/login" | | Pass | 11/15/2015 | |
| **GUI-KPMK-12** | Kiểm tra link Đăng ký | 1. Truy cập trang khôi phục<br>2. Kiểm tra link | Hiển thị text "Chưa có tài khoản?" với link "Đăng ký ngay" href="/user/auth/register" | | Pass | 11/15/2015 | |
| **GUI-KPMK-13** | Kiểm tra layout trang | 1. Truy cập trang khôi phục<br>2. Kiểm tra layout | Trang có min-h-screen flex items-center justify-center bg-gradient-to-br from-primary/5 to-secondary/5 p-4, Card w-full max-w-md | | Pass | 11/15/2015 | |

---

### Check FUNC: Khôi phục mật khẩu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-KPMK-01** | Gửi link khôi phục thành công | 1. Truy cập /user/auth/forgot-password<br>2. Nhập email hợp lệ<br>3. Nhấn "Gửi link khôi phục" | Email được gửi thành công, hiển thị card trạng thái gửi, toast "Email khôi phục mật khẩu đã được gửi!", token khôi phục được tạo và lưu trữ an toàn | | Pass | 11/15/2015 | |
| **FUNC-KPMK-02** | Gửi link với email trống | 1. Truy cập trang khôi phục<br>2. Để trống email<br>3. Nhấn "Gửi link khôi phục" | Hiển thị toast lỗi "Vui lòng nhập email", không gửi email | | Pass | 11/15/2015 | |
| **FUNC-KPMK-03** | Gửi link với email không tồn tại | 1. Nhập email không tồn tại trong hệ thống<br>2. Nhấn "Gửi link khôi phục" | Hệ thống kiểm tra và hiển thị thông báo lỗi "Email không tồn tại trong hệ thống" hoặc vẫn hiển thị thành công để bảo mật | | Pass | 11/15/2015 | |
| **FUNC-KPMK-04** | Gửi link với email không hợp lệ | 1. Nhập email không đúng định dạng<br>2. Nhấn "Gửi link khôi phục" | Input type="email" tự động validate, không cho phép submit nếu email không hợp lệ | | Pass | 11/15/2015 | |
| **FUNC-KPMK-05** | Tạo token khôi phục | 1. Gửi link khôi phục thành công<br>2. Kiểm tra token | Token khôi phục được tạo duy nhất, có thời hạn sử dụng (1 giờ), chỉ sử dụng một lần, được mã hóa và lưu trữ an toàn | | Pass | 11/15/2015 | |
| **FUNC-KPMK-06** | Chặn spam yêu cầu khôi phục | 1. Gửi nhiều yêu cầu khôi phục liên tiếp<br>2. Kiểm tra hệ thống | Hệ thống ghi lại thời gian yêu cầu, chặn yêu cầu quá thường xuyên, hiển thị thông báo "Vui lòng đợi trước khi gửi lại" | | Pass | 11/15/2015 | |
| **FUNC-KPMK-07** | Gửi lại email | 1. Gửi email thành công<br>2. Nhấn "Gửi lại email" | Email được gửi lại, token mới được tạo, thời gian hết hạn được reset | | Pass | 11/15/2015 | |
| **FUNC-KPMK-08** | Quay lại đăng nhập | 1. Nhấn link "Quay lại đăng nhập"<br>2. Kiểm tra điều hướng | Chuyển đến trang /user/auth/login | | Pass | 11/15/2015 | |
| **FUNC-KPMK-09** | Loading state khi gửi | 1. Nhập email<br>2. Nhấn "Gửi link khôi phục"<br>3. Kiểm tra loading | Nút hiển thị "Đang gửi..." và disabled trong khi gửi | | Pass | 11/15/2015 | |
| **FUNC-KPMK-10** | Xử lý lỗi khi gửi email | 1. Gửi email<br>2. Giả lập lỗi server<br>3. Kiểm tra xử lý | Hiển thị toast lỗi "Có lỗi xảy ra, vui lòng thử lại", không hiển thị card trạng thái gửi | | Pass | 11/15/2015 | |

---

### Function: Lịch sử đăng nhập

#### Check GUI: Lịch sử đăng nhập

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-LSDN-01** | Kiểm tra tiêu đề tab | 1. Truy cập tab "Lịch sử đăng nhập"<br>2. Kiểm tra tiêu đề | Hiển thị CardTitle "Lịch sử đăng nhập" với icon Clock h-5 w-5 | | Pass | 11/15/2015 | |
| **GUI-LSDN-02** | Kiểm tra mô tả chức năng | 1. Truy cập tab "Lịch sử đăng nhập"<br>2. Kiểm tra mô tả | Hiển thị CardDescription "Xem lịch sử đăng nhập gần đây" | | Pass | 11/15/2015 | |
| **GUI-LSDN-03** | Kiểm tra bộ lọc thời gian | 1. Truy cập tab "Lịch sử đăng nhập"<br>2. Kiểm tra bộ lọc | Hiển thị Select với Label "Thời gian", options: "Tất cả", "Tuần này", "Tháng này", "3 tháng gần đây" | | Pass | 11/15/2015 | |
| **GUI-LSDN-04** | Kiểm tra bộ lọc thiết bị | 1. Truy cập tab "Lịch sử đăng nhập"<br>2. Kiểm tra bộ lọc | Hiển thị Select với Label "Thiết bị", options: "Tất cả", "Desktop", "Mobile", "Tablet" | | Pass | 11/15/2015 | |
| **GUI-LSDN-05** | Kiểm tra bộ lọc trạng thái | 1. Truy cập tab "Lịch sử đăng nhập"<br>2. Kiểm tra bộ lọc | Hiển thị Select với Label "Trạng thái", options: "Tất cả", "Thành công", "Thất bại" | | Pass | 11/15/2015 | |
| **GUI-LSDN-06** | Kiểm tra card đăng nhập | 1. Xem danh sách lịch sử<br>2. Kiểm tra card | Hiển thị Card border-dashed với CardContent p-4 grid md:grid-cols-5 gap-2 text-sm | | Pass | 11/15/2015 | |
| **GUI-LSDN-07** | Kiểm tra thời gian đăng nhập | 1. Xem card đăng nhập<br>2. Kiểm tra thời gian | Hiển thị thời gian với font-medium, địa chỉ IP text-muted-foreground | | Pass | 11/15/2015 | |
| **GUI-LSDN-08** | Kiểm tra thiết bị và hệ điều hành | 1. Xem card đăng nhập<br>2. Kiểm tra thiết bị | Hiển thị tên thiết bị, hệ điều hành text-muted-foreground | | Pass | 11/15/2015 | |
| **GUI-LSDN-09** | Kiểm tra trình duyệt và vị trí | 1. Xem card đăng nhập<br>2. Kiểm tra trình duyệt | Hiển thị tên trình duyệt, vị trí text-muted-foreground | | Pass | 11/15/2015 | |
| **GUI-LSDN-10** | Kiểm tra badge trạng thái | 1. Xem card đăng nhập<br>2. Kiểm tra badge | Hiển thị Badge variant secondary nếu thành công, variant destructive nếu thất bại, text "Thành công" hoặc "Thất bại" | | Pass | 11/15/2015 | |
| **GUI-LSDN-11** | Kiểm tra lý do thất bại | 1. Xem đăng nhập thất bại<br>2. Kiểm tra lý do | Hiển thị lý do thất bại text-muted-foreground trong ngoặc đơn nếu có | | Pass | 11/15/2015 | |
| **GUI-LSDN-12** | Kiểm tra ID đăng nhập | 1. Xem card đăng nhập<br>2. Kiểm tra ID | Hiển thị ID text-right text-muted-foreground | | Pass | 11/15/2015 | |
| **GUI-LSDN-13** | Kiểm tra icon thiết bị | 1. Xem card đăng nhập<br>2. Kiểm tra icon | Hiển thị icon Smartphone nếu là mobile, icon Monitor nếu là desktop, h-5 w-5 text-muted-foreground | | Pass | 11/15/2015 | |
| **GUI-LSDN-14** | Kiểm tra badge Hiện tại | 1. Xem đăng nhập hiện tại<br>2. Kiểm tra badge | Hiển thị Badge variant default text "Hiện tại" nếu là phiên hiện tại | | Pass | 11/15/2015 | |
| **GUI-LSDN-15** | Kiểm tra icon trạng thái | 1. Xem card đăng nhập<br>2. Kiểm tra icon | Hiển thị icon CheckCircle nếu thành công, icon XCircle nếu thất bại, trong Badge | | Pass | 11/15/2015 | |
| **GUI-LSDN-16** | Kiểm tra phân trang | 1. Xem danh sách lịch sử<br>2. Kiểm tra phân trang | Hiển thị phân trang nếu có nhiều đăng nhập, có thể điều hướng giữa các trang | | Pass | 11/15/2015 | |

---

### Check FUNC: Lịch sử đăng nhập

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-LSDN-01** | Hiển thị lịch sử đăng nhập | 1. Truy cập tab "Lịch sử đăng nhập"<br>2. Xem danh sách | Hiển thị danh sách các lần đăng nhập với đầy đủ thông tin: thời gian, địa chỉ IP, thiết bị, hệ điều hành, trình duyệt, vị trí, trạng thái, lý do thất bại (nếu có) | | Pass | 11/15/2015 | |
| **FUNC-LSDN-02** | Lọc theo thời gian - Tất cả | 1. Chọn bộ lọc thời gian "Tất cả"<br>2. Xem danh sách | Hiển thị tất cả lịch sử đăng nhập không giới hạn thời gian | | Pass | 11/15/2015 | |
| **FUNC-LSDN-03** | Lọc theo thời gian - Tuần này | 1. Chọn bộ lọc thời gian "Tuần này"<br>2. Xem danh sách | Chỉ hiển thị các lần đăng nhập trong tuần này | | Pass | 11/15/2015 | |
| **FUNC-LSDN-04** | Lọc theo thời gian - Tháng này | 1. Chọn bộ lọc thời gian "Tháng này"<br>2. Xem danh sách | Chỉ hiển thị các lần đăng nhập trong tháng này | | Pass | 11/15/2015 | |
| **FUNC-LSDN-05** | Lọc theo thời gian - 3 tháng gần đây | 1. Chọn bộ lọc thời gian "3 tháng gần đây"<br>2. Xem danh sách | Chỉ hiển thị các lần đăng nhập trong 3 tháng gần đây | | Pass | 11/15/2015 | |
| **FUNC-LSDN-06** | Lọc theo thiết bị - Desktop | 1. Chọn bộ lọc thiết bị "Desktop"<br>2. Xem danh sách | Chỉ hiển thị các lần đăng nhập từ thiết bị Desktop | | Pass | 11/15/2015 | |
| **FUNC-LSDN-07** | Lọc theo thiết bị - Mobile | 1. Chọn bộ lọc thiết bị "Mobile"<br>2. Xem danh sách | Chỉ hiển thị các lần đăng nhập từ thiết bị Mobile | | Pass | 11/15/2015 | |
| **FUNC-LSDN-08** | Lọc theo thiết bị - Tablet | 1. Chọn bộ lọc thiết bị "Tablet"<br>2. Xem danh sách | Chỉ hiển thị các lần đăng nhập từ thiết bị Tablet | | Pass | 11/15/2015 | |
| **FUNC-LSDN-09** | Lọc theo trạng thái - Thành công | 1. Chọn bộ lọc trạng thái "Thành công"<br>2. Xem danh sách | Chỉ hiển thị các lần đăng nhập thành công | | Pass | 11/15/2015 | |
| **FUNC-LSDN-10** | Lọc theo trạng thái - Thất bại | 1. Chọn bộ lọc trạng thái "Thất bại"<br>2. Xem danh sách | Chỉ hiển thị các lần đăng nhập thất bại với lý do | | Pass | 11/15/2015 | |
| **FUNC-LSDN-11** | Kết hợp nhiều bộ lọc | 1. Chọn bộ lọc thời gian, thiết bị và trạng thái<br>2. Xem danh sách | Danh sách được lọc theo tất cả tiêu chí, chỉ hiển thị đăng nhập thỏa mãn tất cả điều kiện | | Pass | 11/15/2015 | |
| **FUNC-LSDN-12** | Phát hiện đăng nhập lạ | 1. Có đăng nhập từ thiết bị mới hoặc vị trí mới<br>2. Kiểm tra hệ thống | Hệ thống tự động phát hiện và đánh dấu đăng nhập lạ, gửi thông báo qua email/SMS để cảnh báo người dùng | | Pass | 11/15/2015 | |
| **FUNC-LSDN-13** | Sắp xếp theo thời gian mới nhất | 1. Xem danh sách lịch sử<br>2. Kiểm tra sắp xếp | Danh sách được sắp xếp theo thời gian đăng nhập mới nhất trước | | Pass | 11/15/2015 | |
| **FUNC-LSDN-14** | Hiển thị khi không có lịch sử | 1. Xem tài khoản không có lịch sử đăng nhập<br>2. Kiểm tra hiển thị | Hiển thị thông báo "Chưa có lịch sử đăng nhập" hoặc danh sách trống | | Pass | 11/15/2015 | |
| **FUNC-LSDN-15** | Cập nhật real-time | 1. Xem danh sách lịch sử<br>2. Có đăng nhập mới | Danh sách được cập nhật real-time, đăng nhập mới xuất hiện trong danh sách | | Pass | 11/15/2015 | |

---

### Function: Xóa phiên đăng nhập

#### Check GUI: Xóa phiên đăng nhập

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XPDN-01** | Kiểm tra tiêu đề tab | 1. Truy cập tab "Phiên đăng nhập"<br>2. Kiểm tra tiêu đề | Hiển thị CardTitle "Phiên đăng nhập hiện tại" với icon Globe h-5 w-5 | | Pass | 11/15/2015 | |
| **GUI-XPDN-02** | Kiểm tra mô tả chức năng | 1. Truy cập tab "Phiên đăng nhập"<br>2. Kiểm tra mô tả | Hiển thị CardDescription "Quản lý các phiên đăng nhập đang hoạt động" | | Pass | 11/15/2015 | |
| **GUI-XPDN-03** | Kiểm tra card phiên hiện tại | 1. Xem phiên đăng nhập<br>2. Kiểm tra card | Hiển thị card với flex items-center justify-between p-4 border rounded-lg | | Pass | 11/15/2015 | |
| **GUI-XPDN-04** | Kiểm tra thông tin thiết bị | 1. Xem card phiên<br>2. Kiểm tra thông tin | Hiển thị icon thiết bị, tên thiết bị font-medium, badge "Hiện tại" nếu là phiên hiện tại, browser và OS text-sm text-muted-foreground | | Pass | 11/15/2015 | |
| **GUI-XPDN-05** | Kiểm tra thông tin vị trí và IP | 1. Xem card phiên<br>2. Kiểm tra thông tin | Hiển thị vị trí với icon MapPin h-3 w-3, IP với icon Globe h-3 w-3, thời gian hoạt động với icon Clock h-3 w-3, text-xs text-muted-foreground | | Pass | 11/15/2015 | |
| **GUI-XPDN-06** | Kiểm tra nút Kết thúc | 1. Xem phiên không phải hiện tại<br>2. Kiểm tra nút | Hiển thị nút "Kết thúc" variant destructive size sm với icon Trash2 h-4 w-4, chỉ hiển thị cho phiên không phải hiện tại | | Pass | 11/15/2015 | |
| **GUI-XPDN-07** | Kiểm tra nút Đăng xuất tất cả | 1. Xem danh sách phiên<br>2. Kiểm tra nút | Hiển thị nút "Kết thúc tất cả" variant destructive với icon Trash2 h-4 w-4 mr-2 | | Pass | 11/15/2015 | |
| **GUI-XPDN-08** | Kiểm tra modal xác nhận | 1. Nhấn nút "Kết thúc"<br>2. Kiểm tra modal | Hiển thị modal với DialogTitle "Xác nhận xóa phiên đăng nhập", DialogDescription "Bạn có chắc chắn muốn xóa phiên đăng nhập này?", Card hiển thị thông tin phiên | | Pass | 11/15/2015 | |
| **GUI-XPDN-09** | Kiểm tra nút Xác nhận xóa | 1. Mở modal xác nhận<br>2. Kiểm tra nút | Hiển thị nút "Xác nhận xóa" variant destructive | | Pass | 11/15/2015 | |
| **GUI-XPDN-10** | Kiểm tra nút Hủy trong modal | 1. Mở modal xác nhận<br>2. Kiểm tra nút | Hiển thị nút "Hủy" variant outline | | Pass | 11/15/2015 | |

---

### Check FUNC: Xóa phiên đăng nhập

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XPDN-01** | Hiển thị phiên đăng nhập | 1. Truy cập tab "Phiên đăng nhập"<br>2. Xem danh sách | Hiển thị danh sách tất cả phiên đăng nhập đang hoạt động với đầy đủ thông tin: thiết bị, hệ điều hành, trình duyệt, vị trí, IP, thời gian hoạt động, trạng thái | | Pass | 11/15/2015 | |
| **FUNC-XPDN-02** | Xóa phiên đăng nhập | 1. Xem phiên không phải hiện tại<br>2. Nhấn nút "Kết thúc"<br>3. Xác nhận xóa | Hiển thị modal xác nhận với thông tin phiên, sau khi xác nhận, phiên được xóa, hiển thị toast "Đã kết thúc phiên đăng nhập", phiên biến mất khỏi danh sách, thiết bị được đăng xuất | | Pass | 11/15/2015 | |
| **FUNC-XPDN-03** | Hủy xóa phiên | 1. Nhấn nút "Kết thúc"<br>2. Nhấn nút "Hủy" trong modal | Modal đóng, không xóa phiên, phiên vẫn còn | | Pass | 11/15/2015 | |
| **FUNC-XPDN-04** | Đăng xuất tất cả thiết bị | 1. Nhấn nút "Kết thúc tất cả"<br>2. Xác nhận | Tất cả thiết bị khác được đăng xuất, chỉ còn phiên hiện tại, hiển thị toast "Đã kết thúc tất cả phiên đăng nhập khác", thông báo được gửi đến các thiết bị | | Pass | 11/15/2015 | |
| **FUNC-XPDN-05** | Không thể xóa phiên hiện tại | 1. Xem phiên hiện tại<br>2. Kiểm tra nút | Nút "Kết thúc" không hiển thị cho phiên hiện tại, chỉ hiển thị badge "Hiện tại" | | Pass | 11/15/2015 | |
| **FUNC-XPDN-06** | Cập nhật trạng thái phiên | 1. Xem danh sách phiên<br>2. Có phiên không hoạt động hoặc hết hạn | Trạng thái phiên được cập nhật, phiên không hoạt động hoặc hết hạn được đánh dấu, tự động đăng xuất (auto logout), cảnh báo trước khi hết hạn | | Pass | 11/15/2015 | |
| **FUNC-XPDN-07** | Sắp xếp theo thời gian hoạt động | 1. Xem danh sách phiên<br>2. Kiểm tra sắp xếp | Danh sách được sắp xếp theo thời gian hoạt động mới nhất trước | | Pass | 11/15/2015 | |
| **FUNC-XPDN-08** | Đóng modal bằng click overlay | 1. Mở modal xác nhận<br>2. Click vào overlay | Modal đóng, không xóa phiên | | Pass | 11/15/2015 | |
| **FUNC-XPDN-09** | Hiển thị khi không có phiên | 1. Xem tài khoản không có phiên đăng nhập<br>2. Kiểm tra hiển thị | Hiển thị thông báo "Chưa có phiên đăng nhập nào" hoặc danh sách trống | | Pass | 11/15/2015 | |
| **FUNC-XPDN-10** | Cảnh báo trước khi hết hạn | 1. Xem phiên sắp hết hạn<br>2. Kiểm tra cảnh báo | Hệ thống cảnh báo trước khi phiên hết hạn, hiển thị thông báo hoặc badge cảnh báo | | Pass | 11/15/2015 | |

---

### Check VALIDATION: Chức năng bảo mật

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **VALID-BM-01** | Khôi phục mật khẩu với email không hợp lệ | 1. Nhập email không đúng định dạng<br>2. Gửi link khôi phục | Input type="email" tự động validate, không cho phép submit, hiển thị thông báo lỗi trình duyệt | | Pass | 11/15/2015 | |
| **VALID-BM-02** | Khôi phục mật khẩu quá thường xuyên | 1. Gửi nhiều yêu cầu khôi phục liên tiếp<br>2. Kiểm tra hệ thống | Hệ thống chặn spam, hiển thị thông báo "Bạn đã gửi yêu cầu quá thường xuyên, vui lòng đợi X phút" | | Pass | 11/15/2015 | |
| **VALID-BM-03** | Token khôi phục hết hạn | 1. Sử dụng link khôi phục đã hết hạn<br>2. Kiểm tra xử lý | Hiển thị thông báo lỗi "Link khôi phục đã hết hạn, vui lòng yêu cầu lại" | | Pass | 11/15/2015 | |
| **VALID-BM-04** | Token khôi phục đã sử dụng | 1. Sử dụng link khôi phục đã được sử dụng<br>2. Kiểm tra xử lý | Hiển thị thông báo lỗi "Link khôi phục đã được sử dụng, vui lòng yêu cầu lại" | | Pass | 11/15/2015 | |
| **VALID-BM-05** | Xóa phiên với giá trị không hợp lệ | 1. Thử xóa phiên không tồn tại<br>2. Kiểm tra xử lý | Hệ thống xử lý an toàn, không gây lỗi, hiển thị thông báo "Phiên không tồn tại" | | Pass | 11/15/2015 | |
| **VALID-BM-06** | Lọc lịch sử với giá trị không hợp lệ | 1. Chọn bộ lọc với giá trị không hợp lệ<br>2. Kiểm tra kết quả | Hệ thống xử lý an toàn, không gây lỗi, hiển thị danh sách mặc định | | Pass | 11/15/2015 | |
| **VALID-BM-07** | Xem lịch sử khi chưa đăng nhập | 1. Chưa đăng nhập<br>2. Truy cập trang lịch sử | Yêu cầu đăng nhập, chuyển đến trang đăng nhập | | Pass | 11/15/2015 | |
| **VALID-BM-08** | Xem phiên đăng nhập khi chưa đăng nhập | 1. Chưa đăng nhập<br>2. Truy cập trang phiên đăng nhập | Yêu cầu đăng nhập, chuyển đến trang đăng nhập | | Pass | 11/15/2015 | |

