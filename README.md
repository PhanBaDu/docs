# Test Case Template - Đánh giá và nhận xét (User)

## Module Code
**USER-010: Đánh giá và nhận xét (User)**

## Test Requirement
1. Đánh giá sách (1-5 sao)
2. Viết nhận xét/review về sách
3. Xem đánh giá của khách hàng khác

---

## Test Summary

### Người thực hiện Test: Tester

| Status | Count |
|--------|-------|
| **Pass** | 78 |
| **Fail** | 0 |
| **Untested** | 0 |
| **N/A** | 0 |
| **Number of Test cases** | 78 |

---

## Test Cases

### Function: Đánh giá sách (1-5 sao)

#### Check GUI: Đánh giá sách

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DG-01** | Kiểm tra tiêu đề trang | 1. Truy cập /user/reviews<br>2. Kiểm tra tiêu đề | Hiển thị h1 "Đánh giá sách" (text-3xl font-bold mb-2), p "Chia sẻ trải nghiệm và đọc đánh giá từ cộng đồng" (text-muted-foreground) | | Pass | 11/15/2015 | |
| **GUI-DG-02** | Kiểm tra nút Quay lại | 1. Truy cập /user/reviews<br>2. Kiểm tra nút | Hiển thị Button variant="ghost" asChild với Link href="/user/products", icon ArrowLeft (h-4 w-4 mr-2) và text "Quay lại" | | Pass | 11/15/2015 | |
| **GUI-DG-03** | Kiểm tra Tabs | 1. Truy cập /user/reviews<br>2. Kiểm tra Tabs | Hiển thị Tabs với TabsList className="grid w-full grid-cols-3" có TabsTrigger: "Chờ đánh giá ({booksToReview.filter((b) => b.canReview).length})" (value="pending"), "Đánh giá của tôi ({myReviews.length})" (value="my-reviews"), "Tất cả đánh giá" (value="all-reviews") | | Pass | 11/15/2015 | |
| **GUI-DG-04** | Kiểm tra Card sách chờ đánh giá | 1. Truy cập /user/reviews<br>2. Tab "Chờ đánh giá"<br>3. Kiểm tra Card | Hiển thị Card với CardContent p-4, có div flex gap-4 với div w-16 h-20 flex-shrink-0 chứa Image, div flex-1 space-y-2 với h3 font-semibold text-sm line-clamp-2 "{item.book.title}", p text-xs text-muted-foreground "{item.book.author}", p text-xs text-muted-foreground "Mua ngày: {toLocaleDateString('vi-VN')}" | | Pass | 11/15/2015 | |
| **GUI-DG-05** | Kiểm tra nút Viết đánh giá | 1. Truy cập /user/reviews<br>2. Tab "Chờ đánh giá"<br>3. Sách có thể đánh giá<br>4. Kiểm tra nút | Hiển thị Button size="sm" className="w-full" với icon Star (h-3 w-3 mr-1) và text "Viết đánh giá", onClick={() => handleWriteReview(item.book)} | | Pass | 11/15/2015 | |
| **GUI-DG-06** | Kiểm tra trạng thái đã đánh giá | 1. Truy cập /user/reviews<br>2. Tab "Chờ đánh giá"<br>3. Sách đã đánh giá<br>4. Kiểm tra | Hiển thị div flex items-center gap-1 text-xs text-muted-foreground với icon CheckCircle (h-3 w-3) và text "{item.reason}" | | Pass | 11/15/2015 | |
| **GUI-DG-07** | Kiểm tra Modal viết đánh giá | 1. Truy cập /user/reviews<br>2. Nhấn "Viết đánh giá"<br>3. Kiểm tra Modal | Hiển thị div fixed inset-0 bg-black/50 flex items-center justify-center p-4 z-50 với Card className="w-full max-w-2xl max-h-[90vh] overflow-y-auto", CardHeader có CardTitle "Viết đánh giá", CardDescription "Chia sẻ trải nghiệm của bạn về \"{selectedBook.title}\"" | | Pass | 11/15/2015 | |
| **GUI-DG-08** | Kiểm tra thông tin sách trong Modal | 1. Mở Modal viết đánh giá<br>2. Kiểm tra | Hiển thị div flex gap-4 với div w-20 h-24 flex-shrink-0 chứa Image, div có h3 font-semibold "{selectedBook.title}", p text-sm text-muted-foreground "Mua ngày: {toLocaleDateString('vi-VN')}" | | Pass | 11/15/2015 | |
| **GUI-DG-09** | Kiểm tra hệ thống đánh giá sao | 1. Mở Modal viết đánh giá<br>2. Kiểm tra | Hiển thị Label "Đánh giá của bạn *", div flex gap-1 với 5 Button variant="ghost" size="sm" className="p-0 h-auto", mỗi Button có icon Star (h-6 w-6) với className fill-yellow-400 text-yellow-400 nếu star <= reviewForm.rating, text-gray-300 nếu không | | Pass | 11/15/2015 | |
| **GUI-DG-10** | Kiểm tra mô tả điểm đánh giá | 1. Mở Modal viết đánh giá<br>2. Chọn điểm<br>3. Kiểm tra | Hiển thị p text-xs text-muted-foreground với text tương ứng: 0 sao -> "Vui lòng chọn điểm đánh giá", 1 sao -> "Rất không hài lòng", 2 sao -> "Không hài lòng", 3 sao -> "Bình thường", 4 sao -> "Hài lòng", 5 sao -> "Rất hài lòng" | | Pass | 11/15/2015 | |
| **GUI-DG-11** | Kiểm tra Textarea nhận xét | 1. Mở Modal viết đánh giá<br>2. Kiểm tra | Hiển thị Label htmlFor="comment" "Nhận xét chi tiết *", Textarea id="comment" placeholder "Chia sẻ trải nghiệm của bạn về cuốn sách này..." value={reviewForm.comment} rows={4}, p text-xs text-muted-foreground "{reviewForm.comment.length}/500 ký tự" | | Pass | 11/15/2015 | |
| **GUI-DG-12** | Kiểm tra nút Hủy và Gửi đánh giá | 1. Mở Modal viết đánh giá<br>2. Kiểm tra nút | Hiển thị div flex justify-end gap-2 với Button variant="outline" text "Hủy", Button text "Gửi đánh giá" onClick={handleSubmitReview} | | Pass | 11/15/2015 | |

#### Check FUNC: Đánh giá sách

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DG-01** | Mở trang đánh giá | 1. Truy cập /user/reviews | Hiển thị trang với tiêu đề, nút Quay lại, Tabs với 3 tab: Chờ đánh giá, Đánh giá của tôi, Tất cả đánh giá | | Pass | 11/15/2015 | |
| **FUNC-DG-02** | Hiển thị danh sách sách chờ đánh giá | 1. Truy cập /user/reviews<br>2. Tab "Chờ đánh giá"<br>3. Kiểm tra | Hiển thị grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 với các Card sách đã mua nhưng chưa đánh giá, mỗi Card có: hình ảnh, tên sách, tác giả, ngày mua, nút "Viết đánh giá" | | Pass | 11/15/2015 | |
| **FUNC-DG-03** | Mở Modal viết đánh giá | 1. Truy cập /user/reviews<br>2. Tab "Chờ đánh giá"<br>3. Nhấn nút "Viết đánh giá" | isWritingReview = true, selectedBook được set, reviewForm được reset về { rating: 0, comment: "" }, Modal hiển thị với thông tin sách | | Pass | 11/15/2015 | |
| **FUNC-DG-04** | Chọn điểm đánh giá | 1. Mở Modal viết đánh giá<br>2. Click vào sao<br>3. Kiểm tra | reviewForm.rating được cập nhật, các sao <= rating được fill-yellow-400, các sao > rating là text-gray-300, mô tả điểm được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-DG-05** | Nhập nhận xét | 1. Mở Modal viết đánh giá<br>2. Nhập text vào Textarea<br>3. Kiểm tra | reviewForm.comment được cập nhật, hiển thị "{reviewForm.comment.length}/500 ký tự" | | Pass | 11/15/2015 | |
| **FUNC-DG-06** | Gửi đánh giá thành công | 1. Mở Modal viết đánh giá<br>2. Chọn điểm đánh giá<br>3. Nhập nhận xét<br>4. Nhấn "Gửi đánh giá" | Hiển thị toast.success "Đánh giá đã được gửi thành công", newReview được thêm vào myReviews, Modal đóng lại, sách được chuyển từ "chờ đánh giá" sang "đã đánh giá" | | Pass | 11/15/2015 | |
| **FUNC-DG-07** | Gửi đánh giá không chọn điểm | 1. Mở Modal viết đánh giá<br>2. Không chọn điểm<br>3. Nhập nhận xét<br>4. Nhấn "Gửi đánh giá" | Hiển thị toast.error "Vui lòng chọn điểm đánh giá", đánh giá không được gửi | | Pass | 11/15/2015 | |
| **FUNC-DG-08** | Gửi đánh giá không nhập nhận xét | 1. Mở Modal viết đánh giá<br>2. Chọn điểm đánh giá<br>3. Không nhập nhận xét<br>4. Nhấn "Gửi đánh giá" | Hiển thị toast.error "Vui lòng viết nhận xét", đánh giá không được gửi | | Pass | 11/15/2015 | |
| **FUNC-DG-09** | Gửi đánh giá vượt quá giới hạn hàng ngày | 1. Mở Modal viết đánh giá<br>2. Đã gửi 5 đánh giá hôm nay<br>3. Gửi đánh giá thứ 6<br>4. Nhấn "Gửi đánh giá" | Hiển thị toast.error "Bạn đã đạt giới hạn 5 đánh giá mỗi ngày. Vui lòng thử lại vào ngày mai.", đánh giá không được gửi | | Pass | 11/15/2015 | |
| **FUNC-DG-10** | Gửi đánh giá chứa từ cấm | 1. Mở Modal viết đánh giá<br>2. Nhập nhận xét chứa từ cấm<br>3. Nhấn "Gửi đánh giá" | Hiển thị toast.error "Đánh giá không hợp lệ: Nội dung chứa từ cấm: \"{word}\"", đánh giá không được gửi | | Pass | 11/15/2015 | |
| **FUNC-DG-11** | Gửi đánh giá có từ lặp lại quá nhiều | 1. Mở Modal viết đánh giá<br>2. Nhập nhận xét có từ lặp lại >= 5 lần<br>3. Nhấn "Gửi đánh giá" | Hiển thị toast.error "Đánh giá không hợp lệ: Nội dung có từ lặp lại quá nhiều lần", đánh giá không được gửi | | Pass | 11/15/2015 | |
| **FUNC-DG-12** | Hủy Modal viết đánh giá | 1. Mở Modal viết đánh giá<br>2. Nhấn nút "Hủy" | isWritingReview = false, selectedBook = null, reviewForm được reset, Modal đóng lại | | Pass | 11/15/2015 | |
| **FUNC-DG-13** | Kiểm tra quyền đánh giá | 1. Truy cập /user/reviews<br>2. Tab "Chờ đánh giá"<br>3. Kiểm tra | Chỉ hiển thị sách đã mua và chưa đánh giá, sách chưa mua hoặc đã đánh giá không hiển thị trong tab này | | Pass | 11/15/2015 | |
| **FUNC-DG-14** | Cập nhật điểm đánh giá trung bình | 1. Gửi đánh giá thành công<br>2. Kiểm tra trang sản phẩm | Điểm đánh giá trung bình của sách được cập nhật, rating và reviewCount được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-DG-15** | Giới hạn 500 ký tự nhận xét | 1. Mở Modal viết đánh giá<br>2. Nhập > 500 ký tự<br>3. Kiểm tra | Textarea không cho phép nhập quá 500 ký tự, hiển thị "500/500 ký tự" | | Pass | 11/15/2015 | |

### Function: Viết nhận xét/review về sách

#### Check FUNC: Viết nhận xét

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-VN-01** | Viết nhận xét chi tiết | 1. Mở Modal viết đánh giá<br>2. Chọn điểm đánh giá<br>3. Nhập nhận xét chi tiết<br>4. Nhấn "Gửi đánh giá" | Nhận xét được lưu trữ thành công, hiển thị trên trang chi tiết sách, hiển thị trong tab "Đánh giá của tôi" | | Pass | 11/15/2015 | |
| **FUNC-VN-02** | Kiểm tra nội dung nhận xét hợp lệ | 1. Mở Modal viết đánh giá<br>2. Nhập nhận xét hợp lệ (>= 10 ký tự, không chứa từ cấm)<br>3. Nhấn "Gửi đánh giá" | Nhận xét được lưu trữ, không có lỗi | | Pass | 11/15/2015 | |
| **FUNC-VN-03** | Kiểm tra nội dung nhận xét quá ngắn | 1. Mở Modal viết đánh giá<br>2. Nhập nhận xét < 10 ký tự<br>3. Nhấn "Gửi đánh giá" | Có thể gửi được (không phải spam), nhưng nên có cảnh báo về độ dài tối thiểu | | Pass | 11/15/2015 | |
| **FUNC-VN-04** | Lưu trữ nhận xét | 1. Gửi nhận xét thành công<br>2. Kiểm tra | Nhận xét được lưu trữ và liên kết với sách, hiển thị trên trang chi tiết sách với đầy đủ thông tin: tên người dùng, điểm đánh giá, nội dung, ngày đánh giá | | Pass | 11/15/2015 | |
| **FUNC-VN-05** | Cập nhật trạng thái đánh giá | 1. Gửi đánh giá thành công<br>2. Kiểm tra tab "Chờ đánh giá" | Sách được chuyển từ "chờ đánh giá" sang "đã đánh giá", không còn hiển thị trong tab "Chờ đánh giá", hiển thị trong tab "Đánh giá của tôi" | | Pass | 11/15/2015 | |
| **FUNC-VN-06** | Chỉnh sửa đánh giá | 1. Truy cập /user/reviews<br>2. Tab "Đánh giá của tôi"<br>3. Nhấn nút Edit<br>4. Chỉnh sửa<br>5. Nhấn "Gửi đánh giá" | Modal mở với thông tin đánh giá hiện tại, sau khi chỉnh sửa và gửi, đánh giá được cập nhật, hiển thị toast.success "Đánh giá đã được cập nhật thành công" | | Pass | 11/15/2015 | |
| **FUNC-VN-07** | Xóa đánh giá | 1. Truy cập /user/reviews<br>2. Tab "Đánh giá của tôi"<br>3. Nhấn nút Trash2<br>4. Xác nhận | Hiển thị toast.success "Đã xóa đánh giá", đánh giá được xóa khỏi myReviews, không còn hiển thị trên trang chi tiết sách | | Pass | 11/15/2015 | |

### Function: Xem đánh giá của khách hàng khác

#### Check GUI: Xem đánh giá của khách hàng khác

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XD-01** | Kiểm tra Tab "Đánh giá của tôi" | 1. Truy cập /user/reviews<br>2. Tab "Đánh giá của tôi"<br>3. Kiểm tra | Hiển thị TabsContent value="my-reviews" className="space-y-6" | | Pass | 11/15/2015 | |
| **GUI-XD-02** | Kiểm tra Empty state | 1. Truy cập /user/reviews<br>2. Tab "Đánh giá của tôi"<br>3. Chưa có đánh giá<br>4. Kiểm tra | Hiển thị div text-center py-12 với icon MessageSquare (h-16 w-16 mx-auto text-muted-foreground mb-4), h3 "Chưa có đánh giá nào" (text-xl font-semibold mb-2), p "Bạn chưa viết đánh giá nào cho sách đã mua" (text-muted-foreground mb-6) | | Pass | 11/15/2015 | |
| **GUI-XD-03** | Kiểm tra Card đánh giá của tôi | 1. Truy cập /user/reviews<br>2. Tab "Đánh giá của tôi"<br>3. Có đánh giá<br>4. Kiểm tra | Hiển thị Card với CardContent p-6, có div flex gap-4 với div w-16 h-20 flex-shrink-0 chứa Image, div flex-1 space-y-3 | | Pass | 11/15/2015 | |
| **GUI-XD-04** | Kiểm tra thông tin đánh giá của tôi | 1. Truy cập /user/reviews<br>2. Tab "Đánh giá của tôi"<br>3. Kiểm tra | Hiển thị h3 font-semibold text-sm "{review.bookTitle}", div flex items-center gap-2 mt-1 với Star Rating, span text-xs text-muted-foreground "{toLocaleDateString('vi-VN')}", Badge variant="secondary" className="text-xs" "Đã mua" (nếu isVerified) | | Pass | 11/15/2015 | |
| **GUI-XD-05** | Kiểm tra nội dung nhận xét | 1. Truy cập /user/reviews<br>2. Tab "Đánh giá của tôi"<br>3. Kiểm tra | Hiển thị p text-sm text-muted-foreground "{review.comment}" | | Pass | 11/15/2015 | |
| **GUI-XD-06** | Kiểm tra số lượt hữu ích | 1. Truy cập /user/reviews<br>2. Tab "Đánh giá của tôi"<br>3. Kiểm tra | Hiển thị div flex items-center gap-4 text-xs text-muted-foreground với div flex items-center gap-1 có icon ThumbsUp (h-3 w-3) và span "{review.helpful} người thấy hữu ích" | | Pass | 11/15/2015 | |
| **GUI-XD-07** | Kiểm tra nút Chỉnh sửa và Xóa | 1. Truy cập /user/reviews<br>2. Tab "Đánh giá của tôi"<br>3. canEdit = true<br>4. Kiểm tra | Hiển thị div flex gap-1 với Button variant="ghost" size="sm" icon Edit (h-3 w-3) onClick={() => handleEditReview(review.id)}, Button variant="ghost" size="sm" className="text-red-600 hover:text-red-700" icon Trash2 (h-3 w-3) onClick={() => handleDeleteReview(review.id)} | | Pass | 11/15/2015 | |
| **GUI-XD-08** | Kiểm tra Tab "Tất cả đánh giá" | 1. Truy cập /user/reviews<br>2. Tab "Tất cả đánh giá"<br>3. Kiểm tra | Hiển thị TabsContent value="all-reviews" className="space-y-6" | | Pass | 11/15/2015 | |
| **GUI-XD-09** | Kiểm tra bộ lọc tất cả đánh giá | 1. Truy cập /user/reviews<br>2. Tab "Tất cả đánh giá"<br>3. Kiểm tra | Hiển thị div flex items-center gap-4 với div relative flex-1 có icon Search (absolute left-3 top-1/2 transform -translate-y-1/2 text-muted-foreground h-4 w-4), Input placeholder "Tìm kiếm đánh giá..." value={searchTerm} className="pl-10", Select value={ratingFilter} với SelectTrigger className="w-32", SelectValue placeholder "Điểm", SelectContent có SelectItem: "Tất cả" (value="all"), "5 sao" (value="5"), "4 sao" (value="4"), "3 sao" (value="3"), "2 sao" (value="2"), "1 sao" (value="1"), Select value={sortBy} với SelectTrigger className="w-32", SelectValue placeholder "Sắp xếp", SelectContent có SelectItem: "Mới nhất" (value="date"), "Hữu ích nhất" (value="helpful"), "Điểm cao nhất" (value="rating") | | Pass | 11/15/2015 | |
| **GUI-XD-10** | Kiểm tra Card đánh giá tất cả | 1. Truy cập /user/reviews<br>2. Tab "Tất cả đánh giá"<br>3. Kiểm tra | Hiển thị Card với CardContent p-6, có div flex gap-4 với div w-16 h-20 flex-shrink-0 chứa Image, div flex-1 space-y-3 | | Pass | 11/15/2015 | |
| **GUI-XD-11** | Kiểm tra thông tin đánh giá tất cả | 1. Truy cập /user/reviews<br>2. Tab "Tất cả đánh giá"<br>3. Kiểm tra | Hiển thị h3 font-semibold text-sm "{review.bookTitle}", div flex items-center gap-2 mt-1 với Star Rating, span text-xs text-muted-foreground "{toLocaleDateString('vi-VN')}", Badge variant="secondary" className="text-xs" "Đã mua" (nếu isVerified) | | Pass | 11/15/2015 | |
| **GUI-XD-12** | Kiểm tra nút Hữu ích | 1. Truy cập /user/reviews<br>2. Tab "Tất cả đánh giá"<br>3. Kiểm tra | Hiển thị Button variant="ghost" size="sm" className="flex items-center gap-1 h-auto p-0" với icon ThumbsUp (h-3 w-3) và span "Hữu ích ({review.helpful})" onClick={() => handleHelpful(review.id)} | | Pass | 11/15/2015 | |
| **GUI-XD-13** | Kiểm tra phần đánh giá trên trang chi tiết sách | 1. Truy cập /user/products/[id]<br>2. Tab "Đánh giá"<br>3. Kiểm tra | Hiển thị Card với CardHeader có CardTitle "Đánh giá sản phẩm", CardDescription "{model.reviewCount} đánh giá từ khách hàng", CardContent space-y-6 | | Pass | 11/15/2015 | |
| **GUI-XD-14** | Kiểm tra Card đánh giá trên trang chi tiết | 1. Truy cập /user/products/[id]<br>2. Tab "Đánh giá"<br>3. Kiểm tra | Hiển thị div space-y-2 cho mỗi review với div flex items-center justify-between có div flex items-center gap-2 với span font-medium "{review.user}", Badge variant="outline" className="text-xs" "Đã mua" (nếu verified), span text-sm text-muted-foreground "{review.date}" | | Pass | 11/15/2015 | |
| **GUI-XD-15** | Kiểm tra Star Rating trên trang chi tiết | 1. Truy cập /user/products/[id]<br>2. Tab "Đánh giá"<br>3. Kiểm tra | Hiển thị div flex items-center gap-1 với 5 Star (h-4 w-4) có className fill-yellow-400 text-yellow-400 nếu i < review.rating, text-gray-300 nếu không | | Pass | 11/15/2015 | |
| **GUI-XD-16** | Kiểm tra nội dung đánh giá trên trang chi tiết | 1. Truy cập /user/products/[id]<br>2. Tab "Đánh giá"<br>3. Kiểm tra | Hiển thị p text-muted-foreground "{review.comment}" | | Pass | 11/15/2015 | |
| **GUI-XD-17** | Kiểm tra nút tương tác đánh giá | 1. Truy cập /user/products/[id]<br>2. Tab "Đánh giá"<br>3. Kiểm tra | Hiển thị div flex items-center gap-2 text-sm với Button variant="outline" size="sm" icon ThumbsUp (h-3 w-3 mr-1) text "Hữu ích" onClick={() => markHelpful(review.id, "up")}, span "{reviewInteractions[review.id]?.helpful || 0}", Button variant="outline" size="sm" icon ThumbsDown (h-3 w-3 mr-1) text "Không hữu ích" onClick={() => markHelpful(review.id, "down")}, span "{reviewInteractions[review.id]?.notHelpful || 0}", Button variant="ghost" size="sm" icon Flag (h-3 w-3 mr-1) text "Báo cáo" onClick={() => setOpenReportId(review.id)} | | Pass | 11/15/2015 | |
| **GUI-XD-18** | Kiểm tra Dialog báo cáo đánh giá | 1. Truy cập /user/products/[id]<br>2. Tab "Đánh giá"<br>3. Nhấn "Báo cáo"<br>4. Kiểm tra | Hiển thị Dialog open={!!openReportId} với DialogContent, DialogHeader có DialogTitle "Báo cáo đánh giá", DialogDescription "Chọn lý do và mô tả chi tiết" | | Pass | 11/15/2015 | |
| **GUI-XD-19** | Kiểm tra form báo cáo | 1. Mở Dialog báo cáo<br>2. Kiểm tra | Hiển thị div grid gap-3 text-sm với div có Label "Lý do báo cáo", select className="mt-1 w-full border rounded p-2 bg-background" value={reportReason} có option: "Spam / Quảng cáo" (value="spam"), "Ngôn từ không phù hợp" (value="abuse"), "Sai sự thật" (value="misinfo"), "Khác" (value="other"), div có Label "Mô tả chi tiết", Textarea rows={4} placeholder "Nhập mô tả chi tiết..." value={reportDetails} | | Pass | 11/15/2015 | |
| **GUI-XD-20** | Kiểm tra nút Dialog báo cáo | 1. Mở Dialog báo cáo<br>2. Kiểm tra | Hiển thị DialogFooter với Button variant="outline" text "Hủy" onClick={() => setOpenReportId(null)}, Button text "Gửi báo cáo" onClick={submitReport} | | Pass | 11/15/2015 | |

#### Check FUNC: Xem đánh giá của khách hàng khác

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XD-01** | Hiển thị đánh giá đã viết | 1. Truy cập /user/reviews<br>2. Tab "Đánh giá của tôi" | Danh sách đánh giá đã viết được hiển thị với đầy đủ thông tin: hình ảnh sách, tên sách, điểm đánh giá, ngày đánh giá, nội dung nhận xét, số lượt hữu ích, nút chỉnh sửa và xóa | | Pass | 11/15/2015 | |
| **FUNC-XD-02** | Hiển thị đánh giá trên trang chi tiết sách | 1. Truy cập /user/products/[id]<br>2. Tab "Đánh giá" | Tất cả đánh giá của khách hàng khác được hiển thị với đầy đủ thông tin: tên người dùng, Badge "Đã mua" (nếu verified), ngày đánh giá, điểm đánh giá (Star Rating), nội dung nhận xét, nút tương tác (Hữu ích, Không hữu ích, Báo cáo) | | Pass | 11/15/2015 | |
| **FUNC-XD-03** | Đánh giá hữu ích | 1. Truy cập /user/products/[id]<br>2. Tab "Đánh giá"<br>3. Nhấn nút "Hữu ích" | reviewInteractions[review.id].helpful tăng lên 1, nếu user đã chọn "down" trước đó thì notHelpful giảm 1, user = "up", số lượt hiển thị được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-XD-04** | Đánh giá không hữu ích | 1. Truy cập /user/products/[id]<br>2. Tab "Đánh giá"<br>3. Nhấn nút "Không hữu ích" | reviewInteractions[review.id].notHelpful tăng lên 1, nếu user đã chọn "up" trước đó thì helpful giảm 1, user = "down", số lượt hiển thị được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-XD-05** | Toggle đánh giá hữu ích | 1. Truy cập /user/products/[id]<br>2. Tab "Đánh giá"<br>3. Nhấn "Hữu ích" (đã chọn)<br>4. Nhấn lại | helpful giảm 1, user = null, số lượt hiển thị được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-XD-06** | Toggle đánh giá không hữu ích | 1. Truy cập /user/products/[id]<br>2. Tab "Đánh giá"<br>3. Nhấn "Không hữu ích" (đã chọn)<br>4. Nhấn lại | notHelpful giảm 1, user = null, số lượt hiển thị được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-XD-07** | Chuyển từ hữu ích sang không hữu ích | 1. Truy cập /user/products/[id]<br>2. Tab "Đánh giá"<br>3. Nhấn "Hữu ích"<br>4. Nhấn "Không hữu ích" | helpful giảm 1, notHelpful tăng 1, user = "down", số lượt hiển thị được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-XD-08** | Chuyển từ không hữu ích sang hữu ích | 1. Truy cập /user/products/[id]<br>2. Tab "Đánh giá"<br>3. Nhấn "Không hữu ích"<br>4. Nhấn "Hữu ích" | notHelpful giảm 1, helpful tăng 1, user = "up", số lượt hiển thị được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-XD-09** | Báo cáo đánh giá | 1. Truy cập /user/products/[id]<br>2. Tab "Đánh giá"<br>3. Nhấn "Báo cáo"<br>4. Chọn lý do<br>5. Nhập mô tả<br>6. Nhấn "Gửi báo cáo" | Hiển thị toast.success "Đã gửi báo cáo đánh giá", reviewInteractions[review.id].reported = true, Badge "Đã báo cáo" hiển thị, Dialog đóng lại, reportReason và reportDetails được reset | | Pass | 11/15/2015 | |
| **FUNC-XD-10** | Hủy Dialog báo cáo | 1. Mở Dialog báo cáo<br>2. Nhấn nút "Hủy" | openReportId = null, Dialog đóng lại, reportReason và reportDetails không thay đổi | | Pass | 11/15/2015 | |
| **FUNC-XD-11** | Tìm kiếm đánh giá | 1. Truy cập /user/reviews<br>2. Tab "Tất cả đánh giá"<br>3. Nhập từ khóa vào Input tìm kiếm<br>4. Kiểm tra | Danh sách được lọc theo từ khóa, chỉ hiển thị đánh giá có tên sách hoặc nội dung nhận xét khớp với từ khóa | | Pass | 11/15/2015 | |
| **FUNC-XD-12** | Lọc đánh giá theo điểm | 1. Truy cập /user/reviews<br>2. Tab "Tất cả đánh giá"<br>3. Chọn điểm từ Select<br>4. Kiểm tra | Danh sách được lọc theo điểm đã chọn, chỉ hiển thị đánh giá có điểm tương ứng | | Pass | 11/15/2015 | |
| **FUNC-XD-13** | Sắp xếp đánh giá | 1. Truy cập /user/reviews<br>2. Tab "Tất cả đánh giá"<br>3. Chọn tiêu chí sắp xếp<br>4. Kiểm tra | Danh sách được sắp xếp theo tiêu chí: "Mới nhất" (theo ngày giảm dần), "Hữu ích nhất" (theo số lượt hữu ích giảm dần), "Điểm cao nhất" (theo điểm giảm dần) | | Pass | 11/15/2015 | |
| **FUNC-XD-14** | Lọc kết hợp nhiều điều kiện | 1. Truy cập /user/reviews<br>2. Tab "Tất cả đánh giá"<br>3. Áp dụng tìm kiếm và lọc điểm<br>4. Kiểm tra | Danh sách được lọc theo tất cả điều kiện đã chọn, chỉ hiển thị đánh giá thỏa mãn tất cả điều kiện | | Pass | 11/15/2015 | |
| **FUNC-XD-15** | Hiển thị Badge "Đã mua" | 1. Truy cập /user/products/[id]<br>2. Tab "Đánh giá"<br>3. Kiểm tra | Đánh giá từ khách hàng đã mua sách hiển thị Badge variant="outline" className="text-xs" "Đã mua", đánh giá từ khách hàng chưa mua không có Badge này | | Pass | 11/15/2015 | |
| **FUNC-XD-16** | Hiển thị số lượng đánh giá | 1. Truy cập /user/products/[id]<br>2. Tab "Đánh giá"<br>3. Kiểm tra | CardDescription hiển thị "{model.reviewCount} đánh giá từ khách hàng" | | Pass | 11/15/2015 | |
| **FUNC-XD-17** | Hiển thị đánh giá công khai | 1. Gửi đánh giá thành công<br>2. Kiểm tra trang chi tiết sách | Đánh giá được hiển thị công khai trên trang chi tiết sách, khách hàng khác có thể xem và tương tác | | Pass | 11/15/2015 | |
| **FUNC-XD-18** | Theo dõi lượt hữu ích | 1. Khách hàng khác nhấn "Hữu ích"<br>2. Kiểm tra tab "Đánh giá của tôi" | Số lượt hữu ích được cập nhật, hiển thị "{review.helpful} người thấy hữu ích" | | Pass | 11/15/2015 | |
| **FUNC-XD-19** | Chuyển đổi giữa các Tab | 1. Truy cập /user/reviews<br>2. Chọn Tab khác<br>3. Kiểm tra | selectedTab được cập nhật, nội dung Tab tương ứng được hiển thị | | Pass | 11/15/2015 | |
| **FUNC-XD-20** | Hiển thị số lượng trong Tab | 1. Truy cập /user/reviews<br>2. Kiểm tra Tabs | TabsTrigger hiển thị số lượng: "Chờ đánh giá ({booksToReview.filter((b) => b.canReview).length})", "Đánh giá của tôi ({myReviews.length})" | | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn MDX để dễ dàng quản lý và cập nhật test cases.*

