# Test Case Template - Cài đặt hệ thống (Admin)

## Module Code
**Model Management Store: Cài đặt hệ thống Admin**

## Test Requirement
1. Cài đặt chính sách giảm giá sản phẩm
2. Cài đặt chính sách giảm giá toàn bộ
3. Cài đặt thanh toán
4. Cài đặt thông tin shop
5. Cài đặt chung

---

## Test Summary

### Người thực hiện Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 42 |
| **Fail** | 0 |
| **Untested** | 47 |
| **N/A** | 0 |
| **Number of Test cases** | 89 |

---

## Test Cases

### Function: Cài đặt chính sách giảm giá sản phẩm

#### Check GUI: Cài đặt chính sách giảm giá sản phẩm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CSGGSP-01** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/settings/product-discounts<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Chính sách giảm giá sản phẩm" với kích thước text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-CSGGSP-02** | Kiểm tra mô tả chức năng | 1. Truy cập /admin/settings/product-discounts<br>2. Kiểm tra mô tả | Hiển thị mô tả "Tạo/chỉnh sửa giảm giá riêng từng SKU" màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-CSGGSP-03** | Kiểm tra Select Chọn sản phẩm | 1. Truy cập /admin/settings/product-discounts<br>2. Kiểm tra Select | Hiển thị label "Chọn sản phẩm *", Select với placeholder "Tìm theo tên/SKU...", có thể tìm kiếm và chọn sản phẩm | | Pass | 11/15/2015 | |
| **GUI-CSGGSP-04** | Kiểm tra Select Loại giảm giá | 1. Truy cập /admin/settings/product-discounts<br>2. Kiểm tra Select | Hiển thị label "Loại giảm giá *", Select với placeholder "Chọn loại giảm giá", có các option: Phần trăm, Cố định | | Pass | 11/15/2015 | |
| **GUI-CSGGSP-05** | Kiểm tra Input Mức giảm | 1. Truy cập /admin/settings/product-discounts<br>2. Kiểm tra Input | Hiển thị label "Mức giảm *", input type number với placeholder "Nhập mức giảm...", có đơn vị hiển thị (% hoặc VNĐ) tùy theo loại giảm giá | | Pass | 11/15/2015 | |
| **GUI-CSGGSP-06** | Kiểm tra Date Range Thời gian hiệu lực | 1. Truy cập /admin/settings/product-discounts<br>2. Kiểm tra Date Range | Hiển thị label "Thời gian hiệu lực *", 2 input date với text "đến" ở giữa, label "Ngày bắt đầu" và "Ngày kết thúc" | | Pass | 11/15/2015 | |
| **GUI-CSGGSP-07** | Kiểm tra Input Điều kiện | 1. Truy cập /admin/settings/product-discounts<br>2. Kiểm tra Input | Hiển thị label "Điều kiện", input type number với placeholder "Đơn hàng tối thiểu (VNĐ)...", có thể thêm nhiều điều kiện | | Pass | 11/15/2015 | |
| **GUI-CSGGSP-08** | Kiểm tra nút Lưu | 1. Truy cập /admin/settings/product-discounts<br>2. Kiểm tra nút | Hiển thị nút "Lưu" type submit | | Pass | 11/15/2015 | |
| **GUI-CSGGSP-09** | Kiểm tra nút Hủy | 1. Truy cập /admin/settings/product-discounts<br>2. Kiểm tra nút | Hiển thị nút "Hủy" variant outline | | Pass | 11/15/2015 | |

---

### Check FUNC: Cài đặt chính sách giảm giá sản phẩm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CSGGSP-01** | Mở trang cài đặt chính sách giảm giá sản phẩm | 1. Truy cập /admin/settings/product-discounts | Hiển thị trang với tiêu đề, mô tả, Select Chọn sản phẩm, Select Loại giảm giá, Input Mức giảm, Date Range Thời gian hiệu lực, Input Điều kiện, nút Lưu, nút Hủy | | Pass | 11/15/2015 | |
| **FUNC-CSGGSP-02** | Tạo chính sách giảm giá sản phẩm thành công - Phần trăm | 1. Truy cập /admin/settings/product-discounts<br>2. Chọn sản phẩm<br>3. Chọn loại giảm giá "Phần trăm"<br>4. Nhập mức giảm (VD: 10)<br>5. Chọn thời gian hiệu lực<br>6. Nhập điều kiện (tùy chọn)<br>7. Click "Lưu" | Hiển thị thông báo "Lưu chính sách giảm giá thành công", chính sách được lưu và có hiệu lực, sản phẩm được áp dụng giảm giá | | Untested | 11/15/2015 | |
| **FUNC-CSGGSP-03** | Tạo chính sách giảm giá sản phẩm thành công - Cố định | 1. Truy cập /admin/settings/product-discounts<br>2. Chọn sản phẩm<br>3. Chọn loại giảm giá "Cố định"<br>4. Nhập mức giảm (VD: 50000 VNĐ)<br>5. Chọn thời gian hiệu lực<br>6. Click "Lưu" | Hiển thị thông báo "Lưu chính sách giảm giá thành công", chính sách được lưu và có hiệu lực | | Untested | 11/15/2015 | |
| **FUNC-CSGGSP-04** | Tạo - Thiếu Chọn sản phẩm | 1. Truy cập /admin/settings/product-discounts<br>2. Không chọn sản phẩm<br>3. Điền các trường khác<br>4. Click "Lưu" | Hiển thị thông báo lỗi "Vui lòng chọn sản phẩm", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-CSGGSP-05** | Tạo - Thiếu Loại giảm giá | 1. Truy cập /admin/settings/product-discounts<br>2. Chọn sản phẩm<br>3. Không chọn loại giảm giá<br>4. Điền các trường khác<br>5. Click "Lưu" | Hiển thị thông báo lỗi "Vui lòng chọn loại giảm giá", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-CSGGSP-06** | Tạo - Thiếu Mức giảm | 1. Truy cập /admin/settings/product-discounts<br>2. Chọn sản phẩm và loại giảm giá<br>3. Để trống mức giảm<br>4. Click "Lưu" | Hiển thị thông báo lỗi "Mức giảm không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-CSGGSP-07** | Tạo - Mức giảm không hợp lệ (Phần trăm > 100) | 1. Truy cập /admin/settings/product-discounts<br>2. Chọn sản phẩm<br>3. Chọn loại giảm giá "Phần trăm"<br>4. Nhập mức giảm > 100<br>5. Click "Lưu" | Hiển thị thông báo lỗi "Mức giảm phần trăm không được vượt quá 100%", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-CSGGSP-08** | Tạo - Thiếu Thời gian hiệu lực | 1. Truy cập /admin/settings/product-discounts<br>2. Chọn sản phẩm và điền các trường<br>3. Không chọn thời gian hiệu lực<br>4. Click "Lưu" | Hiển thị thông báo lỗi "Vui lòng chọn thời gian hiệu lực", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-CSGGSP-09** | Tạo - Ngày kết thúc trước ngày bắt đầu | 1. Truy cập /admin/settings/product-discounts<br>2. Chọn sản phẩm và điền các trường<br>3. Chọn ngày kết thúc trước ngày bắt đầu<br>4. Click "Lưu" | Hiển thị thông báo lỗi "Ngày kết thúc phải sau ngày bắt đầu", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-CSGGSP-10** | Click nút Hủy | 1. Truy cập /admin/settings/product-discounts<br>2. Điền thông tin<br>3. Click "Hủy" | Form được reset hoặc chuyển về trang trước, không lưu chính sách | | Pass | 11/15/2015 | |
| **FUNC-CSGGSP-11** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/settings/product-discounts<br>2. Điền đầy đủ thông tin<br>3. Tắt kết nối mạng<br>4. Click "Lưu" | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", form không được gửi | | Untested | 11/15/2015 | |
| **FUNC-CSGGSP-12** | Xử lý khi server lỗi | 1. Truy cập /admin/settings/product-discounts<br>2. Điền đầy đủ thông tin<br>3. Server trả về lỗi 500<br>4. Click "Lưu" | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau", form không được gửi | | Untested | 11/15/2015 | |

---

### Function: Cài đặt chính sách giảm giá toàn bộ

#### Check GUI: Cài đặt chính sách giảm giá toàn bộ

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CSGGTB-01** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/settings/global-discounts<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Chính sách giảm giá toàn bộ" với kích thước text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-CSGGTB-02** | Kiểm tra mô tả chức năng | 1. Truy cập /admin/settings/global-discounts<br>2. Kiểm tra mô tả | Hiển thị mô tả "Tạo chính sách khuyến mãi/voucher" màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-CSGGTB-03** | Kiểm tra Select Loại ưu đãi | 1. Truy cập /admin/settings/global-discounts<br>2. Kiểm tra Select | Hiển thị label "Loại ưu đãi *", Select với placeholder "Chọn loại ưu đãi", có các option: Mã giảm, Tự động | | Pass | 11/15/2015 | |
| **GUI-CSGGTB-04** | Kiểm tra Input Mã giảm (khi chọn Mã giảm) | 1. Truy cập /admin/settings/global-discounts<br>2. Chọn "Mã giảm"<br>3. Kiểm tra Input | Hiển thị label "Mã giảm *", input type text với placeholder "Nhập mã giảm (VD: SALE10)" | | Pass | 11/15/2015 | |
| **GUI-CSGGTB-05** | Kiểm tra Input Mức giảm | 1. Truy cập /admin/settings/global-discounts<br>2. Kiểm tra Input | Hiển thị label "Mức giảm *", input type number với placeholder "Nhập mức giảm...", có Select đơn vị (% hoặc VNĐ) | | Pass | 11/15/2015 | |
| **GUI-CSGGTB-06** | Kiểm tra Input Điều kiện áp dụng | 1. Truy cập /admin/settings/global-discounts<br>2. Kiểm tra Input | Hiển thị label "Điều kiện áp dụng", các input: Đơn tối thiểu (VNĐ), Nhóm sản phẩm (Select), Khách hàng (Select), có thể thêm nhiều điều kiện | | Pass | 11/15/2015 | |
| **GUI-CSGGTB-07** | Kiểm tra Date Range Thời gian hiệu lực | 1. Truy cập /admin/settings/global-discounts<br>2. Kiểm tra Date Range | Hiển thị label "Thời gian hiệu lực *", 2 input date với text "đến" ở giữa | | Pass | 11/15/2015 | |
| **GUI-CSGGTB-08** | Kiểm tra nút Lưu | 1. Truy cập /admin/settings/global-discounts<br>2. Kiểm tra nút | Hiển thị nút "Lưu" type submit | | Pass | 11/15/2015 | |
| **GUI-CSGGTB-09** | Kiểm tra nút Hủy | 1. Truy cập /admin/settings/global-discounts<br>2. Kiểm tra nút | Hiển thị nút "Hủy" variant outline | | Pass | 11/15/2015 | |

---

### Check FUNC: Cài đặt chính sách giảm giá toàn bộ

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CSGGTB-01** | Mở trang cài đặt chính sách giảm giá toàn bộ | 1. Truy cập /admin/settings/global-discounts | Hiển thị trang với tiêu đề, mô tả, Select Loại ưu đãi, Input Mã giảm (nếu chọn Mã giảm), Input Mức giảm, Input Điều kiện áp dụng, Date Range Thời gian hiệu lực, nút Lưu, nút Hủy | | Pass | 11/15/2015 | |
| **FUNC-CSGGTB-02** | Tạo chính sách giảm giá toàn bộ thành công - Mã giảm | 1. Truy cập /admin/settings/global-discounts<br>2. Chọn loại ưu đãi "Mã giảm"<br>3. Nhập mã giảm<br>4. Nhập mức giảm<br>5. Nhập điều kiện áp dụng (tùy chọn)<br>6. Chọn thời gian hiệu lực<br>7. Click "Lưu" | Hiển thị thông báo "Lưu chính sách giảm giá thành công", chính sách được lưu và áp dụng đúng theo điều kiện | | Untested | 11/15/2015 | |
| **FUNC-CSGGTB-03** | Tạo chính sách giảm giá toàn bộ thành công - Tự động | 1. Truy cập /admin/settings/global-discounts<br>2. Chọn loại ưu đãi "Tự động"<br>3. Nhập mức giảm<br>4. Nhập điều kiện áp dụng<br>5. Chọn thời gian hiệu lực<br>6. Click "Lưu" | Hiển thị thông báo "Lưu chính sách giảm giá thành công", chính sách được lưu và tự động áp dụng khi đáp ứng điều kiện | | Untested | 11/15/2015 | |
| **FUNC-CSGGTB-04** | Tạo - Thiếu Loại ưu đãi | 1. Truy cập /admin/settings/global-discounts<br>2. Không chọn loại ưu đãi<br>3. Điền các trường khác<br>4. Click "Lưu" | Hiển thị thông báo lỗi "Vui lòng chọn loại ưu đãi", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-CSGGTB-05** | Tạo - Thiếu Mã giảm (khi chọn Mã giảm) | 1. Truy cập /admin/settings/global-discounts<br>2. Chọn "Mã giảm"<br>3. Để trống mã giảm<br>4. Điền các trường khác<br>5. Click "Lưu" | Hiển thị thông báo lỗi "Mã giảm không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-CSGGTB-06** | Tạo - Mã giảm đã tồn tại | 1. Truy cập /admin/settings/global-discounts<br>2. Chọn "Mã giảm"<br>3. Nhập mã giảm đã tồn tại<br>4. Điền các trường khác<br>5. Click "Lưu" | Hiển thị thông báo lỗi "Mã giảm đã tồn tại trong hệ thống", form không được gửi | | Untested | 11/15/2015 | |
| **FUNC-CSGGTB-07** | Tạo - Thiếu Mức giảm | 1. Truy cập /admin/settings/global-discounts<br>2. Chọn loại ưu đãi<br>3. Để trống mức giảm<br>4. Click "Lưu" | Hiển thị thông báo lỗi "Mức giảm không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-CSGGTB-08** | Tạo - Thiếu Thời gian hiệu lực | 1. Truy cập /admin/settings/global-discounts<br>2. Chọn loại ưu đãi và điền các trường<br>3. Không chọn thời gian hiệu lực<br>4. Click "Lưu" | Hiển thị thông báo lỗi "Vui lòng chọn thời gian hiệu lực", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-CSGGTB-09** | Click nút Hủy | 1. Truy cập /admin/settings/global-discounts<br>2. Điền thông tin<br>3. Click "Hủy" | Form được reset hoặc chuyển về trang trước, không lưu chính sách | | Pass | 11/15/2015 | |
| **FUNC-CSGGTB-10** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/settings/global-discounts<br>2. Điền đầy đủ thông tin<br>3. Tắt kết nối mạng<br>4. Click "Lưu" | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", form không được gửi | | Untested | 11/15/2015 | |
| **FUNC-CSGGTB-11** | Xử lý khi server lỗi | 1. Truy cập /admin/settings/global-discounts<br>2. Điền đầy đủ thông tin<br>3. Server trả về lỗi 500<br>4. Click "Lưu" | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau", form không được gửi | | Untested | 11/15/2015 | |

---

### Function: Cài đặt thanh toán

#### Check GUI: Cài đặt thanh toán

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CDTT-01** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/settings/payments<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Cài đặt thanh toán" với kích thước text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-CDTT-02** | Kiểm tra mô tả chức năng | 1. Truy cập /admin/settings/payments<br>2. Kiểm tra mô tả | Hiển thị mô tả "Cấu hình phương thức thanh toán" màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-CDTT-03** | Kiểm tra Toggle COD | 1. Truy cập /admin/settings/payments<br>2. Kiểm tra Toggle | Hiển thị Toggle "COD" với label "Thanh toán khi nhận hàng", có thể bật/tắt | | Pass | 11/15/2015 | |
| **GUI-CDTT-04** | Kiểm tra Toggle Banking | 1. Truy cập /admin/settings/payments<br>2. Kiểm tra Toggle | Hiển thị Toggle "Banking" với label "Chuyển khoản ngân hàng", có thể bật/tắt | | Pass | 11/15/2015 | |
| **GUI-CDTT-05** | Kiểm tra Toggle VNPay | 1. Truy cập /admin/settings/payments<br>2. Kiểm tra Toggle | Hiển thị Toggle "VNPay" với label "VNPay", có thể bật/tắt, khi bật hiển thị Form thông tin cổng | | Pass | 11/15/2015 | |
| **GUI-CDTT-06** | Kiểm tra Toggle MoMo | 1. Truy cập /admin/settings/payments<br>2. Kiểm tra Toggle | Hiển thị Toggle "MoMo" với label "MoMo", có thể bật/tắt, khi bật hiển thị Form thông tin cổng | | Pass | 11/15/2015 | |
| **GUI-CDTT-07** | Kiểm tra Toggle ZaloPay | 1. Truy cập /admin/settings/payments<br>2. Kiểm tra Toggle | Hiển thị Toggle "ZaloPay" với label "ZaloPay", có thể bật/tắt, khi bật hiển thị Form thông tin cổng | | Pass | 11/15/2015 | |
| **GUI-CDTT-08** | Kiểm tra Toggle Viettel Money | 1. Truy cập /admin/settings/payments<br>2. Kiểm tra Toggle | Hiển thị Toggle "Viettel Money" với label "Viettel Money", có thể bật/tắt, khi bật hiển thị Form thông tin cổng | | Pass | 11/15/2015 | |
| **GUI-CDTT-09** | Kiểm tra Form Thông tin cổng (VNPay) | 1. Truy cập /admin/settings/payments<br>2. Bật Toggle VNPay<br>3. Kiểm tra Form | Hiển thị Form "Thông tin cổng VNPay" với: label "Merchant ID *", input type text, label "Secret *", input type password, label "Callback URL *", input type text | | Pass | 11/15/2015 | |
| **GUI-CDTT-10** | Kiểm tra nút Lưu cấu hình | 1. Truy cập /admin/settings/payments<br>2. Kiểm tra nút | Hiển thị nút "Lưu cấu hình" type submit | | Pass | 11/15/2015 | |

---

### Check FUNC: Cài đặt thanh toán

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CDTT-01** | Mở trang cài đặt thanh toán | 1. Truy cập /admin/settings/payments | Hiển thị trang với tiêu đề, mô tả, các Toggle phương thức thanh toán (COD, Banking, VNPay, MoMo, ZaloPay, Viettel Money), Form thông tin cổng (khi bật các phương thức cần cấu hình), nút Lưu cấu hình | | Pass | 11/15/2015 | |
| **FUNC-CDTT-02** | Bật/Tắt phương thức thanh toán COD | 1. Truy cập /admin/settings/payments<br>2. Bật/Tắt Toggle COD<br>3. Click "Lưu cấu hình" | Hiển thị thông báo "Lưu cấu hình thành công", phương thức COD được bật/tắt, cấu hình được lưu | | Untested | 11/15/2015 | |
| **FUNC-CDTT-03** | Bật phương thức VNPay thành công | 1. Truy cập /admin/settings/payments<br>2. Bật Toggle VNPay<br>3. Nhập Merchant ID<br>4. Nhập Secret<br>5. Nhập Callback URL<br>6. Click "Lưu cấu hình" | Hiển thị thông báo "Lưu cấu hình thành công", phương thức VNPay được bật, cấu hình cổng được lưu, phương thức hoạt động | | Untested | 11/15/2015 | |
| **FUNC-CDTT-04** | Bật VNPay - Thiếu Merchant ID | 1. Truy cập /admin/settings/payments<br>2. Bật Toggle VNPay<br>3. Để trống Merchant ID<br>4. Nhập Secret và Callback URL<br>5. Click "Lưu cấu hình" | Hiển thị thông báo lỗi "Merchant ID không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-CDTT-05** | Bật VNPay - Thiếu Secret | 1. Truy cập /admin/settings/payments<br>2. Bật Toggle VNPay<br>3. Nhập Merchant ID<br>4. Để trống Secret<br>5. Nhập Callback URL<br>6. Click "Lưu cấu hình" | Hiển thị thông báo lỗi "Secret không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-CDTT-06** | Bật VNPay - Thiếu Callback URL | 1. Truy cập /admin/settings/payments<br>2. Bật Toggle VNPay<br>3. Nhập Merchant ID và Secret<br>4. Để trống Callback URL<br>5. Click "Lưu cấu hình" | Hiển thị thông báo lỗi "Callback URL không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-CDTT-07** | Bật VNPay - Callback URL không hợp lệ | 1. Truy cập /admin/settings/payments<br>2. Bật Toggle VNPay<br>3. Nhập Callback URL không đúng định dạng<br>4. Click "Lưu cấu hình" | Hiển thị thông báo lỗi "Callback URL không hợp lệ", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-CDTT-08** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/settings/payments<br>2. Điều chỉnh cấu hình<br>3. Tắt kết nối mạng<br>4. Click "Lưu cấu hình" | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", form không được gửi | | Untested | 11/15/2015 | |
| **FUNC-CDTT-09** | Xử lý khi server lỗi | 1. Truy cập /admin/settings/payments<br>2. Điều chỉnh cấu hình<br>3. Server trả về lỗi 500<br>4. Click "Lưu cấu hình" | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau", form không được gửi | | Untested | 11/15/2015 | |

---

### Function: Cài đặt thông tin shop

#### Check GUI: Cài đặt thông tin shop

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CDTTS-01** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/settings/shop<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Thông tin shop & chính sách giao hàng" với kích thước text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-CDTTS-02** | Kiểm tra mô tả chức năng | 1. Truy cập /admin/settings/shop<br>2. Kiểm tra mô tả | Hiển thị mô tả "Cập nhật liên hệ & chính sách giao hàng" màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-CDTTS-03** | Kiểm tra Form Thông tin shop | 1. Truy cập /admin/settings/shop<br>2. Kiểm tra Form | Hiển thị Form "Thông tin shop" với: label "Tên shop *", input type text, label "Địa chỉ *", Textarea, label "SĐT *", input type tel, label "Email *", input type email, label "Giờ làm việc", input type text | | Pass | 11/15/2015 | |
| **GUI-CDTTS-04** | Kiểm tra Form Chính sách giao hàng | 1. Truy cập /admin/settings/shop<br>2. Kiểm tra Form | Hiển thị Form "Chính sách giao hàng" với: label "Miễn phí từ (VNĐ)", input type number, label "Phí tiêu chuẩn (VNĐ)", input type number, label "Phí nhanh (VNĐ)", input type number | | Pass | 11/15/2015 | |
| **GUI-CDTTS-05** | Kiểm tra nút Lưu | 1. Truy cập /admin/settings/shop<br>2. Kiểm tra nút | Hiển thị nút "Lưu" type submit | | Pass | 11/15/2015 | |
| **GUI-CDTTS-06** | Kiểm tra nút Hủy | 1. Truy cập /admin/settings/shop<br>2. Kiểm tra nút | Hiển thị nút "Hủy" variant outline | | Pass | 11/15/2015 | |

---

### Check FUNC: Cài đặt thông tin shop

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CDTTS-01** | Mở trang cài đặt thông tin shop | 1. Truy cập /admin/settings/shop | Hiển thị trang với tiêu đề, mô tả, Form Thông tin shop (có giá trị mặc định), Form Chính sách giao hàng (có giá trị mặc định), nút Lưu, nút Hủy | | Pass | 11/15/2015 | |
| **FUNC-CDTTS-02** | Cập nhật thông tin shop thành công | 1. Truy cập /admin/settings/shop<br>2. Sửa thông tin shop (Tên, Địa chỉ, SĐT, Email, Giờ làm việc)<br>3. Sửa chính sách giao hàng<br>4. Click "Lưu" | Hiển thị thông báo "Cập nhật thông tin shop thành công", dữ liệu được lưu và hiển thị chính xác | | Untested | 11/15/2015 | |
| **FUNC-CDTTS-03** | Cập nhật - Thiếu Tên shop | 1. Truy cập /admin/settings/shop<br>2. Xóa tên shop<br>3. Click "Lưu" | Hiển thị thông báo lỗi "Tên shop không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-CDTTS-04** | Cập nhật - Thiếu Địa chỉ | 1. Truy cập /admin/settings/shop<br>2. Xóa địa chỉ<br>3. Click "Lưu" | Hiển thị thông báo lỗi "Địa chỉ không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-CDTTS-05** | Cập nhật - Thiếu SĐT | 1. Truy cập /admin/settings/shop<br>2. Xóa SĐT<br>3. Click "Lưu" | Hiển thị thông báo lỗi "SĐT không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-CDTTS-06** | Cập nhật - Thiếu Email | 1. Truy cập /admin/settings/shop<br>2. Xóa email<br>3. Click "Lưu" | Hiển thị thông báo lỗi "Email không được để trống", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-CDTTS-07** | Cập nhật - Email không hợp lệ | 1. Truy cập /admin/settings/shop<br>2. Nhập email không đúng định dạng<br>3. Click "Lưu" | Hiển thị thông báo lỗi "Email không hợp lệ", form không được gửi | | Pass | 11/15/2015 | |
| **FUNC-CDTTS-08** | Click nút Hủy | 1. Truy cập /admin/settings/shop<br>2. Sửa thông tin<br>3. Click "Hủy" | Form được reset về giá trị ban đầu, không lưu thay đổi | | Pass | 11/15/2015 | |
| **FUNC-CDTTS-09** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/settings/shop<br>2. Sửa thông tin<br>3. Tắt kết nối mạng<br>4. Click "Lưu" | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", form không được gửi | | Untested | 11/15/2015 | |
| **FUNC-CDTTS-10** | Xử lý khi server lỗi | 1. Truy cập /admin/settings/shop<br>2. Sửa thông tin<br>3. Server trả về lỗi 500<br>4. Click "Lưu" | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau", form không được gửi | | Untested | 11/15/2015 | |

---

### Function: Cài đặt chung

#### Check GUI: Cài đặt chung

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CDCH-01** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/settings<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Cài đặt hệ thống" với kích thước text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-CDCH-02** | Kiểm tra mô tả chức năng | 1. Truy cập /admin/settings<br>2. Kiểm tra mô tả | Hiển thị mô tả "Cấu hình các thiết lập hệ thống" màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-CDCH-03** | Kiểm tra Tabs | 1. Truy cập /admin/settings<br>2. Kiểm tra Tabs | Hiển thị Tabs với các tab: Chính sách giảm giá sản phẩm, Chính sách giảm giá toàn bộ, Cài đặt thanh toán, Thông tin shop, Cài đặt chung | | Pass | 11/15/2015 | |
| **GUI-CDCH-04** | Kiểm tra Tab Chính sách giảm giá sản phẩm | 1. Truy cập /admin/settings<br>2. Click tab "Chính sách giảm giá sản phẩm" | Hiển thị nội dung tương tự trang /admin/settings/product-discounts | | Pass | 11/15/2015 | |
| **GUI-CDCH-05** | Kiểm tra Tab Chính sách giảm giá toàn bộ | 1. Truy cập /admin/settings<br>2. Click tab "Chính sách giảm giá toàn bộ" | Hiển thị nội dung tương tự trang /admin/settings/global-discounts | | Pass | 11/15/2015 | |
| **GUI-CDCH-06** | Kiểm tra Tab Cài đặt thanh toán | 1. Truy cập /admin/settings<br>2. Click tab "Cài đặt thanh toán" | Hiển thị nội dung tương tự trang /admin/settings/payments | | Pass | 11/15/2015 | |
| **GUI-CDCH-07** | Kiểm tra Tab Thông tin shop | 1. Truy cập /admin/settings<br>2. Click tab "Thông tin shop" | Hiển thị nội dung tương tự trang /admin/settings/shop | | Pass | 11/15/2015 | |
| **GUI-CDCH-08** | Kiểm tra Tab Cài đặt chung | 1. Truy cập /admin/settings<br>2. Click tab "Cài đặt chung" | Hiển thị Form với các cài đặt chung: Ngôn ngữ, Múi giờ, Định dạng ngày, Định dạng tiền tệ, v.v. | | Pass | 11/15/2015 | |

---

### Check FUNC: Cài đặt chung

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CDCH-01** | Mở trang cài đặt chung | 1. Truy cập /admin/settings | Hiển thị trang với tiêu đề, mô tả, Tabs với các tab cài đặt, tab mặc định được chọn | | Pass | 11/15/2015 | |
| **FUNC-CDCH-02** | Chuyển đổi giữa các Tab | 1. Truy cập /admin/settings<br>2. Click các tab khác nhau | Nội dung tab được thay đổi, tab được chọn được highlight | | Pass | 11/15/2015 | |
| **FUNC-CDCH-03** | Cập nhật cài đặt chung thành công | 1. Truy cập /admin/settings<br>2. Click tab "Cài đặt chung"<br>3. Thay đổi các cài đặt (Ngôn ngữ, Múi giờ, v.v.)<br>4. Click "Lưu" | Hiển thị thông báo "Cập nhật cài đặt thành công", cài đặt được lưu và áp dụng | | Untested | 11/15/2015 | |
| **FUNC-CDCH-04** | Xử lý khi mất kết nối mạng | 1. Truy cập /admin/settings<br>2. Thay đổi cài đặt<br>3. Tắt kết nối mạng<br>4. Click "Lưu" | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại", form không được gửi | | Untested | 11/15/2015 | |
| **FUNC-CDCH-05** | Xử lý khi server lỗi | 1. Truy cập /admin/settings<br>2. Thay đổi cài đặt<br>3. Server trả về lỗi 500<br>4. Click "Lưu" | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau", form không được gửi | | Untested | 11/15/2015 | |

---

**Người tạo:** Testing Team  
**Ngày cập nhật:** 11/15/2015  
**Phiên bản:** 1.0

