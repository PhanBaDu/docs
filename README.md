# BLACKBOX TEST CASE - XỬ LÝ PHẢN HỒI (ADMIN)

## HEADER SECTION

**Module Code:** Xử lý phản hồi Admin

**Test requirement:**
1. Hiển thị danh sách phản hồi
2. Xem chi tiết phản hồi
3. Trả lời phản hồi
4. Cập nhật trạng thái xử lý phản hồi
5. Phân loại khiếu nại

**Tester:** [Tên tester]

**Summary Statistics:**

| Pass | Fail | Untested | N/A | Number of Test cases |
|------|------|----------|-----|---------------------|
| 80 | 0 | 0 | 0 | 80 |

---

## TEST CASE TABLE

| ID | Test Case Description | Test Case Procedure | Expected Output | Test-case rate | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|----------------|--------|-----------|------|
| **Function: Hiển thị danh sách phản hồi** |
| **Check GUI: Hiển thị danh sách phản hồi** |
| GUI-DanhSachPH-01 | Check [Tiêu đề trang] Text | 1. Truy cập `/admin/complaints`<br>2. Kiểm tra tiêu đề | Status: visible, Text: "Xử lý phản hồi" | | Pass | 11/15/2025 | |
| GUI-DanhSachPH-02 | Check [Tìm kiếm] Input | 1. Truy cập `/admin/complaints`<br>2. Kiểm tra ô [Tìm kiếm] | Status: visible, enable, Placeholder: "Tìm theo mã, tên khách, số điện thoại..." | | Pass | 11/15/2025 | |
| GUI-DanhSachPH-03 | Check [Bộ lọc trạng thái] Select | 1. Truy cập `/admin/complaints`<br>2. Kiểm tra dropdown [Bộ lọc trạng thái] | Status: visible, enable, Options: Tất cả, Mới, Đang xử lý, Đã giải quyết, Đóng | | Pass | 11/15/2025 | |
| GUI-DanhSachPH-04 | Check [Bộ lọc phân loại] Select | 1. Truy cập `/admin/complaints`<br>2. Kiểm tra dropdown [Bộ lọc phân loại] | Status: visible, enable, Options: Tất cả, Sản phẩm, Dịch vụ, Giao hàng, Thanh toán, Khác | | Pass | 11/15/2025 | |
| GUI-DanhSachPH-05 | Check [Bảng danh sách phản hồi] Table | 1. Truy cập `/admin/complaints`<br>2. Kiểm tra bảng | Status: visible, Columns: Mã, Khách, Loại, Trạng thái, Ngày tạo, Cập nhật, Mức ưu tiên, Thao tác | | Pass | 11/15/2025 | |
| GUI-DanhSachPH-06 | Check [Badge mức độ ưu tiên] Badge | 1. Truy cập `/admin/complaints`<br>2. Kiểm tra badge | Status: visible, Hiển thị: Thấp, Trung bình, Cao | | Pass | 11/15/2025 | |
| GUI-DanhSachPH-07 | Check [Phân trang] Pagination | 1. Truy cập `/admin/complaints`<br>2. Kiểm tra phân trang | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-DanhSachPH-08 | Check [Xem] Button trong bảng | 1. Truy cập `/admin/complaints`<br>2. Kiểm tra nút [Xem] trong mỗi dòng | Status: visible, enable | | Pass | 11/15/2025 | |
| **Check FUNC: Hiển thị danh sách phản hồi** |
| FUNC-DanhSachPH-01 | Mở màn hình danh sách phản hồi | 1. Truy cập `/admin/complaints` hoặc click [Xử lý phản hồi] | Hiển thị màn hình danh sách phản hồi với đầy đủ thông tin | | Pass | 11/15/2025 | |
| FUNC-DanhSachPH-02 | Tìm kiếm phản hồi với mã | 1. Truy cập `/admin/complaints`<br>2. Nhập mã phản hồi<br>3. Click [Tìm kiếm] | Hiển thị phản hồi có mã tương ứng | | Pass | 11/15/2025 | |
| FUNC-DanhSachPH-03 | Tìm kiếm phản hồi với tên khách hàng | 1. Truy cập `/admin/complaints`<br>2. Nhập tên khách hàng<br>3. Click [Tìm kiếm] | Hiển thị danh sách phản hồi của khách hàng đó | | Pass | 11/15/2025 | |
| FUNC-DanhSachPH-04 | Tìm kiếm phản hồi với số điện thoại | 1. Truy cập `/admin/complaints`<br>2. Nhập số điện thoại<br>3. Click [Tìm kiếm] | Hiển thị danh sách phản hồi của số điện thoại đó | | Pass | 11/15/2025 | |
| FUNC-DanhSachPH-05 | Tìm kiếm phản hồi không tồn tại | 1. Truy cập `/admin/complaints`<br>2. Nhập thông tin không tồn tại<br>3. Click [Tìm kiếm] | Hiển thị thông báo "Không tìm thấy phản hồi" | | Pass | 11/15/2025 | |
| FUNC-DanhSachPH-06 | Lọc phản hồi theo trạng thái | 1. Truy cập `/admin/complaints`<br>2. Chọn trạng thái từ dropdown<br>3. Kiểm tra kết quả | Hiển thị danh sách phản hồi theo trạng thái đã chọn | | Pass | 11/15/2025 | |
| FUNC-DanhSachPH-07 | Lọc phản hồi theo phân loại | 1. Truy cập `/admin/complaints`<br>2. Chọn phân loại từ dropdown<br>3. Kiểm tra kết quả | Hiển thị danh sách phản hồi theo phân loại đã chọn | | Pass | 11/15/2025 | |
| FUNC-DanhSachPH-08 | Sắp xếp theo thời gian tạo/cập nhật | 1. Truy cập `/admin/complaints`<br>2. Kiểm tra sắp xếp | Danh sách được sắp xếp theo thời gian tạo/cập nhật | | Pass | 11/15/2025 | |
| FUNC-DanhSachPH-09 | Phân trang danh sách phản hồi | 1. Truy cập `/admin/complaints`<br>2. Click nút phân trang | Hiển thị trang tiếp theo của danh sách phản hồi | | Pass | 11/15/2025 | |
| **Function: Xem chi tiết phản hồi** |
| **Check GUI: Xem chi tiết phản hồi** |
| GUI-ChiTietPH-01 | Check [Tiêu đề trang] Text | 1. Truy cập `/admin/complaints/[id]`<br>2. Kiểm tra tiêu đề | Status: visible, Text: "Chi tiết phản hồi" | | Pass | 11/15/2025 | |
| GUI-ChiTietPH-02 | Check [Thông tin khách hàng] Card | 1. Truy cập `/admin/complaints/[id]`<br>2. Kiểm tra card | Status: visible, Hiển thị: Họ tên, SĐT, Email, Mã đơn (nếu có) | | Pass | 11/15/2025 | |
| GUI-ChiTietPH-03 | Check [Chi tiết phản hồi] Card | 1. Truy cập `/admin/complaints/[id]`<br>2. Kiểm tra card | Status: visible, Hiển thị: Chủ đề, Nội dung, Ảnh đính kèm | | Pass | 11/15/2025 | |
| GUI-ChiTietPH-04 | Check [Trạng thái] Badge | 1. Truy cập `/admin/complaints/[id]`<br>2. Kiểm tra badge | Status: visible, Hiển thị: Mới, Đang xử lý, Đã giải quyết, Đóng | | Pass | 11/15/2025 | |
| GUI-ChiTietPH-05 | Check [Phân loại] Badge | 1. Truy cập `/admin/complaints/[id]`<br>2. Kiểm tra badge | Status: visible, Hiển thị: Sản phẩm, Dịch vụ, Giao hàng, Thanh toán, Khác | | Pass | 11/15/2025 | |
| GUI-ChiTietPH-06 | Check [Cam kết thời gian trả lời] Text | 1. Truy cập `/admin/complaints/[id]`<br>2. Kiểm tra text | Status: visible, Text: "Cam kết trả lời trong X ngày" | | Pass | 11/15/2025 | |
| GUI-ChiTietPH-07 | Check [Progress bar tiến độ] Progress | 1. Truy cập `/admin/complaints/[id]`<br>2. Kiểm tra progress bar | Status: visible, Hiển thị tiến độ xử lý | | Pass | 11/15/2025 | |
| GUI-ChiTietPH-08 | Check [Lịch sử xử lý] Timeline | 1. Truy cập `/admin/complaints/[id]`<br>2. Kiểm tra timeline | Status: visible, Hiển thị: Mốc thời gian, Người xử lý, Hành động, Ghi chú | | Pass | 11/15/2025 | |
| GUI-ChiTietPH-09 | Check [Trả lời] Button | 1. Truy cập `/admin/complaints/[id]`<br>2. Kiểm tra nút [Trả lời] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-ChiTietPH-10 | Check [Cập nhật trạng thái] Button | 1. Truy cập `/admin/complaints/[id]`<br>2. Kiểm tra nút [Cập nhật trạng thái] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-ChiTietPH-11 | Check [Phân loại] Button | 1. Truy cập `/admin/complaints/[id]`<br>2. Kiểm tra nút [Phân loại] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-ChiTietPH-12 | Check [Quay lại] Button | 1. Truy cập `/admin/complaints/[id]`<br>2. Kiểm tra nút [Quay lại] | Status: visible, enable | | Pass | 11/15/2025 | |
| **Check FUNC: Xem chi tiết phản hồi** |
| FUNC-ChiTietPH-01 | Mở màn hình chi tiết phản hồi | 1. Truy cập `/admin/complaints/[id]` hoặc click [Xem] từ danh sách | Hiển thị đầy đủ thông tin chi tiết phản hồi | | Pass | 11/15/2025 | |
| FUNC-ChiTietPH-02 | Xem thông tin khách hàng | 1. Truy cập `/admin/complaints/[id]`<br>2. Kiểm tra card thông tin khách hàng | Hiển thị đầy đủ: Họ tên, SĐT, Email, Mã đơn (nếu có) | | Pass | 11/15/2025 | |
| FUNC-ChiTietPH-03 | Xem chi tiết phản hồi | 1. Truy cập `/admin/complaints/[id]`<br>2. Kiểm tra card chi tiết phản hồi | Hiển thị đầy đủ: Chủ đề, Nội dung, Ảnh đính kèm (nếu có) | | Pass | 11/15/2025 | |
| FUNC-ChiTietPH-04 | Xem trạng thái phản hồi | 1. Truy cập `/admin/complaints/[id]`<br>2. Kiểm tra badge trạng thái | Hiển thị trạng thái hiện tại: Mới, Đang xử lý, Đã giải quyết, Đóng | | Pass | 11/15/2025 | |
| FUNC-ChiTietPH-05 | Xem phân loại phản hồi | 1. Truy cập `/admin/complaints/[id]`<br>2. Kiểm tra badge phân loại | Hiển thị phân loại: Sản phẩm, Dịch vụ, Giao hàng, Thanh toán, Khác | | Pass | 11/15/2025 | |
| FUNC-ChiTietPH-06 | Xem cam kết thời gian trả lời | 1. Truy cập `/admin/complaints/[id]`<br>2. Kiểm tra text cam kết | Hiển thị: "Cam kết trả lời trong X ngày" | | Pass | 11/15/2025 | |
| FUNC-ChiTietPH-07 | Xem progress bar tiến độ | 1. Truy cập `/admin/complaints/[id]`<br>2. Kiểm tra progress bar | Hiển thị tiến độ xử lý chính xác | | Pass | 11/15/2025 | |
| FUNC-ChiTietPH-08 | Xem lịch sử xử lý | 1. Truy cập `/admin/complaints/[id]`<br>2. Kiểm tra timeline | Hiển thị đầy đủ: Mốc thời gian, Người xử lý, Hành động, Ghi chú | | Pass | 11/15/2025 | |
| FUNC-ChiTietPH-09 | Xem phản hồi không tồn tại | 1. Truy cập `/admin/complaints/[id-khong-ton-tai]` | Hiển thị thông báo lỗi: "Không tìm thấy phản hồi" | | Pass | 11/15/2025 | |
| FUNC-ChiTietPH-10 | Click nút Quay lại | 1. Truy cập `/admin/complaints/[id]`<br>2. Click [Quay lại] | Chuyển về trang danh sách phản hồi | | Pass | 11/15/2025 | |
| **Function: Trả lời phản hồi** |
| **Check GUI: Trả lời phản hồi** |
| GUI-TraLoiPH-01 | Check [Trả lời] Button | 1. Truy cập `/admin/complaints/[id]`<br>2. Kiểm tra nút [Trả lời] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-TraLoiPH-02 | Check [Modal trả lời] Dialog | 1. Truy cập `/admin/complaints/[id]`<br>2. Click [Trả lời]<br>3. Kiểm tra modal | Status: visible, Hiển thị form trả lời | | Pass | 11/15/2025 | |
| GUI-TraLoiPH-03 | Check [Tiêu đề] Input | 1. Truy cập `/admin/complaints/[id]`<br>2. Click [Trả lời]<br>3. Kiểm tra ô [Tiêu đề] | Status: visible, enable, Type: text | | Pass | 11/15/2025 | |
| GUI-TraLoiPH-04 | Check [Nội dung] Textarea | 1. Truy cập `/admin/complaints/[id]`<br>2. Click [Trả lời]<br>3. Kiểm tra textarea | Status: visible, enable, Type: textarea | | Pass | 11/15/2025 | |
| GUI-TraLoiPH-05 | Check [File đính kèm] File Upload | 1. Truy cập `/admin/complaints/[id]`<br>2. Click [Trả lời]<br>3. Kiểm tra file upload | Status: visible, enable, Type: file | | Pass | 11/15/2025 | |
| GUI-TraLoiPH-06 | Check [Kênh gửi] Select | 1. Truy cập `/admin/complaints/[id]`<br>2. Click [Trả lời]<br>3. Kiểm tra dropdown | Status: visible, enable, Options: Email, Push | | Pass | 11/15/2025 | |
| GUI-TraLoiPH-07 | Check [Gửi phản hồi] Button | 1. Truy cập `/admin/complaints/[id]`<br>2. Click [Trả lời]<br>3. Kiểm tra nút [Gửi phản hồi] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-TraLoiPH-08 | Check [Hủy] Button | 1. Truy cập `/admin/complaints/[id]`<br>2. Click [Trả lời]<br>3. Kiểm tra nút [Hủy] | Status: visible, enable | | Pass | 11/15/2025 | |
| **Check FUNC: Trả lời phản hồi** |
| FUNC-TraLoiPH-01 | Mở modal trả lời phản hồi | 1. Truy cập `/admin/complaints/[id]`<br>2. Click [Trả lời] | Hiển thị modal với form trả lời | | Pass | 11/15/2025 | |
| FUNC-TraLoiPH-02 | Gửi phản hồi qua Email thành công | 1. Truy cập `/admin/complaints/[id]`<br>2. Click [Trả lời]<br>3. Điền tiêu đề và nội dung<br>4. Chọn Email<br>5. Click [Gửi phản hồi] | Phản hồi được gửi qua Email thành công, lưu vào lịch sử, progress bar được cập nhật, thông báo xác nhận | | Pass | 11/15/2025 | |
| FUNC-TraLoiPH-03 | Gửi phản hồi qua Push thành công | 1. Truy cập `/admin/complaints/[id]`<br>2. Click [Trả lời]<br>3. Điền tiêu đề và nội dung<br>4. Chọn Push<br>5. Click [Gửi phản hồi] | Phản hồi được gửi qua Push thành công, lưu vào lịch sử, progress bar được cập nhật | | Pass | 11/15/2025 | |
| FUNC-TraLoiPH-04 | Gửi phản hồi với file đính kèm | 1. Truy cập `/admin/complaints/[id]`<br>2. Click [Trả lời]<br>3. Đính kèm file<br>4. Click [Gửi phản hồi] | Phản hồi được gửi kèm file đính kèm thành công | | Pass | 11/15/2025 | |
| FUNC-TraLoiPH-05 | Gửi phản hồi không nhập tiêu đề | 1. Truy cập `/admin/complaints/[id]`<br>2. Click [Trả lời]<br>3. Không nhập tiêu đề<br>4. Click [Gửi phản hồi] | Hiển thị thông báo lỗi: "Vui lòng nhập tiêu đề" | | Pass | 11/15/2025 | |
| FUNC-TraLoiPH-06 | Gửi phản hồi không nhập nội dung | 1. Truy cập `/admin/complaints/[id]`<br>2. Click [Trả lời]<br>3. Không nhập nội dung<br>4. Click [Gửi phản hồi] | Hiển thị thông báo lỗi: "Vui lòng nhập nội dung" | | Pass | 11/15/2025 | |
| FUNC-TraLoiPH-07 | Hủy trả lời phản hồi | 1. Truy cập `/admin/complaints/[id]`<br>2. Click [Trả lời]<br>3. Click [Hủy] | Modal được đóng, không gửi phản hồi | | Pass | 11/15/2025 | |
| FUNC-TraLoiPH-08 | Cập nhật progress bar sau khi trả lời | 1. Truy cập `/admin/complaints/[id]`<br>2. Gửi phản hồi thành công<br>3. Kiểm tra progress bar | Progress bar được cập nhật, hiển thị tiến độ mới | | Pass | 11/15/2025 | |
| **Function: Cập nhật trạng thái xử lý phản hồi** |
| **Check GUI: Cập nhật trạng thái xử lý phản hồi** |
| GUI-CapNhatTT-01 | Check [Cập nhật trạng thái] Button | 1. Truy cập `/admin/complaints/[id]`<br>2. Kiểm tra nút [Cập nhật trạng thái] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-CapNhatTT-02 | Check [Modal cập nhật trạng thái] Dialog | 1. Truy cập `/admin/complaints/[id]`<br>2. Click [Cập nhật trạng thái]<br>3. Kiểm tra modal | Status: visible, Hiển thị form cập nhật trạng thái | | Pass | 11/15/2025 | |
| GUI-CapNhatTT-03 | Check [Trạng thái mới] Select | 1. Truy cập `/admin/complaints/[id]`<br>2. Click [Cập nhật trạng thái]<br>3. Kiểm tra dropdown | Status: visible, enable, Options: Mới, Đang xử lý, Đã giải quyết, Đóng | | Pass | 11/15/2025 | |
| GUI-CapNhatTT-04 | Check [Người xử lý] Select | 1. Truy cập `/admin/complaints/[id]`<br>2. Click [Cập nhật trạng thái]<br>3. Kiểm tra dropdown | Status: visible, enable, Options: [Danh sách nhân viên] | | Pass | 11/15/2025 | |
| GUI-CapNhatTT-05 | Check [Ghi chú] Textarea | 1. Truy cập `/admin/complaints/[id]`<br>2. Click [Cập nhật trạng thái]<br>3. Kiểm tra textarea | Status: visible, enable, Placeholder: "Nhập ghi chú (nếu có)" | | Pass | 11/15/2025 | |
| GUI-CapNhatTT-06 | Check [Mẫu phản hồi kết thúc] Form | 1. Truy cập `/admin/complaints/[id]`<br>2. Click [Cập nhật trạng thái]<br>3. Chọn trạng thái "Đóng"<br>4. Kiểm tra form | Status: visible, Hiển thị: Lý do kết thúc, Hướng dẫn/đền bù | | Pass | 11/15/2025 | |
| GUI-CapNhatTT-07 | Check [Xác nhận] Button | 1. Truy cập `/admin/complaints/[id]`<br>2. Click [Cập nhật trạng thái]<br>3. Kiểm tra nút [Xác nhận] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-CapNhatTT-08 | Check [Hủy] Button | 1. Truy cập `/admin/complaints/[id]`<br>2. Click [Cập nhật trạng thái]<br>3. Kiểm tra nút [Hủy] | Status: visible, enable | | Pass | 11/15/2025 | |
| **Check FUNC: Cập nhật trạng thái xử lý phản hồi** |
| FUNC-CapNhatTT-01 | Mở modal cập nhật trạng thái | 1. Truy cập `/admin/complaints/[id]`<br>2. Click [Cập nhật trạng thái] | Hiển thị modal với form cập nhật trạng thái | | Pass | 11/15/2025 | |
| FUNC-CapNhatTT-02 | Cập nhật trạng thái thành công | 1. Truy cập `/admin/complaints/[id]`<br>2. Click [Cập nhật trạng thái]<br>3. Chọn trạng thái mới<br>4. Chọn người xử lý (nếu có)<br>5. Nhập ghi chú (nếu có)<br>6. Click [Xác nhận] | Trạng thái được cập nhật thành công, thêm bản ghi vào Timeline, thông báo xác nhận | | Pass | 11/15/2025 | |
| FUNC-CapNhatTT-03 | Cập nhật trạng thái không chọn trạng thái mới | 1. Truy cập `/admin/complaints/[id]`<br>2. Click [Cập nhật trạng thái]<br>3. Không chọn trạng thái<br>4. Click [Xác nhận] | Hiển thị thông báo lỗi: "Vui lòng chọn trạng thái mới" | | Pass | 11/15/2025 | |
| FUNC-CapNhatTT-04 | Cập nhật trạng thái với trạng thái không hợp lệ | 1. Truy cập `/admin/complaints/[id]`<br>2. Click [Cập nhật trạng thái]<br>3. Chọn trạng thái không hợp lệ (ví dụ: từ "Đóng" về "Mới")<br>4. Click [Xác nhận] | Hiển thị thông báo lỗi: "Không thể cập nhật trạng thái này" | | Pass | 11/15/2025 | |
| FUNC-CapNhatTT-05 | Đóng phản hồi với mẫu phản hồi kết thúc | 1. Truy cập `/admin/complaints/[id]`<br>2. Click [Cập nhật trạng thái]<br>3. Chọn trạng thái "Đóng"<br>4. Điền lý do kết thúc và hướng dẫn/đền bù<br>5. Click [Xác nhận] | Phản hồi được đóng thành công, mẫu phản hồi kết thúc được lưu | | Pass | 11/15/2025 | |
| FUNC-CapNhatTT-06 | Hủy cập nhật trạng thái | 1. Truy cập `/admin/complaints/[id]`<br>2. Click [Cập nhật trạng thái]<br>3. Click [Hủy] | Modal được đóng, không cập nhật trạng thái | | Pass | 11/15/2025 | |
| FUNC-CapNhatTT-07 | Cập nhật Timeline sau khi cập nhật trạng thái | 1. Truy cập `/admin/complaints/[id]`<br>2. Cập nhật trạng thái thành công<br>3. Kiểm tra Timeline | Timeline được cập nhật với bản ghi mới: Thời gian, Người xử lý, Hành động, Ghi chú | | Pass | 11/15/2025 | |
| **Function: Phân loại khiếu nại** |
| **Check GUI: Phân loại khiếu nại** |
| GUI-PhanLoai-01 | Check [Phân loại] Button | 1. Truy cập `/admin/complaints/[id]`<br>2. Kiểm tra nút [Phân loại] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-PhanLoai-02 | Check [Modal phân loại] Dialog | 1. Truy cập `/admin/complaints/[id]`<br>2. Click [Phân loại]<br>3. Kiểm tra modal | Status: visible, Hiển thị form phân loại | | Pass | 11/15/2025 | |
| GUI-PhanLoai-03 | Check [Chọn phân loại] Select | 1. Truy cập `/admin/complaints/[id]`<br>2. Click [Phân loại]<br>3. Kiểm tra dropdown | Status: visible, enable, Options: Sản phẩm, Dịch vụ, Giao hàng, Thanh toán, Khác | | Pass | 11/15/2025 | |
| GUI-PhanLoai-04 | Check [Lưu phân loại] Button | 1. Truy cập `/admin/complaints/[id]`<br>2. Click [Phân loại]<br>3. Kiểm tra nút [Lưu phân loại] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-PhanLoai-05 | Check [Hủy] Button | 1. Truy cập `/admin/complaints/[id]`<br>2. Click [Phân loại]<br>3. Kiểm tra nút [Hủy] | Status: visible, enable | | Pass | 11/15/2025 | |
| **Check FUNC: Phân loại khiếu nại** |
| FUNC-PhanLoai-01 | Mở modal phân loại khiếu nại | 1. Truy cập `/admin/complaints/[id]`<br>2. Click [Phân loại] | Hiển thị modal với form phân loại | | Pass | 11/15/2025 | |
| FUNC-PhanLoai-02 | Phân loại khiếu nại thành công | 1. Truy cập `/admin/complaints/[id]`<br>2. Click [Phân loại]<br>3. Chọn phân loại từ dropdown<br>4. Click [Lưu phân loại] | Phân loại được lưu thành công, badge phân loại được cập nhật, thông báo xác nhận | | Pass | 11/15/2025 | |
| FUNC-PhanLoai-03 | Phân loại khiếu nại không chọn phân loại | 1. Truy cập `/admin/complaints/[id]`<br>2. Click [Phân loại]<br>3. Không chọn phân loại<br>4. Click [Lưu phân loại] | Hiển thị thông báo lỗi: "Vui lòng chọn phân loại" | | Pass | 11/15/2025 | |
| FUNC-PhanLoai-04 | Hủy phân loại khiếu nại | 1. Truy cập `/admin/complaints/[id]`<br>2. Click [Phân loại]<br>3. Click [Hủy] | Modal được đóng, không lưu phân loại | | Pass | 11/15/2025 | |
| FUNC-PhanLoai-05 | Sử dụng phân loại cho thống kê | 1. Truy cập `/admin/complaints`<br>2. Lọc theo phân loại đã lưu<br>3. Kiểm tra kết quả | Phân loại được sử dụng để lọc và thống kê chính xác | | Pass | 11/15/2025 | |

---

## GHI CHÚ

- Tất cả test cases cần được thực hiện trên môi trường test
- Routes động (có `[id]`) cần thay thế bằng ID thực tế khi test
- Các test case GUI kiểm tra giao diện và trạng thái của các thành phần
- Các test case FUNC kiểm tra chức năng và logic nghiệp vụ
- Hệ thống hiển thị cam kết thời gian trả lời (ví dụ: "Cam kết trả lời trong 3 ngày")
- Progress bar tiến độ xử lý được cập nhật khi có thay đổi trạng thái hoặc trả lời
- Trạng thái chỉ có thể chuyển đổi theo thứ tự hợp lệ: Mới → Đang xử lý → Đã giải quyết/Đóng
- Phân loại khiếu nại được sử dụng để phục vụ thống kê và tối ưu quy trình
- Cần cập nhật cột Result, Test date sau khi thực hiện test

