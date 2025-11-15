# BLACKBOX TEST CASE - ADMIN FUNCTIONS

**Dự án:** Hệ Thống Quản Lý Model Shop  
**Ngày tạo:** 2025  
**Mục đích:** Tài liệu tổng quan về các chức năng Admin và routes để thực hiện blackbox testing

---

## BẢNG TỔNG HỢP TEST CASE

| No | Function Name | Sheet Name | Description | Pre-Condition (Route) |
|----|---------------|------------|-------------|----------------------|
| **1. QUẢN LÝ TÀI KHOẢN** |
| 1 | Function - Đăng nhập (Admin) | Quản lý tài khoản Admin | Check GUI and FUNC login function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Đăng nhập] hoặc truy cập `/admin/auth/login` |
| 2 | Function - Đăng ký (Admin) | Quản lý tài khoản Admin | Check GUI and FUNC register function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Đăng ký] hoặc truy cập `/admin/auth/register` |
| 3 | Function - Đổi mật khẩu (Admin) | Quản lý tài khoản Admin | Check GUI and FUNC change password function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý tài khoản] 2. Click [Đổi mật khẩu] hoặc truy cập `/admin/account` |
| 4 | Function - Cập nhật thông tin cá nhân (Admin) | Quản lý tài khoản Admin | Check GUI and FUNC update personal information function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý tài khoản] 2. Click [Chỉnh sửa] hoặc truy cập `/admin/account` |
| 4.1 | Function - Khôi phục mật khẩu (Admin) | Quản lý tài khoản Admin | Check GUI and FUNC forgot password function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Đăng nhập] 2. Click [Quên mật khẩu] hoặc truy cập `/admin/auth/forgot-password` |
| 4.2 | Function - Đăng xuất (Admin) | Quản lý tài khoản Admin | Check GUI and FUNC logout function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Đăng xuất] hoặc truy cập `/admin/logout` |
| 4.3 | Layout - Quản lý tài khoản (Admin) | [Layout Quản lý Tài khoản Admin](1.%20Quản%20lý%20tài%20khoản%20(Admin).md) | GUI chức năng Quản lý tài khoản Admin | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý tài khoản] hoặc truy cập `/admin/account` |
| **2. QUẢN LÝ SẢN PHẨM** |
| 5 | Function - Hiển thị danh sách sản phẩm (Admin) | Quản lý sản phẩm Admin | Check GUI and FUNC display product list function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý mô hình] hoặc truy cập `/admin/products` |
| 6 | Function - Xem chi tiết sản phẩm (Admin) | Quản lý sản phẩm Admin | Check GUI and FUNC view product details function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý mô hình] 2. Click [Xem] hoặc truy cập `/admin/products/[id]` |
| 7 | Function - Thêm sản phẩm (Admin) | Quản lý sản phẩm Admin | Check GUI and FUNC add product function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý mô hình] 2. Click [Thêm sản phẩm] hoặc truy cập `/admin/products/new` |
| 8 | Function - Cập nhật sản phẩm (Admin) | Quản lý sản phẩm Admin | Check GUI and FUNC update product function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý mô hình] 2. Click [Chỉnh sửa] hoặc truy cập `/admin/products/[id]/edit` |
| 9 | Function - Xóa sản phẩm (Admin) | Quản lý sản phẩm Admin | Check GUI and FUNC delete product function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý mô hình] 2. Click [Xóa] |
| 9.1 | Function - Tìm kiếm sản phẩm (Admin) | Quản lý sản phẩm Admin | Check GUI and FUNC search products function (Admin) | Tại Trang danh sách sản phẩm: 1. Nhập từ khóa vào ô tìm kiếm |
| 9.2 | Function - Lọc sản phẩm (Admin) | Quản lý sản phẩm Admin | Check GUI and FUNC filter products function (Admin) | Tại Trang danh sách sản phẩm: 1. Chọn danh mục, thương hiệu, trạng thái từ dropdown |
| 9.3 | Layout - Quản lý sản phẩm (Admin) | [Layout Quản lý Sản phẩm Admin](2.%20Quản%20lý%20sản%20phẩm%20(Admin).md) | GUI chức năng Quản lý sản phẩm Admin | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý mô hình] hoặc truy cập `/admin/products` |
| **3. QUẢN LÝ TỒN KHO** |
| 10 | Function - Hiển thị danh sách tồn kho (Admin) | Quản lý tồn kho Admin | Check GUI and FUNC display inventory list function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý tồn kho] hoặc truy cập `/admin/inventory` |
| 11 | Function - Xem chi tiết tồn kho (Admin) | Quản lý tồn kho Admin | Check GUI and FUNC view inventory details function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý tồn kho] 2. Click [Xem] hoặc truy cập `/admin/inventory/[id]` |
| 12 | Function - Cập nhật tồn kho (Admin) | Quản lý tồn kho Admin | Check GUI and FUNC update inventory function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý tồn kho] 2. Click [Chỉnh sửa] hoặc truy cập `/admin/inventory/[id]/edit` |
| 13 | Function - Nhập hàng mới (Admin) | Quản lý tồn kho Admin | Check GUI and FUNC import inventory function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý tồn kho] 2. Click [Nhập hàng] hoặc truy cập `/admin/inventory/new` |
| 14 | Function - Cảnh báo tồn kho thấp (Admin) | Quản lý tồn kho Admin | Check GUI and FUNC inventory alerts function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý tồn kho] 2. Click [Cảnh báo] hoặc truy cập `/admin/inventory/alerts` |
| 15 | Function - Kiểm kê tồn kho (Admin) | Quản lý tồn kho Admin | Check GUI and FUNC inventory audit function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý tồn kho] 2. Click [Kiểm kê] hoặc truy cập `/admin/inventory/audit` |
| 16 | Function - Nhập kho (Admin) | Quản lý tồn kho Admin | Check GUI and FUNC import inventory function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý tồn kho] 2. Click [Nhập kho] hoặc truy cập `/admin/inventory/import` |
| 16.1 | Layout - Quản lý tồn kho (Admin) | [Layout Quản lý Tồn kho Admin](3.%20Quản%20lý%20tồn%20kho%20(Admin).md) | GUI chức năng Quản lý tồn kho Admin | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý tồn kho] hoặc truy cập `/admin/inventory` |
| **4. QUẢN LÝ ĐƠN HÀNG** |
| 17 | Function - Hiển thị danh sách đơn hàng (Admin) | Quản lý đơn hàng Admin | Check GUI and FUNC display order list function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Xử lý đơn hàng] hoặc truy cập `/admin/orders` |
| 18 | Function - Xem chi tiết đơn hàng (Admin) | Quản lý đơn hàng Admin | Check GUI and FUNC view order details function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Xử lý đơn hàng] 2. Click [Xem] hoặc truy cập `/admin/orders/[id]` |
| 19 | Function - Cập nhật đơn hàng (Admin) | Quản lý đơn hàng Admin | Check GUI and FUNC update order function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Xử lý đơn hàng] 2. Click [Cập nhật trạng thái] hoặc truy cập `/admin/orders/[id]/update-status` |
| 20 | Function - Xóa đơn hàng (Admin) | Quản lý đơn hàng Admin | Check GUI and FUNC delete order function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Xử lý đơn hàng] 2. Click [Hủy đơn hàng] hoặc truy cập `/admin/orders/[id]/cancel` |
| 21 | Function - Xác nhận đơn hàng (Admin) | Quản lý đơn hàng Admin | Check GUI and FUNC confirm order function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Xử lý đơn hàng] 2. Click [Xác nhận đơn hàng] hoặc truy cập `/admin/orders/[id]/confirm` |
| 22 | Function - In đơn hàng (Admin) | Quản lý đơn hàng Admin | Check GUI and FUNC print order function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Xử lý đơn hàng] 2. Click [In đơn hàng] hoặc truy cập `/admin/orders/[id]/print` |
| 23 | Function - Tạo đơn hàng mới (Admin) | Quản lý đơn hàng Admin | Check GUI and FUNC create new order function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Xử lý đơn hàng] 2. Click [Tạo đơn hàng mới] hoặc truy cập `/admin/orders/new` |
| 23.1 | Layout - Quản lý đơn hàng (Admin) | [Layout Quản lý Đơn hàng Admin](4.%20Quản%20lý%20đơn%20hàng%20(Admin).md) | GUI chức năng Quản lý đơn hàng Admin | Tại Menu Ứng dụng phía Admin: 1. Click [Xử lý đơn hàng] hoặc truy cập `/admin/orders` |
| **5. QUẢN LÝ NGƯỜI DÙNG** |
| 24 | Function - Tạo người dùng (Admin) | Quản lý người dùng Admin | Check GUI and FUNC create user function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý khách hàng] 2. Click [Tạo người dùng] hoặc truy cập `/admin/customers` |
| 25 | Function - Hiển thị danh sách người dùng (Admin) | Quản lý người dùng Admin | Check GUI and FUNC display user list function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý khách hàng] hoặc truy cập `/admin/customers` |
| 26 | Function - Xem chi tiết người dùng (Admin) | Quản lý người dùng Admin | Check GUI and FUNC view user details function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý khách hàng] 2. Click [Xem] hoặc truy cập `/admin/customers/[id]` |
| 27 | Function - Xóa người dùng (Admin) | Quản lý người dùng Admin | Check GUI and FUNC delete user function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý khách hàng] 2. Click [Xóa] |
| 28 | Function - Cập nhật người dùng (Admin) | Quản lý người dùng Admin | Check GUI and FUNC update user function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý khách hàng] 2. Click [Cập nhật] |
| 28.1 | Layout - Quản lý người dùng (Admin) | [Layout Quản lý Người dùng Admin](5.%20Quản%20lý%20người%20dùng%20(Admin).md) | GUI chức năng Quản lý người dùng Admin | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý khách hàng] hoặc truy cập `/admin/customers` |
| **6. YÊU CẦU ĐẶT HÀNG** |
| 29 | Function - Hiển thị danh sách yêu cầu đặt hàng (Admin) | Yêu cầu đặt hàng Admin | Check GUI and FUNC display special requests list function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Yêu cầu đặt hàng] hoặc truy cập `/admin/special-requests` |
| 30 | Function - Xem chi tiết yêu cầu đặt hàng (Admin) | Yêu cầu đặt hàng Admin | Check GUI and FUNC view special request details function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Yêu cầu đặt hàng] 2. Click [Xem] hoặc truy cập `/admin/special-requests/[id]` |
| 31 | Function - Xử lý yêu cầu đặt hàng (Admin) | Yêu cầu đặt hàng Admin | Check GUI and FUNC process special request function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Yêu cầu đặt hàng] 2. Click [Xem chi tiết] 3. Click [Xử lý] |
| 32 | Function - Cập nhật trạng thái yêu cầu đặt hàng (Admin) | Yêu cầu đặt hàng Admin | Check GUI and FUNC update special request status function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Yêu cầu đặt hàng] 2. Click [Xem chi tiết] 3. Click [Cập nhật trạng thái] |
| 32.1 | Layout - Yêu cầu đặt hàng (Admin) | [Layout Yêu cầu Đặt hàng Admin](6.%20Yêu%20cầu%20đặt%20hàng%20(Admin).md) | GUI chức năng Yêu cầu đặt hàng Admin | Tại Menu ứng dụng phía Admin: 1. Click [Yêu cầu đặt hàng] hoặc truy cập `/admin/special-requests` |
| **7. XỬ LÝ ĐẶT TRƯỚC** |
| 33 | Function - Hiển thị danh sách đặt trước (Admin) | Xử lý đặt trước Admin | Check GUI and FUNC display pre-orders list function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Quản lý đặt trước] hoặc truy cập `/admin/pre-orders` |
| 34 | Function - Xem chi tiết đặt trước (Admin) | Xử lý đặt trước Admin | Check GUI and FUNC view pre-order details function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Quản lý đặt trước] 2. Click [Xem] hoặc truy cập `/admin/pre-orders/[id]` |
| 35 | Function - Xử lý đặt trước (Admin) | Xử lý đặt trước Admin | Check GUI and FUNC process pre-order function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Quản lý đặt trước] 2. Click [Xử lý] hoặc truy cập `/admin/pre-orders/[id]/process` |
| 36 | Function - Cập nhật trạng thái đặt trước (Admin) | Xử lý đặt trước Admin | Check GUI and FUNC update pre-order status function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Quản lý đặt trước] 2. Click [Cập nhật trạng thái] hoặc truy cập `/admin/pre-orders/[id]/update-status` |
| 37 | Function - Thông báo có hàng (Admin) | Xử lý đặt trước Admin | Check GUI and FUNC notify stock function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Quản lý đặt trước] 2. Click [Thông báo có hàng] hoặc truy cập `/admin/pre-orders/[id]/notify-stock` |
| 37.1 | Layout - Xử lý đặt trước (Admin) | [Layout Xử lý Đặt trước Admin](7.%20Xử%20lý%20đặt%20trước%20(Admin).md) | GUI chức năng Xử lý đặt trước Admin | Tại Menu ứng dụng phía Admin: 1. Click [Quản lý đặt trước] hoặc truy cập `/admin/pre-orders` |
| **8. QUẢN LÝ HỖ TRỢ - LIÊN HỆ** |
| 38 | Function - Hiển thị danh sách yêu cầu hỗ trợ (Admin) | Quản lý hỗ trợ Admin | Check GUI and FUNC display support request list function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Hỗ trợ khách hàng] hoặc truy cập `/admin/support` |
| 39 | Function - Xem chi tiết yêu cầu hỗ trợ (Admin) | Quản lý hỗ trợ Admin | Check GUI and FUNC view support request details function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Hỗ trợ khách hàng] 2. Click [Xem] hoặc truy cập `/admin/support/[id]` |
| 40 | Function - Chat hỗ trợ khách hàng (Admin) | Quản lý hỗ trợ Admin | Check GUI and FUNC chat support function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Hỗ trợ khách hàng] 2. Click [Chat] hoặc truy cập `/admin/support/[id]/chat` |
| 41 | Function - Trả lời yêu cầu của khách hàng (Admin) | Quản lý hỗ trợ Admin | Check GUI and FUNC reply to customer request function (Admin) | Tại Menu ứng dụng: 1. Click [Hỗ trợ khách hàng] 2. Click [Trả lời] |
| 42 | Function - Xóa yêu cầu của khách hàng (Admin) | Quản lý hỗ trợ Admin | Check GUI and FUNC delete customer request function (Admin) | Tại Menu ứng dụng: 1. Click [Hỗ trợ khách hàng] 2. Click [Xóa yêu cầu] |
| 42.1 | Function - Export lịch sử chat (Admin) | Quản lý hỗ trợ Admin | Check GUI and FUNC export chat history function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Hỗ trợ khách hàng] 2. Click [Chat] 3. Click [Export lịch sử] |
| 42.2 | Function - Tìm kiếm trong chat (Admin) | Quản lý hỗ trợ Admin | Check GUI and FUNC search in chat function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Hỗ trợ khách hàng] 2. Click [Chat] 3. Sử dụng ô tìm kiếm trong chat |
| 42.3 | Function - Quản lý SLA và phân công (Admin) | Quản lý hỗ trợ Admin | Check GUI and FUNC SLA and assignment management function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Hỗ trợ khách hàng] 2. Click [Cài đặt SLA] |
| 42.4 | Layout - Quản lý hỗ trợ - liên hệ (Admin) | [Layout Quản lý Hỗ trợ - Liên hệ Admin](8.%20Quản%20lý%20hỗ%20trợ%20-%20liên%20hệ%20(Admin).md) | GUI chức năng Quản lý hỗ trợ - liên hệ Admin | Tại Menu ứng dụng phía Admin: 1. Click [Hỗ trợ khách hàng] hoặc truy cập `/admin/support` |
| **9. XỬ LÝ PHẢN HỒI - KHIẾU NẠI** |
| 43 | Function - Hiển thị danh sách phản hồi (Admin) | Xử lý phản hồi Admin | Check GUI and FUNC display complaints list function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Xử lý phản hồi] hoặc truy cập `/admin/complaints` |
| 44 | Function - Xem chi tiết phản hồi (Admin) | Xử lý phản hồi Admin | Check GUI and FUNC view complaint details function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Xử lý phản hồi] 2. Click [Xem] hoặc truy cập `/admin/complaints/[id]` |
| 45 | Function - Trả lời phản hồi (Admin) | Xử lý phản hồi Admin | Check GUI and FUNC reply complaint function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Xử lý phản hồi] 2. Click [Trả lời] hoặc truy cập `/admin/complaints/[id]/reply` |
| 46 | Function - Cập nhật trạng thái xử lý phản hồi (Admin) | Xử lý phản hồi Admin | Check GUI and FUNC update complaint status function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Xử lý phản hồi] 2. Click [Xem chi tiết] 3. Click [Cập nhật trạng thái] |
| 47 | Function - Phân loại khiếu nại (Admin) | Xử lý phản hồi Admin | Check GUI and FUNC classify complaint function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Xử lý phản hồi] 2. Click [Xem chi tiết] 3. Click [Phân loại] |
| 47.1 | Layout - Xử lý phản hồi - khiếu nại (Admin) | [Layout Xử lý Phản hồi - Khiếu nại Admin](9.%20Xử%20lý%20phản%20hồi%20-%20khiếu%20nại%20(Admin).md) | GUI chức năng Xử lý phản hồi - khiếu nại Admin | Tại Menu ứng dụng phía Admin: 1. Click [Xử lý phản hồi] hoặc truy cập `/admin/complaints` |
| **10. BÁO CÁO VÀ THỐNG KÊ** |
| 48 | Function - Xem báo cáo doanh thu (Admin) | Báo cáo và thống kê Admin | Check GUI and FUNC view revenue report function (Admin) | Tại Menu ứng dụng: 1. Click [Báo cáo & Thống kê] 2. Click [Xem doanh thu] hoặc truy cập `/admin/reports/revenue` |
| 49 | Function - Xem báo cáo chi phí (Admin) | Báo cáo và thống kê Admin | Check GUI and FUNC view expenses report function (Admin) | Tại Menu ứng dụng: 1. Click [Báo cáo & Thống kê] 2. Click [Xem chi phí] hoặc truy cập `/admin/reports` |
| 50 | Function - Xem báo cáo lợi nhuận (Admin) | Báo cáo và thống kê Admin | Check GUI and FUNC view profit report function (Admin) | Tại Menu ứng dụng: 1. Click [Báo cáo & Thống kê] 2. Click [Xem lợi nhuận] hoặc truy cập `/admin/reports/profit` |
| 51 | Function - Xem sản phẩm bán chạy (Admin) | Báo cáo và thống kê Admin | Check GUI and FUNC view top products report function (Admin) | Tại Menu ứng dụng: 1. Click [Báo cáo & Thống kê] 2. Click [Sản phẩm bán chạy] hoặc truy cập `/admin/reports/top-products` |
| 52 | Function - Xem thống kê khách hàng (Admin) | Báo cáo và thống kê Admin | Check GUI and FUNC view customers statistics function (Admin) | Tại Menu ứng dụng: 1. Click [Báo cáo & Thống kê] 2. Click [Thống kê khách hàng] hoặc truy cập `/admin/reports/customers` |
| 53 | Function - Xem báo cáo tồn kho (Admin) | Báo cáo và thống kê Admin | Check GUI and FUNC view inventory report function (Admin) | Tại Menu ứng dụng: 1. Click [Báo cáo & Thống kê] 2. Click [Báo cáo tồn kho] hoặc truy cập `/admin/reports/inventory` |
| 54 | Function - Tạo báo cáo tùy chỉnh (Admin) | Báo cáo và thống kê Admin | Check GUI and FUNC create custom report function (Admin) | Tại Menu ứng dụng: 1. Click [Báo cáo & Thống kê] 2. Click [Báo cáo nâng cao] hoặc truy cập `/admin/reports/advanced` |
| 54.1 | Layout - Báo cáo và thống kê (Admin) | [Layout Báo cáo và Thống kê Admin](10.%20Báo%20cáo%20và%20thống%20kê%20(Admin).md) | GUI chức năng Báo cáo và thống kê Admin | Tại Menu ứng dụng: 1. Click [Báo cáo & Thống kê] hoặc truy cập `/admin/reports` |
| **11. QUẢN LÝ ĐÁNH GIÁ** |
| 55 | Function - Xem đánh giá sản phẩm (Admin) | Quản lý đánh giá Admin | Check GUI and FUNC product review management function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Quản lý đánh giá] hoặc truy cập `/admin/reviews` |
| 56 | Function - Xem chi tiết đánh giá (Admin) | Quản lý đánh giá Admin | Check GUI and FUNC view review details function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Quản lý đánh giá] 2. Click [Xem chi tiết] hoặc truy cập `/admin/reviews/[id]` |
| 57 | Function - Duyệt đánh giá (Admin) | Quản lý đánh giá Admin | Check GUI and FUNC approve review function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Quản lý đánh giá] 2. Click [Duyệt] |
| 58 | Function - Từ chối đánh giá (Admin) | Quản lý đánh giá Admin | Check GUI and FUNC reject review function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Quản lý đánh giá] 2. Click [Từ chối] |
| 59 | Function - Xóa đánh giá sản phẩm (Admin) | Quản lý đánh giá Admin | Check GUI and FUNC delete product review function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Quản lý đánh giá] 2. Click [Xóa đánh giá] |
| 60 | Function - Phản hồi đánh giá (Admin) | Quản lý đánh giá Admin | Check GUI and FUNC reply to review function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Quản lý đánh giá] 2. Click [Xem chi tiết] 3. Click [Phản hồi] |
| 60.1 | Layout - Quản lý đánh giá (Admin) | [Layout Quản lý Đánh giá Admin](11.%20Quản%20lý%20đánh%20giá%20(Admin).md) | GUI chức năng Quản lý đánh giá Admin | Tại Menu ứng dụng phía Admin: 1. Click [Quản lý đánh giá] hoặc truy cập `/admin/reviews` |
| **12. CÀI ĐẶT HỆ THỐNG** |
| 61 | Function - Cài đặt chính sách giảm giá sản phẩm (Admin) | Cài đặt hệ thống Admin | Check GUI and FUNC product discount policy function (Admin) | Tại Menu ứng dụng: 1. Click [Cài đặt hệ thống] 2. Click [Giảm giá sản phẩm] hoặc truy cập `/admin/settings/product-discounts` |
| 62 | Function - Cài đặt chính sách giảm giá toàn bộ (Admin) | Cài đặt hệ thống Admin | Check GUI and FUNC global discount policy function (Admin) | Tại Menu ứng dụng: 1. Click [Cài đặt hệ thống] 2. Click [Giảm giá toàn bộ] hoặc truy cập `/admin/settings/global-discounts` |
| 63 | Function - Cài đặt thanh toán (Admin) | Cài đặt hệ thống Admin | Check GUI and FUNC payment settings function (Admin) | Tại Menu ứng dụng: 1. Click [Cài đặt hệ thống] 2. Click [Cài đặt thanh toán] hoặc truy cập `/admin/settings/payments` |
| 64 | Function - Cài đặt thông tin shop (Admin) | Cài đặt hệ thống Admin | Check GUI and FUNC shop information function (Admin) | Tại Menu ứng dụng: 1. Click [Cài đặt hệ thống] 2. Click [Thông tin shop] hoặc truy cập `/admin/settings/shop` |
| 65 | Function - Cài đặt chung (Admin) | Cài đặt hệ thống Admin | Check GUI and FUNC general settings function (Admin) | Tại Menu ứng dụng: 1. Click [Cài đặt hệ thống] hoặc truy cập `/admin/settings` |
| 65.1 | Layout - Cài đặt hệ thống (Admin) | [Layout Cài đặt Hệ thống Admin](12.%20Cài%20đặt%20hệ%20thống%20(Admin).md) | GUI chức năng Cài đặt hệ thống Admin | Tại Menu ứng dụng: 1. Click [Cài đặt hệ thống] hoặc truy cập `/admin/settings` |
| **13. QUẢN LÝ BÀI VIẾT** |
| 66 | Function - Hiển thị danh sách bài viết (Admin) | Quản lý bài viết Admin | Check GUI and FUNC display posts list function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Quản lý bài viết] hoặc truy cập `/admin/posts` |
| 67 | Function - Xem chi tiết bài viết (Admin) | Quản lý bài viết Admin | Check GUI and FUNC view post details function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Quản lý bài viết] 2. Click [Xem] hoặc truy cập `/admin/posts/[id]` |
| 68 | Function - Xóa bài viết (Admin) | Quản lý bài viết Admin | Check GUI and FUNC delete post function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Quản lý bài viết] 2. Click [Xóa] |
| 69 | Function - Chỉnh sửa bài viết (Admin) | Quản lý bài viết Admin | Check GUI and FUNC edit post function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Quản lý bài viết] 2. Click [Xem chi tiết] 3. Click [Chỉnh sửa] |
| 70 | Function - Xóa bình luận (Admin) | Quản lý bài viết Admin | Check GUI and FUNC delete comment function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Quản lý bài viết] 2. Click [Xem chi tiết] 3. Click [Xóa bình luận] |
| 71 | Function - Khóa tài khoản đăng bài (Admin) | Quản lý bài viết Admin | Check GUI and FUNC ban user posting function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Quản lý bài viết] 2. Click [Xem chi tiết] 3. Click [Khóa tài khoản] |
| 72 | Function - Tìm kiếm và lọc bài viết (Admin) | Quản lý bài viết Admin | Check GUI and FUNC search and filter posts function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Quản lý bài viết] 2. Sử dụng bộ lọc và tìm kiếm |
| 72.1 | Layout - Quản lý bài viết (Admin) | [Layout Quản lý Bài viết Admin](13.%20Quản%20lý%20bài%20viết%20(Admin).md) | GUI chức năng Quản lý bài viết Admin | Tại Menu ứng dụng phía Admin: 1. Click [Quản lý bài viết] hoặc truy cập `/admin/posts` |
| **14. BẢO MẬT** |
| 73 | Function - Xem lịch sử đăng nhập (Admin) | Bảo mật Admin | Check GUI and FUNC login history function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Bảo mật] 2. Click [Lịch sử đăng nhập] hoặc truy cập `/admin/security/login-history` |
| 74 | Function - Quản lý phiên đăng nhập (Admin) | Bảo mật Admin | Check GUI and FUNC sessions management function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Bảo mật] 2. Click [Phiên đăng nhập] hoặc truy cập `/admin/security/sessions` |
| 75 | Function - Phát hiện đăng nhập lạ (Admin) | Bảo mật Admin | Check GUI and FUNC detect suspicious login function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Bảo mật] 2. Click [Lịch sử đăng nhập] - Hệ thống tự động phát hiện và cảnh báo |
| 76 | Function - Auto logout khi hết hạn (Admin) | Bảo mật Admin | Check GUI and FUNC auto logout on timeout function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Bảo mật] 2. Click [Phiên đăng nhập] - Hệ thống tự động đăng xuất khi timeout |
| 76.1 | Layout - Bảo mật (Admin) | [Layout Bảo mật Admin](14.%20Bảo%20mật%20(Admin).md) | GUI chức năng Bảo mật Admin | Tại Menu ứng dụng phía Admin: 1. Click [Bảo mật] hoặc truy cập `/admin/security` |
| **15. THÔNG BÁO** |
| 77 | Function - Quản lý thông báo (Admin) | Thông báo Admin | Check GUI and FUNC notifications management function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Quản lý thông báo] hoặc truy cập `/admin/notifications` |
| 77.1 | Layout - Thông báo (Admin) | [Layout Thông báo Admin](15.%20Thông%20báo%20(Admin).md) | GUI chức năng Thông báo Admin | Tại Menu ứng dụng phía Admin: 1. Click [Quản lý thông báo] hoặc truy cập `/admin/notifications` |

---

## GHI CHÚ QUAN TRỌNG

### Về Routes:
- Tất cả routes được xác định dựa trên cấu trúc thư mục `src/app/admin/`
- Routes có thể truy cập trực tiếp qua URL hoặc thông qua menu navigation
- Routes động (có `[id]`) cần thay thế `[id]` bằng ID thực tế khi test
- Ví dụ: `/admin/products/1` thay vì `/admin/products/[id]`

### Về Pre-Condition:
- Pre-Condition mô tả các bước điều hướng từ menu hoặc URL trực tiếp
- Có thể kết hợp cả hai cách: click menu hoặc truy cập URL trực tiếp
- Tất cả chức năng Admin yêu cầu đăng nhập trước khi truy cập
- Admin cần có quyền truy cập các chức năng tương ứng

### Về Test Cases:
- Mỗi function có thể có nhiều test case con (GUI test, Functional test, Validation test, Integration test, etc.)
- Cần bổ sung thêm các test case chi tiết cho từng function trong các sheet riêng
- Test cases cần bao gồm: Test ID, Test Description, Pre-Condition, Test Steps, Test Data, Expected Result, Actual Result, Status, Priority
- Các loại test case cần có:
  - **GUI Test**: Kiểm tra giao diện, layout, responsive
  - **Functional Test**: Kiểm tra chức năng hoạt động đúng
  - **Validation Test**: Kiểm tra validation input, error handling
  - **Boundary Test**: Kiểm tra giá trị biên
  - **Negative Test**: Kiểm tra các trường hợp lỗi
  - **Integration Test**: Kiểm tra tích hợp giữa các module

### Về Test Data:
- Cần chuẩn bị test data cho các trường hợp:
  - Tài khoản Admin hợp lệ và không hợp lệ
  - Sản phẩm có hàng và hết hàng
  - Đơn hàng ở các trạng thái khác nhau
  - Khách hàng với các hạng thành viên khác nhau
  - Đánh giá ở các trạng thái khác nhau (Chờ duyệt, Đã duyệt, Từ chối)

### Về Test Environment:
- **Development Environment**: `http://localhost:3000`
- **Staging Environment**: `https://staging.modelshop.com`
- **Production Environment**: `https://modelshop.com`
- Cần test trên các trình duyệt: Chrome, Firefox, Safari, Edge
- Cần test trên các thiết bị: Desktop, Tablet, Mobile

### Về Priority:
- **P0 - Critical**: Các chức năng cốt lõi (Đăng nhập, Quản lý đơn hàng, Quản lý sản phẩm)
- **P1 - High**: Các chức năng quan trọng (Quản lý tồn kho, Quản lý khách hàng, Báo cáo)
- **P2 - Medium**: Các chức năng hỗ trợ (Quản lý đánh giá, Quản lý bài viết, Hỗ trợ)
- **P3 - Low**: Các chức năng bổ sung (Thông báo, Cài đặt hệ thống)

---

## THỐNG KÊ TEST CASE

**Tổng số chức năng Admin:** 78 functions

**Phân loại theo 15 mục chức năng:**
1. **Quản lý tài khoản:** 7 functions (1-4.3)
2. **Quản lý sản phẩm:** 9 functions (5-9.3)
3. **Quản lý tồn kho:** 8 functions (10-16.1)
4. **Quản lý đơn hàng:** 8 functions (17-23.1)
5. **Quản lý người dùng:** 6 functions (24-28.1)
6. **Yêu cầu đặt hàng:** 5 functions (29-32.1)
7. **Xử lý đặt trước:** 6 functions (33-37.1)
8. **Quản lý hỗ trợ - liên hệ:** 9 functions (38-42.4)
9. **Xử lý phản hồi - khiếu nại:** 6 functions (43-47.1)
10. **Báo cáo và thống kê:** 8 functions (48-54.1)
11. **Quản lý đánh giá:** 7 functions (55-60.1)
12. **Cài đặt hệ thống:** 6 functions (61-65.1)
13. **Quản lý bài viết:** 8 functions (66-72.1)
14. **Bảo mật:** 5 functions (73-76.1)
15. **Thông báo:** 2 functions (77-77.1)

---

**Người tạo:** Testing Team  
**Ngày cập nhật:** 2025-01-20  
**Phiên bản:** 1.0

