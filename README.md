# Test Case Template - Yêu cầu đặt hàng (Admin)

## Module Code
**Model Management Store: Yêu cầu đặt hàng Admin**

## Test Requirement
1. Hiển thị danh sách yêu cầu đặt hàng
2. Xem chi tiết yêu cầu đặt hàng
3. Xử lý yêu cầu đặt hàng
4. Cập nhật trạng thái yêu cầu đặt hàng

---

## Test Summary

### Người thực hiện Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 56 |
| **Fail** | 0 |
| **Untested** | 46 |
| **N/A** | 0 |
| **Number of Test cases** | 102 |

---

## Test Cases

### Function: Hiển thị danh sách yêu cầu đặt hàng

#### Check GUI: Hiển thị danh sách yêu cầu đặt hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DSYCDH-01** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/special-requests<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Xử lý yêu cầu khách hàng" với kích thước text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-DSYCDH-02** | Kiểm tra mô tả chức năng | 1. Truy cập /admin/special-requests<br>2. Kiểm tra mô tả | Hiển thị mô tả "Hiển thị danh sách các yêu cầu tìm mô hình từ khách hàng" màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-DSYCDH-03** | Kiểm tra Stats Cards | 1. Truy cập /admin/special-requests<br>2. Kiểm tra Stats Cards | Hiển thị 4 card thống kê: Tổng yêu cầu, Mới, Đang xử lý, Đã hoàn thành | | Pass | 11/15/2015 | |
| **GUI-DSYCDH-04** | Kiểm tra trường Tìm kiếm | 1. Truy cập /admin/special-requests<br>2. Kiểm tra trường tìm kiếm | Hiển thị input với icon Search bên trái, placeholder "Tìm kiếm yêu cầu theo ID, tên khách hàng, hoặc mô hình yêu cầu...", có thể nhập và nhấn Enter để tìm | | Pass | 11/15/2015 | |
| **GUI-DSYCDH-05** | Kiểm tra Select Trạng thái | 1. Truy cập /admin/special-requests<br>2. Kiểm tra Select Trạng thái | Hiển thị Select với placeholder "Trạng thái", width w-40, có các option: Tất cả, Mới, Đang xử lý, Đã hoàn thành, Đã hủy | | Pass | 11/15/2015 | |
| **GUI-DSYCDH-06** | Kiểm tra Select Độ ưu tiên | 1. Truy cập /admin/special-requests<br>2. Kiểm tra Select | Hiển thị Select với placeholder "Độ ưu tiên", width w-40, có các option: Tất cả, Cao, Trung bình, Thấp | | Pass | 11/15/2015 | |
| **GUI-DSYCDH-07** | Kiểm tra Date Range | 1. Truy cập /admin/special-requests<br>2. Kiểm tra Date Range | Hiển thị 2 input date với text "đến" ở giữa, width w-40 mỗi input | | Pass | 11/15/2015 | |
| **GUI-DSYCDH-08** | Kiểm tra nút Bộ lọc | 1. Truy cập /admin/special-requests<br>2. Kiểm tra nút | Hiển thị nút "Bộ lọc" với icon Filter variant outline | | Pass | 11/15/2015 | |
| **GUI-DSYCDH-09** | Kiểm tra bảng danh sách yêu cầu | 1. Truy cập /admin/special-requests<br>2. Kiểm tra bảng | Hiển thị Table với các cột: ID Yêu cầu, Khách hàng, Mô hình yêu cầu, Ngày gửi, Trạng thái, Độ ưu tiên, Nhân viên phụ trách, Thao tác | | Pass | 11/15/2015 | |
| **GUI-DSYCDH-10** | Kiểm tra cột ID Yêu cầu trong bảng | 1. Truy cập /admin/special-requests<br>2. Kiểm tra cột ID Yêu cầu | Mỗi dòng hiển thị ID yêu cầu (font-medium, VD: REQ001) | | Pass | 11/15/2015 | |
| **GUI-DSYCDH-11** | Kiểm tra cột Khách hàng trong bảng | 1. Truy cập /admin/special-requests<br>2. Kiểm tra cột Khách hàng | Hiển thị tên khách hàng (font-medium), email (text-sm muted-foreground), số điện thoại (text-sm muted-foreground) | | Pass | 11/15/2015 | |
| **GUI-DSYCDH-12** | Kiểm tra cột Mô hình yêu cầu trong bảng | 1. Truy cập /admin/special-requests<br>2. Kiểm tra cột Mô hình yêu cầu | Hiển thị mô tả mô hình yêu cầu (font-medium) | | Pass | 11/15/2015 | |
| **GUI-DSYCDH-13** | Kiểm tra cột Ngày gửi trong bảng | 1. Truy cập /admin/special-requests<br>2. Kiểm tra cột Ngày gửi | Hiển thị ngày gửi yêu cầu (text-sm) | | Pass | 11/15/2015 | |
| **GUI-DSYCDH-14** | Kiểm tra cột Trạng thái trong bảng | 1. Truy cập /admin/special-requests<br>2. Kiểm tra cột Trạng thái | Hiển thị Badge với icon và màu tương ứng: Mới (Star icon màu xanh, default), Đang xử lý (Clock icon màu vàng, secondary), Đã hoàn thành (CheckCircle icon màu xanh lá, outline), Đã hủy (XCircle icon màu đỏ, destructive) | | Pass | 11/15/2015 | |
| **GUI-DSYCDH-15** | Kiểm tra cột Độ ưu tiên trong bảng | 1. Truy cập /admin/special-requests<br>2. Kiểm tra cột Độ ưu tiên | Hiển thị Badge với icon và màu tương ứng: Cao (AlertTriangle icon màu đỏ, destructive), Trung bình (Clock icon màu vàng, secondary), Thấp (CheckCircle icon màu xanh lá, outline) | | Pass | 11/15/2015 | |
| **GUI-DSYCDH-16** | Kiểm tra cột Nhân viên phụ trách trong bảng | 1. Truy cập /admin/special-requests<br>2. Kiểm tra cột | Hiển thị icon User và tên nhân viên (text-sm) nếu đã gán, hoặc text "Chưa gán" (text-sm muted-foreground) nếu chưa gán | | Pass | 11/15/2015 | |
| **GUI-DSYCDH-17** | Kiểm tra cột Thao tác trong bảng | 1. Truy cập /admin/special-requests<br>2. Kiểm tra cột Thao tác | Hiển thị 5 nút: Xem (icon Eye link đến /admin/special-requests/[id]), Cập nhật trạng thái (icon CheckCircle), Phản hồi (icon MessageSquare), Gán nhân viên (icon User), Xóa (icon Trash2), tất cả variant ghost size sm | | Pass | 11/15/2015 | |
| **GUI-DSYCDH-18** | Kiểm tra Pagination | 1. Truy cập /admin/special-requests<br>2. Kiểm tra Pagination | Hiển thị text "Hiển thị 1-X trong Y yêu cầu", các nút phân trang: Trước (disabled), số trang, Sau | | Pass | 11/15/2015 | |

---

### Check FUNC: Hiển thị danh sách yêu cầu đặt hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DSYCDH-01** | Mở trang danh sách yêu cầu đặt hàng | 1. Truy cập /admin/special-requests | Hiển thị trang với tiêu đề, mô tả, 4 Stats Cards, bộ lọc (tìm kiếm, trạng thái, độ ưu tiên, date range, nút Bộ lọc), bảng danh sách yêu cầu, pagination | | Pass | 11/15/2015 | |
| **FUNC-DSYCDH-02** | Hiển thị danh sách yêu cầu mặc định | 1. Truy cập /admin/special-requests | Hiển thị tất cả yêu cầu trong bảng, mỗi yêu cầu có đầy đủ thông tin: ID yêu cầu, khách hàng, mô hình yêu cầu, ngày gửi, trạng thái, độ ưu tiên, nhân viên phụ trách, các nút thao tác | | Pass | 11/15/2015 | |
| **FUNC-DSYCDH-03** | Click nút Xem (icon Eye) | 1. Truy cập /admin/special-requests<br>2. Click nút Xem của một yêu cầu | Chuyển đến trang chi tiết yêu cầu /admin/special-requests/[id] | | Pass | 11/15/2015 | |
| **FUNC-DSYCDH-04** | Click nút Cập nhật trạng thái (icon CheckCircle) | 1. Truy cập /admin/special-requests<br>2. Click nút Cập nhật trạng thái của một yêu cầu | Hiển thị thông báo "Cập nhật trạng thái thành công" hoặc mở modal cập nhật trạng thái | | Pass | 11/15/2015 | |
| **FUNC-DSYCDH-05** | Click nút Phản hồi (icon MessageSquare) | 1. Truy cập /admin/special-requests<br>2. Click nút Phản hồi của một yêu cầu | Mở modal phản hồi khách hàng | | Pass | 11/15/2015 | |
| **FUNC-DSYCDH-06** | Click nút Gán nhân viên (icon User) | 1. Truy cập /admin/special-requests<br>2. Click nút Gán nhân viên của một yêu cầu | Mở modal gán nhân viên phụ trách | | Pass | 11/15/2015 | |
| **FUNC-DSYCDH-07** | Click nút Xóa (icon Trash2) | 1. Truy cập /admin/special-requests<br>2. Click nút Xóa của một yêu cầu | Hiển thị thông báo "Xóa yêu cầu thành công" hoặc mở dialog xác nhận xóa | | Pass | 11/15/2015 | |
| **FUNC-DSYCDH-08** | Lọc theo Trạng thái | 1. Truy cập /admin/special-requests<br>2. Chọn trạng thái (VD: Mới)<br>3. Click "Bộ lọc" | Hiển thị danh sách yêu cầu có trạng thái đã chọn, Stats Cards được cập nhật | | Untested | 11/15/2015 | |
| **FUNC-DSYCDH-09** | Lọc theo Độ ưu tiên | 1. Truy cập /admin/special-requests<br>2. Chọn độ ưu tiên (VD: Cao)<br>3. Click "Bộ lọc" | Hiển thị danh sách yêu cầu có độ ưu tiên đã chọn | | Untested | 11/15/2015 | |
| **FUNC-DSYCDH-10** | Lọc theo Date Range | 1. Truy cập /admin/special-requests<br>2. Chọn khoảng ngày gửi<br>3. Click "Bộ lọc" | Hiển thị danh sách yêu cầu gửi trong khoảng ngày đã chọn | | Untested | 11/15/2015 | |
| **FUNC-DSYCDH-11** | Tìm kiếm yêu cầu | 1. Truy cập /admin/special-requests<br>2. Nhập từ khóa tìm kiếm (ID, tên khách hàng hoặc mô hình yêu cầu)<br>3. Nhấn Enter hoặc click "Bộ lọc" | Hiển thị danh sách yêu cầu phù hợp với từ khóa tìm kiếm | | Untested | 11/15/2015 | |
| **FUNC-DSYCDH-12** | Xử lý khi không có yêu cầu | 1. Truy cập /admin/special-requests<br>2. Lọc để không có yêu cầu nào | Hiển thị thông báo "Không tìm thấy yêu cầu nào" hoặc bảng trống | | Untested | 11/15/2015 | |
| **FUNC-DSYCDH-13** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/special-requests<br>2. Tắt kết nối mạng | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại" | | Untested | 11/15/2015 | |
| **FUNC-DSYCDH-14** | Xử lý khi server lỗi | 1. Truy cập /admin/special-requests<br>2. Server trả về lỗi 500 | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau" | | Untested | 11/15/2015 | |

---

### Function: Xem chi tiết yêu cầu đặt hàng

#### Check GUI: Xem chi tiết yêu cầu đặt hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CTYCDH-01** | Kiểm tra nút Quay lại | 1. Truy cập /admin/special-requests/[id]<br>2. Kiểm tra nút Quay lại | Hiển thị nút "Quay lại" với icon ArrowLeft variant outline size sm, link đến /admin/special-requests | | Pass | 11/15/2015 | |
| **GUI-CTYCDH-02** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/special-requests/[id]<br>2. Kiểm tra tiêu đề | Hiển thị "Yêu cầu #[id]" với kích thước text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-CTYCDH-03** | Kiểm tra mô tả trang | 1. Truy cập /admin/special-requests/[id]<br>2. Kiểm tra mô tả | Hiển thị "Chi tiết yêu cầu đặt hàng" màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-CTYCDH-04** | Kiểm tra Badge trạng thái | 1. Truy cập /admin/special-requests/[id]<br>2. Kiểm tra Badge | Hiển thị Badge trạng thái với icon và màu tương ứng: Mới (Star icon màu xanh, default), Đang xử lý (Clock icon màu vàng, secondary), Đã hoàn thành (CheckCircle icon màu xanh lá, outline), Đã hủy (XCircle icon màu đỏ, destructive) | | Pass | 11/15/2015 | |
| **GUI-CTYCDH-05** | Kiểm tra Badge độ ưu tiên | 1. Truy cập /admin/special-requests/[id]<br>2. Kiểm tra Badge | Hiển thị Badge độ ưu tiên với icon và màu tương ứng: Cao (AlertTriangle icon màu đỏ, destructive), Trung bình (Clock icon màu vàng, secondary), Thấp (CheckCircle icon màu xanh lá, outline) | | Pass | 11/15/2015 | |
| **GUI-CTYCDH-06** | Kiểm tra nút Cập nhật trạng thái | 1. Truy cập /admin/special-requests/[id]<br>2. Kiểm tra nút | Hiển thị nút "Cập nhật trạng thái" với icon CheckCircle variant outline | | Pass | 11/15/2015 | |
| **GUI-CTYCDH-07** | Kiểm tra nút Phản hồi khách hàng | 1. Truy cập /admin/special-requests/[id]<br>2. Kiểm tra nút | Hiển thị nút "Phản hồi khách hàng" với icon MessageSquare variant secondary | | Pass | 11/15/2015 | |
| **GUI-CTYCDH-08** | Kiểm tra nút Gán nhân viên | 1. Truy cập /admin/special-requests/[id]<br>2. Kiểm tra nút | Hiển thị nút "Gán nhân viên" với icon User variant outline | | Pass | 11/15/2015 | |
| **GUI-CTYCDH-09** | Kiểm tra nút Tìm sản phẩm | 1. Truy cập /admin/special-requests/[id]<br>2. Kiểm tra nút | Hiển thị nút "Tìm sản phẩm" với icon Search variant outline | | Pass | 11/15/2015 | |
| **GUI-CTYCDH-10** | Kiểm tra card Thông tin yêu cầu | 1. Truy cập /admin/special-requests/[id]<br>2. Kiểm tra card | Hiển thị card "Thông tin yêu cầu" với: ID Yêu cầu, Ngày gửi (icon Calendar), Trạng thái (Badge), Độ ưu tiên (Badge) | | Pass | 11/15/2015 | |
| **GUI-CTYCDH-11** | Kiểm tra card Thông tin khách hàng | 1. Truy cập /admin/special-requests/[id]<br>2. Kiểm tra card | Hiển thị card "Thông tin khách hàng" với: Tên khách hàng (icon User), Email (icon Mail), Số điện thoại (icon Phone), Địa chỉ (icon MapPin) | | Pass | 11/15/2015 | |
| **GUI-CTYCDH-12** | Kiểm tra card Mô tả mô hình yêu cầu | 1. Truy cập /admin/special-requests/[id]<br>2. Kiểm tra card | Hiển thị card "Mô tả mô hình yêu cầu" với Textarea hiển thị mô tả chi tiết về mô hình mà khách hàng đang tìm kiếm | | Pass | 11/15/2015 | |
| **GUI-CTYCDH-13** | Kiểm tra card Thông tin bổ sung | 1. Truy cập /admin/special-requests/[id]<br>2. Kiểm tra card | Hiển thị card "Thông tin bổ sung" với: Thương hiệu (icon Package), Tỷ lệ, Màu sắc, Giá dự kiến (icon DollarSign), Thời gian cần (icon Clock) | | Pass | 11/15/2015 | |
| **GUI-CTYCDH-14** | Kiểm tra card Ghi chú nội bộ Admin | 1. Truy cập /admin/special-requests/[id]<br>2. Kiểm tra card | Hiển thị card "Ghi chú nội bộ Admin" với Textarea hiển thị ghi chú hiện tại, nút "Thêm ghi chú" hoặc "Cập nhật ghi chú" | | Pass | 11/15/2015 | |
| **GUI-CTYCDH-15** | Kiểm tra card Nhân viên phụ trách | 1. Truy cập /admin/special-requests/[id]<br>2. Kiểm tra card | Hiển thị card "Nhân viên phụ trách" với: Tên nhân viên (icon User), Email, Số điện thoại, Ngày gán (icon Calendar) hoặc text "Chưa gán" nếu chưa có nhân viên | | Pass | 11/15/2015 | |
| **GUI-CTYCDH-16** | Kiểm tra card Lịch sử xử lý | 1. Truy cập /admin/special-requests/[id]<br>2. Kiểm tra card | Hiển thị card "Lịch sử xử lý" với Table hiển thị các cột: Thời gian, Người xử lý, Hành động, Ghi chú | | Pass | 11/15/2015 | |
| **GUI-CTYCDH-17** | Kiểm tra card Tệp đính kèm | 1. Truy cập /admin/special-requests/[id]<br>2. Kiểm tra card | Hiển thị card "Tệp đính kèm" với danh sách các hình ảnh hoặc tài liệu khách hàng đã gửi kèm, có thể xem preview hoặc tải về | | Pass | 11/15/2015 | |

---

### Check FUNC: Xem chi tiết yêu cầu đặt hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CTYCDH-01** | Mở trang chi tiết yêu cầu | 1. Truy cập /admin/special-requests/[id] | Hiển thị trang với nút Quay lại, tiêu đề "Yêu cầu #[id]", mô tả, Badge trạng thái, Badge độ ưu tiên, các nút thao tác, card Thông tin yêu cầu, card Thông tin khách hàng, card Mô tả mô hình yêu cầu, card Thông tin bổ sung, card Ghi chú nội bộ Admin, card Nhân viên phụ trách, card Lịch sử xử lý, card Tệp đính kèm | | Pass | 11/15/2015 | |
| **FUNC-CTYCDH-02** | Hiển thị đầy đủ thông tin yêu cầu | 1. Truy cập /admin/special-requests/[id] | Hiển thị đầy đủ thông tin: ID yêu cầu, ngày gửi, trạng thái, độ ưu tiên, thông tin khách hàng, mô tả mô hình yêu cầu, thông tin bổ sung, ghi chú nội bộ, nhân viên phụ trách, lịch sử xử lý, tệp đính kèm | | Pass | 11/15/2015 | |
| **FUNC-CTYCDH-03** | Click nút Quay lại | 1. Truy cập /admin/special-requests/[id]<br>2. Click nút "Quay lại" | Chuyển về trang /admin/special-requests | | Pass | 11/15/2015 | |
| **FUNC-CTYCDH-04** | Click nút Cập nhật trạng thái | 1. Truy cập /admin/special-requests/[id]<br>2. Click nút "Cập nhật trạng thái" | Mở modal cập nhật trạng thái yêu cầu | | Pass | 11/15/2015 | |
| **FUNC-CTYCDH-05** | Click nút Phản hồi khách hàng | 1. Truy cập /admin/special-requests/[id]<br>2. Click nút "Phản hồi khách hàng" | Mở modal phản hồi khách hàng | | Pass | 11/15/2015 | |
| **FUNC-CTYCDH-06** | Click nút Gán nhân viên | 1. Truy cập /admin/special-requests/[id]<br>2. Click nút "Gán nhân viên" | Mở modal gán nhân viên phụ trách | | Pass | 11/15/2015 | |
| **FUNC-CTYCDH-07** | Click nút Tìm sản phẩm | 1. Truy cập /admin/special-requests/[id]<br>2. Click nút "Tìm sản phẩm" | Chuyển đến trang tìm kiếm sản phẩm với các tiêu chí từ yêu cầu | | Pass | 11/15/2015 | |
| **FUNC-CTYCDH-08** | Thêm ghi chú nội bộ thành công | 1. Truy cập /admin/special-requests/[id]<br>2. Nhập ghi chú vào Textarea<br>3. Click "Thêm ghi chú" hoặc "Cập nhật ghi chú" | Hiển thị thông báo "Thêm ghi chú thành công" hoặc "Cập nhật ghi chú thành công", ghi chú được lưu và hiển thị | | Untested | 11/15/2015 | |
| **FUNC-CTYCDH-09** | Xem tệp đính kèm | 1. Truy cập /admin/special-requests/[id]<br>2. Click vào tệp đính kèm | Hiển thị preview tệp đính kèm hoặc tải về tệp | | Pass | 11/15/2015 | |
| **FUNC-CTYCDH-10** | Xử lý khi yêu cầu không tồn tại | 1. Truy cập /admin/special-requests/[id không tồn tại] | Hiển thị thông báo lỗi "Yêu cầu không tồn tại" hoặc chuyển về trang danh sách | | Untested | 11/15/2015 | |
| **FUNC-CTYCDH-11** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/special-requests/[id]<br>2. Tắt kết nối mạng | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại" | | Untested | 11/15/2015 | |
| **FUNC-CTYCDH-12** | Xử lý khi server lỗi | 1. Truy cập /admin/special-requests/[id]<br>2. Server trả về lỗi 500 | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau" | | Untested | 11/15/2015 | |

---

### Function: Xử lý yêu cầu đặt hàng

#### Check GUI: Xử lý yêu cầu đặt hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XLYCDH-01** | Kiểm tra modal Phản hồi khách hàng | 1. Truy cập /admin/special-requests<br>2. Click nút Phản hồi (icon MessageSquare) của một yêu cầu<br>3. Kiểm tra modal | Hiển thị Dialog với tiêu đề "Phản hồi khách hàng", mô tả "Gửi phản hồi cho yêu cầu [id]" | | Pass | 11/15/2015 | |
| **GUI-XLYCDH-02** | Kiểm tra trường Tiêu đề phản hồi | 1. Truy cập /admin/special-requests<br>2. Click nút Phản hồi<br>3. Kiểm tra trường | Hiển thị label "Tiêu đề phản hồi", input type text với placeholder "Nhập tiêu đề..." | | Pass | 11/15/2015 | |
| **GUI-XLYCDH-03** | Kiểm tra trường Nội dung phản hồi | 1. Truy cập /admin/special-requests<br>2. Click nút Phản hồi<br>3. Kiểm tra trường | Hiển thị label "Nội dung phản hồi", Textarea với placeholder "Nhập nội dung phản hồi...", rows 4 | | Pass | 11/15/2015 | |
| **GUI-XLYCDH-04** | Kiểm tra Select Loại phản hồi | 1. Truy cập /admin/special-requests<br>2. Click nút Phản hồi<br>3. Kiểm tra Select | Hiển thị label "Loại phản hồi", Select với các option: Thông báo trạng thái, Tìm thấy sản phẩm, Cần thêm thông tin, Không tìm thấy | | Pass | 11/15/2015 | |
| **GUI-XLYCDH-05** | Kiểm tra Select Cập nhật trạng thái | 1. Truy cập /admin/special-requests<br>2. Click nút Phản hồi<br>3. Kiểm tra Select | Hiển thị label "Cập nhật trạng thái", Select với các option: Đang xử lý, Đã hoàn thành, Không tìm thấy, Đã hủy | | Pass | 11/15/2015 | |
| **GUI-XLYCDH-06** | Kiểm tra checkbox Gửi qua email | 1. Truy cập /admin/special-requests<br>2. Click nút Phản hồi<br>3. Kiểm tra checkbox | Hiển thị checkbox với label "Gửi qua email" | | Pass | 11/15/2015 | |
| **GUI-XLYCDH-07** | Kiểm tra checkbox Gửi qua SMS | 1. Truy cập /admin/special-requests<br>2. Click nút Phản hồi<br>3. Kiểm tra checkbox | Hiển thị checkbox với label "Gửi qua SMS" | | Pass | 11/15/2015 | |
| **GUI-XLYCDH-08** | Kiểm tra nút Hủy | 1. Truy cập /admin/special-requests<br>2. Click nút Phản hồi<br>3. Kiểm tra nút | Hiển thị nút "Hủy" variant outline | | Pass | 11/15/2015 | |
| **GUI-XLYCDH-09** | Kiểm tra nút Gửi phản hồi | 1. Truy cập /admin/special-requests<br>2. Click nút Phản hồi<br>3. Kiểm tra nút | Hiển thị nút "Gửi phản hồi" type submit | | Pass | 11/15/2015 | |
| **GUI-XLYCDH-10** | Kiểm tra modal Gán nhân viên | 1. Truy cập /admin/special-requests<br>2. Click nút Gán nhân viên (icon User) của một yêu cầu<br>3. Kiểm tra modal | Hiển thị Dialog với tiêu đề "Gán nhân viên phụ trách", mô tả "Gán nhân viên xử lý yêu cầu [id]" | | Pass | 11/15/2015 | |
| **GUI-XLYCDH-11** | Kiểm tra Select Chọn nhân viên | 1. Truy cập /admin/special-requests<br>2. Click nút Gán nhân viên<br>3. Kiểm tra Select | Hiển thị label "Chọn nhân viên", Select với placeholder "Chọn nhân viên...", có các option: danh sách nhân viên | | Pass | 11/15/2015 | |
| **GUI-XLYCDH-12** | Kiểm tra trường Ghi chú | 1. Truy cập /admin/special-requests<br>2. Click nút Gán nhân viên<br>3. Kiểm tra trường | Hiển thị label "Ghi chú", Textarea với placeholder "Nhập ghi chú cho nhân viên...", rows 3 | | Pass | 11/15/2015 | |
| **GUI-XLYCDH-13** | Kiểm tra nút Hủy (modal Gán nhân viên) | 1. Truy cập /admin/special-requests<br>2. Click nút Gán nhân viên<br>3. Kiểm tra nút | Hiển thị nút "Hủy" variant outline | | Pass | 11/15/2015 | |
| **GUI-XLYCDH-14** | Kiểm tra nút Gán nhân viên | 1. Truy cập /admin/special-requests<br>2. Click nút Gán nhân viên<br>3. Kiểm tra nút | Hiển thị nút "Gán nhân viên" type submit | | Pass | 11/15/2015 | |

---

### Check FUNC: Xử lý yêu cầu đặt hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XLYCDH-01** | Mở modal phản hồi khách hàng | 1. Truy cập /admin/special-requests<br>2. Click nút "Phản hồi" của một yêu cầu | Hiển thị Dialog với tiêu đề "Phản hồi khách hàng", mô tả, các trường: Tiêu đề phản hồi, Nội dung phản hồi, Loại phản hồi, Cập nhật trạng thái, checkbox Gửi qua email, checkbox Gửi qua SMS, nút Hủy, nút Gửi phản hồi | | Pass | 11/15/2015 | |
| **FUNC-XLYCDH-02** | Gửi phản hồi thành công | 1. Truy cập /admin/special-requests<br>2. Click nút "Phản hồi"<br>3. Nhập tiêu đề phản hồi<br>4. Nhập nội dung phản hồi<br>5. Chọn loại phản hồi<br>6. Chọn cập nhật trạng thái (tùy chọn)<br>7. Tích checkbox Gửi qua email/SMS<br>8. Click "Gửi phản hồi" | Hiển thị thông báo "Gửi phản hồi thành công", phản hồi được gửi đến khách hàng qua email/SMS (nếu được chọn), trạng thái yêu cầu được cập nhật (nếu được chọn), modal đóng | | Untested | 11/15/2015 | |
| **FUNC-XLYCDH-03** | Gửi phản hồi - Thiếu Tiêu đề | 1. Truy cập /admin/special-requests<br>2. Click nút "Phản hồi"<br>3. Để trống tiêu đề<br>4. Nhập nội dung<br>5. Click "Gửi phản hồi" | Hiển thị thông báo lỗi "Tiêu đề phản hồi không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-XLYCDH-04** | Gửi phản hồi - Thiếu Nội dung | 1. Truy cập /admin/special-requests<br>2. Click nút "Phản hồi"<br>3. Nhập tiêu đề<br>4. Để trống nội dung<br>5. Click "Gửi phản hồi" | Hiển thị thông báo lỗi "Nội dung phản hồi không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-XLYCDH-05** | Gửi phản hồi - Không chọn kênh gửi | 1. Truy cập /admin/special-requests<br>2. Click nút "Phản hồi"<br>3. Nhập đầy đủ thông tin<br>4. Không tích checkbox Gửi qua email/SMS<br>5. Click "Gửi phản hồi" | Hiển thị thông báo lỗi "Vui lòng chọn ít nhất một kênh gửi (Email hoặc SMS)", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-XLYCDH-06** | Click nút Hủy (modal Phản hồi) | 1. Truy cập /admin/special-requests<br>2. Click nút "Phản hồi"<br>3. Click "Hủy" | Modal đóng, không gửi phản hồi | | Pass | 11/15/2015 | |
| **FUNC-XLYCDH-07** | Mở modal gán nhân viên | 1. Truy cập /admin/special-requests<br>2. Click nút "Gán nhân viên" của một yêu cầu | Hiển thị Dialog với tiêu đề "Gán nhân viên phụ trách", mô tả, các trường: Chọn nhân viên, Ghi chú, nút Hủy, nút Gán nhân viên | | Pass | 11/15/2015 | |
| **FUNC-XLYCDH-08** | Gán nhân viên thành công | 1. Truy cập /admin/special-requests<br>2. Click nút "Gán nhân viên"<br>3. Chọn nhân viên<br>4. Nhập ghi chú (tùy chọn)<br>5. Click "Gán nhân viên" | Hiển thị thông báo "Gán nhân viên thành công", nhân viên được gán cho yêu cầu, cột Nhân viên phụ trách được cập nhật, lịch sử xử lý được ghi nhận, modal đóng | | Untested | 11/15/2015 | |
| **FUNC-XLYCDH-09** | Gán nhân viên - Thiếu Chọn nhân viên | 1. Truy cập /admin/special-requests<br>2. Click nút "Gán nhân viên"<br>3. Không chọn nhân viên<br>4. Click "Gán nhân viên" | Hiển thị thông báo lỗi "Vui lòng chọn nhân viên", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-XLYCDH-10** | Click nút Hủy (modal Gán nhân viên) | 1. Truy cập /admin/special-requests<br>2. Click nút "Gán nhân viên"<br>3. Click "Hủy" | Modal đóng, không gán nhân viên | | Pass | 11/15/2015 | |
| **FUNC-XLYCDH-11** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/special-requests<br>2. Click nút "Phản hồi"<br>3. Điền đầy đủ thông tin<br>4. Tắt kết nối mạng<br>5. Click "Gửi phản hồi" | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", form không được gửi | | Untested | 11/15/2015 | |
| **FUNC-XLYCDH-12** | Xử lý khi server lỗi | 1. Truy cập /admin/special-requests<br>2. Click nút "Phản hồi"<br>3. Điền đầy đủ thông tin<br>4. Server trả về lỗi 500<br>5. Click "Gửi phản hồi" | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau", form không được gửi | | Untested | 11/15/2015 | |

---

### Function: Cập nhật trạng thái yêu cầu đặt hàng

#### Check GUI: Cập nhật trạng thái yêu cầu đặt hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CNTTYCDH-01** | Kiểm tra modal Cập nhật trạng thái | 1. Truy cập /admin/special-requests<br>2. Click nút Cập nhật trạng thái (icon CheckCircle) của một yêu cầu<br>3. Kiểm tra modal | Hiển thị Dialog với tiêu đề "Cập nhật trạng thái yêu cầu", mô tả "Thay đổi trạng thái xử lý yêu cầu [id]" | | Pass | 11/15/2015 | |
| **GUI-CNTTYCDH-02** | Kiểm tra trường Trạng thái hiện tại | 1. Truy cập /admin/special-requests<br>2. Click nút Cập nhật trạng thái<br>3. Kiểm tra trường | Hiển thị label "Trạng thái hiện tại", Display hiển thị trạng thái hiện tại với Badge và icon | | Pass | 11/15/2015 | |
| **GUI-CNTTYCDH-03** | Kiểm tra Select Trạng thái mới | 1. Truy cập /admin/special-requests<br>2. Click nút Cập nhật trạng thái<br>3. Kiểm tra Select | Hiển thị label "Trạng thái mới *", Select với placeholder "Chọn trạng thái mới", có các option: Mới, Đang xử lý, Đã hoàn thành, Đã hủy | | Pass | 11/15/2015 | |
| **GUI-CNTTYCDH-04** | Kiểm tra trường Lý do thay đổi | 1. Truy cập /admin/special-requests<br>2. Click nút Cập nhật trạng thái<br>3. Kiểm tra trường | Hiển thị label "Lý do thay đổi", Textarea với placeholder "Nhập lý do thay đổi trạng thái (tùy chọn)" | | Pass | 11/15/2015 | |
| **GUI-CNTTYCDH-05** | Kiểm tra checkbox Thông báo khách hàng | 1. Truy cập /admin/special-requests<br>2. Click nút Cập nhật trạng thái<br>3. Kiểm tra checkbox | Hiển thị checkbox với label "Gửi thông báo cho khách hàng về thay đổi trạng thái", mặc định checked | | Pass | 11/15/2015 | |
| **GUI-CNTTYCDH-06** | Kiểm tra nút Hủy | 1. Truy cập /admin/special-requests<br>2. Click nút Cập nhật trạng thái<br>3. Kiểm tra nút | Hiển thị nút "Hủy" variant outline | | Pass | 11/15/2015 | |
| **GUI-CNTTYCDH-07** | Kiểm tra nút Cập nhật trạng thái | 1. Truy cập /admin/special-requests<br>2. Click nút Cập nhật trạng thái<br>3. Kiểm tra nút | Hiển thị nút "Cập nhật trạng thái" type submit | | Pass | 11/15/2015 | |

---

### Check FUNC: Cập nhật trạng thái yêu cầu đặt hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CNTTYCDH-01** | Mở modal cập nhật trạng thái | 1. Truy cập /admin/special-requests<br>2. Click nút "Cập nhật trạng thái" của một yêu cầu | Hiển thị Dialog với tiêu đề "Cập nhật trạng thái yêu cầu", mô tả, trường Trạng thái hiện tại, Select Trạng thái mới, Textarea Lý do thay đổi, checkbox Thông báo khách hàng, nút Hủy, nút Cập nhật trạng thái | | Pass | 11/15/2015 | |
| **FUNC-CNTTYCDH-02** | Cập nhật trạng thái thành công | 1. Truy cập /admin/special-requests<br>2. Click nút "Cập nhật trạng thái"<br>3. Chọn trạng thái mới<br>4. Nhập lý do (tùy chọn)<br>5. Tích checkbox Thông báo khách hàng<br>6. Click "Cập nhật trạng thái" | Hiển thị thông báo "Cập nhật trạng thái thành công", trạng thái yêu cầu được cập nhật, gửi thông báo cho khách hàng (nếu được chọn), lịch sử xử lý được ghi nhận, modal đóng | | Untested | 11/15/2015 | |
| **FUNC-CNTTYCDH-03** | Cập nhật - Thiếu Trạng thái mới | 1. Truy cập /admin/special-requests<br>2. Click nút "Cập nhật trạng thái"<br>3. Không chọn trạng thái mới<br>4. Click "Cập nhật trạng thái" | Hiển thị thông báo lỗi "Vui lòng chọn trạng thái mới", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-CNTTYCDH-04** | Cập nhật - Chọn trạng thái giống hiện tại | 1. Truy cập /admin/special-requests<br>2. Click nút "Cập nhật trạng thái"<br>3. Chọn trạng thái mới giống trạng thái hiện tại<br>4. Click "Cập nhật trạng thái" | Hiển thị thông báo lỗi "Trạng thái mới phải khác trạng thái hiện tại", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-CNTTYCDH-05** | Cập nhật - Không gửi thông báo | 1. Truy cập /admin/special-requests<br>2. Click nút "Cập nhật trạng thái"<br>3. Chọn trạng thái mới<br>4. Bỏ tích checkbox Thông báo khách hàng<br>5. Click "Cập nhật trạng thái" | Hiển thị thông báo "Cập nhật trạng thái thành công", trạng thái được cập nhật, không gửi thông báo cho khách hàng | | Untested | 11/15/2015 | |
| **FUNC-CNTTYCDH-06** | Click nút Hủy | 1. Truy cập /admin/special-requests<br>2. Click nút "Cập nhật trạng thái"<br>3. Click "Hủy" | Modal đóng, trạng thái không được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-CNTTYCDH-07** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/special-requests<br>2. Click nút "Cập nhật trạng thái"<br>3. Chọn trạng thái mới<br>4. Tắt kết nối mạng<br>5. Click "Cập nhật trạng thái" | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", form không được gửi | | Untested | 11/15/2015 | |
| **FUNC-CNTTYCDH-08** | Xử lý khi server lỗi | 1. Truy cập /admin/special-requests<br>2. Click nút "Cập nhật trạng thái"<br>3. Chọn trạng thái mới<br>4. Server trả về lỗi 500<br>5. Click "Cập nhật trạng thái" | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau", form không được gửi | | Untested | 11/15/2015 | |

---

**Người tạo:** Testing Team  
**Ngày cập nhật:** 11/15/2015  
**Phiên bản:** 1.0

