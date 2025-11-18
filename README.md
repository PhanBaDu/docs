# Test Case Template - Bộ lọc sách (User)

## Module Code
**USER-004: Bộ lọc sách (User)**

## Test Requirement
1. Bộ lọc sách
2. Sắp xếp danh sách sách theo tiêu chí

---

## Test Summary

### Người thực hiện Test: Tester

| Status | Count |
|--------|-------|
| **Pass** | 48 |
| **Fail** | 0 |
| **Untested** | 0 |
| **N/A** | 0 |
| **Number of Test cases** | 48 |

---

## Test Cases

### Function: Bộ lọc sách

#### Check GUI: Bộ lọc sách

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-BL-01** | Kiểm tra Card bộ lọc | 1. Truy cập /user/products<br>2. Kiểm tra Card | Hiển thị Card với CardContent (p-6), có div space-y-4 | | Pass | 11/15/2015 | |
| **GUI-BL-02** | Kiểm tra tiêu đề bộ lọc | 1. Truy cập /user/products<br>2. Kiểm tra tiêu đề | Hiển thị div flex items-center gap-2 với icon Filter (h-4 w-4) và text "Bộ lọc:" (font-medium) | | Pass | 11/15/2015 | |
| **GUI-BL-03** | Kiểm tra Select danh mục | 1. Truy cập /user/products<br>2. Kiểm tra Select | Hiển thị Select với SelectTrigger (w-48), SelectValue placeholder "Danh mục", SelectContent có các options: Tất cả, Văn học, Truyện tranh - Manga, Công nghệ - Kỹ thuật, Kinh tế, Ảnh - Sách ảnh, Lịch sử, Khác | | Pass | 11/15/2015 | |
| **GUI-BL-04** | Kiểm tra Select nhà xuất bản | 1. Truy cập /user/products<br>2. Kiểm tra Select | Hiển thị Select với SelectTrigger (w-48), SelectValue placeholder "Nhà xuất bản", SelectContent có các options: Tất cả, NXB Kim Đồng, NXB Trẻ, NXB Tổng hợp, NXB Văn học, NXB Kinh tế | | Pass | 11/15/2015 | |
| **GUI-BL-05** | Kiểm tra Label khoảng giá | 1. Truy cập /user/products<br>2. Kiểm tra Label | Hiển thị label "Khoảng giá" (text-sm font-medium) | | Pass | 11/15/2015 | |
| **GUI-BL-06** | Kiểm tra Slider khoảng giá | 1. Truy cập /user/products<br>2. Kiểm tra Slider | Hiển thị Slider với value=priceRange, min=0, max=10000000, step=100000, className w-full, trong div với className px-3 | | Pass | 11/15/2015 | |
| **GUI-BL-07** | Kiểm tra hiển thị giá tối thiểu và tối đa | 1. Truy cập /user/products<br>2. Kiểm tra hiển thị | Hiển thị div flex justify-between text-sm text-muted-foreground mt-1 với span "Từ: {priceRange[0].toLocaleString('vi-VN')} VNĐ" và span "Đến: {priceRange[1].toLocaleString('vi-VN')} VNĐ" | | Pass | 11/15/2015 | |
| **GUI-BL-08** | Kiểm tra thông báo giới hạn giá | 1. Truy cập /user/products<br>2. Kiểm tra thông báo | Hiển thị p "Giá từ 0 đến 10.000.000 VNĐ" (text-xs text-muted-foreground mt-1) | | Pass | 11/15/2015 | |
| **GUI-BL-09** | Kiểm tra SortControls | 1. Truy cập /user/products<br>2. Kiểm tra SortControls | Hiển thị component SortControls với icon SortAsc (h-4 w-4), icon SortDesc (h-4 w-4 -ml-2), Label "Sắp xếp" (text-sm), Select với SelectTrigger (w-40) | | Pass | 11/15/2015 | |
| **GUI-BL-10** | Kiểm tra các options sắp xếp | 1. Truy cập /user/products<br>2. Mở Select sắp xếp<br>3. Kiểm tra options | Hiển thị SelectContent với các SelectItem: "Liên quan" (value="relevance"), "Giá thấp" (value="price-low"), "Giá cao" (value="price-high"), "Đánh giá" (value="rating"), "Mới nhất" (value="newest") | | Pass | 11/15/2015 | |
| **GUI-BL-11** | Kiểm tra nút chế độ hiển thị | 1. Truy cập /user/products<br>2. Kiểm tra nút | Hiển thị 2 Button: Grid (icon Grid3X3) và List (icon List), variant default khi active, outline khi không active, size sm | | Pass | 11/15/2015 | |
| **GUI-BL-12** | Kiểm tra thông tin số lượng kết quả | 1. Truy cập /user/products<br>2. Kiểm tra thông tin | Hiển thị p "Hiển thị {filteredBooks.length} trong tổng số {books.length} sách" (text-muted-foreground) | | Pass | 11/15/2015 | |

#### Check FUNC: Bộ lọc sách

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-BL-01** | Mở trang danh sách sách với bộ lọc | 1. Truy cập /user/products | Hiển thị trang với Card bộ lọc, các Select (danh mục, nhà xuất bản), SortControls, Slider khoảng giá, nút chế độ hiển thị, thông tin số lượng, danh sách sách | | Pass | 11/15/2015 | |
| **FUNC-BL-02** | Lọc sách theo danh mục | 1. Truy cập /user/products<br>2. Chọn danh mục từ Select<br>3. Kiểm tra kết quả | Danh sách sách được lọc theo danh mục đã chọn, chỉ hiển thị sách thuộc danh mục đó (matchesCategory = category === "Tất cả" \|\| book.category === category), thông tin số lượng được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-BL-03** | Lọc sách theo nhà xuất bản | 1. Truy cập /user/products<br>2. Chọn nhà xuất bản từ Select<br>3. Kiểm tra kết quả | Danh sách sách được lọc theo nhà xuất bản đã chọn, chỉ hiển thị sách của nhà xuất bản đó (matchesPublisher = publisher === "Tất cả" \|\| book.brand === publisher), thông tin số lượng được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-BL-04** | Lọc sách theo khoảng giá hợp lệ | 1. Truy cập /user/products<br>2. Kéo Slider khoảng giá<br>3. Kiểm tra kết quả | Danh sách sách được lọc theo khoảng giá đã chọn, chỉ hiển thị sách có giá trong khoảng đó (matchesPrice = book.price >= price[0] && book.price <= price[1]), giá tối thiểu và tối đa được hiển thị với toLocaleString("vi-VN"), thông tin số lượng được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-BL-05** | Lọc sách với giá tối thiểu = 0 | 1. Truy cập /user/products<br>2. Đặt giá tối thiểu = 0<br>3. Kiểm tra | Tất cả sách có giá >= 0 được hiển thị, không có lỗi | | Pass | 11/15/2015 | |
| **FUNC-BL-06** | Lọc sách với giá tối đa = 10.000.000 | 1. Truy cập /user/products<br>2. Đặt giá tối đa = 10.000.000<br>3. Kiểm tra | Tất cả sách có giá <= 10.000.000 được hiển thị, không có lỗi | | Pass | 11/15/2015 | |
| **FUNC-BL-07** | Lọc sách với giá tối thiểu < 0 | 1. Truy cập /user/products<br>2. Đặt giá tối thiểu < 0<br>3. Kiểm tra | Hiển thị toast.error "Giá tối thiểu không thể âm", giá được validate về 0 (Math.max(0, price[0])), bộ lọc không được áp dụng | | Pass | 11/15/2015 | |
| **FUNC-BL-08** | Lọc sách với giá tối đa > 10.000.000 | 1. Truy cập /user/products<br>2. Đặt giá tối đa > 10.000.000<br>3. Kiểm tra | Hiển thị toast.error "Giá tối đa không được vượt quá 10.000.000 VNĐ", giá được validate về 10.000.000 (Math.min(10000000, price[1])), bộ lọc không được áp dụng | | Pass | 11/15/2015 | |
| **FUNC-BL-09** | Lọc sách với giá tối thiểu > giá tối đa | 1. Truy cập /user/products<br>2. Đặt giá tối thiểu > giá tối đa<br>3. Kiểm tra | Hiển thị toast.error "Giá tối thiểu không thể lớn hơn giá tối đa", bộ lọc không được áp dụng | | Pass | 11/15/2015 | |
| **FUNC-BL-10** | Lọc sách kết hợp nhiều điều kiện | 1. Truy cập /user/products<br>2. Chọn danh mục<br>3. Chọn nhà xuất bản<br>4. Đặt khoảng giá<br>5. Kiểm tra kết quả | Kết quả được lọc theo tất cả điều kiện: danh mục, nhà xuất bản, và khoảng giá (matchesCategory && matchesPublisher && matchesPrice), chỉ hiển thị sách thỏa mãn tất cả điều kiện | | Pass | 11/15/2015 | |
| **FUNC-BL-11** | Lọc sách không có kết quả | 1. Truy cập /user/products<br>2. Áp dụng bộ lọc không có kết quả<br>3. Kiểm tra | Hiển thị Card với icon Package (h-12 w-12 mx-auto text-muted-foreground mb-4), h3 "Không tìm thấy sách" (text-lg font-semibold mb-2), p "Thử thay đổi bộ lọc hoặc từ khóa tìm kiếm" (text-muted-foreground mb-4), Button "Xóa bộ lọc" variant outline | | Pass | 11/15/2015 | |
| **FUNC-BL-12** | Xóa bộ lọc | 1. Truy cập /user/products<br>2. Áp dụng bộ lọc<br>3. Nhấn nút "Xóa bộ lọc" | Tất cả bộ lọc được reset về mặc định (selectedCategory="Tất cả", selectedBrand="Tất cả", priceRange=[0, 5000000]), danh sách sách hiển thị lại đầy đủ | | Pass | 11/15/2015 | |
| **FUNC-BL-13** | Cập nhật giá khi kéo Slider | 1. Truy cập /user/products<br>2. Kéo Slider<br>3. Kiểm tra | priceRange được cập nhật, giá tối thiểu và tối đa được hiển thị với toLocaleString("vi-VN"), kết quả lọc được cập nhật ngay lập tức | | Pass | 11/15/2015 | |
| **FUNC-BL-14** | Step của Slider | 1. Truy cập /user/products<br>2. Kéo Slider<br>3. Kiểm tra | Slider có step=100000, giá chỉ thay đổi theo bước 100.000 VNĐ | | Pass | 11/15/2015 | |

### Function: Sắp xếp danh sách sách theo tiêu chí

#### Check GUI: Sắp xếp sách

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-SX-01** | Kiểm tra SortControls component | 1. Truy cập /user/products<br>2. Kiểm tra SortControls | Hiển thị div với icon SortAsc (h-4 w-4), icon SortDesc (h-4 w-4 -ml-2), Label "Sắp xếp" (text-sm), Select với SelectTrigger (w-40), SelectValue hiển thị label của option đã chọn | | Pass | 11/15/2015 | |
| **GUI-SX-02** | Kiểm tra Select sắp xếp | 1. Truy cập /user/products<br>2. Click vào Select sắp xếp<br>3. Kiểm tra | Hiển thị SelectContent với các SelectItem: "Liên quan" (value="relevance"), "Giá thấp" (value="price-low"), "Giá cao" (value="price-high"), "Đánh giá" (value="rating"), "Mới nhất" (value="newest") | | Pass | 11/15/2015 | |

#### Check FUNC: Sắp xếp sách

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-SX-01** | Sắp xếp theo liên quan (mặc định) | 1. Truy cập /user/products<br>2. Chọn "Liên quan" từ Select sắp xếp<br>3. Kiểm tra | Danh sách sách được sắp xếp theo thứ tự mặc định (không sắp xếp, giữ nguyên thứ tự ban đầu), sortBy = "relevance" | | Pass | 11/15/2015 | |
| **FUNC-SX-02** | Sắp xếp theo giá thấp đến cao | 1. Truy cập /user/products<br>2. Chọn "Giá thấp" từ Select sắp xếp<br>3. Kiểm tra | Danh sách sách được sắp xếp theo giá tăng dần (a.price - b.price), sách có giá thấp nhất ở đầu, sortBy = "price-low" | | Pass | 11/15/2015 | |
| **FUNC-SX-03** | Sắp xếp theo giá cao đến thấp | 1. Truy cập /user/products<br>2. Chọn "Giá cao" từ Select sắp xếp<br>3. Kiểm tra | Danh sách sách được sắp xếp theo giá giảm dần (b.price - a.price), sách có giá cao nhất ở đầu, sortBy = "price-high" | | Pass | 11/15/2015 | |
| **FUNC-SX-04** | Sắp xếp theo đánh giá | 1. Truy cập /user/products<br>2. Chọn "Đánh giá" từ Select sắp xếp<br>3. Kiểm tra | Danh sách sách được sắp xếp theo rating giảm dần (b.rating - a.rating), sách có rating cao nhất ở đầu, sortBy = "rating" | | Pass | 11/15/2015 | |
| **FUNC-SX-05** | Sắp xếp theo mới nhất | 1. Truy cập /user/products<br>2. Chọn "Mới nhất" từ Select sắp xếp<br>3. Kiểm tra | Danh sách sách được sắp xếp với sách có isNew = true ở đầu ((b.isNew ? 1 : 0) - (a.isNew ? 1 : 0)), sortBy = "newest" | | Pass | 11/15/2015 | |
| **FUNC-SX-06** | Sắp xếp kết hợp với bộ lọc | 1. Truy cập /user/products<br>2. Áp dụng bộ lọc<br>3. Chọn tiêu chí sắp xếp<br>4. Kiểm tra | Kết quả được lọc trước, sau đó được sắp xếp theo tiêu chí đã chọn, thứ tự sắp xếp được áp dụng cho danh sách đã lọc | | Pass | 11/15/2015 | |
| **FUNC-SX-07** | Thay đổi tiêu chí sắp xếp | 1. Truy cập /user/products<br>2. Chọn tiêu chí sắp xếp A<br>3. Chọn tiêu chí sắp xếp B<br>4. Kiểm tra | Danh sách được sắp xếp lại theo tiêu chí B, sortBy được cập nhật, thứ tự sách thay đổi ngay lập tức | | Pass | 11/15/2015 | |
| **FUNC-SX-08** | Sắp xếp với sách có giá bằng nhau | 1. Truy cập /user/products<br>2. Có sách có giá bằng nhau<br>3. Sắp xếp theo giá<br>4. Kiểm tra | Sách có giá bằng nhau được giữ nguyên thứ tự tương đối (stable sort), không có lỗi | | Pass | 11/15/2015 | |
| **FUNC-SX-09** | Sắp xếp với sách có rating bằng nhau | 1. Truy cập /user/products<br>2. Có sách có rating bằng nhau<br>3. Sắp xếp theo đánh giá<br>4. Kiểm tra | Sách có rating bằng nhau được giữ nguyên thứ tự tương đối (stable sort), không có lỗi | | Pass | 11/15/2015 | |
| **FUNC-SX-10** | Sắp xếp với danh sách rỗng | 1. Truy cập /user/products<br>2. Áp dụng bộ lọc không có kết quả<br>3. Chọn tiêu chí sắp xếp<br>4. Kiểm tra | Không có lỗi, màn hình "Không tìm thấy sách" vẫn hiển thị | | Pass | 11/15/2015 | |
| **FUNC-SX-11** | Sắp xếp với 1 sách | 1. Truy cập /user/products<br>2. Áp dụng bộ lọc chỉ còn 1 sách<br>3. Chọn tiêu chí sắp xếp<br>4. Kiểm tra | Sách duy nhất vẫn hiển thị, không có lỗi | | Pass | 11/15/2015 | |
| **FUNC-SX-12** | Hiển thị SelectValue đúng | 1. Truy cập /user/products<br>2. Chọn tiêu chí sắp xếp<br>3. Kiểm tra SelectValue | SelectValue hiển thị label tương ứng với value đã chọn (ví dụ: "Giá thấp" khi value="price-low") | | Pass | 11/15/2015 | |
| **FUNC-SX-13** | Sắp xếp với sách có originalPrice | 1. Truy cập /user/products<br>2. Có sách có originalPrice<br>3. Sắp xếp theo giá<br>4. Kiểm tra | Sắp xếp dựa trên price (giá hiện tại), không phải originalPrice, thứ tự đúng | | Pass | 11/15/2015 | |
| **FUNC-SX-14** | Sắp xếp với sách không có isNew | 1. Truy cập /user/products<br>2. Có sách không có isNew<br>3. Sắp xếp theo mới nhất<br>4. Kiểm tra | Sách có isNew = true ở đầu, sách không có isNew (undefined/false) ở sau, không có lỗi | | Pass | 11/15/2015 | |
| **FUNC-SX-15** | Sắp xếp với sách có giá = 0 | 1. Truy cập /user/products<br>2. Có sách có giá = 0<br>3. Sắp xếp theo giá thấp<br>4. Kiểm tra | Sách có giá = 0 được hiển thị ở đầu danh sách, không có lỗi | | Pass | 11/15/2015 | |
| **FUNC-SX-16** | Sắp xếp với sách có rating = 0 | 1. Truy cập /user/products<br>2. Có sách có rating = 0<br>3. Sắp xếp theo đánh giá<br>4. Kiểm tra | Sách có rating = 0 được hiển thị ở cuối danh sách (vì sắp xếp giảm dần), không có lỗi | | Pass | 11/15/2015 | |
| **FUNC-SX-17** | Sắp xếp với nhiều sách | 1. Truy cập /user/products<br>2. Có nhiều sách<br>3. Sắp xếp theo giá<br>4. Kiểm tra | Tất cả sách được sắp xếp đúng thứ tự, không có sách nào bị thiếu hoặc trùng lặp | | Pass | 11/15/2015 | |
| **FUNC-SX-18** | Sắp xếp kết hợp với tìm kiếm | 1. Truy cập /user/products<br>2. Nhập từ khóa tìm kiếm<br>3. Chọn tiêu chí sắp xếp<br>4. Kiểm tra | Kết quả tìm kiếm được sắp xếp theo tiêu chí đã chọn, thứ tự đúng | | Pass | 11/15/2015 | |
| **FUNC-SX-19** | Thay đổi sắp xếp không làm mất bộ lọc | 1. Truy cập /user/products<br>2. Áp dụng bộ lọc<br>3. Chọn tiêu chí sắp xếp<br>4. Thay đổi tiêu chí sắp xếp<br>5. Kiểm tra | Bộ lọc vẫn được giữ nguyên, chỉ thứ tự sắp xếp thay đổi | | Pass | 11/15/2015 | |
| **FUNC-SX-20** | Thay đổi bộ lọc không làm mất sắp xếp | 1. Truy cập /user/products<br>2. Chọn tiêu chí sắp xếp<br>3. Thay đổi bộ lọc<br>4. Kiểm tra | Tiêu chí sắp xếp vẫn được giữ nguyên, kết quả lọc mới được sắp xếp theo tiêu chí đã chọn | | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn MDX để dễ dàng quản lý và cập nhật test cases.*

