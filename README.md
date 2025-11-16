# Test Case Template - Quản lý hỗ trợ - liên hệ (Admin)

## Module Code
**Model Management Store: Quản lý hỗ trợ - liên hệ Admin**

## Test Requirement
1. Hiển thị danh sách yêu cầu hỗ trợ
2. Xem chi tiết yêu cầu hỗ trợ
3. Chat hỗ trợ khách hàng
4. Trả lời yêu cầu của khách hàng
5. Xóa yêu cầu của khách hàng
6. Export lịch sử chat
7. Tìm kiếm trong chat
8. Quản lý SLA và phân công

---

## Test Summary

### Người thực hiện Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 54 |
| **Fail** | 0 |
| **Untested** | 60 |
| **N/A** | 0 |
| **Number of Test cases** | 114 |

---

## Test Cases

### Function: Hiển thị danh sách yêu cầu hỗ trợ

#### Check GUI: Hiển thị danh sách yêu cầu hỗ trợ

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DSYCHT-01** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/support<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Hỗ trợ khách hàng" với kích thước text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-DSYCHT-02** | Kiểm tra mô tả chức năng | 1. Truy cập /admin/support<br>2. Kiểm tra mô tả | Hiển thị mô tả "Quản lý và xử lý các yêu cầu hỗ trợ từ khách hàng" màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-DSYCHT-03** | Kiểm tra Select Bộ lọc trạng thái | 1. Truy cập /admin/support<br>2. Kiểm tra Select | Hiển thị Select với placeholder "Trạng thái", có các option: Tất cả, Mới, Đang xử lý, Đã giải quyết, Đóng | | Pass | 11/15/2015 | |
| **GUI-DSYCHT-04** | Kiểm tra Select Bộ lọc ưu tiên | 1. Truy cập /admin/support<br>2. Kiểm tra Select | Hiển thị Select với placeholder "Ưu tiên", có các option: Tất cả, Thấp, Trung bình, Cao | | Pass | 11/15/2015 | |
| **GUI-DSYCHT-05** | Kiểm tra trường Tìm kiếm | 1. Truy cập /admin/support<br>2. Kiểm tra trường tìm kiếm | Hiển thị input với icon Search bên trái, placeholder "Tìm theo mã, tên khách, số điện thoại...", có thể nhập và nhấn Enter để tìm | | Pass | 11/15/2015 | |
| **GUI-DSYCHT-06** | Kiểm tra danh sách hội thoại | 1. Truy cập /admin/support<br>2. Kiểm tra danh sách | Hiển thị List với các item: Avatar, Tên khách hàng, Chủ đề, Trạng thái (Badge), Thời gian cập nhật, Badge chưa đọc (nếu có) | | Pass | 11/15/2015 | |
| **GUI-DSYCHT-07** | Kiểm tra Badge chưa đọc | 1. Truy cập /admin/support<br>2. Kiểm tra Badge | Mỗi hội thoại có tin nhắn chưa đọc hiển thị Badge với số lượng tin nhắn chưa đọc (màu đỏ) | | Pass | 11/15/2015 | |
| **GUI-DSYCHT-08** | Kiểm tra Badge trạng thái | 1. Truy cập /admin/support<br>2. Kiểm tra Badge | Hiển thị Badge trạng thái với màu tương ứng: Mới (default), Đang xử lý (secondary), Đã giải quyết (outline), Đóng (destructive) | | Pass | 11/15/2015 | |
| **GUI-DSYCHT-09** | Kiểm tra Badge ưu tiên | 1. Truy cập /admin/support<br>2. Kiểm tra Badge | Hiển thị Badge ưu tiên với màu tương ứng: Cao (destructive), Trung bình (secondary), Thấp (outline) | | Pass | 11/15/2015 | |
| **GUI-DSYCHT-10** | Kiểm tra nút Xem chi tiết | 1. Truy cập /admin/support<br>2. Kiểm tra nút | Mỗi hội thoại có nút "Xem chi tiết" hoặc click vào hội thoại để mở chi tiết | | Pass | 11/15/2015 | |
| **GUI-DSYCHT-11** | Kiểm tra Pagination | 1. Truy cập /admin/support<br>2. Kiểm tra Pagination | Hiển thị text "Hiển thị 1-X trong Y hội thoại", các nút phân trang: Trước (disabled), số trang, Sau | | Pass | 11/15/2015 | |
| **GUI-DSYCHT-12** | Kiểm tra sắp xếp | 1. Truy cập /admin/support<br>2. Kiểm tra sắp xếp | Danh sách hội thoại được sắp xếp theo cập nhật mới nhất (mặc định) | | Pass | 11/15/2015 | |

---

### Check FUNC: Hiển thị danh sách yêu cầu hỗ trợ

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DSYCHT-01** | Mở trang danh sách yêu cầu hỗ trợ | 1. Truy cập /admin/support | Hiển thị trang với tiêu đề, mô tả, bộ lọc trạng thái, bộ lọc ưu tiên, trường tìm kiếm, danh sách hội thoại, pagination | | Pass | 11/15/2015 | |
| **FUNC-DSYCHT-02** | Hiển thị danh sách hội thoại mặc định | 1. Truy cập /admin/support | Hiển thị tất cả hội thoại trong danh sách, mỗi hội thoại có đầy đủ thông tin: avatar, tên khách hàng, chủ đề, trạng thái, ưu tiên, thời gian cập nhật, badge chưa đọc (nếu có) | | Pass | 11/15/2015 | |
| **FUNC-DSYCHT-03** | Lọc theo Trạng thái | 1. Truy cập /admin/support<br>2. Chọn trạng thái (VD: Mới)<br>3. Kiểm tra danh sách | Hiển thị danh sách hội thoại có trạng thái đã chọn | | Untested | 11/15/2015 | |
| **FUNC-DSYCHT-04** | Lọc theo Ưu tiên | 1. Truy cập /admin/support<br>2. Chọn ưu tiên (VD: Cao)<br>3. Kiểm tra danh sách | Hiển thị danh sách hội thoại có ưu tiên đã chọn | | Untested | 11/15/2015 | |
| **FUNC-DSYCHT-05** | Tìm kiếm hội thoại | 1. Truy cập /admin/support<br>2. Nhập từ khóa tìm kiếm (mã, tên khách, số điện thoại)<br>3. Nhấn Enter | Hiển thị danh sách hội thoại phù hợp với từ khóa tìm kiếm | | Untested | 11/15/2015 | |
| **FUNC-DSYCHT-06** | Click vào hội thoại | 1. Truy cập /admin/support<br>2. Click vào một hội thoại | Chuyển đến trang chi tiết hội thoại /admin/support/[id] | | Pass | 11/15/2015 | |
| **FUNC-DSYCHT-07** | Đánh dấu đã đọc | 1. Truy cập /admin/support<br>2. Click vào hội thoại có tin nhắn chưa đọc<br>3. Xem tin nhắn | Badge chưa đọc giảm hoặc biến mất, trạng thái cập nhật real-time | | Untested | 11/15/2015 | |
| **FUNC-DSYCHT-08** | Xử lý khi không có hội thoại | 1. Truy cập /admin/support<br>2. Lọc để không có hội thoại nào | Hiển thị thông báo "Không tìm thấy hội thoại nào" hoặc danh sách trống | | Untested | 11/15/2015 | |
| **FUNC-DSYCHT-09** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/support<br>2. Tắt kết nối mạng | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại" | | Untested | 11/15/2015 | |
| **FUNC-DSYCHT-10** | Xử lý khi server lỗi | 1. Truy cập /admin/support<br>2. Server trả về lỗi 500 | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau" | | Untested | 11/15/2015 | |

---

### Function: Xem chi tiết yêu cầu hỗ trợ

#### Check GUI: Xem chi tiết yêu cầu hỗ trợ

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CTYCHT-01** | Kiểm tra nút Quay lại | 1. Truy cập /admin/support/[id]<br>2. Kiểm tra nút Quay lại | Hiển thị nút "Quay lại" với icon ArrowLeft variant outline size sm, link đến /admin/support | | Pass | 11/15/2015 | |
| **GUI-CTYCHT-02** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/support/[id]<br>2. Kiểm tra tiêu đề | Hiển thị "Hội thoại hỗ trợ #[id]" hoặc "Chủ đề: [chủ đề]" với kích thước text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-CTYCHT-03** | Kiểm tra card Thông tin khách hàng | 1. Truy cập /admin/support/[id]<br>2. Kiểm tra card | Hiển thị card "Thông tin khách hàng" với: Tên (icon User), SĐT (icon Phone), Email (icon Mail), Mã khách hàng | | Pass | 11/15/2015 | |
| **GUI-CTYCHT-04** | Kiểm tra Container Luồng hội thoại | 1. Truy cập /admin/support/[id]<br>2. Kiểm tra Container | Hiển thị Container "Luồng hội thoại" với các tin nhắn: Tin nhắn khách hàng (bên trái, màu xám), Tin nhắn hỗ trợ (bên phải, màu xanh), Thời gian (text-sm muted-foreground) | | Pass | 11/15/2015 | |
| **GUI-CTYCHT-05** | Kiểm tra trường Tìm kiếm trong chat | 1. Truy cập /admin/support/[id]<br>2. Kiểm tra trường | Hiển thị input với icon Search, placeholder "Tìm kiếm trong lịch sử chat..." | | Pass | 11/15/2015 | |
| **GUI-CTYCHT-06** | Kiểm tra nút Export lịch sử chat | 1. Truy cập /admin/support/[id]<br>2. Kiểm tra nút | Hiển thị nút "Export lịch sử chat" với icon Download variant outline | | Pass | 11/15/2015 | |
| **GUI-CTYCHT-07** | Kiểm tra Badge Trạng thái đã đọc | 1. Truy cập /admin/support/[id]<br>2. Kiểm tra Badge | Hiển thị Badge "Đã đọc" (outline) hoặc "Chưa đọc" (default) | | Pass | 11/15/2015 | |
| **GUI-CTYCHT-08** | Kiểm tra List File đính kèm | 1. Truy cập /admin/support/[id]<br>2. Kiểm tra List | Hiển thị List "File đính kèm" với danh sách file, mỗi file có nút tải xuống hoặc xem trước | | Pass | 11/15/2015 | |
| **GUI-CTYCHT-09** | Kiểm tra nút Trả lời | 1. Truy cập /admin/support/[id]<br>2. Kiểm tra nút | Hiển thị nút "Trả lời" với icon Reply variant outline | | Pass | 11/15/2015 | |
| **GUI-CTYCHT-10** | Kiểm tra nút Chat | 1. Truy cập /admin/support/[id]<br>2. Kiểm tra nút | Hiển thị nút "Chat" với icon MessageSquare variant secondary | | Pass | 11/15/2015 | |

---

### Check FUNC: Xem chi tiết yêu cầu hỗ trợ

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CTYCHT-01** | Mở trang chi tiết yêu cầu hỗ trợ | 1. Truy cập /admin/support/[id] | Hiển thị trang với nút Quay lại, tiêu đề, card Thông tin khách hàng, Container Luồng hội thoại, trường Tìm kiếm trong chat, nút Export lịch sử chat, Badge Trạng thái đã đọc, List File đính kèm, nút Trả lời, nút Chat | | Pass | 11/15/2015 | |
| **FUNC-CTYCHT-02** | Hiển thị đầy đủ nội dung hội thoại | 1. Truy cập /admin/support/[id] | Hiển thị đầy đủ lịch sử trao đổi, hỗ trợ tải thêm theo trang, cuộn vô hạn, tất cả tin nhắn được lưu trữ trong lịch sử chat | | Pass | 11/15/2015 | |
| **FUNC-CTYCHT-03** | Click nút Quay lại | 1. Truy cập /admin/support/[id]<br>2. Click nút "Quay lại" | Chuyển về trang /admin/support | | Pass | 11/15/2015 | |
| **FUNC-CTYCHT-04** | Tải/xem file đính kèm | 1. Truy cập /admin/support/[id]<br>2. Click vào file đính kèm | File mở/tải thành công, an toàn, hiển thị preview hoặc tải về | | Pass | 11/15/2015 | |
| **FUNC-CTYCHT-05** | Tìm kiếm trong chat | 1. Truy cập /admin/support/[id]<br>2. Nhập từ khóa vào trường tìm kiếm<br>3. Nhấn Enter | Hiển thị các tin nhắn chứa từ khóa, highlight từ khóa trong kết quả | | Untested | 11/15/2015 | |
| **FUNC-CTYCHT-06** | Xem lịch sử chat | 1. Truy cập /admin/support/[id]<br>2. Cuộn xuống hoặc click "Xem thêm" | Hiển thị lịch sử chat đầy đủ và chính xác, tải thêm tin nhắn theo trang | | Pass | 11/15/2015 | |
| **FUNC-CTYCHT-07** | Click nút Trả lời | 1. Truy cập /admin/support/[id]<br>2. Click nút "Trả lời" | Mở ô nhập nội dung trả lời hoặc chuyển đến phần chat | | Pass | 11/15/2015 | |
| **FUNC-CTYCHT-08** | Click nút Chat | 1. Truy cập /admin/support/[id]<br>2. Click nút "Chat" | Chuyển đến trang chat /admin/support/[id]/chat | | Pass | 11/15/2015 | |
| **FUNC-CTYCHT-09** | Xử lý khi hội thoại không tồn tại | 1. Truy cập /admin/support/[id không tồn tại] | Hiển thị thông báo lỗi "Hội thoại không tồn tại" hoặc chuyển về trang danh sách | | Untested | 11/15/2015 | |
| **FUNC-CTYCHT-10** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/support/[id]<br>2. Tắt kết nối mạng | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại" | | Untested | 11/15/2015 | |
| **FUNC-CTYCHT-11** | Xử lý khi server lỗi | 1. Truy cập /admin/support/[id]<br>2. Server trả về lỗi 500 | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau" | | Untested | 11/15/2015 | |

---

### Function: Chat hỗ trợ khách hàng

#### Check GUI: Chat hỗ trợ khách hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CHAT-01** | Kiểm tra tiêu đề trang Chat | 1. Truy cập /admin/support/[id]/chat<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Chat hỗ trợ" với kích thước text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-CHAT-02** | Kiểm tra Container Chat | 1. Truy cập /admin/support/[id]/chat<br>2. Kiểm tra Container | Hiển thị Container chat với các tin nhắn: Tin nhắn khách hàng (bên trái), Tin nhắn hỗ trợ (bên phải), Thời gian, Trạng thái đã đọc | | Pass | 11/15/2015 | |
| **GUI-CHAT-03** | Kiểm tra Textarea Ô nhập tin nhắn | 1. Truy cập /admin/support/[id]/chat<br>2. Kiểm tra Textarea | Hiển thị Textarea với placeholder "Nhập tin nhắn...", có thể nhập nhiều dòng, có nút gửi file đính kèm (icon Paperclip) | | Pass | 11/15/2015 | |
| **GUI-CHAT-04** | Kiểm tra nút Gửi | 1. Truy cập /admin/support/[id]/chat<br>2. Kiểm tra nút | Hiển thị nút "Gửi" với icon Send variant default, disabled khi Textarea trống | | Pass | 11/15/2015 | |
| **GUI-CHAT-05** | Kiểm tra Badge Trạng thái kết nối | 1. Truy cập /admin/support/[id]/chat<br>2. Kiểm tra Badge | Hiển thị Badge "Đang kết nối" (secondary) hoặc "Đã kết nối" (default) ở góc trên bên phải | | Pass | 11/15/2015 | |
| **GUI-CHAT-06** | Kiểm tra Dropdown Gợi ý câu trả lời | 1. Truy cập /admin/support/[id]/chat<br>2. Kiểm tra Dropdown | Hiển thị Dropdown "Gợi ý câu trả lời" với các template: "Xin chào, tôi có thể giúp gì cho bạn?", "Cảm ơn bạn đã liên hệ...", "Tôi sẽ kiểm tra và phản hồi sớm nhất..." | | Pass | 11/15/2015 | |
| **GUI-CHAT-07** | Kiểm tra Input Gắn thẻ nội bộ | 1. Truy cập /admin/support/[id]/chat<br>2. Kiểm tra Input | Hiển thị Input "Gắn thẻ nội bộ" với placeholder "VD: vận chuyển, hoàn tiền...", có thể nhập nhiều tag | | Pass | 11/15/2015 | |
| **GUI-CHAT-08** | Kiểm tra nút Đính kèm file | 1. Truy cập /admin/support/[id]/chat<br>2. Kiểm tra nút | Hiển thị nút đính kèm file với icon Paperclip, click để chọn file | | Pass | 11/15/2015 | |

---

### Check FUNC: Chat hỗ trợ khách hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CHAT-01** | Mở trang Chat hỗ trợ | 1. Truy cập /admin/support/[id]/chat | Hiển thị trang với tiêu đề, Container Chat hiển thị lịch sử tin nhắn, Textarea Ô nhập tin nhắn, nút Gửi, Badge Trạng thái kết nối, Dropdown Gợi ý câu trả lời, Input Gắn thẻ nội bộ, nút Đính kèm file | | Pass | 11/15/2015 | |
| **FUNC-CHAT-02** | Gửi tin nhắn real-time thành công | 1. Truy cập /admin/support/[id]/chat<br>2. Nhập tin nhắn vào Textarea<br>3. Click nút "Gửi" | Tin nhắn được gửi ngay, hiển thị trong Container Chat (bên phải), hiển thị thời gian gửi, trạng thái đã đọc cập nhật, tin nhắn được lưu vào lịch sử chat | | Untested | 11/15/2015 | |
| **FUNC-CHAT-03** | Nhận tin nhắn real-time | 1. Truy cập /admin/support/[id]/chat<br>2. Khách hàng gửi tin nhắn mới | Tin nhắn mới hiển thị ngay trong Container Chat (bên trái), có thông báo hoặc badge chưa đọc, tin nhắn được lưu vào lịch sử | | Untested | 11/15/2015 | |
| **FUNC-CHAT-04** | Gửi tin nhắn - Textarea trống | 1. Truy cập /admin/support/[id]/chat<br>2. Để trống Textarea<br>3. Click nút "Gửi" | Nút "Gửi" bị disabled, không thể gửi tin nhắn | | Pass | 11/15/2015 | |
| **FUNC-CHAT-05** | Sử dụng Gợi ý câu trả lời | 1. Truy cập /admin/support/[id]/chat<br>2. Click Dropdown "Gợi ý câu trả lời"<br>3. Chọn một template | Template được chèn vào Textarea, có thể chỉnh sửa trước khi gửi | | Pass | 11/15/2015 | |
| **FUNC-CHAT-06** | Gắn thẻ nội bộ | 1. Truy cập /admin/support/[id]/chat<br>2. Nhập tag vào Input "Gắn thẻ nội bộ"<br>3. Nhấn Enter hoặc click "Thêm tag" | Tag được thêm vào hội thoại, hiển thị dưới dạng Badge, giúp phân loại chủ đề | | Untested | 11/15/2015 | |
| **FUNC-CHAT-07** | Đính kèm file | 1. Truy cập /admin/support/[id]/chat<br>2. Click nút đính kèm file<br>3. Chọn file<br>4. Click "Gửi" | File được đính kèm, hiển thị preview hoặc tên file, file được gửi cùng tin nhắn | | Untested | 11/15/2015 | |
| **FUNC-CHAT-08** | Xử lý khi mất kết nối | 1. Truy cập /admin/support/[id]/chat<br>2. Tắt kết nối mạng<br>3. Gửi tin nhắn | Hiển thị thông báo "Mất kết nối. Đang thử kết nối lại...", Badge chuyển thành "Đang kết nối", tin nhắn được lưu tạm và gửi khi kết nối lại | | Untested | 11/15/2015 | |
| **FUNC-CHAT-09** | Xử lý khi server lỗi | 1. Truy cập /admin/support/[id]/chat<br>2. Server trả về lỗi 500<br>3. Gửi tin nhắn | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau", tin nhắn không được gửi | | Untested | 11/15/2015 | |

---

### Function: Trả lời yêu cầu của khách hàng

#### Check GUI: Trả lời yêu cầu của khách hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-TLYC-01** | Kiểm tra modal Trả lời | 1. Truy cập /admin/support/[id]<br>2. Click nút "Trả lời"<br>3. Kiểm tra modal | Hiển thị Dialog với tiêu đề "Trả lời yêu cầu hỗ trợ", mô tả "Trả lời yêu cầu từ khách hàng" | | Pass | 11/15/2015 | |
| **GUI-TLYC-02** | Kiểm tra trường Tiêu đề | 1. Truy cập /admin/support/[id]<br>2. Click nút "Trả lời"<br>3. Kiểm tra trường | Hiển thị label "Tiêu đề", input type text với giá trị mặc định là "Re: [chủ đề gốc]" | | Pass | 11/15/2015 | |
| **GUI-TLYC-03** | Kiểm tra Textarea Nội dung | 1. Truy cập /admin/support/[id]<br>2. Click nút "Trả lời"<br>3. Kiểm tra Textarea | Hiển thị label "Nội dung *", Textarea với placeholder "Nhập nội dung trả lời...", rows 6 | | Pass | 11/15/2015 | |
| **GUI-TLYC-04** | Kiểm tra Select Loại phản hồi | 1. Truy cập /admin/support/[id]<br>2. Click nút "Trả lời"<br>3. Kiểm tra Select | Hiển thị label "Loại phản hồi", Select với các option: Thông tin, Giải quyết, Cần thêm thông tin, Chuyển tiếp | | Pass | 11/15/2015 | |
| **GUI-TLYC-05** | Kiểm tra checkbox Gửi qua email | 1. Truy cập /admin/support/[id]<br>2. Click nút "Trả lời"<br>3. Kiểm tra checkbox | Hiển thị checkbox với label "Gửi qua email", mặc định checked | | Pass | 11/15/2015 | |
| **GUI-TLYC-06** | Kiểm tra nút Đính kèm file | 1. Truy cập /admin/support/[id]<br>2. Click nút "Trả lời"<br>3. Kiểm tra nút | Hiển thị nút "Đính kèm file" với icon Paperclip | | Pass | 11/15/2015 | |
| **GUI-TLYC-07** | Kiểm tra nút Hủy | 1. Truy cập /admin/support/[id]<br>2. Click nút "Trả lời"<br>3. Kiểm tra nút | Hiển thị nút "Hủy" variant outline | | Pass | 11/15/2015 | |
| **GUI-TLYC-08** | Kiểm tra nút Gửi trả lời | 1. Truy cập /admin/support/[id]<br>2. Click nút "Trả lời"<br>3. Kiểm tra nút | Hiển thị nút "Gửi trả lời" type submit | | Pass | 11/15/2015 | |

---

### Check FUNC: Trả lời yêu cầu của khách hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TLYC-01** | Mở modal trả lời | 1. Truy cập /admin/support/[id]<br>2. Click nút "Trả lời" | Hiển thị Dialog với tiêu đề "Trả lời yêu cầu hỗ trợ", mô tả, trường Tiêu đề (có giá trị mặc định), Textarea Nội dung, Select Loại phản hồi, checkbox Gửi qua email, nút Đính kèm file, nút Hủy, nút Gửi trả lời | | Pass | 11/15/2015 | |
| **FUNC-TLYC-02** | Trả lời yêu cầu thành công | 1. Truy cập /admin/support/[id]<br>2. Click nút "Trả lời"<br>3. Điều chỉnh tiêu đề (nếu cần)<br>4. Nhập nội dung trả lời<br>5. Chọn loại phản hồi<br>6. Tích checkbox Gửi qua email<br>7. Click "Gửi trả lời" | Hiển thị thông báo "Gửi trả lời thành công", trả lời được gửi đến khách hàng qua email (nếu được chọn), trả lời được thêm vào lịch sử hội thoại, trạng thái hội thoại được cập nhật, modal đóng | | Untested | 11/15/2015 | |
| **FUNC-TLYC-03** | Trả lời - Thiếu Nội dung | 1. Truy cập /admin/support/[id]<br>2. Click nút "Trả lời"<br>3. Để trống nội dung<br>4. Click "Gửi trả lời" | Hiển thị thông báo lỗi "Nội dung không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-TLYC-04** | Trả lời - Đính kèm file | 1. Truy cập /admin/support/[id]<br>2. Click nút "Trả lời"<br>3. Nhập nội dung<br>4. Click "Đính kèm file"<br>5. Chọn file<br>6. Click "Gửi trả lời" | File được đính kèm, hiển thị tên file, file được gửi cùng trả lời | | Untested | 11/15/2015 | |
| **FUNC-TLYC-05** | Click nút Hủy | 1. Truy cập /admin/support/[id]<br>2. Click nút "Trả lời"<br>3. Click "Hủy" | Modal đóng, không gửi trả lời | | Pass | 11/15/2015 | |
| **FUNC-TLYC-06** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/support/[id]<br>2. Click nút "Trả lời"<br>3. Điền đầy đủ thông tin<br>4. Tắt kết nối mạng<br>5. Click "Gửi trả lời" | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", form không được gửi | | Untested | 11/15/2015 | |
| **FUNC-TLYC-07** | Xử lý khi server lỗi | 1. Truy cập /admin/support/[id]<br>2. Click nút "Trả lời"<br>3. Điền đầy đủ thông tin<br>4. Server trả về lỗi 500<br>5. Click "Gửi trả lời" | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau", form không được gửi | | Untested | 11/15/2015 | |

---

### Function: Xóa yêu cầu của khách hàng

#### Check GUI: Xóa yêu cầu của khách hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XYC-01** | Kiểm tra nút Xóa | 1. Truy cập /admin/support/[id]<br>2. Kiểm tra nút | Hiển thị nút "Xóa yêu cầu" với icon Trash2 variant destructive | | Pass | 11/15/2015 | |
| **GUI-XYC-02** | Kiểm tra Dialog xác nhận xóa | 1. Truy cập /admin/support/[id]<br>2. Click nút "Xóa yêu cầu"<br>3. Kiểm tra dialog | Hiển thị Dialog với tiêu đề "Xác nhận xóa yêu cầu hỗ trợ", mô tả "Bạn có chắc chắn muốn xóa yêu cầu này? Hành động này không thể hoàn tác", textarea "Lý do xóa", nút "Hủy" variant outline, nút "Xóa vĩnh viễn" variant destructive | | Pass | 11/15/2015 | |

---

### Check FUNC: Xóa yêu cầu của khách hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XYC-01** | Xóa yêu cầu thành công | 1. Truy cập /admin/support/[id]<br>2. Click nút "Xóa yêu cầu"<br>3. Nhập lý do xóa<br>4. Click "Xóa vĩnh viễn" | Hiển thị thông báo "Đã xóa yêu cầu hỗ trợ", yêu cầu bị xóa khỏi hệ thống, chuyển về trang danh sách | | Untested | 11/15/2015 | |
| **FUNC-XYC-02** | Hủy xóa yêu cầu | 1. Truy cập /admin/support/[id]<br>2. Click nút "Xóa yêu cầu"<br>3. Click "Hủy" trong dialog | Dialog đóng, yêu cầu không bị xóa, vẫn ở trang chi tiết | | Pass | 11/15/2015 | |
| **FUNC-XYC-03** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/support/[id]<br>2. Click nút "Xóa yêu cầu"<br>3. Nhập lý do<br>4. Tắt kết nối mạng<br>5. Click "Xóa vĩnh viễn" | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", yêu cầu không bị xóa | | Untested | 11/15/2015 | |
| **FUNC-XYC-04** | Xử lý khi server lỗi | 1. Truy cập /admin/support/[id]<br>2. Click nút "Xóa yêu cầu"<br>3. Nhập lý do<br>4. Server trả về lỗi 500<br>5. Click "Xóa vĩnh viễn" | Hiển thị thông báo lỗi "Lỗi xóa yêu cầu", yêu cầu không bị xóa | | Untested | 11/15/2015 | |

---

### Function: Export lịch sử chat

#### Check GUI: Export lịch sử chat

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-EXPORT-01** | Kiểm tra nút Export lịch sử chat | 1. Truy cập /admin/support/[id]<br>2. Kiểm tra nút | Hiển thị nút "Export lịch sử chat" với icon Download variant outline | | Pass | 11/15/2015 | |
| **GUI-EXPORT-02** | Kiểm tra modal Export | 1. Truy cập /admin/support/[id]<br>2. Click nút "Export lịch sử chat"<br>3. Kiểm tra modal | Hiển thị Dialog với tiêu đề "Export lịch sử chat", mô tả "Xuất lịch sử chat ra file" | | Pass | 11/15/2015 | |
| **GUI-EXPORT-03** | Kiểm tra Select Định dạng file | 1. Truy cập /admin/support/[id]<br>2. Click nút "Export lịch sử chat"<br>3. Kiểm tra Select | Hiển thị label "Định dạng file *", Select với các option: CSV, TXT, PDF | | Pass | 11/15/2015 | |
| **GUI-EXPORT-04** | Kiểm tra Date Range | 1. Truy cập /admin/support/[id]<br>2. Click nút "Export lịch sử chat"<br>3. Kiểm tra Date Range | Hiển thị 2 input date với text "đến" ở giữa, checkbox "Export toàn bộ" | | Pass | 11/15/2015 | |
| **GUI-EXPORT-05** | Kiểm tra nút Hủy | 1. Truy cập /admin/support/[id]<br>2. Click nút "Export lịch sử chat"<br>3. Kiểm tra nút | Hiển thị nút "Hủy" variant outline | | Pass | 11/15/2015 | |
| **GUI-EXPORT-06** | Kiểm tra nút Export | 1. Truy cập /admin/support/[id]<br>2. Click nút "Export lịch sử chat"<br>3. Kiểm tra nút | Hiển thị nút "Export" type submit | | Pass | 11/15/2015 | |

---

### Check FUNC: Export lịch sử chat

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-EXPORT-01** | Mở modal Export | 1. Truy cập /admin/support/[id]<br>2. Click nút "Export lịch sử chat" | Hiển thị Dialog với tiêu đề "Export lịch sử chat", mô tả, Select Định dạng file, Date Range, checkbox Export toàn bộ, nút Hủy, nút Export | | Pass | 11/15/2015 | |
| **FUNC-EXPORT-02** | Export lịch sử chat thành công - CSV | 1. Truy cập /admin/support/[id]<br>2. Click nút "Export lịch sử chat"<br>3. Chọn định dạng CSV<br>4. Tích checkbox "Export toàn bộ"<br>5. Click "Export" | Hiển thị thông báo "Export lịch sử chat thành công", tải về file CSV với đầy đủ lịch sử chat, file có định dạng đúng | | Untested | 11/15/2015 | |
| **FUNC-EXPORT-03** | Export lịch sử chat thành công - PDF | 1. Truy cập /admin/support/[id]<br>2. Click nút "Export lịch sử chat"<br>3. Chọn định dạng PDF<br>4. Chọn khoảng thời gian<br>5. Click "Export" | Hiển thị thông báo "Export lịch sử chat thành công", tải về file PDF với lịch sử chat trong khoảng thời gian đã chọn, file có định dạng đúng | | Untested | 11/15/2015 | |
| **FUNC-EXPORT-04** | Export - Thiếu Định dạng file | 1. Truy cập /admin/support/[id]<br>2. Click nút "Export lịch sử chat"<br>3. Không chọn định dạng<br>4. Click "Export" | Hiển thị thông báo lỗi "Vui lòng chọn định dạng file", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-EXPORT-05** | Click nút Hủy | 1. Truy cập /admin/support/[id]<br>2. Click nút "Export lịch sử chat"<br>3. Click "Hủy" | Modal đóng, không export lịch sử chat | | Pass | 11/15/2015 | |
| **FUNC-EXPORT-06** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/support/[id]<br>2. Click nút "Export lịch sử chat"<br>3. Chọn định dạng<br>4. Tắt kết nối mạng<br>5. Click "Export" | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", form không được gửi | | Untested | 11/15/2015 | |
| **FUNC-EXPORT-07** | Xử lý khi server lỗi | 1. Truy cập /admin/support/[id]<br>2. Click nút "Export lịch sử chat"<br>3. Chọn định dạng<br>4. Server trả về lỗi 500<br>5. Click "Export" | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau", form không được gửi | | Untested | 11/15/2015 | |

---

### Function: Tìm kiếm trong chat

#### Check GUI: Tìm kiếm trong chat

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-TKCHAT-01** | Kiểm tra trường Tìm kiếm trong chat | 1. Truy cập /admin/support/[id]<br>2. Kiểm tra trường | Hiển thị input với icon Search, placeholder "Tìm kiếm trong lịch sử chat..." | | Pass | 11/15/2015 | |
| **GUI-TKCHAT-02** | Kiểm tra nút Xóa tìm kiếm | 1. Truy cập /admin/support/[id]<br>2. Nhập từ khóa vào trường tìm kiếm<br>3. Kiểm tra nút | Hiển thị nút "X" để xóa từ khóa tìm kiếm | | Pass | 11/15/2015 | |

---

### Check FUNC: Tìm kiếm trong chat

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TKCHAT-01** | Tìm kiếm trong chat thành công | 1. Truy cập /admin/support/[id]<br>2. Nhập từ khóa vào trường tìm kiếm<br>3. Nhấn Enter | Hiển thị các tin nhắn chứa từ khóa, highlight từ khóa trong kết quả, hiển thị số lượng kết quả tìm thấy | | Untested | 11/15/2015 | |
| **FUNC-TKCHAT-02** | Tìm kiếm - Không có kết quả | 1. Truy cập /admin/support/[id]<br>2. Nhập từ khóa không có trong chat<br>3. Nhấn Enter | Hiển thị thông báo "Không tìm thấy kết quả nào" | | Untested | 11/15/2015 | |
| **FUNC-TKCHAT-03** | Xóa tìm kiếm | 1. Truy cập /admin/support/[id]<br>2. Nhập từ khóa<br>3. Click nút "X" | Từ khóa được xóa, hiển thị lại toàn bộ lịch sử chat | | Pass | 11/15/2015 | |

---

### Function: Quản lý SLA và phân công

#### Check GUI: Quản lý SLA và phân công

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-SLA-01** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/support/sla<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Quản lý SLA và phân công" với kích thước text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-SLA-02** | Kiểm tra Form Thiết lập SLA | 1. Truy cập /admin/support/sla<br>2. Kiểm tra Form | Hiển thị Form "Thiết lập SLA" với: label "Mục tiêu phản hồi (phút) *", input type number, label "Mục tiêu giải quyết (giờ) *", input type number | | Pass | 11/15/2015 | |
| **GUI-SLA-03** | Kiểm tra Select Phân công Agent | 1. Truy cập /admin/support/sla<br>2. Kiểm tra Select | Hiển thị label "Agent phụ trách", Select với placeholder "Chọn agent...", có danh sách agent | | Pass | 11/15/2015 | |
| **GUI-SLA-04** | Kiểm tra Select Nhóm hỗ trợ | 1. Truy cập /admin/support/sla<br>2. Kiểm tra Select | Hiển thị label "Nhóm hỗ trợ", Select với placeholder "Chọn nhóm...", có danh sách nhóm | | Pass | 11/15/2015 | |
| **GUI-SLA-05** | Kiểm tra nút Lưu cấu hình | 1. Truy cập /admin/support/sla<br>2. Kiểm tra nút | Hiển thị nút "Lưu cấu hình" type submit | | Pass | 11/15/2015 | |
| **GUI-SLA-06** | Kiểm tra Card Báo cáo tuân thủ | 1. Truy cập /admin/support/sla<br>2. Kiểm tra Card | Hiển thị Card "Báo cáo tuân thủ" với: Tỉ lệ đáp ứng SLA (%), Tỉ lệ quá hạn (%), Biểu đồ theo dõi hiệu suất | | Pass | 11/15/2015 | |

---

### Check FUNC: Quản lý SLA và phân công

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-SLA-01** | Mở trang Quản lý SLA | 1. Truy cập /admin/support/sla | Hiển thị trang với tiêu đề, Form Thiết lập SLA, Select Phân công Agent, Select Nhóm hỗ trợ, nút Lưu cấu hình, Card Báo cáo tuân thủ | | Pass | 11/15/2015 | |
| **FUNC-SLA-02** | Thiết lập SLA thành công | 1. Truy cập /admin/support/sla<br>2. Nhập Mục tiêu phản hồi (VD: 15 phút)<br>3. Nhập Mục tiêu giải quyết (VD: 24 giờ)<br>4. Click "Lưu cấu hình" | Hiển thị thông báo "Thiết lập SLA thành công", SLA được lưu và áp dụng ngay, báo cáo tuân thủ được cập nhật | | Untested | 11/15/2015 | |
| **FUNC-SLA-03** | Thiết lập SLA - Thiếu Mục tiêu phản hồi | 1. Truy cập /admin/support/sla<br>2. Để trống Mục tiêu phản hồi<br>3. Nhập Mục tiêu giải quyết<br>4. Click "Lưu cấu hình" | Hiển thị thông báo lỗi "Mục tiêu phản hồi không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-SLA-04** | Thiết lập SLA - Thiếu Mục tiêu giải quyết | 1. Truy cập /admin/support/sla<br>2. Nhập Mục tiêu phản hồi<br>3. Để trống Mục tiêu giải quyết<br>4. Click "Lưu cấu hình" | Hiển thị thông báo lỗi "Mục tiêu giải quyết không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-SLA-05** | Phân công Agent thành công | 1. Truy cập /admin/support/sla<br>2. Chọn Agent phụ trách<br>3. Click "Lưu cấu hình" | Hiển thị thông báo "Phân công agent thành công", ticket/hội thoại hiển thị người phụ trách, thông báo đến agent | | Untested | 11/15/2015 | |
| **FUNC-SLA-06** | Phân công Nhóm hỗ trợ thành công | 1. Truy cập /admin/support/sla<br>2. Chọn Nhóm hỗ trợ<br>3. Click "Lưu cấu hình" | Hiển thị thông báo "Phân công nhóm hỗ trợ thành công", ticket/hội thoại được gán cho nhóm, thông báo đến nhóm | | Untested | 11/15/2015 | |
| **FUNC-SLA-07** | Xem báo cáo tuân thủ | 1. Truy cập /admin/support/sla<br>2. Kiểm tra Card Báo cáo tuân thủ | Hiển thị Tỉ lệ đáp ứng SLA (%), Tỉ lệ quá hạn (%), Biểu đồ theo dõi hiệu suất, số liệu chính xác | | Pass | 11/15/2015 | |
| **FUNC-SLA-08** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/support/sla<br>2. Điền đầy đủ thông tin<br>3. Tắt kết nối mạng<br>4. Click "Lưu cấu hình" | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", form không được gửi | | Untested | 11/15/2015 | |
| **FUNC-SLA-09** | Xử lý khi server lỗi | 1. Truy cập /admin/support/sla<br>2. Điền đầy đủ thông tin<br>3. Server trả về lỗi 500<br>4. Click "Lưu cấu hình" | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau", form không được gửi | | Untested | 11/15/2015 | |

---

**Người tạo:** Testing Team  
**Ngày cập nhật:** 11/15/2015  
**Phiên bản:** 1.0

