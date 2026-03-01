# 📚 HƯỚNG DẪN NỘP BÀI TẬP – GIT WORKFLOW

Repository này được sử dụng để sinh viên nộp bài tập.

Tất cả sinh viên **bắt buộc tuân theo quy trình Git dưới đây** để đảm bảo cấu trúc rõ ràng và dễ dàng review.

---

## 🌿 Quy tắc về Branch

- `main` → Nhánh chính (chỉ chứa code đã được duyệt)
- Mỗi sinh viên phải tạo **1 branch riêng**
- Không được commit trực tiếp vào `main`

### 📌 Quy tắc đặt tên branch
```
student/<khoa-hoc>-<ho-ten-khong-dau>
```

### Ví dụ:
```
student/k63-nguyen-van-a
student/k64-tran-thi-b
```

---

## 📁 Cấu trúc thư mục

Trong branch của mình, sinh viên phải tạo thư mục riêng theo cấu trúc:
```
/<khoa-hoc>-<ho-ten-khong-dau>/
```


⚠️ Tất cả code bài tập phải đặt bên trong thư mục của mình.
⚠️ Không chỉnh sửa code của sinh viên khác.

---

## 🚀 Các bước nộp bài

### 1️⃣ Clone repository

```bash
git clone <repository-url>
cd <repository-name>
```

### 2️⃣ Tạo branch riêng
```bash
git checkout -b student/<khoa-hoc>-<ho-ten-khong-dau>
```
Ví dụ:
```bash
git checkout -b student/k64-tran-thi-b
```

### 3️⃣ Tạo thư mục của mình
```bash
mkdir -p /tran-thi-b
```

### 4️⃣ Thêm code vào thư mục
Đặt toàn bộ file bài tập vào: `/tran-thi-b`

### 5️⃣ Commit và Push lên Git
```bash
git add .
git commit -m "Submit assignment"
git push
```

### 6️⃣ Tạo Pull Request
- Vào repository trên GitHub/GitLab
- Chọn Create Pull Request
- Merge từ branch của bạn vào main
- Chờ giảng viên review

## ❌ Lưu ý quan trọng
- Không commit trực tiếp vào main
- Không sửa bài của người khác
- Không đổi cấu trúc thư mục
- Pull Request không đúng format sẽ bị từ chối

## ✅ Quy trình chuẩn
```
Clone → Tạo branch → Tạo folder → Code → Commit → Push → Tạo Pull Request → Review → Merge vào main
```

---

# 📖 Tài liệu học Git tham khảo

Để hiểu rõ hơn về Git, Branch, Merge và Pull Request, sinh viên nên tham khảo thêm các tài liệu sau:

- 🎥 Video hướng dẫn cơ bản về git: https://www.youtube.com/watch?v=cC7vg8lWneo
- 🎥 Video hướng dẫn Git tiếng Việt trên YouTube: https://www.youtube.com/watch?v=O5uT6p6VWjY

💡 Khuyến khích:
- Tự thực hành tạo branch, merge thử trên repository cá nhân.
- Thử tạo conflict và học cách resolve.
- Đọc hiểu commit history để làm việc nhóm hiệu quả hơn.

Việc thành thạo Git là kỹ năng bắt buộc trong môi trường làm việc thực tế.