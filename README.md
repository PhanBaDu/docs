# Test Case Template - Chức năng bộ lọc sản phẩm - phân loại sản phẩm (User)

## Module Code
**Model Management Store: Chức năng bộ lọc sản phẩm - phân loại sản phẩm User**

## Test Requirement
1. Bộ lọc sản phẩm
2. Lọc theo danh mục
3. Lọc theo thương hiệu
4. Lọc theo khoảng giá
5. Lọc theo tỷ lệ (Scale)
6. Lọc theo đánh giá
7. Sắp xếp sản phẩm
8. Xóa bộ lọc

---

## Test Summary

### Người thực hiện Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 142 |
| **Fail** | 0 |
| **Untested** | 28 |
| **N/A** | 0 |
| **Number of Test cases** | 170 |

---

## Test Cases

### Function: Bộ lọc sản phẩm

#### Check GUI: Bộ lọc sản phẩm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-BL-01** | Kiểm tra tiêu đề bộ lọc | 1. Truy cập /user/products<br>2. Kiểm tra tiêu đề | Hiển thị text "Bộ lọc:" với icon Filter | | Pass | 11/15/2015 | |
| **GUI-BL-02** | Kiểm tra bộ lọc thể loại | 1. Truy cập /user/products<br>2. Kiểm tra dropdown thể loại | Hiển thị Select với các option: Tất cả, Gundam, Figure, Mô hình xe, Máy bay, Tàu chiến, Khác | | Pass | 11/15/2015 | |
| **GUI-BL-03** | Kiểm tra bộ lọc thương hiệu | 1. Truy cập /user/products<br>2. Kiểm tra dropdown thương hiệu | Hiển thị Select với các option: Tất cả, Bandai, Good Smile Company, Tamiya, Hasegawa, Kotobukiya, Max Factory | | Pass | 11/15/2015 | |
| **GUI-BL-04** | Kiểm tra slider khoảng giá | 1. Truy cập /user/products<br>2. Kiểm tra slider | Hiển thị Slider với label "Khoảng giá", giá trị từ 0 đến 5.000.000 VNĐ, hiển thị giá trị min và max hiện tại | | Pass | 11/15/2015 | |
| **GUI-BL-05** | Kiểm tra bộ lọc scale | 1. Truy cập /user/products<br>2. Kiểm tra dropdown scale | Hiển thị Select với các option: Tất cả, 1/144, 1/100, 1/72, 1/48, 1/24, 1/350, Khác | | Pass | 11/15/2015 | |
| **GUI-BL-06** | Kiểm tra bộ lọc tình trạng hàng | 1. Truy cập /user/products<br>2. Kiểm tra dropdown tình trạng | Hiển thị Select với các option: Tất cả, Đang bán, Chưa ra mắt, Hết hàng, Sắp có hàng | | Pass | 11/15/2015 | |
| **GUI-BL-07** | Kiểm tra bộ lọc rating | 1. Truy cập /user/products<br>2. Kiểm tra dropdown rating | Hiển thị Select với các option: Tất cả, 5 sao, 4 sao trở lên, 3 sao trở lên, 2 sao trở lên, 1 sao trở lên | | Pass | 11/15/2015 | |
| **GUI-BL-08** | Kiểm tra nút Xóa bộ lọc | 1. Truy cập /user/products<br>2. Áp dụng một số bộ lọc<br>3. Kiểm tra nút | Hiển thị nút "Xóa bộ lọc" variant outline, có thể click | | Pass | 11/15/2015 | |
| **GUI-BL-09** | Kiểm tra chế độ hiển thị Grid | 1. Truy cập /user/products<br>2. Kiểm tra nút Grid | Hiển thị nút với icon Grid3X3, có thể click để chuyển sang chế độ Grid | | Pass | 11/15/2015 | |
| **GUI-BL-10** | Kiểm tra chế độ hiển thị List | 1. Truy cập /user/products<br>2. Kiểm tra nút List | Hiển thị nút với icon List, có thể click để chuyển sang chế độ List | | Pass | 11/15/2015 | |
| **GUI-BL-11** | Kiểm tra tóm tắt kết quả | 1. Truy cập /user/products<br>2. Áp dụng bộ lọc<br>3. Kiểm tra tóm tắt | Hiển thị text "Hiển thị X trong tổng số Y mô hình" với giá trị được cập nhật sau khi lọc | | Pass | 11/15/2015 | |

---

### Check FUNC: Bộ lọc sản phẩm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-BL-01** | Lọc theo thể loại - Tất cả | 1. Truy cập /user/products<br>2. Chọn "Tất cả" từ dropdown thể loại<br>3. Kiểm tra kết quả | Hiển thị tất cả sản phẩm, không lọc theo thể loại | | Pass | 11/15/2015 | |
| **FUNC-BL-02** | Lọc theo thể loại - Gundam | 1. Truy cập /user/products<br>2. Chọn "Gundam" từ dropdown thể loại<br>3. Kiểm tra kết quả | Hiển thị chỉ sản phẩm thuộc thể loại Gundam, cập nhật tóm tắt kết quả | | Pass | 11/15/2015 | |
| **FUNC-BL-03** | Lọc theo thể loại - Figure | 1. Truy cập /user/products<br>2. Chọn "Figure" từ dropdown thể loại<br>3. Kiểm tra kết quả | Hiển thị chỉ sản phẩm thuộc thể loại Figure, cập nhật tóm tắt kết quả | | Pass | 11/15/2015 | |
| **FUNC-BL-04** | Lọc theo thể loại - Mô hình xe | 1. Truy cập /user/products<br>2. Chọn "Mô hình xe" từ dropdown thể loại<br>3. Kiểm tra kết quả | Hiển thị chỉ sản phẩm thuộc thể loại Mô hình xe, cập nhật tóm tắt kết quả | | Pass | 11/15/2015 | |
| **FUNC-BL-05** | Lọc theo thể loại - Máy bay | 1. Truy cập /user/products<br>2. Chọn "Máy bay" từ dropdown thể loại<br>3. Kiểm tra kết quả | Hiển thị chỉ sản phẩm thuộc thể loại Máy bay, cập nhật tóm tắt kết quả | | Pass | 11/15/2015 | |
| **FUNC-BL-06** | Lọc theo thể loại - Tàu chiến | 1. Truy cập /user/products<br>2. Chọn "Tàu chiến" từ dropdown thể loại<br>3. Kiểm tra kết quả | Hiển thị chỉ sản phẩm thuộc thể loại Tàu chiến, cập nhật tóm tắt kết quả | | Pass | 11/15/2015 | |
| **FUNC-BL-07** | Lọc theo thể loại - Khác | 1. Truy cập /user/products<br>2. Chọn "Khác" từ dropdown thể loại<br>3. Kiểm tra kết quả | Hiển thị chỉ sản phẩm thuộc thể loại Khác, cập nhật tóm tắt kết quả | | Pass | 11/15/2015 | |
| **FUNC-BL-08** | Lọc theo thương hiệu - Tất cả | 1. Truy cập /user/products<br>2. Chọn "Tất cả" từ dropdown thương hiệu<br>3. Kiểm tra kết quả | Hiển thị tất cả sản phẩm, không lọc theo thương hiệu | | Pass | 11/15/2015 | |
| **FUNC-BL-09** | Lọc theo thương hiệu - Bandai | 1. Truy cập /user/products<br>2. Chọn "Bandai" từ dropdown thương hiệu<br>3. Kiểm tra kết quả | Hiển thị chỉ sản phẩm của thương hiệu Bandai, cập nhật tóm tắt kết quả | | Pass | 11/15/2015 | |
| **FUNC-BL-10** | Lọc theo thương hiệu - Good Smile Company | 1. Truy cập /user/products<br>2. Chọn "Good Smile Company" từ dropdown thương hiệu<br>3. Kiểm tra kết quả | Hiển thị chỉ sản phẩm của thương hiệu Good Smile Company, cập nhật tóm tắt kết quả | | Pass | 11/15/2015 | |
| **FUNC-BL-11** | Lọc theo thương hiệu - Tamiya | 1. Truy cập /user/products<br>2. Chọn "Tamiya" từ dropdown thương hiệu<br>3. Kiểm tra kết quả | Hiển thị chỉ sản phẩm của thương hiệu Tamiya, cập nhật tóm tắt kết quả | | Pass | 11/15/2015 | |
| **FUNC-BL-12** | Lọc theo khoảng giá | 1. Truy cập /user/products<br>2. Điều chỉnh slider khoảng giá (VD: 500.000 - 2.000.000)<br>3. Kiểm tra kết quả | Hiển thị chỉ sản phẩm có giá trong khoảng đã chọn, cập nhật tóm tắt kết quả, hiển thị giá trị min và max | | Pass | 11/15/2015 | |
| **FUNC-BL-13** | Lọc theo khoảng giá - Giá min | 1. Truy cập /user/products<br>2. Điều chỉnh slider giá min<br>3. Kiểm tra kết quả | Hiển thị chỉ sản phẩm có giá >= giá min đã chọn | | Pass | 11/15/2015 | |
| **FUNC-BL-14** | Lọc theo khoảng giá - Giá max | 1. Truy cập /user/products<br>2. Điều chỉnh slider giá max<br>3. Kiểm tra kết quả | Hiển thị chỉ sản phẩm có giá <= giá max đã chọn | | Pass | 11/15/2015 | |
| **FUNC-BL-15** | Lọc theo scale - Tất cả | 1. Truy cập /user/products<br>2. Chọn "Tất cả" từ dropdown scale<br>3. Kiểm tra kết quả | Hiển thị tất cả sản phẩm, không lọc theo scale | | Pass | 11/15/2015 | |
| **FUNC-BL-16** | Lọc theo scale - 1/144 | 1. Truy cập /user/products<br>2. Chọn "1/144" từ dropdown scale<br>3. Kiểm tra kết quả | Hiển thị chỉ sản phẩm có scale 1/144, cập nhật tóm tắt kết quả | | Pass | 11/15/2015 | |
| **FUNC-BL-17** | Lọc theo scale - 1/100 | 1. Truy cập /user/products<br>2. Chọn "1/100" từ dropdown scale<br>3. Kiểm tra kết quả | Hiển thị chỉ sản phẩm có scale 1/100, cập nhật tóm tắt kết quả | | Pass | 11/15/2015 | |
| **FUNC-BL-18** | Lọc theo scale - 1/72 | 1. Truy cập /user/products<br>2. Chọn "1/72" từ dropdown scale<br>3. Kiểm tra kết quả | Hiển thị chỉ sản phẩm có scale 1/72, cập nhật tóm tắt kết quả | | Pass | 11/15/2015 | |
| **FUNC-BL-19** | Lọc theo scale - 1/48 | 1. Truy cập /user/products<br>2. Chọn "1/48" từ dropdown scale<br>3. Kiểm tra kết quả | Hiển thị chỉ sản phẩm có scale 1/48, cập nhật tóm tắt kết quả | | Pass | 11/15/2015 | |
| **FUNC-BL-20** | Lọc theo scale - 1/24 | 1. Truy cập /user/products<br>2. Chọn "1/24" từ dropdown scale<br>3. Kiểm tra kết quả | Hiển thị chỉ sản phẩm có scale 1/24, cập nhật tóm tắt kết quả | | Pass | 11/15/2015 | |
| **FUNC-BL-21** | Lọc theo scale - 1/350 | 1. Truy cập /user/products<br>2. Chọn "1/350" từ dropdown scale<br>3. Kiểm tra kết quả | Hiển thị chỉ sản phẩm có scale 1/350, cập nhật tóm tắt kết quả | | Pass | 11/15/2015 | |
| **FUNC-BL-22** | Lọc theo scale - Khác | 1. Truy cập /user/products<br>2. Chọn "Khác" từ dropdown scale<br>3. Kiểm tra kết quả | Hiển thị chỉ sản phẩm có scale khác các scale đã liệt kê, cập nhật tóm tắt kết quả | | Pass | 11/15/2015 | |
| **FUNC-BL-23** | Lọc theo tình trạng hàng - Tất cả | 1. Truy cập /user/products<br>2. Chọn "Tất cả" từ dropdown tình trạng<br>3. Kiểm tra kết quả | Hiển thị tất cả sản phẩm, không lọc theo tình trạng | | Pass | 11/15/2015 | |
| **FUNC-BL-24** | Lọc theo tình trạng hàng - Đang bán | 1. Truy cập /user/products<br>2. Chọn "Đang bán" từ dropdown tình trạng<br>3. Kiểm tra kết quả | Hiển thị chỉ sản phẩm đang bán (còn hàng), cập nhật tóm tắt kết quả | | Pass | 11/15/2015 | |
| **FUNC-BL-25** | Lọc theo tình trạng hàng - Chưa ra mắt | 1. Truy cập /user/products<br>2. Chọn "Chưa ra mắt" từ dropdown tình trạng<br>3. Kiểm tra kết quả | Hiển thị chỉ sản phẩm chưa ra mắt, cập nhật tóm tắt kết quả | | Pass | 11/15/2015 | |
| **FUNC-BL-26** | Lọc theo tình trạng hàng - Hết hàng | 1. Truy cập /user/products<br>2. Chọn "Hết hàng" từ dropdown tình trạng<br>3. Kiểm tra kết quả | Hiển thị chỉ sản phẩm hết hàng, cập nhật tóm tắt kết quả | | Pass | 11/15/2015 | |
| **FUNC-BL-27** | Lọc theo tình trạng hàng - Sắp có hàng | 1. Truy cập /user/products<br>2. Chọn "Sắp có hàng" từ dropdown tình trạng<br>3. Kiểm tra kết quả | Hiển thị chỉ sản phẩm sắp có hàng, cập nhật tóm tắt kết quả | | Pass | 11/15/2015 | |
| **FUNC-BL-28** | Lọc theo rating - Tất cả | 1. Truy cập /user/products<br>2. Chọn "Tất cả" từ dropdown rating<br>3. Kiểm tra kết quả | Hiển thị tất cả sản phẩm, không lọc theo rating | | Pass | 11/15/2015 | |
| **FUNC-BL-29** | Lọc theo rating - 5 sao | 1. Truy cập /user/products<br>2. Chọn "5 sao" từ dropdown rating<br>3. Kiểm tra kết quả | Hiển thị chỉ sản phẩm có rating = 5 sao, cập nhật tóm tắt kết quả | | Pass | 11/15/2015 | |
| **FUNC-BL-30** | Lọc theo rating - 4 sao trở lên | 1. Truy cập /user/products<br>2. Chọn "4 sao trở lên" từ dropdown rating<br>3. Kiểm tra kết quả | Hiển thị chỉ sản phẩm có rating >= 4 sao, cập nhật tóm tắt kết quả | | Pass | 11/15/2015 | |
| **FUNC-BL-31** | Lọc theo rating - 3 sao trở lên | 1. Truy cập /user/products<br>2. Chọn "3 sao trở lên" từ dropdown rating<br>3. Kiểm tra kết quả | Hiển thị chỉ sản phẩm có rating >= 3 sao, cập nhật tóm tắt kết quả | | Pass | 11/15/2015 | |
| **FUNC-BL-32** | Lọc theo rating - 2 sao trở lên | 1. Truy cập /user/products<br>2. Chọn "2 sao trở lên" từ dropdown rating<br>3. Kiểm tra kết quả | Hiển thị chỉ sản phẩm có rating >= 2 sao, cập nhật tóm tắt kết quả | | Pass | 11/15/2015 | |
| **FUNC-BL-33** | Lọc theo rating - 1 sao trở lên | 1. Truy cập /user/products<br>2. Chọn "1 sao trở lên" từ dropdown rating<br>3. Kiểm tra kết quả | Hiển thị chỉ sản phẩm có rating >= 1 sao, cập nhật tóm tắt kết quả | | Pass | 11/15/2015 | |
| **FUNC-BL-34** | Kết hợp nhiều bộ lọc | 1. Truy cập /user/products<br>2. Chọn thể loại, thương hiệu, khoảng giá, scale, tình trạng, rating<br>3. Kiểm tra kết quả | Hiển thị chỉ sản phẩm thỏa mãn tất cả điều kiện lọc, cập nhật tóm tắt kết quả | | Pass | 11/15/2015 | |
| **FUNC-BL-35** | Cập nhật kết quả real-time | 1. Truy cập /user/products<br>2. Thay đổi bộ lọc<br>3. Quan sát kết quả | Danh sách sản phẩm được cập nhật ngay lập tức khi thay đổi bộ lọc, không cần submit | | Pass | 11/15/2015 | |
| **FUNC-BL-36** | Xóa tất cả bộ lọc | 1. Truy cập /user/products<br>2. Áp dụng một số bộ lọc<br>3. Click nút "Xóa bộ lọc"<br>4. Kiểm tra kết quả | Tất cả bộ lọc được reset về "Tất cả", slider giá về 0-5.000.000, hiển thị lại tất cả sản phẩm, cập nhật tóm tắt kết quả | | Pass | 11/15/2015 | |
| **FUNC-BL-37** | Lọc không có kết quả | 1. Truy cập /user/products<br>2. Áp dụng bộ lọc không có sản phẩm nào thỏa mãn<br>3. Kiểm tra kết quả | Hiển thị thông báo "Không tìm thấy mô hình", "Thử thay đổi bộ lọc hoặc từ khóa tìm kiếm", nút "Xóa bộ lọc" | | Pass | 11/15/2015 | |

---

### Function: Sắp xếp sản phẩm

#### Check GUI: Sắp xếp sản phẩm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-SX-01** | Kiểm tra dropdown sắp xếp | 1. Truy cập /user/products<br>2. Kiểm tra dropdown | Hiển thị Select với các option: Liên quan, Giá thấp, Giá cao, Đánh giá, Mới nhất | | Pass | 11/15/2015 | |
| **GUI-SX-02** | Kiểm tra icon sắp xếp | 1. Truy cập /user/products<br>2. Kiểm tra icon | Có thể hiển thị icon SortAsc hoặc SortDesc tùy theo tiêu chí sắp xếp | | Pass | 11/15/2015 | |

---

### Check FUNC: Sắp xếp sản phẩm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-SX-01** | Sắp xếp theo liên quan | 1. Truy cập /user/products<br>2. Chọn "Liên quan" từ dropdown sắp xếp<br>3. Kiểm tra kết quả | Sản phẩm được sắp xếp theo độ liên quan (mặc định), không thay đổi thứ tự nếu không có từ khóa tìm kiếm | | Pass | 11/15/2015 | |
| **FUNC-SX-02** | Sắp xếp theo giá thấp đến cao | 1. Truy cập /user/products<br>2. Chọn "Giá thấp" từ dropdown sắp xếp<br>3. Kiểm tra kết quả | Sản phẩm được sắp xếp theo giá tăng dần (thấp nhất trước) | | Pass | 11/15/2015 | |
| **FUNC-SX-03** | Sắp xếp theo giá cao đến thấp | 1. Truy cập /user/products<br>2. Chọn "Giá cao" từ dropdown sắp xếp<br>3. Kiểm tra kết quả | Sản phẩm được sắp xếp theo giá giảm dần (cao nhất trước) | | Pass | 11/15/2015 | |
| **FUNC-SX-04** | Sắp xếp theo đánh giá | 1. Truy cập /user/products<br>2. Chọn "Đánh giá" từ dropdown sắp xếp<br>3. Kiểm tra kết quả | Sản phẩm được sắp xếp theo điểm đánh giá giảm dần (cao nhất trước) | | Pass | 11/15/2015 | |
| **FUNC-SX-05** | Sắp xếp theo mới nhất | 1. Truy cập /user/products<br>2. Chọn "Mới nhất" từ dropdown sắp xếp<br>3. Kiểm tra kết quả | Sản phẩm được sắp xếp theo sản phẩm mới nhất trước (isNew = true) | | Pass | 11/15/2015 | |
| **FUNC-SX-06** | Sắp xếp sau khi lọc | 1. Truy cập /user/products<br>2. Áp dụng bộ lọc<br>3. Chọn tiêu chí sắp xếp<br>4. Kiểm tra kết quả | Kết quả sau khi lọc được sắp xếp theo tiêu chí đã chọn | | Pass | 11/15/2015 | |
| **FUNC-SX-07** | Cập nhật sắp xếp real-time | 1. Truy cập /user/products<br>2. Thay đổi tiêu chí sắp xếp<br>3. Quan sát kết quả | Danh sách sản phẩm được sắp xếp lại ngay lập tức khi thay đổi tiêu chí | | Pass | 11/15/2015 | |
| **FUNC-SX-08** | Kết hợp lọc và sắp xếp | 1. Truy cập /user/products<br>2. Áp dụng bộ lọc (thể loại, thương hiệu)<br>3. Chọn tiêu chí sắp xếp<br>4. Kiểm tra kết quả | Kết quả được lọc trước, sau đó được sắp xếp theo tiêu chí đã chọn | | Pass | 11/15/2015 | |

---

### Function: Chuyển đổi chế độ xem

#### Check GUI: Chuyển đổi chế độ xem

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CDX-01** | Kiểm tra nút Grid | 1. Truy cập /user/products<br>2. Kiểm tra nút Grid | Hiển thị nút với icon Grid3X3, có thể click, có variant default khi đang ở chế độ Grid | | Pass | 11/15/2015 | |
| **GUI-CDX-02** | Kiểm tra nút List | 1. Truy cập /user/products<br>2. Kiểm tra nút List | Hiển thị nút với icon List, có thể click, có variant default khi đang ở chế độ List | | Pass | 11/15/2015 | |

---

### Check FUNC: Chuyển đổi chế độ xem

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CDX-01** | Chuyển sang chế độ Grid | 1. Truy cập /user/products<br>2. Click nút Grid<br>3. Kiểm tra hiển thị | Sản phẩm hiển thị dạng grid (lưới), mỗi sản phẩm là một card riêng biệt, nút Grid có variant default | | Pass | 11/15/2015 | |
| **FUNC-CDX-02** | Chuyển sang chế độ List | 1. Truy cập /user/products<br>2. Click nút List<br>3. Kiểm tra hiển thị | Sản phẩm hiển thị dạng list (danh sách), các sản phẩm xếp theo hàng dọc, nút List có variant default | | Pass | 11/15/2015 | |
| **FUNC-CDX-03** | Lưu trữ lựa chọn chế độ xem | 1. Truy cập /user/products<br>2. Chọn chế độ List<br>3. Đóng và mở lại trang<br>4. Kiểm tra chế độ | Chế độ List được lưu vào localStorage, vẫn giữ nguyên khi mở lại trang | | Untested | 11/15/2015 | |

---

*Template này được tạo theo chuẩn Markdown để dễ dàng quản lý và cập nhật test cases.*

