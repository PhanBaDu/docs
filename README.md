# Test Case Template - Tìm kiếm sách (User)

## Module Code
**USER-003: Tìm kiếm sách (User)**

## Test Requirement
1. Tìm kiếm sách
2. Hiển thị kết quả tìm kiếm

---

## Test Summary

### Người thực hiện Test: Tester

| Status | Count |
|--------|-------|
| **Pass** | 58 |
| **Fail** | 0 |
| **Untested** | 0 |
| **N/A** | 0 |
| **Number of Test cases** | 58 |

---

## Test Cases

### Function: Tìm kiếm sách

#### Check GUI: Tìm kiếm sách

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-TK-01** | Kiểm tra tiêu đề trang | 1. Truy cập /user/search<br>2. Kiểm tra tiêu đề | Hiển thị h1 "Tìm kiếm sách" (text-3xl font-bold mb-2), p "Tìm kiếm sách theo tên, tác giả, thể loại hoặc từ khóa" (text-muted-foreground) | | Pass | 11/15/2015 | |
| **GUI-TK-02** | Kiểm tra nút Quay lại | 1. Truy cập /user/search<br>2. Kiểm tra nút | Hiển thị Link đến /user với Button variant outline size sm, icon ArrowLeft và text "Quay lại" | | Pass | 11/15/2015 | |
| **GUI-TK-03** | Kiểm tra Card thanh tìm kiếm | 1. Truy cập /user/search<br>2. Kiểm tra Card | Hiển thị Card với CardContent (p-6), có Input với placeholder "Tìm kiếm sách, tác giả, thể loại..." | | Pass | 11/15/2015 | |
| **GUI-TK-04** | Kiểm tra Input tìm kiếm | 1. Truy cập /user/search<br>2. Kiểm tra Input | Hiển thị Input với icon Search ở bên trái (absolute left-3 top-1/2), className "pl-10 pr-10", có nút X (×) ở bên phải khi có searchTerm | | Pass | 11/15/2015 | |
| **GUI-TK-05** | Kiểm tra nút Xóa tìm kiếm | 1. Truy cập /user/search<br>2. Nhập từ khóa<br>3. Kiểm tra nút | Hiển thị Button variant ghost size sm (h-6 w-6 p-0) ở absolute right-3 top-1/2 với text "×", chỉ hiển thị khi searchTerm có giá trị | | Pass | 11/15/2015 | |
| **GUI-TK-06** | Kiểm tra phần gợi ý tìm kiếm | 1. Truy cập /user/search<br>2. Nhập từ khóa<br>3. Kiểm tra gợi ý | Hiển thị div với className "mt-2 border rounded-lg bg-background shadow-lg max-h-60 overflow-y-auto" khi showSuggestions = true và searchTerm.length > 0 | | Pass | 11/15/2015 | |
| **GUI-TK-07** | Kiểm tra item gợi ý | 1. Truy cập /user/search<br>2. Nhập từ khóa<br>3. Kiểm tra item | Hiển thị div với className "flex items-center justify-between p-3 hover:bg-muted cursor-pointer", có icon Package (h-4 w-4 text-muted-foreground), text suggestion.text, Badge variant outline hiển thị "Sách", "NXB", hoặc "Thể loại" tùy theo type, span hiển thị count nếu có | | Pass | 11/15/2015 | |
| **GUI-TK-08** | Kiểm tra phần tìm kiếm gần đây | 1. Truy cập /user/search<br>2. Không nhập từ khóa<br>3. Có lịch sử tìm kiếm<br>4. Kiểm tra phần | Hiển thị div với h3 "Tìm kiếm gần đây" (text-sm font-medium mb-2), div flex flex-wrap gap-2 với các Button variant outline size sm, icon Clock (h-3 w-3 mr-1), text search term, className text-xs | | Pass | 11/15/2015 | |
| **GUI-TK-09** | Kiểm tra Card bộ lọc | 1. Truy cập /user/search<br>2. Kiểm tra Card | Hiển thị Card với CardContent (p-4), có icon Filter (h-4 w-4) và text "Bộ lọc:" (font-medium) | | Pass | 11/15/2015 | |
| **GUI-TK-10** | Kiểm tra Select danh mục | 1. Truy cập /user/search<br>2. Kiểm tra Select | Hiển thị Select với SelectTrigger (w-48), SelectValue placeholder "Danh mục", SelectContent có các options: Tất cả, Lập trình, Truyện tranh - Manga, Công nghệ - Kỹ thuật, Kinh tế, Ảnh - Sách ảnh, Lịch sử, Khác | | Pass | 11/15/2015 | |
| **GUI-TK-11** | Kiểm tra Select nhà xuất bản | 1. Truy cập /user/search<br>2. Kiểm tra Select | Hiển thị Select với SelectTrigger (w-48), SelectValue placeholder "Nhà xuất bản", SelectContent có các options: Tất cả, NXB Kim Đồng, NXB Trẻ, NXB Tổng hợp, NXB Văn học, NXB Kinh tế | | Pass | 11/15/2015 | |
| **GUI-TK-12** | Kiểm tra Select sắp xếp | 1. Truy cập /user/search<br>2. Kiểm tra Select | Hiển thị Select với SelectTrigger (w-48), SelectValue placeholder "Sắp xếp", SelectContent có các options: Liên quan, Giá thấp, Giá cao, Đánh giá, Mới nhất | | Pass | 11/15/2015 | |
| **GUI-TK-13** | Kiểm tra Card thể loại sách | 1. Truy cập /user/search<br>2. Scroll xuống<br>3. Kiểm tra Card | Hiển thị Card với CardHeader có CardTitle "Thể loại sách" (icon Package h-5 w-5), CardDescription "Khám phá sách theo thể loại", CardContent có grid grid-cols-2 md:grid-cols-3 lg:grid-cols-6 gap-4 | | Pass | 11/15/2015 | |
| **GUI-TK-14** | Kiểm tra nút thể loại | 1. Truy cập /user/search<br>2. Kiểm tra nút thể loại | Hiển thị Button variant outline với className "h-20 flex flex-col items-center justify-center gap-2", icon Package (h-6 w-6), text category (text-sm) | | Pass | 11/15/2015 | |

#### Check FUNC: Tìm kiếm sách

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TK-01** | Mở trang tìm kiếm | 1. Truy cập /user/search | Hiển thị trang với tiêu đề, nút Quay lại, Card thanh tìm kiếm, Card bộ lọc, phần kết quả (nếu có), Card thể loại sách | | Pass | 11/15/2015 | |
| **FUNC-TK-02** | Nhập từ khóa tìm kiếm | 1. Truy cập /user/search<br>2. Nhập từ khóa vào Input<br>3. Kiểm tra | showSuggestions = true nếu searchTerm.length > 0, danh sách gợi ý được lọc theo từ khóa, kết quả tìm kiếm được cập nhật theo thời gian thực | | Pass | 11/15/2015 | |
| **FUNC-TK-03** | Tìm kiếm với từ khóa hợp lệ | 1. Truy cập /user/search<br>2. Nhập từ khóa "React"<br>3. Kiểm tra kết quả | Danh sách sách được lọc theo từ khóa, hiển thị các sách có title, brand, category, hoặc description chứa từ khóa, thông tin số lượng được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-TK-04** | Tìm kiếm không có kết quả | 1. Truy cập /user/search<br>2. Nhập từ khóa không tồn tại<br>3. Kiểm tra | Hiển thị Card với icon Package (h-12 w-12 mx-auto text-muted-foreground mb-4), h3 "Không tìm thấy sách" (text-lg font-semibold mb-2), p "Không có sách nào phù hợp với từ khóa \"{searchTerm}\"", Button "Xóa bộ lọc" variant outline | | Pass | 11/15/2015 | |
| **FUNC-TK-05** | Click vào gợi ý tìm kiếm | 1. Truy cập /user/search<br>2. Nhập từ khóa<br>3. Click vào item gợi ý | searchTerm được set thành suggestion.text, showSuggestions = false, kết quả tìm kiếm được cập nhật, từ khóa được thêm vào recentSearches (tối đa 5 từ khóa) | | Pass | 11/15/2015 | |
| **FUNC-TK-06** | Click vào tìm kiếm gần đây | 1. Truy cập /user/search<br>2. Có lịch sử tìm kiếm<br>3. Click vào từ khóa gần đây | searchTerm được set thành từ khóa đã chọn, kết quả tìm kiếm được cập nhật, showSuggestions = false | | Pass | 11/15/2015 | |
| **FUNC-TK-07** | Lưu lịch sử tìm kiếm | 1. Truy cập /user/search<br>2. Nhập từ khóa và tìm kiếm<br>3. Kiểm tra lịch sử | Từ khóa được thêm vào đầu danh sách recentSearches, giới hạn tối đa 5 từ khóa (slice(0, 4) + từ khóa mới), không thêm trùng lặp | | Pass | 11/15/2015 | |
| **FUNC-TK-08** | Xóa từ khóa tìm kiếm | 1. Truy cập /user/search<br>2. Nhập từ khóa<br>3. Click nút X | searchTerm = "", filteredBooks = [], showSuggestions = false, nút X biến mất | | Pass | 11/15/2015 | |
| **FUNC-TK-09** | Tìm kiếm với query parameter | 1. Truy cập /user/search?q=React<br>2. Kiểm tra | searchTerm được khởi tạo với giá trị từ query parameter "q", kết quả tìm kiếm được hiển thị ngay | | Pass | 11/15/2015 | |
| **FUNC-TK-10** | Lọc theo danh mục | 1. Truy cập /user/search<br>2. Nhập từ khóa<br>3. Chọn danh mục từ Select | Kết quả tìm kiếm được lọc theo danh mục đã chọn, chỉ hiển thị sách thuộc danh mục đó, currentPage được reset về 1 | | Pass | 11/15/2015 | |
| **FUNC-TK-11** | Lọc theo nhà xuất bản | 1. Truy cập /user/search<br>2. Nhập từ khóa<br>3. Chọn nhà xuất bản từ Select | Kết quả tìm kiếm được lọc theo nhà xuất bản đã chọn, chỉ hiển thị sách của nhà xuất bản đó, currentPage được reset về 1 | | Pass | 11/15/2015 | |
| **FUNC-TK-12** | Sắp xếp theo liên quan | 1. Truy cập /user/search<br>2. Nhập từ khóa<br>3. Chọn "Liên quan" | Kết quả được sắp xếp theo thứ tự mặc định (không sắp xếp), currentPage được reset về 1 | | Pass | 11/15/2015 | |
| **FUNC-TK-13** | Sắp xếp theo giá thấp | 1. Truy cập /user/search<br>2. Nhập từ khóa<br>3. Chọn "Giá thấp" | Kết quả được sắp xếp theo giá tăng dần (a.price - b.price), currentPage được reset về 1 | | Pass | 11/15/2015 | |
| **FUNC-TK-14** | Sắp xếp theo giá cao | 1. Truy cập /user/search<br>2. Nhập từ khóa<br>3. Chọn "Giá cao" | Kết quả được sắp xếp theo giá giảm dần (b.price - a.price), currentPage được reset về 1 | | Pass | 11/15/2015 | |
| **FUNC-TK-15** | Sắp xếp theo đánh giá | 1. Truy cập /user/search<br>2. Nhập từ khóa<br>3. Chọn "Đánh giá" | Kết quả được sắp xếp theo rating giảm dần (b.rating - a.rating), currentPage được reset về 1 | | Pass | 11/15/2015 | |
| **FUNC-TK-16** | Sắp xếp theo mới nhất | 1. Truy cập /user/search<br>2. Nhập từ khóa<br>3. Chọn "Mới nhất" | Kết quả được sắp xếp với sách có isNew = true ở đầu ((b.isNew ? 1 : 0) - (a.isNew ? 1 : 0)), currentPage được reset về 1 | | Pass | 11/15/2015 | |
| **FUNC-TK-17** | Click vào nút thể loại | 1. Truy cập /user/search<br>2. Click vào nút thể loại | selectedCategory được set thành category đã chọn, searchTerm = "", kết quả được lọc theo thể loại | | Pass | 11/15/2015 | |
| **FUNC-TK-18** | Focus vào Input tìm kiếm | 1. Truy cập /user/search<br>2. Click vào Input | showSuggestions = true nếu searchTerm.length > 0, danh sách gợi ý được hiển thị | | Pass | 11/15/2015 | |
| **FUNC-TK-19** | Nhấn nút Quay lại | 1. Truy cập /user/search<br>2. Nhấn nút "Quay lại" | Chuyển đến trang /user | | Pass | 11/15/2015 | |

### Function: Hiển thị kết quả tìm kiếm

#### Check GUI: Kết quả tìm kiếm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-KQ-01** | Kiểm tra tiêu đề kết quả | 1. Truy cập /user/search<br>2. Nhập từ khóa và tìm kiếm<br>3. Kiểm tra tiêu đề | Hiển thị h2 "Kết quả tìm kiếm cho \"{searchTerm}\"" (text-xl font-semibold) nếu có searchTerm, hoặc "Tìm thấy X kết quả" nếu không có searchTerm nhưng có kết quả, hoặc "Nhập từ khóa để tìm kiếm" nếu không có kết quả | | Pass | 11/15/2015 | |
| **GUI-KQ-02** | Kiểm tra thông tin số lượng | 1. Truy cập /user/search<br>2. Có kết quả tìm kiếm<br>3. Kiểm tra thông tin | Hiển thị div flex items-center gap-2 với icon TrendingUp (h-4 w-4), text "Hiển thị {startIndex + 1}-{Math.min(endIndex, filteredBooks.length)} trong tổng số {filteredBooks.length} sách" (text-sm text-muted-foreground) | | Pass | 11/15/2015 | |
| **GUI-KQ-03** | Kiểm tra grid kết quả | 1. Truy cập /user/search<br>2. Có kết quả<br>3. Kiểm tra grid | Hiển thị grid grid-cols-2 md:grid-cols-3 lg:grid-cols-6 gap-6 với các Card sách | | Pass | 11/15/2015 | |
| **GUI-KQ-04** | Kiểm tra Card sách trong kết quả | 1. Truy cập /user/search<br>2. Có kết quả<br>3. Kiểm tra Card | Hiển thị Card với className "group hover:shadow-lg transition-shadow duration-200", CardContent (p-0), có ảnh bìa, Badge trạng thái, nút yêu thích, thông tin sách, giá, trạng thái tồn kho, nút Xem và Mua | | Pass | 11/15/2015 | |
| **GUI-KQ-05** | Kiểm tra phân trang | 1. Truy cập /user/search<br>2. Có > 20 kết quả<br>3. Kiểm tra phân trang | Hiển thị Pagination component với PaginationContent, PaginationPrevious (disabled nếu currentPage === 1), các PaginationLink cho các trang (hiển thị trang 1, trang cuối, trang hiện tại, và các trang xung quanh), PaginationEllipsis cho các trang bị ẩn, PaginationNext (disabled nếu currentPage === totalPages) | | Pass | 11/15/2015 | |
| **GUI-KQ-06** | Kiểm tra màn hình không có kết quả | 1. Truy cập /user/search<br>2. Tìm kiếm không có kết quả<br>3. Kiểm tra | Hiển thị div col-span-full text-center py-12 với icon Package (h-12 w-12 mx-auto text-muted-foreground mb-4), h3 "Không tìm thấy sách" (text-lg font-semibold mb-2), p "Không có sách nào phù hợp với từ khóa \"{searchTerm}\"", Button "Xóa bộ lọc" variant outline | | Pass | 11/15/2015 | |
| **GUI-KQ-07** | Kiểm tra màn hình chưa tìm kiếm | 1. Truy cập /user/search<br>2. Chưa nhập từ khóa<br>3. Kiểm tra | Hiển thị div col-span-full text-center py-12 với icon Package (h-12 w-12 mx-auto text-muted-foreground mb-4), h3 "Tìm kiếm sách yêu thích" (text-lg font-semibold mb-2), p "Nhập từ khóa để tìm kiếm sách bạn muốn" (text-muted-foreground) | | Pass | 11/15/2015 | |

#### Check FUNC: Kết quả tìm kiếm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-KQ-01** | Hiển thị kết quả tìm kiếm | 1. Truy cập /user/search<br>2. Nhập từ khóa và tìm kiếm<br>3. Kiểm tra kết quả | Danh sách sách được hiển thị trong grid, mỗi Card có đầy đủ thông tin: ảnh, tên, tác giả, đánh giá, giá, trạng thái tồn kho, các nút hành động | | Pass | 11/15/2015 | |
| **FUNC-KQ-02** | Phân trang kết quả | 1. Truy cập /user/search<br>2. Tìm kiếm có > 20 kết quả<br>3. Kiểm tra phân trang | itemsPerPage = 20, totalPages = Math.ceil(filteredBooks.length / itemsPerPage), chỉ hiển thị 20 sách đầu tiên, phân trang được hiển thị nếu totalPages > 1 | | Pass | 11/15/2015 | |
| **FUNC-KQ-03** | Chuyển sang trang sau | 1. Truy cập /user/search<br>2. Có nhiều trang<br>3. Nhấn PaginationNext | currentPage tăng lên 1, hiển thị 20 sách tiếp theo (startIndex = (currentPage - 1) * itemsPerPage, endIndex = startIndex + itemsPerPage) | | Pass | 11/15/2015 | |
| **FUNC-KQ-04** | Chuyển về trang trước | 1. Truy cập /user/search<br>2. Ở trang > 1<br>3. Nhấn PaginationPrevious | currentPage giảm xuống 1, hiển thị 20 sách trước đó | | Pass | 11/15/2015 | |
| **FUNC-KQ-05** | Click vào số trang | 1. Truy cập /user/search<br>2. Có nhiều trang<br>3. Click vào số trang X | currentPage được set về X, hiển thị 20 sách tương ứng với trang X, PaginationLink có isActive = true cho trang hiện tại | | Pass | 11/15/2015 | |
| **FUNC-KQ-06** | Disable nút Trang trước ở trang đầu | 1. Truy cập /user/search<br>2. Ở trang đầu (currentPage = 1)<br>3. Kiểm tra nút | PaginationPrevious có className "pointer-events-none opacity-50", không thể click | | Pass | 11/15/2015 | |
| **FUNC-KQ-07** | Disable nút Trang sau ở trang cuối | 1. Truy cập /user/search<br>2. Ở trang cuối (currentPage = totalPages)<br>3. Kiểm tra nút | PaginationNext có className "pointer-events-none opacity-50", không thể click | | Pass | 11/15/2015 | |
| **FUNC-KQ-08** | Hiển thị PaginationEllipsis | 1. Truy cập /user/search<br>2. Có nhiều trang<br>3. Ở trang giữa<br>4. Kiểm tra | Hiển thị PaginationEllipsis cho các trang bị ẩn (page === currentPage - 2 hoặc page === currentPage + 2), chỉ hiển thị trang 1, trang cuối, trang hiện tại, và các trang xung quanh | | Pass | 11/15/2015 | |
| **FUNC-KQ-09** | Reset về trang đầu khi thay đổi bộ lọc | 1. Truy cập /user/search<br>2. Ở trang > 1<br>3. Thay đổi bộ lọc hoặc sắp xếp | currentPage được reset về 1, hiển thị 20 sách đầu tiên của kết quả mới | | Pass | 11/15/2015 | |
| **FUNC-KQ-10** | Thêm sách vào yêu thích từ kết quả | 1. Truy cập /user/search<br>2. Có kết quả<br>3. Nhấn nút Heart trên Card sách | Hiển thị toast.success "Đã thêm vào danh sách yêu thích" hoặc "Đã xóa khỏi danh sách yêu thích", icon Heart chuyển sang fill-red-500 text-red-500 hoặc text-muted-foreground, bookId được thêm/xóa khỏi favoriteBooks | | Pass | 11/15/2015 | |
| **FUNC-KQ-11** | Thêm sách vào giỏ hàng từ kết quả | 1. Truy cập /user/search<br>2. Có kết quả<br>3. Nhấn nút "Mua" trên Card sách | Hiển thị toast.success "Đã thêm \"{model.title}\" vào giỏ hàng" | | Pass | 11/15/2015 | |
| **FUNC-KQ-12** | Xem chi tiết sách từ kết quả | 1. Truy cập /user/search<br>2. Có kết quả<br>3. Nhấn nút "Xem" trên Card sách | Chuyển đến trang /user/products/{model.id} | | Pass | 11/15/2015 | |
| **FUNC-KQ-13** | Thêm sách hết hàng vào giỏ hàng | 1. Truy cập /user/search<br>2. Tìm sách hết hàng (stock = 0)<br>3. Nhấn nút "Mua" | Nút "Mua" bị disabled, không thể thêm vào giỏ hàng | | Pass | 11/15/2015 | |
| **FUNC-KQ-14** | Tính toán startIndex và endIndex | 1. Truy cập /user/search<br>2. Có kết quả<br>3. Chuyển trang<br>4. Kiểm tra | startIndex = (currentPage - 1) * itemsPerPage, endIndex = startIndex + itemsPerPage, paginatedBooks = filteredBooks.slice(startIndex, endIndex) | | Pass | 11/15/2015 | |
| **FUNC-KQ-15** | Hiển thị đúng số lượng kết quả | 1. Truy cập /user/search<br>2. Tìm kiếm<br>3. Kiểm tra số lượng | Thông tin hiển thị "Hiển thị {startIndex + 1}-{Math.min(endIndex, filteredBooks.length)} trong tổng số {filteredBooks.length} sách" chính xác | | Pass | 11/15/2015 | |
| **FUNC-KQ-16** | Xóa bộ lọc khi không có kết quả | 1. Truy cập /user/search<br>2. Tìm kiếm không có kết quả<br>3. Nhấn nút "Xóa bộ lọc" | searchTerm = "", filteredBooks = [], showSuggestions = false, hiển thị màn hình chưa tìm kiếm | | Pass | 11/15/2015 | |
| **FUNC-KQ-17** | Tìm kiếm kết hợp nhiều điều kiện | 1. Truy cập /user/search<br>2. Nhập từ khóa<br>3. Chọn danh mục<br>4. Chọn nhà xuất bản<br>5. Chọn sắp xếp | Kết quả được lọc theo tất cả điều kiện: từ khóa (title, brand, category, description), danh mục, nhà xuất bản, và được sắp xếp theo tiêu chí đã chọn | | Pass | 11/15/2015 | |
| **FUNC-KQ-18** | Tìm kiếm không phân biệt hoa thường | 1. Truy cập /user/search<br>2. Nhập từ khóa "REACT"<br>3. Kiểm tra kết quả | Kết quả tìm kiếm giống như nhập "react" hoặc "React", tìm kiếm không phân biệt hoa thường (toLowerCase()) | | Pass | 11/15/2015 | |
| **FUNC-KQ-19** | Tìm kiếm theo mô tả sách | 1. Truy cập /user/search<br>2. Nhập từ khóa có trong mô tả<br>3. Kiểm tra kết quả | Sách có description chứa từ khóa được hiển thị trong kết quả | | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn MDX để dễ dàng quản lý và cập nhật test cases.*

