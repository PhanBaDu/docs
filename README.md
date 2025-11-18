# Test Case Template - Hiển thị sách (User)

## Module Code
**USER-002: Hiển thị sách (User)**

## Test Requirement
1. Hiển thị danh sách sách
2. Xem chi tiết thông tin sách
3. Hiển thị nội dung sách "đọc thử"

---

## Test Summary

### Người thực hiện Test: Tester

| Status | Count |
|--------|-------|
| **Pass** | 62 |
| **Fail** | 0 |
| **Untested** | 0 |
| **N/A** | 0 |
| **Number of Test cases** | 62 |

---

## Test Cases

### Function: Hiển thị danh sách sách

#### Check GUI: Hiển thị danh sách sách

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DS-01** | Kiểm tra tiêu đề trang | 1. Truy cập /user/products<br>2. Kiểm tra tiêu đề | Hiển thị h1 "Danh sách sách" (text-3xl font-bold mb-2), p "Khám phá bộ sưu tập sách đa dạng với nhiều thể loại và nhà xuất bản uy tín" (text-muted-foreground) | | Pass | 11/15/2015 | |
| **GUI-DS-02** | Kiểm tra Card bộ lọc | 1. Truy cập /user/products<br>2. Kiểm tra Card bộ lọc | Hiển thị Card với CardContent (p-6), có icon Filter (h-4 w-4) và text "Bộ lọc:" (font-medium) | | Pass | 11/15/2015 | |
| **GUI-DS-03** | Kiểm tra Select danh mục | 1. Truy cập /user/products<br>2. Kiểm tra Select danh mục | Hiển thị Select với SelectTrigger (w-48), SelectValue placeholder "Danh mục", SelectContent có các options: Tất cả, Văn học, Truyện tranh - Manga, Công nghệ - Kỹ thuật, Kinh tế, Ảnh - Sách ảnh, Lịch sử, Khác | | Pass | 11/15/2015 | |
| **GUI-DS-04** | Kiểm tra Select nhà xuất bản | 1. Truy cập /user/products<br>2. Kiểm tra Select nhà xuất bản | Hiển thị Select với SelectTrigger (w-48), SelectValue placeholder "Nhà xuất bản", SelectContent có các options: Tất cả, NXB Kim Đồng, NXB Trẻ, NXB Tổng hợp, NXB Văn học, NXB Kinh tế | | Pass | 11/15/2015 | |
| **GUI-DS-05** | Kiểm tra SortControls | 1. Truy cập /user/products<br>2. Kiểm tra SortControls | Hiển thị component SortControls với các options sắp xếp: relevance, price-low, price-high, rating, newest | | Pass | 11/15/2015 | |
| **GUI-DS-06** | Kiểm tra nút chế độ hiển thị | 1. Truy cập /user/products<br>2. Kiểm tra nút | Hiển thị 2 Button: Grid (icon Grid3X3) và List (icon List), variant default khi active, outline khi không active, size sm | | Pass | 11/15/2015 | |
| **GUI-DS-07** | Kiểm tra Slider khoảng giá | 1. Truy cập /user/products<br>2. Kiểm tra Slider | Hiển thị Label "Khoảng giá" (text-sm font-medium), Slider với min=0, max=10000000, step=100000, hiển thị text "Từ: X VNĐ" và "Đến: Y VNĐ" (toLocaleString), text-xs "Giá từ 0 đến 10.000.000 VNĐ" | | Pass | 11/15/2015 | |
| **GUI-DS-08** | Kiểm tra thông tin số lượng | 1. Truy cập /user/products<br>2. Kiểm tra thông tin | Hiển thị text "Hiển thị X trong tổng số Y sách" (text-muted-foreground) | | Pass | 11/15/2015 | |
| **GUI-DS-09** | Kiểm tra Card sách (Grid mode) | 1. Truy cập /user/products<br>2. Chọn chế độ Grid<br>3. Kiểm tra Card | Hiển thị grid grid-cols-2 md:grid-cols-3 lg:grid-cols-6 gap-4, mỗi Card có className "group hover:shadow-lg transition-shadow duration-200" | | Pass | 11/15/2015 | |
| **GUI-DS-10** | Kiểm tra ảnh bìa sách | 1. Truy cập /user/products<br>2. Kiểm tra ảnh | Hiển thị Image component với src từ book.image, alt=book.title, width=300, height=300, className "w-full h-48 object-cover rounded-t-lg" | | Pass | 11/15/2015 | |
| **GUI-DS-11** | Kiểm tra Badge trạng thái | 1. Truy cập /user/products<br>2. Kiểm tra Badge | Hiển thị Badge "Mới" (bg-green-500) nếu isNew, Badge "Bán chạy" (bg-orange-500) nếu isBestseller, Badge "-X%" (variant destructive) nếu có discount, ở vị trí absolute top-2 left-2 | | Pass | 11/15/2015 | |
| **GUI-DS-12** | Kiểm tra nút yêu thích | 1. Truy cập /user/products<br>2. Kiểm tra nút | Hiển thị Button variant ghost size sm (h-8 w-8 p-0) ở absolute top-2 right-2, icon Heart với fill-red-500 text-red-500 nếu đã yêu thích, text-muted-foreground nếu chưa | | Pass | 11/15/2015 | |
| **GUI-DS-13** | Kiểm tra tên sách | 1. Truy cập /user/products<br>2. Kiểm tra tên | Hiển thị h3 với book.title (font-semibold text-lg mb-1 line-clamp-2) | | Pass | 11/15/2015 | |
| **GUI-DS-14** | Kiểm tra thông tin nhà xuất bản | 1. Truy cập /user/products<br>2. Kiểm tra thông tin | Hiển thị p với text "{book.brand} {book.series && `• ${book.series}`}" (text-sm text-muted-foreground mb-2) | | Pass | 11/15/2015 | |
| **GUI-DS-15** | Kiểm tra đánh giá sao | 1. Truy cập /user/products<br>2. Kiểm tra đánh giá | Hiển thị icon Star (h-4 w-4 fill-yellow-400 text-yellow-400), span với book.rating (text-sm font-medium), span với "({book.reviewCount})" (text-sm text-muted-foreground) | | Pass | 11/15/2015 | |
| **GUI-DS-16** | Kiểm tra giá sách | 1. Truy cập /user/products<br>2. Kiểm tra giá | Hiển thị span với book.price.toLocaleString("vi-VN") VNĐ (text-lg font-bold text-primary), nếu có originalPrice thì hiển thị span với originalPrice.toLocaleString("vi-VN") VNĐ (text-sm text-muted-foreground line-through ml-2) | | Pass | 11/15/2015 | |
| **GUI-DS-17** | Kiểm tra trạng thái tồn kho | 1. Truy cập /user/products<br>2. Kiểm tra trạng thái | Hiển thị text "Còn hàng (X)" (text-green-600) nếu stock > 0, "Hết hàng" (text-red-600) nếu stock = 0 (text-sm text-muted-foreground) | | Pass | 11/15/2015 | |
| **GUI-DS-18** | Kiểm tra nút Xem và Mua | 1. Truy cập /user/products<br>2. Kiểm tra nút | Hiển thị Button variant outline size sm với Link đến /user/products/{book.id}, icon Package và text "Xem", Button size sm với icon ShoppingCart và text "Mua", disabled nếu stock = 0 | | Pass | 11/15/2015 | |
| **GUI-DS-19** | Kiểm tra Card không có kết quả | 1. Truy cập /user/products<br>2. Áp dụng bộ lọc không có kết quả<br>3. Kiểm tra Card | Hiển thị Card với text-center py-12, icon Package (h-12 w-12 mx-auto text-muted-foreground mb-4), h3 "Không tìm thấy sách" (text-lg font-semibold mb-2), p "Thử thay đổi bộ lọc hoặc từ khóa tìm kiếm" (text-muted-foreground mb-4), Button "Xóa bộ lọc" variant outline | | Pass | 11/15/2015 | |

#### Check FUNC: Hiển thị danh sách sách

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DS-01** | Mở trang danh sách sách | 1. Truy cập /user/products | Hiển thị trang với tiêu đề, Card bộ lọc (danh mục, nhà xuất bản, sắp xếp, chế độ hiển thị, khoảng giá), thông tin số lượng, grid/list các Card sách với đầy đủ thông tin | | Pass | 11/15/2015 | |
| **FUNC-DS-02** | Lọc sách theo danh mục | 1. Truy cập /user/products<br>2. Chọn danh mục từ Select<br>3. Kiểm tra kết quả | Danh sách sách được lọc theo danh mục đã chọn, thông tin số lượng được cập nhật, chỉ hiển thị sách thuộc danh mục đó | | Pass | 11/15/2015 | |
| **FUNC-DS-03** | Lọc sách theo nhà xuất bản | 1. Truy cập /user/products<br>2. Chọn nhà xuất bản từ Select<br>3. Kiểm tra kết quả | Danh sách sách được lọc theo nhà xuất bản đã chọn, thông tin số lượng được cập nhật, chỉ hiển thị sách của nhà xuất bản đó | | Pass | 11/15/2015 | |
| **FUNC-DS-04** | Sắp xếp sách theo giá thấp đến cao | 1. Truy cập /user/products<br>2. Chọn "Giá thấp đến cao" từ SortControls<br>3. Kiểm tra kết quả | Danh sách sách được sắp xếp theo giá tăng dần, sách có giá thấp nhất ở đầu | | Pass | 11/15/2015 | |
| **FUNC-DS-05** | Sắp xếp sách theo giá cao đến thấp | 1. Truy cập /user/products<br>2. Chọn "Giá cao đến thấp" từ SortControls<br>3. Kiểm tra kết quả | Danh sách sách được sắp xếp theo giá giảm dần, sách có giá cao nhất ở đầu | | Pass | 11/15/2015 | |
| **FUNC-DS-06** | Sắp xếp sách theo đánh giá | 1. Truy cập /user/products<br>2. Chọn "Đánh giá cao nhất" từ SortControls<br>3. Kiểm tra kết quả | Danh sách sách được sắp xếp theo rating giảm dần, sách có rating cao nhất ở đầu | | Pass | 11/15/2015 | |
| **FUNC-DS-07** | Sắp xếp sách theo mới nhất | 1. Truy cập /user/products<br>2. Chọn "Mới nhất" từ SortControls<br>3. Kiểm tra kết quả | Danh sách sách được sắp xếp với sách có isNew = true ở đầu | | Pass | 11/15/2015 | |
| **FUNC-DS-08** | Lọc sách theo khoảng giá hợp lệ | 1. Truy cập /user/products<br>2. Kéo Slider khoảng giá<br>3. Kiểm tra kết quả | Danh sách sách được lọc theo khoảng giá đã chọn, chỉ hiển thị sách có giá trong khoảng đó, thông tin số lượng được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-DS-09** | Lọc sách theo khoảng giá không hợp lệ (min > max) | 1. Truy cập /user/products<br>2. Đặt giá tối thiểu > giá tối đa<br>3. Kiểm tra | Hiển thị toast.error "Giá tối thiểu không thể lớn hơn giá tối đa", giá không được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-DS-10** | Lọc sách theo khoảng giá âm | 1. Truy cập /user/products<br>2. Đặt giá tối thiểu < 0<br>3. Kiểm tra | Hiển thị toast.error "Giá tối thiểu không thể âm", giá được validate về 0 | | Pass | 11/15/2015 | |
| **FUNC-DS-11** | Lọc sách theo khoảng giá vượt quá giới hạn | 1. Truy cập /user/products<br>2. Đặt giá tối đa > 10.000.000<br>3. Kiểm tra | Hiển thị toast.error "Giá tối đa không được vượt quá 10.000.000 VNĐ", giá được validate về 10.000.000 | | Pass | 11/15/2015 | |
| **FUNC-DS-12** | Chuyển đổi chế độ hiển thị Grid | 1. Truy cập /user/products<br>2. Nhấn nút Grid | Hiển thị sách dạng grid với grid-cols-2 md:grid-cols-3 lg:grid-cols-6, nút Grid có variant default | | Pass | 11/15/2015 | |
| **FUNC-DS-13** | Chuyển đổi chế độ hiển thị List | 1. Truy cập /user/products<br>2. Nhấn nút List | Hiển thị sách dạng list với space-y-4, nút List có variant default | | Pass | 11/15/2015 | |
| **FUNC-DS-14** | Thêm sách vào yêu thích | 1. Truy cập /user/products<br>2. Nhấn nút Heart trên Card sách | Hiển thị toast.success "Đã thêm vào danh sách yêu thích", icon Heart chuyển sang fill-red-500 text-red-500, bookId được thêm vào favoriteBooks | | Pass | 11/15/2015 | |
| **FUNC-DS-15** | Xóa sách khỏi yêu thích | 1. Truy cập /user/products<br>2. Nhấn nút Heart trên Card sách đã yêu thích | Hiển thị toast.success "Đã xóa khỏi danh sách yêu thích", icon Heart chuyển về text-muted-foreground, bookId được xóa khỏi favoriteBooks | | Pass | 11/15/2015 | |
| **FUNC-DS-16** | Thêm sách vào giỏ hàng | 1. Truy cập /user/products<br>2. Nhấn nút "Mua" trên Card sách | Hiển thị toast.success "Đã thêm \"{book.title}\" vào giỏ hàng" | | Pass | 11/15/2015 | |
| **FUNC-DS-17** | Thêm sách hết hàng vào giỏ hàng | 1. Truy cập /user/products<br>2. Tìm sách hết hàng (stock = 0)<br>3. Nhấn nút "Mua" | Nút "Mua" bị disabled, không thể thêm vào giỏ hàng | | Pass | 11/15/2015 | |
| **FUNC-DS-18** | Nhấn nút Xem chi tiết | 1. Truy cập /user/products<br>2. Nhấn nút "Xem" trên Card sách | Chuyển đến trang /user/products/{book.id} | | Pass | 11/15/2015 | |
| **FUNC-DS-19** | Xóa bộ lọc khi không có kết quả | 1. Truy cập /user/products<br>2. Áp dụng bộ lọc không có kết quả<br>3. Nhấn nút "Xóa bộ lọc" | Tất cả bộ lọc được reset về mặc định (searchTerm="", selectedCategory="Tất cả", selectedBrand="Tất cả", priceRange=[0, 5000000]), danh sách sách hiển thị lại đầy đủ | | Pass | 11/15/2015 | |

### Function: Xem chi tiết thông tin sách

#### Check GUI: Xem chi tiết sách

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CT-01** | Kiểm tra Breadcrumb | 1. Truy cập /user/products/[id]<br>2. Kiểm tra Breadcrumb | Hiển thị Link đến /user với Button variant ghost size sm "Trang chủ" (icon ArrowLeft), text "/", Link đến /user/products với Button "Sách", text "/", span với model.title (text-sm text-muted-foreground) | | Pass | 11/15/2015 | |
| **GUI-CT-02** | Kiểm tra phần ảnh sách | 1. Truy cập /user/products/[id]<br>2. Kiểm tra phần ảnh | Hiển thị grid grid-cols-1 lg:grid-cols-2 gap-8, div aspect-square relative với Image fill, grid grid-cols-3 gap-2 với các ảnh thumbnail, ảnh được chọn có ring-2 ring-primary | | Pass | 11/15/2015 | |
| **GUI-CT-03** | Kiểm tra Badge trạng thái | 1. Truy cập /user/products/[id]<br>2. Kiểm tra Badge | Hiển thị Badge "Mới" (bg-green-500) nếu isNew, Badge "Bán chạy" (bg-orange-500) nếu isBestseller, Badge "-X%" (variant destructive) nếu có discount | | Pass | 11/15/2015 | |
| **GUI-CT-04** | Kiểm tra tên sách và tác giả | 1. Truy cập /user/products/[id]<br>2. Kiểm tra thông tin | Hiển thị h1 với model.title (text-3xl font-bold mb-2), p với "{model.brand} {model.series && `• ${model.series}`}" (text-muted-foreground mb-4) | | Pass | 11/15/2015 | |
| **GUI-CT-05** | Kiểm tra đánh giá tổng quan | 1. Truy cập /user/products/[id]<br>2. Kiểm tra đánh giá | Hiển thị icon Star (h-5 w-5 fill-yellow-400 text-yellow-400), span với model.rating (font-medium), span với "({model.reviewCount} đánh giá)" (text-muted-foreground) | | Pass | 11/15/2015 | |
| **GUI-CT-06** | Kiểm tra giá sách | 1. Truy cập /user/products/[id]<br>2. Kiểm tra giá | Hiển thị span với model.price.toLocaleString("vi-VN") VNĐ (text-3xl font-bold text-primary), nếu có originalPrice thì hiển thị span với originalPrice.toLocaleString("vi-VN") VNĐ (text-lg text-muted-foreground line-through ml-2) | | Pass | 11/15/2015 | |
| **GUI-CT-07** | Kiểm tra trạng thái tồn kho | 1. Truy cập /user/products/[id]<br>2. Kiểm tra trạng thái | Hiển thị Label "Tình trạng", nếu stock > 0: icon CheckCircle (h-4 w-4 text-green-600), text "Còn hàng (X sản phẩm)" (text-green-600 font-medium), nếu stock = 0: icon CheckCircle (h-4 w-4 text-red-600), text "Hết hàng" (text-red-600 font-medium) | | Pass | 11/15/2015 | |
| **GUI-CT-08** | Kiểm tra chọn số lượng | 1. Truy cập /user/products/[id]<br>2. Kiểm tra số lượng | Hiển thị Label "Số lượng", Button variant outline size sm với icon Minus (disabled nếu quantity <= 1), Input type number với value=quantity, min=1, max=stock, className w-20 text-center, Button variant outline size sm với icon Plus (disabled nếu quantity >= stock) | | Pass | 11/15/2015 | |
| **GUI-CT-09** | Kiểm tra nút Thêm vào giỏ hàng | 1. Truy cập /user/products/[id]<br>2. Kiểm tra nút | Hiển thị Button size lg className flex-1 với icon ShoppingCart và text "Thêm vào giỏ hàng", disabled nếu stock = 0 | | Pass | 11/15/2015 | |
| **GUI-CT-10** | Kiểm tra nút Yêu thích và Chia sẻ | 1. Truy cập /user/products/[id]<br>2. Kiểm tra nút | Hiển thị Button size lg variant outline với icon Heart (fill-red-500 text-red-500 nếu isFavorite), Button size lg variant outline với icon Share2 | | Pass | 11/15/2015 | |
| **GUI-CT-11** | Kiểm tra nút Mua ngay | 1. Truy cập /user/products/[id]<br>2. Kiểm tra nút | Hiển thị Button size lg className w-full với text "Mua ngay", disabled nếu stock = 0 | | Pass | 11/15/2015 | |
| **GUI-CT-12** | Kiểm tra Card Điểm nổi bật | 1. Truy cập /user/products/[id]<br>2. Kiểm tra Card | Hiển thị Card với CardTitle "Điểm nổi bật" (text-lg), CardContent có ul với các li, mỗi li có icon CheckCircle (h-4 w-4 text-green-600) và text feature | | Pass | 11/15/2015 | |
| **GUI-CT-13** | Kiểm tra Card Khuyến mãi đặc biệt | 1. Truy cập /user/products/[id]<br>2. Kiểm tra Card | Hiển thị Card với CardTitle "{productPromo.title}" (text-lg), CardDescription "Mã giảm cho riêng sản phẩm này", CardContent có Badge "Giảm giá", text mã code, thông tin mức giảm, giá gốc, giá sau giảm, thời gian áp dụng, điều kiện, Button "Áp dụng mã" hoặc "Xóa mã" | | Pass | 11/15/2015 | |
| **GUI-CT-14** | Kiểm tra Tabs nội dung | 1. Truy cập /user/products/[id]<br>2. Kiểm tra Tabs | Hiển thị Tabs với TabsList grid grid-cols-4, các TabsTrigger: "Mô tả", "Thông tin", "Đánh giá", "Vận chuyển" | | Pass | 11/15/2015 | |
| **GUI-CT-15** | Kiểm tra Tab Mô tả | 1. Truy cập /user/products/[id]<br>2. Click Tab "Mô tả" | Hiển thị Card với CardTitle "Mô tả sản phẩm", CardContent có p với model.detailedDescription (text-muted-foreground leading-relaxed), Button "Đọc thử", Button variant outline "Tải PDF mẫu" | | Pass | 11/15/2015 | |
| **GUI-CT-16** | Kiểm tra Tab Thông tin | 1. Truy cập /user/products/[id]<br>2. Click Tab "Thông tin" | Hiển thị Card với CardTitle "Thông tin", CardContent có grid grid-cols-2 gap-4 với các Label và p: Nhà xuất bản, Series, Chất liệu, Độ tuổi | | Pass | 11/15/2015 | |
| **GUI-CT-17** | Kiểm tra Tab Đánh giá | 1. Truy cập /user/products/[id]<br>2. Click Tab "Đánh giá" | Hiển thị Card với CardTitle "Đánh giá sản phẩm", CardDescription "{model.reviewCount} đánh giá từ khách hàng", CardContent có danh sách reviews với tên người dùng, Badge "Đã mua" nếu verified, ngày đánh giá, sao đánh giá, comment, các nút Hữu ích/Không hữu ích, Báo cáo | | Pass | 11/15/2015 | |
| **GUI-CT-18** | Kiểm tra Tab Vận chuyển | 1. Truy cập /user/products/[id]<br>2. Click Tab "Vận chuyển" | Hiển thị Card với CardTitle "Thông tin vận chuyển", CardContent có thông tin về phí vận chuyển và thời gian giao hàng | | Pass | 11/15/2015 | |

#### Check FUNC: Xem chi tiết sách

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CT-01** | Mở trang chi tiết sách | 1. Truy cập /user/products/[id] | Hiển thị trang với Breadcrumb, grid 2 cột (ảnh và thông tin), Badge trạng thái, tên sách, tác giả, đánh giá, giá, trạng thái tồn kho, chọn số lượng, các nút hành động, Card điểm nổi bật, Card khuyến mãi, Tabs nội dung | | Pass | 11/15/2015 | |
| **FUNC-CT-02** | Chọn ảnh thumbnail | 1. Truy cập /user/products/[id]<br>2. Click vào ảnh thumbnail | Ảnh chính được thay đổi thành ảnh thumbnail đã chọn, thumbnail được chọn có ring-2 ring-primary | | Pass | 11/15/2015 | |
| **FUNC-CT-03** | Tăng số lượng | 1. Truy cập /user/products/[id]<br>2. Nhấn nút Plus | Số lượng tăng lên 1, nút Plus bị disabled nếu quantity >= stock | | Pass | 11/15/2015 | |
| **FUNC-CT-04** | Giảm số lượng | 1. Truy cập /user/products/[id]<br>2. Nhấn nút Minus | Số lượng giảm xuống 1, nút Minus bị disabled nếu quantity <= 1 | | Pass | 11/15/2015 | |
| **FUNC-CT-05** | Nhập số lượng trực tiếp | 1. Truy cập /user/products/[id]<br>2. Nhập số lượng vào Input | Số lượng được cập nhật nếu giá trị >= 1 và <= stock, không cập nhật nếu ngoài khoảng này | | Pass | 11/15/2015 | |
| **FUNC-CT-06** | Thêm vào giỏ hàng | 1. Truy cập /user/products/[id]<br>2. Chọn số lượng<br>3. Nhấn "Thêm vào giỏ hàng" | Hiển thị toast.success "Đã thêm {quantity} \"{model.title}\" vào giỏ hàng" | | Pass | 11/15/2015 | |
| **FUNC-CT-07** | Thêm sách hết hàng vào giỏ hàng | 1. Truy cập /user/products/[id] (stock = 0)<br>2. Nhấn "Thêm vào giỏ hàng" | Nút bị disabled, không thể thêm vào giỏ hàng | | Pass | 11/15/2015 | |
| **FUNC-CT-08** | Mua ngay | 1. Truy cập /user/products/[id]<br>2. Chọn số lượng<br>3. Nhấn "Mua ngay" | Hiển thị toast.success "Chuyển đến trang thanh toán" | | Pass | 11/15/2015 | |
| **FUNC-CT-09** | Thêm vào yêu thích | 1. Truy cập /user/products/[id]<br>2. Nhấn nút Heart | Hiển thị toast.success "Đã thêm vào danh sách yêu thích", icon Heart chuyển sang fill-red-500 text-red-500, isFavorite = true | | Pass | 11/15/2015 | |
| **FUNC-CT-10** | Xóa khỏi yêu thích | 1. Truy cập /user/products/[id]<br>2. Nhấn nút Heart (đã yêu thích) | Hiển thị toast.success "Đã xóa khỏi danh sách yêu thích", icon Heart chuyển về mặc định, isFavorite = false | | Pass | 11/15/2015 | |
| **FUNC-CT-11** | Áp dụng mã khuyến mãi sản phẩm | 1. Truy cập /user/products/[id]<br>2. Nhấn nút "Áp dụng mã" | Hiển thị toast.success "Áp dụng mã giảm giá sản phẩm thành công", appliedProductCode được set, hiển thị text "Đã áp dụng mã {code}. Giá sau giảm sẽ thể hiện ở trang thanh toán.", nút chuyển thành "Xóa mã" | | Pass | 11/15/2015 | |
| **FUNC-CT-12** | Xóa mã khuyến mãi sản phẩm | 1. Truy cập /user/products/[id]<br>2. Áp dụng mã<br>3. Nhấn "Xóa mã" | Hiển thị toast.success "Đã xóa mã giảm giá sản phẩm", appliedProductCode = null, nút chuyển về "Áp dụng mã" | | Pass | 11/15/2015 | |
| **FUNC-CT-13** | Chuyển Tab | 1. Truy cập /user/products/[id]<br>2. Click các Tab | Nội dung Tab được hiển thị tương ứng: Mô tả, Thông tin, Đánh giá, Vận chuyển | | Pass | 11/15/2015 | |
| **FUNC-CT-14** | Đánh dấu đánh giá hữu ích | 1. Truy cập /user/products/[id]<br>2. Click Tab "Đánh giá"<br>3. Nhấn nút "Hữu ích" | Số lượng hữu ích tăng lên 1, nếu đã nhấn "Không hữu ích" trước đó thì số không hữu ích giảm 1, user = "up" | | Pass | 11/15/2015 | |
| **FUNC-CT-15** | Đánh dấu đánh giá không hữu ích | 1. Truy cập /user/products/[id]<br>2. Click Tab "Đánh giá"<br>3. Nhấn nút "Không hữu ích" | Số lượng không hữu ích tăng lên 1, nếu đã nhấn "Hữu ích" trước đó thì số hữu ích giảm 1, user = "down" | | Pass | 11/15/2015 | |
| **FUNC-CT-16** | Báo cáo đánh giá | 1. Truy cập /user/products/[id]<br>2. Click Tab "Đánh giá"<br>3. Nhấn nút "Báo cáo"<br>4. Chọn lý do và nhập mô tả<br>5. Nhấn "Gửi báo cáo" | Hiển thị Dialog với DialogTitle "Báo cáo đánh giá", có select lý do (spam, abuse, misinfo, other), Textarea mô tả, nút Hủy và Gửi báo cáo. Sau khi gửi, hiển thị toast.success "Đã gửi báo cáo đánh giá", Dialog đóng, Badge "Đã báo cáo" xuất hiện | | Pass | 11/15/2015 | |
| **FUNC-CT-17** | Nhấn nút Đọc thử | 1. Truy cập /user/products/[id]<br>2. Click Tab "Mô tả"<br>3. Nhấn nút "Đọc thử" | Chuyển đến trang /user/products/[id]/preview | | Pass | 11/15/2015 | |
| **FUNC-CT-18** | Tải PDF mẫu | 1. Truy cập /user/products/[id]<br>2. Click Tab "Mô tả"<br>3. Nhấn nút "Tải PDF mẫu" | Hiển thị toast.success "Đã tải PDF mẫu (demo)" | | Pass | 11/15/2015 | |

### Function: Hiển thị nội dung sách "đọc thử"

#### Check GUI: Đọc thử sách

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DT-01** | Kiểm tra tiêu đề trang | 1. Truy cập /user/products/[id]/preview<br>2. Kiểm tra tiêu đề | Hiển thị div flex items-center gap-2 với icon BookOpen (h-5 w-5), h1 "Đọc thử miễn phí" (text-xl font-semibold), Badge variant secondary "Sách #{bookId}" | | Pass | 11/15/2015 | |
| **GUI-DT-02** | Kiểm tra nút Đóng | 1. Truy cập /user/products/[id]/preview<br>2. Kiểm tra nút | Hiển thị Button variant ghost với icon X và text "Đóng" | | Pass | 11/15/2015 | |
| **GUI-DT-03** | Kiểm tra Card trình đọc | 1. Truy cập /user/products/[id]/preview<br>2. Kiểm tra Card | Hiển thị Card với CardHeader có CardTitle "Trang {current + 1} / {total}" (text-base), CardContent | | Pass | 11/15/2015 | |
| **GUI-DT-04** | Kiểm tra điều hướng trang | 1. Truy cập /user/products/[id]/preview<br>2. Kiểm tra nút | Hiển thị Button variant outline với icon ChevronLeft (disabled nếu current === 0), Button variant outline với icon ChevronRight (disabled nếu current === total - 1) | | Pass | 11/15/2015 | |
| **GUI-DT-05** | Kiểm tra thanh tiến độ | 1. Truy cập /user/products/[id]/preview<br>2. Kiểm tra thanh | Hiển thị Progress component với value = Math.round(((current + 1) / total) * 100), text-xs "Tiến độ đọc: {progress}%" (text-muted-foreground mt-1 text-center) | | Pass | 11/15/2015 | |
| **GUI-DT-06** | Kiểm tra ảnh trang sách | 1. Truy cập /user/products/[id]/preview<br>2. Kiểm tra ảnh | Hiển thị div relative w-full aspect-[3/4] với Image fill, src=pages[current], alt="Trang {current + 1}", className "object-contain bg-white" | | Pass | 11/15/2015 | |
| **GUI-DT-07** | Kiểm tra điểm điều hướng | 1. Truy cập /user/products/[id]/preview<br>2. Kiểm tra điểm | Hiển thị div flex items-center justify-center gap-2 với các button h-2 w-2 rounded-full, bg-primary nếu idx === current, bg-muted nếu không | | Pass | 11/15/2015 | |

#### Check FUNC: Đọc thử sách

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DT-01** | Mở trang đọc thử | 1. Truy cập /user/products/[id]/preview | Hiển thị trang với tiêu đề, nút Đóng, Card trình đọc với ảnh trang đầu tiên, điều hướng trang, thanh tiến độ, điểm điều hướng | | Pass | 11/15/2015 | |
| **FUNC-DT-02** | Chuyển sang trang sau | 1. Truy cập /user/products/[id]/preview<br>2. Nhấn nút ChevronRight | current tăng lên 1, ảnh trang được cập nhật, thanh tiến độ được cập nhật, CardTitle hiển thị "Trang {current + 1} / {total}", điểm điều hướng được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-DT-03** | Chuyển về trang trước | 1. Truy cập /user/products/[id]/preview<br>2. Ở trang > 1<br>3. Nhấn nút ChevronLeft | current giảm xuống 1, ảnh trang được cập nhật, thanh tiến độ được cập nhật, CardTitle hiển thị "Trang {current + 1} / {total}", điểm điều hướng được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-DT-04** | Disable nút Trang trước ở trang đầu | 1. Truy cập /user/products/[id]/preview<br>2. Ở trang đầu (current = 0)<br>3. Kiểm tra nút | Nút ChevronLeft bị disabled, không thể nhấn | | Pass | 11/15/2015 | |
| **FUNC-DT-05** | Disable nút Trang sau ở trang cuối | 1. Truy cập /user/products/[id]/preview<br>2. Ở trang cuối (current = total - 1)<br>3. Kiểm tra nút | Nút ChevronRight bị disabled, không thể nhấn | | Pass | 11/15/2015 | |
| **FUNC-DT-06** | Click vào điểm điều hướng | 1. Truy cập /user/products/[id]/preview<br>2. Click vào điểm điều hướng thứ X | current được set về X, ảnh trang được cập nhật, thanh tiến độ được cập nhật, CardTitle hiển thị "Trang {current + 1} / {total}" | | Pass | 11/15/2015 | |
| **FUNC-DT-07** | Tính toán tiến độ đọc | 1. Truy cập /user/products/[id]/preview<br>2. Chuyển trang<br>3. Kiểm tra tiến độ | progress = Math.round(((current + 1) / total) * 100), Progress value được cập nhật, text hiển thị đúng phần trăm | | Pass | 11/15/2015 | |
| **FUNC-DT-08** | Nhấn nút Đóng | 1. Truy cập /user/products/[id]/preview<br>2. Nhấn nút "Đóng" | Chuyển về trang /user/products/[id] | | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn MDX để dễ dàng quản lý và cập nhật test cases.*

