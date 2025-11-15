# Test Case Template - Chức năng quản lý đơn hàng (User)

## Module Code
**Model Management Store: Chức năng quản lý đơn hàng User**

## Test Requirement
1. Xem thông tin đơn hàng
2. Xem chi tiết đơn hàng
3. Theo dõi đơn hàng
4. Lọc đơn hàng theo trạng thái
5. Hủy đơn hàng
6. Đánh giá đơn hàng
7. Đặt lại đơn hàng
8. Yêu cầu đổi/trả hàng
9. Xem timeline vận chuyển
10. Xem thông tin thanh toán

---

## Test Summary

### Người thực hiện Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 168 |
| **Fail** | 0 |
| **Untested** | 42 |
| **N/A** | 0 |
| **Number of Test cases** | 210 |

---

## Test Cases

### Function: Xem thông tin đơn hàng

#### Check GUI: Xem thông tin đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XTTDH-01** | Kiểm tra tiêu đề trang | 1. Truy cập /user/account/orders<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Quản lý đơn hàng" với icon Package | | Pass | 11/15/2015 | |
| **GUI-XTTDH-02** | Kiểm tra mô tả trang | 1. Truy cập /user/account/orders<br>2. Kiểm tra mô tả | Hiển thị mô tả "Theo dõi và quản lý các đơn hàng của bạn" | | Pass | 11/15/2015 | |
| **GUI-XTTDH-03** | Kiểm tra bộ lọc trạng thái | 1. Truy cập /user/account/orders<br>2. Kiểm tra dropdown | Hiển thị Select với các option: Tất cả, Đang xử lý, Đang giao, Đã giao, Đã hủy | | Pass | 11/15/2015 | |
| **GUI-XTTDH-04** | Kiểm tra thống kê số lượng đơn hàng | 1. Truy cập /user/account/orders<br>2. Kiểm tra thống kê | Hiển thị text "X đơn hàng" với màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-XTTDH-05** | Kiểm tra card đơn hàng | 1. Truy cập /user/account/orders<br>2. Có đơn hàng<br>3. Kiểm tra card | Hiển thị card với icon Package, mã đơn hàng, ngày đặt hàng, badge trạng thái, danh sách sản phẩm, địa chỉ giao hàng, phương thức thanh toán, mã vận đơn, tổng tiền, các nút hành động | | Pass | 11/15/2015 | |
| **GUI-XTTDH-06** | Kiểm tra mã đơn hàng | 1. Truy cập /user/account/orders<br>2. Kiểm tra mã | Hiển thị "Đơn hàng #[Mã]" với icon Package | | Pass | 11/15/2015 | |
| **GUI-XTTDH-07** | Kiểm tra ngày đặt hàng | 1. Truy cập /user/account/orders<br>2. Kiểm tra ngày | Hiển thị "Đặt ngày [Ngày]" với định dạng Việt Nam | | Pass | 11/15/2015 | |
| **GUI-XTTDH-08** | Kiểm tra badge trạng thái | 1. Truy cập /user/account/orders<br>2. Kiểm tra badge | Hiển thị badge với icon tương ứng, màu sắc và text trạng thái (Đang xử lý, Đang giao, Đã giao, Đã hủy) | | Pass | 11/15/2015 | |
| **GUI-XTTDH-09** | Kiểm tra danh sách sản phẩm | 1. Truy cập /user/account/orders<br>2. Kiểm tra danh sách | Hiển thị danh sách sản phẩm với tên, số lượng, giá tổng cho mỗi sản phẩm | | Pass | 11/15/2015 | |
| **GUI-XTTDH-10** | Kiểm tra thông tin giao hàng | 1. Truy cập /user/account/orders<br>2. Kiểm tra thông tin | Hiển thị icon MapPin, label "Địa chỉ giao hàng:", địa chỉ đầy đủ | | Pass | 11/15/2015 | |
| **GUI-XTTDH-11** | Kiểm tra thông tin thanh toán | 1. Truy cập /user/account/orders<br>2. Kiểm tra thông tin | Hiển thị icon CreditCard, label "Phương thức thanh toán:", phương thức thanh toán | | Pass | 11/15/2015 | |
| **GUI-XTTDH-12** | Kiểm tra mã vận đơn | 1. Truy cập /user/account/orders<br>2. Đơn hàng có mã vận đơn<br>3. Kiểm tra mã | Hiển thị icon Truck, label "Mã vận đơn:", mã vận đơn với font mono | | Pass | 11/15/2015 | |
| **GUI-XTTDH-13** | Kiểm tra tổng tiền | 1. Truy cập /user/account/orders<br>2. Kiểm tra tổng tiền | Hiển thị "Tổng cộng: [Số tiền] VNĐ" với font bold text-lg | | Pass | 11/15/2015 | |
| **GUI-XTTDH-14** | Kiểm tra nút Xem chi tiết | 1. Truy cập /user/account/orders<br>2. Kiểm tra nút | Hiển thị nút "Xem chi tiết" variant outline size sm với icon Eye | | Pass | 11/15/2015 | |
| **GUI-XTTDH-15** | Kiểm tra nút Đặt lại | 1. Truy cập /user/account/orders<br>2. Đơn hàng có thể đặt lại<br>3. Kiểm tra nút | Hiển thị nút "Đặt lại" variant outline size sm với icon RotateCcw, chỉ hiển thị khi có thể đặt lại | | Pass | 11/15/2015 | |
| **GUI-XTTDH-16** | Kiểm tra nút Đánh giá | 1. Truy cập /user/account/orders<br>2. Đơn hàng đã giao<br>3. Kiểm tra nút | Hiển thị nút "Đánh giá" variant outline size sm với icon Star, chỉ hiển thị khi đơn đã giao | | Pass | 11/15/2015 | |
| **GUI-XTTDH-17** | Kiểm tra nút Hủy đơn | 1. Truy cập /user/account/orders<br>2. Đơn hàng đang xử lý<br>3. Kiểm tra nút | Hiển thị nút "Hủy đơn" variant destructive size sm với icon XCircle, chỉ hiển thị khi đơn đang xử lý | | Pass | 11/15/2015 | |
| **GUI-XTTDH-18** | Kiểm tra nút Đổi trả | 1. Truy cập /user/account/orders<br>2. Đơn hàng đã giao<br>3. Kiểm tra nút | Hiển thị nút "Đổi trả" variant outline size sm với icon RotateCcw, chỉ hiển thị khi đơn đã giao | | Pass | 11/15/2015 | |
| **GUI-XTTDH-19** | Kiểm tra thông báo không có đơn hàng | 1. Truy cập /user/account/orders<br>2. Không có đơn hàng<br>3. Kiểm tra thông báo | Hiển thị card với icon Package, tiêu đề "Không có đơn hàng", mô tả, nút "Mua sắm ngay" | | Pass | 11/15/2015 | |
| **GUI-XTTDH-20** | Kiểm tra card Thống kê đơn hàng | 1. Truy cập /user/account/orders<br>2. Kiểm tra card | Hiển thị card với tiêu đề "Thống kê đơn hàng", grid 4 cột: Đang xử lý, Đang giao, Đã giao, Đã hủy với số lượng và màu sắc tương ứng | | Pass | 11/15/2015 | |

---

### Check FUNC: Xem thông tin đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XTTDH-01** | Mở trang quản lý đơn hàng | 1. Truy cập /user/account/orders | Hiển thị trang với tiêu đề, mô tả, bộ lọc trạng thái, danh sách đơn hàng, thống kê đơn hàng | | Pass | 11/15/2015 | |
| **FUNC-XTTDH-02** | Hiển thị danh sách đơn hàng | 1. Truy cập /user/account/orders<br>2. Có đơn hàng<br>3. Kiểm tra danh sách | Hiển thị tất cả đơn hàng với đầy đủ thông tin, sắp xếp theo thời gian mới nhất trước | | Pass | 11/15/2015 | |
| **FUNC-XTTDH-03** | Lọc đơn hàng theo trạng thái - Tất cả | 1. Truy cập /user/account/orders<br>2. Chọn "Tất cả" từ dropdown<br>3. Kiểm tra kết quả | Hiển thị tất cả đơn hàng, không lọc theo trạng thái | | Pass | 11/15/2015 | |
| **FUNC-XTTDH-04** | Lọc đơn hàng theo trạng thái - Đang xử lý | 1. Truy cập /user/account/orders<br>2. Chọn "Đang xử lý" từ dropdown<br>3. Kiểm tra kết quả | Hiển thị chỉ đơn hàng có trạng thái "Đang xử lý", cập nhật số lượng đơn hàng | | Pass | 11/15/2015 | |
| **FUNC-XTTDH-05** | Lọc đơn hàng theo trạng thái - Đang giao | 1. Truy cập /user/account/orders<br>2. Chọn "Đang giao" từ dropdown<br>3. Kiểm tra kết quả | Hiển thị chỉ đơn hàng có trạng thái "Đang giao", cập nhật số lượng đơn hàng | | Pass | 11/15/2015 | |
| **FUNC-XTTDH-06** | Lọc đơn hàng theo trạng thái - Đã giao | 1. Truy cập /user/account/orders<br>2. Chọn "Đã giao" từ dropdown<br>3. Kiểm tra kết quả | Hiển thị chỉ đơn hàng có trạng thái "Đã giao", cập nhật số lượng đơn hàng | | Pass | 11/15/2015 | |
| **FUNC-XTTDH-07** | Lọc đơn hàng theo trạng thái - Đã hủy | 1. Truy cập /user/account/orders<br>2. Chọn "Đã hủy" từ dropdown<br>3. Kiểm tra kết quả | Hiển thị chỉ đơn hàng có trạng thái "Đã hủy", cập nhật số lượng đơn hàng | | Pass | 11/15/2015 | |
| **FUNC-XTTDH-08** | Lọc không có kết quả | 1. Truy cập /user/account/orders<br>2. Chọn trạng thái không có đơn hàng<br>3. Kiểm tra kết quả | Hiển thị thông báo "Không có đơn hàng với trạng thái '[Trạng thái]'", nút "Mua sắm ngay" | | Pass | 11/15/2015 | |
| **FUNC-XTTDH-09** | Cập nhật danh sách real-time | 1. Truy cập /user/account/orders<br>2. Thay đổi bộ lọc<br>3. Quan sát kết quả | Danh sách đơn hàng được cập nhật ngay lập tức khi thay đổi bộ lọc | | Pass | 11/15/2015 | |
| **FUNC-XTTDH-10** | Hiển thị thống kê đơn hàng | 1. Truy cập /user/account/orders<br>2. Kiểm tra thống kê | Hiển thị số lượng đơn hàng theo từng trạng thái: Đang xử lý (màu xanh dương), Đang giao (màu vàng), Đã giao (màu xanh lá), Đã hủy (màu đỏ) | | Pass | 11/15/2015 | |
| **FUNC-XTTDH-11** | Click nút Mua sắm ngay | 1. Truy cập /user/account/orders<br>2. Không có đơn hàng<br>3. Click nút "Mua sắm ngay" | Chuyển đến trang /user/products | | Pass | 11/15/2015 | |

---

### Function: Xem chi tiết đơn hàng

#### Check GUI: Xem chi tiết đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XCTDH-01** | Kiểm tra tiêu đề trang | 1. Truy cập /user/account/orders/[id]<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Chi tiết đơn hàng" | | Pass | 11/15/2015 | |
| **GUI-XCTDH-02** | Kiểm tra mã đơn hàng | 1. Truy cập /user/account/orders/[id]<br>2. Kiểm tra mã | Hiển thị mã đơn hàng với format rõ ràng | | Pass | 11/15/2015 | |
| **GUI-XCTDH-03** | Kiểm tra badge trạng thái | 1. Truy cập /user/account/orders/[id]<br>2. Kiểm tra badge | Hiển thị badge trạng thái với màu sắc và icon tương ứng | | Pass | 11/15/2015 | |
| **GUI-XCTDH-04** | Kiểm tra card Thông tin khách hàng | 1. Truy cập /user/account/orders/[id]<br>2. Kiểm tra card | Hiển thị card với tiêu đề "Thông tin khách hàng", thông tin người đặt hàng | | Pass | 11/15/2015 | |
| **GUI-XCTDH-05** | Kiểm tra card Danh sách sản phẩm | 1. Truy cập /user/account/orders/[id]<br>2. Kiểm tra card | Hiển thị card với danh sách sản phẩm, mỗi sản phẩm có hình ảnh, tên, số lượng, giá, tổng tiền | | Pass | 11/15/2015 | |
| **GUI-XCTDH-06** | Kiểm tra card Thông tin giao hàng | 1. Truy cập /user/account/orders/[id]<br>2. Kiểm tra card | Hiển thị card với tiêu đề "Thông tin giao hàng", thông tin người nhận, địa chỉ | | Pass | 11/15/2015 | |
| **GUI-XCTDH-07** | Kiểm tra card Thông tin thanh toán | 1. Truy cập /user/account/orders/[id]<br>2. Kiểm tra card | Hiển thị card với tiêu đề "Thông tin thanh toán", phương thức thanh toán, trạng thái thanh toán | | Pass | 11/15/2015 | |
| **GUI-XCTDH-08** | Kiểm tra card Tóm tắt đơn hàng | 1. Truy cập /user/account/orders/[id]<br>2. Kiểm tra card | Hiển thị card với tiêu đề "Tóm tắt đơn hàng", Tạm tính, Phí vận chuyển, Giảm giá, Tổng cộng | | Pass | 11/15/2015 | |
| **GUI-XCTDH-09** | Kiểm tra Timeline lịch sử trạng thái | 1. Truy cập /user/account/orders/[id]<br>2. Kiểm tra timeline | Hiển thị timeline các thay đổi trạng thái theo thời gian, bao gồm trạng thái hoàn tiền | | Pass | 11/15/2015 | |

---

### Check FUNC: Xem chi tiết đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XCTDH-01** | Mở trang chi tiết đơn hàng | 1. Truy cập /user/account/orders/[id] | Hiển thị trang với đầy đủ thông tin: mã đơn hàng, trạng thái, thông tin khách hàng, danh sách sản phẩm, thông tin giao hàng, thông tin thanh toán, tóm tắt đơn hàng, timeline | | Pass | 11/15/2015 | |
| **FUNC-XCTDH-02** | Hiển thị thông tin khách hàng | 1. Truy cập /user/account/orders/[id]<br>2. Kiểm tra thông tin | Hiển thị đầy đủ: Họ tên, Email, Số điện thoại của người đặt hàng | | Pass | 11/15/2015 | |
| **FUNC-XCTDH-03** | Hiển thị danh sách sản phẩm | 1. Truy cập /user/account/orders/[id]<br>2. Kiểm tra danh sách | Hiển thị tất cả sản phẩm trong đơn hàng với hình ảnh, tên, số lượng, giá đơn vị, tổng tiền cho mỗi sản phẩm | | Pass | 11/15/2015 | |
| **FUNC-XCTDH-04** | Hiển thị thông tin giao hàng | 1. Truy cập /user/account/orders/[id]<br>2. Kiểm tra thông tin | Hiển thị đầy đủ: Họ tên người nhận, Số điện thoại, Địa chỉ giao hàng, Ghi chú (nếu có) | | Pass | 11/15/2015 | |
| **FUNC-XCTDH-05** | Hiển thị thông tin thanh toán | 1. Truy cập /user/account/orders/[id]<br>2. Kiểm tra thông tin | Hiển thị đầy đủ: Phương thức thanh toán, Trạng thái thanh toán, Mã giao dịch (nếu có) | | Pass | 11/15/2015 | |
| **FUNC-XCTDH-06** | Hiển thị tóm tắt đơn hàng | 1. Truy cập /user/account/orders/[id]<br>2. Kiểm tra tóm tắt | Hiển thị đầy đủ: Tạm tính, Phí vận chuyển, Giảm giá (nếu có), Tổng cộng, tất cả được tính toán chính xác | | Pass | 11/15/2015 | |
| **FUNC-XCTDH-07** | Hiển thị timeline lịch sử trạng thái | 1. Truy cập /user/account/orders/[id]<br>2. Kiểm tra timeline | Hiển thị timeline các thay đổi trạng thái theo thời gian, bao gồm: Chờ xử lý, Đã xác nhận, Đang chuẩn bị, Đang giao hàng, Đã giao hàng, Đã hủy, Đã hoàn tiền, Hoàn tiền một phần | | Pass | 11/15/2015 | |
| **FUNC-XCTDH-08** | Click nút Xem chi tiết từ danh sách | 1. Truy cập /user/account/orders<br>2. Click nút "Xem chi tiết" trên một đơn hàng<br>3. Kiểm tra kết quả | Chuyển đến trang /user/account/orders/[id] với thông tin chi tiết đơn hàng | | Pass | 11/15/2015 | |

---

### Function: Theo dõi đơn hàng

#### Check GUI: Theo dõi đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-TDDH-01** | Kiểm tra tiêu đề trang | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Theo dõi đơn hàng #[id]" | | Pass | 11/15/2015 | |
| **GUI-TDDH-02** | Kiểm tra mô tả trang | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra mô tả | Hiển thị mô tả "Trạng thái đơn hàng và thanh toán" | | Pass | 11/15/2015 | |
| **GUI-TDDH-03** | Kiểm tra trạng thái đơn hàng | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra trạng thái | Hiển thị "Trạng thái đơn hàng:" với badge trạng thái | | Pass | 11/15/2015 | |
| **GUI-TDDH-04** | Kiểm tra trạng thái thanh toán | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra trạng thái | Hiển thị "Trạng thái thanh toán:" với badge trạng thái | | Pass | 11/15/2015 | |
| **GUI-TDDH-05** | Kiểm tra mã vận đơn | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra mã | Hiển thị "Mã vận đơn: [Mã]" | | Pass | 11/15/2015 | |
| **GUI-TDDH-06** | Kiểm tra địa chỉ giao hàng | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra địa chỉ | Hiển thị "Địa chỉ giao hàng: [Địa chỉ]" | | Pass | 11/15/2015 | |
| **GUI-TDDH-07** | Kiểm tra thời gian dự kiến | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra thời gian | Hiển thị "Thời gian dự kiến: [Thời gian]" | | Pass | 11/15/2015 | |
| **GUI-TDDH-08** | Kiểm tra nút Hủy đơn hàng | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra nút | Hiển thị nút "Hủy đơn hàng" variant destructive, chỉ hiển thị khi đơn có thể hủy | | Pass | 11/15/2015 | |
| **GUI-TDDH-09** | Kiểm tra nút Liên hệ hỗ trợ | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra nút | Hiển thị nút "Liên hệ hỗ trợ" variant outline | | Pass | 11/15/2015 | |
| **GUI-TDDH-10** | Kiểm tra card Timeline vận chuyển | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra card | Hiển thị card với tiêu đề "Timeline vận chuyển", mô tả "Các mốc cập nhật gần đây", danh sách các mốc thời gian | | Pass | 11/15/2015 | |
| **GUI-TDDH-11** | Kiểm tra card Thông tin thanh toán | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra card | Hiển thị card với tiêu đề "Thông tin thanh toán", mô tả "Chi tiết thanh toán", Phương thức, Trạng thái, Mã giao dịch | | Pass | 11/15/2015 | |

---

### Check FUNC: Theo dõi đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TDDH-01** | Mở trang theo dõi đơn hàng | 1. Truy cập /user/orders/track/[id] | Hiển thị trang với tiêu đề, trạng thái đơn hàng, trạng thái thanh toán, mã vận đơn, địa chỉ, thời gian, timeline, thông tin thanh toán | | Pass | 11/15/2015 | |
| **FUNC-TDDH-02** | Hiển thị trạng thái đơn hàng | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra trạng thái | Hiển thị trạng thái hiện tại của đơn hàng với badge màu sắc tương ứng | | Pass | 11/15/2015 | |
| **FUNC-TDDH-03** | Hiển thị trạng thái thanh toán | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra trạng thái | Hiển thị trạng thái thanh toán (Đã thanh toán, Chưa thanh toán, Đã hoàn tiền, Hoàn tiền một phần) với badge màu sắc tương ứng | | Pass | 11/15/2015 | |
| **FUNC-TDDH-04** | Hiển thị timeline vận chuyển | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra timeline | Hiển thị timeline các mốc cập nhật: Đơn hàng đang giao, Đơn hàng đã rời kho, Đơn hàng đã đến kho trung chuyển, với thời gian cụ thể | | Pass | 11/15/2015 | |
| **FUNC-TDDH-05** | Cập nhật timeline real-time | 1. Truy cập /user/orders/track/[id]<br>2. Trạng thái đơn hàng thay đổi<br>3. Kiểm tra timeline | Timeline được cập nhật với mốc mới, hiển thị thời gian và mô tả | | Untested | 11/15/2015 | |
| **FUNC-TDDH-06** | Click nút Liên hệ hỗ trợ | 1. Truy cập /user/orders/track/[id]<br>2. Click nút "Liên hệ hỗ trợ" | Chuyển đến trang /user/support | | Pass | 11/15/2015 | |
| **FUNC-TDDH-07** | Thông báo cập nhật real-time | 1. Truy cập /user/orders/track/[id]<br>2. Trạng thái đơn hàng thay đổi<br>3. Kiểm tra thông báo | Hiển thị thông báo notification khi có cập nhật trạng thái mới | | Untested | 11/15/2015 | |

---

### Function: Lọc đơn hàng theo trạng thái

#### Check GUI: Lọc đơn hàng theo trạng thái

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-LCTTDH-01** | Kiểm tra dropdown lọc | 1. Truy cập /user/account/orders<br>2. Kiểm tra dropdown | Hiển thị Select với width 48, các option: Tất cả, Đang xử lý, Đang giao, Đã giao, Đã hủy | | Pass | 11/15/2015 | |

---

### Check FUNC: Lọc đơn hàng theo trạng thái

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-LCTTDH-01** | Lọc đơn hàng theo trạng thái | 1. Truy cập /user/account/orders<br>2. Chọn trạng thái từ dropdown<br>3. Kiểm tra kết quả | Danh sách đơn hàng được lọc theo trạng thái đã chọn, cập nhật số lượng đơn hàng, cập nhật thống kê | | Pass | 11/15/2015 | |
| **FUNC-LCTTDH-02** | Cập nhật danh sách real-time | 1. Truy cập /user/account/orders<br>2. Thay đổi bộ lọc<br>3. Quan sát kết quả | Danh sách đơn hàng được cập nhật ngay lập tức khi thay đổi bộ lọc, không cần submit | | Pass | 11/15/2015 | |

---

### Function: Hủy đơn hàng

#### Check GUI: Hủy đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-HDH-01** | Kiểm tra nút Hủy đơn hàng | 1. Truy cập /user/account/orders/[id]<br>2. Đơn hàng đang xử lý<br>3. Kiểm tra nút | Hiển thị nút "Hủy đơn hàng" variant destructive với icon XCircle | | Pass | 11/15/2015 | |
| **GUI-HDH-02** | Kiểm tra modal xác nhận | 1. Truy cập /user/account/orders/[id]<br>2. Click nút Hủy đơn hàng<br>3. Kiểm tra modal | Hiển thị Dialog với tiêu đề "Xác nhận hủy đơn hàng", thông báo "Bạn có chắc chắn muốn hủy đơn hàng này?" | | Pass | 11/15/2015 | |
| **GUI-HDH-03** | Kiểm tra dropdown lý do hủy | 1. Truy cập /user/account/orders/[id]<br>2. Mở modal hủy<br>3. Kiểm tra dropdown | Hiển thị Select với các lý do hủy: Không cần nữa, Đổi ý, Sản phẩm không phù hợp, Lý do khác | | Pass | 11/15/2015 | |
| **GUI-HDH-04** | Kiểm tra textarea lý do chi tiết | 1. Truy cập /user/account/orders/[id]<br>2. Mở modal hủy<br>3. Kiểm tra textarea | Hiển thị Textarea với label "Lý do hủy chi tiết (bắt buộc)", placeholder, required | | Pass | 11/15/2015 | |
| **GUI-HDH-05** | Kiểm tra textarea ghi chú | 1. Truy cập /user/account/orders/[id]<br>2. Mở modal hủy<br>3. Kiểm tra textarea | Hiển thị Textarea với label "Ghi chú thêm", placeholder, không bắt buộc | | Pass | 11/15/2015 | |
| **GUI-HDH-06** | Kiểm tra nút Xác nhận hủy | 1. Truy cập /user/account/orders/[id]<br>2. Mở modal hủy<br>3. Kiểm tra nút | Hiển thị nút "Xác nhận hủy" | | Pass | 11/15/2015 | |
| **GUI-HDH-07** | Kiểm tra nút Hủy | 1. Truy cập /user/account/orders/[id]<br>2. Mở modal hủy<br>3. Kiểm tra nút | Hiển thị nút "Hủy" variant outline | | Pass | 11/15/2015 | |

---

### Check FUNC: Hủy đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-HDH-01** | Mở modal hủy đơn hàng | 1. Truy cập /user/account/orders/[id]<br>2. Click nút "Hủy đơn hàng" | Modal Dialog hiển thị với tiêu đề, thông báo, dropdown lý do, textarea lý do chi tiết, textarea ghi chú, 2 nút (Hủy, Xác nhận hủy) | | Pass | 11/15/2015 | |
| **FUNC-HDH-02** | Hủy đơn hàng thành công | 1. Truy cập /user/account/orders/[id]<br>2. Click nút Hủy đơn hàng<br>3. Chọn lý do hủy<br>4. Nhập lý do chi tiết<br>5. Click "Xác nhận hủy" | Hiển thị thông báo "Đơn hàng đã được hủy thành công", trạng thái đơn hàng chuyển thành "Đã hủy", hoàn tiền nếu đã thanh toán, trạng thái hoàn tiền được cập nhật | | Untested | 11/15/2015 | |
| **FUNC-HDH-03** | Hủy đơn hàng - Thiếu lý do chi tiết | 1. Truy cập /user/account/orders/[id]<br>2. Mở modal hủy<br>3. Chọn lý do hủy<br>4. Để trống lý do chi tiết<br>5. Click "Xác nhận hủy" | Hiển thị cảnh báo "Lý do hủy chi tiết là bắt buộc", không hủy đơn hàng | | Pass | 11/15/2015 | |
| **FUNC-HDH-04** | Hủy đơn hàng - Đóng modal bằng nút Hủy | 1. Truy cập /user/account/orders/[id]<br>2. Mở modal hủy<br>3. Click nút "Hủy" | Modal đóng, không hủy đơn hàng | | Pass | 11/15/2015 | |
| **FUNC-HDH-05** | Hủy đơn hàng - Đóng modal bằng click bên ngoài | 1. Truy cập /user/account/orders/[id]<br>2. Mở modal hủy<br>3. Click bên ngoài modal | Modal đóng, không hủy đơn hàng | | Pass | 11/15/2015 | |
| **FUNC-HDH-06** | Hủy đơn hàng - Đơn đang giao hàng | 1. Truy cập /user/account/orders/[id] (đơn đang giao)<br>2. Kiểm tra nút Hủy | Nút "Hủy đơn hàng" không hiển thị hoặc bị disabled, không thể hủy đơn đang giao | | Pass | 11/15/2015 | |
| **FUNC-HDH-07** | Hủy đơn hàng - Đơn đã giao | 1. Truy cập /user/account/orders/[id] (đơn đã giao)<br>2. Kiểm tra nút Hủy | Nút "Hủy đơn hàng" không hiển thị, không thể hủy đơn đã giao | | Pass | 11/15/2015 | |
| **FUNC-HDH-08** | Hủy đơn hàng - Đơn đã hủy | 1. Truy cập /user/account/orders/[id] (đơn đã hủy)<br>2. Kiểm tra nút Hủy | Nút "Hủy đơn hàng" không hiển thị, không thể hủy đơn đã hủy | | Pass | 11/15/2015 | |
| **FUNC-HDH-09** | Hoàn tiền sau khi hủy đơn | 1. Truy cập /user/account/orders/[id]<br>2. Đơn hàng đã thanh toán<br>3. Hủy đơn hàng thành công<br>4. Kiểm tra hoàn tiền | Trạng thái hoàn tiền được cập nhật thành "Đã hoàn tiền" hoặc "Hoàn tiền một phần", tiền được hoàn về tài khoản | | Untested | 11/15/2015 | |

---

### Function: Đánh giá đơn hàng

#### Check GUI: Đánh giá đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DGDH-01** | Kiểm tra nút Đánh giá | 1. Truy cập /user/account/orders/[id]<br>2. Đơn hàng đã giao<br>3. Kiểm tra nút | Hiển thị nút "Đánh giá" variant outline size sm với icon Star, chỉ hiển thị khi đơn đã giao | | Pass | 11/15/2015 | |
| **GUI-DGDH-02** | Kiểm tra modal đánh giá | 1. Truy cập /user/account/orders/[id]<br>2. Click nút Đánh giá<br>3. Kiểm tra modal | Hiển thị Dialog với tiêu đề "Đánh giá sản phẩm" | | Pass | 11/15/2015 | |
| **GUI-DGDH-03** | Kiểm tra tên sản phẩm trong modal | 1. Truy cập /user/account/orders/[id]<br>2. Mở modal đánh giá<br>3. Kiểm tra tên | Hiển thị tên sản phẩm cần đánh giá | | Pass | 11/15/2015 | |
| **GUI-DGDH-04** | Kiểm tra hình ảnh sản phẩm trong modal | 1. Truy cập /user/account/orders/[id]<br>2. Mở modal đánh giá<br>3. Kiểm tra hình ảnh | Hiển thị hình ảnh đại diện của sản phẩm | | Pass | 11/15/2015 | |
| **GUI-DGDH-05** | Kiểm tra đánh giá sao | 1. Truy cập /user/account/orders/[id]<br>2. Mở modal đánh giá<br>3. Kiểm tra sao | Hiển thị component Star Rating với 5 sao, có thể click để chọn 1-5 sao | | Pass | 11/15/2015 | |
| **GUI-DGDH-06** | Kiểm tra textarea nhận xét | 1. Truy cập /user/account/orders/[id]<br>2. Mở modal đánh giá<br>3. Kiểm tra textarea | Hiển thị Textarea với label "Nhận xét về sản phẩm", placeholder, có thể nhập text | | Pass | 11/15/2015 | |
| **GUI-DGDH-07** | Kiểm tra file input upload hình ảnh | 1. Truy cập /user/account/orders/[id]<br>2. Mở modal đánh giá<br>3. Kiểm tra input | Hiển thị File Input với label "Upload hình ảnh", có thể chọn nhiều file ảnh | | Pass | 11/15/2015 | |
| **GUI-DGDH-08** | Kiểm tra nút Gửi đánh giá | 1. Truy cập /user/account/orders/[id]<br>2. Mở modal đánh giá<br>3. Kiểm tra nút | Hiển thị nút "Gửi đánh giá" | | Pass | 11/15/2015 | |
| **GUI-DGDH-09** | Kiểm tra nút Hủy | 1. Truy cập /user/account/orders/[id]<br>2. Mở modal đánh giá<br>3. Kiểm tra nút | Hiển thị nút "Hủy" variant outline | | Pass | 11/15/2015 | |

---

### Check FUNC: Đánh giá đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DGDH-01** | Mở modal đánh giá | 1. Truy cập /user/account/orders/[id]<br>2. Click nút "Đánh giá" | Modal Dialog hiển thị với tên sản phẩm, hình ảnh, đánh giá sao, textarea nhận xét, file input upload, 2 nút (Hủy, Gửi đánh giá) | | Pass | 11/15/2015 | |
| **FUNC-DGDH-02** | Đánh giá sản phẩm thành công | 1. Truy cập /user/account/orders/[id]<br>2. Mở modal đánh giá<br>3. Chọn số sao<br>4. Nhập nhận xét<br>5. Click "Gửi đánh giá" | Hiển thị thông báo "Đánh giá đã được gửi thành công", modal đóng, đánh giá được lưu và hiển thị trên trang sản phẩm | | Untested | 11/15/2015 | |
| **FUNC-DGDH-03** | Đánh giá sản phẩm - Chỉ chọn sao | 1. Truy cập /user/account/orders/[id]<br>2. Mở modal đánh giá<br>3. Chọn số sao<br>4. Để trống nhận xét<br>5. Click "Gửi đánh giá" | Đánh giá được gửi thành công với chỉ số sao, nhận xét có thể để trống | | Pass | 11/15/2015 | |
| **FUNC-DGDH-04** | Đánh giá sản phẩm - Upload hình ảnh | 1. Truy cập /user/account/orders/[id]<br>2. Mở modal đánh giá<br>3. Upload hình ảnh<br>4. Gửi đánh giá<br>5. Kiểm tra kết quả | Hình ảnh được upload thành công, hiển thị preview, đánh giá được lưu kèm hình ảnh | | Pass | 11/15/2015 | |
| **FUNC-DGDH-05** | Đánh giá sản phẩm - Upload nhiều hình ảnh | 1. Truy cập /user/account/orders/[id]<br>2. Mở modal đánh giá<br>3. Upload nhiều hình ảnh<br>4. Gửi đánh giá<br>5. Kiểm tra kết quả | Tất cả hình ảnh được upload thành công, hiển thị preview, đánh giá được lưu kèm tất cả hình ảnh | | Pass | 11/15/2015 | |
| **FUNC-DGDH-06** | Đánh giá sản phẩm - Hủy đánh giá | 1. Truy cập /user/account/orders/[id]<br>2. Mở modal đánh giá<br>3. Click nút "Hủy" | Modal đóng, không gửi đánh giá | | Pass | 11/15/2015 | |
| **FUNC-DGDH-07** | Đánh giá sản phẩm - Đơn chưa giao | 1. Truy cập /user/account/orders/[id]<br>2. Đơn hàng chưa giao<br>3. Kiểm tra nút Đánh giá | Nút "Đánh giá" không hiển thị, không thể đánh giá đơn chưa giao | | Pass | 11/15/2015 | |
| **FUNC-DGDH-08** | Đánh giá nhiều sản phẩm trong đơn | 1. Truy cập /user/account/orders/[id]<br>2. Đơn hàng có nhiều sản phẩm<br>3. Đánh giá từng sản phẩm<br>4. Kiểm tra kết quả | Mỗi sản phẩm có thể được đánh giá riêng, modal hiển thị sản phẩm tương ứng | | Untested | 11/15/2015 | |

---

### Function: Đặt lại đơn hàng

#### Check GUI: Đặt lại đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DLDH-01** | Kiểm tra nút Đặt lại | 1. Truy cập /user/account/orders/[id]<br>2. Đơn hàng có thể đặt lại<br>3. Kiểm tra nút | Hiển thị nút "Đặt lại" variant outline size sm với icon RotateCcw | | Pass | 11/15/2015 | |
| **GUI-DLDH-02** | Kiểm tra modal xác nhận | 1. Truy cập /user/account/orders/[id]<br>2. Click nút Đặt lại<br>3. Kiểm tra modal | Hiển thị Dialog với tiêu đề "Xác nhận đặt lại đơn hàng", thông báo "Bạn có chắc chắn muốn đặt lại đơn hàng này?" | | Pass | 11/15/2015 | |

---

### Check FUNC: Đặt lại đơn hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DLDH-01** | Mở modal đặt lại đơn hàng | 1. Truy cập /user/account/orders/[id]<br>2. Click nút "Đặt lại" | Modal Dialog hiển thị với tiêu đề, thông báo xác nhận, 2 nút (Hủy, Xác nhận) | | Pass | 11/15/2015 | |
| **FUNC-DLDH-02** | Đặt lại đơn hàng thành công | 1. Truy cập /user/account/orders/[id]<br>2. Click nút Đặt lại<br>3. Click "Xác nhận"<br>4. Kiểm tra kết quả | Hiển thị thông báo "Đã thêm sản phẩm vào giỏ hàng", tất cả sản phẩm còn hàng được thêm vào giỏ hàng với số lượng tương ứng, chuyển đến trang /user/cart | | Untested | 11/15/2015 | |
| **FUNC-DLDH-03** | Đặt lại đơn hàng - Sản phẩm hết hàng | 1. Truy cập /user/account/orders/[id]<br>2. Đơn hàng có sản phẩm hết hàng<br>3. Đặt lại đơn hàng<br>4. Kiểm tra kết quả | Hiển thị thông báo về sản phẩm hết hàng, chỉ sản phẩm còn hàng được thêm vào giỏ hàng | | Untested | 11/15/2015 | |
| **FUNC-DLDH-04** | Đặt lại đơn hàng - Hủy đặt lại | 1. Truy cập /user/account/orders/[id]<br>2. Mở modal đặt lại<br>3. Click nút "Hủy" | Modal đóng, không đặt lại đơn hàng | | Pass | 11/15/2015 | |
| **FUNC-DLDH-05** | Đặt lại đơn hàng - Đơn đang xử lý | 1. Truy cập /user/account/orders/[id]<br>2. Đơn hàng đang xử lý<br>3. Kiểm tra nút Đặt lại | Nút "Đặt lại" không hiển thị hoặc bị disabled, không thể đặt lại đơn đang xử lý | | Pass | 11/15/2015 | |

---

### Function: Yêu cầu đổi/trả hàng

#### Check GUI: Yêu cầu đổi/trả hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-YCDTH-01** | Kiểm tra nút Yêu cầu đổi/trả | 1. Truy cập /user/account/orders/[id]<br>2. Đơn hàng đã giao<br>3. Kiểm tra nút | Hiển thị nút "Yêu cầu đổi/trả hàng" variant outline size sm với icon RotateCcw, chỉ hiển thị khi đơn đã giao | | Pass | 11/15/2015 | |
| **GUI-YCDTH-02** | Kiểm tra modal yêu cầu | 1. Truy cập /user/account/orders/[id]<br>2. Click nút Yêu cầu đổi/trả<br>3. Kiểm tra modal | Hiển thị Dialog với tiêu đề "Yêu cầu đổi/trả hàng" | | Pass | 11/15/2015 | |
| **GUI-YCDTH-03** | Kiểm tra dropdown loại yêu cầu | 1. Truy cập /user/account/orders/[id]<br>2. Mở modal yêu cầu<br>3. Kiểm tra dropdown | Hiển thị Select với các option: Đổi hàng, Trả hàng | | Pass | 11/15/2015 | |
| **GUI-YCDTH-04** | Kiểm tra dropdown sản phẩm | 1. Truy cập /user/account/orders/[id]<br>2. Mở modal yêu cầu<br>3. Kiểm tra dropdown | Hiển thị Select với label "Chọn sản phẩm cần đổi/trả", các option là sản phẩm trong đơn hàng | | Pass | 11/15/2015 | |
| **GUI-YCDTH-05** | Kiểm tra dropdown lý do | 1. Truy cập /user/account/orders/[id]<br>2. Mở modal yêu cầu<br>3. Kiểm tra dropdown | Hiển thị Select với label "Lý do đổi/trả hàng", các option: Sản phẩm lỗi, Không đúng mô tả, Không vừa, Lý do khác | | Pass | 11/15/2015 | |
| **GUI-YCDTH-06** | Kiểm tra textarea mô tả chi tiết | 1. Truy cập /user/account/orders/[id]<br>2. Mở modal yêu cầu<br>3. Kiểm tra textarea | Hiển thị Textarea với label "Mô tả chi tiết về vấn đề", placeholder, có thể nhập text | | Pass | 11/15/2015 | |
| **GUI-YCDTH-07** | Kiểm tra file input upload hình ảnh | 1. Truy cập /user/account/orders/[id]<br>2. Mở modal yêu cầu<br>3. Kiểm tra input | Hiển thị File Input với label "Upload hình ảnh minh chứng", có thể chọn nhiều file ảnh | | Pass | 11/15/2015 | |
| **GUI-YCDTH-08** | Kiểm tra nút Gửi yêu cầu | 1. Truy cập /user/account/orders/[id]<br>2. Mở modal yêu cầu<br>3. Kiểm tra nút | Hiển thị nút "Gửi yêu cầu" | | Pass | 11/15/2015 | |
| **GUI-YCDTH-09** | Kiểm tra nút Hủy | 1. Truy cập /user/account/orders/[id]<br>2. Mở modal yêu cầu<br>3. Kiểm tra nút | Hiển thị nút "Hủy" variant outline | | Pass | 11/15/2015 | |

---

### Check FUNC: Yêu cầu đổi/trả hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-YCDTH-01** | Mở modal yêu cầu đổi/trả | 1. Truy cập /user/account/orders/[id]<br>2. Click nút "Yêu cầu đổi/trả hàng" | Modal Dialog hiển thị với dropdown loại yêu cầu, dropdown sản phẩm, dropdown lý do, textarea mô tả, file input upload, 2 nút (Hủy, Gửi yêu cầu) | | Pass | 11/15/2015 | |
| **FUNC-YCDTH-02** | Gửi yêu cầu đổi hàng thành công | 1. Truy cập /user/account/orders/[id]<br>2. Mở modal yêu cầu<br>3. Chọn "Đổi hàng"<br>4. Chọn sản phẩm<br>5. Chọn lý do<br>6. Nhập mô tả<br>7. Click "Gửi yêu cầu" | Hiển thị thông báo "Yêu cầu đã được gửi thành công", modal đóng, yêu cầu được gửi đến admin | | Untested | 11/15/2015 | |
| **FUNC-YCDTH-03** | Gửi yêu cầu trả hàng thành công | 1. Truy cập /user/account/orders/[id]<br>2. Mở modal yêu cầu<br>3. Chọn "Trả hàng"<br>4. Chọn sản phẩm<br>5. Chọn lý do<br>6. Nhập mô tả<br>7. Click "Gửi yêu cầu" | Hiển thị thông báo "Yêu cầu đã được gửi thành công", modal đóng, yêu cầu được gửi đến admin | | Untested | 11/15/2015 | |
| **FUNC-YCDTH-04** | Gửi yêu cầu - Upload hình ảnh minh chứng | 1. Truy cập /user/account/orders/[id]<br>2. Mở modal yêu cầu<br>3. Upload hình ảnh<br>4. Gửi yêu cầu<br>5. Kiểm tra kết quả | Hình ảnh được upload thành công, hiển thị preview, yêu cầu được gửi kèm hình ảnh | | Pass | 11/15/2015 | |
| **FUNC-YCDTH-05** | Gửi yêu cầu - Thiếu thông tin | 1. Truy cập /user/account/orders/[id]<br>2. Mở modal yêu cầu<br>3. Để trống một số trường bắt buộc<br>4. Click "Gửi yêu cầu" | Hiển thị cảnh báo về trường bắt buộc, không gửi yêu cầu | | Pass | 11/15/2015 | |
| **FUNC-YCDTH-06** | Gửi yêu cầu - Hủy yêu cầu | 1. Truy cập /user/account/orders/[id]<br>2. Mở modal yêu cầu<br>3. Click nút "Hủy" | Modal đóng, không gửi yêu cầu | | Pass | 11/15/2015 | |
| **FUNC-YCDTH-07** | Gửi yêu cầu - Đơn chưa giao | 1. Truy cập /user/account/orders/[id]<br>2. Đơn hàng chưa giao<br>3. Kiểm tra nút Yêu cầu đổi/trả | Nút "Yêu cầu đổi/trả hàng" không hiển thị, không thể gửi yêu cầu cho đơn chưa giao | | Pass | 11/15/2015 | |

---

### Function: Xem timeline vận chuyển

#### Check GUI: Xem timeline vận chuyển

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XTLVC-01** | Kiểm tra card Timeline vận chuyển | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra card | Hiển thị card với tiêu đề "Timeline vận chuyển", mô tả "Các mốc cập nhật gần đây" | | Pass | 11/15/2015 | |
| **GUI-XTLVC-02** | Kiểm tra các mốc timeline | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra timeline | Hiển thị danh sách các mốc với thời gian và mô tả, sắp xếp theo thời gian mới nhất trước | | Pass | 11/15/2015 | |

---

### Check FUNC: Xem timeline vận chuyển

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XTLVC-01** | Hiển thị timeline vận chuyển | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra timeline | Hiển thị timeline các mốc: Đơn hàng đang giao, Đơn hàng đã rời kho, Đơn hàng đã đến kho trung chuyển, với thời gian cụ thể | | Pass | 11/15/2015 | |
| **FUNC-XTLVC-02** | Cập nhật timeline real-time | 1. Truy cập /user/orders/track/[id]<br>2. Trạng thái đơn hàng thay đổi<br>3. Kiểm tra timeline | Timeline được cập nhật với mốc mới, hiển thị thời gian và mô tả | | Untested | 11/15/2015 | |
| **FUNC-XTLVC-03** | Sắp xếp timeline theo thời gian | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra thứ tự | Timeline được sắp xếp theo thời gian, mốc mới nhất ở trên cùng | | Pass | 11/15/2015 | |

---

### Function: Xem thông tin thanh toán

#### Check GUI: Xem thông tin thanh toán

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XTTTT-01** | Kiểm tra card Thông tin thanh toán | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra card | Hiển thị card với tiêu đề "Thông tin thanh toán", mô tả "Chi tiết thanh toán" | | Pass | 11/15/2015 | |
| **GUI-XTTTT-02** | Kiểm tra phương thức thanh toán | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra phương thức | Hiển thị "Phương thức: [Phương thức]" (COD, Banking, E-wallet) | | Pass | 11/15/2015 | |
| **GUI-XTTTT-03** | Kiểm tra trạng thái thanh toán | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra trạng thái | Hiển thị "Trạng thái: [Trạng thái]" (Đã thanh toán, Chưa thanh toán, Đã hoàn tiền, Hoàn tiền một phần) | | Pass | 11/15/2015 | |
| **GUI-XTTTT-04** | Kiểm tra mã giao dịch | 1. Truy cập /user/orders/track/[id]<br>2. Đơn hàng đã thanh toán<br>3. Kiểm tra mã | Hiển thị "Mã giao dịch: [Mã]" (nếu có) | | Pass | 11/15/2015 | |

---

### Check FUNC: Xem thông tin thanh toán

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XTTTT-01** | Hiển thị thông tin thanh toán | 1. Truy cập /user/orders/track/[id]<br>2. Kiểm tra thông tin | Hiển thị đầy đủ: Phương thức thanh toán, Trạng thái thanh toán, Mã giao dịch (nếu có) | | Pass | 11/15/2015 | |
| **FUNC-XTTTT-02** | Hiển thị thông tin thanh toán trong chi tiết đơn hàng | 1. Truy cập /user/account/orders/[id]<br>2. Kiểm tra card Thông tin thanh toán | Hiển thị đầy đủ: Phương thức thanh toán, Trạng thái thanh toán, Mã giao dịch, Số tiền thanh toán | | Pass | 11/15/2015 | |
| **FUNC-XTTTT-03** | Hiển thị trạng thái hoàn tiền | 1. Truy cập /user/account/orders/[id]<br>2. Đơn hàng đã hủy và hoàn tiền<br>3. Kiểm tra trạng thái | Hiển thị trạng thái "Đã hoàn tiền" hoặc "Hoàn tiền một phần" với thông tin chi tiết | | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn Markdown để dễ dàng quản lý và cập nhật test cases.*

