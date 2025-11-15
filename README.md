# BLACKBOX TEST CASE - TẠO - HIỂN THỊ BÀI VIẾT (USER)

## HEADER SECTION

**Module Code:** Tạo - hiển thị bài viết User

**Test requirement:**
1. Hiển thị danh sách bài viết
2. Xem chi tiết bài viết
3. Tạo bài viết
4. Chỉnh sửa bài viết
5. Xóa bài viết

**Tester:** [Tên tester]

**Summary Statistics:**

| Pass | Fail | Untested | N/A | Number of Test cases |
|------|------|----------|-----|---------------------|
| 84 | 0 | 0 | 0 | 84 |

---

## TEST CASE TABLE

| ID | Test Case Description | Test Case Procedure | Expected Output | Test-case rate | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|----------------|--------|-----------|------|
| **Function: Hiển thị danh sách bài viết** |
| **Check GUI: Hiển thị danh sách bài viết** |
| GUI-DanhSachBV-01 | Check [Tiêu đề trang] Text | 1. Truy cập `/user/community`<br>2. Kiểm tra tiêu đề | Status: visible, Text: "Cộng đồng mô hình" | | Pass | 11/15/2025 | |
| GUI-DanhSachBV-02 | Check [Tab danh mục] Tabs | 1. Truy cập `/user/community`<br>2. Kiểm tra tabs | Status: visible, enable, Options: Tất cả, Gundam, Figure, Mô hình xe, Máy bay, Khác | | Pass | 11/15/2025 | |
| GUI-DanhSachBV-03 | Check [Bộ lọc danh mục] Select | 1. Truy cập `/user/community`<br>2. Kiểm tra dropdown [Bộ lọc danh mục] | Status: visible, enable, Options: Tất cả, Gundam, Figure, Mô hình xe, Máy bay, Khác | | Pass | 11/15/2025 | |
| GUI-DanhSachBV-04 | Check [Bộ lọc thời gian] Select | 1. Truy cập `/user/community`<br>2. Kiểm tra dropdown [Bộ lọc thời gian] | Status: visible, enable, Options: Hôm nay, Tuần này, Tháng này, Tất cả | | Pass | 11/15/2025 | |
| GUI-DanhSachBV-05 | Check [Bộ lọc sắp xếp] Select | 1. Truy cập `/user/community`<br>2. Kiểm tra dropdown [Sắp xếp] | Status: visible, enable, Options: Mới nhất, Nhiều like nhất, Nhiều bình luận nhất | | Pass | 11/15/2025 | |
| GUI-DanhSachBV-06 | Check [Tìm kiếm bài viết] Input | 1. Truy cập `/user/community`<br>2. Kiểm tra ô [Tìm kiếm] | Status: visible, enable, Type: text, Placeholder: "Tìm kiếm bài viết" | | Pass | 11/15/2025 | |
| GUI-DanhSachBV-07 | Check [Card bài viết] Card | 1. Truy cập `/user/community`<br>2. Kiểm tra card | Status: visible, Hiển thị thông tin bài viết | | Pass | 11/15/2025 | |
| GUI-DanhSachBV-08 | Check [Ảnh đại diện tác giả] Avatar | 1. Truy cập `/user/community`<br>2. Kiểm tra avatar | Status: visible, Hiển thị ảnh đại diện người đăng | | Pass | 11/15/2025 | |
| GUI-DanhSachBV-09 | Check [Tên tác giả] Text | 1. Truy cập `/user/community`<br>2. Kiểm tra tên | Status: visible, Hiển thị tên người đăng bài viết | | Pass | 11/15/2025 | |
| GUI-DanhSachBV-10 | Check [Thời gian đăng] Text | 1. Truy cập `/user/community`<br>2. Kiểm tra thời gian | Status: visible, Hiển thị thời gian bài viết được đăng | | Pass | 11/15/2025 | |
| GUI-DanhSachBV-11 | Check [Tiêu đề bài viết] Text | 1. Truy cập `/user/community`<br>2. Kiểm tra tiêu đề | Status: visible, Hiển thị tiêu đề bài viết | | Pass | 11/15/2025 | |
| GUI-DanhSachBV-12 | Check [Nội dung tóm tắt] Text | 1. Truy cập `/user/community`<br>2. Kiểm tra nội dung | Status: visible, Hiển thị nội dung tóm tắt bài viết | | Pass | 11/15/2025 | |
| GUI-DanhSachBV-13 | Check [Hình ảnh bài viết] Image | 1. Truy cập `/user/community`<br>2. Kiểm tra hình ảnh | Status: visible, Hiển thị hình ảnh mô hình trong bài viết | | Pass | 11/15/2025 | |
| GUI-DanhSachBV-14 | Check [Video bài viết] Video | 1. Truy cập `/user/community`<br>2. Kiểm tra video | Status: visible, Hiển thị video mô hình trong bài viết | | Pass | 11/15/2025 | |
| GUI-DanhSachBV-15 | Check [Số lượng like] Badge | 1. Truy cập `/user/community`<br>2. Kiểm tra badge | Status: visible, Hiển thị số lượng người thích bài viết | | Pass | 11/15/2025 | |
| GUI-DanhSachBV-16 | Check [Số lượng bình luận] Badge | 1. Truy cập `/user/community`<br>2. Kiểm tra badge | Status: visible, Hiển thị số lượng bình luận | | Pass | 11/15/2025 | |
| GUI-DanhSachBV-17 | Check [Số lượng chia sẻ] Badge | 1. Truy cập `/user/community`<br>2. Kiểm tra badge | Status: visible, Hiển thị số lượng người chia sẻ | | Pass | 11/15/2025 | |
| GUI-DanhSachBV-18 | Check [Nút like] Button | 1. Truy cập `/user/community`<br>2. Kiểm tra nút [Like] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-DanhSachBV-19 | Check [Nút bình luận] Button | 1. Truy cập `/user/community`<br>2. Kiểm tra nút [Bình luận] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-DanhSachBV-20 | Check [Nút chia sẻ] Button | 1. Truy cập `/user/community`<br>2. Kiểm tra nút [Chia sẻ] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-DanhSachBV-21 | Check [Nút xem chi tiết] Button | 1. Truy cập `/user/community`<br>2. Kiểm tra nút [Xem chi tiết] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-DanhSachBV-22 | Check [Phân trang] Pagination | 1. Truy cập `/user/community`<br>2. Kiểm tra phân trang | Status: visible, enable | | Pass | 11/15/2025 | |
| **Check FUNC: Hiển thị danh sách bài viết** |
| FUNC-DanhSachBV-01 | Mở màn hình danh sách bài viết | 1. Truy cập `/user/community` hoặc click [Cộng đồng] | Hiển thị danh sách bài viết cộng đồng với đầy đủ thông tin | | Pass | 11/15/2025 | |
| FUNC-DanhSachBV-02 | Lọc bài viết theo danh mục - Gundam | 1. Truy cập `/user/community`<br>2. Click tab [Gundam] hoặc chọn từ dropdown | Hiển thị chỉ bài viết về Gundam | | Pass | 11/15/2025 | |
| FUNC-DanhSachBV-03 | Lọc bài viết theo thời gian - Tuần này | 1. Truy cập `/user/community`<br>2. Chọn [Tuần này] từ dropdown | Hiển thị chỉ bài viết trong tuần này | | Pass | 11/15/2025 | |
| FUNC-DanhSachBV-04 | Sắp xếp theo mới nhất | 1. Truy cập `/user/community`<br>2. Chọn [Mới nhất] từ dropdown | Danh sách được sắp xếp theo thời gian đăng mới nhất | | Pass | 11/15/2025 | |
| FUNC-DanhSachBV-05 | Sắp xếp theo nhiều like nhất | 1. Truy cập `/user/community`<br>2. Chọn [Nhiều like nhất] từ dropdown | Danh sách được sắp xếp theo số lượng like giảm dần | | Pass | 11/15/2025 | |
| FUNC-DanhSachBV-06 | Sắp xếp theo nhiều bình luận nhất | 1. Truy cập `/user/community`<br>2. Chọn [Nhiều bình luận nhất] từ dropdown | Danh sách được sắp xếp theo số lượng bình luận giảm dần | | Pass | 11/15/2025 | |
| FUNC-DanhSachBV-07 | Tìm kiếm bài viết | 1. Truy cập `/user/community`<br>2. Nhập từ khóa vào ô tìm kiếm<br>3. Nhấn Enter | Hiển thị bài viết chứa từ khóa (tiêu đề hoặc nội dung) | | Pass | 11/15/2025 | |
| FUNC-DanhSachBV-08 | Phân trang danh sách bài viết | 1. Truy cập `/user/community`<br>2. Scroll xuống hoặc click phân trang | Hiển thị trang tiếp theo của danh sách | | Pass | 11/15/2025 | |
| **Function: Xem chi tiết bài viết** |
| **Check GUI: Xem chi tiết bài viết** |
| GUI-ChiTietBV-01 | Check [Thông tin tác giả] Card | 1. Truy cập `/user/community/[id]`<br>2. Kiểm tra card tác giả | Status: visible, Hiển thị: Avatar, Tên, Số bài viết | | Pass | 11/15/2025 | |
| GUI-ChiTietBV-02 | Check [Nút theo dõi] Button | 1. Truy cập `/user/community/[id]`<br>2. Kiểm tra nút [Theo dõi] | Status: visible, enable, Options: Theo dõi, Bỏ theo dõi | | Pass | 11/15/2025 | |
| GUI-ChiTietBV-03 | Check [Nội dung bài viết] Text | 1. Truy cập `/user/community/[id]`<br>2. Kiểm tra nội dung | Status: visible, Hiển thị nội dung đầy đủ bài viết | | Pass | 11/15/2025 | |
| GUI-ChiTietBV-04 | Check [Hình ảnh bài viết] Gallery | 1. Truy cập `/user/community/[id]`<br>2. Kiểm tra gallery | Status: visible, Hiển thị bộ sưu tập hình ảnh mô hình | | Pass | 11/15/2025 | |
| GUI-ChiTietBV-05 | Check [Video bài viết] Video | 1. Truy cập `/user/community/[id]`<br>2. Kiểm tra video | Status: visible, Hiển thị video mô hình | | Pass | 11/15/2025 | |
| GUI-ChiTietBV-06 | Check [Số lượng like] Badge | 1. Truy cập `/user/community/[id]`<br>2. Kiểm tra badge | Status: visible, Hiển thị số lượng người thích | | Pass | 11/15/2025 | |
| GUI-ChiTietBV-07 | Check [Số lượng bình luận] Badge | 1. Truy cập `/user/community/[id]`<br>2. Kiểm tra badge | Status: visible, Hiển thị số lượng bình luận | | Pass | 11/15/2025 | |
| GUI-ChiTietBV-08 | Check [Số lượng chia sẻ] Badge | 1. Truy cập `/user/community/[id]`<br>2. Kiểm tra badge | Status: visible, Hiển thị số lượng người chia sẻ | | Pass | 11/15/2025 | |
| GUI-ChiTietBV-09 | Check [Nút like] Button | 1. Truy cập `/user/community/[id]`<br>2. Kiểm tra nút [Like] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-ChiTietBV-10 | Check [Nút bình luận] Button | 1. Truy cập `/user/community/[id]`<br>2. Kiểm tra nút [Bình luận] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-ChiTietBV-11 | Check [Nút chia sẻ] Button | 1. Truy cập `/user/community/[id]`<br>2. Kiểm tra nút [Chia sẻ] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-ChiTietBV-12 | Check [Danh sách bình luận] List | 1. Truy cập `/user/community/[id]`<br>2. Kiểm tra danh sách | Status: visible, Hiển thị danh sách bình luận | | Pass | 11/15/2025 | |
| GUI-ChiTietBV-13 | Check [Form bình luận] Form | 1. Truy cập `/user/community/[id]`<br>2. Kiểm tra form | Status: visible, Hiển thị form viết bình luận mới | | Pass | 11/15/2025 | |
| GUI-ChiTietBV-14 | Check [Nút quay lại] Button | 1. Truy cập `/user/community/[id]`<br>2. Kiểm tra nút [Quay lại] | Status: visible, enable | | Pass | 11/15/2025 | |
| **Check FUNC: Xem chi tiết bài viết** |
| FUNC-ChiTietBV-01 | Mở màn hình chi tiết bài viết | 1. Truy cập `/user/community/[id]` hoặc click [Xem chi tiết] từ danh sách | Hiển thị đầy đủ thông tin chi tiết về bài viết | | Pass | 11/15/2025 | |
| FUNC-ChiTietBV-02 | Theo dõi tác giả | 1. Truy cập `/user/community/[id]`<br>2. Click nút [Theo dõi] | Tác giả được thêm vào danh sách theo dõi, nút chuyển thành [Bỏ theo dõi] | | Pass | 11/15/2025 | |
| FUNC-ChiTietBV-03 | Bỏ theo dõi tác giả | 1. Truy cập `/user/community/[id]` với tác giả đã theo dõi<br>2. Click nút [Bỏ theo dõi] | Tác giả bị xóa khỏi danh sách theo dõi, nút chuyển thành [Theo dõi] | | Pass | 11/15/2025 | |
| FUNC-ChiTietBV-04 | Xem gallery hình ảnh | 1. Truy cập `/user/community/[id]`<br>2. Click vào hình ảnh | Hiển thị gallery với khả năng zoom và chuyển ảnh | | Pass | 11/15/2025 | |
| FUNC-ChiTietBV-05 | Xem video bài viết | 1. Truy cập `/user/community/[id]`<br>2. Click play video | Video được phát | | Pass | 11/15/2025 | |
| FUNC-ChiTietBV-06 | Click nút Quay lại | 1. Truy cập `/user/community/[id]`<br>2. Click [Quay lại] | Quay về trang danh sách bài viết | | Pass | 11/15/2025 | |
| **Function: Tạo bài viết** |
| **Check GUI: Tạo bài viết** |
| GUI-TaoBV-01 | Check [Tạo bài viết] Button | 1. Truy cập `/user/community`<br>2. Kiểm tra nút [Tạo bài viết] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-TaoBV-02 | Check [Form tạo bài viết] Form | 1. Truy cập `/user/community`<br>2. Click [Tạo bài viết]<br>3. Kiểm tra form | Status: visible, Hiển thị form nhập thông tin bài viết | | Pass | 11/15/2025 | |
| GUI-TaoBV-03 | Check [Tiêu đề bài viết] Input | 1. Truy cập `/user/community`<br>2. Mở form tạo bài viết<br>3. Kiểm tra ô [Tiêu đề] | Status: visible, enable, Type: text | | Pass | 11/15/2025 | |
| GUI-TaoBV-04 | Check [Nội dung bài viết] Textarea | 1. Truy cập `/user/community`<br>2. Mở form tạo bài viết<br>3. Kiểm tra textarea | Status: visible, enable, Type: textarea | | Pass | 11/15/2025 | |
| GUI-TaoBV-05 | Check [Danh mục] Select | 1. Truy cập `/user/community`<br>2. Mở form tạo bài viết<br>3. Kiểm tra dropdown | Status: visible, enable, Options: Gundam, Figure, Mô hình xe, Máy bay, Khác | | Pass | 11/15/2025 | |
| GUI-TaoBV-06 | Check [Upload hình ảnh] File Input | 1. Truy cập `/user/community`<br>2. Mở form tạo bài viết<br>3. Kiểm tra file input | Status: visible, enable, Type: file, Accept: image/* | | Pass | 11/15/2025 | |
| GUI-TaoBV-07 | Check [Upload video] File Input | 1. Truy cập `/user/community`<br>2. Mở form tạo bài viết<br>3. Kiểm tra file input | Status: visible, enable, Type: file, Accept: video/* | | Pass | 11/15/2025 | |
| GUI-TaoBV-08 | Check [Danh sách file đã upload] List | 1. Truy cập `/user/community`<br>2. Upload file<br>3. Kiểm tra danh sách | Status: visible, Hiển thị file đã upload với nút xóa | | Pass | 11/15/2025 | |
| GUI-TaoBV-09 | Check [Đăng bài] Button | 1. Truy cập `/user/community`<br>2. Mở form tạo bài viết<br>3. Kiểm tra nút [Đăng bài] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-TaoBV-10 | Check [Hủy] Button | 1. Truy cập `/user/community`<br>2. Mở form tạo bài viết<br>3. Kiểm tra nút [Hủy] | Status: visible, enable | | Pass | 11/15/2025 | |
| **Check FUNC: Tạo bài viết** |
| FUNC-TaoBV-01 | Mở form tạo bài viết | 1. Truy cập `/user/community`<br>2. Click [Tạo bài viết] | Hiển thị form tạo bài viết với các trường trống | | Pass | 11/15/2025 | |
| FUNC-TaoBV-02 | Tạo bài viết thiếu Tiêu đề | 1. Truy cập `/user/community`<br>2. Mở form tạo bài viết<br>3. Không nhập Tiêu đề<br>4. Click [Đăng bài] | Hiển thị thông báo lỗi: "Tiêu đề bài viết là bắt buộc" | | Pass | 11/15/2025 | |
| FUNC-TaoBV-03 | Tạo bài viết thiếu Nội dung | 1. Truy cập `/user/community`<br>2. Mở form tạo bài viết<br>3. Không nhập Nội dung<br>4. Click [Đăng bài] | Hiển thị thông báo lỗi: "Nội dung bài viết là bắt buộc" | | Pass | 11/15/2025 | |
| FUNC-TaoBV-04 | Tạo bài viết thiếu Danh mục | 1. Truy cập `/user/community`<br>2. Mở form tạo bài viết<br>3. Không chọn Danh mục<br>4. Click [Đăng bài] | Hiển thị thông báo lỗi: "Vui lòng chọn danh mục" | | Pass | 11/15/2025 | |
| FUNC-TaoBV-05 | Tạo bài viết với thông tin hợp lệ | 1. Truy cập `/user/community`<br>2. Mở form tạo bài viết<br>3. Điền đầy đủ thông tin<br>4. Click [Đăng bài] | Bài viết được tạo thành công, hiển thị trên danh sách, thông báo xác nhận | | Pass | 11/15/2025 | |
| FUNC-TaoBV-06 | Upload hình ảnh bài viết | 1. Truy cập `/user/community`<br>2. Mở form tạo bài viết<br>3. Click [Upload hình ảnh]<br>4. Chọn file ảnh | Ảnh được upload thành công, hiển thị trong danh sách file đã upload | | Pass | 11/15/2025 | |
| FUNC-TaoBV-07 | Upload video bài viết | 1. Truy cập `/user/community`<br>2. Mở form tạo bài viết<br>3. Click [Upload video]<br>4. Chọn file video | Video được upload thành công, hiển thị trong danh sách file đã upload | | Pass | 11/15/2025 | |
| FUNC-TaoBV-08 | Upload file không đúng định dạng | 1. Truy cập `/user/community`<br>2. Mở form tạo bài viết<br>3. Upload file .txt | Hiển thị thông báo lỗi: "File không đúng định dạng" | | Pass | 11/15/2025 | |
| FUNC-TaoBV-09 | Upload file quá lớn | 1. Truy cập `/user/community`<br>2. Mở form tạo bài viết<br>3. Upload file > giới hạn | Hiển thị thông báo lỗi: "File quá lớn" | | Pass | 11/15/2025 | |
| FUNC-TaoBV-10 | Xóa file đã upload | 1. Truy cập `/user/community`<br>2. Upload file<br>3. Click nút xóa trên file | File bị xóa khỏi danh sách | | Pass | 11/15/2025 | |
| FUNC-TaoBV-11 | Click nút Hủy | 1. Truy cập `/user/community`<br>2. Mở form tạo bài viết<br>3. Điền một số thông tin<br>4. Click [Hủy] | Form được đóng, không lưu thông tin | | Pass | 11/15/2025 | |
| **Function: Chỉnh sửa bài viết** |
| **Check GUI: Chỉnh sửa bài viết** |
| GUI-ChinhSuaBV-01 | Check [Chỉnh sửa] Button | 1. Truy cập `/user/community/[id]` với bài viết của mình<br>2. Kiểm tra nút [Chỉnh sửa] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-ChinhSuaBV-02 | Check [Form chỉnh sửa] Form | 1. Truy cập `/user/community/[id]`<br>2. Click [Chỉnh sửa]<br>3. Kiểm tra form | Status: visible, Hiển thị form với thông tin hiện tại đã điền sẵn | | Pass | 11/15/2025 | |
| **Check FUNC: Chỉnh sửa bài viết** |
| FUNC-ChiTietBV-01 | Mở form chỉnh sửa bài viết | 1. Truy cập `/user/community/[id]` với bài viết của mình<br>2. Click [Chỉnh sửa] | Hiển thị form chỉnh sửa với thông tin hiện tại đã điền sẵn | | Pass | 11/15/2025 | |
| FUNC-ChinhSuaBV-02 | Chỉnh sửa tiêu đề bài viết | 1. Truy cập `/user/community/[id]`<br>2. Mở form chỉnh sửa<br>3. Sửa tiêu đề<br>4. Click [Lưu] | Tiêu đề được cập nhật, thông báo xác nhận | | Pass | 11/15/2025 | |
| FUNC-ChinhSuaBV-03 | Chỉnh sửa nội dung bài viết | 1. Truy cập `/user/community/[id]`<br>2. Mở form chỉnh sửa<br>3. Sửa nội dung<br>4. Click [Lưu] | Nội dung được cập nhật, thông báo xác nhận | | Pass | 11/15/2025 | |
| FUNC-ChinhSuaBV-04 | Chỉnh sửa danh mục bài viết | 1. Truy cập `/user/community/[id]`<br>2. Mở form chỉnh sửa<br>3. Chọn danh mục mới<br>4. Click [Lưu] | Danh mục được cập nhật | | Pass | 11/15/2025 | |
| FUNC-ChinhSuaBV-05 | Chỉnh sửa hình ảnh bài viết | 1. Truy cập `/user/community/[id]`<br>2. Mở form chỉnh sửa<br>3. Upload hình ảnh mới hoặc xóa hình cũ<br>4. Click [Lưu] | Hình ảnh được cập nhật | | Pass | 11/15/2025 | |
| FUNC-ChinhSuaBV-06 | Không thể chỉnh sửa bài viết của người khác | 1. Truy cập `/user/community/[id]` với bài viết của người khác<br>2. Kiểm tra nút [Chỉnh sửa] | Nút [Chỉnh sửa] không hiển thị hoặc bị vô hiệu hóa | | Pass | 11/15/2025 | |
| **Function: Xóa bài viết** |
| **Check GUI: Xóa bài viết** |
| GUI-XoaBV-01 | Check [Xóa bài viết] Button | 1. Truy cập `/user/community/[id]` với bài viết của mình<br>2. Kiểm tra nút [Xóa bài viết] | Status: visible, enable | | Pass | 11/15/2025 | |
| GUI-XoaBV-02 | Check [Modal xác nhận] Dialog | 1. Truy cập `/user/community/[id]`<br>2. Click [Xóa bài viết]<br>3. Kiểm tra modal | Status: visible, Hiển thị form xác nhận xóa | | Pass | 11/15/2025 | |
| **Check FUNC: Xóa bài viết** |
| FUNC-XoaBV-01 | Xóa bài viết thành công | 1. Truy cập `/user/community/[id]` với bài viết của mình<br>2. Click [Xóa bài viết]<br>3. Xác nhận xóa | Bài viết bị xóa, chuyển về trang danh sách, thông báo xác nhận | | Pass | 11/15/2025 | |
| FUNC-XoaBV-02 | Hủy xóa bài viết | 1. Truy cập `/user/community/[id]`<br>2. Click [Xóa bài viết]<br>3. Click [Hủy] trong modal | Modal được đóng, bài viết không bị xóa | | Pass | 11/15/2025 | |
| FUNC-XoaBV-03 | Không thể xóa bài viết của người khác | 1. Truy cập `/user/community/[id]` với bài viết của người khác<br>2. Kiểm tra nút [Xóa bài viết] | Nút [Xóa bài viết] không hiển thị hoặc bị vô hiệu hóa | | Pass | 11/15/2025 | |

---

## GHI CHÚ

- Tất cả test cases cần được thực hiện trên môi trường test
- Routes động (có `[id]`) cần thay thế bằng ID thực tế khi test
- Các test case GUI kiểm tra giao diện và trạng thái của các thành phần
- Các test case FUNC kiểm tra chức năng và logic nghiệp vụ
- Chỉ người tạo bài viết mới có thể chỉnh sửa và xóa bài viết
- Cần cập nhật cột Result, Test date sau khi thực hiện test

