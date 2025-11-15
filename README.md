# Test Case Template - Tạo - hiển thị bài viết (User)

## Module Code
**Model Management Store: Tạo - hiển thị bài viết User**

## Test Requirement
1. Hiển thị danh sách bài viết
2. Xem chi tiết bài viết
3. Tạo bài viết
4. Chỉnh sửa bài viết
5. Xóa bài viết

---

## Test Summary

### Người thực hiện Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 130 |
| **Fail** | 0 |
| **Untested** | 40 |
| **N/A** | 0 |
| **Number of Test cases** | 170 |

---

## Test Cases

### Function: Hiển thị danh sách bài viết

#### Check GUI: Hiển thị danh sách bài viết

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-HTDS-BV-01** | Kiểm tra tiêu đề trang | 1. Truy cập trang cộng đồng<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Cộng đồng mô hình" với icon Users h-5 w-5, CardTitle | | Pass | 11/15/2015 | |
| **GUI-HTDS-BV-02** | Kiểm tra mô tả trang | 1. Truy cập trang cộng đồng<br>2. Kiểm tra mô tả | Hiển thị CardDescription "Danh sách bài viết cộng đồng" | | Pass | 11/15/2015 | |
| **GUI-HTDS-BV-03** | Kiểm tra tab danh mục | 1. Truy cập trang cộng đồng<br>2. Kiểm tra tab | Hiển thị TabsList grid-cols-5 với các tab: "Tất cả", "Gundam", "Figure", "Mô hình xe", "Máy bay" | | Pass | 11/15/2015 | |
| **GUI-HTDS-BV-04** | Kiểm tra ô tìm kiếm | 1. Truy cập trang cộng đồng<br>2. Kiểm tra tìm kiếm | Hiển thị Input với icon Search bên trái, placeholder "Tìm bài viết...", pl-9 | | Pass | 11/15/2015 | |
| **GUI-HTDS-BV-05** | Kiểm tra bộ lọc danh mục | 1. Truy cập trang cộng đồng<br>2. Kiểm tra bộ lọc | Hiển thị Select với trigger w-48, các option: "Tất cả", "Gundam", "Figure", "Mô hình xe", "Máy bay", "Khác" | | Pass | 11/15/2015 | |
| **GUI-HTDS-BV-06** | Kiểm tra bộ lọc thời gian | 1. Truy cập trang cộng đồng<br>2. Kiểm tra bộ lọc | Hiển thị Select với trigger w-48, các option: "Hôm nay", "Tuần này", "Tháng này", "Tất cả" | | Pass | 11/15/2015 | |
| **GUI-HTDS-BV-07** | Kiểm tra bộ lọc sắp xếp | 1. Truy cập trang cộng đồng<br>2. Kiểm tra bộ lọc | Hiển thị Select với trigger w-56, các option: "Mới nhất", "Nhiều like nhất", "Nhiều bình luận nhất" | | Pass | 11/15/2015 | |
| **GUI-HTDS-BV-08** | Kiểm tra nút Tạo bài viết | 1. Truy cập trang cộng đồng<br>2. Kiểm tra nút | Hiển thị nút "Tạo bài viết" với link đến /user/posts/create | | Pass | 11/15/2015 | |
| **GUI-HTDS-BV-09** | Kiểm tra card bài viết | 1. Xem danh sách bài viết<br>2. Kiểm tra card | Hiển thị card với overflow-hidden, chứa Avatar, tên tác giả, thời gian đăng, badge danh mục, hình ảnh, tiêu đề, nội dung tóm tắt, số lượng tương tác | | Pass | 11/15/2015 | |
| **GUI-HTDS-BV-10** | Kiểm tra avatar tác giả | 1. Xem card bài viết<br>2. Kiểm tra avatar | Hiển thị Avatar h-8 w-8 với AvatarImage hoặc AvatarFallback (chữ cái đầu) | | Pass | 11/15/2015 | |
| **GUI-HTDS-BV-11** | Kiểm tra badge danh mục | 1. Xem card bài viết<br>2. Kiểm tra badge | Hiển thị Badge variant secondary với tên danh mục | | Pass | 11/15/2015 | |
| **GUI-HTDS-BV-12** | Kiểm tra hình ảnh bài viết | 1. Xem bài viết có hình ảnh<br>2. Kiểm tra hình ảnh | Hiển thị hình ảnh h-40 w-full object-cover trong div overflow-hidden | | Pass | 11/15/2015 | |
| **GUI-HTDS-BV-13** | Kiểm tra số lượng like | 1. Xem card bài viết<br>2. Kiểm tra số lượng | Hiển thị số lượng like với icon Heart h-3 w-3, text-xs | | Pass | 11/15/2015 | |
| **GUI-HTDS-BV-14** | Kiểm tra số lượng bình luận | 1. Xem card bài viết<br>2. Kiểm tra số lượng | Hiển thị số lượng bình luận với icon MessageSquare h-3 w-3, text-xs | | Pass | 11/15/2015 | |
| **GUI-HTDS-BV-15** | Kiểm tra số lượng chia sẻ | 1. Xem card bài viết<br>2. Kiểm tra số lượng | Hiển thị số lượng chia sẻ với icon Share2 h-3 w-3, text-xs | | Pass | 11/15/2015 | |
| **GUI-HTDS-BV-16** | Kiểm tra nút Xem chi tiết | 1. Xem card bài viết<br>2. Kiểm tra nút | Hiển thị nút "Xem chi tiết" với variant outline size sm, link đến /user/posts/[id] | | Pass | 11/15/2015 | |
| **GUI-HTDS-BV-17** | Kiểm tra phân trang | 1. Xem danh sách bài viết<br>2. Kiểm tra phân trang | Hiển thị phân trang với nút Previous (ChevronLeft), hiển thị "Trang X/Y", nút Next (ChevronRight) | | Pass | 11/15/2015 | |

---

### Check FUNC: Hiển thị danh sách bài viết

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-HTDS-BV-01** | Mở trang cộng đồng | 1. Truy cập trang cộng đồng từ menu | Hiển thị danh sách tất cả bài viết, có tab danh mục, ô tìm kiếm, bộ lọc | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BV-02** | Hiển thị danh sách bài viết | 1. Truy cập trang cộng đồng | Hiển thị danh sách với đầy đủ thông tin: avatar tác giả, tên tác giả, thời gian đăng, danh mục, hình ảnh, tiêu đề, nội dung tóm tắt, số lượng like/comment/share | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BV-03** | Sắp xếp theo thời gian mới nhất | 1. Truy cập trang cộng đồng<br>2. Chọn sắp xếp "Mới nhất" | Danh sách được sắp xếp theo thời gian đăng mới nhất trước | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BV-04** | Sắp xếp theo nhiều like nhất | 1. Truy cập trang cộng đồng<br>2. Chọn sắp xếp "Nhiều like nhất" | Danh sách được sắp xếp theo số lượng like giảm dần | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BV-05** | Sắp xếp theo nhiều bình luận nhất | 1. Truy cập trang cộng đồng<br>2. Chọn sắp xếp "Nhiều bình luận nhất" | Danh sách được sắp xếp theo số lượng bình luận giảm dần | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BV-06** | Tìm kiếm theo tiêu đề | 1. Truy cập trang cộng đồng<br>2. Nhập từ khóa vào ô tìm kiếm | Danh sách được lọc, chỉ hiển thị bài viết có tiêu đề chứa từ khóa | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BV-07** | Tìm kiếm theo nội dung | 1. Truy cập trang cộng đồng<br>2. Nhập từ khóa vào ô tìm kiếm | Danh sách được lọc, chỉ hiển thị bài viết có nội dung tóm tắt chứa từ khóa | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BV-08** | Lọc theo danh mục - Gundam | 1. Chọn tab "Gundam" hoặc bộ lọc "Gundam" | Chỉ hiển thị các bài viết thuộc danh mục "Gundam" | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BV-09** | Lọc theo danh mục - Figure | 1. Chọn tab "Figure" hoặc bộ lọc "Figure" | Chỉ hiển thị các bài viết thuộc danh mục "Figure" | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BV-10** | Lọc theo danh mục - Mô hình xe | 1. Chọn tab "Mô hình xe" hoặc bộ lọc "Mô hình xe" | Chỉ hiển thị các bài viết thuộc danh mục "Mô hình xe" | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BV-11** | Lọc theo danh mục - Máy bay | 1. Chọn tab "Máy bay" hoặc bộ lọc "Máy bay" | Chỉ hiển thị các bài viết thuộc danh mục "Máy bay" | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BV-12** | Lọc theo thời gian - Hôm nay | 1. Chọn bộ lọc thời gian "Hôm nay" | Chỉ hiển thị các bài viết được đăng hôm nay | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BV-13** | Lọc theo thời gian - Tuần này | 1. Chọn bộ lọc thời gian "Tuần này" | Chỉ hiển thị các bài viết được đăng trong tuần này | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BV-14** | Lọc theo thời gian - Tháng này | 1. Chọn bộ lọc thời gian "Tháng này" | Chỉ hiển thị các bài viết được đăng trong tháng này | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BV-15** | Kết hợp tìm kiếm và lọc | 1. Nhập từ khóa tìm kiếm<br>2. Chọn tab danh mục và bộ lọc thời gian<br>3. Chọn sắp xếp | Danh sách được lọc và sắp xếp theo tất cả tiêu chí, chỉ hiển thị bài viết thỏa mãn tất cả điều kiện | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BV-16** | Hiển thị khi không có bài viết | 1. Chọn tab danh mục không có bài viết<br>2. Kiểm tra hiển thị | Hiển thị thông báo "Không có bài viết nào" hoặc danh sách trống | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BV-17** | Tìm kiếm real-time | 1. Truy cập trang cộng đồng<br>2. Nhập từ khóa vào ô tìm kiếm | Danh sách được lọc ngay khi nhập, không cần nhấn Enter | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BV-18** | Phân trang | 1. Xem danh sách có nhiều bài viết<br>2. Điều hướng phân trang | Có thể chuyển trang, hiển thị số trang chính xác, nút Previous/Next hoạt động đúng | | Pass | 11/15/2015 | |

---

### Function: Xem chi tiết bài viết

#### Check GUI: Xem chi tiết bài viết

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XCT-BV-01** | Kiểm tra tiêu đề chi tiết | 1. Xem chi tiết bài viết<br>2. Kiểm tra tiêu đề | Hiển thị CardTitle "Chi tiết bài viết" với CardDescription ID bài viết | | Pass | 11/15/2015 | |
| **GUI-XCT-BV-02** | Kiểm tra nút Quay lại | 1. Xem chi tiết bài viết<br>2. Kiểm tra nút | Hiển thị nút "Quay lại danh sách" với icon ArrowLeft, variant ghost size sm, link đến /user/posts | | Pass | 11/15/2015 | |
| **GUI-XCT-BV-03** | Kiểm tra thông tin tác giả | 1. Xem chi tiết bài viết<br>2. Kiểm tra thông tin | Hiển thị Avatar h-10 w-10, tên tác giả font-medium, thời gian đăng text-xs text-muted-foreground | | Pass | 11/15/2015 | |
| **GUI-XCT-BV-04** | Kiểm tra nút Theo dõi | 1. Xem chi tiết bài viết<br>2. Kiểm tra nút | Hiển thị nút "Theo dõi" hoặc "Bỏ theo dõi" variant outline size sm | | Pass | 11/15/2015 | |
| **GUI-XCT-BV-05** | Kiểm tra nút Chỉnh sửa | 1. Xem chi tiết bài viết của mình<br>2. Kiểm tra nút | Hiển thị nút "Chỉnh sửa" với icon Edit, variant outline size sm, link đến /user/posts/[id]/edit | | Pass | 11/15/2015 | |
| **GUI-XCT-BV-06** | Kiểm tra nút Xóa bài viết | 1. Xem chi tiết bài viết của mình<br>2. Kiểm tra nút | Hiển thị nút "Xóa bài viết" với icon Trash2, variant destructive size sm | | Pass | 11/15/2015 | |
| **GUI-XCT-BV-07** | Kiểm tra tiêu đề bài viết | 1. Xem chi tiết bài viết<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề với text-xl font-semibold | | Pass | 11/15/2015 | |
| **GUI-XCT-BV-08** | Kiểm tra nội dung bài viết | 1. Xem chi tiết bài viết<br>2. Kiểm tra nội dung | Hiển thị nội dung đầy đủ với text-sm leading-relaxed text-muted-foreground, không bị cắt | | Pass | 11/15/2015 | |
| **GUI-XCT-BV-09** | Kiểm tra gallery hình ảnh | 1. Xem bài viết có hình ảnh<br>2. Kiểm tra gallery | Hiển thị grid grid-cols-2 md:grid-cols-3 gap-2 với các hình ảnh aspect-video object-cover rounded-lg | | Pass | 11/15/2015 | |
| **GUI-XCT-BV-10** | Kiểm tra video bài viết | 1. Xem bài viết có video<br>2. Kiểm tra video | Hiển thị video với controls, w-full h-64 object-cover rounded-lg | | Pass | 11/15/2015 | |
| **GUI-XCT-BV-11** | Kiểm tra nút Like | 1. Xem chi tiết bài viết<br>2. Kiểm tra nút | Hiển thị nút "Like" hoặc "Unlike" với icon Heart, variant outline hoặc default tùy trạng thái, fill-red-500 nếu đã like | | Pass | 11/15/2015 | |
| **GUI-XCT-BV-12** | Kiểm tra nút Bình luận | 1. Xem chi tiết bài viết<br>2. Kiểm tra nút | Hiển thị nút "Bình luận" với icon MessageSquare, variant outline size sm | | Pass | 11/15/2015 | |
| **GUI-XCT-BV-13** | Kiểm tra nút Chia sẻ | 1. Xem chi tiết bài viết<br>2. Kiểm tra nút | Hiển thị nút "Chia sẻ" với icon Share2, variant outline size sm | | Pass | 11/15/2015 | |
| **GUI-XCT-BV-14** | Kiểm tra badge số lượng like | 1. Xem chi tiết bài viết<br>2. Kiểm tra badge | Hiển thị Badge bg-pink-100 text-pink-800 cursor-pointer với số lượng like, có thể click để xem danh sách | | Pass | 11/15/2015 | |
| **GUI-XCT-BV-15** | Kiểm tra form bình luận | 1. Xem chi tiết bài viết<br>2. Kiểm tra form | Hiển thị form bình luận với Avatar, Textarea placeholder "Viết bình luận...", nút "Gửi bình luận" và "Hủy" | | Pass | 11/15/2015 | |
| **GUI-XCT-BV-16** | Kiểm tra danh sách bình luận | 1. Xem chi tiết bài viết<br>2. Kiểm tra danh sách | Hiển thị danh sách bình luận với Avatar, tên người dùng, thời gian, nội dung, nút Thích/Phản hồi/Chỉnh sửa/Xóa | | Pass | 11/15/2015 | |

---

### Check FUNC: Xem chi tiết bài viết

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XCT-BV-01** | Mở chi tiết bài viết | 1. Từ danh sách bài viết<br>2. Nhấn nút "Xem chi tiết" | Mở trang chi tiết bài viết với đầy đủ thông tin | | Pass | 11/15/2015 | |
| **FUNC-XCT-BV-02** | Hiển thị chi tiết đầy đủ | 1. Xem chi tiết bài viết | Hiển thị đầy đủ: thông tin tác giả, tiêu đề, nội dung, hình ảnh/video, số lượng tương tác, danh sách bình luận | | Pass | 11/15/2015 | |
| **FUNC-XCT-BV-03** | Like bài viết | 1. Xem chi tiết bài viết<br>2. Nhấn nút "Like" | Bài viết được like, số lượng like tăng, nút chuyển thành "Unlike", icon Heart fill-red-500, hiển thị toast "Đã thích bài viết" | | Pass | 11/15/2015 | |
| **FUNC-XCT-BV-04** | Unlike bài viết | 1. Xem chi tiết bài viết đã like<br>2. Nhấn nút "Unlike" | Bài viết được unlike, số lượng like giảm, nút chuyển thành "Like", icon Heart không fill | | Pass | 11/15/2015 | |
| **FUNC-XCT-BV-05** | Xem danh sách người like | 1. Xem chi tiết bài viết<br>2. Click vào badge số lượng like | Mở modal hiển thị danh sách người đã like với Avatar, tên, thời gian like | | Pass | 11/15/2015 | |
| **FUNC-XCT-BV-06** | Theo dõi tác giả | 1. Xem chi tiết bài viết<br>2. Nhấn nút "Theo dõi" | Tác giả được theo dõi, nút chuyển thành "Bỏ theo dõi", thông báo được gửi đến tác giả | | Pass | 11/15/2015 | |
| **FUNC-XCT-BV-07** | Bỏ theo dõi tác giả | 1. Xem chi tiết bài viết đã theo dõi<br>2. Nhấn nút "Bỏ theo dõi" | Tác giả được bỏ theo dõi, nút chuyển thành "Theo dõi" | | Pass | 11/15/2015 | |
| **FUNC-XCT-BV-08** | Quay lại danh sách | 1. Xem chi tiết bài viết<br>2. Nhấn nút "Quay lại danh sách" | Quay lại trang danh sách bài viết, giữ nguyên trạng thái lọc và tìm kiếm | | Pass | 11/15/2015 | |
| **FUNC-XCT-BV-09** | Chia sẻ bài viết | 1. Xem chi tiết bài viết<br>2. Nhấn nút "Chia sẻ" | Mở modal hoặc copy link chia sẻ, hiển thị toast "Đã sao chép link chia sẻ" | | Pass | 11/15/2015 | |
| **FUNC-XCT-BV-10** | Gửi bình luận | 1. Xem chi tiết bài viết<br>2. Nhập nội dung bình luận<br>3. Nhấn "Gửi bình luận" | Bình luận được gửi, xuất hiện trong danh sách bình luận, số lượng bình luận tăng, form được reset | | Pass | 11/15/2015 | |
| **FUNC-XCT-BV-11** | Xem danh sách bình luận | 1. Xem chi tiết bài viết<br>2. Kiểm tra danh sách | Hiển thị danh sách bình luận với đầy đủ thông tin: avatar, tên, thời gian, nội dung, có thể tương tác | | Pass | 11/15/2015 | |

---

### Function: Tạo bài viết

#### Check GUI: Tạo bài viết

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-TBV-01** | Kiểm tra tiêu đề trang | 1. Truy cập trang tạo bài viết<br>2. Kiểm tra tiêu đề | Hiển thị CardTitle "Tạo bài viết mới" với icon Plus h-5 w-5 | | Pass | 11/15/2015 | |
| **GUI-TBV-02** | Kiểm tra nút Quay lại | 1. Truy cập trang tạo bài viết<br>2. Kiểm tra nút | Hiển thị nút "Quay lại" với icon ArrowLeft, variant ghost size sm, link đến /user/posts | | Pass | 11/15/2015 | |
| **GUI-TBV-03** | Kiểm tra trường Tiêu đề | 1. Truy cập trang tạo bài viết<br>2. Kiểm tra trường | Hiển thị Label "Tiêu đề bài viết", Input với placeholder "Nhập tiêu đề", required | | Pass | 11/15/2015 | |
| **GUI-TBV-04** | Kiểm tra trường Danh mục | 1. Truy cập trang tạo bài viết<br>2. Kiểm tra trường | Hiển thị Label "Danh mục mô hình", Select với các option: "Gundam", "Figure", "Mô hình xe", "Máy bay", "Khác" | | Pass | 11/15/2015 | |
| **GUI-TBV-05** | Kiểm tra trường Nội dung | 1. Truy cập trang tạo bài viết<br>2. Kiểm tra trường | Hiển thị Label "Nội dung", Textarea với placeholder "Chia sẻ kinh nghiệm, cảm nhận...", rows 6, required | | Pass | 11/15/2015 | |
| **GUI-TBV-06** | Kiểm tra upload hình ảnh | 1. Truy cập trang tạo bài viết<br>2. Kiểm tra upload | Hiển thị Label "Upload hình ảnh", Input type="file" accept="image/*" multiple, nút "Chọn ảnh", preview hình ảnh đã upload | | Pass | 11/15/2015 | |
| **GUI-TBV-07** | Kiểm tra upload video | 1. Truy cập trang tạo bài viết<br>2. Kiểm tra upload | Hiển thị Label "Upload video", Input type="file" accept="video/*", nút "Chọn video", preview video đã upload | | Pass | 11/15/2015 | |
| **GUI-TBV-08** | Kiểm tra thông tin mô hình | 1. Truy cập trang tạo bài viết<br>2. Kiểm tra card | Hiển thị Card border-dashed với các trường: Tên mô hình, Thương hiệu, Scale, Ghi chú | | Pass | 11/15/2015 | |
| **GUI-TBV-09** | Kiểm tra cài đặt quyền riêng tư | 1. Truy cập trang tạo bài viết<br>2. Kiểm tra trường | Hiển thị Label "Quyền riêng tư", Select với các option: "Công khai", "Bạn bè", "Riêng tư" | | Pass | 11/15/2015 | |
| **GUI-TBV-10** | Kiểm tra nút Lưu nháp | 1. Truy cập trang tạo bài viết<br>2. Kiểm tra nút | Hiển thị nút "Lưu nháp" variant outline | | Pass | 11/15/2015 | |
| **GUI-TBV-11** | Kiểm tra nút Đăng bài | 1. Truy cập trang tạo bài viết<br>2. Kiểm tra nút | Hiển thị nút "Đăng bài" variant default | | Pass | 11/15/2015 | |

---

### Check FUNC: Tạo bài viết

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TBV-01** | Mở trang tạo bài viết | 1. Từ danh sách bài viết<br>2. Nhấn nút "Tạo bài viết" | Mở trang tạo bài viết với form trống sẵn sàng nhập | | Pass | 11/15/2015 | |
| **FUNC-TBV-02** | Tạo bài viết thành công | 1. Điền đầy đủ: tiêu đề, danh mục, nội dung<br>2. Nhấn "Đăng bài" | Bài viết được tạo thành công, hiển thị toast "Đã tạo bài viết thành công", quay lại danh sách, bài viết xuất hiện trong danh sách | | Pass | 11/15/2015 | |
| **FUNC-TBV-03** | Tạo bài viết thiếu tiêu đề | 1. Để trống tiêu đề<br>2. Nhập các trường khác<br>3. Nhấn "Đăng bài" | Hiển thị toast lỗi "Vui lòng điền đầy đủ tiêu đề và nội dung", không tạo bài viết | | Pass | 11/15/2015 | |
| **FUNC-TBV-04** | Tạo bài viết thiếu nội dung | 1. Nhập tiêu đề<br>2. Để trống nội dung<br>3. Nhấn "Đăng bài" | Hiển thị toast lỗi "Vui lòng điền đầy đủ tiêu đề và nội dung", không tạo bài viết | | Pass | 11/15/2015 | |
| **FUNC-TBV-05** | Upload hình ảnh | 1. Truy cập trang tạo bài viết<br>2. Chọn hình ảnh để upload | Hình ảnh được upload, hiển thị preview, có thể xóa từng ảnh, tối đa 10 ảnh | | Pass | 11/15/2015 | |
| **FUNC-TBV-06** | Upload video | 1. Truy cập trang tạo bài viết<br>2. Chọn video để upload | Video được upload, hiển thị preview, có thể xóa, tối đa 1 video | | Pass | 11/15/2015 | |
| **FUNC-TBV-07** | Lưu nháp | 1. Nhập một số thông tin<br>2. Nhấn "Lưu nháp" | Bài viết được lưu nháp, hiển thị toast "Đã lưu nháp", có thể tiếp tục chỉnh sửa sau | | Pass | 11/15/2015 | |
| **FUNC-TBV-08** | Tạo bài viết với đầy đủ thông tin | 1. Nhập đầy đủ: tiêu đề, danh mục, nội dung, hình ảnh, video, thông tin mô hình, quyền riêng tư<br>2. Nhấn "Đăng bài" | Bài viết được tạo với đầy đủ thông tin, hiển thị trong danh sách với tất cả thông tin đã nhập | | Pass | 11/15/2015 | |
| **FUNC-TBV-09** | Chọn quyền riêng tư | 1. Truy cập trang tạo bài viết<br>2. Chọn quyền riêng tư | Quyền riêng tư được chọn, mặc định là "Công khai", có thể thay đổi | | Pass | 11/15/2015 | |
| **FUNC-TBV-10** | Xóa hình ảnh đã upload | 1. Upload hình ảnh<br>2. Nhấn nút xóa hình ảnh | Hình ảnh được xóa khỏi preview, có thể upload lại | | Pass | 11/15/2015 | |
| **FUNC-TBV-11** | Xóa video đã upload | 1. Upload video<br>2. Nhấn nút xóa video | Video được xóa khỏi preview, có thể upload lại | | Pass | 11/15/2015 | |

---

### Function: Chỉnh sửa bài viết

#### Check GUI: Chỉnh sửa bài viết

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CSBV-01** | Kiểm tra tiêu đề trang | 1. Truy cập trang chỉnh sửa<br>2. Kiểm tra tiêu đề | Hiển thị CardTitle "Chỉnh sửa bài viết" với icon Edit h-5 w-5 | | Pass | 11/15/2015 | |
| **GUI-CSBV-02** | Kiểm tra nút Quay lại | 1. Truy cập trang chỉnh sửa<br>2. Kiểm tra nút | Hiển thị nút "Quay lại chi tiết" với icon ArrowLeft, variant ghost size sm, link đến /user/posts/[id] | | Pass | 11/15/2015 | |
| **GUI-CSBV-03** | Kiểm tra form chỉnh sửa | 1. Truy cập trang chỉnh sửa<br>2. Kiểm tra form | Hiển thị form với các trường đã điền sẵn: tiêu đề, danh mục, nội dung, hình ảnh, video, thông tin mô hình, quyền riêng tư | | Pass | 11/15/2015 | |
| **GUI-CSBV-04** | Kiểm tra nút Thêm hình ảnh | 1. Xem hình ảnh hiện tại<br>2. Kiểm tra nút | Hiển thị nút "Thêm ảnh" với icon Plus, variant outline size sm | | Pass | 11/15/2015 | |
| **GUI-CSBV-05** | Kiểm tra nút Xóa hình ảnh | 1. Xem hình ảnh hiện tại<br>2. Kiểm tra nút | Hiển thị nút xóa trên mỗi hình ảnh với icon Trash2, variant destructive size xs, absolute top-1 right-1 | | Pass | 11/15/2015 | |
| **GUI-CSBV-06** | Kiểm tra nút Lưu thay đổi | 1. Truy cập trang chỉnh sửa<br>2. Kiểm tra nút | Hiển thị nút "Lưu thay đổi" variant default | | Pass | 11/15/2015 | |
| **GUI-CSBV-07** | Kiểm tra nút Hủy | 1. Truy cập trang chỉnh sửa<br>2. Kiểm tra nút | Hiển thị nút "Hủy" variant outline | | Pass | 11/15/2015 | |

---

### Check FUNC: Chỉnh sửa bài viết

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CSBV-01** | Mở trang chỉnh sửa | 1. Từ chi tiết bài viết của mình<br>2. Nhấn nút "Chỉnh sửa" | Mở trang chỉnh sửa với form đã điền sẵn thông tin hiện tại | | Pass | 11/15/2015 | |
| **FUNC-CSBV-02** | Chỉnh sửa bài viết thành công | 1. Mở trang chỉnh sửa<br>2. Sửa một số thông tin<br>3. Nhấn "Lưu thay đổi" | Bài viết được cập nhật, hiển thị toast "Đã cập nhật bài viết", quay lại chi tiết, thông tin được cập nhật, lịch sử chỉnh sửa được lưu | | Pass | 11/15/2015 | |
| **FUNC-CSBV-03** | Thêm hình ảnh mới | 1. Mở trang chỉnh sửa<br>2. Nhấn "Thêm ảnh"<br>3. Chọn hình ảnh | Hình ảnh mới được thêm vào danh sách, hiển thị preview, có thể xóa | | Pass | 11/15/2015 | |
| **FUNC-CSBV-04** | Xóa hình ảnh | 1. Mở trang chỉnh sửa<br>2. Nhấn nút xóa trên hình ảnh | Hình ảnh được xóa khỏi danh sách, preview được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-CSBV-05** | Thêm video mới | 1. Mở trang chỉnh sửa<br>2. Nhấn "Thêm/đổi video"<br>3. Chọn video | Video mới được thay thế, hiển thị preview, có thể xóa | | Pass | 11/15/2015 | |
| **FUNC-CSBV-06** | Xóa video | 1. Mở trang chỉnh sửa<br>2. Nhấn "Xóa video" | Video được xóa, preview biến mất, có thể thêm video mới | | Pass | 11/15/2015 | |
| **FUNC-CSBV-07** | Hủy chỉnh sửa | 1. Mở trang chỉnh sửa<br>2. Sửa một số thông tin<br>3. Nhấn "Hủy" | Quay lại trang chi tiết, thông tin không thay đổi, không lưu các chỉnh sửa | | Pass | 11/15/2015 | |
| **FUNC-CSBV-08** | Lưu lịch sử chỉnh sửa | 1. Chỉnh sửa bài viết<br>2. Lưu thay đổi<br>3. Kiểm tra lịch sử | Lịch sử chỉnh sửa được lưu với thời gian, nội dung thay đổi, có thể xem timeline | | Pass | 11/15/2015 | |
| **FUNC-CSBV-09** | Thông báo cho người theo dõi | 1. Chỉnh sửa bài viết<br>2. Lưu thay đổi<br>3. Kiểm tra thông báo | Thông báo được gửi đến người theo dõi về việc cập nhật bài viết | | Pass | 11/15/2015 | |

---

### Function: Xóa bài viết

#### Check GUI: Xóa bài viết

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XBV-01** | Kiểm tra nút Xóa bài viết | 1. Xem chi tiết bài viết của mình<br>2. Kiểm tra nút | Hiển thị nút "Xóa bài viết" với icon Trash2, variant destructive size sm | | Pass | 11/15/2015 | |
| **GUI-XBV-02** | Kiểm tra modal xác nhận | 1. Nhấn nút "Xóa bài viết"<br>2. Kiểm tra modal | Hiển thị modal với DialogTitle "Xác nhận xóa bài viết", DialogDescription "Bạn có chắc chắn muốn xóa bài viết này?", Card hiển thị thông tin bài viết | | Pass | 11/15/2015 | |
| **GUI-XBV-03** | Kiểm tra thông tin bài viết trong modal | 1. Mở modal xác nhận<br>2. Kiểm tra thông tin | Hiển thị tiêu đề bài viết, thời gian đăng, số lượng like/comment/share | | Pass | 11/15/2015 | |
| **GUI-XBV-04** | Kiểm tra nút Xác nhận xóa | 1. Mở modal xác nhận<br>2. Kiểm tra nút | Hiển thị nút "Xác nhận xóa" variant destructive | | Pass | 11/15/2015 | |
| **GUI-XBV-05** | Kiểm tra nút Hủy trong modal | 1. Mở modal xác nhận<br>2. Kiểm tra nút | Hiển thị nút "Hủy" variant outline | | Pass | 11/15/2015 | |

---

### Check FUNC: Xóa bài viết

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XBV-01** | Xóa bài viết | 1. Xem chi tiết bài viết của mình<br>2. Nhấn nút "Xóa bài viết"<br>3. Xác nhận xóa | Hiển thị modal xác nhận với thông tin bài viết, sau khi xác nhận, bài viết được xóa, hiển thị toast "Đã xóa bài viết", quay lại danh sách, bài viết biến mất | | Pass | 11/15/2015 | |
| **FUNC-XBV-02** | Hủy xóa bài viết | 1. Nhấn nút "Xóa bài viết"<br>2. Nhấn nút "Hủy" trong modal | Modal đóng, không xóa bài viết, bài viết vẫn còn | | Pass | 11/15/2015 | |
| **FUNC-XBV-03** | Xử lý dữ liệu liên quan | 1. Xóa bài viết có bình luận và like<br>2. Kiểm tra dữ liệu | Tất cả dữ liệu liên quan được xóa: bình luận, like, share, thông báo được gửi đến người tương tác | | Pass | 11/15/2015 | |
| **FUNC-XBV-04** | Đóng modal bằng click overlay | 1. Mở modal xác nhận<br>2. Click vào overlay | Modal đóng, không xóa bài viết | | Pass | 11/15/2015 | |

---

### Check VALIDATION: Tạo - hiển thị bài viết

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **VALID-THT-BV-01** | Tạo bài viết với tiêu đề quá dài | 1. Nhập tiêu đề > 200 ký tự<br>2. Gửi bài viết | Hiển thị cảnh báo hoặc tự động cắt tiêu đề, không cho phép gửi nếu vượt quá giới hạn | | Pass | 11/15/2015 | |
| **VALID-THT-BV-02** | Tạo bài viết với nội dung quá dài | 1. Nhập nội dung > 2000 ký tự<br>2. Gửi bài viết | Hiển thị cảnh báo hoặc tự động cắt nội dung, hiển thị số ký tự đã nhập/giới hạn | | Pass | 11/15/2015 | |
| **VALID-THT-BV-03** | Upload hình ảnh không đúng định dạng | 1. Chọn file không phải hình ảnh<br>2. Upload | Hiển thị thông báo lỗi "File không đúng định dạng", không upload | | Pass | 11/15/2015 | |
| **VALID-THT-BV-04** | Upload hình ảnh quá lớn | 1. Chọn hình ảnh > 10MB<br>2. Upload | Hiển thị thông báo lỗi "File quá lớn", không upload | | Pass | 11/15/2015 | |
| **VALID-THT-BV-05** | Upload quá nhiều hình ảnh | 1. Upload > 10 hình ảnh<br>2. Kiểm tra | Hệ thống chỉ cho phép tối đa 10 hình ảnh, hiển thị cảnh báo nếu vượt quá | | Pass | 11/15/2015 | |
| **VALID-THT-BV-06** | Upload video không đúng định dạng | 1. Chọn file không phải video<br>2. Upload | Hiển thị thông báo lỗi "File không đúng định dạng", không upload | | Pass | 11/15/2015 | |
| **VALID-THT-BV-07** | Upload video quá lớn | 1. Chọn video > 100MB<br>2. Upload | Hiển thị thông báo lỗi "File quá lớn", không upload | | Pass | 11/15/2015 | |
| **VALID-THT-BV-08** | Chỉnh sửa bài viết không phải của mình | 1. Xem chi tiết bài viết của người khác<br>2. Kiểm tra nút chỉnh sửa | Nút "Chỉnh sửa" không hiển thị, không thể chỉnh sửa bài viết của người khác | | Pass | 11/15/2015 | |
| **VALID-THT-BV-09** | Xóa bài viết không phải của mình | 1. Xem chi tiết bài viết của người khác<br>2. Kiểm tra nút xóa | Nút "Xóa bài viết" không hiển thị, không thể xóa bài viết của người khác | | Pass | 11/15/2015 | |
| **VALID-THT-BV-10** | Tìm kiếm với từ khóa đặc biệt | 1. Nhập từ khóa có ký tự đặc biệt<br>2. Tìm kiếm | Hệ thống xử lý an toàn, không gây lỗi, lọc kết quả chính xác | | Pass | 11/15/2015 | |

