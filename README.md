# BLACKBOX TEST CASE - USER FUNCTIONS

**Dự án:** Hệ Thống Quản Lý Model Shop  
**Ngày tạo:** 2025  
**Mục đích:** Tài liệu tổng quan về các chức năng User và routes để thực hiện blackbox testing

---

## BẢNG TỔNG HỢP TEST CASE

| No | Function Name | Sheet Name | Description | Pre-Condition (Route) |
|----|---------------|------------|-------------|----------------------|
| **USER - QUẢN LÝ TÀI KHOẢN** |
| 1 | Function - Đăng nhập (User) | Quản lý tài khoản User | Check GUI and FUNC login function (User) | Tại Menu Ứng dụng phía User: 1. Click [Đăng nhập] hoặc truy cập `/user/auth/login` |
| 2 | Function - Đăng ký (User) | Quản lý tài khoản User | Check GUI and FUNC register function (User) | Tại Menu Ứng dụng phía User: 1. Click [Đăng ký] hoặc truy cập `/user/auth/register` |
| 3 | Function - Đổi mật khẩu (User) | Quản lý tài khoản User | Check GUI and FUNC change password function (User) | Tại Menu Ứng dụng phía User: 1. Click [Tài khoản] 2. Click [Đổi mật khẩu] hoặc truy cập `/user/account` |
| 4 | Function - Cập nhật thông tin cá nhân (User) | Quản lý tài khoản User | Check GUI and FUNC update personal information function (User) | Tại Menu Ứng dụng phía User: 1. Click [Tài khoản] 2. Click [Cập nhật thông tin] hoặc truy cập `/user/account` |
| 5 | Layout - Quản lý thông tin cá nhân (User) | Quản lý tài khoản User | GUI function for User personal information management | Tại Menu Ứng dụng phía User: 1. Click [Tài khoản] hoặc truy cập `/user/account` |
| 5.1 | Function - Khôi phục mật khẩu (User) | Quản lý tài khoản User | Check GUI and FUNC forgot password function (User) | Tại Menu Ứng dụng phía User: 1. Click [Đăng nhập] 2. Click [Quên mật khẩu] hoặc truy cập `/user/auth/forgot-password` |
| 5.2 | Function - Quản lý địa chỉ (User) | Quản lý tài khoản User | Check GUI and FUNC manage addresses function (User) | Tại Menu Ứng dụng phía User: 1. Click [Tài khoản] 2. Click [Địa chỉ] hoặc truy cập `/user/account/addresses` |
| 5.3 | Function - Quản lý thanh toán (User) | Quản lý tài khoản User | Check GUI and FUNC manage payments function (User) | Tại Menu Ứng dụng phía User: 1. Click [Tài khoản] 2. Click [Thanh toán] hoặc truy cập `/user/account/payments` |
| 5.4 | Function - Xem hạng thành viên (User) | Quản lý tài khoản User | Check GUI and FUNC view membership rank function (User) | Tại Menu Ứng dụng phía User: 1. Click [Tài khoản] 2. Click [Hạng thành viên] hoặc truy cập `/user/account/rank` |
| 5.5 | Function - Xem lịch sử đăng nhập (User) | Quản lý tài khoản User | Check GUI and FUNC view login history function (User) | Tại Menu Ứng dụng phía User: 1. Click [Tài khoản] 2. Click [Lịch sử đăng nhập] hoặc truy cập `/user/account/logins` |
| 5.6 | Function - Quản lý phiên đăng nhập (User) | Quản lý tài khoản User | Check GUI and FUNC manage sessions function (User) | Tại Menu Ứng dụng phía User: 1. Click [Tài khoản] 2. Click [Phiên đăng nhập] hoặc truy cập `/user/account/sessions` |
| 5.7 | Function - Đăng xuất (User) | Quản lý tài khoản User | Check GUI and FUNC logout function (User) | Tại Menu Ứng dụng phía User: 1. Click [Đăng xuất] hoặc truy cập `/user/logout` |
| **USER - HIỂN THỊ SẢN PHẨM** |
| 6 | Function - Hiển thị danh sách sản phẩm (User) | Hiển thị sản phẩm User | Check GUI and FUNC display products list function (User) | Tại Menu Ứng dụng phía User: 1. Click [Mô hình] hoặc truy cập `/user/products` |
| 7 | Function - Xem chi tiết sản phẩm (User) | Hiển thị sản phẩm User | Check GUI and FUNC view product details function (User) | Tại Menu Ứng dụng phía User: 1. Click [Mô hình] 2. Click vào sản phẩm hoặc truy cập `/user/products/[id]` |
| 7.1 | Function - Chuyển đổi chế độ xem (Grid/List) (User) | Hiển thị sản phẩm User | Check GUI and FUNC toggle view mode function (User) | Tại Trang danh sách sản phẩm: 1. Click nút chuyển đổi Grid/List |
| 7.2 | Function - Xem hình ảnh sản phẩm (User) | Hiển thị sản phẩm User | Check GUI and FUNC view product images function (User) | Tại Trang chi tiết sản phẩm: 1. Click vào hình ảnh để xem full size |
| 7.3 | Function - Xem thông số kỹ thuật sản phẩm (User) | Hiển thị sản phẩm User | Check GUI and FUNC view product specifications function (User) | Tại Trang chi tiết sản phẩm: 1. Click tab [Thông số kỹ thuật] |
| **USER - TÌM KIẾM SẢN PHẨM** |
| 8 | Function - Tìm kiếm sản phẩm (User) | Tìm kiếm sản phẩm User | Check GUI and FUNC search products function (User) | Tại Menu Ứng dụng: 1. Click [Tìm kiếm] hoặc truy cập `/user/search` |
| 8.1 | Function - Gợi ý tìm kiếm (User) | Tìm kiếm sản phẩm User | Check GUI and FUNC search suggestions function (User) | Tại Trang tìm kiếm: 1. Nhập từ khóa vào ô tìm kiếm - Hệ thống hiển thị gợi ý |
| 8.2 | Function - Lịch sử tìm kiếm (User) | Tìm kiếm sản phẩm User | Check GUI and FUNC search history function (User) | Tại Trang tìm kiếm: 1. Xem lịch sử tìm kiếm gần đây |
| 8.3 | Function - Xóa lịch sử tìm kiếm (User) | Tìm kiếm sản phẩm User | Check GUI and FUNC clear search history function (User) | Tại Trang tìm kiếm: 1. Click [Xóa lịch sử] |
| **USER - BỘ LỌC VÀ PHÂN LOẠI** |
| 9 | Layout - Bộ lọc sản phẩm (User) | Bộ lọc sản phẩm User | GUI function for product filtering and categorization | Tại Menu Ứng dụng phía User: 1. Click [Mô hình] hoặc truy cập `/user/products` |
| 9.1 | Function - Lọc theo danh mục (User) | Bộ lọc sản phẩm User | Check GUI and FUNC filter by category function (User) | Tại Trang danh sách sản phẩm: 1. Chọn danh mục từ dropdown |
| 9.2 | Function - Lọc theo thương hiệu (User) | Bộ lọc sản phẩm User | Check GUI and FUNC filter by brand function (User) | Tại Trang danh sách sản phẩm: 1. Chọn thương hiệu từ dropdown |
| 9.3 | Function - Lọc theo khoảng giá (User) | Bộ lọc sản phẩm User | Check GUI and FUNC filter by price range function (User) | Tại Trang danh sách sản phẩm: 1. Điều chỉnh slider khoảng giá |
| 9.4 | Function - Sắp xếp sản phẩm (User) | Bộ lọc sản phẩm User | Check GUI and FUNC sort products function (User) | Tại Trang danh sách sản phẩm: 1. Chọn tiêu chí sắp xếp (giá, đánh giá, mới nhất) |
| 9.5 | Function - Xóa bộ lọc (User) | Bộ lọc sản phẩm User | Check GUI and FUNC clear filters function (User) | Tại Trang danh sách sản phẩm: 1. Click [Xóa bộ lọc] |
| **USER - QUẢN LÝ GIỎ HÀNG** |
| 10 | Function - Thêm sản phẩm vào giỏ hàng (User) | Quản lý giỏ hàng User | Check GUI and FUNC add product to cart function (User) | Tại Danh sách sản phẩm hoặc trang chi tiết: 1. Click [Thêm vào giỏ hàng] |
| 11 | Function - Hiển thị giỏ hàng (User) | Quản lý giỏ hàng User | Check GUI and FUNC view cart function (User) | Tại Menu chính: 1. Click [Giỏ hàng] hoặc truy cập `/user/cart` |
| 12 | Function - Xóa sản phẩm khỏi giỏ hàng (User) | Quản lý giỏ hàng User | Check GUI and FUNC delete product from cart function (User) | Tại Trang giỏ hàng: 1. Click [Xóa] bên cạnh sản phẩm |
| 13 | Function - Cập nhật số lượng sản phẩm (User) | Quản lý giỏ hàng User | Check GUI and FUNC update product quantity function (User) | Tại Trang giỏ hàng: 1. Thay đổi số lượng bằng nút +/- hoặc nhập trực tiếp |
| 14 | Function - Chọn/Bỏ chọn sản phẩm (User) | Quản lý giỏ hàng User | Check GUI and FUNC select/deselect product function (User) | Tại Trang giỏ hàng: 1. Click checkbox để chọn/bỏ chọn sản phẩm |
| 15 | Function - Chọn tất cả sản phẩm (User) | Quản lý giỏ hàng User | Check GUI and FUNC select all products function (User) | Tại Trang giỏ hàng: 1. Click [Chọn tất cả] |
| 16 | Function - Áp dụng mã giảm giá (User) | Quản lý giỏ hàng User | Check GUI and FUNC apply discount code function (User) | Tại Trang giỏ hàng: 1. Nhập mã giảm giá 2. Click [Áp dụng] |
| 17 | Function - Xóa mã giảm giá (User) | Quản lý giỏ hàng User | Check GUI and FUNC remove discount code function (User) | Tại Trang giỏ hàng: 1. Click [Xóa mã] sau khi đã áp dụng |
| 18 | Function - Thêm vào yêu thích từ giỏ hàng (User) | Quản lý giỏ hàng User | Check GUI and FUNC add to wishlist from cart function (User) | Tại Trang giỏ hàng: 1. Click [Thêm yêu thích] bên cạnh sản phẩm |
| 19 | Function - Thực hiện thanh toán (User) | Quản lý giỏ hàng User | Check GUI and FUNC proceed to checkout function (User) | Tại Trang giỏ hàng: 1. Click [Thanh toán] hoặc truy cập `/user/checkout` |
| 19.1 | Function - Tính phí vận chuyển (User) | Quản lý giỏ hàng User | Check GUI and FUNC calculate shipping fee function (User) | Tại Trang giỏ hàng: 1. Nhập địa chỉ giao hàng 2. Hệ thống tự động tính phí |
| 19.2 | Function - Chọn đơn vị vận chuyển (User) | Quản lý giỏ hàng User | Check GUI and FUNC select shipping carrier function (User) | Tại Trang giỏ hàng: 1. Chọn đơn vị vận chuyển (GHTK, GHN, J&T) |
| **USER - THANH TOÁN ĐƠN HÀNG** |
| 20 | Function - Chọn phương thức thanh toán (User) | Thanh toán đơn hàng User | Check GUI and FUNC select payment method function (User) | Tại Trang thanh toán: 1. Chọn phương thức thanh toán (COD, Banking, E-wallet) |
| 21 | Function - Thanh toán khi nhận hàng (User) | Thanh toán đơn hàng User | Check GUI and FUNC cash on delivery payment function (User) | Tại Trang thanh toán: 1. Chọn [Thanh toán khi nhận hàng] 2. Click [Xác nhận đơn hàng] |
| 22 | Function - Thanh toán VNPAY (User) | Thanh toán đơn hàng User | Check GUI and FUNC VNPAY payment function (User) | Tại Trang thanh toán: 1. Chọn [Thanh toán VNPAY] 2. Click [Xác nhận thanh toán] hoặc truy cập `/user/checkout/processing` |
| 23 | Function - Thanh toán ví điện tử (User) | Thanh toán đơn hàng User | Check GUI and FUNC e-wallet payment function (User) | Tại Trang thanh toán: 1. Chọn [Ví điện tử] (MoMo, ZaloPay) 2. Click [Xác nhận] |
| 24 | Function - Xác nhận đơn hàng (User) | Thanh toán đơn hàng User | Check GUI and FUNC confirm order function (User) | Tại Trang thanh toán: 1. Điền đầy đủ thông tin giao hàng 2. Click [Xác nhận đơn hàng] |
| 24.1 | Function - Sử dụng địa chỉ đã lưu (User) | Thanh toán đơn hàng User | Check GUI and FUNC use saved address function (User) | Tại Trang thanh toán: 1. Check [Sử dụng địa chỉ đã lưu] |
| 24.2 | Function - Lưu địa chỉ làm mặc định (User) | Thanh toán đơn hàng User | Check GUI and FUNC save address as default function (User) | Tại Trang thanh toán: 1. Check [Lưu địa chỉ này làm mặc định] |
| 24.3 | Function - Đồng ý điều khoản (User) | Thanh toán đơn hàng User | Check GUI and FUNC accept terms function (User) | Tại Trang thanh toán: 1. Check [Tôi đồng ý với điều khoản] |
| **USER - QUẢN LÝ ĐƠN HÀNG** |
| 25 | Function - Xem thông tin đơn hàng (User) | Quản lý đơn hàng User | Check GUI and FUNC view order information function (User) | Tại Menu Ứng dụng phía User: 1. Click [Lịch sử đơn hàng] hoặc truy cập `/user/account/orders` |
| 26 | Function - Xem chi tiết đơn hàng (User) | Quản lý đơn hàng User | Check GUI and FUNC view order details function (User) | Tại Trang lịch sử đơn hàng: 1. Click [Xem chi tiết] hoặc truy cập `/user/account/orders/[id]` |
| 27 | Function - Theo dõi đơn hàng (User) | Quản lý đơn hàng User | Check GUI and FUNC track order function (User) | Tại Menu Ứng dụng phía User: 1. Click [Theo dõi đơn hàng] hoặc truy cập `/user/orders/track/[id]` |
| 28 | Function - Lọc đơn hàng theo trạng thái (User) | Quản lý đơn hàng User | Check GUI and FUNC filter orders by status function (User) | Tại Trang lịch sử đơn hàng: 1. Chọn trạng thái từ dropdown (Đang xử lý, Đang giao, Đã giao, Đã hủy) |
| 29 | Function - Hủy đơn hàng (User) | Quản lý đơn hàng User | Check GUI and FUNC cancel order function (User) | Tại Trang chi tiết đơn hàng: 1. Click [Hủy đơn hàng] (chỉ áp dụng cho đơn đang xử lý) |
| 30 | Function - Đánh giá đơn hàng (User) | Quản lý đơn hàng User | Check GUI and FUNC rate order function (User) | Tại Trang chi tiết đơn hàng đã giao: 1. Click [Đánh giá] |
| 31 | Function - Đặt lại đơn hàng (User) | Quản lý đơn hàng User | Check GUI and FUNC reorder function (User) | Tại Trang chi tiết đơn hàng hoặc danh sách: 1. Click [Đặt lại] |
| 32 | Function - Yêu cầu đổi/trả hàng (User) | Quản lý đơn hàng User | Check GUI and FUNC request return/exchange function (User) | Tại Trang chi tiết đơn hàng đã giao: 1. Click [Yêu cầu đổi/trả hàng] |
| 32.1 | Function - Xem timeline vận chuyển (User) | Quản lý đơn hàng User | Check GUI and FUNC view shipping timeline function (User) | Tại Trang theo dõi đơn hàng: 1. Xem timeline các mốc cập nhật |
| 32.2 | Function - Xem thông tin thanh toán (User) | Quản lý đơn hàng User | Check GUI and FUNC view payment information function (User) | Tại Trang chi tiết đơn hàng: 1. Xem phần thông tin thanh toán |
| **USER - ĐÁNH GIÁ SẢN PHẨM** |
| 33 | Function - Để lại đánh giá sản phẩm (User) | Đánh giá sản phẩm User | Check GUI and FUNC leave product review function (User) | Tại Trang chi tiết sản phẩm hoặc trang đánh giá: 1. Click [Viết đánh giá] hoặc truy cập `/user/reviews` |
| 34 | Function - Xem đánh giá sản phẩm (User) | Đánh giá sản phẩm User | Check GUI and FUNC view product reviews function (User) | Tại Trang chi tiết sản phẩm: 1. Scroll xuống phần đánh giá |
| 35 | Function - Chỉnh sửa đánh giá (User) | Đánh giá sản phẩm User | Check GUI and FUNC edit review function (User) | Tại Trang đánh giá của tôi: 1. Click [Chỉnh sửa] bên cạnh đánh giá |
| 36 | Function - Xóa đánh giá (User) | Đánh giá sản phẩm User | Check GUI and FUNC delete review function (User) | Tại Trang đánh giá của tôi: 1. Click [Xóa] bên cạnh đánh giá |
| 37 | Function - Đánh giá hữu ích (User) | Đánh giá sản phẩm User | Check GUI and FUNC mark review helpful function (User) | Tại Trang đánh giá sản phẩm: 1. Click [Hữu ích] hoặc [Không hữu ích] |
| 38 | Function - Báo cáo đánh giá (User) | Đánh giá sản phẩm User | Check GUI and FUNC report review function (User) | Tại Trang đánh giá sản phẩm: 1. Click [Báo cáo] bên cạnh đánh giá |
| 38.1 | Function - Lọc đánh giá theo điểm (User) | Đánh giá sản phẩm User | Check GUI and FUNC filter reviews by rating function (User) | Tại Trang đánh giá: 1. Chọn điểm từ dropdown (1-5 sao) |
| 38.2 | Function - Sắp xếp đánh giá (User) | Đánh giá sản phẩm User | Check GUI and FUNC sort reviews function (User) | Tại Trang đánh giá: 1. Chọn tiêu chí sắp xếp (Mới nhất, Hữu ích nhất, Điểm cao nhất) |
| 38.3 | Function - Xem đánh giá chờ xử lý (User) | Đánh giá sản phẩm User | Check GUI and FUNC view pending reviews function (User) | Tại Trang đánh giá: 1. Click tab [Chờ đánh giá] |
| **USER - YÊU CẦU HỖ TRỢ** |
| 39 | Function - Gửi yêu cầu hỗ trợ (User) | Hỗ trợ - liên hệ User | Check GUI and FUNC send support request function (User) | Tại Menu ứng dụng phía User: 1. Click [Hỗ trợ] 2. Click [Tạo yêu cầu mới] hoặc truy cập `/user/support` |
| 40 | Function - Chat hỗ trợ (User) | Hỗ trợ - liên hệ User | Check GUI and FUNC chat support function (User) | Tại Trang hỗ trợ: 1. Click tab [Chat trực tiếp] |
| 41 | Function - Quản lý yêu cầu hỗ trợ (User) | Hỗ trợ - liên hệ User | Check GUI and FUNC manage support requests function (User) | Tại Trang hỗ trợ: 1. Click tab [Yêu cầu hỗ trợ] - Xem danh sách, lọc, tìm kiếm |
| 42 | Function - Câu hỏi thường gặp (User) | Hỗ trợ - liên hệ User | Check GUI and FUNC FAQ function (User) | Tại Trang hỗ trợ: 1. Click tab [Câu hỏi thường gặp] |
| 43 | Function - Thông tin liên hệ (User) | Hỗ trợ - liên hệ User | Check GUI and FUNC contact information function (User) | Tại Trang hỗ trợ: 1. Xem thông tin liên hệ (Hotline, Email, Địa chỉ) |
| 44 | Function - Lọc yêu cầu hỗ trợ (User) | Hỗ trợ - liên hệ User | Check GUI and FUNC filter support requests function (User) | Tại Trang yêu cầu hỗ trợ: 1. Chọn trạng thái và danh mục từ dropdown |
| 45 | Function - Xem chi tiết yêu cầu hỗ trợ (User) | Hỗ trợ - liên hệ User | Check GUI and FUNC view support request details function (User) | Tại Trang yêu cầu hỗ trợ: 1. Click vào yêu cầu để xem chi tiết |
| 45.1 | Function - Export lịch sử chat (User) | Hỗ trợ - liên hệ User | Check GUI and FUNC export chat history function (User) | Tại Trang chat hỗ trợ: 1. Click [Export lịch sử] |
| 45.2 | Function - Tìm kiếm trong chat (User) | Hỗ trợ - liên hệ User | Check GUI and FUNC search in chat function (User) | Tại Trang chat hỗ trợ: 1. Sử dụng ô tìm kiếm trong chat |
| **USER - KHUYẾN MÃI** |
| 46 | Function - Xem danh sách khuyến mãi (User) | Khuyến mãi User | Check GUI and FUNC view promotions list function (User) | Tại Menu ứng dụng: 1. Click [Khuyến mãi] hoặc truy cập `/user/promotions` |
| 47 | Function - Xem chi tiết khuyến mãi (User) | Khuyến mãi User | Check GUI and FUNC view promotion details function (User) | Tại Trang khuyến mãi: 1. Click vào khuyến mãi hoặc truy cập `/user/promotions/[code]` |
| 48 | Function - Áp dụng mã giảm giá (User) | Khuyến mãi User | Check GUI and FUNC apply discount code function (User) | Tại Trang giỏ hàng hoặc thanh toán: 1. Nhập mã giảm giá 2. Click [Áp dụng] |
| 48.1 | Function - Xem mã giảm giá khả dụng (User) | Khuyến mãi User | Check GUI and FUNC view available discount codes function (User) | Tại Trang giỏ hàng: 1. Xem danh sách mã giảm giá có sẵn |
| 48.2 | Function - Áp dụng mã giảm giá sản phẩm (User) | Khuyến mãi User | Check GUI and FUNC apply product discount code function (User) | Tại Trang chi tiết sản phẩm: 1. Click [Áp dụng mã] cho mã giảm giá riêng sản phẩm |
| **USER - SẢN PHẨM YÊU THÍCH** |
| 49 | Function - Xem danh sách yêu thích (User) | Danh sách yêu thích User | Check GUI and FUNC view wishlist function (User) | Tại Menu Ứng dụng phía User: 1. Click [Yêu thích] hoặc truy cập `/user/wishlist` |
| 50 | Function - Thêm vào yêu thích (User) | Danh sách yêu thích User | Check GUI and FUNC add to wishlist function (User) | Tại Trang chi tiết sản phẩm hoặc danh sách: 1. Click [Thêm vào yêu thích] |
| 51 | Function - Xóa khỏi yêu thích (User) | Danh sách yêu thích User | Check GUI and FUNC remove from wishlist function (User) | Tại Trang yêu thích: 1. Click [Xóa] hoặc icon trái tim |
| 52 | Function - Tìm kiếm trong yêu thích (User) | Danh sách yêu thích User | Check GUI and FUNC search in wishlist function (User) | Tại Trang yêu thích: 1. Nhập từ khóa vào ô tìm kiếm |
| 53 | Function - Lọc yêu thích theo danh mục (User) | Danh sách yêu thích User | Check GUI and FUNC filter wishlist by category function (User) | Tại Trang yêu thích: 1. Chọn danh mục từ dropdown |
| 54 | Function - Sắp xếp yêu thích (User) | Danh sách yêu thích User | Check GUI and FUNC sort wishlist function (User) | Tại Trang yêu thích: 1. Chọn tiêu chí sắp xếp (Ngày thêm, Giá, Tên, Đánh giá) |
| 55 | Function - Thêm tất cả vào giỏ hàng (User) | Danh sách yêu thích User | Check GUI and FUNC add all to cart function (User) | Tại Trang yêu thích: 1. Click [Thêm tất cả vào giỏ] |
| 56 | Function - Chia sẻ sản phẩm yêu thích (User) | Danh sách yêu thích User | Check GUI and FUNC share wishlist item function (User) | Tại Trang yêu thích: 1. Click [Chia sẻ] bên cạnh sản phẩm |
| 57 | Function - So sánh sản phẩm (User) | Danh sách yêu thích User | Check GUI and FUNC compare products function (User) | Tại Trang yêu thích: 1. Click [So sánh] bên cạnh sản phẩm |
| 58 | Function - Đăng ký thông báo giá (User) | Danh sách yêu thích User | Check GUI and FUNC price alert function (User) | Tại Trang yêu thích: 1. Click [Thông báo giá] bên cạnh sản phẩm |
| 59 | Function - Xóa tất cả yêu thích (User) | Danh sách yêu thích User | Check GUI and FUNC clear all wishlist function (User) | Tại Trang yêu thích: 1. Click [Xóa tất cả] |
| **USER - ĐẶT TRƯỚC SẢN PHẨM** |
| 60 | Function - Đặt trước sản phẩm (User) | Đặt trước sản phẩm User | Check GUI and FUNC pre-order product function (User) | Tại Menu Ứng dụng phía User: 1. Click [Đặt trước mô hình] hoặc truy cập `/user/borrow` |
| 61 | Function - Xem danh sách đặt trước (User) | Đặt trước sản phẩm User | Check GUI and FUNC view pre-orders list function (User) | Tại Trang đặt trước: 1. Xem danh sách các sản phẩm đã đặt trước |
| 62 | Function - Hủy đặt trước (User) | Đặt trước sản phẩm User | Check GUI and FUNC cancel pre-order function (User) | Tại Trang đặt trước: 1. Click [Hủy đặt trước] bên cạnh sản phẩm |
| 63 | Function - Xem chi tiết đặt trước (User) | Đặt trước sản phẩm User | Check GUI and FUNC view pre-order details function (User) | Tại Trang danh sách đặt trước: 1. Click [Xem chi tiết] |
| 64 | Function - Quản lý trạng thái đặt trước (User) | Đặt trước sản phẩm User | Check GUI and FUNC manage pre-order status function (User) | Tại Trang danh sách đặt trước: 1. Sử dụng tab trạng thái để lọc và theo dõi |
| 64.1 | Function - Nhận thông báo có hàng (User) | Đặt trước sản phẩm User | Check GUI and FUNC receive stock notification function (User) | Tại Trang đặt trước: 1. Hệ thống tự động gửi thông báo khi có hàng |
| **USER - YÊU CẦU ĐẶT HÀNG** |
| 65 | Function - Gửi yêu cầu đặt hàng (User) | Yêu cầu đặt hàng User | Check GUI and FUNC send special request function (User) | Tại Menu Ứng dụng phía User: 1. Click [Yêu cầu nhập hàng] hoặc truy cập `/user/requests` |
| 66 | Function - Xem chi tiết yêu cầu (User) | Yêu cầu đặt hàng User | Check GUI and FUNC view request details function (User) | Tại Trang yêu cầu đặt hàng: 1. Click [Xem] hoặc truy cập `/user/requests/[id]` |
| 66.1 | Function - Lọc yêu cầu theo trạng thái (User) | Yêu cầu đặt hàng User | Check GUI and FUNC filter requests by status function (User) | Tại Trang yêu cầu đặt hàng: 1. Chọn trạng thái từ dropdown |
| 66.2 | Function - Hủy yêu cầu đặt hàng (User) | Yêu cầu đặt hàng User | Check GUI and FUNC cancel request function (User) | Tại Trang chi tiết yêu cầu: 1. Click [Hủy yêu cầu] (nếu chưa được xử lý) |
| **USER - VẬN CHUYỂN** |
| 67 | Layout - Chọn phương thức vận chuyển (User) | Vận chuyển User | GUI function for shipping method selection | Tại Trang thanh toán hoặc giỏ hàng: 1. Chọn phương thức vận chuyển |
| 67.1 | Function - Chọn đơn vị vận chuyển (User) | Vận chuyển User | Check GUI and FUNC select shipping carrier function (User) | Tại Trang thanh toán: 1. Chọn đơn vị vận chuyển (GHTK, GHN, J&T) |
| 67.2 | Function - Tính phí vận chuyển (User) | Vận chuyển User | Check GUI and FUNC calculate shipping fee function (User) | Tại Trang thanh toán: 1. Nhập địa chỉ - Hệ thống tự động tính phí |
| 67.3 | Function - Xem thông tin vận chuyển (User) | Vận chuyển User | Check GUI and FUNC view shipping information function (User) | Tại Trang chi tiết sản phẩm: 1. Click tab [Vận chuyển] |
| 67.4 | Function - Nhập thông tin giao hàng (User) | Vận chuyển User | Check GUI and FUNC enter shipping information function (User) | Tại Trang thanh toán: 1. Điền đầy đủ thông tin (Tên, SĐT, Địa chỉ, Ghi chú) |
| **USER - THÔNG BÁO** |
| 68 | Function - Xem thông báo (User) | Thông báo User | Check GUI and FUNC view notifications function (User) | Tại Menu Ứng dụng phía User: 1. Click [Thông báo] hoặc truy cập `/user/notifications` |
| 69 | Function - Đánh dấu đã đọc (User) | Thông báo User | Check GUI and FUNC mark as read function (User) | Tại Trang thông báo: 1. Click [Đánh dấu đã đọc] bên cạnh thông báo |
| 70 | Function - Đánh dấu tất cả đã đọc (User) | Thông báo User | Check GUI and FUNC mark all as read function (User) | Tại Trang thông báo: 1. Click [Đánh dấu tất cả đã đọc] |
| 71 | Function - Xóa thông báo (User) | Thông báo User | Check GUI and FUNC delete notification function (User) | Tại Trang thông báo: 1. Click [Xóa] bên cạnh thông báo |
| 72 | Function - Xóa tất cả thông báo đã đọc (User) | Thông báo User | Check GUI and FUNC clear all read notifications function (User) | Tại Trang thông báo: 1. Click [Xóa đã đọc] |
| 73 | Function - Lọc thông báo theo loại (User) | Thông báo User | Check GUI and FUNC filter notifications by type function (User) | Tại Trang thông báo: 1. Chọn tab loại thông báo (Đơn hàng, Khuyến mãi, Yêu thích, Đánh giá, Hệ thống, Hỗ trợ) |
| 74 | Function - Lọc thông báo theo mức độ ưu tiên (User) | Thông báo User | Check GUI and FUNC filter notifications by priority function (User) | Tại Trang thông báo: 1. Chọn mức độ ưu tiên từ dropdown (Cao, Trung bình, Thấp) |
| 75 | Function - Tìm kiếm thông báo (User) | Thông báo User | Check GUI and FUNC search notifications function (User) | Tại Trang thông báo: 1. Nhập từ khóa vào ô tìm kiếm |
| 76 | Function - Xem chi tiết thông báo (User) | Thông báo User | Check GUI and FUNC view notification details function (User) | Tại Trang thông báo: 1. Click vào thông báo để xem chi tiết và thực hiện hành động |
| **USER - BÀI VIẾT** |
| 77 | Function - Tạo bài viết (User) | Tạo - hiển thị bài viết User | Check GUI and FUNC create post function (User) | Tại Menu Ứng dụng phía User: 1. Click [Tạo bài viết] hoặc truy cập `/user/posts/create` |
| 78 | Function - Hiển thị danh sách bài viết (User) | Tạo - hiển thị bài viết User | Check GUI and FUNC display posts list function (User) | Tại Menu Ứng dụng phía User: 1. Click [Bài viết] hoặc truy cập `/user/posts` |
| 79 | Function - Xem chi tiết bài viết (User) | Tạo - hiển thị bài viết User | Check GUI and FUNC view post details function (User) | Tại Trang danh sách bài viết: 1. Click vào bài viết hoặc truy cập `/user/posts/[id]` |
| 80 | Function - Chỉnh sửa bài viết (User) | Tạo - hiển thị bài viết User | Check GUI and FUNC edit post function (User) | Tại Trang chi tiết bài viết của mình: 1. Click [Chỉnh sửa] hoặc truy cập `/user/posts/[id]/edit` |
| 81 | Function - Xóa bài viết (User) | Tạo - hiển thị bài viết User | Check GUI and FUNC delete post function (User) | Tại Trang chi tiết bài viết của mình: 1. Click [Xóa bài viết] |
| 82 | Function - Tìm kiếm bài viết (User) | Tạo - hiển thị bài viết User | Check GUI and FUNC search posts function (User) | Tại Trang danh sách bài viết: 1. Nhập từ khóa vào ô tìm kiếm |
| 83 | Function - Lọc bài viết theo danh mục (User) | Tạo - hiển thị bài viết User | Check GUI and FUNC filter posts by category function (User) | Tại Trang danh sách bài viết: 1. Chọn danh mục từ dropdown (Gundam, Figure, Mô hình xe, Máy bay) |
| 84 | Function - Lọc bài viết theo thời gian (User) | Tạo - hiển thị bài viết User | Check GUI and FUNC filter posts by time function (User) | Tại Trang danh sách bài viết: 1. Chọn khoảng thời gian (Hôm nay, Tuần này, Tháng này) |
| 85 | Function - Sắp xếp bài viết (User) | Tạo - hiển thị bài viết User | Check GUI and FUNC sort posts function (User) | Tại Trang danh sách bài viết: 1. Chọn tiêu chí sắp xếp (Mới nhất, Nhiều like nhất, Nhiều bình luận nhất) |
| 86 | Function - Phân trang bài viết (User) | Tạo - hiển thị bài viết User | Check GUI and FUNC paginate posts function (User) | Tại Trang danh sách bài viết: 1. Sử dụng nút phân trang để xem thêm |
| **USER - TƯƠNG TÁC BÀI VIẾT** |
| 87 | Function - Like bài viết (User) | Tương tác bài viết User | Check GUI and FUNC like post function (User) | Tại Trang chi tiết bài viết: 1. Click [Like] hoặc icon trái tim |
| 88 | Function - Bình luận bài viết (User) | Tương tác bài viết User | Check GUI and FUNC comment post function (User) | Tại Trang chi tiết bài viết: 1. Nhập bình luận 2. Click [Gửi] |
| 89 | Function - Chia sẻ bài viết (User) | Tương tác bài viết User | Check GUI and FUNC share post function (User) | Tại Trang chi tiết bài viết: 1. Click [Chia sẻ] |
| 90 | Function - Xóa bình luận (User) | Tương tác bài viết User | Check GUI and FUNC delete comment function (User) | Tại Trang chi tiết bài viết: 1. Click [Xóa] bên cạnh bình luận của mình |
| 91 | Function - Chỉnh sửa bình luận (User) | Tương tác bài viết User | Check GUI and FUNC edit comment function (User) | Tại Trang chi tiết bài viết: 1. Click [Chỉnh sửa] bên cạnh bình luận của mình |
| 91.1 | Function - Like bình luận (User) | Tương tác bài viết User | Check GUI and FUNC like comment function (User) | Tại Trang chi tiết bài viết: 1. Click [Like] bên cạnh bình luận |
| 91.2 | Function - Phản hồi bình luận (User) | Tương tác bài viết User | Check GUI and FUNC reply to comment function (User) | Tại Trang chi tiết bài viết: 1. Click [Phản hồi] bên cạnh bình luận |
| **USER - XEM TRANG CÁ NHÂN** |
| 92 | Function - Xem trang cá nhân người lạ (User) | Xem trang cá nhân User | Check GUI and FUNC view stranger profile function (User) | Tại Trang bài viết hoặc bình luận: 1. Click vào tên người dùng hoặc truy cập `/user/profile/[id]` |
| 92.1 | Function - Xem bài viết của người khác (User) | Xem trang cá nhân User | Check GUI and FUNC view other user posts function (User) | Tại Trang cá nhân người khác: 1. Xem danh sách bài viết của họ |
| 92.2 | Function - Theo dõi người dùng (User) | Xem trang cá nhân User | Check GUI and FUNC follow user function (User) | Tại Trang cá nhân người khác: 1. Click [Theo dõi] |
| 92.3 | Function - Bỏ theo dõi người dùng (User) | Xem trang cá nhân User | Check GUI and FUNC unfollow user function (User) | Tại Trang cá nhân người đang theo dõi: 1. Click [Bỏ theo dõi] |
| **USER - BẢO MẬT** |
| 93 | Function - Xem lịch sử đăng nhập (User) | Bảo mật User | Check GUI and FUNC login history function (User) | Tại Menu Ứng dụng phía User: 1. Click [Tài khoản] 2. Click [Lịch sử đăng nhập] hoặc truy cập `/user/account/logins` |
| 94 | Function - Quản lý phiên đăng nhập (User) | Bảo mật User | Check GUI and FUNC sessions management function (User) | Tại Menu Ứng dụng phía User: 1. Click [Tài khoản] 2. Click [Phiên đăng nhập] hoặc truy cập `/user/account/sessions` |
| 95 | Function - Đăng xuất khỏi thiết bị khác (User) | Bảo mật User | Check GUI and FUNC logout from other device function (User) | Tại Trang quản lý phiên đăng nhập: 1. Click [Đăng xuất] bên cạnh thiết bị |
| 96 | Function - Phát hiện đăng nhập lạ (User) | Bảo mật User | Check GUI and FUNC detect suspicious login function (User) | Tại Trang lịch sử đăng nhập: 1. Hệ thống tự động phát hiện và cảnh báo đăng nhập từ thiết bị/IP lạ |
| 97 | Function - Auto logout khi hết hạn (User) | Bảo mật User | Check GUI and FUNC auto logout on timeout function (User) | Tại Trang quản lý phiên đăng nhập: 1. Hệ thống tự động đăng xuất khi session hết hạn |
| 97.1 | Function - Xác thực hai yếu tố (User) | Bảo mật User | Check GUI and FUNC two-factor authentication function (User) | Tại Trang cài đặt bảo mật: 1. Bật/tắt xác thực hai yếu tố |
| **USER - CÀI ĐẶT** |
| 98 | Function - Cài đặt tài khoản (User) | Cài đặt User | Check GUI and FUNC account settings function (User) | Tại Menu Ứng dụng phía User: 1. Click [Cài đặt] hoặc truy cập `/user/settings` |
| 98.1 | Function - Cài đặt thông báo (User) | Cài đặt User | Check GUI and FUNC notification settings function (User) | Tại Trang cài đặt: 1. Cấu hình các loại thông báo muốn nhận |
| 98.2 | Function - Cài đặt ngôn ngữ (User) | Cài đặt User | Check GUI and FUNC language settings function (User) | Tại Trang cài đặt: 1. Chọn ngôn ngữ hiển thị |
| 98.3 | Function - Cài đặt giao diện (User) | Cài đặt User | Check GUI and FUNC theme settings function (User) | Tại Trang cài đặt: 1. Chọn chế độ sáng/tối |
| **USER - TRANG CHỦ** |
| 99 | Layout - Trang chủ (User) | Trang chủ User | GUI function for User homepage | Tại Menu Ứng dụng phía User: 1. Click [Trang chủ] hoặc truy cập `/user` |
| 99.1 | Function - Xem sản phẩm nổi bật (User) | Trang chủ User | Check GUI and FUNC view featured products function (User) | Tại Trang chủ: 1. Xem phần sản phẩm nổi bật |
| 99.2 | Function - Xem danh mục sản phẩm (User) | Trang chủ User | Check GUI and FUNC view product categories function (User) | Tại Trang chủ: 1. Xem phần danh mục mô hình |
| 99.3 | Function - Tìm kiếm nhanh (User) | Trang chủ User | Check GUI and FUNC quick search function (User) | Tại Trang chủ: 1. Sử dụng thanh tìm kiếm ở header |
| 99.4 | Function - Xem thống kê nhanh (User) | Trang chủ User | Check GUI and FUNC view quick stats function (User) | Tại Trang chủ: 1. Xem các thống kê nhanh (Giỏ hàng, Yêu thích, Thông báo) |

---

## GHI CHÚ QUAN TRỌNG

### Về Routes:
- Tất cả routes được xác định dựa trên cấu trúc thư mục `src/app/user/`
- Routes có thể truy cập trực tiếp qua URL hoặc thông qua menu navigation
- Routes động (có `[id]`) cần thay thế `[id]` bằng ID thực tế khi test
- Ví dụ: `/user/products/1` thay vì `/user/products/[id]`

### Về Pre-Condition:
- Pre-Condition mô tả các bước điều hướng từ menu hoặc URL trực tiếp
- Có thể kết hợp cả hai cách: click menu hoặc truy cập URL trực tiếp
- Một số chức năng yêu cầu đăng nhập trước khi truy cập (ví dụ: Quản lý tài khoản, Giỏ hàng, Đơn hàng)
- Một số chức năng có thể truy cập mà không cần đăng nhập (ví dụ: Xem sản phẩm, Tìm kiếm)

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
  - Tài khoản hợp lệ và không hợp lệ
  - Sản phẩm có hàng và hết hàng
  - Đơn hàng ở các trạng thái khác nhau
  - Mã giảm giá hợp lệ và không hợp lệ
  - Địa chỉ giao hàng hợp lệ và không hợp lệ

### Về Test Environment:
- **Development Environment**: `http://localhost:3000`
- **Staging Environment**: `https://staging.modelshop.com`
- **Production Environment**: `https://modelshop.com`
- Cần test trên các trình duyệt: Chrome, Firefox, Safari, Edge
- Cần test trên các thiết bị: Desktop, Tablet, Mobile

### Về Priority:
- **P0 - Critical**: Các chức năng cốt lõi (Đăng nhập, Đăng ký, Thanh toán, Đặt hàng)
- **P1 - High**: Các chức năng quan trọng (Quản lý đơn hàng, Giỏ hàng, Sản phẩm)
- **P2 - Medium**: Các chức năng hỗ trợ (Yêu thích, Đánh giá, Bài viết)
- **P3 - Low**: Các chức năng bổ sung (Cài đặt, Thông báo, Hỗ trợ)

---

## THỐNG KÊ TEST CASE

**Tổng số chức năng User:** 99 functions

**Phân loại theo nhóm:**
- **Quản lý tài khoản:** 13 functions (1-5.7)
- **Hiển thị sản phẩm:** 4 functions (6-7.3)
- **Tìm kiếm sản phẩm:** 4 functions (8-8.3)
- **Bộ lọc và phân loại:** 6 functions (9-9.5)
- **Quản lý giỏ hàng:** 10 functions (10-19.2)
- **Thanh toán đơn hàng:** 5 functions (20-24.3)
- **Quản lý đơn hàng:** 8 functions (25-32.2)
- **Đánh giá sản phẩm:** 6 functions (33-38.3)
- **Yêu cầu hỗ trợ:** 7 functions (39-45.2)
- **Khuyến mãi:** 3 functions (46-48.2)
- **Sản phẩm yêu thích:** 11 functions (49-59)
- **Đặt trước sản phẩm:** 5 functions (60-64.1)
- **Yêu cầu đặt hàng:** 3 functions (65-66.2)
- **Vận chuyển:** 5 functions (67-67.4)
- **Thông báo:** 9 functions (68-76)
- **Bài viết:** 10 functions (77-86)
- **Tương tác bài viết:** 5 functions (87-91.2)
- **Xem trang cá nhân:** 4 functions (92-92.3)
- **Bảo mật:** 5 functions (93-97.1)
- **Cài đặt:** 4 functions (98-98.3)
- **Trang chủ:** 5 functions (99-99.4)

---

**Người tạo:** Testing Team  
**Ngày cập nhật:** 2025-01-20  
**Phiên bản:** 1.0

