🛠 Công nghệ sử dụng (Tech Stack)
Dự án sử dụng mô hình PERN Stack:
- Frontend: React.js + Vite + Tailwind CSS
- Backend: Node.js + Express.js
- Cơ sở dữ liệu: PostgreSQL
- Giao tiếp API: Axios
  
✨ Chức năng chính
Hệ thống phân quyền người dùng thành 3 vai trò: Admin, Giáo viên (Teacher), và Học sinh (Student).
1. Quản trị viên (Admin)
- Quản lý người dùng (Thêm, sửa, xóa, phân quyền).
- Quản lý lớp học (Tạo lớp, phân công giáo viên chủ nhiệm).
- Quản lý môn học (Tạo môn, cấu hình hệ số điểm).
- Quản lý danh sách học sinh.
  
2. Giáo viên (Teacher)
- Giáo viên bộ môn: Xem danh sách lớp dạy, nhập/sửa/xóa điểm các đầu điểm (TX, GK, CK) cho môn mình dạy.
- Giáo viên chủ nhiệm: Xem danh sách lớp chủ nhiệm, xem bảng điểm tổng hợp, xem xếp loại học lực của học sinh trong lớp.

3. Học sinh (Student)
- Xem điểm chi tiết các môn học theo kỳ.
- Xem điểm trung bình môn và trung bình toàn kỳ.
- Xem xếp loại học lực cá nhân.

⚙️ Yêu cầu môi trường (Prerequisites)
Để chạy được dự án, máy tính cần cài đặt:
- Node.js: Phiên bản 18.x hoặc cao hơn.
- PostgreSQL: Phiên bản 17.x hoặc cao hơn.
- Package Manager: npm (9.x+) hoặc yarn.
- Công cụ quản lý DB: pgAdmin4.

📂 Cấu trúc thư mục
project-root/
├── be/                 # Backend (Node.js + Express)
│   ├── controllers/    # Xử lý logic nghiệp vụ (Auth, Score, Class,...)
│   ├── routes/         # Định nghĩa API endpoints
│   ├── middleware/     # Xác thực (Auth middleware)
│   ├── db/             # Kết nối Database
│   ├── .env            # Biến môi trường
│   └── server.js       # Entry point
│
├── fe/                 # Frontend (React + Vite)
│   ├── src/
│   │   ├── components/ # Components tái sử dụng
│   │   ├── pages/      # Các trang giao diện
│   │   └── ...
│   ├── package.json
│   └── vite.config.js
│
└── db.backup           # File backup cơ sở dữ liệu
