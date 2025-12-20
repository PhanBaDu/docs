# Test Case Document

## Test Summary

| Module Code | Quản lý Thông tin Giáo viên |
|-------------|----------------------------|
| **Test requirement** | 1. Thêm giáo viên mới<br/>2. Xem danh sách giáo viên<br/>3. Tìm kiếm giáo viên<br/>4. Cập nhật thông tin giáo viên<br/>5. Xóa giáo viên<br/>6. Xem chi tiết giáo viên<br/>7. Upload ảnh đại diện<br/>8. Quản lý trạng thái |
| **Tester** | |

### Test Statistics

| Pass | Fail | Untested | N/A | Number of Test |
|------|------|----------|-----|----------------|
| 0    | 0    | 0        | 0   | 0              |

---

## Test Cases

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|-----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| | **Function: Thêm giáo viên mới** | | | | | | |
| | **Check FUNC - Thêm giáo viên mới** | | | | | | |
| FUNC-AddTeacher-01 | Thêm giáo viên mới thành công | Tại Menu Ứng dụng (Admin):<br/>1. Click [Quản lý Giáo viên]<br/>2. Click [Thêm giáo viên mới]<br/>3. Nhập mã giáo viên (VD: GV001)<br/>4. Nhập họ tên<br/>5. Nhập ngày sinh<br/>6. Nhập giới tính<br/>7. Nhập số điện thoại<br/>8. Nhập email<br/>9. Nhập địa chỉ<br/>10. Chọn khoa<br/>11. Nhập các thông tin khác<br/>12. Click [Lưu] | Hiển thị thông báo: "Thêm giáo viên thành công!"<br/>Giáo viên được thêm vào hệ thống<br/>Tài khoản tự động được tạo | | | | |
| FUNC-AddTeacher-02 | Thêm giáo viên thất bại - Mã trùng | Tại form thêm giáo viên:<br/>1. Nhập mã giáo viên đã tồn tại<br/>2. Nhập các thông tin khác<br/>3. Click [Lưu] | Hiển thị thông báo lỗi: "Mã giáo viên đã tồn tại!" | | | | |
| FUNC-AddTeacher-03 | Thêm giáo viên thất bại - Email trùng | Tại form thêm giáo viên:<br/>1. Nhập email đã được sử dụng<br/>2. Nhập các thông tin khác<br/>3. Click [Lưu] | Hiển thị thông báo lỗi: "Email đã được sử dụng!" | | | | |
| FUNC-AddTeacher-04 | Thêm giáo viên thất bại - Thiếu thông tin bắt buộc | Tại form thêm giáo viên:<br/>1. Không nhập họ tên<br/>2. Nhập các thông tin khác<br/>3. Click [Lưu] | Hiển thị thông báo lỗi: "Vui lòng nhập họ tên!" | | | | |
| FUNC-AddTeacher-05 | Import danh sách giáo viên từ Excel | Tại màn hình quản lý:<br/>1. Click [Import từ Excel]<br/>2. Chọn file Excel có danh sách giáo viên<br/>3. Click [Import] | Hiển thị thông báo: "Import thành công X giáo viên!"<br/>Tất cả giáo viên trong file được thêm vào hệ thống | | | | |
| | **Function: Xem danh sách giáo viên** | | | | | | |
| | **Check FUNC - Xem danh sách giáo viên** | | | | | | |
| FUNC-ListTeacher-01 | Xem danh sách giáo viên thành công | Tại Menu Ứng dụng:<br/>1. Click [Quản lý Giáo viên]<br/>2. Click [Danh sách giáo viên] | Hiển thị danh sách tất cả giáo viên:<br/>- Mã giáo viên<br/>- Họ tên<br/>- Khoa<br/>- Môn dạy<br/>- Trạng thái<br/>- Ảnh đại diện | | | | |
| FUNC-ListTeacher-02 | Phân trang danh sách giáo viên | Tại màn hình danh sách:<br/>1. Có hơn 20 giáo viên<br/>2. Click [Sau] | Hiển thị trang tiếp theo với 20 giáo viên tiếp theo | | | | |
| FUNC-ListTeacher-03 | Xem danh sách giáo viên theo khoa | Tại màn hình danh sách:<br/>1. Chọn khoa (VD: Khoa Toán)<br/>2. Click [Lọc] | Hiển thị chỉ các giáo viên thuộc khoa đó | | | | |
| | **Function: Tìm kiếm giáo viên** | | | | | | |
| | **Check FUNC - Tìm kiếm giáo viên** | | | | | | |
| FUNC-SearchTeacher-01 | Tìm kiếm theo tên thành công | Tại màn hình danh sách:<br/>1. Nhập tên giáo viên vào ô tìm kiếm (VD: Nguyễn Văn A)<br/>2. Nhấn Enter | Hiển thị danh sách giáo viên có tên chứa từ khóa | | | | |
| FUNC-SearchTeacher-02 | Tìm kiếm theo mã số | Tại màn hình danh sách:<br/>1. Nhập mã giáo viên (VD: GV001)<br/>2. Nhấn Enter | Hiển thị giáo viên có mã số đó | | | | |
| FUNC-SearchTeacher-03 | Tìm kiếm theo môn dạy | Tại màn hình danh sách:<br/>1. Chọn môn dạy (VD: Toán)<br/>2. Click [Tìm kiếm] | Hiển thị danh sách giáo viên dạy môn đó | | | | |
| FUNC-SearchTeacher-04 | Tìm kiếm theo khoa | Tại màn hình danh sách:<br/>1. Chọn khoa (VD: Khoa Toán)<br/>2. Click [Tìm kiếm] | Hiển thị danh sách giáo viên thuộc khoa đó | | | | |
| FUNC-SearchTeacher-05 | Tìm kiếm nâng cao với nhiều tiêu chí | Tại màn hình tìm kiếm:<br/>1. Nhập tên<br/>2. Chọn khoa<br/>3. Chọn môn dạy<br/>4. Chọn trạng thái<br/>5. Click [Tìm kiếm] | Hiển thị danh sách giáo viên phù hợp với tất cả tiêu chí | | | | |
| FUNC-SearchTeacher-06 | Tìm kiếm thất bại - Không tìm thấy | Tại màn hình danh sách:<br/>1. Nhập từ khóa không tồn tại<br/>2. Nhấn Enter | Hiển thị thông báo: "Không tìm thấy giáo viên phù hợp!" | | | | |
| | **Function: Cập nhật thông tin giáo viên** | | | | | | |
| | **Check FUNC - Cập nhật thông tin giáo viên** | | | | | | |
| FUNC-UpdateTeacher-01 | Cập nhật thông tin giáo viên thành công | Tại màn hình danh sách:<br/>1. Chọn một giáo viên<br/>2. Click [Sửa]<br/>3. Sửa thông tin (VD: Đổi số điện thoại, địa chỉ)<br/>4. Click [Lưu] | Hiển thị thông báo: "Cập nhật thông tin giáo viên thành công!"<br/>Thông tin được cập nhật | | | | |
| FUNC-UpdateTeacher-02 | Cập nhật thất bại - Mã giáo viên không được sửa | Tại form sửa:<br/>1. Sửa mã giáo viên<br/>2. Click [Lưu] | Field mã giáo viên bị disable hoặc hiển thị thông báo: "Mã giáo viên không được phép thay đổi!" | | | | |
| FUNC-UpdateTeacher-03 | Cập nhật thất bại - Email trùng với giáo viên khác | Tại form sửa:<br/>1. Sửa email thành email đã được sử dụng bởi giáo viên khác<br/>2. Click [Lưu] | Hiển thị thông báo lỗi: "Email đã được sử dụng!" | | | | |
| FUNC-UpdateTeacher-04 | Giáo viên tự cập nhật thông tin của mình | Tại Menu Ứng dụng (Giáo viên):<br/>1. Click [Thông tin cá nhân]<br/>2. Click [Sửa thông tin]<br/>3. Sửa thông tin (VD: Đổi số điện thoại)<br/>4. Click [Lưu] | Hiển thị thông báo: "Cập nhật thông tin thành công!"<br/>Thông tin được cập nhật | | | | |
| | **Function: Xóa giáo viên** | | | | | | |
| | **Check FUNC - Xóa giáo viên** | | | | | | |
| FUNC-DeleteTeacher-01 | Xóa giáo viên thành công - Không có dữ liệu liên quan | Tại màn hình danh sách:<br/>1. Chọn giáo viên không có lớp, không có phân công<br/>2. Click [Xóa]<br/>3. Xác nhận xóa | Hiển thị thông báo: "Xóa giáo viên thành công!"<br/>Giáo viên bị xóa khỏi hệ thống | | | | |
| FUNC-DeleteTeacher-02 | Xóa thất bại - Giáo viên có lớp đang dạy | Tại màn hình danh sách:<br/>1. Chọn giáo viên có lớp đang dạy<br/>2. Click [Xóa]<br/>3. Xác nhận xóa | Hiển thị thông báo lỗi: "Không thể xóa giáo viên này vì đang có lớp dạy! Vui lòng hủy phân công trước." | | | | |
| FUNC-DeleteTeacher-03 | Xóa thất bại - Giáo viên có phân công | Tại màn hình danh sách:<br/>1. Chọn giáo viên có phân công giảng dạy<br/>2. Click [Xóa]<br/>3. Xác nhận xóa | Hiển thị thông báo lỗi: "Không thể xóa giáo viên này vì có phân công giảng dạy! Vui lòng hủy phân công trước." | | | | |
| FUNC-DeleteTeacher-04 | Hủy xóa giáo viên | Tại màn hình danh sách:<br/>1. Chọn một giáo viên<br/>2. Click [Xóa]<br/>3. Click [Hủy] trong dialog xác nhận | Dialog đóng lại<br/>Giáo viên không bị xóa | | | | |
| | **Function: Xem chi tiết giáo viên** | | | | | | |
| | **Check FUNC - Xem chi tiết giáo viên** | | | | | | |
| FUNC-ViewDetail-01 | Xem chi tiết giáo viên thành công | Tại màn hình danh sách:<br/>1. Chọn một giáo viên<br/>2. Click [Xem chi tiết] | Hiển thị đầy đủ thông tin giáo viên:<br/>- Thông tin cá nhân<br/>- Thông tin chuyên môn<br/>- Môn dạy<br/>- Lớp đang dạy<br/>- Lịch sử công tác<br/>- Đánh giá | | | | |
| FUNC-ViewDetail-02 | Xem lịch sử công tác | Tại màn hình chi tiết:<br/>1. Click [Lịch sử công tác] | Hiển thị lịch sử:<br/>- Các lớp đã dạy<br/>- Các môn đã dạy<br/>- Thời gian<br/>- Đánh giá | | | | |
| FUNC-ViewDetail-03 | Xem đánh giá giáo viên | Tại màn hình chi tiết:<br/>1. Click [Đánh giá] | Hiển thị:<br/>- Đánh giá từ học sinh<br/>- Đánh giá từ ban giám hiệu<br/>- Xếp loại<br/>- Lịch sử đánh giá | | | | |
| | **Function: Upload ảnh đại diện** | | | | | | |
| | **Check FUNC - Upload ảnh đại diện** | | | | | | |
| FUNC-UploadAvatar-01 | Upload ảnh đại diện thành công | Tại màn hình quản lý giáo viên:<br/>1. Chọn một giáo viên<br/>2. Click [Upload ảnh đại diện]<br/>3. Chọn file ảnh<br/>4. Click [Lưu] | Ảnh đại diện được cập nhật<br/>Hiển thị ảnh mới | | | | |
| FUNC-UploadAvatar-02 | Upload thất bại - File không phải ảnh | Tại form upload:<br/>1. Chọn file không phải ảnh (VD: PDF, Word)<br/>2. Click [Lưu] | Hiển thị thông báo lỗi: "File phải là ảnh! Chỉ chấp nhận: JPG, PNG, GIF" | | | | |
| FUNC-UploadAvatar-03 | Upload thất bại - Ảnh quá lớn | Tại form upload:<br/>1. Chọn ảnh > 5MB<br/>2. Click [Lưu] | Hiển thị thông báo lỗi: "Ảnh quá lớn! Kích thước tối đa là 5MB" | | | | |
| FUNC-UploadAvatar-04 | Xóa ảnh đại diện | Tại màn hình quản lý:<br/>1. Chọn giáo viên có ảnh đại diện<br/>2. Click [Xóa ảnh đại diện]<br/>3. Xác nhận | Hiển thị thông báo: "Xóa ảnh đại diện thành công!"<br/>Ảnh đại diện bị xóa<br/>Hiển thị ảnh mặc định | | | | |
| | **Function: Quản lý trạng thái** | | | | | | |
| | **Check FUNC - Quản lý trạng thái** | | | | | | |
| FUNC-ManageStatus-01 | Kích hoạt tài khoản giáo viên thành công | Tại màn hình danh sách:<br/>1. Chọn giáo viên có trạng thái "Tạm ngưng"<br/>2. Click [Kích hoạt] | Hiển thị thông báo: "Kích hoạt tài khoản thành công!"<br/>Trạng thái chuyển thành "Đang làm việc"<br/>Giáo viên có thể đăng nhập | | | | |
| FUNC-ManageStatus-02 | Tạm ngưng tài khoản giáo viên | Tại màn hình danh sách:<br/>1. Chọn giáo viên có trạng thái "Đang làm việc"<br/>2. Click [Tạm ngưng]<br/>3. Nhập lý do<br/>4. Xác nhận | Hiển thị thông báo: "Tạm ngưng tài khoản thành công!"<br/>Trạng thái chuyển thành "Tạm ngưng"<br/>Giáo viên không thể đăng nhập | | | | |
| FUNC-ManageStatus-03 | Đánh dấu nghỉ việc | Tại màn hình danh sách:<br/>1. Chọn giáo viên<br/>2. Click [Nghỉ việc]<br/>3. Nhập lý do<br/>4. Xác nhận | Hiển thị thông báo: "Đánh dấu nghỉ việc thành công!"<br/>Trạng thái chuyển thành "Nghỉ việc"<br/>Giáo viên không thể đăng nhập<br/>Dữ liệu được lưu trữ | | | | |
| FUNC-ManageStatus-04 | Xem lịch sử thay đổi trạng thái | Tại màn hình chi tiết giáo viên:<br/>1. Click [Lịch sử trạng thái] | Hiển thị lịch sử tất cả các lần thay đổi trạng thái:<br/>- Trạng thái cũ<br/>- Trạng thái mới<br/>- Thời gian thay đổi<br/>- Người thay đổi<br/>- Lý do | | | | |

