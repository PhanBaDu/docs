| ID   | Control Type                    | Mô tả                                           | Thuộc tính                                                    |
|------|---------------------------------|-------------------------------------------------|---------------------------------------------------------------|
| X-01 | [Tên cán bộ] Textbox           | Nhập vào tên cán bộ cần thêm.                  | Status = enable<br>Default = blank<br>Max-length = 100        |
| X-02 | [Giới tính] Combobox           | Lựa chọn giới tính cán bộ.                      | Status = enable<br>Max-length = 20                            |
| X-03 | [Ngày sinh] Datechoose         | Lựa chọn ngày sinh cán bộ.                      | Status = enable                                               |
| X-04 | [Số điện thoại] Textbox        | Nhập vào số điện thoại cán bộ.                  | Status = enable<br>Default = blank<br>Max-length = 50         |
| X-05 | [Hình ảnh] Choosefile          | Chọn hình ảnh đại diện.                         | Status = enable                                               |
| X-06 | [Email] Textbox                | Nhập vào địa chỉ email cán bộ.                  | Status = enable<br>Default = blank<br>Max-length = 50         |
| X-07 | [Địa chỉ] Textbox              | Nhập vào địa chỉ cán bộ.                        | Status = enable<br>Max-length = 100                           |
| X-08 | [Nơi công tác] Textbox         | Nhập vào nơi công tác của cán bộ.               | Status = enable<br>Default = blank<br>Max-length = 100        |
| X-09 | [Chức vụ] Textbox              | Nhập vào chức vụ của cán bộ.                    | Status = enable<br>Default = blank<br>Max-length = 50         |
| X-10 | [OK] Button                    | Nút xác nhận thực hiện thao tác.                | Status = enable                                               |
| X-11 | [Reset] Button                 | Nút xóa toàn bộ dữ liệu đã nhập.                | Status = enable                                               |
| X-12 | [Hủy] Button                   | Nút hủy bỏ thao tác và đóng form.               | Status = enable                                               |
| X-13 | [Ghi chú] Textarea             | Nhập ghi chú chi tiết về cán bộ.                | Status = enable<br>Default = blank<br>Max-length = 500        |
| X-14 | [Mật khẩu] Password            | Nhập mật khẩu tài khoản.                        | Status = enable<br>Default = blank<br>Max-length = 50         |
| X-15 | [Website] URL                  | Nhập địa chỉ website cá nhân.                   | Status = enable<br>Default = blank<br>Max-length = 100        |
| X-16 | [Tuổi] Number                  | Nhập tuổi của cán bộ.                           | Status = enable<br>Min = 18<br>Max = 65                       |
| X-17 | [Lương] Range                  | Chọn mức lương mong muốn.                       | Status = enable<br>Min = 5000000<br>Max = 50000000            |
| X-18 | [Giờ làm việc] Time            | Chọn giờ bắt đầu làm việc.                      | Status = enable<br>Default = 08:00                            |
| X-19 | [Tháng tuyển dụng] Month       | Chọn tháng dự kiến tuyển dụng.                  | Status = enable                                               |
| X-20 | [Nhận tin] Checkbox            | Đồng ý nhận thông tin qua email.                | Status = enable<br>Default = unchecked                        |
| X-21 | [Loại hợp đồng] Radio          | Chọn loại hợp đồng làm việc.                    | Status = enable<br>Options = Chính thức, Thử việc, Part-time  |
| X-22 | [Phòng ban] Dropdown           | Chọn phòng ban công tác.                        | Status = enable<br>Default = blank                            |
| X-23 | [Kỹ năng] Listbox              | Chọn các kỹ năng của cán bộ.                    | Status = enable<br>Multiple = true                            |
| X-24 | [Tìm kiếm] Search              | Tìm kiếm cán bộ trong hệ thống.                 | Status = enable<br>Default = blank                            |
| X-25 | [CV file] File                 | Upload file CV của cán bộ.                      | Status = enable<br>Accept = .pdf,.doc,.docx                   |
| X-26 | [Màu đồng phục] Color          | Chọn màu đồng phục yêu thích.                   | Status = enable<br>Default = #000000                          |
| X-27 | [Đánh giá] Rating              | Đánh giá năng lực cán bộ.                       | Status = enable<br>Max = 5<br>Default = 0                     |
| X-28 | [Chứng chỉ] Tag-input          | Nhập các chứng chỉ đã có.                       | Status = enable<br>Default = blank                            |
| X-29 | [Kích hoạt] Switch             | Bật/tắt trạng thái kích hoạt tài khoản.         | Status = enable<br>Default = off                              |
| X-30 | [Ảnh CCCD] Image               | Upload ảnh căn cước công dân.                   | Status = enable<br>Accept = .jpg,.png                         |
| X-31 | [Trình độ] Cascader            | Chọn trình độ học vấn theo cấp.                 | Status = enable                                               |
| X-32 | [Quyền truy cập] Transfer      | Phân quyền truy cập các module.                 | Status = enable                                               |
| X-33 | [Mã OTP] OTP-input             | Nhập mã OTP xác thực.                           | Status = enable<br>Length = 6                                 |
| X-34 | [Ký tên] Signature             | Ký tên điện tử xác nhận.                        | Status = enable<br>Format = base64                            |
| X-35 | [Vị trí làm việc] Map-picker   | Chọn vị trí làm việc trên bản đồ.               | Status = enable                                               |
| X-36 | [Mô tả công việc] Rich-text    | Nhập mô tả công việc chi tiết.                  | Status = enable<br>Default = blank<br>Max-length = 2000       |
| X-37 | [Code mẫu] Code-editor         | Nhập code mẫu kỹ năng lập trình.                | Status = enable<br>Language = javascript                      |
| X-38 | [Đã kết hôn] Toggle            | Chọn tình trạng hôn nhân.                       | Status = enable<br>Default = off                              |
| X-39 | [Thâm niên] Slider             | Chọn số năm kinh nghiệm.                        | Status = enable<br>Min = 0<br>Max = 30                        |
| X-40 | [Bằng cấp] Tree-select         | Chọn bằng cấp từ cấu trúc phân cấp.             | Status = enable                                               |
| X-41 | [Tài liệu] File-multiple       | Upload nhiều tài liệu liên quan.                | Status = enable<br>Accept = .pdf,.doc,.docx,.xlsx             |
| X-42 | [Xác thực] Captcha             | Xác thực người dùng không phải robot.           | Status = enable                                               |
| X-43 | [Ghi âm] Audio                 | Ghi âm giọng nói giới thiệu.                    | Status = enable<br>Max-duration = 60s                         |
| X-44 | [Video giới thiệu] Video       | Quay video giới thiệu bản thân.                 | Status = enable<br>Max-duration = 120s                        |
| X-45 | [Quét QR] QR-scanner           | Quét mã QR thẻ nhân viên.                       | Status = enable                                               |
| X-46 | [Nhập giọng nói] Voice-input   | Nhập liệu bằng giọng nói.                       | Status = enable<br>Language = vi-VN                           |
| X-47 | [Chụp ảnh] Camera-capture      | Chụp ảnh trực tiếp từ camera.                   | Status = enable<br>Resolution = 1920x1080                     |
| X-48 | [Loại nhân viên] Segmented     | Chọn loại nhân viên.                            | Status = enable<br>Options = Fulltime, Parttime, Freelance    |
| X-49 | [Ghi chú Markdown] Markdown    | Nhập ghi chú định dạng Markdown.                | Status = enable<br>Default = blank                            |
| X-50 | [ID ẩn] Hidden                 | Lưu trữ ID cán bộ (không hiển thị).             | Status = enable<br>Value = auto-generate                      |
