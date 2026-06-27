# 🐧 Linux Path Cheatsheet
## Cấu Trúc Thư Mục Gốc Trong Linux

> Trong Linux, mọi thứ đều bắt đầu từ **`/`** (root directory — thư mục gốc).  
> Đây là "ổ C:\" của Linux, nhưng chỉ có **một** thư mục gốc duy nhất cho toàn hệ thống.

---

## 📂 Tổng Quan Cây Thư Mục

```
/
├── /bin
├── /boot
├── /dev
├── /etc
├── /home
├── /lib
├── /media
├── /mnt
├── /opt
├── /proc
├── /root
├── /run
├── /sbin
├── /srv
├── /sys
├── /tmp
├── /usr
└── /var
```

---

## 📋 Bảng Chi Tiết Từng Thư Mục

| Đường Dẫn | Tên Tiếng Anh | Giải Thích (EN) | Giải Thích (VI) |
|-----------|---------------|-----------------|-----------------|
| `/bin` | Binary | Essential user commands | Chứa các lệnh cơ bản cho người dùng như `ls`, `cp`, `mv`, `cat` — lệnh nào cũng cần dùng hàng ngày |
| `/boot` | Boot | Boot loader files | Chứa các file khởi động hệ thống, bao gồm Linux kernel (`vmlinuz`) và GRUB bootloader |
| `/dev` | Device | Device files | Chứa file đại diện cho các thiết bị phần cứng: ổ cứng (`/dev/sda`), USB, màn hình, v.v. |
| `/etc` | Et Cetera | System configuration files | Chứa toàn bộ file cấu hình hệ thống: cài đặt mạng, user, password, phần mềm cài sẵn |
| `/home` | Home | User home directories | Thư mục cá nhân của từng user. Ví dụ: `/home/john` — giống "My Documents" trong Windows |
| `/lib` | Library | Essential shared libraries | Chứa thư viện dùng chung cho các lệnh trong `/bin` và `/sbin` — giống `.dll` trong Windows |
| `/media` | Media | Removable media mount points | Điểm gắn thiết bị lưu trữ ngoài: USB, CD/DVD, thẻ nhớ được tự động mount vào đây |
| `/mnt` | Mount | Temporary mount points | Điểm gắn thủ công tạm thời: dùng khi bạn tự mount ổ cứng, phân vùng, hoặc network drive |
| `/opt` | Optional | Optional software packages | Chứa phần mềm cài thêm từ bên ngoài (không qua package manager), ví dụ: Chrome, VSCode |
| `/proc` | Process | Process and kernel information | Thư mục ảo (không có trên ổ cứng thật), chứa thông tin về các tiến trình đang chạy và kernel |
| `/root` | Root | Root user's home directory | Thư mục home riêng của user `root` (admin). Khác với `/home` — chỉ dành cho superuser |
| `/run` | Run | Runtime data | Chứa dữ liệu runtime tạm thời: PID files, socket files — được tạo lại mỗi lần khởi động |
| `/sbin` | System Binary | System administration commands | Chứa lệnh quản trị hệ thống chỉ dành cho root: `fdisk`, `iptables`, `reboot`, `shutdown` |
| `/srv` | Service | Service data | Chứa dữ liệu của các service đang chạy, ví dụ: web server lưu file HTML vào `/srv/www` |
| `/sys` | System | Kernel and hardware information | Thư mục ảo cung cấp thông tin về phần cứng và kernel theo thời gian thực |
| `/tmp` | Temporary | Temporary files | Chứa file tạm thời, bị xóa tự động khi restart. Mọi user đều có quyền ghi vào đây |
| `/usr` | Unix System Resources | User applications and data | Chứa phần lớn phần mềm cài qua package manager: `/usr/bin`, `/usr/lib`, `/usr/share` |
| `/var` | Variable | Variable data (logs, cache, etc.) | Chứa dữ liệu thay đổi liên tục: log hệ thống (`/var/log`), cache, email, database files |

---

## 🔍 Giải Thích Chi Tiết Từng Thư Mục Quan Trọng

### `/etc` — Cấu Hình Hệ Thống
Đây là nơi bạn sẽ vào nhiều nhất khi cần chỉnh sửa cấu hình.

| File / Thư Mục | Chức Năng |
|----------------|-----------|
| `/etc/passwd` | Danh sách tất cả user trong hệ thống |
| `/etc/shadow` | Mật khẩu đã mã hóa của các user |
| `/etc/hosts` | Mapping IP ↔ hostname thủ công |
| `/etc/fstab` | Cấu hình tự động mount ổ cứng khi khởi động |
| `/etc/nginx/` | Cấu hình web server Nginx |
| `/etc/ssh/` | Cấu hình SSH server |
| `/etc/crontab` | Lịch chạy tự động (cron jobs) |

---

### `/var` — Dữ Liệu Động
Nơi lưu log và dữ liệu thay đổi theo thời gian.

| File / Thư Mục | Chức Năng |
|----------------|-----------|
| `/var/log/` | Tất cả file log hệ thống |
| `/var/log/syslog` | Log chung của hệ thống |
| `/var/log/auth.log` | Log đăng nhập, xác thực |
| `/var/log/nginx/` | Log của Nginx web server |
| `/var/cache/` | Cache của các phần mềm |
| `/var/lib/` | Dữ liệu của các ứng dụng (database, v.v.) |
| `/var/mail/` | Email của user trong hệ thống |

---

### `/usr` — Phần Mềm Người Dùng
Nơi phần lớn phần mềm cài đặt thông qua `apt`, `yum`, `dnf`.

| Thư Mục | Chức Năng |
|---------|-----------|
| `/usr/bin/` | Lệnh của các phần mềm cài thêm (không phải lệnh hệ thống cốt lõi) |
| `/usr/sbin/` | Lệnh quản trị của phần mềm cài thêm |
| `/usr/lib/` | Thư viện của phần mềm cài thêm |
| `/usr/share/` | File dùng chung: tài liệu, icon, theme |
| `/usr/local/` | Phần mềm cài thủ công (biên dịch từ source) |

---

### `/proc` — Thông Tin Tiến Trình (Ảo)
Không phải file thật — đây là interface để xem thông tin kernel.

| File | Chức Năng |
|------|-----------|
| `/proc/cpuinfo` | Thông tin CPU |
| `/proc/meminfo` | Thông tin RAM |
| `/proc/uptime` | Thời gian hệ thống đã chạy |
| `/proc/<PID>/` | Thư mục chứa thông tin của tiến trình có PID tương ứng |
| `/proc/net/` | Thông tin mạng |

---

## ⚡ Lệnh Điều Hướng Nhanh

| Lệnh | Chức Năng |
|------|-----------|
| `ls /` | Xem toàn bộ thư mục gốc |
| `ls /etc` | Xem nội dung thư mục `/etc` |
| `cat /etc/os-release` | Xem thông tin distro Linux đang dùng |
| `cat /proc/cpuinfo` | Xem thông tin CPU |
| `cat /proc/meminfo` | Xem thông tin bộ nhớ RAM |
| `df -h /` | Xem dung lượng ổ đĩa gốc |
| `du -sh /var/log` | Xem kích thước thư mục log |
| `ls /home` | Xem danh sách tất cả user |
| `ls /dev/sd*` | Xem danh sách ổ cứng |

---

## 💡 Mẹo Nhớ Nhanh

| Nhóm | Thư Mục | Cách Nhớ |
|------|---------|----------|
| **Lệnh hệ thống** | `/bin`, `/sbin` | **bin** = binary (file thực thi). `sbin` = system binary (chỉ root dùng) |
| **Cấu hình** | `/etc` | Mọi thứ cần **chỉnh sửa** đều nằm ở đây |
| **Người dùng** | `/home`, `/root` | `/home` cho user thường, `/root` cho admin |
| **Phần mềm** | `/usr`, `/opt` | `/usr` = cài qua package manager, `/opt` = cài thủ công |
| **Dữ liệu động** | `/var`, `/tmp` | `/var` lưu lâu dài, `/tmp` xóa khi reboot |
| **Phần cứng** | `/dev`, `/sys`, `/proc` | Đây là "cửa sổ" nhìn vào phần cứng và kernel |
| **Mount** | `/media`, `/mnt` | `/media` = tự động, `/mnt` = thủ công |

---

> 📌 **Lưu ý:** Trong Linux, **mọi thứ đều là file** — kể cả thiết bị phần cứng, tiến trình, và kết nối mạng đều được biểu diễn dưới dạng file trong cây thư mục này.
