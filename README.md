# Test Case Template - Khuyến mãi (User)

## Module Code
**USER-009: Khuyến mãi (User)**

## Test Requirement
1. Hiển thị các mã giảm giá
2. Xem chi tiết mã giảm giá
3. Chức năng xếp hạng người dùng
4. Xem xếp hạng hiện tại
5. Mã giảm cho riêng từng sản phẩm

---

## Test Summary

### Người thực hiện Test: Tester

| Status | Count |
|--------|-------|
| **Pass** | 68 |
| **Fail** | 0 |
| **Untested** | 0 |
| **N/A** | 0 |
| **Number of Test cases** | 68 |

---

## Test Cases

### Function: Hiển thị các mã giảm giá

#### Check GUI: Hiển thị mã giảm giá

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-HT-01** | Kiểm tra Card khuyến mãi | 1. Truy cập /user/promotions<br>2. Kiểm tra Card | Hiển thị Card với CardHeader có CardTitle "Khuyến mãi & Mã giảm giá", CardDescription "Khám phá các ưu đãi và mã giảm giá hấp dẫn", CardContent | | Pass | 11/15/2015 | |
| **GUI-HT-02** | Kiểm tra Alert quy tắc ưu tiên | 1. Truy cập /user/promotions<br>2. Kiểm tra Alert | Hiển thị Alert className="mb-4" với icon Info (h-4 w-4), AlertDescription có text "Quy tắc ưu tiên: Chỉ có thể áp dụng 1 mã giảm giá cho mỗi đơn hàng. Hệ thống sẽ tự động chọn mã có giá trị cao nhất nếu bạn chọn nhiều mã." | | Pass | 11/15/2015 | |
| **GUI-HT-03** | Kiểm tra grid danh sách mã giảm giá | 1. Truy cập /user/promotions<br>2. Kiểm tra grid | Hiển thị div grid md:grid-cols-2 gap-4 với các Card cho mỗi mã giảm giá | | Pass | 11/15/2015 | |
| **GUI-HT-04** | Kiểm tra Card mã giảm giá | 1. Truy cập /user/promotions<br>2. Kiểm tra Card | Hiển thị Card với className={`border-dashed ${isSelected ? "border-primary bg-primary/5" : ""}`}, CardContent p-4 | | Pass | 11/15/2015 | |
| **GUI-HT-05** | Kiểm tra thông tin mã giảm giá | 1. Truy cập /user/promotions<br>2. Kiểm tra thông tin | Hiển thị div flex items-center justify-between mb-3 với div chứa: div flex items-center gap-2 mb-1 có span text-lg font-semibold "{p.code}", Badge "{p.type}", Badge variant="secondary" "Còn hiệu lực", Badge className="bg-green-500" "Đã chọn" (nếu isSelected), div text-sm text-muted-foreground "Giảm {p.value} • ĐH tối thiểu {p.min}", div text-xs text-muted-foreground mt-1 "Giá trị ước tính: {discountAmount.toLocaleString()} VNĐ" | | Pass | 11/15/2015 | |
| **GUI-HT-06** | Kiểm tra nút Chi tiết | 1. Truy cập /user/promotions<br>2. Kiểm tra nút | Hiển thị Button asChild variant="outline" size="sm" với Link href={`/user/promotions/${p.code}`} text "Chi tiết" | | Pass | 11/15/2015 | |
| **GUI-HT-07** | Kiểm tra nút Sao chép mã | 1. Truy cập /user/promotions<br>2. Kiểm tra nút | Hiển thị Button variant="outline" size="sm" với text "Sao chép mã", onClick={copyCode} | | Pass | 11/15/2015 | |
| **GUI-HT-08** | Kiểm tra nút Sử dụng ngay | 1. Truy cập /user/promotions<br>2. Kiểm tra nút | Hiển thị Button size="sm" variant={isSelected ? "default" : "outline"} với text "{isSelected ? 'Đã chọn' : 'Sử dụng ngay'}", onClick={() => handleSelectCode(p.code)} | | Pass | 11/15/2015 | |
| **GUI-HT-09** | Kiểm tra Alert mã đã chọn | 1. Truy cập /user/promotions<br>2. Chọn mã<br>3. Kiểm tra Alert | Hiển thị Alert className="mt-4" với icon AlertCircle (h-4 w-4), AlertDescription có text "Mã đã chọn: {selectedCodes[0]} - Giảm {calculateDiscount().toLocaleString()} VNĐ", text-xs "Bạn có thể thay đổi mã khác, hệ thống sẽ tự động áp dụng mã có giá trị cao nhất." | | Pass | 11/15/2015 | |

#### Check FUNC: Hiển thị mã giảm giá

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-HT-01** | Mở trang khuyến mãi | 1. Truy cập /user/promotions | Hiển thị trang với Card khuyến mãi, Alert quy tắc ưu tiên, grid danh sách mã giảm giá, mỗi mã hiển thị trong Card riêng | | Pass | 11/15/2015 | |
| **FUNC-HT-02** | Hiển thị danh sách mã giảm giá | 1. Truy cập /user/promotions<br>2. Kiểm tra danh sách | Tất cả mã giảm giá đang có sẵn được hiển thị với đầy đủ thông tin: tên mã, loại (Phần trăm/Cố định), mức giảm, điều kiện tối thiểu, giá trị ước tính | | Pass | 11/15/2015 | |
| **FUNC-HT-03** | Chọn mã giảm giá | 1. Truy cập /user/promotions<br>2. Nhấn nút "Sử dụng ngay" trên mã<br>3. Kiểm tra | Hiển thị toast.success "Đã chọn mã {code}", selectedCodes được cập nhật, Card có className border-primary bg-primary/5, Badge "Đã chọn" hiển thị, nút hiển thị "Đã chọn", Alert mã đã chọn hiển thị | | Pass | 11/15/2015 | |
| **FUNC-HT-04** | Bỏ chọn mã giảm giá | 1. Truy cập /user/promotions<br>2. Đã chọn mã<br>3. Nhấn nút "Đã chọn" | Hiển thị toast.info "Đã bỏ chọn mã {code}", selectedCodes được xóa mã đó, Card không còn className border-primary bg-primary/5, Badge "Đã chọn" ẩn, nút hiển thị "Sử dụng ngay", Alert mã đã chọn ẩn | | Pass | 11/15/2015 | |
| **FUNC-HT-05** | Chọn mã thứ 2 khi đã chọn mã thứ 1 - Mã mới có giá trị cao hơn | 1. Truy cập /user/promotions<br>2. Chọn mã A<br>3. Chọn mã B (giá trị cao hơn) | Hiển thị toast.success "Đã chọn mã {codeB} (giá trị cao hơn: {value})", selectedCodes chỉ chứa mã B, mã A bị bỏ chọn, Alert cập nhật với mã B | | Pass | 11/15/2015 | |
| **FUNC-HT-06** | Chọn mã thứ 2 khi đã chọn mã thứ 1 - Mã mới có giá trị thấp hơn | 1. Truy cập /user/promotions<br>2. Chọn mã A (giá trị cao)<br>3. Chọn mã B (giá trị thấp) | Hiển thị toast.warning "Mã {codeB} có giá trị thấp hơn mã đã chọn. Chỉ có thể áp dụng 1 mã giảm giá.", selectedCodes vẫn chứa mã A, mã B không được chọn | | Pass | 11/15/2015 | |
| **FUNC-HT-07** | Tính toán giá trị ước tính - Phần trăm | 1. Truy cập /user/promotions<br>2. Mã giảm giá loại "Phần trăm"<br>3. Kiểm tra | Giá trị ước tính = (orderTotal * discountValue / 100), hiển thị với toLocaleString() VNĐ | | Pass | 11/15/2015 | |
| **FUNC-HT-08** | Tính toán giá trị ước tính - Cố định | 1. Truy cập /user/promotions<br>2. Mã giảm giá loại "Cố định"<br>3. Kiểm tra | Giá trị ước tính = discountValue, hiển thị với toLocaleString() VNĐ | | Pass | 11/15/2015 | |
| **FUNC-HT-09** | Sao chép mã giảm giá | 1. Truy cập /user/promotions<br>2. Nhấn nút "Sao chép mã" | Mã được sao chép vào clipboard, hiển thị toast.success "Đã sao chép mã {code}" | | Pass | 11/15/2015 | |
| **FUNC-HT-10** | Nhấn nút Chi tiết | 1. Truy cập /user/promotions<br>2. Nhấn nút "Chi tiết" | Chuyển đến trang /user/promotions/{code} | | Pass | 11/15/2015 | |
| **FUNC-HT-11** | Tính toán giá trị ước tính khi orderTotal thay đổi | 1. Truy cập /user/promotions<br>2. orderTotal thay đổi<br>3. Kiểm tra | Giá trị ước tính được tính lại cho mã loại "Phần trăm", hiển thị được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-HT-12** | Hiển thị Badge trạng thái | 1. Truy cập /user/promotions<br>2. Kiểm tra Badge | Mỗi mã hiển thị Badge variant="secondary" "Còn hiệu lực", nếu mã đã chọn thì hiển thị thêm Badge className="bg-green-500" "Đã chọn" | | Pass | 11/15/2015 | |
| **FUNC-HT-13** | Hiển thị Alert mã đã chọn | 1. Truy cập /user/promotions<br>2. Chọn mã<br>3. Kiểm tra Alert | Hiển thị Alert với thông tin: "Mã đã chọn: {selectedCodes[0]} - Giảm {calculateDiscount().toLocaleString()} VNĐ", text-xs giải thích về quy tắc ưu tiên | | Pass | 11/15/2015 | |
| **FUNC-HT-14** | Tính toán calculateDiscount | 1. Truy cập /user/promotions<br>2. Chọn mã<br>3. Kiểm tra | calculateDiscount() trả về giá trị giảm đúng: nếu loại "Phần trăm" thì (orderTotal * discountValue / 100), nếu loại "Cố định" thì discountValue | | Pass | 11/15/2015 | |

### Function: Xem chi tiết mã giảm giá

#### Check FUNC: Xem chi tiết mã giảm giá

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-CT-01** | Mở trang chi tiết mã giảm giá | 1. Truy cập /user/promotions/{code} | Hiển thị trang với tiêu đề "Mã giảm giá {code}", thông tin mã, mô tả chi tiết, điều kiện áp dụng, thời gian hiệu lực, số lượng, sản phẩm áp dụng, nút "Sử dụng mã này", nút "Sao chép mã" | | Pass | 11/15/2015 | |
| **FUNC-CT-02** | Hiển thị thông tin mã đầy đủ | 1. Truy cập /user/promotions/{code}<br>2. Kiểm tra | Tất cả thông tin mã được hiển thị: mã code, mức giảm, loại giảm giá, điều kiện áp dụng, thời gian hiệu lực, số lượng, sản phẩm áp dụng | | Pass | 11/15/2015 | |
| **FUNC-CT-03** | Kiểm tra điều kiện áp dụng | 1. Truy cập /user/promotions/{code}<br>2. Kiểm tra | Hệ thống kiểm tra và hiển thị điều kiện áp dụng: giá trị đơn hàng tối thiểu, loại sản phẩm, lịch sử sử dụng, chỉ hiển thị nút "Sử dụng mã này" nếu mã có thể áp dụng | | Pass | 11/15/2015 | |
| **FUNC-CT-04** | Sao chép mã từ trang chi tiết | 1. Truy cập /user/promotions/{code}<br>2. Nhấn nút "Sao chép mã" | Mã được sao chép vào clipboard, hiển thị toast.success "Đã sao chép mã {code}" | | Pass | 11/15/2015 | |
| **FUNC-CT-05** | Sử dụng mã từ trang chi tiết | 1. Truy cập /user/promotions/{code}<br>2. Nhấn nút "Sử dụng mã này" | Mã được chọn, chuyển đến trang /user/cart hoặc /user/checkout với mã đã được áp dụng | | Pass | 11/15/2015 | |

### Function: Chức năng xếp hạng người dùng

#### Check GUI: Xếp hạng người dùng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-XH-01** | Kiểm tra tiêu đề trang | 1. Truy cập /user/account/rank<br>2. Kiểm tra tiêu đề | Hiển thị h1 "Điểm tích lũy và hạng thành viên" (text-2xl font-bold), p "Theo dõi hạng hiện tại, tổng chi tiêu và ưu đãi" (text-muted-foreground) | | Pass | 11/15/2015 | |
| **GUI-XH-02** | Kiểm tra Card thông tin hạng | 1. Truy cập /user/account/rank<br>2. Kiểm tra Card | Hiển thị Card với CardHeader có div flex items-center justify-between, CardTitle className="flex items-center gap-2" với icon Crown (h-5 w-5 text-yellow-500) và text "Thông tin hạng", CardDescription "Hạng hiện tại, điểm và chi tiêu", Badge variant="secondary" "ID: user_001", CardContent grid md:grid-cols-2 gap-4 text-sm | | Pass | 11/15/2015 | |
| **GUI-XH-03** | Kiểm tra thông tin hạng hiện tại | 1. Truy cập /user/account/rank<br>2. Kiểm tra | Hiển thị div space-y-2 với: div flex items-center gap-2 "Hạng hiện tại:" và Badge "{currentRank}", div "Điểm tích lũy: {currentPoints.toLocaleString('vi-VN')} điểm", div "Tổng chi tiêu: {totalSpent.toLocaleString('vi-VN')} VNĐ", div "Phần trăm giảm giá: {discountPercent}%" | | Pass | 11/15/2015 | |
| **GUI-XH-04** | Kiểm tra tiến độ hạng tiếp theo | 1. Truy cập /user/account/rank<br>2. Kiểm tra | Hiển thị div space-y-2 với: div "Tiến độ hạng tiếp theo", Progress value={progressValue}, div text-muted-foreground "{currentPoints}/{nextRankTarget} điểm", div text-xs text-muted-foreground "Quy tắc nâng hạng có thể dựa trên điểm hoặc tổng chi tiêu" | | Pass | 11/15/2015 | |
| **GUI-XH-05** | Kiểm tra Card quyền lợi hạng | 1. Truy cập /user/account/rank<br>2. Kiểm tra Card | Hiển thị Card với CardHeader có CardTitle "Quyền lợi hạng", CardDescription "Giảm giá và ưu đãi theo hạng", CardContent grid md:grid-cols-4 gap-3 text-sm | | Pass | 11/15/2015 | |
| **GUI-XH-06** | Kiểm tra danh sách quyền lợi | 1. Truy cập /user/account/rank<br>2. Kiểm tra | Hiển thị div p-3 rounded-lg border cho mỗi hạng với div font-medium mb-1 "{b.name}", div text-muted-foreground "Giảm {b.discount}" | | Pass | 11/15/2015 | |
| **GUI-XH-07** | Kiểm tra Card lịch sử tích điểm | 1. Truy cập /user/account/rank<br>2. Kiểm tra Card | Hiển thị Card với CardHeader có CardTitle "Lịch sử tích điểm", CardDescription "Ngày, Mô tả, Điểm tích, Điểm sử dụng, Số dư", CardContent | | Pass | 11/15/2015 | |
| **GUI-XH-08** | Kiểm tra Table lịch sử | 1. Truy cập /user/account/rank<br>2. Kiểm tra Table | Hiển thị Table với TableHeader có TableRow chứa TableHead: "Ngày", "Mô tả", "Điểm tích" (text-right), "Điểm sử dụng" (text-right), "Số dư" (text-right) | | Pass | 11/15/2015 | |
| **GUI-XH-09** | Kiểm tra Table row lịch sử | 1. Truy cập /user/account/rank<br>2. Kiểm tra Table | Hiển thị TableBody với TableRow cho mỗi history item, có TableCell: Ngày (toLocaleDateString("vi-VN")), Mô tả, Điểm tích (text-right, hiển thị "+{pointsEarned}" hoặc "-"), Điểm sử dụng (text-right, hiển thị "-{pointsUsed}" hoặc "-"), Số dư (text-right) | | Pass | 11/15/2015 | |
| **GUI-XH-10** | Kiểm tra nút Xem lịch sử giao dịch | 1. Truy cập /user/account/rank<br>2. Kiểm tra nút | Hiển thị Button asChild variant="outline" size="sm" với Link href="/user/account/orders" text "Xem lịch sử giao dịch" | | Pass | 11/15/2015 | |

#### Check FUNC: Xếp hạng người dùng

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XH-01** | Mở trang xếp hạng | 1. Truy cập /user/account/rank | Hiển thị trang với tiêu đề, Card thông tin hạng, Card quyền lợi hạng, Card lịch sử tích điểm | | Pass | 11/15/2015 | |
| **FUNC-XH-02** | Hiển thị hạng hiện tại | 1. Truy cập /user/account/rank<br>2. Kiểm tra | Hiển thị Badge với tên hạng hiện tại (Bronze, Silver, Gold, Kim cương, VIP), màu sắc và icon tương ứng | | Pass | 11/15/2015 | |
| **FUNC-XH-03** | Hiển thị điểm tích lũy | 1. Truy cập /user/account/rank<br>2. Kiểm tra | Hiển thị số điểm tích lũy hiện tại với toLocaleString("vi-VN") | | Pass | 11/15/2015 | |
| **FUNC-XH-04** | Hiển thị tổng chi tiêu | 1. Truy cập /user/account/rank<br>2. Kiểm tra | Hiển thị tổng số tiền đã chi tiêu với toLocaleString("vi-VN") VNĐ | | Pass | 11/15/2015 | |
| **FUNC-XH-05** | Hiển thị phần trăm giảm giá | 1. Truy cập /user/account/rank<br>2. Kiểm tra | Hiển thị phần trăm giảm giá được hưởng dựa trên hạng hiện tại | | Pass | 11/15/2015 | |
| **FUNC-XH-06** | Tính toán tiến độ hạng tiếp theo | 1. Truy cập /user/account/rank<br>2. Kiểm tra | progressValue = Math.min(100, Math.round((currentPoints / nextRankTarget) * 100)), Progress hiển thị với value={progressValue}, hiển thị "{currentPoints}/{nextRankTarget} điểm" | | Pass | 11/15/2015 | |
| **FUNC-XH-07** | Hiển thị quyền lợi các hạng | 1. Truy cập /user/account/rank<br>2. Kiểm tra | Hiển thị danh sách các hạng: Bronze (0%), Silver (3%), Gold (5%), Kim cương (8%), mỗi hạng hiển thị tên và mức giảm giá | | Pass | 11/15/2015 | |
| **FUNC-XH-08** | Hiển thị lịch sử tích điểm | 1. Truy cập /user/account/rank<br>2. Kiểm tra | Table hiển thị lịch sử các giao dịch tích điểm: Ngày, Mô tả, Điểm tích (nếu có), Điểm sử dụng (nếu có), Số dư, được sắp xếp theo thời gian (mới nhất trước) | | Pass | 11/15/2015 | |
| **FUNC-XH-09** | Tính toán rank dựa trên tổng chi tiêu | 1. Truy cập /user/account/rank<br>2. Tổng chi tiêu thay đổi<br>3. Kiểm tra | Hệ thống tự động tính toán và cập nhật rank dựa trên tổng chi tiêu và điều kiện do Admin thiết lập, rank được cập nhật khi đủ điều kiện | | Pass | 11/15/2015 | |
| **FUNC-XH-10** | Cập nhật điểm tích lũy sau đơn hàng | 1. Đặt đơn hàng thành công<br>2. Truy cập /user/account/rank<br>3. Kiểm tra | Điểm tích lũy được cập nhật, lịch sử tích điểm có thêm entry mới, số dư được cập nhật | | Pass | 11/15/2015 | |
| **FUNC-XH-11** | Thông báo lên rank | 1. Đủ điều kiện lên rank mới<br>2. Kiểm tra | Hiển thị toast.success hoặc notification "Chúc mừng! Bạn đã lên hạng {newRank}", rank được cập nhật, đặc quyền mới được áp dụng | | Pass | 11/15/2015 | |
| **FUNC-XH-12** | Nhấn nút Xem lịch sử giao dịch | 1. Truy cập /user/account/rank<br>2. Nhấn nút | Chuyển đến trang /user/account/orders | | Pass | 11/15/2015 | |
| **FUNC-XH-13** | Hiển thị điều kiện rank tiếp theo | 1. Truy cập /user/account/rank<br>2. Kiểm tra | Hiển thị thông tin điều kiện để lên rank tiếp theo: cần chi tiêu thêm bao nhiêu hoặc cần tích lũy thêm bao nhiêu điểm | | Pass | 11/15/2015 | |
| **FUNC-XH-14** | Hiển thị đặc quyền rank hiện tại | 1. Truy cập /user/account/rank<br>2. Kiểm tra | Hiển thị các đặc quyền đang được hưởng: mức giảm giá, miễn phí ship (nếu có), ưu tiên hỗ trợ (nếu có) | | Pass | 11/15/2015 | |

### Function: Xem xếp hạng hiện tại

#### Check FUNC: Xem xếp hạng hiện tại

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-XH-HT-01** | Hiển thị thông tin xếp hạng đầy đủ | 1. Truy cập /user/account/rank<br>2. Kiểm tra | Tất cả thông tin xếp hạng được hiển thị: rank hiện tại, điểm tích lũy, tổng chi tiêu, phần trăm giảm giá, tiến độ rank tiếp theo, quyền lợi các hạng, lịch sử tích điểm | | Pass | 11/15/2015 | |
| **FUNC-XH-HT-02** | Thống kê chi tiêu theo thời gian | 1. Truy cập /user/account/rank<br>2. Kiểm tra | Hiển thị thống kê: chi tiêu tháng này, chi tiêu năm nay, tổng chi tiêu, số đơn hàng (nếu có) | | Pass | 11/15/2015 | |
| **FUNC-XH-HT-03** | Cập nhật thông tin real-time | 1. Truy cập /user/account/rank<br>2. Có thay đổi<br>3. Kiểm tra | Thông tin xếp hạng và thống kê được cập nhật tự động khi có thay đổi (đặt đơn hàng, tích điểm, sử dụng điểm) | | Pass | 11/15/2015 | |

### Function: Mã giảm cho riêng từng sản phẩm

#### Check GUI: Mã giảm sản phẩm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **GUI-SP-01** | Kiểm tra Badge giảm giá trên sản phẩm | 1. Truy cập /user/products/[id]<br>2. Sản phẩm có mã giảm<br>3. Kiểm tra | Hiển thị Badge variant="destructive" className="text-xs" với text "-{discount}%" hoặc "-{discountValue} VNĐ" trên Card sản phẩm | | Pass | 11/15/2015 | |
| **GUI-SP-02** | Kiểm tra giá sau giảm | 1. Truy cập /user/products/[id]<br>2. Sản phẩm có mã giảm<br>3. Kiểm tra | Hiển thị giá sau giảm (price), giá gốc (originalPrice) với line-through, Badge giảm giá | | Pass | 11/15/2015 | |
| **GUI-SP-03** | Kiểm tra thông báo mã giảm | 1. Truy cập /user/products/[id]<br>2. Sản phẩm có mã giảm<br>3. Kiểm tra | Hiển thị Alert hoặc Info Box với thông tin về mã giảm đặc biệt: tên mã, mức giảm, thời gian hiệu lực | | Pass | 11/15/2015 | |

#### Check FUNC: Mã giảm sản phẩm

| ID | Test Case Description | Test Case Procedure | Expected Output | Inter-test case Dependence | Result | Test date | Note |
|----|----------------------|---------------------|-----------------|---------------------------|--------|-----------|------|
| **FUNC-SP-01** | Hiển thị mã giảm trên sản phẩm | 1. Truy cập /user/products<br>2. Sản phẩm có mã giảm<br>3. Kiểm tra | Badge giảm giá hiển thị trên Card sản phẩm, giá sau giảm được hiển thị, giá gốc có line-through | | Pass | 11/15/2015 | |
| **FUNC-SP-02** | Thông báo mã giảm sản phẩm | 1. Admin tạo mã giảm cho sản phẩm<br>2. User nhận thông báo<br>3. Kiểm tra | Hiển thị notification về mã giảm đặc biệt cho sản phẩm, có link đến trang sản phẩm | | Pass | 11/15/2015 | |
| **FUNC-SP-03** | Áp dụng mã giảm sản phẩm | 1. Truy cập /user/products/[id]<br>2. Sản phẩm có mã giảm<br>3. Thêm vào giỏ hàng<br>4. Kiểm tra | Giá sản phẩm trong giỏ hàng là giá sau giảm, mã giảm được áp dụng tự động | | Pass | 11/15/2015 | |
| **FUNC-SP-04** | Kiểm tra tính khả dụng mã giảm sản phẩm | 1. Truy cập /user/products/[id]<br>2. Mã giảm hết hạn<br>3. Kiểm tra | Badge giảm giá ẩn hoặc hiển thị "Đã hết hạn", giá hiển thị là giá gốc, Alert "Mã giảm giá đã hết hạn" (nếu có) | | Pass | 11/15/2015 | |
| **FUNC-SP-05** | Hiển thị thời gian hiệu lực | 1. Truy cập /user/products/[id]<br>2. Sản phẩm có mã giảm<br>3. Kiểm tra | Hiển thị thông tin thời gian hiệu lực: "Chỉ trong ngày hôm nay", "Còn lại X ngày", "Hết hạn DD/MM/YYYY" | | Pass | 11/15/2015 | |
| **FUNC-SP-06** | Tính toán giá sau giảm - Phần trăm | 1. Truy cập /user/products/[id]<br>2. Mã giảm loại phần trăm<br>3. Kiểm tra | Giá sau giảm = originalPrice * (1 - discount/100), hiển thị đúng | | Pass | 11/15/2015 | |
| **FUNC-SP-07** | Tính toán giá sau giảm - Cố định | 1. Truy cập /user/products/[id]<br>2. Mã giảm loại cố định<br>3. Kiểm tra | Giá sau giảm = originalPrice - discountValue, hiển thị đúng | | Pass | 11/15/2015 | |
| **FUNC-SP-08** | Mã giảm sản phẩm không áp dụng với mã khác | 1. Truy cập /user/products/[id]<br>2. Sản phẩm có mã giảm<br>3. Áp dụng mã giảm khác<br>4. Kiểm tra | Hiển thị thông báo "Mã giảm sản phẩm không thể kết hợp với mã giảm khác", chỉ áp dụng một mã | | Pass | 11/15/2015 | |

---

*Template này được tạo theo chuẩn MDX để dễ dàng quản lý và cập nhật test cases.*

