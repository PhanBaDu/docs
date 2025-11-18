# Test Case Template - Vận chuyển (User)

## Module Code
**USER-007: Vận chuyển (User)**

## Test Requirement
1. Hiển thị các đơn vị vận chuyển
2. Chọn nhà vận chuyển

---

## Test Summary

### Người thực hiện Test: Tester

| Status | Count |
|--------|-------|
| **Pass** | 38 |
| **Fail** | 0 |
| **Untested** | 0 |
| **N/A** | 0 |
| **Number of Test cases** | 38 |

---

## Test Cases

### Function: Hiển thị các đơn vị vận chuyển

#### Check GUI: Hiển thị đơn vị vận chuyển

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-HT-01** | Kiểm tra Card vận chuyển | 1. Truy cập /user/cart<br>2. Kiểm tra Card | Hiển thị Card với CardHeader có CardTitle "Vận chuyển" (text-lg, icon Truck h-5 w-5), CardContent space-y-3 | | Pass | 11/15/2015 | |
| **GUI-HT-02** | Kiểm tra radio Giao hàng tiêu chuẩn | 1. Truy cập /user/cart<br>2. Kiểm tra radio | Hiển thị div flex items-center gap-2 với input type="radio" id="standard" name="shipping" value="standard" checked={shippingMethod === "standard"}, Label htmlFor="standard" className="flex-1" có div flex justify-between với span "Giao hàng tiêu chuẩn" và span font-medium hiển thị "Miễn phí" nếu subtotal >= 500000, "30.000 VNĐ" nếu không, p text-sm text-muted-foreground "3-5 ngày làm việc" | | Pass | 11/15/2015 | |
| **GUI-HT-03** | Kiểm tra radio Giao hàng nhanh | 1. Truy cập /user/cart<br>2. Kiểm tra radio | Hiển thị div flex items-center gap-2 với input type="radio" id="express" name="shipping" value="express" checked={shippingMethod === "express"}, Label htmlFor="express" className="flex-1" có div flex justify-between với span "Giao hàng nhanh" và span font-medium "50.000 VNĐ", p text-sm text-muted-foreground "1-2 ngày làm việc" | | Pass | 11/15/2015 | |
| **GUI-HT-04** | Kiểm tra Card đơn vị vận chuyển | 1. Truy cập /user/cart<br>2. Kiểm tra Card | Hiển thị Card với CardHeader có CardTitle "Đơn vị vận chuyển" (text-lg, icon Truck h-5 w-5), CardContent space-y-4 | | Pass | 11/15/2015 | |
| **GUI-HT-05** | Kiểm tra danh sách đơn vị vận chuyển | 1. Truy cập /user/cart<br>2. Kiểm tra danh sách | Hiển thị div space-y-3 với các div flex items-start gap-2 cho mỗi carrier, có input type="radio" id={`carrier-${c.id}`} name="carrier" value={c.id} checked={selectedCarrier === c.id}, Label htmlFor={`carrier-${c.id}`} className="flex-1" | | Pass | 11/15/2015 | |
| **GUI-HT-06** | Kiểm tra thông tin đơn vị GHTK | 1. Truy cập /user/cart<br>2. Kiểm tra đơn vị GHTK | Hiển thị Label với div flex justify-between có span "Giao hàng tiết kiệm" và span font-medium hiển thị "Miễn phí (tiêu chuẩn)" nếu subtotal >= 500000, "30.000 VNĐ" nếu không, p text-sm text-muted-foreground "Thời gian giao: 3-5 ngày • Tiêu chuẩn, tiết kiệm chi phí" | | Pass | 11/15/2015 | |
| **GUI-HT-07** | Kiểm tra thông tin đơn vị GHN | 1. Truy cập /user/cart<br>2. Kiểm tra đơn vị GHN | Hiển thị Label với div flex justify-between có span "Giao hàng nhanh (GHN)" và span font-medium "50.000 VNĐ", p text-sm text-muted-foreground "Thời gian giao: 1-2 ngày • Nhanh, ổn định nội thành" | | Pass | 11/15/2015 | |
| **GUI-HT-08** | Kiểm tra thông tin đơn vị JT | 1. Truy cập /user/cart<br>2. Kiểm tra đơn vị JT | Hiển thị Label với div flex justify-between có span "J&T Express" và span font-medium hiển thị "Miễn phí (tiêu chuẩn)" nếu subtotal >= 500000, "30.000 VNĐ" nếu không, p text-sm text-muted-foreground "Thời gian giao: 2-4 ngày • Phủ rộng toàn quốc" | | Pass | 11/15/2015 | |
| **GUI-HT-09** | Kiểm tra thông báo điều kiện miễn phí | 1. Truy cập /user/cart<br>2. Kiểm tra thông báo | Hiển thị div text-sm text-muted-foreground "Điều kiện miễn phí: đơn từ 500.000 VNĐ với phương thức tiêu chuẩn" | | Pass | 11/15/2015 | |
| **GUI-HT-10** | Kiểm tra Card tính phí vận chuyển | 1. Truy cập /user/cart<br>2. Kiểm tra Card | Hiển thị Card với CardHeader có CardTitle "Tính phí vận chuyển" (text-lg), CardContent space-y-3 text-sm | | Pass | 11/15/2015 | |
| **GUI-HT-11** | Kiểm tra Input địa chỉ giao hàng | 1. Truy cập /user/cart<br>2. Kiểm tra Input | Hiển thị div grid gap-1 với Label "Địa chỉ giao hàng", Input placeholder "Số nhà, đường, phường/xã, quận/huyện, tỉnh/thành", value=shippingAddress | | Pass | 11/15/2015 | |
| **GUI-HT-12** | Kiểm tra Input trọng lượng | 1. Truy cập /user/cart<br>2. Kiểm tra Input | Hiển thị div grid gap-1 với Label "Trọng lượng (kg)", Input value={totalWeightKg} readOnly | | Pass | 11/15/2015 | |
| **GUI-HT-13** | Kiểm tra Input khoảng cách | 1. Truy cập /user/cart<br>2. Kiểm tra Input | Hiển thị div grid gap-1 với Label "Khoảng cách (km)", Input value={distanceKm} readOnly | | Pass | 11/15/2015 | |
| **GUI-HT-14** | Kiểm tra thông tin phí cơ bản | 1. Truy cập /user/cart<br>2. Kiểm tra thông tin | Hiển thị div flex justify-between với span "Phí cơ bản", span "10.000 VNĐ" | | Pass | 11/15/2015 | |
| **GUI-HT-15** | Kiểm tra thông tin phí theo trọng lượng | 1. Truy cập /user/cart<br>2. Kiểm tra thông tin | Hiển thị div flex justify-between với span "Phí theo trọng lượng", span "8.000 VNĐ" | | Pass | 11/15/2015 | |
| **GUI-HT-16** | Kiểm tra thông tin phí theo khoảng cách | 1. Truy cập /user/cart<br>2. Kiểm tra thông tin | Hiển thị div flex justify-between với span "Phí theo khoảng cách", span "12.000 VNĐ" | | Pass | 11/15/2015 | |
| **GUI-HT-17** | Kiểm tra tổng phí vận chuyển | 1. Truy cập /user/cart<br>2. Kiểm tra tổng phí | Hiển thị div flex justify-between font-medium với span "Tổng phí vận chuyển (ước tính)", span hiển thị "Miễn phí" nếu shippingFee === 0, "{shippingFee.toLocaleString('vi-VN')} VNĐ" nếu không | | Pass | 11/15/2015 | |

#### Check FUNC: Hiển thị đơn vị vận chuyển

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-HT-01** | Mở trang giỏ hàng với phần vận chuyển | 1. Truy cập /user/cart | Hiển thị Card vận chuyển, Card đơn vị vận chuyển, Card tính phí vận chuyển, phương thức "Giao hàng tiêu chuẩn" được chọn mặc định (shippingMethod = "standard"), đơn vị "GHTK" được chọn mặc định (selectedCarrier = "GHTK") | | Pass | 11/15/2015 | |
| **FUNC-HT-02** | Hiển thị danh sách đơn vị vận chuyển | 1. Truy cập /user/cart<br>2. Kiểm tra danh sách | Hiển thị đầy đủ 3 đơn vị: GHTK (Giao hàng tiết kiệm), GHN (Giao hàng nhanh), JT (J&T Express), mỗi đơn vị có thông tin: tên, phí, thời gian giao, đặc điểm | | Pass | 11/15/2015 | |
| **FUNC-HT-03** | Tính toán phí vận chuyển - Miễn phí | 1. Truy cập /user/cart<br>2. Tạm tính >= 500.000<br>3. Chọn phương thức tiêu chuẩn<br>4. Chọn đơn vị GHTK hoặc JT<br>5. Kiểm tra | Phí vận chuyển = 0, hiển thị "Miễn phí (tiêu chuẩn)" cho GHTK và JT, tổng cộng được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-HT-04** | Tính toán phí vận chuyển - Có phí tiêu chuẩn | 1. Truy cập /user/cart<br>2. Tạm tính < 500.000<br>3. Chọn phương thức tiêu chuẩn<br>4. Chọn đơn vị GHTK hoặc JT<br>5. Kiểm tra | Phí vận chuyển = 30.000 VNĐ, hiển thị "30.000 VNĐ" cho GHTK và JT, tổng cộng được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-HT-05** | Tính toán phí vận chuyển - Giao hàng nhanh | 1. Truy cập /user/cart<br>2. Chọn phương thức giao hàng nhanh<br>3. Chọn đơn vị GHN<br>4. Kiểm tra | Phí vận chuyển = 50.000 VNĐ, hiển thị "50.000 VNĐ" cho GHN, tổng cộng được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-HT-06** | Cập nhật phí khi thay đổi phương thức | 1. Truy cập /user/cart<br>2. Chọn phương thức tiêu chuẩn<br>3. Chọn phương thức nhanh<br>4. Kiểm tra | Phí vận chuyển được tính lại (30.000đ -> 50.000đ), tổng cộng được cập nhật ngay lập tức | | Pass | 11/15/2015 | |
| **FUNC-HT-07** | Cập nhật phí khi tạm tính thay đổi | 1. Truy cập /user/cart<br>2. Tạm tính < 500.000<br>3. Thay đổi số lượng hoặc chọn sản phẩm<br>4. Tạm tính >= 500.000<br>5. Kiểm tra | Phí vận chuyển chuyển thành 0 (nếu phương thức tiêu chuẩn và đơn vị GHTK/JT), hiển thị "Miễn phí (tiêu chuẩn)", tổng cộng được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-HT-08** | Hiển thị thời gian giao hàng | 1. Truy cập /user/cart<br>2. Kiểm tra thời gian | Mỗi đơn vị hiển thị thời gian giao: GHTK "3-5 ngày", GHN "1-2 ngày", JT "2-4 ngày" | | Pass | 11/15/2015 | |
| **FUNC-HT-09** | Hiển thị đặc điểm đơn vị | 1. Truy cập /user/cart<br>2. Kiểm tra đặc điểm | Mỗi đơn vị hiển thị đặc điểm: GHTK "Tiêu chuẩn, tiết kiệm chi phí", GHN "Nhanh, ổn định nội thành", JT "Phủ rộng toàn quốc" | | Pass | 11/15/2015 | |
| **FUNC-HT-10** | Hiển thị thông tin tính phí | 1. Truy cập /user/cart<br>2. Kiểm tra Card tính phí | Hiển thị địa chỉ giao hàng (có thể nhập), trọng lượng (readOnly, value=totalWeightKg), khoảng cách (readOnly, value=distanceKm), các phí: Phí cơ bản 10.000 VNĐ, Phí theo trọng lượng 8.000 VNĐ, Phí theo khoảng cách 12.000 VNĐ, Phí dịch vụ 0 VNĐ, Tổng phí vận chuyển (ước tính) | | Pass | 11/15/2015 | |
| **FUNC-HT-11** | Nhập địa chỉ giao hàng | 1. Truy cập /user/cart<br>2. Nhập địa chỉ vào Input | shippingAddress được cập nhật theo giá trị đã nhập | | Pass | 11/15/2015 | |

### Function: Chọn nhà vận chuyển

#### Check GUI: Chọn đơn vị vận chuyển

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CH-01** | Kiểm tra radio đơn vị vận chuyển | 1. Truy cập /user/cart<br>2. Kiểm tra radio | Hiển thị input type="radio" cho mỗi đơn vị với id={`carrier-${c.id}`}, name="carrier", value={c.id}, checked={selectedCarrier === c.id} | | Pass | 11/15/2015 | |

#### Check FUNC: Chọn đơn vị vận chuyển

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CH-01** | Chọn đơn vị GHTK | 1. Truy cập /user/cart<br>2. Chọn radio GHTK | selectedCarrier = "GHTK", radio GHTK được checked, các radio khác không được checked, phí vận chuyển được tính lại (0 nếu subtotal >= 500000, 30.000đ nếu không), tổng cộng được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-CH-02** | Chọn đơn vị GHN | 1. Truy cập /user/cart<br>2. Chọn radio GHN | selectedCarrier = "GHN", radio GHN được checked, các radio khác không được checked, phí vận chuyển = 50.000 VNĐ, tổng cộng được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-CH-03** | Chọn đơn vị JT | 1. Truy cập /user/cart<br>2. Chọn radio JT | selectedCarrier = "JT", radio JT được checked, các radio khác không được checked, phí vận chuyển được tính lại (0 nếu subtotal >= 500000, 30.000đ nếu không), tổng cộng được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-CH-04** | Chỉ có một đơn vị được chọn | 1. Truy cập /user/cart<br>2. Chọn đơn vị A<br>3. Chọn đơn vị B | Chỉ đơn vị B được checked, đơn vị A không được checked, selectedCarrier được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-CH-05** | Chọn phương thức vận chuyển tiêu chuẩn | 1. Truy cập /user/cart<br>2. Chọn radio "Giao hàng tiêu chuẩn" | shippingMethod = "standard", radio được checked, phí vận chuyển được tính lại (0 nếu subtotal >= 500000 và đơn vị GHTK/JT, 30.000đ nếu không), tổng cộng được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-CH-06** | Chọn phương thức vận chuyển nhanh | 1. Truy cập /user/cart<br>2. Chọn radio "Giao hàng nhanh" | shippingMethod = "express", radio được checked, phí vận chuyển = 50.000 VNĐ, tổng cộng được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-CH-07** | Chỉ có một phương thức được chọn | 1. Truy cập /user/cart<br>2. Chọn phương thức A<br>3. Chọn phương thức B | Chỉ phương thức B được checked, phương thức A không được checked, shippingMethod được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-CH-08** | Kết hợp phương thức và đơn vị | 1. Truy cập /user/cart<br>2. Chọn phương thức tiêu chuẩn<br>3. Chọn đơn vị GHTK<br>4. Kiểm tra | Phí vận chuyển được tính dựa trên cả phương thức và đơn vị, tổng cộng được cập nhật đúng | | Pass | 11/15/2015 | |
| **FUNC-CH-09** | Thay đổi đơn vị không làm mất phương thức | 1. Truy cập /user/cart<br>2. Chọn phương thức tiêu chuẩn<br>3. Thay đổi đơn vị<br>4. Kiểm tra | Phương thức vận chuyển vẫn được giữ nguyên, chỉ đơn vị thay đổi, phí được tính lại | | Pass | 11/15/2015 | |
| **FUNC-CH-10** | Thay đổi phương thức không làm mất đơn vị | 1. Truy cập /user/cart<br>2. Chọn đơn vị GHTK<br>3. Thay đổi phương thức<br>4. Kiểm tra | Đơn vị vận chuyển vẫn được giữ nguyên, chỉ phương thức thay đổi, phí được tính lại | | Pass | 11/15/2015 | |
| **FUNC-CH-11** | Hiển thị chi tiết đơn vị đã chọn | 1. Truy cập /user/cart<br>2. Chọn đơn vị<br>3. Kiểm tra | Thông tin đơn vị đã chọn được hiển thị đầy đủ: tên, phí, thời gian giao, đặc điểm, radio được checked | | Pass | 11/15/2015 | |
| **FUNC-CH-12** | Cập nhật tổng cộng khi chọn đơn vị | 1. Truy cập /user/cart<br>2. Chọn đơn vị<br>3. Kiểm tra tổng cộng | Tổng cộng được tính lại = Tạm tính + Phí vận chuyển - Giảm giá, được cập nhật ngay lập tức | | Pass | 11/15/2015 | |
| **FUNC-CH-13** | Hiển thị điều kiện miễn phí | 1. Truy cập /user/cart<br>2. Kiểm tra thông báo | Hiển thị text "Điều kiện miễn phí: đơn từ 500.000 VNĐ với phương thức tiêu chuẩn" (text-sm text-muted-foreground) | | Pass | 11/15/2015 | |
| **FUNC-CH-14** | Đơn vị mặc định được chọn | 1. Truy cập /user/cart<br>2. Kiểm tra | Đơn vị "GHTK" được chọn mặc định (selectedCarrier = "GHTK"), radio được checked | | Pass | 11/15/2015 | |
| **FUNC-CH-15** | Phương thức mặc định được chọn | 1. Truy cập /user/cart<br>2. Kiểm tra | Phương thức "Giao hàng tiêu chuẩn" được chọn mặc định (shippingMethod = "standard"), radio được checked | | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn MDX để dễ dàng quản lý và cập nhật test cases.*

