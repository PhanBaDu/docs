# ✏️ Nano & Vi/Vim Cheat Sheet
## Các Cú Pháp Hay Dùng Nhất

> **Nano** = Editor đơn giản, thân thiện cho người mới.  
> **Vi/Vim** = Editor mạnh mẽ hơn, có mặt trên mọi Linux server, cần học để dùng được.

---

## 🟢 NANO

> Mở file: `nano filename.txt`  
> Các phím tắt hiển thị ở **thanh dưới màn hình** — `^` nghĩa là phím `Ctrl`

---

### 📂 Mở & Thoát

| Phím Tắt | Tiếng Anh | Tiếng Việt |
|----------|-----------|------------|
| `nano <file>` | Open a file | Mở file để chỉnh sửa |
| `nano +N <file>` | Open file at line N | Mở file và nhảy đến dòng N |
| `Ctrl + X` | Exit | Thoát khỏi nano |
| `Ctrl + X` → `Y` → `Enter` | Save and exit | Lưu file rồi thoát |
| `Ctrl + X` → `N` | Exit without saving | Thoát mà không lưu |

---

### 💾 Lưu File

| Phím Tắt | Tiếng Anh | Tiếng Việt |
|----------|-----------|------------|
| `Ctrl + O` | Write Out (Save) | Lưu file (giữ nguyên tên) |
| `Ctrl + O` → đổi tên → `Enter` | Save as new name | Lưu file với tên khác |

---

### 🔍 Tìm Kiếm & Thay Thế

| Phím Tắt | Tiếng Anh | Tiếng Việt |
|----------|-----------|------------|
| `Ctrl + W` | Search (Where is) | Tìm kiếm từ/cụm từ |
| `Ctrl + W` → `Enter` | Search next | Tìm kết quả tiếp theo |
| `Alt + W` | Search previous | Tìm kết quả trước đó |
| `Ctrl + \` | Search and Replace | Tìm và thay thế |

---

### 🖱️ Di Chuyển Con Trỏ

| Phím Tắt | Tiếng Anh | Tiếng Việt |
|----------|-----------|------------|
| `Ctrl + A` | Go to beginning of line | Về đầu dòng |
| `Ctrl + E` | Go to end of line | Về cuối dòng |
| `Ctrl + Y` | Page Up | Cuộn lên một trang |
| `Ctrl + V` | Page Down | Cuộn xuống một trang |
| `Ctrl + _` | Go to line number | Nhảy đến số dòng cụ thể |
| `Alt + \` | Go to first line | Nhảy về dòng đầu tiên |
| `Alt + /` | Go to last line | Nhảy xuống dòng cuối cùng |

---

### ✂️ Cắt, Sao Chép & Dán

| Phím Tắt | Tiếng Anh | Tiếng Việt |
|----------|-----------|------------|
| `Ctrl + K` | Cut current line | Cắt dòng hiện tại (vào clipboard) |
| `Ctrl + U` | Paste (Uncut) | Dán nội dung từ clipboard |
| `Alt + 6` | Copy current line | Sao chép dòng hiện tại |
| `Ctrl + K` (nhiều lần) | Cut multiple lines | Cắt nhiều dòng liên tiếp |

---

### 🔧 Tiện Ích Khác

| Phím Tắt | Tiếng Anh | Tiếng Việt |
|----------|-----------|------------|
| `Ctrl + G` | Help | Mở trang trợ giúp |
| `Ctrl + C` | Show cursor position | Hiển thị vị trí con trỏ (dòng, cột) |
| `Alt + U` | Undo | Hoàn tác thay đổi vừa làm |
| `Alt + E` | Redo | Làm lại thay đổi đã hoàn tác |
| `Alt + N` | Toggle line numbers | Bật/tắt hiển thị số dòng |
| `Alt + M` | Toggle mouse support | Bật/tắt dùng chuột |
| `Ctrl + L` | Refresh screen | Làm mới màn hình |

---

---

## 🔵 VI / VIM

> Mở file: `vi filename.txt` hoặc `vim filename.txt`

### ⚠️ Hiểu Về Chế Độ (Mode) — Quan Trọng Nhất

Vim có **3 chế độ chính**, đây là điểm khác biệt lớn nhất so với các editor khác:

| Chế Độ | Tên | Mô Tả |
|--------|-----|--------|
| **Normal** | Normal Mode | Chế độ mặc định khi mở file. Dùng để di chuyển, xóa, copy, paste. **Không gõ được chữ.** |
| **Insert** | Insert Mode | Chế độ gõ văn bản bình thường như các editor khác. Nhấn `i` để vào. |
| **Command** | Command Mode | Chế độ nhập lệnh (lưu, thoát, tìm kiếm). Nhấn `:` để vào. |

```
Mở file → [Normal Mode]
              ↓ i / a / o
         [Insert Mode]  →  Gõ văn bản
              ↓ Esc
         [Normal Mode]
              ↓ :
         [Command Mode] →  :w  :q  :wq
```

---

### 🚪 Vào / Thoát Các Chế Độ

| Phím | Từ Chế Độ | Tiếng Anh | Tiếng Việt |
|------|-----------|-----------|------------|
| `i` | Normal → Insert | Insert before cursor | Vào Insert Mode — gõ trước con trỏ |
| `I` | Normal → Insert | Insert at beginning of line | Vào Insert Mode — nhảy về đầu dòng rồi gõ |
| `a` | Normal → Insert | Append after cursor | Vào Insert Mode — gõ sau con trỏ |
| `A` | Normal → Insert | Append at end of line | Vào Insert Mode — nhảy về cuối dòng rồi gõ |
| `o` | Normal → Insert | Open new line below | Tạo dòng mới bên dưới rồi vào Insert Mode |
| `O` | Normal → Insert | Open new line above | Tạo dòng mới bên trên rồi vào Insert Mode |
| `Esc` | Insert → Normal | Exit Insert Mode | Thoát khỏi Insert Mode, về Normal Mode |
| `:` | Normal → Command | Enter Command Mode | Vào Command Mode để gõ lệnh |

---

### 💾 Lưu & Thoát (Command Mode)

> Nhớ nhấn `Esc` trước, rồi gõ lệnh bắt đầu bằng `:`

| Lệnh | Tiếng Anh | Tiếng Việt |
|------|-----------|------------|
| `:w` | Write (save) | Lưu file |
| `:w <tên>` | Save as new filename | Lưu file với tên khác |
| `:q` | Quit | Thoát (chỉ thoát được nếu chưa sửa gì) |
| `:q!` | Force quit without saving | Thoát mà không lưu, bỏ qua mọi thay đổi |
| `:wq` | Write and quit | Lưu rồi thoát |
| `:wq!` | Force write and quit | Buộc lưu rồi thoát |
| `ZZ` | Save and quit (shortcut) | Lưu và thoát nhanh (ở Normal Mode, không cần `:`) |
| `ZQ` | Quit without saving | Thoát không lưu nhanh (ở Normal Mode) |

---

### 🖱️ Di Chuyển Con Trỏ (Normal Mode)

#### Di Chuyển Cơ Bản

| Phím | Tiếng Anh | Tiếng Việt |
|------|-----------|------------|
| `h` | Move left | Di chuyển sang trái |
| `l` | Move right | Di chuyển sang phải |
| `j` | Move down | Di chuyển xuống |
| `k` | Move up | Di chuyển lên |
| `w` | Next word | Nhảy đến đầu từ tiếp theo |
| `b` | Back word | Nhảy về đầu từ trước đó |
| `e` | End of word | Nhảy đến cuối từ hiện tại |

#### Di Chuyển Theo Dòng

| Phím | Tiếng Anh | Tiếng Việt |
|------|-----------|------------|
| `0` | Beginning of line | Về đầu dòng |
| `^` | First non-blank character | Về ký tự không trắng đầu tiên trong dòng |
| `$` | End of line | Về cuối dòng |
| `G` | Go to last line | Nhảy xuống dòng cuối file |
| `gg` | Go to first line | Nhảy lên dòng đầu file |
| `:<N>` | Go to line N | Nhảy đến dòng số N (vd: `:25`) |
| `Ctrl + F` | Page down | Cuộn xuống một trang |
| `Ctrl + B` | Page up | Cuộn lên một trang |
| `Ctrl + D` | Half page down | Cuộn xuống nửa trang |
| `Ctrl + U` | Half page up | Cuộn lên nửa trang |

---

### ✂️ Xóa (Normal Mode)

| Phím | Tiếng Anh | Tiếng Việt |
|------|-----------|------------|
| `x` | Delete character | Xóa một ký tự tại con trỏ |
| `X` | Delete character before | Xóa ký tự trước con trỏ (như Backspace) |
| `dd` | Delete current line | Xóa toàn bộ dòng hiện tại |
| `dw` | Delete word | Xóa từ hiện tại |
| `d$` | Delete to end of line | Xóa từ con trỏ đến cuối dòng |
| `d0` | Delete to beginning of line | Xóa từ đầu dòng đến con trỏ |
| `dgg` | Delete to first line | Xóa từ dòng hiện tại lên đến dòng đầu |
| `dG` | Delete to last line | Xóa từ dòng hiện tại xuống đến dòng cuối |
| `5dd` | Delete 5 lines | Xóa 5 dòng liên tiếp (thay 5 bằng số bất kỳ) |

---

### 📋 Sao Chép & Dán (Normal Mode)

| Phím | Tiếng Anh | Tiếng Việt |
|------|-----------|------------|
| `yy` | Yank (copy) current line | Sao chép dòng hiện tại |
| `yw` | Yank word | Sao chép một từ |
| `y$` | Yank to end of line | Sao chép từ con trỏ đến cuối dòng |
| `5yy` | Yank 5 lines | Sao chép 5 dòng liên tiếp |
| `p` | Paste after cursor | Dán nội dung sau con trỏ / sau dòng hiện tại |
| `P` | Paste before cursor | Dán nội dung trước con trỏ / trước dòng hiện tại |

---

### 🔄 Hoàn Tác & Làm Lại (Normal Mode)

| Phím | Tiếng Anh | Tiếng Việt |
|------|-----------|------------|
| `u` | Undo | Hoàn tác thay đổi vừa làm |
| `Ctrl + R` | Redo | Làm lại thay đổi đã hoàn tác |
| `U` | Undo all changes on line | Hoàn tác tất cả thay đổi trên dòng hiện tại |

---

### 🔍 Tìm Kiếm & Thay Thế

| Lệnh | Tiếng Anh | Tiếng Việt |
|------|-----------|------------|
| `/text` | Search forward | Tìm kiếm xuôi xuống (gõ `/` rồi nhập từ cần tìm) |
| `?text` | Search backward | Tìm kiếm ngược lên trên |
| `n` | Next match | Nhảy đến kết quả tìm kiếm tiếp theo |
| `N` | Previous match | Nhảy về kết quả tìm kiếm trước đó |
| `:%s/old/new/g` | Replace all | Thay thế tất cả `old` bằng `new` trong toàn file |
| `:%s/old/new/gc` | Replace with confirm | Thay thế từng cái một, hỏi xác nhận trước mỗi lần |
| `:s/old/new/g` | Replace in current line | Chỉ thay thế trong dòng hiện tại |

---

### 🔧 Chỉnh Sửa Nhanh (Normal Mode)

| Phím | Tiếng Anh | Tiếng Việt |
|------|-----------|------------|
| `r` | Replace single character | Thay thế đúng 1 ký tự tại con trỏ |
| `R` | Replace mode | Vào chế độ ghi đè (gõ đè lên ký tự cũ) |
| `cc` | Change entire line | Xóa dòng hiện tại và vào Insert Mode |
| `cw` | Change word | Xóa từ hiện tại và vào Insert Mode |
| `c$` | Change to end of line | Xóa từ con trỏ đến cuối dòng và vào Insert Mode |
| `~` | Toggle case | Đổi chữ hoa ↔ chữ thường |
| `>>` | Indent line | Thêm tab/indent cho dòng |
| `<<` | Unindent line | Bỏ tab/indent của dòng |
| `==` | Auto-indent line | Tự động căn chỉnh indent |

---

### 🖥️ Lệnh Hữu Ích Khác (Command Mode)

| Lệnh | Tiếng Anh | Tiếng Việt |
|------|-----------|------------|
| `:set number` | Show line numbers | Bật hiển thị số dòng |
| `:set nonumber` | Hide line numbers | Tắt hiển thị số dòng |
| `:set hlsearch` | Highlight search | Bật highlight kết quả tìm kiếm |
| `:set nohlsearch` | Remove highlight | Tắt highlight tìm kiếm |
| `:set paste` | Paste mode | Bật chế độ dán (tránh lỗi indent khi paste) |
| `:syntax on` | Syntax highlighting | Bật tô màu cú pháp |
| `:syntax off` | No syntax highlighting | Tắt tô màu cú pháp |
| `:%d` | Delete all lines | Xóa toàn bộ nội dung file |
| `:10,20d` | Delete lines 10 to 20 | Xóa từ dòng 10 đến dòng 20 |
| `:!<cmd>` | Run shell command | Chạy lệnh shell mà không thoát vim (vd: `:!ls`) |

---

## ⚡ So Sánh Nano vs Vim

| Tiêu Chí | Nano | Vim |
|----------|------|-----|
| **Độ khó** | Dễ, phù hợp người mới | Khó ban đầu, cần học mode |
| **Tốc độ** | Chậm hơn | Rất nhanh khi thành thạo |
| **Có sẵn trên server** | Không phải lúc nào cũng có | Hầu như luôn có (`vi`) |
| **Tính năng** | Cơ bản | Rất mạnh, hỗ trợ plugin |
| **Phù hợp cho** | Sửa nhanh file cấu hình | Lập trình, chỉnh sửa phức tạp |
| **Thoát như thế nào** | `Ctrl + X` | `Esc` → `:q!` |

---

## 🆘 Bị Kẹt Trong Vim? Thoát Ngay!

```
1. Nhấn  Esc  (một hoặc vài lần)
2. Gõ    :q!
3. Nhấn  Enter
```

> `:q!` = thoát ngay lập tức, **không lưu** bất kỳ thay đổi nào.
