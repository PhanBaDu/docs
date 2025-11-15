# Test Case Template - Chức năng danh sách sản phẩm yêu thích (User)

## Module Code
**Model Management Store: Chức năng danh sách sản phẩm yêu thích User**

## Test Requirement
1. Thêm vào danh sách yêu thích
2. Hiển thị danh sách yêu thích
3. Quản lý danh sách yêu thích
4. Tìm kiếm và lọc sản phẩm yêu thích
5. Thao tác với sản phẩm yêu thích

---

## Test Summary

### Người thực hiện Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 132 |
| **Fail** | 0 |
| **Untested** | 38 |
| **N/A** | 0 |
| **Number of Test cases** | 170 |

---

## Test Cases

### Function: Thêm vào danh sách yêu thích

#### Check GUI: Thêm vào danh sách yêu thích

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-TVDSYT-01** | Kiểm tra nút yêu thích trên trang sản phẩm | 1. Truy cập /user/products<br>2. Kiểm tra nút yêu thích | Hiển thị nút với icon Heart, có thể click, khi đã yêu thích có màu fill-red-500 text-red-500 | | Pass | 11/15/2015 | |
| **GUI-TVDSYT-02** | Kiểm tra nút yêu thích trên trang chi tiết sản phẩm | 1. Truy cập /user/products/[id]<br>2. Kiểm tra nút yêu thích | Hiển thị nút "Yêu thích" với icon Heart, variant outline size lg, khi đã yêu thích icon có màu fill-red-500 text-red-500 | | Pass | 11/15/2015 | |
| **GUI-TVDSYT-03** | Kiểm tra nút yêu thích trên trang giỏ hàng | 1. Truy cập /user/cart<br>2. Kiểm tra nút yêu thích | Hiển thị nút với icon Heart, variant ghost, khi đã yêu thích có màu fill-red-500 text-red-500 | | Pass | 11/15/2015 | |
| **GUI-TVDSYT-04** | Kiểm tra trạng thái chưa yêu thích | 1. Xem sản phẩm chưa yêu thích<br>2. Kiểm tra icon | Icon Heart không có fill, màu text mặc định | | Pass | 11/15/2015 | |
| **GUI-TVDSYT-05** | Kiểm tra trạng thái đã yêu thích | 1. Xem sản phẩm đã yêu thích<br>2. Kiểm tra icon | Icon Heart có fill-red-500 text-red-500 | | Pass | 11/15/2015 | |
| **GUI-TVDSYT-06** | Kiểm tra số lượng yêu thích trên header | 1. Truy cập bất kỳ trang nào<br>2. Kiểm tra badge số lượng | Hiển thị badge với số lượng sản phẩm trong danh sách yêu thích (nếu có) | | Pass | 11/15/2015 | |
| **GUI-TVDSYT-07** | Kiểm tra animation khi click | 1. Click nút yêu thích<br>2. Quan sát animation | Có hiệu ứng animation khi click, icon thay đổi màu mượt mà | | Pass | 11/15/2015 | |

---

### Check FUNC: Thêm vào danh sách yêu thích

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TVDSYT-01** | Thêm sản phẩm vào yêu thích từ trang sản phẩm | 1. Truy cập /user/products<br>2. Click nút yêu thích trên sản phẩm chưa yêu thích | Sản phẩm được thêm vào danh sách yêu thích, icon chuyển sang màu đỏ, hiển thị toast "Đã thêm vào danh sách yêu thích", số lượng yêu thích tăng lên | | Pass | 11/15/2015 | |
| **FUNC-TVDSYT-02** | Thêm sản phẩm vào yêu thích từ trang chi tiết | 1. Truy cập /user/products/[id]<br>2. Click nút "Yêu thích" | Sản phẩm được thêm vào danh sách yêu thích, icon chuyển sang màu đỏ, hiển thị toast "Đã thêm vào danh sách yêu thích" | | Pass | 11/15/2015 | |
| **FUNC-TVDSYT-03** | Thêm sản phẩm vào yêu thích từ giỏ hàng | 1. Truy cập /user/cart<br>2. Click nút yêu thích trên sản phẩm trong giỏ | Sản phẩm được thêm vào danh sách yêu thích, icon chuyển sang màu đỏ, hiển thị toast "Đã thêm vào danh sách yêu thích" | | Pass | 11/15/2015 | |
| **FUNC-TVDSYT-04** | Xóa sản phẩm khỏi yêu thích | 1. Click nút yêu thích trên sản phẩm đã yêu thích | Sản phẩm được xóa khỏi danh sách yêu thích, icon quay về màu mặc định, hiển thị toast "Đã xóa khỏi danh sách yêu thích", số lượng yêu thích giảm đi | | Pass | 11/15/2015 | |
| **FUNC-TVDSYT-05** | Cập nhật trạng thái đồng bộ | 1. Thêm sản phẩm vào yêu thích ở trang A<br>2. Chuyển sang trang B<br>3. Kiểm tra trạng thái | Trạng thái yêu thích được đồng bộ trên tất cả các trang, icon hiển thị đúng trạng thái | | Pass | 11/15/2015 | |
| **FUNC-TVDSYT-06** | Thêm nhiều sản phẩm vào yêu thích | 1. Thêm lần lượt nhiều sản phẩm vào yêu thích | Tất cả sản phẩm được thêm thành công, số lượng yêu thích tăng tương ứng, mỗi sản phẩm có toast xác nhận riêng | | Pass | 11/15/2015 | |
| **FUNC-TVDSYT-07** | Kiểm tra sản phẩm đã có trong yêu thích | 1. Thêm sản phẩm vào yêu thích<br>2. Thêm lại cùng sản phẩm | Hệ thống không thêm trùng, hoặc tự động xóa nếu đã có, hiển thị thông báo phù hợp | | Pass | 11/15/2015 | |
| **FUNC-TVDSYT-08** | Thêm sản phẩm khi chưa đăng nhập | 1. Đăng xuất<br>2. Thử thêm sản phẩm vào yêu thích | Hiển thị thông báo yêu cầu đăng nhập, chuyển đến trang đăng nhập, sau khi đăng nhập có thể thêm yêu thích | | Pass | 11/15/2015 | |

---

### Function: Hiển thị danh sách yêu thích

#### Check GUI: Hiển thị danh sách yêu thích

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-HTDSYT-01** | Kiểm tra tiêu đề trang | 1. Truy cập /user/wishlist<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Danh sách yêu thích" với text-3xl font-bold | | Pass | 11/15/2015 | |
| **GUI-HTDSYT-02** | Kiểm tra icon trang | 1. Truy cập /user/wishlist<br>2. Kiểm tra icon | Hiển thị icon Heart với màu red-500 hoặc trong component | | Pass | 11/15/2015 | |
| **GUI-HTDSYT-03** | Kiểm tra số lượng sản phẩm | 1. Truy cập /user/wishlist<br>2. Kiểm tra số lượng | Hiển thị "[Số] sách trong danh sách yêu thích của bạn" với text-muted-foreground | | Pass | 11/15/2015 | |
| **GUI-HTDSYT-04** | Kiểm tra grid layout | 1. Truy cập /user/wishlist<br>2. Kiểm tra layout | Hiển thị grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-6 | | Pass | 11/15/2015 | |
| **GUI-HTDSYT-05** | Kiểm tra card sản phẩm | 1. Xem danh sách yêu thích<br>2. Kiểm tra card | Hiển thị card với hover:shadow-lg transition-shadow, chứa hình ảnh, thông tin sản phẩm | | Pass | 11/15/2015 | |
| **GUI-HTDSYT-06** | Kiểm tra hình ảnh sản phẩm | 1. Xem card sản phẩm<br>2. Kiểm tra hình ảnh | Hiển thị hình ảnh với aspect-[3/4], object-cover, rounded-t-lg, có hiệu ứng hover:scale-105 | | Pass | 11/15/2015 | |
| **GUI-HTDSYT-07** | Kiểm tra tên sản phẩm | 1. Xem card sản phẩm<br>2. Kiểm tra tên | Hiển thị tên sản phẩm với font-semibold text-sm line-clamp-2 | | Pass | 11/15/2015 | |
| **GUI-HTDSYT-08** | Kiểm tra tác giả/thương hiệu | 1. Xem card sản phẩm<br>2. Kiểm tra tác giả | Hiển thị tác giả/thương hiệu với text-xs text-muted-foreground, có icon User | | Pass | 11/15/2015 | |
| **GUI-HTDSYT-09** | Kiểm tra giá sản phẩm | 1. Xem card sản phẩm<br>2. Kiểm tra giá | Hiển thị giá với font-bold text-primary, format VNĐ, có giá gốc line-through nếu có giảm giá | | Pass | 11/15/2015 | |
| **GUI-HTDSYT-10** | Kiểm tra đánh giá | 1. Xem card sản phẩm<br>2. Kiểm tra đánh giá | Hiển thị 5 ngôi sao, sao được chọn có fill-yellow-400 text-yellow-400, có số lượng đánh giá trong ngoặc đơn | | Pass | 11/15/2015 | |
| **GUI-HTDSYT-11** | Kiểm tra trạng thái kho | 1. Xem card sản phẩm<br>2. Kiểm tra trạng thái | Hiển thị "Còn hàng ([Số])" màu green-600 hoặc "Hết hàng" màu red-600 với text-xs | | Pass | 11/15/2015 | |
| **GUI-HTDSYT-12** | Kiểm tra ngày thêm | 1. Xem card sản phẩm<br>2. Kiểm tra ngày | Hiển thị "Thêm vào: [Ngày]" với format ngày Việt Nam, text-xs text-muted-foreground | | Pass | 11/15/2015 | |
| **GUI-HTDSYT-13** | Kiểm tra badge sản phẩm | 1. Xem card sản phẩm<br>2. Kiểm tra badge | Hiển thị badge "Mới" (green-500), "Bán chạy" (orange-500), "-X%" (red-500) ở góc trên trái | | Pass | 11/15/2015 | |
| **GUI-HTDSYT-14** | Kiểm tra nút xóa khỏi yêu thích | 1. Xem card sản phẩm<br>2. Kiểm tra nút | Hiển thị nút với icon Heart fill-red-500, variant ghost size sm, absolute top-2 right-2 | | Pass | 11/15/2015 | |
| **GUI-HTDSYT-15** | Kiểm tra nút Quay lại | 1. Truy cập /user/wishlist<br>2. Kiểm tra nút | Hiển thị nút "Tiếp tục mua sắm" với icon ArrowLeft, variant ghost, link đến /user/products | | Pass | 11/15/2015 | |

---

### Check FUNC: Hiển thị danh sách yêu thích

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-HTDSYT-01** | Mở trang danh sách yêu thích | 1. Truy cập /user/wishlist | Hiển thị trang với tiêu đề "Danh sách yêu thích", số lượng sản phẩm, danh sách sản phẩm yêu thích | | Pass | 11/15/2015 | |
| **FUNC-HTDSYT-02** | Hiển thị danh sách sản phẩm | 1. Truy cập /user/wishlist<br>2. Có sản phẩm trong yêu thích | Hiển thị danh sách tất cả sản phẩm yêu thích với đầy đủ thông tin: hình ảnh, tên, tác giả, giá, đánh giá, trạng thái kho, ngày thêm | | Pass | 11/15/2015 | |
| **FUNC-HTDSYT-03** | Hiển thị thông tin chi tiết sản phẩm | 1. Xem danh sách yêu thích<br>2. Kiểm tra thông tin | Mỗi sản phẩm hiển thị đầy đủ: hình ảnh, tên, tác giả/thương hiệu, giá (có giá gốc nếu giảm), đánh giá, số lượng đánh giá, trạng thái kho, ngày thêm | | Pass | 11/15/2015 | |
| **FUNC-HTDSYT-04** | Hiển thị số lượng sản phẩm chính xác | 1. Truy cập /user/wishlist<br>2. Kiểm tra số lượng | Số lượng hiển thị chính xác với số sản phẩm thực tế trong danh sách, cập nhật tự động khi có thay đổi | | Pass | 11/15/2015 | |
| **FUNC-HTDSYT-05** | Hiển thị khi danh sách trống | 1. Truy cập /user/wishlist<br>2. Không có sản phẩm yêu thích | Hiển thị icon Heart, tiêu đề "Danh sách yêu thích trống", mô tả "Bạn chưa có sách nào trong danh sách yêu thích", nút "Khám phá sách" link đến /user/products | | Pass | 11/15/2015 | |
| **FUNC-HTDSYT-06** | Cập nhật real-time thông tin sản phẩm | 1. Xem danh sách yêu thích<br>2. Giá/thông tin sản phẩm thay đổi | Thông tin sản phẩm được cập nhật real-time để phản ánh đúng tình trạng hiện tại (giá, trạng thái kho) | | Pass | 11/15/2015 | |
| **FUNC-HTDSYT-07** | Hiển thị sản phẩm đã xóa khỏi shop | 1. Sản phẩm trong yêu thích bị xóa khỏi shop<br>2. Xem danh sách yêu thích | Sản phẩm vẫn hiển thị với badge "Sản phẩm không còn bán" hoặc tự động xóa khỏi danh sách yêu thích | | Pass | 11/15/2015 | |
| **FUNC-HTDSYT-08** | Kiểm tra responsive layout | 1. Truy cập /user/wishlist<br>2. Thay đổi kích thước màn hình | Layout tự động điều chỉnh: 1 cột mobile, 2 cột tablet, 3 cột desktop, 4 cột xl | | Pass | 11/15/2015 | |

---

### Function: Quản lý danh sách yêu thích

#### Check GUI: Quản lý danh sách yêu thích

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-QLDSYT-01** | Kiểm tra nút xóa sản phẩm | 1. Truy cập /user/wishlist<br>2. Kiểm tra nút xóa | Hiển thị nút với icon Heart fill-red-500, variant ghost size sm, absolute top-2 right-2 trên card | | Pass | 11/15/2015 | |
| **GUI-QLDSYT-02** | Kiểm tra nút thêm vào giỏ hàng | 1. Xem card sản phẩm<br>2. Kiểm tra nút | Hiển thị nút "Mua" với icon ShoppingCart, size sm, flex-1, disabled nếu hết hàng | | Pass | 11/15/2015 | |
| **GUI-QLDSYT-03** | Kiểm tra nút thêm tất cả vào giỏ hàng | 1. Truy cập /user/wishlist<br>2. Kiểm tra nút | Hiển thị nút "Thêm tất cả vào giỏ" với icon ShoppingCart, variant outline, disabled nếu không có sản phẩm còn hàng | | Pass | 11/15/2015 | |
| **GUI-QLDSYT-04** | Kiểm tra nút xóa tất cả | 1. Truy cập /user/wishlist<br>2. Kiểm tra nút | Hiển thị nút "Xóa tất cả" với icon Trash2, variant outline, màu text-red-600 hover:text-red-700 | | Pass | 11/15/2015 | |
| **GUI-QLDSYT-05** | Kiểm tra modal xác nhận xóa | 1. Nhấn nút xóa tất cả<br>2. Kiểm tra modal | Hiển thị modal xác nhận với tiêu đề, mô tả, nút "Xác nhận" và "Hủy" | | Pass | 11/15/2015 | |
| **GUI-QLDSYT-06** | Kiểm tra nút Xem chi tiết | 1. Xem card sản phẩm<br>2. Kiểm tra nút | Hiển thị nút "Chi tiết" với icon BookOpen, variant outline size sm, link đến /user/products/[id] | | Pass | 11/15/2015 | |

---

### Check FUNC: Quản lý danh sách yêu thích

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-QLDSYT-01** | Xóa sản phẩm khỏi danh sách | 1. Truy cập /user/wishlist<br>2. Nhấn nút xóa trên card sản phẩm | Sản phẩm được xóa khỏi danh sách, card biến mất, hiển thị toast "Đã xóa khỏi danh sách yêu thích", số lượng giảm đi | | Pass | 11/15/2015 | |
| **FUNC-QLDSYT-02** | Thêm sản phẩm vào giỏ hàng | 1. Truy cập /user/wishlist<br>2. Nhấn nút "Mua" trên sản phẩm còn hàng | Sản phẩm được thêm vào giỏ hàng, hiển thị toast "Đã thêm "[Tên sản phẩm]" vào giỏ hàng" | | Pass | 11/15/2015 | |
| **FUNC-QLDSYT-03** | Thêm sản phẩm hết hàng vào giỏ | 1. Truy cập /user/wishlist<br>2. Nhấn nút "Mua" trên sản phẩm hết hàng | Nút bị disabled, không thể thêm vào giỏ hàng, hiển thị thông báo "Sản phẩm đã hết hàng" | | Pass | 11/15/2015 | |
| **FUNC-QLDSYT-04** | Thêm tất cả vào giỏ hàng | 1. Truy cập /user/wishlist<br>2. Nhấn nút "Thêm tất cả vào giỏ" | Tất cả sản phẩm còn hàng được thêm vào giỏ hàng, hiển thị toast "Đã thêm [Số] sách vào giỏ hàng" | | Pass | 11/15/2015 | |
| **FUNC-QLDSYT-05** | Thêm tất cả khi không có sản phẩm còn hàng | 1. Truy cập /user/wishlist<br>2. Tất cả sản phẩm hết hàng<br>3. Nhấn nút "Thêm tất cả vào giỏ" | Nút bị disabled, hiển thị toast "Không có sách nào còn hàng" | | Pass | 11/15/2015 | |
| **FUNC-QLDSYT-06** | Xóa tất cả sản phẩm | 1. Truy cập /user/wishlist<br>2. Nhấn nút "Xóa tất cả"<br>3. Xác nhận xóa | Hiển thị modal xác nhận, sau khi xác nhận, tất cả sản phẩm bị xóa, hiển thị toast "Đã xóa tất cả sách khỏi danh sách yêu thích", hiển thị thông báo danh sách trống | | Pass | 11/15/2015 | |
| **FUNC-QLDSYT-07** | Hủy xóa tất cả | 1. Truy cập /user/wishlist<br>2. Nhấn nút "Xóa tất cả"<br>3. Hủy trong modal | Modal đóng, không xóa sản phẩm, danh sách vẫn giữ nguyên | | Pass | 11/15/2015 | |
| **FUNC-QLDSYT-08** | Xem chi tiết sản phẩm | 1. Truy cập /user/wishlist<br>2. Nhấn nút "Chi tiết" | Chuyển đến trang /user/products/[id] với thông tin chi tiết sản phẩm | | Pass | 11/15/2015 | |
| **FUNC-QLDSYT-09** | Click vào hình ảnh sản phẩm | 1. Truy cập /user/wishlist<br>2. Click vào hình ảnh | Chuyển đến trang chi tiết sản phẩm | | Pass | 11/15/2015 | |
| **FUNC-QLDSYT-10** | Click vào tên sản phẩm | 1. Truy cập /user/wishlist<br>2. Click vào tên sản phẩm | Chuyển đến trang chi tiết sản phẩm | | Pass | 11/15/2015 | |

---

### Function: Tìm kiếm và lọc sản phẩm yêu thích

#### Check GUI: Tìm kiếm và lọc sản phẩm yêu thích

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-TKLC-01** | Kiểm tra ô tìm kiếm | 1. Truy cập /user/wishlist<br>2. Kiểm tra ô tìm kiếm | Hiển thị input với icon Search bên trái, placeholder "Tìm kiếm trong danh sách yêu thích...", pl-10 | | Pass | 11/15/2015 | |
| **GUI-TKLC-02** | Kiểm tra bộ lọc danh mục | 1. Truy cập /user/wishlist<br>2. Kiểm tra bộ lọc | Hiển thị Select với trigger w-48, các option: "Tất cả", "Kỹ năng sống", "Tâm lý học", "Lịch sử", v.v. | | Pass | 11/15/2015 | |
| **GUI-TKLC-03** | Kiểm tra sắp xếp | 1. Truy cập /user/wishlist<br>2. Kiểm tra sắp xếp | Hiển thị Select với trigger w-48, các option: "Ngày thêm", "Giá", "Tên sách", "Năm xuất bản", "Đánh giá" | | Pass | 11/15/2015 | |
| **GUI-TKLC-04** | Kiểm tra nút đảo ngược thứ tự | 1. Truy cập /user/wishlist<br>2. Kiểm tra nút | Hiển thị nút với icon SortAsc hoặc SortDesc, variant outline size sm, thay đổi icon theo thứ tự | | Pass | 11/15/2015 | |
| **GUI-TKLC-05** | Kiểm tra số lượng kết quả | 1. Truy cập /user/wishlist<br>2. Tìm kiếm/lọc<br>3. Kiểm tra số lượng | Hiển thị "Hiển thị [Số] trong tổng số [Số] sách" với text-sm text-muted-foreground | | Pass | 11/15/2015 | |

---

### Check FUNC: Tìm kiếm và lọc sản phẩm yêu thích

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TKLC-01** | Tìm kiếm theo tên sản phẩm | 1. Truy cập /user/wishlist<br>2. Nhập tên sản phẩm vào ô tìm kiếm | Danh sách được lọc, chỉ hiển thị sản phẩm có tên chứa từ khóa, cập nhật số lượng kết quả | | Pass | 11/15/2015 | |
| **FUNC-TKLC-02** | Tìm kiếm theo tác giả | 1. Truy cập /user/wishlist<br>2. Nhập tên tác giả vào ô tìm kiếm | Danh sách được lọc, chỉ hiển thị sản phẩm có tác giả chứa từ khóa | | Pass | 11/15/2015 | |
| **FUNC-TKLC-03** | Tìm kiếm theo danh mục | 1. Truy cập /user/wishlist<br>2. Nhập tên danh mục vào ô tìm kiếm | Danh sách được lọc, chỉ hiển thị sản phẩm có danh mục chứa từ khóa | | Pass | 11/15/2015 | |
| **FUNC-TKLC-04** | Tìm kiếm không có kết quả | 1. Truy cập /user/wishlist<br>2. Nhập từ khóa không có trong danh sách | Hiển thị thông báo "Không tìm thấy sách", icon Heart, nút "Xóa bộ lọc" | | Pass | 11/15/2015 | |
| **FUNC-TKLC-05** | Lọc theo danh mục | 1. Truy cập /user/wishlist<br>2. Chọn danh mục trong bộ lọc | Danh sách được lọc, chỉ hiển thị sản phẩm thuộc danh mục đã chọn, cập nhật số lượng kết quả | | Pass | 11/15/2015 | |
| **FUNC-TKLC-06** | Lọc - Tất cả | 1. Truy cập /user/wishlist<br>2. Chọn "Tất cả" trong bộ lọc | Hiển thị tất cả sản phẩm không phân biệt danh mục | | Pass | 11/15/2015 | |
| **FUNC-TKLC-07** | Sắp xếp theo Ngày thêm | 1. Truy cập /user/wishlist<br>2. Chọn sắp xếp "Ngày thêm" | Danh sách được sắp xếp theo ngày thêm, mới nhất hoặc cũ nhất tùy thứ tự | | Pass | 11/15/2015 | |
| **FUNC-TKLC-08** | Sắp xếp theo Giá | 1. Truy cập /user/wishlist<br>2. Chọn sắp xếp "Giá" | Danh sách được sắp xếp theo giá, tăng dần hoặc giảm dần tùy thứ tự | | Pass | 11/15/2015 | |
| **FUNC-TKLC-09** | Sắp xếp theo Tên sách | 1. Truy cập /user/wishlist<br>2. Chọn sắp xếp "Tên sách" | Danh sách được sắp xếp theo tên sách A-Z hoặc Z-A tùy thứ tự | | Pass | 11/15/2015 | |
| **FUNC-TKLC-10** | Sắp xếp theo Đánh giá | 1. Truy cập /user/wishlist<br>2. Chọn sắp xếp "Đánh giá" | Danh sách được sắp xếp theo điểm đánh giá, cao nhất hoặc thấp nhất tùy thứ tự | | Pass | 11/15/2015 | |
| **FUNC-TKLC-11** | Đảo ngược thứ tự sắp xếp | 1. Truy cập /user/wishlist<br>2. Chọn sắp xếp<br>3. Nhấn nút đảo ngược | Thứ tự sắp xếp được đảo ngược (tăng dần ↔ giảm dần), icon thay đổi giữa SortAsc và SortDesc | | Pass | 11/15/2015 | |
| **FUNC-TKLC-12** | Kết hợp tìm kiếm và lọc | 1. Truy cập /user/wishlist<br>2. Nhập từ khóa tìm kiếm<br>3. Chọn danh mục | Danh sách được lọc theo cả từ khóa và danh mục, chỉ hiển thị sản phẩm thỏa mãn cả hai điều kiện | | Pass | 11/15/2015 | |
| **FUNC-TKLC-13** | Xóa bộ lọc | 1. Truy cập /user/wishlist<br>2. Áp dụng tìm kiếm/lọc<br>3. Nhấn nút "Xóa bộ lọc" | Tất cả bộ lọc và tìm kiếm được xóa, hiển thị lại toàn bộ danh sách yêu thích | | Pass | 11/15/2015 | |
| **FUNC-TKLC-14** | Tìm kiếm real-time | 1. Truy cập /user/wishlist<br>2. Nhập từ khóa vào ô tìm kiếm | Danh sách được lọc ngay khi nhập, không cần nhấn Enter hoặc nút tìm kiếm | | Pass | 11/15/2015 | |

---

### Function: Thao tác với sản phẩm yêu thích

#### Check GUI: Thao tác với sản phẩm yêu thích

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-TTVSPYT-01** | Kiểm tra nút Chia sẻ | 1. Xem card sản phẩm<br>2. Kiểm tra nút | Hiển thị nút "Chia sẻ" với icon Share2, variant outline size sm, flex-1 | | Pass | 11/15/2015 | |
| **GUI-TTVSPYT-02** | Kiểm tra nút So sánh | 1. Xem card sản phẩm<br>2. Kiểm tra nút | Hiển thị nút "So sánh" với icon Scale, variant outline size sm, flex-1 | | Pass | 11/15/2015 | |
| **GUI-TTVSPYT-03** | Kiểm tra nút Thông báo giá | 1. Xem card sản phẩm<br>2. Kiểm tra nút | Hiển thị nút "Thông báo giá" với icon Bell, variant outline size sm, flex-1 | | Pass | 11/15/2015 | |
| **GUI-TTVSPYT-04** | Kiểm tra modal chia sẻ | 1. Nhấn nút "Chia sẻ"<br>2. Kiểm tra modal | Hiển thị modal với tiêu đề "Chia sẻ sản phẩm", mô tả, input link readonly, các nút chia sẻ Facebook/Twitter/Email | | Pass | 11/15/2015 | |
| **GUI-TTVSPYT-05** | Kiểm tra modal so sánh | 1. Nhấn nút "So sánh"<br>2. Kiểm tra modal | Hiển thị modal với tiêu đề "So sánh sản phẩm", danh sách sản phẩm đang so sánh, nút "Xóa danh sách" và "Đóng" | | Pass | 11/15/2015 | |
| **GUI-TTVSPYT-06** | Kiểm tra modal thông báo giá | 1. Nhấn nút "Thông báo giá"<br>2. Kiểm tra modal | Hiển thị modal với tiêu đề "Đăng ký thông báo giá", input Email, input Mức giá mong muốn, Textarea Ghi chú, nút "Hủy" và "Đăng ký" | | Pass | 11/15/2015 | |

---

### Check FUNC: Thao tác với sản phẩm yêu thích

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TTVSPYT-01** | Xem chi tiết sản phẩm | 1. Truy cập /user/wishlist<br>2. Nhấn nút "Chi tiết" | Chuyển đến trang /user/products/[id] với đầy đủ thông tin sản phẩm | | Pass | 11/15/2015 | |
| **FUNC-TTVSPYT-02** | Chia sẻ sản phẩm | 1. Truy cập /user/wishlist<br>2. Nhấn nút "Chia sẻ" | Mở modal chia sẻ với link sản phẩm readonly, các nút chia sẻ Facebook/Twitter/Email | | Pass | 11/15/2015 | |
| **FUNC-TTVSPYT-03** | Sao chép link chia sẻ | 1. Mở modal chia sẻ<br>2. Click vào input link | Link được sao chép vào clipboard, hiển thị toast "Đã sao chép link" | | Pass | 11/15/2015 | |
| **FUNC-TTVSPYT-04** | Chia sẻ qua Facebook | 1. Mở modal chia sẻ<br>2. Nhấn nút "Facebook" | Mở cửa sổ chia sẻ Facebook với link sản phẩm | | Pass | 11/15/2015 | |
| **FUNC-TTVSPYT-05** | Chia sẻ qua Twitter | 1. Mở modal chia sẻ<br>2. Nhấn nút "Twitter" | Mở cửa sổ chia sẻ Twitter với link sản phẩm | | Pass | 11/15/2015 | |
| **FUNC-TTVSPYT-06** | Chia sẻ qua Email | 1. Mở modal chia sẻ<br>2. Nhấn nút "Email" | Mở ứng dụng email với link sản phẩm trong nội dung | | Pass | 11/15/2015 | |
| **FUNC-TTVSPYT-07** | Đóng modal chia sẻ | 1. Mở modal chia sẻ<br>2. Nhấn nút "Đóng" | Modal đóng, quay lại trang danh sách yêu thích | | Pass | 11/15/2015 | |
| **FUNC-TTVSPYT-08** | Thêm sản phẩm vào so sánh | 1. Truy cập /user/wishlist<br>2. Nhấn nút "So sánh" trên sản phẩm | Sản phẩm được thêm vào danh sách so sánh, mở modal so sánh hiển thị sản phẩm | | Pass | 11/15/2015 | |
| **FUNC-TTVSPYT-09** | Thêm nhiều sản phẩm vào so sánh | 1. Truy cập /user/wishlist<br>2. Nhấn nút "So sánh" trên nhiều sản phẩm | Tất cả sản phẩm được thêm vào danh sách so sánh, modal hiển thị grid các sản phẩm | | Pass | 11/15/2015 | |
| **FUNC-TTVSPYT-10** | Xóa danh sách so sánh | 1. Mở modal so sánh<br>2. Nhấn nút "Xóa danh sách" | Danh sách so sánh được xóa, modal hiển thị "Chưa có sản phẩm nào" | | Pass | 11/15/2015 | |
| **FUNC-TTVSPYT-11** | Đóng modal so sánh | 1. Mở modal so sánh<br>2. Nhấn nút "Đóng" | Modal đóng, danh sách so sánh vẫn được lưu | | Pass | 11/15/2015 | |
| **FUNC-TTVSPYT-12** | Đăng ký thông báo giá | 1. Truy cập /user/wishlist<br>2. Nhấn nút "Thông báo giá"<br>3. Nhập email và mức giá<br>4. Nhấn "Đăng ký" | Đăng ký thành công, modal đóng, hiển thị toast "Đã đăng ký thông báo giá" | | Pass | 11/15/2015 | |
| **FUNC-TTVSPYT-13** | Đăng ký thông báo giá thiếu email | 1. Mở modal thông báo giá<br>2. Không nhập email<br>3. Nhấn "Đăng ký" | Hiển thị thông báo lỗi "Vui lòng nhập email", không đăng ký | | Pass | 11/15/2015 | |
| **FUNC-TTVSPYT-14** | Đăng ký thông báo giá email sai định dạng | 1. Mở modal thông báo giá<br>2. Nhập email sai định dạng<br>3. Nhấn "Đăng ký" | Hiển thị thông báo lỗi "Email không hợp lệ", không đăng ký | | Pass | 11/15/2015 | |
| **FUNC-TTVSPYT-15** | Hủy đăng ký thông báo giá | 1. Mở modal thông báo giá<br>2. Nhấn nút "Hủy" | Modal đóng, không đăng ký thông báo | | Pass | 11/15/2015 | |
| **FUNC-TTVSPYT-16** | Đóng modal bằng click overlay | 1. Mở bất kỳ modal nào<br>2. Click vào overlay | Modal đóng, quay lại trang danh sách yêu thích | | Pass | 11/15/2015 | |

---

### Check VALIDATION: Danh sách sản phẩm yêu thích

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **VALID-DSYT-01** | Thêm sản phẩm khi chưa đăng nhập | 1. Đăng xuất<br>2. Thử thêm sản phẩm vào yêu thích | Hiển thị thông báo yêu cầu đăng nhập, chuyển đến trang đăng nhập | | Pass | 11/15/2015 | |
| **VALID-DSYT-02** | Xóa tất cả không có xác nhận | 1. Truy cập /user/wishlist<br>2. Nhấn nút "Xóa tất cả" | Hiển thị modal xác nhận trước khi xóa, không xóa ngay lập tức | | Pass | 11/15/2015 | |
| **VALID-DSYT-03** | Thêm sản phẩm hết hàng vào giỏ | 1. Truy cập /user/wishlist<br>2. Nhấn nút "Mua" trên sản phẩm hết hàng | Nút bị disabled, không thể thêm vào giỏ hàng | | Pass | 11/15/2015 | |
| **VALID-DSYT-04** | Đăng ký thông báo giá thiếu email | 1. Mở modal thông báo giá<br>2. Để trống email<br>3. Nhấn "Đăng ký" | Hiển thị thông báo lỗi "Vui lòng nhập email", không đăng ký | | Pass | 11/15/2015 | |
| **VALID-DSYT-05** | Đăng ký thông báo giá email sai | 1. Mở modal thông báo giá<br>2. Nhập email sai định dạng<br>3. Nhấn "Đăng ký" | Hiển thị thông báo lỗi "Email không hợp lệ", không đăng ký | | Pass | 11/15/2015 | |
| **VALID-DSYT-06** | Đăng ký thông báo giá giá không hợp lệ | 1. Mở modal thông báo giá<br>2. Nhập giá không phải số<br>3. Nhấn "Đăng ký" | Hiển thị thông báo lỗi "Mức giá không hợp lệ", không đăng ký | | Pass | 11/15/2015 | |
| **VALID-DSYT-07** | Tìm kiếm với từ khóa đặc biệt | 1. Truy cập /user/wishlist<br>2. Nhập từ khóa có ký tự đặc biệt | Hệ thống xử lý an toàn, không gây lỗi, lọc kết quả chính xác | | Pass | 11/15/2015 | |
| **VALID-DSYT-08** | Tìm kiếm với từ khóa rất dài | 1. Truy cập /user/wishlist<br>2. Nhập từ khóa rất dài (>100 ký tự) | Hệ thống xử lý bình thường, không gây lỗi, lọc kết quả nếu có | | Pass | 11/15/2015 | |

