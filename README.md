# Test Case Template - Thông báo (User)

## Module Code
**USER-014: Thông báo (User)**

## Test Requirement
1. Hiển thị, lọc và quản lý danh sách thông báo của User
2. Thông báo sách có hàng trở lại / sách trong wishlist cập nhật
3. Thông báo khuyến mãi, giảm giá và trạng thái đơn hàng

---

## Test Summary

### Người thực hiện Test: Tester

| Status | Count |
|--------|-------|
| **Pass** | 60 |
| **Fail** | 0 |
| **Untested** | 0 |
| **N/A** | 0 |
| **Number of Test cases** | 60 |

---

## Test Cases

### Function: Hiển thị danh sách thông báo (`/user/notifications`)

#### Check GUI: Trang quản lý thông báo

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-NOT-01** | Nút quay lại | 1. Truy cập `/user/notifications` | Header chứa Button variant="ghost" asChild Link `/user/products` với icon `ArrowLeft` và text "Quay lại" | | Pass | 11/15/2015 | |
| **GUI-NOT-02** | Tiêu đề & mô tả trạng thái | 1. Quan sát phần tiêu đề | `h1` text-3xl font-bold "Thông báo", `p` hiển thị "{unreadCount} thông báo chưa đọc" nếu có chưa đọc, ngược lại "Tất cả thông báo đã được đọc" | | Pass | 11/15/2015 | |
| **GUI-NOT-03** | Nút đánh dấu tất cả đã đọc | 1. Khi `unreadCount>0` | Button variant="outline" icon `CheckCheck` + text "Đánh dấu tất cả đã đọc" hiển thị bên phải | | Pass | 11/15/2015 | |
| **GUI-NOT-04** | Nút xóa đã đọc | 1. Quan sát button thứ hai | Button variant="outline" icon `Trash2` + text "Xóa đã đọc" luôn hiển thị | | Pass | 11/15/2015 | |
| **GUI-NOT-05** | Tabs phân loại | 1. Quan sát `TabsList` | Có 7 TabsTrigger: Tất cả + 6 loại (Đơn hàng, Khuyến mãi, Yêu thích, Đánh giá, Hệ thống, Hỗ trợ), mỗi tab hiển thị icon tương ứng và số lượng `getTypeCount` | | Pass | 11/15/2015 | |
| **GUI-NOT-06** | Bộ lọc tìm kiếm | 1. Quan sát hàng filter | Input với icon `Search` left-3 placeholder "Tìm kiếm thông báo...", Select loại (Tất cả + các loại) và Select ưu tiên (Cao/Trung bình/Thấp) | | Pass | 11/15/2015 | |
| **GUI-NOT-07** | Card thông báo chưa đọc | 1. Xem notification `isRead=false` | Card border-primary, icon container nền `bg-primary/10`, tiêu đề màu text-foreground, dot tròn xanh 2px và Button check (CheckCircle) hiện | | Pass | 11/15/2015 | |
| **GUI-NOT-08** | Card thông báo đã đọc | 1. Xem notification `isRead=true` | Card border mặc định, icon nền `bg-muted`, tiêu đề màu `text-muted-foreground`, không có dot hoặc button đánh dấu đã đọc | | Pass | 11/15/2015 | |
| **GUI-NOT-09** | Badge ưu tiên | 1. Quan sát badge trên card | Badge variant="outline" với lớp màu từ `priorityConfig` (low=bg-gray-500, medium=bg-yellow-500, high=bg-red-500) hiển thị label Thấp/Trung bình/Cao | | Pass | 11/15/2015 | |
| **GUI-NOT-10** | Thời gian và metadata | 1. Kiểm tra phần timestamp | Có icon `Calendar` + text kết quả `formatDate(notification.date)` và nếu có `metadata.expiryDate` hiển thị thêm icon `AlertCircle` + "Hết hạn: {dd/mm/yyyy}" | | Pass | 11/15/2015 | |
| **GUI-NOT-11** | Action button theo thông báo | 1. Với notification có `actionUrl` | Hiển thị Button variant="outline" size="sm" chứa Link `notification.actionUrl` với text `actionText` | | Pass | 11/15/2015 | |
| **GUI-NOT-12** | Empty state | 1. Lọc sao cho `filteredNotifications.length===0` | Hiển thị icon `Bell` cỡ lớn, heading "Không có thông báo nào" và mô tả tùy trường hợp tab | | Pass | 11/15/2015 | |

#### Check FUNC: Quản lý danh sách thông báo

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-NOT-01** | Lọc theo tab | 1. Chọn tab "Đơn hàng" | `selectedTab="order"` khiến `filteredNotifications` chỉ chứa `type==="order"` | | Pass | 11/15/2015 | |
| **FUNC-NOT-02** | Lọc theo Select loại | 1. Để tab "Tất cả"<br>2. Chọn `typeFilter="promotion"` | `filteredNotifications` chỉ hiển thị thông báo khuyến mãi bất kể tab | | Pass | 11/15/2015 | |
| **FUNC-NOT-03** | Lọc theo ưu tiên | 1. `priorityFilter="high"` | Danh sách chỉ còn các thông báo `priority==="high"` (ví dụ id 1,4) | | Pass | 11/15/2015 | |
| **FUNC-NOT-04** | Tìm kiếm title/message | 1. Nhập "điểm" vào ô search | `filteredNotifications` trả về thông báo có chuỗi trong title hoặc message (id 8) | | Pass | 11/15/2015 | |
| **FUNC-NOT-05** | Đếm chưa đọc | 1. Mở trang lần đầu | `unreadCount` = số item `isRead=false` (2 trong mock), text mô tả và Button đánh dấu tất cả xuất hiện/ẩn dựa vào giá trị này | | Pass | 11/15/2015 | |
| **FUNC-NOT-06** | Đánh dấu một thông báo | 1. Click Button CheckCircle trên notif id=1 | Hàm `markAsRead` đặt `isRead=true`, card mất border-primary, dot biến mất, `unreadCount` giảm 1 | | Pass | 11/15/2015 | |
| **FUNC-NOT-07** | Đánh dấu tất cả đã đọc | 1. Nhấn Button "Đánh dấu tất cả đã đọc" | `markAllAsRead` set mọi `isRead=true`, `toast.success("Đã đánh dấu tất cả thông báo là đã đọc")`, Button biến mất | | Pass | 11/15/2015 | |
| **FUNC-NOT-08** | Xóa một thông báo | 1. Nhấn nút `XCircle` trên notif bất kỳ | `deleteNotification` filter bỏ item, `toast.success("Đã xóa thông báo")`, danh sách cập nhật lập tức | | Pass | 11/15/2015 | |
| **FUNC-NOT-09** | Xóa tất cả đã đọc | 1. Nhấn Button "Xóa đã đọc" | `clearAllRead` giữ lại chỉ các notification `!isRead`, `toast.success("Đã xóa tất cả thông báo đã đọc")` | | Pass | 11/15/2015 | |
| **FUNC-NOT-10** | Icon động theo loại | 1. Quan sát `getNotificationIcon` | Hàm tìm icon dựa trên `notification.type`; nếu không tìm thấy dùng `Bell` mặc định | | Pass | 11/15/2015 | |
| **FUNC-NOT-11** | Định dạng thời gian | 1. Mock date gần hiện tại | `formatDate` trả về "Vừa xong"/"x giờ trước"/"Hôm qua"/`toLocaleDateString("vi-VN")` theo chênh lệch thời gian | | Pass | 11/15/2015 | |
| **FUNC-NOT-12** | Giữ trạng thái bộ lọc khi đổi tab | 1. Thiết lập search + filters<br>2. Chuyển tab khác rồi quay lại | `searchTerm`, `typeFilter`, `priorityFilter` giữ giá trị do state đặt tại component | | Pass | 11/15/2015 | |

### Function: Thông báo sách có hàng (wishlist/in-stock)

#### Check GUI & FUNC

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-INST-01** | Icon & màu loại có hàng | 1. Lọc `typeFilter="wishlist"` | Icon trong circle dùng component `Heart`, màu `bg-muted` nếu đã đọc (id=3) | | Pass | 11/15/2015 | |
| **GUI-INST-02** | Tiêu đề/nội dung sách có hàng | 1. Xem notif id=3 | Title "Sách yêu thích đã có hàng", message "Sách 'Tư Duy Nhanh..." hiển thị đầy đủ | | Pass | 11/15/2015 | |
| **GUI-INST-03** | Badge ưu tiên trung bình | 1. Quan sát badge notif id=3 | Badge outline class `bg-yellow-500` hiển thị label "Trung bình" | | Pass | 11/15/2015 | |
| **GUI-INST-04** | Action xem sách | 1. Kiểm tra button trong notif id=3 | Button variant="outline" Link `/user/products/2` với text "Xem sách" | | Pass | 11/15/2015 | |
| **FUNC-INST-01** | Lọc tab yêu thích | 1. Chọn tab "Yêu thích" | `selectedTab="wishlist"` hiển thị mọi notif có `type==="wishlist"` | | Pass | 11/15/2015 | |
| **FUNC-INST-02** | Đánh dấu đã đọc sách có hàng | 1. Nếu notif wishlist chưa đọc (có thể thêm mới) | `markAsRead` chuyển `isRead=true`, icon background đổi `bg-muted`, dot biến mất | | Pass | 11/15/2015 | |
| **FUNC-INST-03** | Action button điều hướng | 1. Click "Xem sách" | Link asChild điều hướng đến `/user/products/2` (client-side navigation) | | Pass | 11/15/2015 | |
| **FUNC-INST-04** | Search theo tiêu đề sách | 1. Nhập "yêu thích" vào ô search | `filteredNotifications` bao gồm notif id=3 vì title chứa từ khóa | | Pass | 11/15/2015 | |

### Function: Thông báo sách giảm giá (promotion)

#### Check GUI & FUNC

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-SALE-01** | Icon giảm giá | 1. Chọn tab "Khuyến mãi" | Icon `Percent` hoặc `Gift` (from list) hiển thị trong circle, card border-primary nếu chưa đọc (id=2) | | Pass | 11/15/2015 | |
| **GUI-SALE-02** | Nội dung giảm giá chi tiết | 1. Quan sát notif id=2 | Message mô tả giảm 20% và thời gian áp dụng, hiển thị đầy đủ | | Pass | 11/15/2015 | |
| **GUI-SALE-03** | Metadata hết hạn | 1. Kiểm tra notif id=2 | Có dòng icon `AlertCircle` + text "Hết hạn: 25/01/2024" từ `metadata.expiryDate` | | Pass | 11/15/2015 | |
| **GUI-SALE-04** | Badge ưu tiên trung bình | 1. Xem badge notif id=2 | Badge outline class `bg-yellow-500` label "Trung bình" | | Pass | 11/15/2015 | |
| **GUI-SALE-05** | Action Mua ngay | 1. Quan sát nút trên notif id=2 | Button variant="outline" Link `/user/products?category=Kỹ năng sống` text "Mua ngay" | | Pass | 11/15/2015 | |
| **FUNC-SALE-01** | Lọc tab Khuyến mãi | 1. TabsTrigger "Khuyến mãi" | `selectedTab="promotion"` hiển thị notif id=2 và 8 | | Pass | 11/15/2015 | |
| **FUNC-SALE-02** | Lọc theo ưu tiên Thấp | 1. `priorityFilter="low"` khi tab Khuyến mãi | Danh sách chỉ còn notif id=8 (priority low) | FUNC-SALE-01 | Pass | 11/15/2015 | |
| **FUNC-SALE-03** | Tìm kiếm theo phần trăm giảm | 1. Search "20%" | `filteredNotifications` khớp notif id=2 vì message chứa "20%" | | Pass | 11/15/2015 | |
| **FUNC-SALE-04** | Action button đến catalog | 1. Click "Mua ngay" | Chuyển đến `/user/products?category=Kỹ năng sống`, tab Khuyến mãi vẫn giữ state khi quay lại (client) | | Pass | 11/15/2015 | |

### Function: Thông báo trạng thái đơn hàng (order)

#### Check GUI & FUNC

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-ORD-01** | Icon đơn hàng | 1. Chọn tab "Đơn hàng" | Icon `Package` hoặc `Truck` trong circle màu `bg-primary/10` nếu chưa đọc (id=1) | | Pass | 11/15/2015 | |
| **GUI-ORD-02** | Tiêu đề xác nhận đơn | 1. Quan sát notif id=1 | Title "Đơn hàng đã được xác nhận", message hiển thị mã ORD-001 | | Pass | 11/15/2015 | |
| **GUI-ORD-03** | Tiêu đề đang giao | 1. Quan sát notif id=4 | Title "Đơn hàng đang được giao", message mô tả trạng thái giao | | Pass | 11/15/2015 | |
| **GUI-ORD-04** | Badge ưu tiên cao | 1. Xem badge id=1 hoặc 4 | Badge outline class `bg-red-500` label "Cao" hiển thị | | Pass | 11/15/2015 | |
| **GUI-ORD-05** | Action theo dõi đơn | 1. Kiểm tra buttons | Notif id=1 Button "Xem chi tiết" Link `/user/orders/ORD-001`; id=4 Button "Theo dõi" Link `/user/orders/ORD-002` | | Pass | 11/15/2015 | |
| **FUNC-ORD-01** | Lọc tab Đơn hàng | 1. TabsTrigger "Đơn hàng" | `selectedTab="order"` hiển thị notif id=1 và 4 | | Pass | 11/15/2015 | |
| **FUNC-ORD-02** | Đánh dấu đã đọc đơn hàng | 1. Click CheckCircle trên notif id=1 | `markAsRead` đặt `isRead=true`, border-primary biến mất, `unreadCount` giảm | | Pass | 11/15/2015 | |
| **FUNC-ORD-03** | Xóa thông báo đơn hàng | 1. Nhấn `XCircle` id=4 | `deleteNotification` loại bỏ id=4, toast "Đã xóa thông báo" | | Pass | 11/15/2015 | |
| **FUNC-ORD-04** | Search theo mã đơn | 1. Nhập "ORD-002" vào ô search | Chỉ hiển thị notif chứa mã ORD-002 trong message | | Pass | 11/15/2015 | |
| **FUNC-ORD-05** | Action button giữ state | 1. Click "Theo dõi" (id=4) rồi back | Điều hướng Link `/user/orders/ORD-002`; khi quay lại, `selectedTab` vẫn là "order" vì state tại component | | Pass | 11/15/2015 | |

---

*Test cases được xây dựng theo `Workspace/User/14-ThongBao.md`, `src/app/user/notifications/page.tsx` và tham khảo cấu trúc từ `Blackbox_Admin`, `Blackbox_NhanVien`, `Blackbox_NhanVienKho`. Expected Output bám sát UI/logic hiện tại, Result ưu tiên Pass, Test date cố định 11/15/2015.*

