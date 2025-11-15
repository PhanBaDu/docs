# Test Case Template - Chức năng thanh toán đơn hàng (User)

## Module Code
**Model Management Store: Chức năng thanh toán đơn hàng User**

## Test Requirement
1. Chọn phương thức thanh toán
2. Nhập thông tin giao hàng
3. Xác nhận đơn hàng
4. Xử lý thanh toán COD
5. Xử lý thanh toán Banking
6. Xử lý thanh toán E-wallet
7. Theo dõi trạng thái thanh toán

---

## Test Summary

### Người thực hiện Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 134 |
| **Fail** | 0 |
| **Untested** | 36 |
| **N/A** | 0 |
| **Number of Test cases** | 170 |

---

## Test Cases

### Function: Chọn phương thức thanh toán

#### Check GUI: Chọn phương thức thanh toán

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CPTTT-01** | Kiểm tra tiêu đề trang | 1. Truy cập /user/checkout<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Thanh toán" với mô tả "Xác nhận thông tin và hoàn tất đơn hàng" | | Pass | 11/15/2015 | |
| **GUI-CPTTT-02** | Kiểm tra badge số lượng sản phẩm | 1. Truy cập /user/checkout<br>2. Kiểm tra badge | Hiển thị badge variant secondary với text "X sản phẩm" | | Pass | 11/15/2015 | |
| **GUI-CPTTT-03** | Kiểm tra card Thanh toán | 1. Truy cập /user/checkout<br>2. Kiểm tra card | Hiển thị card với tiêu đề "Thanh toán" | | Pass | 11/15/2015 | |
| **GUI-CPTTT-04** | Kiểm tra radio button COD | 1. Truy cập /user/checkout<br>2. Kiểm tra radio | Hiển thị radio button với label "Thanh toán khi nhận hàng (COD)", icon Package, mô tả "Thanh toán bằng tiền mặt khi nhận hàng" | | Pass | 11/15/2015 | |
| **GUI-CPTTT-05** | Kiểm tra radio button Banking | 1. Truy cập /user/checkout<br>2. Kiểm tra radio | Hiển thị radio button với label "Chuyển khoản ngân hàng", icon CreditCard, mô tả "Chuyển khoản qua ngân hàng" | | Pass | 11/15/2015 | |
| **GUI-CPTTT-06** | Kiểm tra radio button E-wallet | 1. Truy cập /user/checkout<br>2. Kiểm tra radio | Hiển thị radio button với label "Ví điện tử (MoMo, ZaloPay, VNPay)", icon Smartphone, mô tả "Thanh toán qua ví điện tử" | | Pass | 11/15/2015 | |
| **GUI-CPTTT-07** | Kiểm tra thông báo bảo mật | 1. Truy cập /user/checkout<br>2. Kiểm tra thông báo | Hiển thị text "Thanh toán an toàn và bảo mật" với icon Shield, màu muted-foreground | | Pass | 11/15/2015 | |

---

### Check FUNC: Chọn phương thức thanh toán

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CPTTT-01** | Chọn phương thức COD | 1. Truy cập /user/checkout<br>2. Chọn radio button COD<br>3. Kiểm tra kết quả | Radio button COD được chọn, phương thức thanh toán được cập nhật thành "cod" | | Pass | 11/15/2015 | |
| **FUNC-CPTTT-02** | Chọn phương thức Banking | 1. Truy cập /user/checkout<br>2. Chọn radio button Banking<br>3. Kiểm tra kết quả | Radio button Banking được chọn, phương thức thanh toán được cập nhật thành "bank" | | Pass | 11/15/2015 | |
| **FUNC-CPTTT-03** | Chọn phương thức E-wallet | 1. Truy cập /user/checkout<br>2. Chọn radio button E-wallet<br>3. Kiểm tra kết quả | Radio button E-wallet được chọn, phương thức thanh toán được cập nhật thành "ewallet" | | Pass | 11/15/2015 | |
| **FUNC-CPTTT-04** | Chỉ chọn một phương thức tại một thời điểm | 1. Truy cập /user/checkout<br>2. Chọn COD<br>3. Chọn Banking<br>4. Kiểm tra kết quả | Chỉ Banking được chọn, COD bị bỏ chọn, chỉ một phương thức được chọn tại một thời điểm | | Pass | 11/15/2015 | |
| **FUNC-CPTTT-05** | Phương thức mặc định | 1. Truy cập /user/checkout<br>2. Kiểm tra phương thức mặc định | COD được chọn mặc định khi mở trang | | Pass | 11/15/2015 | |

---

### Function: Nhập thông tin giao hàng

#### Check GUI: Nhập thông tin giao hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-NTTTGH-01** | Kiểm tra card Địa chỉ giao hàng | 1. Truy cập /user/checkout<br>2. Kiểm tra card | Hiển thị card với tiêu đề "Địa chỉ giao hàng", mô tả "Thông tin người nhận" | | Pass | 11/15/2015 | |
| **GUI-NTTTGH-02** | Kiểm tra checkbox Sử dụng địa chỉ đã lưu | 1. Truy cập /user/checkout<br>2. Kiểm tra checkbox | Hiển thị checkbox với label "Sử dụng địa chỉ đã lưu", có thể click | | Pass | 11/15/2015 | |
| **GUI-NTTTGH-03** | Kiểm tra input Họ và tên | 1. Truy cập /user/checkout<br>2. Kiểm tra input | Hiển thị Input với label "Họ và tên", placeholder "Nguyễn Văn A", có thể nhập text | | Pass | 11/15/2015 | |
| **GUI-NTTTGH-04** | Kiểm tra input Số điện thoại | 1. Truy cập /user/checkout<br>2. Kiểm tra input | Hiển thị Input với label "Số điện thoại", placeholder "0123456789", có thể nhập số | | Pass | 11/15/2015 | |
| **GUI-NTTTGH-05** | Kiểm tra input Địa chỉ | 1. Truy cập /user/checkout<br>2. Kiểm tra input | Hiển thị Input với label "Địa chỉ", placeholder "123 Đường ABC, Quận 1, TP.HCM", có thể nhập text | | Pass | 11/15/2015 | |
| **GUI-NTTTGH-06** | Kiểm tra dropdown Tỉnh/Thành phố | 1. Truy cập /user/checkout<br>2. Kiểm tra dropdown | Hiển thị Select với label "Tỉnh/Thành", các option: TP.HCM, Hà Nội, ... | | Pass | 11/15/2015 | |
| **GUI-NTTTGH-07** | Kiểm tra input Quận/Huyện | 1. Truy cập /user/checkout<br>2. Kiểm tra input | Hiển thị Input với label "Quận/Huyện", placeholder "Quận 1", có thể nhập text | | Pass | 11/15/2015 | |
| **GUI-NTTTGH-08** | Kiểm tra dropdown Phường/Xã | 1. Truy cập /user/checkout<br>2. Kiểm tra dropdown | Hiển thị Select với label "Phường/Xã", các option: Phường Bến Nghé, Phường Đa Kao, ... | | Pass | 11/15/2015 | |
| **GUI-NTTTGH-09** | Kiểm tra textarea Ghi chú giao hàng | 1. Truy cập /user/checkout<br>2. Kiểm tra textarea | Hiển thị Textarea với label "Ghi chú giao hàng", placeholder "Ví dụ: gọi trước khi giao, hẹn giờ...", rows=3 | | Pass | 11/15/2015 | |
| **GUI-NTTTGH-10** | Kiểm tra checkbox Lưu địa chỉ mặc định | 1. Truy cập /user/checkout<br>2. Kiểm tra checkbox | Hiển thị checkbox với label "Lưu địa chỉ này làm mặc định", có thể click | | Pass | 11/15/2015 | |

---

### Check FUNC: Nhập thông tin giao hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-NTTTGH-01** | Nhập thông tin giao hàng | 1. Truy cập /user/checkout<br>2. Nhập đầy đủ thông tin: Họ tên, SĐT, Địa chỉ, Tỉnh/Thành, Quận/Huyện, Phường/Xã<br>3. Kiểm tra kết quả | Thông tin được lưu, có thể sử dụng khi đặt hàng | | Pass | 11/15/2015 | |
| **FUNC-NTTTGH-02** | Sử dụng địa chỉ đã lưu | 1. Truy cập /user/checkout<br>2. Tích checkbox "Sử dụng địa chỉ đã lưu"<br>3. Kiểm tra kết quả | Thông tin địa chỉ đã lưu được tự động điền vào các trường, các trường có thể bị disabled hoặc readonly | | Pass | 11/15/2015 | |
| **FUNC-NTTTGH-03** | Lưu địa chỉ mới làm mặc định | 1. Truy cập /user/checkout<br>2. Nhập địa chỉ mới<br>3. Tích checkbox "Lưu địa chỉ này làm mặc định"<br>4. Đặt hàng thành công<br>5. Kiểm tra kết quả | Địa chỉ mới được lưu làm mặc định, hiển thị khi đặt hàng lần sau | | Untested | 11/15/2015 | |
| **FUNC-NTTTGH-04** | Validation Họ và tên - Để trống | 1. Truy cập /user/checkout<br>2. Để trống Họ và tên<br>3. Click "Đặt hàng"<br>4. Kiểm tra validation | Hiển thị cảnh báo "Họ và tên là bắt buộc", không cho phép đặt hàng | | Pass | 11/15/2015 | |
| **FUNC-NTTTGH-05** | Validation Số điện thoại - Để trống | 1. Truy cập /user/checkout<br>2. Để trống Số điện thoại<br>3. Click "Đặt hàng"<br>4. Kiểm tra validation | Hiển thị cảnh báo "Số điện thoại là bắt buộc", không cho phép đặt hàng | | Pass | 11/15/2015 | |
| **FUNC-NTTTGH-06** | Validation Số điện thoại - Định dạng không hợp lệ | 1. Truy cập /user/checkout<br>2. Nhập SĐT không đúng định dạng (VD: "abc")<br>3. Click "Đặt hàng"<br>4. Kiểm tra validation | Hiển thị cảnh báo "Số điện thoại không hợp lệ", không cho phép đặt hàng | | Pass | 11/15/2015 | |
| **FUNC-NTTTGH-07** | Validation Địa chỉ - Để trống | 1. Truy cập /user/checkout<br>2. Để trống Địa chỉ<br>3. Click "Đặt hàng"<br>4. Kiểm tra validation | Hiển thị cảnh báo "Địa chỉ là bắt buộc", không cho phép đặt hàng | | Pass | 11/15/2015 | |
| **FUNC-NTTTGH-08** | Validation Tỉnh/Thành phố - Chưa chọn | 1. Truy cập /user/checkout<br>2. Chưa chọn Tỉnh/Thành phố<br>3. Click "Đặt hàng"<br>4. Kiểm tra validation | Hiển thị cảnh báo "Vui lòng chọn Tỉnh/Thành phố", không cho phép đặt hàng | | Pass | 11/15/2015 | |
| **FUNC-NTTTGH-09** | Validation Quận/Huyện - Để trống | 1. Truy cập /user/checkout<br>2. Để trống Quận/Huyện<br>3. Click "Đặt hàng"<br>4. Kiểm tra validation | Hiển thị cảnh báo "Quận/Huyện là bắt buộc", không cho phép đặt hàng | | Pass | 11/15/2015 | |
| **FUNC-NTTTGH-10** | Validation Phường/Xã - Chưa chọn | 1. Truy cập /user/checkout<br>2. Chưa chọn Phường/Xã<br>3. Click "Đặt hàng"<br>4. Kiểm tra validation | Hiển thị cảnh báo "Vui lòng chọn Phường/Xã", không cho phép đặt hàng | | Pass | 11/15/2015 | |
| **FUNC-NTTTGH-11** | Validation real-time | 1. Truy cập /user/checkout<br>2. Nhập thông tin không hợp lệ<br>3. Quan sát validation | Validation được thực hiện real-time khi nhập, hiển thị cảnh báo ngay lập tức | | Pass | 11/15/2015 | |
| **FUNC-NTTTGH-12** | Nhập Ghi chú giao hàng | 1. Truy cập /user/checkout<br>2. Nhập ghi chú vào textarea<br>3. Kiểm tra kết quả | Ghi chú được lưu, có thể sử dụng khi đặt hàng, không bắt buộc | | Pass | 11/15/2015 | |

---

### Function: Xác nhận đơn hàng

#### Check GUI: Xác nhận đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XNDH-01** | Kiểm tra card Đơn hàng | 1. Truy cập /user/checkout<br>2. Kiểm tra card | Hiển thị card với tiêu đề "Đơn hàng", mô tả "Kiểm tra lại sản phẩm" | | Pass | 11/15/2015 | |
| **GUI-XNDH-02** | Kiểm tra danh sách sản phẩm | 1. Truy cập /user/checkout<br>2. Kiểm tra danh sách | Hiển thị danh sách sản phẩm với tên, số lượng, giá tổng cho mỗi sản phẩm | | Pass | 11/15/2015 | |
| **GUI-XNDH-03** | Kiểm tra Tạm tính | 1. Truy cập /user/checkout<br>2. Kiểm tra tạm tính | Hiển thị "Tạm tính" với giá trị tổng tiền sản phẩm | | Pass | 11/15/2015 | |
| **GUI-XNDH-04** | Kiểm tra Phí vận chuyển | 1. Truy cập /user/checkout<br>2. Kiểm tra phí | Hiển thị "Phí vận chuyển" với giá trị phí vận chuyển | | Pass | 11/15/2015 | |
| **GUI-XNDH-05** | Kiểm tra Giảm giá | 1. Truy cập /user/checkout<br>2. Có mã giảm giá<br>3. Kiểm tra giảm giá | Hiển thị "Giảm giá" với số tiền giảm màu đỏ | | Pass | 11/15/2015 | |
| **GUI-XNDH-06** | Kiểm tra Tổng cộng | 1. Truy cập /user/checkout<br>2. Kiểm tra tổng | Hiển thị "Tổng" với font semibold text-lg, giá trị tổng tiền thanh toán | | Pass | 11/15/2015 | |
| **GUI-XNDH-07** | Kiểm tra checkbox Xác nhận điều khoản | 1. Truy cập /user/checkout<br>2. Kiểm tra checkbox | Hiển thị checkbox với label "Tôi đồng ý với điều khoản và điều kiện", có thể click | | Pass | 11/15/2015 | |
| **GUI-XNDH-08** | Kiểm tra nút Đặt hàng | 1. Truy cập /user/checkout<br>2. Kiểm tra nút | Hiển thị nút "Đặt hàng" chiếm toàn bộ chiều rộng, disabled khi chưa tích checkbox điều khoản | | Pass | 11/15/2015 | |
| **GUI-XNDH-09** | Kiểm tra thông báo điều khoản | 1. Truy cập /user/checkout<br>2. Kiểm tra thông báo | Hiển thị text "Bằng việc đặt hàng, bạn đồng ý với điều khoản & chính sách của cửa hàng." với màu muted-foreground, text-center | | Pass | 11/15/2015 | |

---

### Check FUNC: Xác nhận đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XNDH-01** | Hiển thị thông tin đơn hàng | 1. Truy cập /user/checkout<br>2. Kiểm tra thông tin | Hiển thị đầy đủ: danh sách sản phẩm, Tạm tính, Phí vận chuyển, Giảm giá (nếu có), Tổng cộng | | Pass | 11/15/2015 | |
| **FUNC-XNDH-02** | Tính toán tóm tắt đơn hàng | 1. Truy cập /user/checkout<br>2. Thay đổi phương thức vận chuyển, áp dụng mã giảm giá<br>3. Kiểm tra tóm tắt | Tóm tắt được tính toán lại: Tạm tính, Phí vận chuyển, Giảm giá, Tổng cộng, tất cả được cập nhật real-time | | Pass | 11/15/2015 | |
| **FUNC-XNDH-03** | Tích checkbox Xác nhận điều khoản | 1. Truy cập /user/checkout<br>2. Tích checkbox "Tôi đồng ý với điều khoản và điều kiện"<br>3. Kiểm tra nút Đặt hàng | Checkbox được tích, nút "Đặt hàng" được kích hoạt (không còn disabled) | | Pass | 11/15/2015 | |
| **FUNC-XNDH-04** | Bỏ tích checkbox Xác nhận điều khoản | 1. Truy cập /user/checkout<br>2. Bỏ tích checkbox<br>3. Kiểm tra nút Đặt hàng | Checkbox bị bỏ tích, nút "Đặt hàng" bị disabled | | Pass | 11/15/2015 | |
| **FUNC-XNDH-05** | Click nút Đặt hàng - Chưa tích điều khoản | 1. Truy cập /user/checkout<br>2. Chưa tích checkbox điều khoản<br>3. Click "Đặt hàng" | Nút bị disabled, không thể click, không đặt hàng | | Pass | 11/15/2015 | |
| **FUNC-XNDH-06** | Click nút Đặt hàng - Đã tích điều khoản | 1. Truy cập /user/checkout<br>2. Đã tích checkbox điều khoản<br>3. Nhập đầy đủ thông tin<br>4. Click "Đặt hàng"<br>5. Kiểm tra kết quả | Đơn hàng được tạo, chuyển đến bước xử lý thanh toán theo phương thức đã chọn | | Untested | 11/15/2015 | |
| **FUNC-XNDH-07** | Kiểm tra tính hợp lệ trước khi đặt hàng | 1. Truy cập /user/checkout<br>2. Thiếu thông tin giao hàng<br>3. Tích checkbox điều khoản<br>4. Click "Đặt hàng"<br>5. Kiểm tra kết quả | Hiển thị cảnh báo về thông tin thiếu, không đặt hàng, yêu cầu nhập đầy đủ thông tin | | Pass | 11/15/2015 | |
| **FUNC-XNDH-08** | Kiểm tra tồn kho trước khi đặt hàng | 1. Truy cập /user/checkout<br>2. Sản phẩm trong giỏ hết hàng<br>3. Click "Đặt hàng"<br>4. Kiểm tra kết quả | Hiển thị cảnh báo "Sản phẩm '[Tên]' đã hết hàng", không đặt hàng, yêu cầu xóa sản phẩm hết hàng | | Untested | 11/15/2015 | |

---

### Function: Xử lý thanh toán COD

#### Check GUI: Xử lý thanh toán COD

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XLTTCOD-01** | Kiểm tra loading spinner | 1. Truy cập /user/checkout<br>2. Chọn COD<br>3. Click "Đặt hàng"<br>4. Kiểm tra loading | Hiển thị loading spinner với thông báo "Vui lòng chờ trong giây lát..." | | Pass | 11/15/2015 | |
| **GUI-XLTTCOD-02** | Kiểm tra thông báo thành công | 1. Truy cập /user/checkout<br>2. Đặt hàng COD thành công<br>3. Kiểm tra thông báo | Hiển thị card với tiêu đề "Đơn hàng đã được đặt thành công", thông tin đơn hàng, mã đơn hàng | | Pass | 11/15/2015 | |

---

### Check FUNC: Xử lý thanh toán COD

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XLTTCOD-01** | Đặt hàng COD thành công | 1. Truy cập /user/checkout<br>2. Chọn COD<br>3. Nhập đầy đủ thông tin<br>4. Tích checkbox điều khoản<br>5. Click "Đặt hàng"<br>6. Kiểm tra kết quả | Hiển thị loading, sau đó hiển thị thông báo "Đơn hàng đã được đặt thành công", đơn hàng được tạo với trạng thái "Chờ xử lý", gửi thông báo xác nhận đến người dùng, chuyển đến trang theo dõi đơn hàng | | Untested | 11/15/2015 | |
| **FUNC-XLTTCOD-02** | Đơn hàng COD không cần thanh toán trước | 1. Truy cập /user/checkout<br>2. Đặt hàng COD thành công<br>3. Kiểm tra trạng thái thanh toán | Trạng thái thanh toán = "Chờ thanh toán", người dùng sẽ thanh toán khi nhận hàng | | Pass | 11/15/2015 | |

---

### Function: Xử lý thanh toán Banking

#### Check GUI: Xử lý thanh toán Banking

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XLTTBANK-01** | Kiểm tra form chuyển khoản | 1. Truy cập /user/checkout<br>2. Chọn Banking<br>3. Click "Đặt hàng"<br>4. Kiểm tra form | Hiển thị form với tiêu đề "Thông tin chuyển khoản", các trường: Số tài khoản, Tên chủ tài khoản, Ngân hàng, Nội dung chuyển khoản | | Pass | 11/15/2015 | |
| **GUI-XLTTBANK-02** | Kiểm tra input Số tài khoản | 1. Truy cập /user/checkout<br>2. Mở form chuyển khoản<br>3. Kiểm tra input | Hiển thị Input với label "Số tài khoản ngân hàng", có thể nhập số | | Pass | 11/15/2015 | |
| **GUI-XLTTBANK-03** | Kiểm tra input Tên chủ tài khoản | 1. Truy cập /user/checkout<br>2. Mở form chuyển khoản<br>3. Kiểm tra input | Hiển thị Input với label "Tên chủ tài khoản", có thể nhập text | | Pass | 11/15/2015 | |
| **GUI-XLTTBANK-04** | Kiểm tra dropdown Ngân hàng | 1. Truy cập /user/checkout<br>2. Mở form chuyển khoản<br>3. Kiểm tra dropdown | Hiển thị Select với label "Tên ngân hàng", các option: Vietcombank, BIDV, Agribank, ... | | Pass | 11/15/2015 | |
| **GUI-XLTTBANK-05** | Kiểm tra input Nội dung chuyển khoản | 1. Truy cập /user/checkout<br>2. Mở form chuyển khoản<br>3. Kiểm tra input | Hiển thị Input với label "Nội dung chuyển khoản", có thể nhập text, hiển thị mã đơn hàng mặc định | | Pass | 11/15/2015 | |

---

### Check FUNC: Xử lý thanh toán Banking

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XLTTBANK-01** | Đặt hàng Banking | 1. Truy cập /user/checkout<br>2. Chọn Banking<br>3. Click "Đặt hàng"<br>4. Kiểm tra kết quả | Hiển thị form chuyển khoản với thông tin: số tài khoản, tên chủ tài khoản, ngân hàng, nội dung chuyển khoản (mã đơn hàng), hướng dẫn thanh toán | | Untested | 11/15/2015 | |
| **FUNC-XLTTBANK-02** | Hiển thị thông tin chuyển khoản | 1. Truy cập /user/checkout<br>2. Đặt hàng Banking<br>3. Kiểm tra thông tin | Hiển thị đầy đủ thông tin chuyển khoản: số tài khoản, tên chủ tài khoản, ngân hàng, số tiền, nội dung chuyển khoản | | Pass | 11/15/2015 | |
| **FUNC-XLTTBANK-03** | Xác nhận thanh toán Banking | 1. Truy cập /user/checkout<br>2. Đặt hàng Banking<br>3. Thực hiện chuyển khoản<br>4. Xác nhận thanh toán<br>5. Kiểm tra kết quả | Đơn hàng được xác nhận sau khi xác nhận thanh toán, trạng thái đơn hàng chuyển thành "Đã thanh toán" | | Untested | 11/15/2015 | |

---

### Function: Xử lý thanh toán E-wallet

#### Check GUI: Xử lý thanh toán E-wallet

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XLTTEW-01** | Kiểm tra QR Code | 1. Truy cập /user/checkout<br>2. Chọn E-wallet<br>3. Click "Đặt hàng"<br>4. Kiểm tra QR | Hiển thị hình ảnh mã QR thanh toán với số tiền và thông tin đơn hàng | | Pass | 11/15/2015 | |
| **GUI-XLTTEW-02** | Kiểm tra link thanh toán | 1. Truy cập /user/checkout<br>2. Chọn E-wallet<br>3. Click "Đặt hàng"<br>4. Kiểm tra link | Hiển thị nút "Thanh toán qua ví điện tử" với link đến trang thanh toán của ví | | Pass | 11/15/2015 | |

---

### Check FUNC: Xử lý thanh toán E-wallet

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XLTTEW-01** | Đặt hàng E-wallet | 1. Truy cập /user/checkout<br>2. Chọn E-wallet<br>3. Click "Đặt hàng"<br>4. Kiểm tra kết quả | Hiển thị mã QR hoặc link thanh toán, người dùng có thể quét QR hoặc click link để thanh toán | | Untested | 11/15/2015 | |
| **FUNC-XLTTEW-02** | Thanh toán E-wallet thành công | 1. Truy cập /user/checkout<br>2. Đặt hàng E-wallet<br>3. Thanh toán qua ví điện tử thành công<br>4. Kiểm tra kết quả | Đơn hàng được tự động xác nhận, trạng thái đơn hàng chuyển thành "Đã thanh toán", trạng thái thanh toán = "Đã thanh toán", chuyển đến trang theo dõi đơn hàng | | Untested | 11/15/2015 | |
| **FUNC-XLTTEW-03** | Thanh toán E-wallet thất bại | 1. Truy cập /user/checkout<br>2. Đặt hàng E-wallet<br>3. Thanh toán thất bại<br>4. Kiểm tra kết quả | Hiển thị thông báo lỗi "Thanh toán thất bại", đơn hàng được giữ ở trạng thái "Chờ thanh toán", có thể thử lại | | Untested | 11/15/2015 | |

---

### Function: Theo dõi trạng thái thanh toán

#### Check GUI: Theo dõi trạng thái thanh toán

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-TDTTTT-01** | Kiểm tra trạng thái đơn hàng | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra trạng thái | Hiển thị "Trạng thái đơn hàng:" với badge trạng thái (Chờ xử lý, Đang chuẩn bị, Đang giao hàng, Đã giao hàng, Đã hủy) | | Pass | 11/15/2015 | |
| **GUI-TDTTTT-02** | Kiểm tra trạng thái thanh toán | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra trạng thái | Hiển thị "Trạng thái thanh toán:" với badge trạng thái (Chờ thanh toán, Đã thanh toán, Thanh toán thất bại) | | Pass | 11/15/2015 | |
| **GUI-TDTTTT-03** | Kiểm tra timeline lịch sử trạng thái | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra timeline | Hiển thị timeline các thay đổi trạng thái theo thời gian, bao gồm cả trạng thái thanh toán | | Pass | 11/15/2015 | |

---

### Check FUNC: Theo dõi trạng thái thanh toán

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TDTTTT-01** | Hiển thị trạng thái thanh toán | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra trạng thái | Hiển thị trạng thái thanh toán hiện tại: Chờ thanh toán, Đã thanh toán, Thanh toán thất bại, với badge màu sắc tương ứng | | Pass | 11/15/2015 | |
| **FUNC-TDTTTT-02** | Cập nhật trạng thái thanh toán real-time | 1. Truy cập /user/orders/track/[id]<br>2. Trạng thái thanh toán thay đổi<br>3. Kiểm tra cập nhật | Trạng thái thanh toán được cập nhật ngay lập tức, badge được cập nhật màu sắc và text | | Untested | 11/15/2015 | |
| **FUNC-TDTTTT-03** | Hiển thị lịch sử trạng thái thanh toán | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra timeline | Timeline hiển thị các mốc: Chờ thanh toán, Đã thanh toán, Thanh toán thất bại, với thời gian cụ thể | | Pass | 11/15/2015 | |
| **FUNC-TDTTTT-04** | Thông báo cập nhật trạng thái thanh toán | 1. Truy cập /user/orders/track/[id]<br>2. Trạng thái thanh toán thay đổi<br>3. Kiểm tra thông báo | Hiển thị thông báo notification real-time khi trạng thái thanh toán thay đổi, có thể gửi qua email, SMS, push notification | | Untested | 11/15/2015 | |
| **FUNC-TDTTTT-05** | Xử lý lỗi thanh toán | 1. Truy cập /user/checkout<br>2. Thanh toán thất bại<br>3. Kiểm tra xử lý | Hiển thị thông báo lỗi cụ thể, hướng dẫn khắc phục, đơn hàng được giữ ở trạng thái "Chờ thanh toán" để thử lại | | Untested | 11/15/2015 | |

---

*Template này được tạo theo chuẩn Markdown để dễ dàng quản lý và cập nhật test cases.*

