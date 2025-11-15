# Test Case Template - Chức năng xem trang cá nhân người lạ (User)

## Module Code
**Model Management Store: Chức năng xem trang cá nhân người lạ User**

## Test Requirement
1. Hiển thị danh sách bài viết
2. Xem chi tiết các ảnh

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
| **GUI-HTDS-BV-01** | Kiểm tra tiêu đề trang | 1. Truy cập trang cá nhân người lạ<br>2. Kiểm tra tiêu đề | Hiển thị Card với CardHeader, CardTitle text-2xl với tên người dùng | | Pass | 11/15/2015 | |
| **GUI-HTDS-BV-02** | Kiểm tra thông tin cá nhân | 1. Truy cập trang cá nhân<br>2. Kiểm tra thông tin | Hiển thị Card với Avatar h-16 w-16, CardTitle, CardDescription với bio, Badge variant secondary với số bài viết, người theo dõi, đang theo dõi | | Pass | 11/15/2015 | |
| **GUI-HTDS-BV-03** | Kiểm tra avatar người dùng | 1. Xem thông tin cá nhân<br>2. Kiểm tra avatar | Hiển thị Avatar h-16 w-16 với AvatarImage và AvatarFallback là ký tự đầu của tên | | Pass | 11/15/2015 | |
| **GUI-HTDS-BV-04** | Kiểm tra tên người dùng | 1. Xem thông tin cá nhân<br>2. Kiểm tra tên | Hiển thị CardTitle text-2xl với tên người dùng | | Pass | 11/15/2015 | |
| **GUI-HTDS-BV-05** | Kiểm tra bio | 1. Xem thông tin cá nhân<br>2. Kiểm tra bio | Hiển thị CardDescription với bio của người dùng | | Pass | 11/15/2015 | |
| **GUI-HTDS-BV-06** | Kiểm tra badge số bài viết | 1. Xem thông tin cá nhân<br>2. Kiểm tra badge | Hiển thị Badge variant secondary với text "{số} bài viết" | | Pass | 11/15/2015 | |
| **GUI-HTDS-BV-07** | Kiểm tra badge số người theo dõi | 1. Xem thông tin cá nhân<br>2. Kiểm tra badge | Hiển thị Badge variant secondary với text "{số} người theo dõi", format số với toLocaleString() | | Pass | 11/15/2015 | |
| **GUI-HTDS-BV-08** | Kiểm tra badge đang theo dõi | 1. Xem thông tin cá nhân<br>2. Kiểm tra badge | Hiển thị Badge variant secondary với text "Đang theo dõi {số}" | | Pass | 11/15/2015 | |
| **GUI-HTDS-BV-09** | Kiểm tra nút Theo dõi | 1. Xem thông tin cá nhân<br>2. Kiểm tra nút | Hiển thị nút "+ Theo dõi" variant default, có thể click để theo dõi/bỏ theo dõi | | Pass | 11/15/2015 | |
| **GUI-HTDS-BV-10** | Kiểm tra nút Nhắn tin | 1. Xem thông tin cá nhân<br>2. Kiểm tra nút | Hiển thị nút "Nhắn tin" variant outline, có thể click để mở chat | | Pass | 11/15/2015 | |
| **GUI-HTDS-BV-11** | Kiểm tra tab danh mục | 1. Xem trang cá nhân<br>2. Kiểm tra tab | Hiển thị TabsList với TabsTrigger: "Bài viết" (icon ImageIcon), "Ảnh" (icon Camera), "Video" (icon VideoIcon) | | Pass | 11/15/2015 | |
| **GUI-HTDS-BV-12** | Kiểm tra ô tìm kiếm | 1. Xem trang cá nhân<br>2. Kiểm tra tìm kiếm | Hiển thị Input với icon Search absolute left-3 top-3, placeholder "Tìm bài viết/ảnh/video...", className pl-9 | | Pass | 11/15/2015 | |
| **GUI-HTDS-BV-13** | Kiểm tra bộ lọc thời gian | 1. Xem trang cá nhân<br>2. Kiểm tra bộ lọc | Hiển thị Select với trigger w-[160px], options: "Tất cả", "Tuần này", "Tháng này", "Năm nay" | | Pass | 11/15/2015 | |
| **GUI-HTDS-BV-14** | Kiểm tra bộ lọc sắp xếp | 1. Xem trang cá nhân<br>2. Kiểm tra bộ lọc | Hiển thị Select với trigger w-[200px], options: "Mới nhất", "Nhiều like nhất", "Nhiều bình luận nhất" | | Pass | 11/15/2015 | |
| **GUI-HTDS-BV-15** | Kiểm tra bộ lọc danh mục (tab Ảnh) | 1. Chọn tab "Ảnh"<br>2. Kiểm tra bộ lọc | Hiển thị Select với trigger w-[200px], options: "Tất cả", "Gunpla", "Action Figures", "Model Kits", "Khác" | | Pass | 11/15/2015 | |
| **GUI-HTDS-BV-16** | Kiểm tra nút Lọc | 1. Xem trang cá nhân<br>2. Kiểm tra nút | Hiển thị nút "Lọc" variant outline với icon Filter h-4 w-4 | | Pass | 11/15/2015 | |
| **GUI-HTDS-BV-17** | Kiểm tra card bài viết | 1. Xem tab "Bài viết"<br>2. Kiểm tra card | Hiển thị Card trong grid grid-cols-1 md:grid-cols-2 gap-4, có hình ảnh cover, CardHeader, CardContent | | Pass | 11/15/2015 | |
| **GUI-HTDS-BV-18** | Kiểm tra hình ảnh bài viết | 1. Xem card bài viết<br>2. Kiểm tra hình ảnh | Hiển thị hình ảnh w-full h-40 md:h-48 object-cover trong div overflow-hidden | | Pass | 11/15/2015 | |
| **GUI-HTDS-BV-19** | Kiểm tra tiêu đề bài viết | 1. Xem card bài viết<br>2. Kiểm tra tiêu đề | Hiển thị CardTitle text-base line-clamp-1 với tiêu đề bài viết | | Pass | 11/15/2015 | |
| **GUI-HTDS-BV-20** | Kiểm tra nội dung tóm tắt | 1. Xem card bài viết<br>2. Kiểm tra nội dung | Hiển thị CardDescription line-clamp-2 với nội dung tóm tắt | | Pass | 11/15/2015 | |
| **GUI-HTDS-BV-21** | Kiểm tra thời gian đăng | 1. Xem card bài viết<br>2. Kiểm tra thời gian | Hiển thị text-xs text-muted-foreground với thời gian đăng | | Pass | 11/15/2015 | |
| **GUI-HTDS-BV-22** | Kiểm tra số lượng like | 1. Xem card bài viết<br>2. Kiểm tra số lượng | Hiển thị số lượng like với icon Heart h-4 w-4, text-sm | | Pass | 11/15/2015 | |
| **GUI-HTDS-BV-23** | Kiểm tra số lượng bình luận | 1. Xem card bài viết<br>2. Kiểm tra số lượng | Hiển thị số lượng bình luận với icon MessageSquare h-4 w-4, text-sm | | Pass | 11/15/2015 | |
| **GUI-HTDS-BV-24** | Kiểm tra số lượng chia sẻ | 1. Xem card bài viết<br>2. Kiểm tra số lượng | Hiển thị số lượng chia sẻ với icon Share2 h-4 w-4, text-sm | | Pass | 11/15/2015 | |
| **GUI-HTDS-BV-25** | Kiểm tra tags bài viết | 1. Xem card bài viết<br>2. Kiểm tra tags | Hiển thị Badge variant secondary text-xs với các tags, flex flex-wrap gap-1 | | Pass | 11/15/2015 | |
| **GUI-HTDS-BV-26** | Kiểm tra phân trang | 1. Xem danh sách bài viết<br>2. Kiểm tra phân trang | Hiển thị phân trang nếu có nhiều bài viết, có thể điều hướng giữa các trang | | Pass | 11/15/2015 | |

---

### Check FUNC: Hiển thị danh sách bài viết

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-HTDS-BV-01** | Hiển thị trang cá nhân | 1. Click vào tên tác giả từ bài viết<br>2. Xem trang cá nhân | Hiển thị trang cá nhân với đầy đủ thông tin: avatar, tên, bio, số bài viết, người theo dõi, đang theo dõi, nút theo dõi, nút nhắn tin | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BV-02** | Hiển thị danh sách bài viết | 1. Chọn tab "Bài viết"<br>2. Xem danh sách | Hiển thị danh sách bài viết công khai với đầy đủ thông tin: hình ảnh cover, tiêu đề, nội dung tóm tắt, thời gian đăng, số lượng like/bình luận/chia sẻ, tags | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BV-03** | Lọc theo thời gian - Tất cả | 1. Chọn bộ lọc thời gian "Tất cả"<br>2. Xem danh sách | Hiển thị tất cả bài viết không giới hạn thời gian | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BV-04** | Lọc theo thời gian - Tuần này | 1. Chọn bộ lọc thời gian "Tuần này"<br>2. Xem danh sách | Chỉ hiển thị các bài viết được đăng trong tuần này | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BV-05** | Lọc theo thời gian - Tháng này | 1. Chọn bộ lọc thời gian "Tháng này"<br>2. Xem danh sách | Chỉ hiển thị các bài viết được đăng trong tháng này | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BV-06** | Lọc theo thời gian - Năm nay | 1. Chọn bộ lọc thời gian "Năm nay"<br>2. Xem danh sách | Chỉ hiển thị các bài viết được đăng trong năm nay | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BV-07** | Sắp xếp theo Mới nhất | 1. Chọn sắp xếp "Mới nhất"<br>2. Xem danh sách | Danh sách được sắp xếp theo thời gian đăng mới nhất trước | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BV-08** | Sắp xếp theo Nhiều like nhất | 1. Chọn sắp xếp "Nhiều like nhất"<br>2. Xem danh sách | Danh sách được sắp xếp theo số lượng like giảm dần | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BV-09** | Sắp xếp theo Nhiều bình luận nhất | 1. Chọn sắp xếp "Nhiều bình luận nhất"<br>2. Xem danh sách | Danh sách được sắp xếp theo số lượng bình luận giảm dần | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BV-10** | Tìm kiếm bài viết | 1. Nhập từ khóa vào ô tìm kiếm<br>2. Xem kết quả | Danh sách được lọc, chỉ hiển thị bài viết có tiêu đề hoặc nội dung chứa từ khóa | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BV-11** | Kết hợp tìm kiếm và lọc | 1. Nhập từ khóa tìm kiếm<br>2. Chọn bộ lọc thời gian và sắp xếp | Danh sách được lọc và sắp xếp theo tất cả tiêu chí, chỉ hiển thị bài viết thỏa mãn tất cả điều kiện | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BV-12** | Theo dõi người dùng | 1. Nhấn nút "+ Theo dõi"<br>2. Kiểm tra trạng thái | Người dùng được theo dõi, nút chuyển thành "Bỏ theo dõi", số lượng người theo dõi tăng, hiển thị toast "Đã theo dõi" | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BV-13** | Bỏ theo dõi người dùng | 1. Nhấn nút "Bỏ theo dõi"<br>2. Kiểm tra trạng thái | Người dùng được bỏ theo dõi, nút chuyển thành "+ Theo dõi", số lượng người theo dõi giảm, hiển thị toast "Đã bỏ theo dõi" | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BV-14** | Nhắn tin cho người dùng | 1. Nhấn nút "Nhắn tin"<br>2. Kiểm tra hành động | Mở trang chat hoặc modal chat với người dùng, có thể gửi tin nhắn | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BV-15** | Xem chi tiết bài viết | 1. Click vào card bài viết hoặc tiêu đề<br>2. Xem chi tiết | Chuyển đến trang chi tiết bài viết với đầy đủ nội dung, hình ảnh, video, bình luận | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BV-16** | Hiển thị khi không có bài viết | 1. Xem trang cá nhân không có bài viết<br>2. Kiểm tra hiển thị | Hiển thị thông báo "Chưa có bài viết nào" hoặc danh sách trống | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BV-17** | Tìm kiếm real-time | 1. Nhập từ khóa vào ô tìm kiếm<br>2. Xem kết quả | Danh sách được lọc ngay khi nhập, không cần nhấn Enter | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BV-18** | Chuyển đổi tab | 1. Chọn tab "Bài viết", "Ảnh", hoặc "Video"<br>2. Xem nội dung | Nội dung được thay đổi theo tab đã chọn, bộ lọc danh mục chỉ hiển thị ở tab "Ảnh" | | Pass | 11/15/2015 | |

---

### Function: Xem chi tiết các ảnh

#### Check GUI: Xem chi tiết các ảnh

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XCT-A-01** | Kiểm tra tab Ảnh | 1. Chọn tab "Ảnh"<br>2. Kiểm tra tab | Hiển thị TabsTrigger value="photos" với icon Camera h-4 w-4, text "Ảnh" | | Pass | 11/15/2015 | |
| **GUI-XCT-A-02** | Kiểm tra gallery ảnh | 1. Chọn tab "Ảnh"<br>2. Kiểm tra gallery | Hiển thị grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-3 với các button chứa ảnh | | Pass | 11/15/2015 | |
| **GUI-XCT-A-03** | Kiểm tra card ảnh | 1. Xem gallery ảnh<br>2. Kiểm tra card | Hiển thị button relative group aspect-square overflow-hidden rounded-lg border với ảnh bên trong | | Pass | 11/15/2015 | |
| **GUI-XCT-A-04** | Kiểm tra ảnh mô hình | 1. Xem card ảnh<br>2. Kiểm tra ảnh | Hiển thị ảnh h-full w-full object-cover transition-transform group-hover:scale-105 | | Pass | 11/15/2015 | |
| **GUI-XCT-A-05** | Kiểm tra overlay khi hover | 1. Hover vào card ảnh<br>2. Kiểm tra overlay | Hiển thị overlay absolute inset-0 bg-black/0 group-hover:bg-black/30 transition-colors | | Pass | 11/15/2015 | |
| **GUI-XCT-A-06** | Kiểm tra thông tin ảnh khi hover | 1. Hover vào card ảnh<br>2. Kiểm tra thông tin | Hiển thị thông tin absolute bottom-2 left-2 right-2 text-white text-xs opacity-0 group-hover:opacity-100 với tên ảnh, số like, số bình luận | | Pass | 11/15/2015 | |
| **GUI-XCT-A-07** | Kiểm tra modal xem ảnh | 1. Click vào ảnh<br>2. Kiểm tra modal | Hiển thị Dialog với DialogContent max-w-3xl, DialogHeader, DialogTitle, DialogDescription | | Pass | 11/15/2015 | |
| **GUI-XCT-A-08** | Kiểm tra ảnh phóng to trong modal | 1. Mở modal xem ảnh<br>2. Kiểm tra ảnh | Hiển thị ảnh trong div aspect-video w-full overflow-hidden rounded-lg border với object-cover | | Pass | 11/15/2015 | |
| **GUI-XCT-A-09** | Kiểm tra thông tin chi tiết trong modal | 1. Mở modal xem ảnh<br>2. Kiểm tra thông tin | Hiển thị DialogTitle với tên ảnh, số like (icon Heart), số bình luận (icon MessageSquare), DialogDescription với thời gian upload | | Pass | 11/15/2015 | |
| **GUI-XCT-A-10** | Kiểm tra danh sách bình luận trong modal | 1. Mở modal xem ảnh<br>2. Kiểm tra bình luận | Hiển thị Label "Bình luận", danh sách bình luận text-sm text-muted-foreground với tên người dùng và nội dung | | Pass | 11/15/2015 | |
| **GUI-XCT-A-11** | Kiểm tra nút đóng modal | 1. Mở modal xem ảnh<br>2. Kiểm tra nút | Có thể đóng modal bằng cách click overlay hoặc nút đóng | | Pass | 11/15/2015 | |

---

### Check FUNC: Xem chi tiết các ảnh

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XCT-A-01** | Hiển thị gallery ảnh | 1. Chọn tab "Ảnh"<br>2. Xem gallery | Hiển thị gallery ảnh mô hình với grid layout, mỗi ảnh có hover effect, hiển thị thông tin khi hover | | Pass | 11/15/2015 | |
| **FUNC-XCT-A-02** | Lọc ảnh theo thời gian | 1. Chọn tab "Ảnh"<br>2. Chọn bộ lọc thời gian | Gallery được lọc theo thời gian đã chọn, chỉ hiển thị ảnh trong khoảng thời gian đó | | Pass | 11/15/2015 | |
| **FUNC-XCT-A-03** | Lọc ảnh theo danh mục | 1. Chọn tab "Ảnh"<br>2. Chọn bộ lọc danh mục | Gallery được lọc theo danh mục đã chọn (Gunpla, Action Figures, Model Kits, Khác), chỉ hiển thị ảnh thuộc danh mục đó | | Pass | 11/15/2015 | |
| **FUNC-XCT-A-04** | Sắp xếp ảnh theo Mới nhất | 1. Chọn tab "Ảnh"<br>2. Chọn sắp xếp "Mới nhất" | Gallery được sắp xếp theo thời gian upload mới nhất trước | | Pass | 11/15/2015 | |
| **FUNC-XCT-A-05** | Sắp xếp ảnh theo Nhiều like nhất | 1. Chọn tab "Ảnh"<br>2. Chọn sắp xếp "Nhiều like nhất" | Gallery được sắp xếp theo số lượng like giảm dần | | Pass | 11/15/2015 | |
| **FUNC-XCT-A-06** | Sắp xếp ảnh theo Cũ nhất | 1. Chọn tab "Ảnh"<br>2. Chọn sắp xếp "Cũ nhất" | Gallery được sắp xếp theo thời gian upload cũ nhất trước | | Pass | 11/15/2015 | |
| **FUNC-XCT-A-07** | Mở modal xem ảnh chi tiết | 1. Click vào ảnh trong gallery<br>2. Xem modal | Mở modal hiển thị ảnh phóng to, thông tin chi tiết (tên, số like, số bình luận, thời gian upload), danh sách bình luận | | Pass | 11/15/2015 | |
| **FUNC-XCT-A-08** | Đóng modal xem ảnh | 1. Mở modal xem ảnh<br>2. Click overlay hoặc nút đóng | Modal đóng, quay lại gallery | | Pass | 11/15/2015 | |
| **FUNC-XCT-A-09** | Tìm kiếm ảnh | 1. Chọn tab "Ảnh"<br>2. Nhập từ khóa vào ô tìm kiếm | Gallery được lọc, chỉ hiển thị ảnh có tên hoặc thông tin chứa từ khóa | | Pass | 11/15/2015 | |
| **FUNC-XCT-A-10** | Kết hợp tìm kiếm và lọc | 1. Nhập từ khóa tìm kiếm<br>2. Chọn bộ lọc thời gian, danh mục và sắp xếp | Gallery được lọc và sắp xếp theo tất cả tiêu chí, chỉ hiển thị ảnh thỏa mãn tất cả điều kiện | | Pass | 11/15/2015 | |
| **FUNC-XCT-A-11** | Hiển thị khi không có ảnh | 1. Xem trang cá nhân không có ảnh<br>2. Kiểm tra hiển thị | Hiển thị thông báo "Chưa có ảnh nào" hoặc gallery trống | | Pass | 11/15/2015 | |
| **FUNC-XCT-A-12** | Tương tác với ảnh trong modal | 1. Mở modal xem ảnh<br>2. Tương tác với ảnh | Có thể like, bình luận, chia sẻ ảnh từ modal, số lượng được cập nhật real-time | | Pass | 11/15/2015 | |
| **FUNC-XCT-A-13** | Xem video trong tab Video | 1. Chọn tab "Video"<br>2. Xem danh sách | Hiển thị grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4 với Card chứa thumbnail, duration, tiêu đề, thời gian upload, số like, số bình luận | | Pass | 11/15/2015 | |
| **FUNC-XCT-A-14** | Phân trang gallery ảnh | 1. Xem gallery có nhiều ảnh<br>2. Kiểm tra phân trang | Hiển thị phân trang, có thể điều hướng giữa các trang | | Pass | 11/15/2015 | |

---

### Check VALIDATION: Chức năng xem trang cá nhân người lạ

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **VALID-XTCPNL-01** | Truy cập trang cá nhân không tồn tại | 1. Truy cập URL với ID người dùng không tồn tại<br>2. Kiểm tra hiển thị | Hiển thị thông báo lỗi "Người dùng không tồn tại" hoặc trang 404 | | Pass | 11/15/2015 | |
| **VALID-XTCPNL-02** | Truy cập trang cá nhân bị chặn | 1. Truy cập trang cá nhân của người dùng đã chặn mình<br>2. Kiểm tra hiển thị | Hiển thị thông báo "Bạn không thể xem trang cá nhân này" hoặc chặn truy cập | | Pass | 11/15/2015 | |
| **VALID-XTCPNL-03** | Tìm kiếm với từ khóa đặc biệt | 1. Nhập từ khóa có ký tự đặc biệt<br>2. Tìm kiếm | Hệ thống xử lý an toàn, không gây lỗi, lọc kết quả chính xác | | Pass | 11/15/2015 | |
| **VALID-XTCPNL-04** | Theo dõi chính mình | 1. Truy cập trang cá nhân của chính mình<br>2. Kiểm tra nút theo dõi | Nút "Theo dõi" không hiển thị hoặc bị vô hiệu hóa, hiển thị thông báo "Đây là trang cá nhân của bạn" | | Pass | 11/15/2015 | |
| **VALID-XTCPNL-05** | Xem ảnh không tồn tại | 1. Click vào ảnh không tồn tại<br>2. Kiểm tra modal | Hiển thị thông báo lỗi "Ảnh không tồn tại" hoặc không mở modal | | Pass | 11/15/2015 | |
| **VALID-XTCPNL-06** | Lọc với giá trị không hợp lệ | 1. Chọn bộ lọc với giá trị không hợp lệ<br>2. Kiểm tra kết quả | Hệ thống xử lý an toàn, không gây lỗi, hiển thị danh sách mặc định | | Pass | 11/15/2015 | |
| **VALID-XTCPNL-07** | Tìm kiếm với từ khóa rỗng | 1. Để trống ô tìm kiếm<br>2. Xem kết quả | Hiển thị tất cả nội dung, không lọc | | Pass | 11/15/2015 | |
| **VALID-XTCPNL-08** | Xem trang cá nhân khi chưa đăng nhập | 1. Chưa đăng nhập<br>2. Truy cập trang cá nhân | Hiển thị trang cá nhân công khai hoặc yêu cầu đăng nhập tùy cài đặt quyền riêng tư | | Pass | 11/15/2015 | |

