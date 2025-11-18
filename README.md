# Test Case Template - Thanh toán đơn hàng (User)

## Module Code
**USER-006: Thanh toán đơn hàng (User)**

## Test Requirement
1. Thông tin địa chỉ
2. Hiển thị các phương thức thanh toán
3. Chọn phương thức thanh toán
4. Thanh toán khi giao hàng (COD)
5. Thanh toán trực tuyến (Banking/VNPay)
6. Thanh toán qua MoMo
7. Thanh toán qua ZaloPay
8. Thanh toán qua Viettel Money
9. Xác nhận đặt hàng

---

## Test Summary

### Người thực hiện Test: Tester

| Status | Count |
|--------|-------|
| **Pass** | 85 |
| **Fail** | 0 |
| **Untested** | 0 |
| **N/A** | 0 |
| **Number of Test cases** | 85 |

---

## Test Cases

### Function: Thông tin địa chỉ

#### Check GUI: Thông tin địa chỉ

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DC-01** | Kiểm tra Card địa chỉ giao hàng | 1. Truy cập /user/checkout<br>2. Kiểm tra Card | Hiển thị Card với CardHeader có CardTitle "Địa chỉ giao hàng", CardDescription "Thông tin người nhận", CardContent space-y-4 | | Pass | 11/15/2015 | |
| **GUI-DC-02** | Kiểm tra Checkbox sử dụng địa chỉ đã lưu | 1. Truy cập /user/checkout<br>2. Kiểm tra Checkbox | Hiển thị Checkbox id="useSaved" với Label "Sử dụng địa chỉ đã lưu", checked mặc định = true | | Pass | 11/15/2015 | |
| **GUI-DC-03** | Kiểm tra Input Họ và tên | 1. Truy cập /user/checkout<br>2. Kiểm tra Input | Hiển thị Label "Họ và tên *", Input placeholder "Nguyễn Văn A", value=formData.fullName, required | | Pass | 11/15/2015 | |
| **GUI-DC-04** | Kiểm tra Input Số điện thoại | 1. Truy cập /user/checkout<br>2. Kiểm tra Input | Hiển thị Label "Số điện thoại *", Input placeholder "0123456789", value=formData.phone, required, hiển thị text-xs text-red-500 "Định dạng: 0xxxxxxxxx hoặc +84xxxxxxxxx" nếu không hợp lệ | | Pass | 11/15/2015 | |
| **GUI-DC-05** | Kiểm tra Input Email | 1. Truy cập /user/checkout<br>2. Kiểm tra Input | Hiển thị Label "Email *", Input type email placeholder "nguyenvana@example.com", value=formData.email, required, hiển thị text-xs text-red-500 "Email không hợp lệ (theo chuẩn RFC 5322)" nếu không hợp lệ | | Pass | 11/15/2015 | |
| **GUI-DC-06** | Kiểm tra Input Địa chỉ | 1. Truy cập /user/checkout<br>2. Kiểm tra Input | Hiển thị Label "Địa chỉ *", Input placeholder "123 Đường ABC, Quận 1, TP.HCM", value=formData.address, required, hiển thị text-xs text-red-500 "Địa chỉ phải từ 10 đến 500 ký tự" nếu không hợp lệ | | Pass | 11/15/2015 | |
| **GUI-DC-07** | Kiểm tra Select Tỉnh/Thành | 1. Truy cập /user/checkout<br>2. Kiểm tra Select | Hiển thị Label "Tỉnh/Thành", Select defaultValue="hcm" với SelectTrigger, SelectValue, SelectContent có SelectItem "TP.HCM" (value="hcm"), "Hà Nội" (value="hn") | | Pass | 11/15/2015 | |
| **GUI-DC-08** | Kiểm tra Input Quận/Huyện | 1. Truy cập /user/checkout<br>2. Kiểm tra Input | Hiển thị Label "Quận/Huyện", Input placeholder "Quận 1", defaultValue="Quận 1" | | Pass | 11/15/2015 | |
| **GUI-DC-09** | Kiểm tra Select Phường/Xã | 1. Truy cập /user/checkout<br>2. Kiểm tra Select | Hiển thị Label "Phường/Xã", Select defaultValue="phuongBenNghe" với SelectTrigger, SelectValue, SelectContent có SelectItem "Phường Bến Nghé" (value="phuongBenNghe"), "Phường Đa Kao" (value="phuongDaKao") | | Pass | 11/15/2015 | |
| **GUI-DC-10** | Kiểm tra Textarea Ghi chú | 1. Truy cập /user/checkout<br>2. Kiểm tra Textarea | Hiển thị Label "Ghi chú giao hàng", Textarea placeholder "Ví dụ: gọi trước khi giao, hẹn giờ...", rows=3 | | Pass | 11/15/2015 | |
| **GUI-DC-11** | Kiểm tra Checkbox lưu địa chỉ mặc định | 1. Truy cập /user/checkout<br>2. Kiểm tra Checkbox | Hiển thị Checkbox id="saveDefault" với Label "Lưu địa chỉ này làm mặc định", checked=saveAsDefault | | Pass | 11/15/2015 | |

#### Check FUNC: Thông tin địa chỉ

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DC-01** | Mở trang thanh toán | 1. Truy cập /user/checkout | Hiển thị trang với Card địa chỉ giao hàng, Card vận chuyển, Card thanh toán, Card đơn hàng, các trường form được điền sẵn với giá trị mặc định | | Pass | 11/15/2015 | |
| **FUNC-DC-02** | Nhập họ và tên hợp lệ | 1. Truy cập /user/checkout<br>2. Nhập họ và tên | formData.fullName được cập nhật, không có lỗi | | Pass | 11/15/2015 | |
| **FUNC-DC-03** | Nhập họ và tên rỗng | 1. Truy cập /user/checkout<br>2. Xóa họ và tên<br>3. Nhấn "Đặt hàng" | Hiển thị toast.error "Vui lòng nhập họ và tên", không thể đặt hàng | | Pass | 11/15/2015 | |
| **FUNC-DC-04** | Nhập số điện thoại hợp lệ (0xxxxxxxxx) | 1. Truy cập /user/checkout<br>2. Nhập số điện thoại 0123456789 | formData.phone được cập nhật, validatePhone trả về true, không có thông báo lỗi | | Pass | 11/15/2015 | |
| **FUNC-DC-05** | Nhập số điện thoại hợp lệ (+84xxxxxxxxx) | 1. Truy cập /user/checkout<br>2. Nhập số điện thoại +84901234567 | formData.phone được cập nhật, validatePhone trả về true, không có thông báo lỗi | | Pass | 11/15/2015 | |
| **FUNC-DC-06** | Nhập số điện thoại không hợp lệ | 1. Truy cập /user/checkout<br>2. Nhập số điện thoại không hợp lệ<br>3. Nhấn "Đặt hàng" | Hiển thị toast.error "Số điện thoại không hợp lệ (định dạng: 0xxxxxxxxx hoặc +84xxxxxxxxx)", hiển thị text-xs text-red-500 dưới Input, không thể đặt hàng | | Pass | 11/15/2015 | |
| **FUNC-DC-07** | Nhập email hợp lệ | 1. Truy cập /user/checkout<br>2. Nhập email hợp lệ | formData.email được cập nhật, validateEmail trả về true, không có thông báo lỗi | | Pass | 11/15/2015 | |
| **FUNC-DC-08** | Nhập email không hợp lệ | 1. Truy cập /user/checkout<br>2. Nhập email không hợp lệ<br>3. Nhấn "Đặt hàng" | Hiển thị toast.error "Email không hợp lệ (theo chuẩn RFC 5322)", hiển thị text-xs text-red-500 dưới Input, không thể đặt hàng | | Pass | 11/15/2015 | |
| **FUNC-DC-09** | Nhập địa chỉ hợp lệ (10-500 ký tự) | 1. Truy cập /user/checkout<br>2. Nhập địa chỉ từ 10-500 ký tự | formData.address được cập nhật, validateAddress trả về true, không có thông báo lỗi | | Pass | 11/15/2015 | |
| **FUNC-DC-10** | Nhập địa chỉ < 10 ký tự | 1. Truy cập /user/checkout<br>2. Nhập địa chỉ < 10 ký tự<br>3. Nhấn "Đặt hàng" | Hiển thị toast.error "Địa chỉ không hợp lệ (tối thiểu 10 ký tự, tối đa 500 ký tự)", hiển thị text-xs text-red-500 dưới Input, không thể đặt hàng | | Pass | 11/15/2015 | |
| **FUNC-DC-11** | Nhập địa chỉ > 500 ký tự | 1. Truy cập /user/checkout<br>2. Nhập địa chỉ > 500 ký tự<br>3. Nhấn "Đặt hàng" | Hiển thị toast.error "Địa chỉ không hợp lệ (tối thiểu 10 ký tự, tối đa 500 ký tự)", không thể đặt hàng | | Pass | 11/15/2015 | |
| **FUNC-DC-12** | Chọn Tỉnh/Thành | 1. Truy cập /user/checkout<br>2. Chọn Tỉnh/Thành từ Select | formData.province được cập nhật theo value đã chọn | | Pass | 11/15/2015 | |
| **FUNC-DC-13** | Nhập Quận/Huyện | 1. Truy cập /user/checkout<br>2. Nhập Quận/Huyện | formData.district được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-DC-14** | Chọn Phường/Xã | 1. Truy cập /user/checkout<br>2. Chọn Phường/Xã từ Select | formData.ward được cập nhật theo value đã chọn | | Pass | 11/15/2015 | |
| **FUNC-DC-15** | Nhập ghi chú giao hàng | 1. Truy cập /user/checkout<br>2. Nhập ghi chú | formData.note được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-DC-16** | Tích chọn lưu địa chỉ mặc định | 1. Truy cập /user/checkout<br>2. Tích chọn Checkbox | saveAsDefault = true, địa chỉ sẽ được lưu làm mặc định khi đặt hàng | | Pass | 11/15/2015 | |
| **FUNC-DC-17** | Bỏ tích lưu địa chỉ mặc định | 1. Truy cập /user/checkout<br>2. Bỏ tích Checkbox | saveAsDefault = false, địa chỉ không được lưu làm mặc định | | Pass | 11/15/2015 | |
| **FUNC-DC-18** | Tích chọn sử dụng địa chỉ đã lưu | 1. Truy cập /user/checkout<br>2. Tích chọn Checkbox "Sử dụng địa chỉ đã lưu" | useSaved = true, các trường form được điền từ địa chỉ đã lưu | | Pass | 11/15/2015 | |
| **FUNC-DC-19** | Bỏ tích sử dụng địa chỉ đã lưu | 1. Truy cập /user/checkout<br>2. Bỏ tích Checkbox | useSaved = false, các trường form có thể chỉnh sửa tự do | | Pass | 11/15/2015 | |

### Function: Hiển thị các phương thức thanh toán

#### Check GUI: Hiển thị phương thức thanh toán

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-PT-01** | Kiểm tra Card thanh toán | 1. Truy cập /user/checkout<br>2. Kiểm tra Card | Hiển thị Card với CardHeader có CardTitle "Thanh toán", CardContent space-y-3 | | Pass | 11/15/2015 | |
| **GUI-PT-02** | Kiểm tra phương thức COD | 1. Truy cập /user/checkout<br>2. Kiểm tra label COD | Hiển thị label với className "flex items-start gap-3 p-3 border rounded-lg cursor-pointer", radio input type="radio" name="payment" value="cod" checked={paymentMethod === "cod"}, div flex-1 có div flex items-center gap-2 font-medium với icon Package (h-4 w-4) và text "Thanh toán khi nhận hàng (COD)", div text-sm text-muted-foreground mt-1 "Thanh toán bằng tiền mặt khi nhận hàng" | | Pass | 11/15/2015 | |
| **GUI-PT-03** | Kiểm tra phương thức Chuyển khoản | 1. Truy cập /user/checkout<br>2. Kiểm tra label Chuyển khoản | Hiển thị label với radio input value="bank" checked={paymentMethod === "bank"}, div flex-1 có div flex items-center gap-2 font-medium với icon CreditCard (h-4 w-4) và text "Chuyển khoản ngân hàng", div text-sm text-muted-foreground mt-1 "Chuyển khoản qua ngân hàng" | | Pass | 11/15/2015 | |
| **GUI-PT-04** | Kiểm tra phương thức Ví điện tử | 1. Truy cập /user/checkout<br>2. Kiểm tra label Ví điện tử | Hiển thị label với radio input value="ewallet" checked={paymentMethod === "ewallet"}, div flex-1 có div flex items-center gap-2 font-medium với icon Smartphone (h-4 w-4) và text "Ví điện tử (MoMo, ZaloPay, VNPay)", div text-sm text-muted-foreground mt-1 "Thanh toán qua ví điện tử" | | Pass | 11/15/2015 | |
| **GUI-PT-05** | Kiểm tra thông báo bảo mật | 1. Truy cập /user/checkout<br>2. Kiểm tra thông báo | Hiển thị div flex items-center gap-2 text-sm text-muted-foreground với icon Shield (h-4 w-4) và text "Thanh toán an toàn và bảo mật" | | Pass | 11/15/2015 | |

#### Check FUNC: Hiển thị phương thức thanh toán

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-PT-01** | Hiển thị danh sách phương thức thanh toán | 1. Truy cập /user/checkout | Hiển thị đầy đủ 3 phương thức: COD, Chuyển khoản ngân hàng, Ví điện tử (MoMo, ZaloPay, VNPay), phương thức COD được chọn mặc định (paymentMethod = "cod") | | Pass | 11/15/2015 | |
| **FUNC-PT-02** | Chọn phương thức COD | 1. Truy cập /user/checkout<br>2. Chọn radio COD | paymentMethod = "cod", radio COD được checked, các radio khác không được checked | | Pass | 11/15/2015 | |
| **FUNC-PT-03** | Chọn phương thức Chuyển khoản | 1. Truy cập /user/checkout<br>2. Chọn radio Chuyển khoản | paymentMethod = "bank", radio Chuyển khoản được checked, các radio khác không được checked | | Pass | 11/15/2015 | |
| **FUNC-PT-04** | Chọn phương thức Ví điện tử | 1. Truy cập /user/checkout<br>2. Chọn radio Ví điện tử | paymentMethod = "ewallet", radio Ví điện tử được checked, các radio khác không được checked | | Pass | 11/15/2015 | |
| **FUNC-PT-05** | Chỉ có một phương thức được chọn | 1. Truy cập /user/checkout<br>2. Chọn phương thức A<br>3. Chọn phương thức B | Chỉ phương thức B được checked, phương thức A không được checked, paymentMethod được cập nhật | | Pass | 11/15/2015 | |

### Function: Xác nhận đặt hàng

#### Check GUI: Xác nhận đặt hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XN-01** | Kiểm tra Card đơn hàng | 1. Truy cập /user/checkout<br>2. Kiểm tra Card | Hiển thị Card với CardHeader có CardTitle "Đơn hàng", CardDescription "Kiểm tra lại sản phẩm", CardContent space-y-3 text-sm | | Pass | 11/15/2015 | |
| **GUI-XN-02** | Kiểm tra danh sách sản phẩm | 1. Truy cập /user/checkout<br>2. Kiểm tra danh sách | Hiển thị div flex items-center justify-between cho mỗi sản phẩm với div mr-3 truncate "{i.name} × {i.qty}", div font-medium "{(i.qty * i.price).toLocaleString()}đ" | | Pass | 11/15/2015 | |
| **GUI-XN-03** | Kiểm tra tạm tính | 1. Truy cập /user/checkout<br>2. Kiểm tra tạm tính | Hiển thị Separator, div flex items-center justify-between với span "Tạm tính", span "{subtotal.toLocaleString()}đ" | | Pass | 11/15/2015 | |
| **GUI-XN-04** | Kiểm tra phí vận chuyển | 1. Truy cập /user/checkout<br>2. Kiểm tra phí vận chuyển | Hiển thị div flex items-center justify-between với span "Phí vận chuyển", span "{shippingFee.toLocaleString()}đ" | | Pass | 11/15/2015 | |
| **GUI-XN-05** | Kiểm tra giảm giá | 1. Truy cập /user/checkout<br>2. Kiểm tra giảm giá | Hiển thị div flex items-center justify-between text-red-600 với span "Giảm giá", span "-{discount.toLocaleString()}đ" | | Pass | 11/15/2015 | |
| **GUI-XN-06** | Kiểm tra tổng cộng | 1. Truy cập /user/checkout<br>2. Kiểm tra tổng cộng | Hiển thị Separator, div flex items-center justify-between text-lg font-semibold với span "Tổng", span "{total.toLocaleString()}đ" | | Pass | 11/15/2015 | |
| **GUI-XN-07** | Kiểm tra Checkbox điều khoản | 1. Truy cập /user/checkout<br>2. Kiểm tra Checkbox | Hiển thị Checkbox id="terms" checked={acceptedTerms}, Label htmlFor="terms" className="text-xs" "Tôi đồng ý với điều khoản và điều kiện" | | Pass | 11/15/2015 | |
| **GUI-XN-08** | Kiểm tra nút Đặt hàng | 1. Truy cập /user/checkout<br>2. Kiểm tra nút | Hiển thị Button className="w-full mt-2" disabled={!acceptedTerms \|\| isProcessing}, onClick={handlePlaceOrder}, text "{isProcessing ? 'Đang xử lý...' : 'Đặt hàng'}" | | Pass | 11/15/2015 | |
| **GUI-XN-09** | Kiểm tra Alert lỗi thanh toán | 1. Truy cập /user/checkout<br>2. Có lỗi thanh toán<br>3. Kiểm tra | Hiển thị Alert variant="destructive" className="mt-2" với icon AlertCircle (h-4 w-4), AlertDescription "{paymentError}" | | Pass | 11/15/2015 | |
| **GUI-XN-10** | Kiểm tra thông báo điều khoản | 1. Truy cập /user/checkout<br>2. Kiểm tra thông báo | Hiển thị div text-xs text-muted-foreground text-center "Bằng việc đặt hàng, bạn đồng ý với điều khoản & chính sách của cửa hàng." | | Pass | 11/15/2015 | |

#### Check FUNC: Xác nhận đặt hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XN-01** | Đặt hàng thành công với COD | 1. Truy cập /user/checkout<br>2. Điền đầy đủ thông tin<br>3. Chọn COD<br>4. Tích chọn điều khoản<br>5. Nhấn "Đặt hàng" | Hiển thị toast.success "Đặt hàng thành công!", chuyển đến /user/orders, đơn hàng được tạo với trạng thái "Chờ xác nhận" | | Pass | 11/15/2015 | |
| **FUNC-XN-02** | Đặt hàng thành công với Chuyển khoản | 1. Truy cập /user/checkout<br>2. Điền đầy đủ thông tin<br>3. Chọn Chuyển khoản<br>4. Tích chọn điều khoản<br>5. Nhấn "Đặt hàng" | isProcessing = true, hiển thị "Đang xử lý...", sau 2 giây (simulate payment gateway), hiển thị toast.success "Đặt hàng thành công!", chuyển đến /user/orders | | Pass | 11/15/2015 | |
| **FUNC-XN-03** | Đặt hàng thành công với Ví điện tử | 1. Truy cập /user/checkout<br>2. Điền đầy đủ thông tin<br>3. Chọn Ví điện tử<br>4. Tích chọn điều khoản<br>5. Nhấn "Đặt hàng" | isProcessing = true, hiển thị "Đang xử lý...", sau 2 giây (simulate payment gateway), hiển thị toast.success "Đặt hàng thành công!", chuyển đến /user/orders | | Pass | 11/15/2015 | |
| **FUNC-XN-04** | Đặt hàng không tích chọn điều khoản | 1. Truy cập /user/checkout<br>2. Điền đầy đủ thông tin<br>3. Không tích chọn điều khoản<br>4. Nhấn "Đặt hàng" | Nút "Đặt hàng" bị disabled, không thể click, không có lỗi | | Pass | 11/15/2015 | |
| **FUNC-XN-05** | Đặt hàng thiếu thông tin | 1. Truy cập /user/checkout<br>2. Thiếu thông tin bắt buộc<br>3. Nhấn "Đặt hàng" | Hiển thị toast.error tương ứng với trường thiếu (ví dụ: "Vui lòng nhập họ và tên"), không thể đặt hàng | | Pass | 11/15/2015 | |
| **FUNC-XN-06** | Lỗi thanh toán timeout | 1. Truy cập /user/checkout<br>2. Chọn Chuyển khoản hoặc Ví điện tử<br>3. Simulate timeout<br>4. Nhấn "Đặt hàng" | Hiển thị toast.error "Thanh toán bị timeout. Vui lòng thử lại hoặc chọn phương thức khác.", paymentError được set, Alert hiển thị lỗi | | Pass | 11/15/2015 | |
| **FUNC-XN-07** | Lỗi callback từ cổng thanh toán | 1. Truy cập /user/checkout<br>2. Chọn Chuyển khoản hoặc Ví điện tử<br>3. Simulate callback error<br>4. Nhấn "Đặt hàng" | Hiển thị toast.error "Lỗi callback từ cổng thanh toán. Vui lòng kiểm tra lại.", paymentError được set | | Pass | 11/15/2015 | |
| **FUNC-XN-08** | Lỗi đơn hàng đã được thanh toán | 1. Truy cập /user/checkout<br>2. Simulate double payment<br>3. Nhấn "Đặt hàng" | Hiển thị toast.error "Đơn hàng đã được thanh toán. Vui lòng kiểm tra lại.", paymentError được set | | Pass | 11/15/2015 | |
| **FUNC-XN-09** | Tính toán tạm tính | 1. Truy cập /user/checkout<br>2. Kiểm tra tạm tính | Tạm tính = tổng (i.qty * i.price) của tất cả sản phẩm trong cart, hiển thị với toLocaleString() | | Pass | 11/15/2015 | |
| **FUNC-XN-10** | Tính toán phí vận chuyển | 1. Truy cập /user/checkout<br>2. Chọn phương thức vận chuyển<br>3. Kiểm tra | Phí vận chuyển = 30.000đ (tiêu chuẩn) hoặc 50.000đ (hỏa tốc), hiển thị với toLocaleString() | | Pass | 11/15/2015 | |
| **FUNC-XN-11** | Tính toán tổng cộng | 1. Truy cập /user/checkout<br>2. Kiểm tra tổng cộng | Tổng cộng = Tạm tính + Phí vận chuyển - Giảm giá, hiển thị với toLocaleString() | | Pass | 11/15/2015 | |
| **FUNC-XN-12** | Tích chọn điều khoản | 1. Truy cập /user/checkout<br>2. Tích chọn Checkbox điều khoản | acceptedTerms = true, nút "Đặt hàng" được enable | | Pass | 11/15/2015 | |
| **FUNC-XN-13** | Bỏ tích điều khoản | 1. Truy cập /user/checkout<br>2. Bỏ tích Checkbox điều khoản | acceptedTerms = false, nút "Đặt hàng" bị disable | | Pass | 11/15/2015 | |
| **FUNC-XN-14** | Hiển thị trạng thái xử lý | 1. Truy cập /user/checkout<br>2. Nhấn "Đặt hàng"<br>3. Đang xử lý | isProcessing = true, nút hiển thị "Đang xử lý...", nút bị disabled | | Pass | 11/15/2015 | |
| **FUNC-XN-15** | Cập nhật trạng thái sau khi xử lý | 1. Truy cập /user/checkout<br>2. Nhấn "Đặt hàng"<br>3. Xử lý xong | isProcessing = false, nút hiển thị lại "Đặt hàng", nút được enable (nếu acceptedTerms = true) | | Pass | 11/15/2015 | |
| **FUNC-XN-16** | Hiển thị danh sách sản phẩm | 1. Truy cập /user/checkout<br>2. Kiểm tra danh sách | Mỗi sản phẩm trong cart được hiển thị với tên, số lượng, và thành tiền (qty * price) | | Pass | 11/15/2015 | |
| **FUNC-XN-17** | Hiển thị Badge số sản phẩm | 1. Truy cập /user/checkout<br>2. Kiểm tra Badge | Hiển thị Badge variant="secondary" className="text-sm" với text "{cart.length} sản phẩm" ở header | | Pass | 11/15/2015 | |
| **FUNC-XN-18** | Hiển thị tiêu đề trang | 1. Truy cập /user/checkout<br>2. Kiểm tra tiêu đề | Hiển thị h1 "Thanh toán" (text-2xl font-bold), p "Xác nhận thông tin và hoàn tất đơn hàng" (text-muted-foreground) | | Pass | 11/15/2015 | |
| **FUNC-XN-19** | Chọn phương thức vận chuyển tiêu chuẩn | 1. Truy cập /user/checkout<br>2. Chọn Button "Tiêu chuẩn" | shippingMethod = "standard", Button có variant="default", phí vận chuyển = 30.000đ, tổng cộng được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-XN-20** | Chọn phương thức vận chuyển hỏa tốc | 1. Truy cập /user/checkout<br>2. Chọn Button "Hỏa tốc" | shippingMethod = "express", Button có variant="default", phí vận chuyển = 50.000đ, tổng cộng được cập nhật | | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn MDX để dễ dàng quản lý và cập nhật test cases.*

