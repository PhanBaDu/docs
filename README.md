# BLACKBOX TEST CASE - TỔNG QUAN DỰ ÁN

**Dự án:** Hệ Thống Quản Lý Nhà Sách  
**Ngày tạo:** 2025  
**Mục đích:** Tài liệu tổng quan về các chức năng và routes để thực hiện blackbox testing

---

## BẢNG TỔNG HỢP TEST CASE

| No | Function Name | Sheet Name | Description | Pre-Condition (Route) |
|----|---------------|------------|-------------|----------------------|
| **ADMIN - QUẢN LÝ TÀI KHOẢN** |
| 1 | Function - Đăng nhập (Admin) | Quản lý tài khoản Admin | Check GUI and FUNC login function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Đăng nhập] hoặc truy cập `/admin/auth/login` |
| 2 | Function - Đăng ký (Admin) | Quản lý tài khoản Admin | Check GUI and FUNC register function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Đăng ký] hoặc truy cập `/admin/auth/register` |
| 3 | Function - Đổi mật khẩu (Admin) | Quản lý tài khoản Admin | Check GUI and FUNC change password function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Tài khoản] 2. Click [Đổi mật khẩu] hoặc truy cập `/admin/account` |
| 4 | Layout - Quản lý thông tin cá nhân (Admin) | Quản lý tài khoản Admin | GUI function for Admin personal information management | Tại Menu Ứng dụng phía Admin: 1. Click [Tài khoản] hoặc truy cập `/admin/account` |
| 5 | Function - Khôi phục mật khẩu (Admin) | Quản lý tài khoản Admin | Check GUI and FUNC forgot password function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Đăng nhập] 2. Click [Quên mật khẩu] hoặc truy cập `/admin/auth/forgot-password` |
| **ADMIN - QUẢN LÝ NHÂN VIÊN** |
| 6 | Function - Hiển thị danh sách nhân viên (Admin) | Quản lý nhân viên Admin | Check GUI and FUNC display employees list function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý nhân viên] hoặc truy cập `/admin/employees` |
| 7 | Function - Xem chi tiết nhân viên (Admin) | Quản lý nhân viên Admin | Check GUI and FUNC view employee details function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý nhân viên] 2. Click [Xem] hoặc truy cập `/admin/employees/[id]` |
| 8 | Function - Thêm nhân viên mới (Admin) | Quản lý nhân viên Admin | Check GUI and FUNC add new employee function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý nhân viên] 2. Click [Thêm nhân viên] hoặc truy cập `/admin/employees/new` |
| 9 | Function - Cập nhật thông tin nhân viên (Admin) | Quản lý nhân viên Admin | Check GUI and FUNC update employee information function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý nhân viên] 2. Click [Chỉnh sửa] hoặc truy cập `/admin/employees/[id]/edit` |
| 10 | Function - Xóa nhân viên (Admin) | Quản lý nhân viên Admin | Check GUI and FUNC delete employee function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý nhân viên] 2. Click [Xóa] |
| 11 | Function - Phân quyền nhân viên (Admin) | Quản lý nhân viên Admin | Check GUI and FUNC assign permissions function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý nhân viên] 2. Click [Phân quyền] |
| **ADMIN - QUẢN LÝ KHÁCH HÀNG** |
| 12 | Function - Hiển thị danh sách khách hàng (Admin) | Quản lý khách hàng Admin | Check GUI and FUNC display customers list function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý khách hàng] hoặc truy cập `/admin/customers` |
| 13 | Function - Xem chi tiết khách hàng (Admin) | Quản lý khách hàng Admin | Check GUI and FUNC view customer details function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý khách hàng] 2. Click [Xem] hoặc truy cập `/admin/customers/[id]` |
| 14 | Function - Cập nhật thông tin khách hàng (Admin) | Quản lý khách hàng Admin | Check GUI and FUNC update customer information function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý khách hàng] 2. Click [Chỉnh sửa] |
| 15 | Function - Khóa/Mở khóa tài khoản khách hàng (Admin) | Quản lý khách hàng Admin | Check GUI and FUNC block/unblock customer account function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý khách hàng] 2. Click [Khóa/Mở khóa] |
| **ADMIN - QUẢN LÝ SÁCH** |
| 16 | Function - Hiển thị danh sách sách (Admin) | Quản lý sách Admin | Check GUI and FUNC display books list function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý sách] hoặc truy cập `/admin/products` |
| 17 | Function - Xem chi tiết sách (Admin) | Quản lý sách Admin | Check GUI and FUNC view book details function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý sách] 2. Click [Xem] hoặc truy cập `/admin/products/[id]` |
| 18 | Function - Thêm sách mới (Admin) | Quản lý sách Admin | Check GUI and FUNC add new book function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý sách] 2. Click [Thêm sách] hoặc truy cập `/admin/products/new` |
| 19 | Function - Cập nhật thông tin sách (Admin) | Quản lý sách Admin | Check GUI and FUNC update book information function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý sách] 2. Click [Chỉnh sửa] hoặc truy cập `/admin/products/[id]/edit` |
| 20 | Function - Xóa sách (Admin) | Quản lý sách Admin | Check GUI and FUNC delete book function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý sách] 2. Click [Xóa] |
| 21 | Function - Ẩn/Hiện sách (Admin) | Quản lý sách Admin | Check GUI and FUNC hide/show book function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý sách] 2. Click [Ẩn/Hiện] |
| **ADMIN - QUẢN LÝ TỒN KHO** |
| 22 | Function - Hiển thị danh sách tồn kho (Admin) | Quản lý tồn kho Admin | Check GUI and FUNC display inventory list function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Tồn kho] hoặc truy cập `/admin/inventory` |
| 23 | Function - Xem chi tiết tồn kho (Admin) | Quản lý tồn kho Admin | Check GUI and FUNC view inventory details function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Tồn kho] 2. Click [Xem] hoặc truy cập `/admin/inventory/[id]` |
| 24 | Function - Cập nhật số lượng tồn kho (Admin) | Quản lý tồn kho Admin | Check GUI and FUNC update inventory quantity function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Tồn kho] 2. Click [Cập nhật] |
| 25 | Function - Nhập hàng (Admin) | Quản lý tồn kho Admin | Check GUI and FUNC import goods function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Tồn kho] 2. Click [Nhập hàng] hoặc truy cập `/admin/inventory/import` |
| 26 | Function - Xuất hàng (Admin) | Quản lý tồn kho Admin | Check GUI and FUNC export goods function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Tồn kho] 2. Click [Xuất hàng] hoặc truy cập `/admin/inventory/export` |
| 27 | Function - Kiểm kê tồn kho (Admin) | Quản lý tồn kho Admin | Check GUI and FUNC inventory audit function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Tồn kho] 2. Click [Kiểm kê] hoặc truy cập `/admin/inventory/audit` |
| 28 | Function - Cảnh báo tồn kho thấp (Admin) | Quản lý tồn kho Admin | Check GUI and FUNC low stock alert function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Tồn kho] 2. Click [Cảnh báo] hoặc truy cập `/admin/inventory/alerts` |
| **ADMIN - QUẢN LÝ ĐƠN HÀNG** |
| 29 | Function - Hiển thị danh sách đơn hàng (Admin) | Quản lý đơn hàng Admin | Check GUI and FUNC display orders list function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Đơn hàng] hoặc truy cập `/admin/orders` |
| 30 | Function - Xem chi tiết đơn hàng (Admin) | Quản lý đơn hàng Admin | Check GUI and FUNC view order details function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Đơn hàng] 2. Click [Xem] hoặc truy cập `/admin/orders/[id]` |
| 31 | Function - Cập nhật trạng thái đơn hàng (Admin) | Quản lý đơn hàng Admin | Check GUI and FUNC update order status function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Đơn hàng] 2. Click [Cập nhật trạng thái] hoặc truy cập `/admin/orders/[id]/update-status` |
| 32 | Function - Hủy đơn hàng (Admin) | Quản lý đơn hàng Admin | Check GUI and FUNC cancel order function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Đơn hàng] 2. Click [Hủy đơn hàng] hoặc truy cập `/admin/orders/[id]/cancel` |
| 33 | Function - Xác nhận đơn hàng (Admin) | Quản lý đơn hàng Admin | Check GUI and FUNC confirm order function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Đơn hàng] 2. Click [Xác nhận đơn hàng] hoặc truy cập `/admin/orders/[id]/confirm` |
| 34 | Function - In đơn hàng (Admin) | Quản lý đơn hàng Admin | Check GUI and FUNC print order function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Đơn hàng] 2. Click [In đơn hàng] hoặc truy cập `/admin/orders/[id]/print` |
| **ADMIN - QUẢN LÝ ĐẶT TRƯỚC** |
| 35 | Function - Hiển thị danh sách đặt trước (Admin) | Quản lý đặt trước Admin | Check GUI and FUNC display pre-orders list function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Đặt trước] hoặc truy cập `/admin/pre-orders` |
| 36 | Function - Xem chi tiết đặt trước (Admin) | Quản lý đặt trước Admin | Check GUI and FUNC view pre-order details function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Đặt trước] 2. Click [Xem] hoặc truy cập `/admin/pre-orders/[id]` |
| 37 | Function - Xử lý đặt trước (Admin) | Quản lý đặt trước Admin | Check GUI and FUNC process pre-order function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Đặt trước] 2. Click [Xử lý] hoặc truy cập `/admin/pre-orders/[id]/process` |
| 38 | Function - Thông báo có hàng (Admin) | Quản lý đặt trước Admin | Check GUI and FUNC notify stock available function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Đặt trước] 2. Click [Thông báo có hàng] hoặc truy cập `/admin/pre-orders/[id]/notify-stock` |
| **ADMIN - QUẢN LÝ YÊU CẦU** |
| 39 | Function - Hiển thị danh sách yêu cầu (Admin) | Quản lý yêu cầu Admin | Check GUI and FUNC display requests list function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Yêu cầu] hoặc truy cập `/admin/requests` |
| 40 | Function - Xem chi tiết yêu cầu (Admin) | Quản lý yêu cầu Admin | Check GUI and FUNC view request details function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Yêu cầu] 2. Click [Xem] hoặc truy cập `/admin/requests/[id]` |
| 41 | Function - Phê duyệt yêu cầu (Admin) | Quản lý yêu cầu Admin | Check GUI and FUNC approve request function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Yêu cầu] 2. Click [Phê duyệt] |
| 42 | Function - Từ chối yêu cầu (Admin) | Quản lý yêu cầu Admin | Check GUI and FUNC reject request function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Yêu cầu] 2. Click [Từ chối] |
| **ADMIN - QUẢN LÝ ĐÁNH GIÁ** |
| 43 | Function - Hiển thị danh sách đánh giá (Admin) | Quản lý đánh giá Admin | Check GUI and FUNC display reviews list function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Đánh giá] hoặc truy cập `/admin/reviews` |
| 44 | Function - Xem chi tiết đánh giá (Admin) | Quản lý đánh giá Admin | Check GUI and FUNC view review details function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Đánh giá] 2. Click [Xem chi tiết] hoặc truy cập `/admin/reviews/[id]` |
| 45 | Function - Duyệt đánh giá (Admin) | Quản lý đánh giá Admin | Check GUI and FUNC approve review function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Đánh giá] 2. Click [Duyệt] |
| 46 | Function - Từ chối đánh giá (Admin) | Quản lý đánh giá Admin | Check GUI and FUNC reject review function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Đánh giá] 2. Click [Từ chối] |
| 47 | Function - Xóa đánh giá (Admin) | Quản lý đánh giá Admin | Check GUI and FUNC delete review function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Đánh giá] 2. Click [Xóa đánh giá] |
| **ADMIN - QUẢN LÝ BÀI VIẾT** |
| 48 | Function - Hiển thị danh sách bài viết (Admin) | Quản lý bài viết Admin | Check GUI and FUNC display posts list function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý bài viết] hoặc truy cập `/admin/posts` |
| 49 | Function - Xem chi tiết bài viết (Admin) | Quản lý bài viết Admin | Check GUI and FUNC view post details function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý bài viết] 2. Click [Xem] hoặc truy cập `/admin/posts/[id]` |
| 50 | Function - Xóa bài viết (Admin) | Quản lý bài viết Admin | Check GUI and FUNC delete post function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý bài viết] 2. Click [Xóa] |
| 51 | Function - Chỉnh sửa bài viết (Admin) | Quản lý bài viết Admin | Check GUI and FUNC edit post function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Quản lý bài viết] 2. Click [Chỉnh sửa] |
| **ADMIN - BÁO CÁO VÀ THỐNG KÊ** |
| 52 | Function - Xem báo cáo doanh thu (Admin) | Báo cáo và thống kê Admin | Check GUI and FUNC view revenue report function (Admin) | Tại Menu Ứng dụng: 1. Click [Báo cáo & Thống kê] 2. Click [Doanh thu] hoặc truy cập `/admin/reports/revenue` |
| 53 | Function - Xem báo cáo chi phí (Admin) | Báo cáo và thống kê Admin | Check GUI and FUNC view expenses report function (Admin) | Tại Menu Ứng dụng: 1. Click [Báo cáo & Thống kê] 2. Click [Chi phí] hoặc truy cập `/admin/reports/expenses` |
| 54 | Function - Xem báo cáo lợi nhuận (Admin) | Báo cáo và thống kê Admin | Check GUI and FUNC view profit report function (Admin) | Tại Menu Ứng dụng: 1. Click [Báo cáo & Thống kê] 2. Click [Lợi nhuận] hoặc truy cập `/admin/reports/profit` |
| 55 | Function - Xem sản phẩm bán chạy (Admin) | Báo cáo và thống kê Admin | Check GUI and FUNC view top products report function (Admin) | Tại Menu Ứng dụng: 1. Click [Báo cáo & Thống kê] 2. Click [Sản phẩm bán chạy] hoặc truy cập `/admin/reports/top-products` |
| 56 | Function - Xem thống kê khách hàng (Admin) | Báo cáo và thống kê Admin | Check GUI and FUNC view customers statistics function (Admin) | Tại Menu Ứng dụng: 1. Click [Báo cáo & Thống kê] 2. Click [Thống kê khách hàng] hoặc truy cập `/admin/reports/customers` |
| 57 | Function - Xem báo cáo tồn kho (Admin) | Báo cáo và thống kê Admin | Check GUI and FUNC view inventory report function (Admin) | Tại Menu Ứng dụng: 1. Click [Báo cáo & Thống kê] 2. Click [Báo cáo tồn kho] hoặc truy cập `/admin/reports/inventory` |
| **ADMIN - QUẢN LÝ VẬN CHUYỂN** |
| 58 | Function - Hiển thị danh sách đơn vận chuyển (Admin) | Quản lý vận chuyển Admin | Check GUI and FUNC display shipping list function (Admin) | Tại Menu Ứng dụng: 1. Click [Vận chuyển] hoặc truy cập `/admin/shipping` |
| 59 | Function - Cập nhật trạng thái vận chuyển (Admin) | Quản lý vận chuyển Admin | Check GUI and FUNC update shipping status function (Admin) | Tại Menu Ứng dụng: 1. Click [Vận chuyển] 2. Click [Cập nhật trạng thái] |
| **ADMIN - HỖ TRỢ KHÁCH HÀNG** |
| 60 | Function - Hiển thị danh sách yêu cầu hỗ trợ (Admin) | Quản lý hỗ trợ Admin | Check GUI and FUNC display support requests list function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Hỗ trợ] hoặc truy cập `/admin/support` |
| 61 | Function - Chat hỗ trợ khách hàng (Admin) | Quản lý hỗ trợ Admin | Check GUI and FUNC chat support function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Hỗ trợ] 2. Click [Chat] hoặc truy cập `/admin/support/[id]/chat` |
| 62 | Function - Trả lời yêu cầu hỗ trợ (Admin) | Quản lý hỗ trợ Admin | Check GUI and FUNC reply support request function (Admin) | Tại Menu Ứng dụng: 1. Click [Hỗ trợ] 2. Click [Trả lời] |
| **ADMIN - XỬ LÝ KHIẾU NẠI** |
| 63 | Function - Hiển thị danh sách khiếu nại (Admin) | Xử lý khiếu nại Admin | Check GUI and FUNC display complaints list function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Khiếu nại] hoặc truy cập `/admin/complaints` |
| 64 | Function - Xem chi tiết khiếu nại (Admin) | Xử lý khiếu nại Admin | Check GUI and FUNC view complaint details function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Khiếu nại] 2. Click [Xem] hoặc truy cập `/admin/complaints/[id]` |
| 65 | Function - Trả lời khiếu nại (Admin) | Xử lý khiếu nại Admin | Check GUI and FUNC reply complaint function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Khiếu nại] 2. Click [Trả lời] hoặc truy cập `/admin/complaints/[id]/reply` |
| **ADMIN - CÀI ĐẶT HỆ THỐNG** |
| 66 | Function - Cài đặt chính sách giảm giá (Admin) | Cài đặt hệ thống Admin | Check GUI and FUNC discount policy function (Admin) | Tại Menu Ứng dụng: 1. Click [Cài đặt] 2. Click [Chính sách giảm giá] hoặc truy cập `/admin/settings/discounts` |
| 67 | Function - Cài đặt thanh toán (Admin) | Cài đặt hệ thống Admin | Check GUI and FUNC payment settings function (Admin) | Tại Menu Ứng dụng: 1. Click [Cài đặt] 2. Click [Cài đặt thanh toán] hoặc truy cập `/admin/settings/payments` |
| 68 | Function - Cài đặt thông tin shop (Admin) | Cài đặt hệ thống Admin | Check GUI and FUNC shop information function (Admin) | Tại Menu Ứng dụng: 1. Click [Cài đặt] 2. Click [Thông tin shop] hoặc truy cập `/admin/settings/shop` |
| 69 | Function - Cài đặt chung (Admin) | Cài đặt hệ thống Admin | Check GUI and FUNC general settings function (Admin) | Tại Menu Ứng dụng: 1. Click [Cài đặt] hoặc truy cập `/admin/settings` |
| **ADMIN - BẢO MẬT** |
| 70 | Function - Xem lịch sử đăng nhập (Admin) | Bảo mật Admin | Check GUI and FUNC login history function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Bảo mật] 2. Click [Lịch sử đăng nhập] hoặc truy cập `/admin/security/login-history` |
| 71 | Function - Quản lý phiên đăng nhập (Admin) | Bảo mật Admin | Check GUI and FUNC sessions management function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Bảo mật] 2. Click [Phiên đăng nhập] hoặc truy cập `/admin/security/sessions` |
| 72 | Function - Phát hiện đăng nhập lạ (Admin) | Bảo mật Admin | Check GUI and FUNC detect suspicious login function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Bảo mật] 2. Click [Lịch sử đăng nhập] - Hệ thống tự động phát hiện |
| **ADMIN - THÔNG BÁO** |
| 73 | Function - Quản lý thông báo (Admin) | Thông báo Admin | Check GUI and FUNC notifications management function (Admin) | Tại Menu Ứng dụng phía Admin: 1. Click [Thông báo] hoặc truy cập `/admin/notifications` |
| **NHÂN VIÊN - QUẢN LÝ TÀI KHOẢN** |
| 74 | Function - Đăng nhập (Nhân viên) | Quản lý tài khoản Nhân viên | Check GUI and FUNC login function (Nhân viên) | Tại Menu Ứng dụng phía Nhân viên: 1. Click [Đăng nhập] hoặc truy cập `/nhanvien/auth/login` |
| 75 | Function - Đổi mật khẩu (Nhân viên) | Quản lý tài khoản Nhân viên | Check GUI and FUNC change password function (Nhân viên) | Tại Menu Ứng dụng phía Nhân viên: 1. Click [Tài khoản] 2. Click [Đổi mật khẩu] hoặc truy cập `/nhanvien/account` |
| 76 | Layout - Quản lý thông tin cá nhân (Nhân viên) | Quản lý tài khoản Nhân viên | GUI function for Nhân viên personal information management | Tại Menu Ứng dụng phía Nhân viên: 1. Click [Tài khoản] hoặc truy cập `/nhanvien/account` |
| **NHÂN VIÊN - TÌM KIẾM VÀ HIỂN THỊ SÁCH** |
| 77 | Function - Tìm kiếm sách (Nhân viên) | Tìm kiếm sách Nhân viên | Check GUI and FUNC search books function (Nhân viên) | Tại Menu Ứng dụng phía Nhân viên: 1. Sử dụng thanh tìm kiếm hoặc truy cập `/nhanvien/products` |
| 78 | Function - Hiển thị danh sách sách (Nhân viên) | Hiển thị sách Nhân viên | Check GUI and FUNC display books list function (Nhân viên) | Tại Menu Ứng dụng phía Nhân viên: 1. Click [Sách] hoặc truy cập `/nhanvien/products` |
| 79 | Function - Xem chi tiết sách (Nhân viên) | Hiển thị sách Nhân viên | Check GUI and FUNC view book details function (Nhân viên) | Tại Menu Ứng dụng phía Nhân viên: 1. Click [Sách] 2. Click vào sách hoặc truy cập `/nhanvien/products/[id]` |
| **NHÂN VIÊN - XỬ LÝ ĐƠN HÀNG** |
| 80 | Function - Hiển thị danh sách đơn hàng (Nhân viên) | Xử lý đơn hàng Nhân viên | Check GUI and FUNC display orders list function (Nhân viên) | Tại Menu Ứng dụng phía Nhân viên: 1. Click [Xử lý đơn hàng] hoặc truy cập `/nhanvien/orders` |
| 81 | Function - Xem chi tiết đơn hàng (Nhân viên) | Xử lý đơn hàng Nhân viên | Check GUI and FUNC view order details function (Nhân viên) | Tại Menu Ứng dụng phía Nhân viên: 1. Click [Xử lý đơn hàng] 2. Click [Xem] hoặc truy cập `/nhanvien/orders/[id]` |
| 82 | Function - Cập nhật trạng thái đơn hàng (Nhân viên) | Xử lý đơn hàng Nhân viên | Check GUI and FUNC update order status function (Nhân viên) | Tại Menu Ứng dụng phía Nhân viên: 1. Click [Xử lý đơn hàng] 2. Click [Cập nhật trạng thái] hoặc truy cập `/nhanvien/orders/[id]/update-status` |
| 83 | Function - Xác nhận đơn hàng (Nhân viên) | Xử lý đơn hàng Nhân viên | Check GUI and FUNC confirm order function (Nhân viên) | Tại Menu Ứng dụng phía Nhân viên: 1. Click [Xử lý đơn hàng] 2. Click [Xác nhận đơn hàng] |
| 84 | Function - Hủy đơn hàng (Nhân viên) | Xử lý đơn hàng Nhân viên | Check GUI and FUNC cancel order function (Nhân viên) | Tại Menu Ứng dụng phía Nhân viên: 1. Click [Xử lý đơn hàng] 2. Click [Hủy đơn hàng] |
| 85 | Function - In đơn hàng (Nhân viên) | Xử lý đơn hàng Nhân viên | Check GUI and FUNC print order function (Nhân viên) | Tại Menu Ứng dụng phía Nhân viên: 1. Click [Xử lý đơn hàng] 2. Click [In đơn hàng] |
| **NHÂN VIÊN - QUẢN LÝ KHÁCH HÀNG** |
| 86 | Function - Hiển thị danh sách khách hàng (Nhân viên) | Quản lý khách hàng Nhân viên | Check GUI and FUNC display customers list function (Nhân viên) | Tại Menu Ứng dụng phía Nhân viên: 1. Click [Quản lý khách hàng] hoặc truy cập `/nhanvien/customers` |
| 87 | Function - Xem chi tiết khách hàng (Nhân viên) | Quản lý khách hàng Nhân viên | Check GUI and FUNC view customer details function (Nhân viên) | Tại Menu Ứng dụng phía Nhân viên: 1. Click [Quản lý khách hàng] 2. Click [Xem] hoặc truy cập `/nhanvien/customers/[id]` |
| 88 | Function - Cập nhật thông tin khách hàng (Nhân viên) | Quản lý khách hàng Nhân viên | Check GUI and FUNC update customer information function (Nhân viên) | Tại Menu Ứng dụng phía Nhân viên: 1. Click [Quản lý khách hàng] 2. Click [Chỉnh sửa] |
| **NHÂN VIÊN - XỬ LÝ ĐỔI TRẢ** |
| 89 | Function - Hiển thị danh sách yêu cầu đổi trả (Nhân viên) | Xử lý đổi trả Nhân viên | Check GUI and FUNC display returns list function (Nhân viên) | Tại Menu Ứng dụng phía Nhân viên: 1. Click [Đổi trả] hoặc truy cập `/nhanvien/returns` |
| 90 | Function - Xem chi tiết yêu cầu đổi trả (Nhân viên) | Xử lý đổi trả Nhân viên | Check GUI and FUNC view return details function (Nhân viên) | Tại Menu Ứng dụng phía Nhân viên: 1. Click [Đổi trả] 2. Click [Xem] hoặc truy cập `/nhanvien/returns/[id]` |
| 91 | Function - Xử lý yêu cầu đổi trả (Nhân viên) | Xử lý đổi trả Nhân viên | Check GUI and FUNC process return request function (Nhân viên) | Tại Menu Ứng dụng phía Nhân viên: 1. Click [Đổi trả] 2. Click [Xử lý] |
| **NHÂN VIÊN - CHAT HỖ TRỢ** |
| 92 | Function - Chat hỗ trợ khách hàng (Nhân viên) | Chat hỗ trợ Nhân viên | Check GUI and FUNC chat support function (Nhân viên) | Tại Menu Ứng dụng phía Nhân viên: 1. Click [Hỗ trợ khách hàng] 2. Click [Chat] hoặc truy cập `/nhanvien/support` |
| 93 | Function - Xem lịch sử chat (Nhân viên) | Chat hỗ trợ Nhân viên | Check GUI and FUNC view chat history function (Nhân viên) | Tại Menu Ứng dụng phía Nhân viên: 1. Click [Hỗ trợ khách hàng] 2. Click [Lịch sử chat] |
| **NHÂN VIÊN - QUẢN LÝ YÊU CẦU** |
| 94 | Function - Hiển thị danh sách yêu cầu (Nhân viên) | Quản lý yêu cầu Nhân viên | Check GUI and FUNC display requests list function (Nhân viên) | Tại Menu Ứng dụng phía Nhân viên: 1. Click [Yêu cầu] hoặc truy cập `/nhanvien/requests` |
| 95 | Function - Xem chi tiết yêu cầu (Nhân viên) | Quản lý yêu cầu Nhân viên | Check GUI and FUNC view request details function (Nhân viên) | Tại Menu Ứng dụng phía Nhân viên: 1. Click [Yêu cầu] 2. Click [Xem] hoặc truy cập `/nhanvien/requests/[id]` |
| **NHÂN VIÊN - CẬP NHẬT ĐƠN HÀNG ONLINE** |
| 96 | Function - Cập nhật đơn hàng online (Nhân viên) | Cập nhật đơn hàng online Nhân viên | Check GUI and FUNC update online order function (Nhân viên) | Tại Menu Ứng dụng phía Nhân viên: 1. Click [Cập nhật đơn hàng online] |
| **NHÂN VIÊN - BÁO CÁO VÀ THỐNG KÊ** |
| 97 | Function - Xem báo cáo doanh thu (Nhân viên) | Báo cáo và thống kê Nhân viên | Check GUI and FUNC view revenue report function (Nhân viên) | Tại Menu Ứng dụng: 1. Click [Báo cáo & Thống kê] 2. Click [Doanh thu] hoặc truy cập `/nhanvien/reports/revenue` |
| 98 | Function - Xem báo cáo bán hàng (Nhân viên) | Báo cáo và thống kê Nhân viên | Check GUI and FUNC view sales report function (Nhân viên) | Tại Menu Ứng dụng: 1. Click [Báo cáo & Thống kê] 2. Click [Bán hàng] hoặc truy cập `/nhanvien/reports/sales` |
| **NHÂN VIÊN - BẢO MẬT** |
| 99 | Function - Xem lịch sử đăng nhập (Nhân viên) | Bảo mật Nhân viên | Check GUI and FUNC login history function (Nhân viên) | Tại Menu Ứng dụng phía Nhân viên: 1. Click [Bảo mật] 2. Click [Lịch sử đăng nhập] hoặc truy cập `/nhanvien/security/login-history` |
| 100 | Function - Quản lý phiên đăng nhập (Nhân viên) | Bảo mật Nhân viên | Check GUI and FUNC sessions management function (Nhân viên) | Tại Menu Ứng dụng phía Nhân viên: 1. Click [Bảo mật] 2. Click [Phiên đăng nhập] hoặc truy cập `/nhanvien/security/sessions` |
| **NHÂN VIÊN KHO - QUẢN LÝ TÀI KHOẢN** |
| 101 | Function - Đăng nhập (Nhân viên kho) | Quản lý tài khoản Nhân viên kho | Check GUI and FUNC login function (Nhân viên kho) | Tại Menu Ứng dụng phía Nhân viên kho: 1. Click [Đăng nhập] hoặc truy cập `/nhanvienkho/auth/login` |
| 102 | Function - Đổi mật khẩu (Nhân viên kho) | Quản lý tài khoản Nhân viên kho | Check GUI and FUNC change password function (Nhân viên kho) | Tại Menu Ứng dụng phía Nhân viên kho: 1. Click [Tài khoản] 2. Click [Đổi mật khẩu] hoặc truy cập `/nhanvienkho/account` |
| 103 | Layout - Quản lý thông tin cá nhân (Nhân viên kho) | Quản lý tài khoản Nhân viên kho | GUI function for Nhân viên kho personal information management | Tại Menu Ứng dụng phía Nhân viên kho: 1. Click [Tài khoản] hoặc truy cập `/nhanvienkho/account` |
| **NHÂN VIÊN KHO - QUẢN LÝ SÁCH** |
| 104 | Function - Hiển thị danh sách sách (Nhân viên kho) | Quản lý sách Nhân viên kho | Check GUI and FUNC display books list function (Nhân viên kho) | Tại Menu Ứng dụng phía Nhân viên kho: 1. Click [Sách] hoặc truy cập `/nhanvienkho/books` |
| 105 | Function - Xem chi tiết sách (Nhân viên kho) | Quản lý sách Nhân viên kho | Check GUI and FUNC view book details function (Nhân viên kho) | Tại Menu Ứng dụng phía Nhân viên kho: 1. Click [Sách] 2. Click vào sách hoặc truy cập `/nhanvienkho/books/[id]` |
| 106 | Function - Thêm sách mới (Nhân viên kho) | Quản lý sách Nhân viên kho | Check GUI and FUNC add new book function (Nhân viên kho) | Tại Menu Ứng dụng phía Nhân viên kho: 1. Click [Sách] 2. Click [Thêm sách] hoặc truy cập `/nhanvienkho/books/new` |
| 107 | Function - Cập nhật thông tin sách (Nhân viên kho) | Quản lý sách Nhân viên kho | Check GUI and FUNC update book information function (Nhân viên kho) | Tại Menu Ứng dụng phía Nhân viên kho: 1. Click [Sách] 2. Click [Chỉnh sửa] hoặc truy cập `/nhanvienkho/books/[id]/edit` |
| 108 | Function - Ẩn sách (Nhân viên kho) | Quản lý sách Nhân viên kho | Check GUI and FUNC hide book function (Nhân viên kho) | Tại Menu Ứng dụng phía Nhân viên kho: 1. Click [Sách] 2. Click [Ẩn sách] |
| 109 | Function - Tìm kiếm sách (Nhân viên kho) | Quản lý sách Nhân viên kho | Check GUI and FUNC search books function (Nhân viên kho) | Tại Menu Ứng dụng phía Nhân viên kho: 1. Sử dụng thanh tìm kiếm |
| **NHÂN VIÊN KHO - QUẢN LÝ TỒN KHO** |
| 110 | Function - Hiển thị danh sách tồn kho (Nhân viên kho) | Quản lý tồn kho Nhân viên kho | Check GUI and FUNC display inventory list function (Nhân viên kho) | Tại Menu Ứng dụng phía Nhân viên kho: 1. Click [Tồn kho] hoặc truy cập `/nhanvienkho/inventory` |
| 111 | Function - Cập nhật số lượng tồn kho (Nhân viên kho) | Quản lý tồn kho Nhân viên kho | Check GUI and FUNC update inventory quantity function (Nhân viên kho) | Tại Menu Ứng dụng phía Nhân viên kho: 1. Click [Tồn kho] 2. Click [Cập nhật] |
| 112 | Function - Nhập hàng (Nhân viên kho) | Quản lý tồn kho Nhân viên kho | Check GUI and FUNC import goods function (Nhân viên kho) | Tại Menu Ứng dụng phía Nhân viên kho: 1. Click [Tồn kho] 2. Click [Nhập hàng] hoặc truy cập `/nhanvienkho/inventory/import` |
| 113 | Function - Xuất hàng (Nhân viên kho) | Quản lý tồn kho Nhân viên kho | Check GUI and FUNC export goods function (Nhân viên kho) | Tại Menu Ứng dụng phía Nhân viên kho: 1. Click [Tồn kho] 2. Click [Xuất hàng] hoặc truy cập `/nhanvienkho/inventory/export` |
| 114 | Function - Kiểm kê tồn kho (Nhân viên kho) | Quản lý tồn kho Nhân viên kho | Check GUI and FUNC inventory audit function (Nhân viên kho) | Tại Menu Ứng dụng phía Nhân viên kho: 1. Click [Tồn kho] 2. Click [Kiểm kê] hoặc truy cập `/nhanvienkho/inventory/audit` |
| **NHÂN VIÊN KHO - BÁO CÁO KHO** |
| 115 | Function - Xem sách tồn kho thấp (Nhân viên kho) | Báo cáo kho Nhân viên kho | Check GUI and FUNC view low stock books function (Nhân viên kho) | Tại Menu Ứng dụng: 1. Click [Báo cáo] 2. Click [Sách tồn kho thấp] hoặc truy cập `/nhanvienkho/reports/low-stock` |
| 116 | Function - Xem báo cáo tồn kho (Nhân viên kho) | Báo cáo kho Nhân viên kho | Check GUI and FUNC view inventory report function (Nhân viên kho) | Tại Menu Ứng dụng: 1. Click [Báo cáo] 2. Click [Báo cáo tồn kho] hoặc truy cập `/nhanvienkho/reports/inventory` |
| 117 | Function - Xem lịch sử nhập/xuất (Nhân viên kho) | Báo cáo kho Nhân viên kho | Check GUI and FUNC view import/export history function (Nhân viên kho) | Tại Menu Ứng dụng: 1. Click [Báo cáo] 2. Click [Lịch sử nhập/xuất] hoặc truy cập `/nhanvienkho/reports/history` |
| **NHÂN VIÊN KHO - XỬ LÝ YÊU CẦU** |
| 118 | Function - Hiển thị danh sách yêu cầu (Nhân viên kho) | Xử lý yêu cầu Nhân viên kho | Check GUI and FUNC display requests list function (Nhân viên kho) | Tại Menu Ứng dụng phía Nhân viên kho: 1. Click [Yêu cầu] hoặc truy cập `/nhanvienkho/requests` |
| 119 | Function - Xem chi tiết yêu cầu (Nhân viên kho) | Xử lý yêu cầu Nhân viên kho | Check GUI and FUNC view request details function (Nhân viên kho) | Tại Menu Ứng dụng phía Nhân viên kho: 1. Click [Yêu cầu] 2. Click [Xem] hoặc truy cập `/nhanvienkho/requests/[id]` |
| 120 | Function - Xử lý yêu cầu nhập hàng (Nhân viên kho) | Xử lý yêu cầu Nhân viên kho | Check GUI and FUNC process import request function (Nhân viên kho) | Tại Menu Ứng dụng phía Nhân viên kho: 1. Click [Yêu cầu] 2. Click [Xử lý yêu cầu nhập] |
| 121 | Function - Xử lý yêu cầu xuất hàng (Nhân viên kho) | Xử lý yêu cầu Nhân viên kho | Check GUI and FUNC process export request function (Nhân viên kho) | Tại Menu Ứng dụng phía Nhân viên kho: 1. Click [Yêu cầu] 2. Click [Xử lý yêu cầu xuất] |
| 122 | Function - Theo dõi trạng thái yêu cầu (Nhân viên kho) | Xử lý yêu cầu Nhân viên kho | Check GUI and FUNC track request status function (Nhân viên kho) | Tại Menu Ứng dụng phía Nhân viên kho: 1. Click [Yêu cầu] 2. Click [Theo dõi trạng thái] |
| **NHÂN VIÊN KHO - HỖ TRỢ BÁN HÀNG** |
| 123 | Function - Kiểm tra tồn kho cho đơn hàng (Nhân viên kho) | Hỗ trợ bán hàng Nhân viên kho | Check GUI and FUNC check stock for order function (Nhân viên kho) | Tại Menu Ứng dụng phía Nhân viên kho: 1. Click [Hỗ trợ bán hàng] 2. Click [Kiểm tra tồn kho] |
| 124 | Function - Xác nhận khả năng giao hàng (Nhân viên kho) | Hỗ trợ bán hàng Nhân viên kho | Check GUI and FUNC confirm delivery capability function (Nhân viên kho) | Tại Menu Ứng dụng phía Nhân viên kho: 1. Click [Hỗ trợ bán hàng] 2. Click [Xác nhận giao hàng] |
| 125 | Function - Cập nhật trạng thái đơn hàng (Nhân viên kho) | Hỗ trợ bán hàng Nhân viên kho | Check GUI and FUNC update order status function (Nhân viên kho) | Tại Menu Ứng dụng phía Nhân viên kho: 1. Click [Hỗ trợ bán hàng] 2. Click [Cập nhật trạng thái] |
| 126 | Function - Hỗ trợ xử lý đơn đặc biệt (Nhân viên kho) | Hỗ trợ bán hàng Nhân viên kho | Check GUI and FUNC support special order processing function (Nhân viên kho) | Tại Menu Ứng dụng phía Nhân viên kho: 1. Click [Hỗ trợ bán hàng] 2. Click [Đơn đặc biệt] |
| **NHÂN VIÊN KHO - BẢO MẬT** |
| 127 | Function - Xem lịch sử đăng nhập (Nhân viên kho) | Bảo mật Nhân viên kho | Check GUI and FUNC login history function (Nhân viên kho) | Tại Menu Ứng dụng phía Nhân viên kho: 1. Click [Bảo mật] 2. Click [Lịch sử đăng nhập] hoặc truy cập `/nhanvienkho/security/sessions` |
| 128 | Function - Quản lý phiên đăng nhập (Nhân viên kho) | Bảo mật Nhân viên kho | Check GUI and FUNC sessions management function (Nhân viên kho) | Tại Menu Ứng dụng phía Nhân viên kho: 1. Click [Bảo mật] 2. Click [Phiên đăng nhập] hoặc truy cập `/nhanvienkho/security/sessions` |
| **USER - QUẢN LÝ TÀI KHOẢN** |
| 129 | Function - Đăng ký (User) | Quản lý tài khoản User | Check GUI and FUNC register function (User) | Tại Menu Ứng dụng phía User: 1. Click [Đăng ký] hoặc truy cập `/user/auth/register` |
| 130 | Function - Đăng nhập (User) | Quản lý tài khoản User | Check GUI and FUNC login function (User) | Tại Menu Ứng dụng phía User: 1. Click [Đăng nhập] hoặc truy cập `/user/auth/login` |
| 131 | Function - Đổi mật khẩu (User) | Quản lý tài khoản User | Check GUI and FUNC change password function (User) | Tại Menu Ứng dụng phía User: 1. Click [Tài khoản] 2. Click [Đổi mật khẩu] hoặc truy cập `/user/account` |
| 132 | Layout - Quản lý thông tin cá nhân (User) | Quản lý tài khoản User | GUI function for User personal information management | Tại Menu Ứng dụng phía User: 1. Click [Tài khoản] hoặc truy cập `/user/account` |
| 133 | Function - Khôi phục mật khẩu (User) | Quản lý tài khoản User | Check GUI and FUNC forgot password function (User) | Tại Menu Ứng dụng phía User: 1. Click [Đăng nhập] 2. Click [Quên mật khẩu] hoặc truy cập `/user/auth/forgot-password` |
| 134 | Function - Xem điểm tích lũy và hạng thành viên (User) | Quản lý tài khoản User | Check GUI and FUNC view loyalty points and membership rank function (User) | Tại Menu Ứng dụng phía User: 1. Click [Tài khoản] 2. Click [Hạng thành viên] hoặc truy cập `/user/account/rank` |
| **USER - HIỂN THỊ SÁCH** |
| 135 | Function - Hiển thị danh sách sách (User) | Hiển thị sách User | Check GUI and FUNC display books list function (User) | Tại Menu Ứng dụng phía User: 1. Click [Sách] hoặc truy cập `/user/products` |
| 136 | Function - Xem chi tiết sách (User) | Hiển thị sách User | Check GUI and FUNC view book details function (User) | Tại Menu Ứng dụng phía User: 1. Click [Sách] 2. Click vào sách hoặc truy cập `/user/products/[id]` |
| 137 | Function - Hiển thị nội dung đọc thử (User) | Hiển thị sách User | Check GUI and FUNC display read trial content function (User) | Tại Trang chi tiết sách: 1. Click [Đọc thử] |
| **USER - TÌM KIẾM SÁCH** |
| 138 | Function - Tìm kiếm sách (User) | Tìm kiếm sách User | Check GUI and FUNC search books function (User) | Tại Menu Ứng dụng phía User: 1. Click [Tìm kiếm] hoặc truy cập `/user/search` |
| 139 | Function - Hiển thị kết quả tìm kiếm (User) | Tìm kiếm sách User | Check GUI and FUNC display search results function (User) | Tại Trang tìm kiếm: 1. Nhập từ khóa 2. Click [Tìm kiếm] |
| **USER - BỘ LỌC SÁCH** |
| 140 | Layout - Bộ lọc sách (User) | Bộ lọc sách User | GUI function for book filtering | Tại Menu Ứng dụng phía User: 1. Click [Sách] hoặc truy cập `/user/products` |
| 141 | Function - Lọc sách theo khoảng giá (User) | Bộ lọc sách User | Check GUI and FUNC filter books by price range function (User) | Tại Trang danh sách sách: 1. Sử dụng bộ lọc giá |
| 142 | Function - Lọc sách theo năm xuất bản (User) | Bộ lọc sách User | Check GUI and FUNC filter books by publication year function (User) | Tại Trang danh sách sách: 1. Sử dụng bộ lọc năm xuất bản |
| 143 | Function - Lọc sách theo nhà xuất bản (User) | Bộ lọc sách User | Check GUI and FUNC filter books by publisher function (User) | Tại Trang danh sách sách: 1. Sử dụng bộ lọc nhà xuất bản |
| 144 | Function - Sắp xếp danh sách sách (User) | Bộ lọc sách User | Check GUI and FUNC sort books list function (User) | Tại Trang danh sách sách: 1. Sử dụng bộ sắp xếp |
| **USER - QUẢN LÝ GIỎ HÀNG** |
| 145 | Function - Thêm sách vào giỏ hàng (User) | Quản lý giỏ hàng User | Check GUI and FUNC add book to cart function (User) | Tại Trang chi tiết sách: 1. Click [Thêm vào giỏ hàng] |
| 146 | Function - Hiển thị giỏ hàng (User) | Quản lý giỏ hàng User | Check GUI and FUNC view cart function (User) | Tại Menu chính: 1. Click [Giỏ hàng] hoặc truy cập `/user/cart` |
| 147 | Function - Xóa sách khỏi giỏ hàng (User) | Quản lý giỏ hàng User | Check GUI and FUNC remove book from cart function (User) | Tại Trang giỏ hàng: 1. Click [Xóa] |
| 148 | Function - Cập nhật số lượng sách (User) | Quản lý giỏ hàng User | Check GUI and FUNC update book quantity function (User) | Tại Trang giỏ hàng: 1. Thay đổi số lượng |
| 149 | Function - Đặt hàng (User) | Quản lý giỏ hàng User | Check GUI and FUNC place order function (User) | Tại Trang giỏ hàng: 1. Click [Đặt hàng] hoặc truy cập `/user/checkout` |
| **USER - THANH TOÁN ĐƠN HÀNG** |
| 150 | Function - Nhập thông tin địa chỉ (User) | Thanh toán đơn hàng User | Check GUI and FUNC enter address information function (User) | Tại Trang thanh toán: 1. Nhập thông tin địa chỉ hoặc truy cập `/user/checkout` |
| 151 | Function - Hiển thị phương thức thanh toán (User) | Thanh toán đơn hàng User | Check GUI and FUNC display payment methods function (User) | Tại Trang thanh toán: 1. Xem danh sách phương thức thanh toán |
| 152 | Function - Chọn phương thức thanh toán (User) | Thanh toán đơn hàng User | Check GUI and FUNC select payment method function (User) | Tại Trang thanh toán: 1. Chọn phương thức thanh toán |
| 153 | Function - Thanh toán khi nhận hàng (COD) (User) | Thanh toán đơn hàng User | Check GUI and FUNC COD payment function (User) | Tại Trang thanh toán: 1. Chọn [Thanh toán khi nhận hàng] 2. Click [Xác nhận] |
| 154 | Function - Thanh toán online Banking/VNPay (User) | Thanh toán đơn hàng User | Check GUI and FUNC online banking/VNPay payment function (User) | Tại Trang thanh toán: 1. Chọn [Thanh toán online] 2. Chọn [Banking/VNPay] 3. Click [Xác nhận] |
| 155 | Function - Thanh toán MoMo (User) | Thanh toán đơn hàng User | Check GUI and FUNC MoMo payment function (User) | Tại Trang thanh toán: 1. Chọn [MoMo] 2. Click [Xác nhận] |
| 156 | Function - Thanh toán ZaloPay (User) | Thanh toán đơn hàng User | Check GUI and FUNC ZaloPay payment function (User) | Tại Trang thanh toán: 1. Chọn [ZaloPay] 2. Click [Xác nhận] |
| 157 | Function - Thanh toán Viettel Money (User) | Thanh toán đơn hàng User | Check GUI and FUNC Viettel Money payment function (User) | Tại Trang thanh toán: 1. Chọn [Viettel Money] 2. Click [Xác nhận] |
| 158 | Function - Xác nhận đơn hàng (User) | Thanh toán đơn hàng User | Check GUI and FUNC confirm order function (User) | Tại Trang thanh toán: 1. Click [Xác nhận đơn hàng] |
| **USER - VẬN CHUYỂN** |
| 159 | Layout - Chọn phương thức vận chuyển (User) | Vận chuyển User | GUI function for shipping method selection | Tại Trang thanh toán: 1. Chọn phương thức vận chuyển |
| 160 | Function - Hiển thị danh sách đơn vị vận chuyển (User) | Vận chuyển User | Check GUI and FUNC display shipping carriers function (User) | Tại Trang thanh toán: 1. Xem danh sách đơn vị vận chuyển |
| 161 | Function - Chọn đơn vị vận chuyển (User) | Vận chuyển User | Check GUI and FUNC select shipping carrier function (User) | Tại Trang thanh toán: 1. Chọn đơn vị vận chuyển |
| **USER - QUẢN LÝ ĐƠN HÀNG** |
| 162 | Function - Hiển thị danh sách đơn hàng (User) | Quản lý đơn hàng User | Check GUI and FUNC display orders list function (User) | Tại Menu Ứng dụng phía User: 1. Click [Lịch sử đơn hàng] hoặc truy cập `/user/account/orders` |
| 163 | Function - Xem chi tiết đơn hàng (User) | Quản lý đơn hàng User | Check GUI and FUNC view order details function (User) | Tại Menu Ứng dụng phía User: 1. Click [Lịch sử đơn hàng] 2. Click [Xem chi tiết] hoặc truy cập `/user/orders/[id]` |
| 164 | Function - Đặt lại đơn hàng (User) | Quản lý đơn hàng User | Check GUI and FUNC reorder function (User) | Tại Trang chi tiết đơn hàng: 1. Click [Đặt lại] |
| 165 | Function - Đánh giá đơn hàng (User) | Quản lý đơn hàng User | Check GUI and FUNC rate order function (User) | Tại Trang chi tiết đơn hàng: 1. Click [Đánh giá] |
| 166 | Function - Hủy đơn hàng (User) | Quản lý đơn hàng User | Check GUI and FUNC cancel order function (User) | Tại Trang chi tiết đơn hàng: 1. Click [Hủy đơn hàng] |
| 167 | Function - Theo dõi đơn hàng (User) | Quản lý đơn hàng User | Check GUI and FUNC track order function (User) | Tại Trang chi tiết đơn hàng: 1. Click [Theo dõi đơn hàng] hoặc truy cập `/user/orders/track/[id]` |
| 168 | Function - Yêu cầu đổi/trả hàng (User) | Quản lý đơn hàng User | Check GUI and FUNC request return/exchange function (User) | Tại Trang chi tiết đơn hàng đã giao: 1. Click [Yêu cầu đổi/trả hàng] hoặc truy cập `/user/returns` |
| **USER - KHUYẾN MÃI** |
| 169 | Function - Hiển thị danh sách mã giảm giá (User) | Khuyến mãi User | Check GUI and FUNC display discount codes function (User) | Tại Menu Ứng dụng: 1. Click [Khuyến mãi] hoặc truy cập `/user/promotions` |
| 170 | Function - Xem chi tiết khuyến mãi (User) | Khuyến mãi User | Check GUI and FUNC view promotion details function (User) | Tại Trang khuyến mãi: 1. Click vào khuyến mãi hoặc truy cập `/user/promotions/[code]` |
| 171 | Function - Xem hạng thành viên (User) | Khuyến mãi User | Check GUI and FUNC view membership rank function (User) | Tại Trang khuyến mãi: 1. Click [Hạng thành viên] |
| 172 | Function - Xem hạng hiện tại (User) | Khuyến mãi User | Check GUI and FUNC view current rank function (User) | Tại Trang khuyến mãi: 1. Xem hạng hiện tại |
| 173 | Function - Xem giảm giá theo sản phẩm (User) | Khuyến mãi User | Check GUI and FUNC view product-specific discounts function (User) | Tại Trang chi tiết sách: 1. Xem thông tin giảm giá |
| **USER - ĐÁNH GIÁ VÀ NHẬN XÉT** |
| 174 | Function - Đánh giá sách (1-5 sao) (User) | Đánh giá và nhận xét User | Check GUI and FUNC rate book function (User) | Tại Trang chi tiết sách: 1. Click [Đánh giá] 2. Chọn số sao |
| 175 | Function - Viết nhận xét (User) | Đánh giá và nhận xét User | Check GUI and FUNC write review function (User) | Tại Trang chi tiết sách: 1. Click [Viết nhận xét] 2. Nhập nội dung |
| 176 | Function - Xem nhận xét của khách hàng khác (User) | Đánh giá và nhận xét User | Check GUI and FUNC view other customers reviews function (User) | Tại Trang chi tiết sách: 1. Scroll xuống phần đánh giá |
| **USER - DANH SÁCH SÁCH YÊU THÍCH** |
| 177 | Function - Thêm sách vào yêu thích (User) | Danh sách sách yêu thích User | Check GUI and FUNC add book to wishlist function (User) | Tại Trang chi tiết sách: 1. Click [Thêm vào yêu thích] |
| 178 | Function - Xem danh sách yêu thích (User) | Danh sách sách yêu thích User | Check GUI and FUNC view wishlist function (User) | Tại Menu Ứng dụng phía User: 1. Click [Yêu thích] hoặc truy cập `/user/wishlist` |
| 179 | Function - Xóa sách khỏi yêu thích (User) | Danh sách sách yêu thích User | Check GUI and FUNC remove book from wishlist function (User) | Tại Trang yêu thích: 1. Click [Xóa] |
| **USER - HỖ TRỢ** |
| 180 | Function - Chat/Liên hệ nhân viên hỗ trợ (User) | Hỗ trợ User | Check GUI and FUNC chat/contact support staff function (User) | Tại Menu Ứng dụng phía User: 1. Click [Hỗ trợ] 2. Click [Chat] hoặc truy cập `/user/support` |
| 181 | Function - Gửi phản hồi/khiếu nại (User) | Hỗ trợ User | Check GUI and FUNC send feedback/complaint function (User) | Tại Menu Ứng dụng phía User: 1. Click [Hỗ trợ] 2. Click [Gửi phản hồi] |
| **USER - YÊU CẦU NHẬP HÀNG** |
| 182 | Function - Yêu cầu nhập lại sách hết hàng (User) | Yêu cầu nhập hàng User | Check GUI and FUNC request restocking out-of-stock books function (User) | Tại Menu Ứng dụng phía User: 1. Click [Yêu cầu nhập hàng] hoặc truy cập `/user/requests` |
| 183 | Function - Yêu cầu nhập sách mới theo gợi ý (User) | Yêu cầu nhập hàng User | Check GUI and FUNC request new books based on customer suggestions function (User) | Tại Menu Ứng dụng phía User: 1. Click [Yêu cầu nhập hàng] 2. Click [Yêu cầu sách mới] |
| 184 | Function - Xem danh sách yêu cầu đã gửi (User) | Yêu cầu nhập hàng User | Check GUI and FUNC view sent import requests function (User) | Tại Menu Ứng dụng phía User: 1. Click [Yêu cầu nhập hàng] 2. Xem danh sách |
| 185 | Function - Xem chi tiết yêu cầu nhập hàng (User) | Yêu cầu nhập hàng User | Check GUI and FUNC view import request details function (User) | Tại Trang danh sách yêu cầu: 1. Click [Xem chi tiết] hoặc truy cập `/user/requests/[id]` |
| 186 | Function - Hủy yêu cầu nhập hàng (User) | Yêu cầu nhập hàng User | Check GUI and FUNC cancel import request function (User) | Tại Trang chi tiết yêu cầu: 1. Click [Hủy yêu cầu] |
| **USER - THÔNG BÁO** |
| 187 | Function - Hiển thị danh sách thông báo (User) | Thông báo User | Check GUI and FUNC display notifications list function (User) | Tại Menu Ứng dụng phía User: 1. Click [Thông báo] hoặc truy cập `/user/notifications` |
| 188 | Function - Thông báo sách có hàng (User) | Thông báo User | Check GUI and FUNC notifications for in-stock books function (User) | Tại Trang thông báo: 1. Xem thông báo sách có hàng |
| 189 | Function - Thông báo sách giảm giá (User) | Thông báo User | Check GUI and FUNC notifications for discounted books function (User) | Tại Trang thông báo: 1. Xem thông báo sách giảm giá |
| 190 | Function - Thông báo trạng thái đơn hàng (User) | Thông báo User | Check GUI and FUNC order status notifications function (User) | Tại Trang thông báo: 1. Xem thông báo trạng thái đơn hàng |
| **USER - BÀI VIẾT** |
| 191 | Function - Hiển thị danh sách bài viết (User) | Bài viết User | Check GUI and FUNC display posts list function (User) | Tại Menu Ứng dụng phía User: 1. Click [Bài viết] hoặc truy cập `/user/posts` |
| 192 | Function - Xem chi tiết bài viết (User) | Bài viết User | Check GUI and FUNC view post details function (User) | Tại Trang danh sách bài viết: 1. Click vào bài viết hoặc truy cập `/user/posts/[id]` |
| 193 | Function - Tạo bài viết (User) | Bài viết User | Check GUI and FUNC create post function (User) | Tại Menu Ứng dụng phía User: 1. Click [Tạo bài viết] hoặc truy cập `/user/posts/create` |
| 194 | Function - Chỉnh sửa bài viết (User) | Bài viết User | Check GUI and FUNC edit post function (User) | Tại Trang chi tiết bài viết: 1. Click [Chỉnh sửa] hoặc truy cập `/user/posts/[id]/edit` |
| **USER - BẢO MẬT** |
| 195 | Function - Đổi mật khẩu (User) | Bảo mật User | Check GUI and FUNC change password function (User) | Tại Menu Ứng dụng phía User: 1. Click [Tài khoản] 2. Click [Bảo mật] 3. Click [Đổi mật khẩu] hoặc truy cập `/user/account/security` |
| 196 | Function - Cài đặt bảo mật (User) | Bảo mật User | Check GUI and FUNC security settings function (User) | Tại Menu Ứng dụng phía User: 1. Click [Tài khoản] 2. Click [Bảo mật] hoặc truy cập `/user/account/security` |
| 197 | Function - Xem hoạt động bảo mật gần đây (User) | Bảo mật User | Check GUI and FUNC view recent security activities function (User) | Tại Trang bảo mật: 1. Xem hoạt động bảo mật gần đây |

---

## GHI CHÚ QUAN TRỌNG

### Về Routes:
- Tất cả routes được xác định dựa trên cấu trúc thư mục `src/app/admin/`, `src/app/nhanvien/`, `src/app/nhanvienkho/`, và `src/app/user/`
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

**Tổng số chức năng:** 197 functions  
**Admin:** 73 functions  
**Nhân viên:** 27 functions  
**Nhân viên kho:** 28 functions  
**User:** 69 functions

