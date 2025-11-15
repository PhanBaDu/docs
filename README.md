# Test Case Template - Chức năng khuyến mãi (User)

## Module Code
**Model Management Store: Chức năng khuyến mãi User**

## Test Requirement
1. Hiển thị các mã giảm giá
2. Xem chi tiết mã giảm giá
3. Áp dụng mã giảm giá
4. Xem xếp hạng người dùng
5. Xem thống kê chi tiêu
6. Mã giảm cho riêng từng sản phẩm

---

## Test Summary

### Người thực hiện Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 126 |
| **Fail** | 0 |
| **Untested** | 34 |
| **N/A** | 0 |
| **Number of Test cases** | 160 |

---

## Test Cases

### Function: Hiển thị các mã giảm giá

#### Check GUI: Hiển thị các mã giảm giá

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-HTMMGG-01** | Kiểm tra tiêu đề khuyến mãi | 1. Truy cập /user/cart<br>2. Kiểm tra tiêu đề | Hiển thị text "Mã giảm giá:" với icon Gift hoặc Percent | | Pass | 11/15/2015 | |
| **GUI-HTMMGG-02** | Kiểm tra card Mã giảm giá | 1. Truy cập /user/cart<br>2. Kiểm tra card | Hiển thị card với icon Gift, tiêu đề "Mã giảm giá" | | Pass | 11/15/2015 | |
| **GUI-HTMMGG-03** | Kiểm tra danh sách mã giảm giá | 1. Truy cập /user/cart<br>2. Kiểm tra danh sách | Hiển thị danh sách các mã giảm giá có sẵn với thông tin: mã code, loại giảm giá, mức giảm giá, điều kiện, mô tả | | Pass | 11/15/2015 | |
| **GUI-HTMMGG-04** | Kiểm tra mã giảm giá | 1. Truy cập /user/cart<br>2. Kiểm tra mã | Hiển thị mã code (VD: WELCOME10, SAVE50K) với font medium | | Pass | 11/15/2015 | |
| **GUI-HTMMGG-05** | Kiểm tra badge loại giảm giá | 1. Truy cập /user/cart<br>2. Kiểm tra badge | Hiển thị badge với text "Phần trăm" hoặc "Cố định" tùy theo loại mã | | Pass | 11/15/2015 | |
| **GUI-HTMMGG-06** | Kiểm tra mức giảm giá | 1. Truy cập /user/cart<br>2. Kiểm tra mức giảm | Hiển thị mức giảm giá: "10%" hoặc "50.000 VNĐ" tùy theo loại | | Pass | 11/15/2015 | |
| **GUI-HTMMGG-07** | Kiểm tra điều kiện áp dụng | 1. Truy cập /user/cart<br>2. Kiểm tra điều kiện | Hiển thị "Đơn hàng tối thiểu: [Số tiền] VNĐ" | | Pass | 11/15/2015 | |
| **GUI-HTMMGG-08** | Kiểm tra mô tả mã giảm giá | 1. Truy cập /user/cart<br>2. Kiểm tra mô tả | Hiển thị mô tả chi tiết về mã giảm giá với màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-HTMMGG-09** | Kiểm tra thời gian hiệu lực | 1. Truy cập /user/cart<br>2. Kiểm tra thời gian | Hiển thị "Thời gian: [Ngày bắt đầu] - [Ngày kết thúc]" | | Pass | 11/15/2015 | |
| **GUI-HTMMGG-10** | Kiểm tra số lượng còn lại | 1. Truy cập /user/cart<br>2. Kiểm tra số lượng | Hiển thị "Số lượng còn lại: [Số]" hoặc "Hết số lượng" | | Pass | 11/15/2015 | |
| **GUI-HTMMGG-11** | Kiểm tra giới hạn lượt dùng/user | 1. Truy cập /user/cart<br>2. Kiểm tra giới hạn | Hiển thị "Giới hạn: [Số] lượt/user" hoặc "Không giới hạn" | | Pass | 11/15/2015 | |
| **GUI-HTMMGG-12** | Kiểm tra nút Áp dụng mã | 1. Truy cập /user/cart<br>2. Kiểm tra nút | Hiển thị nút "Áp dụng mã" variant outline size sm với icon Gift, có thể click | | Pass | 11/15/2015 | |
| **GUI-HTMMGG-13** | Kiểm tra gợi ý mã giảm giá | 1. Truy cập /user/cart<br>2. Kiểm tra gợi ý | Hiển thị text "Mã khả dụng: xem tất cả", grid các button mã giảm giá | | Pass | 11/15/2015 | |

---

### Check FUNC: Hiển thị các mã giảm giá

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-HTMMGG-01** | Hiển thị danh sách mã giảm giá | 1. Truy cập /user/cart<br>2. Kiểm tra danh sách | Hiển thị tất cả mã giảm giá có sẵn với đầy đủ thông tin: mã code, loại, mức giảm, điều kiện, mô tả, thời gian, số lượng | | Pass | 11/15/2015 | |
| **FUNC-HTMMGG-02** | Hiển thị thông tin chi tiết mã | 1. Truy cập /user/cart<br>2. Xem một mã giảm giá<br>3. Kiểm tra thông tin | Hiển thị đầy đủ: mô tả, điều kiện áp dụng, thời gian hiệu lực, số lượng còn lại, giới hạn lượt dùng | | Pass | 11/15/2015 | |
| **FUNC-HTMMGG-03** | Cập nhật thông tin real-time | 1. Truy cập /user/cart<br>2. Mã giảm giá hết số lượng<br>3. Kiểm tra cập nhật | Thông tin mã được cập nhật real-time, hiển thị "Hết số lượng", nút "Áp dụng mã" bị disabled | | Pass | 11/15/2015 | |
| **FUNC-HTMMGG-04** | Hiển thị điều kiện áp dụng | 1. Truy cập /user/cart<br>2. Kiểm tra điều kiện | Hiển thị rõ ràng: giá trị đơn hàng tối thiểu, loại sản phẩm áp dụng, thời gian hiệu lực | | Pass | 11/15/2015 | |
| **FUNC-HTMMGG-05** | Kiểm tra trạng thái khả dụng | 1. Truy cập /user/cart<br>2. Tạm tính < điều kiện tối thiểu<br>3. Kiểm tra trạng thái | Mã giảm giá hiển thị trạng thái "Chưa đủ điều kiện" hoặc nút bị disabled | | Pass | 11/15/2015 | |
| **FUNC-HTMMGG-06** | Click vào mã gợi ý | 1. Truy cập /user/cart<br>2. Click vào button mã gợi ý<br>3. Kiểm tra kết quả | Mã được điền vào input, có thể click "Áp dụng" để áp dụng | | Pass | 11/15/2015 | |
| **FUNC-HTMMGG-07** | Hiển thị mã hết hạn | 1. Truy cập /user/cart<br>2. Mã giảm giá hết hạn<br>3. Kiểm tra hiển thị | Mã hiển thị với badge "Hết hạn", nút "Áp dụng mã" bị disabled, không thể áp dụng | | Pass | 11/15/2015 | |
| **FUNC-HTMMGG-08** | Hiển thị mã hết số lượng | 1. Truy cập /user/cart<br>2. Mã giảm giá hết số lượng<br>3. Kiểm tra hiển thị | Mã hiển thị với text "Hết số lượng", nút "Áp dụng mã" bị disabled, không thể áp dụng | | Pass | 11/15/2015 | |

---

### Function: Xem chi tiết mã giảm giá

#### Check GUI: Xem chi tiết mã giảm giá

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XCTMGG-01** | Kiểm tra tiêu đề chi tiết | 1. Truy cập /user/promotions/[id]<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Chi tiết mã giảm giá" | | Pass | 11/15/2015 | |
| **GUI-XCTMGG-02** | Kiểm tra mã giảm giá | 1. Truy cập /user/promotions/[id]<br>2. Kiểm tra mã | Hiển thị mã code với font bold text-lg | | Pass | 11/15/2015 | |
| **GUI-XCTMGG-03** | Kiểm tra badge loại giảm giá | 1. Truy cập /user/promotions/[id]<br>2. Kiểm tra badge | Hiển thị badge với text "Phần trăm" hoặc "Cố định" | | Pass | 11/15/2015 | |
| **GUI-XCTMGG-04** | Kiểm tra mức giảm giá | 1. Truy cập /user/promotions/[id]<br>2. Kiểm tra mức giảm | Hiển thị mức giảm giá chi tiết với font bold | | Pass | 11/15/2015 | |
| **GUI-XCTMGG-05** | Kiểm tra mô tả chi tiết | 1. Truy cập /user/promotions/[id]<br>2. Kiểm tra mô tả | Hiển thị mô tả đầy đủ về mã giảm giá | | Pass | 11/15/2015 | |
| **GUI-XCTMGG-06** | Kiểm tra card Điều kiện áp dụng | 1. Truy cập /user/promotions/[id]<br>2. Kiểm tra card | Hiển thị card với tiêu đề "Điều kiện áp dụng", Giá trị đơn hàng tối thiểu, Loại sản phẩm áp dụng | | Pass | 11/15/2015 | |
| **GUI-XCTMGG-07** | Kiểm tra card Thời gian hiệu lực | 1. Truy cập /user/promotions/[id]<br>2. Kiểm tra card | Hiển thị card với tiêu đề "Thời gian hiệu lực", Ngày bắt đầu, Ngày kết thúc | | Pass | 11/15/2015 | |
| **GUI-XCTMGG-08** | Kiểm tra số lượng còn lại | 1. Truy cập /user/promotions/[id]<br>2. Kiểm tra số lượng | Hiển thị "Số lượng còn lại: [Số]" | | Pass | 11/15/2015 | |
| **GUI-XCTMGG-09** | Kiểm tra giới hạn lượt dùng/user | 1. Truy cập /user/promotions/[id]<br>2. Kiểm tra giới hạn | Hiển thị "Giới hạn lượt dùng/user: [Số]" hoặc "Không giới hạn" | | Pass | 11/15/2015 | |
| **GUI-XCTMGG-10** | Kiểm tra badge trạng thái | 1. Truy cập /user/promotions/[id]<br>2. Kiểm tra badge | Hiển thị badge trạng thái: "Có hiệu lực" (màu xanh), "Hết hạn" (màu đỏ), "Hết số lượng" (màu xám) | | Pass | 11/15/2015 | |

---

### Check FUNC: Xem chi tiết mã giảm giá

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XCTMGG-01** | Mở trang chi tiết mã giảm giá | 1. Truy cập /user/promotions/[id] | Hiển thị trang với đầy đủ thông tin: mã code, loại, mức giảm, mô tả, điều kiện, thời gian, số lượng, giới hạn, trạng thái | | Pass | 11/15/2015 | |
| **FUNC-XCTMGG-02** | Hiển thị chi tiết mã giảm giá | 1. Truy cập /user/promotions/[id]<br>2. Kiểm tra thông tin | Hiển thị đầy đủ: mức giảm giá, mô tả, điều kiện áp dụng, thời gian hiệu lực, trạng thái hiện tại | | Pass | 11/15/2015 | |
| **FUNC-XCTMGG-03** | Kiểm tra trạng thái mã - Có hiệu lực | 1. Truy cập /user/promotions/[id]<br>2. Mã còn hiệu lực<br>3. Kiểm tra trạng thái | Hiển thị badge "Có hiệu lực" màu xanh, mã có thể áp dụng | | Pass | 11/15/2015 | |
| **FUNC-XCTMGG-04** | Kiểm tra trạng thái mã - Hết hạn | 1. Truy cập /user/promotions/[id]<br>2. Mã hết hạn<br>3. Kiểm tra trạng thái | Hiển thị badge "Hết hạn" màu đỏ, mã không thể áp dụng | | Pass | 11/15/2015 | |
| **FUNC-XCTMGG-05** | Kiểm tra trạng thái mã - Hết số lượng | 1. Truy cập /user/promotions/[id]<br>2. Mã hết số lượng<br>3. Kiểm tra trạng thái | Hiển thị badge "Hết số lượng" màu xám, mã không thể áp dụng | | Pass | 11/15/2015 | |
| **FUNC-XCTMGG-06** | Cập nhật trạng thái real-time | 1. Truy cập /user/promotions/[id]<br>2. Trạng thái mã thay đổi<br>3. Kiểm tra cập nhật | Trạng thái được cập nhật ngay lập tức, badge được cập nhật màu sắc và text | | Untested | 11/15/2015 | |
| **FUNC-XCTMGG-07** | Hiển thị điều kiện áp dụng | 1. Truy cập /user/promotions/[id]<br>2. Kiểm tra điều kiện | Hiển thị rõ ràng: giá trị đơn hàng tối thiểu, loại sản phẩm áp dụng, điều kiện đặc biệt khác | | Pass | 11/15/2015 | |

---

### Function: Áp dụng mã giảm giá

#### Check GUI: Áp dụng mã giảm giá

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-AMGG-01** | Kiểm tra input nhập mã | 1. Truy cập /user/cart<br>2. Kiểm tra input | Hiển thị Input với placeholder "Nhập mã giảm giá", có thể nhập text | | Pass | 11/15/2015 | |
| **GUI-AMGG-02** | Kiểm tra nút Áp dụng | 1. Truy cập /user/cart<br>2. Kiểm tra nút | Hiển thị nút "Áp dụng" với icon Percent, chiếm toàn bộ chiều rộng | | Pass | 11/15/2015 | |
| **GUI-AMGG-03** | Kiểm tra thông báo lỗi | 1. Truy cập /user/cart<br>2. Nhập mã không hợp lệ<br>3. Kiểm tra thông báo | Hiển thị Alert với thông báo lỗi màu đỏ (VD: "Mã giảm giá không hợp lệ") | | Pass | 11/15/2015 | |
| **GUI-AMGG-04** | Kiểm tra thông báo thành công | 1. Truy cập /user/cart<br>2. Áp dụng mã thành công<br>3. Kiểm tra thông báo | Hiển thị Alert với thông báo thành công màu xanh (VD: "Áp dụng mã giảm giá thành công!") | | Pass | 11/15/2015 | |
| **GUI-AMGG-05** | Kiểm tra card Mã đã áp dụng | 1. Truy cập /user/cart<br>2. Áp dụng mã thành công<br>3. Kiểm tra card | Hiển thị card với background green-50, mã giảm giá, mô tả, nút xóa | | Pass | 11/15/2015 | |
| **GUI-AMGG-06** | Kiểm tra tên mã đã áp dụng | 1. Truy cập /user/cart<br>2. Áp dụng mã thành công<br>3. Kiểm tra tên | Hiển thị tên mã giảm giá với font medium màu green-800 | | Pass | 11/15/2015 | |
| **GUI-AMGG-07** | Kiểm tra mức giảm giá đã áp dụng | 1. Truy cập /user/cart<br>2. Áp dụng mã thành công<br>3. Kiểm tra mức giảm | Hiển thị mức giảm giá được áp dụng với màu green-600 | | Pass | 11/15/2015 | |
| **GUI-AMGG-08** | Kiểm tra số tiền giảm | 1. Truy cập /user/cart<br>2. Áp dụng mã thành công<br>3. Kiểm tra số tiền | Hiển thị số tiền được giảm trong tóm tắt đơn hàng với màu xanh | | Pass | 11/15/2015 | |
| **GUI-AMGG-09** | Kiểm tra nút Xóa mã | 1. Truy cập /user/cart<br>2. Áp dụng mã thành công<br>3. Kiểm tra nút | Hiển thị nút variant ghost size sm với icon Trash2, có thể click | | Pass | 11/15/2015 | |

---

### Check FUNC: Áp dụng mã giảm giá

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-AMGG-01** | Nhập mã giảm giá | 1. Truy cập /user/cart<br>2. Nhập mã vào ô input<br>3. Kiểm tra kết quả | Mã được nhập thành công, hệ thống kiểm tra tính hợp lệ, hỗ trợ cả chữ hoa và chữ thường | | Pass | 11/15/2015 | |
| **FUNC-AMGG-02** | Áp dụng mã giảm giá thành công | 1. Truy cập /user/cart<br>2. Nhập mã hợp lệ<br>3. Click "Áp dụng"<br>4. Kiểm tra kết quả | Hiển thị thông báo "Áp dụng mã giảm giá thành công!", mã được áp dụng, tổng tiền được tính lại, số lượng mã và lượt dùng được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-AMGG-03** | Áp dụng mã không hợp lệ | 1. Truy cập /user/cart<br>2. Nhập mã không tồn tại<br>3. Click "Áp dụng"<br>4. Kiểm tra kết quả | Hiển thị thông báo lỗi "Mã giảm giá không hợp lệ", mã không được áp dụng | | Pass | 11/15/2015 | |
| **FUNC-AMGG-04** | Áp dụng mã hết hạn | 1. Truy cập /user/cart<br>2. Nhập mã hết hạn<br>3. Click "Áp dụng"<br>4. Kiểm tra kết quả | Hiển thị thông báo lỗi "Mã giảm giá đã hết hạn", mã không được áp dụng | | Pass | 11/15/2015 | |
| **FUNC-AMGG-05** | Áp dụng mã hết số lượng | 1. Truy cập /user/cart<br>2. Nhập mã hết số lượng<br>3. Click "Áp dụng"<br>4. Kiểm tra kết quả | Hiển thị thông báo lỗi "Mã giảm giá đã hết số lượng", mã không được áp dụng | | Pass | 11/15/2015 | |
| **FUNC-AMGG-06** | Áp dụng mã - Không đủ điều kiện | 1. Truy cập /user/cart<br>2. Tạm tính < điều kiện tối thiểu<br>3. Nhập mã<br>4. Click "Áp dụng"<br>5. Kiểm tra kết quả | Hiển thị thông báo lỗi "Đơn hàng tối thiểu [Số tiền] VNĐ", mã không được áp dụng | | Pass | 11/15/2015 | |
| **FUNC-AMGG-07** | Áp dụng mã - Vượt quá giới hạn lượt dùng | 1. Truy cập /user/cart<br>2. User đã dùng hết lượt cho phép<br>3. Nhập mã<br>4. Click "Áp dụng"<br>5. Kiểm tra kết quả | Hiển thị thông báo lỗi "Bạn đã sử dụng hết lượt cho phép", mã không được áp dụng | | Untested | 11/15/2015 | |
| **FUNC-AMGG-08** | Áp dụng mã phần trăm | 1. Truy cập /user/cart<br>2. Áp dụng mã phần trăm (VD: 10%)<br>3. Kiểm tra giảm giá | Số tiền giảm = tổng tiền × phần trăm, hiển thị trong tóm tắt đơn hàng | | Pass | 11/15/2015 | |
| **FUNC-AMGG-09** | Áp dụng mã cố định | 1. Truy cập /user/cart<br>2. Áp dụng mã cố định (VD: 50.000 VNĐ)<br>3. Kiểm tra giảm giá | Số tiền giảm = số tiền cố định, hiển thị trong tóm tắt đơn hàng | | Pass | 11/15/2015 | |
| **FUNC-AMGG-10** | Cập nhật tổng tiền sau khi áp dụng mã | 1. Truy cập /user/cart<br>2. Áp dụng mã giảm giá<br>3. Kiểm tra tổng tiền | Tổng tiền = Tạm tính + Phí vận chuyển - Giảm giá, được cập nhật ngay lập tức | | Pass | 11/15/2015 | |
| **FUNC-AMGG-11** | Xóa mã giảm giá | 1. Truy cập /user/cart<br>2. Áp dụng mã thành công<br>3. Click nút xóa mã<br>4. Kiểm tra kết quả | Hiển thị thông báo "Đã xóa mã giảm giá", mã bị xóa, tổng tiền được tính lại không có giảm giá | | Pass | 11/15/2015 | |
| **FUNC-AMGG-12** | Cập nhật số lượng mã sau khi áp dụng | 1. Truy cập /user/cart<br>2. Áp dụng mã thành công<br>3. Kiểm tra số lượng | Số lượng mã còn lại được giảm đi 1, hiển thị trong danh sách mã | | Untested | 11/15/2015 | |
| **FUNC-AMGG-13** | Cập nhật lượt dùng của user | 1. Truy cập /user/cart<br>2. Áp dụng mã có giới hạn lượt dùng<br>3. Kiểm tra lượt dùng | Số lượt đã dùng của user được tăng lên 1, hiển thị trong thông tin mã | | Untested | 11/15/2015 | |
| **FUNC-AMGG-14** | Áp dụng mã không phân biệt hoa thường | 1. Truy cập /user/cart<br>2. Nhập mã chữ thường (VD: "welcome10")<br>3. Click "Áp dụng"<br>4. Kiểm tra kết quả | Mã được áp dụng thành công, không phân biệt hoa thường | | Pass | 11/15/2015 | |

---

### Function: Xem xếp hạng người dùng

#### Check GUI: Xem xếp hạng người dùng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XXHND-01** | Kiểm tra tiêu đề xếp hạng | 1. Truy cập /user/account<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Thông tin thành viên" với icon Crown | | Pass | 11/15/2015 | |
| **GUI-XXHND-02** | Kiểm tra badge hạng hiện tại | 1. Truy cập /user/account<br>2. Kiểm tra badge | Hiển thị badge hạng: Bronze (màu đồng), Silver (màu bạc), Gold (màu vàng), Platinum (màu bạch kim) | | Pass | 11/15/2015 | |
| **GUI-XXHND-03** | Kiểm tra tổng chi tiêu | 1. Truy cập /user/account<br>2. Kiểm tra tổng chi tiêu | Hiển thị "Tổng chi tiêu: [Số tiền] VNĐ" | | Pass | 11/15/2015 | |
| **GUI-XXHND-04** | Kiểm tra điểm tích lũy | 1. Truy cập /user/account<br>2. Kiểm tra điểm | Hiển thị "Điểm tích lũy: [Số điểm]" | | Pass | 11/15/2015 | |
| **GUI-XXHND-05** | Kiểm tra mức giảm giá | 1. Truy cập /user/account<br>2. Kiểm tra mức giảm | Hiển thị "Mức giảm giá: [Phần trăm]%" theo hạng | | Pass | 11/15/2015 | |
| **GUI-XXHND-06** | Kiểm tra thanh tiến độ hạng tiếp theo | 1. Truy cập /user/account<br>2. Kiểm tra thanh tiến độ | Hiển thị Progress bar với phần trăm tiến độ đến hạng tiếp theo | | Pass | 11/15/2015 | |
| **GUI-XXHND-07** | Kiểm tra điều kiện hạng tiếp theo | 1. Truy cập /user/account<br>2. Kiểm tra điều kiện | Hiển thị "Cần chi thêm [Số tiền] VNĐ để lên hạng [Hạng tiếp theo]" | | Pass | 11/15/2015 | |
| **GUI-XXHND-08** | Kiểm tra nút Xem lịch sử giao dịch | 1. Truy cập /user/account<br>2. Kiểm tra nút | Hiển thị nút "Xem lịch sử giao dịch" variant outline | | Pass | 11/15/2015 | |
| **GUI-XXHND-09** | Kiểm tra card Quyền lợi hạng | 1. Truy cập /user/account<br>2. Kiểm tra card | Hiển thị card với tiêu đề "Quyền lợi hạng [Hạng]", danh sách quyền lợi | | Pass | 11/15/2015 | |

---

### Check FUNC: Xem xếp hạng người dùng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XXHND-01** | Hiển thị thông tin hạng | 1. Truy cập /user/account<br>2. Kiểm tra thông tin | Hiển thị đầy đủ: tên hạng, tổng chi tiêu, điểm tích lũy, mức giảm giá, tiến độ đến hạng tiếp theo | | Pass | 11/15/2015 | |
| **FUNC-XXHND-02** | Tính toán xếp hạng | 1. Truy cập /user/account<br>2. Có giao dịch mới<br>3. Kiểm tra xếp hạng | Xếp hạng được tính toán dựa trên tổng giá trị chi tiêu, cập nhật real-time, mỗi sản phẩm mua được quy đổi thành điểm tích lũy | | Untested | 11/15/2015 | |
| **FUNC-XXHND-03** | Hiển thị hạng Bronze | 1. Truy cập /user/account<br>2. User có hạng Bronze<br>3. Kiểm tra hạng | Hiển thị badge "Bronze" màu đồng, mức giảm giá tương ứng | | Pass | 11/15/2015 | |
| **FUNC-XXHND-04** | Hiển thị hạng Silver | 1. Truy cập /user/account<br>2. User có hạng Silver<br>3. Kiểm tra hạng | Hiển thị badge "Silver" màu bạc, mức giảm giá tương ứng | | Pass | 11/15/2015 | |
| **FUNC-XXHND-05** | Hiển thị hạng Gold | 1. Truy cập /user/account<br>2. User có hạng Gold<br>3. Kiểm tra hạng | Hiển thị badge "Gold" màu vàng, mức giảm giá tương ứng | | Pass | 11/15/2015 | |
| **FUNC-XXHND-06** | Hiển thị hạng Platinum | 1. Truy cập /user/account<br>2. User có hạng Platinum<br>3. Kiểm tra hạng | Hiển thị badge "Platinum" màu bạch kim, mức giảm giá tương ứng | | Pass | 11/15/2015 | |
| **FUNC-XXHND-07** | Cập nhật tiến độ hạng | 1. Truy cập /user/account<br>2. Có giao dịch mới<br>3. Kiểm tra tiến độ | Tiến độ được cập nhật dựa trên chi tiêu hiện tại, hiển thị số tiền cần chi thêm để lên hạng tiếp theo | | Untested | 11/15/2015 | |
| **FUNC-XXHND-08** | Lên hạng tự động | 1. Truy cập /user/account<br>2. Chi tiêu đủ điều kiện lên hạng<br>3. Kiểm tra hạng | Hạng được tự động nâng lên, badge được cập nhật, mức giảm giá được cập nhật, hiển thị thông báo chúc mừng | | Untested | 11/15/2015 | |
| **FUNC-XXHND-09** | Click nút Xem lịch sử giao dịch | 1. Truy cập /user/account<br>2. Click nút "Xem lịch sử giao dịch" | Chuyển đến trang /user/account/orders | | Pass | 11/15/2015 | |
| **FUNC-XXHND-10** | Hiển thị quyền lợi hạng | 1. Truy cập /user/account<br>2. Kiểm tra quyền lợi | Hiển thị danh sách quyền lợi của hạng hiện tại: mức giảm giá, ưu đãi đặc biệt, dịch vụ miễn phí | | Pass | 11/15/2015 | |

---

### Function: Xem thống kê chi tiêu

#### Check GUI: Xem thống kê chi tiêu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XTKCT-01** | Kiểm tra tiêu đề thống kê | 1. Truy cập /user/account/statistics<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Thống kê chi tiêu" | | Pass | 11/15/2015 | |
| **GUI-XTKCT-02** | Kiểm tra card Thống kê theo thời gian | 1. Truy cập /user/account/statistics<br>2. Kiểm tra card | Hiển thị card với Chi tiêu tháng này, Chi tiêu năm này | | Pass | 11/15/2015 | |
| **GUI-XTKCT-03** | Kiểm tra Chi tiêu tháng này | 1. Truy cập /user/account/statistics<br>2. Kiểm tra chi tiêu | Hiển thị "Chi tiêu tháng này: [Số tiền] VNĐ" | | Pass | 11/15/2015 | |
| **GUI-XTKCT-04** | Kiểm tra Chi tiêu năm này | 1. Truy cập /user/account/statistics<br>2. Kiểm tra chi tiêu | Hiển thị "Chi tiêu năm này: [Số tiền] VNĐ" | | Pass | 11/15/2015 | |
| **GUI-XTKCT-05** | Kiểm tra Số đơn hàng | 1. Truy cập /user/account/statistics<br>2. Kiểm tra số đơn | Hiển thị "Tổng số đơn hàng: [Số]" | | Pass | 11/15/2015 | |
| **GUI-XTKCT-06** | Kiểm tra Đơn hàng thành công | 1. Truy cập /user/account/statistics<br>2. Kiểm tra đơn thành công | Hiển thị "Đơn hàng thành công: [Số]" | | Pass | 11/15/2015 | |
| **GUI-XTKCT-07** | Kiểm tra Đơn hàng đang xử lý | 1. Truy cập /user/account/statistics<br>2. Kiểm tra đơn xử lý | Hiển thị "Đơn hàng đang xử lý: [Số]" | | Pass | 11/15/2015 | |
| **GUI-XTKCT-08** | Kiểm tra Biểu đồ chi tiêu | 1. Truy cập /user/account/statistics<br>2. Kiểm tra biểu đồ | Hiển thị Chart với biểu đồ chi tiêu theo thời gian (tháng/năm) | | Pass | 11/15/2015 | |
| **GUI-XTKCT-09** | Kiểm tra card Top sản phẩm | 1. Truy cập /user/account/statistics<br>2. Kiểm tra card | Hiển thị card với tiêu đề "Top sản phẩm", danh sách sản phẩm mua nhiều nhất | | Pass | 11/15/2015 | |
| **GUI-XTKCT-10** | Kiểm tra Table Lịch sử giao dịch | 1. Truy cập /user/account/statistics<br>2. Kiểm tra table | Hiển thị Table với các cột: Mã đơn hàng, Số tiền, Thời gian, Trạng thái | | Pass | 11/15/2015 | |

---

### Check FUNC: Xem thống kê chi tiêu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XTKCT-01** | Hiển thị thống kê chi tiêu | 1. Truy cập /user/account/statistics<br>2. Kiểm tra thống kê | Hiển thị đầy đủ: chi tiêu theo tháng/năm, số đơn hàng, các chỉ số khác, được tính toán chính xác | | Pass | 11/15/2015 | |
| **FUNC-XTKCT-02** | Tính toán chi tiêu tháng này | 1. Truy cập /user/account/statistics<br>2. Kiểm tra chi tiêu | Chi tiêu tháng này = tổng giá trị các đơn hàng trong tháng hiện tại, được tính toán chính xác | | Pass | 11/15/2015 | |
| **FUNC-XTKCT-03** | Tính toán chi tiêu năm này | 1. Truy cập /user/account/statistics<br>2. Kiểm tra chi tiêu | Chi tiêu năm này = tổng giá trị các đơn hàng trong năm hiện tại, được tính toán chính xác | | Pass | 11/15/2015 | |
| **FUNC-XTKCT-04** | Hiển thị số đơn hàng | 1. Truy cập /user/account/statistics<br>2. Kiểm tra số đơn | Hiển thị tổng số đơn hàng đã đặt, được tính toán chính xác | | Pass | 11/15/2015 | |
| **FUNC-XTKCT-05** | Hiển thị đơn hàng thành công | 1. Truy cập /user/account/statistics<br>2. Kiểm tra đơn thành công | Hiển thị số đơn hàng đã hoàn thành thành công, được tính toán chính xác | | Pass | 11/15/2015 | |
| **FUNC-XTKCT-06** | Hiển thị đơn hàng đang xử lý | 1. Truy cập /user/account/statistics<br>2. Kiểm tra đơn xử lý | Hiển thị số đơn hàng đang trong quá trình xử lý, được tính toán chính xác | | Pass | 11/15/2015 | |
| **FUNC-XTKCT-07** | Hiển thị biểu đồ chi tiêu | 1. Truy cập /user/account/statistics<br>2. Kiểm tra biểu đồ | Hiển thị biểu đồ chi tiêu theo thời gian, cập nhật real-time, hiển thị xu hướng tăng/giảm chi tiêu | | Untested | 11/15/2015 | |
| **FUNC-XTKCT-08** | Hiển thị top sản phẩm | 1. Truy cập /user/account/statistics<br>2. Kiểm tra top sản phẩm | Hiển thị danh sách sản phẩm được mua nhiều nhất, sắp xếp theo số lượng mua | | Pass | 11/15/2015 | |
| **FUNC-XTKCT-09** | Hiển thị lịch sử giao dịch | 1. Truy cập /user/account/statistics<br>2. Kiểm tra lịch sử | Hiển thị lịch sử giao dịch chi tiết: mã đơn hàng, số tiền, thời gian, trạng thái, sắp xếp theo thời gian | | Pass | 11/15/2015 | |
| **FUNC-XTKCT-10** | Tìm kiếm lịch sử giao dịch | 1. Truy cập /user/account/statistics<br>2. Nhập từ khóa tìm kiếm<br>3. Kiểm tra kết quả | Lịch sử được lọc theo từ khóa, hiển thị kết quả phù hợp | | Pass | 11/15/2015 | |
| **FUNC-XTKCT-11** | Lọc lịch sử giao dịch | 1. Truy cập /user/account/statistics<br>2. Chọn bộ lọc (thời gian, trạng thái)<br>3. Kiểm tra kết quả | Lịch sử được lọc theo tiêu chí đã chọn, hiển thị kết quả phù hợp | | Pass | 11/15/2015 | |

---

### Function: Mã giảm cho riêng từng sản phẩm

#### Check GUI: Mã giảm cho riêng từng sản phẩm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-MGGTSP-01** | Kiểm tra tiêu đề mã sản phẩm | 1. Truy cập /user/products/[id]<br>2. Sản phẩm có mã giảm<br>3. Kiểm tra tiêu đề | Hiển thị tiêu đề "Khuyến mãi đặc biệt" | | Pass | 11/15/2015 | |
| **GUI-MGGTSP-02** | Kiểm tra badge khuyến mãi | 1. Truy cập /user/products/[id]<br>2. Sản phẩm có mã giảm<br>3. Kiểm tra badge | Hiển thị badge "Giảm giá" variant destructive với phần trăm giảm (VD: -26%) | | Pass | 11/15/2015 | |
| **GUI-MGGTSP-03** | Kiểm tra mã giảm giá sản phẩm | 1. Truy cập /user/products/[id]<br>2. Sản phẩm có mã giảm<br>3. Kiểm tra mã | Hiển thị mã code riêng cho sản phẩm (VD: "PRODUCT10") | | Pass | 11/15/2015 | |
| **GUI-MGGTSP-04** | Kiểm tra mức giảm giá | 1. Truy cập /user/products/[id]<br>2. Sản phẩm có mã giảm<br>3. Kiểm tra mức giảm | Hiển thị mức giảm giá: "10%" hoặc "50.000 VNĐ" | | Pass | 11/15/2015 | |
| **GUI-MGGTSP-05** | Kiểm tra giá gốc | 1. Truy cập /user/products/[id]<br>2. Sản phẩm có mã giảm<br>3. Kiểm tra giá gốc | Hiển thị giá gốc với line-through, màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-MGGTSP-06** | Kiểm tra giá sau giảm | 1. Truy cập /user/products/[id]<br>2. Sản phẩm có mã giảm<br>3. Kiểm tra giá sau giảm | Hiển thị giá sau giảm với font bold màu primary | | Pass | 11/15/2015 | |
| **GUI-MGGTSP-07** | Kiểm tra thời gian áp dụng | 1. Truy cập /user/products/[id]<br>2. Sản phẩm có mã giảm<br>3. Kiểm tra thời gian | Hiển thị "Thời gian: [Ngày bắt đầu] - [Ngày kết thúc]" | | Pass | 11/15/2015 | |
| **GUI-MGGTSP-08** | Kiểm tra điều kiện áp dụng | 1. Truy cập /user/products/[id]<br>2. Sản phẩm có mã giảm<br>3. Kiểm tra điều kiện | Hiển thị điều kiện để sử dụng mã (nếu có) | | Pass | 11/15/2015 | |
| **GUI-MGGTSP-09** | Kiểm tra nút Áp dụng mã | 1. Truy cập /user/products/[id]<br>2. Sản phẩm có mã giảm<br>3. Kiểm tra nút | Hiển thị nút "Áp dụng mã" variant outline | | Pass | 11/15/2015 | |
| **GUI-MGGTSP-10** | Kiểm tra thông báo đặc biệt | 1. Truy cập /user/products/[id]<br>2. Sản phẩm có mã giảm<br>3. Kiểm tra thông báo | Hiển thị Alert với thông báo về mã đặc biệt (nếu có) | | Pass | 11/15/2015 | |

---

### Check FUNC: Mã giảm cho riêng từng sản phẩm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-MGGTSP-01** | Hiển thị mã sản phẩm | 1. Truy cập /user/products/[id]<br>2. Sản phẩm có mã giảm<br>3. Kiểm tra hiển thị | Hiển thị nổi bật mã giảm giá dành riêng cho sản phẩm với thông tin: mức giảm giá, thời gian áp dụng, điều kiện sử dụng | | Pass | 11/15/2015 | |
| **FUNC-MGGTSP-02** | Tính toán giá sau giảm | 1. Truy cập /user/products/[id]<br>2. Sản phẩm có mã giảm<br>3. Kiểm tra giá | Giá sau giảm được tính toán chính xác, hiển thị rõ ràng giá gốc và giá sau giảm để so sánh | | Pass | 11/15/2015 | |
| **FUNC-MGGTSP-03** | Tính giá sau giảm phần trăm | 1. Truy cập /user/products/[id]<br>2. Sản phẩm có mã giảm 10%<br>3. Kiểm tra giá | Giá sau giảm = Giá gốc × (1 - 10%), hiển thị chính xác | | Pass | 11/15/2015 | |
| **FUNC-MGGTSP-04** | Tính giá sau giảm cố định | 1. Truy cập /user/products/[id]<br>2. Sản phẩm có mã giảm 50.000 VNĐ<br>3. Kiểm tra giá | Giá sau giảm = Giá gốc - 50.000 VNĐ, hiển thị chính xác | | Pass | 11/15/2015 | |
| **FUNC-MGGTSP-05** | Thông báo mã đặc biệt | 1. Truy cập /user/products/[id]<br>2. Sản phẩm có mã giảm đặc biệt<br>3. Kiểm tra thông báo | Hiển thị thông báo về mã đặc biệt, có thể gửi qua email, SMS, push notification | | Untested | 11/15/2015 | |
| **FUNC-MGGTSP-06** | Áp dụng mã sản phẩm | 1. Truy cập /user/products/[id]<br>2. Click nút "Áp dụng mã"<br>3. Kiểm tra kết quả | Mã được áp dụng, giá được cập nhật, có thể thêm vào giỏ hàng với giá đã giảm | | Untested | 11/15/2015 | |
| **FUNC-MGGTSP-07** | Hiển thị mã hết hạn | 1. Truy cập /user/products/[id]<br>2. Mã giảm hết hạn<br>3. Kiểm tra hiển thị | Mã không hiển thị hoặc hiển thị với badge "Hết hạn", không thể áp dụng | | Pass | 11/15/2015 | |
| **FUNC-MGGTSP-08** | Hiển thị trong danh sách sản phẩm | 1. Truy cập /user/products<br>2. Sản phẩm có mã giảm<br>3. Kiểm tra hiển thị | Hiển thị badge giảm giá trên card sản phẩm, giá gốc và giá sau giảm | | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn Markdown để dễ dàng quản lý và cập nhật test cases.*

