# SE04_TEST REPORT V2.0

## HEADER SECTION

**Project Name:** Xây dựng hệ thống quản lý đặt hàng sản phẩm mô hình

**Project Code:** SE04

**Document Code:** SE04_Test Report_v2.0

**Creator:** [Tên người tạo]

**Reviewer/Approver:** [Tên người review/phê duyệt]

**Issue Date:** [Ngày phát hành]

**Notes:** [Ghi chú]

---

## TEST CASE SUMMARY TABLE

| No | Module code | Pass | Fail | Untested | N/A | Number of test cases |
|----|-------------|------|------|----------|-----|---------------------|
| **ADMIN MODULES** |
| 1 | Quản lý tài khoản Admin | 0 | 0 | 129 | 0 | 129 |
| 2 | Quản lý đơn hàng Admin | 0 | 0 | 102 | 0 | 102 |
| 3 | Quản lý người dùng Admin | 0 | 0 | 87 | 0 | 87 |
| 4 | Quản lý sản phẩm Admin | 0 | 0 | 83 | 0 | 83 |
| 5 | Quản lý tồn kho Admin | 0 | 0 | 88 | 0 | 88 |
| 6 | Quản lý đánh giá Admin | 0 | 0 | 75 | 0 | 75 |
| 7 | Quản lý hỗ trợ Admin | 0 | 0 | 87 | 0 | 87 |
| 8 | Xử lý phản hồi Admin | 0 | 0 | 80 | 0 | 80 |
| 9 | Xử lý đặt trước Admin | 0 | 0 | 75 | 0 | 75 |
| 10 | Yêu cầu đặt hàng Admin | 0 | 0 | 54 | 0 | 54 |
| 11 | Quản lý bài viết Admin | 0 | 0 | 84 | 0 | 84 |
| 12 | Báo cáo và thống kê Admin | 0 | 0 | 86 | 0 | 86 |
| 13 | Cài đặt hệ thống Admin | 0 | 0 | 77 | 0 | 77 |
| 14 | Bảo mật Admin | 0 | 0 | 43 | 0 | 43 |
| 15 | Thông báo Admin | 0 | 0 | 30 | 0 | 30 |
| **Sub total (Admin)** | | **0** | **0** | **1,174** | **0** | **1,174** |
| **USER MODULES** |
| 16 | Quản lý tài khoản User | 0 | 0 | 123 | 0 | 123 |
| 17 | Hiển thị sản phẩm User | 0 | 0 | 63 | 0 | 63 |
| 18 | Tìm kiếm sản phẩm User | 0 | 0 | 41 | 0 | 41 |
| 19 | Bộ lọc sản phẩm User | 0 | 0 | 39 | 0 | 39 |
| 20 | Quản lý giỏ hàng User | 0 | 0 | 84 | 0 | 84 |
| 21 | Thanh toán đơn hàng User | 0 | 0 | 67 | 0 | 67 |
| 22 | Quản lý đơn hàng User | 0 | 0 | 72 | 0 | 72 |
| 23 | Đánh giá sản phẩm User | 0 | 0 | 58 | 0 | 58 |
| 24 | Hỗ trợ - liên hệ User | 0 | 0 | 70 | 0 | 70 |
| 25 | Khuyến mãi User | 0 | 0 | 52 | 0 | 52 |
| 26 | Danh sách yêu thích User | 0 | 0 | 61 | 0 | 61 |
| 27 | Đặt trước sản phẩm User | 0 | 0 | 73 | 0 | 73 |
| 28 | Yêu cầu đặt hàng User | 0 | 0 | 67 | 0 | 67 |
| 29 | Vận chuyển User | 0 | 0 | 65 | 0 | 65 |
| 30 | Thông báo User | 0 | 0 | 67 | 0 | 67 |
| 31 | Tạo - hiển thị bài viết User | 0 | 0 | 84 | 0 | 84 |
| 32 | Tương tác bài viết User | 0 | 0 | 71 | 0 | 71 |
| 33 | Xem trang cá nhân User | 0 | 0 | 74 | 0 | 74 |
| 34 | Bảo mật User | 0 | 0 | 48 | 0 | 48 |
| 35 | Cài đặt User | 0 | 0 | 58 | 0 | 58 |
| **Sub total (User)** | | **0** | **0** | **1,336** | **0** | **1,336** |
| **GRAND TOTAL** | | **0** | **0** | **2,510** | **0** | **2,510** |

---

## COVERAGE SUMMARY

**Test coverage:** 0.00 %

**Test successful coverage:** 0.00 %

---

## NOTES

- Tất cả test cases hiện tại đang ở trạng thái "Untested" vì chưa được thực hiện test
- Số lượng test cases được tính dựa trên các file test case đã tạo trong thư mục BlackBox_Admin và BlackBox_User
- Test coverage và Test successful coverage sẽ được cập nhật sau khi thực hiện test
- Tổng số test cases: 2,510 cases
  - Admin: 1,174 test cases (15 modules)
  - User: 1,336 test cases (20 modules)

---

## MODULE DETAILS

### ADMIN MODULES

1. **Quản lý tài khoản Admin** (129 test cases)
   - Đăng nhập, Đăng ký, Đổi mật khẩu, Quản lý thông tin cá nhân, Khôi phục mật khẩu, Đăng xuất

2. **Quản lý đơn hàng Admin** (102 test cases)
   - Hiển thị danh sách, Xem chi tiết, Cập nhật, Xóa, Xác nhận, In đơn hàng, Tạo đơn hàng mới

3. **Quản lý người dùng Admin** (87 test cases)
   - Tạo, Hiển thị danh sách, Xem chi tiết, Xóa, Cập nhật người dùng

4. **Quản lý sản phẩm Admin** (83 test cases)
   - Hiển thị danh sách, Xem chi tiết, Thêm, Cập nhật, Xóa sản phẩm

5. **Quản lý tồn kho Admin** (88 test cases)
   - Hiển thị danh sách, Xem chi tiết, Cập nhật, Nhập hàng mới, Cảnh báo, Kiểm kê, Nhập kho

6. **Quản lý đánh giá Admin** (75 test cases)
   - Xem đánh giá, Xem chi tiết, Duyệt, Từ chối, Xóa, Phản hồi đánh giá

7. **Quản lý hỗ trợ Admin** (87 test cases)
   - Hiển thị danh sách, Xem chi tiết, Chat hỗ trợ, Trả lời, Xóa, Export lịch sử, Tìm kiếm, Quản lý SLA

8. **Xử lý phản hồi Admin** (80 test cases)
   - Hiển thị danh sách, Xem chi tiết, Trả lời, Cập nhật trạng thái, Phân loại khiếu nại

9. **Xử lý đặt trước Admin** (75 test cases)
   - Hiển thị danh sách, Xem chi tiết, Xử lý, Cập nhật trạng thái, Thông báo có hàng

10. **Yêu cầu đặt hàng Admin** (54 test cases)
    - Hiển thị danh sách, Xem chi tiết, Xử lý, Cập nhật trạng thái

11. **Quản lý bài viết Admin** (84 test cases)
    - Hiển thị danh sách, Xem chi tiết, Chỉnh sửa, Xóa, Xóa bình luận, Khóa tài khoản, Tìm kiếm và lọc

12. **Báo cáo và thống kê Admin** (86 test cases)
    - Báo cáo doanh thu, Chi phí, Lợi nhuận, Sản phẩm bán chạy, Thống kê khách hàng, Báo cáo tồn kho, Báo cáo tùy chỉnh

13. **Cài đặt hệ thống Admin** (77 test cases)
    - Chính sách giảm giá sản phẩm, Chính sách giảm giá toàn bộ, Cài đặt thanh toán, Thông tin shop

14. **Bảo mật Admin** (43 test cases)
    - Khôi phục mật khẩu, Lịch sử đăng nhập, Xóa phiên đăng nhập, Phát hiện đăng nhập lạ, Auto logout

15. **Thông báo Admin** (30 test cases)
    - Quản lý thông báo

### USER MODULES

1. **Quản lý tài khoản User** (123 test cases)
   - Đăng nhập, Đăng ký, Đổi mật khẩu, Cập nhật thông tin, Quản lý địa chỉ, Quản lý thanh toán, Xem hạng thành viên, Khôi phục mật khẩu

2. **Hiển thị sản phẩm User** (63 test cases)
   - Hiển thị danh sách, Xem chi tiết sản phẩm

3. **Tìm kiếm sản phẩm User** (41 test cases)
   - Tìm kiếm và lọc sản phẩm

4. **Bộ lọc sản phẩm User** (39 test cases)
   - Bộ lọc và phân loại sản phẩm

5. **Quản lý giỏ hàng User** (84 test cases)
   - Thêm sản phẩm, Hiển thị giỏ hàng, Xóa sản phẩm, Cập nhật số lượng, Áp dụng mã giảm giá, Thực hiện thanh toán

6. **Thanh toán đơn hàng User** (67 test cases)
   - Chọn phương thức thanh toán, Thanh toán COD, Thanh toán VNPAY, Xác nhận đơn hàng

7. **Quản lý đơn hàng User** (72 test cases)
   - Xem thông tin, Xem chi tiết, Theo dõi, Hủy đơn hàng, Đánh giá, Đặt lại, Yêu cầu đổi/trả hàng

8. **Đánh giá sản phẩm User** (58 test cases)
   - Để lại đánh giá, Xem đánh giá sản phẩm

9. **Hỗ trợ - liên hệ User** (70 test cases)
   - Gửi yêu cầu hỗ trợ, Chat hỗ trợ, Quản lý yêu cầu, FAQ, Thông tin liên hệ, Export lịch sử, Tìm kiếm trong chat

10. **Khuyến mãi User** (52 test cases)
    - Xem danh sách, Xem chi tiết, Áp dụng mã giảm giá

11. **Danh sách yêu thích User** (61 test cases)
    - Xem danh sách, Thêm vào yêu thích, Xóa khỏi yêu thích

12. **Đặt trước sản phẩm User** (73 test cases)
    - Đặt trước sản phẩm, Xem danh sách, Hủy đặt trước, Xem chi tiết, Quản lý trạng thái

13. **Yêu cầu đặt hàng User** (67 test cases)
    - Gửi yêu cầu, Xem chi tiết yêu cầu

14. **Vận chuyển User** (65 test cases)
    - Chọn phương thức vận chuyển

15. **Thông báo User** (67 test cases)
    - Xem thông báo

16. **Tạo - hiển thị bài viết User** (84 test cases)
    - Tạo bài viết, Hiển thị danh sách, Xem chi tiết, Chỉnh sửa bài viết

17. **Tương tác bài viết User** (71 test cases)
    - Like, Bình luận, Chia sẻ bài viết

18. **Xem trang cá nhân User** (74 test cases)
    - Xem trang cá nhân người lạ

19. **Bảo mật User** (48 test cases)
    - Lịch sử đăng nhập, Quản lý phiên đăng nhập, Phát hiện đăng nhập lạ, Auto logout

20. **Cài đặt User** (58 test cases)
    - Cài đặt tài khoản

---

## TEST EXECUTION STATUS

**Status:** Not Started

**Last Updated:** [Ngày cập nhật]

**Next Steps:**
1. Bắt đầu thực hiện test cho từng module
2. Cập nhật kết quả test vào bảng Test Case Summary
3. Tính toán lại Test coverage và Test successful coverage sau mỗi đợt test
4. Báo cáo các lỗi phát hiện được trong quá trình test

---

**Document Version:** 2.0  
**Last Modified:** [Ngày chỉnh sửa]  
**Prepared by:** [Tên người soạn]  
**Approved by:** [Tên người phê duyệt]

