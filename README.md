# 🖥️ Cheat Sheet Terminal
## Các Lệnh Hay Dùng Cho Developer

---

## 📁 1. Điều Hướng Thư Mục

| Lệnh | Chức Năng |
|------|-----------|
| `pwd` | Xem thư mục hiện tại |
| `ls` | Liệt kê file và thư mục |
| `ls -la` | Liệt kê chi tiết (kể cả file ẩn) |
| `cd <folder>` | Di chuyển vào thư mục |
| `cd ..` | Lùi lại 1 cấp |
| `cd ~` | Về thư mục home |
| `cd -` | Quay lại thư mục trước đó |
| `tree` | Hiển thị cấu trúc thư mục |

```bash
$ pwd
$ ls -la
$ cd src
$ cd ..
```

---

## 📄 2. Quản Lý File

| Lệnh | Chức Năng |
|------|-----------|
| `touch file.txt` | Tạo file mới |
| `cat file.txt` | Xem nội dung file |
| `less file.txt` | Xem file dài (cuộn) |
| `head file.txt` | Xem 10 dòng đầu |
| `tail file.txt` | Xem 10 dòng cuối |
| `tail -f log.txt` | Theo dõi log realtime |
| `nano file.txt` | Mở file bằng editor nano |
| `echo "text" > file.txt` | Ghi nội dung vào file |

```bash
$ cat package.json
$ tail -f production.log
```

---

## 📂 Quản Lý Thư Mục & File

| Lệnh | Chức Năng |
|------|-----------|
| `mkdir folder` | Tạo thư mục |
| `mkdir -p a/b/c` | Tạo nhiều thư mục cấp |
| `rm file.txt` | Xóa file |
| `rm -rf folder` | Xóa thư mục (force) |
| `cp a.txt b.txt` | Sao chép file |
| `cp -r src/ dest/` | Sao chép thư mục |
| `mv a.txt b.txt` | Đổi tên file |
| `mv file.txt folder/` | Di chuyển file |

```bash
$ mkdir project
$ cp src/index.js backup.js
$ mv old.txt new.txt
```

---

## 🔍 Tìm Kiếm

| Lệnh | Chức Năng |
|------|-----------|
| `find . -name "*.js"` | Tìm file theo tên |
| `find . -type d -name "src"` | Tìm thư mục |
| `grep "text" file.txt` | Tìm text trong file |
| `grep -r "text" .` | Tìm text trong toàn bộ thư mục |
| `which node` | Tìm đường dẫn của lệnh |
| `whereis python` | Tìm binary, source, man page |

```bash
$ find . -name "*.rb"
$ grep -r "TODO" .
$ which docker
```

---

## ⚙️ Process & Hệ Thống

| Lệnh | Chức Năng |
|------|-----------|
| `ps aux` | Liệt kê tất cả process |
| `top` | Theo dõi hệ thống realtime |
| `htop` | Top nâng cao (nếu có) |
| `kill <PID>` | Dừng process |
| `kill -9 <PID>` | Force kill process |
| `df -h` | Xem dung lượng ổ đĩa |
| `du -sh *` | Xem dung lượng thư mục |
| `free -h` | Xem RAM |
| `uname -a` | Thông tin hệ thống |

```bash
$ ps aux | grep node
$ kill 12345
```

---

## 🌐 Network

| Lệnh | Chức Năng |
|------|-----------|
| `ping google.com` | Kiểm tra kết nối mạng |
| `curl https://api.github.com` | Gọi API (hiển thị kết quả) |
| `curl -I example.com` | Xem header |
| `wget https://file/file.zip` | Tải file |
| `netstat -tulpn` | Xem các port đang mở |
| `lsof -i :3000` | Xem process dùng port |
| `nslookup domain.com` | Tra cứu DNS |

```bash
$ ping google.com
$ curl https://api.github.com
$ lsof -i :3000
```

---

## 🔀 Git (Cơ Bản)

| Lệnh | Chức Năng |
|------|-----------|
| `git status` | Xem trạng thái |
| `git add .` | Thêm tất cả file |
| `git commit -m "message"` | Commit với message |
| `git push` | Đẩy code lên remote |
| `git pull` | Kéo code từ remote |
| `git checkout branch` | Chuyển branch (cũ) |
| `git switch branch` | Chuyển branch (mới) |
| `git log --oneline` | Xem lịch sử commit ngắn |
| `git diff` | Xem thay đổi |
| `git stash` | Lưu thay đổi tạm thời |

```bash
$ git status
$ git add . && git commit -m "update"
$ git push
```

---

## 🟢 Node.js / NPM

| Lệnh | Chức Năng |
|------|-----------|
| `node -v` | Xem version Node |
| `npm -v` | Xem version NPM |
| `npm install` | Cài đặt dependencies |
| `npm install -g package` | Cài global package |
| `npm run dev` | Chạy script dev |
| `npm run build` | Build project |
| `npm test` | Chạy test |
| `npx create-next-app` | Tạo project Next.js |
| `yarn` | Cài dependencies (Yarn) |
| `pnpm install` | Cài dependencies (PNPM) |

```bash
$ npm install
$ npm run dev
```

---

## 🐳 Docker

| Lệnh | Chức Năng |
|------|-----------|
| `docker ps` | Xem container đang chạy |
| `docker ps -a` | Xem tất cả container |
| `docker images` | Xem danh sách image |
| `docker build -t myapp .` | Build image |
| `docker run -d -p 3000:3000 myapp` | Chạy container |
| `docker logs <container_id>` | Xem logs |
| `docker exec -it <id> sh` | Vào container |
| `docker stop <id>` | Dừng container |
| `docker rm <id>` | Xóa container |
| `docker rmi <image>` | Xóa image |

```bash
$ docker ps
$ docker logs my_container
```

---

## ☸️ Kubernetes (Kubectl)

| Lệnh | Chức Năng |
|------|-----------|
| `kubectl get pods` | Xem pods |
| `kubectl get svc` | Xem services |
| `kubectl get deployments` | Xem deployments |
| `kubectl describe pod <pod>` | Chi tiết pod |
| `kubectl logs <pod>` | Xem logs pod |
| `kubectl exec -it <pod> -- sh` | Vào pod |
| `kubectl apply -f file.yaml` | Áp dụng file yaml |
| `kubectl delete -f file.yaml` | Xóa theo file yaml |

```bash
$ kubectl get pods
$ kubectl logs my-pod
```

---

## ⚡ Nâng Suất Terminal

| Lệnh / Phím | Chức Năng |
|-------------|-----------|
| `history` | Xem lịch sử lệnh |
| `!!` | Thực thi lại lệnh vừa chạy |
| `!n` | Thực thi lệnh số n trong history |
| `Ctrl + R` | Tìm kiếm trong history |
| `Tab` | Tự động hoàn thành |
| `Ctrl + C` | Hủy lệnh đang chạy |
| `Ctrl + L` hoặc `clear` | Xóa màn hình |
| `exit` | Thoát terminal |
| `alias ll="ls -la"` | Tạo alias (ví dụ) |
| `unalias ll` | Xóa alias |

```bash
$ history
$ !!
$ clear
```

---

## 💡 Mẹo Hay

- ✅ Sử dụng `↑` `↓` để duyệt các lệnh đã dùng.
- ✅ Dùng `Tab` để tự động hoàn thành đường dẫn.
- ✅ Dùng `Ctrl + R` để tìm lệnh nhanh trong history.
- ✅ Dùng `2>&1` để ghi log lỗi cùng output.
- ✅ Dùng `>>` để ghi đè, `>>` để thêm vào cuối file.
- ✅ Dùng `|` (pipe) để kết hợp lệnh.
- ✅ Dùng `man <command>` để xem hướng dẫn.

### Ví Dụ Pipe

```bash
$ ps aux | grep node      # Tìm process node
$ cat log.txt | grep ERROR  # Tìm ERROR trong log
$ ls -la | less           # Xem kết quả dài
```

---

## 📚 Tài Liệu Nhanh

```bash
man <command>        # hoặc
<command> --help

# Ví dụ:
man ls
git --help
```

---

> ⭐ **Ghi Nhớ:** Không cần nhớ tất cả! Hãy dùng thường xuyên để thành thạo.

> ⚠️ **Luôn Sao Lưu Trước Khi Xóa:** Đặc biệt với lệnh `rm -rf` — Không có nút "Undo" trong terminal!
