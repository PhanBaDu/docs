# Test Case Template - Danh sách sách yêu thích (User)

## Module Code
**USER-011: Danh sách sách yêu thích (User)**

## Test Requirement
1. Thêm sách vào danh sách yêu thích
2. Xem danh sách sách yêu thích
3. Xóa sách khỏi danh sách yêu thích

---

## Test Summary

### Người thực hiện Test: Tester

| Status | Count |
|--------|-------|
| **Pass** | 72 |
| **Fail** | 0 |
| **Untested** | 0 |
| **N/A** | 0 |
| **Number of Test cases** | 72 |

---

## Test Cases

### Function: Thêm sách vào danh sách yêu thích

#### Check GUI: Thêm sách vào yêu thích

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-TH-01** | Kiểm tra nút yêu thích trên trang chi tiết sách | 1. Truy cập /user/products/[id]<br>2. Kiểm tra nút | Hiển thị Button size="lg" variant="outline" với icon Heart className={`h-4 w-4 ${isFavorite ? "fill-red-500 text-red-500" : ""}`} onClick={toggleFavorite} | | Pass | 11/15/2015 | |
| **GUI-TH-02** | Kiểm tra trạng thái chưa yêu thích | 1. Truy cập /user/products/[id]<br>2. Sách chưa yêu thích<br>3. Kiểm tra | Icon Heart không có fill-red-500 text-red-500, chỉ có className="h-4 w-4" | | Pass | 11/15/2015 | |
| **GUI-TH-03** | Kiểm tra trạng thái đã yêu thích | 1. Truy cập /user/products/[id]<br>2. Sách đã yêu thích<br>3. Kiểm tra | Icon Heart có className="h-4 w-4 fill-red-500 text-red-500" | | Pass | 11/15/2015 | |
| **GUI-TH-04** | Kiểm tra nút yêu thích trên trang danh sách sách | 1. Truy cập /user/products<br>2. Kiểm tra nút trên Card sách | Hiển thị Button variant="ghost" size="sm" className="absolute top-2 right-2 h-8 w-8 p-0 bg-white/80 hover:bg-white" với icon Heart className={`h-4 w-4 ${isFavorite ? "fill-red-500 text-red-500" : ""}`} | | Pass | 11/15/2015 | |

#### Check FUNC: Thêm sách vào yêu thích

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TH-01** | Thêm sách vào danh sách yêu thích | 1. Truy cập /user/products/[id]<br>2. Nhấn nút Heart (chưa yêu thích)<br>3. Kiểm tra | Hiển thị toast.success "Đã thêm vào danh sách yêu thích", isFavorite = true, icon Heart có fill-red-500 text-red-500, sách được thêm vào wishlist | | Pass | 11/15/2015 | |
| **FUNC-TH-02** | Thêm sách đã có trong danh sách | 1. Truy cập /user/products/[id]<br>2. Sách đã có trong wishlist<br>3. Nhấn nút Heart<br>4. Kiểm tra | Hiển thị toast.error "Sách đã có trong danh sách yêu thích", sách không được thêm trùng lặp | | Pass | 11/15/2015 | |
| **FUNC-TH-03** | Thêm sách khi đạt giới hạn | 1. Truy cập /user/products/[id]<br>2. Wishlist đã có 200 sách<br>3. Nhấn nút Heart<br>4. Kiểm tra | Hiển thị toast.error "Danh sách yêu thích đã đạt giới hạn tối đa 200 sách. Vui lòng xóa bớt sách để thêm mới.", sách không được thêm | | Pass | 11/15/2015 | |
| **FUNC-TH-04** | Lưu trữ thông tin yêu thích | 1. Thêm sách vào yêu thích thành công<br>2. Kiểm tra | Thông tin sách được lưu trữ với: ID sách, ngày thêm (addedDate), thông tin người dùng, có thể truy xuất từ wishlist | | Pass | 11/15/2015 | |
| **FUNC-TH-05** | Cập nhật giao diện sau khi thêm | 1. Thêm sách vào yêu thích<br>2. Kiểm tra | Icon Heart chuyển từ outline sang filled (fill-red-500 text-red-500), Badge "Yêu thích" hiển thị (nếu có), counter yêu thích tăng lên | | Pass | 11/15/2015 | |
| **FUNC-TH-06** | Kiểm tra trạng thái yêu thích | 1. Truy cập /user/products/[id]<br>2. Kiểm tra | Hệ thống kiểm tra xem sách đã có trong wishlist hay chưa, hiển thị trạng thái đúng: nếu có thì icon filled, nếu không thì icon outline | | Pass | 11/15/2015 | |

### Function: Xem danh sách sách yêu thích

#### Check GUI: Xem danh sách yêu thích

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XD-01** | Kiểm tra tiêu đề trang | 1. Truy cập /user/wishlist<br>2. Kiểm tra tiêu đề | Hiển thị h1 "Danh sách yêu thích" (text-3xl font-bold mb-2), p "{books.length}/{MAX_WISHLIST_ITEMS} sách trong danh sách yêu thích của bạn" (text-muted-foreground) | | Pass | 11/15/2015 | |
| **GUI-XD-02** | Kiểm tra nút Tiếp tục mua sắm | 1. Truy cập /user/wishlist<br>2. Kiểm tra nút | Hiển thị Button variant="ghost" asChild với Link href="/user/products", icon ArrowLeft (h-4 w-4 mr-2) và text "Tiếp tục mua sắm" | | Pass | 11/15/2015 | |
| **GUI-XD-03** | Kiểm tra thông báo giới hạn | 1. Truy cập /user/wishlist<br>2. books.length >= 200<br>3. Kiểm tra | Hiển thị div mt-2 p-3 bg-orange-50 border border-orange-200 rounded-lg với p text-sm text-orange-800 "⚠️ Bạn đã đạt giới hạn tối đa 200 sách. Vui lòng xóa bớt sách để thêm mới." | | Pass | 11/15/2015 | |
| **GUI-XD-04** | Kiểm tra Empty state | 1. Truy cập /user/wishlist<br>2. books.length === 0<br>3. Kiểm tra | Hiển thị div text-center py-12 với icon Heart (h-16 w-16 mx-auto text-muted-foreground mb-4), h3 "Danh sách yêu thích trống" (text-xl font-semibold mb-2), p "Bạn chưa có sách nào trong danh sách yêu thích" (text-muted-foreground mb-6), Button asChild với Link href="/user/products" text "Khám phá sách" | | Pass | 11/15/2015 | |
| **GUI-XD-05** | Kiểm tra Input tìm kiếm | 1. Truy cập /user/wishlist<br>2. Có sách<br>3. Kiểm tra | Hiển thị div relative với icon Search (absolute left-3 top-1/2 transform -translate-y-1/2 text-muted-foreground h-4 w-4), Input placeholder "Tìm kiếm trong danh sách yêu thích..." value={searchTerm} className="pl-10" | | Pass | 11/15/2015 | |
| **GUI-XD-06** | Kiểm tra Select thể loại | 1. Truy cập /user/wishlist<br>2. Có sách<br>3. Kiểm tra | Hiển thị Select value={selectedCategory} với SelectTrigger className="w-48", SelectValue placeholder "Thể loại", SelectContent có SelectItem cho mỗi category: "Tất cả", "Kỹ năng sống", "Tâm lý học", "Lịch sử", "Phát triển bản thân", "Kinh doanh", "Văn học", "Khoa học", "Công nghệ" | | Pass | 11/15/2015 | |
| **GUI-XD-07** | Kiểm tra Select sắp xếp | 1. Truy cập /user/wishlist<br>2. Có sách<br>3. Kiểm tra | Hiển thị Select value={sortBy} với SelectTrigger className="w-48", SelectValue placeholder "Sắp xếp theo", SelectContent có SelectItem: "Ngày thêm" (value="addedDate"), "Giá" (value="price"), "Tên sách" (value="title"), "Năm xuất bản" (value="publishYear"), "Đánh giá" (value="rating") | | Pass | 11/15/2015 | |
| **GUI-XD-08** | Kiểm tra nút toggle sắp xếp | 1. Truy cập /user/wishlist<br>2. Có sách<br>3. Kiểm tra | Hiển thị Button variant="outline" size="sm" className="flex items-center gap-1" với icon SortAsc (h-4 w-4) nếu sortOrder === "asc", SortDesc (h-4 w-4) nếu sortOrder === "desc", onClick={toggleSortOrder} | | Pass | 11/15/2015 | |
| **GUI-XD-09** | Kiểm tra nút Thêm tất cả vào giỏ | 1. Truy cập /user/wishlist<br>2. Có sách<br>3. Kiểm tra | Hiển thị Button variant="outline" với icon ShoppingCart (h-4 w-4 mr-2) và text "Thêm tất cả vào giỏ", disabled={filteredBooks.filter((book) => book.stock > 0).length === 0}, onClick={addAllToCart} | | Pass | 11/15/2015 | |
| **GUI-XD-10** | Kiểm tra nút Xóa tất cả | 1. Truy cập /user/wishlist<br>2. Có sách<br>3. Kiểm tra | Hiển thị Button variant="outline" className="text-red-600 hover:text-red-700" với icon Trash2 (h-4 w-4 mr-2) và text "Xóa tất cả", onClick={clearWishlist} | | Pass | 11/15/2015 | |
| **GUI-XD-11** | Kiểm tra thông tin số lượng | 1. Truy cập /user/wishlist<br>2. Có sách<br>3. Kiểm tra | Hiển thị p text-sm text-muted-foreground "Hiển thị {filteredBooks.length} trong tổng số {books.length} sách" | | Pass | 11/15/2015 | |
| **GUI-XD-12** | Kiểm tra grid danh sách sách | 1. Truy cập /user/wishlist<br>2. Có sách<br>3. Kiểm tra | Hiển thị div grid grid-cols-2 md:grid-cols-3 lg:grid-cols-6 gap-6 với các Card cho mỗi book | | Pass | 11/15/2015 | |
| **GUI-XD-13** | Kiểm tra Card sách | 1. Truy cập /user/wishlist<br>2. Có sách<br>3. Kiểm tra | Hiển thị Card className="group hover:shadow-lg transition-shadow" với CardHeader p-0, CardContent p-4 | | Pass | 11/15/2015 | |
| **GUI-XD-14** | Kiểm tra hình ảnh sách | 1. Truy cập /user/wishlist<br>2. Có sách<br>3. Kiểm tra | Hiển thị div relative với div aspect-[3/4] overflow-hidden rounded-t-lg chứa Image src={book.image} alt={book.title} width={300} height={400} className="w-full h-full object-cover group-hover:scale-105 transition-transform duration-300" | | Pass | 11/15/2015 | |
| **GUI-XD-15** | Kiểm tra Badge trên hình ảnh | 1. Truy cập /user/wishlist<br>2. Có sách<br>3. Kiểm tra | Hiển thị div absolute top-2 left-2 flex flex-col gap-1 với Badge className="bg-green-500 text-white" "Mới" (nếu isNew), Badge className="bg-orange-500 text-white" "Bán chạy" (nếu isBestseller), Badge className="bg-red-500 text-white" "-{book.discount}%" (nếu discount) | | Pass | 11/15/2015 | |
| **GUI-XD-16** | Kiểm tra nút xóa yêu thích trên Card | 1. Truy cập /user/wishlist<br>2. Có sách<br>3. Kiểm tra | Hiển thị Button variant="ghost" size="sm" className="absolute top-2 right-2 h-8 w-8 p-0 bg-white/80 hover:bg-white" với icon Heart className="h-4 w-4 fill-red-500 text-red-500" onClick={() => removeFromWishlist(book.id)} | | Pass | 11/15/2015 | |
| **GUI-XD-17** | Kiểm tra thông tin sách trong Card | 1. Truy cập /user/wishlist<br>2. Có sách<br>3. Kiểm tra | Hiển thị div space-y-3 với: h3 font-semibold text-sm line-clamp-2 mb-1 "{book.title}", p text-xs text-muted-foreground flex items-center gap-1 với icon User (h-3 w-3) và text "{book.author}" | | Pass | 11/15/2015 | |
| **GUI-XD-18** | Kiểm tra Star Rating | 1. Truy cập /user/wishlist<br>2. Có sách<br>3. Kiểm tra | Hiển thị div flex items-center gap-1 với div flex items-center có 5 Star (h-3 w-3) với className fill-yellow-400 text-yellow-400 nếu i < Math.floor(book.rating), text-gray-300 nếu không, span text-xs text-muted-foreground "({book.reviewCount})" | | Pass | 11/15/2015 | |
| **GUI-XD-19** | Kiểm tra giá sách | 1. Truy cập /user/wishlist<br>2. Có sách<br>3. Kiểm tra | Hiển thị div flex items-center gap-2 với span font-bold text-primary "{book.price.toLocaleString('vi-VN')} VNĐ", span text-xs text-muted-foreground line-through "{book.originalPrice.toLocaleString('vi-VN')} VNĐ" (nếu originalPrice) | | Pass | 11/15/2015 | |
| **GUI-XD-20** | Kiểm tra trạng thái tồn kho | 1. Truy cập /user/wishlist<br>2. Có sách<br>3. Kiểm tra | Hiển thị div text-xs với span text-green-600 "Còn hàng ({book.stock})" nếu stock > 0, span text-red-600 "Hết hàng" nếu stock === 0 | | Pass | 11/15/2015 | |
| **GUI-XD-21** | Kiểm tra ngày thêm | 1. Truy cập /user/wishlist<br>2. Có sách<br>3. Kiểm tra | Hiển thị div text-xs text-muted-foreground "Thêm vào: {new Date(book.addedDate).toLocaleDateString('vi-VN')}" | | Pass | 11/15/2015 | |
| **GUI-XD-22** | Kiểm tra nút Chi tiết và Mua | 1. Truy cập /user/wishlist<br>2. Có sách<br>3. Kiểm tra | Hiển thị div flex gap-2 với Button variant="outline" size="sm" className="flex-1" asChild với Link href={`/user/products/${book.id}`} icon BookOpen (h-3 w-3 mr-1) text "Chi tiết", Button size="sm" className="flex-1" icon ShoppingCart (h-3 w-3 mr-1) text "Mua" disabled={book.stock === 0} onClick={() => addToCart(book)} | | Pass | 11/15/2015 | |
| **GUI-XD-23** | Kiểm tra nút Chia sẻ, So sánh, Thông báo giá | 1. Truy cập /user/wishlist<br>2. Có sách<br>3. Kiểm tra | Hiển thị div flex gap-2 mt-2 với Button variant="outline" size="sm" className="flex-1" icon Share2 (h-3 w-3 mr-1) text "Chia sẻ" onClick={() => openShare(book)}, Button variant="outline" size="sm" className="flex-1" icon Scale (h-3 w-3 mr-1) text "So sánh" onClick={() => openCompare(book)}, Button variant="outline" size="sm" className="flex-1" icon Bell (h-3 w-3 mr-1) text "Thông báo giá" onClick={() => openPriceAlert(book)} | | Pass | 11/15/2015 | |
| **GUI-XD-24** | Kiểm tra Empty state không tìm thấy | 1. Truy cập /user/wishlist<br>2. Áp dụng bộ lọc không có kết quả<br>3. Kiểm tra | Hiển thị div text-center py-12 với icon Heart (h-12 w-12 mx-auto text-muted-foreground mb-4), h3 "Không tìm thấy sách" (text-lg font-semibold mb-2), p "Hãy thử thay đổi từ khóa tìm kiếm hoặc bộ lọc" (text-muted-foreground mb-4), Button variant="outline" text "Xóa bộ lọc" onClick={clearFilters} | | Pass | 11/15/2015 | |
| **GUI-XD-25** | Kiểm tra Dialog Chia sẻ | 1. Truy cập /user/wishlist<br>2. Nhấn nút "Chia sẻ"<br>3. Kiểm tra | Hiển thị Dialog open={!!shareTarget} với DialogContent, DialogHeader có DialogTitle "Chia sẻ sản phẩm", DialogDescription "Chia sẻ đường link sản phẩm cho bạn bè hoặc mạng xã hội" | | Pass | 11/15/2015 | |
| **GUI-XD-26** | Kiểm tra form chia sẻ | 1. Mở Dialog chia sẻ<br>2. Kiểm tra | Hiển thị div grid gap-3 text-sm với div có Label "Link", Input readOnly value={`${location.origin}/user/products/${shareTarget.id}`}, div grid grid-cols-3 gap-2 với Button variant="outline" "Facebook", "Twitter", "Email" | | Pass | 11/15/2015 | |
| **GUI-XD-27** | Kiểm tra Dialog So sánh | 1. Truy cập /user/wishlist<br>2. Nhấn nút "So sánh"<br>3. Kiểm tra | Hiển thị Dialog open={compareOpen} với DialogContent, DialogHeader có DialogTitle "So sánh sản phẩm", DialogDescription "Danh sách sản phẩm đang so sánh" | | Pass | 11/15/2015 | |
| **GUI-XD-28** | Kiểm tra form so sánh | 1. Mở Dialog so sánh<br>2. Kiểm tra | Hiển thị div grid gap-3 text-sm với div text-muted-foreground "Chưa có sản phẩm nào" (nếu compareList.length === 0), div grid grid-cols-1 md:grid-cols-2 gap-3 với các div p-3 rounded-lg border cho mỗi book có div font-medium line-clamp-2 "{b.title}", div text-xs text-muted-foreground "{b.category} • {b.publishYear}", div text-xs "Giá: {b.price.toLocaleString('vi-VN')}đ" | | Pass | 11/15/2015 | |
| **GUI-XD-29** | Kiểm tra Dialog Thông báo giá | 1. Truy cập /user/wishlist<br>2. Nhấn nút "Thông báo giá"<br>3. Kiểm tra | Hiển thị Dialog open={!!priceAlertTarget} với DialogContent, DialogHeader có DialogTitle "Đăng ký thông báo giá", DialogDescription "Nhận thông báo khi sản phẩm giảm giá" | | Pass | 11/15/2015 | |
| **GUI-XD-30** | Kiểm tra form thông báo giá | 1. Mở Dialog thông báo giá<br>2. Kiểm tra | Hiển thị div grid gap-3 text-sm với div có Label "Email nhận thông báo", Input type="email" value={alertEmail} placeholder "you@email.com", div có Label "Mức giá mong muốn (VNĐ)", Input value={alertPrice} placeholder "Ví dụ: 120000", div có Label "Ghi chú", Textarea rows={3} placeholder "Tùy chọn" | | Pass | 11/15/2015 | |

#### Check FUNC: Xem danh sách yêu thích

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XD-01** | Mở trang danh sách yêu thích | 1. Truy cập /user/wishlist | Hiển thị trang với tiêu đề, nút Tiếp tục mua sắm, thông báo giới hạn (nếu có), Empty state (nếu không có sách), hoặc danh sách sách với bộ lọc và sắp xếp | | Pass | 11/15/2015 | |
| **FUNC-XD-02** | Hiển thị danh sách sách yêu thích | 1. Truy cập /user/wishlist<br>2. Có sách<br>3. Kiểm tra | Tất cả sách trong wishlist được hiển thị với đầy đủ thông tin: hình ảnh, tên sách, tác giả, giá, đánh giá, trạng thái tồn kho, ngày thêm, các nút hành động | | Pass | 11/15/2015 | |
| **FUNC-XD-03** | Tìm kiếm trong danh sách | 1. Truy cập /user/wishlist<br>2. Nhập từ khóa vào Input tìm kiếm<br>3. Kiểm tra | Danh sách được lọc theo từ khóa, chỉ hiển thị sách có tên, tác giả hoặc thể loại khớp với từ khóa, filteredBooks được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-XD-04** | Lọc theo thể loại | 1. Truy cập /user/wishlist<br>2. Chọn thể loại từ Select<br>3. Kiểm tra | Danh sách được lọc theo thể loại đã chọn, chỉ hiển thị sách thuộc thể loại đó, filteredBooks được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-XD-05** | Sắp xếp theo ngày thêm | 1. Truy cập /user/wishlist<br>2. Chọn "Ngày thêm" từ Select<br>3. Kiểm tra | Danh sách được sắp xếp theo addedDate, thứ tự phụ thuộc vào sortOrder (asc/desc) | | Pass | 11/15/2015 | |
| **FUNC-XD-06** | Sắp xếp theo giá | 1. Truy cập /user/wishlist<br>2. Chọn "Giá" từ Select<br>3. Kiểm tra | Danh sách được sắp xếp theo price, thứ tự phụ thuộc vào sortOrder (asc/desc) | | Pass | 11/15/2015 | |
| **FUNC-XD-07** | Sắp xếp theo tên sách | 1. Truy cập /user/wishlist<br>2. Chọn "Tên sách" từ Select<br>3. Kiểm tra | Danh sách được sắp xếp theo title (alphabetical), thứ tự phụ thuộc vào sortOrder (asc/desc) | | Pass | 11/15/2015 | |
| **FUNC-XD-08** | Sắp xếp theo năm xuất bản | 1. Truy cập /user/wishlist<br>2. Chọn "Năm xuất bản" từ Select<br>3. Kiểm tra | Danh sách được sắp xếp theo publishYear, thứ tự phụ thuộc vào sortOrder (asc/desc) | | Pass | 11/15/2015 | |
| **FUNC-XD-09** | Sắp xếp theo đánh giá | 1. Truy cập /user/wishlist<br>2. Chọn "Đánh giá" từ Select<br>3. Kiểm tra | Danh sách được sắp xếp theo rating, thứ tự phụ thuộc vào sortOrder (asc/desc) | | Pass | 11/15/2015 | |
| **FUNC-XD-10** | Toggle thứ tự sắp xếp | 1. Truy cập /user/wishlist<br>2. Nhấn nút toggle sortOrder<br>3. Kiểm tra | sortOrder chuyển từ "asc" sang "desc" hoặc ngược lại, icon chuyển từ SortAsc sang SortDesc hoặc ngược lại, danh sách được sắp xếp lại theo thứ tự mới | | Pass | 11/15/2015 | |
| **FUNC-XD-11** | Lọc kết hợp nhiều điều kiện | 1. Truy cập /user/wishlist<br>2. Áp dụng tìm kiếm và lọc thể loại<br>3. Kiểm tra | Danh sách được lọc theo tất cả điều kiện đã chọn, chỉ hiển thị sách thỏa mãn tất cả điều kiện | | Pass | 11/15/2015 | |
| **FUNC-XD-12** | Thêm tất cả vào giỏ hàng | 1. Truy cập /user/wishlist<br>2. Có sách còn hàng<br>3. Nhấn nút "Thêm tất cả vào giỏ" | Hiển thị toast.success "Đã thêm {availableBooks.length} sách vào giỏ hàng", chỉ các sách còn hàng (stock > 0) được thêm vào giỏ hàng | | Pass | 11/15/2015 | |
| **FUNC-XD-13** | Thêm tất cả vào giỏ - không có sách còn hàng | 1. Truy cập /user/wishlist<br>2. Tất cả sách hết hàng<br>3. Nhấn nút "Thêm tất cả vào giỏ" | Nút bị disabled, hiển thị toast.error "Không có sách nào còn hàng" nếu nhấn được | | Pass | 11/15/2015 | |
| **FUNC-XD-14** | Nhấn nút Chi tiết | 1. Truy cập /user/wishlist<br>2. Nhấn nút "Chi tiết" | Chuyển đến trang /user/products/{book.id} | | Pass | 11/15/2015 | |
| **FUNC-XD-15** | Nhấn nút Mua | 1. Truy cập /user/wishlist<br>2. Sách còn hàng<br>3. Nhấn nút "Mua" | Hiển thị toast.success "Đã thêm \"{book.title}\" vào giỏ hàng", sách được thêm vào giỏ hàng | | Pass | 11/15/2015 | |
| **FUNC-XD-16** | Nhấn nút Mua - sách hết hàng | 1. Truy cập /user/wishlist<br>2. Sách hết hàng<br>3. Nhấn nút "Mua" | Nút bị disabled, không thể nhấn | | Pass | 11/15/2015 | |
| **FUNC-XD-17** | Chia sẻ sách | 1. Truy cập /user/wishlist<br>2. Nhấn nút "Chia sẻ"<br>3. Kiểm tra | shareTarget được set, Dialog chia sẻ hiển thị với link sản phẩm, có thể sao chép link hoặc chia sẻ qua Facebook, Twitter, Email | | Pass | 11/15/2015 | |
| **FUNC-XD-18** | So sánh sách | 1. Truy cập /user/wishlist<br>2. Nhấn nút "So sánh" trên sách A<br>3. Nhấn nút "So sánh" trên sách B<br>4. Kiểm tra | compareList được cập nhật với sách A và B, Dialog so sánh hiển thị với danh sách sách đang so sánh, không thêm trùng lặp nếu sách đã có trong compareList | | Pass | 11/15/2015 | |
| **FUNC-XD-19** | Xóa danh sách so sánh | 1. Mở Dialog so sánh<br>2. Nhấn nút "Xóa danh sách" | compareList được xóa ([]), Dialog đóng lại | | Pass | 11/15/2015 | |
| **FUNC-XD-20** | Đăng ký thông báo giá | 1. Truy cập /user/wishlist<br>2. Nhấn nút "Thông báo giá"<br>3. Nhập email và mức giá<br>4. Nhấn "Đăng ký" | Hiển thị toast.success "Đã đăng ký thông báo giá", priceAlertTarget = null, alertEmail và alertPrice được reset, Dialog đóng lại | | Pass | 11/15/2015 | |
| **FUNC-XD-21** | Hủy Dialog thông báo giá | 1. Mở Dialog thông báo giá<br>2. Nhấn nút "Hủy" | priceAlertTarget = null, Dialog đóng lại, alertEmail và alertPrice không thay đổi | | Pass | 11/15/2015 | |
| **FUNC-XD-22** | Xóa bộ lọc | 1. Truy cập /user/wishlist<br>2. Áp dụng bộ lọc<br>3. Nhấn nút "Xóa bộ lọc" | searchTerm = "", selectedCategory = "Tất cả", filteredBooks = books, tất cả sách được hiển thị lại | | Pass | 11/15/2015 | |
| **FUNC-XD-23** | Hiển thị số lượng sách | 1. Truy cập /user/wishlist<br>2. Kiểm tra | Hiển thị "Hiển thị {filteredBooks.length} trong tổng số {books.length} sách", số lượng được cập nhật khi lọc hoặc xóa sách | | Pass | 11/15/2015 | |
| **FUNC-XD-24** | Hiển thị giới hạn wishlist | 1. Truy cập /user/wishlist<br>2. Kiểm tra | Hiển thị "{books.length}/{MAX_WISHLIST_ITEMS} sách trong danh sách yêu thích của bạn", nếu books.length >= MAX_WISHLIST_ITEMS thì hiển thị thông báo cảnh báo | | Pass | 11/15/2015 | |

### Function: Xóa sách khỏi danh sách yêu thích

#### Check FUNC: Xóa sách khỏi yêu thích

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XO-01** | Xóa sách khỏi danh sách yêu thích | 1. Truy cập /user/wishlist<br>2. Nhấn nút Heart filled trên Card sách<br>3. Kiểm tra | Hiển thị toast.success "Đã xóa khỏi danh sách yêu thích", sách được xóa khỏi books và filteredBooks, Card sách không còn hiển thị | | Pass | 11/15/2015 | |
| **FUNC-XO-02** | Xóa sách từ trang chi tiết | 1. Truy cập /user/products/[id]<br>2. Sách đã yêu thích<br>3. Nhấn nút Heart filled<br>4. Kiểm tra | Hiển thị toast.success "Đã xóa khỏi danh sách yêu thích", isFavorite = false, icon Heart chuyển từ filled về outline, sách được xóa khỏi wishlist | | Pass | 11/15/2015 | |
| **FUNC-XO-03** | Xóa tất cả sách | 1. Truy cập /user/wishlist<br>2. Nhấn nút "Xóa tất cả"<br>3. Xác nhận<br>4. Kiểm tra | Hiển thị toast.success "Đã xóa tất cả sách khỏi danh sách yêu thích", books = [], filteredBooks = [], hiển thị Empty state | | Pass | 11/15/2015 | |
| **FUNC-XO-04** | Cập nhật giao diện sau khi xóa | 1. Xóa sách khỏi yêu thích<br>2. Kiểm tra | Icon Heart trên trang chi tiết chuyển từ filled về outline, Badge "Yêu thích" ẩn (nếu có), counter yêu thích giảm, Card sách không còn trong danh sách | | Pass | 11/15/2015 | |
| **FUNC-XO-05** | Cập nhật số lượng sau khi xóa | 1. Xóa sách khỏi yêu thích<br>2. Kiểm tra | Số lượng sách được cập nhật: "{books.length - 1}/{MAX_WISHLIST_ITEMS}", thông báo giới hạn ẩn nếu books.length < MAX_WISHLIST_ITEMS | | Pass | 11/15/2015 | |
| **FUNC-XO-06** | Xóa sách và thêm lại | 1. Xóa sách khỏi yêu thích<br>2. Thêm lại sách vào yêu thích<br>3. Kiểm tra | Sách được thêm lại thành công, addedDate được cập nhật thành ngày mới, sách hiển thị trong danh sách | | Pass | 11/15/2015 | |
| **FUNC-XO-07** | Xóa sách khi đang lọc | 1. Truy cập /user/wishlist<br>2. Áp dụng bộ lọc<br>3. Xóa sách trong kết quả lọc<br>4. Kiểm tra | Sách được xóa khỏi books và filteredBooks, danh sách được cập nhật, nếu không còn sách nào thì hiển thị Empty state "Không tìm thấy sách" | | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn MDX để dễ dàng quản lý và cập nhật test cases.*

