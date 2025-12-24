| ID   | Mô tả test case | Các bước thực hiện | Kết quả mong đợi |
|------|-----------------|-------------------|------------------|
| **[Tên cán bộ] Textbox** |
| X-01 | Mở màn hình Thêm cán bộ thành công | Tại Menu Ứng dụng: Click Thêm cán bộ<br>Tại màn hình Danh sách cán bộ: Click Thêm<br>Tại màn hình thêm cán bộ: | Hiển thị màn hình Thêm cán bộ |
| X-02 | Không nhập tên cán bộ | Tại màn hình Thêm cán bộ:<br>1. Không nhập dữ liệu vào [Tên cán bộ] textbox.<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Vui lòng nhập tên cán bộ!"<br>Trỏ chuột tại [Tên cán bộ] textbox. |
| X-03 | Nhập tên cán bộ quá số kí tự cho phép | Tại màn hình Thêm cán bộ:<br>1. Nhập quá 100 ký tự tại [Tên cán bộ] textbox<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Vui lòng không nhập quá 100 ký tự!"<br>Trỏ chuột tại [Tên cán bộ]textbox. |
| X-04 | Nhập tên cán bộ toàn kí tự trống. | Tại màn hình Thêm cán bộ:<br>1. Nhập toàn bộ kí tự trống tại [Tên cán bộ] textbox<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Vui lòng không nhập toàn bộ ký tự trống!"<br>Trỏ chuột tại [Tên cán bộ]textbox. |
| X-05 | Nhập tên cán bộ có kí tự đặc biệt. | Tại màn hình Thêm cán bộ:<br>1. Nhập ký tự đặc biệt tại [Tên cán bộ] textbox<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Vui lòng không nhập ký tự đặc biệt!"<br>Trỏ chuột tại [Tên cán bộ]textbox. |
| X-06 | Nhập tên cán bộ có ký tự số. | Tại màn hình Thêm cán bộ:<br>1. Nhập ký tự số tại [Tên cán bộ] textbox<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Vui lòng không nhập ký tự số!"<br>Trỏ chuột tại [Tên cán bộ]textbox. |
| **[Giới tính] Combobox** |
| X-07 | Không chọn giới tính | Tại màn hình Thêm cán bộ:<br>1. Không chọn giới tính tại [Giới tính] Combobox.<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Vui lòng chọn giới tính!"<br>Trỏ chuột tại [Giới tính] Combobox. |
| **[Ngày sinh] Datechoose** |
| X-08 | Không nhập ngày sinh | Tại màn hình Thêm cán bộ:<br>1. Không chọn ngày sinh tại [Ngày sinh] Datechoose.<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Vui lòng chọn năm sinh!"<br>Trỏ chuột tại [Ngày sinh] Datechoose. |
| X-09 | Chọn ngày sinh trong tương lai | Tại màn hình Thêm cán bộ:<br>1. Chọn ngày sinh > ngày hiện tại tại [Ngày sinh] Datechoose.<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Ngày sinh không hợp lệ!"<br>Trỏ chuột tại [Ngày sinh] Datechoose. |
| X-10 | Chọn ngày sinh dưới 18 tuổi | Tại màn hình Thêm cán bộ:<br>1. Chọn ngày sinh < 18 tuổi tại [Ngày sinh] Datechoose.<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Cán bộ phải từ 18 tuổi trở lên!"<br>Trỏ chuột tại [Ngày sinh] Datechoose. |
| **[Số điện thoại] Textbox** |
| X-11 | Không nhập số điện thoại | Tại màn hình Thêm cán bộ:<br>1. Không nhập dữ liệu vào [Số điện thoại] textbox.<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Vui lòng nhập số điện thoại!"<br>Trỏ chuột tại [Số điện thoại] textbox. |
| X-12 | Nhập quá số ký tự số điện thoại cho phép | Tại màn hình Thêm cán bộ:<br>1. Nhập quá 50 ký tự tại [Số điện thoại] textbox<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Vui lòng không nhập quá 50 ký tự!"<br>Trỏ chuột tại [Số điện thoại]textbox. |
| X-13 | Nhập toàn ký tự trống. | Tại màn hình Thêm cán bộ:<br>1. Nhập toàn bộ là ký tự trống tại [Số điện thoại] textbox<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Vui lòng không nhập toàn bộ là ký tự trống!"<br>Trỏ chuột tại [Số điện thoại]textbox. |
| X-14 | Nhập số điện thoại có ký tự là chữ cái. | Tại màn hình Thêm cán bộ:<br>1. Nhập ký tự chữ cái tại [Số điện thoại] textbox<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Vui lòng không nhập chữ cái!"<br>Trỏ chuột tại [Số điện thoại]textbox. |
| X-15 | Nhập số điện thoại có ký tự đặc biệt. | Tại màn hình Thêm cán bộ:<br>1. Nhập ký tự đặc biệt tại [Số điện thoại] textbox<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Vui lòng không nhập ký tự đặc biệt!"<br>Trỏ chuột tại [Số điện thoại]textbox. |
| X-16 | Nhập số điện thoại không đúng định dạng | Tại màn hình Thêm cán bộ:<br>1. Nhập số điện thoại < 10 số tại [Số điện thoại] textbox<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Số điện thoại không hợp lệ!"<br>Trỏ chuột tại [Số điện thoại] textbox. |
| **[Hình ảnh] Choosefile** |
| X-17 | Không chọn hình ảnh | Tại màn hình Thêm cán bộ:<br>1. Không chọn hình ảnh đại diện.<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Vui lòng chọn hình ảnh!"<br>Trỏ chuột tại [Hình ảnh] Choosefile. |
| X-18 | Chọn file không đúng định dạng | Tại màn hình Thêm cán bộ:<br>1. Chọn file không phải jpg, png tại [Hình ảnh] Choosefile.<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Vui lòng chọn file ảnh hợp lệ!"<br>Trỏ chuột tại [Hình ảnh] Choosefile. |
| X-19 | Chọn file ảnh quá dung lượng cho phép | Tại màn hình Thêm cán bộ:<br>1. Chọn file ảnh > 5MB tại [Hình ảnh] Choosefile.<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Dung lượng file quá lớn!"<br>Trỏ chuột tại [Hình ảnh] Choosefile. |
| **[Email] Textbox** |
| X-20 | Không nhập địa chỉ email | Tại màn hình Thêm cán bộ:<br>1. Không nhập dữ liệu vào [Email] textbox.<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Vui lòng nhập địa chỉ email!"<br>Trỏ chuột tại [Email] textbox. |
| X-21 | Nhập quá số ký tự email cho phép | Tại màn hình Thêm cán bộ:<br>1. Nhập quá 50 ký tự tại [Email] textbox.<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Vui lòng không nhập quá 50 ký tự!"<br>Trỏ chuột vào [Email]textbox. |
| X-22 | Nhập sai định dạng email | Tại màn hình Thêm cán bộ:<br>1. Nhập sai định dạng email tại [Email]textbox.<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Vui lòng nhập lại địa chỉ email!"<br>Trỏ chuột tại [Email] textbox. |
| X-23 | Nhập email không có ký tự @ | Tại màn hình Thêm cán bộ:<br>1. Nhập email thiếu @ tại [Email]textbox.<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Email không hợp lệ!"<br>Trỏ chuột tại [Email] textbox. |
| **[Địa chỉ] Textbox** |
| X-24 | Không nhập địa chỉ | Tại màn hình Thêm cán bộ:<br>1. Không nhập dữ liệu địa chỉ tại [Địa chỉ]textbox.<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Vui lòng nhập địa chỉ!"<br>Trỏ chuột tại [Địa chỉ] textbox. |
| X-25 | Nhập quá số ký tự địa chỉ cho phép | Tại màn hình Thêm cán bộ:<br>1. Nhập quá 100 ký tự tại [Địa chỉ]textbox.<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Vui lòng không nhập quá 100 ký tự!"<br>Trỏ chuột tại [Địa chỉ] textbox. |
| X-26 | Nhập địa chỉ có ký tự đặc biệt. | Tại màn hình Thêm cán bộ:<br>1. Nhập ký tự đặc biệt tại [Địa chỉ]textbox.<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Vui lòng không nhập ký tự đặc biệt!"<br>Trỏ chuột tại [Địa chỉ]textbox. |
| **[Nơi công tác] Textbox** |
| X-27 | Nhập quá số ký tự nơi công tác cho phép. | Tại màn hình Thêm cán bộ:<br>1. Nhập quá 100 ký tự tại [Nơi công tác]textbox.<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Vui lòng không nhập quá 100 ký tự!"<br>Trỏ chuột tại [Nơi công tác]textbox. |
| X-28 | Nhập nơi công tác có ký tự đặc biệt. | Tại màn hình Thêm cán bộ:<br>1. Nhập ký tự đặc biệt tại [Nơi công tác]textbox.<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Vui lòng không nhập ký tự đặc biệt!"<br>Trỏ chuột tại [Nơi công tác]textbox. |
| **[Chức vụ] Textbox** |
| X-29 | Không nhập chức vụ | Tại màn hình Thêm cán bộ:<br>1. Không nhập dữ liệu chức vụ tại [Chức vụ]textbox.<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Vui lòng nhập chức vụ!"<br>Trỏ chuột tại [Chức vụ] textbox. |
| X-30 | Nhập chức vụ có ký tự đặc biệt | Tại màn hình Thêm cán bộ:<br>1. Nhập ký tự đặc biệt tại [Chức vụ]textbox.<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Vui lòng không nhập ký tự đặc biệt!"<br>Trỏ chuột tại [Chức vụ] textbox. |
| **[Ghi chú] Textarea** |
| X-31 | Nhập quá số ký tự ghi chú cho phép. | Tại màn hình Thêm cán bộ:<br>1. Nhập quá 500 ký tự tại [Ghi chú] Textarea.<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Vui lòng không nhập quá 500 ký tự!"<br>Trỏ chuột tại [Ghi chú] Textarea. |
| X-32 | Nhập ghi chú toàn ký tự trống | Tại màn hình Thêm cán bộ:<br>1. Nhập toàn ký tự trống tại [Ghi chú] Textarea.<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Vui lòng nhập nội dung!"<br>Trỏ chuột tại [Ghi chú] Textarea. |
| **[Mật khẩu] Password** |
| X-33 | Không nhập mật khẩu | Tại màn hình Thêm cán bộ:<br>1. Không nhập dữ liệu vào [Mật khẩu] Password.<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Vui lòng nhập mật khẩu!"<br>Trỏ chuột tại [Mật khẩu] Password. |
| X-34 | Nhập mật khẩu quá ngắn | Tại màn hình Thêm cán bộ:<br>1. Nhập mật khẩu < 8 ký tự tại [Mật khẩu] Password.<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Mật khẩu phải từ 8 ký tự trở lên!"<br>Trỏ chuột tại [Mật khẩu] Password. |
| X-35 | Nhập mật khẩu không đúng yêu cầu | Tại màn hình Thêm cán bộ:<br>1. Nhập mật khẩu không có chữ hoa, số, ký tự đặc biệt tại [Mật khẩu] Password.<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Mật khẩu phải chứa chữ hoa, số và ký tự đặc biệt!"<br>Trỏ chuột tại [Mật khẩu] Password. |
| **[Website] URL** |
| X-36 | Không nhập URL website | Tại màn hình Thêm cán bộ:<br>1. Không nhập dữ liệu vào [Website] URL.<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Vui lòng nhập địa chỉ website!"<br>Trỏ chuột tại [Website] URL. |
| X-37 | Nhập URL không đúng định dạng | Tại màn hình Thêm cán bộ:<br>1. Nhập URL không có http/https tại [Website] URL.<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "URL không hợp lệ!"<br>Trỏ chuột tại [Website] URL. |
| X-38 | Nhập URL quá dài | Tại màn hình Thêm cán bộ:<br>1. Nhập quá 100 ký tự tại [Website] URL.<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Vui lòng không nhập quá 100 ký tự!"<br>Trỏ chuột tại [Website] URL. |
| **[Tuổi] Number** |
| X-39 | Không nhập tuổi | Tại màn hình Thêm cán bộ:<br>1. Không nhập dữ liệu vào [Tuổi] Number.<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Vui lòng nhập tuổi!"<br>Trỏ chuột tại [Tuổi] Number. |
| X-40 | Nhập tuổi < 18 | Tại màn hình Thêm cán bộ:<br>1. Nhập tuổi < 18 tại [Tuổi] Number.<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Tuổi phải từ 18 trở lên!"<br>Trỏ chuột tại [Tuổi] Number. |
| X-41 | Nhập tuổi > 65 | Tại màn hình Thêm cán bộ:<br>1. Nhập tuổi > 65 tại [Tuổi] Number.<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Tuổi không được vượt quá 65!"<br>Trỏ chuột tại [Tuổi] Number. |
| X-42 | Nhập tuổi có ký tự chữ | Tại màn hình Thêm cán bộ:<br>1. Nhập ký tự chữ tại [Tuổi] Number.<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Vui lòng chỉ nhập số!"<br>Trỏ chuột tại [Tuổi] Number. |
| **[Lương] Range** |
| X-43 | Không chọn mức lương | Tại màn hình Thêm cán bộ:<br>1. Không chọn giá trị tại [Lương] Range.<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Vui lòng chọn mức lương!"<br>Trỏ chuột tại [Lương] Range. |
| X-44 | Chọn mức lương < min | Tại màn hình Thêm cán bộ:<br>1. Chọn mức lương < 5.000.000 tại [Lương] Range.<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Lương tối thiểu là 5.000.000đ!"<br>Trỏ chuột tại [Lương] Range. |
| **[Giờ làm việc] Time** |
| X-45 | Không chọn giờ làm việc | Tại màn hình Thêm cán bộ:<br>1. Không chọn giờ tại [Giờ làm việc] Time.<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Vui lòng chọn giờ làm việc!"<br>Trỏ chuột tại [Giờ làm việc] Time. |
| X-46 | Chọn giờ ngoài giờ hành chính | Tại màn hình Thêm cán bộ:<br>1. Chọn giờ < 6h hoặc > 22h tại [Giờ làm việc] Time.<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Giờ làm việc không hợp lệ!"<br>Trỏ chuột tại [Giờ làm việc] Time. |
| **[Tháng tuyển dụng] Month** |
| X-47 | Không chọn tháng tuyển dụng | Tại màn hình Thêm cán bộ:<br>1. Không chọn tháng tại [Tháng tuyển dụng] Month.<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Vui lòng chọn tháng tuyển dụng!"<br>Trỏ chuột tại [Tháng tuyển dụng] Month. |
| X-48 | Chọn tháng trong quá khứ | Tại màn hình Thêm cán bộ:<br>1. Chọn tháng < tháng hiện tại tại [Tháng tuyển dụng] Month.<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Không thể chọn tháng trong quá khứ!"<br>Trỏ chuột tại [Tháng tuyển dụng] Month. |
| **[Nhận tin] Checkbox** |
| X-49 | Không chọn checkbox nhận tin | Tại màn hình Thêm cán bộ:<br>1. Không check [Nhận tin] Checkbox.<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Vui lòng đồng ý nhận thông tin!"<br>Trỏ chuột tại [Nhận tin] Checkbox. |
| **[Loại hợp đồng] Radio** |
| X-50 | Không chọn loại hợp đồng | Tại màn hình Thêm cán bộ:<br>1. Không chọn radio tại [Loại hợp đồng] Radio.<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Vui lòng chọn loại hợp đồng!"<br>Trỏ chuột tại [Loại hợp đồng] Radio. |
| **[Phòng ban] Dropdown** |
| X-51 | Không chọn phòng ban | Tại màn hình Thêm cán bộ:<br>1. Không chọn giá trị tại [Phòng ban] Dropdown.<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Vui lòng chọn phòng ban!"<br>Trỏ chuột tại [Phòng ban] Dropdown. |
| **[Kỹ năng] Listbox** |
| X-52 | Không chọn kỹ năng | Tại màn hình Thêm cán bộ:<br>1. Không chọn item nào tại [Kỹ năng] Listbox.<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Vui lòng chọn ít nhất 1 kỹ năng!"<br>Trỏ chuột tại [Kỹ năng] Listbox. |
| X-53 | Chọn quá số lượng kỹ năng cho phép | Tại màn hình Thêm cán bộ:<br>1. Chọn > 10 kỹ năng tại [Kỹ năng] Listbox.<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Chỉ được chọn tối đa 10 kỹ năng!"<br>Trỏ chuột tại [Kỹ năng] Listbox. |
| **[Tìm kiếm] Search** |
| X-54 | Tìm kiếm với từ khóa trống | Tại màn hình Thêm cán bộ:<br>1. Không nhập từ khóa tại [Tìm kiếm] Search.<br>2. Nhấn nút tìm kiếm. | Hiển thị thông báo: "Vui lòng nhập từ khóa tìm kiếm!"<br>Trỏ chuột tại [Tìm kiếm] Search. |
| X-55 | Tìm kiếm với ký tự đặc biệt | Tại màn hình Thêm cán bộ:<br>1. Nhập ký tự đặc biệt tại [Tìm kiếm] Search.<br>2. Nhấn nút tìm kiếm. | Hiển thị thông báo: "Từ khóa không hợp lệ!"<br>Trỏ chuột tại [Tìm kiếm] Search. |
| **[CV file] File** |
| X-56 | Không upload file CV | Tại màn hình Thêm cán bộ:<br>1. Không chọn file tại [CV file] File.<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Vui lòng upload file CV!"<br>Trỏ chuột tại [CV file] File. |
| X-57 | Upload file không đúng định dạng | Tại màn hình Thêm cán bộ:<br>1. Chọn file không phải pdf, doc, docx tại [CV file] File.<br>2. Nhấn [Thêm] button. | Hiển thị thông báo: "Chỉ chấp nhận file pdf, doc, docx!"<br>Trỏ chuột tại [CV file] File. |
| X-58 | Upload file quá dung lượng | Tại màn hình Thêm cán bộ:<br>1. Chọn file > 10MB tại [CV file] File.<br>2. Nhấn [Thêm] button. | Hiển thị thông báo:
