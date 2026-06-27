# 🐳 Docker Cheat Sheet

---

## 📦 Installation & Version

| Lệnh | Chức Năng |
|------|-----------|
| `docker --version` | Xem version Docker |
| `docker info` | Hiển thị thông tin toàn hệ thống |
| `docker version` | Chi tiết version client & server |

---

## 🖼️ Images

### 🔍 Pull & Search

| Lệnh | Chức Năng |
|------|-----------|
| `docker pull <image>` | Pull image từ registry |
| `docker pull <image>:<tag>` | Pull image theo tag cụ thể |
| `docker search <term>` | Tìm kiếm image trên Docker Hub |

### 📋 List & Inspect

| Lệnh | Chức Năng |
|------|-----------|
| `docker images` | Liệt kê tất cả image local |
| `docker images -a` | Bao gồm cả intermediate images |
| `docker inspect <image>` | Xem metadata chi tiết của image |

### 🔧 Build

| Lệnh | Chức Năng |
|------|-----------|
| `docker build -t <n>:<tag> .` | Build từ Dockerfile ở thư mục hiện tại |
| `docker build -f Dockerfile.dev .` | Build từ Dockerfile cụ thể |
| `docker build --no-cache -t <n> .` | Build không dùng cache |

### 🗑️ Remove Images

| Lệnh | Chức Năng |
|------|-----------|
| `docker rmi <image>` | Xóa một image |
| `docker rmi $(docker images -q)` | Xóa tất cả image |
| `docker image prune` | Xóa dangling images |
| `docker image prune -a` | Xóa tất cả image không dùng |

---

## 📦 Containers

### ▶️ Run

| Lệnh | Chức Năng |
|------|-----------|
| `docker run <image>` | Chạy một container |
| `docker run -d <image>` | Chạy ở chế độ nền (detached) |
| `docker run -it <image> bash` | Chạy tương tác với bash |
| `docker run --name <n> <image>` | Đặt tên cho container |
| `docker run -p 8080:80 <image>` | Map port host:container |
| `docker run -v /host/path:/container/path <image>` | Bind mount volume |
| `docker run --rm <image>` | Tự xóa container sau khi thoát |
| `docker run -e VAR=value <image>` | Đặt biến môi trường |
| `docker run --env-file .env <image>` | Load biến môi trường từ file |
| `docker run --network <network> <image>` | Kết nối vào một network |

### 📊 List

| Lệnh | Chức Năng |
|------|-----------|
| `docker ps` | Liệt kê container đang chạy |
| `docker ps -a` | Liệt kê tất cả container (kể cả đã dừng) |
| `docker ps -q` | Chỉ hiển thị container IDs |

### ⏯️ Start / Stop / Restart

| Lệnh | Chức Năng |
|------|-----------|
| `docker start <container>` | Khởi động container đã dừng |
| `docker stop <container>` | Dừng container nhẹ nhàng |
| `docker kill <container>` | Buộc dừng container |
| `docker restart <container>` | Khởi động lại container |
| `docker pause <container>` | Tạm dừng container |
| `docker unpause <container>` | Tiếp tục container |

### 🔎 Inspect & Logs

| Lệnh | Chức Năng |
|------|-----------|
| `docker logs <container>` | Xem logs của container |
| `docker logs -f <container>` | Theo dõi logs realtime |
| `docker logs --tail 100 <container>` | Xem 100 dòng log cuối |
| `docker inspect <container>` | Xem thông tin chi tiết container |
| `docker stats` | Thống kê tài nguyên realtime |
| `docker top <container>` | Xem các process đang chạy trong container |
| `docker port <container>` | Xem mapping port |

### 💻 Execute & Attach

| Lệnh | Chức Năng |
|------|-----------|
| `docker exec -it <container> bash` | Mở shell trong container đang chạy |
| `docker exec <container> <cmd>` | Chạy lệnh trong container |
| `docker attach <container>` | Gắn vào STDIN/STDOUT của container |

### 📁 Copy Files

| Lệnh | Chức Năng |
|------|-----------|
| `docker cp <container>:/path/file ./local` | Copy file từ container ra host |
| `docker cp ./local <container>:/path/file` | Copy file từ host vào container |

### 🗑️ Remove Containers

| Lệnh | Chức Năng |
|------|-----------|
| `docker rm <container>` | Xóa container đã dừng |
| `docker rm -f <container>` | Buộc xóa container đang chạy |
| `docker rm $(docker ps -aq)` | Xóa tất cả container |
| `docker container prune` | Xóa tất cả container đã dừng |

---

## 💾 Volumes

| Lệnh | Chức Năng |
|------|-----------|
| `docker volume create <n>` | Tạo một named volume |
| `docker volume ls` | Liệt kê tất cả volume |
| `docker volume inspect <n>` | Xem chi tiết volume |
| `docker volume rm <n>` | Xóa một volume |
| `docker volume prune` | Xóa tất cả volume không dùng |
| `docker run -v myvolume:/app/data <image>` | Mount named volume vào container |

---

## 🌐 Networks

| Lệnh | Chức Năng |
|------|-----------|
| `docker network create <n>` | Tạo một network |
| `docker network ls` | Liệt kê các network |
| `docker network inspect <n>` | Xem chi tiết network |
| `docker network rm <n>` | Xóa một network |
| `docker network prune` | Xóa tất cả network không dùng |
| `docker network connect <network> <container>` | Kết nối container vào network |
| `docker network disconnect <network> <container>` | Ngắt kết nối container khỏi network |

### 🔌 Common Network Drivers

| Driver | Mô Tả |
|--------|--------|
| `bridge` | Network mặc định, cô lập (các container trên cùng host) |
| `host` | Container dùng chung network với host |
| `none` | Không có networking |

---

## 🐙 Docker Compose

### Các Lệnh Chính

| Lệnh | Chức Năng |
|------|-----------|
| `docker compose up` | Khởi động các service |
| `docker compose up -d` | Khởi động ở chế độ nền |
| `docker compose up --build` | Rebuild image trước khi khởi động |
| `docker compose down` | Dừng và xóa containers |
| `docker compose down -v` | Dừng, xóa containers và volumes |
| `docker compose ps` | Liệt kê các service đang chạy |
| `docker compose logs` | Xem logs tất cả service |
| `docker compose logs -f <service>` | Theo dõi logs của một service |
| `docker compose exec <svc> bash` | Mở shell trong một service |
| `docker compose build` | Build/rebuild các service |
| `docker compose pull` | Pull image mới nhất |
| `docker compose restart <service>` | Restart một service |
| `docker compose stop` | Dừng service (không xóa) |
| `docker compose start` | Khởi động service đã dừng |
| `docker compose config` | Kiểm tra và xem cấu hình compose |

### 📄 Ví Dụ `docker-compose.yml`

```yaml
version: "3.9"

services:
  web:
    build: .
    ports:
      - "8080:80"
    environment:
      - NODE_ENV=production
    depends_on:
      - db
    volumes:
      - .:/app
    networks:
      - app-net

  db:
    image: postgres:15
    environment:
      POSTGRES_PASSWORD: secret
    volumes:
      - db-data:/var/lib/postgresql/data
    networks:
      - app-net

volumes:
  db-data:

networks:
  app-net:
```

---

## 📝 Dockerfile Reference

| Instruction | Chức Năng |
|-------------|-----------|
| `FROM node:20-alpine` | Chỉ định base image |
| `WORKDIR /app` | Đặt thư mục làm việc |
| `COPY package*.json ./` | Copy file dependency |
| `RUN npm install` | Chạy lệnh trong quá trình build |
| `COPY . .` | Copy toàn bộ source code |
| `EXPOSE 3000` | Khai báo port (không publish) |
| `ENV NODE_ENV=production` | Đặt biến môi trường |
| `ARG VERSION=1.0` | Tham số build-time |
| `VOLUME ["/data"]` | Khai báo điểm mount volume |
| `USER node` | Chuyển sang non-root user |
| `CMD ["node", "server.js"]` | Lệnh mặc định (có thể override) |
| `ENTRYPOINT ["node"]` | Entrypoint cố định |
| `HEALTHCHECK --interval=30s CMD curl -f http://localhost/ \|\| exit 1` | Kiểm tra sức khỏe container |

> **CMD vs ENTRYPOINT:** `ENTRYPOINT` đặt executable; `CMD` cung cấp tham số mặc định. Khi cả hai được đặt, các tham số `CMD` được truyền vào `ENTRYPOINT`.

---

## 🏪 Registry & Docker Hub

| Lệnh | Chức Năng |
|------|-----------|
| `docker login` | Đăng nhập Docker Hub |
| `docker login <registry-url>` | Đăng nhập private registry |
| `docker logout` | Đăng xuất |
| `docker tag <image> <user>/<repo>:<tag>` | Tag một image |
| `docker push <user>/<repo>:<tag>` | Push lên registry |
| `docker pull <user>/<repo>:<tag>` | Pull từ registry |

---

## 🧹 System & Cleanup

### Disk Usage

| Lệnh | Chức Năng |
|------|-----------|
| `docker system df` | Xem dung lượng disk đang dùng |
| `docker system prune` | Xóa tất cả dữ liệu không dùng |
| `docker system prune -a` | Xóa tất cả dữ liệu không dùng (kể cả images) |
| `docker system prune -a --volumes` | Xóa tất cả kể cả volumes |

### Individual Pruning

| Lệnh | Chức Năng |
|------|-----------|
| `docker container prune` | Xóa container đã dừng |
| `docker image prune -a` | Xóa image không dùng |
| `docker volume prune` | Xóa volume không dùng |
| `docker network prune` | Xóa network không dùng |

---

## 💡 Useful Tips & Tricks

| Lệnh | Chức Năng |
|------|-----------|
| `docker inspect -f '{{range.NetworkSettings.Networks}}{{.IPAddress}}{{end}}' <container>` | Lấy IP address của container |
| `docker run --rm -it ubuntu bash` | Chạy lệnh một lần và tự xóa |
| `docker export <container> > backup.tar` | Export container thành file tar |
| `docker import backup.tar <image-name>` | Import container từ file tar |
| `docker save -o myimage.tar <image>` | Lưu image thành file tar |
| `docker load -i myimage.tar` | Load image từ file tar |
| `docker history <image>` | Xem các layer của image |
| `docker logs -f --timestamps <container>` | Theo dõi logs kèm timestamp |
| `docker run --memory="512m" --cpus="1.5" <image>` | Giới hạn tài nguyên container |

---

## 🏷️ Common Flags Reference

| Flag | Mô Tả |
|------|--------|
| `-d` | Chế độ nền (detached) |
| `-it` | Interactive + pseudo-TTY |
| `-p host:container` | Map port |
| `-v host:container` | Volume / bind mount |
| `-e KEY=VAL` | Biến môi trường |
| `--name` | Đặt tên container |
| `--rm` | Xóa container sau khi thoát |
| `--network` | Kết nối vào một network |
| `--restart` | Restart policy (`always`, `unless-stopped`, `on-failure`) |
| `--memory` | Giới hạn bộ nhớ (vd: `512m`) |
| `--cpus` | Giới hạn CPU (vd: `1.5`) |
| `--user` | Đặt user (vd: `1000:1000`) |
