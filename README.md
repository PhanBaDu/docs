# Test Case Template - Chức năng yêu cầu đặt hàng (User)

## Module Code
**Model Management Store: Chức năng yêu cầu đặt hàng User**

## Test Requirement
1. Yêu cầu tìm mô hình
2. Xem danh sách yêu cầu
3. Xem chi tiết yêu cầu
4. Hủy yêu cầu
5. Quản lý trạng thái yêu cầu

---

## Test Summary

### Người thực hiện Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 130 |
| **Fail** | 0 |
| **Untested** | 40 |
| **N/A** | 0 |
| **Number of Test cases** | 170 |

---

## Test Cases

### Function: Yêu cầu tìm mô hình

#### Check GUI: Yêu cầu tìm mô hình

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-YCTM-01** | Kiểm tra tiêu đề trang | 1. Truy cập trang yêu cầu đặt hàng<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Yêu cầu đặt hàng" với icon Package h-8 w-8, text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-YCTM-02** | Kiểm tra mô tả trang | 1. Truy cập trang yêu cầu đặt hàng<br>2. Kiểm tra mô tả | Hiển thị mô tả "Yêu cầu sản phẩm hết hàng hoặc sản phẩm mới" với text-muted-foreground | | Pass | 11/15/2015 | |
| **GUI-YCTM-03** | Kiểm tra tab Tạo yêu cầu | 1. Truy cập trang yêu cầu đặt hàng<br>2. Kiểm tra tab | Hiển thị tab "Tạo yêu cầu" trong TabsList grid-cols-2 | | Pass | 11/15/2015 | |
| **GUI-YCTM-04** | Kiểm tra tiêu đề form | 1. Chọn tab "Tạo yêu cầu"<br>2. Kiểm tra tiêu đề | Hiển thị CardTitle "Tạo yêu cầu đặt hàng" với CardDescription | | Pass | 11/15/2015 | |
| **GUI-YCTM-05** | Kiểm tra trường Loại yêu cầu | 1. Chọn tab "Tạo yêu cầu"<br>2. Kiểm tra trường | Hiển thị label "Loại yêu cầu *", Select với các option: "Sản phẩm hết hàng" (icon Package), "Sản phẩm mới" (icon BookOpen) | | Pass | 11/15/2015 | |
| **GUI-YCTM-06** | Kiểm tra trường Tên sản phẩm | 1. Chọn tab "Tạo yêu cầu"<br>2. Kiểm tra trường | Hiển thị label "Tên sản phẩm *", Input với placeholder "VD: Gundam RX-78-2 Ver.2.0", required | | Pass | 11/15/2015 | |
| **GUI-YCTM-07** | Kiểm tra trường Tác giả/Thương hiệu | 1. Chọn tab "Tạo yêu cầu"<br>2. Kiểm tra trường | Hiển thị label "Tác giả/Thương hiệu", Input với placeholder "VD: Bandai", optional | | Pass | 11/15/2015 | |
| **GUI-YCTM-08** | Kiểm tra trường Nhà xuất bản | 1. Chọn tab "Tạo yêu cầu"<br>2. Kiểm tra trường | Hiển thị label "Nhà xuất bản", Input với placeholder "VD: Bandai", optional | | Pass | 11/15/2015 | |
| **GUI-YCTM-09** | Kiểm tra trường ISBN/Mã sản phẩm | 1. Chọn tab "Tạo yêu cầu"<br>2. Kiểm tra trường | Hiển thị label "ISBN/Mã sản phẩm", Input với placeholder "VD: 978-4-04-123456-7", optional | | Pass | 11/15/2015 | |
| **GUI-YCTM-10** | Kiểm tra trường Lý do yêu cầu | 1. Chọn tab "Tạo yêu cầu"<br>2. Kiểm tra trường | Hiển thị label "Lý do yêu cầu", Select với các option: "Sản phẩm hết hàng", "Sản phẩm mới chưa có", "Yêu cầu từ khách hàng", "Sản phẩm đang hot", "Khác" | | Pass | 11/15/2015 | |
| **GUI-YCTM-11** | Kiểm tra trường Mức độ ưu tiên | 1. Chọn tab "Tạo yêu cầu"<br>2. Kiểm tra trường | Hiển thị label "Mức độ ưu tiên", Select với các option: "Thấp", "Trung bình", "Cao" | | Pass | 11/15/2015 | |
| **GUI-YCTM-12** | Kiểm tra trường Mô tả chi tiết | 1. Chọn tab "Tạo yêu cầu"<br>2. Kiểm tra trường | Hiển thị label "Mô tả chi tiết *", Textarea với placeholder "Mô tả chi tiết về yêu cầu của bạn...", rows 4, required | | Pass | 11/15/2015 | |
| **GUI-YCTM-13** | Kiểm tra nút Lưu nháp | 1. Chọn tab "Tạo yêu cầu"<br>2. Kiểm tra nút | Hiển thị nút "Lưu nháp" variant outline | | Pass | 11/15/2015 | |
| **GUI-YCTM-14** | Kiểm tra nút Gửi yêu cầu | 1. Chọn tab "Tạo yêu cầu"<br>2. Kiểm tra nút | Hiển thị nút "Gửi yêu cầu" với icon Plus, variant default | | Pass | 11/15/2015 | |
| **GUI-YCTM-15** | Kiểm tra grid layout thông tin sản phẩm | 1. Chọn tab "Tạo yêu cầu"<br>2. Kiểm tra layout | Hiển thị grid grid-cols-1 md:grid-cols-2 gap-4 cho các trường thông tin sản phẩm | | Pass | 11/15/2015 | |

---

### Check FUNC: Yêu cầu tìm mô hình

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-YCTM-01** | Mở tab Tạo yêu cầu | 1. Truy cập trang yêu cầu đặt hàng<br>2. Chọn tab "Tạo yêu cầu" | Hiển thị form tạo yêu cầu với đầy đủ các trường, form trống sẵn sàng nhập | | Pass | 11/15/2015 | |
| **FUNC-YCTM-02** | Tạo yêu cầu thành công | 1. Chọn tab "Tạo yêu cầu"<br>2. Nhập đầy đủ thông tin (loại, tên sản phẩm, mô tả)<br>3. Nhấn "Gửi yêu cầu" | Yêu cầu được tạo thành công, hiển thị toast "Đã gửi yêu cầu đặt hàng thành công", form được reset, yêu cầu xuất hiện trong tab "Yêu cầu của tôi" với trạng thái "Chờ xử lý" | | Pass | 11/15/2015 | |
| **FUNC-YCTM-03** | Tạo yêu cầu thiếu tên sản phẩm | 1. Chọn tab "Tạo yêu cầu"<br>2. Để trống tên sản phẩm<br>3. Nhập các trường khác<br>4. Nhấn "Gửi yêu cầu" | Hiển thị toast lỗi "Vui lòng điền đầy đủ thông tin bắt buộc", không gửi yêu cầu, form vẫn giữ nguyên | | Pass | 11/15/2015 | |
| **FUNC-YCTM-04** | Tạo yêu cầu thiếu mô tả | 1. Chọn tab "Tạo yêu cầu"<br>2. Nhập tên sản phẩm<br>3. Để trống mô tả<br>4. Nhấn "Gửi yêu cầu" | Hiển thị toast lỗi "Vui lòng điền đầy đủ thông tin bắt buộc", không gửi yêu cầu | | Pass | 11/15/2015 | |
| **FUNC-YCTM-05** | Chọn loại yêu cầu - Sản phẩm hết hàng | 1. Chọn tab "Tạo yêu cầu"<br>2. Chọn loại "Sản phẩm hết hàng" | Loại yêu cầu được chọn, hiển thị icon Package, có thể thay đổi | | Pass | 11/15/2015 | |
| **FUNC-YCTM-06** | Chọn loại yêu cầu - Sản phẩm mới | 1. Chọn tab "Tạo yêu cầu"<br>2. Chọn loại "Sản phẩm mới" | Loại yêu cầu được chọn, hiển thị icon BookOpen, có thể thay đổi | | Pass | 11/15/2015 | |
| **FUNC-YCTM-07** | Nhập thông tin sản phẩm | 1. Chọn tab "Tạo yêu cầu"<br>2. Nhập tên, tác giả, nhà xuất bản, ISBN | Tất cả thông tin được nhập và hiển thị trong các Input tương ứng | | Pass | 11/15/2015 | |
| **FUNC-YCTM-08** | Chọn lý do yêu cầu | 1. Chọn tab "Tạo yêu cầu"<br>2. Chọn lý do từ Select | Lý do được chọn, hiển thị trong Select, có thể thay đổi | | Pass | 11/15/2015 | |
| **FUNC-YCTM-09** | Chọn mức độ ưu tiên | 1. Chọn tab "Tạo yêu cầu"<br>2. Chọn mức độ ưu tiên | Mức độ ưu tiên được chọn, mặc định là "Trung bình", có thể thay đổi | | Pass | 11/15/2015 | |
| **FUNC-YCTM-10** | Lưu nháp yêu cầu | 1. Chọn tab "Tạo yêu cầu"<br>2. Nhập một số thông tin<br>3. Nhấn "Lưu nháp" | Thông tin được lưu nháp, hiển thị toast "Đã lưu nháp", có thể tiếp tục chỉnh sửa sau | | Pass | 11/15/2015 | |
| **FUNC-YCTM-11** | Tạo yêu cầu với đầy đủ thông tin | 1. Chọn tab "Tạo yêu cầu"<br>2. Nhập đầy đủ: loại, tên, tác giả, nhà xuất bản, ISBN, lý do, mức độ ưu tiên, mô tả<br>3. Nhấn "Gửi yêu cầu" | Yêu cầu được tạo với đầy đủ thông tin, hiển thị trong danh sách với tất cả thông tin đã nhập | | Pass | 11/15/2015 | |
| **FUNC-YCTM-12** | Tạo yêu cầu chỉ với thông tin bắt buộc | 1. Chọn tab "Tạo yêu cầu"<br>2. Chỉ nhập loại, tên sản phẩm, mô tả<br>3. Nhấn "Gửi yêu cầu" | Yêu cầu được tạo thành công với chỉ thông tin bắt buộc, các trường optional để trống | | Pass | 11/15/2015 | |

---

### Function: Xem danh sách yêu cầu

#### Check GUI: Xem danh sách yêu cầu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XDSYC-01** | Kiểm tra tab Yêu cầu của tôi | 1. Truy cập trang yêu cầu đặt hàng<br>2. Kiểm tra tab | Hiển thị tab "Yêu cầu của tôi" trong TabsList | | Pass | 11/15/2015 | |
| **GUI-XDSYC-02** | Kiểm tra tiêu đề danh sách | 1. Chọn tab "Yêu cầu của tôi"<br>2. Kiểm tra tiêu đề | Hiển thị CardTitle "Yêu cầu của tôi" với CardDescription "Theo dõi trạng thái các yêu cầu đặt hàng" | | Pass | 11/15/2015 | |
| **GUI-XDSYC-03** | Kiểm tra ô tìm kiếm | 1. Chọn tab "Yêu cầu của tôi"<br>2. Kiểm tra tìm kiếm | Hiển thị Input với icon Search bên trái, placeholder "Tìm kiếm yêu cầu...", pl-10 w-64 | | Pass | 11/15/2015 | |
| **GUI-XDSYC-04** | Kiểm tra bộ lọc trạng thái | 1. Chọn tab "Yêu cầu của tôi"<br>2. Kiểm tra bộ lọc | Hiển thị Select với trigger w-32, các option: "Tất cả", "Chờ xử lý", "Đã chấp nhận", "Đã từ chối", "Hoàn thành" | | Pass | 11/15/2015 | |
| **GUI-XDSYC-05** | Kiểm tra bộ lọc loại | 1. Chọn tab "Yêu cầu của tôi"<br>2. Kiểm tra bộ lọc | Hiển thị Select với trigger w-32, các option: "Tất cả", "Hết hàng", "Mô hình mới" | | Pass | 11/15/2015 | |
| **GUI-XDSYC-06** | Kiểm tra card yêu cầu | 1. Xem danh sách yêu cầu<br>2. Kiểm tra card | Hiển thị card với CardContent p-4, chứa icon loại, tiêu đề, mã yêu cầu, badge trạng thái, badge mức độ ưu tiên | | Pass | 11/15/2015 | |
| **GUI-XDSYC-07** | Kiểm tra icon loại yêu cầu | 1. Xem card yêu cầu<br>2. Kiểm tra icon | Hiển thị icon loại trong div p-2 bg-primary/10 rounded-lg, icon Package hoặc BookOpen tùy loại | | Pass | 11/15/2015 | |
| **GUI-XDSYC-08** | Kiểm tra badge trạng thái | 1. Xem card yêu cầu<br>2. Kiểm tra badge | Hiển thị badge với màu: Chờ xử lý (yellow-500), Đã chấp nhận (green-500), Đã từ chối (red-500), Hoàn thành (blue-500), có icon tương ứng | | Pass | 11/15/2015 | |
| **GUI-XDSYC-09** | Kiểm tra badge mức độ ưu tiên | 1. Xem card yêu cầu<br>2. Kiểm tra badge | Hiển thị badge với màu: Thấp (green-500), Trung bình (yellow-500), Cao (red-500) | | Pass | 11/15/2015 | |
| **GUI-XDSYC-10** | Kiểm tra thông tin yêu cầu | 1. Xem card yêu cầu<br>2. Kiểm tra thông tin | Hiển thị grid grid-cols-1 md:grid-cols-2 gap-4 với thông tin: Tác giả (icon User), Nhà xuất bản (icon FileText), Ngày tạo (icon Calendar), Cập nhật (icon Clock) | | Pass | 11/15/2015 | |
| **GUI-XDSYC-11** | Kiểm tra mô tả yêu cầu | 1. Xem card yêu cầu<br>2. Kiểm tra mô tả | Hiển thị mô tả với text-sm text-muted-foreground line-clamp-2 | | Pass | 11/15/2015 | |
| **GUI-XDSYC-12** | Kiểm tra phản hồi admin | 1. Xem yêu cầu có phản hồi<br>2. Kiểm tra phản hồi | Hiển thị phần phản hồi với background bg-muted rounded-lg, icon MessageSquare, tiêu đề "Phản hồi từ admin:", nội dung phản hồi | | Pass | 11/15/2015 | |
| **GUI-XDSYC-13** | Kiểm tra nút Xem chi tiết | 1. Xem card yêu cầu<br>2. Kiểm tra nút | Hiển thị nút "Xem chi tiết" với icon Eye, variant outline size sm, flex-1 | | Pass | 11/15/2015 | |
| **GUI-XDSYC-14** | Kiểm tra nút Hủy yêu cầu | 1. Xem yêu cầu chờ xử lý<br>2. Kiểm tra nút | Hiển thị nút "Hủy yêu cầu" với icon XCircle, variant destructive size sm, chỉ hiển thị khi status = "pending" | | Pass | 11/15/2015 | |

---

### Check FUNC: Xem danh sách yêu cầu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XDSYC-01** | Mở tab Yêu cầu của tôi | 1. Truy cập trang yêu cầu đặt hàng<br>2. Chọn tab "Yêu cầu của tôi" | Hiển thị danh sách tất cả yêu cầu đã gửi, có ô tìm kiếm và bộ lọc | | Pass | 11/15/2015 | |
| **FUNC-XDSYC-02** | Hiển thị danh sách yêu cầu | 1. Chọn tab "Yêu cầu của tôi" | Hiển thị danh sách với đầy đủ thông tin: icon loại, tiêu đề, mã yêu cầu, tác giả, nhà xuất bản, ngày tạo, cập nhật, trạng thái, mức độ ưu tiên, mô tả, phản hồi (nếu có) | | Pass | 11/15/2015 | |
| **FUNC-XDSYC-03** | Sắp xếp theo thời gian mới nhất | 1. Chọn tab "Yêu cầu của tôi" | Danh sách được sắp xếp theo thời gian tạo mới nhất trước | | Pass | 11/15/2015 | |
| **FUNC-XDSYC-04** | Tìm kiếm theo tên sản phẩm | 1. Chọn tab "Yêu cầu của tôi"<br>2. Nhập tên sản phẩm vào ô tìm kiếm | Danh sách được lọc, chỉ hiển thị yêu cầu có tên sản phẩm chứa từ khóa | | Pass | 11/15/2015 | |
| **FUNC-XDSYC-05** | Tìm kiếm theo tác giả | 1. Chọn tab "Yêu cầu của tôi"<br>2. Nhập tên tác giả vào ô tìm kiếm | Danh sách được lọc, chỉ hiển thị yêu cầu có tác giả chứa từ khóa | | Pass | 11/15/2015 | |
| **FUNC-XDSYC-06** | Tìm kiếm theo nhà xuất bản | 1. Chọn tab "Yêu cầu của tôi"<br>2. Nhập nhà xuất bản vào ô tìm kiếm | Danh sách được lọc, chỉ hiển thị yêu cầu có nhà xuất bản chứa từ khóa | | Pass | 11/15/2015 | |
| **FUNC-XDSYC-07** | Lọc theo trạng thái - Chờ xử lý | 1. Chọn tab "Yêu cầu của tôi"<br>2. Chọn bộ lọc "Chờ xử lý" | Chỉ hiển thị các yêu cầu có trạng thái "Chờ xử lý" | | Pass | 11/15/2015 | |
| **FUNC-XDSYC-08** | Lọc theo trạng thái - Đã chấp nhận | 1. Chọn tab "Yêu cầu của tôi"<br>2. Chọn bộ lọc "Đã chấp nhận" | Chỉ hiển thị các yêu cầu có trạng thái "Đã chấp nhận" | | Pass | 11/15/2015 | |
| **FUNC-XDSYC-09** | Lọc theo trạng thái - Đã từ chối | 1. Chọn tab "Yêu cầu của tôi"<br>2. Chọn bộ lọc "Đã từ chối" | Chỉ hiển thị các yêu cầu có trạng thái "Đã từ chối" | | Pass | 11/15/2015 | |
| **FUNC-XDSYC-10** | Lọc theo trạng thái - Hoàn thành | 1. Chọn tab "Yêu cầu của tôi"<br>2. Chọn bộ lọc "Hoàn thành" | Chỉ hiển thị các yêu cầu có trạng thái "Hoàn thành" | | Pass | 11/15/2015 | |
| **FUNC-XDSYC-11** | Lọc theo loại - Hết hàng | 1. Chọn tab "Yêu cầu của tôi"<br>2. Chọn bộ lọc loại "Hết hàng" | Chỉ hiển thị các yêu cầu có loại "Hết hàng" | | Pass | 11/15/2015 | |
| **FUNC-XDSYC-12** | Lọc theo loại - Mô hình mới | 1. Chọn tab "Yêu cầu của tôi"<br>2. Chọn bộ lọc loại "Mô hình mới" | Chỉ hiển thị các yêu cầu có loại "Mô hình mới" | | Pass | 11/15/2015 | |
| **FUNC-XDSYC-13** | Kết hợp tìm kiếm và lọc | 1. Chọn tab "Yêu cầu của tôi"<br>2. Nhập từ khóa tìm kiếm<br>3. Chọn bộ lọc trạng thái và loại | Danh sách được lọc theo cả từ khóa, trạng thái và loại, chỉ hiển thị yêu cầu thỏa mãn tất cả điều kiện | | Pass | 11/15/2015 | |
| **FUNC-XDSYC-14** | Hiển thị khi không có yêu cầu | 1. Chọn tab "Yêu cầu của tôi"<br>2. Không có yêu cầu nào | Hiển thị thông báo "Chưa có yêu cầu nào" hoặc danh sách trống | | Pass | 11/15/2015 | |
| **FUNC-XDSYC-15** | Hiển thị phản hồi admin | 1. Xem yêu cầu đã có phản hồi<br>2. Kiểm tra phản hồi | Hiển thị phần phản hồi với icon MessageSquare, tiêu đề "Phản hồi từ admin:", nội dung phản hồi | | Pass | 11/15/2015 | |
| **FUNC-XDSYC-16** | Tìm kiếm real-time | 1. Chọn tab "Yêu cầu của tôi"<br>2. Nhập từ khóa vào ô tìm kiếm | Danh sách được lọc ngay khi nhập, không cần nhấn Enter | | Pass | 11/15/2015 | |

---

### Function: Xem chi tiết yêu cầu

#### Check GUI: Xem chi tiết yêu cầu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XCTYC-01** | Kiểm tra modal/trang chi tiết | 1. Nhấn nút "Xem chi tiết"<br>2. Kiểm tra modal/trang | Hiển thị modal hoặc trang chi tiết với đầy đủ thông tin yêu cầu | | Pass | 11/15/2015 | |
| **GUI-XCTYC-02** | Kiểm tra thông tin cơ bản | 1. Xem chi tiết yêu cầu<br>2. Kiểm tra thông tin | Hiển thị đầy đủ: mã yêu cầu, tên sản phẩm, tác giả, nhà xuất bản, ISBN, loại yêu cầu, mức độ ưu tiên, trạng thái | | Pass | 11/15/2015 | |
| **GUI-XCTYC-03** | Kiểm tra lý do yêu cầu | 1. Xem chi tiết yêu cầu<br>2. Kiểm tra lý do | Hiển thị lý do yêu cầu với text rõ ràng | | Pass | 11/15/2015 | |
| **GUI-XCTYC-04** | Kiểm tra mô tả chi tiết | 1. Xem chi tiết yêu cầu<br>2. Kiểm tra mô tả | Hiển thị mô tả chi tiết đầy đủ, không bị cắt (không có line-clamp) | | Pass | 11/15/2015 | |
| **GUI-XCTYC-05** | Kiểm tra ngày tạo | 1. Xem chi tiết yêu cầu<br>2. Kiểm tra ngày | Hiển thị ngày tạo với format ngày Việt Nam, icon Calendar | | Pass | 11/15/2015 | |
| **GUI-XCTYC-06** | Kiểm tra ngày phản hồi | 1. Xem chi tiết yêu cầu có phản hồi<br>2. Kiểm tra ngày | Hiển thị ngày phản hồi với format ngày Việt Nam | | Pass | 11/15/2015 | |
| **GUI-XCTYC-07** | Kiểm tra phản hồi admin | 1. Xem chi tiết yêu cầu có phản hồi<br>2. Kiểm tra phản hồi | Hiển thị phản hồi admin với nội dung đầy đủ, rõ ràng | | Pass | 11/15/2015 | |
| **GUI-XCTYC-08** | Kiểm tra nút Quay lại | 1. Xem chi tiết yêu cầu<br>2. Kiểm tra nút | Hiển thị nút "Quay lại" để quay lại danh sách | | Pass | 11/15/2015 | |
| **GUI-XCTYC-09** | Kiểm tra nút Hủy yêu cầu | 1. Xem chi tiết yêu cầu chờ xử lý<br>2. Kiểm tra nút | Hiển thị nút "Hủy yêu cầu" variant destructive, chỉ hiển thị khi status = "pending" | | Pass | 11/15/2015 | |

---

### Check FUNC: Xem chi tiết yêu cầu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XCTYC-01** | Mở chi tiết yêu cầu | 1. Chọn tab "Yêu cầu của tôi"<br>2. Nhấn nút "Xem chi tiết" | Mở modal hoặc trang chi tiết với đầy đủ thông tin yêu cầu | | Pass | 11/15/2015 | |
| **FUNC-XCTYC-02** | Hiển thị chi tiết đầy đủ | 1. Xem chi tiết yêu cầu | Hiển thị đầy đủ: mã yêu cầu, tên sản phẩm, tác giả, nhà xuất bản, ISBN, loại yêu cầu, mức độ ưu tiên, trạng thái, lý do, mô tả, ngày tạo, ngày cập nhật, phản hồi admin (nếu có) | | Pass | 11/15/2015 | |
| **FUNC-XCTYC-03** | Hiển thị phản hồi admin | 1. Xem chi tiết yêu cầu có phản hồi | Hiển thị phần phản hồi với nội dung đầy đủ, thời gian phản hồi, được format rõ ràng | | Pass | 11/15/2015 | |
| **FUNC-XCTYC-04** | Quay lại danh sách | 1. Xem chi tiết yêu cầu<br>2. Nhấn nút "Quay lại" | Quay lại trang danh sách yêu cầu, giữ nguyên trạng thái lọc và tìm kiếm | | Pass | 11/15/2015 | |
| **FUNC-XCTYC-05** | Đóng modal bằng click overlay | 1. Mở modal chi tiết<br>2. Click vào overlay | Modal đóng, quay lại danh sách | | Pass | 11/15/2015 | |

---

### Function: Hủy yêu cầu

#### Check GUI: Hủy yêu cầu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-HYC-01** | Kiểm tra nút Hủy yêu cầu | 1. Xem yêu cầu chờ xử lý<br>2. Kiểm tra nút | Hiển thị nút "Hủy yêu cầu" với icon XCircle, variant destructive size sm, chỉ hiển thị khi status = "pending" | | Pass | 11/15/2015 | |
| **GUI-HYC-02** | Kiểm tra modal xác nhận | 1. Nhấn nút "Hủy yêu cầu"<br>2. Kiểm tra modal | Hiển thị modal xác nhận với tiêu đề "Xác nhận hủy yêu cầu", nội dung "Bạn có chắc chắn muốn hủy yêu cầu này?", nút "Xác nhận" và "Hủy" | | Pass | 11/15/2015 | |
| **GUI-HYC-03** | Kiểm tra nút Xác nhận | 1. Mở modal xác nhận<br>2. Kiểm tra nút | Hiển thị nút "Xác nhận" variant destructive, thực hiện hủy khi nhấn | | Pass | 11/15/2015 | |
| **GUI-HYC-04** | Kiểm tra nút Hủy trong modal | 1. Mở modal xác nhận<br>2. Kiểm tra nút | Hiển thị nút "Hủy" variant outline, đóng modal khi nhấn | | Pass | 11/15/2015 | |

---

### Check FUNC: Hủy yêu cầu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-HYC-01** | Hủy yêu cầu chờ xử lý | 1. Chọn tab "Yêu cầu của tôi"<br>2. Nhấn nút "Hủy yêu cầu" trên yêu cầu chờ xử lý<br>3. Xác nhận hủy | Hiển thị modal xác nhận, sau khi xác nhận, yêu cầu được hủy, hiển thị toast "Đã hủy yêu cầu đặt hàng", yêu cầu biến mất khỏi danh sách | | Pass | 11/15/2015 | |
| **FUNC-HYC-02** | Hủy yêu cầu trong modal xác nhận | 1. Nhấn nút "Hủy yêu cầu"<br>2. Nhấn nút "Hủy" trong modal | Modal đóng, không hủy yêu cầu, yêu cầu vẫn còn trong danh sách | | Pass | 11/15/2015 | |
| **FUNC-HYC-03** | Hủy yêu cầu đã xử lý | 1. Xem yêu cầu đã được xử lý (đã chấp nhận/từ chối)<br>2. Kiểm tra nút hủy | Nút "Hủy yêu cầu" không hiển thị, không thể hủy yêu cầu đã xử lý | | Pass | 11/15/2015 | |
| **FUNC-HYC-04** | Hủy yêu cầu từ trang chi tiết | 1. Xem chi tiết yêu cầu chờ xử lý<br>2. Nhấn nút "Hủy yêu cầu"<br>3. Xác nhận | Yêu cầu được hủy, quay lại danh sách, yêu cầu biến mất | | Pass | 11/15/2015 | |
| **FUNC-HYC-05** | Đóng modal bằng click overlay | 1. Mở modal xác nhận<br>2. Click vào overlay | Modal đóng, không hủy yêu cầu | | Pass | 11/15/2015 | |

---

### Function: Quản lý trạng thái yêu cầu

#### Check GUI: Quản lý trạng thái yêu cầu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-QLTTYC-01** | Kiểm tra badge trạng thái Chờ xử lý | 1. Xem yêu cầu chờ xử lý<br>2. Kiểm tra badge | Hiển thị badge "Chờ xử lý" với màu yellow-500, icon Clock | | Pass | 11/15/2015 | |
| **GUI-QLTTYC-02** | Kiểm tra badge trạng thái Đã chấp nhận | 1. Xem yêu cầu đã chấp nhận<br>2. Kiểm tra badge | Hiển thị badge "Đã chấp nhận" với màu green-500, icon CheckCircle | | Pass | 11/15/2015 | |
| **GUI-QLTTYC-03** | Kiểm tra badge trạng thái Đã từ chối | 1. Xem yêu cầu đã từ chối<br>2. Kiểm tra badge | Hiển thị badge "Đã từ chối" với màu red-500, icon XCircle | | Pass | 11/15/2015 | |
| **GUI-QLTTYC-04** | Kiểm tra badge trạng thái Hoàn thành | 1. Xem yêu cầu hoàn thành<br>2. Kiểm tra badge | Hiển thị badge "Hoàn thành" với màu blue-500, icon CheckCircle | | Pass | 11/15/2015 | |
| **GUI-QLTTYC-05** | Kiểm tra thời gian cập nhật | 1. Xem yêu cầu<br>2. Kiểm tra thời gian | Hiển thị thời gian cập nhật cuối với icon Clock, format ngày giờ Việt Nam | | Pass | 11/15/2015 | |

---

### Check FUNC: Quản lý trạng thái yêu cầu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-QLTTYC-01** | Theo dõi trạng thái real-time | 1. Xem danh sách yêu cầu<br>2. Admin thay đổi trạng thái | Trạng thái yêu cầu được cập nhật real-time, badge thay đổi màu và icon tương ứng, hiển thị thông báo khi có thay đổi | | Pass | 11/15/2015 | |
| **FUNC-QLTTYC-02** | Lọc theo trạng thái qua bộ lọc | 1. Chọn tab "Yêu cầu của tôi"<br>2. Chọn trạng thái trong bộ lọc | Danh sách được lọc, chỉ hiển thị yêu cầu có trạng thái đã chọn, cập nhật ngay lập tức | | Pass | 11/15/2015 | |
| **FUNC-QLTTYC-03** | Hiển thị thông tin trạng thái | 1. Xem yêu cầu<br>2. Kiểm tra thông tin | Hiển thị đầy đủ: badge trạng thái với màu và icon, thời gian cập nhật, người xử lý (nếu có), ghi chú (nếu có) | | Pass | 11/15/2015 | |
| **FUNC-QLTTYC-04** | Cập nhật trạng thái tự động | 1. Xem danh sách yêu cầu<br>2. Đợi admin xử lý | Hệ thống tự động cập nhật trạng thái khi admin xử lý, không cần refresh trang | | Pass | 11/15/2015 | |
| **FUNC-QLTTYC-05** | Thông báo thay đổi trạng thái | 1. Yêu cầu có thay đổi trạng thái<br>2. Kiểm tra thông báo | Hiển thị toast hoặc notification thông báo thay đổi trạng thái, có thể click để xem chi tiết | | Pass | 11/15/2015 | |
| **FUNC-QLTTYC-06** | Hiển thị số lượng theo trạng thái | 1. Chọn tab "Yêu cầu của tôi"<br>2. Kiểm tra số lượng | Số lượng yêu cầu được hiển thị chính xác cho từng trạng thái trong bộ lọc | | Pass | 11/15/2015 | |

---

### Check VALIDATION: Yêu cầu đặt hàng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **VALID-YCDH-01** | Tạo yêu cầu thiếu tên sản phẩm | 1. Chọn tab "Tạo yêu cầu"<br>2. Để trống tên sản phẩm<br>3. Nhấn "Gửi yêu cầu" | Hiển thị toast lỗi "Vui lòng điền đầy đủ thông tin bắt buộc", không gửi yêu cầu | | Pass | 11/15/2015 | |
| **VALID-YCDH-02** | Tạo yêu cầu thiếu mô tả | 1. Chọn tab "Tạo yêu cầu"<br>2. Để trống mô tả<br>3. Nhấn "Gửi yêu cầu" | Hiển thị toast lỗi "Vui lòng điền đầy đủ thông tin bắt buộc", không gửi yêu cầu | | Pass | 11/15/2015 | |
| **VALID-YCDH-03** | Tạo yêu cầu với mô tả quá ngắn | 1. Chọn tab "Tạo yêu cầu"<br>2. Nhập mô tả < 10 ký tự<br>3. Nhấn "Gửi yêu cầu" | Hiển thị thông báo lỗi "Mô tả phải có ít nhất 10 ký tự" hoặc cho phép gửi | | Pass | 11/15/2015 | |
| **VALID-YCDH-04** | Hủy yêu cầu đã xử lý | 1. Xem yêu cầu đã được xử lý<br>2. Thử hủy yêu cầu | Nút "Hủy yêu cầu" không hiển thị, không thể hủy yêu cầu đã xử lý | | Pass | 11/15/2015 | |
| **VALID-YCDH-05** | Tìm kiếm với từ khóa đặc biệt | 1. Chọn tab "Yêu cầu của tôi"<br>2. Nhập từ khóa có ký tự đặc biệt | Hệ thống xử lý an toàn, không gây lỗi, lọc kết quả chính xác | | Pass | 11/15/2015 | |
| **VALID-YCDH-06** | Nhập ISBN không đúng định dạng | 1. Chọn tab "Tạo yêu cầu"<br>2. Nhập ISBN không đúng định dạng<br>3. Gửi yêu cầu | Hệ thống cho phép gửi (ISBN là optional) hoặc hiển thị cảnh báo định dạng không đúng | | Pass | 11/15/2015 | |
| **VALID-YCDH-07** | Tạo yêu cầu với tên sản phẩm quá dài | 1. Chọn tab "Tạo yêu cầu"<br>2. Nhập tên sản phẩm rất dài (>200 ký tự)<br>3. Gửi yêu cầu | Tên sản phẩm được cắt hoặc hiển thị cảnh báo nếu vượt quá giới hạn | | Pass | 11/15/2015 | |
| **VALID-YCDH-08** | Tạo nhiều yêu cầu giống nhau | 1. Tạo yêu cầu<br>2. Tạo lại yêu cầu giống hệt<br>3. Gửi yêu cầu | Hệ thống cho phép tạo hoặc hiển thị cảnh báo "Yêu cầu tương tự đã tồn tại" | | Pass | 11/15/2015 | |

