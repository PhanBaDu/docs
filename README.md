# Test Case Template - Chat hỗ trợ (Nhân viên)

## Module Code
**Giao lộ 19: Họcl6c (Nhân viên)**

## Test Requirement
1. Danh sách chat chờ xử lý
2. Chi tiết cuộc chat
3. Trả lời khách hàng / đánh dấu hoàn thành
4. Liên hệ & chuyển tiếp
5. Xử lý khiếu nại

---

## Test Summary

### Người lớp Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 38 |
| **Fail** | 0 |
| **Untested** | 0 |
| **N/A** | 0 |
| **Number of Test cases** | 38 |

---

## Test Cases

### Function: Danh sách chat chờ xử lý

#### Check GUI: Danh sách chat chờ xử lý

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CHAT-LIST-01** | Kiểm tra tiêu đề trang | 1. Đăng nhập Nhân viên<br>2. Truy cập `/nhanvien/support` | Hiển thị h1 `Chat hỗ trợ` class text-2xl font-bold và mô tả `Quản lý tin nhắn hỗ trợ đang chờ xử lý` class text-sm text-muted-foreground | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-CHAT-LIST-02** | Kiểm tra thống kê tổng quan | 1. Truy cập `/nhanvien/support`<br>2. Quan sát grid thống kê | Grid `grid-cols-2 md:grid-cols-4 gap-4` gồm 4 Card hiển thị `Tổng chat 45`, `Chờ xử lý 12`, `Đang xử lý 8`, `Đã hoàn thành 25` | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-CHAT-LIST-03** | Kiểm tra card Tìm kiếm & Bộ lọc | 1. Truy cập `/nhanvien/support`<br>2. Kiểm tra card | CardTitle `Tìm kiếm & Bộ lọc`, CardDescription `Tìm theo ID/tên/email/nội dung, lọc theo trạng thái & ưu tiên`, CardContent grid md:grid-cols-6 gap-3 chứa Input tìm kiếm, Select Trạng thái, Select Độ ưu tiên | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-CHAT-LIST-04** | Kiểm tra bảng danh sách chat | 1. Truy cập `/nhanvien/support`<br>2. Quan sát Card danh sách | CardTitle `Danh sách chat chờ xử lý`, CardDescription `Tổng quan các cuộc chat`, Table với TableHead: `ID chat`, `Khách hàng`, `Chủ đề`, `Tin nhắn cuối`, `Trạng thái`, `Thời gian`, `Nhân viên`, `Thao tác` | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-CHAT-LIST-05** | Kiểm tra cột Khách hàng | 1. Truy cập `/nhanvien/support`<br>2. Quan sát hàng #CHAT001 | TableCell chứa div text-sm font-medium (Tên), div text-xs text-muted-foreground `email • SĐT • Hạng` | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-CHAT-LIST-06** | Kiểm tra cột Thao tác | 1. Truy cập `/nhanvien/support` | Cột Thao tác hiển thị Button size=sm variant=outline `Xem` (Link `/nhanvien/support/CHAT001`) và Button size=sm `Trả lời` (Link `/nhanvien/support/CHAT001/reply`) | FUNC-DN-02 | Pass | 11/15/2015 | |

---

#### Check FUNC: Danh sách chat chờ xử lý

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CHAT-LIST-01** | Xem danh sách chat | 1. Đăng nhập<br>2. Truy cập `/nhanvien/support` | Trang hiển thị đầy đủ thống kê, bộ lọc, bảng chat. Mỗi hàng hiển thị Badge ID (#CHAT001), thông tin khách, chủ đề, tin nhắn cuối, trạng thái, thời gian, nhân viên, các nút thao tác | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-CHAT-LIST-02** | Tìm kiếm chat theo từ khóa | 1. Truy cập `/nhanvien/support`<br>2. Nhập `CHAT001` vào ô tìm kiếm | Bảng chỉ hiển thị chat có ID hoặc nội dung phù hợp với từ khóa, nếu không có hiển thị thông báo “Không tìm thấy chat” | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-CHAT-LIST-03** | Lọc chat theo trạng thái | 1. Truy cập `/nhanvien/support`<br>2. Chọn Trạng thái = `Chờ xử lý` | Bảng cập nhật, chỉ hiển thị chat có Badge `Chờ xử lý`, thống kê có thể cập nhật | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-CHAT-LIST-04** | Lọc chat theo độ ưu tiên | 1. Truy cập `/nhanvien/support`<br>2. Chọn Độ ưu tiên = `Cao` | Danh sách chat chỉ hiển thị các chat ưu tiên cao, Badge/ghi chú thể hiện mức ưu tiên, thao tác vẫn hoạt động | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-CHAT-LIST-05** | Xem chi tiết chat | 1. Truy cập `/nhanvien/support`<br>2. Click nút `Xem` | Điều hướng đến `/nhanvien/support/CHAT001`, hiển thị trang chi tiết | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-CHAT-LIST-06** | Mở trang trả lời chat | 1. Truy cập `/nhanvien/support`<br>2. Click nút `Trả lời` | Điều hướng đến `/nhanvien/support/CHAT001/reply`, hiển thị cửa sổ chat | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Chi tiết cuộc chat

#### Check GUI: Chi tiết chat `/nhanvien/support/CHAT001`

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CHAT-DETAIL-01** | Kiểm tra tiêu đề trang | 1. Mở `/nhanvien/support/CHAT001` | Tiêu đề `Chi tiết chat hỗ trợ #CHAT001` | FUNC-CHAT-LIST-05 | Pass | 11/15/2015 | |
| **GUI-CHAT-DETAIL-02** | Kiểm tra card Thông tin khách hàng | 1. Mở trang chi tiết | CardTitle `Thông tin khách hàng`, CardDescription, grid md:grid-cols-4 hiển thị Tên, Email, SĐT, Hạng (Badge), Lịch sử hỗ trợ trước | FUNC-CHAT-LIST-05 | Pass | 11/15/2015 | |
| **GUI-CHAT-DETAIL-03** | Kiểm tra card Cuộc hội thoại | 1. Mở trang chi tiết | CardTitle `Cuộc hội thoại`, CardContent hiển thị các bubble `[Khách]` (bg-muted) và `[Nhân viên]` (bg-primary/10) theo thời gian | FUNC-CHAT-LIST-05 | Pass | 11/15/2015 | |
| **GUI-CHAT-DETAIL-04** | Kiểm tra card Ghi chú & Ưu tiên | 1. Mở trang chi tiết | CardTitle `Ghi chú & Ưu tiên`, CardContent grid md:grid-cols-2, Textarea `Ghi chú nội bộ`, badges hiển thị độ ưu tiên, các Button `Trả lời chat`, `Đánh dấu hoàn thành`, `Chuyển tiếp / Escalate`, `Đóng chat` | FUNC-CHAT-LIST-05 | Pass | 11/15/2015 | |
| **GUI-CHAT-DETAIL-05** | Kiểm tra dialog chuyển tiếp | 1. Click `Chuyển tiếp / Escalate` | Dialog hiển thị Select `Chuyển đến *` với các option (Supervisor, Nhân viên B/C, Admin, Bộ phận kỹ thuật), Textarea `Lý do chuyển tiếp *`, Buttons `Hủy`, `Xác nhận chuyển tiếp` | FUNC-CHAT-LIST-05 | Pass | 11/15/2015 | |
| **GUI-CHAT-DETAIL-06** | Kiểm tra hiển thị lỗi | 1. Giả lập errorState | Alert variant destructive hiển thị (icon AlertCircle, mô tả lỗi) ở đầu trang | FUNC-CHAT-LIST-05 | Pass | 11/15/2015 | |

---

#### Check FUNC: Chi tiết cuộc chat

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CHAT-DETAIL-01** | Xem nội dung chat | 1. Truy cập `/nhanvien/support/CHAT001` | Lịch sử tin nhắn hiển thị đúng thứ tự thời gian, bubble khách/nhân viên rõ ràng | FUNC-CHAT-LIST-05 | Pass | 11/15/2015 | |
| **FUNC-CHAT-DETAIL-02** | Thêm ghi chú nội bộ | 1. Nhập ghi chú<br>2. Click `Ghi chú nội bộ` (nút `Thêm ghi chú`) | Ghi chú được lưu, hiển thị toast success, ghi log | FUNC-CHAT-DETAIL-01 | Pass | 11/15/2015 | |
| **FUNC-CHAT-DETAIL-03** | Đánh dấu hoàn thành | 1. Click `Đánh dấu hoàn thành` | Toast success “Đã đánh dấu hoàn thành”, trạng thái chat cập nhật, chat biến mất khỏi danh sách chờ xử lý | FUNC-CHAT-DETAIL-01 | Pass | 11/15/2015 | |
| **FUNC-CHAT-DETAIL-04** | Chuyển tiếp chat | 1. Click `Chuyển tiếp / Escalate`<br>2. Chọn người nhận, nhập lý do<br>3. `Xác nhận chuyển tiếp` | Nếu hợp lệ: hiển thị toast success `Đã chuyển tiếp chat đến ...`, dialog đóng, form reset. Nếu thiếu chọn/lý do: hiển thị toast error tương ứng | FUNC-CHAT-DETAIL-05 | Pass | 11/15/2015 | |
| **FUNC-CHAT-DETAIL-05** | Đóng chat | 1. Click `Đóng chat` | Toast success “Chat đã được đóng”, chat chuyển trạng thái `Đã đóng`, ghi lịch sử | FUNC-CHAT-DETAIL-01 | Pass | 11/15/2015 | |
| **FUNC-CHAT-DETAIL-06** | Truy cập trang reply | 1. Click `Trả lời chat` | Điều hướng `/nhanvien/support/CHAT001/reply` | FUNC-CHAT-DETAIL-01 | Pass | 11/15/2015 | |

---

### Function: Chat / trả lời khách hàng

#### Check GUI: Cửa sổ reply `/nhanvien/support/CHAT001/reply`

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CHAT-REPLY-01** | Kiểm tra tiêu đề trang | 1. Mở `/nhanvien/support/CHAT001/reply` | Tiêu đề `Chat hỗ trợ với Nguyễn Văn A` | FUNC-CHAT-DETAIL-06 | Pass | 11/15/2015 | |
| **GUI-CHAT-REPLY-02** | Kiểm tra card Cửa sổ trò chuyện | 1. Quan sát card đầu | CardTitle `Cửa sổ trò chuyện`, CardDescription, CardContent hiển thị `div space-y-2 text-sm max-h-80 overflow-auto border rounded p-3` chứa lịch sử tin nhắn (bubble) | FUNC-CHAT-DETAIL-06 | Pass | 11/15/2015 | |
| **GUI-CHAT-REPLY-03** | Kiểm tra khu nhập tin nhắn | 1. Quan sát grid `Tin nhắn mới` | Textarea rows=4 placeholder `Nhập nội dung tin nhắn...`, Select `Mẫu tin nhắn` với các option (welcome, thanks, guide, sorry), Button `Áp dụng mẫu` | FUNC-CHAT-DETAIL-06 | Pass | 11/15/2015 | |
| **GUI-CHAT-REPLY-04** | Kiểm tra nhóm nút hành động | 1. Quan sát phần cuối card | Các Button: `Gửi tin nhắn`, `Gửi tệp đính kèm`, `Thêm ghi chú` | FUNC-CHAT-DETAIL-06 | Pass | 11/15/2015 | |
| **GUI-CHAT-REPLY-05** | Kiểm tra card Đánh dấu chat đã xử lý | 1. Quan sát card thứ hai | CardTitle `Đánh dấu chat đã xử lý`, CardDescription `Chọn lý do và xác nhận`, grid md:grid-cols-3: Select `Lý do hoàn thành`, Select `Gửi tin nhắn cảm ơn`, Textarea `Ghi chú`, Button `Đánh dấu hoàn thành`, Button `Đóng chat` | FUNC-CHAT-DETAIL-06 | Pass | 11/15/2015 | |

---

#### Check FUNC: Chat / trả lời khách hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CHAT-REPLY-01** | Gửi tin nhắn thủ công | 1. Vào `/nhanvien/support/CHAT001/reply`<br>2. Nhập nội dung<br>3. Click `Gửi tin nhắn` | Tin nhắn được gửi, hiển thị toast success, bubble `[Nhân viên]` mới xuất hiện, khách hàng nhận được tin nhắn trong real-time | FUNC-CHAT-DETAIL-06 | Pass | 11/15/2015 | |
| **FUNC-CHAT-REPLY-02** | Sử dụng mẫu tin nhắn | 1. Chọn mẫu `Xin chào...`<br>2. Click `Áp dụng mẫu`<br>3. Gửi | Textarea được điền sẵn nội dung mẫu, tin nhắn gửi với nội dung đó, hiển thị log “Sử dụng mẫu tin nhắn” | FUNC-CHAT-DETAIL-06 | Pass | 11/15/2015 | |
| **FUNC-CHAT-REPLY-03** | Gửi tệp đính kèm | 1. Click `Gửi tệp đính kèm`<br>2. Chọn file | File được upload (modal/preview), gửi kèm tin nhắn, hiển thị thông báo thành công | FUNC-CHAT-DETAIL-06 | Pass | 11/15/2015 | |
| **FUNC-CHAT-REPLY-04** | Thêm ghi chú nhanh | 1. Click `Thêm ghi chú`<br>2. Nhập nội dung | Ghi chú lưu vào hệ thống, hiển thị confirm message | FUNC-CHAT-DETAIL-06 | Pass | 11/15/2015 | |
| **FUNC-CHAT-REPLY-05** | Đánh dấu hoàn thành (từ reply) | 1. Trong card “Đánh dấu chat đã xử lý”, chọn Lý do + Gửi tin nhắn cảm ơn `Có`<br>2. Nhập ghi chú<br>3. Click `Đánh dấu hoàn thành` | Chat chuyển trạng thái `Đã hoàn thành`, tin nhắn cảm ơn tự động gửi, hiển thị toast success | FUNC-CHAT-DETAIL-06 | Pass | 11/15/2015 | |
| **FUNC-CHAT-REPLY-06** | Đóng chat không gửi cảm ơn | 1. Chọn Gửi tin nhắn cảm ơn = `Không`<br>2. Click `Đóng chat` | Chat chuyển trạng thái `Đã đóng`, không gửi tin nhắn cảm ơn, hiển thị toast success | FUNC-CHAT-DETAIL-06 | Pass | 11/15/2015 | |

---

### Function: Liên hệ & chuyển tiếp (contact, escalate)

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CHAT-CONTACT-01** | Liên hệ khách hàng qua điện thoại | 1. Từ trang chi tiết, click `Liên hệ khách hàng` (nếu có) hoặc truy cập `/nhanvien/returns/RT-001/contact` (đối với đổi trả) *hoặc* dùng khối Gọi điện (nếu UI chat có) | Nhập thời gian gọi, ghi chú, chọn kết quả. Sau khi `Xác nhận gọi`: lịch sử liên hệ bổ sung dòng “Gọi điện thoại ... Thành công”, trạng thái chat cập nhật `Đã liên hệ` | FUNC-CHAT-DETAIL-01 | Pass | 11/15/2015 | |
| **FUNC-CHAT-CONTACT-02** | Gửi email hỗ trợ | 1. Tại contact card `Gửi email`<br>2. Nhập tiêu đề, nội dung<br>3. Click `Gửi email` | Email gửi thành công, ghi lại lịch sử liên hệ `Gửi email • ... • Thành công`, khách hàng nhận mail | FUNC-CHAT-DETAIL-01 | Pass | 11/15/2015 | |
| **FUNC-CHAT-CONTACT-03** | Gửi SMS thông báo | 1. Nhập nội dung SMS<br>2. Click `Gửi SMS` | Tin nhắn gửi thành công, log trong lịch sử, trạng thái có thể cập nhật | FUNC-CHAT-DETAIL-01 | Pass | 11/15/2015 | |
| **FUNC-CHAT-CONTACT-04** | Gửi tin nhắn chat mẫu từ contact | 1. Chọn tin nhắn mẫu (Chat trực tuyến section)<br>2. Click `Mở chat` & `Gửi tin nhắn` | Cửa sổ chat mở, tin nhắn được gửi, hiển thị confirm | FUNC-CHAT-DETAIL-01 | Pass | 11/15/2015 | |
| **FUNC-CHAT-CONTACT-05** | Cập nhật trạng thái từ contact | 1. Click `Đã liên hệ` (card `Cập nhật trạng thái yêu cầu`) | Trạng thái chat đổi sang tương ứng, hiển thị toast success, timeline bổ sung | FUNC-CHAT-DETAIL-01 | Pass | 11/15/2015 | |
| **FUNC-CHAT-CONTACT-06** | Chuyển tiếp chat (escalate) | 1. Trên trang chi tiết chat, mở dialog `Chuyển tiếp / Escalate`<br>2. Chọn người nhận & lý do<br>3. `Xác nhận chuyển tiếp` | Chat gán cho nhân sự mới, log “Chuyển tiếp chat đến …”, toast success. Nếu thiếu dữ liệu hiển thị toast error | FUNC-CHAT-DETAIL-04 | Pass | 11/15/2015 | |

---

### Function: Xử lý khiếu nại (Modal escalate cao)

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CHAT-KN-01** | Tiếp nhận khiếu nại từ chat | 1. Khi phát hiện khiếu nại (ví dụ trong chat), mở modal “Xử lý khiếu nại” (theo tài liệu) hoặc quy trình escalate | Modal hiển thị thông tin khiếu nại, loại khiếu nại (Radio), mức độ nghiêm trọng, trạng thái xử lý, nội dung chi tiết, kế hoạch xử lý, người chịu trách nhiệm, thời hạn, checkbox thông báo khách hàng, Buttons `Hủy`/`Lưu` | FUNC-CHAT-DETAIL-04 | Pass | 11/15/2015 | |
| **FUNC-CHAT-KN-02** | Lưu kế hoạch xử lý khiếu nại | 1. Điền đầy đủ thông tin trong modal<br>2. Click `Lưu` | Thông tin khiếu nại được lưu, chat gắn cờ “Khiếu nại”, hiển thị toast success, timeline cập nhật, khách hàng được thông báo nếu checkbox | FUNC-CHAT-KN-01 | Pass | 11/15/2015 | |
| **FUNC-CHAT-KN-03** | Cập nhật tiến độ khiếu nại | 1. Mở modal xử lý<br>2. Đổi trạng thái `Đang điều tra` → `Đã giải quyết`<br>3. Thêm ghi chú | Tiến độ cập nhật, timeline ghi nhận, khách hàng nhận thông báo (nếu bật), hiển thị confirm message | FUNC-CHAT-KN-01 | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn MDX để dễ dàng quản lý và cập nhật test cases.*

