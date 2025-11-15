# BLACKBOX TEST CASE - USER FUNCTIONS

**Dự án:** Hệ Thống Quản Lý Model Shop  
**Ngày tạo:** 2025  
**Mục đích:** Tài liệu tổng quan về các chức năng User và routes để thực hiện blackbox testing

---

## BẢNG TỔNG HỢP TEST CASE

| No | Function Name | Sheet Name | Description | Pre-Condition (Route) |
|----|---------------|------------|-------------|----------------------|
| **1. QUẢN LÝ TÀI KHOẢN** |
| 1 | Function - Đăng nhập (User) | Quản lý tài khoản | Check GUI and FUNC login function (User) | Tại Menu Ứng dụng phía User: 1. Click [Đăng nhập] hoặc truy cập `/user/auth/login` |
| 2 | Function - Đăng ký (User) | Quản lý tài khoản | Check GUI and FUNC register function (User) | Tại Menu Ứng dụng phía User: 1. Click [Đăng ký] hoặc truy cập `/user/auth/register` |
| 3 | Function - Đổi mật khẩu (User) | Quản lý tài khoản | Check GUI and FUNC change password function (User) | Tại Menu Ứng dụng phía User: 1. Click [Tài khoản] 2. Click [Đổi mật khẩu] hoặc truy cập `/user/account` |
| 4 | Function - Cập nhật thông tin cá nhân (User) | Quản lý tài khoản | Check GUI and FUNC update personal information function (User) | Tại Menu Ứng dụng phía User: 1. Click [Tài khoản] 2. Click [Cập nhật thông tin] hoặc truy cập `/user/account` |
| 5 | Layout - Quản lý thông tin cá nhân (User) | Quản lý tài khoản | GUI function for User personal information management | Tại Menu Ứng dụng phía User: 1. Click [Tài khoản] hoặc truy cập `/user/account` |
| 5.1 | Function - Khôi phục mật khẩu (User) | Quản lý tài khoản | Check GUI and FUNC forgot password function (User) | Tại Menu Ứng dụng phía User: 1. Click [Đăng nhập] 2. Click [Quên mật khẩu] hoặc truy cập `/user/auth/forgot-password` |
| 5.2 | Function - Quản lý địa chỉ (User) | Quản lý tài khoản | Check GUI and FUNC manage addresses function (User) | Tại Menu Ứng dụng phía User: 1. Click [Tài khoản] 2. Click [Địa chỉ] hoặc truy cập `/user/account/addresses` |
| 5.3 | Function - Xem hạng thành viên (User) | Quản lý tài khoản | Check GUI and FUNC view membership rank function (User) | Tại Menu Ứng dụng phía User: 1. Click [Tài khoản] 2. Click [Hạng thành viên] hoặc truy cập `/user/account/rank` |
| 5.4 | Function - Đăng xuất (User) | Quản lý tài khoản | Check GUI and FUNC logout function (User) | Tại Menu Ứng dụng phía User: 1. Click [Đăng xuất] hoặc truy cập `/user/logout` |
| 5.5 | Layout - Quản lý tài khoản (User) | [Layout Quản lý Tài khoản](1.%20Quản%20lý%20tài%20khoản.md) | GUI chức năng Quản lý tài khoản | Tại Menu Ứng dụng phía User: 1. Click [Tài khoản] hoặc truy cập `/user/account` |
| **2. CHỨC NĂNG HIỂN THỊ SẢN PHẨM** |
| 6 | Function - Hiển thị danh sách sản phẩm (User) | Hiển thị sản phẩm | Check GUI and FUNC display products list function (User) | Tại Menu Ứng dụng phía User: 1. Click [Mô hình] hoặc truy cập `/user/products` |
| 7 | Function - Xem chi tiết sản phẩm (User) | Hiển thị sản phẩm | Check GUI and FUNC view product details function (User) | Tại Menu Ứng dụng phía User: 1. Click [Mô hình] 2. Click vào sản phẩm hoặc truy cập `/user/products/[id]` |
| 7.1 | Function - Chuyển đổi chế độ xem (Grid/List) (User) | Hiển thị sản phẩm | Check GUI and FUNC toggle view mode function (User) | Tại Trang danh sách sản phẩm: 1. Click nút chuyển đổi Grid/List |
| 7.2 | Function - Xem hình ảnh sản phẩm (User) | Hiển thị sản phẩm | Check GUI and FUNC view product images function (User) | Tại Trang chi tiết sản phẩm: 1. Click vào hình ảnh để xem full size |
| 7.3 | Function - Xem thông số kỹ thuật sản phẩm (User) | Hiển thị sản phẩm | Check GUI and FUNC view product specifications function (User) | Tại Trang chi tiết sản phẩm: 1. Click tab [Thông số kỹ thuật] |
| 7.4 | Function - Xem mô tả sản phẩm (User) | Hiển thị sản phẩm | Check GUI and FUNC view product description function (User) | Tại Trang chi tiết sản phẩm: 1. Click tab [Mô tả] |
| 7.5 | Layout - Hiển thị sản phẩm (User) | [Layout Hiển thị Sản phẩm](2.%20Chức%20năng%20hiển%20thị%20sản%20phẩm.md) | GUI chức năng Hiển thị sản phẩm | Tại Menu Ứng dụng phía User: 1. Click [Mô hình] hoặc truy cập `/user/products` |
| **3. CHỨC NĂNG TÌM KIẾM SẢN PHẨM** |
| 8 | Function - Tìm kiếm sản phẩm (User) | Tìm kiếm sản phẩm | Check GUI and FUNC search products function (User) | Tại Menu Ứng dụng: 1. Click [Tìm kiếm] hoặc truy cập `/user/search` |
| 8.1 | Function - Gợi ý tìm kiếm (User) | Tìm kiếm sản phẩm | Check GUI and FUNC search suggestions function (User) | Tại Trang tìm kiếm: 1. Nhập từ khóa vào ô tìm kiếm - Hệ thống hiển thị gợi ý |
| 8.2 | Function - Lịch sử tìm kiếm (User) | Tìm kiếm sản phẩm | Check GUI and FUNC search history function (User) | Tại Trang tìm kiếm: 1. Xem lịch sử tìm kiếm gần đây |
| 8.3 | Function - Xóa lịch sử tìm kiếm (User) | Tìm kiếm sản phẩm | Check GUI and FUNC clear search history function (User) | Tại Trang tìm kiếm: 1. Click [Xóa lịch sử] |
| 8.4 | Function - Tìm kiếm nâng cao (User) | Tìm kiếm sản phẩm | Check GUI and FUNC advanced search function (User) | Tại Trang tìm kiếm: 1. Sử dụng các bộ lọc nâng cao |
| 8.5 | Layout - Tìm kiếm sản phẩm (User) | [Layout Tìm kiếm Sản phẩm](3.%20Chức%20năng%20tìm%20kiếm%20sản%20phẩm.md) | GUI chức năng Tìm kiếm sản phẩm | Tại Menu Ứng dụng: 1. Click [Tìm kiếm] hoặc truy cập `/user/search` |
| **4. CHỨC NĂNG BỘ LỌC SẢN PHẨM - PHÂN LOẠI SẢN PHẨM** |
| 9 | Layout - Bộ lọc sản phẩm (User) | Bộ lọc sản phẩm - phân loại sản phẩm | GUI function for product filtering and categorization | Tại Menu Ứng dụng phía User: 1. Click [Mô hình] hoặc truy cập `/user/products` |
| 9.1 | Function - Lọc theo danh mục (User) | Bộ lọc sản phẩm - phân loại sản phẩm | Check GUI and FUNC filter by category function (User) | Tại Trang danh sách sản phẩm: 1. Chọn danh mục từ dropdown |
| 9.2 | Function - Lọc theo thương hiệu (User) | Bộ lọc sản phẩm - phân loại sản phẩm | Check GUI and FUNC filter by brand function (User) | Tại Trang danh sách sản phẩm: 1. Chọn thương hiệu từ dropdown |
| 9.3 | Function - Lọc theo khoảng giá (User) | Bộ lọc sản phẩm - phân loại sản phẩm | Check GUI and FUNC filter by price range function (User) | Tại Trang danh sách sản phẩm: 1. Điều chỉnh slider khoảng giá |
| 9.4 | Function - Lọc theo tỷ lệ (Scale) (User) | Bộ lọc sản phẩm - phân loại sản phẩm | Check GUI and FUNC filter by scale function (User) | Tại Trang danh sách sản phẩm: 1. Chọn tỷ lệ từ dropdown (1/144, 1/100, 1/72, etc.) |
| 9.5 | Function - Lọc theo đánh giá (User) | Bộ lọc sản phẩm - phân loại sản phẩm | Check GUI and FUNC filter by rating function (User) | Tại Trang danh sách sản phẩm: 1. Chọn mức đánh giá từ dropdown |
| 9.6 | Function - Sắp xếp sản phẩm (User) | Bộ lọc sản phẩm - phân loại sản phẩm | Check GUI and FUNC sort products function (User) | Tại Trang danh sách sản phẩm: 1. Chọn tiêu chí sắp xếp (giá, đánh giá, mới nhất) |
| 9.7 | Function - Xóa bộ lọc (User) | Bộ lọc sản phẩm - phân loại sản phẩm | Check GUI and FUNC clear filters function (User) | Tại Trang danh sách sản phẩm: 1. Click [Xóa bộ lọc] |
| 9.8 | Layout - Bộ lọc sản phẩm - phân loại sản phẩm (User) | [Layout Bộ lọc Sản phẩm](4.%20Chức%20năng%20bộ%20lọc%20sản%20phẩm%20-%20phân%20loại%20sản%20phẩm.md) | GUI chức năng Bộ lọc sản phẩm - phân loại sản phẩm | Tại Menu Ứng dụng phía User: 1. Click [Mô hình] hoặc truy cập `/user/products` |
| **5. CHỨC NĂNG QUẢN LÝ GIỎ HÀNG** |
| 10 | Function - Thêm sản phẩm vào giỏ hàng (User) | Quản lý giỏ hàng | Check GUI and FUNC add product to cart function (User) | Tại Danh sách sản phẩm hoặc trang chi tiết: 1. Click [Thêm vào giỏ hàng] |
| 11 | Function - Hiển thị giỏ hàng (User) | Quản lý giỏ hàng | Check GUI and FUNC view cart function (User) | Tại Menu chính: 1. Click [Giỏ hàng] hoặc truy cập `/user/cart` |
| 12 | Function - Xóa sản phẩm khỏi giỏ hàng (User) | Quản lý giỏ hàng | Check GUI and FUNC delete product from cart function (User) | Tại Trang giỏ hàng: 1. Click [Xóa] bên cạnh sản phẩm |
| 13 | Function - Cập nhật số lượng sản phẩm (User) | Quản lý giỏ hàng | Check GUI and FUNC update product quantity function (User) | Tại Trang giỏ hàng: 1. Thay đổi số lượng bằng nút +/- hoặc nhập trực tiếp |
| 14 | Function - Chọn/Bỏ chọn sản phẩm (User) | Quản lý giỏ hàng | Check GUI and FUNC select/deselect product function (User) | Tại Trang giỏ hàng: 1. Click checkbox để chọn/bỏ chọn sản phẩm |
| 15 | Function - Chọn tất cả sản phẩm (User) | Quản lý giỏ hàng | Check GUI and FUNC select all products function (User) | Tại Trang giỏ hàng: 1. Click [Chọn tất cả] |
| 16 | Function - Áp dụng mã giảm giá (User) | Quản lý giỏ hàng | Check GUI and FUNC apply discount code function (User) | Tại Trang giỏ hàng: 1. Nhập mã giảm giá 2. Click [Áp dụng] |
| 17 | Function - Xóa mã giảm giá (User) | Quản lý giỏ hàng | Check GUI and FUNC remove discount code function (User) | Tại Trang giỏ hàng: 1. Click [Xóa mã] sau khi đã áp dụng |
| 18 | Function - Thêm vào yêu thích từ giỏ hàng (User) | Quản lý giỏ hàng | Check GUI and FUNC add to wishlist from cart function (User) | Tại Trang giỏ hàng: 1. Click [Thêm yêu thích] bên cạnh sản phẩm |
| 19 | Function - Thực hiện thanh toán (User) | Quản lý giỏ hàng | Check GUI and FUNC proceed to checkout function (User) | Tại Trang giỏ hàng: 1. Click [Thanh toán] hoặc truy cập `/user/checkout` |
| 19.1 | Layout - Quản lý giỏ hàng (User) | [Layout Quản lý Giỏ hàng](5.%20Chức%20năng%20quản%20lý%20giỏ%20hàng.md) | GUI chức năng Quản lý giỏ hàng | Tại Menu chính: 1. Click [Giỏ hàng] hoặc truy cập `/user/cart` |
| **6. CHỨC NĂNG QUẢN LÝ ĐƠN HÀNG** |
| 20 | Function - Xem thông tin đơn hàng (User) | Quản lý đơn hàng | Check GUI and FUNC view order information function (User) | Tại Menu Ứng dụng phía User: 1. Click [Lịch sử đơn hàng] hoặc truy cập `/user/account/orders` |
| 21 | Function - Xem chi tiết đơn hàng (User) | Quản lý đơn hàng | Check GUI and FUNC view order details function (User) | Tại Trang lịch sử đơn hàng: 1. Click [Xem chi tiết] hoặc truy cập `/user/account/orders/[id]` |
| 22 | Function - Theo dõi đơn hàng (User) | Quản lý đơn hàng | Check GUI and FUNC track order function (User) | Tại Menu Ứng dụng phía User: 1. Click [Theo dõi đơn hàng] hoặc truy cập `/user/orders/track/[id]` |
| 23 | Function - Lọc đơn hàng theo trạng thái (User) | Quản lý đơn hàng | Check GUI and FUNC filter orders by status function (User) | Tại Trang lịch sử đơn hàng: 1. Chọn trạng thái từ dropdown (Đang xử lý, Đang giao, Đã giao, Đã hủy) |
| 24 | Function - Hủy đơn hàng (User) | Quản lý đơn hàng | Check GUI and FUNC cancel order function (User) | Tại Trang chi tiết đơn hàng: 1. Click [Hủy đơn hàng] (chỉ áp dụng cho đơn đang xử lý) |
| 25 | Function - Đánh giá đơn hàng (User) | Quản lý đơn hàng | Check GUI and FUNC rate order function (User) | Tại Trang chi tiết đơn hàng đã giao: 1. Click [Đánh giá] |
| 26 | Function - Đặt lại đơn hàng (User) | Quản lý đơn hàng | Check GUI and FUNC reorder function (User) | Tại Trang chi tiết đơn hàng hoặc danh sách: 1. Click [Đặt lại] |
| 27 | Function - Yêu cầu đổi/trả hàng (User) | Quản lý đơn hàng | Check GUI and FUNC request return/exchange function (User) | Tại Trang chi tiết đơn hàng đã giao: 1. Click [Yêu cầu đổi/trả hàng] |
| 27.1 | Function - Xem timeline vận chuyển (User) | Quản lý đơn hàng | Check GUI and FUNC view shipping timeline function (User) | Tại Trang theo dõi đơn hàng: 1. Xem timeline các mốc cập nhật |
| 27.2 | Function - Xem thông tin thanh toán (User) | Quản lý đơn hàng | Check GUI and FUNC view payment information function (User) | Tại Trang chi tiết đơn hàng: 1. Xem phần thông tin thanh toán |
| 27.3 | Layout - Quản lý đơn hàng (User) | [Layout Quản lý Đơn hàng](6.%20Chức%20năng%20quản%20lý%20đơn%20hàng.md) | GUI chức năng Quản lý đơn hàng | Tại Menu Ứng dụng phía User: 1. Click [Lịch sử đơn hàng] hoặc truy cập `/user/account/orders` |
| **7. CHỨC NĂNG THANH TOÁN ĐƠN HÀNG** |
| 28 | Function - Chọn phương thức thanh toán (User) | Thanh toán đơn hàng | Check GUI and FUNC select payment method function (User) | Tại Trang thanh toán: 1. Chọn phương thức thanh toán (COD, Banking, E-wallet) |
| 29 | Function - Thanh toán khi nhận hàng (User) | Thanh toán đơn hàng | Check GUI and FUNC cash on delivery payment function (User) | Tại Trang thanh toán: 1. Chọn [Thanh toán khi nhận hàng] 2. Click [Xác nhận đơn hàng] |
| 30 | Function - Thanh toán VNPAY (User) | Thanh toán đơn hàng | Check GUI and FUNC VNPAY payment function (User) | Tại Trang thanh toán: 1. Chọn [Thanh toán VNPAY] 2. Click [Xác nhận thanh toán] hoặc truy cập `/user/checkout/processing` |
| 31 | Function - Thanh toán ví điện tử (User) | Thanh toán đơn hàng | Check GUI and FUNC e-wallet payment function (User) | Tại Trang thanh toán: 1. Chọn [Ví điện tử] (MoMo, ZaloPay) 2. Click [Xác nhận] |
| 32 | Function - Xác nhận đơn hàng (User) | Thanh toán đơn hàng | Check GUI and FUNC confirm order function (User) | Tại Trang thanh toán: 1. Điền đầy đủ thông tin giao hàng 2. Click [Xác nhận đơn hàng] |
| 32.1 | Function - Sử dụng địa chỉ đã lưu (User) | Thanh toán đơn hàng | Check GUI and FUNC use saved address function (User) | Tại Trang thanh toán: 1. Check [Sử dụng địa chỉ đã lưu] |
| 32.2 | Function - Lưu địa chỉ làm mặc định (User) | Thanh toán đơn hàng | Check GUI and FUNC save address as default function (User) | Tại Trang thanh toán: 1. Check [Lưu địa chỉ này làm mặc định] |
| 32.3 | Function - Đồng ý điều khoản (User) | Thanh toán đơn hàng | Check GUI and FUNC accept terms function (User) | Tại Trang thanh toán: 1. Check [Tôi đồng ý với điều khoản] |
| 32.4 | Layout - Thanh toán đơn hàng (User) | [Layout Thanh toán Đơn hàng](7.%20Chức%20năng%20thanh%20toán%20đơn%20hàng.md) | GUI chức năng Thanh toán đơn hàng | Tại Trang giỏ hàng: 1. Click [Thanh toán] hoặc truy cập `/user/checkout` |
| **8. CHỨC NĂNG VẬN CHUYỂN** |
| 33 | Layout - Chọn phương thức vận chuyển (User) | Vận chuyển | GUI function for shipping method selection | Tại Trang thanh toán hoặc giỏ hàng: 1. Chọn phương thức vận chuyển |
| 33.1 | Function - Chọn đơn vị vận chuyển (User) | Vận chuyển | Check GUI and FUNC select shipping carrier function (User) | Tại Trang thanh toán hoặc giỏ hàng: 1. Chọn đơn vị vận chuyển (GHTK, GHN, J&T) |
| 33.2 | Function - Tính phí vận chuyển (User) | Vận chuyển | Check GUI and FUNC calculate shipping fee function (User) | Tại Trang thanh toán hoặc giỏ hàng: 1. Nhập địa chỉ - Hệ thống tự động tính phí |
| 33.3 | Function - Xem thông tin vận chuyển (User) | Vận chuyển | Check GUI and FUNC view shipping information function (User) | Tại Trang chi tiết sản phẩm: 1. Click tab [Vận chuyển] |
| 33.4 | Function - Nhập thông tin giao hàng (User) | Vận chuyển | Check GUI and FUNC enter shipping information function (User) | Tại Trang thanh toán: 1. Điền đầy đủ thông tin (Tên, SĐT, Địa chỉ, Ghi chú) |
| 33.5 | Function - Xem trạng thái vận chuyển (User) | Vận chuyển | Check GUI and FUNC view shipping status function (User) | Tại Trang theo dõi đơn hàng: 1. Xem trạng thái vận chuyển hiện tại |
| 33.6 | Layout - Vận chuyển (User) | [Layout Vận chuyển](8.%20Chức%20năng%20vận%20chuyển.md) | GUI chức năng Vận chuyển | Tại Trang thanh toán hoặc giỏ hàng: 1. Chọn phương thức vận chuyển |
| **9. CHỨC NĂNG KHUYẾN MÃI** |
| 34 | Function - Xem danh sách khuyến mãi (User) | Khuyến mãi | Check GUI and FUNC view promotions list function (User) | Tại Menu ứng dụng: 1. Click [Khuyến mãi] hoặc truy cập `/user/promotions` |
| 35 | Function - Xem chi tiết khuyến mãi (User) | Khuyến mãi | Check GUI and FUNC view promotion details function (User) | Tại Trang khuyến mãi: 1. Click vào khuyến mãi hoặc truy cập `/user/promotions/[code]` |
| 36 | Function - Áp dụng mã giảm giá (User) | Khuyến mãi | Check GUI and FUNC apply discount code function (User) | Tại Trang giỏ hàng hoặc thanh toán: 1. Nhập mã giảm giá 2. Click [Áp dụng] |
| 36.1 | Function - Xem mã giảm giá khả dụng (User) | Khuyến mãi | Check GUI and FUNC view available discount codes function (User) | Tại Trang giỏ hàng: 1. Xem danh sách mã giảm giá có sẵn |
| 36.2 | Function - Áp dụng mã giảm giá sản phẩm (User) | Khuyến mãi | Check GUI and FUNC apply product discount code function (User) | Tại Trang chi tiết sản phẩm: 1. Click [Áp dụng mã] cho mã giảm giá riêng sản phẩm |
| 36.3 | Function - Xem khuyến mãi theo hạng thành viên (User) | Khuyến mãi | Check GUI and FUNC view member rank promotions function (User) | Tại Trang khuyến mãi: 1. Xem các khuyến mãi dành cho hạng thành viên của mình |
| 36.4 | Layout - Khuyến mãi (User) | [Layout Khuyến mãi](9.%20Chức%20năng%20khuyến%20mãi.md) | GUI chức năng Khuyến mãi | Tại Menu ứng dụng: 1. Click [Khuyến mãi] hoặc truy cập `/user/promotions` |
| **10. CHỨC NĂNG ĐÁNH GIÁ NÂNG CAO - ĐÁNH GIÁ SẢN PHẨM SAU KHI MUA HÀNG** |
| 37 | Function - Để lại đánh giá sản phẩm (User) | Đánh giá nâng cao - đánh giá sản phẩm sau khi mua hàng | Check GUI and FUNC leave product review function (User) | Tại Trang chi tiết sản phẩm hoặc trang đánh giá: 1. Click [Viết đánh giá] hoặc truy cập `/user/reviews` |
| 38 | Function - Xem đánh giá sản phẩm (User) | Đánh giá nâng cao - đánh giá sản phẩm sau khi mua hàng | Check GUI and FUNC view product reviews function (User) | Tại Trang chi tiết sản phẩm: 1. Scroll xuống phần đánh giá |
| 39 | Function - Chỉnh sửa đánh giá (User) | Đánh giá nâng cao - đánh giá sản phẩm sau khi mua hàng | Check GUI and FUNC edit review function (User) | Tại Trang đánh giá của tôi: 1. Click [Chỉnh sửa] bên cạnh đánh giá |
| 40 | Function - Xóa đánh giá (User) | Đánh giá nâng cao - đánh giá sản phẩm sau khi mua hàng | Check GUI and FUNC delete review function (User) | Tại Trang đánh giá của tôi: 1. Click [Xóa] bên cạnh đánh giá |
| 41 | Function - Đánh giá hữu ích (User) | Đánh giá nâng cao - đánh giá sản phẩm sau khi mua hàng | Check GUI and FUNC mark review helpful function (User) | Tại Trang đánh giá sản phẩm: 1. Click [Hữu ích] hoặc [Không hữu ích] |
| 42 | Function - Báo cáo đánh giá (User) | Đánh giá nâng cao - đánh giá sản phẩm sau khi mua hàng | Check GUI and FUNC report review function (User) | Tại Trang đánh giá sản phẩm: 1. Click [Báo cáo] bên cạnh đánh giá |
| 42.1 | Function - Lọc đánh giá theo điểm (User) | Đánh giá nâng cao - đánh giá sản phẩm sau khi mua hàng | Check GUI and FUNC filter reviews by rating function (User) | Tại Trang đánh giá: 1. Chọn điểm từ dropdown (1-5 sao) |
| 42.2 | Function - Sắp xếp đánh giá (User) | Đánh giá nâng cao - đánh giá sản phẩm sau khi mua hàng | Check GUI and FUNC sort reviews function (User) | Tại Trang đánh giá: 1. Chọn tiêu chí sắp xếp (Mới nhất, Hữu ích nhất, Điểm cao nhất) |
| 42.3 | Function - Xem đánh giá chờ xử lý (User) | Đánh giá nâng cao - đánh giá sản phẩm sau khi mua hàng | Check GUI and FUNC view pending reviews function (User) | Tại Trang đánh giá: 1. Click tab [Chờ đánh giá] |
| 42.4 | Function - Đánh giá với hình ảnh/video (User) | Đánh giá nâng cao - đánh giá sản phẩm sau khi mua hàng | Check GUI and FUNC review with images/videos function (User) | Tại Trang viết đánh giá: 1. Upload hình ảnh hoặc video kèm theo đánh giá |
| 42.5 | Layout - Đánh giá nâng cao - đánh giá sản phẩm sau khi mua hàng (User) | [Layout Đánh giá Nâng cao](10.%20Chức%20năng%20đánh%20giá%20nâng%20cao%20-%20đánh%20giá%20sản%20phẩm%20sau%20khi%20mua%20hàng.md) | GUI chức năng Đánh giá nâng cao - đánh giá sản phẩm sau khi mua hàng | Tại Trang chi tiết sản phẩm hoặc trang đánh giá: 1. Click [Viết đánh giá] hoặc truy cập `/user/reviews` |
| **11. CHỨC NĂNG DANH SÁCH SẢN PHẨM YÊU THÍCH** |
| 43 | Function - Xem danh sách yêu thích (User) | Danh sách sản phẩm yêu thích | Check GUI and FUNC view wishlist function (User) | Tại Menu Ứng dụng phía User: 1. Click [Yêu thích] hoặc truy cập `/user/wishlist` |
| 44 | Function - Thêm vào yêu thích (User) | Danh sách sản phẩm yêu thích | Check GUI and FUNC add to wishlist function (User) | Tại Trang chi tiết sản phẩm hoặc danh sách: 1. Click [Thêm vào yêu thích] |
| 45 | Function - Xóa khỏi yêu thích (User) | Danh sách sản phẩm yêu thích | Check GUI and FUNC remove from wishlist function (User) | Tại Trang yêu thích: 1. Click [Xóa] hoặc icon trái tim |
| 45.1 | Function - Tìm kiếm trong yêu thích (User) | Danh sách sản phẩm yêu thích | Check GUI and FUNC search in wishlist function (User) | Tại Trang yêu thích: 1. Nhập từ khóa vào ô tìm kiếm |
| 45.2 | Function - Lọc yêu thích theo danh mục (User) | Danh sách sản phẩm yêu thích | Check GUI and FUNC filter wishlist by category function (User) | Tại Trang yêu thích: 1. Chọn danh mục từ dropdown |
| 45.3 | Function - Sắp xếp yêu thích (User) | Danh sách sản phẩm yêu thích | Check GUI and FUNC sort wishlist function (User) | Tại Trang yêu thích: 1. Chọn tiêu chí sắp xếp (Ngày thêm, Giá, Tên, Đánh giá) |
| 45.4 | Function - Thêm tất cả vào giỏ hàng (User) | Danh sách sản phẩm yêu thích | Check GUI and FUNC add all to cart function (User) | Tại Trang yêu thích: 1. Click [Thêm tất cả vào giỏ] |
| 45.5 | Function - Chia sẻ sản phẩm yêu thích (User) | Danh sách sản phẩm yêu thích | Check GUI and FUNC share wishlist item function (User) | Tại Trang yêu thích: 1. Click [Chia sẻ] bên cạnh sản phẩm |
| 45.6 | Function - So sánh sản phẩm (User) | Danh sách sản phẩm yêu thích | Check GUI and FUNC compare products function (User) | Tại Trang yêu thích: 1. Click [So sánh] bên cạnh sản phẩm |
| 45.7 | Function - Đăng ký thông báo giá (User) | Danh sách sản phẩm yêu thích | Check GUI and FUNC price alert function (User) | Tại Trang yêu thích: 1. Click [Thông báo giá] bên cạnh sản phẩm |
| 45.8 | Function - Xóa tất cả yêu thích (User) | Danh sách sản phẩm yêu thích | Check GUI and FUNC clear all wishlist function (User) | Tại Trang yêu thích: 1. Click [Xóa tất cả] |
| 45.9 | Layout - Danh sách sản phẩm yêu thích (User) | [Layout Danh sách Sản phẩm Yêu thích](11.%20Chức%20năng%20danh%20sách%20sản%20phẩm%20yêu%20thích.md) | GUI chức năng Danh sách sản phẩm yêu thích | Tại Menu Ứng dụng phía User: 1. Click [Yêu thích] hoặc truy cập `/user/wishlist` |
| **12. CHỨC NĂNG HỖ TRỢ - LIÊN HỆ** |
| 46 | Function - Gửi yêu cầu hỗ trợ (User) | Hỗ trợ - liên hệ | Check GUI and FUNC send support request function (User) | Tại Menu ứng dụng phía User: 1. Click [Hỗ trợ] 2. Click [Tạo yêu cầu mới] hoặc truy cập `/user/support` |
| 47 | Function - Chat hỗ trợ (User) | Hỗ trợ - liên hệ | Check GUI and FUNC chat support function (User) | Tại Trang hỗ trợ: 1. Click tab [Chat trực tiếp] |
| 48 | Function - Quản lý yêu cầu hỗ trợ (User) | Hỗ trợ - liên hệ | Check GUI and FUNC manage support requests function (User) | Tại Trang hỗ trợ: 1. Click tab [Yêu cầu hỗ trợ] - Xem danh sách, lọc, tìm kiếm |
| 49 | Function - Câu hỏi thường gặp (User) | Hỗ trợ - liên hệ | Check GUI and FUNC FAQ function (User) | Tại Trang hỗ trợ: 1. Click tab [Câu hỏi thường gặp] |
| 50 | Function - Thông tin liên hệ (User) | Hỗ trợ - liên hệ | Check GUI and FUNC contact information function (User) | Tại Trang hỗ trợ: 1. Xem thông tin liên hệ (Hotline, Email, Địa chỉ) |
| 50.1 | Function - Lọc yêu cầu hỗ trợ (User) | Hỗ trợ - liên hệ | Check GUI and FUNC filter support requests function (User) | Tại Trang yêu cầu hỗ trợ: 1. Chọn trạng thái và danh mục từ dropdown |
| 50.2 | Function - Xem chi tiết yêu cầu hỗ trợ (User) | Hỗ trợ - liên hệ | Check GUI and FUNC view support request details function (User) | Tại Trang yêu cầu hỗ trợ: 1. Click vào yêu cầu để xem chi tiết |
| 50.3 | Function - Export lịch sử chat (User) | Hỗ trợ - liên hệ | Check GUI and FUNC export chat history function (User) | Tại Trang chat hỗ trợ: 1. Click [Export lịch sử] |
| 50.4 | Function - Tìm kiếm trong chat (User) | Hỗ trợ - liên hệ | Check GUI and FUNC search in chat function (User) | Tại Trang chat hỗ trợ: 1. Sử dụng ô tìm kiếm trong chat |
| 50.5 | Layout - Hỗ trợ - liên hệ (User) | [Layout Hỗ trợ - Liên hệ](12.%20Chức%20năng%20hỗ%20trợ%20-%20liên%20hệ.md) | GUI chức năng Hỗ trợ - liên hệ | Tại Menu ứng dụng phía User: 1. Click [Hỗ trợ] hoặc truy cập `/user/support` |
| **13. CHỨC NĂNG YÊU CẦU ĐẶT HÀNG** |
| 51 | Function - Gửi yêu cầu đặt hàng (User) | Yêu cầu đặt hàng | Check GUI and FUNC send special request function (User) | Tại Menu Ứng dụng phía User: 1. Click [Yêu cầu nhập hàng] hoặc truy cập `/user/requests` |
| 52 | Function - Xem chi tiết yêu cầu (User) | Yêu cầu đặt hàng | Check GUI and FUNC view request details function (User) | Tại Trang yêu cầu đặt hàng: 1. Click [Xem] hoặc truy cập `/user/requests/[id]` |
| 52.1 | Function - Lọc yêu cầu theo trạng thái (User) | Yêu cầu đặt hàng | Check GUI and FUNC filter requests by status function (User) | Tại Trang yêu cầu đặt hàng: 1. Chọn trạng thái từ dropdown |
| 52.2 | Function - Hủy yêu cầu đặt hàng (User) | Yêu cầu đặt hàng | Check GUI and FUNC cancel request function (User) | Tại Trang chi tiết yêu cầu: 1. Click [Hủy yêu cầu] (nếu chưa được xử lý) |
| 52.3 | Function - Cập nhật yêu cầu đặt hàng (User) | Yêu cầu đặt hàng | Check GUI and FUNC update request function (User) | Tại Trang chi tiết yêu cầu: 1. Click [Chỉnh sửa] để cập nhật thông tin |
| 52.4 | Layout - Yêu cầu đặt hàng (User) | [Layout Yêu cầu Đặt hàng](13.%20Chức%20năng%20yêu%20cầu%20đặt%20hàng.md) | GUI chức năng Yêu cầu đặt hàng | Tại Menu Ứng dụng phía User: 1. Click [Yêu cầu nhập hàng] hoặc truy cập `/user/requests` |
| **14. CHỨC NĂNG ĐẶT TRƯỚC SẢN PHẨM** |
| 53 | Function - Đặt trước sản phẩm (User) | Đặt trước sản phẩm | Check GUI and FUNC pre-order product function (User) | Tại Menu Ứng dụng phía User: 1. Click [Đặt trước mô hình] hoặc truy cập `/user/borrow` |
| 54 | Function - Xem danh sách đặt trước (User) | Đặt trước sản phẩm | Check GUI and FUNC view pre-orders list function (User) | Tại Trang đặt trước: 1. Xem danh sách các sản phẩm đã đặt trước |
| 55 | Function - Hủy đặt trước (User) | Đặt trước sản phẩm | Check GUI and FUNC cancel pre-order function (User) | Tại Trang đặt trước: 1. Click [Hủy đặt trước] bên cạnh sản phẩm |
| 55.1 | Function - Xem chi tiết đặt trước (User) | Đặt trước sản phẩm | Check GUI and FUNC view pre-order details function (User) | Tại Trang danh sách đặt trước: 1. Click [Xem chi tiết] |
| 55.2 | Function - Quản lý trạng thái đặt trước (User) | Đặt trước sản phẩm | Check GUI and FUNC manage pre-order status function (User) | Tại Trang danh sách đặt trước: 1. Sử dụng tab trạng thái để lọc và theo dõi |
| 55.3 | Function - Nhận thông báo có hàng (User) | Đặt trước sản phẩm | Check GUI and FUNC receive stock notification function (User) | Tại Trang đặt trước: 1. Hệ thống tự động gửi thông báo khi có hàng |
| 55.4 | Layout - Đặt trước sản phẩm (User) | [Layout Đặt trước Sản phẩm](14.%20Chức%20năng%20đặt%20trước%20sản%20phẩm.md) | GUI chức năng Đặt trước sản phẩm | Tại Menu Ứng dụng phía User: 1. Click [Đặt trước mô hình] hoặc truy cập `/user/borrow` |
| **15. CHỨC NĂNG THÔNG BÁO** |
| 56 | Function - Xem thông báo (User) | Thông báo | Check GUI and FUNC view notifications function (User) | Tại Menu Ứng dụng phía User: 1. Click [Thông báo] hoặc truy cập `/user/notifications` |
| 57 | Function - Đánh dấu đã đọc (User) | Thông báo | Check GUI and FUNC mark as read function (User) | Tại Trang thông báo: 1. Click [Đánh dấu đã đọc] bên cạnh thông báo |
| 58 | Function - Đánh dấu tất cả đã đọc (User) | Thông báo | Check GUI and FUNC mark all as read function (User) | Tại Trang thông báo: 1. Click [Đánh dấu tất cả đã đọc] |
| 59 | Function - Xóa thông báo (User) | Thông báo | Check GUI and FUNC delete notification function (User) | Tại Trang thông báo: 1. Click [Xóa] bên cạnh thông báo |
| 60 | Function - Xóa tất cả thông báo đã đọc (User) | Thông báo | Check GUI and FUNC clear all read notifications function (User) | Tại Trang thông báo: 1. Click [Xóa đã đọc] |
| 60.1 | Function - Lọc thông báo theo loại (User) | Thông báo | Check GUI and FUNC filter notifications by type function (User) | Tại Trang thông báo: 1. Chọn tab loại thông báo (Đơn hàng, Khuyến mãi, Yêu thích, Đánh giá, Hệ thống, Hỗ trợ) |
| 60.2 | Function - Lọc thông báo theo mức độ ưu tiên (User) | Thông báo | Check GUI and FUNC filter notifications by priority function (User) | Tại Trang thông báo: 1. Chọn mức độ ưu tiên từ dropdown (Cao, Trung bình, Thấp) |
| 60.3 | Function - Tìm kiếm thông báo (User) | Thông báo | Check GUI and FUNC search notifications function (User) | Tại Trang thông báo: 1. Nhập từ khóa vào ô tìm kiếm |
| 60.4 | Function - Xem chi tiết thông báo (User) | Thông báo | Check GUI and FUNC view notification details function (User) | Tại Trang thông báo: 1. Click vào thông báo để xem chi tiết và thực hiện hành động |
| 60.5 | Layout - Thông báo (User) | [Layout Thông báo](15.%20Chức%20năng%20thông%20báo.md) | GUI chức năng Thông báo | Tại Menu Ứng dụng phía User: 1. Click [Thông báo] hoặc truy cập `/user/notifications` |
| **16. TẠO - HIỂN THỊ BÀI VIẾT** |
| 61 | Function - Tạo bài viết (User) | Tạo - hiển thị bài viết | Check GUI and FUNC create post function (User) | Tại Menu Ứng dụng phía User: 1. Click [Tạo bài viết] hoặc truy cập `/user/posts/create` |
| 62 | Function - Hiển thị danh sách bài viết (User) | Tạo - hiển thị bài viết | Check GUI and FUNC display posts list function (User) | Tại Menu Ứng dụng phía User: 1. Click [Bài viết] hoặc truy cập `/user/posts` |
| 63 | Function - Xem chi tiết bài viết (User) | Tạo - hiển thị bài viết | Check GUI and FUNC view post details function (User) | Tại Trang danh sách bài viết: 1. Click vào bài viết hoặc truy cập `/user/posts/[id]` |
| 64 | Function - Chỉnh sửa bài viết (User) | Tạo - hiển thị bài viết | Check GUI and FUNC edit post function (User) | Tại Trang chi tiết bài viết của mình: 1. Click [Chỉnh sửa] hoặc truy cập `/user/posts/[id]/edit` |
| 65 | Function - Xóa bài viết (User) | Tạo - hiển thị bài viết | Check GUI and FUNC delete post function (User) | Tại Trang chi tiết bài viết của mình: 1. Click [Xóa bài viết] |
| 65.1 | Function - Tìm kiếm bài viết (User) | Tạo - hiển thị bài viết | Check GUI and FUNC search posts function (User) | Tại Trang danh sách bài viết: 1. Nhập từ khóa vào ô tìm kiếm |
| 65.2 | Function - Lọc bài viết theo danh mục (User) | Tạo - hiển thị bài viết | Check GUI and FUNC filter posts by category function (User) | Tại Trang danh sách bài viết: 1. Chọn danh mục từ dropdown (Gundam, Figure, Mô hình xe, Máy bay) |
| 65.3 | Function - Lọc bài viết theo thời gian (User) | Tạo - hiển thị bài viết | Check GUI and FUNC filter posts by time function (User) | Tại Trang danh sách bài viết: 1. Chọn khoảng thời gian (Hôm nay, Tuần này, Tháng này) |
| 65.4 | Function - Sắp xếp bài viết (User) | Tạo - hiển thị bài viết | Check GUI and FUNC sort posts function (User) | Tại Trang danh sách bài viết: 1. Chọn tiêu chí sắp xếp (Mới nhất, Nhiều like nhất, Nhiều bình luận nhất) |
| 65.5 | Function - Phân trang bài viết (User) | Tạo - hiển thị bài viết | Check GUI and FUNC paginate posts function (User) | Tại Trang danh sách bài viết: 1. Sử dụng nút phân trang để xem thêm |
| 65.6 | Layout - Tạo - hiển thị bài viết (User) | [Layout Tạo - Hiển thị Bài viết](16.%20Tạo%20-%20hiển%20thị%20bài%20viết.md) | GUI chức năng Tạo - hiển thị bài viết | Tại Menu Ứng dụng phía User: 1. Click [Bài viết] hoặc truy cập `/user/posts` |
| **17. TƯƠNG TÁC BÀI VIẾT** |
| 66 | Function - Like bài viết (User) | Tương tác bài viết | Check GUI and FUNC like post function (User) | Tại Trang chi tiết bài viết: 1. Click [Like] hoặc icon trái tim |
| 67 | Function - Bình luận bài viết (User) | Tương tác bài viết | Check GUI and FUNC comment post function (User) | Tại Trang chi tiết bài viết: 1. Nhập bình luận 2. Click [Gửi] |
| 68 | Function - Chia sẻ bài viết (User) | Tương tác bài viết | Check GUI and FUNC share post function (User) | Tại Trang chi tiết bài viết: 1. Click [Chia sẻ] |
| 68.1 | Function - Xóa bình luận (User) | Tương tác bài viết | Check GUI and FUNC delete comment function (User) | Tại Trang chi tiết bài viết: 1. Click [Xóa] bên cạnh bình luận của mình |
| 68.2 | Function - Chỉnh sửa bình luận (User) | Tương tác bài viết | Check GUI and FUNC edit comment function (User) | Tại Trang chi tiết bài viết: 1. Click [Chỉnh sửa] bên cạnh bình luận của mình |
| 68.3 | Function - Like bình luận (User) | Tương tác bài viết | Check GUI and FUNC like comment function (User) | Tại Trang chi tiết bài viết: 1. Click [Like] bên cạnh bình luận |
| 68.4 | Function - Phản hồi bình luận (User) | Tương tác bài viết | Check GUI and FUNC reply to comment function (User) | Tại Trang chi tiết bài viết: 1. Click [Phản hồi] bên cạnh bình luận |
| 68.5 | Layout - Tương tác bài viết (User) | [Layout Tương tác Bài viết](17.%20Tương%20tác%20bài%20viết.md) | GUI chức năng Tương tác bài viết | Tại Trang chi tiết bài viết: 1. Xem phần bình luận và tương tác |
| **18. CHỨC NĂNG XEM TRANG CÁ NHÂN NGƯỜI LẠ** |
| 69 | Function - Xem trang cá nhân người lạ (User) | Xem trang cá nhân người lạ | Check GUI and FUNC view stranger profile function (User) | Tại Trang bài viết hoặc bình luận: 1. Click vào tên người dùng hoặc truy cập `/user/profile/[id]` |
| 69.1 | Function - Xem bài viết của người khác (User) | Xem trang cá nhân người lạ | Check GUI and FUNC view other user posts function (User) | Tại Trang cá nhân người khác: 1. Xem danh sách bài viết của họ |
| 69.2 | Function - Xem thư viện ảnh (User) | Xem trang cá nhân người lạ | Check GUI and FUNC view photo gallery function (User) | Tại Trang cá nhân người khác: 1. Click [Thư viện ảnh] |
| 69.3 | Function - Theo dõi người dùng (User) | Xem trang cá nhân người lạ | Check GUI and FUNC follow user function (User) | Tại Trang cá nhân người khác: 1. Click [Theo dõi] |
| 69.4 | Function - Bỏ theo dõi người dùng (User) | Xem trang cá nhân người lạ | Check GUI and FUNC unfollow user function (User) | Tại Trang cá nhân người đang theo dõi: 1. Click [Bỏ theo dõi] |
| 69.5 | Layout - Xem trang cá nhân người lạ (User) | [Layout Xem Trang Cá nhân Người lạ](18.%20Chức%20năng%20xem%20trang%20cá%20nhân%20người%20lạ.md) | GUI chức năng Xem trang cá nhân người lạ | Tại Trang bài viết hoặc bình luận: 1. Click vào tên người dùng hoặc truy cập `/user/profile/[id]` |
| **19. CHỨC NĂNG BẢO MẬT** |
| 70 | Function - Xem lịch sử đăng nhập (User) | Bảo mật | Check GUI and FUNC login history function (User) | Tại Menu Ứng dụng phía User: 1. Click [Tài khoản] 2. Click [Lịch sử đăng nhập] hoặc truy cập `/user/account/logins` |
| 71 | Function - Quản lý phiên đăng nhập (User) | Bảo mật | Check GUI and FUNC sessions management function (User) | Tại Menu Ứng dụng phía User: 1. Click [Tài khoản] 2. Click [Phiên đăng nhập] hoặc truy cập `/user/account/sessions` |
| 72 | Function - Đăng xuất khỏi thiết bị khác (User) | Bảo mật | Check GUI and FUNC logout from other device function (User) | Tại Trang quản lý phiên đăng nhập: 1. Click [Đăng xuất] bên cạnh thiết bị |
| 73 | Function - Phát hiện đăng nhập lạ (User) | Bảo mật | Check GUI and FUNC detect suspicious login function (User) | Tại Trang lịch sử đăng nhập: 1. Hệ thống tự động phát hiện và cảnh báo đăng nhập từ thiết bị/IP lạ |
| 74 | Function - Auto logout khi hết hạn (User) | Bảo mật | Check GUI and FUNC auto logout on timeout function (User) | Tại Trang quản lý phiên đăng nhập: 1. Hệ thống tự động đăng xuất khi session hết hạn |
| 74.1 | Function - Xác thực hai yếu tố (User) | Bảo mật | Check GUI and FUNC two-factor authentication function (User) | Tại Trang cài đặt bảo mật: 1. Bật/tắt xác thực hai yếu tố |
| 74.2 | Function - Xác minh email (User) | Bảo mật | Check GUI and FUNC email verification function (User) | Tại Trang tài khoản: 1. Click [Xác minh email] |
| 74.3 | Layout - Bảo mật (User) | [Layout Bảo mật](19.%20Chức%20năng%20bảo%20mật.md) | GUI chức năng Bảo mật | Tại Menu Ứng dụng phía User: 1. Click [Tài khoản] 2. Click [Bảo mật] hoặc truy cập `/user/account/security` |

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
- **P3 - Low**: Các chức năng bổ sung (Thông báo, Hỗ trợ)

---

## THỐNG KÊ TEST CASE

**Tổng số chức năng User:** 93 functions

**Phân loại theo 19 mục chức năng:**
1. **Quản lý tài khoản:** 10 functions (1-5.5)
2. **Chức năng hiển thị sản phẩm:** 6 functions (6-7.5)
3. **Chức năng tìm kiếm sản phẩm:** 6 functions (8-8.5)
4. **Chức năng bộ lọc sản phẩm - phân loại sản phẩm:** 9 functions (9-9.8)
5. **Chức năng quản lý giỏ hàng:** 11 functions (10-19.1)
6. **Chức năng quản lý đơn hàng:** 9 functions (20-27.3)
7. **Chức năng thanh toán đơn hàng:** 7 functions (28-32.4)
8. **Chức năng vận chuyển:** 7 functions (33-33.6)
9. **Chức năng khuyến mãi:** 5 functions (34-36.4)
10. **Chức năng đánh giá nâng cao - đánh giá sản phẩm sau khi mua hàng:** 9 functions (37-42.5)
11. **Chức năng danh sách sản phẩm yêu thích:** 10 functions (43-45.9)
12. **Chức năng hỗ trợ - liên hệ:** 10 functions (46-50.5)
13. **Chức năng yêu cầu đặt hàng:** 5 functions (51-52.4)
14. **Chức năng đặt trước sản phẩm:** 6 functions (53-55.4)
15. **Chức năng thông báo:** 10 functions (56-60.5)
16. **Tạo - hiển thị bài viết:** 11 functions (61-65.6)
17. **Tương tác bài viết:** 6 functions (66-68.5)
18. **Chức năng xem trang cá nhân người lạ:** 6 functions (69-69.5)
19. **Chức năng bảo mật:** 6 functions (70-74.3)

---

**Người tạo:** Testing Team  
**Ngày cập nhật:** 2025-01-20  
**Phiên bản:** 1.0
