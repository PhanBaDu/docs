# BLACKBOX TEST CASE - TỔNG QUAN DỰ ÁN

**Dự án:** Hệ Thống Quản Lý Model Shop  
**Ngày tạo:** 2025  
**Mục đích:** Tài liệu tổng quan về các chức năng và routes để thực hiện blackbox testing

---

## BẢNG TỔNG HỢP TEST CASE

| No | Function Name | Sheet Name | Description | Pre-Condition (Route) |
|----|---------------|------------|-------------|----------------------|
| **ADMIN - QUẢN LÝ TÀI KHOẢN** |
| 1 | Function - Đăng nhập (Admin) | Quản lý tài khoản Admin | Check GUI and FUNC login function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Đăng nhập] hoặc truy cập `/admin/auth/login` |
| 2 | Function - Đăng ký (Admin) | Quản lý tài khoản Admin | Check GUI and FUNC register function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Đăng ký] hoặc truy cập `/admin/auth/register` |
| 3 | Function - Đổi mật khẩu (Admin) | Quản lý tài khoản Admin | Check GUI and FUNC change password function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý tài khoản] 2. Click [Đổi mật khẩu] hoặc truy cập `/admin/account` |
| 4 | Layout - Quản lý thông tin cá nhân (Admin) | Quản lý tài khoản Admin | GUI function for Admin personal information management | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý tài khoản] hoặc truy cập `/admin/account` |
| 4.1 | Function - Khôi phục mật khẩu (Admin) | Quản lý tài khoản Admin | Check GUI and FUNC forgot password function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Đăng nhập] 2. Click [Quên mật khẩu] hoặc truy cập `/admin/auth/forgot-password` |
| **ADMIN - QUẢN LÝ ĐƠN HÀNG** |
| 5 | Function - Hiển thị danh sách đơn hàng (Admin) | Quản lý đơn hàng Admin | Check GUI and FUNC display order list function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Xử lý đơn hàng] hoặc truy cập `/admin/orders` |
| 6 | Function - Xem chi tiết đơn hàng (Admin) | Quản lý đơn hàng Admin | Check GUI and FUNC view order details function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Xử lý đơn hàng] 2. Click [Xem] hoặc truy cập `/admin/orders/[id]` |
| 7 | Function - Cập nhật đơn hàng (Admin) | Quản lý đơn hàng Admin | Check GUI and FUNC update order function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Xử lý đơn hàng] 2. Click [Cập nhật trạng thái] hoặc truy cập `/admin/orders/[id]/update-status` |
| 8 | Function - Xóa đơn hàng (Admin) | Quản lý đơn hàng Admin | Check GUI and FUNC delete order function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Xử lý đơn hàng] 2. Click [Hủy đơn hàng] hoặc truy cập `/admin/orders/[id]/cancel` |
| 9 | Function - Xác nhận đơn hàng (Admin) | Quản lý đơn hàng Admin | Check GUI and FUNC confirm order function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Xử lý đơn hàng] 2. Click [Xác nhận đơn hàng] hoặc truy cập `/admin/orders/[id]/confirm` |
| 10 | Function - In đơn hàng (Admin) | Quản lý đơn hàng Admin | Check GUI and FUNC print order function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Xử lý đơn hàng] 2. Click [In đơn hàng] hoặc truy cập `/admin/orders/[id]/print` |
| 10.1 | Function - Tạo đơn hàng mới (Admin) | Quản lý đơn hàng Admin | Check GUI and FUNC create new order function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Xử lý đơn hàng] 2. Click [Tạo đơn hàng mới] hoặc truy cập `/admin/orders/new` |
| **ADMIN - QUẢN LÝ NGƯỜI DÙNG** |
| 11 | Function - Tạo người dùng (Admin) | Quản lý người dùng Admin | Check GUI and FUNC create user function | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý khách hàng] 2. Click [Tạo người dùng] hoặc truy cập `/admin/customers` |
| 12 | Function - Hiển thị danh sách người dùng (Admin) | Quản lý người dùng Admin | Check GUI and FUNC display user list function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý khách hàng] hoặc truy cập `/admin/customers` |
| 13 | Function - Xem chi tiết người dùng (Admin) | Quản lý người dùng Admin | Check GUI and FUNC view user details function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý khách hàng] 2. Click [Xem] hoặc truy cập `/admin/customers/[id]` |
| 14 | Function - Xóa người dùng (Admin) | Quản lý người dùng Admin | Check GUI and FUNC delete user function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý khách hàng] 2. Click [Xóa] |
| 15 | Function - Cập nhật người dùng (Admin) | Quản lý người dùng Admin | Check GUI and FUNC update user function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý khách hàng] 2. Click [Cập nhật] |
| **ADMIN - QUẢN LÝ SẢN PHẨM** |
| 16 | Function - Hiển thị danh sách sản phẩm (Admin) | Quản lý sản phẩm Admin | Check GUI and FUNC display product list function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý mô hình] hoặc truy cập `/admin/products` |
| 17 | Function - Xem chi tiết sản phẩm (Admin) | Quản lý sản phẩm Admin | Check GUI and FUNC view product details function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý mô hình] 2. Click [Xem] hoặc truy cập `/admin/products/[id]` |
| 18 | Function - Thêm sản phẩm (Admin) | Quản lý sản phẩm Admin | Check GUI and FUNC add product function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý mô hình] 2. Click [Thêm sản phẩm] hoặc truy cập `/admin/products/new` |
| 19 | Function - Cập nhật sản phẩm (Admin) | Quản lý sản phẩm Admin | Check GUI and FUNC update product function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý mô hình] 2. Click [Chỉnh sửa] hoặc truy cập `/admin/products/[id]/edit` |
| 20 | Function - Xóa sản phẩm (Admin) | Quản lý sản phẩm Admin | Check GUI and FUNC delete product function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý mô hình] 2. Click [Xóa] |
| **ADMIN - QUẢN LÝ TỒN KHO** |
| 21 | Function - Hiển thị danh sách tồn kho (Admin) | Quản lý tồn kho Admin | Check GUI and FUNC display inventory list function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý tồn kho] hoặc truy cập `/admin/inventory` |
| 22 | Function - Xem chi tiết tồn kho (Admin) | Quản lý tồn kho Admin | Check GUI and FUNC view inventory details function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý tồn kho] 2. Click [Xem] hoặc truy cập `/admin/inventory/[id]` |
| 23 | Function - Cập nhật tồn kho (Admin) | Quản lý tồn kho Admin | Check GUI and FUNC update inventory function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý tồn kho] 2. Click [Chỉnh sửa] hoặc truy cập `/admin/inventory/[id]/edit` |
| 24 | Function - Nhập hàng mới (Admin) | Quản lý tồn kho Admin | Check GUI and FUNC import inventory function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý tồn kho] 2. Click [Nhập hàng] hoặc truy cập `/admin/inventory/new` |
| 25 | Function - Cảnh báo tồn kho thấp (Admin) | Quản lý tồn kho Admin | Check GUI and FUNC inventory alerts function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý tồn kho] 2. Click [Cảnh báo] hoặc truy cập `/admin/inventory/alerts` |
| 26 | Function - Kiểm kê tồn kho (Admin) | Quản lý tồn kho Admin | Check GUI and FUNC inventory audit function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý tồn kho] 2. Click [Kiểm kê] hoặc truy cập `/admin/inventory/audit` |
| 27 | Function - Nhập kho (Admin) | Quản lý tồn kho Admin | Check GUI and FUNC import inventory function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý tồn kho] 2. Click [Nhập kho] hoặc truy cập `/admin/inventory/import` |
| **ADMIN - QUẢN LÝ ĐÁNH GIÁ** |
| 28 | Function - Xem đánh giá sản phẩm (Admin) | Quản lý đánh giá Admin | Check GUI and FUNC product review management function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Quản lý đánh giá] hoặc truy cập `/admin/reviews` |
| 29 | Function - Xem chi tiết đánh giá (Admin) | Quản lý đánh giá Admin | Check GUI and FUNC view review details function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Quản lý đánh giá] 2. Click [Xem chi tiết] hoặc truy cập `/admin/reviews/[id]` |
| 30 | Function - Duyệt đánh giá (Admin) | Quản lý đánh giá Admin | Check GUI and FUNC approve review function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Quản lý đánh giá] 2. Click [Duyệt] |
| 31 | Function - Từ chối đánh giá (Admin) | Quản lý đánh giá Admin | Check GUI and FUNC reject review function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Quản lý đánh giá] 2. Click [Từ chối] |
| 32 | Function - Xóa đánh giá sản phẩm (Admin) | Quản lý đánh giá Admin | Check GUI and FUNC delete product review function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Quản lý đánh giá] 2. Click [Xóa đánh giá] |
| 32.1 | Function - Phản hồi đánh giá (Admin) | Quản lý đánh giá Admin | Check GUI and FUNC reply to review function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Quản lý đánh giá] 2. Click [Xem chi tiết] 3. Click [Phản hồi] |
| **ADMIN - HỖ TRỢ KHÁCH HÀNG** |
| 33 | Function - Hiển thị danh sách yêu cầu hỗ trợ (Admin) | Quản lý hỗ trợ Admin | Check GUI and FUNC display support request list function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Hỗ trợ khách hàng] hoặc truy cập `/admin/support` |
| 34 | Function - Xem chi tiết yêu cầu hỗ trợ (Admin) | Quản lý hỗ trợ Admin | Check GUI and FUNC view support request details function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Hỗ trợ khách hàng] 2. Click [Xem] hoặc truy cập `/admin/support/[id]` |
| 35 | Function - Chat hỗ trợ khách hàng (Admin) | Quản lý hỗ trợ Admin | Check GUI and FUNC chat support function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Hỗ trợ khách hàng] 2. Click [Chat] hoặc truy cập `/admin/support/[id]/chat` |
| 36 | Function - Trả lời yêu cầu của khách hàng (Admin) | Quản lý hỗ trợ Admin | Check GUI and FUNC reply to customer request function (Admin) | Tại Menu ứng dụng: 1. Click [Hỗ trợ khách hàng] 2. Click [Trả lời] |
| 37 | Function - Xóa yêu cầu của khách hàng (Admin) | Quản lý hỗ trợ Admin | Check GUI and FUNC delete customer request function (Admin) | Tại Menu ứng dụng: 1. Click [Hỗ trợ khách hàng] 2. Click [Xóa yêu cầu] |
| 37.1 | Function - Export lịch sử chat (Admin) | Quản lý hỗ trợ Admin | Check GUI and FUNC export chat history function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Hỗ trợ khách hàng] 2. Click [Chat] 3. Click [Export lịch sử] |
| 37.2 | Function - Tìm kiếm trong chat (Admin) | Quản lý hỗ trợ Admin | Check GUI and FUNC search in chat function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Hỗ trợ khách hàng] 2. Click [Chat] 3. Sử dụng ô tìm kiếm trong chat |
| 37.3 | Function - Quản lý SLA và phân công (Admin) | Quản lý hỗ trợ Admin | Check GUI and FUNC SLA and assignment management function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Hỗ trợ khách hàng] 2. Click [Cài đặt SLA] |
| **ADMIN - XỬ LÝ PHẢN HỒI - KHIẾU NẠI** |
| 38 | Function - Hiển thị danh sách phản hồi (Admin) | Xử lý phản hồi Admin | Check GUI and FUNC display complaints list function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Xử lý phản hồi] hoặc truy cập `/admin/complaints` |
| 39 | Function - Xem chi tiết phản hồi (Admin) | Xử lý phản hồi Admin | Check GUI and FUNC view complaint details function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Xử lý phản hồi] 2. Click [Xem] hoặc truy cập `/admin/complaints/[id]` |
| 40 | Function - Trả lời phản hồi (Admin) | Xử lý phản hồi Admin | Check GUI and FUNC reply complaint function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Xử lý phản hồi] 2. Click [Trả lời] hoặc truy cập `/admin/complaints/[id]/reply` |
| 40.1 | Function - Cập nhật trạng thái xử lý phản hồi (Admin) | Xử lý phản hồi Admin | Check GUI and FUNC update complaint status function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Xử lý phản hồi] 2. Click [Xem chi tiết] 3. Click [Cập nhật trạng thái] |
| 40.2 | Function - Phân loại khiếu nại (Admin) | Xử lý phản hồi Admin | Check GUI and FUNC classify complaint function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Xử lý phản hồi] 2. Click [Xem chi tiết] 3. Click [Phân loại] |
| **ADMIN - QUẢN LÝ ĐẶT TRƯỚC** |
| 41 | Function - Hiển thị danh sách đặt trước (Admin) | Xử lý đặt trước Admin | Check GUI and FUNC display pre-orders list function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Quản lý đặt trước] hoặc truy cập `/admin/pre-orders` |
| 42 | Function - Xem chi tiết đặt trước (Admin) | Xử lý đặt trước Admin | Check GUI and FUNC view pre-order details function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Quản lý đặt trước] 2. Click [Xem] hoặc truy cập `/admin/pre-orders/[id]` |
| 43 | Function - Xử lý đặt trước (Admin) | Xử lý đặt trước Admin | Check GUI and FUNC process pre-order function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Quản lý đặt trước] 2. Click [Xử lý] hoặc truy cập `/admin/pre-orders/[id]/process` |
| 44 | Function - Cập nhật trạng thái đặt trước (Admin) | Xử lý đặt trước Admin | Check GUI and FUNC update pre-order status function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Quản lý đặt trước] 2. Click [Cập nhật trạng thái] hoặc truy cập `/admin/pre-orders/[id]/update-status` |
| 45 | Function - Thông báo có hàng (Admin) | Xử lý đặt trước Admin | Check GUI and FUNC notify stock function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Quản lý đặt trước] 2. Click [Thông báo có hàng] hoặc truy cập `/admin/pre-orders/[id]/notify-stock` |
| **ADMIN - YÊU CẦU ĐẶT HÀNG** |
| 46 | Function - Hiển thị danh sách yêu cầu đặt hàng (Admin) | Yêu cầu đặt hàng Admin | Check GUI and FUNC display special requests list function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Yêu cầu đặt hàng] hoặc truy cập `/admin/special-requests` |
| 47 | Function - Xem chi tiết yêu cầu đặt hàng (Admin) | Yêu cầu đặt hàng Admin | Check GUI and FUNC view special request details function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Yêu cầu đặt hàng] 2. Click [Xem] hoặc truy cập `/admin/special-requests/[id]` |
| 47.1 | Function - Xử lý yêu cầu đặt hàng (Admin) | Yêu cầu đặt hàng Admin | Check GUI and FUNC process special request function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Yêu cầu đặt hàng] 2. Click [Xem chi tiết] 3. Click [Xử lý] |
| 47.2 | Function - Cập nhật trạng thái yêu cầu đặt hàng (Admin) | Yêu cầu đặt hàng Admin | Check GUI and FUNC update special request status function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Yêu cầu đặt hàng] 2. Click [Xem chi tiết] 3. Click [Cập nhật trạng thái] |
| **ADMIN - QUẢN LÝ BÀI VIẾT** |
| 48 | Function - Hiển thị danh sách bài viết (Admin) | Quản lý bài viết Admin | Check GUI and FUNC display posts list function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Quản lý bài viết] hoặc truy cập `/admin/posts` |
| 49 | Function - Xem chi tiết bài viết (Admin) | Quản lý bài viết Admin | Check GUI and FUNC view post details function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Quản lý bài viết] 2. Click [Xem] hoặc truy cập `/admin/posts/[id]` |
| 50 | Function - Xóa bài viết (Admin) | Quản lý bài viết Admin | Check GUI and FUNC delete post function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Quản lý bài viết] 2. Click [Xóa] |
| 50.1 | Function - Chỉnh sửa bài viết (Admin) | Quản lý bài viết Admin | Check GUI and FUNC edit post function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Quản lý bài viết] 2. Click [Xem chi tiết] 3. Click [Chỉnh sửa] |
| 50.2 | Function - Xóa bình luận (Admin) | Quản lý bài viết Admin | Check GUI and FUNC delete comment function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Quản lý bài viết] 2. Click [Xem chi tiết] 3. Click [Xóa bình luận] |
| 50.3 | Function - Khóa tài khoản đăng bài (Admin) | Quản lý bài viết Admin | Check GUI and FUNC ban user posting function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Quản lý bài viết] 2. Click [Xem chi tiết] 3. Click [Khóa tài khoản] |
| 50.4 | Function - Tìm kiếm và lọc bài viết (Admin) | Quản lý bài viết Admin | Check GUI and FUNC search and filter posts function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Quản lý bài viết] 2. Sử dụng bộ lọc và tìm kiếm |
| **ADMIN - BÁO CÁO VÀ THỐNG KÊ** |
| 51 | Function - Xem báo cáo doanh thu (Admin) | Báo cáo và thống kê Admin | Check GUI and FUNC view revenue report function (Admin) | Tại Menu ứng dụng: 1. Click [Báo cáo & Thống kê] 2. Click [Xem doanh thu] hoặc truy cập `/admin/reports/revenue` |
| 52 | Function - Xem báo cáo chi phí (Admin) | Báo cáo và thống kê Admin | Check GUI and FUNC view expenses report function (Admin) | Tại Menu ứng dụng: 1. Click [Báo cáo & Thống kê] 2. Click [Xem chi phí] hoặc truy cập `/admin/reports` |
| 53 | Function - Xem báo cáo lợi nhuận (Admin) | Báo cáo và thống kê Admin | Check GUI and FUNC view profit report function (Admin) | Tại Menu ứng dụng: 1. Click [Báo cáo & Thống kê] 2. Click [Xem lợi nhuận] hoặc truy cập `/admin/reports/profit` |
| 54 | Function - Xem sản phẩm bán chạy (Admin) | Báo cáo và thống kê Admin | Check GUI and FUNC view top products report function (Admin) | Tại Menu ứng dụng: 1. Click [Báo cáo & Thống kê] 2. Click [Sản phẩm bán chạy] hoặc truy cập `/admin/reports/top-products` |
| 55 | Function - Xem thống kê khách hàng (Admin) | Báo cáo và thống kê Admin | Check GUI and FUNC view customers statistics function (Admin) | Tại Menu ứng dụng: 1. Click [Báo cáo & Thống kê] 2. Click [Thống kê khách hàng] hoặc truy cập `/admin/reports/customers` |
| 56 | Function - Xem báo cáo tồn kho (Admin) | Báo cáo và thống kê Admin | Check GUI and FUNC view inventory report function (Admin) | Tại Menu ứng dụng: 1. Click [Báo cáo & Thống kê] 2. Click [Báo cáo tồn kho] hoặc truy cập `/admin/reports/inventory` |
| 57 | Function - Tạo báo cáo tùy chỉnh (Admin) | Báo cáo và thống kê Admin | Check GUI and FUNC create custom report function (Admin) | Tại Menu ứng dụng: 1. Click [Báo cáo & Thống kê] 2. Click [Báo cáo nâng cao] hoặc truy cập `/admin/reports/advanced` |
| **ADMIN - CÀI ĐẶT HỆ THỐNG** |
| 58 | Function - Cài đặt chính sách giảm giá sản phẩm (Admin) | Cài đặt hệ thống Admin | Check GUI and FUNC product discount policy function (Admin) | Tại Menu ứng dụng: 1. Click [Cài đặt hệ thống] 2. Click [Giảm giá sản phẩm] hoặc truy cập `/admin/settings/product-discounts` |
| 59 | Function - Cài đặt chính sách giảm giá toàn bộ (Admin) | Cài đặt hệ thống Admin | Check GUI and FUNC global discount policy function (Admin) | Tại Menu ứng dụng: 1. Click [Cài đặt hệ thống] 2. Click [Giảm giá toàn bộ] hoặc truy cập `/admin/settings/global-discounts` |
| 60 | Function - Cài đặt thanh toán (Admin) | Cài đặt hệ thống Admin | Check GUI and FUNC payment settings function (Admin) | Tại Menu ứng dụng: 1. Click [Cài đặt hệ thống] 2. Click [Cài đặt thanh toán] hoặc truy cập `/admin/settings/payments` |
| 61 | Function - Cài đặt thông tin shop (Admin) | Cài đặt hệ thống Admin | Check GUI and FUNC shop information function (Admin) | Tại Menu ứng dụng: 1. Click [Cài đặt hệ thống] 2. Click [Thông tin shop] hoặc truy cập `/admin/settings/shop` |
| 62 | Function - Cài đặt chung (Admin) | Cài đặt hệ thống Admin | Check GUI and FUNC general settings function (Admin) | Tại Menu ứng dụng: 1. Click [Cài đặt hệ thống] hoặc truy cập `/admin/settings` |
| **ADMIN - BẢO MẬT** |
| 63 | Function - Xem lịch sử đăng nhập (Admin) | Bảo mật Admin | Check GUI and FUNC login history function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Bảo mật] 2. Click [Lịch sử đăng nhập] hoặc truy cập `/admin/security/login-history` |
| 64 | Function - Quản lý phiên đăng nhập (Admin) | Bảo mật Admin | Check GUI and FUNC sessions management function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Bảo mật] 2. Click [Phiên đăng nhập] hoặc truy cập `/admin/security/sessions` |
| 64.1 | Function - Phát hiện đăng nhập lạ (Admin) | Bảo mật Admin | Check GUI and FUNC detect suspicious login function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Bảo mật] 2. Click [Lịch sử đăng nhập] - Hệ thống tự động phát hiện và cảnh báo |
| 64.2 | Function - Auto logout khi hết hạn (Admin) | Bảo mật Admin | Check GUI and FUNC auto logout on timeout function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Bảo mật] 2. Click [Phiên đăng nhập] - Hệ thống tự động đăng xuất khi timeout |
| **ADMIN - THÔNG BÁO** |
| 65 | Function - Quản lý thông báo (Admin) | Thông báo Admin | Check GUI and FUNC notifications management function (Admin) | Tại Menu ứng dụng phía Admin: 1. Click [Quản lý thông báo] hoặc truy cập `/admin/notifications` |
| **USER - QUẢN LÝ TÀI KHOẢN** |
| 66 | Function - Đăng nhập (User) | Quản lý tài khoản User | Check GUI and FUNC login function (User) | Tại Menu Ứng dụng phía User: 1. Click [Đăng nhập] hoặc truy cập `/user/auth/login` |
| 67 | Function - Đăng ký (User) | Quản lý tài khoản User | Check GUI and FUNC register function (User) | Tại Menu Ứng dụng phía User: 1. Click [Đăng ký] hoặc truy cập `/user/auth/register` |
| 68 | Function - Đổi mật khẩu (User) | Quản lý tài khoản User | Check GUI and FUNC change password function (User) | Tại Menu Ứng dụng phía User: 1. Click [Tài khoản] 2. Click [Đổi mật khẩu] hoặc truy cập `/user/account` |
| 69 | Function - Cập nhật thông tin cá nhân (User) | Quản lý tài khoản User | Check GUI and FUNC update personal information function (User) | Tại Menu Ứng dụng phía User: 1. Click [Tài khoản] 2. Click [Cập nhật thông tin] hoặc truy cập `/user/account` |
| 70 | Layout - Quản lý thông tin cá nhân (User) | Quản lý tài khoản User | GUI function for User personal information management | Tại Menu Ứng dụng phía User: 1. Click [Tài khoản] hoặc truy cập `/user/account` |
| 70.1 | Function - Khôi phục mật khẩu (User) | Quản lý tài khoản User | Check GUI and FUNC forgot password function (User) | Tại Menu Ứng dụng phía User: 1. Click [Đăng nhập] 2. Click [Quên mật khẩu] hoặc truy cập `/user/auth/forgot-password` |
| 70.2 | Function - Quản lý địa chỉ (User) | Quản lý tài khoản User | Check GUI and FUNC manage addresses function (User) | Tại Menu Ứng dụng phía User: 1. Click [Tài khoản] 2. Click [Địa chỉ] hoặc truy cập `/user/account/addresses` |
| 70.3 | Function - Quản lý thanh toán (User) | Quản lý tài khoản User | Check GUI and FUNC manage payments function (User) | Tại Menu Ứng dụng phía User: 1. Click [Tài khoản] 2. Click [Thanh toán] hoặc truy cập `/user/account/payments` |
| 70.4 | Function - Xem hạng thành viên (User) | Quản lý tài khoản User | Check GUI and FUNC view membership rank function (User) | Tại Menu Ứng dụng phía User: 1. Click [Tài khoản] 2. Click [Hạng thành viên] hoặc truy cập `/user/account/rank` |
| **USER - HIỂN THỊ SẢN PHẨM** |
| 71 | Function - Hiển thị danh sách sản phẩm (User) | Hiển thị sản phẩm User | Check GUI and FUNC display products list function (User) | Tại Menu Ứng dụng phía User: 1. Click [Mô hình] hoặc truy cập `/user/products` |
| 72 | Function - Xem chi tiết sản phẩm (User) | Hiển thị sản phẩm User | Check GUI and FUNC view product details function (User) | Tại Menu Ứng dụng phía User: 1. Click [Mô hình] 2. Click vào sản phẩm hoặc truy cập `/user/products/[id]` |
| **USER - TÌM KIẾM SẢN PHẨM** |
| 73 | Function - Tìm kiếm và lọc sản phẩm (User) | Tìm kiếm sản phẩm User | Check GUI and FUNC search and filter products function (User) | Tại Menu Ứng dụng: 1. Click [Tìm kiếm] hoặc truy cập `/user/search` |
| **USER - BỘ LỌC VÀ PHÂN LOẠI** |
| 74 | Layout - Bộ lọc sản phẩm (User) | Bộ lọc sản phẩm User | GUI function for product filtering and categorization | Tại Menu Ứng dụng phía User: 1. Click [Mô hình] hoặc truy cập `/user/products` |
| **USER - QUẢN LÝ GIỎ HÀNG** |
| 75 | Function - Thêm sản phẩm vào giỏ hàng (User) | Quản lý giỏ hàng User | Check GUI and FUNC add product to cart function (User) | Tại Danh sách sản phẩm: 1. Click [Thêm vào giỏ hàng] hoặc từ trang chi tiết sản phẩm |
| 76 | Function - Hiển thị giỏ hàng (User) | Quản lý giỏ hàng User | Check GUI and FUNC view cart function (User) | Tại Menu chính: 1. Click [Giỏ hàng] hoặc truy cập `/user/cart` |
| 77 | Function - Xóa sản phẩm khỏi giỏ hàng (User) | Quản lý giỏ hàng User | Check GUI and FUNC delete product from cart function (User) | Tại Menu Giỏ hàng: 1. Click [Xóa] |
| 78 | Function - Cập nhật số lượng sản phẩm (User) | Quản lý giỏ hàng User | Check GUI and FUNC update product quantity function (User) | Tại Menu Giỏ hàng: 1. Thay đổi số lượng trong ô input |
| 79 | Function - Áp dụng mã giảm giá (User) | Quản lý giỏ hàng User | Check GUI and FUNC apply discount code function (User) | Tại Menu Giỏ hàng: 1. Nhập mã giảm giá 2. Click [Áp dụng] |
| 80 | Function - Thực hiện thanh toán (User) | Quản lý giỏ hàng User | Check GUI and FUNC proceed to checkout function (User) | Tại Menu Giỏ hàng: 1. Click [Thực hiện thanh toán] hoặc truy cập `/user/checkout` |
| **USER - THANH TOÁN ĐƠN HÀNG** |
| 81 | Function - Chọn phương thức thanh toán (User) | Thanh toán đơn hàng User | Check GUI and FUNC select payment method function (User) | Tại Menu Giỏ hàng: 1. Click [Thanh toán] hoặc truy cập `/user/checkout` |
| 82 | Function - Thanh toán khi nhận hàng (User) | Thanh toán đơn hàng User | Check GUI and FUNC cash on delivery payment function (User) | Tại Menu Giỏ hàng: 1. Click [Thanh toán khi nhận hàng] 2. Click [Xác nhận thanh toán] |
| 83 | Function - Thanh toán VNPAY (User) | Thanh toán đơn hàng User | Check GUI and FUNC VNPAY payment function (User) | Tại Menu Giỏ hàng: 1. Click [Thanh toán VNPAY] 2. Click [Xác nhận thanh toán] hoặc truy cập `/user/checkout/processing` |
| 84 | Function - Xác nhận đơn hàng (User) | Thanh toán đơn hàng User | Check GUI and FUNC confirm order function (User) | Tại Trang thanh toán: 1. Điền thông tin giao hàng 2. Click [Xác nhận đơn hàng] |
| **USER - QUẢN LÝ ĐƠN HÀNG** |
| 85 | Function - Xem thông tin đơn hàng (User) | Quản lý đơn hàng User | Check GUI and FUNC view order information function (User) | Tại Menu Ứng dụng phía User: 1. Click [Lịch sử đơn hàng] hoặc truy cập `/user/account/orders` |
| 86 | Function - Xem chi tiết đơn hàng (User) | Quản lý đơn hàng User | Check GUI and FUNC view order details function (User) | Tại Menu Ứng dụng phía User: 1. Click [Lịch sử đơn hàng] 2. Click [Xem chi tiết] hoặc truy cập `/user/account/orders/[id]` |
| 87 | Function - Theo dõi đơn hàng (User) | Quản lý đơn hàng User | Check GUI and FUNC track order function (User) | Tại Menu Ứng dụng phía User: 1. Click [Theo dõi đơn hàng] hoặc truy cập `/user/orders/track/[id]` |
| 88 | Function - Hủy đơn hàng (User) | Quản lý đơn hàng User | Check GUI and FUNC cancel order function (User) | Tại Trang chi tiết đơn hàng: 1. Click [Hủy đơn hàng] |
| 89 | Function - Đánh giá đơn hàng (User) | Quản lý đơn hàng User | Check GUI and FUNC rate order function (User) | Tại Trang chi tiết đơn hàng: 1. Click [Đánh giá] |
| 89.1 | Function - Đặt lại đơn hàng (User) | Quản lý đơn hàng User | Check GUI and FUNC reorder function (User) | Tại Trang chi tiết đơn hàng hoặc danh sách đơn hàng: 1. Click [Đặt lại] |
| 89.2 | Function - Yêu cầu đổi/trả hàng (User) | Quản lý đơn hàng User | Check GUI and FUNC request return/exchange function (User) | Tại Trang chi tiết đơn hàng đã giao: 1. Click [Yêu cầu đổi/trả hàng] |
| **USER - ĐÁNH GIÁ SẢN PHẨM** |
| 90 | Function - Để lại đánh giá sản phẩm (User) | Đánh giá sản phẩm User | Check GUI and FUNC leave product review function (User) | Tại Menu ứng dụng phía User: 1. Click vào sản phẩm 2. Click [Gửi đánh giá] hoặc truy cập `/user/reviews` |
| 91 | Function - Xem đánh giá sản phẩm (User) | Đánh giá sản phẩm User | Check GUI and FUNC view product reviews function (User) | Tại Trang chi tiết sản phẩm: 1. Scroll xuống phần đánh giá |
| **USER - YÊU CẦU HỖ TRỢ** |
| 92 | Function - Gửi yêu cầu hỗ trợ (User) | Hỗ trợ - liên hệ User | Check GUI and FUNC send support request function (User) | Tại Menu ứng dụng phía User: 1. Click [Hỗ trợ] 2. Click [Gửi yêu cầu] hoặc truy cập `/user/support` |
| 93 | Function - Chat hỗ trợ (User) | Hỗ trợ - liên hệ User | Check GUI and FUNC chat support function (User) | Tại Menu ứng dụng phía User: 1. Click [Hỗ trợ] 2. Click [Chat] |
| 93.1 | Function - Quản lý yêu cầu hỗ trợ (User) | Hỗ trợ - liên hệ User | Check GUI and FUNC manage support requests function (User) | Tại Menu ứng dụng phía User: 1. Click [Hỗ trợ] 2. Click [Yêu cầu hỗ trợ] - Xem danh sách, lọc, tìm kiếm |
| 93.2 | Function - Câu hỏi thường gặp (User) | Hỗ trợ - liên hệ User | Check GUI and FUNC FAQ function (User) | Tại Menu ứng dụng phía User: 1. Click [Hỗ trợ] 2. Click [Câu hỏi thường gặp] |
| 93.3 | Function - Thông tin liên hệ (User) | Hỗ trợ - liên hệ User | Check GUI and FUNC contact information function (User) | Tại Menu ứng dụng phía User: 1. Click [Hỗ trợ] 2. Click [Thông tin liên hệ] |
| 93.4 | Function - Export lịch sử chat (User) | Hỗ trợ - liên hệ User | Check GUI and FUNC export chat history function (User) | Tại Menu ứng dụng phía User: 1. Click [Hỗ trợ] 2. Click [Chat] 3. Click [Export lịch sử] |
| 93.5 | Function - Tìm kiếm trong chat (User) | Hỗ trợ - liên hệ User | Check GUI and FUNC search in chat function (User) | Tại Menu ứng dụng phía User: 1. Click [Hỗ trợ] 2. Click [Chat] 3. Sử dụng ô tìm kiếm trong chat |
| **USER - KHUYẾN MÃI** |
| 94 | Function - Xem danh sách khuyến mãi (User) | Khuyến mãi User | Check GUI and FUNC promotion management function | Tại Menu ứng dụng: 1. Click [Khuyến mãi] hoặc truy cập `/user/promotions` |
| 95 | Function - Xem chi tiết khuyến mãi (User) | Khuyến mãi User | Check GUI and FUNC view promotion details function | Tại Menu ứng dụng: 1. Click [Khuyến mãi] 2. Click vào khuyến mãi hoặc truy cập `/user/promotions/[code]` |
| 96 | Function - Áp dụng mã giảm giá (User) | Khuyến mãi User | Check GUI and FUNC apply discount code function | Tại Trang giỏ hàng: 1. Nhập mã giảm giá 2. Click [Áp dụng] |
| **USER - SẢN PHẨM YÊU THÍCH** |
| 97 | Function - Xem danh sách yêu thích (User) | Danh sách yêu thích User | Check GUI and FUNC view wishlist function (User) | Tại Menu Ứng dụng phía User: 1. Click [Yêu thích] hoặc truy cập `/user/wishlist` |
| 98 | Function - Thêm vào yêu thích (User) | Danh sách yêu thích User | Check GUI and FUNC add to wishlist function (User) | Tại Trang chi tiết sản phẩm: 1. Click [Thêm vào yêu thích] |
| 99 | Function - Xóa khỏi yêu thích (User) | Danh sách yêu thích User | Check GUI and FUNC remove from wishlist function (User) | Tại Trang yêu thích: 1. Click [Xóa] |
| **USER - ĐẶT TRƯỚC SẢN PHẨM** |
| 100 | Function - Đặt trước sản phẩm (User) | Đặt trước sản phẩm User | Check GUI and FUNC pre-order product function (User) | Tại Menu Ứng dụng phía User: 1. Click [Đặt trước mô hình] hoặc truy cập `/user/borrow` |
| 101 | Function - Xem danh sách đặt trước (User) | Đặt trước sản phẩm User | Check GUI and FUNC view pre-orders list function (User) | Tại Menu Ứng dụng phía User: 1. Click [Đặt trước mô hình] |
| 102 | Function - Hủy đặt trước (User) | Đặt trước sản phẩm User | Check GUI and FUNC cancel pre-order function (User) | Tại Trang đặt trước: 1. Click [Hủy đặt trước] |
| 102.1 | Function - Xem chi tiết đặt trước (User) | Đặt trước sản phẩm User | Check GUI and FUNC view pre-order details function (User) | Tại Trang danh sách đặt trước: 1. Click [Xem chi tiết] |
| 102.2 | Function - Quản lý trạng thái đặt trước (User) | Đặt trước sản phẩm User | Check GUI and FUNC manage pre-order status function (User) | Tại Trang danh sách đặt trước: 1. Sử dụng tab trạng thái để lọc và theo dõi |
| **USER - YÊU CẦU ĐẶT HÀNG** |
| 103 | Function - Gửi yêu cầu đặt hàng (User) | Yêu cầu đặt hàng User | Check GUI and FUNC send special request function (User) | Tại Menu Ứng dụng phía User: 1. Click [Yêu cầu nhập hàng] hoặc truy cập `/user/requests` |
| 104 | Function - Xem chi tiết yêu cầu (User) | Yêu cầu đặt hàng User | Check GUI and FUNC view request details function (User) | Tại Menu Ứng dụng phía User: 1. Click [Yêu cầu nhập hàng] 2. Click [Xem] hoặc truy cập `/user/requests/[id]` |
| **USER - VẬN CHUYỂN** |
| 105 | Layout - Chọn phương thức vận chuyển (User) | Vận chuyển User | GUI function for shipping method selection | Tại Trang thanh toán: 1. Chọn phương thức vận chuyển |
| **USER - THÔNG BÁO** |
| 106 | Function - Xem thông báo (User) | Thông báo User | Check GUI and FUNC view notifications function (User) | Tại Menu Ứng dụng phía User: 1. Click [Thông báo] hoặc truy cập `/user/notifications` |
| **USER - BÀI VIẾT** |
| 107 | Function - Tạo bài viết (User) | Tạo - hiển thị bài viết User | Check GUI and FUNC create post function (User) | Tại Menu Ứng dụng phía User: 1. Click [Tạo bài viết] hoặc truy cập `/user/posts/create` |
| 108 | Function - Hiển thị danh sách bài viết (User) | Tạo - hiển thị bài viết User | Check GUI and FUNC display posts list function (User) | Tại Menu Ứng dụng phía User: 1. Click [Bài viết] hoặc truy cập `/user/posts` |
| 109 | Function - Xem chi tiết bài viết (User) | Tạo - hiển thị bài viết User | Check GUI and FUNC view post details function (User) | Tại Menu Ứng dụng phía User: 1. Click [Bài viết] 2. Click vào bài viết hoặc truy cập `/user/posts/[id]` |
| 110 | Function - Chỉnh sửa bài viết (User) | Tạo - hiển thị bài viết User | Check GUI and FUNC edit post function (User) | Tại Trang chi tiết bài viết: 1. Click [Chỉnh sửa] hoặc truy cập `/user/posts/[id]/edit` |
| **USER - TƯƠNG TÁC BÀI VIẾT** |
| 111 | Function - Like bài viết (User) | Tương tác bài viết User | Check GUI and FUNC like post function (User) | Tại Trang chi tiết bài viết: 1. Click [Like] |
| 112 | Function - Bình luận bài viết (User) | Tương tác bài viết User | Check GUI and FUNC comment post function (User) | Tại Trang chi tiết bài viết: 1. Nhập bình luận 2. Click [Gửi] |
| 113 | Function - Chia sẻ bài viết (User) | Tương tác bài viết User | Check GUI and FUNC share post function (User) | Tại Trang chi tiết bài viết: 1. Click [Chia sẻ] |
| **USER - XEM TRANG CÁ NHÂN** |
| 114 | Function - Xem trang cá nhân người lạ (User) | Xem trang cá nhân User | Check GUI and FUNC view stranger profile function (User) | Tại Trang bài viết hoặc bình luận: 1. Click vào tên người dùng hoặc truy cập `/user/profile/[id]` |
| **USER - BẢO MẬT** |
| 115 | Function - Xem lịch sử đăng nhập (User) | Bảo mật User | Check GUI and FUNC login history function (User) | Tại Menu Ứng dụng phía User: 1. Click [Tài khoản] 2. Click [Lịch sử đăng nhập] hoặc truy cập `/user/account/logins` |
| 116 | Function - Quản lý phiên đăng nhập (User) | Bảo mật User | Check GUI and FUNC sessions management function (User) | Tại Menu Ứng dụng phía User: 1. Click [Tài khoản] 2. Click [Phiên đăng nhập] hoặc truy cập `/user/account/sessions` |
| 116.1 | Function - Phát hiện đăng nhập lạ (User) | Bảo mật User | Check GUI and FUNC detect suspicious login function (User) | Tại Menu Ứng dụng phía User: 1. Click [Tài khoản] 2. Click [Lịch sử đăng nhập] - Hệ thống tự động phát hiện và cảnh báo |
| 116.2 | Function - Auto logout khi hết hạn (User) | Bảo mật User | Check GUI and FUNC auto logout on timeout function (User) | Tại Menu Ứng dụng phía User: 1. Click [Tài khoản] 2. Click [Phiên đăng nhập] - Hệ thống tự động đăng xuất khi timeout |
| **USER - CÀI ĐẶT** |
| 117 | Function - Cài đặt tài khoản (User) | Cài đặt User | Check GUI and FUNC account settings function (User) | Tại Menu Ứng dụng phía User: 1. Click [Cài đặt] hoặc truy cập `/user/settings` |

---

## GHI CHÚ QUAN TRỌNG

### Về Routes:
- Tất cả routes được xác định dựa trên cấu trúc thư mục `src/app/admin/` và `src/app/user/`
- Routes có thể truy cập trực tiếp qua URL hoặc thông qua menu navigation
- Routes động (có `[id]`) cần thay thế `[id]` bằng ID thực tế khi test

### Về Pre-Condition:
- Pre-Condition mô tả các bước điều hướng từ menu hoặc URL trực tiếp
- Có thể kết hợp cả hai cách: click menu hoặc truy cập URL trực tiếp
- Một số chức năng yêu cầu đăng nhập trước khi truy cập

### Về Test Cases:
- Mỗi function có thể có nhiều test case con (GUI test, Functional test, Validation test, etc.)
- Cần bổ sung thêm các test case chi tiết cho từng function trong các sheet riêng
- Test cases cần bao gồm: Test ID, Test Description, Pre-Condition, Test Steps, Expected Result, Actual Result, Status

---

**Tổng số chức năng:** 147 functions  
**Admin:** 79 functions  
**User:** 68 functions
