# Test Case Template - Quản lý yêu cầu và phê duyệt (Admin)

## Module Code
**Giao lộ 19: Họcl6c (Admin)**

## Test Requirement
1. Hiển thị danh sách yêu cầu
2. Xem chi tiết yêu cầu
3. Phê duyệt yêu cầu
4. Từ chối yêu cầu
5. Theo dõi trạng thái yêu cầu

---

## Test Summary

### Người lớp Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 22 |
| **Fail** | 0 |
| **Untested** | 0 |
| **N/A** | 0 |
| **Number of Test cases** | 22 |

---

## Test Cases

### Function: Hiển thị danh sách yêu cầu

#### Check GUI: Hiển thị danh sách yêu cầu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DSYC-01** | Kiểm tra tiêu đề trang | 1. Đăng nhập Admin<br>2. Truy cập /admin/requests<br>3. Kiểm tra tiêu đề | Hiển thị Card với CardHeader có CardTitle "Quản lý yêu cầu và phê duyệt" với class text-2xl font-bold, layout trong div space-y-6 | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSYC-02** | Kiểm tra card Bộ lọc | 1. Đăng nhập Admin<br>2. Truy cập /admin/requests<br>3. Kiểm tra card bộ lọc | Hiển thị Card với CardContent có grid gap-4 md:grid-cols-5 chứa: Select "Loại yêu cầu" với placeholder, Select "Trạng thái" với placeholder, Select "Người gửi" với placeholder, Select "Khoảng thời gian" với placeholder, Input placeholder="Tìm mã yêu cầu" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSYC-03** | Kiểm tra dropdown Loại yêu cầu | 1. Đăng nhập Admin<br>2. Truy cập /admin/requests<br>3. Kiểm tra dropdown | Hiển thị Select với SelectTrigger, SelectValue placeholder="Loại yêu cầu", SelectContent có các option: "Nhập hàng", "Trả hàng", "Đổi hàng", "Hỗ trợ", "Khác" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSYC-04** | Kiểm tra dropdown Trạng thái | 1. Đăng nhập Admin<br>2. Truy cập /admin/requests<br>3. Kiểm tra dropdown | Hiển thị Select với SelectTrigger, SelectValue placeholder="Trạng thái", SelectContent có các option: "Chờ phê duyệt", "Đã phê duyệt", "Từ chối", "Đang xử lý", "Hoàn thành" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSYC-05** | Kiểm tra dropdown Người gửi | 1. Đăng nhập Admin<br>2. Truy cập /admin/requests<br>3. Kiểm tra dropdown | Hiển thị Select với SelectTrigger, SelectValue placeholder="Người gửi", SelectContent có các option: "Nhân viên bán hàng", "Nhân viên kho", "Khách hàng", "Admin" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSYC-06** | Kiểm tra dropdown Khoảng thời gian | 1. Đăng nhập Admin<br>2. Truy cập /admin/requests<br>3. Kiểm tra dropdown | Hiển thị Select với SelectTrigger, SelectValue placeholder="Khoảng thời gian", SelectContent có các option: "Tất cả", "Hôm nay", "Tuần này", "Tháng này", "Quý này", "Năm này", "Tùy chọn" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSYC-07** | Kiểm tra card Danh sách yêu cầu | 1. Đăng nhập Admin<br>2. Truy cập /admin/requests<br>3. Kiểm tra card | Hiển thị Card với CardContent chứa Table | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSYC-08** | Kiểm tra bảng danh sách yêu cầu | 1. Đăng nhập Admin<br>2. Truy cập /admin/requests<br>3. Kiểm tra bảng | Hiển thị Table với TableHeader có các TableHead: "Mã yêu cầu", "Loại yêu cầu", "Người gửi", "Ngày tạo", "Trạng thái", "Ưu tiên", "Thao tác". TableBody có các TableRow với TableCell tương ứng | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSYC-09** | Kiểm tra cột Mã yêu cầu | 1. Đăng nhập Admin<br>2. Truy cập /admin/requests<br>3. Kiểm tra cột | Mỗi hàng có TableCell chứa div flex items-center gap-2 với span (mã yêu cầu, VD: YC001) và Badge với variant="destructive" nếu priority="Cao" hoặc variant="secondary" nếu khác, hiển thị priority | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DSYC-10** | Kiểm tra các nút thao tác | 1. Đăng nhập Admin<br>2. Truy cập /admin/requests<br>3. Kiểm tra nút thao tác | Mỗi hàng có TableCell "Thao tác" với class space-x-2 chứa: Button size="sm" variant="outline" "Xem chi tiết" với Link href="/admin/requests/[id]", Button size="sm" variant="outline" "Phê duyệt", Button size="sm" variant="outline" "Từ chối", Button size="sm" variant="outline" "Giao việc" | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Hiển thị danh sách yêu cầu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DSYC-01** | Xem danh sách yêu cầu | 1. Đăng nhập Admin<br>2. Truy cập /admin/requests | Hiển thị đầy đủ: card Bộ lọc với 4 Select (Loại yêu cầu, Trạng thái, Người gửi, Khoảng thời gian) và 1 Input tìm kiếm, card Danh sách yêu cầu với Table hiển thị các yêu cầu, mỗi hàng có Mã yêu cầu (với Badge priority), Loại yêu cầu, Người gửi, Ngày tạo, Trạng thái, Ưu tiên, các nút thao tác (Xem chi tiết, Phê duyệt, Từ chối, Giao việc) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSYC-02** | Tìm kiếm yêu cầu | 1. Đăng nhập Admin<br>2. Truy cập /admin/requests<br>3. Nhập từ khóa tìm kiếm vào ô "Tìm mã yêu cầu" | Danh sách yêu cầu được lọc theo từ khóa (mã yêu cầu), bảng cập nhật ngay lập tức (real-time filtering), hiển thị các yêu cầu có mã chứa từ khóa (case-insensitive) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSYC-03** | Lọc yêu cầu theo loại | 1. Đăng nhập Admin<br>2. Truy cập /admin/requests<br>3. Chọn loại yêu cầu từ dropdown (VD: "Nhập hàng") | Danh sách yêu cầu được lọc theo loại đã chọn, bảng chỉ hiển thị yêu cầu có loại tương ứng, cập nhật ngay lập tức | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSYC-04** | Lọc yêu cầu theo trạng thái | 1. Đăng nhập Admin<br>2. Truy cập /admin/requests<br>3. Chọn trạng thái từ dropdown (VD: "Chờ phê duyệt") | Danh sách yêu cầu được lọc theo trạng thái đã chọn, bảng chỉ hiển thị yêu cầu có trạng thái tương ứng, cập nhật ngay lập tức | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSYC-05** | Lọc yêu cầu theo người gửi | 1. Đăng nhập Admin<br>2. Truy cập /admin/requests<br>3. Chọn người gửi từ dropdown (VD: "Nhân viên kho") | Danh sách yêu cầu được lọc theo người gửi đã chọn, bảng chỉ hiển thị yêu cầu có người gửi tương ứng, cập nhật ngay lập tức | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSYC-06** | Lọc yêu cầu theo khoảng thời gian | 1. Đăng nhập Admin<br>2. Truy cập /admin/requests<br>3. Chọn khoảng thời gian từ dropdown (VD: "Tuần này") | Danh sách yêu cầu được lọc theo khoảng thời gian đã chọn, bảng chỉ hiển thị yêu cầu được tạo trong khoảng thời gian tương ứng, cập nhật ngay lập tức | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DSYC-07** | Kết hợp nhiều bộ lọc | 1. Đăng nhập Admin<br>2. Truy cập /admin/requests<br>3. Chọn loại "Nhập hàng"<br>4. Chọn trạng thái "Chờ phê duyệt"<br>5. Chọn người gửi "Nhân viên kho"<br>6. Nhập từ khóa tìm kiếm | Danh sách yêu cầu được lọc theo tất cả các tiêu chí đã chọn, bảng chỉ hiển thị yêu cầu thỏa mãn tất cả điều kiện, cập nhật ngay lập tức | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Xem chi tiết yêu cầu

#### Check GUI: Xem chi tiết yêu cầu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CTYC-01** | Kiểm tra tiêu đề trang | 1. Đăng nhập Admin<br>2. Truy cập /admin/requests/[id]<br>3. Kiểm tra tiêu đề | Hiển thị tiêu đề "Chi tiết yêu cầu - [Mã yêu cầu]" hoặc "Chi tiết yêu cầu - YC001" với class text-2xl font-bold, layout tương tự trang chi tiết nhân viên | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-CTYC-02** | Kiểm tra card Thông tin cơ bản | 1. Đăng nhập Admin<br>2. Truy cập /admin/requests/[id]<br>3. Kiểm tra card | Hiển thị Card với CardHeader có CardTitle "Thông tin cơ bản", CardContent có grid layout, hiển thị các trường: Mã yêu cầu, Loại yêu cầu (Badge), Người gửi, Ngày tạo, Trạng thái (Badge), Ưu tiên (Badge) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-CTYC-03** | Kiểm tra card Nội dung yêu cầu | 1. Đăng nhập Admin<br>2. Truy cập /admin/requests/[id]<br>3. Kiểm tra card | Hiển thị Card với CardHeader có CardTitle "Nội dung yêu cầu", CardContent hiển thị các trường: Tiêu đề, Mô tả, Lý do, Yêu cầu cụ thể, Thời hạn, Ghi chú | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-CTYC-04** | Kiểm tra card Lịch sử xử lý | 1. Đăng nhập Admin<br>2. Truy cập /admin/requests/[id]<br>3. Kiểm tra card | Hiển thị Card với CardHeader có CardTitle "Lịch sử xử lý", CardContent có Table hoặc timeline hiển thị các sự kiện: Thời gian, Người xử lý, Hành động, Ghi chú | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Xem chi tiết yêu cầu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CTYC-01** | Xem chi tiết yêu cầu | 1. Đăng nhập Admin<br>2. Truy cập /admin/requests<br>3. Click nút "Xem chi tiết" hoặc Link href="/admin/requests/[id]" | Hiển thị đầy đủ thông tin: tiêu đề "Chi tiết yêu cầu - [Mã]", card Thông tin cơ bản với đầy đủ các trường (Mã yêu cầu, Loại yêu cầu với Badge, Người gửi, Ngày tạo, Trạng thái với Badge, Ưu tiên với Badge), card Nội dung yêu cầu với đầy đủ các trường (Tiêu đề, Mô tả, Lý do, Yêu cầu cụ thể, Thời hạn, Ghi chú), card Lịch sử xử lý với Table/timeline, các nút thao tác (Phê duyệt, Từ chối, Giao việc) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-CTYC-02** | Xem lịch sử xử lý | 1. Đăng nhập Admin<br>2. Truy cập /admin/requests/[id]<br>3. Xem card Lịch sử xử lý | Hiển thị lịch sử xử lý theo dòng thời gian từ cũ đến mới, mỗi sự kiện có: Thời gian, Người xử lý, Hành động (Tạo yêu cầu, Phê duyệt, Từ chối, Giao việc, Cập nhật trạng thái), Ghi chú | FUNC-DN-02, FUNC-CTYC-01 | Pass | 11/15/2015 | |

---

### Function: Phê duyệt yêu cầu

#### Check FUNC: Phê duyệt yêu cầu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-PDYC-01** | Phê duyệt yêu cầu hoàn toàn | 1. Đăng nhập Admin<br>2. Truy cập /admin/requests<br>3. Click nút "Phê duyệt" trên một yêu cầu<br>4. Chọn "Phê duyệt hoàn toàn"<br>5. Chọn người thực hiện từ Select (nếu có)<br>6. Nhập ghi chú (nếu có)<br>7. Click "Xác nhận" | Hiển thị Dialog hoặc form phê duyệt với Select loại phê duyệt ("Phê duyệt hoàn toàn", "Phê duyệt có điều kiện"), có thể có Select người thực hiện, Textarea ghi chú. Sau khi xác nhận: yêu cầu được phê duyệt thành công, hiển thị thông báo thành công (toast success), trạng thái cập nhật thành "Đã phê duyệt" với Badge, thông báo được gửi cho người gửi qua email/SMS về việc yêu cầu đã được phê duyệt, thông báo được gửi cho người thực hiện (nếu có), lịch sử xử lý được ghi nhận với hành động "Phê duyệt", dialog/form đóng, bảng được refresh | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-PDYC-02** | Phê duyệt yêu cầu có điều kiện | 1. Đăng nhập Admin<br>2. Truy cập /admin/requests<br>3. Click nút "Phê duyệt"<br>4. Chọn "Phê duyệt có điều kiện"<br>5. Nhập điều kiện vào Textarea<br>6. Chọn người thực hiện<br>7. Click "Xác nhận" | Hiển thị Dialog hoặc form với Textarea "Điều kiện phê duyệt" required. Sau khi xác nhận: yêu cầu được phê duyệt có điều kiện thành công, hiển thị thông báo thành công, trạng thái cập nhật thành "Đã phê duyệt (có điều kiện)" hoặc "Đang xử lý", điều kiện được ghi nhận trong lịch sử xử lý, thông báo được gửi cho người gửi với điều kiện, thông báo được gửi cho người thực hiện | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-PDYC-03** | Phê duyệt yêu cầu đã được phê duyệt | 1. Đăng nhập Admin<br>2. Truy cập /admin/requests<br>3. Tìm yêu cầu có trạng thái "Đã phê duyệt"<br>4. Click nút "Phê duyệt" | Hiển thị thông báo cảnh báo "Yêu cầu này đã được phê duyệt" hoặc nút "Phê duyệt" bị disabled, không thể phê duyệt lại | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-PDYC-04** | Hủy phê duyệt yêu cầu | 1. Đăng nhập Admin<br>2. Truy cập /admin/requests<br>3. Click nút "Phê duyệt"<br>4. Nhập thông tin<br>5. Click "Hủy" trong dialog | Dialog đóng lại, không phê duyệt yêu cầu, trạng thái không thay đổi | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Từ chối yêu cầu

#### Check FUNC: Từ chối yêu cầu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TCYC-01** | Từ chối yêu cầu | 1. Đăng nhập Admin<br>2. Truy cập /admin/requests<br>3. Click nút "Từ chối" trên một yêu cầu<br>4. Chọn lý do từ chối từ Select hoặc nhập vào Textarea<br>5. Nhập ghi chú (nếu có)<br>6. Click "Xác nhận từ chối" | Hiển thị Dialog hoặc form từ chối với Select "Lý do từ chối" (có thể có các option: "Không đủ điều kiện", "Không phù hợp", "Khác") hoặc Textarea "Lý do từ chối" required, có thể có Textarea "Ghi chú". Sau khi xác nhận: yêu cầu được từ chối thành công, hiển thị thông báo thành công (toast success), trạng thái cập nhật thành "Từ chối" với Badge variant="destructive", thông báo được gửi cho người gửi qua email/SMS về việc yêu cầu bị từ chối và lý do, lịch sử xử lý được ghi nhận với hành động "Từ chối" và lý do, dialog/form đóng, bảng được refresh | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TCYC-02** | Từ chối yêu cầu thiếu lý do | 1. Đăng nhập Admin<br>2. Truy cập /admin/requests<br>3. Click nút "Từ chối"<br>4. Để trống lý do từ chối<br>5. Click "Xác nhận từ chối" | Hiển thị thông báo lỗi "Vui lòng nhập lý do từ chối" (toast error), không từ chối yêu cầu, dialog vẫn mở | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TCYC-03** | Từ chối yêu cầu đã được xử lý | 1. Đăng nhập Admin<br>2. Truy cập /admin/requests<br>3. Tìm yêu cầu có trạng thái "Đã phê duyệt" hoặc "Hoàn thành"<br>4. Click nút "Từ chối" | Hiển thị thông báo cảnh báo "Không thể từ chối yêu cầu đã được xử lý" hoặc nút "Từ chối" bị disabled, không thể từ chối | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TCYC-04** | Hủy từ chối yêu cầu | 1. Đăng nhập Admin<br>2. Truy cập /admin/requests<br>3. Click nút "Từ chối"<br>4. Nhập lý do<br>5. Click "Hủy" trong dialog | Dialog đóng lại, không từ chối yêu cầu, trạng thái không thay đổi | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Theo dõi trạng thái yêu cầu

#### Check FUNC: Theo dõi trạng thái yêu cầu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TDYC-01** | Xem trạng thái yêu cầu | 1. Đăng nhập Admin<br>2. Truy cập /admin/requests<br>3. Xem trạng thái các yêu cầu trong bảng | Hiển thị trạng thái của các yêu cầu dưới dạng Badge với màu sắc tương ứng: "Chờ phê duyệt" (màu vàng/cam), "Đã phê duyệt" (màu xanh), "Từ chối" (màu đỏ), "Đang xử lý" (màu xanh dương), "Hoàn thành" (màu xanh lá), có thể có icon tương ứng | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TDYC-02** | Cập nhật trạng thái yêu cầu | 1. Đăng nhập Admin<br>2. Truy cập /admin/requests/[id]<br>3. Click nút "Cập nhật trạng thái" hoặc chọn trạng thái mới từ Select<br>4. Nhập ghi chú (nếu có)<br>5. Click "Lưu" | Hiển thị form hoặc Dialog với Select trạng thái (các option: Chờ phê duyệt, Đã phê duyệt, Từ chối, Đang xử lý, Hoàn thành), có thể có Textarea ghi chú. Sau khi lưu: trạng thái yêu cầu được cập nhật thành công, hiển thị thông báo thành công (toast success), Badge trạng thái được cập nhật với màu sắc và icon tương ứng, thông báo được gửi cho người gửi về việc thay đổi trạng thái, lịch sử xử lý được ghi nhận với hành động "Cập nhật trạng thái" | FUNC-DN-02, FUNC-CTYC-01 | Pass | 11/15/2015 | |
| **FUNC-TDYC-03** | Giao việc cho nhân viên | 1. Đăng nhập Admin<br>2. Truy cập /admin/requests<br>3. Click nút "Giao việc" trên một yêu cầu<br>4. Chọn nhân viên từ Select<br>5. Nhập hướng dẫn/ghi chú<br>6. Click "Xác nhận" | Hiển thị Dialog hoặc form giao việc với Select "Chọn nhân viên" (danh sách nhân viên), Textarea "Hướng dẫn" hoặc "Ghi chú". Sau khi xác nhận: yêu cầu được giao cho nhân viên thành công, hiển thị thông báo thành công (toast success), trạng thái cập nhật thành "Đang xử lý", thông báo được gửi cho nhân viên được giao việc qua email/SMS, lịch sử xử lý được ghi nhận với hành động "Giao việc" và người được giao, dialog/form đóng, bảng được refresh | FUNC-DN-02 | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn MDX để dễ dàng quản lý và cập nhật test cases.*
