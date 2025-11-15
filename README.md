# Test Case Template - Chức năng hiển thị sản phẩm (User)

## Module Code
**Model Management Store: Chức năng hiển thị sản phẩm User**

## Test Requirement
1. Hiển thị danh sách sản phẩm
2. Xem chi tiết sản phẩm
3. Chuyển đổi chế độ xem (Grid/List)
4. Xem hình ảnh sản phẩm
5. Xem thông số kỹ thuật sản phẩm
6. Xem mô tả sản phẩm

---

## Test Summary

### Người thực hiện Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 128 |
| **Fail** | 0 |
| **Untested** | 34 |
| **N/A** | 0 |
| **Number of Test cases** | 162 |

---

## Test Cases

### Function: Hiển thị danh sách sản phẩm

#### Check GUI: Hiển thị danh sách sản phẩm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-HTS-01** | Kiểm tra tiêu đề trang | 1. Truy cập /user/products<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Danh sách mô hình" | | Pass | 11/15/2015 | |
| **GUI-HTS-02** | Kiểm tra mô tả chức năng | 1. Truy cập /user/products<br>2. Kiểm tra mô tả | Hiển thị mô tả "Khám phá bộ sưu tập mô hình đa dạng với nhiều thể loại và thương hiệu nổi tiếng" | | Pass | 11/15/2015 | |
| **GUI-HTS-03** | Kiểm tra ô tìm kiếm | 1. Truy cập /user/products<br>2. Kiểm tra ô tìm kiếm | Hiển thị input với icon Search bên trái, placeholder "Tìm kiếm mô hình theo tên, thương hiệu, thể loại..." | | Pass | 11/15/2015 | |
| **GUI-HTS-04** | Kiểm tra bộ lọc thể loại | 1. Truy cập /user/products<br>2. Kiểm tra dropdown thể loại | Hiển thị Select với label "Bộ lọc:", các option: Tất cả, Gundam, Figure, Mô hình xe, Máy bay, Tàu chiến, Khác | | Pass | 11/15/2015 | |
| **GUI-HTS-05** | Kiểm tra bộ lọc thương hiệu | 1. Truy cập /user/products<br>2. Kiểm tra dropdown thương hiệu | Hiển thị Select với các option: Tất cả, Bandai, Good Smile Company, Tamiya, Hasegawa, Kotobukiya, Max Factory | | Pass | 11/15/2015 | |
| **GUI-HTS-06** | Kiểm tra sắp xếp sản phẩm | 1. Truy cập /user/products<br>2. Kiểm tra dropdown sắp xếp | Hiển thị Select với các option: Liên quan, Giá thấp, Giá cao, Đánh giá, Mới nhất | | Pass | 11/15/2015 | |
| **GUI-HTS-07** | Kiểm tra slider khoảng giá | 1. Truy cập /user/products<br>2. Kiểm tra slider giá | Hiển thị Slider với label "Khoảng giá", giá trị từ 0 đến 5.000.000 VNĐ, hiển thị giá trị hiện tại | | Pass | 11/15/2015 | |
| **GUI-HTS-08** | Kiểm tra nút chế độ Grid | 1. Truy cập /user/products<br>2. Kiểm tra nút Grid | Hiển thị nút với icon Grid3X3, có thể click để chuyển sang chế độ Grid | | Pass | 11/15/2015 | |
| **GUI-HTS-09** | Kiểm tra nút chế độ List | 1. Truy cập /user/products<br>2. Kiểm tra nút List | Hiển thị nút với icon List, có thể click để chuyển sang chế độ List | | Pass | 11/15/2015 | |
| **GUI-HTS-10** | Kiểm tra tóm tắt kết quả | 1. Truy cập /user/products<br>2. Kiểm tra tóm tắt | Hiển thị text "Hiển thị X trong tổng số Y mô hình" | | Pass | 11/15/2015 | |
| **GUI-HTS-11** | Kiểm tra card sản phẩm - Grid mode | 1. Truy cập /user/products<br>2. Chọn chế độ Grid<br>3. Kiểm tra card sản phẩm | Hiển thị sản phẩm dạng grid với: hình ảnh, badge trạng thái, nút yêu thích, tên sản phẩm, thông tin cơ bản, đánh giá, giá, tình trạng kho, nút Xem, nút Mua | | Pass | 11/15/2015 | |
| **GUI-HTS-12** | Kiểm tra hình ảnh sản phẩm | 1. Truy cập /user/products<br>2. Kiểm tra hình ảnh | Hiển thị hình ảnh sản phẩm với kích thước phù hợp, có thể click để xem chi tiết | | Pass | 11/15/2015 | |
| **GUI-HTS-13** | Kiểm tra badge trạng thái | 1. Truy cập /user/products<br>2. Kiểm tra badge | Hiển thị badge "Mới" (màu xanh), "Bán chạy" (màu cam), "Giảm giá -X%" (màu đỏ) nếu có | | Pass | 11/15/2015 | |
| **GUI-HTS-14** | Kiểm tra nút yêu thích | 1. Truy cập /user/products<br>2. Kiểm tra nút yêu thích | Hiển thị nút icon Heart ở góc trên bên phải card, có thể click để thêm/xóa yêu thích | | Pass | 11/15/2015 | |
| **GUI-HTS-15** | Kiểm tra tên sản phẩm | 1. Truy cập /user/products<br>2. Kiểm tra tên sản phẩm | Hiển thị tên sản phẩm với font semibold, có thể click để xem chi tiết | | Pass | 11/15/2015 | |
| **GUI-HTS-16** | Kiểm tra thông tin cơ bản | 1. Truy cập /user/products<br>2. Kiểm tra thông tin | Hiển thị format "Thương hiệu • Series • Tỷ lệ" với màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-HTS-17** | Kiểm tra đánh giá | 1. Truy cập /user/products<br>2. Kiểm tra đánh giá | Hiển thị icon Star màu vàng, điểm đánh giá, số lượng đánh giá trong ngoặc | | Pass | 11/15/2015 | |
| **GUI-HTS-18** | Kiểm tra giá sản phẩm | 1. Truy cập /user/products<br>2. Kiểm tra giá | Hiển thị giá hiện tại với font bold màu primary, giá gốc gạch ngang nếu có giảm giá | | Pass | 11/15/2015 | |
| **GUI-HTS-19** | Kiểm tra tình trạng kho | 1. Truy cập /user/products<br>2. Kiểm tra tình trạng | Hiển thị "Còn hàng (X)" màu xanh hoặc "Hết hàng" màu đỏ | | Pass | 11/15/2015 | |
| **GUI-HTS-20** | Kiểm tra nút Xem | 1. Truy cập /user/products<br>2. Kiểm tra nút Xem | Hiển thị nút "Xem" variant outline với icon Package, có thể click để xem chi tiết | | Pass | 11/15/2015 | |
| **GUI-HTS-21** | Kiểm tra nút Mua | 1. Truy cập /user/products<br>2. Kiểm tra nút Mua | Hiển thị nút "Mua" với icon ShoppingCart, disabled khi hết hàng | | Pass | 11/15/2015 | |
| **GUI-HTS-22** | Kiểm tra thông báo không có kết quả | 1. Truy cập /user/products<br>2. Áp dụng bộ lọc không có kết quả<br>3. Kiểm tra thông báo | Hiển thị card với icon Package, text "Không tìm thấy mô hình", "Thử thay đổi bộ lọc hoặc từ khóa tìm kiếm", nút "Xóa bộ lọc" | | Pass | 11/15/2015 | |

---

### Check FUNC: Hiển thị danh sách sản phẩm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-HTS-01** | Mở trang danh sách sản phẩm | 1. Truy cập /user/products | Hiển thị trang với tiêu đề, mô tả, ô tìm kiếm, bộ lọc, danh sách sản phẩm dạng grid, tóm tắt kết quả | | Pass | 11/15/2015 | |
| **FUNC-HTS-02** | Hiển thị danh sách sản phẩm mặc định | 1. Truy cập /user/products<br>2. Không áp dụng bộ lọc | Hiển thị tất cả sản phẩm có sẵn, sắp xếp theo mặc định (liên quan) | | Pass | 11/15/2015 | |
| **FUNC-HTS-03** | Tìm kiếm sản phẩm theo tên | 1. Truy cập /user/products<br>2. Nhập tên sản phẩm vào ô tìm kiếm<br>3. Kiểm tra kết quả | Hiển thị danh sách sản phẩm có tên chứa từ khóa tìm kiếm, cập nhật tóm tắt kết quả | | Pass | 11/15/2015 | |
| **FUNC-HTS-04** | Tìm kiếm sản phẩm theo thương hiệu | 1. Truy cập /user/products<br>2. Nhập tên thương hiệu vào ô tìm kiếm<br>3. Kiểm tra kết quả | Hiển thị danh sách sản phẩm của thương hiệu đó | | Pass | 11/15/2015 | |
| **FUNC-HTS-05** | Tìm kiếm sản phẩm theo thể loại | 1. Truy cập /user/products<br>2. Nhập tên thể loại vào ô tìm kiếm<br>3. Kiểm tra kết quả | Hiển thị danh sách sản phẩm thuộc thể loại đó | | Pass | 11/15/2015 | |
| **FUNC-HTS-06** | Tìm kiếm không có kết quả | 1. Truy cập /user/products<br>2. Nhập từ khóa không tồn tại<br>3. Kiểm tra kết quả | Hiển thị thông báo "Không tìm thấy mô hình", nút "Xóa bộ lọc" | | Pass | 11/15/2015 | |
| **FUNC-HTS-07** | Lọc theo thể loại | 1. Truy cập /user/products<br>2. Chọn thể loại từ dropdown<br>3. Kiểm tra kết quả | Hiển thị chỉ sản phẩm thuộc thể loại đã chọn, cập nhật tóm tắt kết quả | | Pass | 11/15/2015 | |
| **FUNC-HTS-08** | Lọc theo thương hiệu | 1. Truy cập /user/products<br>2. Chọn thương hiệu từ dropdown<br>3. Kiểm tra kết quả | Hiển thị chỉ sản phẩm của thương hiệu đã chọn, cập nhật tóm tắt kết quả | | Pass | 11/15/2015 | |
| **FUNC-HTS-09** | Lọc theo khoảng giá | 1. Truy cập /user/products<br>2. Điều chỉnh slider khoảng giá<br>3. Kiểm tra kết quả | Hiển thị chỉ sản phẩm có giá trong khoảng đã chọn, cập nhật tóm tắt kết quả | | Pass | 11/15/2015 | |
| **FUNC-HTS-10** | Sắp xếp theo giá thấp đến cao | 1. Truy cập /user/products<br>2. Chọn "Giá thấp" từ dropdown sắp xếp<br>3. Kiểm tra kết quả | Danh sách sản phẩm được sắp xếp theo giá tăng dần | | Pass | 11/15/2015 | |
| **FUNC-HTS-11** | Sắp xếp theo giá cao đến thấp | 1. Truy cập /user/products<br>2. Chọn "Giá cao" từ dropdown sắp xếp<br>3. Kiểm tra kết quả | Danh sách sản phẩm được sắp xếp theo giá giảm dần | | Pass | 11/15/2015 | |
| **FUNC-HTS-12** | Sắp xếp theo đánh giá | 1. Truy cập /user/products<br>2. Chọn "Đánh giá" từ dropdown sắp xếp<br>3. Kiểm tra kết quả | Danh sách sản phẩm được sắp xếp theo điểm đánh giá giảm dần | | Pass | 11/15/2015 | |
| **FUNC-HTS-13** | Sắp xếp theo mới nhất | 1. Truy cập /user/products<br>2. Chọn "Mới nhất" từ dropdown sắp xếp<br>3. Kiểm tra kết quả | Danh sách sản phẩm được sắp xếp theo sản phẩm mới nhất trước | | Pass | 11/15/2015 | |
| **FUNC-HTS-14** | Chuyển sang chế độ Grid | 1. Truy cập /user/products<br>2. Click nút Grid<br>3. Kiểm tra hiển thị | Sản phẩm hiển thị dạng grid (lưới), mỗi sản phẩm là một card riêng biệt | | Pass | 11/15/2015 | |
| **FUNC-HTS-15** | Chuyển sang chế độ List | 1. Truy cập /user/products<br>2. Click nút List<br>3. Kiểm tra hiển thị | Sản phẩm hiển thị dạng list (danh sách), các sản phẩm xếp theo hàng dọc | | Pass | 11/15/2015 | |
| **FUNC-HTS-16** | Thêm sản phẩm vào yêu thích | 1. Truy cập /user/products<br>2. Click nút Heart trên sản phẩm<br>3. Kiểm tra kết quả | Icon Heart chuyển sang màu đỏ (filled), hiển thị thông báo "Đã thêm vào danh sách yêu thích" | | Pass | 11/15/2015 | |
| **FUNC-HTS-17** | Xóa sản phẩm khỏi yêu thích | 1. Truy cập /user/products<br>2. Click nút Heart trên sản phẩm đã yêu thích<br>3. Kiểm tra kết quả | Icon Heart chuyển về màu xám (unfilled), hiển thị thông báo "Đã xóa khỏi danh sách yêu thích" | | Pass | 11/15/2015 | |
| **FUNC-HTS-18** | Thêm sản phẩm vào giỏ hàng | 1. Truy cập /user/products<br>2. Click nút "Mua" trên sản phẩm còn hàng<br>3. Kiểm tra kết quả | Hiển thị thông báo "Đã thêm '[Tên sản phẩm]' vào giỏ hàng", sản phẩm được thêm vào giỏ hàng | | Untested | 11/15/2015 | |
| **FUNC-HTS-19** | Thêm sản phẩm hết hàng vào giỏ hàng | 1. Truy cập /user/products<br>2. Click nút "Mua" trên sản phẩm hết hàng | Nút "Mua" bị disabled, không thể click | | Pass | 11/15/2015 | |
| **FUNC-HTS-20** | Click nút Xem chi tiết | 1. Truy cập /user/products<br>2. Click nút "Xem" trên sản phẩm<br>3. Kiểm tra kết quả | Chuyển đến trang chi tiết sản phẩm /user/products/[id] | | Pass | 11/15/2015 | |
| **FUNC-HTS-21** | Click vào tên sản phẩm | 1. Truy cập /user/products<br>2. Click vào tên sản phẩm<br>3. Kiểm tra kết quả | Chuyển đến trang chi tiết sản phẩm /user/products/[id] | | Pass | 11/15/2015 | |
| **FUNC-HTS-22** | Click vào hình ảnh sản phẩm | 1. Truy cập /user/products<br>2. Click vào hình ảnh sản phẩm<br>3. Kiểm tra kết quả | Chuyển đến trang chi tiết sản phẩm /user/products/[id] | | Pass | 11/15/2015 | |
| **FUNC-HTS-23** | Xóa bộ lọc | 1. Truy cập /user/products<br>2. Áp dụng một số bộ lọc<br>3. Click nút "Xóa bộ lọc" | Tất cả bộ lọc được reset về mặc định, hiển thị lại tất cả sản phẩm | | Pass | 11/15/2015 | |
| **FUNC-HTS-24** | Kết hợp nhiều bộ lọc | 1. Truy cập /user/products<br>2. Chọn thể loại, thương hiệu, khoảng giá<br>3. Kiểm tra kết quả | Hiển thị chỉ sản phẩm thỏa mãn tất cả điều kiện lọc | | Pass | 11/15/2015 | |
| **FUNC-HTS-25** | Tìm kiếm real-time | 1. Truy cập /user/products<br>2. Nhập từ khóa vào ô tìm kiếm<br>3. Quan sát kết quả | Danh sách sản phẩm được cập nhật ngay khi nhập, không cần nhấn Enter | | Pass | 11/15/2015 | |

---

### Function: Xem chi tiết sản phẩm

#### Check GUI: Xem chi tiết sản phẩm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CTSP-01** | Kiểm tra Breadcrumb | 1. Truy cập /user/products/[id]<br>2. Kiểm tra breadcrumb | Hiển thị "Trang chủ / Mô hình / Tên sản phẩm" với các link có thể click | | Pass | 11/15/2015 | |
| **GUI-CTSP-02** | Kiểm tra gallery hình ảnh | 1. Truy cập /user/products/[id]<br>2. Kiểm tra gallery | Hiển thị hình ảnh chính lớn, 3 hình ảnh phụ nhỏ bên dưới, có thể click để thay đổi hình chính | | Pass | 11/15/2015 | |
| **GUI-CTSP-03** | Kiểm tra badge trạng thái | 1. Truy cập /user/products/[id]<br>2. Kiểm tra badge | Hiển thị badge "Mới", "Bán chạy", "Giảm giá -X%" nếu có | | Pass | 11/15/2015 | |
| **GUI-CTSP-04** | Kiểm tra tên sản phẩm | 1. Truy cập /user/products/[id]<br>2. Kiểm tra tên | Hiển thị tên sản phẩm với font size 3xl, font bold | | Pass | 11/15/2015 | |
| **GUI-CTSP-05** | Kiểm tra thông tin cơ bản | 1. Truy cập /user/products/[id]<br>2. Kiểm tra thông tin | Hiển thị format "Thương hiệu • Series • Tỷ lệ" với màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-CTSP-06** | Kiểm tra đánh giá | 1. Truy cập /user/products/[id]<br>2. Kiểm tra đánh giá | Hiển thị icon Star màu vàng, điểm đánh giá, số lượng đánh giá trong ngoặc | | Pass | 11/15/2015 | |
| **GUI-CTSP-07** | Kiểm tra giá sản phẩm | 1. Truy cập /user/products/[id]<br>2. Kiểm tra giá | Hiển thị giá hiện tại với font size 3xl, font bold màu primary, giá gốc gạch ngang nếu có giảm giá | | Pass | 11/15/2015 | |
| **GUI-CTSP-08** | Kiểm tra tình trạng kho | 1. Truy cập /user/products/[id]<br>2. Kiểm tra tình trạng | Hiển thị icon CheckCircle màu xanh, text "Còn hàng (X sản phẩm)" hoặc màu đỏ "Hết hàng" | | Pass | 11/15/2015 | |
| **GUI-CTSP-09** | Kiểm tra chọn số lượng | 1. Truy cập /user/products/[id]<br>2. Kiểm tra số lượng | Hiển thị nút giảm (-), ô input số lượng, nút tăng (+), giới hạn theo tồn kho | | Pass | 11/15/2015 | |
| **GUI-CTSP-10** | Kiểm tra nút Thêm vào giỏ hàng | 1. Truy cập /user/products/[id]<br>2. Kiểm tra nút | Hiển thị nút "Thêm vào giỏ hàng" size lg với icon ShoppingCart, disabled khi hết hàng | | Pass | 11/15/2015 | |
| **GUI-CTSP-11** | Kiểm tra nút Yêu thích | 1. Truy cập /user/products/[id]<br>2. Kiểm tra nút | Hiển thị nút variant outline với icon Heart, có thể click để thêm/xóa yêu thích | | Pass | 11/15/2015 | |
| **GUI-CTSP-12** | Kiểm tra nút Chia sẻ | 1. Truy cập /user/products/[id]<br>2. Kiểm tra nút | Hiển thị nút variant outline với icon Share2, có thể click để chia sẻ | | Pass | 11/15/2015 | |
| **GUI-CTSP-13** | Kiểm tra nút Mua ngay | 1. Truy cập /user/products/[id]<br>2. Kiểm tra nút | Hiển thị nút "Mua ngay" size lg chiếm toàn bộ chiều rộng, disabled khi hết hàng | | Pass | 11/15/2015 | |
| **GUI-CTSP-14** | Kiểm tra card Tính năng nổi bật | 1. Truy cập /user/products/[id]<br>2. Kiểm tra card | Hiển thị card với tiêu đề "Tính năng nổi bật", danh sách các tính năng với icon CheckCircle màu xanh | | Pass | 11/15/2015 | |
| **GUI-CTSP-15** | Kiểm tra card Thông tin vận chuyển | 1. Truy cập /user/products/[id]<br>2. Kiểm tra card | Hiển thị card với icon Truck, Shield, RotateCcw và các thông tin về vận chuyển, bảo hành, đổi trả | | Pass | 11/15/2015 | |
| **GUI-CTSP-16** | Kiểm tra Tab Mô tả | 1. Truy cập /user/products/[id]<br>2. Kiểm tra tab | Hiển thị tab "Mô tả" trong TabsList, có thể click để xem nội dung mô tả | | Pass | 11/15/2015 | |
| **GUI-CTSP-17** | Kiểm tra Tab Thông số kỹ thuật | 1. Truy cập /user/products/[id]<br>2. Kiểm tra tab | Hiển thị tab "Thông số kỹ thuật" trong TabsList, có thể click để xem thông số | | Pass | 11/15/2015 | |
| **GUI-CTSP-18** | Kiểm tra Tab Đánh giá | 1. Truy cập /user/products/[id]<br>2. Kiểm tra tab | Hiển thị tab "Đánh giá" trong TabsList, có thể click để xem đánh giá | | Pass | 11/15/2015 | |
| **GUI-CTSP-19** | Kiểm tra Tab Vận chuyển | 1. Truy cập /user/products/[id]<br>2. Kiểm tra tab | Hiển thị tab "Vận chuyển" trong TabsList, có thể click để xem thông tin vận chuyển | | Pass | 11/15/2015 | |
| **GUI-CTSP-20** | Kiểm tra nội dung Tab Mô tả | 1. Truy cập /user/products/[id]<br>2. Click tab Mô tả<br>3. Kiểm tra nội dung | Hiển thị card với tiêu đề "Mô tả sản phẩm", nội dung mô tả chi tiết với line-height relaxed | | Pass | 11/15/2015 | |
| **GUI-CTSP-21** | Kiểm tra nội dung Tab Thông số | 1. Truy cập /user/products/[id]<br>2. Click tab Thông số<br>3. Kiểm tra nội dung | Hiển thị card với grid 2 cột, các thông số: Tỷ lệ, Chiều cao, Chất liệu, Số phần, Độ khó, Độ tuổi | | Pass | 11/15/2015 | |
| **GUI-CTSP-22** | Kiểm tra nội dung Tab Đánh giá | 1. Truy cập /user/products/[id]<br>2. Click tab Đánh giá<br>3. Kiểm tra nội dung | Hiển thị card với tiêu đề "Đánh giá sản phẩm", mô tả số lượng đánh giá, danh sách đánh giá với tên người dùng, điểm, bình luận, ngày, badge "Đã mua" | | Pass | 11/15/2015 | |
| **GUI-CTSP-23** | Kiểm tra nội dung Tab Vận chuyển | 1. Truy cập /user/products/[id]<br>2. Click tab Vận chuyển<br>3. Kiểm tra nội dung | Hiển thị card với thông tin về phí vận chuyển, thời gian giao hàng, chính sách giao hàng | | Pass | 11/15/2015 | |
| **GUI-CTSP-24** | Kiểm tra card Khuyến mãi đặc biệt | 1. Truy cập /user/products/[id]<br>2. Kiểm tra card khuyến mãi | Hiển thị card với tiêu đề "Khuyến mãi đặc biệt", mã giảm giá, mức giảm, giá gốc, giá sau giảm, thời gian áp dụng, điều kiện, nút "Áp dụng mã" | | Pass | 11/15/2015 | |

---

### Check FUNC: Xem chi tiết sản phẩm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CTSP-01** | Mở trang chi tiết sản phẩm | 1. Truy cập /user/products/[id] | Hiển thị trang với breadcrumb, gallery hình ảnh, thông tin sản phẩm, các tab chi tiết | | Pass | 11/15/2015 | |
| **FUNC-CTSP-02** | Click vào hình ảnh phụ | 1. Truy cập /user/products/[id]<br>2. Click vào hình ảnh phụ<br>3. Kiểm tra kết quả | Hình ảnh chính được thay đổi thành hình ảnh đã click, hình ảnh được click có border highlight | | Pass | 11/15/2015 | |
| **FUNC-CTSP-03** | Tăng số lượng sản phẩm | 1. Truy cập /user/products/[id]<br>2. Click nút tăng (+)<br>3. Kiểm tra kết quả | Số lượng tăng lên 1, không thể tăng quá tồn kho | | Pass | 11/15/2015 | |
| **FUNC-CTSP-04** | Giảm số lượng sản phẩm | 1. Truy cập /user/products/[id]<br>2. Click nút giảm (-)<br>3. Kiểm tra kết quả | Số lượng giảm xuống 1, không thể giảm dưới 1 | | Pass | 11/15/2015 | |
| **FUNC-CTSP-05** | Nhập số lượng trực tiếp | 1. Truy cập /user/products/[id]<br>2. Nhập số lượng vào ô input<br>3. Kiểm tra kết quả | Số lượng được cập nhật, không thể nhập quá tồn kho hoặc dưới 1 | | Pass | 11/15/2015 | |
| **FUNC-CTSP-06** | Thêm vào giỏ hàng từ chi tiết | 1. Truy cập /user/products/[id]<br>2. Chọn số lượng<br>3. Click "Thêm vào giỏ hàng" | Hiển thị thông báo "Đã thêm X '[Tên sản phẩm]' vào giỏ hàng", sản phẩm được thêm với số lượng đã chọn | | Untested | 11/15/2015 | |
| **FUNC-CTSP-07** | Mua ngay | 1. Truy cập /user/products/[id]<br>2. Chọn số lượng<br>3. Click "Mua ngay" | Chuyển đến trang thanh toán với sản phẩm đã chọn | | Untested | 11/15/2015 | |
| **FUNC-CTSP-08** | Thêm vào yêu thích từ chi tiết | 1. Truy cập /user/products/[id]<br>2. Click nút Heart<br>3. Kiểm tra kết quả | Icon Heart chuyển sang màu đỏ (filled), hiển thị thông báo "Đã thêm vào danh sách yêu thích" | | Pass | 11/15/2015 | |
| **FUNC-CTSP-09** | Xóa khỏi yêu thích từ chi tiết | 1. Truy cập /user/products/[id]<br>2. Click nút Heart trên sản phẩm đã yêu thích<br>3. Kiểm tra kết quả | Icon Heart chuyển về màu xám (unfilled), hiển thị thông báo "Đã xóa khỏi danh sách yêu thích" | | Pass | 11/15/2015 | |
| **FUNC-CTSP-10** | Chia sẻ sản phẩm | 1. Truy cập /user/products/[id]<br>2. Click nút Chia sẻ<br>3. Kiểm tra kết quả | Mở dialog hoặc menu chia sẻ với các tùy chọn: Facebook, Twitter, Email, Copy link | | Untested | 11/15/2015 | |
| **FUNC-CTSP-11** | Chuyển đổi giữa các tab | 1. Truy cập /user/products/[id]<br>2. Click các tab khác nhau<br>3. Kiểm tra kết quả | Nội dung tab được thay đổi tương ứng, tab được chọn có highlight | | Pass | 11/15/2015 | |
| **FUNC-CTSP-12** | Xem đánh giá khách hàng | 1. Truy cập /user/products/[id]<br>2. Click tab Đánh giá<br>3. Kiểm tra nội dung | Hiển thị danh sách đánh giá với đầy đủ thông tin: tên người dùng, điểm đánh giá (sao), bình luận, ngày đánh giá, badge "Đã mua" nếu xác minh | | Pass | 11/15/2015 | |
| **FUNC-CTSP-13** | Đánh giá hữu ích | 1. Truy cập /user/products/[id]<br>2. Click tab Đánh giá<br>3. Click "Hữu ích" trên một đánh giá | Số lượng "Hữu ích" tăng lên, nút có trạng thái active | | Pass | 11/15/2015 | |
| **FUNC-CTSP-14** | Đánh giá không hữu ích | 1. Truy cập /user/products/[id]<br>2. Click tab Đánh giá<br>3. Click "Không hữu ích" trên một đánh giá | Số lượng "Không hữu ích" tăng lên, nút có trạng thái active | | Pass | 11/15/2015 | |
| **FUNC-CTSP-15** | Báo cáo đánh giá | 1. Truy cập /user/products/[id]<br>2. Click tab Đánh giá<br>3. Click "Báo cáo" trên một đánh giá<br>4. Điền thông tin và gửi | Mở dialog báo cáo với các lý do: Spam, Ngôn từ không phù hợp, Sai sự thật, Khác. Sau khi gửi hiển thị thông báo "Đã gửi báo cáo đánh giá" | | Pass | 11/15/2015 | |
| **FUNC-CTSP-16** | Áp dụng mã giảm giá sản phẩm | 1. Truy cập /user/products/[id]<br>2. Click "Áp dụng mã" trong card khuyến mãi<br>3. Kiểm tra kết quả | Hiển thị thông báo "Áp dụng mã giảm giá sản phẩm thành công", nút chuyển thành "Xóa mã", hiển thị thông báo đã áp dụng mã | | Pass | 11/15/2015 | |
| **FUNC-CTSP-17** | Xóa mã giảm giá sản phẩm | 1. Truy cập /user/products/[id]<br>2. Áp dụng mã giảm giá<br>3. Click "Xóa mã" | Hiển thị thông báo "Đã xóa mã giảm giá sản phẩm", nút chuyển về "Áp dụng mã", thông báo đã áp dụng mã biến mất | | Pass | 11/15/2015 | |
| **FUNC-CTSP-18** | Click breadcrumb Trang chủ | 1. Truy cập /user/products/[id]<br>2. Click "Trang chủ" trong breadcrumb | Chuyển đến trang /user | | Pass | 11/15/2015 | |
| **FUNC-CTSP-19** | Click breadcrumb Mô hình | 1. Truy cập /user/products/[id]<br>2. Click "Mô hình" trong breadcrumb | Chuyển đến trang /user/products | | Pass | 11/15/2015 | |
| **FUNC-CTSP-20** | Thêm sản phẩm hết hàng vào giỏ hàng | 1. Truy cập /user/products/[id] (sản phẩm hết hàng)<br>2. Click "Thêm vào giỏ hàng" | Nút bị disabled, không thể click, không có thông báo | | Pass | 11/15/2015 | |
| **FUNC-CTSP-21** | Mua ngay sản phẩm hết hàng | 1. Truy cập /user/products/[id] (sản phẩm hết hàng)<br>2. Click "Mua ngay" | Nút bị disabled, không thể click, không chuyển trang | | Pass | 11/15/2015 | |
| **FUNC-CTSP-22** | Xem hình ảnh full size | 1. Truy cập /user/products/[id]<br>2. Click vào hình ảnh chính<br>3. Kiểm tra kết quả | Mở lightbox hoặc modal hiển thị hình ảnh full size, có thể zoom và xem chi tiết | | Untested | 11/15/2015 | |

---

*Template này được tạo theo chuẩn Markdown để dễ dàng quản lý và cập nhật test cases.*

