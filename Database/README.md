# Databases Security 

---

## Beginner Level (Cơ bản)

### 1. What are the 6 aggregate functions of SQL?

**EN:**  
The six common aggregate functions in SQL are:
- `COUNT()`: Counts the number of rows.
- `SUM()`: Calculates the total sum of a column.
- `AVG()`: Calculates the average value.
- `MIN()`: Finds the minimum value.
- `MAX()`: Finds the maximum value.
- `GROUP_CONCAT()` (or `STRING_AGG()` in Postgres): Concatenates values from multiple rows into a single string (may vary by DB).

**VI:**  
Sáu hàm tổng hợp phổ biến trong SQL là:
- `COUNT()`: Đếm số dòng.
- `SUM()`: Tính tổng các giá trị của một cột.
- `AVG()`: Tính giá trị trung bình.
- `MIN()`: Tìm giá trị nhỏ nhất.
- `MAX()`: Tìm giá trị lớn nhất.
- `GROUP_CONCAT()` (hoặc `STRING_AGG()` trong Postgres): Nối các giá trị từ nhiều dòng thành một chuỗi (tùy hệ quản trị CSDL).

---

## Intermediate Level (Trung bình)

### 2. How would you secure a Mongo database?

**EN:**  
- Enable authentication and enforce strong passwords.
- Restrict network access using firewalls/VPCs (bind only to localhost or trusted IPs).
- Use TLS/SSL for encrypted connections.
- Regularly update MongoDB to latest versions.
- Backup data securely and monitor logs.

**VI:**  
- Bật xác thực và sử dụng mật khẩu mạnh.
- Giới hạn truy cập mạng bằng tường lửa/VPC (chỉ cho phép localhost hoặc IP tin cậy).
- Sử dụng TLS/SSL để mã hóa kết nối.
- Thường xuyên cập nhật MongoDB lên bản mới nhất.
- Sao lưu dữ liệu an toàn và giám sát nhật ký hệ thống.

---

### 3. How would you secure Postgres?

**EN:**  
- Enforce strong authentication and password policies.
- Restrict network access via `pg_hba.conf` and firewall.
- Use SSL/TLS for encrypted communication.
- Apply role-based access control (GRANT/REVOKE).
- Keep PostgreSQL updated and monitor logs/audits.

**VI:**  
- Áp dụng chính sách xác thực mạnh và mật khẩu phức tạp.
- Giới hạn truy cập qua `pg_hba.conf` và tường lửa.
- Bật SSL/TLS cho kết nối an toàn.
- Phân quyền truy cập bằng GRANT/REVOKE.
- Luôn cập nhật PostgreSQL và giám sát nhật ký/an ninh.

---

## Advanced Level (Nâng cao)

### 4. Our DB was stolen/exfiltrated. It was secured with one round of sha256 with a static salt. What do we do now? Are we at risk? What do we change?

**EN:**  
- **Are we at risk?**  
  Yes, using a single round of sha256 with a static salt is weak. Attackers can perform offline brute-force or use rainbow tables, especially if passwords are simple or reused.
- **What do we do now?**  
  - Immediately force a password reset for all users.
  - Monitor for suspicious logins or credential stuffing attacks.
  - Inform users and relevant authorities if necessary.
- **What do we change?**  
  - Switch to a stronger password hashing algorithm (e.g., bcrypt, Argon2, PBKDF2) with a unique salt per password.
  - Consider adding multi-factor authentication (MFA).
  - Review and enhance overall security practices.

**VI:**  
- **Chúng ta có gặp rủi ro không?**  
  Có. Dùng sha256 với một salt tĩnh rất yếu, dễ bị brute-force hoặc rainbow table nếu mật khẩu đơn giản hoặc bị lộ nơi khác.
- **Giờ nên làm gì?**  
  - Bắt buộc tất cả người dùng đổi mật khẩu ngay lập tức.
  - Theo dõi các đăng nhập bất thường hoặc tấn công nhồi thông tin (credential stuffing).
  - Thông báo cho người dùng và cơ quan quản lý nếu cần thiết.
- **Cần thay đổi gì?**  
  - Chuyển sang thuật toán băm mạnh hơn (bcrypt, Argon2, PBKDF2) với salt riêng cho từng mật khẩu.
  - Cân nhắc bổ sung xác thực đa yếu tố (MFA).
  - Rà soát và nâng cấp toàn diện chính sách bảo mật.

---
