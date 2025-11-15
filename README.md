# Test Case Template - Chức năng đánh giá nâng cao - đánh giá sản phẩm sau khi mua hàng (User)

## Module Code
**Model Management Store: Chức năng đánh giá nâng cao - đánh giá sản phẩm sau khi mua hàng User**

## Test Requirement
1. Đánh giá sản phẩm
2. Viết review
3. Xem đánh giá
4. Quản lý đánh giá của tôi
5. Tương tác với đánh giá

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

### Function: Đánh giá sản phẩm

#### Check GUI: Đánh giá sản phẩm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DGSP-01** | Kiểm tra tiêu đề đánh giá | 1. Truy cập /user/reviews<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Đánh giá sách" với font-bold text-3xl | | Pass | 11/15/2015 | |
| **GUI-DGSP-02** | Kiểm tra mô tả trang | 1. Truy cập /user/reviews<br>2. Kiểm tra mô tả | Hiển thị mô tả "Chia sẻ trải nghiệm và đọc đánh giá từ cộng đồng" với màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-DGSP-03** | Kiểm tra icon đánh giá | 1. Truy cập /user/reviews<br>2. Kiểm tra icon | Hiển thị icon Star trong tab "Chờ đánh giá" | | Pass | 11/15/2015 | |
| **GUI-DGSP-04** | Kiểm tra tab Chờ đánh giá | 1. Truy cập /user/reviews<br>2. Kiểm tra tab | Hiển thị tab "Chờ đánh giá" với số lượng sản phẩm chờ đánh giá trong ngoặc đơn | | Pass | 11/15/2015 | |
| **GUI-DGSP-05** | Kiểm tra card sản phẩm chờ đánh giá | 1. Truy cập /user/reviews<br>2. Chọn tab "Chờ đánh giá"<br>3. Kiểm tra card | Hiển thị card sản phẩm với layout flex gap-4, chứa hình ảnh, tên sản phẩm, tác giả, ngày mua | | Pass | 11/15/2015 | |
| **GUI-DGSP-06** | Kiểm tra hình ảnh sản phẩm | 1. Truy cập /user/reviews<br>2. Kiểm tra hình ảnh | Hiển thị hình ảnh sản phẩm với kích thước w-16 h-20, object-cover rounded | | Pass | 11/15/2015 | |
| **GUI-DGSP-07** | Kiểm tra tên sản phẩm | 1. Truy cập /user/reviews<br>2. Kiểm tra tên | Hiển thị tên sản phẩm với font-semibold text-sm, line-clamp-2 | | Pass | 11/15/2015 | |
| **GUI-DGSP-08** | Kiểm tra tác giả | 1. Truy cập /user/reviews<br>2. Kiểm tra tác giả | Hiển thị tên tác giả với text-xs text-muted-foreground | | Pass | 11/15/2015 | |
| **GUI-DGSP-09** | Kiểm tra ngày mua | 1. Truy cập /user/reviews<br>2. Kiểm tra ngày mua | Hiển thị "Mua ngày: [Ngày]" với format ngày Việt Nam, text-xs text-muted-foreground | | Pass | 11/15/2015 | |
| **GUI-DGSP-10** | Kiểm tra nút Viết đánh giá | 1. Truy cập /user/reviews<br>2. Kiểm tra nút | Hiển thị nút "Viết đánh giá" với icon Star, size sm, variant default, chiếm toàn bộ chiều rộng card | | Pass | 11/15/2015 | |
| **GUI-DGSP-11** | Kiểm tra badge Đã đánh giá | 1. Truy cập /user/reviews<br>2. Kiểm tra sản phẩm đã đánh giá | Hiển thị badge với icon CheckCircle, text "Đã đánh giá", text-xs text-muted-foreground | | Pass | 11/15/2015 | |
| **GUI-DGSP-12** | Kiểm tra grid layout | 1. Truy cập /user/reviews<br>2. Kiểm tra layout | Hiển thị grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 cho danh sách sản phẩm | | Pass | 11/15/2015 | |
| **GUI-DGSP-13** | Kiểm tra nút Quay lại | 1. Truy cập /user/reviews<br>2. Kiểm tra nút | Hiển thị nút "Quay lại" với icon ArrowLeft, variant ghost, link đến /user/products | | Pass | 11/15/2015 | |

---

### Check FUNC: Đánh giá sản phẩm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DGSP-01** | Mở trang đánh giá | 1. Truy cập /user/reviews | Hiển thị trang đánh giá với tiêu đề "Đánh giá sách", mô tả, 3 tabs (Chờ đánh giá, Đánh giá của tôi, Tất cả đánh giá), danh sách sản phẩm chờ đánh giá | | Pass | 11/15/2015 | |
| **FUNC-DGSP-02** | Hiển thị sản phẩm chờ đánh giá | 1. Truy cập /user/reviews<br>2. Chọn tab "Chờ đánh giá" | Hiển thị danh sách các sản phẩm đã mua nhưng chưa đánh giá, mỗi card hiển thị hình ảnh, tên, tác giả, ngày mua, nút "Viết đánh giá" | | Pass | 11/15/2015 | |
| **FUNC-DGSP-03** | Hiển thị sản phẩm đã đánh giá | 1. Truy cập /user/reviews<br>2. Chọn tab "Chờ đánh giá" | Hiển thị sản phẩm đã đánh giá với badge "Đã đánh giá" và icon CheckCircle, không hiển thị nút "Viết đánh giá" | | Pass | 11/15/2015 | |
| **FUNC-DGSP-04** | Xác thực quyền đánh giá - Đã mua | 1. Truy cập /user/reviews<br>2. Kiểm tra sản phẩm đã mua | Hệ thống kiểm tra lịch sử mua hàng, chỉ hiển thị sản phẩm đã mua trong danh sách chờ đánh giá, hiển thị nút "Viết đánh giá" | | Pass | 11/15/2015 | |
| **FUNC-DGSP-05** | Xác thực quyền đánh giá - Chưa mua | 1. Truy cập /user/reviews<br>2. Kiểm tra sản phẩm chưa mua | Sản phẩm chưa mua không xuất hiện trong danh sách chờ đánh giá | | Pass | 11/15/2015 | |
| **FUNC-DGSP-06** | Nhấn nút Viết đánh giá | 1. Truy cập /user/reviews<br>2. Chọn tab "Chờ đánh giá"<br>3. Nhấn nút "Viết đánh giá" | Mở modal viết đánh giá với thông tin sản phẩm đã chọn, form nhập điểm đánh giá và nhận xét | | Pass | 11/15/2015 | |
| **FUNC-DGSP-07** | Hiển thị danh sách rỗng | 1. Truy cập /user/reviews<br>2. Chọn tab "Chờ đánh giá"<br>3. Không có sản phẩm chờ đánh giá | Hiển thị thông báo "Không có sản phẩm nào chờ đánh giá" hoặc danh sách trống | | Pass | 11/15/2015 | |
| **FUNC-DGSP-08** | Kiểm tra số lượng sản phẩm chờ đánh giá | 1. Truy cập /user/reviews<br>2. Kiểm tra tab | Tab "Chờ đánh giá" hiển thị số lượng chính xác sản phẩm có thể đánh giá trong ngoặc đơn | | Pass | 11/15/2015 | |
| **FUNC-DGSP-09** | Nhấn nút Quay lại | 1. Truy cập /user/reviews<br>2. Nhấn nút "Quay lại" | Chuyển đến trang /user/products | | Pass | 11/15/2015 | |
| **FUNC-DGSP-10** | Kiểm tra responsive layout | 1. Truy cập /user/reviews<br>2. Thay đổi kích thước màn hình | Layout tự động điều chỉnh: 1 cột trên mobile, 2 cột trên tablet, 3 cột trên desktop | | Pass | 11/15/2015 | |

---

### Function: Viết review

#### Check GUI: Viết review

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-VR-01** | Kiểm tra modal viết review | 1. Truy cập /user/reviews<br>2. Nhấn nút "Viết đánh giá"<br>3. Kiểm tra modal | Hiển thị modal với background overlay đen 50%, card container max-w-2xl, max-h-[90vh] overflow-y-auto | | Pass | 11/15/2015 | |
| **GUI-VR-02** | Kiểm tra tiêu đề modal | 1. Mở modal viết review<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Viết đánh giá" với CardTitle | | Pass | 11/15/2015 | |
| **GUI-VR-03** | Kiểm tra mô tả modal | 1. Mở modal viết review<br>2. Kiểm tra mô tả | Hiển thị mô tả "Chia sẻ trải nghiệm của bạn về "[Tên sản phẩm]"" với CardDescription | | Pass | 11/15/2015 | |
| **GUI-VR-04** | Kiểm tra thông tin sản phẩm | 1. Mở modal viết review<br>2. Kiểm tra thông tin | Hiển thị layout flex gap-4 với hình ảnh sản phẩm w-20 h-24, tên sản phẩm font-semibold, ngày mua | | Pass | 11/15/2015 | |
| **GUI-VR-05** | Kiểm tra hệ thống sao | 1. Mở modal viết review<br>2. Kiểm tra sao | Hiển thị 5 ngôi sao với icon Star, có thể click để chọn điểm từ 1-5, sao được chọn có màu fill-yellow-400 text-yellow-400 | | Pass | 11/15/2015 | |
| **GUI-VR-06** | Kiểm tra label Đánh giá của bạn | 1. Mở modal viết review<br>2. Kiểm tra label | Hiển thị label "Đánh giá của bạn *" với dấu sao bắt buộc | | Pass | 11/15/2015 | |
| **GUI-VR-07** | Kiểm tra mô tả điểm đánh giá | 1. Mở modal viết review<br>2. Chọn điểm đánh giá<br>3. Kiểm tra mô tả | Hiển thị text mô tả tương ứng: "Rất không hài lòng" (1 sao), "Không hài lòng" (2 sao), "Bình thường" (3 sao), "Hài lòng" (4 sao), "Rất hài lòng" (5 sao) | | Pass | 11/15/2015 | |
| **GUI-VR-08** | Kiểm tra ô nhập nhận xét | 1. Mở modal viết review<br>2. Kiểm tra textarea | Hiển thị label "Nhận xét chi tiết *", textarea với placeholder "Chia sẻ trải nghiệm của bạn về cuốn sách này...", rows 4 | | Pass | 11/15/2015 | |
| **GUI-VR-09** | Kiểm tra đếm ký tự | 1. Mở modal viết review<br>2. Nhập nhận xét<br>3. Kiểm tra đếm | Hiển thị "[Số]/500 ký tự" với text-xs text-muted-foreground, cập nhật real-time khi nhập | | Pass | 11/15/2015 | |
| **GUI-VR-10** | Kiểm tra nút Hủy | 1. Mở modal viết review<br>2. Kiểm tra nút | Hiển thị nút "Hủy" variant outline, đóng modal khi nhấn | | Pass | 11/15/2015 | |
| **GUI-VR-11** | Kiểm tra nút Gửi đánh giá | 1. Mở modal viết review<br>2. Kiểm tra nút | Hiển thị nút "Gửi đánh giá" variant default, gửi đánh giá khi nhấn | | Pass | 11/15/2015 | |
| **GUI-VR-12** | Kiểm tra upload ảnh | 1. Mở modal viết review<br>2. Kiểm tra upload | Hiển thị nút "Upload ảnh" với file input, hỗ trợ định dạng ảnh (jpg, png, webp) | | Pass | 11/15/2015 | |
| **GUI-VR-13** | Kiểm tra upload video | 1. Mở modal viết review<br>2. Kiểm tra upload | Hiển thị nút "Upload video" với file input, hỗ trợ định dạng video (mp4, webm) | | Pass | 11/15/2015 | |
| **GUI-VR-14** | Kiểm tra danh sách file đã upload | 1. Mở modal viết review<br>2. Upload file<br>3. Kiểm tra danh sách | Hiển thị danh sách file đã upload với preview, có nút xóa từng file | | Pass | 11/15/2015 | |

---

### Check FUNC: Viết review

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-VR-01** | Mở modal viết review | 1. Truy cập /user/reviews<br>2. Nhấn nút "Viết đánh giá" | Mở modal với thông tin sản phẩm đã chọn, form trống sẵn sàng nhập | | Pass | 11/15/2015 | |
| **FUNC-VR-02** | Chọn điểm đánh giá 1 sao | 1. Mở modal viết review<br>2. Click vào sao thứ 1 | Sao thứ 1 được chọn, hiển thị màu vàng, mô tả "Rất không hài lòng" | | Pass | 11/15/2015 | |
| **FUNC-VR-03** | Chọn điểm đánh giá 5 sao | 1. Mở modal viết review<br>2. Click vào sao thứ 5 | Tất cả 5 sao được chọn, hiển thị màu vàng, mô tả "Rất hài lòng" | | Pass | 11/15/2015 | |
| **FUNC-VR-04** | Thay đổi điểm đánh giá | 1. Mở modal viết review<br>2. Chọn 3 sao<br>3. Click vào sao thứ 5 | Điểm đánh giá thay đổi từ 3 sao sang 5 sao, mô tả cập nhật tương ứng | | Pass | 11/15/2015 | |
| **FUNC-VR-05** | Nhập nhận xét chi tiết | 1. Mở modal viết review<br>2. Nhập nhận xét vào textarea | Nhận xét được nhập và hiển thị trong textarea, đếm ký tự cập nhật real-time | | Pass | 11/15/2015 | |
| **FUNC-VR-06** | Kiểm tra giới hạn ký tự | 1. Mở modal viết review<br>2. Nhập quá 500 ký tự | Hệ thống giới hạn nhập ở 500 ký tự, hiển thị "500/500 ký tự", không cho nhập thêm | | Pass | 11/15/2015 | |
| **FUNC-VR-07** | Gửi đánh giá thành công | 1. Mở modal viết review<br>2. Chọn điểm đánh giá (VD: 5 sao)<br>3. Nhập nhận xét<br>4. Nhấn "Gửi đánh giá" | Đánh giá được gửi thành công, modal đóng, hiển thị toast "Đánh giá đã được gửi thành công", đánh giá xuất hiện trong tab "Đánh giá của tôi" với trạng thái "Đang chờ duyệt" | | Pass | 11/15/2015 | |
| **FUNC-VR-08** | Gửi đánh giá thiếu điểm | 1. Mở modal viết review<br>2. Không chọn điểm đánh giá<br>3. Nhập nhận xét<br>4. Nhấn "Gửi đánh giá" | Hiển thị toast lỗi "Vui lòng chọn điểm đánh giá", không gửi đánh giá, modal vẫn mở | | Pass | 11/15/2015 | |
| **FUNC-VR-09** | Gửi đánh giá thiếu nhận xét | 1. Mở modal viết review<br>2. Chọn điểm đánh giá<br>3. Để trống nhận xét<br>4. Nhấn "Gửi đánh giá" | Hiển thị toast lỗi "Vui lòng viết nhận xét", không gửi đánh giá, modal vẫn mở | | Pass | 11/15/2015 | |
| **FUNC-VR-10** | Gửi đánh giá nhận xét chỉ có khoảng trắng | 1. Mở modal viết review<br>2. Chọn điểm đánh giá<br>3. Nhập chỉ khoảng trắng<br>4. Nhấn "Gửi đánh giá" | Hiển thị toast lỗi "Vui lòng viết nhận xét", không gửi đánh giá | | Pass | 11/15/2015 | |
| **FUNC-VR-11** | Upload ảnh thành công | 1. Mở modal viết review<br>2. Nhấn "Upload ảnh"<br>3. Chọn file ảnh hợp lệ | File ảnh được upload, hiển thị trong danh sách file đã upload với preview, có nút xóa | | Pass | 11/15/2015 | |
| **FUNC-VR-12** | Upload video thành công | 1. Mở modal viết review<br>2. Nhấn "Upload video"<br>3. Chọn file video hợp lệ | File video được upload, hiển thị trong danh sách file đã upload với preview, có nút xóa | | Pass | 11/15/2015 | |
| **FUNC-VR-13** | Upload file không hợp lệ | 1. Mở modal viết review<br>2. Upload file không đúng định dạng | Hiển thị thông báo lỗi "Định dạng file không được hỗ trợ", file không được upload | | Pass | 11/15/2015 | |
| **FUNC-VR-14** | Upload file quá kích thước | 1. Mở modal viết review<br>2. Upload file vượt quá giới hạn (VD: >10MB) | Hiển thị thông báo lỗi "File quá lớn. Kích thước tối đa: 10MB", file không được upload | | Pass | 11/15/2015 | |
| **FUNC-VR-15** | Xóa file đã upload | 1. Mở modal viết review<br>2. Upload file<br>3. Nhấn nút xóa file | File được xóa khỏi danh sách, không còn trong preview | | Pass | 11/15/2015 | |
| **FUNC-VR-16** | Nhấn nút Hủy | 1. Mở modal viết review<br>2. Nhập một số thông tin<br>3. Nhấn "Hủy" | Modal đóng, không lưu thông tin đã nhập, quay lại trang đánh giá | | Pass | 11/15/2015 | |
| **FUNC-VR-17** | Đóng modal bằng click overlay | 1. Mở modal viết review<br>2. Click vào vùng overlay đen | Modal đóng, quay lại trang đánh giá | | Pass | 11/15/2015 | |
| **FUNC-VR-18** | Gửi đánh giá với ảnh/video | 1. Mở modal viết review<br>2. Chọn điểm, nhập nhận xét<br>3. Upload ảnh/video<br>4. Nhấn "Gửi đánh giá" | Đánh giá được gửi kèm file đính kèm, hiển thị trong đánh giá của tôi với file đính kèm | | Pass | 11/15/2015 | |
| **FUNC-VR-19** | Kiểm tra trạng thái đang chờ duyệt | 1. Gửi đánh giá thành công<br>2. Kiểm tra tab "Đánh giá của tôi" | Đánh giá hiển thị với badge "Đang chờ duyệt", chưa hiển thị công khai | | Pass | 11/15/2015 | |

---

### Function: Xem đánh giá

#### Check GUI: Xem đánh giá

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XDG-01** | Kiểm tra tab Tất cả đánh giá | 1. Truy cập /user/reviews<br>2. Kiểm tra tab | Hiển thị tab "Tất cả đánh giá" trong TabsList | | Pass | 11/15/2015 | |
| **GUI-XDG-02** | Kiểm tra ô tìm kiếm | 1. Truy cập /user/reviews<br>2. Chọn tab "Tất cả đánh giá"<br>3. Kiểm tra tìm kiếm | Hiển thị input tìm kiếm với icon Search bên trái, placeholder "Tìm kiếm đánh giá...", pl-10 | | Pass | 11/15/2015 | |
| **GUI-XDG-03** | Kiểm tra bộ lọc điểm đánh giá | 1. Chọn tab "Tất cả đánh giá"<br>2. Kiểm tra bộ lọc | Hiển thị Select với trigger w-32, các option: "Tất cả", "5 sao", "4 sao", "3 sao", "2 sao", "1 sao" | | Pass | 11/15/2015 | |
| **GUI-XDG-04** | Kiểm tra sắp xếp | 1. Chọn tab "Tất cả đánh giá"<br>2. Kiểm tra sắp xếp | Hiển thị Select với trigger w-32, các option: "Mới nhất", "Hữu ích nhất", "Điểm cao nhất" | | Pass | 11/15/2015 | |
| **GUI-XDG-05** | Kiểm tra card đánh giá | 1. Chọn tab "Tất cả đánh giá"<br>2. Kiểm tra card | Hiển thị card đánh giá với layout flex gap-4, chứa hình ảnh sản phẩm, thông tin đánh giá | | Pass | 11/15/2015 | |
| **GUI-XDG-06** | Kiểm tra hình ảnh sản phẩm trong đánh giá | 1. Xem danh sách đánh giá<br>2. Kiểm tra hình ảnh | Hiển thị hình ảnh sản phẩm w-16 h-20, object-cover rounded | | Pass | 11/15/2015 | |
| **GUI-XDG-07** | Kiểm tra tên sản phẩm | 1. Xem danh sách đánh giá<br>2. Kiểm tra tên | Hiển thị tên sản phẩm với font-semibold text-sm | | Pass | 11/15/2015 | |
| **GUI-XDG-08** | Kiểm tra điểm đánh giá | 1. Xem danh sách đánh giá<br>2. Kiểm tra điểm | Hiển thị 5 ngôi sao, sao được chọn có màu fill-yellow-400 text-yellow-400, sao không chọn có màu text-gray-300 | | Pass | 11/15/2015 | |
| **GUI-XDG-09** | Kiểm tra ngày đánh giá | 1. Xem danh sách đánh giá<br>2. Kiểm tra ngày | Hiển thị ngày đánh giá với format ngày Việt Nam, text-xs text-muted-foreground | | Pass | 11/15/2015 | |
| **GUI-XDG-10** | Kiểm tra badge Đã mua | 1. Xem danh sách đánh giá<br>2. Kiểm tra badge | Hiển thị badge "Đã mua" variant secondary, text-xs cho đánh giá từ khách đã mua | | Pass | 11/15/2015 | |
| **GUI-XDG-11** | Kiểm tra nội dung đánh giá | 1. Xem danh sách đánh giá<br>2. Kiểm tra nội dung | Hiển thị nội dung đánh giá với text-sm text-muted-foreground | | Pass | 11/15/2015 | |
| **GUI-XDG-12** | Kiểm tra nút Hữu ích | 1. Xem danh sách đánh giá<br>2. Kiểm tra nút | Hiển thị nút "Hữu ích" với icon ThumbsUp, variant ghost size sm, hiển thị số lượt trong ngoặc đơn | | Pass | 11/15/2015 | |
| **GUI-XDG-13** | Kiểm tra ảnh đính kèm | 1. Xem đánh giá có ảnh<br>2. Kiểm tra ảnh | Hiển thị ảnh đính kèm với kích thước phù hợp, có thể click để xem to | | Pass | 11/15/2015 | |
| **GUI-XDG-14** | Kiểm tra video đính kèm | 1. Xem đánh giá có video<br>2. Kiểm tra video | Hiển thị video đính kèm với player, có thể phát video | | Pass | 11/15/2015 | |

---

### Check FUNC: Xem đánh giá

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XDG-01** | Mở tab Tất cả đánh giá | 1. Truy cập /user/reviews<br>2. Chọn tab "Tất cả đánh giá" | Hiển thị danh sách tất cả đánh giá đã được duyệt, có bộ lọc và sắp xếp | | Pass | 11/15/2015 | |
| **FUNC-XDG-02** | Hiển thị danh sách đánh giá | 1. Chọn tab "Tất cả đánh giá" | Hiển thị danh sách đánh giá với đầy đủ thông tin: hình ảnh sản phẩm, tên sản phẩm, điểm đánh giá, ngày đánh giá, nội dung, số lượt hữu ích | | Pass | 11/15/2015 | |
| **FUNC-XDG-03** | Chỉ hiển thị đánh giá đã duyệt | 1. Chọn tab "Tất cả đánh giá" | Chỉ hiển thị các đánh giá có trạng thái "Đã duyệt", không hiển thị đánh giá "Đang chờ duyệt" hoặc "Từ chối" | | Pass | 11/15/2015 | |
| **FUNC-XDG-04** | Tìm kiếm đánh giá theo tên sản phẩm | 1. Chọn tab "Tất cả đánh giá"<br>2. Nhập tên sản phẩm vào ô tìm kiếm | Danh sách đánh giá được lọc theo tên sản phẩm, chỉ hiển thị đánh giá có tên sản phẩm chứa từ khóa | | Pass | 11/15/2015 | |
| **FUNC-XDG-05** | Tìm kiếm đánh giá theo nội dung | 1. Chọn tab "Tất cả đánh giá"<br>2. Nhập từ khóa vào ô tìm kiếm | Danh sách đánh giá được lọc theo nội dung, chỉ hiển thị đánh giá có nội dung chứa từ khóa | | Pass | 11/15/2015 | |
| **FUNC-XDG-06** | Lọc đánh giá theo 5 sao | 1. Chọn tab "Tất cả đánh giá"<br>2. Chọn bộ lọc "5 sao" | Chỉ hiển thị các đánh giá có điểm 5 sao | | Pass | 11/15/2015 | |
| **FUNC-XDG-07** | Lọc đánh giá theo 1 sao | 1. Chọn tab "Tất cả đánh giá"<br>2. Chọn bộ lọc "1 sao" | Chỉ hiển thị các đánh giá có điểm 1 sao | | Pass | 11/15/2015 | |
| **FUNC-XDG-08** | Lọc đánh giá - Tất cả | 1. Chọn tab "Tất cả đánh giá"<br>2. Chọn bộ lọc "Tất cả" | Hiển thị tất cả đánh giá không phân biệt điểm | | Pass | 11/15/2015 | |
| **FUNC-XDG-09** | Sắp xếp theo Mới nhất | 1. Chọn tab "Tất cả đánh giá"<br>2. Chọn sắp xếp "Mới nhất" | Danh sách đánh giá được sắp xếp theo ngày đánh giá mới nhất trước | | Pass | 11/15/2015 | |
| **FUNC-XDG-10** | Sắp xếp theo Hữu ích nhất | 1. Chọn tab "Tất cả đánh giá"<br>2. Chọn sắp xếp "Hữu ích nhất" | Danh sách đánh giá được sắp xếp theo số lượt hữu ích giảm dần | | Pass | 11/15/2015 | |
| **FUNC-XDG-11** | Sắp xếp theo Điểm cao nhất | 1. Chọn tab "Tất cả đánh giá"<br>2. Chọn sắp xếp "Điểm cao nhất" | Danh sách đánh giá được sắp xếp theo điểm đánh giá giảm dần (5 sao trước) | | Pass | 11/15/2015 | |
| **FUNC-XDG-12** | Kết hợp tìm kiếm và lọc | 1. Chọn tab "Tất cả đánh giá"<br>2. Nhập từ khóa tìm kiếm<br>3. Chọn bộ lọc điểm | Danh sách đánh giá được lọc theo cả từ khóa và điểm đánh giá | | Pass | 11/15/2015 | |
| **FUNC-XDG-13** | Hiển thị đánh giá không có kết quả | 1. Chọn tab "Tất cả đánh giá"<br>2. Tìm kiếm/lọc không có kết quả | Hiển thị thông báo "Không tìm thấy đánh giá nào" hoặc danh sách trống | | Pass | 11/15/2015 | |
| **FUNC-XDG-14** | Nhấn nút Hữu ích | 1. Chọn tab "Tất cả đánh giá"<br>2. Nhấn nút "Hữu ích" | Số lượt hữu ích tăng lên, hiển thị toast "Cảm ơn bạn đã đánh giá hữu ích", nút chuyển sang trạng thái đã nhấn | | Pass | 11/15/2015 | |
| **FUNC-XDG-15** | Xem ảnh đính kèm | 1. Xem đánh giá có ảnh<br>2. Click vào ảnh | Mở lightbox hoặc modal hiển thị ảnh to, có thể zoom và xem chi tiết | | Pass | 11/15/2015 | |
| **FUNC-XDG-16** | Phát video đính kèm | 1. Xem đánh giá có video<br>2. Click phát video | Video được phát trong player, có controls để play/pause/volume | | Pass | 11/15/2015 | |
| **FUNC-XDG-17** | Hiển thị đánh giá từ trang chi tiết sản phẩm | 1. Truy cập /user/products/[id]<br>2. Xem phần đánh giá | Hiển thị danh sách đánh giá của sản phẩm đó, có thể lọc và sắp xếp | | Pass | 11/15/2015 | |

---

### Function: Quản lý đánh giá của tôi

#### Check GUI: Quản lý đánh giá của tôi

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-QLDG-01** | Kiểm tra tab Đánh giá của tôi | 1. Truy cập /user/reviews<br>2. Kiểm tra tab | Hiển thị tab "Đánh giá của tôi" với số lượng đánh giá trong ngoặc đơn | | Pass | 11/15/2015 | |
| **GUI-QLDG-02** | Kiểm tra card đánh giá của tôi | 1. Chọn tab "Đánh giá của tôi"<br>2. Kiểm tra card | Hiển thị card đánh giá với layout flex gap-4, chứa hình ảnh sản phẩm, thông tin đánh giá, nút chỉnh sửa/xóa | | Pass | 11/15/2015 | |
| **GUI-QLDG-03** | Kiểm tra nút Chỉnh sửa | 1. Chọn tab "Đánh giá của tôi"<br>2. Kiểm tra nút | Hiển thị nút chỉnh sửa với icon Edit, variant ghost size sm | | Pass | 11/15/2015 | |
| **GUI-QLDG-04** | Kiểm tra nút Xóa | 1. Chọn tab "Đánh giá của tôi"<br>2. Kiểm tra nút | Hiển thị nút xóa với icon Trash2, variant ghost size sm, màu text-red-600 hover:text-red-700 | | Pass | 11/15/2015 | |
| **GUI-QLDG-05** | Kiểm tra badge trạng thái | 1. Chọn tab "Đánh giá của tôi"<br>2. Kiểm tra badge | Hiển thị badge trạng thái: "Đã gửi", "Đang chờ duyệt", "Đã duyệt", "Từ chối" với màu tương ứng | | Pass | 11/15/2015 | |
| **GUI-QLDG-06** | Kiểm tra thông báo chưa có đánh giá | 1. Chọn tab "Đánh giá của tôi"<br>2. Không có đánh giá | Hiển thị icon MessageSquare, tiêu đề "Chưa có đánh giá nào", mô tả "Bạn chưa viết đánh giá nào cho sách đã mua" | | Pass | 11/15/2015 | |
| **GUI-QLDG-07** | Kiểm tra số lượt hữu ích | 1. Chọn tab "Đánh giá của tôi"<br>2. Kiểm tra số lượt | Hiển thị "[Số] người thấy hữu ích" với icon ThumbsUp, text-xs text-muted-foreground | | Pass | 11/15/2015 | |

---

### Check FUNC: Quản lý đánh giá của tôi

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-QLDG-01** | Mở tab Đánh giá của tôi | 1. Truy cập /user/reviews<br>2. Chọn tab "Đánh giá của tôi" | Hiển thị danh sách tất cả đánh giá mà người dùng đã viết, sắp xếp theo thời gian mới nhất | | Pass | 11/15/2015 | |
| **FUNC-QLDG-02** | Hiển thị danh sách đánh giá của tôi | 1. Chọn tab "Đánh giá của tôi" | Hiển thị đầy đủ thông tin: hình ảnh sản phẩm, tên sản phẩm, điểm đánh giá, ngày đánh giá, nội dung, trạng thái, số lượt hữu ích | | Pass | 11/15/2015 | |
| **FUNC-QLDG-03** | Hiển thị trạng thái Đang chờ duyệt | 1. Chọn tab "Đánh giá của tôi"<br>2. Xem đánh giá vừa gửi | Hiển thị badge "Đang chờ duyệt" cho đánh giá mới gửi, chưa được admin duyệt | | Pass | 11/15/2015 | |
| **FUNC-QLDG-04** | Hiển thị trạng thái Đã duyệt | 1. Chọn tab "Đánh giá của tôi"<br>2. Xem đánh giá đã được duyệt | Hiển thị badge "Đã duyệt" cho đánh giá đã được admin phê duyệt, đánh giá này hiển thị công khai | | Pass | 11/15/2015 | |
| **FUNC-QLDG-05** | Hiển thị trạng thái Từ chối | 1. Chọn tab "Đánh giá của tôi"<br>2. Xem đánh giá bị từ chối | Hiển thị badge "Từ chối" cho đánh giá bị admin từ chối, đánh giá không hiển thị công khai | | Pass | 11/15/2015 | |
| **FUNC-QLDG-06** | Chỉnh sửa đánh giá | 1. Chọn tab "Đánh giá của tôi"<br>2. Nhấn nút "Chỉnh sửa" | Mở modal chỉnh sửa với thông tin đánh giá hiện tại đã điền sẵn, cho phép thay đổi điểm đánh giá, nội dung, file đính kèm | | Pass | 11/15/2015 | |
| **FUNC-QLDG-07** | Lưu chỉnh sửa đánh giá | 1. Chỉnh sửa đánh giá<br>2. Thay đổi điểm và nội dung<br>3. Nhấn "Gửi đánh giá" | Đánh giá được cập nhật, hiển thị thông báo thành công, trạng thái chuyển về "Đang chờ duyệt", hiển thị thời gian chỉnh sửa cuối cùng | | Pass | 11/15/2015 | |
| **FUNC-QLDG-08** | Xóa đánh giá | 1. Chọn tab "Đánh giá của tôi"<br>2. Nhấn nút "Xóa"<br>3. Xác nhận xóa | Hiển thị dialog xác nhận "Bạn có chắc muốn xóa đánh giá này?", sau khi xác nhận, đánh giá bị xóa, hiển thị toast "Đã xóa đánh giá", danh sách được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-QLDG-09** | Hủy xóa đánh giá | 1. Chọn tab "Đánh giá của tôi"<br>2. Nhấn nút "Xóa"<br>3. Hủy xóa | Dialog đóng, đánh giá không bị xóa, vẫn hiển thị trong danh sách | | Pass | 11/15/2015 | |
| **FUNC-QLDG-10** | Chỉnh sửa đánh giá đã duyệt | 1. Chọn tab "Đánh giá của tôi"<br>2. Chỉnh sửa đánh giá đã duyệt | Cho phép chỉnh sửa đánh giá đã duyệt, sau khi lưu, trạng thái chuyển về "Đang chờ duyệt" để admin xem xét lại | | Pass | 11/15/2015 | |
| **FUNC-QLDG-11** | Không cho chỉnh sửa đánh giá đã từ chối | 1. Chọn tab "Đánh giá của tôi"<br>2. Xem đánh giá bị từ chối | Đánh giá bị từ chối vẫn có thể chỉnh sửa, sau khi chỉnh sửa và gửi lại, trạng thái chuyển về "Đang chờ duyệt" | | Pass | 11/15/2015 | |
| **FUNC-QLDG-12** | Hiển thị số lượt hữu ích | 1. Chọn tab "Đánh giá của tôi"<br>2. Xem đánh giá | Hiển thị số lượt người dùng khác đánh dấu đánh giá là hữu ích | | Pass | 11/15/2015 | |
| **FUNC-QLDG-13** | Sắp xếp theo thời gian mới nhất | 1. Chọn tab "Đánh giá của tôi" | Danh sách đánh giá được sắp xếp theo thời gian đánh giá mới nhất trước | | Pass | 11/15/2015 | |
| **FUNC-QLDG-14** | Hiển thị khi chưa có đánh giá | 1. Chọn tab "Đánh giá của tôi"<br>2. Chưa có đánh giá nào | Hiển thị thông báo "Chưa có đánh giá nào" với icon MessageSquare, mô tả "Bạn chưa viết đánh giá nào cho sách đã mua" | | Pass | 11/15/2015 | |
| **FUNC-QLDG-15** | Kiểm tra lịch sử chỉnh sửa | 1. Chỉnh sửa đánh giá nhiều lần<br>2. Kiểm tra lịch sử | Hệ thống lưu lại lịch sử chỉnh sửa, hiển thị thời gian chỉnh sửa cuối cùng | | Pass | 11/15/2015 | |

---

### Function: Tương tác với đánh giá

#### Check GUI: Tương tác với đánh giá

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-TT-01** | Kiểm tra nút Hữu ích | 1. Xem đánh giá<br>2. Kiểm tra nút | Hiển thị nút "Hữu ích" với icon ThumbsUp, variant ghost size sm, hiển thị số lượt trong ngoặc đơn | | Pass | 11/15/2015 | |
| **GUI-TT-02** | Kiểm tra nút Không hữu ích | 1. Xem đánh giá<br>2. Kiểm tra nút | Hiển thị nút "Không hữu ích" với icon ThumbsDown, variant ghost size sm, hiển thị số lượt trong ngoặc đơn | | Pass | 11/15/2015 | |
| **GUI-TT-03** | Kiểm tra nút Báo cáo | 1. Xem đánh giá<br>2. Kiểm tra nút | Hiển thị nút "Báo cáo" với icon Flag, variant ghost size sm | | Pass | 11/15/2015 | |
| **GUI-TT-04** | Kiểm tra modal báo cáo | 1. Nhấn nút "Báo cáo"<br>2. Kiểm tra modal | Hiển thị modal với tiêu đề "Báo cáo đánh giá", có Select lý do báo cáo, Textarea mô tả, nút "Gửi báo cáo" và "Hủy" | | Pass | 11/15/2015 | |
| **GUI-TT-05** | Kiểm tra Select lý do báo cáo | 1. Mở modal báo cáo<br>2. Kiểm tra Select | Hiển thị Select với các option: "Nội dung không phù hợp", "Spam", "Thông tin sai lệch", "Vi phạm quy định", "Khác" | | Pass | 11/15/2015 | |
| **GUI-TT-06** | Kiểm tra Textarea mô tả | 1. Mở modal báo cáo<br>2. Kiểm tra Textarea | Hiển thị Textarea với label "Mô tả chi tiết", placeholder "Nhập mô tả về lý do báo cáo..." | | Pass | 11/15/2015 | |

---

### Check FUNC: Tương tác với đánh giá

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TT-01** | Đánh dấu hữu ích | 1. Xem đánh giá<br>2. Nhấn nút "Hữu ích" | Số lượt hữu ích tăng lên, nút chuyển sang trạng thái đã nhấn (màu khác), hiển thị toast "Cảm ơn bạn đã đánh giá hữu ích", lựa chọn được lưu lại | | Pass | 11/15/2015 | |
| **FUNC-TT-02** | Bỏ đánh dấu hữu ích | 1. Đã đánh dấu hữu ích<br>2. Nhấn lại nút "Hữu ích" | Số lượt hữu ích giảm đi, nút quay về trạng thái ban đầu, lựa chọn được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-TT-03** | Đánh dấu không hữu ích | 1. Xem đánh giá<br>2. Nhấn nút "Không hữu ích" | Số lượt không hữu ích tăng lên, nút chuyển sang trạng thái đã nhấn, lựa chọn được lưu lại | | Pass | 11/15/2015 | |
| **FUNC-TT-04** | Bỏ đánh dấu không hữu ích | 1. Đã đánh dấu không hữu ích<br>2. Nhấn lại nút "Không hữu ích" | Số lượt không hữu ích giảm đi, nút quay về trạng thái ban đầu | | Pass | 11/15/2015 | |
| **FUNC-TT-05** | Chuyển từ hữu ích sang không hữu ích | 1. Đã đánh dấu hữu ích<br>2. Nhấn nút "Không hữu ích" | Số lượt hữu ích giảm, số lượt không hữu ích tăng, nút hữu ích quay về trạng thái ban đầu, nút không hữu ích chuyển sang trạng thái đã nhấn | | Pass | 11/15/2015 | |
| **FUNC-TT-06** | Mở modal báo cáo | 1. Xem đánh giá<br>2. Nhấn nút "Báo cáo" | Mở modal báo cáo với Select lý do và Textarea mô tả | | Pass | 11/15/2015 | |
| **FUNC-TT-07** | Gửi báo cáo thành công | 1. Mở modal báo cáo<br>2. Chọn lý do báo cáo<br>3. Nhập mô tả<br>4. Nhấn "Gửi báo cáo" | Báo cáo được gửi thành công, modal đóng, hiển thị toast "Báo cáo đã được gửi. Cảm ơn bạn đã phản hồi", báo cáo được gửi đến admin để xem xét | | Pass | 11/15/2015 | |
| **FUNC-TT-08** | Gửi báo cáo thiếu lý do | 1. Mở modal báo cáo<br>2. Không chọn lý do<br>3. Nhấn "Gửi báo cáo" | Hiển thị thông báo lỗi "Vui lòng chọn lý do báo cáo", không gửi báo cáo | | Pass | 11/15/2015 | |
| **FUNC-TT-09** | Gửi báo cáo thiếu mô tả | 1. Mở modal báo cáo<br>2. Chọn lý do<br>3. Để trống mô tả<br>4. Nhấn "Gửi báo cáo" | Hiển thị thông báo lỗi "Vui lòng nhập mô tả chi tiết", không gửi báo cáo | | Pass | 11/15/2015 | |
| **FUNC-TT-10** | Hủy báo cáo | 1. Mở modal báo cáo<br>2. Nhấn nút "Hủy" | Modal đóng, không gửi báo cáo | | Pass | 11/15/2015 | |
| **FUNC-TT-11** | Đóng modal bằng click overlay | 1. Mở modal báo cáo<br>2. Click vào overlay | Modal đóng, không gửi báo cáo | | Pass | 11/15/2015 | |
| **FUNC-TT-12** | Hiển thị trạng thái tương tác | 1. Xem đánh giá đã tương tác<br>2. Kiểm tra trạng thái | Nút hữu ích/không hữu ích hiển thị trạng thái đã nhấn, cập nhật real-time khi có thay đổi | | Pass | 11/15/2015 | |
| **FUNC-TT-13** | Báo cáo đánh giá của chính mình | 1. Xem đánh giá của chính mình<br>2. Nhấn nút "Báo cáo" | Cho phép báo cáo đánh giá của chính mình, báo cáo được gửi đến admin | | Pass | 11/15/2015 | |
| **FUNC-TT-14** | Báo cáo nhiều lần cùng một đánh giá | 1. Đã báo cáo đánh giá<br>2. Báo cáo lại | Cho phép báo cáo nhiều lần, mỗi báo cáo được gửi riêng đến admin | | Pass | 11/15/2015 | |
| **FUNC-TT-15** | Kiểm tra cập nhật real-time số lượt | 1. Xem đánh giá<br>2. Người khác đánh dấu hữu ích | Số lượt hữu ích được cập nhật real-time mà không cần refresh trang | | Pass | 11/15/2015 | |

---

### Check VALIDATION: Đánh giá sản phẩm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **VALID-DGSP-01** | Đánh giá với điểm 0 | 1. Mở modal viết review<br>2. Không chọn điểm<br>3. Nhập nhận xét<br>4. Nhấn "Gửi đánh giá" | Hiển thị toast lỗi "Vui lòng chọn điểm đánh giá", không gửi đánh giá | | Pass | 11/15/2015 | |
| **VALID-DGSP-02** | Đánh giá với nhận xét rỗng | 1. Mở modal viết review<br>2. Chọn điểm<br>3. Để trống nhận xét<br>4. Nhấn "Gửi đánh giá" | Hiển thị toast lỗi "Vui lòng viết nhận xét", không gửi đánh giá | | Pass | 11/15/2015 | |
| **VALID-DGSP-03** | Đánh giá với nhận xét chỉ khoảng trắng | 1. Mở modal viết review<br>2. Chọn điểm<br>3. Nhập chỉ khoảng trắng<br>4. Nhấn "Gửi đánh giá" | Hiển thị toast lỗi "Vui lòng viết nhận xét", không gửi đánh giá | | Pass | 11/15/2015 | |
| **VALID-DGSP-04** | Đánh giá với nhận xét quá dài | 1. Mở modal viết review<br>2. Chọn điểm<br>3. Nhập nhận xét > 500 ký tự | Hệ thống giới hạn ở 500 ký tự, không cho nhập thêm, hiển thị "500/500 ký tự" | | Pass | 11/15/2015 | |
| **VALID-DGSP-05** | Upload file ảnh không hợp lệ | 1. Mở modal viết review<br>2. Upload file không phải ảnh | Hiển thị thông báo lỗi "Định dạng file không được hỗ trợ. Chỉ chấp nhận: jpg, png, webp", file không được upload | | Pass | 11/15/2015 | |
| **VALID-DGSP-06** | Upload file video không hợp lệ | 1. Mở modal viết review<br>2. Upload file không phải video | Hiển thị thông báo lỗi "Định dạng file không được hỗ trợ. Chỉ chấp nhận: mp4, webm", file không được upload | | Pass | 11/15/2015 | |
| **VALID-DGSP-07** | Upload file quá kích thước | 1. Mở modal viết review<br>2. Upload file > 10MB | Hiển thị thông báo lỗi "File quá lớn. Kích thước tối đa: 10MB cho ảnh, 50MB cho video", file không được upload | | Pass | 11/15/2015 | |
| **VALID-DGSP-08** | Upload quá nhiều file | 1. Mở modal viết review<br>2. Upload nhiều file vượt quá giới hạn (VD: >5 ảnh) | Hiển thị thông báo lỗi "Số lượng file tối đa: 5 ảnh và 1 video", file thừa không được upload | | Pass | 11/15/2015 | |
| **VALID-DGSP-09** | Báo cáo thiếu lý do | 1. Mở modal báo cáo<br>2. Không chọn lý do<br>3. Nhấn "Gửi báo cáo" | Hiển thị thông báo lỗi "Vui lòng chọn lý do báo cáo", không gửi báo cáo | | Pass | 11/15/2015 | |
| **VALID-DGSP-10** | Báo cáo thiếu mô tả | 1. Mở modal báo cáo<br>2. Chọn lý do<br>3. Để trống mô tả<br>4. Nhấn "Gửi báo cáo" | Hiển thị thông báo lỗi "Vui lòng nhập mô tả chi tiết", không gửi báo cáo | | Pass | 11/15/2015 | |

