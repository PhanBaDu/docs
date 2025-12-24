# TEST CASE TEMPLATE - MÀN HÌNH THÊM CÁN BỘ

## 1. TEST CASE CHUNG

| ID | Mô tả test case | Các bước thực hiện | Kết quả mong đợi |
|---|---|---|---|
| X-01 | Mở màn hình Thêm cán bộ thành công | Tại Menu Ứng dụng: Click Thêm cán bộ<br>Tại màn hình Danh sách cán bộ: Click Thêm | Hiển thị màn hình Thêm cán bộ |

---

## 2. [TÊN CÁN BỘ] - TEXTBOX

| ID | Mô tả test case | Các bước thực hiện | Kết quả mong đợi |
|---|---|---|---|
| X-02 | Không nhập tên cán bộ | Tại màn hình Thêm cán bộ:<br>1. Không nhập dữ liệu vào [Tên cán bộ] textbox<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Vui lòng nhập tên cán bộ!"<br>Trỏ chuột tại [Tên cán bộ] textbox |
| X-03 | Nhập tên cán bộ quá số ký tự cho phép | Tại màn hình Thêm cán bộ:<br>1. Nhập quá 100 ký tự tại [Tên cán bộ] textbox<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Vui lòng không nhập quá 100 ký tự!"<br>Trỏ chuột tại [Tên cán bộ] textbox |
| X-04 | Nhập tên cán bộ toàn ký tự trống | Tại màn hình Thêm cán bộ:<br>1. Nhập toàn bộ ký tự trống tại [Tên cán bộ] textbox<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Vui lòng không nhập toàn bộ ký tự trống!"<br>Trỏ chuột tại [Tên cán bộ] textbox |
| X-05 | Nhập tên cán bộ có ký tự đặc biệt | Tại màn hình Thêm cán bộ:<br>1. Nhập ký tự đặc biệt tại [Tên cán bộ] textbox<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Vui lòng không nhập ký tự đặc biệt!"<br>Trỏ chuột tại [Tên cán bộ] textbox |
| X-06 | Nhập tên cán bộ có ký tự số | Tại màn hình Thêm cán bộ:<br>1. Nhập ký tự số tại [Tên cán bộ] textbox<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Vui lòng không nhập ký tự số!"<br>Trỏ chuột tại [Tên cán bộ] textbox |

---

## 3. [GIỚI TÍNH] - COMBOBOX

| ID | Mô tả test case | Các bước thực hiện | Kết quả mong đợi |
|---|---|---|---|
| X-07 | Không chọn giới tính | Tại màn hình Thêm cán bộ:<br>1. Không chọn giới tính tại [Giới tính] Combobox<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Vui lòng chọn giới tính!"<br>Trỏ chuột tại [Giới tính] Combobox |

---

## 4. [NGÀY SINH] - DATEPICKER

| ID | Mô tả test case | Các bước thực hiện | Kết quả mong đợi |
|---|---|---|---|
| X-08 | Không nhập ngày sinh | Tại màn hình Thêm cán bộ:<br>1. Không chọn ngày sinh tại [Ngày sinh] Datepicker<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Vui lòng chọn năm sinh!"<br>Trỏ chuột tại [Ngày sinh] Datepicker |
| X-09 | Chọn ngày sinh trong tương lai | Tại màn hình Thêm cán bộ:<br>1. Chọn ngày sinh > ngày hiện tại tại [Ngày sinh] Datepicker<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Ngày sinh không hợp lệ!"<br>Trỏ chuột tại [Ngày sinh] Datepicker |
| X-10 | Chọn ngày sinh dưới 18 tuổi | Tại màn hình Thêm cán bộ:<br>1. Chọn ngày sinh < 18 tuổi tại [Ngày sinh] Datepicker<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Cán bộ phải từ 18 tuổi trở lên!"<br>Trỏ chuột tại [Ngày sinh] Datepicker |

---

## 5. [SỐ ĐIỆN THOẠI] - TEXTBOX

| ID | Mô tả test case | Các bước thực hiện | Kết quả mong đợi |
|---|---|---|---|
| X-11 | Không nhập số điện thoại | Tại màn hình Thêm cán bộ:<br>1. Không nhập dữ liệu vào [Số điện thoại] textbox<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Vui lòng nhập số điện thoại!"<br>Trỏ chuột tại [Số điện thoại] textbox |
| X-12 | Nhập quá số ký tự số điện thoại cho phép | Tại màn hình Thêm cán bộ:<br>1. Nhập quá 50 ký tự tại [Số điện thoại] textbox<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Vui lòng không nhập quá 50 ký tự!"<br>Trỏ chuột tại [Số điện thoại] textbox |
| X-13 | Nhập toàn ký tự trống | Tại màn hình Thêm cán bộ:<br>1. Nhập toàn bộ là ký tự trống tại [Số điện thoại] textbox<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Vui lòng không nhập toàn bộ là ký tự trống!"<br>Trỏ chuột tại [Số điện thoại] textbox |
| X-14 | Nhập số điện thoại có ký tự là chữ cái | Tại màn hình Thêm cán bộ:<br>1. Nhập ký tự chữ cái tại [Số điện thoại] textbox<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Vui lòng không nhập chữ cái!"<br>Trỏ chuột tại [Số điện thoại] textbox |
| X-15 | Nhập số điện thoại có ký tự đặc biệt | Tại màn hình Thêm cán bộ:<br>1. Nhập ký tự đặc biệt tại [Số điện thoại] textbox<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Vui lòng không nhập ký tự đặc biệt!"<br>Trỏ chuột tại [Số điện thoại] textbox |
| X-16 | Nhập số điện thoại không đúng định dạng | Tại màn hình Thêm cán bộ:<br>1. Nhập số điện thoại < 10 số tại [Số điện thoại] textbox<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Số điện thoại không hợp lệ!"<br>Trỏ chuột tại [Số điện thoại] textbox |

---

## 6. [HÌNH ẢNH] - FILE CHOOSER

| ID | Mô tả test case | Các bước thực hiện | Kết quả mong đợi |
|---|---|---|---|
| X-17 | Không chọn hình ảnh | Tại màn hình Thêm cán bộ:<br>1. Không chọn hình ảnh đại diện<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Vui lòng chọn hình ảnh!"<br>Trỏ chuột tại [Hình ảnh] Choosefile |
| X-18 | Chọn file không đúng định dạng | Tại màn hình Thêm cán bộ:<br>1. Chọn file không phải jpg, png tại [Hình ảnh] Choosefile<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Vui lòng chọn file ảnh hợp lệ!"<br>Trỏ chuột tại [Hình ảnh] Choosefile |
| X-19 | Chọn file ảnh quá dung lượng cho phép | Tại màn hình Thêm cán bộ:<br>1. Chọn file ảnh > 5MB tại [Hình ảnh] Choosefile<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Dung lượng file quá lớn!"<br>Trỏ chuột tại [Hình ảnh] Choosefile |

---

## 7. [EMAIL] - TEXTBOX

| ID | Mô tả test case | Các bước thực hiện | Kết quả mong đợi |
|---|---|---|---|
| X-20 | Không nhập địa chỉ email | Tại màn hình Thêm cán bộ:<br>1. Không nhập dữ liệu vào [Email] textbox<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Vui lòng nhập địa chỉ email!"<br>Trỏ chuột tại [Email] textbox |
| X-21 | Nhập quá số ký tự email cho phép | Tại màn hình Thêm cán bộ:<br>1. Nhập quá 50 ký tự tại [Email] textbox<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Vui lòng không nhập quá 50 ký tự!"<br>Trỏ chuột vào [Email] textbox |
| X-22 | Nhập sai định dạng email | Tại màn hình Thêm cán bộ:<br>1. Nhập sai định dạng email tại [Email] textbox<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Vui lòng nhập lại địa chỉ email!"<br>Trỏ chuột tại [Email] textbox |
| X-23 | Nhập email không có ký tự @ | Tại màn hình Thêm cán bộ:<br>1. Nhập email thiếu @ tại [Email] textbox<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Email không hợp lệ!"<br>Trỏ chuột tại [Email] textbox |

---

## 8. [ĐỊA CHỈ] - TEXTBOX

| ID | Mô tả test case | Các bước thực hiện | Kết quả mong đợi |
|---|---|---|---|
| X-24 | Không nhập địa chỉ | Tại màn hình Thêm cán bộ:<br>1. Không nhập dữ liệu địa chỉ tại [Địa chỉ] textbox<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Vui lòng nhập địa chỉ!"<br>Trỏ chuột tại [Địa chỉ] textbox |
| X-25 | Nhập quá số ký tự địa chỉ cho phép | Tại màn hình Thêm cán bộ:<br>1. Nhập quá 100 ký tự tại [Địa chỉ] textbox<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Vui lòng không nhập quá 100 ký tự!"<br>Trỏ chuột tại [Địa chỉ] textbox |
| X-26 | Nhập địa chỉ có ký tự đặc biệt | Tại màn hình Thêm cán bộ:<br>1. Nhập ký tự đặc biệt tại [Địa chỉ] textbox<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Vui lòng không nhập ký tự đặc biệt!"<br>Trỏ chuột tại [Địa chỉ] textbox |

---

## 9. [NƠI CÔNG TÁC] - TEXTBOX

| ID | Mô tả test case | Các bước thực hiện | Kết quả mong đợi |
|---|---|---|---|
| X-27 | Nhập quá số ký tự nơi công tác cho phép | Tại màn hình Thêm cán bộ:<br>1. Nhập quá 100 ký tự tại [Nơi công tác] textbox<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Vui lòng không nhập quá 100 ký tự!"<br>Trỏ chuột tại [Nơi công tác] textbox |
| X-28 | Nhập nơi công tác có ký tự đặc biệt | Tại màn hình Thêm cán bộ:<br>1. Nhập ký tự đặc biệt tại [Nơi công tác] textbox<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Vui lòng không nhập ký tự đặc biệt!"<br>Trỏ chuột tại [Nơi công tác] textbox |

---

## 10. [CHỨC VỤ] - TEXTBOX

| ID | Mô tả test case | Các bước thực hiện | Kết quả mong đợi |
|---|---|---|---|
| X-29 | Không nhập chức vụ | Tại màn hình Thêm cán bộ:<br>1. Không nhập dữ liệu chức vụ tại [Chức vụ] textbox<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Vui lòng nhập chức vụ!"<br>Trỏ chuột tại [Chức vụ] textbox |
| X-30 | Nhập chức vụ có ký tự đặc biệt | Tại màn hình Thêm cán bộ:<br>1. Nhập ký tự đặc biệt tại [Chức vụ] textbox<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Vui lòng không nhập ký tự đặc biệt!"<br>Trỏ chuột tại [Chức vụ] textbox |

---

## 11. [GHI CHÚ] - TEXTAREA

| ID | Mô tả test case | Các bước thực hiện | Kết quả mong đợi |
|---|---|---|---|
| X-31 | Nhập quá số ký tự ghi chú cho phép | Tại màn hình Thêm cán bộ:<br>1. Nhập quá 500 ký tự tại [Ghi chú] Textarea<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Vui lòng không nhập quá 500 ký tự!"<br>Trỏ chuột tại [Ghi chú] Textarea |
| X-32 | Nhập ghi chú toàn ký tự trống | Tại màn hình Thêm cán bộ:<br>1. Nhập toàn ký tự trống tại [Ghi chú] Textarea<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Vui lòng nhập nội dung!"<br>Trỏ chuột tại [Ghi chú] Textarea |

---

## 12. [MẬT KHẨU] - PASSWORD

| ID | Mô tả test case | Các bước thực hiện | Kết quả mong đợi |
|---|---|---|---|
| X-33 | Không nhập mật khẩu | Tại màn hình Thêm cán bộ:<br>1. Không nhập dữ liệu vào [Mật khẩu] Password<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Vui lòng nhập mật khẩu!"<br>Trỏ chuột tại [Mật khẩu] Password |
| X-34 | Nhập mật khẩu quá ngắn | Tại màn hình Thêm cán bộ:<br>1. Nhập mật khẩu < 8 ký tự tại [Mật khẩu] Password<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Mật khẩu phải từ 8 ký tự trở lên!"<br>Trỏ chuột tại [Mật khẩu] Password |
| X-35 | Nhập mật khẩu không đúng yêu cầu | Tại màn hình Thêm cán bộ:<br>1. Nhập mật khẩu không có chữ hoa, số, ký tự đặc biệt tại [Mật khẩu] Password<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Mật khẩu phải chứa chữ hoa, số và ký tự đặc biệt!"<br>Trỏ chuột tại [Mật khẩu] Password |

---

## 13. [WEBSITE] - URL

| ID | Mô tả test case | Các bước thực hiện | Kết quả mong đợi |
|---|---|---|---|
| X-36 | Không nhập URL website | Tại màn hình Thêm cán bộ:<br>1. Không nhập dữ liệu vào [Website] URL<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Vui lòng nhập địa chỉ website!"<br>Trỏ chuột tại [Website] URL |
| X-37 | Nhập URL không đúng định dạng | Tại màn hình Thêm cán bộ:<br>1. Nhập URL không có http/https tại [Website] URL<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "URL không hợp lệ!"<br>Trỏ chuột tại [Website] URL |
| X-38 | Nhập URL quá dài | Tại màn hình Thêm cán bộ:<br>1. Nhập quá 100 ký tự tại [Website] URL<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Vui lòng không nhập quá 100 ký tự!"<br>Trỏ chuột tại [Website] URL |

---

## 14. [TUỔI] - NUMBER

| ID | Mô tả test case | Các bước thực hiện | Kết quả mong đợi |
|---|---|---|---|
| X-39 | Không nhập tuổi | Tại màn hình Thêm cán bộ:<br>1. Không nhập dữ liệu vào [Tuổi] Number<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Vui lòng nhập tuổi!"<br>Trỏ chuột tại [Tuổi] Number |
| X-40 | Nhập tuổi < 18 | Tại màn hình Thêm cán bộ:<br>1. Nhập tuổi < 18 tại [Tuổi] Number<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Tuổi phải từ 18 trở lên!"<br>Trỏ chuột tại [Tuổi] Number |
| X-41 | Nhập tuổi > 65 | Tại màn hình Thêm cán bộ:<br>1. Nhập tuổi > 65 tại [Tuổi] Number<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Tuổi không được vượt quá 65!"<br>Trỏ chuột tại [Tuổi] Number |
| X-42 | Nhập tuổi có ký tự chữ | Tại màn hình Thêm cán bộ:<br>1. Nhập ký tự chữ tại [Tuổi] Number<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Vui lòng chỉ nhập số!"<br>Trỏ chuột tại [Tuổi] Number |

---

## 15. [LƯƠNG] - RANGE

| ID | Mô tả test case | Các bước thực hiện | Kết quả mong đợi |
|---|---|---|---|
| X-43 | Không chọn mức lương | Tại màn hình Thêm cán bộ:<br>1. Không chọn giá trị tại [Lương] Range<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Vui lòng chọn mức lương!"<br>Trỏ chuột tại [Lương] Range |
| X-44 | Chọn mức lương < min | Tại màn hình Thêm cán bộ:<br>1. Chọn mức lương < 5.000.000 tại [Lương] Range<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Lương tối thiểu là 5.000.000đ!"<br>Trỏ chuột tại [Lương] Range |

---

## 16. [GIỜ LÀM VIỆC] - TIME

| ID | Mô tả test case | Các bước thực hiện | Kết quả mong đợi |
|---|---|---|---|
| X-45 | Không chọn giờ làm việc | Tại màn hình Thêm cán bộ:<br>1. Không chọn giờ tại [Giờ làm việc] Time<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Vui lòng chọn giờ làm việc!"<br>Trỏ chuột tại [Giờ làm việc] Time |
| X-46 | Chọn giờ ngoài giờ hành chính | Tại màn hình Thêm cán bộ:<br>1. Chọn giờ < 6h hoặc > 22h tại [Giờ làm việc] Time<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Giờ làm việc không hợp lệ!"<br>Trỏ chuột tại [Giờ làm việc] Time |

---

## 17. [THÁNG TUYỂN DỤNG] - MONTH

| ID | Mô tả test case | Các bước thực hiện | Kết quả mong đợi |
|---|---|---|---|
| X-47 | Không chọn tháng tuyển dụng | Tại màn hình Thêm cán bộ:<br>1. Không chọn tháng tại [Tháng tuyển dụng] Month<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Vui lòng chọn tháng tuyển dụng!"<br>Trỏ chuột tại [Tháng tuyển dụng] Month |
| X-48 | Chọn tháng trong quá khứ | Tại màn hình Thêm cán bộ:<br>1. Chọn tháng < tháng hiện tại tại [Tháng tuyển dụng] Month<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Không thể chọn tháng trong quá khứ!"<br>Trỏ chuột tại [Tháng tuyển dụng] Month |

---

## 18. [NHẬN TIN] - CHECKBOX

| ID | Mô tả test case | Các bước thực hiện | Kết quả mong đợi |
|---|---|---|---|
| X-49 | Không chọn checkbox nhận tin | Tại màn hình Thêm cán bộ:<br>1. Không check [Nhận tin] Checkbox<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Vui lòng đồng ý nhận thông tin!"<br>Trỏ chuột tại [Nhận tin] Checkbox |

---

## 19. [LOẠI HỢP ĐỒNG] - RADIO

| ID | Mô tả test case | Các bước thực hiện | Kết quả mong đợi |
|---|---|---|---|
| X-50 | Không chọn loại hợp đồng | Tại màn hình Thêm cán bộ:<br>1. Không chọn radio tại [Loại hợp đồng] Radio<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Vui lòng chọn loại hợp đồng!"<br>Trỏ chuột tại [Loại hợp đồng] Radio |

---

## 20. [PHÒNG BAN] - DROPDOWN

| ID | Mô tả test case | Các bước thực hiện | Kết quả mong đợi |
|---|---|---|---|
| X-51 | Không chọn phòng ban | Tại màn hình Thêm cán bộ:<br>1. Không chọn giá trị tại [Phòng ban] Dropdown<br>2. Nhấn [Thêm] button | Hiển thị thông báo: "Vui lòng chọn phòng ban!"<br>Trỏ chuột tại [Phòng ban] Dropdown |

---
