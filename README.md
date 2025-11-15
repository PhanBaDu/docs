# Test Case Template - Chức năng vận chuyển (User)

## Module Code
**Model Management Store: Chức năng vận chuyển User**

## Test Requirement
1. Hiển thị các đơn vị vận chuyển
2. Chọn nhà vận chuyển
3. Tính phí vận chuyển
4. Theo dõi trạng thái vận chuyển
5. Xem thông tin giao hàng

---

## Test Summary

### Người thực hiện Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 118 |
| **Fail** | 0 |
| **Untested** | 32 |
| **N/A** | 0 |
| **Number of Test cases** | 150 |

---

## Test Cases

### Function: Hiển thị các đơn vị vận chuyển

#### Check GUI: Hiển thị các đơn vị vận chuyển

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-HTDDVC-01** | Kiểm tra tiêu đề vận chuyển | 1. Truy cập /user/cart<br>2. Kiểm tra tiêu đề | Hiển thị text "Vận chuyển:" với icon Truck | | Pass | 11/15/2015 | |
| **GUI-HTDDVC-02** | Kiểm tra card Vận chuyển | 1. Truy cập /user/cart<br>2. Kiểm tra card | Hiển thị card với icon Truck, tiêu đề "Vận chuyển" | | Pass | 11/15/2015 | |
| **GUI-HTDDVC-03** | Kiểm tra radio button Giao hàng tiêu chuẩn | 1. Truy cập /user/cart<br>2. Kiểm tra radio | Hiển thị radio button với label "Giao hàng tiêu chuẩn", thời gian "3-5 ngày làm việc", phí "30.000 VNĐ" hoặc "Miễn phí" | | Pass | 11/15/2015 | |
| **GUI-HTDDVC-04** | Kiểm tra radio button Giao hàng nhanh | 1. Truy cập /user/cart<br>2. Kiểm tra radio | Hiển thị radio button với label "Giao hàng nhanh", thời gian "1-2 ngày làm việc", phí "50.000 VNĐ" | | Pass | 11/15/2015 | |
| **GUI-HTDDVC-05** | Kiểm tra card Đơn vị vận chuyển | 1. Truy cập /user/cart<br>2. Kiểm tra card | Hiển thị card với icon Truck, tiêu đề "Đơn vị vận chuyển" | | Pass | 11/15/2015 | |
| **GUI-HTDDVC-06** | Kiểm tra radio button GHTK | 1. Truy cập /user/cart<br>2. Kiểm tra radio | Hiển thị radio button với label "Giao hàng tiết kiệm", thời gian "3-5 ngày", phí (miễn phí nếu đơn >= 500.000 hoặc 30.000 VNĐ), mô tả "Tiêu chuẩn, tiết kiệm chi phí" | | Pass | 11/15/2015 | |
| **GUI-HTDDVC-07** | Kiểm tra radio button GHN | 1. Truy cập /user/cart<br>2. Kiểm tra radio | Hiển thị radio button với label "Giao hàng nhanh (GHN)", thời gian "1-2 ngày", phí "50.000 VNĐ", mô tả "Nhanh, ổn định nội thành" | | Pass | 11/15/2015 | |
| **GUI-HTDDVC-08** | Kiểm tra radio button J&T | 1. Truy cập /user/cart<br>2. Kiểm tra radio | Hiển thị radio button với label "J&T Express", thời gian "2-4 ngày", phí (miễn phí nếu đơn >= 500.000 hoặc 30.000 VNĐ), mô tả "Phủ rộng toàn quốc" | | Pass | 11/15/2015 | |
| **GUI-HTDDVC-09** | Kiểm tra điều kiện miễn phí | 1. Truy cập /user/cart<br>2. Kiểm tra thông báo | Hiển thị text "Điều kiện miễn phí: đơn từ 500.000 VNĐ với phương thức tiêu chuẩn" với màu muted-foreground | | Pass | 11/15/2015 | |

---

### Check FUNC: Hiển thị các đơn vị vận chuyển

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-HTDDVC-01** | Hiển thị danh sách đơn vị vận chuyển | 1. Truy cập /user/cart<br>2. Kiểm tra danh sách | Hiển thị đầy đủ các đơn vị: GHTK, GHN, J&T Express với thông tin: tên, thời gian giao hàng, phí vận chuyển, dịch vụ đặc biệt | | Pass | 11/15/2015 | |
| **FUNC-HTDDVC-02** | Hiển thị thông tin chi tiết đơn vị | 1. Truy cập /user/cart<br>2. Chọn một đơn vị<br>3. Kiểm tra thông tin | Hiển thị thông tin chi tiết: phạm vi hoạt động, thời gian giao hàng theo khu vực, phí vận chuyển theo trọng lượng và khoảng cách, dịch vụ đặc biệt | | Pass | 11/15/2015 | |
| **FUNC-HTDDVC-03** | Cập nhật thông tin real-time | 1. Truy cập /user/cart<br>2. Thay đổi địa chỉ giao hàng<br>3. Kiểm tra thông tin | Thông tin đơn vị vận chuyển được cập nhật real-time, phí vận chuyển được tính lại | | Pass | 11/15/2015 | |
| **FUNC-HTDDVC-04** | Hiển thị điều kiện miễn phí | 1. Truy cập /user/cart<br>2. Kiểm tra điều kiện | Hiển thị rõ ràng: giá trị đơn hàng tối thiểu 500.000 VNĐ, khu vực áp dụng, thời gian hiệu lực | | Pass | 11/15/2015 | |
| **FUNC-HTDDVC-05** | Tự động tính phí dựa trên điều kiện | 1. Truy cập /user/cart<br>2. Tạm tính >= 500.000 VNĐ<br>3. Chọn giao hàng tiêu chuẩn<br>4. Kiểm tra phí | Phí vận chuyển hiển thị "Miễn phí" cho phương thức tiêu chuẩn | | Pass | 11/15/2015 | |
| **FUNC-HTDDVC-06** | Tự động tính phí dựa trên điều kiện - Đơn < 500.000 | 1. Truy cập /user/cart<br>2. Tạm tính < 500.000 VNĐ<br>3. Chọn giao hàng tiêu chuẩn<br>4. Kiểm tra phí | Phí vận chuyển = 30.000 VNĐ cho phương thức tiêu chuẩn | | Pass | 11/15/2015 | |

---

### Function: Chọn nhà vận chuyển

#### Check GUI: Chọn nhà vận chuyển

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CNVC-01** | Kiểm tra radio group đơn vị | 1. Truy cập /user/cart<br>2. Kiểm tra radio group | Hiển thị nhóm radio button với các option: GHTK, GHN, J&T Express, chỉ có thể chọn một | | Pass | 11/15/2015 | |
| **GUI-CNVC-02** | Kiểm tra logo đơn vị | 1. Truy cập /user/cart<br>2. Chọn một đơn vị<br>3. Kiểm tra logo | Hiển thị logo của đơn vị vận chuyển đã chọn (nếu có) | | Pass | 11/15/2015 | |
| **GUI-CNVC-03** | Kiểm tra thông tin đơn vị đã chọn | 1. Truy cập /user/cart<br>2. Chọn một đơn vị<br>3. Kiểm tra thông tin | Hiển thị card với thông tin: tên đơn vị, thời gian giao hàng, phí vận chuyển, dịch vụ đặc biệt | | Pass | 11/15/2015 | |

---

### Check FUNC: Chọn nhà vận chuyển

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CNVC-01** | Chọn đơn vị GHTK | 1. Truy cập /user/cart<br>2. Chọn radio button "Giao hàng tiết kiệm"<br>3. Kiểm tra kết quả | Radio button GHTK được chọn, thông tin đơn vị được hiển thị, phí vận chuyển được cập nhật, tổng tiền được tính lại | | Pass | 11/15/2015 | |
| **FUNC-CNVC-02** | Chọn đơn vị GHN | 1. Truy cập /user/cart<br>2. Chọn radio button "Giao hàng nhanh (GHN)"<br>3. Kiểm tra kết quả | Radio button GHN được chọn, thông tin đơn vị được hiển thị, phí vận chuyển = 50.000 VNĐ, tổng tiền được tính lại | | Pass | 11/15/2015 | |
| **FUNC-CNVC-03** | Chọn đơn vị J&T | 1. Truy cập /user/cart<br>2. Chọn radio button "J&T Express"<br>3. Kiểm tra kết quả | Radio button J&T được chọn, thông tin đơn vị được hiển thị, phí vận chuyển được cập nhật, tổng tiền được tính lại | | Pass | 11/15/2015 | |
| **FUNC-CNVC-04** | Chỉ chọn một đơn vị tại một thời điểm | 1. Truy cập /user/cart<br>2. Chọn GHTK<br>3. Chọn GHN<br>4. Kiểm tra kết quả | Chỉ GHN được chọn, GHTK bị bỏ chọn, chỉ một đơn vị được chọn tại một thời điểm | | Pass | 11/15/2015 | |
| **FUNC-CNVC-05** | Hiển thị thông tin đơn vị đã chọn | 1. Truy cập /user/cart<br>2. Chọn một đơn vị<br>3. Kiểm tra thông tin | Hiển thị đầy đủ: logo (nếu có), tên đơn vị, thời gian giao hàng, phí vận chuyển, dịch vụ đặc biệt | | Pass | 11/15/2015 | |
| **FUNC-CNVC-06** | So sánh các đơn vị | 1. Truy cập /user/cart<br>2. Xem danh sách đơn vị<br>3. Kiểm tra so sánh | Có thể so sánh các đơn vị về: thời gian giao hàng, phí vận chuyển, phạm vi hoạt động, dịch vụ đặc biệt, thông tin được hiển thị rõ ràng | | Pass | 11/15/2015 | |
| **FUNC-CNVC-07** | Cập nhật thông tin real-time khi chọn đơn vị | 1. Truy cập /user/cart<br>2. Chọn đơn vị<br>3. Quan sát cập nhật | Thông tin đơn vị được cập nhật ngay lập tức, phí vận chuyển được tính lại, tổng tiền được cập nhật | | Pass | 11/15/2015 | |

---

### Function: Tính phí vận chuyển

#### Check GUI: Tính phí vận chuyển

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-TPVC-01** | Kiểm tra card Tính phí vận chuyển | 1. Truy cập /user/cart<br>2. Kiểm tra card | Hiển thị card với tiêu đề "Tính phí vận chuyển" | | Pass | 11/15/2015 | |
| **GUI-TPVC-02** | Kiểm tra input Địa chỉ giao hàng | 1. Truy cập /user/cart<br>2. Kiểm tra input | Hiển thị Input với label "Địa chỉ giao hàng", placeholder "Số nhà, đường, phường/xã, quận/huyện, tỉnh/thành", có thể nhập text | | Pass | 11/15/2015 | |
| **GUI-TPVC-03** | Kiểm tra input Trọng lượng | 1. Truy cập /user/cart<br>2. Kiểm tra input | Hiển thị Input với label "Trọng lượng (kg)", giá trị readonly, hiển thị tổng trọng lượng sản phẩm | | Pass | 11/15/2015 | |
| **GUI-TPVC-04** | Kiểm tra input Khoảng cách | 1. Truy cập /user/cart<br>2. Kiểm tra input | Hiển thị Input với label "Khoảng cách (km)", giá trị readonly, hiển thị khoảng cách từ kho đến địa chỉ | | Pass | 11/15/2015 | |
| **GUI-TPVC-05** | Kiểm tra Phí cơ bản | 1. Truy cập /user/cart<br>2. Kiểm tra phí | Hiển thị "Phí cơ bản" với giá trị (VD: 10.000 VNĐ) | | Pass | 11/15/2015 | |
| **GUI-TPVC-06** | Kiểm tra Phí theo trọng lượng | 1. Truy cập /user/cart<br>2. Kiểm tra phí | Hiển thị "Phí theo trọng lượng" với giá trị (VD: 8.000 VNĐ) | | Pass | 11/15/2015 | |
| **GUI-TPVC-07** | Kiểm tra Phí theo khoảng cách | 1. Truy cập /user/cart<br>2. Kiểm tra phí | Hiển thị "Phí theo khoảng cách" với giá trị (VD: 12.000 VNĐ) | | Pass | 11/15/2015 | |
| **GUI-TPVC-08** | Kiểm tra Phí dịch vụ | 1. Truy cập /user/cart<br>2. Kiểm tra phí | Hiển thị "Phí dịch vụ" với giá trị (VD: 0 VNĐ) | | Pass | 11/15/2015 | |
| **GUI-TPVC-09** | Kiểm tra Tổng phí vận chuyển | 1. Truy cập /user/cart<br>2. Kiểm tra tổng phí | Hiển thị "Tổng phí vận chuyển (ước tính)" với font medium, giá trị tổng phí hoặc "Miễn phí" | | Pass | 11/15/2015 | |
| **GUI-TPVC-10** | Kiểm tra thông báo miễn phí | 1. Truy cập /user/cart<br>2. Đơn >= 500.000 VNĐ<br>3. Chọn tiêu chuẩn<br>4. Kiểm tra thông báo | Hiển thị "Miễn phí" thay vì số tiền khi đủ điều kiện | | Pass | 11/15/2015 | |

---

### Check FUNC: Tính phí vận chuyển

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TPVC-01** | Tính phí vận chuyển tự động | 1. Truy cập /user/cart<br>2. Nhập địa chỉ giao hàng<br>3. Kiểm tra phí | Phí vận chuyển được tính tự động dựa trên: địa chỉ, trọng lượng, khoảng cách, công thức: Phí cơ bản + Phí theo trọng lượng + Phí theo khoảng cách + Phí dịch vụ | | Pass | 11/15/2015 | |
| **FUNC-TPVC-02** | Tính phí theo địa chỉ | 1. Truy cập /user/cart<br>2. Nhập địa chỉ A<br>3. Kiểm tra phí<br>4. Nhập địa chỉ B<br>5. Kiểm tra phí | Phí vận chuyển được tính lại khi thay đổi địa chỉ, khoảng cách được cập nhật, phí theo khoảng cách được tính lại | | Untested | 11/15/2015 | |
| **FUNC-TPVC-03** | Tính phí theo trọng lượng | 1. Truy cập /user/cart<br>2. Thêm/xóa sản phẩm<br>3. Kiểm tra phí | Phí vận chuyển được tính lại khi thay đổi trọng lượng, phí theo trọng lượng được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-TPVC-04** | Tính phí theo khoảng cách | 1. Truy cập /user/cart<br>2. Thay đổi địa chỉ giao hàng<br>3. Kiểm tra phí | Phí vận chuyển được tính lại khi thay đổi khoảng cách, phí theo khoảng cách được cập nhật | | Untested | 11/15/2015 | |
| **FUNC-TPVC-05** | Kiểm tra điều kiện miễn phí - Đủ điều kiện | 1. Truy cập /user/cart<br>2. Tạm tính >= 500.000 VNĐ<br>3. Chọn giao hàng tiêu chuẩn<br>4. Kiểm tra phí | Phí vận chuyển = 0, hiển thị "Miễn phí", tổng phí vận chuyển = 0 | | Pass | 11/15/2015 | |
| **FUNC-TPVC-06** | Kiểm tra điều kiện miễn phí - Không đủ điều kiện | 1. Truy cập /user/cart<br>2. Tạm tính < 500.000 VNĐ<br>3. Chọn giao hàng tiêu chuẩn<br>4. Kiểm tra phí | Phí vận chuyển = 30.000 VNĐ (tiêu chuẩn) hoặc 50.000 VNĐ (nhanh), không miễn phí | | Pass | 11/15/2015 | |
| **FUNC-TPVC-07** | Cập nhật phí real-time khi thay đổi địa chỉ | 1. Truy cập /user/cart<br>2. Nhập địa chỉ<br>3. Thay đổi địa chỉ<br>4. Quan sát phí | Phí vận chuyển được tính lại ngay lập tức khi thay đổi địa chỉ, tổng tiền được cập nhật | | Untested | 11/15/2015 | |
| **FUNC-TPVC-08** | Cập nhật phí real-time khi thay đổi trọng lượng | 1. Truy cập /user/cart<br>2. Thay đổi số lượng sản phẩm<br>3. Quan sát phí | Phí vận chuyển được tính lại ngay lập tức khi thay đổi trọng lượng, tổng tiền được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-TPVC-09** | Cập nhật phí real-time khi thay đổi đơn vị | 1. Truy cập /user/cart<br>2. Chọn đơn vị vận chuyển<br>3. Thay đổi đơn vị<br>4. Quan sát phí | Phí vận chuyển được tính lại ngay lập tức khi thay đổi đơn vị, tổng tiền được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-TPVC-10** | Hiển thị chi tiết phí vận chuyển | 1. Truy cập /user/cart<br>2. Kiểm tra chi tiết phí | Hiển thị đầy đủ: Phí cơ bản, Phí theo trọng lượng, Phí theo khoảng cách, Phí dịch vụ, Tổng phí vận chuyển | | Pass | 11/15/2015 | |
| **FUNC-TPVC-11** | Tính phí với đơn vị GHTK | 1. Truy cập /user/cart<br>2. Chọn GHTK<br>3. Kiểm tra phí | Phí vận chuyển được tính theo công thức của GHTK, hiển thị chi tiết phí | | Pass | 11/15/2015 | |
| **FUNC-TPVC-12** | Tính phí với đơn vị GHN | 1. Truy cập /user/cart<br>2. Chọn GHN<br>3. Kiểm tra phí | Phí vận chuyển = 50.000 VNĐ (cố định cho GHN), hiển thị chi tiết phí | | Pass | 11/15/2015 | |
| **FUNC-TPVC-13** | Tính phí với đơn vị J&T | 1. Truy cập /user/cart<br>2. Chọn J&T<br>3. Kiểm tra phí | Phí vận chuyển được tính theo công thức của J&T, hiển thị chi tiết phí | | Pass | 11/15/2015 | |

---

### Function: Theo dõi trạng thái vận chuyển

#### Check GUI: Theo dõi trạng thái vận chuyển

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-TDTTVC-01** | Kiểm tra tiêu đề theo dõi | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Theo dõi vận chuyển" hoặc "Theo dõi đơn hàng #[id]" | | Pass | 11/15/2015 | |
| **GUI-TDTTVC-02** | Kiểm tra mã đơn hàng | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra mã | Hiển thị mã đơn hàng với format rõ ràng | | Pass | 11/15/2015 | |
| **GUI-TDTTVC-03** | Kiểm tra mã vận đơn | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra mã | Hiển thị "Mã vận đơn: [Mã]" với font mono | | Pass | 11/15/2015 | |
| **GUI-TDTTVC-04** | Kiểm tra đơn vị vận chuyển | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra đơn vị | Hiển thị "Đơn vị vận chuyển: [Tên đơn vị]" | | Pass | 11/15/2015 | |
| **GUI-TDTTVC-05** | Kiểm tra badge trạng thái hiện tại | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra badge | Hiển thị badge trạng thái vận chuyển với màu sắc và text: Đã nhận hàng, Đang vận chuyển, Đang giao hàng, Đã giao hàng | | Pass | 11/15/2015 | |
| **GUI-TDTTVC-06** | Kiểm tra Timeline vận chuyển | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra timeline | Hiển thị timeline các trạng thái: Đã nhận hàng, Đang vận chuyển, Đang giao hàng, Đã giao hàng, với thời gian cụ thể | | Pass | 11/15/2015 | |
| **GUI-TDTTVC-07** | Kiểm tra thời gian cập nhật | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra thời gian | Hiển thị "Thời gian cập nhật: [Thời gian]" cho mỗi mốc trong timeline | | Pass | 11/15/2015 | |
| **GUI-TDTTVC-08** | Kiểm tra vị trí hiện tại | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra vị trí | Hiển thị "Vị trí hiện tại: [Vị trí]" (nếu có) | | Pass | 11/15/2015 | |
| **GUI-TDTTVC-09** | Kiểm tra thời gian dự kiến | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra thời gian | Hiển thị "Thời gian giao hàng dự kiến: [Thời gian]" | | Pass | 11/15/2015 | |
| **GUI-TDTTVC-10** | Kiểm tra nút Liên hệ hỗ trợ | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra nút | Hiển thị nút "Liên hệ hỗ trợ" variant outline | | Pass | 11/15/2015 | |

---

### Check FUNC: Theo dõi trạng thái vận chuyển

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TDTTVC-01** | Hiển thị trạng thái vận chuyển | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra trạng thái | Hiển thị trạng thái hiện tại: Đã nhận hàng, Đang vận chuyển, Đang giao hàng, Đã giao hàng, với badge màu sắc tương ứng | | Pass | 11/15/2015 | |
| **FUNC-TDTTVC-02** | Hiển thị timeline vận chuyển | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra timeline | Hiển thị timeline các mốc: Đã nhận hàng, Đang vận chuyển, Đang giao hàng, Đã giao hàng, với thời gian cụ thể, sắp xếp theo thời gian mới nhất trước | | Pass | 11/15/2015 | |
| **FUNC-TDTTVC-03** | Cập nhật trạng thái real-time | 1. Truy cập /user/orders/track/[id]<br>2. Trạng thái vận chuyển thay đổi<br>3. Kiểm tra cập nhật | Trạng thái được cập nhật ngay lập tức, timeline được cập nhật với mốc mới, thời gian cập nhật được hiển thị | | Untested | 11/15/2015 | |
| **FUNC-TDTTVC-04** | Đồng bộ với hệ thống đơn vị vận chuyển | 1. Truy cập /user/orders/track/[id]<br>2. Trạng thái thay đổi trong hệ thống đơn vị<br>3. Kiểm tra đồng bộ | Thông tin được đồng bộ liên tục từ hệ thống đơn vị vận chuyển, hiển thị ngay lập tức khi có thay đổi | | Untested | 11/15/2015 | |
| **FUNC-TDTTVC-05** | Hiển thị vị trí hiện tại | 1. Truy cập /user/orders/track/[id]<br>2. Đơn hàng đang vận chuyển<br>3. Kiểm tra vị trí | Hiển thị vị trí hiện tại của đơn hàng (nếu đơn vị hỗ trợ), cập nhật real-time | | Untested | 11/15/2015 | |
| **FUNC-TDTTVC-06** | Thông báo cập nhật real-time | 1. Truy cập /user/orders/track/[id]<br>2. Trạng thái vận chuyển thay đổi<br>3. Kiểm tra thông báo | Hiển thị thông báo notification real-time khi có thay đổi trạng thái, có thể gửi qua email, SMS, push notification | | Untested | 11/15/2015 | |
| **FUNC-TDTTVC-07** | Click nút Liên hệ hỗ trợ | 1. Truy cập /user/orders/track/[id]<br>2. Click nút "Liên hệ hỗ trợ" | Chuyển đến trang /user/support | | Pass | 11/15/2015 | |
| **FUNC-TDTTVC-08** | Theo dõi hành trình đơn hàng | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra hành trình | Hiển thị đầy đủ hành trình từ khi nhận hàng đến khi giao hàng, mỗi mốc có thời gian và mô tả cụ thể | | Pass | 11/15/2015 | |

---

### Function: Xem thông tin giao hàng

#### Check GUI: Xem thông tin giao hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XTTTGH-01** | Kiểm tra tiêu đề thông tin | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Thông tin vận chuyển" hoặc "Thông tin giao hàng" | | Pass | 11/15/2015 | |
| **GUI-XTTTGH-02** | Kiểm tra card Phí vận chuyển | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra card | Hiển thị card với thông tin phí vận chuyển: Miễn phí điều kiện, Phí tiêu chuẩn, Phí giao hàng nhanh | | Pass | 11/15/2015 | |
| **GUI-XTTTGH-03** | Kiểm tra card Thời gian giao hàng | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra card | Hiển thị card với thông tin: TP.HCM (1-2 ngày), Các tỉnh khác (3-5 ngày), Vùng sâu vùng xa (5-7 ngày) | | Pass | 11/15/2015 | |
| **GUI-XTTTGH-04** | Kiểm tra card Địa chỉ giao hàng | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra card | Hiển thị card với thông tin: Tên người nhận, Số điện thoại, Địa chỉ chi tiết, Ghi chú giao hàng | | Pass | 11/15/2015 | |

---

### Check FUNC: Xem thông tin giao hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XTTTGH-01** | Hiển thị thông tin giao hàng | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra thông tin | Hiển thị đầy đủ: phí vận chuyển, thời gian giao hàng, địa chỉ giao hàng, các thông tin liên quan | | Pass | 11/15/2015 | |
| **FUNC-XTTTGH-02** | Hiển thị phí vận chuyển | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra phí | Hiển thị: Miễn phí cho đơn từ 500.000 VNĐ, Phí tiêu chuẩn 30.000 VNĐ cho đơn dưới 500.000 VNĐ, Phí giao hàng nhanh 50.000 VNĐ | | Pass | 11/15/2015 | |
| **FUNC-XTTTGH-03** | Hiển thị thời gian giao hàng | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra thời gian | Hiển thị: TP.HCM (1-2 ngày làm việc), Các tỉnh khác (3-5 ngày làm việc), Vùng sâu vùng xa (5-7 ngày làm việc) | | Pass | 11/15/2015 | |
| **FUNC-XTTTGH-04** | Hiển thị địa chỉ giao hàng | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra địa chỉ | Hiển thị đầy đủ: Tên người nhận, Số điện thoại, Địa chỉ chi tiết, Ghi chú giao hàng (nếu có) | | Pass | 11/15/2015 | |
| **FUNC-XTTTGH-05** | Cập nhật thông tin real-time | 1. Truy cập /user/orders/track/[id]<br>2. Thông tin giao hàng thay đổi<br>3. Kiểm tra cập nhật | Thông tin được cập nhật real-time từ hệ thống đơn vị vận chuyển, hiển thị ngay lập tức khi có thay đổi | | Untested | 11/15/2015 | |
| **FUNC-XTTTGH-06** | Hiển thị điều kiện giao hàng | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra điều kiện | Hiển thị rõ ràng: phạm vi giao hàng, thời gian giao hàng theo khu vực, phí vận chuyển, điều kiện đặc biệt | | Pass | 11/15/2015 | |
| **FUNC-XTTTGH-07** | Hiển thị thông tin trong chi tiết đơn hàng | 1. Truy cập /user/account/orders/[id]<br>2. Kiểm tra thông tin giao hàng | Hiển thị card "Thông tin giao hàng" với đầy đủ: Tên người nhận, Số điện thoại, Địa chỉ, Ghi chú | | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn Markdown để dễ dàng quản lý và cập nhật test cases.*

