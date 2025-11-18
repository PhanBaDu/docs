# Test Case Template - Hỗ trợ khách hàng (Admin)

## Module Code
**Giao lộ 19: Họcl6c (Admin)**

## Test Requirement
1. Hiển thị danh sách yêu cầu hỗ trợ
2. Chat hỗ trợ khách hàng
3. Trả lời yêu cầu hỗ trợ

---

## Test Summary

### Người lớp Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 18 |
| **Fail** | 0 |
| **Untested** | 0 |
| **N/A** | 0 |
| **Number of Test cases** | 18 |

---

## Test Cases

### Function: Hiển thị danh sách yêu cầu hỗ trợ

#### Check GUI: Hiển thị danh sách yêu cầu hỗ trợ

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DSHT-01** | Kiểm tra tiêu đề trang | 1. Đăng nhập Admin<br>2. Truy cập /admin/support<br>3. Kiểm tra tiêu đề | Hiển thị tiêu đề "Danh sách tin nhắn hỗ trợ" với class text-3xl font-bold, mô tả "Quản lý các cuộc hội thoại hỗ trợ với khách hàng" với class text-muted-foreground, nằm trong div flex items-center justify-between | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSHT-02** | Kiểm tra nút header | 1. Đăng nhập Admin<br>2. Truy cập /admin/support<br>3. Kiểm tra nút | Hiển thị div flex gap-2 bên phải tiêu đề với Button "Đánh dấu tất cả đã đọc" onClick | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSHT-03** | Kiểm tra thống kê hỗ trợ | 1. Đăng nhập Admin<br>2. Truy cập /admin/support<br>3. Kiểm tra thống kê | Hiển thị grid grid-cols-1 md:grid-cols-2 lg:grid-cols-6 gap-4 với 6 Card: Card 1 "Tổng ticket" với icon MessageSquare h-4 w-4 text-muted-foreground, Card 2 "Mới" với icon Clock h-4 w-4 text-blue-600 và số text-blue-600, Card 3 "Đang xử lý" với icon AlertCircle h-4 w-4 text-orange-600 và số text-orange-600, Card 4 "Đã giải quyết" với icon CheckCircle h-4 w-4 text-green-600 và số text-green-600, Card 5 "Đóng" với icon XCircle h-4 w-4 text-gray-600 và số text-gray-600, Card 6 "Chưa đọc" với icon MessageSquare h-4 w-4 text-red-600 và số text-red-600. Mỗi card có CardHeader flex flex-row items-center justify-between space-y-0 pb-2 với CardTitle text-sm font-medium và icon, CardContent có text-2xl font-bold | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSHT-04** | Kiểm tra card Bộ lọc | 1. Đăng nhập Admin<br>2. Truy cập /admin/support<br>3. Kiểm tra card bộ lọc | Hiển thị Card với CardHeader có CardTitle "Bộ lọc", CardContent có grid grid-cols-2 md:grid-cols-3 lg:grid-cols-6 gap-4 chứa: div space-y-2 với Label "Tìm kiếm" và Input với icon Search absolute left-2 top-2.5, placeholder="Tìm theo mã, tên khách, SĐT...", class pl-8, Select "Trạng thái" với placeholder="Chọn trạng thái", Select "Ưu tiên" với placeholder="Chọn mức ưu tiên", Button "Áp dụng bộ lọc" onClick | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSHT-05** | Kiểm tra dropdown Trạng thái | 1. Đăng nhập Admin<br>2. Truy cập /admin/support<br>3. Kiểm tra dropdown | Hiển thị Select với SelectTrigger, SelectValue placeholder="Chọn trạng thái", SelectContent có các option: "Tất cả", "Mới", "Đang xử lý", "Đã giải quyết", "Đóng" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSHT-06** | Kiểm tra dropdown Ưu tiên | 1. Đăng nhập Admin<br>2. Truy cập /admin/support<br>3. Kiểm tra dropdown | Hiển thị Select với SelectTrigger, SelectValue placeholder="Chọn mức ưu tiên", SelectContent có các option: "Tất cả", "Thấp", "Trung bình", "Cao" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSHT-07** | Kiểm tra card Danh sách hội thoại | 1. Đăng nhập Admin<br>2. Truy cập /admin/support<br>3. Kiểm tra card | Hiển thị Card với CardHeader có CardTitle "Danh sách hội thoại hỗ trợ", CardDescription "Hiển thị [số] cuộc hội thoại", CardContent có div space-y-4 chứa danh sách các ticket | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSHT-08** | Kiểm tra item hội thoại | 1. Đăng nhập Admin<br>2. Truy cập /admin/support<br>3. Kiểm tra item | Mỗi item có div flex items-center gap-4 p-4 border rounded-lg hover:bg-gray-50 chứa: Avatar h-12 w-12 với AvatarImage và AvatarFallback (chữ cái đầu tên), div flex-1 min-w-0 với h3 font-semibold truncate (tên khách hàng), các Badge (trạng thái với màu tương ứng, ưu tiên với màu tương ứng, "X tin nhắn mới" variant="destructive" nếu unreadCount > 0), p text-sm font-medium text-gray-900 (subject), p text-sm text-gray-600 (lastMessage), div flex items-center gap-4 text-xs text-gray-500 với icon User + assignedStaff, icon Clock + lastUpdate, icon Phone + customerPhone, icon Mail + customerEmail, div flex items-center gap-2 với Button "Xem chi tiết" và Button "Đánh dấu đã đọc" (nếu unreadCount > 0) | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Hiển thị danh sách yêu cầu hỗ trợ

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DSHT-01** | Xem danh sách yêu cầu hỗ trợ | 1. Đăng nhập Admin<br>2. Truy cập /admin/support | Hiển thị đầy đủ: tiêu đề và mô tả, nút "Đánh dấu tất cả đã đọc", thống kê 6 card (Tổng ticket, Mới, Đang xử lý, Đã giải quyết, Đóng, Chưa đọc) với số liệu và icon màu tương ứng, card Bộ lọc với ô tìm kiếm (có icon Search), 2 dropdown (Trạng thái, Ưu tiên), nút "Áp dụng bộ lọc", card Danh sách hội thoại hỗ trợ với danh sách các ticket, mỗi ticket có Avatar, tên khách hàng, Badge trạng thái (màu tương ứng), Badge ưu tiên (màu tương ứng), Badge "X tin nhắn mới" (nếu có), subject, lastMessage, thông tin assignedStaff, lastUpdate, customerPhone, customerEmail, các nút thao tác | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSHT-02** | Tìm kiếm yêu cầu hỗ trợ | 1. Đăng nhập Admin<br>2. Truy cập /admin/support<br>3. Nhập từ khóa tìm kiếm vào ô "Tìm theo mã, tên khách, SĐT..."<br>4. Nhấn Enter hoặc click nút "Áp dụng bộ lọc" | Danh sách ticket được lọc theo từ khóa (mã ticket, tên khách hàng, số điện thoại, subject), danh sách cập nhật với các ticket phù hợp, CardDescription được cập nhật "Hiển thị [số] cuộc hội thoại" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSHT-03** | Lọc yêu cầu hỗ trợ theo trạng thái | 1. Đăng nhập Admin<br>2. Truy cập /admin/support<br>3. Chọn trạng thái từ dropdown (VD: "Mới")<br>4. Click nút "Áp dụng bộ lọc" | Danh sách ticket được lọc theo trạng thái đã chọn, danh sách chỉ hiển thị ticket có trạng thái tương ứng, CardDescription được cập nhật | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSHT-04** | Lọc yêu cầu hỗ trợ theo ưu tiên | 1. Đăng nhập Admin<br>2. Truy cập /admin/support<br>3. Chọn ưu tiên từ dropdown (VD: "Cao")<br>4. Click nút "Áp dụng bộ lọc" | Danh sách ticket được lọc theo ưu tiên đã chọn, danh sách chỉ hiển thị ticket có ưu tiên tương ứng, CardDescription được cập nhật | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSHT-05** | Kết hợp nhiều bộ lọc | 1. Đăng nhập Admin<br>2. Truy cập /admin/support<br>3. Chọn trạng thái "Mới"<br>4. Chọn ưu tiên "Cao"<br>5. Nhập từ khóa tìm kiếm<br>6. Click nút "Áp dụng bộ lọc" | Danh sách ticket được lọc theo tất cả các tiêu chí đã chọn, danh sách chỉ hiển thị ticket thỏa mãn tất cả điều kiện, CardDescription được cập nhật | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSHT-06** | Đánh dấu tất cả đã đọc | 1. Đăng nhập Admin<br>2. Truy cập /admin/support<br>3. Click nút "Đánh dấu tất cả đã đọc" | Hiển thị thông báo thành công "Đã đánh dấu ticket all là đã đọc" (toast success), tất cả Badge "X tin nhắn mới" biến mất, số "Chưa đọc" trong thống kê về 0, các nút "Đánh dấu đã đọc" biến mất | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSHT-07** | Đánh dấu một ticket đã đọc | 1. Đăng nhập Admin<br>2. Truy cập /admin/support<br>3. Click nút "Đánh dấu đã đọc" trên một ticket có unreadCount > 0 | Hiển thị thông báo thành công "Đã đánh dấu ticket [id] là đã đọc" (toast success), Badge "X tin nhắn mới" biến mất trên ticket đó, nút "Đánh dấu đã đọc" biến mất, số "Chưa đọc" trong thống kê giảm đi số lượng tương ứng | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Chat hỗ trợ khách hàng

#### Check GUI: Chat hỗ trợ

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CHAT-01** | Kiểm tra tiêu đề trang | 1. Đăng nhập Admin<br>2. Truy cập /admin/support/tickets/[id]<br>3. Kiểm tra tiêu đề | Hiển thị tiêu đề "Chat hỗ trợ - [Mã ticket]" hoặc "Chat hỗ trợ - ST001" với class text-2xl font-bold, layout tương tự trang chi tiết | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-CHAT-02** | Kiểm tra giao diện chat | 1. Đăng nhập Admin<br>2. Truy cập /admin/support/tickets/[id]<br>3. Kiểm tra giao diện | Hiển thị Card với CardHeader có CardTitle "Chat hỗ trợ với [Tên khách hàng]", CardContent có div flex flex-col h-[600px] chứa: div flex-1 overflow-y-auto space-y-4 (khung chat với danh sách tin nhắn), div flex items-center gap-2 p-4 border-t (ô nhập tin nhắn với Input và Button "Gửi" có icon Send) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-CHAT-03** | Kiểm tra thông tin khách hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/support/tickets/[id]<br>3. Kiểm tra thông tin | Hiển thị Card với CardHeader có CardTitle "Thông tin khách hàng", CardContent hiển thị các trường: Avatar, Tên khách hàng, Email, Số điện thoại, Link đến trang chi tiết khách hàng | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Chat hỗ trợ khách hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CHAT-01** | Mở chat hỗ trợ | 1. Đăng nhập Admin<br>2. Truy cập /admin/support<br>3. Click nút "Xem chi tiết" trên một ticket | Hiển thị thông báo "Chuyển đến chi tiết ticket [id]" (toast success), chuyển đến trang /admin/support/tickets/[id], hiển thị giao diện chat với: tiêu đề "Chat hỗ trợ - [Mã ticket]", card Thông tin khách hàng, card Chat với lịch sử tin nhắn (nếu có), ô nhập tin nhắn, nút "Gửi" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-CHAT-02** | Gửi tin nhắn | 1. Đăng nhập Admin<br>2. Truy cập /admin/support/tickets/[id]<br>3. Nhập tin nhắn vào Input<br>4. Click nút "Gửi" hoặc nhấn Enter | Tin nhắn được gửi thành công, hiển thị trong khung chat với format: div flex justify-end (tin nhắn của Admin), div p-3 rounded-lg bg-primary text-primary-foreground (nội dung tin nhắn), span text-xs text-muted-foreground (thời gian gửi), tin nhắn được lưu vào database, thông báo được gửi cho khách hàng qua email/SMS (nếu có cấu hình), trạng thái ticket có thể cập nhật thành "Đang xử lý" nếu đang là "Mới" | FUNC-DN-02, FUNC-CHAT-01 | Pass | 11/15/2015 | |
| **FUNC-CHAT-03** | Gửi tin nhắn rỗng | 1. Đăng nhập Admin<br>2. Truy cập /admin/support/tickets/[id]<br>3. Để trống ô nhập tin nhắn<br>4. Click nút "Gửi" | Hiển thị thông báo cảnh báo "Vui lòng nhập tin nhắn" (toast warning), không gửi tin nhắn, ô nhập vẫn trống | FUNC-DN-02, FUNC-CHAT-01 | Pass | 11/15/2015 | |
| **FUNC-CHAT-04** | Nhận tin nhắn từ khách hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/support/tickets/[id]<br>3. Chờ tin nhắn từ khách hàng (hoặc giả lập) | Tin nhắn mới từ khách hàng hiển thị trong khung chat với format: div flex justify-start (tin nhắn của khách hàng), div p-3 rounded-lg bg-muted (nội dung tin nhắn), span text-xs text-muted-foreground (thời gian gửi), có thể có thông báo (notification) hoặc badge "Tin nhắn mới", unreadCount tăng lên, khung chat tự động scroll xuống tin nhắn mới nhất | FUNC-DN-02, FUNC-CHAT-01 | Pass | 11/15/2015 | |
| **FUNC-CHAT-05** | Xem lịch sử tin nhắn | 1. Đăng nhập Admin<br>2. Truy cập /admin/support/tickets/[id]<br>3. Xem khung chat | Hiển thị lịch sử tin nhắn theo dòng thời gian từ cũ đến mới, mỗi tin nhắn có: người gửi (Admin hoặc Khách hàng), nội dung, thời gian gửi, tin nhắn của Admin hiển thị bên phải (justify-end) với màu primary, tin nhắn của khách hàng hiển thị bên trái (justify-start) với màu muted | FUNC-DN-02, FUNC-CHAT-01 | Pass | 11/15/2015 | |

---

### Function: Trả lời yêu cầu hỗ trợ

#### Check FUNC: Trả lời yêu cầu hỗ trợ

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TLHT-01** | Trả lời yêu cầu hỗ trợ | 1. Đăng nhập Admin<br>2. Truy cập /admin/support/tickets/[id]<br>3. Nhập câu trả lời vào ô nhập tin nhắn<br>4. Click nút "Gửi" | Câu trả lời được gửi thành công, hiển thị trong khung chat, trạng thái ticket được cập nhật (từ "Mới" thành "Đang xử lý" hoặc từ "Đang xử lý" thành "Đã giải quyết" nếu câu trả lời giải quyết vấn đề), thông báo được gửi cho khách hàng qua email/SMS về việc có phản hồi mới, lịch sử ticket được ghi nhận, unreadCount của khách hàng tăng lên | FUNC-DN-02, FUNC-CHAT-01 | Pass | 11/15/2015 | |
| **FUNC-TLHT-02** | Đánh dấu ticket đã giải quyết | 1. Đăng nhập Admin<br>2. Truy cập /admin/support/tickets/[id]<br>3. Click nút "Đánh dấu đã giải quyết" hoặc chọn trạng thái "Đã giải quyết"<br>4. Xác nhận | Trạng thái ticket được cập nhật thành "Đã giải quyết", hiển thị thông báo thành công (toast success), Badge trạng thái được cập nhật với màu xanh, thông báo được gửi cho khách hàng về việc ticket đã được giải quyết, ticket có thể được đóng sau một thời gian | FUNC-DN-02, FUNC-CHAT-01 | Pass | 11/15/2015 | |
| **FUNC-TLHT-03** | Đóng ticket | 1. Đăng nhập Admin<br>2. Truy cập /admin/support/tickets/[id]<br>3. Click nút "Đóng ticket"<br>4. Nhập lý do đóng (nếu có)<br>5. Xác nhận | Ticket được đóng thành công, hiển thị thông báo thành công (toast success), trạng thái cập nhật thành "Đóng" với Badge màu xám, thông báo được gửi cho khách hàng về việc ticket đã được đóng, ticket không thể gửi tin nhắn mới (ô nhập và nút "Gửi" bị disabled) | FUNC-DN-02, FUNC-CHAT-01 | Pass | 11/15/2015 | |
| **FUNC-TLHT-04** | Gán ticket cho nhân viên | 1. Đăng nhập Admin<br>2. Truy cập /admin/support/tickets/[id]<br>3. Click nút "Gán cho nhân viên" hoặc chọn từ Select<br>4. Chọn nhân viên<br>5. Xác nhận | Ticket được gán cho nhân viên thành công, hiển thị thông báo thành công (toast success), thông tin "Người phụ trách" được cập nhật, thông báo được gửi cho nhân viên được gán về việc có ticket mới, lịch sử ticket được ghi nhận | FUNC-DN-02, FUNC-CHAT-01 | Pass | 11/15/2015 | |
| **FUNC-TLHT-05** | Thay đổi mức ưu tiên | 1. Đăng nhập Admin<br>2. Truy cập /admin/support/tickets/[id]<br>3. Click nút "Thay đổi ưu tiên" hoặc chọn từ Select<br>4. Chọn mức ưu tiên mới<br>5. Xác nhận | Mức ưu tiên được cập nhật thành công, hiển thị thông báo thành công (toast success), Badge ưu tiên được cập nhật với màu tương ứng (xanh cho Thấp, vàng cho Trung bình, đỏ cho Cao), lịch sử ticket được ghi nhận | FUNC-DN-02, FUNC-CHAT-01 | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn MDX để dễ dàng quản lý và cập nhật test cases.*
