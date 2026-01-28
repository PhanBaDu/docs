# PROMPT 1: PHÂN TÍCH DATABASE

## Tổng quan Database: LiteCommerceDB

### 1. Loại dự án phù hợp

Database **LiteCommerceDB** được thiết kế cho **Hệ thống Thương mại điện tử (E-commerce)** hoặc **Quản lý bán hàng trực tuyến**.

**Đặc điểm nhận biết:**
- Có quản lý sản phẩm với nhiều thuộc tính và hình ảnh
- Có quy trình đơn hàng từ đặt hàng → xử lý → vận chuyển → hoàn thành
- Có phân quyền người dùng (Employees với RoleNames)
- Có quản lý khách hàng với tài khoản đăng nhập
- Có quản lý vận chuyển (Shippers)

---

### 2. Quy trình nghiệp vụ được hỗ trợ

#### 2.1. Quy trình Quản lý Sản phẩm
- **Nhập hàng từ nhà cung cấp**: Suppliers → Products
- **Phân loại sản phẩm**: Categories → Products
- **Quản lý thông tin chi tiết**: ProductAttributes, ProductPhotos
- **Cập nhật trạng thái bán**: IsSelling flag

#### 2.2. Quy trình Bán hàng trực tuyến
```
Khách hàng đặt hàng (Orders)
    ↓
Nhân viên xác nhận (Employees → AcceptTime)
    ↓
Phân công vận chuyển (Shippers)
    ↓
Giao hàng (ShippedTime)
    ↓
Hoàn thành (FinishedTime)
```

#### 2.3. Quy trình Quản lý Khách hàng
- Đăng ký tài khoản (Customers)
- Quản lý thông tin cá nhân
- Quản lý địa chỉ giao hàng theo tỉnh (Provinces)
- Khóa/mở khóa tài khoản (IsLocked)

#### 2.4. Quy trình Quản lý Nhân sự
- Quản lý thông tin nhân viên (Employees)
- Phân quyền theo vai trò (RoleNames)
- Theo dõi trạng thái làm việc (IsWorking)
- Gán nhân viên xử lý đơn hàng

---

### 3. Vai trò từng nhóm bảng

#### **Nhóm 1: Danh mục cơ bản (Master Data)**

| Bảng | Vai trò | Mục đích |
|------|---------|----------|
| `Categories` | Phân loại sản phẩm | Tổ chức sản phẩm theo danh mục |
| `Suppliers` | Quản lý nhà cung cấp | Theo dõi nguồn hàng |
| `Provinces` | Danh sách tỉnh/thành | Chuẩn hóa địa chỉ |
| `Shippers` | Đơn vị vận chuyển | Quản lý giao hàng |
| `OrderStatus` | Trạng thái đơn hàng | Theo dõi quy trình đơn |

**Đặc điểm:**
- Dữ liệu ít thay đổi
- Được sử dụng làm dữ liệu tham chiếu
- Hỗ trợ dropdown, combobox trong giao diện

---

#### **Nhóm 2: Quản lý Sản phẩm (Product Management)**

| Bảng | Vai trò | Mối quan hệ |
|------|---------|-------------|
| `Products` | Thông tin sản phẩm chính | Liên kết Categories, Suppliers |
| `ProductPhotos` | Hình ảnh sản phẩm | 1 Product - N Photos |
| `ProductAttributes` | Thuộc tính mở rộng | 1 Product - N Attributes |

**Chức năng hỗ trợ:**
- Quản lý catalog sản phẩm
- Hiển thị đa phương tiện (nhiều ảnh)
- Mô tả chi tiết sản phẩm (size, màu sắc, chất liệu...)
- Quản lý giá và đơn vị tính
- Đánh dấu sản phẩm đang/ngừng bán

---

#### **Nhóm 3: Giao dịch Bán hàng (Transaction)**

| Bảng | Vai trò | Dữ liệu lưu trữ |
|------|---------|-----------------|
| `Orders` | Đơn hàng (Header) | Thông tin chung: khách, nhân viên, shipper, thời gian, trạng thái |
| `OrderDetails` | Chi tiết đơn hàng (Lines) | Sản phẩm, số lượng, giá bán |

**Thiết kế:**
- Mô hình Master-Detail (1-N)
- Lưu trữ lịch sử giao dịch
- Theo dõi timeline: OrderTime → AcceptTime → ShippedTime → FinishedTime
- Hỗ trợ tính toán doanh thu, thống kê

---

#### **Nhóm 4: Quản lý Người dùng (User Management)**

| Bảng | Vai trò | Đối tượng |
|------|---------|-----------|
| `Customers` | Khách hàng | Người mua hàng, có tài khoản |
| `Employees` | Nhân viên | Người quản lý, xử lý đơn |

**Tính năng bảo mật:**
- Lưu trữ Email/Password
- Phân quyền (RoleNames cho Employees)
- Quản lý trạng thái (IsLocked, IsWorking)
- Lưu thông tin liên hệ, địa chỉ

---

### 4. Sơ đồ mối quan hệ chính

```
Suppliers ──┐
            ├──→ Products ──┬──→ ProductPhotos
Categories ─┘              └──→ ProductAttributes
                                      ↓
Customers ──→ Orders ──→ OrderDetails ─┘
                ↓
            ┌───┼───┬────────┐
            ↓   ↓   ↓        ↓
      Employees Shippers OrderStatus Provinces
```

---

### 5. Đánh giá Database

#### **Ưu điểm:**

1. **Chuẩn hóa tốt (3NF)**
   - Không có dữ liệu dư thừa
   - Khóa chính/ngoại rõ ràng
   - Dễ bảo trì, mở rộng

2. **Hỗ trợ đầy đủ quy trình E-commerce**
   - Quản lý sản phẩm chi tiết
   - Theo dõi đơn hàng từng bước
   - Phân quyền người dùng

3. **Thiết kế linh hoạt**
   - ProductAttributes: Mở rộng thuộc tính không giới hạn
   - ProductPhotos: Hỗ trợ nhiều ảnh, sắp xếp thứ tự
   - OrderStatus: Dễ tùy chỉnh quy trình

4. **Hỗ trợ báo cáo**
   - Có timestamp chi tiết (OrderTime, AcceptTime, ShippedTime, FinishedTime)
   - Lưu giá bán tại thời điểm (SalePrice trong OrderDetails)

#### **Hạn chế & Đề xuất cải tiến:**

| Vấn đề | Giải pháp đề xuất |
|--------|-------------------|
| Chưa có Giỏ hàng | Thêm bảng `Cart`, `CartItems` |
| Chưa quản lý Thanh toán | Thêm bảng `Payments` (phương thức, trạng thái) |
| Chưa có Đánh giá sản phẩm | Thêm bảng `ProductReviews` (rating, comment) |
| Chưa có Khuyến mãi | Thêm bảng `Promotions`, `Coupons` |
| Chưa quản lý Tồn kho | Thêm trường `StockQuantity` vào `Products` |
| Chưa có Lịch sử giá | Thêm bảng `PriceHistory` |
| Chưa có Wishlist | Thêm bảng `Wishlists` |

#### **Mức độ phù hợp:**

- **Phù hợp cho:** Website bán hàng vừa và nhỏ, cửa hàng trực tuyến
- **Quy mô:** 1,000 - 10,000 sản phẩm, 10,000 - 100,000 đơn hàng/năm
- **Loại hình:** B2C (Business to Customer)

---

### 6. Kết luận

Database **LiteCommerceDB** là một thiết kế **cơ bản nhưng đầy đủ** cho hệ thống quản lý bán hàng trực tuyến. 

**Điểm mạnh:**
- Cấu trúc rõ ràng, dễ hiểu
- Hỗ trợ đầy đủ quy trình bán hàng cơ bản
- Có khả năng mở rộng tốt

**Phù hợp cho:**
- Đồ án môn học
- Dự án startup nhỏ
- Website bán hàng đơn giản

**Cần bổ sung nếu triển khai thực tế:**
- Giỏ hàng
- Thanh toán trực tuyến
- Đánh giá sản phẩm
- Quản lý tồn kho chi tiết
- Khuyến mãi/Voucher

---

**Ngày phân tích:** 28/01/2026  
**Phiên bản Database:** LiteCommerceDB_Update2026
