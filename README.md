# Test Case Template - Quản lý tài khoản (Admin)

## Module Code
**Giao lộ 19: Họcl6c (Admin)**

## Test Requirement
1. Đăng nhập
2. Đăng ký
3. Đổi mật khẩu
4. Quản lý thông tin cá nhân
5. Khôi phục mật khẩu
6. Đăng xuất

---

## Test Summary

### Người lớp Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 0 |
| **Fail** | 0 |
| **Untested** | 0 |
| **N/A** | 0 |
| **Number of Test cases** | 0 |

---

## Test Cases

### Function: Đăng nhập

#### Check GUI: Đăng nhập

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DN-01** | Kiểm tra hiển thị header | 1. Truy cập /admin/auth/login<br>2. Kiểm tra hiển thị header | Hiển thị header với logo và tiêu đề "Nhà sách - Quản trị viên" | | | | |
| **GUI-DN-02** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/auth/login<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Đăng nhập Admin" | | | | |
| **GUI-DN-03** | Kiểm tra form đăng nhập | 1. Truy cập /admin/auth/login<br>2. Kiểm tra form | Hiển thị form đăng nhập với các trường: Tên đăng nhập, Mật khẩu, nút Đăng nhập, nút Quên mật khẩu | | | | |
| **GUI-DN-04** | Kiểm tra trường Tên đăng nhập | 1. Truy cập /admin/auth/login<br>2. Kiểm tra trường Tên đăng nhập | Hiển thị label "Tên đăng nhập", input type text với placeholder, bắt buộc nhập | | | | |
| **GUI-DN-05** | Kiểm tra trường Mật khẩu | 1. Truy cập /admin/auth/login<br>2. Kiểm tra trường Mật khẩu | Hiển thị label "Mật khẩu", input type password với placeholder, bắt buộc nhập | | | | |
| **GUI-DN-06** | Kiểm tra nút Đăng nhập | 1. Truy cập /admin/auth/login<br>2. Kiểm tra nút Đăng nhập | Hiển thị nút "Đăng nhập" có thể click | | | | |
| **GUI-DN-07** | Kiểm tra nút Quên mật khẩu | 1. Truy cập /admin/auth/login<br>2. Kiểm tra nút Quên mật khẩu | Hiển thị link/nút "Quên mật khẩu" có thể click | | | | |

---

### Check FUNC: Đăng nhập

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DN-01** | Mở trang đăng nhập | 1. Truy cập /admin/auth/login | Hiển thị form đăng nhập với các ô: tên đăng nhập, mật khẩu, nút đăng nhập, nút quên mật khẩu | | | | |
| **FUNC-DN-02** | Đăng nhập thành công | 1. Truy cập /admin/auth/login<br>2. Nhập tên đăng nhập hợp lệ<br>3. Nhập mật khẩu đúng<br>4. Nhấn nút Đăng nhập | Hệ thống xác thực đăng nhập, chuyển đến trang dashboard admin (/admin), lưu phiên đăng nhập và lưu token | | | | |
| **FUNC-DN-03** | Đăng nhập với tên đăng nhập không tồn tại | 1. Truy cập /admin/auth/login<br>2. Nhập tên đăng nhập không tồn tại<br>3. Nhập mật khẩu<br>4. Nhấn Đăng nhập | Hiển thị thông báo lỗi "Tên đăng nhập hoặc mật khẩu không đúng", không chuyển trang | | | | |
| **FUNC-DN-04** | Đăng nhập với mật khẩu sai | 1. Truy cập /admin/auth/login<br>2. Nhập tên đăng nhập hợp lệ<br>3. Nhập mật khẩu sai<br>4. Nhấn Đăng nhập | Hiển thị thông báo lỗi "Tên đăng nhập hoặc mật khẩu không đúng", không chuyển trang | | | | |
| **FUNC-DN-05** | Đăng nhập thiếu tên đăng nhập | 1. Truy cập /admin/auth/login<br>2. Để trống tên đăng nhập<br>3. Nhập mật khẩu<br>4. Nhấn Đăng nhập | Trình duyệt hiển thị cảnh báo "Please fill out this field", form không được gửi | | | | |
| **FUNC-DN-06** | Đăng nhập thiếu mật khẩu | 1. Truy cập /admin/auth/login<br>2. Nhập tên đăng nhập<br>3. Để trống mật khẩu<br>4. Nhấn Đăng nhập | Trình duyệt hiển thị cảnh báo "Please fill out this field", form không được gửi | | | | |
| **FUNC-DN-07** | Nhấn link Quên mật khẩu | 1. Truy cập /admin/auth/login<br>2. Nhấn link "Quên mật khẩu" | Chuyển đến trang /admin/auth/forgot-password | | | | |
| **FUNC-DN-08** | Submit form bằng phím Enter | 1. Truy cập /admin/auth/login<br>2. Nhập đúng thông tin<br>3. Nhấn Enter trong trường mật khẩu | Form được gửi, xử lý đăng nhập như khi nhấn nút | | | | |

---

### Function: Đăng ký

#### Check GUI: Đăng ký

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DK-01** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/auth/register<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Đăng ký Admin" | | | | |
| **GUI-DK-02** | Kiểm tra form đăng ký | 1. Truy cập /admin/auth/register<br>2. Kiểm tra form | Hiển thị form đăng ký với các trường: Họ tên, Email, Mật khẩu, Xác nhận mật khẩu, nút Đăng ký | | | | |

---

### Check FUNC: Đăng ký

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DK-01** | Đăng ký thành công | 1. Truy cập /admin/auth/register<br>2. Nhập đầy đủ thông tin hợp lệ<br>3. Nhấn Đăng ký | Tài khoản được tạo thành công, chuyển đến trang đăng nhập hoặc dashboard | | | | |
| **FUNC-DK-02** | Đăng ký với email đã tồn tại | 1. Truy cập /admin/auth/register<br>2. Nhập email đã tồn tại<br>3. Nhập các thông tin khác<br>4. Nhấn Đăng ký | Hiển thị thông báo lỗi "Email đã tồn tại", không tạo tài khoản | | | | |

---

### Function: Đổi mật khẩu

#### Check GUI: Đổi mật khẩu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DMK-01** | Kiểm tra tiêu đề trang | 1. Đăng nhập Admin<br>2. Truy cập /admin/account<br>3. Click Đổi mật khẩu<br>4. Kiểm tra tiêu đề | Hiển thị tiêu đề "Đổi mật khẩu Admin" | FUNC-DN-02 | | | |
| **GUI-DMK-02** | Kiểm tra form đổi mật khẩu | 1. Đăng nhập Admin<br>2. Truy cập /admin/account<br>3. Click Đổi mật khẩu<br>4. Kiểm tra form | Hiển thị form với các trường: Mật khẩu hiện tại, Mật khẩu mới, Xác nhận mật khẩu mới | FUNC-DN-02 | | | |

---

### Check FUNC: Đổi mật khẩu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DMK-01** | Đổi mật khẩu thành công | 1. Đăng nhập Admin<br>2. Truy cập /admin/account<br>3. Click Đổi mật khẩu<br>4. Nhập mật khẩu hiện tại đúng<br>5. Nhập mật khẩu mới<br>6. Xác nhận mật khẩu mới<br>7. Nhấn Đổi mật khẩu | Mật khẩu được đổi thành công, hiển thị thông báo xác nhận, gửi email thông báo | FUNC-DN-02 | | | |
| **FUNC-DMK-02** | Đổi mật khẩu với mật khẩu hiện tại sai | 1. Đăng nhập Admin<br>2. Truy cập /admin/account<br>3. Click Đổi mật khẩu<br>4. Nhập mật khẩu hiện tại sai<br>5. Nhập mật khẩu mới<br>6. Nhấn Đổi mật khẩu | Hiển thị thông báo lỗi "Mật khẩu hiện tại không đúng", không đổi mật khẩu | FUNC-DN-02 | | | |
| **FUNC-DMK-03** | Đổi mật khẩu với mật khẩu mới không khớp | 1. Đăng nhập Admin<br>2. Truy cập /admin/account<br>3. Click Đổi mật khẩu<br>4. Nhập mật khẩu hiện tại đúng<br>5. Nhập mật khẩu mới<br>6. Xác nhận mật khẩu mới không khớp<br>7. Nhấn Đổi mật khẩu | Hiển thị thông báo lỗi "Mật khẩu xác nhận không khớp", không đổi mật khẩu | FUNC-DN-02 | | | |

---

### Function: Quản lý thông tin cá nhân

#### Check GUI: Quản lý thông tin cá nhân

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-TT-01** | Kiểm tra tiêu đề trang | 1. Đăng nhập Admin<br>2. Truy cập /admin/account<br>3. Kiểm tra tiêu đề | Hiển thị tiêu đề "Thông tin cá nhân Admin" | FUNC-DN-02 | | | |
| **GUI-TT-02** | Kiểm tra hiển thị thông tin hiện tại | 1. Đăng nhập Admin<br>2. Truy cập /admin/account<br>3. Kiểm tra thông tin | Hiển thị thông tin cá nhân: Họ tên, Email, Số điện thoại, Vai trò, Ngày tạo, Trạng thái | FUNC-DN-02 | | | |
| **GUI-TT-03** | Kiểm tra form cập nhật | 1. Đăng nhập Admin<br>2. Truy cập /admin/account<br>3. Kiểm tra form | Hiển thị form với các trường: Họ tên, Email, Số điện thoại, Địa chỉ, Ghi chú | FUNC-DN-02 | | | |

---

### Check FUNC: Quản lý thông tin cá nhân

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TT-01** | Xem thông tin cá nhân | 1. Đăng nhập Admin<br>2. Truy cập /admin/account | Hiển thị đầy đủ thông tin cá nhân của Admin hiện tại | FUNC-DN-02 | | | |
| **FUNC-TT-02** | Cập nhật thông tin cá nhân thành công | 1. Đăng nhập Admin<br>2. Truy cập /admin/account<br>3. Cập nhật thông tin<br>4. Nhấn Lưu | Thông tin được cập nhật thành công, hiển thị thông báo xác nhận, gửi email thông báo (nếu có thay đổi quan trọng) | FUNC-DN-02 | | | |

---

### Function: Khôi phục mật khẩu

#### Check GUI: Khôi phục mật khẩu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-KPMK-01** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/auth/forgot-password<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Khôi phục mật khẩu Admin" | | | | |
| **GUI-KPMK-02** | Kiểm tra form khôi phục | 1. Truy cập /admin/auth/forgot-password<br>2. Kiểm tra form | Hiển thị form với trường Email/Số điện thoại, Phương thức khôi phục (Email/SMS), nút Gửi mã | | | | |

---

### Check FUNC: Khôi phục mật khẩu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-KPMK-01** | Gửi mã khôi phục thành công | 1. Truy cập /admin/auth/forgot-password<br>2. Nhập email đã đăng ký<br>3. Chọn phương thức Email<br>4. Nhấn Gửi mã | Mã khôi phục được gửi thành công qua email, hiển thị thông báo xác nhận, hiển thị form nhập mã | | | | |
| **FUNC-KPMK-02** | Gửi mã với email không tồn tại | 1. Truy cập /admin/auth/forgot-password<br>2. Nhập email không tồn tại<br>3. Nhấn Gửi mã | Hiển thị thông báo lỗi "Email không tồn tại", không gửi mã | | | | |
| **FUNC-KPMK-03** | Đặt lại mật khẩu thành công | 1. Gửi mã khôi phục thành công<br>2. Nhập mã xác thực đúng<br>3. Nhập mật khẩu mới<br>4. Xác nhận mật khẩu mới<br>5. Nhấn Đặt lại mật khẩu | Mật khẩu được đặt lại thành công, hiển thị thông báo, yêu cầu đăng nhập lại | FUNC-KPMK-01 | | | |
| **FUNC-KPMK-04** | Đặt lại mật khẩu với mã sai | 1. Gửi mã khôi phục thành công<br>2. Nhập mã xác thực sai<br>3. Nhập mật khẩu mới<br>4. Nhấn Đặt lại mật khẩu | Hiển thị thông báo lỗi "Mã xác thực không đúng hoặc đã hết hạn", không đặt lại mật khẩu | FUNC-KPMK-01 | | | |

---

### Function: Đăng xuất

#### Check FUNC: Đăng xuất

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DX-01** | Đăng xuất thành công | 1. Đăng nhập Admin<br>2. Click [Đăng xuất] hoặc truy cập /admin/logout<br>3. Xác nhận đăng xuất | Đăng xuất thành công, phiên đăng nhập được kết thúc, chuyển hướng về trang đăng nhập (/admin/auth/login), hiển thị thông báo đăng xuất thành công | FUNC-DN-02 | | | |

---

*Template này được tạo theo chuẩn MDX để dễ dàng quản lý và cập nhật test cases.*

