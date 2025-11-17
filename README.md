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
| **Pass** | 45 |
| **Fail** | 0 |
| **Untested** | 0 |
| **N/A** | 0 |
| **Number of Test cases** | 45 |

---

## Test Cases

### Function: Đăng nhập

#### Check GUI: Đăng nhập

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DN-01** | Kiểm tra icon Shield header | 1. Truy cập /admin/auth/login<br>2. Kiểm tra icon Shield | Hiển thị icon Shield trong vòng tròn (h-12 w-12) với background primary/10, icon màu primary (h-6 w-6), nằm ở header card, căn giữa | | Pass | 11/15/2015 | |
| **GUI-DN-02** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/auth/login<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Đăng nhập Admin" với class text-2xl font-bold, nằm trong CardHeader, căn giữa | | Pass | 11/15/2015 | |
| **GUI-DN-03** | Kiểm tra mô tả chức năng | 1. Truy cập /admin/auth/login<br>2. Kiểm tra mô tả | Hiển thị mô tả "Đăng nhập vào hệ thống quản trị" với class CardDescription, nằm dưới tiêu đề, căn giữa | | Pass | 11/15/2015 | |
| **GUI-DN-04** | Kiểm tra trường Email Admin | 1. Truy cập /admin/auth/login<br>2. Kiểm tra label và input Email | Hiển thị label "Email Admin" với component Label, input type email với id="email", placeholder="admin@modelshop.com", có thuộc tính required, nằm trong div space-y-2 | | Pass | 11/15/2015 | |
| **GUI-DN-05** | Kiểm tra trường Mật khẩu | 1. Truy cập /admin/auth/login<br>2. Kiểm tra label và input Mật khẩu | Hiển thị label "Mật khẩu" với component Label, input type password với id="password", placeholder="Nhập mật khẩu", có thuộc tính required, nằm trong div space-y-2 | | Pass | 11/15/2015 | |
| **GUI-DN-06** | Kiểm tra checkbox Ghi nhớ | 1. Truy cập /admin/auth/login<br>2. Kiểm tra checkbox | Hiển thị checkbox với id="remember", label "Ghi nhớ đăng nhập" với class text-sm, nằm trong flex items-center space-x-2, bên trái | | Pass | 11/15/2015 | |
| **GUI-DN-07** | Kiểm tra link Quên mật khẩu | 1. Truy cập /admin/auth/login<br>2. Kiểm tra link Quên mật khẩu | Hiển thị link "Quên mật khẩu?" với href="/admin/auth/forgot-password", class text-sm text-primary hover:underline, nằm bên phải trong flex justify-between | | Pass | 11/15/2015 | |
| **GUI-DN-08** | Kiểm tra nút Đăng nhập Admin | 1. Truy cập /admin/auth/login<br>2. Kiểm tra nút Đăng nhập | Hiển thị nút "Đăng nhập Admin" type submit, class w-full, nằm trong form space-y-4 | | Pass | 11/15/2015 | |
| **GUI-DN-09** | Kiểm tra separator "Hoặc" | 1. Truy cập /admin/auth/login<br>2. Kiểm tra separator | Hiển thị separator với text "Hoặc" ở giữa, class text-xs uppercase, background bg-background px-2 text-muted-foreground, có đường kẻ ngang | | Pass | 11/15/2015 | |
| **GUI-DN-10** | Kiểm tra link Đăng nhập với tài khoản khách hàng | 1. Truy cập /admin/auth/login<br>2. Kiểm tra link | Hiển thị link "Đăng nhập với tài khoản khách hàng" với icon ArrowLeft (h-4 w-4 mr-1), href="/user/auth/login", class inline-flex items-center text-sm text-primary hover:underline, căn giữa | | Pass | 11/15/2015 | |
| **GUI-DN-11** | Kiểm tra thông báo cảnh báo | 1. Truy cập /admin/auth/login<br>2. Kiểm tra thông báo | Hiển thị text "Chỉ dành cho quản trị viên được ủy quyền" với class text-center text-sm text-muted-foreground, nằm dưới link đăng nhập khách hàng | | Pass | 11/15/2015 | |
| **GUI-DN-12** | Kiểm tra layout trang | 1. Truy cập /admin/auth/login<br>2. Kiểm tra layout tổng thể | Trang có background gradient từ primary/5 đến secondary/5 (bg-gradient-to-br from-primary/5 to-secondary/5), min-h-screen flex items-center justify-center, card container nằm giữa màn hình với w-full max-w-md, padding p-4 | | Pass | 11/15/2015 | |
| **GUI-DN-13** | Kiểm tra card container | 1. Truy cập /admin/auth/login<br>2. Kiểm tra card | Hiển thị card container chứa toàn bộ form đăng nhập, có CardHeader và CardContent, CardContent có class space-y-4 | | Pass | 11/15/2015 | |

---

### Check FUNC: Đăng nhập

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DN-01** | Mở trang đăng nhập | 1. Truy cập /admin/auth/login | Hiển thị form đăng nhập với đầy đủ các thành phần: icon Shield trong vòng tròn, tiêu đề "Đăng nhập Admin", mô tả "Đăng nhập vào hệ thống quản trị", 2 trường nhập (Email Admin với placeholder "admin@modelshop.com", Mật khẩu với placeholder "Nhập mật khẩu"), checkbox ghi nhớ, link quên mật khẩu, nút đăng nhập Admin, separator "Hoặc", link đăng nhập với tài khoản khách hàng, thông báo cảnh báo. Layout có background gradient, card nằm giữa màn hình | | Pass | 11/15/2015 | |
| **FUNC-DN-02** | Đăng nhập thành công với thông tin hợp lệ | 1. Truy cập /admin/auth/login<br>2. Nhập email hợp lệ (VD: admin@modelshop.com)<br>3. Nhập mật khẩu đúng<br>4. Nhấn nút Đăng nhập Admin | Hệ thống xác thực thông tin, hiển thị loading state trên nút (nếu có), sau đó chuyển đến dashboard Admin (/admin), lưu phiên đăng nhập và lưu token vào localStorage/sessionStorage, hiển thị thông báo thành công (toast notification) | | Pass | 11/15/2015 | |
| **FUNC-DN-03** | Đăng nhập với email không tồn tại | 1. Truy cập /admin/auth/login<br>2. Nhập email không tồn tại (VD: notexist@test.com)<br>3. Nhập mật khẩu bất kỳ<br>4. Nhấn Đăng nhập Admin | Hiển thị thông báo lỗi "Tài khoản hoặc mật khẩu không đúng" (toast error), không chuyển trang, vẫn ở trang đăng nhập, các trường input vẫn giữ giá trị đã nhập | | Pass | 11/15/2015 | |
| **FUNC-DN-04** | Đăng nhập với mật khẩu sai | 1. Truy cập /admin/auth/login<br>2. Nhập email hợp lệ<br>3. Nhập mật khẩu sai<br>4. Nhấn Đăng nhập Admin | Hiển thị thông báo lỗi "Tài khoản hoặc mật khẩu không đúng" (toast error), không chuyển trang, vẫn ở trang đăng nhập, các trường input vẫn giữ giá trị đã nhập | | Pass | 11/15/2015 | |
| **FUNC-DN-05** | Đăng nhập thiếu email | 1. Truy cập /admin/auth/login<br>2. Để trống email<br>3. Nhập mật khẩu<br>4. Nhấn Đăng nhập Admin | Trình duyệt hiển thị cảnh báo "Please fill out this field" hoặc validation message "Trường này là bắt buộc" trên trường email, form không được gửi, không có request đến server | | Pass | 11/15/2015 | |
| **FUNC-DN-06** | Đăng nhập thiếu mật khẩu | 1. Truy cập /admin/auth/login<br>2. Nhập email<br>3. Để trống mật khẩu<br>4. Nhấn Đăng nhập Admin | Trình duyệt hiển thị cảnh báo "Please fill out this field" hoặc validation message "Trường này là bắt buộc" trên trường mật khẩu, form không được gửi, không có request đến server | | Pass | 11/15/2015 | |
| **FUNC-DN-07** | Đăng nhập với email sai định dạng | 1. Truy cập /admin/auth/login<br>2. Nhập email không đúng định dạng (VD: "invalid-email")<br>3. Nhập mật khẩu<br>4. Nhấn Đăng nhập Admin | Trình duyệt hiển thị cảnh báo "Please include an '@' in the email address" hoặc validation message "Dữ liệu không hợp lệ" trên trường email, form không được gửi, không có request đến server | | Pass | 11/15/2015 | |
| **FUNC-DN-08** | Chức năng ghi nhớ - Có tích chọn | 1. Truy cập /admin/auth/login<br>2. Tích checkbox "Ghi nhớ đăng nhập"<br>3. Nhập thông tin hợp lệ<br>4. Đăng nhập thành công | Đăng nhập thành công, trình duyệt lưu cookie/session với thời hạn dài hơn (VD: 30 ngày), khi đóng trình duyệt và mở lại vẫn còn đăng nhập, token được lưu vào localStorage | | Pass | 11/15/2015 | |
| **FUNC-DN-09** | Chức năng ghi nhớ - Không tích chọn | 1. Truy cập /admin/auth/login<br>2. Không tích checkbox<br>3. Nhập thông tin hợp lệ<br>4. Đăng nhập thành công | Đăng nhập thành công, trình duyệt lưu cookie/session với thời hạn ngắn hơn (VD: session), khi đóng trình duyệt sẽ đăng xuất, token được lưu vào sessionStorage | | Pass | 11/15/2015 | |
| **FUNC-DN-10** | Nhấn link Quên mật khẩu | 1. Truy cập /admin/auth/login<br>2. Nhấn link "Quên mật khẩu?" | Chuyển đến trang /admin/auth/forgot-password, URL thay đổi, trang mới được load | | Pass | 11/15/2015 | |
| **FUNC-DN-11** | Nhấn link Đăng nhập với tài khoản khách hàng | 1. Truy cập /admin/auth/login<br>2. Nhấn link "Đăng nhập với tài khoản khách hàng" | Chuyển đến trang /user/auth/login, URL thay đổi, trang mới được load | | Pass | 11/15/2015 | |
| **FUNC-DN-12** | Submit form bằng phím Enter | 1. Truy cập /admin/auth/login<br>2. Nhập thông tin hợp lệ<br>3. Nhấn Enter trong trường mật khẩu | Form được gửi, xử lý đăng nhập như khi nhấn nút Đăng nhập Admin, chuyển đến dashboard nếu thành công | | Pass | 11/15/2015 | |

---

### Function: Đăng ký

#### Check GUI: Đăng ký

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DK-01** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/auth/register<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Đăng ký tài khoản Admin" với class text-2xl font-bold, nằm trong CardHeader, căn giữa | | Pass | 11/15/2015 | |
| **GUI-DK-02** | Kiểm tra form đăng ký | 1. Truy cập /admin/auth/register<br>2. Kiểm tra form | Hiển thị form đăng ký với các trường: Họ tên, Email, Mật khẩu, Xác nhận mật khẩu, nút Đăng ký, layout tương tự trang đăng nhập | | Pass | 11/15/2015 | |

---

### Check FUNC: Đăng ký

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DK-01** | Đăng ký thành công | 1. Truy cập /admin/auth/register<br>2. Nhập đầy đủ thông tin hợp lệ (Họ tên, Email, Mật khẩu, Xác nhận mật khẩu)<br>3. Nhấn Đăng ký | Tài khoản được tạo thành công, hiển thị thông báo thành công (toast), chuyển đến trang đăng nhập (/admin/auth/login) hoặc dashboard (/admin) nếu tự động đăng nhập | | Pass | 11/15/2015 | |
| **FUNC-DK-02** | Đăng ký với email đã tồn tại | 1. Truy cập /admin/auth/register<br>2. Nhập email đã tồn tại<br>3. Nhập các thông tin khác hợp lệ<br>4. Nhấn Đăng ký | Hiển thị thông báo lỗi "Email đã tồn tại" (toast error), không tạo tài khoản, vẫn ở trang đăng ký, các trường input vẫn giữ giá trị đã nhập | | Pass | 11/15/2015 | |

---

### Function: Đổi mật khẩu

#### Check GUI: Đổi mật khẩu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-DMK-01** | Kiểm tra dialog đổi mật khẩu | 1. Đăng nhập Admin<br>2. Truy cập /admin/account<br>3. Click nút "Đổi mật khẩu"<br>4. Kiểm tra dialog | Hiển thị Dialog với tiêu đề "Đổi mật khẩu", mô tả "Nhập mật khẩu hiện tại và mật khẩu mới để thay đổi", có các trường: Mật khẩu hiện tại, Mật khẩu mới, Xác nhận mật khẩu mới, mỗi trường có icon Eye/EyeOff để hiển thị/ẩn mật khẩu | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-DMK-02** | Kiểm tra form đổi mật khẩu | 1. Đăng nhập Admin<br>2. Truy cập /admin/account<br>3. Click "Đổi mật khẩu"<br>4. Kiểm tra form | Hiển thị form với các trường: Label "Mật khẩu hiện tại" với Input type password, có nút icon Eye/EyeOff bên phải, Label "Mật khẩu mới" với Input type password, có nút icon Eye/EyeOff, Label "Xác nhận mật khẩu mới" với Input type password, có nút icon Eye/EyeOff, nút "Hủy" và nút "Đổi mật khẩu" | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Đổi mật khẩu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DMK-01** | Đổi mật khẩu thành công | 1. Đăng nhập Admin<br>2. Truy cập /admin/account<br>3. Click nút "Đổi mật khẩu"<br>4. Nhập mật khẩu hiện tại đúng<br>5. Nhập mật khẩu mới (ít nhất 6 ký tự)<br>6. Xác nhận mật khẩu mới khớp<br>7. Nhấn "Đổi mật khẩu" | Mật khẩu được đổi thành công, hiển thị thông báo "Đổi mật khẩu thành công" (toast success), dialog đóng lại, form được reset về trạng thái ban đầu, gửi email thông báo thay đổi mật khẩu (nếu có) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DMK-02** | Đổi mật khẩu với mật khẩu hiện tại sai | 1. Đăng nhập Admin<br>2. Truy cập /admin/account<br>3. Click "Đổi mật khẩu"<br>4. Nhập mật khẩu hiện tại sai<br>5. Nhập mật khẩu mới<br>6. Nhấn "Đổi mật khẩu" | Hiển thị thông báo lỗi "Mật khẩu hiện tại không đúng" (toast error), không đổi mật khẩu, dialog vẫn mở, các trường input vẫn giữ giá trị đã nhập | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DMK-03** | Đổi mật khẩu với mật khẩu mới không khớp | 1. Đăng nhập Admin<br>2. Truy cập /admin/account<br>3. Click "Đổi mật khẩu"<br>4. Nhập mật khẩu hiện tại đúng<br>5. Nhập mật khẩu mới<br>6. Xác nhận mật khẩu mới không khớp<br>7. Nhấn "Đổi mật khẩu" | Hiển thị thông báo lỗi "Mật khẩu xác nhận không khớp" (toast error), không đổi mật khẩu, dialog vẫn mở | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DMK-04** | Đổi mật khẩu với mật khẩu mới quá ngắn | 1. Đăng nhập Admin<br>2. Truy cập /admin/account<br>3. Click "Đổi mật khẩu"<br>4. Nhập mật khẩu hiện tại đúng<br>5. Nhập mật khẩu mới < 6 ký tự<br>6. Nhấn "Đổi mật khẩu" | Hiển thị thông báo lỗi "Mật khẩu mới phải có ít nhất 6 ký tự" (toast error), không đổi mật khẩu | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DMK-05** | Hủy đổi mật khẩu | 1. Đăng nhập Admin<br>2. Truy cập /admin/account<br>3. Click "Đổi mật khẩu"<br>4. Nhập một số thông tin<br>5. Click nút "Hủy" | Dialog đóng lại, form được reset, không có thay đổi nào được lưu | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Quản lý thông tin cá nhân

#### Check GUI: Quản lý thông tin cá nhân

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-TT-01** | Kiểm tra tiêu đề trang | 1. Đăng nhập Admin<br>2. Truy cập /admin/account<br>3. Kiểm tra tiêu đề | Hiển thị tiêu đề "Quản lý tài khoản" với class text-3xl font-bold, mô tả "Quản lý thông tin cá nhân và cài đặt tài khoản" với class text-muted-foreground, nằm trong div flex items-center justify-between | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-TT-02** | Kiểm tra card Thông tin cá nhân | 1. Đăng nhập Admin<br>2. Truy cập /admin/account<br>3. Kiểm tra card | Hiển thị Card với CardHeader có tiêu đề "Thông tin cá nhân" với icon User (h-5 w-5), mô tả "Thông tin cơ bản của tài khoản quản trị", CardContent có Avatar (h-20 w-20) với fallback là chữ cái đầu của tên, Badge hiển thị role "Super Admin" với icon Shield | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-TT-03** | Kiểm tra form cập nhật thông tin | 1. Đăng nhập Admin<br>2. Truy cập /admin/account<br>3. Kiểm tra form | Hiển thị form với các trường: Label "Họ và tên" với Input disabled khi không edit, Label "Email" với Input type email disabled, Label "Số điện thoại" với Input disabled, Label "Địa chỉ" với Input disabled, Label "Ngày sinh" với Input type date disabled. Có nút "Chỉnh sửa" với icon Edit, khi click chuyển thành nút "Hủy" và "Lưu thay đổi" | FUNC-DN-02 | Pass | 11/15/2015 | |
| **GUI-TT-04** | Kiểm tra card Thông tin tài khoản | 1. Đăng nhập Admin<br>2. Truy cập /admin/account<br>3. Kiểm tra card | Hiển thị Card với CardHeader có tiêu đề "Thông tin tài khoản" với icon Shield, mô tả "Thông tin bảo mật và hoạt động tài khoản", CardContent hiển thị: Email đăng nhập với icon Mail, Ngày tạo tài khoản với icon Calendar, Lần đăng nhập cuối với icon Calendar, Separator, nút "Đổi mật khẩu" với icon Key, nút "Đăng xuất" với icon LogOut variant destructive | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Check FUNC: Quản lý thông tin cá nhân

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TT-01** | Xem thông tin cá nhân | 1. Đăng nhập Admin<br>2. Truy cập /admin/account | Hiển thị đầy đủ thông tin cá nhân của Admin hiện tại: Avatar với fallback là chữ cái đầu, Họ tên, Badge role, các trường thông tin (Họ tên, Email, Số điện thoại, Địa chỉ, Ngày sinh) đều disabled, thông tin tài khoản (Email đăng nhập, Ngày tạo, Lần đăng nhập cuối) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TT-02** | Cập nhật thông tin cá nhân thành công | 1. Đăng nhập Admin<br>2. Truy cập /admin/account<br>3. Click nút "Chỉnh sửa"<br>4. Cập nhật thông tin (Họ tên, Số điện thoại, Địa chỉ, Ngày sinh)<br>5. Nhấn "Lưu thay đổi" | Thông tin được cập nhật thành công, hiển thị thông báo "Cập nhật thông tin thành công" (toast success), các trường chuyển về trạng thái disabled, nút chuyển về "Chỉnh sửa", dữ liệu mới được hiển thị, gửi email thông báo (nếu có thay đổi quan trọng) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TT-03** | Cập nhật thông tin thiếu trường bắt buộc | 1. Đăng nhập Admin<br>2. Truy cập /admin/account<br>3. Click "Chỉnh sửa"<br>4. Xóa Họ tên<br>5. Nhấn "Lưu thay đổi" | Hiển thị thông báo lỗi "Họ tên không được để trống" (toast error), không cập nhật, vẫn ở chế độ edit | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-TT-04** | Hủy cập nhật thông tin | 1. Đăng nhập Admin<br>2. Truy cập /admin/account<br>3. Click "Chỉnh sửa"<br>4. Thay đổi một số thông tin<br>5. Click nút "Hủy" | Form được reset về giá trị ban đầu, các trường chuyển về trạng thái disabled, nút chuyển về "Chỉnh sửa", không có thay đổi nào được lưu | FUNC-DN-02 | Pass | 11/15/2015 | |

---

### Function: Khôi phục mật khẩu

#### Check GUI: Khôi phục mật khẩu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-KPMK-01** | Kiểm tra tiêu đề trang | 1. Truy cập /admin/auth/forgot-password<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Khôi phục mật khẩu Admin" với layout tương tự trang đăng nhập, có icon Shield trong header | | Pass | 11/15/2015 | |
| **GUI-KPMK-02** | Kiểm tra form khôi phục | 1. Truy cập /admin/auth/forgot-password<br>2. Kiểm tra form | Hiển thị form với trường Email/Số điện thoại, Phương thức khôi phục (Email/SMS) dạng radio hoặc select, nút "Gửi mã", có link quay lại trang đăng nhập | | Pass | 11/15/2015 | |

---

### Check FUNC: Khôi phục mật khẩu

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-KPMK-01** | Gửi mã khôi phục thành công | 1. Truy cập /admin/auth/forgot-password<br>2. Nhập email đã đăng ký<br>3. Chọn phương thức Email<br>4. Nhấn "Gửi mã" | Mã khôi phục được gửi thành công qua email, hiển thị thông báo xác nhận "Mã khôi phục đã được gửi đến email của bạn" (toast success), hiển thị form nhập mã xác thực với các trường: Mã xác thực, Mật khẩu mới, Xác nhận mật khẩu mới | | Pass | 11/15/2015 | |
| **FUNC-KPMK-02** | Gửi mã với email không tồn tại | 1. Truy cập /admin/auth/forgot-password<br>2. Nhập email không tồn tại<br>3. Nhấn "Gửi mã" | Hiển thị thông báo lỗi "Email không tồn tại" (toast error), không gửi mã, vẫn ở trang khôi phục mật khẩu | | Pass | 11/15/2015 | |
| **FUNC-KPMK-03** | Đặt lại mật khẩu thành công | 1. Gửi mã khôi phục thành công<br>2. Nhập mã xác thực đúng<br>3. Nhập mật khẩu mới (ít nhất 6 ký tự)<br>4. Xác nhận mật khẩu mới khớp<br>5. Nhấn "Đặt lại mật khẩu" | Mật khẩu được đặt lại thành công, hiển thị thông báo "Đặt lại mật khẩu thành công" (toast success), chuyển đến trang đăng nhập (/admin/auth/login), yêu cầu đăng nhập lại với mật khẩu mới | FUNC-KPMK-01 | Pass | 11/15/2015 | |
| **FUNC-KPMK-04** | Đặt lại mật khẩu với mã sai | 1. Gửi mã khôi phục thành công<br>2. Nhập mã xác thực sai<br>3. Nhập mật khẩu mới<br>4. Nhấn "Đặt lại mật khẩu" | Hiển thị thông báo lỗi "Mã xác thực không đúng hoặc đã hết hạn" (toast error), không đặt lại mật khẩu, vẫn ở trang khôi phục, có thể yêu cầu gửi lại mã | FUNC-KPMK-01 | Pass | 11/15/2015 | |

---

### Function: Đăng xuất

#### Check FUNC: Đăng xuất

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-DX-01** | Đăng xuất thành công | 1. Đăng nhập Admin<br>2. Truy cập /admin/account<br>3. Click nút "Đăng xuất"<br>4. Xác nhận đăng xuất trong AlertDialog | Hiển thị AlertDialog với tiêu đề "Xác nhận đăng xuất", mô tả "Bạn có chắc chắn muốn đăng xuất khỏi hệ thống? Bạn sẽ cần đăng nhập lại để tiếp tục sử dụng", có nút "Hủy" và "Đăng xuất". Sau khi xác nhận: đăng xuất thành công, hiển thị thông báo "Đăng xuất thành công" (toast success), phiên đăng nhập được kết thúc, token được xóa khỏi localStorage/sessionStorage, chuyển hướng về trang đăng nhập (/admin/auth/login) | FUNC-DN-02 | Pass | 11/15/2015 | |
| **FUNC-DX-02** | Hủy đăng xuất | 1. Đăng nhập Admin<br>2. Truy cập /admin/account<br>3. Click nút "Đăng xuất"<br>4. Click nút "Hủy" trong AlertDialog | AlertDialog đóng lại, không đăng xuất, vẫn ở trang /admin/account, vẫn đăng nhập | FUNC-DN-02 | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn MDX để dễ dàng quản lý và cập nhật test cases.*
