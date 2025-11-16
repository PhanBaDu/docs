# Test Case Template - Xử lý phản hồi - khiếu nại (Admin)

## Module Code
**Model Management Store: Xử lý phản hồi - khiếu nại Admin**

## Test Requirement
1. Hiển thị danh sách phản hồi
2. Xem chi tiết phản hồi
3. Trả lời phản hồi
4. Cập nhật trạng thái xử lý phản hồi
5. Phân loại khiếu nại

---

## Test Summary

### Người thực hiện Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 44 |
| **Fail** | 0 |
| **Untested** | 43 |
| **N/A** | 0 |
| **Number of Test cases** | 87 |

---

## Test Cases

### Function: Hiển thị danh sách phản hồi

#### Check GUI: Hiển thị danh sách phản hồi

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DSPH-01** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/complaints<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Xử lý phản hồi - khiếu nại" với kích thước text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-DSPH-02** | Kiểm tra mô tả chức năng | 1. Truy cập /admin/complaints<br>2. Kiểm tra mô tả | Hiển thị mô tả "Quản lý và xử lý các phản hồi, khiếu nại từ khách hàng" màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-DSPH-03** | Kiểm tra Select Bộ lọc trạng thái | 1. Truy cập /admin/complaints<br>2. Kiểm tra Select | Hiển thị Select với placeholder "Trạng thái", có các option: Tất cả, Mới, Đang xử lý, Đã giải quyết, Đóng | | Pass | 11/15/2015 | |
| **GUI-DSPH-04** | Kiểm tra Select Bộ lọc phân loại | 1. Truy cập /admin/complaints<br>2. Kiểm tra Select | Hiển thị Select với placeholder "Phân loại", có các option: Tất cả, Sản phẩm, Dịch vụ, Giao hàng, Thanh toán, Khác | | Pass | 11/15/2015 | |
| **GUI-DSPH-05** | Kiểm tra trường Tìm kiếm | 1. Truy cập /admin/complaints<br>2. Kiểm tra trường tìm kiếm | Hiển thị input với icon Search bên trái, placeholder "Tìm theo mã, tên khách, số điện thoại...", có thể nhập và nhấn Enter để tìm | | Pass | 11/15/2015 | |
| **GUI-DSPH-06** | Kiểm tra bảng danh sách phản hồi | 1. Truy cập /admin/complaints<br>2. Kiểm tra bảng | Hiển thị Table với các cột: Mã, Khách hàng, Loại, Trạng thái, Ngày tạo, Cập nhật, Mức ưu tiên, Thao tác | | Pass | 11/15/2015 | |
| **GUI-DSPH-07** | Kiểm tra cột Mã trong bảng | 1. Truy cập /admin/complaints<br>2. Kiểm tra cột Mã | Mỗi dòng hiển thị mã phản hồi (font-medium, VD: #COMP001) | | Pass | 11/15/2015 | |
| **GUI-DSPH-08** | Kiểm tra cột Khách hàng trong bảng | 1. Truy cập /admin/complaints<br>2. Kiểm tra cột Khách hàng | Hiển thị tên khách hàng (font-medium), email (text-sm muted-foreground) | | Pass | 11/15/2015 | |
| **GUI-DSPH-09** | Kiểm tra cột Loại trong bảng | 1. Truy cập /admin/complaints<br>2. Kiểm tra cột Loại | Hiển thị Badge phân loại: Sản phẩm, Dịch vụ, Giao hàng, Thanh toán, Khác | | Pass | 11/15/2015 | |
| **GUI-DSPH-10** | Kiểm tra cột Trạng thái trong bảng | 1. Truy cập /admin/complaints<br>2. Kiểm tra cột Trạng thái | Hiển thị Badge với màu tương ứng: Mới (default), Đang xử lý (secondary), Đã giải quyết (outline), Đóng (destructive) | | Pass | 11/15/2015 | |
| **GUI-DSPH-11** | Kiểm tra cột Mức ưu tiên trong bảng | 1. Truy cập /admin/complaints<br>2. Kiểm tra cột Mức ưu tiên | Hiển thị Badge với màu tương ứng: Cao (destructive), Trung bình (secondary), Thấp (outline) | | Pass | 11/15/2015 | |
| **GUI-DSPH-12** | Kiểm tra cột Thao tác trong bảng | 1. Truy cập /admin/complaints<br>2. Kiểm tra cột Thao tác | Hiển thị nút "Xem chi tiết" (icon Eye link đến /admin/complaints/[id]) | | Pass | 11/15/2015 | |
| **GUI-DSPH-13** | Kiểm tra Pagination | 1. Truy cập /admin/complaints<br>2. Kiểm tra Pagination | Hiển thị text "Hiển thị 1-X trong Y phản hồi", các nút phân trang: Trước (disabled), số trang, Sau | | Pass | 11/15/2015 | |

---

### Check FUNC: Hiển thị danh sách phản hồi

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DSPH-01** | Mở trang danh sách phản hồi | 1. Truy cập /admin/complaints | Hiển thị trang với tiêu đề, mô tả, bộ lọc trạng thái, bộ lọc phân loại, trường tìm kiếm, bảng danh sách phản hồi, pagination | | Pass | 11/15/2015 | |
| **FUNC-DSPH-02** | Hiển thị danh sách phản hồi mặc định | 1. Truy cập /admin/complaints | Hiển thị tất cả phản hồi trong bảng, mỗi phản hồi có đầy đủ thông tin: mã, khách hàng, loại, trạng thái, ngày tạo, cập nhật, mức ưu tiên, nút xem chi tiết, sắp xếp theo thời gian tạo/cập nhật mới nhất | | Pass | 11/15/2015 | |
| **FUNC-DSPH-03** | Lọc theo Trạng thái | 1. Truy cập /admin/complaints<br>2. Chọn trạng thái (VD: Mới)<br>3. Kiểm tra danh sách | Hiển thị danh sách phản hồi có trạng thái đã chọn | | Untested | 11/15/2015 | |
| **FUNC-DSPH-04** | Lọc theo Phân loại | 1. Truy cập /admin/complaints<br>2. Chọn phân loại (VD: Sản phẩm)<br>3. Kiểm tra danh sách | Hiển thị danh sách phản hồi có phân loại đã chọn | | Untested | 11/15/2015 | |
| **FUNC-DSPH-05** | Tìm kiếm phản hồi | 1. Truy cập /admin/complaints<br>2. Nhập từ khóa tìm kiếm (mã, tên khách, số điện thoại)<br>3. Nhấn Enter | Hiển thị danh sách phản hồi phù hợp với từ khóa tìm kiếm | | Untested | 11/15/2015 | |
| **FUNC-DSPH-06** | Click nút Xem chi tiết | 1. Truy cập /admin/complaints<br>2. Click nút "Xem chi tiết" của một phản hồi | Chuyển đến trang chi tiết phản hồi /admin/complaints/[id] | | Pass | 11/15/2015 | |
| **FUNC-DSPH-07** | Xử lý khi không có phản hồi | 1. Truy cập /admin/complaints<br>2. Lọc để không có phản hồi nào | Hiển thị thông báo "Không tìm thấy phản hồi nào" hoặc bảng trống | | Untested | 11/15/2015 | |
| **FUNC-DSPH-08** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/complaints<br>2. Tắt kết nối mạng | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại" | | Untested | 11/15/2015 | |
| **FUNC-DSPH-09** | Xử lý khi server lỗi | 1. Truy cập /admin/complaints<br>2. Server trả về lỗi 500 | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau" | | Untested | 11/15/2015 | |

---

### Function: Xem chi tiết phản hồi

#### Check GUI: Xem chi tiết phản hồi

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CTPH-01** | Kiểm tra nút Quay lại | 1. Truy cập /admin/complaints/[id]<br>2. Kiểm tra nút Quay lại | Hiển thị nút "Quay lại" với icon ArrowLeft variant outline size sm, link đến /admin/complaints | | Pass | 11/15/2015 | |
| **GUI-CTPH-02** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/complaints/[id]<br>2. Kiểm tra tiêu đề | Hiển thị "Phản hồi #[id]" hoặc "Chủ đề: [chủ đề]" với kích thước text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-CTPH-03** | Kiểm tra card Thông tin khách hàng | 1. Truy cập /admin/complaints/[id]<br>2. Kiểm tra card | Hiển thị card "Thông tin khách hàng" với: Họ tên (icon User), SĐT (icon Phone), Email (icon Mail), Mã đơn hàng (nếu có, icon Package) | | Pass | 11/15/2015 | |
| **GUI-CTPH-04** | Kiểm tra card Chi tiết phản hồi | 1. Truy cập /admin/complaints/[id]<br>2. Kiểm tra card | Hiển thị card "Chi tiết phản hồi" với: Chủ đề (text-xl font-bold), Nội dung (text-sm), Ảnh đính kèm (nếu có, hiển thị preview) | | Pass | 11/15/2015 | |
| **GUI-CTPH-05** | Kiểm tra Badge Trạng thái | 1. Truy cập /admin/complaints/[id]<br>2. Kiểm tra Badge | Hiển thị Badge trạng thái với màu tương ứng: Mới (default), Đang xử lý (secondary), Đã giải quyết (outline), Đóng (destructive) | | Pass | 11/15/2015 | |
| **GUI-CTPH-06** | Kiểm tra Badge Phân loại | 1. Truy cập /admin/complaints/[id]<br>2. Kiểm tra Badge | Hiển thị Badge phân loại: Sản phẩm, Dịch vụ, Giao hàng, Thanh toán, Khác | | Pass | 11/15/2015 | |
| **GUI-CTPH-07** | Kiểm tra Text Cam kết thời gian trả lời | 1. Truy cập /admin/complaints/[id]<br>2. Kiểm tra Text | Hiển thị text "Cam kết trả lời trong X ngày" (VD: "Cam kết trả lời trong 3 ngày") với icon Clock | | Pass | 11/15/2015 | |
| **GUI-CTPH-08** | Kiểm tra Progress bar tiến độ | 1. Truy cập /admin/complaints/[id]<br>2. Kiểm tra Progress bar | Hiển thị Progress bar tiến độ xử lý với phần trăm hoàn thành (VD: 50%), màu thay đổi theo tiến độ | | Pass | 11/15/2015 | |
| **GUI-CTPH-09** | Kiểm tra Timeline Lịch sử xử lý | 1. Truy cập /admin/complaints/[id]<br>2. Kiểm tra Timeline | Hiển thị Timeline "Lịch sử xử lý" với các mốc: Thời gian, Người xử lý, Hành động, Ghi chú | | Pass | 11/15/2015 | |
| **GUI-CTPH-10** | Kiểm tra nút Trả lời | 1. Truy cập /admin/complaints/[id]<br>2. Kiểm tra nút | Hiển thị nút "Trả lời" với icon Reply variant outline | | Pass | 11/15/2015 | |
| **GUI-CTPH-11** | Kiểm tra nút Cập nhật trạng thái | 1. Truy cập /admin/complaints/[id]<br>2. Kiểm tra nút | Hiển thị nút "Cập nhật trạng thái" với icon CheckCircle variant outline | | Pass | 11/15/2015 | |
| **GUI-CTPH-12** | Kiểm tra nút Phân loại | 1. Truy cập /admin/complaints/[id]<br>2. Kiểm tra nút | Hiển thị nút "Phân loại" với icon Tag variant secondary | | Pass | 11/15/2015 | |

---

### Check FUNC: Xem chi tiết phản hồi

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CTPH-01** | Mở trang chi tiết phản hồi | 1. Truy cập /admin/complaints/[id] | Hiển thị trang với nút Quay lại, tiêu đề, card Thông tin khách hàng, card Chi tiết phản hồi, Badge Trạng thái, Badge Phân loại, Text Cam kết thời gian trả lời, Progress bar tiến độ, Timeline Lịch sử xử lý, nút Trả lời, nút Cập nhật trạng thái, nút Phân loại | | Pass | 11/15/2015 | |
| **FUNC-CTPH-02** | Hiển thị đầy đủ thông tin phản hồi | 1. Truy cập /admin/complaints/[id] | Hiển thị đầy đủ nội dung, phân loại, trạng thái, lịch sử xử lý, cam kết thời gian trả lời, progress bar tiến độ xử lý, ảnh đính kèm (nếu có) | | Pass | 11/15/2015 | |
| **FUNC-CTPH-03** | Click nút Quay lại | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Quay lại" | Chuyển về trang /admin/complaints | | Pass | 11/15/2015 | |
| **FUNC-CTPH-04** | Xem ảnh đính kèm | 1. Truy cập /admin/complaints/[id]<br>2. Click vào ảnh đính kèm | Hiển thị preview ảnh hoặc mở ảnh trong tab mới | | Pass | 11/15/2015 | |
| **FUNC-CTPH-05** | Click nút Trả lời | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Trả lời" | Mở modal trả lời phản hồi | | Pass | 11/15/2015 | |
| **FUNC-CTPH-06** | Click nút Cập nhật trạng thái | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Cập nhật trạng thái" | Mở modal cập nhật trạng thái xử lý | | Pass | 11/15/2015 | |
| **FUNC-CTPH-07** | Click nút Phân loại | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Phân loại" | Mở modal phân loại khiếu nại | | Pass | 11/15/2015 | |
| **FUNC-CTPH-08** | Xử lý khi phản hồi không tồn tại | 1. Truy cập /admin/complaints/[id không tồn tại] | Hiển thị thông báo lỗi "Phản hồi không tồn tại" hoặc chuyển về trang danh sách | | Untested | 11/15/2015 | |
| **FUNC-CTPH-09** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/complaints/[id]<br>2. Tắt kết nối mạng | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại" | | Untested | 11/15/2015 | |
| **FUNC-CTPH-10** | Xử lý khi server lỗi | 1. Truy cập /admin/complaints/[id]<br>2. Server trả về lỗi 500 | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau" | | Untested | 11/15/2015 | |

---

### Function: Trả lời phản hồi

#### Check GUI: Trả lời phản hồi

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-TLPH-01** | Kiểm tra modal Trả lời phản hồi | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Trả lời"<br>3. Kiểm tra modal | Hiển thị Dialog với tiêu đề "Trả lời phản hồi", mô tả "Gửi phản hồi đến khách hàng" | | Pass | 11/15/2015 | |
| **GUI-TLPH-02** | Kiểm tra trường Tiêu đề | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Trả lời"<br>3. Kiểm tra trường | Hiển thị label "Tiêu đề *", input type text với giá trị mặc định là "Re: [chủ đề gốc]" | | Pass | 11/15/2015 | |
| **GUI-TLPH-03** | Kiểm tra Textarea Nội dung | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Trả lời"<br>3. Kiểm tra Textarea | Hiển thị label "Nội dung *", Textarea với placeholder "Nhập nội dung trả lời...", rows 6 | | Pass | 11/15/2015 | |
| **GUI-TLPH-04** | Kiểm tra nút Đính kèm file | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Trả lời"<br>3. Kiểm tra nút | Hiển thị nút "Đính kèm file" với icon Paperclip | | Pass | 11/15/2015 | |
| **GUI-TLPH-05** | Kiểm tra Select Kênh gửi | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Trả lời"<br>3. Kiểm tra Select | Hiển thị label "Kênh gửi *", Select với placeholder "Chọn kênh gửi", có các option: Email, Push, có thể chọn nhiều | | Pass | 11/15/2015 | |
| **GUI-TLPH-06** | Kiểm tra nút Hủy | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Trả lời"<br>3. Kiểm tra nút | Hiển thị nút "Hủy" variant outline | | Pass | 11/15/2015 | |
| **GUI-TLPH-07** | Kiểm tra nút Gửi phản hồi | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Trả lời"<br>3. Kiểm tra nút | Hiển thị nút "Gửi phản hồi" type submit | | Pass | 11/15/2015 | |

---

### Check FUNC: Trả lời phản hồi

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TLPH-01** | Mở modal trả lời phản hồi | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Trả lời" | Hiển thị Dialog với tiêu đề "Trả lời phản hồi", mô tả, trường Tiêu đề (có giá trị mặc định), Textarea Nội dung, nút Đính kèm file, Select Kênh gửi, nút Hủy, nút Gửi phản hồi | | Pass | 11/15/2015 | |
| **FUNC-TLPH-02** | Trả lời phản hồi thành công | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Trả lời"<br>3. Điều chỉnh tiêu đề (nếu cần)<br>4. Nhập nội dung trả lời<br>5. Chọn kênh gửi (Email, Push)<br>6. Đính kèm file (tùy chọn)<br>7. Click "Gửi phản hồi" | Hiển thị thông báo "Gửi phản hồi thành công", phản hồi được gửi đến khách hàng qua các kênh đã chọn, bản sao được lưu vào lịch sử, progress bar tiến độ được cập nhật, modal đóng | | Untested | 11/15/2015 | |
| **FUNC-TLPH-03** | Trả lời - Thiếu Tiêu đề | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Trả lời"<br>3. Xóa tiêu đề<br>4. Click "Gửi phản hồi" | Hiển thị thông báo lỗi "Tiêu đề không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-TLPH-04** | Trả lời - Thiếu Nội dung | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Trả lời"<br>3. Để trống nội dung<br>4. Click "Gửi phản hồi" | Hiển thị thông báo lỗi "Nội dung không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-TLPH-05** | Trả lời - Thiếu Kênh gửi | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Trả lời"<br>3. Không chọn kênh gửi<br>4. Click "Gửi phản hồi" | Hiển thị thông báo lỗi "Vui lòng chọn ít nhất một kênh gửi", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-TLPH-06** | Trả lời - Đính kèm file | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Trả lời"<br>3. Nhập nội dung<br>4. Click "Đính kèm file"<br>5. Chọn file<br>6. Click "Gửi phản hồi" | File được đính kèm, hiển thị tên file, file được gửi cùng phản hồi | | Untested | 11/15/2015 | |
| **FUNC-TLPH-07** | Click nút Hủy | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Trả lời"<br>3. Click "Hủy" | Modal đóng, không gửi phản hồi | | Pass | 11/15/2015 | |
| **FUNC-TLPH-08** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Trả lời"<br>3. Điền đầy đủ thông tin<br>4. Tắt kết nối mạng<br>5. Click "Gửi phản hồi" | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", form không được gửi | | Untested | 11/15/2015 | |
| **FUNC-TLPH-09** | Xử lý khi server lỗi | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Trả lời"<br>3. Điền đầy đủ thông tin<br>4. Server trả về lỗi 500<br>5. Click "Gửi phản hồi" | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau", form không được gửi | | Untested | 11/15/2015 | |

---

### Function: Cập nhật trạng thái xử lý phản hồi

#### Check GUI: Cập nhật trạng thái xử lý phản hồi

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CNTTXLP-01** | Kiểm tra modal Cập nhật trạng thái | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Cập nhật trạng thái"<br>3. Kiểm tra modal | Hiển thị Dialog với tiêu đề "Cập nhật trạng thái xử lý", mô tả "Thay đổi trạng thái xử lý phản hồi" | | Pass | 11/15/2015 | |
| **GUI-CNTTXLP-02** | Kiểm tra trường Trạng thái hiện tại | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Cập nhật trạng thái"<br>3. Kiểm tra trường | Hiển thị label "Trạng thái hiện tại", Display hiển thị trạng thái hiện tại với Badge và màu tương ứng | | Pass | 11/15/2015 | |
| **GUI-CNTTXLP-03** | Kiểm tra Select Trạng thái mới | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Cập nhật trạng thái"<br>3. Kiểm tra Select | Hiển thị label "Trạng thái mới *", Select với placeholder "Chọn trạng thái mới", có các option: Mới, Đang xử lý, Đã giải quyết, Đóng | | Pass | 11/15/2015 | |
| **GUI-CNTTXLP-04** | Kiểm tra trường Người xử lý | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Cập nhật trạng thái"<br>3. Kiểm tra trường | Hiển thị label "Người xử lý", Select với placeholder "Chọn người xử lý...", có danh sách nhân viên | | Pass | 11/15/2015 | |
| **GUI-CNTTXLP-05** | Kiểm tra Textarea Ghi chú | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Cập nhật trạng thái"<br>3. Kiểm tra Textarea | Hiển thị label "Ghi chú", Textarea với placeholder "Nhập ghi chú thay đổi trạng thái (tùy chọn)" | | Pass | 11/15/2015 | |
| **GUI-CNTTXLP-06** | Kiểm tra Form Mẫu phản hồi kết thúc | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Cập nhật trạng thái"<br>3. Chọn trạng thái "Đóng"<br>4. Kiểm tra Form | Hiển thị Form "Mẫu phản hồi kết thúc" với: label "Lý do kết thúc *", Textarea, label "Hướng dẫn/đền bù (nếu có)", Textarea | | Pass | 11/15/2015 | |
| **GUI-CNTTXLP-07** | Kiểm tra nút Hủy | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Cập nhật trạng thái"<br>3. Kiểm tra nút | Hiển thị nút "Hủy" variant outline | | Pass | 11/15/2015 | |
| **GUI-CNTTXLP-08** | Kiểm tra nút Cập nhật trạng thái | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Cập nhật trạng thái"<br>3. Kiểm tra nút | Hiển thị nút "Cập nhật trạng thái" type submit | | Pass | 11/15/2015 | |

---

### Check FUNC: Cập nhật trạng thái xử lý phản hồi

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CNTTXLP-01** | Mở modal cập nhật trạng thái | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Cập nhật trạng thái" | Hiển thị Dialog với tiêu đề "Cập nhật trạng thái xử lý", mô tả, trường Trạng thái hiện tại, Select Trạng thái mới, Select Người xử lý, Textarea Ghi chú, nút Hủy, nút Cập nhật trạng thái | | Pass | 11/15/2015 | |
| **FUNC-CNTTXLP-02** | Cập nhật trạng thái thành công | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Cập nhật trạng thái"<br>3. Chọn trạng thái mới<br>4. Chọn người xử lý<br>5. Nhập ghi chú (tùy chọn)<br>6. Click "Cập nhật trạng thái" | Hiển thị thông báo "Cập nhật trạng thái thành công", trạng thái phản hồi được cập nhật, bản ghi được thêm vào Timeline, progress bar tiến độ được cập nhật, modal đóng | | Untested | 11/15/2015 | |
| **FUNC-CNTTXLP-03** | Cập nhật - Thiếu Trạng thái mới | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Cập nhật trạng thái"<br>3. Không chọn trạng thái mới<br>4. Click "Cập nhật trạng thái" | Hiển thị thông báo lỗi "Vui lòng chọn trạng thái mới", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-CNTTXLP-04** | Cập nhật - Chọn trạng thái giống hiện tại | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Cập nhật trạng thái"<br>3. Chọn trạng thái mới giống trạng thái hiện tại<br>4. Click "Cập nhật trạng thái" | Hiển thị thông báo lỗi "Trạng thái mới phải khác trạng thái hiện tại", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-CNTTXLP-05** | Đóng phản hồi - Thiếu Lý do kết thúc | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Cập nhật trạng thái"<br>3. Chọn trạng thái "Đóng"<br>4. Để trống Lý do kết thúc<br>5. Click "Cập nhật trạng thái" | Hiển thị thông báo lỗi "Lý do kết thúc không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-CNTTXLP-06** | Đóng phản hồi thành công | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Cập nhật trạng thái"<br>3. Chọn trạng thái "Đóng"<br>4. Nhập lý do kết thúc<br>5. Nhập hướng dẫn/đền bù (tùy chọn)<br>6. Click "Cập nhật trạng thái" | Hiển thị thông báo "Cập nhật trạng thái thành công", trạng thái chuyển thành "Đóng", bản ghi được thêm vào Timeline, modal đóng | | Untested | 11/15/2015 | |
| **FUNC-CNTTXLP-07** | Click nút Hủy | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Cập nhật trạng thái"<br>3. Click "Hủy" | Modal đóng, trạng thái không được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-CNTTXLP-08** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Cập nhật trạng thái"<br>3. Chọn trạng thái mới<br>4. Tắt kết nối mạng<br>5. Click "Cập nhật trạng thái" | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", form không được gửi | | Untested | 11/15/2015 | |
| **FUNC-CNTTXLP-09** | Xử lý khi server lỗi | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Cập nhật trạng thái"<br>3. Chọn trạng thái mới<br>4. Server trả về lỗi 500<br>5. Click "Cập nhật trạng thái" | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau", form không được gửi | | Untested | 11/15/2015 | |

---

### Function: Phân loại khiếu nại

#### Check GUI: Phân loại khiếu nại

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-PLKN-01** | Kiểm tra modal Phân loại khiếu nại | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Phân loại"<br>3. Kiểm tra modal | Hiển thị Dialog với tiêu đề "Phân loại khiếu nại", mô tả "Gắn nhãn/nhóm để phân tích & báo cáo" | | Pass | 11/15/2015 | |
| **GUI-PLKN-02** | Kiểm tra Select Chọn phân loại | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Phân loại"<br>3. Kiểm tra Select | Hiển thị label "Chọn phân loại *", Select với placeholder "Chọn phân loại...", có các option: Sản phẩm, Dịch vụ, Giao hàng, Thanh toán, Khác | | Pass | 11/15/2015 | |
| **GUI-PLKN-03** | Kiểm tra nút Hủy | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Phân loại"<br>3. Kiểm tra nút | Hiển thị nút "Hủy" variant outline | | Pass | 11/15/2015 | |
| **GUI-PLKN-04** | Kiểm tra nút Lưu phân loại | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Phân loại"<br>3. Kiểm tra nút | Hiển thị nút "Lưu phân loại" type submit | | Pass | 11/15/2015 | |

---

### Check FUNC: Phân loại khiếu nại

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-PLKN-01** | Mở modal phân loại khiếu nại | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Phân loại" | Hiển thị Dialog với tiêu đề "Phân loại khiếu nại", mô tả, Select Chọn phân loại, nút Hủy, nút Lưu phân loại | | Pass | 11/15/2015 | |
| **FUNC-PLKN-02** | Phân loại khiếu nại thành công | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Phân loại"<br>3. Chọn phân loại (VD: Sản phẩm)<br>4. Click "Lưu phân loại" | Hiển thị thông báo "Lưu phân loại thành công", phân loại được lưu, Badge phân loại được cập nhật, có thể xuất báo cáo theo phân loại, modal đóng | | Untested | 11/15/2015 | |
| **FUNC-PLKN-03** | Phân loại - Thiếu Chọn phân loại | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Phân loại"<br>3. Không chọn phân loại<br>4. Click "Lưu phân loại" | Hiển thị thông báo lỗi "Vui lòng chọn phân loại", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-PLKN-04** | Click nút Hủy | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Phân loại"<br>3. Click "Hủy" | Modal đóng, phân loại không được lưu | | Pass | 11/15/2015 | |
| **FUNC-PLKN-05** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Phân loại"<br>3. Chọn phân loại<br>4. Tắt kết nối mạng<br>5. Click "Lưu phân loại" | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", form không được gửi | | Untested | 11/15/2015 | |
| **FUNC-PLKN-06** | Xử lý khi server lỗi | 1. Truy cập /admin/complaints/[id]<br>2. Click nút "Phân loại"<br>3. Chọn phân loại<br>4. Server trả về lỗi 500<br>5. Click "Lưu phân loại" | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau", form không được gửi | | Untested | 11/15/2015 | |

---

**Người tạo:** Testing Team  
**Ngày cập nhật:** 11/15/2015  
**Phiên bản:** 1.0

