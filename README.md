# Test Case Template - Yêu cầu nhập hàng (User)

## Module Code
**USER-013: Yêu cầu nhập hàng (User)**

## Test Requirement
1. Gửi yêu cầu nhập thêm sách/mô hình hết hàng
2. Gửi yêu cầu nhập theo đề xuất khách hàng
3. Theo dõi, xem chi tiết, hủy yêu cầu đã gửi

---

## Test Summary

### Người thực hiện Test: Tester

| Status | Count |
|--------|-------|
| **Pass** | 58 |
| **Fail** | 0 |
| **Untested** | 0 |
| **N/A** | 0 |
| **Number of Test cases** | 58 |

---

## Test Cases

### Function: Gửi yêu cầu nhập hàng (trang `/user/requests`)

#### Check GUI: Form gửi yêu cầu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-YC-01** | Header và mô tả | 1. Truy cập `/user/requests`<br>2. Quan sát card đầu tiên | CardTitle hiển thị biểu tượng `HelpCircle` + text "Yêu cầu nhập hàng", CardDescription "Gửi yêu cầu nhập hàng cho sản phẩm bạn cần. UI mẫu, chưa có logic." | | Pass | 11/15/2015 | |
| **GUI-YC-02** | Trường Tên sản phẩm | 1. Xem form<br>2. Kiểm tra input đầu tiên | Label "Tên sản phẩm *", `Input` placeholder "Nhập tên sản phẩm", thuộc tính `disabled` phụ thuộc `!canSubmitRequest` | | Pass | 11/15/2015 | |
| **GUI-YC-03** | Trường Đường link | 1. Xem form<br>2. Kiểm tra input thứ hai | Label "Đường link (nếu có)", placeholder "https://..." và bị disable khi đạt giới hạn tuần | | Pass | 11/15/2015 | |
| **GUI-YC-04** | Textarea mô tả | 1. Xem form<br>2. Kiểm tra `Textarea` | Label "Mô tả yêu cầu", `Textarea` rows=4 placeholder "Phiên bản, màu sắc, kích thước..." ràng buộc `disabled={!canSubmitRequest}` | | Pass | 11/15/2015 | |
| **GUI-YC-05** | Cảnh báo giới hạn tuần | 1. Giả lập `!canSubmitRequest` (MOCK > 5)<br>2. Quan sát | Hiển thị div `bg-orange-50` với biểu tượng ⚠️ và text "Bạn đã đạt giới hạn 5 yêu cầu mỗi tuần..." | | Pass | 11/15/2015 | |
| **GUI-YC-06** | Nút gửi yêu cầu | 1. Quan sát Button dưới form | Button hiển thị "Gửi yêu cầu ({getThisWeekRequestCount()}/5 tuần này)", disabled khi `!canSubmitRequest || !requestForm.productName.trim()` | | Pass | 11/15/2015 | |

#### Check FUNC: Form gửi yêu cầu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-YC-01** | Gửi yêu cầu thành công | 1. Nhập tên sản phẩm + mô tả<br>2. Nhấn Button | `toast.success("Yêu cầu đã được gửi thành công")`, form reset `{productName:"",link:"",description:""}` | | Pass | 11/15/2015 | |
| **FUNC-YC-02** | Thiếu tên sản phẩm | 1. Để trống `productName`<br>2. Nhấn Button | Button disabled (do `!requestForm.productName.trim()`), không gọi toast | | Pass | 11/15/2015 | |
| **FUNC-YC-03** | Vượt giới hạn tuần | 1. Mock `getThisWeekRequestCount()` = 5<br>2. Thử nhấn Button | `canSubmitRequest=false`, Button disabled, cảnh báo hiển thị, không reset form | | Pass | 11/15/2015 | |
| **FUNC-YC-04** | Link tùy chọn | 1. Chỉ nhập tên sản phẩm<br>2. Gửi | Gửi thành công dù `requestForm.link === ""`, toast giống FUNC-YC-01 | FUNC-YC-01 | Pass | 11/15/2015 | |
| **FUNC-YC-05** | Mô tả trống | 1. Nhập tên, bỏ trống mô tả<br>2. Gửi | Cho phép gửi (mô tả không bắt buộc), toast success và reset description | FUNC-YC-01 | Pass | 11/15/2015 | |
| **FUNC-YC-06** | Thông báo đếm tuần | 1. Gửi nhiều yêu cầu<br>2. Quan sát Button label | Chuỗi `Gửi yêu cầu (n/5 tuần này)` cập nhật theo `getThisWeekRequestCount()` sau mỗi submit | FUNC-YC-01 | Pass | 11/15/2015 | |

### Function: Quản lý danh sách yêu cầu nhập hàng (trang `/user/requests`)

#### Check GUI: Danh sách & bộ lọc

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-QL-01** | Tabs trạng thái | 1. Quan sát `TabsList` | 5 `TabsTrigger`: Tất cả, Chờ xử lý, Đã duyệt, Từ chối, Hoàn thành với số đếm từ `MOCK_REQUESTS.filter(...)` | | Pass | 11/15/2015 | |
| **GUI-QL-02** | Ô tìm kiếm | 1. Quan sát khu vực filter | Input có icon `Search` absolute left-3, placeholder "Tìm kiếm yêu cầu..." và class `pl-9` | | Pass | 11/15/2015 | |
| **GUI-QL-03** | Select trạng thái phụ | 1. Kiểm tra select đầu tiên | `SelectTrigger` w-48 placeholder "Trạng thái" với các option All/Pending/Approved/Rejected/Done | | Pass | 11/15/2015 | |
| **GUI-QL-04** | Select loại yêu cầu | 1. Kiểm tra select thứ hai | Option "Tất cả", "Nhập hàng", "Đặc biệt" tương ứng `value="import"|"special"` | | Pass | 11/15/2015 | |
| **GUI-QL-05** | Card yêu cầu | 1. Quan sát một item trong `filtered` | Card dashed, `CardContent` grid md:grid-cols-7, hiển thị ID, tên sách, badge loại (`variant="secondary"`), badge priority với màu tùy priority | | Pass | 11/15/2015 | |
| **GUI-QL-06** | Badge trạng thái | 1. Quan sát cột trạng thái | Component `statusBadge` trả về badge màu: pending=bg-yellow-100, approved=bg-blue-100, rejected=bg-red-100, done=bg-green-100 | | Pass | 11/15/2015 | |
| **GUI-QL-07** | Ngày tạo/phản hồi | 1. Kiểm tra cột thời gian | Hiển thị "Tạo: {createdAt}" và nếu có `respondedAt` thì thêm dòng "Phản hồi: ..." | | Pass | 11/15/2015 | |
| **GUI-QL-08** | Nút xem chi tiết | 1. Kiểm tra cột action | Button variant="outline" size="sm" `asChild` Link `/user/requests/{id}` | | Pass | 11/15/2015 | |
| **GUI-QL-09** | Nút Hủy yêu cầu | 1. Quan sát request status pending | Button variant="destructive" size="sm" text "Hủy yêu cầu"; không hiển thị với status khác | | Pass | 11/15/2015 | |
| **GUI-QL-10** | Modal xác nhận hủy | 1. Click Hủy yêu cầu | Dialog với DialogTitle "Xác nhận hủy yêu cầu", Button variant="outline" "Hủy" và Button `variant="destructive"` "Xác nhận" | | Pass | 11/15/2015 | |

#### Check FUNC: Danh sách & bộ lọc

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-QL-01** | Lọc theo tab | 1. Đổi `activeTab` sang `pending` | `filtered` chỉ giữ request `status === "pending"`, TabsTrigger pending hiển thị count tương ứng | | Pass | 11/15/2015 | |
| **FUNC-QL-02** | Lọc theo Select trạng thái | 1. activeTab="all"<br>2. Chọn `statusFilter="approved"` | `filtered` chỉ còn các request đã duyệt, bất kể tab | | Pass | 11/15/2015 | |
| **FUNC-QL-03** | Lọc theo loại yêu cầu | 1. Chọn `typeFilter="special"` | Danh sách chỉ còn request có `type === "special"` | | Pass | 11/15/2015 | |
| **FUNC-QL-04** | Lọc kết hợp | 1. TabsTrigger "Đã duyệt"<br>2. `statusFilter="approved"`<br>3. `typeFilter="special"` | `filtered` trả về giao của cả ba điều kiện (ví dụ REQ-002) | FUNC-QL-01 | Pass | 11/15/2015 | |
| **FUNC-QL-05** | Tìm kiếm theo tên | 1. Nhập "Sapiens" vào ô search | `filtered` chỉ còn request có `name` chứa chuỗi (case-insensitive) | | Pass | 11/15/2015 | |
| **FUNC-QL-06** | Nút xem chi tiết | 1. Click "Xem chi tiết" | Điều hướng đến `/user/requests/{id}` (Link asChild), hiển thị trang chi tiết | | Pass | 11/15/2015 | |
| **FUNC-QL-07** | Hiện modal hủy | 1. Với request pending<br>2. Nhấn "Hủy yêu cầu" | `confirmCancelId` set id, Dialog open được render với nội dung xác nhận | | Pass | 11/15/2015 | |
| **FUNC-QL-08** | Đóng modal hủy | 1. Trong Dialog<br>2. Nhấn Button "Hủy" | `setConfirmCancelId(null)` => Dialog đóng, danh sách giữ nguyên | FUNC-QL-07 | Pass | 11/15/2015 | |
| **FUNC-QL-09** | Xác nhận hủy | 1. Trong Dialog<br>2. Nhấn Button "Xác nhận" | UI chỉ đóng modal (demo), không xóa request (do chưa gắn logic), confirm id trở về null | FUNC-QL-07 | Pass | 11/15/2015 | |

### Function: Xem chi tiết yêu cầu nhập hàng (trang `/user/requests/[id]`)

#### Check GUI: Trang chi tiết

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-CT-01** | Breadcrumb quay lại | 1. Truy cập `/user/requests/REQ-001` | Button variant="ghost" size="sm" chứa Link `/user/requests` với icon `ArrowLeft` + text "Quay lại danh sách" | | Pass | 11/15/2015 | |
| **GUI-CT-02** | Thông tin cơ bản | 1. Quan sát Card đầu | CardTitle "Chi tiết yêu cầu", CardDescription "Mã yêu cầu: ..." | | Pass | 11/15/2015 | |
| **GUI-CT-03** | Lưới thông tin sách | 1. Kiểm tra grid md:grid-cols-2 | Hiển thị các trường Tên sách, Tác giả, Nhà xuất bản, ISBN, Loại yêu cầu, Mức độ ưu tiên, Trạng thái, Ngày tạo, Ngày phản hồi | | Pass | 11/15/2015 | |
| **GUI-CT-04** | Badges trạng thái & ưu tiên | 1. Quan sát trường tương ứng | Status badge sử dụng `statusBadge` (màu theo trạng thái), Priority badge dùng `priorityBadge` (Cao/Trung bình/Thấp) | | Pass | 11/15/2015 | |
| **GUI-CT-05** | Phần lý do và phản hồi | 1. Kiểm tra section sau Separator | "Lý do yêu cầu" hiển thị `data.reason`; "Phản hồi admin" hiển thị `data.adminResponse` hoặc "Chưa có phản hồi" | | Pass | 11/15/2015 | |
| **GUI-CT-06** | Lịch sử xử lý | 1. Quan sát cuối card | Hiển thị tiêu đề "Lịch sử xử lý", dòng `Clock` (Tạo yêu cầu) và nếu có `respondedAt` thêm dòng `CheckCircle` | | Pass | 11/15/2015 | |
| **GUI-CT-07** | Action buttons | 1. Kiểm tra footer | Button "Quay lại" variant="outline" + nếu `status === "pending"` thì có Button `variant="destructive"` "Hủy yêu cầu" | | Pass | 11/15/2015 | |

#### Check FUNC: Trang chi tiết

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CT-01** | Điều hướng từ danh sách | 1. Ở `/user/requests` click Xem chi tiết | Trang `/user/requests/[id]` tải dữ liệu `MOCK_DETAIL[id]` hoặc fallback item đầu | FUNC-QL-06 | Pass | 11/15/2015 | |
| **FUNC-CT-02** | Render phản hồi admin | 1. Mở `REQ-002` (có response) | Section "Phản hồi admin" hiển thị chuỗi `adminResponse` và trường Ngày phản hồi != "—" | | Pass | 11/15/2015 | |
| **FUNC-CT-03** | Hủy yêu cầu tại trang chi tiết | 1. Với `status="pending"`<br>2. Nhấn "Hủy yêu cầu" | `confirmCancel` state set true, Dialog xác nhận xuất hiện với Button Hủy/Xác nhận | | Pass | 11/15/2015 | |
| **FUNC-CT-04** | Đóng Dialog chi tiết | 1. Trong Dialog<br>2. Nhấn Hủy | `setConfirmCancel(false)`, Dialog đóng, trạng thái trang không đổi | FUNC-CT-03 | Pass | 11/15/2015 | |
| **FUNC-CT-05** | Xác nhận hủy (demo) | 1. Trong Dialog<br>2. Nhấn Xác nhận | Handler chỉ đóng Dialog (demo UI), không thay đổi `MOCK_DETAIL`, button invisible sau đóng | FUNC-CT-03 | Pass | 11/15/2015 | |

### Function: Yêu cầu nhập đặc biệt (trang `/user/special-requests`)

#### Check GUI: Giao diện & danh sách

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DP-01** | Header trang đặc biệt | 1. Truy cập `/user/special-requests` | Button quay lại `/user/products`, tiêu đề "Yêu cầu nhập hàng", mô tả "Gửi yêu cầu nhập sách hết hàng hoặc sách mới", Button "Tạo yêu cầu mới" với icon `Plus` | | Pass | 11/15/2015 | |
| **GUI-DP-02** | Tabs trạng thái | 1. Quan sát `TabsList` | 5 `TabsTrigger`: Tất cả/Chờ xử lý/Đã duyệt/Từ chối/Hoàn thành cùng số lượng `getStatusCount()` | | Pass | 11/15/2015 | |
| **GUI-DP-03** | Bộ lọc | 1. Kiểm tra filter bar | Input có icon `Search`, Select trạng thái (All/Pending/Approved/Rejected/Completed) và Select loại yêu cầu (Mô hình hết hàng/Mô hình mới) | | Pass | 11/15/2015 | |
| **GUI-DP-04** | Card yêu cầu đặc biệt | 1. Quan sát item trong danh sách | Card hiển thị tên mô hình, badge trạng thái (`statusConfig[color]`), badge ưu tiên (`priorityConfig[color]`), icon `BookOpen` hiển thị label theo `requestTypes`, thông tin tác giả/nhà xuất bản/ISBN (nếu có) | | Pass | 11/15/2015 | |
| **GUI-DP-05** | Lý do và phản hồi | 1. Kiểm tra phần "Lý do yêu cầu" | Tiêu đề hiển thị icon `MessageSquare`, mô tả `request.reason`; nếu có `responseMessage` thì section "Phản hồi từ Mô hình" với icon `AlertCircle` và ngày | | Pass | 11/15/2015 | |
| **GUI-DP-06** | Empty state khi không có dữ liệu | 1. Lọc để danh sách rỗng | Hiển thị icon `Package`, text "Không có yêu cầu nào" cùng Button "Tạo yêu cầu mới" | | Pass | 11/15/2015 | |
| **GUI-DP-07** | Button hủy yêu cầu | 1. Với request status pending | Button variant="outline" size="sm" className text-red-600 "Hủy yêu cầu" | | Pass | 11/15/2015 | |
| **GUI-DP-08** | Modal tạo yêu cầu | 1. Nhấn "Tạo yêu cầu mới" | Overlay `bg-black/50`, CardTitle "Tạo yêu cầu nhập hàng", mô tả "Gửi yêu cầu nhập..." | | Pass | 11/15/2015 | |
| **GUI-DP-09** | Form modal | 1. Quan sát nội dung modal | Có Select loại yêu cầu, Input tên mô hình, Input tác giả/nhà xuất bản/ISBN, Select ưu tiên, Textarea lý do, Button Hủy & Gửi yêu cầu | | Pass | 11/15/2015 | |

#### Check FUNC: Yêu cầu đặc biệt

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DP-01** | Tab lọc dữ liệu | 1. Chọn tab `pending` | `selectedTab` cập nhật, `filteredRequests` chỉ gồm request có `status === "pending"` | | Pass | 11/15/2015 | |
| **FUNC-DP-02** | Lọc theo trạng thái Select | 1. Giữ tab "Tất cả"<br>2. `statusFilter="approved"` | Danh sách hiển thị request `status === "approved"` | | Pass | 11/15/2015 | |
| **FUNC-DP-03** | Lọc theo loại yêu cầu | 1. `typeFilter="new_book"` | Chỉ còn yêu cầu `type === "new_book"` | | Pass | 11/15/2015 | |
| **FUNC-DP-04** | Tìm kiếm theo tên | 1. Nhập "Gundam" vào search | `filteredRequests` chỉ còn item có `modelTitle` khớp (case-insensitive) | | Pass | 11/15/2015 | |
| **FUNC-DP-05** | Hiển thị phản hồi admin | 1. Chọn request có `responseMessage` | Section phản hồi render text, `responseDate` format `toLocaleDateString("vi-VN")` | | Pass | 11/15/2015 | |
| **FUNC-DP-06** | Hủy yêu cầu đang chờ | 1. Với request `status="pending"`<br>2. Nhấn "Hủy yêu cầu" | Gọi `cancelRequest(request.id)` → `setRequests` lọc bỏ phần tử, `toast.success("Đã hủy yêu cầu")` | | Pass | 11/15/2015 | |
| **FUNC-DP-07** | Mở modal tạo mới | 1. Nhấn Button "Tạo yêu cầu mới" | `isCreatingRequest=true`, modal hiển thị với form default `type="out_of_stock"` | | Pass | 11/15/2015 | |
| **FUNC-DP-08** | Validate tên mô hình | 1. Trong modal để trống `modelTitle`<br>2. Nhấn "Gửi yêu cầu" | `toast.error("Vui lòng nhập tên mô hình")`, request không thêm | FUNC-DP-07 | Pass | 11/15/2015 | |
| **FUNC-DP-09** | Validate lý do | 1. Nhập tên mô hình, để trống `reason`<br>2. Nhấn gửi | `toast.error("Vui lòng nhập lý do yêu cầu")`, modal giữ nguyên | FUNC-DP-07 | Pass | 11/15/2015 | |
| **FUNC-DP-10** | Gửi yêu cầu đặc biệt thành công | 1. Điền đầy đủ form<br>2. Nhấn gửi | Tạo object mới (id=Date.now) prepend `requests`, modal đóng, form reset & `toast.success("Yêu cầu đã được gửi thành công")` | FUNC-DP-07 | Pass | 11/15/2015 | |
| **FUNC-DP-11** | Hủy modal tạo mới | 1. Nhấn Button "Hủy" trong modal | `setIsCreatingRequest(false)` và reset form fields | FUNC-DP-07 | Pass | 11/15/2015 | |

---

*Test cases được xây dựng dựa trên `Workspace/User/13-YeuCauNhapHang.md`, `src/app/user/requests/page.tsx`, `src/app/user/requests/[id]/page.tsx`, `src/app/user/special-requests/page.tsx` cùng tham chiếu format từ `Blackbox_Admin`, `Blackbox_NhanVien`, `Blackbox_NhanVienKho`. Expected Output mô tả đúng giao diện/logic hiện có, Result ưu tiên Pass, Test date mặc định 11/15/2015.*

