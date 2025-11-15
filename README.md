# Test Case Template - Chức năng hỗ trợ - liên hệ (User)

## Module Code
**Model Management Store: Chức năng hỗ trợ - liên hệ User**

## Test Requirement
1. Chat hỗ trợ
2. Gửi phản hồi/khiếu nại
3. Quản lý yêu cầu hỗ trợ
4. Câu hỏi thường gặp
5. Thông tin liên hệ

---

## Test Summary

### Người thực hiện Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 140 |
| **Fail** | 0 |
| **Untested** | 40 |
| **N/A** | 0 |
| **Number of Test cases** | 180 |

---

## Test Cases

### Function: Chat hỗ trợ

#### Check GUI: Chat hỗ trợ

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CH-01** | Kiểm tra tiêu đề chat | 1. Truy cập /user/support<br>2. Chọn tab "Chat trực tiếp"<br>3. Kiểm tra tiêu đề | Hiển thị tiêu đề "Chat trực tiếp với nhân viên hỗ trợ" với icon MessageSquare, CardTitle | | Pass | 11/15/2015 | |
| **GUI-CH-02** | Kiểm tra mô tả chat | 1. Chọn tab "Chat trực tiếp"<br>2. Kiểm tra mô tả | Hiển thị mô tả "Nhân viên hỗ trợ sẽ phản hồi trong vài phút" với CardDescription | | Pass | 11/15/2015 | |
| **GUI-CH-03** | Kiểm tra khu vực tin nhắn | 1. Chọn tab "Chat trực tiếp"<br>2. Kiểm tra khu vực | Hiển thị container h-96 overflow-y-auto border rounded-lg p-4 space-y-4 chứa danh sách tin nhắn | | Pass | 11/15/2015 | |
| **GUI-CH-04** | Kiểm tra tin nhắn người dùng | 1. Xem tin nhắn từ user<br>2. Kiểm tra hiển thị | Tin nhắn hiển thị bên phải (justify-end), background bg-primary text-primary-foreground, max-w-xs lg:max-w-md, có thời gian gửi | | Pass | 11/15/2015 | |
| **GUI-CH-05** | Kiểm tra tin nhắn hỗ trợ | 1. Xem tin nhắn từ support<br>2. Kiểm tra hiển thị | Tin nhắn hiển thị bên trái (justify-start), background bg-muted, max-w-xs lg:max-w-md, có thời gian gửi | | Pass | 11/15/2015 | |
| **GUI-CH-06** | Kiểm tra thời gian tin nhắn | 1. Xem tin nhắn<br>2. Kiểm tra thời gian | Hiển thị thời gian với format ngày Việt Nam, text-xs opacity-70 mt-1 | | Pass | 11/15/2015 | |
| **GUI-CH-07** | Kiểm tra ô nhập tin nhắn | 1. Chọn tab "Chat trực tiếp"<br>2. Kiểm tra ô nhập | Hiển thị Input với placeholder "Nhập tin nhắn của bạn...", có thể nhập và gửi bằng Enter | | Pass | 11/15/2015 | |
| **GUI-CH-08** | Kiểm tra nút gửi tin nhắn | 1. Chọn tab "Chat trực tiếp"<br>2. Kiểm tra nút | Hiển thị nút với icon Send, disabled khi ô nhập trống | | Pass | 11/15/2015 | |
| **GUI-CH-09** | Kiểm tra tab Chat trực tiếp | 1. Truy cập /user/support<br>2. Kiểm tra tab | Hiển thị tab "Chat trực tiếp" với icon MessageSquare trong TabsList | | Pass | 11/15/2015 | |
| **GUI-CH-10** | Kiểm tra scroll khu vực tin nhắn | 1. Có nhiều tin nhắn<br>2. Kiểm tra scroll | Khu vực tin nhắn có scroll khi nội dung vượt quá chiều cao, tự động scroll xuống tin nhắn mới nhất | | Pass | 11/15/2015 | |

---

### Check FUNC: Chat hỗ trợ

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CH-01** | Mở tab Chat trực tiếp | 1. Truy cập /user/support<br>2. Chọn tab "Chat trực tiếp" | Hiển thị khu vực chat với tiêu đề, mô tả, danh sách tin nhắn (nếu có), ô nhập và nút gửi | | Pass | 11/15/2015 | |
| **FUNC-CH-02** | Kết nối chat hỗ trợ | 1. Chọn tab "Chat trực tiếp"<br>2. Kiểm tra kết nối | Hệ thống thiết lập kết nối chat real-time, hiển thị trạng thái kết nối, có thể gửi và nhận tin nhắn | | Pass | 11/15/2015 | |
| **FUNC-CH-03** | Gửi tin nhắn | 1. Chọn tab "Chat trực tiếp"<br>2. Nhập tin nhắn<br>3. Nhấn nút gửi hoặc Enter | Tin nhắn được gửi thành công, hiển thị trong khu vực chat bên phải, có thời gian gửi, ô nhập được xóa trống | | Pass | 11/15/2015 | |
| **FUNC-CH-04** | Gửi tin nhắn bằng Enter | 1. Chọn tab "Chat trực tiếp"<br>2. Nhập tin nhắn<br>3. Nhấn Enter | Tin nhắn được gửi như khi nhấn nút gửi | | Pass | 11/15/2015 | |
| **FUNC-CH-05** | Gửi tin nhắn rỗng | 1. Chọn tab "Chat trực tiếp"<br>2. Để trống ô nhập<br>3. Nhấn gửi | Nút gửi bị disabled, không gửi tin nhắn | | Pass | 11/15/2015 | |
| **FUNC-CH-06** | Nhận tin nhắn hỗ trợ | 1. Gửi tin nhắn<br>2. Đợi phản hồi | Tin nhắn từ nhân viên hỗ trợ được hiển thị tự động trong khu vực chat bên trái, có thời gian, trạng thái đã đọc được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-CH-07** | Lưu lịch sử chat | 1. Gửi và nhận tin nhắn<br>2. Tải lại trang<br>3. Kiểm tra lịch sử | Lịch sử chat được lưu trữ, hiển thị lại khi tải trang | | Pass | 11/15/2015 | |
| **FUNC-CH-08** | Tìm kiếm trong lịch sử chat | 1. Chọn tab "Chat trực tiếp"<br>2. Nhập từ khóa tìm kiếm | Lịch sử chat được lọc theo từ khóa, chỉ hiển thị tin nhắn chứa từ khóa | | Pass | 11/15/2015 | |
| **FUNC-CH-09** | Export lịch sử chat | 1. Chọn tab "Chat trực tiếp"<br>2. Nhấn nút export | Lịch sử chat được export ra file CSV hoặc TXT, file được tải xuống | | Pass | 11/15/2015 | |
| **FUNC-CH-10** | Hiển thị trạng thái đã đọc | 1. Nhận tin nhắn hỗ trợ<br>2. Kiểm tra trạng thái | Trạng thái đã đọc được cập nhật khi người dùng xem tin nhắn, hiển thị badge "Đã đọc" | | Pass | 11/15/2015 | |
| **FUNC-CH-11** | Auto-scroll đến tin nhắn mới | 1. Có nhiều tin nhắn<br>2. Gửi/nhận tin nhắn mới | Khu vực chat tự động scroll xuống tin nhắn mới nhất | | Pass | 11/15/2015 | |
| **FUNC-CH-12** | Gửi tin nhắn dài | 1. Nhập tin nhắn rất dài (>500 ký tự)<br>2. Gửi tin nhắn | Tin nhắn được gửi thành công, hiển thị đầy đủ trong khu vực chat, tự động xuống dòng | | Pass | 11/15/2015 | |

---

### Function: Gửi phản hồi/khiếu nại

#### Check GUI: Gửi phản hồi/khiếu nại

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-GPH-01** | Kiểm tra nút tạo yêu cầu mới | 1. Truy cập /user/support<br>2. Chọn tab "Yêu cầu hỗ trợ"<br>3. Kiểm tra nút | Hiển thị nút "Tạo yêu cầu mới" với icon FileText, variant default | | Pass | 11/15/2015 | |
| **GUI-GPH-02** | Kiểm tra modal tạo yêu cầu | 1. Nhấn nút "Tạo yêu cầu mới"<br>2. Kiểm tra modal | Hiển thị modal với background overlay đen 50%, card max-w-2xl max-h-[90vh] overflow-y-auto, tiêu đề "Tạo yêu cầu hỗ trợ" | | Pass | 11/15/2015 | |
| **GUI-GPH-03** | Kiểm tra trường Tiêu đề | 1. Mở modal tạo yêu cầu<br>2. Kiểm tra trường | Hiển thị label "Tiêu đề *", Input với placeholder "Tóm tắt vấn đề của bạn", required | | Pass | 11/15/2015 | |
| **GUI-GPH-04** | Kiểm tra trường Danh mục | 1. Mở modal tạo yêu cầu<br>2. Kiểm tra trường | Hiển thị label "Danh mục *", Select với các option: Đơn hàng, Sản phẩm, Thanh toán, Vận chuyển, Tài khoản, Kỹ thuật, Khác | | Pass | 11/15/2015 | |
| **GUI-GPH-05** | Kiểm tra trường Mức độ ưu tiên | 1. Mở modal tạo yêu cầu<br>2. Kiểm tra trường | Hiển thị label "Mức độ ưu tiên", Select với các option: Thấp, Trung bình, Cao, Khẩn cấp | | Pass | 11/15/2015 | |
| **GUI-GPH-06** | Kiểm tra trường Mô tả vấn đề | 1. Mở modal tạo yêu cầu<br>2. Kiểm tra trường | Hiển thị label "Mô tả chi tiết *", Textarea với placeholder "Mô tả chi tiết vấn đề bạn đang gặp phải...", rows 6, required | | Pass | 11/15/2015 | |
| **GUI-GPH-07** | Kiểm tra trường Mã đơn hàng | 1. Mở modal tạo yêu cầu<br>2. Kiểm tra trường | Hiển thị label "Mã đơn hàng (nếu có)", Input với placeholder "Nhập mã đơn hàng liên quan", optional | | Pass | 11/15/2015 | |
| **GUI-GPH-08** | Kiểm tra trường File đính kèm | 1. Mở modal tạo yêu cầu<br>2. Kiểm tra trường | Hiển thị label "Tệp đính kèm", Input type file multiple, có thể chọn nhiều file | | Pass | 11/15/2015 | |
| **GUI-GPH-09** | Kiểm tra nút Hủy | 1. Mở modal tạo yêu cầu<br>2. Kiểm tra nút | Hiển thị nút "Hủy" variant outline, đóng modal khi nhấn | | Pass | 11/15/2015 | |
| **GUI-GPH-10** | Kiểm tra nút Gửi yêu cầu | 1. Mở modal tạo yêu cầu<br>2. Kiểm tra nút | Hiển thị nút "Gửi yêu cầu" variant default, gửi yêu cầu khi nhấn | | Pass | 11/15/2015 | |

---

### Check FUNC: Gửi phản hồi/khiếu nại

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-GPH-01** | Mở modal tạo yêu cầu | 1. Truy cập /user/support<br>2. Chọn tab "Yêu cầu hỗ trợ"<br>3. Nhấn nút "Tạo yêu cầu mới" | Mở modal với form trống, các trường sẵn sàng nhập | | Pass | 11/15/2015 | |
| **FUNC-GPH-02** | Tạo yêu cầu hỗ trợ thành công | 1. Mở modal tạo yêu cầu<br>2. Nhập đầy đủ thông tin (tiêu đề, danh mục, mô tả)<br>3. Nhấn "Gửi yêu cầu" | Yêu cầu được tạo thành công, modal đóng, hiển thị toast "Yêu cầu hỗ trợ đã được gửi thành công", yêu cầu xuất hiện trong danh sách với trạng thái "Mở" | | Pass | 11/15/2015 | |
| **FUNC-GPH-03** | Tạo yêu cầu thiếu tiêu đề | 1. Mở modal tạo yêu cầu<br>2. Để trống tiêu đề<br>3. Nhập các trường khác<br>4. Nhấn "Gửi yêu cầu" | Hiển thị toast lỗi "Vui lòng nhập tiêu đề", không gửi yêu cầu, modal vẫn mở | | Pass | 11/15/2015 | |
| **FUNC-GPH-04** | Tạo yêu cầu thiếu mô tả | 1. Mở modal tạo yêu cầu<br>2. Nhập tiêu đề<br>3. Để trống mô tả<br>4. Nhấn "Gửi yêu cầu" | Hiển thị toast lỗi "Vui lòng nhập mô tả vấn đề", không gửi yêu cầu | | Pass | 11/15/2015 | |
| **FUNC-GPH-05** | Chọn danh mục yêu cầu | 1. Mở modal tạo yêu cầu<br>2. Chọn danh mục từ Select | Danh mục được chọn, hiển thị trong Select, có thể thay đổi | | Pass | 11/15/2015 | |
| **FUNC-GPH-06** | Chọn mức độ ưu tiên | 1. Mở modal tạo yêu cầu<br>2. Chọn mức độ ưu tiên | Mức độ ưu tiên được chọn, mặc định là "Trung bình", có thể thay đổi | | Pass | 11/15/2015 | |
| **FUNC-GPH-07** | Đính kèm file | 1. Mở modal tạo yêu cầu<br>2. Chọn file đính kèm | File được chọn, hiển thị tên file trong danh sách, có thể chọn nhiều file | | Pass | 11/15/2015 | |
| **FUNC-GPH-08** | Đính kèm file không hợp lệ | 1. Mở modal tạo yêu cầu<br>2. Chọn file không đúng định dạng | Hiển thị thông báo lỗi "Định dạng file không được hỗ trợ", file không được thêm | | Pass | 11/15/2015 | |
| **FUNC-GPH-09** | Đính kèm file quá kích thước | 1. Mở modal tạo yêu cầu<br>2. Chọn file > 10MB | Hiển thị thông báo lỗi "File quá lớn. Kích thước tối đa: 10MB", file không được thêm | | Pass | 11/15/2015 | |
| **FUNC-GPH-10** | Nhập mã đơn hàng | 1. Mở modal tạo yêu cầu<br>2. Nhập mã đơn hàng | Mã đơn hàng được nhập, hiển thị trong Input, optional | | Pass | 11/15/2015 | |
| **FUNC-GPH-11** | Hủy tạo yêu cầu | 1. Mở modal tạo yêu cầu<br>2. Nhập một số thông tin<br>3. Nhấn "Hủy" | Modal đóng, không lưu thông tin đã nhập, quay lại trang yêu cầu hỗ trợ | | Pass | 11/15/2015 | |
| **FUNC-GPH-12** | Đóng modal bằng click overlay | 1. Mở modal tạo yêu cầu<br>2. Click vào overlay | Modal đóng, không lưu thông tin | | Pass | 11/15/2015 | |
| **FUNC-GPH-13** | Tạo yêu cầu với đầy đủ thông tin | 1. Mở modal tạo yêu cầu<br>2. Nhập đầy đủ: tiêu đề, danh mục, mức độ ưu tiên, mô tả, mã đơn hàng, file đính kèm<br>3. Nhấn "Gửi yêu cầu" | Yêu cầu được tạo với đầy đủ thông tin, hiển thị trong danh sách với tất cả thông tin đã nhập | | Pass | 11/15/2015 | |

---

### Function: Quản lý yêu cầu hỗ trợ

#### Check GUI: Quản lý yêu cầu hỗ trợ

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-QLYC-01** | Kiểm tra tab Yêu cầu hỗ trợ | 1. Truy cập /user/support<br>2. Kiểm tra tab | Hiển thị tab "Yêu cầu hỗ trợ" với icon FileText, số lượng yêu cầu trong ngoặc đơn | | Pass | 11/15/2015 | |
| **GUI-QLYC-02** | Kiểm tra bộ lọc trạng thái | 1. Chọn tab "Yêu cầu hỗ trợ"<br>2. Kiểm tra bộ lọc | Hiển thị Select với trigger w-40, các option: "Tất cả", "Mở", "Đang xử lý", "Đã giải quyết", "Đã đóng" với số lượng | | Pass | 11/15/2015 | |
| **GUI-QLYC-03** | Kiểm tra bộ lọc danh mục | 1. Chọn tab "Yêu cầu hỗ trợ"<br>2. Kiểm tra bộ lọc | Hiển thị Select với trigger w-40, các option: "Tất cả", "Đơn hàng", "Sản phẩm", "Thanh toán", v.v. | | Pass | 11/15/2015 | |
| **GUI-QLYC-04** | Kiểm tra ô tìm kiếm | 1. Chọn tab "Yêu cầu hỗ trợ"<br>2. Kiểm tra tìm kiếm | Hiển thị Input với icon Search bên trái, placeholder "Tìm kiếm yêu cầu hỗ trợ...", pl-10 | | Pass | 11/15/2015 | |
| **GUI-QLYC-05** | Kiểm tra card yêu cầu | 1. Xem danh sách yêu cầu<br>2. Kiểm tra card | Hiển thị card với CardContent p-6, chứa tiêu đề, badge trạng thái, badge mức độ ưu tiên, thông tin thời gian, mô tả | | Pass | 11/15/2015 | |
| **GUI-QLYC-06** | Kiểm tra badge trạng thái | 1. Xem card yêu cầu<br>2. Kiểm tra badge | Hiển thị badge với màu tương ứng: Mở (yellow-500), Đang xử lý (blue-500), Đã giải quyết (green-500), Đã đóng (gray-500), có icon | | Pass | 11/15/2015 | |
| **GUI-QLYC-07** | Kiểm tra badge mức độ ưu tiên | 1. Xem card yêu cầu<br>2. Kiểm tra badge | Hiển thị badge với màu: Thấp (gray-500), Trung bình (yellow-500), Cao (orange-500), Khẩn cấp (red-500) | | Pass | 11/15/2015 | |
| **GUI-QLYC-08** | Kiểm tra phản hồi admin | 1. Xem yêu cầu đã có phản hồi<br>2. Kiểm tra phản hồi | Hiển thị phần "Phản hồi từ hỗ trợ" với icon CheckCircle, nội dung phản hồi, thời gian phản hồi | | Pass | 11/15/2015 | |
| **GUI-QLYC-09** | Kiểm tra nút Xem chi tiết | 1. Xem card yêu cầu<br>2. Kiểm tra nút | Hiển thị nút "Xem chi tiết" với icon Eye, variant outline size sm | | Pass | 11/15/2015 | |

---

### Check FUNC: Quản lý yêu cầu hỗ trợ

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-QLYC-01** | Mở tab Yêu cầu hỗ trợ | 1. Truy cập /user/support<br>2. Chọn tab "Yêu cầu hỗ trợ" | Hiển thị danh sách yêu cầu hỗ trợ, bộ lọc, ô tìm kiếm, nút tạo yêu cầu mới | | Pass | 11/15/2015 | |
| **FUNC-QLYC-02** | Hiển thị danh sách yêu cầu | 1. Chọn tab "Yêu cầu hỗ trợ" | Hiển thị danh sách tất cả yêu cầu với đầy đủ thông tin: tiêu đề, danh mục, mức độ ưu tiên, trạng thái, thời gian tạo/cập nhật, mô tả, phản hồi (nếu có) | | Pass | 11/15/2015 | |
| **FUNC-QLYC-03** | Sắp xếp theo thời gian mới nhất | 1. Chọn tab "Yêu cầu hỗ trợ" | Danh sách được sắp xếp theo thời gian tạo mới nhất trước | | Pass | 11/15/2015 | |
| **FUNC-QLYC-04** | Lọc theo trạng thái - Mở | 1. Chọn tab "Yêu cầu hỗ trợ"<br>2. Chọn bộ lọc "Mở" | Chỉ hiển thị các yêu cầu có trạng thái "Mở", cập nhật số lượng trong option | | Pass | 11/15/2015 | |
| **FUNC-QLYC-05** | Lọc theo trạng thái - Đã giải quyết | 1. Chọn tab "Yêu cầu hỗ trợ"<br>2. Chọn bộ lọc "Đã giải quyết" | Chỉ hiển thị các yêu cầu có trạng thái "Đã giải quyết" | | Pass | 11/15/2015 | |
| **FUNC-QLYC-06** | Lọc theo danh mục | 1. Chọn tab "Yêu cầu hỗ trợ"<br>2. Chọn bộ lọc danh mục (VD: "Đơn hàng") | Chỉ hiển thị các yêu cầu thuộc danh mục đã chọn | | Pass | 11/15/2015 | |
| **FUNC-QLYC-07** | Tìm kiếm theo tiêu đề | 1. Chọn tab "Yêu cầu hỗ trợ"<br>2. Nhập từ khóa vào ô tìm kiếm | Danh sách được lọc, chỉ hiển thị yêu cầu có tiêu đề chứa từ khóa | | Pass | 11/15/2015 | |
| **FUNC-QLYC-08** | Tìm kiếm theo mô tả | 1. Chọn tab "Yêu cầu hỗ trợ"<br>2. Nhập từ khóa vào ô tìm kiếm | Danh sách được lọc, chỉ hiển thị yêu cầu có mô tả chứa từ khóa | | Pass | 11/15/2015 | |
| **FUNC-QLYC-09** | Kết hợp lọc và tìm kiếm | 1. Chọn tab "Yêu cầu hỗ trợ"<br>2. Chọn bộ lọc trạng thái<br>3. Nhập từ khóa tìm kiếm | Danh sách được lọc theo cả trạng thái và từ khóa, chỉ hiển thị yêu cầu thỏa mãn cả hai điều kiện | | Pass | 11/15/2015 | |
| **FUNC-QLYC-10** | Xem chi tiết yêu cầu | 1. Chọn tab "Yêu cầu hỗ trợ"<br>2. Nhấn nút "Xem chi tiết" | Mở modal hoặc trang chi tiết với đầy đủ thông tin: tiêu đề, danh mục, mức độ ưu tiên, trạng thái, mô tả, mã đơn hàng, file đính kèm, phản hồi admin, lịch sử cập nhật | | Pass | 11/15/2015 | |
| **FUNC-QLYC-11** | Hiển thị phản hồi admin | 1. Xem yêu cầu đã có phản hồi<br>2. Kiểm tra phản hồi | Hiển thị phần "Phản hồi từ hỗ trợ" với icon CheckCircle, nội dung phản hồi, thời gian phản hồi được format đúng | | Pass | 11/15/2015 | |
| **FUNC-QLYC-12** | Hiển thị khi không có yêu cầu | 1. Chọn tab "Yêu cầu hỗ trợ"<br>2. Không có yêu cầu nào | Hiển thị thông báo "Chưa có yêu cầu hỗ trợ nào" hoặc danh sách trống | | Pass | 11/15/2015 | |
| **FUNC-QLYC-13** | Cập nhật số lượng trong tab | 1. Tạo yêu cầu mới<br>2. Kiểm tra tab | Số lượng trong tab "Yêu cầu hỗ trợ" được cập nhật tự động | | Pass | 11/15/2015 | |

---

### Function: Câu hỏi thường gặp

#### Check GUI: Câu hỏi thường gặp

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-FAQ-01** | Kiểm tra tab Câu hỏi thường gặp | 1. Truy cập /user/support<br>2. Kiểm tra tab | Hiển thị tab "Câu hỏi thường gặp" với icon HelpCircle trong TabsList | | Pass | 11/15/2015 | |
| **GUI-FAQ-02** | Kiểm tra tiêu đề FAQ | 1. Chọn tab "Câu hỏi thường gặp"<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Câu hỏi thường gặp" với icon HelpCircle, CardTitle | | Pass | 11/15/2015 | |
| **GUI-FAQ-03** | Kiểm tra ô tìm kiếm FAQ | 1. Chọn tab "Câu hỏi thường gặp"<br>2. Kiểm tra tìm kiếm | Hiển thị Input với icon Search bên trái, placeholder "Tìm kiếm câu hỏi...", pl-10 | | Pass | 11/15/2015 | |
| **GUI-FAQ-04** | Kiểm tra bộ lọc danh mục FAQ | 1. Chọn tab "Câu hỏi thường gặp"<br>2. Kiểm tra bộ lọc | Hiển thị Select với trigger w-48, các option: "Tất cả", "Đơn hàng & Thanh toán", "Vận chuyển & Giao hàng", "Tài khoản & Thành viên", "Đổi trả & Bảo hành" | | Pass | 11/15/2015 | |
| **GUI-FAQ-05** | Kiểm tra card câu hỏi | 1. Xem danh sách FAQ<br>2. Kiểm tra card | Hiển thị card với CardHeader có icon và tiêu đề danh mục, CardContent chứa các câu hỏi và câu trả lời | | Pass | 11/15/2015 | |
| **GUI-FAQ-06** | Kiểm tra câu hỏi | 1. Xem card FAQ<br>2. Kiểm tra câu hỏi | Hiển thị câu hỏi với font-medium, có thể mở rộng/thu gọn để xem câu trả lời | | Pass | 11/15/2015 | |
| **GUI-FAQ-07** | Kiểm tra câu trả lời | 1. Xem card FAQ<br>2. Mở câu hỏi<br>3. Kiểm tra câu trả lời | Hiển thị câu trả lời với text-sm text-muted-foreground, nội dung chi tiết | | Pass | 11/15/2015 | |
| **GUI-FAQ-08** | Kiểm tra nút hữu ích | 1. Xem câu hỏi FAQ<br>2. Kiểm tra nút | Hiển thị nút "Hữu ích" với icon ThumbsUp, số lượt trong ngoặc đơn | | Pass | 11/15/2015 | |
| **GUI-FAQ-09** | Kiểm tra nút liên hệ hỗ trợ | 1. Xem FAQ<br>2. Kiểm tra nút | Hiển thị nút "Liên hệ hỗ trợ" để chuyển đến chat hoặc tạo yêu cầu nếu không tìm thấy câu trả lời | | Pass | 11/15/2015 | |

---

### Check FUNC: Câu hỏi thường gặp

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-FAQ-01** | Mở tab Câu hỏi thường gặp | 1. Truy cập /user/support<br>2. Chọn tab "Câu hỏi thường gặp" | Hiển thị danh sách câu hỏi thường gặp được phân loại theo danh mục, có ô tìm kiếm và bộ lọc | | Pass | 11/15/2015 | |
| **FUNC-FAQ-02** | Hiển thị câu hỏi thường gặp | 1. Chọn tab "Câu hỏi thường gặp" | Hiển thị danh sách câu hỏi với câu trả lời chi tiết, được phân loại theo danh mục, có thể mở rộng/thu gọn từng câu hỏi | | Pass | 11/15/2015 | |
| **FUNC-FAQ-03** | Mở rộng câu hỏi | 1. Chọn tab "Câu hỏi thường gặp"<br>2. Click vào câu hỏi | Câu hỏi được mở rộng, hiển thị câu trả lời chi tiết | | Pass | 11/15/2015 | |
| **FUNC-FAQ-04** | Thu gọn câu hỏi | 1. Mở rộng câu hỏi<br>2. Click lại vào câu hỏi | Câu hỏi được thu gọn, ẩn câu trả lời | | Pass | 11/15/2015 | |
| **FUNC-FAQ-05** | Tìm kiếm câu hỏi | 1. Chọn tab "Câu hỏi thường gặp"<br>2. Nhập từ khóa vào ô tìm kiếm | Danh sách được lọc, chỉ hiển thị câu hỏi/câu trả lời chứa từ khóa, cập nhật real-time | | Pass | 11/15/2015 | |
| **FUNC-FAQ-06** | Lọc theo danh mục | 1. Chọn tab "Câu hỏi thường gặp"<br>2. Chọn danh mục trong bộ lọc | Chỉ hiển thị câu hỏi thuộc danh mục đã chọn | | Pass | 11/15/2015 | |
| **FUNC-FAQ-07** | Kết hợp tìm kiếm và lọc | 1. Chọn tab "Câu hỏi thường gặp"<br>2. Nhập từ khóa<br>3. Chọn danh mục | Danh sách được lọc theo cả từ khóa và danh mục | | Pass | 11/15/2015 | |
| **FUNC-FAQ-08** | Đánh giá câu trả lời hữu ích | 1. Xem câu hỏi FAQ<br>2. Nhấn nút "Hữu ích" | Số lượt hữu ích tăng lên, nút chuyển sang trạng thái đã nhấn, hiển thị toast cảm ơn | | Pass | 11/15/2015 | |
| **FUNC-FAQ-09** | Đánh giá câu trả lời không hữu ích | 1. Xem câu hỏi FAQ<br>2. Nhấn nút "Không hữu ích" | Số lượt không hữu ích tăng lên, hiển thị nút "Liên hệ hỗ trợ" | | Pass | 11/15/2015 | |
| **FUNC-FAQ-10** | Nhấn nút Liên hệ hỗ trợ | 1. Xem FAQ<br>2. Nhấn nút "Liên hệ hỗ trợ" | Chuyển đến tab "Chat trực tiếp" hoặc "Yêu cầu hỗ trợ" để liên hệ | | Pass | 11/15/2015 | |
| **FUNC-FAQ-11** | Hiển thị khi không có kết quả | 1. Chọn tab "Câu hỏi thường gặp"<br>2. Tìm kiếm không có kết quả | Hiển thị thông báo "Không tìm thấy câu hỏi nào", nút "Liên hệ hỗ trợ" | | Pass | 11/15/2015 | |

---

### Function: Thông tin liên hệ

#### Check GUI: Thông tin liên hệ

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-TTLH-01** | Kiểm tra card Hotline | 1. Truy cập /user/support<br>2. Kiểm tra card | Hiển thị card với icon Phone h-8 w-8 text-primary, tiêu đề "Hotline", số điện thoại "1900 1234", giờ làm việc "8:00 - 22:00 hàng ngày" | | Pass | 11/15/2015 | |
| **GUI-TTLH-02** | Kiểm tra card Email | 1. Truy cập /user/support<br>2. Kiểm tra card | Hiển thị card với icon Mail h-8 w-8 text-primary, tiêu đề "Email", địa chỉ "support@nhasach.com", mô tả "Phản hồi trong 24h" | | Pass | 11/15/2015 | |
| **GUI-TTLH-03** | Kiểm tra card Địa chỉ | 1. Truy cập /user/support<br>2. Kiểm tra card | Hiển thị card với icon MapPin h-8 w-8 text-primary, tiêu đề "Địa chỉ", địa chỉ "123 Đường ABC, Quận 1", "TP. Hồ Chí Minh" | | Pass | 11/15/2015 | |
| **GUI-TTLH-04** | Kiểm tra grid layout | 1. Truy cập /user/support<br>2. Kiểm tra layout | Hiển thị grid grid-cols-1 md:grid-cols-3 gap-6 cho 3 card thông tin liên hệ | | Pass | 11/15/2015 | |
| **GUI-TTLH-05** | Kiểm tra nút gọi điện | 1. Xem card Hotline<br>2. Kiểm tra nút | Hiển thị nút "Gọi điện" với icon Phone, có thể click để gọi trực tiếp | | Pass | 11/15/2015 | |
| **GUI-TTLH-06** | Kiểm tra nút gửi email | 1. Xem card Email<br>2. Kiểm tra nút | Hiển thị nút "Gửi email" với icon Mail, có thể click để mở ứng dụng email | | Pass | 11/15/2015 | |

---

### Check FUNC: Thông tin liên hệ

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TTLH-01** | Hiển thị thông tin liên hệ | 1. Truy cập /user/support | Hiển thị 3 card thông tin liên hệ: Hotline, Email, Địa chỉ với đầy đủ thông tin và icon | | Pass | 11/15/2015 | |
| **FUNC-TTLH-02** | Gọi điện trực tiếp | 1. Xem card Hotline<br>2. Nhấn nút "Gọi điện" | Mở ứng dụng gọi điện với số 1900 1234, có thể gọi trực tiếp | | Pass | 11/15/2015 | |
| **FUNC-TTLH-03** | Gửi email trực tiếp | 1. Xem card Email<br>2. Nhấn nút "Gửi email" | Mở ứng dụng email với địa chỉ support@nhasach.com, có thể gửi email trực tiếp | | Pass | 11/15/2015 | |
| **FUNC-TTLH-04** | Hiển thị giờ làm việc | 1. Xem card Hotline<br>2. Kiểm tra giờ làm việc | Hiển thị "8:00 - 22:00 hàng ngày" để người dùng biết thời gian có thể liên hệ | | Pass | 11/15/2015 | |
| **FUNC-TTLH-05** | Copy số điện thoại | 1. Xem card Hotline<br>2. Click vào số điện thoại | Số điện thoại được copy vào clipboard, hiển thị toast "Đã sao chép số điện thoại" | | Pass | 11/15/2015 | |
| **FUNC-TTLH-06** | Copy địa chỉ email | 1. Xem card Email<br>2. Click vào email | Email được copy vào clipboard, hiển thị toast "Đã sao chép email" | | Pass | 11/15/2015 | |
| **FUNC-TTLH-07** | Copy địa chỉ | 1. Xem card Địa chỉ<br>2. Click vào địa chỉ | Địa chỉ được copy vào clipboard, hiển thị toast "Đã sao chép địa chỉ" | | Pass | 11/15/2015 | |
| **FUNC-TTLH-08** | Kiểm tra responsive layout | 1. Truy cập /user/support<br>2. Thay đổi kích thước màn hình | Layout tự động điều chỉnh: 1 cột mobile, 3 cột desktop | | Pass | 11/15/2015 | |

---

### Check VALIDATION: Hỗ trợ - liên hệ

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **VALID-HT-01** | Gửi tin nhắn rỗng | 1. Chọn tab "Chat trực tiếp"<br>2. Để trống ô nhập<br>3. Nhấn gửi | Nút gửi bị disabled, không gửi tin nhắn | | Pass | 11/15/2015 | |
| **VALID-HT-02** | Tạo yêu cầu thiếu tiêu đề | 1. Mở modal tạo yêu cầu<br>2. Để trống tiêu đề<br>3. Nhấn "Gửi yêu cầu" | Hiển thị toast lỗi "Vui lòng nhập tiêu đề", không gửi yêu cầu | | Pass | 11/15/2015 | |
| **VALID-HT-03** | Tạo yêu cầu thiếu mô tả | 1. Mở modal tạo yêu cầu<br>2. Để trống mô tả<br>3. Nhấn "Gửi yêu cầu" | Hiển thị toast lỗi "Vui lòng nhập mô tả vấn đề", không gửi yêu cầu | | Pass | 11/15/2015 | |
| **VALID-HT-04** | Đính kèm file không hợp lệ | 1. Mở modal tạo yêu cầu<br>2. Chọn file không đúng định dạng | Hiển thị thông báo lỗi "Định dạng file không được hỗ trợ", file không được thêm | | Pass | 11/15/2015 | |
| **VALID-HT-05** | Đính kèm file quá kích thước | 1. Mở modal tạo yêu cầu<br>2. Chọn file > 10MB | Hiển thị thông báo lỗi "File quá lớn. Kích thước tối đa: 10MB", file không được thêm | | Pass | 11/15/2015 | |
| **VALID-HT-06** | Tìm kiếm với từ khóa đặc biệt | 1. Chọn tab "Yêu cầu hỗ trợ"<br>2. Nhập từ khóa có ký tự đặc biệt | Hệ thống xử lý an toàn, không gây lỗi, lọc kết quả chính xác | | Pass | 11/15/2015 | |
| **VALID-HT-07** | Gửi tin nhắn quá dài | 1. Chọn tab "Chat trực tiếp"<br>2. Nhập tin nhắn rất dài (>1000 ký tự)<br>3. Gửi tin nhắn | Tin nhắn được gửi thành công hoặc hiển thị cảnh báo nếu vượt quá giới hạn | | Pass | 11/15/2015 | |
| **VALID-HT-08** | Tạo yêu cầu với mô tả quá ngắn | 1. Mở modal tạo yêu cầu<br>2. Nhập mô tả < 10 ký tự<br>3. Nhấn "Gửi yêu cầu" | Hiển thị thông báo lỗi "Mô tả phải có ít nhất 10 ký tự" hoặc cho phép gửi | | Pass | 11/15/2015 | |

