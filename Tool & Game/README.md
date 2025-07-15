# Tools and Games

---

## Beginner Level (Cơ bản)

### 1. Have I played CTF?

**EN:**  
CTF (Capture The Flag) are cybersecurity competitions involving solving challenges in reverse engineering, web security, cryptography, forensics, etc. Playing CTFs demonstrates hands-on security skills and problem-solving.

**VI:**  
CTF (Capture The Flag) là các cuộc thi an ninh mạng gồm các thử thách về dịch ngược, web, mã hóa, phân tích số liệu, v.v. Tham gia CTF giúp rèn luyện kỹ năng thực chiến về bảo mật và giải quyết vấn đề.

---

### 2. Would you decrypt a steganography image?

**EN:**  
Yes, if authorized. Decrypting a steganography image involves using tools or techniques to extract hidden data (e.g., using `steghide`, `zsteg`, or manual analysis with hex editors).

**VI:**  
Có, nếu được phép. Giải mã ảnh steganography là dùng công cụ hoặc kỹ thuật để tìm dữ liệu ẩn (ví dụ: dùng `steghide`, `zsteg` hoặc phân tích thủ công bằng hex editor).

---

### 3. What technical skill or project are you working on for fun in your free time?

**EN:**  
Examples include building a home lab, writing security scripts, creating CTF challenges, learning a new programming language, or contributing to open-source security tools.

**VI:**  
Ví dụ: xây dựng lab tại nhà, viết script bảo mật, tạo thử thách CTF, học ngôn ngữ lập trình mới, hoặc đóng góp cho dự án mã nguồn mở về an ninh.

---

## Intermediate Level (Trung bình)

### 4. You're given an ip-based phone and asked me to decrypt the message in the phone.

**EN:**  
I would:
- Analyze the firmware or software of the phone for vulnerabilities.
- Intercept network traffic (with permission) to extract the encrypted message.
- Try default credentials, look for known exploits, or extract storage for analysis.
- Use forensic tools if physical access is available.

**VI:**  
Tôi sẽ:
- Phân tích firmware/phần mềm của điện thoại để tìm lỗ hổng.
- Chặn lưu lượng mạng (nếu được phép) để lấy thông điệp mã hóa.
- Thử mật khẩu mặc định, tìm khai thác đã biết, hoặc trích xuất bộ nhớ để phân tích.
- Dùng công cụ pháp y nếu có quyền truy cập vật lý.

---

### 5. What CND tools do you knowledge or experience with?

**EN:**  
Common CND (Computer Network Defense) tools:
- IDS/IPS: Snort, Suricata
- SIEM: Splunk, ELK stack
- Network monitoring: Wireshark, Zeek (Bro)
- Firewalls: pfSense, iptables
- Vulnerability scanners: Nessus, OpenVAS

**VI:**  
Các công cụ CND (Bảo vệ mạng máy tính) phổ biến:
- IDS/IPS: Snort, Suricata
- SIEM: Splunk, ELK stack
- Giám sát mạng: Wireshark, Zeek (Bro)
- Tường lửa: pfSense, iptables
- Quét lỗ hổng: Nessus, OpenVAS

---

### 6. What is the difference between nmap -sS and nmap -sT?

**EN:**  
- `-sS`: SYN scan (half-open), stealthier, sends SYN packets and listens for response without completing TCP handshake.
- `-sT`: TCP connect scan, completes full TCP handshake, easier to detect, requires OS-level permissions.

**VI:**  
- `-sS`: Quét SYN (nửa mở), khó bị phát hiện, chỉ gửi SYN rồi chờ phản hồi, không bắt tay hoàn chỉnh.
- `-sT`: Quét TCP connect, bắt tay hoàn chỉnh, dễ bị phát hiện hơn, cần quyền cao hơn trên hệ điều hành.

---

### 7. How would you filter xyz in Wireshark?

**EN:**  
Use the display filter bar. For example, to filter HTTP traffic: `http`.  
For IP address: `ip.addr == 192.168.1.1`.  
For specific string (xyz): `frame contains "xyz"`.

**VI:**  
Dùng thanh lọc hiển thị (display filter). Ví dụ để lọc HTTP: `http`.  
Địa chỉ IP: `ip.addr == 192.168.1.1`.  
Tìm chuỗi "xyz": `frame contains "xyz"`.

---

### 8. Given a sample packet capture - Identify the protocol, the traffic, and the likelihood of malicious intent.

**EN:**  
- Check protocol in the Protocol column (e.g., HTTP, DNS, SMB).
- Analyze traffic patterns, look for suspicious or uncommon behavior (e.g., repeated failed logins, large data transfers).
- Use IOC (Indicators of Compromise) and threat intelligence for analysis.
- Assess the context for signs of exfiltration or attack.

**VI:**  
- Kiểm tra cột Protocol (ví dụ: HTTP, DNS, SMB).
- Phân tích mẫu lưu lượng, chú ý hành vi bất thường (nhiều đăng nhập thất bại, truyền dữ liệu lớn).
- Dùng các chỉ báo tấn công (IOC), thông tin tình báo để đánh giá.
- Xem xét bối cảnh để xác định khả năng tấn công hoặc rò rỉ dữ liệu.

---

## Advanced Level (Nâng cao)

### 9. If left alone in office with access to a computer, how would you exploit it?

**EN:**  
(Ethically: Only with authorization)  
- Try privilege escalation (using exploits, misconfigurations).
- Search for plain-text credentials, private keys, or sensitive files.
- Bypass local security controls, use USB boot if BIOS/UEFI allows.
- Deploy reverse shell or persistent access.

**VI:**  
(Chỉ làm nếu có phép)  
- Thử leo thang đặc quyền (dùng lỗi bảo mật, cấu hình sai).
- Tìm kiếm mật khẩu, key cá nhân, file nhạy cảm dạng plain-text.
- Vượt qua kiểm soát bảo mật nội bộ, boot USB nếu BIOS/UEFI cho phép.
- Tạo truy cập ngầm hoặc shell kết nối ngược.

---

### 10. How do you fingerprint an iPhone so you can monitor it even after wiping it?

**EN:**  
- Record hardware identifiers (IMEI, serial number, MAC address).
- Monitor for network activity from known identifiers (e.g., via MDM, DHCP logs).
- Use enterprise management tools to re-enroll device if it reconnects.

**VI:**  
- Ghi lại thông tin phần cứng (IMEI, số serial, MAC address).
- Theo dõi thiết bị qua hoạt động mạng (log DHCP, quản lý thiết bị MDM).
- Dùng giải pháp quản lý doanh nghiệp để tự động nhận diện nếu thiết bị kết nối lại.

---

### 11. How would you use CI/CD to improve security?

**EN:**  
- Integrate security checks (SAST/DAST, dependency scanning) into CI/CD pipeline.
- Use automated vulnerability scanning for code and dependencies.
- Enforce security gates before deployment.
- Regularly update pipeline tools to patch vulnerabilities.

**VI:**  
- Tích hợp kiểm tra bảo mật (SAST/DAST, quét thư viện) vào pipeline CI/CD.
- Tự động quét lỗ hổng mã nguồn và thư viện phụ thuộc.
- Đặt các điều kiện kiểm tra bảo mật trước khi triển khai.
- Luôn cập nhật các công cụ pipeline để vá lỗi bảo mật.

---

### 12. You have a pipeline for Docker images. How would you design everything to ensure the proper security checks?

**EN:**  
- Use trusted base images and keep them updated.
- Scan images for vulnerabilities (e.g., Trivy, Clair) in the CI/CD pipeline.
- Enforce image signing and verification.
- Apply principle of least privilege in Dockerfile.
- Store secrets securely (not in images).

**VI:**  
- Sử dụng image gốc đáng tin cậy, luôn cập nhật.
- Tích hợp quét lỗ hổng (Trivy, Clair) vào pipeline CI/CD.
- Yêu cầu ký và xác thực image.
- Thiết kế Dockerfile theo nguyên tắc đặc quyền tối thiểu.
- Lưu trữ secret an toàn, không để trong image.

---

### 13. How would you create a secret storage system?

**EN:**  
- Use tools like HashiCorp Vault, AWS Secrets Manager, or Azure Key Vault.
- Encrypt secrets at rest and in transit.
- Control access via strong authentication and audit logging.
- Rotate and revoke secrets automatically.

**VI:**  
- Dùng công cụ chuyên biệt như HashiCorp Vault, AWS Secrets Manager, Azure Key Vault.
- Mã hóa secret khi lưu trữ và truyền tải.
- Quản lý truy cập bằng xác thực mạnh, ghi log đầy đủ.
- Tự động xoay vòng, thu hồi secret định kỳ.

---

### 14. How would you harden your work laptop if you needed it at Defcon?

**EN:**  
- Update and patch OS & software.
- Use full disk encryption.
- Disable unused services, ports, Bluetooth, Wi-Fi when not in use.
- Use a non-admin account for daily use.
- Backup data, enable remote wipe if possible.

**VI:**  
- Cập nhật, vá lỗi hệ điều hành và phần mềm.
- Bật mã hóa ổ đĩa toàn phần.
- Tắt dịch vụ, cổng, Bluetooth, Wi-Fi khi không cần.
- Dùng tài khoản không phải admin để sử dụng hàng ngày.
- Sao lưu dữ liệu, bật tính năng xóa từ xa nếu có.

---

### 15. If you had to set up supply chain attack prevention, how would you do that?

**EN:**  
- Verify and validate all third-party dependencies (checksums, signatures).
- Use software composition analysis tools.
- Regularly update dependencies and monitor for vulnerabilities.
- Enforce strict access controls and audit supply chain changes.
- Educate staff about supply chain risks.

**VI:**  
- Xác minh, kiểm tra tất cả thư viện bên ngoài (checksum, chữ ký số).
- Dùng công cụ phân tích thành phần phần mềm (SCA).
- Thường xuyên cập nhật, theo dõi lỗ hổng thư viện.
- Kiểm soát quyền truy cập và audit các thay đổi trong chuỗi cung ứng phần mềm.
- Đào tạo nhân viên về rủi ro chuỗi cung ứng.

---
