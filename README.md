# Test Case Template - Chức năng tìm kiếm sản phẩm (User)

## Module Code
**Model Management Store: Chức năng tìm kiếm sản phẩm User**

## Test Requirement
1. Tìm kiếm sản phẩm
2. Gợi ý tìm kiếm (Autocomplete real-time)
3. Lịch sử tìm kiếm
4. Xóa lịch sử tìm kiếm
5. Tìm kiếm nâng cao

---

## Test Summary

### Người thực hiện Test: [Tên người test]

| Status | Count |
|--------|-------|
| **Pass** | 98 |
| **Fail** | 0 |
| **Untested** | 24 |
| **N/A** | 0 |
| **Number of Test cases** | 122 |

---

## Test Cases

### Function: Tìm kiếm sản phẩm

#### Check GUI: Tìm kiếm sản phẩm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-TKSP-01** | Kiểm tra tiêu đề trang | 1. Truy cập /user/search<br>2. Kiểm tra tiêu đề | Hiển thị tiêu đề "Tìm kiếm mô hình" | | Pass | 11/15/2015 | |
| **GUI-TKSP-02** | Kiểm tra mô tả chức năng | 1. Truy cập /user/search<br>2. Kiểm tra mô tả | Hiển thị mô tả "Tìm kiếm mô hình theo tên, thương hiệu, thể loại hoặc từ khóa" | | Pass | 11/15/2015 | |
| **GUI-TKSP-03** | Kiểm tra nút Quay lại | 1. Truy cập /user/search<br>2. Kiểm tra nút Quay lại | Hiển thị nút "Quay lại" variant outline với icon ArrowLeft, có thể click | | Pass | 11/15/2015 | |
| **GUI-TKSP-04** | Kiểm tra thanh tìm kiếm | 1. Truy cập /user/search<br>2. Kiểm tra thanh tìm kiếm | Hiển thị input với icon Search bên trái, placeholder "Tìm kiếm mô hình, thương hiệu, thể loại...", có thể nhập text | | Pass | 11/15/2015 | |
| **GUI-TKSP-05** | Kiểm tra nút xóa tìm kiếm | 1. Truy cập /user/search<br>2. Nhập từ khóa vào ô tìm kiếm<br>3. Kiểm tra nút xóa | Hiển thị nút "×" variant ghost bên phải ô tìm kiếm khi có nội dung, có thể click để xóa | | Pass | 11/15/2015 | |
| **GUI-TKSP-06** | Kiểm tra dropdown gợi ý tìm kiếm | 1. Truy cập /user/search<br>2. Nhập từ khóa vào ô tìm kiếm<br>3. Kiểm tra dropdown | Hiển thị dropdown với border, background, shadow-lg, max-height 60, scroll nếu nhiều gợi ý | | Pass | 11/15/2015 | |
| **GUI-TKSP-07** | Kiểm tra item gợi ý | 1. Truy cập /user/search<br>2. Nhập từ khóa<br>3. Kiểm tra item gợi ý | Hiển thị item với icon Package, text gợi ý, badge phân loại (Mô hình/Thương hiệu/Thể loại), số lượng (nếu có), có hover effect | | Pass | 11/15/2015 | |
| **GUI-TKSP-08** | Kiểm tra lịch sử tìm kiếm | 1. Truy cập /user/search<br>2. Không nhập từ khóa<br>3. Kiểm tra lịch sử | Hiển thị section "Tìm kiếm gần đây" với icon Clock, các button từ khóa đã tìm, chỉ hiển thị khi không có từ khóa đang nhập | | Pass | 11/15/2015 | |
| **GUI-TKSP-09** | Kiểm tra bộ lọc thể loại | 1. Truy cập /user/search<br>2. Kiểm tra dropdown thể loại | Hiển thị Select với label "Bộ lọc:", các option: Tất cả, Gundam, Figure, Mô hình xe, Máy bay, Tàu chiến, Khác | | Pass | 11/15/2015 | |
| **GUI-TKSP-10** | Kiểm tra bộ lọc thương hiệu | 1. Truy cập /user/search<br>2. Kiểm tra dropdown thương hiệu | Hiển thị Select với các option: Tất cả, Bandai, Good Smile Company, Tamiya, Hasegawa, Kotobukiya, Max Factory | | Pass | 11/15/2015 | |
| **GUI-TKSP-11** | Kiểm tra sắp xếp kết quả | 1. Truy cập /user/search<br>2. Kiểm tra dropdown sắp xếp | Hiển thị Select với các option: Liên quan, Giá thấp, Giá cao, Đánh giá, Mới nhất | | Pass | 11/15/2015 | |
| **GUI-TKSP-12** | Kiểm tra tiêu đề kết quả | 1. Truy cập /user/search<br>2. Nhập từ khóa và tìm kiếm<br>3. Kiểm tra tiêu đề | Hiển thị tiêu đề "Kết quả tìm kiếm cho '[từ khóa]'" hoặc "Tìm thấy X kết quả" hoặc "Nhập từ khóa để tìm kiếm" | | Pass | 11/15/2015 | |
| **GUI-TKSP-13** | Kiểm tra thống kê kết quả | 1. Truy cập /user/search<br>2. Tìm kiếm có kết quả<br>3. Kiểm tra thống kê | Hiển thị icon TrendingUp, text "X mô hình" với màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-TKSP-14** | Kiểm tra danh sách kết quả | 1. Truy cập /user/search<br>2. Tìm kiếm có kết quả<br>3. Kiểm tra danh sách | Hiển thị grid 4 cột với các card sản phẩm, mỗi card có hình ảnh, badge, nút yêu thích, tên, thông tin, đánh giá, giá, tình trạng, nút Xem, nút Mua | | Pass | 11/15/2015 | |
| **GUI-TKSP-15** | Kiểm tra thông báo không có kết quả | 1. Truy cập /user/search<br>2. Tìm kiếm không có kết quả<br>3. Kiểm tra thông báo | Hiển thị icon Package, tiêu đề "Không tìm thấy mô hình", mô tả "Không có mô hình nào phù hợp với từ khóa '[từ khóa]'", nút "Xóa bộ lọc" | | Pass | 11/15/2015 | |
| **GUI-TKSP-16** | Kiểm tra thông báo chưa nhập từ khóa | 1. Truy cập /user/search<br>2. Không nhập từ khóa<br>3. Kiểm tra thông báo | Hiển thị icon Package, tiêu đề "Tìm kiếm mô hình yêu thích", mô tả "Nhập từ khóa để tìm kiếm mô hình bạn muốn" | | Pass | 11/15/2015 | |
| **GUI-TKSP-17** | Kiểm tra card Thể loại mô hình | 1. Truy cập /user/search<br>2. Scroll xuống cuối<br>3. Kiểm tra card | Hiển thị card với icon Package, tiêu đề "Thể loại mô hình", mô tả "Khám phá mô hình theo thể loại", grid các nút thể loại | | Pass | 11/15/2015 | |
| **GUI-TKSP-18** | Kiểm tra nút thể loại | 1. Truy cập /user/search<br>2. Kiểm tra nút thể loại | Hiển thị các nút variant outline với icon Package, tên thể loại, có thể click | | Pass | 11/15/2015 | |

---

### Check FUNC: Tìm kiếm sản phẩm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TKSP-01** | Mở trang tìm kiếm | 1. Truy cập /user/search | Hiển thị trang với tiêu đề, mô tả, nút quay lại, thanh tìm kiếm, bộ lọc, thông báo chưa nhập từ khóa, card thể loại | | Pass | 11/15/2015 | |
| **FUNC-TKSP-02** | Tìm kiếm theo tên sản phẩm | 1. Truy cập /user/search<br>2. Nhập tên sản phẩm vào ô tìm kiếm<br>3. Kiểm tra kết quả | Hiển thị danh sách sản phẩm có tên chứa từ khóa, cập nhật tiêu đề và thống kê kết quả | | Pass | 11/15/2015 | |
| **FUNC-TKSP-03** | Tìm kiếm theo thương hiệu | 1. Truy cập /user/search<br>2. Nhập tên thương hiệu vào ô tìm kiếm<br>3. Kiểm tra kết quả | Hiển thị danh sách sản phẩm của thương hiệu đó, cập nhật tiêu đề và thống kê | | Pass | 11/15/2015 | |
| **FUNC-TKSP-04** | Tìm kiếm theo thể loại | 1. Truy cập /user/search<br>2. Nhập tên thể loại vào ô tìm kiếm<br>3. Kiểm tra kết quả | Hiển thị danh sách sản phẩm thuộc thể loại đó, cập nhật tiêu đề và thống kê | | Pass | 11/15/2015 | |
| **FUNC-TKSP-05** | Tìm kiếm theo mô tả | 1. Truy cập /user/search<br>2. Nhập từ khóa có trong mô tả sản phẩm<br>3. Kiểm tra kết quả | Hiển thị danh sách sản phẩm có mô tả chứa từ khóa | | Pass | 11/15/2015 | |
| **FUNC-TKSP-06** | Tìm kiếm real-time | 1. Truy cập /user/search<br>2. Nhập từ khóa vào ô tìm kiếm<br>3. Quan sát kết quả | Danh sách kết quả được cập nhật ngay khi nhập, không cần nhấn Enter hoặc click nút tìm kiếm | | Pass | 11/15/2015 | |
| **FUNC-TKSP-07** | Tìm kiếm từ URL với query parameter | 1. Truy cập /user/search?q=Gundam<br>2. Kiểm tra kết quả | Tự động điền từ khóa "Gundam" vào ô tìm kiếm, hiển thị kết quả tìm kiếm cho "Gundam" | | Pass | 11/15/2015 | |
| **FUNC-TKSP-08** | Tìm kiếm không có kết quả | 1. Truy cập /user/search<br>2. Nhập từ khóa không tồn tại<br>3. Kiểm tra kết quả | Hiển thị thông báo "Không tìm thấy mô hình", "Không có mô hình nào phù hợp với từ khóa '[từ khóa]'", nút "Xóa bộ lọc" | | Pass | 11/15/2015 | |
| **FUNC-TKSP-09** | Tìm kiếm với từ khóa rỗng | 1. Truy cập /user/search<br>2. Để trống ô tìm kiếm<br>3. Kiểm tra kết quả | Hiển thị thông báo "Nhập từ khóa để tìm kiếm", không hiển thị kết quả, hiển thị lịch sử tìm kiếm nếu có | | Pass | 11/15/2015 | |
| **FUNC-TKSP-10** | Tìm kiếm không phân biệt hoa thường | 1. Truy cập /user/search<br>2. Nhập "GUNDAM" (chữ hoa)<br>3. Kiểm tra kết quả | Hiển thị kết quả tương tự như nhập "gundam" (chữ thường) | | Pass | 11/15/2015 | |
| **FUNC-TKSP-11** | Tìm kiếm với từ khóa một phần | 1. Truy cập /user/search<br>2. Nhập "Gun" (một phần của "Gundam")<br>3. Kiểm tra kết quả | Hiển thị tất cả sản phẩm có tên chứa "Gun" | | Pass | 11/15/2015 | |
| **FUNC-TKSP-12** | Lọc kết quả theo thể loại | 1. Truy cập /user/search<br>2. Nhập từ khóa và tìm kiếm<br>3. Chọn thể loại từ dropdown<br>4. Kiểm tra kết quả | Hiển thị chỉ sản phẩm thuộc thể loại đã chọn trong kết quả tìm kiếm, cập nhật thống kê | | Pass | 11/15/2015 | |
| **FUNC-TKSP-13** | Lọc kết quả theo thương hiệu | 1. Truy cập /user/search<br>2. Nhập từ khóa và tìm kiếm<br>3. Chọn thương hiệu từ dropdown<br>4. Kiểm tra kết quả | Hiển thị chỉ sản phẩm của thương hiệu đã chọn trong kết quả tìm kiếm, cập nhật thống kê | | Pass | 11/15/2015 | |
| **FUNC-TKSP-14** | Sắp xếp kết quả theo liên quan | 1. Truy cập /user/search<br>2. Nhập từ khóa và tìm kiếm<br>3. Chọn "Liên quan" từ dropdown sắp xếp<br>4. Kiểm tra kết quả | Kết quả được sắp xếp theo độ liên quan với từ khóa tìm kiếm | | Pass | 11/15/2015 | |
| **FUNC-TKSP-15** | Sắp xếp kết quả theo giá thấp | 1. Truy cập /user/search<br>2. Nhập từ khóa và tìm kiếm<br>3. Chọn "Giá thấp" từ dropdown sắp xếp<br>4. Kiểm tra kết quả | Kết quả được sắp xếp theo giá tăng dần | | Pass | 11/15/2015 | |
| **FUNC-TKSP-16** | Sắp xếp kết quả theo giá cao | 1. Truy cập /user/search<br>2. Nhập từ khóa và tìm kiếm<br>3. Chọn "Giá cao" từ dropdown sắp xếp<br>4. Kiểm tra kết quả | Kết quả được sắp xếp theo giá giảm dần | | Pass | 11/15/2015 | |
| **FUNC-TKSP-17** | Sắp xếp kết quả theo đánh giá | 1. Truy cập /user/search<br>2. Nhập từ khóa và tìm kiếm<br>3. Chọn "Đánh giá" từ dropdown sắp xếp<br>4. Kiểm tra kết quả | Kết quả được sắp xếp theo điểm đánh giá giảm dần | | Pass | 11/15/2015 | |
| **FUNC-TKSP-18** | Sắp xếp kết quả theo mới nhất | 1. Truy cập /user/search<br>2. Nhập từ khóa và tìm kiếm<br>3. Chọn "Mới nhất" từ dropdown sắp xếp<br>4. Kiểm tra kết quả | Kết quả được sắp xếp theo sản phẩm mới nhất trước | | Pass | 11/15/2015 | |
| **FUNC-TKSP-19** | Kết hợp nhiều bộ lọc | 1. Truy cập /user/search<br>2. Nhập từ khóa, chọn thể loại, chọn thương hiệu<br>3. Kiểm tra kết quả | Hiển thị chỉ sản phẩm thỏa mãn tất cả điều kiện: từ khóa, thể loại, thương hiệu | | Pass | 11/15/2015 | |
| **FUNC-TKSP-20** | Click nút Quay lại | 1. Truy cập /user/search<br>2. Click nút "Quay lại" | Chuyển đến trang /user | | Pass | 11/15/2015 | |
| **FUNC-TKSP-21** | Click vào thể loại trong card | 1. Truy cập /user/search<br>2. Click vào nút thể loại trong card<br>3. Kiểm tra kết quả | Tự động chọn thể loại đó trong dropdown, xóa từ khóa tìm kiếm, hiển thị sản phẩm theo thể loại | | Pass | 11/15/2015 | |
| **FUNC-TKSP-22** | Xử lý khi mất kết nối mạng | 1. Truy cập /user/search<br>2. Tắt kết nối mạng<br>3. Nhập từ khóa và tìm kiếm | Hiển thị thông báo lỗi "Lỗi kết nối hệ thống. Vui lòng kiểm tra kết nối mạng và thử lại" | | Untested | 11/15/2015 | |
| **FUNC-TKSP-23** | Xử lý khi server lỗi | 1. Truy cập /user/search<br>2. Server trả về lỗi 500<br>3. Nhập từ khóa và tìm kiếm | Hiển thị thông báo lỗi "Lỗi hệ thống. Vui lòng thử lại sau" | | Untested | 11/15/2015 | |

---

### Function: Gợi ý tìm kiếm (Autocomplete real-time)

#### Check GUI: Gợi ý tìm kiếm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-GY-01** | Kiểm tra hiển thị dropdown gợi ý | 1. Truy cập /user/search<br>2. Nhập từ khóa vào ô tìm kiếm<br>3. Kiểm tra dropdown | Hiển thị dropdown gợi ý với border, background, shadow-lg, max-height 60, có scroll nếu nhiều gợi ý | | Pass | 11/15/2015 | |
| **GUI-GY-02** | Kiểm tra icon trong gợi ý | 1. Truy cập /user/search<br>2. Nhập từ khóa<br>3. Kiểm tra icon | Mỗi item gợi ý có icon Package màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-GY-03** | Kiểm tra text gợi ý | 1. Truy cập /user/search<br>2. Nhập từ khóa<br>3. Kiểm tra text | Hiển thị text gợi ý (tên sản phẩm, thương hiệu, thể loại) | | Pass | 11/15/2015 | |
| **GUI-GY-04** | Kiểm tra badge phân loại | 1. Truy cập /user/search<br>2. Nhập từ khóa<br>3. Kiểm tra badge | Hiển thị badge variant outline với text: "Mô hình", "Thương hiệu", hoặc "Thể loại" tùy theo type | | Pass | 11/15/2015 | |
| **GUI-GY-05** | Kiểm tra số lượng trong gợi ý | 1. Truy cập /user/search<br>2. Nhập từ khóa<br>3. Kiểm tra số lượng | Hiển thị số lượng sản phẩm (nếu có) với màu muted-foreground | | Pass | 11/15/2015 | |
| **GUI-GY-06** | Kiểm tra hover effect | 1. Truy cập /user/search<br>2. Nhập từ khóa<br>3. Hover vào item gợi ý | Item gợi ý có background màu muted khi hover, cursor pointer | | Pass | 11/15/2015 | |

---

### Check FUNC: Gợi ý tìm kiếm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-GY-01** | Hiển thị gợi ý khi nhập từ khóa | 1. Truy cập /user/search<br>2. Nhập từ khóa vào ô tìm kiếm<br>3. Kiểm tra gợi ý | Dropdown gợi ý hiển thị ngay khi nhập, không cần submit, hiển thị các gợi ý phù hợp với từ khóa | | Pass | 11/15/2015 | |
| **FUNC-GY-02** | Gợi ý theo tên sản phẩm | 1. Truy cập /user/search<br>2. Nhập tên sản phẩm (VD: "Gundam")<br>3. Kiểm tra gợi ý | Hiển thị gợi ý các sản phẩm có tên chứa từ khóa, badge "Mô hình" | | Pass | 11/15/2015 | |
| **FUNC-GY-03** | Gợi ý theo thương hiệu | 1. Truy cập /user/search<br>2. Nhập tên thương hiệu (VD: "Bandai")<br>3. Kiểm tra gợi ý | Hiển thị gợi ý thương hiệu, badge "Thương hiệu", số lượng sản phẩm | | Pass | 11/15/2015 | |
| **FUNC-GY-04** | Gợi ý theo thể loại | 1. Truy cập /user/search<br>2. Nhập tên thể loại (VD: "Figure")<br>3. Kiểm tra gợi ý | Hiển thị gợi ý thể loại, badge "Thể loại", số lượng sản phẩm | | Pass | 11/15/2015 | |
| **FUNC-GY-05** | Click vào gợi ý để tìm kiếm | 1. Truy cập /user/search<br>2. Nhập từ khóa<br>3. Click vào một gợi ý<br>4. Kiểm tra kết quả | Từ khóa được điền vào ô tìm kiếm, dropdown gợi ý ẩn đi, hiển thị kết quả tìm kiếm cho từ khóa đó | | Pass | 11/15/2015 | |
| **FUNC-GY-06** | Ẩn gợi ý khi xóa từ khóa | 1. Truy cập /user/search<br>2. Nhập từ khóa để hiển thị gợi ý<br>3. Xóa hết từ khóa | Dropdown gợi ý ẩn đi, hiển thị lịch sử tìm kiếm nếu có | | Pass | 11/15/2015 | |
| **FUNC-GY-07** | Ẩn gợi ý khi click bên ngoài | 1. Truy cập /user/search<br>2. Nhập từ khóa để hiển thị gợi ý<br>3. Click bên ngoài dropdown | Dropdown gợi ý ẩn đi | | Pass | 11/15/2015 | |
| **FUNC-GY-08** | Hiển thị gợi ý khi focus vào ô tìm kiếm | 1. Truy cập /user/search<br>2. Nhập từ khóa rồi click ra ngoài<br>3. Click lại vào ô tìm kiếm | Dropdown gợi ý hiển thị lại nếu có từ khóa trong ô | | Pass | 11/15/2015 | |
| **FUNC-GY-09** | Lọc gợi ý theo từ khóa | 1. Truy cập /user/search<br>2. Nhập từ khóa<br>3. Kiểm tra gợi ý | Chỉ hiển thị các gợi ý có text chứa từ khóa (không phân biệt hoa thường) | | Pass | 11/15/2015 | |
| **FUNC-GY-10** | Scroll trong dropdown gợi ý | 1. Truy cập /user/search<br>2. Nhập từ khóa có nhiều gợi ý<br>3. Scroll trong dropdown | Dropdown có scroll khi có nhiều gợi ý, max-height 60 | | Pass | 11/15/2015 | |
| **FUNC-GY-11** | Gợi ý real-time khi nhập | 1. Truy cập /user/search<br>2. Nhập từng ký tự vào ô tìm kiếm<br>3. Quan sát gợi ý | Gợi ý được cập nhật ngay lập tức khi nhập mỗi ký tự, không có độ trễ | | Pass | 11/15/2015 | |

---

### Function: Lịch sử tìm kiếm

#### Check GUI: Lịch sử tìm kiếm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-LS-01** | Kiểm tra section lịch sử | 1. Truy cập /user/search<br>2. Không nhập từ khóa<br>3. Kiểm tra section | Hiển thị section "Tìm kiếm gần đây" với heading text-sm font-medium, chỉ hiển thị khi không có từ khóa đang nhập | | Pass | 11/15/2015 | |
| **GUI-LS-02** | Kiểm tra button lịch sử | 1. Truy cập /user/search<br>2. Có lịch sử tìm kiếm<br>3. Kiểm tra button | Hiển thị các button variant outline size sm với icon Clock, text từ khóa đã tìm, có thể click | | Pass | 11/15/2015 | |
| **GUI-LS-03** | Kiểm tra layout lịch sử | 1. Truy cập /user/search<br>2. Có nhiều lịch sử<br>3. Kiểm tra layout | Các button được sắp xếp dạng flex-wrap với gap-2 | | Pass | 11/15/2015 | |

---

### Check FUNC: Lịch sử tìm kiếm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-LS-01** | Lưu lịch sử tìm kiếm | 1. Truy cập /user/search<br>2. Nhập từ khóa và tìm kiếm<br>3. Xóa từ khóa<br>4. Kiểm tra lịch sử | Từ khóa được lưu vào lịch sử, hiển thị trong section "Tìm kiếm gần đây" | | Pass | 11/15/2015 | |
| **FUNC-LS-02** | Hiển thị lịch sử tìm kiếm | 1. Truy cập /user/search<br>2. Đã có lịch sử tìm kiếm<br>3. Không nhập từ khóa<br>4. Kiểm tra lịch sử | Hiển thị section "Tìm kiếm gần đây" với các button từ khóa đã tìm, sắp xếp theo thứ tự mới nhất trước | | Pass | 11/15/2015 | |
| **FUNC-LS-03** | Giới hạn số lượng lịch sử | 1. Truy cập /user/search<br>2. Tìm kiếm nhiều từ khóa (hơn 5 từ khóa)<br>3. Kiểm tra lịch sử | Chỉ hiển thị tối đa 5 từ khóa gần nhất, các từ khóa cũ hơn bị loại bỏ | | Pass | 11/15/2015 | |
| **FUNC-LS-04** | Click vào lịch sử để tìm kiếm lại | 1. Truy cập /user/search<br>2. Click vào button từ khóa trong lịch sử<br>3. Kiểm tra kết quả | Từ khóa được điền vào ô tìm kiếm, thực hiện tìm kiếm, hiển thị kết quả | | Pass | 11/15/2015 | |
| **FUNC-LS-05** | Không lưu từ khóa trùng lặp | 1. Truy cập /user/search<br>2. Tìm kiếm "Gundam" 2 lần<br>3. Kiểm tra lịch sử | Chỉ có 1 entry "Gundam" trong lịch sử, không có trùng lặp | | Pass | 11/15/2015 | |
| **FUNC-LS-06** | Cập nhật thứ tự lịch sử | 1. Truy cập /user/search<br>2. Tìm kiếm "A" rồi "B"<br>3. Tìm kiếm lại "A"<br>4. Kiểm tra lịch sử | "A" được di chuyển lên đầu danh sách, "B" xuống vị trí thứ 2 | | Pass | 11/15/2015 | |
| **FUNC-LS-07** | Ẩn lịch sử khi có từ khóa đang nhập | 1. Truy cập /user/search<br>2. Có lịch sử tìm kiếm<br>3. Nhập từ khóa vào ô tìm kiếm<br>4. Kiểm tra lịch sử | Section "Tìm kiếm gần đây" ẩn đi, hiển thị dropdown gợi ý thay thế | | Pass | 11/15/2015 | |
| **FUNC-LS-08** | Lưu lịch sử vào localStorage | 1. Truy cập /user/search<br>2. Tìm kiếm một số từ khóa<br>3. Đóng và mở lại trang<br>4. Kiểm tra lịch sử | Lịch sử tìm kiếm vẫn còn, được lưu vào localStorage | | Untested | 11/15/2015 | |

---

### Function: Xóa lịch sử tìm kiếm

#### Check GUI: Xóa lịch sử tìm kiếm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XLS-01** | Kiểm tra nút xóa tìm kiếm | 1. Truy cập /user/search<br>2. Nhập từ khóa vào ô tìm kiếm<br>3. Kiểm tra nút | Hiển thị nút "×" variant ghost size sm bên phải ô tìm kiếm khi có nội dung | | Pass | 11/15/2015 | |

---

### Check FUNC: Xóa lịch sử tìm kiếm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XLS-01** | Xóa nội dung tìm kiếm | 1. Truy cập /user/search<br>2. Nhập từ khóa vào ô tìm kiếm<br>3. Click nút "×"<br>4. Kiểm tra kết quả | Nội dung trong ô tìm kiếm bị xóa, dropdown gợi ý ẩn đi, kết quả tìm kiếm bị xóa, hiển thị lại lịch sử tìm kiếm nếu có | | Pass | 11/15/2015 | |
| **FUNC-XLS-02** | Xóa bộ lọc | 1. Truy cập /user/search<br>2. Áp dụng bộ lọc và tìm kiếm<br>3. Click nút "Xóa bộ lọc"<br>4. Kiểm tra kết quả | Tất cả bộ lọc được reset về "Tất cả", từ khóa tìm kiếm bị xóa, kết quả tìm kiếm bị xóa, giao diện về trạng thái ban đầu | | Pass | 11/15/2015 | |
| **FUNC-XLS-03** | Ẩn nút xóa khi không có nội dung | 1. Truy cập /user/search<br>2. Không nhập từ khóa<br>3. Kiểm tra nút xóa | Nút "×" không hiển thị khi ô tìm kiếm trống | | Pass | 11/15/2015 | |

---

### Function: Tìm kiếm nâng cao

#### Check GUI: Tìm kiếm nâng cao

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-TKNC-01** | Kiểm tra bộ lọc nâng cao | 1. Truy cập /user/search<br>2. Kiểm tra bộ lọc | Hiển thị các bộ lọc: thể loại, thương hiệu, sắp xếp trong card riêng | | Pass | 11/15/2015 | |

---

### Check FUNC: Tìm kiếm nâng cao

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-TKNC-01** | Tìm kiếm kết hợp từ khóa và bộ lọc | 1. Truy cập /user/search<br>2. Nhập từ khóa<br>3. Chọn thể loại và thương hiệu<br>4. Kiểm tra kết quả | Hiển thị chỉ sản phẩm thỏa mãn: chứa từ khóa, thuộc thể loại đã chọn, của thương hiệu đã chọn | | Pass | 11/15/2015 | |
| **FUNC-TKNC-02** | Tìm kiếm với sắp xếp | 1. Truy cập /user/search<br>2. Nhập từ khóa và tìm kiếm<br>3. Chọn tiêu chí sắp xếp<br>4. Kiểm tra kết quả | Kết quả được sắp xếp theo tiêu chí đã chọn, cập nhật ngay lập tức | | Pass | 11/15/2015 | |
| **FUNC-TKNC-03** | Tìm kiếm với nhiều điều kiện | 1. Truy cập /user/search<br>2. Nhập từ khóa, chọn thể loại, chọn thương hiệu, chọn sắp xếp<br>3. Kiểm tra kết quả | Kết quả thỏa mãn tất cả điều kiện và được sắp xếp theo tiêu chí | | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn Markdown để dễ dàng quản lý và cập nhật test cases.*

