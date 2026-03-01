# 🍽️ BÀI TẬP BACKEND – HỆ THỐNG QUẢN LÝ NHÀ HÀNG

## 🎯 Mục tiêu

Xây dựng **Backend cho hệ thống quản lý nhà hàng**.

Sinh viên có thể lựa chọn:

- Xây dựng theo mô hình **API (RESTful API)** Hoặc mô hình **MVC (Model – View – Controller)**
- Sử dụng **bất kỳ ngôn ngữ hoặc framework nào**
- Bắt buộc **kết nối và thao tác với Database**

---

## 🛠 Công nghệ được phép sử dụng

Sinh viên được tự do lựa chọn:

- NodeJS (Express, NestJS, ...)
- PHP (Laravel, CodeIgniter, ...)
- Java (Spring Boot)
- .NET (ASP.NET Core)
- Python (Django, FastAPI)
- Ruby on Rails
- Hoặc bất kỳ công nghệ backend nào khác

Database có thể sử dụng:

- MySQL
- PostgreSQL
- SQL Server
- MongoDB
- SQLite
- Hoặc hệ quản trị CSDL khác

---

# 📦 YÊU CẦU CHỨC NĂNG

## 1️⃣ Quản lý Món Ăn (Food Management)

Thực hiện đầy đủ CRUD:

- ✅ Tạo món ăn mới
- ✅ Xem danh sách món ăn
- ✅ Xem chi tiết món ăn
- ✅ Cập nhật thông tin món ăn
- ✅ Xóa món ăn

### Gợi ý cấu trúc bảng:

| Field        | Kiểu dữ liệu |
|--------------|--------------|
| id           | int / uuid   |
| name         | string       |
| price        | decimal      |
| description  | text         |
| status       | boolean      |
| created_at   | datetime     |

---

## 2️⃣ Quản lý Bàn (Table Management)

Thực hiện đầy đủ CRUD:

- ✅ Tạo bàn mới
- ✅ Xem danh sách bàn
- ✅ Cập nhật trạng thái bàn (Trống / Đang sử dụng)
- ✅ Xóa bàn

### Gợi ý cấu trúc bảng:

| Field      | Kiểu dữ liệu |
|------------|--------------|
| id         | int / uuid   |
| table_name | string       |
| capacity   | int          |
| status     | enum         |
| created_at | datetime     |

---

## 3️⃣ Đặt Món / Order (Chức năng nâng cao)

### Yêu cầu cơ bản:

- Tạo đơn đặt món
- Một bàn có thể đặt nhiều món
- Một đơn hàng có nhiều món ăn
- Tính tổng tiền tự động

### Gợi ý cấu trúc:

#### Bảng orders

| Field      | Kiểu dữ liệu |
|------------|--------------|
| id         | int / uuid   |
| table_id   | foreign key  |
| total      | decimal      |
| status     | enum         |
| created_at | datetime     |

#### Bảng order_items

| Field     | Kiểu dữ liệu |
|-----------|--------------|
| id        | int / uuid   |
| order_id  | foreign key  |
| food_id   | foreign key  |
| quantity  | int          |
| price     | decimal      |

---

# 🚀 YÊU CẦU KỸ THUẬT

- Bắt buộc sử dụng Database
- Có quan hệ giữa các bảng (relationship)
- Áp dụng validation dữ liệu đầu vào
- Xử lý lỗi hợp lý (error handling)
- Cấu trúc project rõ ràng
- Code dễ đọc, dễ bảo trì

---

# 📌 YÊU CẦU NÂNG CAO (Khuyến khích)

- Phân trang (pagination)
- Tìm kiếm món ăn
- Lọc theo giá
- Soft delete
- API trả về đúng chuẩn HTTP Status Code
