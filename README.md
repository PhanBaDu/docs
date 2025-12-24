# QUY ĐỊNH INPUT VÀ VALIDATION - HỆ THỐNG QUẢN LÝ

## BẢNG TỔNG QUAN TẤT CẢ CÁC TRƯỜNG

| Tên trường | Kiểu dữ liệu | Độ dài | Bắt buộc | Format/Pattern | Ghi chú |
|------------|--------------|--------|----------|----------------|---------|
| **Mã sinh viên** | Text | 10 ký tự | ✅ Có | SV + 8 chữ số | SV12345678 |
| **Mã giảng viên** | Text | 10 ký tự | ✅ Có | GV + 8 chữ số | GV12345678 |
| **Mã cán bộ** | Text | 10 ký tự | ✅ Có | CB + 8 chữ số | CB12345678 |
| **Mã nhân viên** | Text | 10 ký tự | ✅ Có | NV + 8 chữ số | NV12345678 |
| **Mã khoa/phòng ban** | Text | 8 ký tự | ✅ Có | K + 7 chữ số hoặc PB + 6 chữ số | K1234567, PB123456 |
| **Mã lớp học** | Text | 10 ký tú | ✅ Có | LH + 8 chữ số | LH12345678 |
| **Mã môn học** | Text | 10 ký tự | ✅ Có | MH + 8 chữ số | MH12345678 |
| **Họ và tên** | Text | 50-100 ký tự | ✅ Có | Chữ + khoảng trắng | Chỉ chữ cái |
| **Họ** | Text | 20 ký tự | ✅ Có | Chữ + khoảng trắng | Nguyễn, Trần |
| **Tên đệm** | Text | 30 ký tự | ❌ Không | Chữ + khoảng trắng | Văn, Thị |
| **Tên** | Text | 20 ký tự | ✅ Có | Chữ | An, Bình |
| **Giới tính** | Combobox | N/A | ✅ Có | Nam/Nữ/Khác | - |
| **Ngày sinh** | Date | N/A | ✅ Có | DD/MM/YYYY | 1900 - hiện tại |
| **Ngày vào làm** | Date | N/A | ✅ Có | DD/MM/YYYY | Phải ≥ ngày sinh + 18 năm |
| **Ngày tốt nghiệp** | Date | N/A | ❌ Không | DD/MM/YYYY | - |
| **Số điện thoại** | Number | 10-11 số | ✅ Có | 0XXXXXXXXX | Bắt đầu bằng 0 |
| **Số điện thoại cố định** | Number | 10 số | ❌ Không | 024XXXXXXX, 028XXXXXXX | Mã vùng + 7-8 số |
| **Số fax** | Number | 10 số | ❌ Không | 024XXXXXXX | Tương tự SĐT cố định |
| **Email** | Email | 50 ký tự | ✅ Có | user@domain.ext | - |
| **Email công ty** | Email | 50 ký tự | ❌ Không | user@company.com | Domain cố định |
| **Địa chỉ thường trú** | Text | 200 ký tự | ✅ Có | Đầy đủ | Số nhà, đường, phường, quận, TP |
| **Địa chỉ tạm trú** | Text | 200 ký tự | ❌ Không | Đầy đủ | Có thể giống thường trú |
| **Địa chỉ liên hệ** | Text | 200 ký tự | ❌ Không | Đầy đủ | - |
| **Tỉnh/Thành phố** | Combobox | N/A | ✅ Có | Danh sách 63 tỉnh | - |
| **Quận/Huyện** | Combobox | N/A | ✅ Có | Theo tỉnh | - |
| **Phường/Xã** | Combobox | N/A | ✅ Có | Theo quận | - |
| **Mã bưu điện** | Number | 6 số | ❌ Không | XXXXXX | 100000 - 999999 |
| **Số CMND/CCCD** | Number | 9-12 số | ✅ Có | 9 số (CMND) hoặc 12 số (CCCD) | - |
| **Ngày cấp CMND/CCCD** | Date | N/A | ✅ Có | DD/MM/YYYY | ≥ ngày sinh + 14 năm |
| **Nơi cấp** | Text | 100 ký tự | ✅ Có | - | Công an TP.HCM |
| **Số hộ chiếu** | Text | 8-9 ký tự | ❌ Không | Chữ + số | A12345678 |
| **Ngày cấp hộ chiếu** | Date | N/A | ❌ Không | DD/MM/YYYY | - |
| **Ngày hết hạn hộ chiếu** | Date | N/A | ❌ Không | DD/MM/YYYY | > ngày cấp |
| **Số tài khoản ngân hàng** | Number | 10-16 số | ❌ Không | XXXXXXXXXX | - |
| **Tên ngân hàng** | Text | 100 ký tự | ❌ Không | - | Vietcombank, BIDV |
| **Chi nhánh ngân hàng** | Text | 100 ký tự | ❌ Không | - | Quận 1, Tân Bình |
| **Mã số thuế cá nhân** | Text | 10-13 ký tự | ❌ Không | XXXXXXXXXX | - |
| **Trình độ học vấn** | Combobox | N/A | ✅ Có | Danh sách | THCS, THPT, Đại học, Thạc sĩ, Tiến sĩ |
| **Chuyên ngành** | Text | 100 ký tự | ❌ Không | - | Công nghệ thông tin |
| **Nơi đào tạo** | Text | 200 ký tự | ❌ Không | - | Đại học Bách Khoa |
| **Năm tốt nghiệp** | Number | 4 số | ❌ Không | YYYY | 1950 - hiện tại |
| **GPA/Điểm TB** | Decimal | N/A | ❌ Không | 0.00 - 4.00 hoặc 0.00 - 10.00 | Tùy hệ thống |
| **Xếp loại tốt nghiệp** | Combobox | N/A | ❌ Không | Xuất sắc, Giỏi, Khá, TB | - |
| **Nơi công tác** | Text | 200 ký tự | ✅ Có | - | Tên công ty/trường |
| **Chức vụ** | Text | 50 ký tự | ✅ Có | Chữ | Giáo viên, Trưởng phòng |
| **Bộ phận/Phòng ban** | Combobox | N/A | ❌ Không | Danh sách | Hành chính, Kế toán |
| **Cấp bậc** | Combobox | N/A | ❌ Không | Danh sách | Nhân viên, Trưởng phòng, Giám đốc |
| **Loại hợp đồng** | Combobox | N/A | ❌ Không | Danh sách | Thử việc, Có thời hạn, Vô thời hạn |
| **Lương cơ bản** | Number | N/A | ❌ Không | > 0 | Đơn vị: VNĐ |
| **Hệ số lương** | Decimal | N/A | ❌ Không | 1.0 - 10.0 | - |
| **Người liên hệ khẩn cấp** | Text | 100 ký tự | ❌ Không | - | Họ tên người thân |
| **SĐT liên hệ khẩn cấp** | Number | 10-11 số | ❌ Không | 0XXXXXXXXX | - |
| **Quan hệ** | Text | 50 ký tự | ❌ Không | - | Cha, mẹ, vợ, chồng |
| **Dân tộc** | Text | 50 ký tự | ❌ Không | - | Kinh, Tày, Thái |
| **Tôn giáo** | Text | 50 ký tự | ❌ Không | - | Không, Phật giáo, Thiên chúa giáo |
| **Tình trạng hôn nhân** | Combobox | N/A | ❌ Không | Danh sách | Độc thân, Đã kết hôn, Ly hôn, Góa |
| **Số con** | Number | 1-2 số | ❌ Không | 0-99 | - |
| **Nhóm máu** | Combobox | N/A | ❌ Không | A, B, AB, O | Có thể có Rh+/- |
| **Chiều cao** | Number | 3 số | ❌ Không | 100-250 (cm) | - |
| **Cân nặng** | Number | 2-3 số | ❌ Không | 30-200 (kg) | - |
| **Tình trạng sức khỏe** | Text | 500 ký tự | ❌ Không | - | Mô tả bệnh lý nếu có |
| **Website cá nhân** | URL | 200 ký tự | ❌ Không | https://example.com | - |
| **LinkedIn** | URL | 200 ký tự | ❌ Không | linkedin.com/in/username | - |
| **Facebook** | URL | 200 ký tự | ❌ Không | facebook.com/username | - |
| **Ghi chú** | Textarea | 1000 ký tự | ❌ Không | - | Thông tin bổ sung |
| **Hình ảnh đại diện** | File | 5MB | ❌ Không | .jpg, .jpeg, .png | 300x300px |
| **CV/Hồ sơ** | File | 10MB | ❌ Không | .pdf, .doc, .docx | - |
| **Bằng cấp/Chứng chỉ** | File | 10MB | ❌ Không | .pdf, .jpg, .png | Có thể nhiều file |

---

## CHI TIẾT TỪNG NHÓM TRƯỜNG

## 1. NHÓM MÃ ĐỊNH DANH

### 1.1. MÃ SINH VIÊN

**Thông tin:**
- **Độ dài:** 10 ký tự cố định
- **Bắt buộc:** Có
- **Format:** `SV` + 8 chữ số

**Quy tắc:**
- ✅ Bắt đầu bằng "SV" (viết hoa)
- ✅ Theo sau là 8 chữ số (0-9)
- ❌ Không chứa ký tự đặc biệt
- ❌ Không chứa khoảng trắng
- ✅ Phải là duy nhất trong hệ thống

**Ví dụ hợp lệ:**
```
✅ SV12345678
✅ SV00000001
✅ SV20240001
```

**Ví dụ không hợp lệ:**
```
❌ sv12345678 (chữ thường)
❌ SV1234567 (thiếu 1 số)
❌ SV123456789 (thừa 1 số)
❌ SV1234567A (có chữ cái)
❌ SV 12345678 (có khoảng trắng)
```

**Message lỗi:**
- Trống: `"Vui lòng nhập mã sinh viên!"`
- Sai format: `"Mã sinh viên phải có định dạng SV + 8 chữ số!"`
- Trùng lặp: `"Mã sinh viên đã tồn tại trong hệ thống!"`

---

### 1.2. MÃ GIẢNG VIÊN

**Thông tin:**
- **Độ dài:** 10 ký tự cố định
- **Bắt buộc:** Có
- **Format:** `GV` + 8 chữ số

**Quy tắc:**
- ✅ Bắt đầu bằng "GV" (viết hoa)
- ✅ Theo sau là 8 chữ số (0-9)
- ❌ Không chứa ký tự đặc biệt
- ❌ Không chứa khoảng trắng
- ✅ Phải là duy nhất trong hệ thống

**Ví dụ hợp lệ:**
```
✅ GV12345678
✅ GV00000001
✅ GV20240001
```

**Message lỗi:**
- Trống: `"Vui lòng nhập mã giảng viên!"`
- Sai format: `"Mã giảng viên phải có định dạng GV + 8 chữ số!"`
- Trùng lặp: `"Mã giảng viên đã tồn tại trong hệ thống!"`

---

### 1.3. MÃ CÁN BỘ

**Thông tin:**
- **Độ dài:** 10 ký tự cố định
- **Bắt buộc:** Có
- **Format:** `CB` + 8 chữ số

**Ví dụ hợp lệ:**
```
✅ CB12345678
✅ CB00000001
```

---

### 1.4. MÃ NHÂN VIÊN

**Thông tin:**
- **Độ dài:** 10 ký tự cố định
- **Bắt buộc:** Có
- **Format:** `NV` + 8 chữ số

**Ví dụ hợp lệ:**
```
✅ NV12345678
✅ NV00000001
```

---

### 1.5. MÃ KHOA/PHÒNG BAN

**Thông tin:**
- **Độ dài:** 8 ký tự
- **Bắt buộc:** Có
- **Format:** 
  - Khoa: `K` + 7 chữ số
  - Phòng ban: `PB` + 6 chữ số

**Ví dụ hợp lệ:**
```
✅ K1234567 (Khoa CNTT)
✅ PB123456 (Phòng Hành chính)
```

---

### 1.6. MÃ LỚP HỌC

**Thông tin:**
- **Độ dài:** 10 ký tự cố định
- **Bắt buộc:** Có
- **Format:** `LH` + 8 chữ số

**Ví dụ hợp lệ:**
```
✅ LH12345678
✅ LH20240001
```

---

### 1.7. MÃ MÔN HỌC

**Thông tin:**
- **Độ dài:** 10 ký tự cố định
- **Bắt buộc:** Có
- **Format:** `MH` + 8 chữ số

**Ví dụ hợp lệ:**
```
✅ MH12345678
✅ MH00001001
```

---

## 2. NHÓM THÔNG TIN CÁ NHÂN

### 2.1. HỌ VÀ TÊN (ĐẦY ĐỦ)

**Thông tin:**
- **Độ dài:** 50-100 ký tự
- **Bắt buộc:** Có
- **Kiểu dữ liệu:** Text

**Quy tắc:**
- ✅ Chỉ chứa chữ cái và khoảng trắng
- ✅ Tiếng Việt có dấu
- ✅ Viết hoa chữ cái đầu mỗi từ
- ❌ Không chứa số
- ❌ Không chứa ký tự đặc biệt

**Ví dụ hợp lệ:**
```
✅ Nguyễn Văn An
✅ Trần Thị Bích Ngọc
✅ Lê Hoàng Minh Quân
```

---

### 2.2. HỌ (Riêng biệt)

**Thông tin:**
- **Độ dài:** Tối đa 20 ký tự
- **Bắt buộc:** Có

**Ví dụ hợp lệ:**
```
✅ Nguyễn
✅ Trần
✅ Lê
✅ Hoàng
```

---

### 2.3. TÊN ĐỆM

**Thông tin:**
- **Độ dài:** Tối đa 30 ký tự
- **Bắt buộc:** Không

**Ví dụ hợp lệ:**
```
✅ Văn
✅ Thị
✅ Hoàng Minh
✅ (để trống)
```

---

### 2.4. TÊN

**Thông tin:**
- **Độ dài:** Tối đa 20 ký tự
- **Bắt buộc:** Có

**Ví dụ hợp lệ:**
```
✅ An
✅ Bình
✅ Ngọc
```

---

## 3. NHÓM NGÀY THÁNG

### 3.1. NGÀY SINH

**Thông tin:**
- **Format:** DD/MM/YYYY
- **Bắt buộc:** Có

**Quy tắc:**
- ✅ Năm: 1900 - năm hiện tại
- ✅ Phải ≥ 18 tuổi (nếu là nhân viên/giảng viên)
- ✅ Phải ≥ 16 tuổi (nếu là sinh viên)
- ❌ Không được là ngày tương lai

**Ví dụ hợp lệ:**
```
✅ 15/08/1990
✅ 01/01/2005
```

---

### 3.2. NGÀY VÀO LÀM

**Thông tin:**
- **Format:** DD/MM/YYYY
- **Bắt buộc:** Có (đối với nhân viên/giảng viên)

**Quy tắc:**
- ✅ Phải ≥ (ngày sinh + 18 năm)
- ✅ Có thể là quá khứ hoặc tương lai
- ❌ Không được trước ngày sinh + 18 năm

---

### 3.3. NGÀY TỐT NGHIỆP

**Thông tin:**
- **Format:** DD/MM/YYYY
- **Bắt buộc:** Không

**Quy tắc:**
- ✅ Có thể là quá khứ hoặc tương lai
- ✅ Phải > ngày sinh + 18 năm

---

## 4. NHÓM LIÊN LẠC

### 4.1. SỐ ĐIỆN THOẠI DI ĐỘNG

**Thông tin:**
- **Độ dài:** 10-11 số
- **Bắt buộc:** Có

**Quy tắc:**
- ✅ Bắt đầu bằng số 0
- ✅ 10 số: 09X, 08X, 07X, 05X, 03X
- ✅ 11 số: 012X, 016X, 018X, 019X (cũ)
- ❌ Không chứa chữ cái
- ❌ Không chứa ký tự đặc biệt
- ❌ Không chứa khoảng trắng

**Nhà mạng Việt Nam:**
```
✅ Viettel: 086, 096, 097, 098, 032, 033, 034, 035, 036, 037, 038, 039
✅ Vinaphone: 088, 091, 094, 083, 084, 085, 081, 082
✅ Mobifone: 089, 090, 093, 070, 079, 077, 076, 078
✅ Vietnamobile: 092, 056, 058
✅ Gmobile: 099, 059
```

**Ví dụ hợp lệ:**
```
✅ 0912345678
✅ 0987654321
✅ 0123456789
```

**Ví dụ không hợp lệ:**
```
❌ 912345678 (thiếu số 0)
❌ 09123abc78 (có chữ cái)
❌ 0912-345-678 (có dấu gạch)
❌ 091 234 5678 (có khoảng trắng)
```

---

### 4.2. SỐ ĐIỆN THOẠI CỐ ĐỊNH

**Thông tin:**
- **Độ dài:** 10 số
- **Bắt buộc:** Không

**Format:** Mã vùng (2-3 số) + Số thuê bao (7-8 số)

**Mã vùng các tỉnh/thành phố:**
```
✅ Hà Nội: 024
✅ TP.HCM: 028
✅ Hải Phòng: 0225
✅ Đà Nẵng: 0236
✅ Cần Thơ: 0292
```

**Ví dụ hợp lệ:**
```
✅ 0243456789 (Hà Nội)
✅ 0287654321 (TP.HCM)
```

---

### 4.3. SỐ FAX

**Thông tin:**
- **Độ dài:** 10 số
- **Bắt buộc:** Không
- **Format:** Giống số điện thoại cố định

---

### 4.4.
