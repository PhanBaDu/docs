# Test Case Template - Quản lý giỏ hàng (User)

## Module Code
**USER-005: Quản lý giỏ hàng (User)**

## Test Requirement
1. Thêm sách vào giỏ hàng
2. Hiển thị danh sách sách trong giỏ
3. Xóa sách khỏi giỏ hàng
4. Chỉnh sửa số lượng sách
5. Đặt hàng

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

### Function: Thêm sách vào giỏ hàng

#### Check GUI: Thêm sách vào giỏ hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-TG-01** | Kiểm tra nút Thêm vào giỏ hàng ở trang chi tiết | 1. Truy cập /user/products/[id]<br>2. Kiểm tra nút | Hiển thị Button size lg className flex-1 với icon ShoppingCart (h-4 w-4 mr-2) và text "Thêm vào giỏ hàng", disabled nếu stock = 0 | | Pass | 11/15/2015 | |
| **GUI-TG-02** | Kiểm tra nút Mua ở trang danh sách | 1. Truy cập /user/products<br>2. Kiểm tra nút trên Card sách | Hiển thị Button size sm với icon ShoppingCart (h-3 w-3 mr-1) và text "Mua", disabled nếu stock = 0 | | Pass | 11/15/2015 | |
| **GUI-TG-03** | Kiểm tra chọn số lượng trước khi thêm | 1. Truy cập /user/products/[id]<br>2. Kiểm tra bộ chọn số lượng | Hiển thị Label "Số lượng", Button variant outline size sm với icon Minus (disabled nếu quantity <= 1), Input type number với value=quantity, min=1, max=stock, className w-20 text-center, Button variant outline size sm với icon Plus (disabled nếu quantity >= stock) | | Pass | 11/15/2015 | |

#### Check FUNC: Thêm sách vào giỏ hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TG-01** | Thêm sách vào giỏ hàng từ trang chi tiết | 1. Truy cập /user/products/[id]<br>2. Chọn số lượng<br>3. Nhấn "Thêm vào giỏ hàng" | Hiển thị toast.success "Đã thêm {quantity} \"{model.title}\" vào giỏ hàng", sách được thêm vào giỏ hàng với số lượng đã chọn | | Pass | 11/15/2015 | |
| **FUNC-TG-02** | Thêm sách vào giỏ hàng từ trang danh sách | 1. Truy cập /user/products<br>2. Nhấn nút "Mua" trên Card sách | Hiển thị toast.success "Đã thêm \"{book.title}\" vào giỏ hàng", sách được thêm vào giỏ hàng với số lượng = 1 | | Pass | 11/15/2015 | |
| **FUNC-TG-03** | Thêm sách hết hàng vào giỏ hàng | 1. Truy cập /user/products/[id] (stock = 0)<br>2. Nhấn "Thêm vào giỏ hàng" | Nút bị disabled, không thể thêm vào giỏ hàng | | Pass | 11/15/2015 | |
| **FUNC-TG-04** | Thêm sách đã có trong giỏ hàng | 1. Truy cập /user/products/[id]<br>2. Sách đã có trong giỏ hàng<br>3. Thêm lại | Số lượng sách trong giỏ hàng được cộng thêm, không tạo mục mới | | Pass | 11/15/2015 | |
| **FUNC-TG-05** | Thêm sách với số lượng vượt quá tồn kho | 1. Truy cập /user/products/[id]<br>2. Chọn số lượng > stock<br>3. Nhấn "Thêm vào giỏ hàng" | Không thể thêm, hiển thị thông báo lỗi về tồn kho không đủ | | Pass | 11/15/2015 | |
| **FUNC-TG-06** | Kiểm tra giới hạn số lượng tối đa mỗi sản phẩm | 1. Truy cập /user/cart<br>2. Tăng số lượng > MAX_QUANTITY_PER_ITEM (50) | Hiển thị toast.error "Số lượng tối đa cho mỗi sản phẩm là 50", số lượng không được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-TG-07** | Kiểm tra giới hạn số sản phẩm tối đa trong giỏ | 1. Truy cập /user/cart<br>2. Thêm sản phẩm đến khi đạt MAX_CART_ITEMS (20)<br>3. Thêm sản phẩm thứ 21 | Hiển thị Card cảnh báo "Bạn đã đạt giới hạn tối đa 20 sản phẩm trong giỏ hàng. Vui lòng xóa bớt sản phẩm để thêm sản phẩm mới." (border-orange-200 bg-orange-50), không thể thêm sản phẩm mới | | Pass | 11/15/2015 | |

### Function: Hiển thị danh sách sách trong giỏ

#### Check GUI: Hiển thị giỏ hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-HT-01** | Kiểm tra tiêu đề trang | 1. Truy cập /user/cart<br>2. Kiểm tra tiêu đề | Hiển thị h1 "Giỏ hàng" (text-3xl font-bold), p "{cartItems.length} sản phẩm trong giỏ hàng" (text-muted-foreground) | | Pass | 11/15/2015 | |
| **GUI-HT-02** | Kiểm tra nút Tiếp tục mua sắm | 1. Truy cập /user/cart<br>2. Kiểm tra nút | Hiển thị Link đến /user với Button variant outline size sm, icon ArrowLeft (h-4 w-4 mr-2) và text "Tiếp tục mua sắm" | | Pass | 11/15/2015 | |
| **GUI-HT-03** | Kiểm tra Card chọn tất cả | 1. Truy cập /user/cart<br>2. Kiểm tra Card | Hiển thị Card với CardContent (p-4), Checkbox checked nếu tất cả items đã được chọn, Label "Chọn tất cả ({cartItems.length} sản phẩm)" | | Pass | 11/15/2015 | |
| **GUI-HT-04** | Kiểm tra Card sản phẩm trong giỏ | 1. Truy cập /user/cart<br>2. Kiểm tra Card | Hiển thị Card với CardContent (p-4), có Checkbox, ảnh bìa (w-20 h-20 rounded-lg), tên sách, tác giả, giá, số lượng, nút yêu thích, nút xóa | | Pass | 11/15/2015 | |
| **GUI-HT-05** | Kiểm tra ảnh bìa sách | 1. Truy cập /user/cart<br>2. Kiểm tra ảnh | Hiển thị div relative w-20 h-20 rounded-lg overflow-hidden với Image fill, src=item.image, alt=item.title, className object-cover | | Pass | 11/15/2015 | |
| **GUI-HT-06** | Kiểm tra thông tin sách | 1. Truy cập /user/cart<br>2. Kiểm tra thông tin | Hiển thị h3 với item.title (font-semibold text-lg), p với item.brand (text-muted-foreground), span với item.price.toLocaleString("vi-VN") VNĐ (font-bold text-primary), nếu có originalPrice thì hiển thị span với originalPrice.toLocaleString("vi-VN") VNĐ (text-sm text-muted-foreground line-through), nếu có discount thì hiển thị Badge variant destructive "-{item.discount}%" (text-xs) | | Pass | 11/15/2015 | |
| **GUI-HT-07** | Kiểm tra bộ chọn số lượng | 1. Truy cập /user/cart<br>2. Kiểm tra bộ chọn | Hiển thị div flex items-center gap-2 với Button variant outline size sm icon Minus (disabled nếu quantity <= 1), Input type number với value=item.quantity, className w-16 text-center, min=1, max=item.stock, Button variant outline size sm icon Plus (disabled nếu quantity >= stock) | | Pass | 11/15/2015 | |
| **GUI-HT-08** | Kiểm tra nút yêu thích và xóa | 1. Truy cập /user/cart<br>2. Kiểm tra nút | Hiển thị Button variant ghost size sm với icon Heart (h-4 w-4), Button variant ghost size sm với icon Trash2 (h-4 w-4) | | Pass | 11/15/2015 | |
| **GUI-HT-09** | Kiểm tra màn hình giỏ hàng trống | 1. Truy cập /user/cart<br>2. Giỏ hàng trống<br>3. Kiểm tra | Hiển thị Card với CardContent text-center py-12, icon ShoppingCart (h-12 w-12 mx-auto text-muted-foreground mb-4), h3 "Giỏ hàng trống" (text-lg font-semibold mb-2), p "Bạn chưa có sản phẩm nào trong giỏ hàng" (text-muted-foreground mb-4), Link đến /user/products với Button "Tiếp tục mua sắm" | | Pass | 11/15/2015 | |
| **GUI-HT-10** | Kiểm tra Card mã giảm giá | 1. Truy cập /user/cart<br>2. Kiểm tra Card | Hiển thị Card với CardHeader có CardTitle "Mã giảm giá" (text-lg, icon Gift h-5 w-5), CardContent có Input placeholder "Nhập mã giảm giá" hoặc div hiển thị mã đã áp dụng | | Pass | 11/15/2015 | |
| **GUI-HT-11** | Kiểm tra Card vận chuyển | 1. Truy cập /user/cart<br>2. Kiểm tra Card | Hiển thị Card với CardHeader có CardTitle "Vận chuyển" (text-lg, icon Truck h-5 w-5), CardContent có radio buttons cho phương thức vận chuyển | | Pass | 11/15/2015 | |
| **GUI-HT-12** | Kiểm tra Card đơn vị vận chuyển | 1. Truy cập /user/cart<br>2. Kiểm tra Card | Hiển thị Card với CardHeader có CardTitle "Đơn vị vận chuyển" (text-lg, icon Truck h-5 w-5), CardContent có radio buttons cho các đơn vị: GHTK, GHN, JT | | Pass | 11/15/2015 | |
| **GUI-HT-13** | Kiểm tra Card tính phí vận chuyển | 1. Truy cập /user/cart<br>2. Kiểm tra Card | Hiển thị Card với CardHeader có CardTitle "Tính phí vận chuyển" (text-lg), CardContent có Input địa chỉ, Input trọng lượng (readOnly), Input khoảng cách (readOnly), các thông tin phí, tổng phí vận chuyển | | Pass | 11/15/2015 | |
| **GUI-HT-14** | Kiểm tra Card thông tin giao hàng | 1. Truy cập /user/cart<br>2. Kiểm tra Card | Hiển thị Card với CardHeader có CardTitle "Thông tin giao hàng" (text-lg), CardContent có Input "Họ và tên người nhận", Input "Số điện thoại", Input "Địa chỉ giao hàng", Textarea "Ghi chú giao hàng" (rows=3) | | Pass | 11/15/2015 | |
| **GUI-HT-15** | Kiểm tra Card tóm tắt đơn hàng | 1. Truy cập /user/cart<br>2. Kiểm tra Card | Hiển thị Card với CardHeader có CardTitle "Tóm tắt đơn hàng" (text-lg), CardContent có thông tin: Tạm tính, Phí vận chuyển, Giảm giá (nếu có), Separator, Tổng cộng, Button "Thanh toán", text "Thanh toán an toàn và bảo mật" (icon Shield) | | Pass | 11/15/2015 | |

#### Check FUNC: Hiển thị giỏ hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-HT-01** | Mở trang giỏ hàng | 1. Truy cập /user/cart | Hiển thị trang với tiêu đề, nút Tiếp tục mua sắm, Card chọn tất cả, danh sách Card sản phẩm, sidebar với Card mã giảm giá, Card vận chuyển, Card đơn vị vận chuyển, Card tính phí vận chuyển, Card thông tin giao hàng, Card tóm tắt đơn hàng | | Pass | 11/15/2015 | |
| **FUNC-HT-02** | Hiển thị danh sách sản phẩm trong giỏ | 1. Truy cập /user/cart<br>2. Có sản phẩm trong giỏ<br>3. Kiểm tra | Mỗi sản phẩm được hiển thị trong Card riêng với đầy đủ thông tin: Checkbox, ảnh, tên, tác giả, giá, số lượng, nút yêu thích, nút xóa | | Pass | 11/15/2015 | |
| **FUNC-HT-03** | Tính toán tạm tính | 1. Truy cập /user/cart<br>2. Có sản phẩm đã chọn<br>3. Kiểm tra | Tạm tính = tổng (item.price * item.quantity) của các sản phẩm đã chọn (isSelected = true), hiển thị "Tạm tính ({selectedItems.length} sản phẩm): {subtotal.toLocaleString('vi-VN')} VNĐ" | | Pass | 11/15/2015 | |
| **FUNC-HT-04** | Tính toán phí vận chuyển - Miễn phí | 1. Truy cập /user/cart<br>2. Tạm tính >= 500.000<br>3. Chọn phương thức tiêu chuẩn<br>4. Kiểm tra | Phí vận chuyển = 0, hiển thị "Miễn phí" | | Pass | 11/15/2015 | |
| **FUNC-HT-05** | Tính toán phí vận chuyển - Có phí tiêu chuẩn | 1. Truy cập /user/cart<br>2. Tạm tính < 500.000<br>3. Chọn phương thức tiêu chuẩn<br>4. Kiểm tra | Phí vận chuyển = 30.000 VNĐ, hiển thị "30.000 VNĐ" | | Pass | 11/15/2015 | |
| **FUNC-HT-06** | Tính toán phí vận chuyển - Giao hàng nhanh | 1. Truy cập /user/cart<br>2. Chọn phương thức giao hàng nhanh<br>3. Kiểm tra | Phí vận chuyển = 50.000 VNĐ, hiển thị "50.000 VNĐ" | | Pass | 11/15/2015 | |
| **FUNC-HT-07** | Tính toán tổng cộng | 1. Truy cập /user/cart<br>2. Có sản phẩm, phí vận chuyển, mã giảm giá<br>3. Kiểm tra | Tổng cộng = Tạm tính + Phí vận chuyển - Giảm giá, hiển thị "Tổng cộng: {total.toLocaleString('vi-VN')} VNĐ" (text-lg font-bold) | | Pass | 11/15/2015 | |
| **FUNC-HT-08** | Chọn tất cả sản phẩm | 1. Truy cập /user/cart<br>2. Nhấn Checkbox "Chọn tất cả" | Tất cả sản phẩm được chọn (isSelected = true), Checkbox "Chọn tất cả" được checked, tạm tính và tổng cộng được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-HT-09** | Bỏ chọn tất cả sản phẩm | 1. Truy cập /user/cart<br>2. Tất cả đã được chọn<br>3. Nhấn Checkbox "Chọn tất cả" | Tất cả sản phẩm bị bỏ chọn (isSelected = false), Checkbox "Chọn tất cả" không được checked, tạm tính = 0, tổng cộng = phí vận chuyển - giảm giá | | Pass | 11/15/2015 | |
| **FUNC-HT-10** | Chọn từng sản phẩm | 1. Truy cập /user/cart<br>2. Nhấn Checkbox trên Card sản phẩm | Sản phẩm đó được chọn/bỏ chọn, tạm tính và tổng cộng được cập nhật, Checkbox "Chọn tất cả" được cập nhật theo trạng thái | | Pass | 11/15/2015 | |
| **FUNC-HT-11** | Hiển thị giỏ hàng trống | 1. Truy cập /user/cart<br>2. Giỏ hàng trống<br>3. Kiểm tra | Hiển thị Card với icon ShoppingCart, text "Giỏ hàng trống", text "Bạn chưa có sản phẩm nào trong giỏ hàng", Button "Tiếp tục mua sắm" | | Pass | 11/15/2015 | |
| **FUNC-HT-12** | Nhấn nút Tiếp tục mua sắm | 1. Truy cập /user/cart<br>2. Nhấn nút "Tiếp tục mua sắm" | Chuyển đến trang /user | | Pass | 11/15/2015 | |

### Function: Xóa sách khỏi giỏ hàng

#### Check GUI: Xóa sách

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XG-01** | Kiểm tra nút Xóa | 1. Truy cập /user/cart<br>2. Kiểm tra nút | Hiển thị Button variant ghost size sm với icon Trash2 (h-4 w-4) | | Pass | 11/15/2015 | |

#### Check FUNC: Xóa sách

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XG-01** | Xóa sản phẩm khỏi giỏ hàng | 1. Truy cập /user/cart<br>2. Nhấn nút Trash2 trên Card sản phẩm | Hiển thị toast.success "Đã xóa sản phẩm khỏi giỏ hàng", sản phẩm được xóa khỏi danh sách, tạm tính và tổng cộng được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-XG-02** | Xóa sản phẩm đã chọn | 1. Truy cập /user/cart<br>2. Chọn sản phẩm<br>3. Xóa sản phẩm đó | Sản phẩm được xóa, tạm tính giảm đi giá trị của sản phẩm đó, tổng cộng được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-XG-03** | Xóa sản phẩm cuối cùng | 1. Truy cập /user/cart<br>2. Chỉ còn 1 sản phẩm<br>3. Xóa sản phẩm | Sản phẩm được xóa, hiển thị màn hình "Giỏ hàng trống" | | Pass | 11/15/2015 | |

### Function: Chỉnh sửa số lượng sách

#### Check GUI: Chỉnh sửa số lượng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CS-01** | Kiểm tra bộ chọn số lượng | 1. Truy cập /user/cart<br>2. Kiểm tra bộ chọn | Hiển thị Button variant outline size sm với icon Minus (disabled nếu quantity <= 1), Input type number với value=item.quantity, className w-16 text-center, min=1, max=item.stock, Button variant outline size sm với icon Plus (disabled nếu quantity >= stock) | | Pass | 11/15/2015 | |

#### Check FUNC: Chỉnh sửa số lượng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CS-01** | Tăng số lượng sách | 1. Truy cập /user/cart<br>2. Nhấn nút Plus | Số lượng tăng lên 1, tạm tính và tổng cộng được cập nhật, nút Plus bị disabled nếu quantity >= stock | | Pass | 11/15/2015 | |
| **FUNC-CS-02** | Giảm số lượng sách | 1. Truy cập /user/cart<br>2. Nhấn nút Minus | Số lượng giảm xuống 1, tạm tính và tổng cộng được cập nhật, nút Minus bị disabled nếu quantity <= 1 | | Pass | 11/15/2015 | |
| **FUNC-CS-03** | Nhập số lượng trực tiếp | 1. Truy cập /user/cart<br>2. Nhập số lượng vào Input | Số lượng được cập nhật nếu giá trị >= 1 và <= stock, tạm tính và tổng cộng được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-CS-04** | Tăng số lượng vượt quá tồn kho | 1. Truy cập /user/cart<br>2. Số lượng = stock<br>3. Nhấn nút Plus | Hiển thị toast.error "Chỉ còn {item.stock} sản phẩm trong kho", số lượng không được tăng, nút Plus bị disabled | | Pass | 11/15/2015 | |
| **FUNC-CS-05** | Nhập số lượng > tồn kho | 1. Truy cập /user/cart<br>2. Nhập số lượng > stock vào Input | Hiển thị toast.error "Chỉ còn {item.stock} sản phẩm trong kho", số lượng không được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-CS-06** | Nhập số lượng > MAX_QUANTITY_PER_ITEM | 1. Truy cập /user/cart<br>2. Nhập số lượng > 50 | Hiển thị toast.error "Số lượng tối đa cho mỗi sản phẩm là 50", số lượng không được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-CS-07** | Giảm số lượng xuống 0 | 1. Truy cập /user/cart<br>2. Số lượng = 1<br>3. Nhấn nút Minus | Số lượng không được giảm (vẫn = 1), nút Minus bị disabled, không có lỗi | | Pass | 11/15/2015 | |
| **FUNC-CS-08** | Nhập số lượng < 1 | 1. Truy cập /user/cart<br>2. Nhập số lượng = 0 hoặc âm | Số lượng được set về 1 (vì min=1), không có lỗi | | Pass | 11/15/2015 | |
| **FUNC-CS-09** | Cập nhật tạm tính khi thay đổi số lượng | 1. Truy cập /user/cart<br>2. Thay đổi số lượng<br>3. Kiểm tra tạm tính | Tạm tính được tính lại = tổng (item.price * item.quantity) của các sản phẩm đã chọn, được cập nhật ngay lập tức | | Pass | 11/15/2015 | |
| **FUNC-CS-10** | Cập nhật tổng cộng khi thay đổi số lượng | 1. Truy cập /user/cart<br>2. Thay đổi số lượng<br>3. Kiểm tra tổng cộng | Tổng cộng được tính lại = Tạm tính + Phí vận chuyển - Giảm giá, được cập nhật ngay lập tức | | Pass | 11/15/2015 | |

### Function: Đặt hàng

#### Check GUI: Đặt hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DH-01** | Kiểm tra Card mã giảm giá | 1. Truy cập /user/cart<br>2. Kiểm tra Card | Hiển thị Card với CardHeader có CardTitle "Mã giảm giá" (text-lg, icon Gift h-5 w-5), CardContent có Input placeholder "Nhập mã giảm giá" (nếu chưa áp dụng) hoặc div hiển thị mã đã áp dụng (nếu đã áp dụng) | | Pass | 11/15/2015 | |
| **GUI-DH-02** | Kiểm tra Input mã giảm giá | 1. Truy cập /user/cart<br>2. Kiểm tra Input | Hiển thị Input với placeholder "Nhập mã giảm giá", value=couponCode | | Pass | 11/15/2015 | |
| **GUI-DH-03** | Kiểm tra nút Áp dụng mã | 1. Truy cập /user/cart<br>2. Kiểm tra nút | Hiển thị Button với icon Percent (h-4 w-4 mr-2) và text "Áp dụng", className w-full | | Pass | 11/15/2015 | |
| **GUI-DH-04** | Kiểm tra hiển thị mã đã áp dụng | 1. Truy cập /user/cart<br>2. Áp dụng mã giảm giá<br>3. Kiểm tra | Hiển thị div với className "flex items-center justify-between p-2 bg-green-50 rounded-lg", có p với appliedCoupon.code (font-medium text-green-800), p với appliedCoupon.description (text-sm text-green-600), Button variant ghost size sm với icon Trash2 để xóa mã | | Pass | 11/15/2015 | |
| **GUI-DH-05** | Kiểm tra gợi ý mã giảm giá | 1. Truy cập /user/cart<br>2. Kiểm tra phần gợi ý | Hiển thị text "Mã khả dụng: " và Link đến /user/promotions với text "xem tất cả" (underline), grid grid-cols-2 gap-2 với các Button variant outline size sm, icon Gift (h-4 w-4 mr-1) và text mã code | | Pass | 11/15/2015 | |
| **GUI-DH-06** | Kiểm tra Card vận chuyển | 1. Truy cập /user/cart<br>2. Kiểm tra Card | Hiển thị Card với CardHeader có CardTitle "Vận chuyển" (text-lg, icon Truck h-5 w-5), CardContent có radio buttons: "Giao hàng tiêu chuẩn" (3-5 ngày, Miễn phí nếu subtotal >= 500000, 30.000 VNĐ nếu không) và "Giao hàng nhanh" (1-2 ngày, 50.000 VNĐ) | | Pass | 11/15/2015 | |
| **GUI-DH-07** | Kiểm tra Card đơn vị vận chuyển | 1. Truy cập /user/cart<br>2. Kiểm tra Card | Hiển thị Card với CardHeader có CardTitle "Đơn vị vận chuyển" (text-lg, icon Truck h-5 w-5), CardContent có radio buttons cho: GHTK (3-5 ngày, Miễn phí nếu subtotal >= 500000, 30.000 VNĐ nếu không), GHN (1-2 ngày, 50.000 VNĐ), JT (2-4 ngày, Miễn phí nếu subtotal >= 500000, 30.000 VNĐ nếu không), text "Điều kiện miễn phí: đơn từ 500.000 VNĐ với phương thức tiêu chuẩn" (text-sm text-muted-foreground) | | Pass | 11/15/2015 | |
| **GUI-DH-08** | Kiểm tra Card tính phí vận chuyển | 1. Truy cập /user/cart<br>2. Kiểm tra Card | Hiển thị Card với CardHeader có CardTitle "Tính phí vận chuyển" (text-lg), CardContent có Input "Địa chỉ giao hàng" (placeholder "Số nhà, đường, phường/xã, quận/huyện, tỉnh/thành"), Input "Trọng lượng (kg)" (readOnly, value=totalWeightKg), Input "Khoảng cách (km)" (readOnly, value=distanceKm), các thông tin phí, Separator, tổng phí vận chuyển | | Pass | 11/15/2015 | |
| **GUI-DH-09** | Kiểm tra Card thông tin giao hàng | 1. Truy cập /user/cart<br>2. Kiểm tra Card | Hiển thị Card với CardHeader có CardTitle "Thông tin giao hàng" (text-lg), CardContent có Input "Họ và tên người nhận" (placeholder "Nguyễn Văn A"), Input "Số điện thoại" (placeholder "09xxxxxxxx"), Input "Địa chỉ giao hàng" (placeholder "Số nhà, đường, phường/xã, quận/huyện, tỉnh/thành"), Textarea "Ghi chú giao hàng" (placeholder "Hẹn giờ, lưu ý khi giao...", rows=3) | | Pass | 11/15/2015 | |
| **GUI-DH-10** | Kiểm tra Card tóm tắt đơn hàng | 1. Truy cập /user/cart<br>2. Kiểm tra Card | Hiển thị Card với CardHeader có CardTitle "Tóm tắt đơn hàng" (text-lg), CardContent có: "Tạm tính ({selectedItems.length} sản phẩm): {subtotal.toLocaleString('vi-VN')} VNĐ", "Phí vận chuyển: {shippingFee === 0 ? 'Miễn phí' : shippingFee.toLocaleString('vi-VN') + ' VNĐ'}", "Giảm giá ({appliedCoupon.code}): -{discountAmount.toLocaleString('vi-VN')} VNĐ" (nếu có, text-green-600), Separator, "Tổng cộng: {total.toLocaleString('vi-VN')} VNĐ" (text-lg font-bold) | | Pass | 11/15/2015 | |
| **GUI-DH-11** | Kiểm tra nút Thanh toán | 1. Truy cập /user/cart<br>2. Kiểm tra nút | Hiển thị Link đến /user/checkout với Button size lg className w-full, icon CreditCard (h-4 w-4 mr-2) và text "Thanh toán ({selectedItems.length} sản phẩm)", disabled nếu selectedItems.length === 0 | | Pass | 11/15/2015 | |
| **GUI-DH-12** | Kiểm tra thông báo bảo mật | 1. Truy cập /user/cart<br>2. Kiểm tra thông báo | Hiển thị div flex items-center gap-2 text-sm text-muted-foreground với icon Shield (h-4 w-4) và text "Thanh toán an toàn và bảo mật" | | Pass | 11/15/2015 | |

#### Check FUNC: Đặt hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DH-01** | Áp dụng mã giảm giá hợp lệ | 1. Truy cập /user/cart<br>2. Nhập mã giảm giá hợp lệ<br>3. Nhấn "Áp dụng" | Hiển thị toast.success "Áp dụng mã giảm giá thành công!", appliedCoupon được set, hiển thị div mã đã áp dụng, giảm giá được tính vào tổng cộng | | Pass | 11/15/2015 | |
| **FUNC-DH-02** | Áp dụng mã giảm giá không hợp lệ | 1. Truy cập /user/cart<br>2. Nhập mã không tồn tại<br>3. Nhấn "Áp dụng" | Hiển thị toast.error "Mã giảm giá không hợp lệ", mã không được áp dụng | | Pass | 11/15/2015 | |
| **FUNC-DH-03** | Áp dụng mã giảm giá không đủ điều kiện | 1. Truy cập /user/cart<br>2. Tạm tính < minOrder của mã<br>3. Nhập mã và nhấn "Áp dụng" | Hiển thị toast.error "Đơn hàng tối thiểu {coupon.minOrder.toLocaleString()} VNĐ", mã không được áp dụng | | Pass | 11/15/2015 | |
| **FUNC-DH-04** | Xóa mã giảm giá | 1. Truy cập /user/cart<br>2. Đã áp dụng mã<br>3. Nhấn nút Trash2 | Hiển thị toast.success "Đã xóa mã giảm giá", appliedCoupon = null, couponCode = "", hiển thị lại Input mã giảm giá, tổng cộng được cập nhật (tăng lên) | | Pass | 11/15/2015 | |
| **FUNC-DH-05** | Click vào mã gợi ý | 1. Truy cập /user/cart<br>2. Click vào Button mã gợi ý | couponCode được set thành mã đã chọn, Input hiển thị mã đó | | Pass | 11/15/2015 | |
| **FUNC-DH-06** | Tính toán giảm giá theo phần trăm | 1. Truy cập /user/cart<br>2. Áp dụng mã giảm giá type="percentage"<br>3. Kiểm tra | Giảm giá = (subtotal * appliedCoupon.discount) / 100, hiển thị "-{discountAmount.toLocaleString('vi-VN')} VNĐ" | | Pass | 11/15/2015 | |
| **FUNC-DH-07** | Tính toán giảm giá cố định | 1. Truy cập /user/cart<br>2. Áp dụng mã giảm giá type="fixed"<br>3. Kiểm tra | Giảm giá = appliedCoupon.discount, hiển thị "-{discountAmount.toLocaleString('vi-VN')} VNĐ" | | Pass | 11/15/2015 | |
| **FUNC-DH-08** | Chọn phương thức vận chuyển tiêu chuẩn | 1. Truy cập /user/cart<br>2. Chọn radio "Giao hàng tiêu chuẩn" | shippingMethod = "standard", phí vận chuyển được tính lại (0 nếu subtotal >= 500000, 30.000 VNĐ nếu không), tổng cộng được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-DH-09** | Chọn phương thức vận chuyển nhanh | 1. Truy cập /user/cart<br>2. Chọn radio "Giao hàng nhanh" | shippingMethod = "express", phí vận chuyển = 50.000 VNĐ, tổng cộng được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-DH-10** | Chọn đơn vị vận chuyển | 1. Truy cập /user/cart<br>2. Chọn radio đơn vị vận chuyển | selectedCarrier được set thành ID đơn vị đã chọn (GHTK, GHN, hoặc JT) | | Pass | 11/15/2015 | |
| **FUNC-DH-11** | Nhập thông tin giao hàng | 1. Truy cập /user/cart<br>2. Nhập thông tin vào các Input | shippingName, shippingPhone, shippingAddress, shippingNote được cập nhật theo giá trị đã nhập | | Pass | 11/15/2015 | |
| **FUNC-DH-12** | Nhấn nút Thanh toán | 1. Truy cập /user/cart<br>2. Có sản phẩm đã chọn<br>3. Nhấn nút "Thanh toán" | Chuyển đến trang /user/checkout, thông tin giỏ hàng được truyền | | Pass | 11/15/2015 | |
| **FUNC-DH-13** | Nhấn nút Thanh toán khi không có sản phẩm | 1. Truy cập /user/cart<br>2. Không có sản phẩm đã chọn<br>3. Nhấn nút "Thanh toán" | Nút bị disabled, không thể click, không chuyển trang | | Pass | 11/15/2015 | |
| **FUNC-DH-14** | Tính toán tổng cộng với đầy đủ thông tin | 1. Truy cập /user/cart<br>2. Có sản phẩm đã chọn, phí vận chuyển, mã giảm giá<br>3. Kiểm tra | Tổng cộng = Tạm tính + Phí vận chuyển - Giảm giá, hiển thị đúng với toLocaleString("vi-VN") | | Pass | 11/15/2015 | |
| **FUNC-DH-15** | Cập nhật phí vận chuyển khi thay đổi phương thức | 1. Truy cập /user/cart<br>2. Thay đổi phương thức vận chuyển<br>3. Kiểm tra | Phí vận chuyển được tính lại, tổng cộng được cập nhật ngay lập tức | | Pass | 11/15/2015 | |
| **FUNC-DH-16** | Cập nhật phí vận chuyển khi tạm tính thay đổi | 1. Truy cập /user/cart<br>2. Thay đổi số lượng hoặc chọn/bỏ chọn sản phẩm<br>3. Tạm tính >= 500.000<br>4. Kiểm tra | Phí vận chuyển chuyển thành 0 (nếu phương thức tiêu chuẩn), tổng cộng được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-DH-17** | Nhấn link "xem tất cả" mã giảm giá | 1. Truy cập /user/cart<br>2. Nhấn link "xem tất cả" | Chuyển đến trang /user/promotions | | Pass | 11/15/2015 | |
| **FUNC-DH-18** | Thêm vào yêu thích từ giỏ hàng | 1. Truy cập /user/cart<br>2. Nhấn nút Heart trên Card sản phẩm | Hiển thị toast.success "Đã thêm \"{item.title}\" vào danh sách yêu thích" | | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn MDX để dễ dàng quản lý và cập nhật test cases.*

