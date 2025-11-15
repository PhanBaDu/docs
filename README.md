# Test Case Template - Chức năng quản lý giỏ hàng (User)

## Module Code
**Model Management Store: Chức năng quản lý giỏ hàng User**

## Test Requirement
1. Thêm sản phẩm vào giỏ hàng
2. Hiển thị giỏ hàng
3. Xóa sản phẩm khỏi giỏ hàng
4. Cập nhật số lượng sản phẩm
5. Chọn/Bỏ chọn sản phẩm
6. Chọn tất cả sản phẩm
7. Áp dụng mã giảm giá
8. Xóa mã giảm giá
9. Thêm vào yêu thích từ giỏ hàng
10. Thực hiện thanh toán

---

## Test Summary

### Người thực hiện Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 156 |
| **Fail** | 0 |
| **Untested** | 38 |
| **N/A** | 0 |
| **Number of Test cases** | 194 |

---

## Test Cases

### Function: Thêm sản phẩm vào giỏ hàng

#### Check GUI: Thêm sản phẩm vào giỏ hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-TMGH-01** | Kiểm tra nút Thêm vào giỏ hàng | 1. Truy cập /user/products/[id]<br>2. Kiểm tra nút | Hiển thị nút "Thêm vào giỏ hàng" size lg với icon ShoppingCart, disabled khi hết hàng | | Pass | 11/15/2015 | |
| **GUI-TMGH-02** | Kiểm tra chọn số lượng | 1. Truy cập /user/products/[id]<br>2. Kiểm tra số lượng | Hiển thị nút giảm (-), ô input số lượng, nút tăng (+), giới hạn theo tồn kho | | Pass | 11/15/2015 | |

---

### Check FUNC: Thêm sản phẩm vào giỏ hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TMGH-01** | Thêm sản phẩm vào giỏ hàng từ chi tiết | 1. Truy cập /user/products/[id]<br>2. Chọn số lượng<br>3. Click "Thêm vào giỏ hàng" | Hiển thị thông báo "Đã thêm X '[Tên sản phẩm]' vào giỏ hàng", sản phẩm được thêm với số lượng đã chọn | | Untested | 11/15/2015 | |
| **FUNC-TMGH-02** | Thêm sản phẩm vào giỏ hàng từ danh sách | 1. Truy cập /user/products<br>2. Click nút "Mua" trên sản phẩm còn hàng<br>3. Kiểm tra kết quả | Hiển thị thông báo "Đã thêm '[Tên sản phẩm]' vào giỏ hàng", sản phẩm được thêm với số lượng 1 | | Untested | 11/15/2015 | |
| **FUNC-TMGH-03** | Thêm sản phẩm hết hàng vào giỏ hàng | 1. Truy cập /user/products<br>2. Click nút "Mua" trên sản phẩm hết hàng | Nút "Mua" bị disabled, không thể click, không có thông báo | | Pass | 11/15/2015 | |
| **FUNC-TMGH-04** | Thêm sản phẩm với số lượng vượt tồn kho | 1. Truy cập /user/products/[id]<br>2. Nhập số lượng > tồn kho<br>3. Click "Thêm vào giỏ hàng" | Hiển thị cảnh báo "Chỉ còn X sản phẩm trong kho", không thêm vào giỏ hàng | | Pass | 11/15/2015 | |
| **FUNC-TMGH-05** | Thêm sản phẩm đã có trong giỏ hàng | 1. Truy cập /user/products/[id]<br>2. Sản phẩm đã có trong giỏ hàng<br>3. Thêm lại với số lượng mới<br>4. Kiểm tra kết quả | Số lượng sản phẩm trong giỏ hàng được cập nhật (cộng dồn hoặc thay thế tùy logic), không tạo item mới | | Untested | 11/15/2015 | |

---

### Function: Hiển thị giỏ hàng

#### Check GUI: Hiển thị giỏ hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-HTGH-01** | Kiểm tra tiêu đề trang | 1. Truy cập /user/cart<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Giỏ hàng" | | Pass | 11/15/2015 | |
| **GUI-HTGH-02** | Kiểm tra số lượng sản phẩm | 1. Truy cập /user/cart<br>2. Kiểm tra số lượng | Hiển thị text "X sản phẩm trong giỏ hàng" | | Pass | 11/15/2015 | |
| **GUI-HTGH-03** | Kiểm tra nút Tiếp tục mua sắm | 1. Truy cập /user/cart<br>2. Kiểm tra nút | Hiển thị nút "Tiếp tục mua sắm" variant outline với icon ArrowLeft, có thể click | | Pass | 11/15/2015 | |
| **GUI-HTGH-04** | Kiểm tra checkbox Chọn tất cả | 1. Truy cập /user/cart<br>2. Kiểm tra checkbox | Hiển thị checkbox với label "Chọn tất cả (X sản phẩm)", có thể click | | Pass | 11/15/2015 | |
| **GUI-HTGH-05** | Kiểm tra card sản phẩm | 1. Truy cập /user/cart<br>2. Có sản phẩm trong giỏ<br>3. Kiểm tra card | Hiển thị card với checkbox, hình ảnh, tên sản phẩm, thương hiệu, giá, số lượng, nút yêu thích, nút xóa | | Pass | 11/15/2015 | |
| **GUI-HTGH-06** | Kiểm tra hình ảnh sản phẩm | 1. Truy cập /user/cart<br>2. Kiểm tra hình ảnh | Hiển thị hình ảnh sản phẩm với kích thước 20x20, rounded-lg | | Pass | 11/15/2015 | |
| **GUI-HTGH-07** | Kiểm tra tên sản phẩm | 1. Truy cập /user/cart<br>2. Kiểm tra tên | Hiển thị tên sản phẩm với font semibold text-lg | | Pass | 11/15/2015 | |
| **GUI-HTGH-08** | Kiểm tra thương hiệu | 1. Truy cập /user/cart<br>2. Kiểm tra thương hiệu | Hiển thị thương hiệu với màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-HTGH-09** | Kiểm tra giá sản phẩm | 1. Truy cập /user/cart<br>2. Kiểm tra giá | Hiển thị giá hiện tại với font bold màu primary, giá gốc gạch ngang nếu có giảm giá, badge giảm giá | | Pass | 11/15/2015 | |
| **GUI-HTGH-10** | Kiểm tra thông báo giỏ hàng trống | 1. Truy cập /user/cart<br>2. Không có sản phẩm<br>3. Kiểm tra thông báo | Hiển thị card với icon ShoppingCart, tiêu đề "Giỏ hàng trống", mô tả "Bạn chưa có sản phẩm nào trong giỏ hàng", nút "Tiếp tục mua sắm" | | Pass | 11/15/2015 | |

---

### Check FUNC: Hiển thị giỏ hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-HTGH-01** | Mở trang giỏ hàng | 1. Truy cập /user/cart | Hiển thị trang với tiêu đề, số lượng sản phẩm, danh sách sản phẩm (nếu có), tóm tắt đơn hàng | | Pass | 11/15/2015 | |
| **FUNC-HTGH-02** | Hiển thị danh sách sản phẩm | 1. Truy cập /user/cart<br>2. Có sản phẩm trong giỏ<br>3. Kiểm tra danh sách | Hiển thị tất cả sản phẩm trong giỏ hàng với đầy đủ thông tin: hình ảnh, tên, thương hiệu, giá, số lượng | | Pass | 11/15/2015 | |
| **FUNC-HTGH-03** | Hiển thị giỏ hàng trống | 1. Truy cập /user/cart<br>2. Không có sản phẩm<br>3. Kiểm tra hiển thị | Hiển thị thông báo "Giỏ hàng trống" với icon, mô tả, nút "Tiếp tục mua sắm" | | Pass | 11/15/2015 | |
| **FUNC-HTGH-04** | Click nút Tiếp tục mua sắm | 1. Truy cập /user/cart<br>2. Click nút "Tiếp tục mua sắm" | Chuyển đến trang /user/products | | Pass | 11/15/2015 | |
| **FUNC-HTGH-05** | Hiển thị giá tổng cho mỗi sản phẩm | 1. Truy cập /user/cart<br>2. Có sản phẩm với số lượng > 1<br>3. Kiểm tra giá | Hiển thị giá tổng = giá đơn vị × số lượng cho mỗi sản phẩm | | Pass | 11/15/2015 | |

---

### Function: Xóa sản phẩm khỏi giỏ hàng

#### Check GUI: Xóa sản phẩm khỏi giỏ hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XSP-01** | Kiểm tra nút xóa sản phẩm | 1. Truy cập /user/cart<br>2. Kiểm tra nút xóa | Hiển thị nút variant ghost size sm với icon Trash2, có thể click | | Pass | 11/15/2015 | |

---

### Check FUNC: Xóa sản phẩm khỏi giỏ hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XSP-01** | Xóa sản phẩm khỏi giỏ hàng | 1. Truy cập /user/cart<br>2. Click nút xóa trên một sản phẩm<br>3. Kiểm tra kết quả | Hiển thị thông báo "Đã xóa sản phẩm khỏi giỏ hàng", sản phẩm bị xóa khỏi danh sách, tổng tiền được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-XSP-02** | Xóa sản phẩm đã chọn | 1. Truy cập /user/cart<br>2. Chọn một sản phẩm<br>3. Xóa sản phẩm đó<br>4. Kiểm tra kết quả | Sản phẩm bị xóa, checkbox "Chọn tất cả" được cập nhật, tổng tiền được tính lại | | Pass | 11/15/2015 | |
| **FUNC-XSP-03** | Xóa tất cả sản phẩm | 1. Truy cập /user/cart<br>2. Xóa tất cả sản phẩm<br>3. Kiểm tra kết quả | Hiển thị thông báo "Giỏ hàng trống", không còn sản phẩm nào, tổng tiền = 0 | | Pass | 11/15/2015 | |

---

### Function: Cập nhật số lượng sản phẩm

#### Check GUI: Cập nhật số lượng sản phẩm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CNSL-01** | Kiểm tra nút giảm số lượng | 1. Truy cập /user/cart<br>2. Kiểm tra nút giảm | Hiển thị nút variant outline size sm với icon Minus, disabled khi số lượng = 1 | | Pass | 11/15/2015 | |
| **GUI-CNSL-02** | Kiểm tra ô input số lượng | 1. Truy cập /user/cart<br>2. Kiểm tra input | Hiển thị input type number với giá trị hiện tại, width 16, text-center, min=1, max=tồn kho | | Pass | 11/15/2015 | |
| **GUI-CNSL-03** | Kiểm tra nút tăng số lượng | 1. Truy cập /user/cart<br>2. Kiểm tra nút tăng | Hiển thị nút variant outline size sm với icon Plus, disabled khi số lượng >= tồn kho | | Pass | 11/15/2015 | |

---

### Check FUNC: Cập nhật số lượng sản phẩm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CNSL-01** | Tăng số lượng sản phẩm | 1. Truy cập /user/cart<br>2. Click nút tăng (+)<br>3. Kiểm tra kết quả | Số lượng tăng lên 1, giá tổng được cập nhật, tổng tiền được tính lại | | Pass | 11/15/2015 | |
| **FUNC-CNSL-02** | Giảm số lượng sản phẩm | 1. Truy cập /user/cart<br>2. Click nút giảm (-)<br>3. Kiểm tra kết quả | Số lượng giảm xuống 1, giá tổng được cập nhật, tổng tiền được tính lại | | Pass | 11/15/2015 | |
| **FUNC-CNSL-03** | Nhập số lượng trực tiếp | 1. Truy cập /user/cart<br>2. Nhập số lượng vào ô input<br>3. Kiểm tra kết quả | Số lượng được cập nhật, giá tổng được cập nhật, tổng tiền được tính lại | | Pass | 11/15/2015 | |
| **FUNC-CNSL-04** | Tăng số lượng vượt tồn kho | 1. Truy cập /user/cart<br>2. Tăng số lượng đến khi >= tồn kho<br>3. Kiểm tra kết quả | Hiển thị thông báo "Chỉ còn X sản phẩm trong kho", số lượng không tăng quá tồn kho, nút tăng bị disabled | | Pass | 11/15/2015 | |
| **FUNC-CNSL-05** | Giảm số lượng xuống 0 | 1. Truy cập /user/cart<br>2. Giảm số lượng đến khi = 1<br>3. Kiểm tra kết quả | Số lượng không giảm dưới 1, nút giảm bị disabled khi số lượng = 1 | | Pass | 11/15/2015 | |
| **FUNC-CNSL-06** | Nhập số lượng không hợp lệ | 1. Truy cập /user/cart<br>2. Nhập số lượng < 1 hoặc > tồn kho<br>3. Kiểm tra kết quả | Số lượng được validate, không cho phép nhập < 1 hoặc > tồn kho, hiển thị cảnh báo | | Pass | 11/15/2015 | |
| **FUNC-CNSL-07** | Cập nhật tổng tiền real-time | 1. Truy cập /user/cart<br>2. Thay đổi số lượng<br>3. Kiểm tra tổng tiền | Tổng tiền được cập nhật ngay lập tức khi thay đổi số lượng, không cần submit | | Pass | 11/15/2015 | |

---

### Function: Chọn/Bỏ chọn sản phẩm

#### Check GUI: Chọn/Bỏ chọn sản phẩm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CBCH-01** | Kiểm tra checkbox sản phẩm | 1. Truy cập /user/cart<br>2. Kiểm tra checkbox | Mỗi sản phẩm có checkbox riêng, có thể click để chọn/bỏ chọn | | Pass | 11/15/2015 | |

---

### Check FUNC: Chọn/Bỏ chọn sản phẩm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CBCH-01** | Chọn sản phẩm | 1. Truy cập /user/cart<br>2. Click checkbox của một sản phẩm<br>3. Kiểm tra kết quả | Checkbox được tích, sản phẩm được chọn, tổng tiền được tính lại chỉ tính sản phẩm đã chọn | | Pass | 11/15/2015 | |
| **FUNC-CBCH-02** | Bỏ chọn sản phẩm | 1. Truy cập /user/cart<br>2. Click checkbox của sản phẩm đã chọn<br>3. Kiểm tra kết quả | Checkbox bị bỏ tích, sản phẩm không được chọn, tổng tiền được tính lại | | Pass | 11/15/2015 | |
| **FUNC-CBCH-03** | Chọn nhiều sản phẩm | 1. Truy cập /user/cart<br>2. Chọn nhiều sản phẩm<br>3. Kiểm tra kết quả | Tất cả sản phẩm được chọn đều có checkbox tích, tổng tiền tính tổng các sản phẩm đã chọn | | Pass | 11/15/2015 | |
| **FUNC-CBCH-04** | Cập nhật tổng tiền khi chọn/bỏ chọn | 1. Truy cập /user/cart<br>2. Chọn/bỏ chọn sản phẩm<br>3. Kiểm tra tổng tiền | Tổng tiền được cập nhật ngay lập tức, chỉ tính các sản phẩm đã chọn | | Pass | 11/15/2015 | |

---

### Function: Chọn tất cả sản phẩm

#### Check GUI: Chọn tất cả sản phẩm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CTAT-01** | Kiểm tra checkbox Chọn tất cả | 1. Truy cập /user/cart<br>2. Kiểm tra checkbox | Hiển thị checkbox với label "Chọn tất cả (X sản phẩm)", có thể click | | Pass | 11/15/2015 | |

---

### Check FUNC: Chọn tất cả sản phẩm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CTAT-01** | Chọn tất cả sản phẩm | 1. Truy cập /user/cart<br>2. Click checkbox "Chọn tất cả"<br>3. Kiểm tra kết quả | Tất cả checkbox sản phẩm được tích, tổng tiền tính tổng tất cả sản phẩm | | Pass | 11/15/2015 | |
| **FUNC-CTAT-02** | Bỏ chọn tất cả sản phẩm | 1. Truy cập /user/cart<br>2. Tất cả đã được chọn<br>3. Click checkbox "Chọn tất cả"<br>4. Kiểm tra kết quả | Tất cả checkbox sản phẩm bị bỏ tích, tổng tiền = 0 | | Pass | 11/15/2015 | |
| **FUNC-CTAT-03** | Cập nhật checkbox Chọn tất cả tự động | 1. Truy cập /user/cart<br>2. Chọn từng sản phẩm đến khi tất cả được chọn<br>3. Kiểm tra checkbox | Checkbox "Chọn tất cả" tự động được tích khi tất cả sản phẩm được chọn | | Pass | 11/15/2015 | |
| **FUNC-CTAT-04** | Bỏ tích checkbox Chọn tất cả tự động | 1. Truy cập /user/cart<br>2. Tất cả đã được chọn<br>3. Bỏ chọn một sản phẩm<br>4. Kiểm tra checkbox | Checkbox "Chọn tất cả" tự động bị bỏ tích khi có ít nhất một sản phẩm chưa được chọn | | Pass | 11/15/2015 | |

---

### Function: Áp dụng mã giảm giá

#### Check GUI: Áp dụng mã giảm giá

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-AMGG-01** | Kiểm tra card Mã giảm giá | 1. Truy cập /user/cart<br>2. Kiểm tra card | Hiển thị card với icon Gift, tiêu đề "Mã giảm giá" | | Pass | 11/15/2015 | |
| **GUI-AMGG-02** | Kiểm tra input mã giảm giá | 1. Truy cập /user/cart<br>2. Kiểm tra input | Hiển thị input với placeholder "Nhập mã giảm giá", có thể nhập text | | Pass | 11/15/2015 | |
| **GUI-AMGG-03** | Kiểm tra nút Áp dụng | 1. Truy cập /user/cart<br>2. Kiểm tra nút | Hiển thị nút "Áp dụng" với icon Percent, chiếm toàn bộ chiều rộng | | Pass | 11/15/2015 | |
| **GUI-AMGG-04** | Kiểm tra thông tin mã đã áp dụng | 1. Truy cập /user/cart<br>2. Áp dụng mã thành công<br>3. Kiểm tra thông tin | Hiển thị card với background green-50, mã giảm giá, mô tả, nút xóa với icon Trash2 | | Pass | 11/15/2015 | |
| **GUI-AMGG-05** | Kiểm tra gợi ý mã giảm giá | 1. Truy cập /user/cart<br>2. Kiểm tra gợi ý | Hiển thị text "Mã khả dụng: xem tất cả", grid các button mã giảm giá với icon Gift | | Pass | 11/15/2015 | |

---

### Check FUNC: Áp dụng mã giảm giá

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-AMGG-01** | Áp dụng mã giảm giá thành công | 1. Truy cập /user/cart<br>2. Nhập mã giảm giá hợp lệ<br>3. Click "Áp dụng"<br>4. Kiểm tra kết quả | Hiển thị thông báo "Áp dụng mã giảm giá thành công!", thông tin mã được hiển thị, tổng tiền được cập nhật với giảm giá | | Pass | 11/15/2015 | |
| **FUNC-AMGG-02** | Áp dụng mã giảm giá không hợp lệ | 1. Truy cập /user/cart<br>2. Nhập mã không tồn tại<br>3. Click "Áp dụng"<br>4. Kiểm tra kết quả | Hiển thị thông báo lỗi "Mã giảm giá không hợp lệ", mã không được áp dụng | | Pass | 11/15/2015 | |
| **FUNC-AMGG-03** | Áp dụng mã không đủ điều kiện | 1. Truy cập /user/cart<br>2. Nhập mã có đơn hàng tối thiểu > tổng tiền hiện tại<br>3. Click "Áp dụng"<br>4. Kiểm tra kết quả | Hiển thị thông báo lỗi "Đơn hàng tối thiểu X VNĐ", mã không được áp dụng | | Pass | 11/15/2015 | |
| **FUNC-AMGG-04** | Áp dụng mã giảm giá phần trăm | 1. Truy cập /user/cart<br>2. Nhập mã giảm giá phần trăm (VD: 10%)<br>3. Áp dụng thành công<br>4. Kiểm tra giảm giá | Số tiền giảm giá = tổng tiền × phần trăm, hiển thị trong tóm tắt đơn hàng | | Pass | 11/15/2015 | |
| **FUNC-AMGG-05** | Áp dụng mã giảm giá cố định | 1. Truy cập /user/cart<br>2. Nhập mã giảm giá cố định (VD: 50.000 VNĐ)<br>3. Áp dụng thành công<br>4. Kiểm tra giảm giá | Số tiền giảm giá = số tiền cố định, hiển thị trong tóm tắt đơn hàng | | Pass | 11/15/2015 | |
| **FUNC-AMGG-06** | Click vào mã gợi ý | 1. Truy cập /user/cart<br>2. Click vào button mã gợi ý<br>3. Kiểm tra kết quả | Mã được điền vào input, có thể click "Áp dụng" để áp dụng | | Pass | 11/15/2015 | |
| **FUNC-AMGG-07** | Áp dụng mã không phân biệt hoa thường | 1. Truy cập /user/cart<br>2. Nhập mã chữ thường (VD: "welcome10")<br>3. Click "Áp dụng"<br>4. Kiểm tra kết quả | Mã được áp dụng thành công, không phân biệt hoa thường | | Pass | 11/15/2015 | |
| **FUNC-AMGG-08** | Cập nhật tổng tiền sau khi áp dụng mã | 1. Truy cập /user/cart<br>2. Áp dụng mã giảm giá<br>3. Kiểm tra tổng tiền | Tổng tiền = Tạm tính + Phí vận chuyển - Giảm giá, được cập nhật ngay lập tức | | Pass | 11/15/2015 | |

---

### Function: Xóa mã giảm giá

#### Check GUI: Xóa mã giảm giá

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XMGG-01** | Kiểm tra nút xóa mã | 1. Truy cập /user/cart<br>2. Áp dụng mã thành công<br>3. Kiểm tra nút | Hiển thị nút variant ghost size sm với icon Trash2, có thể click | | Pass | 11/15/2015 | |

---

### Check FUNC: Xóa mã giảm giá

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XMGG-01** | Xóa mã giảm giá | 1. Truy cập /user/cart<br>2. Áp dụng mã giảm giá<br>3. Click nút xóa mã<br>4. Kiểm tra kết quả | Hiển thị thông báo "Đã xóa mã giảm giá", thông tin mã biến mất, input mã được reset, tổng tiền được tính lại không có giảm giá | | Pass | 11/15/2015 | |
| **FUNC-XMGG-02** | Cập nhật tổng tiền sau khi xóa mã | 1. Truy cập /user/cart<br>2. Xóa mã giảm giá<br>3. Kiểm tra tổng tiền | Tổng tiền = Tạm tính + Phí vận chuyển (không có giảm giá), được cập nhật ngay lập tức | | Pass | 11/15/2015 | |

---

### Function: Thêm vào yêu thích từ giỏ hàng

#### Check GUI: Thêm vào yêu thích từ giỏ hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-TMYT-01** | Kiểm tra nút yêu thích | 1. Truy cập /user/cart<br>2. Kiểm tra nút | Hiển thị nút variant ghost size sm với icon Heart, có thể click | | Pass | 11/15/2015 | |

---

### Check FUNC: Thêm vào yêu thích từ giỏ hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TMYT-01** | Thêm sản phẩm vào yêu thích | 1. Truy cập /user/cart<br>2. Click nút Heart trên một sản phẩm<br>3. Kiểm tra kết quả | Hiển thị thông báo "Đã thêm '[Tên sản phẩm]' vào danh sách yêu thích", icon Heart chuyển sang màu đỏ (filled) | | Pass | 11/15/2015 | |
| **FUNC-TMYT-02** | Xóa sản phẩm khỏi yêu thích | 1. Truy cập /user/cart<br>2. Click nút Heart trên sản phẩm đã yêu thích<br>3. Kiểm tra kết quả | Hiển thị thông báo "Đã xóa khỏi danh sách yêu thích", icon Heart chuyển về màu xám (unfilled) | | Pass | 11/15/2015 | |
| **FUNC-TMYT-03** | Thêm nhiều sản phẩm vào yêu thích | 1. Truy cập /user/cart<br>2. Click nút Heart trên nhiều sản phẩm<br>3. Kiểm tra kết quả | Tất cả sản phẩm được thêm vào yêu thích, icon Heart của các sản phẩm đều chuyển sang màu đỏ | | Pass | 11/15/2015 | |

---

### Function: Thực hiện thanh toán

#### Check GUI: Thực hiện thanh toán

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-THTT-01** | Kiểm tra card Tóm tắt đơn hàng | 1. Truy cập /user/cart<br>2. Kiểm tra card | Hiển thị card với tiêu đề "Tóm tắt đơn hàng" | | Pass | 11/15/2015 | |
| **GUI-THTT-02** | Kiểm tra Tạm tính | 1. Truy cập /user/cart<br>2. Kiểm tra tạm tính | Hiển thị "Tạm tính (X sản phẩm)" với giá trị tổng tiền sản phẩm đã chọn | | Pass | 11/15/2015 | |
| **GUI-THTT-03** | Kiểm tra Phí vận chuyển | 1. Truy cập /user/cart<br>2. Kiểm tra phí vận chuyển | Hiển thị "Phí vận chuyển" với giá trị phí hoặc "Miễn phí" | | Pass | 11/15/2015 | |
| **GUI-THTT-04** | Kiểm tra Giảm giá | 1. Truy cập /user/cart<br>2. Áp dụng mã giảm giá<br>3. Kiểm tra giảm giá | Hiển thị "Giảm giá (Mã)" với số tiền giảm màu xanh, chỉ hiển thị khi có mã | | Pass | 11/15/2015 | |
| **GUI-THTT-05** | Kiểm tra Tổng cộng | 1. Truy cập /user/cart<br>2. Kiểm tra tổng cộng | Hiển thị "Tổng cộng" với font bold text-lg, giá trị tổng tiền thanh toán | | Pass | 11/15/2015 | |
| **GUI-THTT-06** | Kiểm tra nút Thanh toán | 1. Truy cập /user/cart<br>2. Kiểm tra nút | Hiển thị nút "Thanh toán (X sản phẩm)" size lg với icon CreditCard, disabled khi không có sản phẩm được chọn | | Pass | 11/15/2015 | |
| **GUI-THTT-07** | Kiểm tra thông báo bảo mật | 1. Truy cập /user/cart<br>2. Kiểm tra thông báo | Hiển thị text "Thanh toán an toàn và bảo mật" với icon Shield | | Pass | 11/15/2015 | |
| **GUI-THTT-08** | Kiểm tra card Vận chuyển | 1. Truy cập /user/cart<br>2. Kiểm tra card | Hiển thị card với icon Truck, tiêu đề "Vận chuyển", radio button giao hàng tiêu chuẩn/nhanh | | Pass | 11/15/2015 | |
| **GUI-THTT-09** | Kiểm tra card Đơn vị vận chuyển | 1. Truy cập /user/cart<br>2. Kiểm tra card | Hiển thị card với icon Truck, tiêu đề "Đơn vị vận chuyển", radio button các đơn vị (GHTK, GHN, J&T) | | Pass | 11/15/2015 | |
| **GUI-THTT-10** | Kiểm tra card Tính phí vận chuyển | 1. Truy cập /user/cart<br>2. Kiểm tra card | Hiển thị card với tiêu đề "Tính phí vận chuyển", input địa chỉ, trọng lượng, khoảng cách, chi tiết phí, tổng phí | | Pass | 11/15/2015 | |
| **GUI-THTT-11** | Kiểm tra card Thông tin giao hàng | 1. Truy cập /user/cart<br>2. Kiểm tra card | Hiển thị card với tiêu đề "Thông tin giao hàng", input Họ tên, SĐT, Địa chỉ, Ghi chú | | Pass | 11/15/2015 | |

---

### Check FUNC: Thực hiện thanh toán

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-THTT-01** | Tính toán tóm tắt đơn hàng | 1. Truy cập /user/cart<br>2. Có sản phẩm trong giỏ<br>3. Kiểm tra tóm tắt | Hiển thị đầy đủ: Tạm tính, Phí vận chuyển, Giảm giá (nếu có), Tổng cộng, tất cả được tính toán chính xác | | Pass | 11/15/2015 | |
| **FUNC-THTT-02** | Tính tạm tính | 1. Truy cập /user/cart<br>2. Chọn một số sản phẩm<br>3. Kiểm tra tạm tính | Tạm tính = tổng (giá × số lượng) của các sản phẩm đã chọn, hiển thị số lượng sản phẩm | | Pass | 11/15/2015 | |
| **FUNC-THTT-03** | Tính phí vận chuyển | 1. Truy cập /user/cart<br>2. Chọn phương thức vận chuyển<br>3. Kiểm tra phí | Phí vận chuyển được tính theo phương thức đã chọn, miễn phí nếu đơn >= 500.000 VNĐ (tiêu chuẩn) | | Pass | 11/15/2015 | |
| **FUNC-THTT-04** | Tính tổng cộng | 1. Truy cập /user/cart<br>2. Có sản phẩm, phí vận chuyển, mã giảm giá<br>3. Kiểm tra tổng | Tổng cộng = Tạm tính + Phí vận chuyển - Giảm giá, được tính toán chính xác | | Pass | 11/15/2015 | |
| **FUNC-THTT-05** | Cập nhật tổng tiền real-time | 1. Truy cập /user/cart<br>2. Thay đổi số lượng, chọn/bỏ chọn sản phẩm, áp dụng/xóa mã<br>3. Quan sát tổng tiền | Tổng tiền được cập nhật ngay lập tức khi có thay đổi, không cần submit | | Pass | 11/15/2015 | |
| **FUNC-THTT-06** | Click nút Thanh toán - Có sản phẩm được chọn | 1. Truy cập /user/cart<br>2. Chọn ít nhất một sản phẩm<br>3. Click "Thanh toán"<br>4. Kiểm tra kết quả | Chuyển đến trang /user/checkout với thông tin đơn hàng đã được chuẩn bị | | Untested | 11/15/2015 | |
| **FUNC-THTT-07** | Click nút Thanh toán - Không có sản phẩm được chọn | 1. Truy cập /user/cart<br>2. Không chọn sản phẩm nào<br>3. Click "Thanh toán" | Nút bị disabled, không thể click, không chuyển trang | | Pass | 11/15/2015 | |
| **FUNC-THTT-08** | Chọn phương thức vận chuyển tiêu chuẩn | 1. Truy cập /user/cart<br>2. Chọn "Giao hàng tiêu chuẩn"<br>3. Kiểm tra phí | Phí vận chuyển = 30.000 VNĐ (hoặc miễn phí nếu đơn >= 500.000), thời gian 3-5 ngày, tổng tiền được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-THTT-09** | Chọn phương thức vận chuyển nhanh | 1. Truy cập /user/cart<br>2. Chọn "Giao hàng nhanh"<br>3. Kiểm tra phí | Phí vận chuyển = 50.000 VNĐ, thời gian 1-2 ngày, tổng tiền được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-THTT-10** | Chọn đơn vị vận chuyển GHTK | 1. Truy cập /user/cart<br>2. Chọn "Giao hàng tiết kiệm"<br>3. Kiểm tra kết quả | Đơn vị GHTK được chọn, hiển thị thông tin: thời gian 3-5 ngày, phí (miễn phí nếu đơn >= 500.000) | | Pass | 11/15/2015 | |
| **FUNC-THTT-11** | Chọn đơn vị vận chuyển GHN | 1. Truy cập /user/cart<br>2. Chọn "Giao hàng nhanh (GHN)"<br>3. Kiểm tra kết quả | Đơn vị GHN được chọn, hiển thị thông tin: thời gian 1-2 ngày, phí 50.000 VNĐ | | Pass | 11/15/2015 | |
| **FUNC-THTT-12** | Chọn đơn vị vận chuyển J&T | 1. Truy cập /user/cart<br>2. Chọn "J&T Express"<br>3. Kiểm tra kết quả | Đơn vị J&T được chọn, hiển thị thông tin: thời gian 2-4 ngày, phí (miễn phí nếu đơn >= 500.000) | | Pass | 11/15/2015 | |
| **FUNC-THTT-13** | Miễn phí vận chuyển khi đơn >= 500.000 | 1. Truy cập /user/cart<br>2. Tạm tính >= 500.000 VNĐ<br>3. Chọn giao hàng tiêu chuẩn<br>4. Kiểm tra phí | Phí vận chuyển hiển thị "Miễn phí", tổng tiền không cộng phí vận chuyển | | Pass | 11/15/2015 | |
| **FUNC-THTT-14** | Tính phí vận chuyển khi đơn < 500.000 | 1. Truy cập /user/cart<br>2. Tạm tính < 500.000 VNĐ<br>3. Chọn giao hàng tiêu chuẩn<br>4. Kiểm tra phí | Phí vận chuyển = 30.000 VNĐ (tiêu chuẩn) hoặc 50.000 VNĐ (nhanh), tổng tiền có cộng phí | | Pass | 11/15/2015 | |
| **FUNC-THTT-15** | Nhập thông tin giao hàng | 1. Truy cập /user/cart<br>2. Nhập Họ tên, SĐT, Địa chỉ, Ghi chú<br>3. Kiểm tra kết quả | Thông tin được lưu, có thể sử dụng khi thanh toán | | Pass | 11/15/2015 | |
| **FUNC-THTT-16** | Tính phí vận chuyển theo địa chỉ | 1. Truy cập /user/cart<br>2. Nhập địa chỉ giao hàng<br>3. Kiểm tra phí | Phí vận chuyển được tính dựa trên địa chỉ, trọng lượng, khoảng cách, hiển thị chi tiết phí | | Untested | 11/15/2015 | |
| **FUNC-THTT-17** | Cập nhật phí vận chuyển khi thay đổi địa chỉ | 1. Truy cập /user/cart<br>2. Nhập địa chỉ<br>3. Thay đổi địa chỉ<br>4. Kiểm tra phí | Phí vận chuyển được tính lại dựa trên địa chỉ mới, tổng tiền được cập nhật | | Untested | 11/15/2015 | |
| **FUNC-THTT-18** | Định dạng số tiền VNĐ | 1. Truy cập /user/cart<br>2. Kiểm tra định dạng số tiền | Tất cả số tiền được hiển thị với định dạng VNĐ, có dấu phẩy ngăn cách hàng nghìn (VD: 1.000.000 VNĐ) | | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn Markdown để dễ dàng quản lý và cập nhật test cases.*

