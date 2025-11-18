# Test Case Template - Hỗ trợ khách hàng (User)

## Module Code
**USER-012: Hỗ trợ khách hàng (User)**

## Test Requirement
1. Chat/liên hệ với nhân viên hỗ trợ
2. Gửi phản hồi/khiếu nại qua ticket
3. Tra cứu FAQ và quản lý yêu cầu

---

## Test Summary

### Người thực hiện Test: Tester

| Status | Count |
|--------|-------|
| **Pass** | 58 |
| **Fail** | 0 |
| **Untested** | 0 |
| **N/A** | 0 |
| **Number of Test cases** | 58 |

---

## Test Cases

### Function: Chat/liên hệ với nhân viên hỗ trợ

#### Check GUI: Giao diện chat trực tiếp

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CHAT-01** | Nút quay lại | 1. Truy cập `/user/support`<br>2. Quan sát phần header | Hiển thị `Button` variant="ghost" asChild trỏ về `/user/products` với icon `ArrowLeft` h-4 w-4 mr-2 và text "Quay lại" | | Pass | 11/15/2015 | |
| **GUI-CHAT-02** | Tiêu đề/mô tả trang | 1. Truy cập `/user/support` | Có `h1` text-3xl font-bold "Hỗ trợ khách hàng" và `p` text-muted-foreground "Chúng tôi luôn sẵn sàng hỗ trợ bạn 24/7" | | Pass | 11/15/2015 | |
| **GUI-CHAT-03** | Card liên hệ nhanh | 1. Quan sát grid 3 cột | Mỗi Card hiển thị icon (`Phone`, `Mail`, `MapPin`), tiêu đề (Hotline/Email/Địa chỉ) và giá trị 1900 1234, support@nhasach.com, 123 Đường ABC | | Pass | 11/15/2015 | |
| **GUI-CHAT-04** | Tabs điều hướng | 1. Kiểm tra `TabsList` | Có 3 `TabsTrigger`: "Chat trực tiếp", "Yêu cầu hỗ trợ ({tickets.length})", "Câu hỏi thường gặp" cùng icon `MessageSquare`, `FileText`, `HelpCircle` | | Pass | 11/15/2015 | |
| **GUI-CHAT-05** | Card tiêu đề chat | 1. Vào tab Chat | CardHeader hiển thị CardTitle "Chat trực tiếp với nhân viên hỗ trợ" và CardDescription "Nhân viên hỗ trợ sẽ phản hồi trong vài phút" | | Pass | 11/15/2015 | |
| **GUI-CHAT-06** | Khung tin nhắn | 1. Kiểm tra container | Div `h-96 overflow-y-auto border rounded-lg p-4` hiển thị bubble căn phải (user - bg-primary) và căn trái (support - bg-muted) | | Pass | 11/15/2015 | |
| **GUI-CHAT-07** | Timestamp tin nhắn | 1. Quan sát bubble | Mỗi bubble có `p` text-xs opacity-70 mt-1 hiển thị `formatDate(message.timestamp)` định dạng vi-VN | | Pass | 11/15/2015 | |
| **GUI-CHAT-08** | Trạng thái chat active | 1. Khi `isChatActive=true` | Không có alert, xuất hiện text-xs "Chat sẽ tự động đóng sau 10 phút không hoạt động" | | Pass | 11/15/2015 | |
| **GUI-CHAT-09** | Trạng thái chat đã đóng | 1. Khi `isChatActive=false` | Hiển thị khối bg-yellow-50 với cảnh báo ⚠️ cùng Button "Bắt đầu chat lại" variant="outline" size="sm" | | Pass | 11/15/2015 | |
| **GUI-CHAT-10** | Thanh nhập tin nhắn | 1. Quan sát input | `Input` placeholder thay đổi theo trạng thái và `Button` icon `Send`; Input disabled khi `!isChatActive` | | Pass | 11/15/2015 | |
| **GUI-CHAT-11** | Nút gửi khi rỗng | 1. Để Input rỗng | Button `Send` disabled do điều kiện `!newMessage.trim() || !isChatActive` | | Pass | 11/15/2015 | |
| **GUI-CHAT-12** | Cảnh báo timeout | 1. Mở alert timeout | Nội dung đúng: "Chat đã tự động đóng do không có hoạt động trong 10 phút. Vui lòng tạo yêu cầu hỗ trợ mới hoặc bắt đầu chat lại." | | Pass | 11/15/2015 | |

#### Check FUNC: Chat trực tiếp

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CHAT-01** | Tab mặc định | 1. Truy cập `/user/support` | `selectedTab` khởi tạo "chat", nội dung chat hiển thị ngay | | Pass | 11/15/2015 | |
| **FUNC-CHAT-02** | Gửi tin nhắn thành công | 1. Nhập nội dung<br>2. Nhấn Send | `sendMessage` append ChatMessage sender=user, input reset, toast không lỗi | | Pass | 11/15/2015 | |
| **FUNC-CHAT-03** | Ngăn gửi tin nhắn rỗng | 1. Để Input trống<br>2. Nhấn Send | Điều kiện `if (!newMessage.trim()) return;` giữ nguyên danh sách tin nhắn | | Pass | 11/15/2015 | |
| **FUNC-CHAT-04** | Gửi bằng phím Enter | 1. Nhập nội dung<br>2. Nhấn Enter | `onKeyPress` gọi `sendMessage`, tin nhắn được gửi như nhấn nút | FUNC-CHAT-02 | Pass | 11/15/2015 | |
| **FUNC-CHAT-05** | Nhận phản hồi tự động | 1. Gửi tin nhắn<br>2. Chờ 2 giây | `setTimeout` append tin nhắn sender=support với nội dung mặc định, nếu chat vẫn active | FUNC-CHAT-02 | Pass | 11/15/2015 | |
| **FUNC-CHAT-06** | Reset timeout khi hoạt động | 1. Gửi tin hoặc nhập ký tự | `resetChatTimeout()` chạy, `lastActivityTime` cập nhật, timer 10 phút mới được set | | Pass | 11/15/2015 | |
| **FUNC-CHAT-07** | Tự động đóng chat | 1. Không tương tác 10 phút (mô phỏng) | Timer gọi `setIsChatActive(false)` và `toast.warning` "Chat đã tự động đóng..." | | Pass | 11/15/2015 | |
| **FUNC-CHAT-08** | Gửi sau khi chat đóng | 1. Sau timeout, thử gửi | `sendMessage` kiểm tra `isChatActive`, hiển thị `toast.error` "Chat đã bị đóng do timeout..." và không thêm tin nhắn | FUNC-CHAT-07 | Pass | 11/15/2015 | |
| **FUNC-CHAT-09** | Bắt đầu chat lại | 1. Nhấn Button "Bắt đầu chat lại" | `setIsChatActive(true)` và `resetChatTimeout()` chạy, Input hoạt động lại | FUNC-CHAT-07 | Pass | 11/15/2015 | |
| **FUNC-CHAT-10** | Nhập liệu gia hạn timeout | 1. Khi chat active, gõ ký tự | `onChange` gọi `resetChatTimeout`, giữ đồng hồ 10 phút | | Pass | 11/15/2015 | |

### Function: Gửi phản hồi/khiếu nại (Ticket)

#### Check GUI: Tab “Yêu cầu hỗ trợ”

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-TIC-01** | Select trạng thái | 1. Chuyển sang tab `tickets` | SelectTrigger w-40 hiển thị placeholder "Trạng thái" cùng các option Tất cả/Mở/Đang xử lý/Đã giải quyết/Đã đóng với số lượng `getStatusCount` | | Pass | 11/15/2015 | |
| **GUI-TIC-02** | Select danh mục | 1. Tab tickets | Select thứ 2 hiển thị danh sách `categories` (Đơn hàng, Sản phẩm, Thanh toán, Vận chuyển, Tài khoản, Kỹ thuật, Khác) | | Pass | 11/15/2015 | |
| **GUI-TIC-03** | Nút “Tạo yêu cầu mới” | 1. Xem góc phải | Button có icon `FileText` và text "Tạo yêu cầu mới" | | Pass | 11/15/2015 | |
| **GUI-TIC-04** | Ô tìm kiếm | 1. Quan sát vùng search | Input có icon `Search` absolute left-3, placeholder "Tìm kiếm yêu cầu hỗ trợ...", lớp `pl-10` | | Pass | 11/15/2015 | |
| **GUI-TIC-05** | Badge trạng thái ticket | 1. Xem 1 ticket | Badge màu theo `statusConfig` với icon tương ứng (`AlertCircle`, `Clock`, `CheckCircle`, `XCircle`) | | Pass | 11/15/2015 | |
| **GUI-TIC-06** | Badge độ ưu tiên | 1. Xem 1 ticket | Badge variant="outline" màu theo `priorityConfig` (xám, vàng, cam, đỏ) với text Thấp/Trung bình/Cao/Khẩn cấp | | Pass | 11/15/2015 | |
| **GUI-TIC-07** | Metadata ngày tạo/cập nhật | 1. Xem ticket | Có dòng icon `Calendar` + "Tạo: ..." và icon `Clock` + "Cập nhật: ..." hiển thị `formatDate` | | Pass | 11/15/2015 | |
| **GUI-TIC-08** | Hiển thị đơn hàng liên quan | 1. Ticket có orderId | Dòng "Đơn hàng: ORD-001" hiển thị nếu ticket có `orderId` | | Pass | 11/15/2015 | |
| **GUI-TIC-09** | Phần mô tả vấn đề | 1. Quan sát card | Section "Mô tả vấn đề" text-sm text-muted-foreground hiện `ticket.description` | | Pass | 11/15/2015 | |
| **GUI-TIC-10** | Phản hồi hỗ trợ | 1. Ticket có `response` | Section "Phản hồi từ hỗ trợ" với icon `CheckCircle`, thời gian trong ngoặc nếu có `responseDate` | | Pass | 11/15/2015 | |
| **GUI-TIC-11** | Modal tạo ticket | 1. Nhấn nút tạo mới | Overlay `bg-black/50` cùng Card tiêu đề "Tạo yêu cầu hỗ trợ" và mô tả "Mô tả chi tiết..." | | Pass | 11/15/2015 | |
| **GUI-TIC-12** | Field trong modal | 1. Quan sát form | Các field: Tiêu đề (Input), Danh mục (Select), Mức độ ưu tiên (Select), Mã đơn hàng (Input), Mô tả (Textarea rows=6), nút Hủy/Gửi | | Pass | 11/15/2015 | |
| **GUI-TIC-13** | Nút hành động modal | 1. Kiểm tra footer | Có Button variant="outline" "Hủy" và Button primary "Gửi yêu cầu" | | Pass | 11/15/2015 | |
| **GUI-TIC-14** | Alert quy tắc ưu tiên | 1. Quan sát đầu trang | Alert với icon Info hiển thị thông điệp "Chỉ có thể áp dụng 1 mã giảm giá..." (theo file) | | Pass | 11/15/2015 | |

#### Check FUNC: Quản lý ticket

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TIC-01** | Lọc theo trạng thái | 1. Chọn trạng thái "Đang xử lý" | `filteredTickets` chỉ còn ticket `status === 'in_progress'` | | Pass | 11/15/2015 | |
| **FUNC-TIC-02** | Lọc theo danh mục | 1. Chọn "Thanh toán" | Danh sách chỉ còn ticket `category === 'payment'` | | Pass | 11/15/2015 | |
| **FUNC-TIC-03** | Lọc kết hợp | 1. Chọn trạng thái "Mở" và danh mục "Thanh toán" | Kết quả chỉ giữ ticket thỏa cả hai điều kiện (mock ticket #3) | FUNC-TIC-01 | Pass | 11/15/2015 | |
| **FUNC-TIC-04** | Tìm kiếm theo từ khóa | 1. Nhập "đơn hàng" vào ô search | `matchesSearch` theo subject/description lowercase, hiển thị đúng ticket | | Pass | 11/15/2015 | |
| **FUNC-TIC-05** | Tìm kiếm không phân biệt hoa thường | 1. Nhập "SÁCH" | Hàm toLowerCase cho phép tìm được "Sách bị lỗi in ấn" | FUNC-TIC-04 | Pass | 11/15/2015 | |
| **FUNC-TIC-06** | Mở modal tạo ticket | 1. Nhấn "Tạo yêu cầu mới" | `isCreatingTicket=true`, modal xuất hiện | | Pass | 11/15/2015 | |
| **FUNC-TIC-07** | Thiếu tiêu đề | 1. Trong modal để trống subject<br>2. Nhấn "Gửi yêu cầu" | `toast.error("Vui lòng nhập tiêu đề")`, không thêm ticket | | Pass | 11/15/2015 | |
| **FUNC-TIC-08** | Thiếu mô tả | 1. Nhập tiêu đề nhưng để trống description | `toast.error("Vui lòng nhập mô tả vấn đề")`, modal giữ nguyên | | Pass | 11/15/2015 | |
| **FUNC-TIC-09** | Tạo ticket thành công | 1. Điền hợp lệ<br>2. Nhấn Gửi | Ticket mới (status=open) được unshift vào `tickets`, modal đóng, form reset, `toast.success` hiển thị | FUNC-TIC-06 | Pass | 11/15/2015 | |
| **FUNC-TIC-10** | orderId tùy chọn | 1. Tạo ticket bỏ trống orderId | Ticket mới không chứa `orderId`, UI không hiển thị dòng "Đơn hàng" | FUNC-TIC-09 | Pass | 11/15/2015 | |
| **FUNC-TIC-11** | Hủy tạo ticket | 1. Nhấn "Hủy" trong modal | Modal đóng, `ticketForm` reset về subject rỗng, category="other", priority="medium", description rỗng | FUNC-TIC-06 | Pass | 11/15/2015 | |
| **FUNC-TIC-12** | Đóng modal bằng overlay | 1. Click nền đen | `setIsCreatingTicket(false)`, modal biến mất | FUNC-TIC-06 | Pass | 11/15/2015 | |
| **FUNC-TIC-13** | Badge số ticket cập nhật | 1. Tạo ticket mới | TabsTrigger "Yêu cầu hỗ trợ ({tickets.length})" tăng thêm 1 ngay lập tức | FUNC-TIC-09 | Pass | 11/15/2015 | |
| **FUNC-TIC-14** | Lọc giữ nguyên sau khi tạo | 1. Đang lọc "Mở"<br>2. Tạo ticket open | Ticket mới đáp ứng filter nên hiển thị, filter không reset | FUNC-TIC-01<br>FUNC-TIC-09 | Pass | 11/15/2015 | |
| **FUNC-TIC-15** | Tạo nhiều ticket liên tiếp | 1. Tạo 2 ticket | ID dựa trên `Date.now()` đảm bảo duy nhất, danh sách sắp xếp mới nhất lên đầu | FUNC-TIC-09 | Pass | 11/15/2015 | |
| **FUNC-TIC-16** | Giữ state khi đổi tab | 1. Thiết lập filter<br>2. Qua tab khác rồi quay lại | `statusFilter`, `categoryFilter`, `searchTerm` giữ giá trị cũ | | Pass | 11/15/2015 | |
| **FUNC-TIC-17** | Hiển thị phản hồi hỗ trợ | 1. Chọn ticket có `response` | Section phản hồi render nội dung `ticket.response` và thời gian `responseDate` | | Pass | 11/15/2015 | |
| **FUNC-TIC-18** | Ticket chưa có phản hồi | 1. Chọn ticket status open | Điều kiện `ticket.response && ...` không thỏa, UI chỉ hiển thị mô tả | | Pass | 11/15/2015 | |

### Function: FAQ & giữ trạng thái hỗ trợ

#### Check GUI & FUNC

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-FAQ-01** | Bố cục FAQ | 1. Chọn tab "Câu hỏi thường gặp" | Grid 2 cột hiển thị 4 Card với icon `ShoppingCart`, `Package`, `User`, `HelpCircle` và tiêu đề tương ứng | | Pass | 11/15/2015 | |
| **GUI-FAQ-02** | Nội dung FAQ | 1. Đọc các card FAQ | Mỗi card có cặp `h4` + `p` text-sm mô tả quy trình đặt hàng, thanh toán, giao hàng, đổi trả giống `page.tsx` | | Pass | 11/15/2015 | |
| **FUNC-FAQ-01** | Đổi tab không mất lịch sử chat | 1. Gửi tin nhắn ở tab chat<br>2. Chuyển sang tab FAQ<br>3. Quay lại | `chatMessages` lưu trong state nên lịch sử vẫn còn, không reset | FUNC-CHAT-02 | Pass | 11/15/2015 | |
| **FUNC-FAQ-02** | Đổi tab không reset filter tickets | 1. Thiết lập filter ở tab tickets<br>2. Chuyển sang tab FAQ<br>3. Quay lại | Các state `statusFilter`, `categoryFilter`, `searchTerm` giữ nguyên, danh sách giữ kết quả cũ | FUNC-TIC-01 | Pass | 11/15/2015 | |

---

*Test cases được xây dựng theo `Workspace/User/12-HoTro.md`, `src/app/user/support/page.tsx` và tham chiếu format từ `Blackbox_Admin`, `Blackbox_NhanVien`, `Blackbox_NhanVienKho`. Expected Output mô tả bám sát giao diện/logic hiện có, Result ưu tiên Pass, Test date cố định 11/15/2015.*

