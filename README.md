# Test Case Template - Cài đặt hệ thống (Admin)

## Module Code
**Giao lộ 19: Họcl6c (Admin)**

## Test Requirement
1. Cài đặt thông tin cửa hàng
2. Cài đặt thông báo hệ thống
3. Cài đặt bảo mật
4. Cài đặt tích hợp
5. Cài đặt sao lưu
6. Cài đặt chính sách giảm giá
7. Cài đặt thanh toán

---

## Test Summary

### Người lớp Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 30 |
| **Fail** | 0 |
| **Untested** | 0 |
| **N/A** | 0 |
| **Number of Test cases** | 30 |

---

## Test Cases

### Function: Cài đặt thông tin cửa hàng

#### Check GUI: Cài đặt thông tin cửa hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-TTCH-01** | Kiểm tra tiêu đề trang | 1. Đăng nhập Admin<br>2. Truy cập /admin/settings<br>3. Kiểm tra tiêu đề | Hiển thị tiêu đề "Cài đặt hệ thống" với class text-3xl font-bold, mô tả "Quản lý cài đặt và cấu hình hệ thống" với class text-muted-foreground, nằm trong div flex items-center justify-between | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-TTCH-02** | Kiểm tra nút Lưu tất cả | 1. Đăng nhập Admin<br>2. Truy cập /admin/settings<br>3. Kiểm tra nút | Hiển thị Button "Lưu tất cả" bên phải tiêu đề với icon Save h-4 w-4 mr-2 | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-TTCH-03** | Kiểm tra Tabs | 1. Đăng nhập Admin<br>2. Truy cập /admin/settings<br>3. Kiểm tra tabs | Hiển thị Tabs defaultValue="general" với TabsList className="grid w-full grid-cols-6" có 6 TabsTrigger: "Chung", "Cửa hàng", "Thanh toán", "Vận chuyển", "Thông báo", "Bảo mật" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-TTCH-04** | Kiểm tra Tab Cửa hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/settings<br>3. Click tab "Cửa hàng" | Hiển thị TabsContent value="store" với Card "Thông tin cửa hàng" có CardTitle với icon Store h-5 w-5, CardDescription "Cập nhật thông tin liên hệ và địa chỉ cửa hàng", CardContent có grid grid-cols-2 gap-4 với các Input: Tên cửa hàng, Tên chủ cửa hàng, Địa chỉ (Textarea rows={2}), Số điện thoại, Email, Website | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Cài đặt thông tin cửa hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TTCH-01** | Cập nhật thông tin cửa hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/settings<br>3. Click tab "Cửa hàng"<br>4. Cập nhật thông tin (Tên cửa hàng, Địa chỉ, Số điện thoại, Email, Website)<br>5. Click nút "Lưu tất cả" | Thông tin cửa hàng được cập nhật thành công, hiển thị thông báo thành công (toast success), cài đặt được lưu vào hệ thống, thông tin mới được hiển thị trên các trang công khai (nếu có), form vẫn giữ giá trị đã cập nhật | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TTCH-02** | Cập nhật với email không hợp lệ | 1. Đăng nhập Admin<br>2. Truy cập /admin/settings<br>3. Click tab "Cửa hàng"<br>4. Nhập email không hợp lệ (VD: "invalid-email")<br>5. Click nút "Lưu tất cả" | Trình duyệt hiển thị cảnh báo "Please enter a valid email address" hoặc validation message, form không được gửi, không cập nhật thông tin | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TTCH-03** | Upload logo cửa hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/settings<br>3. Click tab "Cửa hàng"<br>4. Click nút "Upload logo" hoặc chọn file từ File input<br>5. Chọn file ảnh (JPG, PNG, GIF)<br>6. Click "Lưu tất cả" | Logo được upload thành công, hiển thị thông báo thành công (toast success), ảnh được resize về kích thước phù hợp (nếu cần), logo hiển thị trên giao diện (preview), logo được lưu vào hệ thống, logo hiển thị trên các trang công khai (nếu có) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TTCH-04** | Upload logo với file không hợp lệ | 1. Đăng nhập Admin<br>2. Truy cập /admin/settings<br>3. Click tab "Cửa hàng"<br>4. Chọn file không phải ảnh (VD: .pdf, .doc)<br>5. Click "Lưu tất cả" | Hiển thị thông báo lỗi "Chỉ chấp nhận file ảnh (JPG, PNG, GIF)" (toast error), không upload logo, file không được chọn | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Cài đặt thông báo hệ thống

#### Check GUI: Cài đặt thông báo hệ thống

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-TBHT-01** | Kiểm tra Tab Thông báo | 1. Đăng nhập Admin<br>2. Truy cập /admin/settings<br>3. Click tab "Thông báo" | Hiển thị TabsContent value="notifications" với Card "Cài đặt thông báo" có CardTitle với icon Bell h-5 w-5, CardDescription "Quản lý các loại thông báo hệ thống", CardContent có các Switch: "Thông báo đơn hàng mới" (defaultChecked), "Thông báo sắp hết hàng" (defaultChecked), "Thông báo phản hồi khách hàng" (defaultChecked), "Thông báo email" (defaultChecked), "Thông báo SMS" (không checked), mỗi Switch có Label và text-sm text-muted-foreground mô tả, có Separator giữa các mục | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Cài đặt thông báo hệ thống

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TBHT-01** | Bật/tắt thông báo đơn hàng mới | 1. Đăng nhập Admin<br>2. Truy cập /admin/settings<br>3. Click tab "Thông báo"<br>4. Toggle Switch "Thông báo đơn hàng mới"<br>5. Click nút "Lưu tất cả" | Trạng thái Switch được cập nhật (bật/tắt), hiển thị thông báo thành công (toast success), cài đặt được lưu vào hệ thống, hệ thống sẽ gửi/không gửi thông báo khi có đơn hàng mới tùy theo trạng thái Switch | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TBHT-02** | Bật/tắt thông báo sắp hết hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/settings<br>3. Click tab "Thông báo"<br>4. Toggle Switch "Thông báo sắp hết hàng"<br>5. Click nút "Lưu tất cả" | Trạng thái Switch được cập nhật, hiển thị thông báo thành công, cài đặt được lưu, hệ thống sẽ gửi/không gửi cảnh báo khi sản phẩm sắp hết hàng | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TBHT-03** | Bật/tắt thông báo email | 1. Đăng nhập Admin<br>2. Truy cập /admin/settings<br>3. Click tab "Thông báo"<br>4. Toggle Switch "Thông báo email"<br>5. Click nút "Lưu tất cả" | Trạng thái Switch được cập nhật, hiển thị thông báo thành công, cài đặt được lưu, hệ thống sẽ gửi/không gửi thông báo qua email tùy theo trạng thái Switch | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TBHT-04** | Bật/tắt thông báo SMS | 1. Đăng nhập Admin<br>2. Truy cập /admin/settings<br>3. Click tab "Thông báo"<br>4. Toggle Switch "Thông báo SMS"<br>5. Click nút "Lưu tất cả" | Trạng thái Switch được cập nhật, hiển thị thông báo thành công, cài đặt được lưu, hệ thống sẽ gửi/không gửi thông báo qua SMS tùy theo trạng thái Switch | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Cài đặt bảo mật

#### Check GUI: Cài đặt bảo mật

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-BM-01** | Kiểm tra Tab Bảo mật | 1. Đăng nhập Admin<br>2. Truy cập /admin/settings<br>3. Click tab "Bảo mật" | Hiển thị TabsContent value="security" với Card "Cài đặt bảo mật" có CardTitle với icon Shield h-5 w-5, CardDescription "Cấu hình các tùy chọn bảo mật hệ thống", CardContent có các Switch: "Xác thực 2 yếu tố (2FA)" (không checked), "Giới hạn đăng nhập" (defaultChecked), "Phiên đăng nhập hết hạn" (defaultChecked), Input type="number" "Thời gian hết hạn phiên (phút)" defaultValue="30", mỗi Switch có Label và text-sm text-muted-foreground mô tả, có Separator giữa các mục | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Cài đặt bảo mật

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-BM-01** | Bật xác thực 2 yếu tố (2FA) | 1. Đăng nhập Admin<br>2. Truy cập /admin/settings<br>3. Click tab "Bảo mật"<br>4. Toggle Switch "Xác thực 2 yếu tố (2FA)" sang ON<br>5. Click nút "Lưu tất cả" | Trạng thái Switch được cập nhật thành ON, hiển thị thông báo thành công (toast success), cài đặt được lưu vào hệ thống, có thể hiển thị Dialog hướng dẫn thiết lập 2FA (quét QR code, nhập mã xác thực), sau khi lưu, lần đăng nhập tiếp theo sẽ yêu cầu mã 2FA | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-BM-02** | Bật giới hạn đăng nhập | 1. Đăng nhập Admin<br>2. Truy cập /admin/settings<br>3. Click tab "Bảo mật"<br>4. Toggle Switch "Giới hạn đăng nhập" sang ON<br>5. Click nút "Lưu tất cả" | Trạng thái Switch được cập nhật thành ON, hiển thị thông báo thành công, cài đặt được lưu, hệ thống sẽ khóa tài khoản sau 5 lần đăng nhập sai | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-BM-03** | Cài đặt thời gian hết hạn phiên | 1. Đăng nhập Admin<br>2. Truy cập /admin/settings<br>3. Click tab "Bảo mật"<br>4. Nhập thời gian hết hạn phiên (VD: 60 phút) vào Input<br>5. Click nút "Lưu tất cả" | Thời gian hết hạn phiên được cập nhật thành công, hiển thị thông báo thành công, cài đặt được lưu, hệ thống sẽ tự động đăng xuất sau thời gian không hoạt động đã cài đặt | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-BM-04** | Cài đặt thời gian hết hạn phiên với giá trị không hợp lệ | 1. Đăng nhập Admin<br>2. Truy cập /admin/settings<br>3. Click tab "Bảo mật"<br>4. Nhập thời gian < 1 hoặc > 1440 phút<br>5. Click nút "Lưu tất cả" | Hiển thị thông báo lỗi "Thời gian hết hạn phiên phải từ 1 đến 1440 phút" (toast error), không cập nhật, giá trị vẫn giữ nguyên | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Cài đặt tích hợp

#### Check GUI: Cài đặt tích hợp

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-TH-01** | Kiểm tra Tab Thanh toán | 1. Đăng nhập Admin<br>2. Truy cập /admin/settings<br>3. Click tab "Thanh toán" | Hiển thị TabsContent value="payment" với Card "Cài đặt thanh toán" có CardTitle với icon CreditCard h-5 w-5, CardDescription "Cấu hình các phương thức thanh toán", CardContent có các Switch: "Thanh toán khi nhận hàng (COD)" (defaultChecked), "Chuyển khoản ngân hàng" (defaultChecked), "Ví điện tử" (không checked), "Thẻ tín dụng" (không checked), mỗi Switch có Label và text-sm text-muted-foreground mô tả, có Separator giữa các mục | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-TH-02** | Kiểm tra Tab Vận chuyển | 1. Đăng nhập Admin<br>2. Truy cập /admin/settings<br>3. Click tab "Vận chuyển" | Hiển thị TabsContent value="shipping" với Card "Cài đặt vận chuyển" có CardTitle với icon Truck h-5 w-5, CardDescription "Cấu hình phí vận chuyển và phương thức giao hàng", CardContent có Switch "Miễn phí vận chuyển" (defaultChecked), Input "Ngưỡng miễn phí vận chuyển (VNĐ)" type="number" defaultValue="500000", Input "Phí vận chuyển mặc định (VNĐ)" type="number" defaultValue="30000", các Switch phương thức giao hàng: "Giao hàng tiêu chuẩn (5-7 ngày)" (defaultChecked), "Giao hàng nhanh (2-3 ngày)" (defaultChecked), "Giao hàng trong ngày (TP.HCM)" (không checked) | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Cài đặt tích hợp

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TH-01** | Bật/tắt phương thức thanh toán COD | 1. Đăng nhập Admin<br>2. Truy cập /admin/settings<br>3. Click tab "Thanh toán"<br>4. Toggle Switch "Thanh toán khi nhận hàng (COD)"<br>5. Click nút "Lưu tất cả" | Trạng thái Switch được cập nhật, hiển thị thông báo thành công (toast success), cài đặt được lưu, phương thức thanh toán COD sẽ hiển thị/không hiển thị trong danh sách phương thức thanh toán khi khách hàng đặt hàng tùy theo trạng thái Switch | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TH-02** | Bật/tắt phương thức thanh toán ví điện tử | 1. Đăng nhập Admin<br>2. Truy cập /admin/settings<br>3. Click tab "Thanh toán"<br>4. Toggle Switch "Ví điện tử" sang ON<br>5. Click nút "Lưu tất cả" | Trạng thái Switch được cập nhật thành ON, hiển thị thông báo thành công, cài đặt được lưu, có thể hiển thị form cấu hình API (API Key, API Secret) cho các ví điện tử (MoMo, ZaloPay, VNPay), phương thức thanh toán ví điện tử sẽ hiển thị trong danh sách khi khách hàng đặt hàng | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TH-03** | Cài đặt miễn phí vận chuyển | 1. Đăng nhập Admin<br>2. Truy cập /admin/settings<br>3. Click tab "Vận chuyển"<br>4. Toggle Switch "Miễn phí vận chuyển" sang ON<br>5. Nhập ngưỡng miễn phí vận chuyển (VD: 500000 VNĐ)<br>6. Click nút "Lưu tất cả" | Trạng thái Switch được cập nhật thành ON, ngưỡng miễn phí vận chuyển được cập nhật, hiển thị thông báo thành công, cài đặt được lưu, hệ thống sẽ tự động miễn phí vận chuyển cho đơn hàng có tổng giá trị >= ngưỡng đã cài đặt | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TH-04** | Cài đặt phí vận chuyển mặc định | 1. Đăng nhập Admin<br>2. Truy cập /admin/settings<br>3. Click tab "Vận chuyển"<br>4. Nhập phí vận chuyển mặc định (VD: 30000 VNĐ) vào Input<br>5. Click nút "Lưu tất cả" | Phí vận chuyển mặc định được cập nhật thành công, hiển thị thông báo thành công, cài đặt được lưu, phí vận chuyển này sẽ được áp dụng cho các đơn hàng không đủ điều kiện miễn phí vận chuyển | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TH-05** | Bật/tắt phương thức giao hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/settings<br>3. Click tab "Vận chuyển"<br>4. Toggle Switch "Giao hàng trong ngày (TP.HCM)" sang ON<br>5. Click nút "Lưu tất cả" | Trạng thái Switch được cập nhật thành ON, hiển thị thông báo thành công, cài đặt được lưu, phương thức giao hàng "Giao hàng trong ngày" sẽ hiển thị trong danh sách phương thức giao hàng khi khách hàng đặt hàng (chỉ cho địa chỉ TP.HCM) | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Cài đặt sao lưu

#### Check FUNC: Cài đặt sao lưu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-SL-01** | Cài đặt sao lưu tự động | 1. Đăng nhập Admin<br>2. Truy cập /admin/settings/backup<br>3. Thiết lập tần suất (VD: Hàng ngày), thời gian (VD: 02:00), nơi lưu trữ (VD: Cloud Storage)<br>4. Click "Lưu" | Hiển thị form cài đặt sao lưu với Select "Tần suất" (Hàng ngày, Hàng tuần, Hàng tháng), Input type="time" "Thời gian", Select "Nơi lưu trữ" (Local, Cloud Storage). Sau khi lưu: sao lưu tự động được cài đặt thành công, hiển thị thông báo thành công (toast success), hệ thống sẽ tự động tạo sao lưu theo lịch đã cài đặt | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-SL-02** | Tạo sao lưu thủ công | 1. Đăng nhập Admin<br>2. Truy cập /admin/settings/backup<br>3. Click nút "Tạo sao lưu"<br>4. Chờ quá trình sao lưu hoàn tất | Hiển thị Dialog hoặc progress bar "Đang tạo sao lưu...", sau khi hoàn tất: sao lưu thủ công được tạo thành công, hiển thị thông báo thành công (toast success), file sao lưu được lưu trữ với tên chứa ngày tháng (VD: "backup_2024-01-20.sql"), file sao lưu hiển thị trong danh sách sao lưu, có thể tải xuống | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-SL-03** | Khôi phục từ sao lưu | 1. Đăng nhập Admin<br>2. Truy cập /admin/settings/backup<br>3. Chọn file sao lưu từ danh sách<br>4. Click nút "Khôi phục"<br>5. Xác nhận trong Dialog | Hiển thị Dialog xác nhận "Bạn có chắc chắn muốn khôi phục từ file sao lưu này? Tất cả dữ liệu hiện tại sẽ bị thay thế." với nút "Hủy" và "Xác nhận khôi phục" variant="destructive". Sau khi xác nhận: hiển thị progress bar "Đang khôi phục...", sau khi hoàn tất: hệ thống được khôi phục thành công, hiển thị thông báo thành công (toast success), dữ liệu được khôi phục đầy đủ, có thể yêu cầu đăng nhập lại | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Cài đặt chính sách giảm giá

#### Check FUNC: Cài đặt chính sách giảm giá

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-GG-01** | Cài đặt giảm giá toàn cửa hàng | 1. Đăng nhập Admin<br>2. Truy cập /admin/settings/discounts<br>3. Thiết lập giảm giá (VD: 10% cho tất cả sản phẩm trong tháng 12)<br>4. Nhập thời gian áp dụng<br>5. Click "Lưu" | Hiển thị form cài đặt giảm giá với Input "Phần trăm giảm giá" type="number", Input "Số tiền giảm giá" type="number", Input type="date" "Ngày bắt đầu", Input type="date" "Ngày kết thúc", Switch "Áp dụng cho tất cả sản phẩm". Sau khi lưu: chính sách giảm giá toàn cửa hàng được cài đặt thành công, hiển thị thông báo thành công (toast success), giảm giá được áp dụng tự động cho tất cả sản phẩm trong thời gian đã cài đặt | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-GG-02** | Cài đặt giảm giá theo sản phẩm | 1. Đăng nhập Admin<br>2. Truy cập /admin/settings/discounts<br>3. Chọn sản phẩm từ Select hoặc danh sách<br>4. Thiết lập giảm giá (VD: 15% cho sản phẩm cụ thể)<br>5. Nhập thời gian áp dụng<br>6. Click "Lưu" | Hiển thị form với Select "Chọn sản phẩm" (có thể tìm kiếm), Input "Phần trăm giảm giá" hoặc "Số tiền giảm giá", Input type="date" cho thời gian. Sau khi lưu: chính sách giảm giá theo sản phẩm được cài đặt thành công, hiển thị thông báo thành công, giảm giá được áp dụng cho sản phẩm đã chọn trong thời gian đã cài đặt | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Cài đặt thanh toán

#### Check FUNC: Cài đặt thanh toán

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TT-01** | Bật/tắt phương thức thanh toán | 1. Đăng nhập Admin<br>2. Truy cập /admin/settings<br>3. Click tab "Thanh toán"<br>4. Toggle Switch cho một phương thức thanh toán (VD: "Thẻ tín dụng")<br>5. Click nút "Lưu tất cả" | Trạng thái Switch được cập nhật, hiển thị thông báo thành công (toast success), cài đặt được lưu, phương thức thanh toán sẽ hiển thị/không hiển thị trong danh sách phương thức thanh toán khi khách hàng đặt hàng tùy theo trạng thái Switch, nếu bật có thể hiển thị form cấu hình API (API Key, API Secret, Test Mode) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TT-02** | Cấu hình API thanh toán | 1. Đăng nhập Admin<br>2. Truy cập /admin/settings<br>3. Click tab "Thanh toán"<br>4. Bật Switch "Ví điện tử" hoặc "Thẻ tín dụng"<br>5. Nhập API Key và API Secret vào các Input<br>6. Click nút "Lưu tất cả" | Hiển thị form cấu hình với Input "API Key" type="password", Input "API Secret" type="password", Switch "Test Mode" (nếu có), nút "Test kết nối". Sau khi lưu: API thanh toán được cấu hình thành công, hiển thị thông báo thành công, cài đặt được lưu, có thể test kết nối để xác minh API hoạt động | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TT-03** | Test kết nối API thanh toán | 1. Đăng nhập Admin<br>2. Truy cập /admin/settings<br>3. Click tab "Thanh toán"<br>4. Nhập API Key và API Secret<br>5. Click nút "Test kết nối" | Hiển thị progress "Đang kiểm tra kết nối...", sau khi hoàn tất: nếu thành công hiển thị thông báo "Kết nối API thành công" (toast success), nếu thất bại hiển thị thông báo lỗi "Không thể kết nối API. Vui lòng kiểm tra lại API Key và API Secret" (toast error) | FUNC-DN-02 | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn MDX để dễ dàng quản lý và cập nhật test cases.*
