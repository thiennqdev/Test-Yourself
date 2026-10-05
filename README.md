# TestYourself - Online Quiz & Flashcard Learning Platform

Dự án kiểm tra kiến thức trực tuyến với React Frontend và Flask Backend.

---

## 🚀 Khởi chạy nhanh bằng Docker Compose (Khuyên dùng cho Demo)

Chỉ cần cài đặt [Docker Desktop](https://www.docker.com/products/docker-desktop/) và thực hiện đúng 1 lệnh duy nhất:

```bash
docker compose up --build
```

Sau khi các container khởi động thành công:
- **Frontend**: [http://localhost:5173](http://localhost:5173)
- **Backend API**: [http://localhost:5000](http://localhost:5000)

### 🔑 Tài khoản mặc định hệ thống:
- **Tài khoản Quản trị viên (Admin)**:
  - Username: `admin`
  - Password: `admin123`
- **Tài khoản Người dùng (User)**:
  - Có thể đăng ký tài khoản mới trực tiếp tại trang [http://localhost:5173/register](http://localhost:5173/register).

### 🛑 Dừng hệ thống:
```bash
docker compose down
```

*(Dữ liệu khóa học, câu hỏi, điểm thi và file ảnh upload sẽ được lưu an toàn trong Docker Volumes `testyourself-backend-data` và `testyourself-backend-uploads`)*.

---

## 🛠️ Cấu trúc thư mục

```
Test Yourself/
├── testyourself-backend/     # Flask API, SQLAlchemy, SQLite/MySQL
│   ├── Dockerfile
│   ├── app/
│   └── run.py
├── testyourself-frontend/    # React 19, Vite, Tailwind CSS
│   ├── Dockerfile
│   ├── nginx.conf
│   └── src/
├── docker-compose.yml        # Điều phối cả Backend và Frontend
└── README.md
```
