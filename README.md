# Test Case Template - Tương tác bài viết (User)

## Module Code
**Model Management Store: Tương tác bài viết User**

## Test Requirement
1. Hiển thị danh sách bình luận
2. Hiển thị số lượng like
3. Tạo bình luận
4. Xóa bình luận
5. Chỉnh sửa bình luận

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

### Function: Hiển thị danh sách bình luận

#### Check GUI: Hiển thị danh sách bình luận

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-HTDS-BL-01** | Kiểm tra tab Bình luận | 1. Xem chi tiết bài viết<br>2. Kiểm tra tab | Hiển thị tab "Bình luận" trong TabsList, có thể chọn để xem danh sách bình luận | | Pass | 11/15/2015 | |
| **GUI-HTDS-BL-02** | Kiểm tra số lượng bình luận | 1. Xem tab "Bình luận"<br>2. Kiểm tra số lượng | Hiển thị Badge với tổng số bình luận, cập nhật khi có bình luận mới | | Pass | 11/15/2015 | |
| **GUI-HTDS-BL-03** | Kiểm tra bộ lọc bình luận | 1. Xem tab "Bình luận"<br>2. Kiểm tra bộ lọc | Hiển thị Select với trigger w-32, các option: "Tất cả", "Gần đây", "Phổ biến", "Gây tranh cãi" | | Pass | 11/15/2015 | |
| **GUI-HTDS-BL-04** | Kiểm tra bộ lọc sắp xếp | 1. Xem tab "Bình luận"<br>2. Kiểm tra bộ lọc | Hiển thị Select với trigger w-32, các option: "Mới nhất", "Cũ nhất", "Nhiều like nhất", "Nhiều trả lời nhất" | | Pass | 11/15/2015 | |
| **GUI-HTDS-BL-05** | Kiểm tra ô tìm kiếm | 1. Xem tab "Bình luận"<br>2. Kiểm tra tìm kiếm | Hiển thị Input với placeholder "Tìm kiếm bình luận..." | | Pass | 11/15/2015 | |
| **GUI-HTDS-BL-06** | Kiểm tra card bình luận | 1. Xem danh sách bình luận<br>2. Kiểm tra card | Hiển thị card với CardContent p-4, chứa avatar, tên người dùng, thời gian, nội dung, hình ảnh (nếu có), số lượng tương tác, nút hành động | | Pass | 11/15/2015 | |
| **GUI-HTDS-BL-07** | Kiểm tra avatar người bình luận | 1. Xem card bình luận<br>2. Kiểm tra avatar | Hiển thị avatar w-8 h-8 rounded-full với hình ảnh hoặc fallback | | Pass | 11/15/2015 | |
| **GUI-HTDS-BL-08** | Kiểm tra badge rank | 1. Xem card bình luận<br>2. Kiểm tra badge | Hiển thị Badge variant outline text-xs với rank của người dùng | | Pass | 11/15/2015 | |
| **GUI-HTDS-BL-09** | Kiểm tra thời gian bình luận | 1. Xem card bình luận<br>2. Kiểm tra thời gian | Hiển thị thời gian với icon Clock h-3 w-3, format ngày Việt Nam, text-sm text-muted-foreground | | Pass | 11/15/2015 | |
| **GUI-HTDS-BL-10** | Kiểm tra nội dung bình luận | 1. Xem card bình luận<br>2. Kiểm tra nội dung | Hiển thị nội dung với text-muted-foreground, đầy đủ không bị cắt | | Pass | 11/15/2015 | |
| **GUI-HTDS-BL-11** | Kiểm tra hình ảnh đính kèm | 1. Xem bình luận có hình ảnh<br>2. Kiểm tra hình ảnh | Hiển thị hình ảnh w-20 h-20 object-cover rounded-lg cursor-pointer hover:opacity-80 trong flex gap-2 | | Pass | 11/15/2015 | |
| **GUI-HTDS-BL-12** | Kiểm tra số lượng like bình luận | 1. Xem card bình luận<br>2. Kiểm tra số lượng | Hiển thị số lượng like với icon ThumbsUp h-4 w-4, có thể click để like | | Pass | 11/15/2015 | |
| **GUI-HTDS-BL-13** | Kiểm tra số lượng dislike | 1. Xem card bình luận<br>2. Kiểm tra số lượng | Hiển thị số lượng dislike với icon ThumbsDown h-4 w-4, có thể click để dislike | | Pass | 11/15/2015 | |
| **GUI-HTDS-BL-14** | Kiểm tra số lượng phản hồi | 1. Xem card bình luận<br>2. Kiểm tra số lượng | Hiển thị số lượng phản hồi với text "Trả lời (X)", có thể click để xem phản hồi | | Pass | 11/15/2015 | |
| **GUI-HTDS-BL-15** | Kiểm tra nút Like bình luận | 1. Xem card bình luận<br>2. Kiểm tra nút | Hiển thị nút với icon ThumbsUp, variant ghost size sm, text-red-500 nếu đã like | | Pass | 11/15/2015 | |
| **GUI-HTDS-BL-16** | Kiểm tra nút Phản hồi | 1. Xem card bình luận<br>2. Kiểm tra nút | Hiển thị nút "Trả lời" với icon Reply h-4 w-4, variant ghost size sm | | Pass | 11/15/2015 | |
| **GUI-HTDS-BL-17** | Kiểm tra nút Chỉnh sửa | 1. Xem bình luận của mình<br>2. Kiểm tra nút | Hiển thị nút với icon Edit h-4 w-4, variant ghost size sm, chỉ hiển thị cho bình luận của mình | | Pass | 11/15/2015 | |
| **GUI-HTDS-BL-18** | Kiểm tra nút Xóa | 1. Xem bình luận của mình<br>2. Kiểm tra nút | Hiển thị nút với icon Trash2 h-4 w-4, variant ghost size sm, chỉ hiển thị cho bình luận của mình | | Pass | 11/15/2015 | |
| **GUI-HTDS-BL-19** | Kiểm tra nút Báo cáo | 1. Xem bình luận<br>2. Kiểm tra nút | Hiển thị nút với icon Flag h-4 w-4, variant ghost size sm, có thể báo cáo bình luận | | Pass | 11/15/2015 | |
| **GUI-HTDS-BL-20** | Kiểm tra phản hồi bình luận | 1. Xem bình luận có phản hồi<br>2. Kiểm tra phản hồi | Hiển thị phản hồi trong div ml-8 space-y-3, bg-muted rounded-lg, với avatar, tên, nội dung, số lượng like/dislike | | Pass | 11/15/2015 | |
| **GUI-HTDS-BL-21** | Kiểm tra phân trang | 1. Xem danh sách bình luận<br>2. Kiểm tra phân trang | Hiển thị phân trang nếu có nhiều bình luận, có thể điều hướng giữa các trang | | Pass | 11/15/2015 | |

---

### Check FUNC: Hiển thị danh sách bình luận

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-HTDS-BL-01** | Mở tab Bình luận | 1. Xem chi tiết bài viết<br>2. Chọn tab "Bình luận" | Hiển thị danh sách tất cả bình luận, có form tạo bình luận, bộ lọc, ô tìm kiếm | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BL-02** | Hiển thị danh sách bình luận | 1. Chọn tab "Bình luận" | Hiển thị danh sách với đầy đủ thông tin: avatar, tên người dùng, rank, thời gian, nội dung, hình ảnh (nếu có), số lượng like/dislike/phản hồi, phản hồi (nếu có) | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BL-03** | Sắp xếp theo mới nhất | 1. Chọn tab "Bình luận"<br>2. Chọn sắp xếp "Mới nhất" | Danh sách được sắp xếp theo thời gian đăng mới nhất trước | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BL-04** | Sắp xếp theo cũ nhất | 1. Chọn tab "Bình luận"<br>2. Chọn sắp xếp "Cũ nhất" | Danh sách được sắp xếp theo thời gian đăng cũ nhất trước | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BL-05** | Sắp xếp theo nhiều like nhất | 1. Chọn tab "Bình luận"<br>2. Chọn sắp xếp "Nhiều like nhất" | Danh sách được sắp xếp theo số lượng like giảm dần | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BL-06** | Sắp xếp theo nhiều trả lời nhất | 1. Chọn tab "Bình luận"<br>2. Chọn sắp xếp "Nhiều trả lời nhất" | Danh sách được sắp xếp theo số lượng phản hồi giảm dần | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BL-07** | Lọc theo Gần đây | 1. Chọn tab "Bình luận"<br>2. Chọn bộ lọc "Gần đây" | Chỉ hiển thị các bình luận được đăng trong 24 giờ qua | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BL-08** | Lọc theo Phổ biến | 1. Chọn tab "Bình luận"<br>2. Chọn bộ lọc "Phổ biến" | Chỉ hiển thị các bình luận có số lượng like > 5 | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BL-09** | Lọc theo Gây tranh cãi | 1. Chọn tab "Bình luận"<br>2. Chọn bộ lọc "Gây tranh cãi" | Chỉ hiển thị các bình luận có dislike > 0 | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BL-10** | Tìm kiếm theo nội dung | 1. Chọn tab "Bình luận"<br>2. Nhập từ khóa vào ô tìm kiếm | Danh sách được lọc, chỉ hiển thị bình luận có nội dung chứa từ khóa | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BL-11** | Tìm kiếm theo tên người dùng | 1. Chọn tab "Bình luận"<br>2. Nhập tên người dùng vào ô tìm kiếm | Danh sách được lọc, chỉ hiển thị bình luận của người dùng có tên chứa từ khóa | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BL-12** | Kết hợp tìm kiếm và lọc | 1. Nhập từ khóa tìm kiếm<br>2. Chọn bộ lọc và sắp xếp | Danh sách được lọc và sắp xếp theo tất cả tiêu chí, chỉ hiển thị bình luận thỏa mãn tất cả điều kiện | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BL-13** | Hiển thị phản hồi bình luận | 1. Xem bình luận có phản hồi<br>2. Kiểm tra hiển thị | Hiển thị phản hồi trong div ml-8, với đầy đủ thông tin: avatar, tên, nội dung, số lượng like/dislike | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BL-14** | Hiển thị khi không có bình luận | 1. Xem bài viết không có bình luận<br>2. Kiểm tra hiển thị | Hiển thị thông báo "Chưa có bình luận nào" hoặc danh sách trống | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BL-15** | Tìm kiếm real-time | 1. Chọn tab "Bình luận"<br>2. Nhập từ khóa vào ô tìm kiếm | Danh sách được lọc ngay khi nhập, không cần nhấn Enter | | Pass | 11/15/2015 | |
| **FUNC-HTDS-BL-16** | Cập nhật số lượng bình luận | 1. Xem danh sách bình luận<br>2. Có bình luận mới | Số lượng bình luận được cập nhật real-time, bình luận mới xuất hiện trong danh sách | | Pass | 11/15/2015 | |

---

### Function: Hiển thị số lượng like

#### Check GUI: Hiển thị số lượng like

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-HT-SLL-01** | Kiểm tra badge số lượng like | 1. Xem chi tiết bài viết<br>2. Kiểm tra badge | Hiển thị Badge với số lượng like, có thể click để xem danh sách, bg-pink-100 text-pink-800 cursor-pointer | | Pass | 11/15/2015 | |
| **GUI-HT-SLL-02** | Kiểm tra nút Like | 1. Xem chi tiết bài viết<br>2. Kiểm tra nút | Hiển thị nút "Like" hoặc "Unlike" với icon Heart, variant outline hoặc default tùy trạng thái, fill-red-500 nếu đã like | | Pass | 11/15/2015 | |
| **GUI-HT-SLL-03** | Kiểm tra icon Heart | 1. Xem chi tiết bài viết<br>2. Kiểm tra icon | Hiển thị icon Heart h-4 w-4, fill-current nếu đã like | | Pass | 11/15/2015 | |
| **GUI-HT-SLL-04** | Kiểm tra tab Người thích | 1. Xem chi tiết bài viết<br>2. Kiểm tra tab | Hiển thị tab "Người thích" trong TabsList, có thể chọn để xem danh sách | | Pass | 11/15/2015 | |
| **GUI-HT-SLL-05** | Kiểm tra modal danh sách người like | 1. Click vào badge số lượng like<br>2. Kiểm tra modal | Hiển thị modal với DialogTitle "Danh sách người đã like", DialogDescription, danh sách người dùng | | Pass | 11/15/2015 | |
| **GUI-HT-SLL-06** | Kiểm tra avatar người like | 1. Xem modal danh sách người like<br>2. Kiểm tra avatar | Hiển thị Avatar h-6 w-6 với hình ảnh hoặc fallback | | Pass | 11/15/2015 | |
| **GUI-HT-SLL-07** | Kiểm tra tên người like | 1. Xem modal danh sách người like<br>2. Kiểm tra tên | Hiển thị tên người dùng với font-medium | | Pass | 11/15/2015 | |
| **GUI-HT-SLL-08** | Kiểm tra thời gian like | 1. Xem modal danh sách người like<br>2. Kiểm tra thời gian | Hiển thị thời gian like với text-xs text-muted-foreground, format "vừa xong" hoặc ngày giờ | | Pass | 11/15/2015 | |
| **GUI-HT-SLL-09** | Kiểm tra nút Đóng modal | 1. Mở modal danh sách người like<br>2. Kiểm tra nút | Hiển thị nút "Đóng" trong DialogFooter | | Pass | 11/15/2015 | |

---

### Check FUNC: Hiển thị số lượng like

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-HT-SLL-01** | Hiển thị số lượng like | 1. Xem chi tiết bài viết | Hiển thị số lượng like chính xác, cập nhật real-time khi có thay đổi | | Pass | 11/15/2015 | |
| **FUNC-HT-SLL-02** | Like bài viết | 1. Xem chi tiết bài viết<br>2. Nhấn nút "Like" | Bài viết được like, số lượng like tăng, nút chuyển thành "Unlike", icon Heart fill-red-500, người dùng được thêm vào danh sách người like, hiển thị toast "Đã thích bài viết" | | Pass | 11/15/2015 | |
| **FUNC-HT-SLL-03** | Unlike bài viết | 1. Xem chi tiết bài viết đã like<br>2. Nhấn nút "Unlike" | Bài viết được unlike, số lượng like giảm, nút chuyển thành "Like", icon Heart không fill, người dùng được xóa khỏi danh sách người like | | Pass | 11/15/2015 | |
| **FUNC-HT-SLL-04** | Xem danh sách người like | 1. Click vào badge số lượng like<br>2. Xem danh sách | Mở modal hiển thị danh sách đầy đủ người đã like với avatar, tên, rank, thời gian like | | Pass | 11/15/2015 | |
| **FUNC-HT-SLL-05** | Chặn spam like | 1. Like bài viết nhiều lần liên tiếp<br>2. Kiểm tra hệ thống | Hệ thống chặn spam like, mỗi user chỉ được like 1 lần cho mỗi bài viết, không cho phép like lại nếu đã like | | Pass | 11/15/2015 | |
| **FUNC-HT-SLL-06** | Chặn bom like | 1. Nhiều user like trong thời gian ngắn<br>2. Kiểm tra hệ thống | Hệ thống phát hiện và chặn hành vi bom like, có thể giới hạn số lượng like trong khoảng thời gian nhất định | | Pass | 11/15/2015 | |
| **FUNC-HT-SLL-07** | Cập nhật số lượng real-time | 1. Xem chi tiết bài viết<br>2. Có người khác like | Số lượng like được cập nhật real-time, không cần refresh trang | | Pass | 11/15/2015 | |
| **FUNC-HT-SLL-08** | Đóng modal danh sách | 1. Mở modal danh sách người like<br>2. Nhấn nút "Đóng" hoặc click overlay | Modal đóng, quay lại trang chi tiết | | Pass | 11/15/2015 | |
| **FUNC-HT-SLL-09** | Xem tab Người thích | 1. Chọn tab "Người thích"<br>2. Xem danh sách | Hiển thị danh sách người đã like với CardTitle "Người thích bài viết", CardDescription số lượng, danh sách với avatar, tên, rank, nút "Xem trang cá nhân" | | Pass | 11/15/2015 | |

---

### Function: Tạo bình luận

#### Check GUI: Tạo bình luận

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-TBL-01** | Kiểm tra form bình luận | 1. Xem tab "Bình luận"<br>2. Kiểm tra form | Hiển thị Card với CardTitle "Viết bình luận", CardContent chứa form | | Pass | 11/15/2015 | |
| **GUI-TBL-02** | Kiểm tra avatar người dùng | 1. Xem form bình luận<br>2. Kiểm tra avatar | Hiển thị avatar của người dùng hiện tại (nếu có) | | Pass | 11/15/2015 | |
| **GUI-TBL-03** | Kiểm tra ô nhập bình luận | 1. Xem form bình luận<br>2. Kiểm tra ô nhập | Hiển thị Label "Nội dung bình luận", Textarea với placeholder "Viết bình luận của bạn...", rows 4, required | | Pass | 11/15/2015 | |
| **GUI-TBL-04** | Kiểm tra upload hình ảnh | 1. Xem form bình luận<br>2. Kiểm tra upload | Hiển thị Label "Hình ảnh (tối đa 5 ảnh)", Input type="file" accept="image/*" multiple, nút "Chọn ảnh" với icon Image | | Pass | 11/15/2015 | |
| **GUI-TBL-05** | Kiểm tra preview hình ảnh | 1. Upload hình ảnh<br>2. Kiểm tra preview | Hiển thị preview hình ảnh w-20 h-20 object-cover rounded-lg với nút xóa absolute -top-2 -right-2 | | Pass | 11/15/2015 | |
| **GUI-TBL-06** | Kiểm tra nút Gửi bình luận | 1. Xem form bình luận<br>2. Kiểm tra nút | Hiển thị nút "Gửi bình luận" với icon Send h-4 w-4, variant default | | Pass | 11/15/2015 | |

---

### Check FUNC: Tạo bình luận

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TBL-01** | Tạo bình luận thành công | 1. Xem tab "Bình luận"<br>2. Nhập nội dung bình luận<br>3. Nhấn "Gửi bình luận" | Bình luận được tạo thành công, hiển thị trong danh sách, số lượng bình luận tăng, form được reset, hiển thị toast "Đã thêm bình luận" | | Pass | 11/15/2015 | |
| **FUNC-TBL-02** | Tạo bình luận thiếu nội dung | 1. Xem tab "Bình luận"<br>2. Để trống nội dung<br>3. Nhấn "Gửi bình luận" | Hiển thị toast lỗi "Vui lòng nhập nội dung bình luận", không gửi bình luận | | Pass | 11/15/2015 | |
| **FUNC-TBL-03** | Upload hình ảnh đính kèm | 1. Xem form bình luận<br>2. Chọn hình ảnh để upload | Hình ảnh được upload, hiển thị preview, có thể xóa từng ảnh, tối đa 5 ảnh | | Pass | 11/15/2015 | |
| **FUNC-TBL-04** | Tạo bình luận với hình ảnh | 1. Nhập nội dung bình luận<br>2. Upload hình ảnh<br>3. Gửi bình luận | Bình luận được tạo với hình ảnh đính kèm, hiển thị trong danh sách với hình ảnh | | Pass | 11/15/2015 | |
| **FUNC-TBL-05** | Xóa hình ảnh đã upload | 1. Upload hình ảnh<br>2. Nhấn nút xóa hình ảnh | Hình ảnh được xóa khỏi preview, có thể upload lại | | Pass | 11/15/2015 | |
| **FUNC-TBL-06** | Chặn spam comment | 1. Gửi nhiều bình luận liên tiếp trong thời gian ngắn<br>2. Kiểm tra hệ thống | Hệ thống chặn spam comment, giới hạn số lần bình luận trong khoảng thời gian nhất định, hiển thị thông báo nếu vượt quá giới hạn | | Pass | 11/15/2015 | |
| **FUNC-TBL-07** | Chặn bom comment | 1. Nhiều user bình luận cùng lúc<br>2. Kiểm tra hệ thống | Hệ thống phát hiện và chặn hành vi bom comment, có thể giới hạn số lượng bình luận trong khoảng thời gian nhất định | | Pass | 11/15/2015 | |
| **FUNC-TBL-08** | Tạo bình luận với nội dung dài | 1. Nhập nội dung bình luận rất dài<br>2. Gửi bình luận | Bình luận được tạo thành công, nội dung được hiển thị đầy đủ hoặc có "Xem thêm" | | Pass | 11/15/2015 | |

---

### Function: Xóa bình luận

#### Check GUI: Xóa bình luận

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XBL-01** | Kiểm tra nút Xóa bình luận | 1. Xem bình luận của mình<br>2. Kiểm tra nút | Hiển thị nút với icon Trash2 h-4 w-4, variant ghost size sm, chỉ hiển thị cho bình luận của mình | | Pass | 11/15/2015 | |
| **GUI-XBL-02** | Kiểm tra modal xác nhận | 1. Nhấn nút "Xóa"<br>2. Kiểm tra modal | Hiển thị modal với DialogTitle "Xác nhận xóa bình luận", DialogDescription "Bạn có chắc chắn muốn xóa bình luận này?", Card hiển thị thông tin bình luận | | Pass | 11/15/2015 | |
| **GUI-XBL-03** | Kiểm tra thông tin bình luận trong modal | 1. Mở modal xác nhận<br>2. Kiểm tra thông tin | Hiển thị nội dung bình luận, thời gian đăng, số lượng like/phản hồi | | Pass | 11/15/2015 | |
| **GUI-XBL-04** | Kiểm tra nút Xác nhận xóa | 1. Mở modal xác nhận<br>2. Kiểm tra nút | Hiển thị nút "Xác nhận xóa" variant destructive | | Pass | 11/15/2015 | |
| **GUI-XBL-05** | Kiểm tra nút Hủy trong modal | 1. Mở modal xác nhận<br>2. Kiểm tra nút | Hiển thị nút "Hủy" variant outline | | Pass | 11/15/2015 | |

---

### Check FUNC: Xóa bình luận

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XBL-01** | Xóa bình luận | 1. Xem bình luận của mình<br>2. Nhấn nút "Xóa"<br>3. Xác nhận xóa | Hiển thị modal xác nhận với thông tin bình luận, sau khi xác nhận, bình luận được xóa, hiển thị toast "Đã xóa bình luận", bình luận biến mất khỏi danh sách, số lượng bình luận giảm | | Pass | 11/15/2015 | |
| **FUNC-XBL-02** | Hủy xóa bình luận | 1. Nhấn nút "Xóa"<br>2. Nhấn nút "Hủy" trong modal | Modal đóng, không xóa bình luận, bình luận vẫn còn | | Pass | 11/15/2015 | |
| **FUNC-XBL-03** | Xử lý dữ liệu liên quan | 1. Xóa bình luận có like và phản hồi<br>2. Kiểm tra dữ liệu | Tất cả dữ liệu liên quan được xóa: like, dislike, phản hồi, thông báo được gửi đến người tương tác | | Pass | 11/15/2015 | |
| **FUNC-XBL-04** | Xóa bình luận không phải của mình | 1. Xem bình luận của người khác<br>2. Kiểm tra nút xóa | Nút "Xóa" không hiển thị, không thể xóa bình luận của người khác | | Pass | 11/15/2015 | |
| **FUNC-XBL-05** | Đóng modal bằng click overlay | 1. Mở modal xác nhận<br>2. Click vào overlay | Modal đóng, không xóa bình luận | | Pass | 11/15/2015 | |

---

### Function: Chỉnh sửa bình luận

#### Check GUI: Chỉnh sửa bình luận

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CSBL-01** | Kiểm tra nút Chỉnh sửa | 1. Xem bình luận của mình<br>2. Kiểm tra nút | Hiển thị nút với icon Edit h-4 w-4, variant ghost size sm, chỉ hiển thị cho bình luận của mình | | Pass | 11/15/2015 | |
| **GUI-CSBL-02** | Kiểm tra form chỉnh sửa | 1. Nhấn nút "Chỉnh sửa"<br>2. Kiểm tra form | Hiển thị Textarea với nội dung hiện tại, có thể chỉnh sửa, rows 3 | | Pass | 11/15/2015 | |
| **GUI-CSBL-03** | Kiểm tra nút Lưu | 1. Mở form chỉnh sửa<br>2. Kiểm tra nút | Hiển thị nút "Lưu" với icon CheckCircle h-4 w-4, variant default size sm | | Pass | 11/15/2015 | |
| **GUI-CSBL-04** | Kiểm tra nút Hủy | 1. Mở form chỉnh sửa<br>2. Kiểm tra nút | Hiển thị nút "Hủy" với icon XCircle h-4 w-4, variant outline size sm | | Pass | 11/15/2015 | |
| **GUI-CSBL-05** | Kiểm tra badge Đã chỉnh sửa | 1. Xem bình luận đã chỉnh sửa<br>2. Kiểm tra badge | Hiển thị text "Đã chỉnh sửa" với text-sm text-muted-foreground, sau thời gian đăng | | Pass | 11/15/2015 | |

---

### Check FUNC: Chỉnh sửa bình luận

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CSBL-01** | Mở form chỉnh sửa | 1. Xem bình luận của mình<br>2. Nhấn nút "Chỉnh sửa" | Form chỉnh sửa được hiển thị với nội dung hiện tại đã điền sẵn, có thể chỉnh sửa | | Pass | 11/15/2015 | |
| **FUNC-CSBL-02** | Chỉnh sửa bình luận thành công | 1. Mở form chỉnh sửa<br>2. Sửa nội dung<br>3. Nhấn "Lưu" | Bình luận được cập nhật, hiển thị toast "Đã cập nhật bình luận", form chỉnh sửa đóng, nội dung mới được hiển thị, badge "Đã chỉnh sửa" xuất hiện, lịch sử chỉnh sửa được lưu | | Pass | 11/15/2015 | |
| **FUNC-CSBL-03** | Hủy chỉnh sửa | 1. Mở form chỉnh sửa<br>2. Sửa nội dung<br>3. Nhấn "Hủy" | Form chỉnh sửa đóng, nội dung không thay đổi, không lưu các chỉnh sửa | | Pass | 11/15/2015 | |
| **FUNC-CSBL-04** | Chỉnh sửa với nội dung trống | 1. Mở form chỉnh sửa<br>2. Xóa hết nội dung<br>3. Nhấn "Lưu" | Hiển thị toast lỗi "Vui lòng nhập nội dung", không cập nhật bình luận | | Pass | 11/15/2015 | |
| **FUNC-CSBL-05** | Lưu lịch sử chỉnh sửa | 1. Chỉnh sửa bình luận<br>2. Lưu thay đổi<br>3. Kiểm tra lịch sử | Lịch sử chỉnh sửa được lưu với thời gian, nội dung thay đổi, có thể xem timeline | | Pass | 11/15/2015 | |
| **FUNC-CSBL-06** | Thông báo cho người tương tác | 1. Chỉnh sửa bình luận có người like/phản hồi<br>2. Lưu thay đổi<br>3. Kiểm tra thông báo | Thông báo được gửi đến người tương tác về việc cập nhật bình luận | | Pass | 11/15/2015 | |
| **FUNC-CSBL-07** | Chỉnh sửa bình luận không phải của mình | 1. Xem bình luận của người khác<br>2. Kiểm tra nút chỉnh sửa | Nút "Chỉnh sửa" không hiển thị, không thể chỉnh sửa bình luận của người khác | | Pass | 11/15/2015 | |
| **FUNC-CSBL-08** | Thêm hình ảnh khi chỉnh sửa | 1. Mở form chỉnh sửa<br>2. Thêm hình ảnh mới | Hình ảnh mới được thêm vào, hiển thị preview, có thể xóa | | Pass | 11/15/2015 | |
| **FUNC-CSBL-09** | Xóa hình ảnh khi chỉnh sửa | 1. Mở form chỉnh sửa<br>2. Xóa hình ảnh hiện tại | Hình ảnh được xóa khỏi bình luận, preview được cập nhật | | Pass | 11/15/2015 | |

---

### Check VALIDATION: Tương tác bài viết

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **VALID-TTBV-01** | Tạo bình luận với nội dung quá dài | 1. Nhập nội dung bình luận rất dài (>5000 ký tự)<br>2. Gửi bình luận | Hiển thị cảnh báo hoặc tự động cắt nội dung, không cho phép gửi nếu vượt quá giới hạn | | Pass | 11/15/2015 | |
| **VALID-TTBV-02** | Upload hình ảnh không đúng định dạng | 1. Chọn file không phải hình ảnh<br>2. Upload | Hiển thị thông báo lỗi "File không đúng định dạng", không upload | | Pass | 11/15/2015 | |
| **VALID-TTBV-03** | Upload hình ảnh quá lớn | 1. Chọn hình ảnh > 5MB<br>2. Upload | Hiển thị thông báo lỗi "File quá lớn", không upload | | Pass | 11/15/2015 | |
| **VALID-TTBV-04** | Upload quá nhiều hình ảnh | 1. Upload > 5 hình ảnh<br>2. Kiểm tra | Hệ thống chỉ cho phép tối đa 5 hình ảnh, hiển thị cảnh báo nếu vượt quá | | Pass | 11/15/2015 | |
| **VALID-TTBV-05** | Like nhiều lần cùng một bài viết | 1. Like bài viết<br>2. Thử like lại | Hệ thống chặn, không cho phép like lại, hiển thị thông báo "Bạn đã like bài viết này rồi" | | Pass | 11/15/2015 | |
| **VALID-TTBV-06** | Gửi bình luận spam | 1. Gửi nhiều bình luận giống nhau liên tiếp<br>2. Kiểm tra hệ thống | Hệ thống chặn spam, giới hạn số lần bình luận trong khoảng thời gian, hiển thị thông báo "Bạn đã bình luận quá nhiều, vui lòng đợi" | | Pass | 11/15/2015 | |
| **VALID-TTBV-07** | Tìm kiếm với từ khóa đặc biệt | 1. Nhập từ khóa có ký tự đặc biệt<br>2. Tìm kiếm | Hệ thống xử lý an toàn, không gây lỗi, lọc kết quả chính xác | | Pass | 11/15/2015 | |
| **VALID-TTBV-08** | Chỉnh sửa bình luận với nội dung trống | 1. Mở form chỉnh sửa<br>2. Xóa hết nội dung<br>3. Lưu | Hiển thị thông báo lỗi "Nội dung bình luận không được để trống", không lưu | | Pass | 11/15/2015 | |

