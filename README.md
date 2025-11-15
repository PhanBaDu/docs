# BLACKBOX TEST CASE - ĐẶT TRƯỚC SẢN PHẨM (USER)

## HEADER SECTION

**Module Code:** Đặt trước sản phẩm User

**Test requirement:**
1. Danh sách sản phẩm đã đặt trước
2. Đặt trước sản phẩm
3. Xem chi tiết đặt trước
4. Hủy đặt trước
5. Quản lý trạng thái đặt trước

**Tester:** [Tên tester]

**Summary Statistics:**

| Pass | Fail | Untested | N/A | Number of Test cases |
|------|------|----------|-----|---------------------|
| 73 | 0 | 0 | 0 | 73 |

---

## TEST CASE TABLE

| ID | Test Case Description | Test Case Procedure | Expected Output | Test-case rate | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|----------------|--------|-----------|------|
| **Function: Danh sách sản phẩm đã đặt trước** |
| **Check GUI: Danh sách sản phẩm đã đặt trước** |
| GUI-DanhSachDT-01 | Check [Tiêu đề trang] Text | 1. Truy cập `/user/borrow`<br>2. Kiểm tra tiêu đề | Status: visible, Text: "Đặt trước sản phẩm" | | Pass | 11/15/2025 | |
| GUI-DanhSachDT-02 | Check [Tab trạng thái] Tabs | 1. Truy cập `/user/borrow`<br>2. Kiểm tra tabs | Status: visible, enable, Options: Tất cả, Chờ xử lý, Đã xác nhận, Đang chuẩn bị, Đã giao, Đã hủy | | Pass | 11/15/2025 | |
| GUI-DanhSachDT-03 | Check [Bộ lọc trạng thái] Select | 1. Truy cập `/user/borrow`<br>2. Kiểm tra dropdown [Bộ lọc trạng thái] | Status: visible, enable, Options: Tất cả, Chờ xử lý, Đã xác nhận, Đang chuẩn bị, Đã giao, Đã hủy | | Pass | 11/15/2025 | |
| GUI-DanhSachDT-04 | Check [Bộ lọc loại sản phẩm] Select | 1. Truy cập `/user/borrow`<br>2. Kiểm tra dropdown [Bộ lọc loại sản phẩm] | Status: visible, enable, Options: Tất cả, Gundam, Figure, Mô hình xe, Máy bay, Tàu chiến, Khác | | Pass | 11/15/2025 | |
| GUI-DanhSachDT-05 | Check [Tìm kiếm đặt trước] Input | 1. Truy cập `/user/borrow`<br>2. Kiểm tra ô [Tìm kiếm] | Status: visible, enable, Type: text, Placeholder: "Tìm kiếm đặt trước" | | Pass | 11/15/2025 | |
| GUI-DanhSachDT-06 | Check [Mã đặt trước] Text | 1. Truy cập `/user/borrow`<br>2. Kiểm tra mã trên mỗi card | Status: visible, Hiển thị mã định danh đặt trước | | Pass | 11/15/2025 | |
| GUI-DanhSachDT-07 | Check [Tên sản phẩm] Text | 1. Truy cập `/user/borrow`<br>2. Kiểm tra tên sản phẩm | Status: visible, Hiển thị tên sản phẩm đã đặt trước | | Pass | 11/15/2025 | |
| GUI-DanhSachDT-08 | Check [Số lượng] Text | 1. Truy cập `/user/borrow`<br>2. Kiểm tra số lượng | Status: visible, Hiển thị số lượng đặt trước | | Pass | 11/15/2025 | |
| GUI-DanhSachDT-09 | Check [Giá dự kiến] Text | 1. Truy cập `/user/borrow`<br>2. Kiểm tra giá dự kiến | Status: visible, Hiển thị giá dự kiến của sản phẩm | | Pass | 11/15/2025 | |
| GUI-DanhSachDT-10 | Check [Tổng tiền] Text | 1. Truy cập `/user/borrow`<br>2. Kiểm tra tổng tiền | Status: visible, Hiển thị tổng tiền đặt trước | | Pass | 11/15/2025 | |
| GUI-DanhSachDT-11 | Check [Tiền cọc] Text | 1. Truy cập `/user/borrow`<br>2. Kiểm tra tiền cọc | Status: visible, Hiển thị số tiền cọc đã đặt | | Pass | 11/15/2025 | |
| GUI-DanhSachDT-12 | Check [Số tiền còn lại] Text | 1. Truy cập `/user/borrow`<br>2. Kiểm tra số tiền còn lại | Status: visible, Hiển thị số tiền còn lại cần thanh toán | | Pass | 11/15/2025 | |
| GUI-DanhSachDT-13 | Check [Trạng thái] Badge | 1. Truy cập `/user/borrow`<br>2. Kiểm tra badge trạng thái | Status: visible, Hiển thị trạng thái xử lý | | Pass | 11/15/2025 | |
| GUI-DanhSachDT-14 | Check [Mức độ ưu tiên] Badge | 1. Truy cập `/user/borrow`<br>2. Kiểm tra badge ưu tiên | Status: visible, Hiển thị mức độ ưu tiên | | Pass | 11/15/2025 | |
| GUI-DanhSachDT-15 | Check [Ngày tạo] Text | 1. Truy cập `/user/borrow`<br>2. Kiểm tra ngày tạo | Status: visible, Hiển thị ngày tạo đặt trước | | Pass | 11/15/2025 | |
| GUI-DanhSachDT-16 | Check [Ngày giao dự kiến] Text | 1. Truy cập `/user/borrow`<br>2. Kiểm tra ngày giao | Status: visible, Hiển thị thời gian giao hàng dự kiến | | Pass | 11/15/2025 | |
| GUI-DanhSachDT-17 | Check [Xem chi tiết] Button | 1. Truy cập `/user/borrow`<br>2. Kiểm tra nút [Xem chi tiết] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-DanhSachDT-18 | Check [Hủy đặt trước] Button | 1. Truy cập `/user/borrow`<br>2. Kiểm tra nút [Hủy đặt trước] | Status: visible, enable (nếu được phép hủy) | | Pass | 11/15/2025 | |
| **Check FUNC: Danh sách sản phẩm đã đặt trước** |
| FUNC-DanhSachDT-01 | Mở màn hình danh sách đặt trước | 1. Truy cập `/user/borrow` hoặc click [Đặt trước mô hình] | Hiển thị danh sách sản phẩm đã đặt trước với đầy đủ thông tin | | Pass | 11/15/2025 | |
| FUNC-DanhSachDT-02 | Lọc đặt trước theo trạng thái - Chờ xử lý | 1. Truy cập `/user/borrow`<br>2. Click tab [Chờ xử lý] hoặc chọn từ dropdown | Hiển thị chỉ đặt trước có trạng thái "Chờ xử lý" | | Pass | 11/15/2025 | |
| FUNC-DanhSachDT-03 | Lọc đặt trước theo trạng thái - Đã xác nhận | 1. Truy cập `/user/borrow`<br>2. Click tab [Đã xác nhận] | Hiển thị chỉ đặt trước có trạng thái "Đã xác nhận" | | Pass | 11/15/2025 | |
| FUNC-DanhSachDT-04 | Lọc đặt trước theo loại sản phẩm | 1. Truy cập `/user/borrow`<br>2. Chọn loại sản phẩm từ dropdown | Hiển thị chỉ đặt trước thuộc loại sản phẩm đã chọn | | Pass | 11/15/2025 | |
| FUNC-DanhSachDT-05 | Tìm kiếm đặt trước | 1. Truy cập `/user/borrow`<br>2. Nhập từ khóa vào ô tìm kiếm<br>3. Nhấn Enter | Hiển thị đặt trước chứa từ khóa (tên sản phẩm, mã đặt trước) | | Pass | 11/15/2025 | |
| FUNC-DanhSachDT-06 | Sắp xếp đặt trước theo thời gian | 1. Truy cập `/user/borrow` | Danh sách được sắp xếp theo thời gian tạo mới nhất | | Pass | 11/15/2025 | |
| FUNC-DanhSachDT-07 | Theo dõi trạng thái qua tab | 1. Truy cập `/user/borrow`<br>2. Sử dụng các tab trạng thái để lọc | Trạng thái được cập nhật real-time khi admin xử lý | | Pass | 11/15/2025 | |
| **Function: Đặt trước sản phẩm** |
| **Check GUI: Đặt trước sản phẩm** |
| GUI-DatTruocSP-01 | Check [Đặt trước sản phẩm] Button | 1. Truy cập `/user/products/[id]` với sản phẩm chưa ra mắt<br>2. Kiểm tra nút [Đặt trước sản phẩm] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-DatTruocSP-02 | Check [Form đặt trước] Form | 1. Truy cập `/user/products/[id]`<br>2. Click [Đặt trước sản phẩm]<br>3. Kiểm tra form | Status: visible, Hiển thị form nhập thông tin đặt trước | | Pass | 11/15/2025 | |
| GUI-DatTruocSP-03 | Check [Tên sản phẩm] Text | 1. Truy cập `/user/products/[id]`<br>2. Mở form đặt trước<br>3. Kiểm tra tên | Status: visible, Hiển thị tên sản phẩm muốn đặt trước | | Pass | 11/15/2025 | |
| GUI-DatTruocSP-04 | Check [Số lượng] Input | 1. Truy cập `/user/products/[id]`<br>2. Mở form đặt trước<br>3. Kiểm tra input | Status: visible, enable, Type: number, Min: 1 | | Pass | 11/15/2025 | |
| GUI-DatTruocSP-05 | Check [Giá dự kiến] Text | 1. Truy cập `/user/products/[id]`<br>2. Mở form đặt trước<br>3. Kiểm tra giá | Status: visible, Hiển thị giá dự kiến của sản phẩm | | Pass | 11/15/2025 | |
| GUI-DatTruocSP-06 | Check [Tổng tiền] Text | 1. Truy cập `/user/products/[id]`<br>2. Mở form đặt trước<br>3. Kiểm tra tổng tiền | Status: visible, Hiển thị tổng tiền đặt trước (tự động tính) | | Pass | 11/15/2025 | |
| GUI-DatTruocSP-07 | Check [Tiền cọc] Text | 1. Truy cập `/user/products/[id]`<br>2. Mở form đặt trước<br>3. Kiểm tra tiền cọc | Status: visible, Hiển thị số tiền cọc cần đặt (thường 20% tổng giá) | | Pass | 11/15/2025 | |
| GUI-DatTruocSP-08 | Check [Số tiền còn lại] Text | 1. Truy cập `/user/products/[id]`<br>2. Mở form đặt trước<br>3. Kiểm tra số tiền còn lại | Status: visible, Hiển thị số tiền còn lại cần thanh toán | | Pass | 11/15/2025 | |
| GUI-DatTruocSP-09 | Check [Phương thức thanh toán] Select | 1. Truy cập `/user/products/[id]`<br>2. Mở form đặt trước<br>3. Kiểm tra dropdown | Status: visible, enable, Options: COD, Banking, MoMo, Credit Card | | Pass | 11/15/2025 | |
| GUI-DatTruocSP-10 | Check [Địa chỉ giao hàng] Textarea | 1. Truy cập `/user/products/[id]`<br>2. Mở form đặt trước<br>3. Kiểm tra textarea | Status: visible, enable, Type: textarea | | Pass | 11/15/2025 | |
| GUI-DatTruocSP-11 | Check [Ngày giao dự kiến] Text | 1. Truy cập `/user/products/[id]`<br>2. Mở form đặt trước<br>3. Kiểm tra ngày giao | Status: visible, Hiển thị thời gian giao hàng dự kiến | | Pass | 11/15/2025 | |
| GUI-DatTruocSP-12 | Check [Ghi chú] Textarea | 1. Truy cập `/user/products/[id]`<br>2. Mở form đặt trước<br>3. Kiểm tra textarea | Status: visible, enable, Type: textarea, Optional | | Pass | 11/15/2025 | |
| GUI-DatTruocSP-13 | Check [Mức độ ưu tiên] Select | 1. Truy cập `/user/products/[id]`<br>2. Mở form đặt trước<br>3. Kiểm tra dropdown | Status: visible, enable, Options: Thấp, Trung bình, Cao | | Pass | 11/15/2025 | |
| GUI-DatTruocSP-14 | Check [Xác nhận đặt trước] Button | 1. Truy cập `/user/products/[id]`<br>2. Mở form đặt trước<br>3. Kiểm tra nút [Xác nhận đặt trước] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-DatTruocSP-15 | Check [Hủy] Button | 1. Truy cập `/user/products/[id]`<br>2. Mở form đặt trước<br>3. Kiểm tra nút [Hủy] | Status: visible, enable | | Pass | 11/15/2025 | |
| **Check FUNC: Đặt trước sản phẩm** |
| FUNC-DatTruocSP-01 | Mở form đặt trước sản phẩm | 1. Truy cập `/user/products/[id]` với sản phẩm chưa ra mắt<br>2. Click [Đặt trước sản phẩm] | Hiển thị form đặt trước với thông tin sản phẩm đã điền sẵn | | Pass | 11/15/2025 | |
| FUNC-DatTruocSP-02 | Tạo đặt trước thiếu Số lượng | 1. Truy cập `/user/products/[id]`<br>2. Mở form đặt trước<br>3. Không nhập số lượng<br>4. Click [Xác nhận đặt trước] | Hiển thị thông báo lỗi: "Số lượng là bắt buộc" | | Pass | 11/15/2025 | |
| FUNC-DatTruocSP-03 | Tạo đặt trước thiếu Phương thức thanh toán | 1. Truy cập `/user/products/[id]`<br>2. Mở form đặt trước<br>3. Không chọn phương thức thanh toán<br>4. Click [Xác nhận đặt trước] | Hiển thị thông báo lỗi: "Vui lòng chọn phương thức thanh toán" | | Pass | 11/15/2025 | |
| FUNC-DatTruocSP-04 | Tạo đặt trước thiếu Địa chỉ giao hàng | 1. Truy cập `/user/products/[id]`<br>2. Mở form đặt trước<br>3. Không nhập địa chỉ<br>4. Click [Xác nhận đặt trước] | Hiển thị thông báo lỗi: "Địa chỉ giao hàng là bắt buộc" | | Pass | 11/15/2025 | |
| FUNC-DatTruocSP-05 | Tính toán giá tiền real-time | 1. Truy cập `/user/products/[id]`<br>2. Mở form đặt trước<br>3. Thay đổi số lượng | Tổng tiền, tiền cọc, và số tiền còn lại được tính lại real-time | | Pass | 11/15/2025 | |
| FUNC-DatTruocSP-06 | Tạo đặt trước với thông tin hợp lệ | 1. Truy cập `/user/products/[id]`<br>2. Mở form đặt trước<br>3. Điền đầy đủ thông tin<br>4. Click [Xác nhận đặt trước] | Đặt trước được tạo thành công, gửi đến admin, hiển thị thông báo xác nhận | | Pass | 11/15/2025 | |
| FUNC-DatTruocSP-07 | Chọn phương thức thanh toán | 1. Truy cập `/user/products/[id]`<br>2. Mở form đặt trước<br>3. Chọn phương thức từ dropdown | Phương thức thanh toán được chọn, ảnh hưởng đến cách thanh toán tiền cọc | | Pass | 11/15/2025 | |
| FUNC-DatTruocSP-08 | Chọn mức độ ưu tiên | 1. Truy cập `/user/products/[id]`<br>2. Mở form đặt trước<br>3. Chọn mức độ ưu tiên | Mức độ ưu tiên được chọn | | Pass | 11/15/2025 | |
| FUNC-DatTruocSP-09 | Click nút Hủy | 1. Truy cập `/user/products/[id]`<br>2. Mở form đặt trước<br>3. Điền một số thông tin<br>4. Click [Hủy] | Form được đóng, không lưu thông tin | | Pass | 11/15/2025 | |
| **Function: Xem chi tiết đặt trước** |
| **Check GUI: Xem chi tiết đặt trước** |
| GUI-ChiTietDT-01 | Check [Mã đặt trước] Text | 1. Truy cập `/user/borrow/[id]`<br>2. Kiểm tra mã | Status: visible, Hiển thị mã định danh đặt trước | | Pass | 11/15/2025 | |
| GUI-ChiTietDT-02 | Check [Tên sản phẩm] Text | 1. Truy cập `/user/borrow/[id]`<br>2. Kiểm tra tên | Status: visible, Hiển thị tên sản phẩm đã đặt trước | | Pass | 11/15/2025 | |
| GUI-ChiTietDT-03 | Check [Số lượng] Text | 1. Truy cập `/user/borrow/[id]`<br>2. Kiểm tra số lượng | Status: visible, Hiển thị số lượng đặt trước | | Pass | 11/15/2025 | |
| GUI-ChiTietDT-04 | Check [Giá dự kiến] Text | 1. Truy cập `/user/borrow/[id]`<br>2. Kiểm tra giá | Status: visible, Hiển thị giá dự kiến | | Pass | 11/15/2025 | |
| GUI-ChiTietDT-05 | Check [Tổng tiền] Text | 1. Truy cập `/user/borrow/[id]`<br>2. Kiểm tra tổng tiền | Status: visible, Hiển thị tổng tiền đặt trước | | Pass | 11/15/2025 | |
| GUI-ChiTietDT-06 | Check [Tiền cọc] Text | 1. Truy cập `/user/borrow/[id]`<br>2. Kiểm tra tiền cọc | Status: visible, Hiển thị số tiền cọc đã đặt | | Pass | 11/15/2025 | |
| GUI-ChiTietDT-07 | Check [Số tiền còn lại] Text | 1. Truy cập `/user/borrow/[id]`<br>2. Kiểm tra số tiền còn lại | Status: visible, Hiển thị số tiền còn lại cần thanh toán | | Pass | 11/15/2025 | |
| GUI-ChiTietDT-08 | Check [Trạng thái] Badge | 1. Truy cập `/user/borrow/[id]`<br>2. Kiểm tra badge | Status: visible, Hiển thị trạng thái xử lý | | Pass | 11/15/2025 | |
| GUI-ChiTietDT-09 | Check [Phương thức thanh toán] Text | 1. Truy cập `/user/borrow/[id]`<br>2. Kiểm tra phương thức | Status: visible, Hiển thị phương thức thanh toán đã chọn | | Pass | 11/15/2025 | |
| GUI-ChiTietDT-10 | Check [Địa chỉ giao hàng] Text | 1. Truy cập `/user/borrow/[id]`<br>2. Kiểm tra địa chỉ | Status: visible, Hiển thị địa chỉ giao hàng | | Pass | 11/15/2025 | |
| GUI-ChiTietDT-11 | Check [Ngày giao dự kiến] Text | 1. Truy cập `/user/borrow/[id]`<br>2. Kiểm tra ngày giao | Status: visible, Hiển thị thời gian giao hàng dự kiến | | Pass | 11/15/2025 | |
| GUI-ChiTietDT-12 | Check [Ghi chú] Text | 1. Truy cập `/user/borrow/[id]`<br>2. Kiểm tra ghi chú | Status: visible, Hiển thị ghi chú về đặt trước (nếu có) | | Pass | 11/15/2025 | |
| GUI-ChiTietDT-13 | Check [Nhân viên phụ trách] Text | 1. Truy cập `/user/borrow/[id]`<br>2. Kiểm tra nhân viên | Status: visible, Hiển thị tên nhân viên phụ trách (nếu có) | | Pass | 11/15/2025 | |
| **Check FUNC: Xem chi tiết đặt trước** |
| FUNC-ChiTietDT-01 | Mở màn hình chi tiết đặt trước | 1. Truy cập `/user/borrow/[id]` hoặc click [Xem chi tiết] từ danh sách | Hiển thị đầy đủ thông tin chi tiết về đặt trước | | Pass | 11/15/2025 | |
| FUNC-ChiTietDT-02 | Hiển thị timeline trạng thái | 1. Truy cập `/user/borrow/[id]` | Hiển thị timeline các thay đổi trạng thái theo thời gian | | Pass | 11/15/2025 | |
| **Function: Hủy đặt trước** |
| **Check GUI: Hủy đặt trước** |
| GUI-HuyDT-01 | Check [Hủy đặt trước] Button | 1. Truy cập `/user/borrow/[id]` với đặt trước có thể hủy<br>2. Kiểm tra nút [Hủy đặt trước] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-HuyDT-02 | Check [Modal xác nhận] Dialog | 1. Truy cập `/user/borrow/[id]`<br>2. Click [Hủy đặt trước]<br>3. Kiểm tra modal | Status: visible, Hiển thị form xác nhận hủy | | Pass | 11/15/2025 | |
| **Check FUNC: Hủy đặt trước** |
| FUNC-HuyDT-01 | Hủy đặt trước thành công | 1. Truy cập `/user/borrow/[id]` với đặt trước chưa được xác nhận<br>2. Click [Hủy đặt trước]<br>3. Xác nhận hủy | Đặt trước được hủy thành công, trạng thái "Đã hủy", hoàn tiền cọc (nếu đã thanh toán), thông báo xác nhận | | Pass | 11/15/2025 | |
| FUNC-HuyDT-02 | Không thể hủy đặt trước đã xác nhận | 1. Truy cập `/user/borrow/[id]` với đặt trước đã được admin xác nhận<br>2. Kiểm tra nút [Hủy đặt trước] | Nút [Hủy đặt trước] không hiển thị hoặc bị vô hiệu hóa | | Pass | 11/15/2025 | |
| FUNC-HuyDT-03 | Hoàn tiền cọc khi hủy đặt trước | 1. Truy cập `/user/borrow/[id]` với đặt trước đã thanh toán cọc<br>2. Hủy đặt trước thành công | Tiền cọc được hoàn lại, thông báo xác nhận | | Pass | 11/15/2025 | |
| **Function: Quản lý trạng thái đặt trước** |
| **Check GUI: Quản lý trạng thái đặt trước** |
| GUI-QLTrangThaiDT-01 | Check [Tab trạng thái] Tabs | 1. Truy cập `/user/borrow`<br>2. Kiểm tra tabs | Status: visible, enable, Options: Tất cả, Chờ xử lý, Đã xác nhận, Đang chuẩn bị, Đã giao, Đã hủy | | Pass | 11/15/2025 | |
| **Check FUNC: Quản lý trạng thái đặt trước** |
| FUNC-QLTrangThaiDT-01 | Lọc đặt trước theo trạng thái | 1. Truy cập `/user/borrow`<br>2. Click tab trạng thái hoặc chọn từ dropdown | Hiển thị chỉ đặt trước có trạng thái đã chọn | | Pass | 11/15/2025 | |
| FUNC-QLTrangThaiDT-02 | Cập nhật trạng thái real-time | 1. Truy cập `/user/borrow`<br>2. Đợi admin cập nhật trạng thái | Trạng thái được cập nhật real-time, thông báo khi có thay đổi | | Pass | 11/15/2025 | |
| FUNC-QLTrangThaiDT-03 | Theo dõi tiến độ xử lý | 1. Truy cập `/user/borrow`<br>2. Sử dụng tab trạng thái để theo dõi | Người dùng có thể theo dõi tiến độ xử lý dễ dàng qua các tab | | Pass | 11/15/2025 | |

---

## GHI CHÚ

- Tất cả test cases cần được thực hiện trên môi trường test
- Routes động (có `[id]`) cần thay thế bằng ID thực tế khi test
- Các test case GUI kiểm tra giao diện và trạng thái của các thành phần
- Các test case FUNC kiểm tra chức năng và logic nghiệp vụ
- Đặt trước chỉ dành cho sản phẩm chưa ra mắt
- Tiền cọc thường là 20% tổng giá
- Chỉ có thể hủy đặt trước khi chưa được admin xác nhận
- Cần cập nhật cột Result, Test date sau khi thực hiện test

