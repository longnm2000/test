# TD.TaskManager - Hướng dẫn cài đặt

## 1. Yêu cầu môi trường

* **.NET SDK 10.0+**
* **Node.js v20+**
* **Yarn v1.22+** (không phải Yarn v2) **hoặc** **npm v10+**
* **SQL Server**
---

## 2. Các bước cài đặt

### **Bước 1: Clone dự án**

Mở terminal và chạy:

```bash
git clone https://github.com/longnm2000/TD.TaskManager
cd TD.TaskManager
```

---

### **Bước 2: Cấu hình kết nối Database**

Mở file:

* `TD.TaskManager.HttpApi.Host/appsettings.json`
* `TD.TaskManager.DbMigrator/appsettings.json`

tìm mục `ConnectionStrings` và sửa lại theo server của bạn:

```json
"ConnectionStrings": {
    "Default": "Server=localhost;Database=[Tên_DB];Trusted_Connection=True;TrustServerCertificate=True"
}
```

---

### **Bước 3: Khởi tạo database**

Trong terminal, di chuyển đến thư mục DbMigrator:

```bash
cd TD.TaskManager.DbMigrator
dotnet run
```

---

### **Bước 4: Chạy Backend (.NET API)**

```bash
cd ../TD.TaskManager.HttpApi.Host
dotnet build
dotnet run
```

Sau khi chạy, mở trình duyệt truy cập:

```
https://localhost:44377
```

---

### **Bước 5: Cài đặt dependencies cho Angular**

```bash
cd ../angular
npm install --legacy-peer-deps
```

---

### **Bước 6: Khởi động giao diện Angular**

```bash
npm start
# hoặc
yarn start
```

Sau đó mở trình duyệt truy cập:

```
http://localhost:4200
```

---

### **Bước 7: Đăng nhập hệ thống**

Tại trang đăng nhập, sử dụng tài khoản mặc định:

* **Tài khoản:** `admin`
* **Mật khẩu:** `1q2w3E*`

---

Chúc bạn cài đặt và chạy hệ thống thành công!
