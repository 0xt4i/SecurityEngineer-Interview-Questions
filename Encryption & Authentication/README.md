# Encryption & Authentication

---

## Beginner Level (Cơ bản)

### 1. What is a three-way handshake?
**EN:**  
A three-way handshake is a process used in TCP/IP networks to establish a reliable connection between a client and a server.  
It involves three steps:  
- SYN: The client sends a SYN (synchronize) packet to the server.  
- SYN-ACK: The server responds with a SYN-ACK packet.  
- ACK: The client sends an ACK (acknowledgment) packet back to the server.  
After these steps, the connection is established.

**VI:**  
Bắt tay ba bước (three-way handshake) là quá trình dùng trong mạng TCP/IP để thiết lập kết nối đáng tin cậy giữa client và server, gồm:  
- SYN: Client gửi gói SYN (đồng bộ) tới server.  
- SYN-ACK: Server phản hồi bằng gói SYN-ACK.  
- ACK: Client gửi gói ACK (xác nhận) lại cho server.  
Sau ba bước này, kết nối được thiết lập.
---

### 1.1 Explain the OSI and TCP/IP models.
*(Giải thích mô hình OSI và TCP/IP.)*

**EN:**  
The OSI (Open Systems Interconnection) model is a 7-layer theoretical framework that standardizes network communication:  
1. **Physical:** Transmits bits over the physical medium.  
2. **Data Link:** Ensures reliable link-to-link communication (MAC, error detection).  
3. **Network:** Provides logical addressing and routing (IP).  
4. **Transport:** Ensures reliable end-to-end delivery (TCP/UDP).  
5. **Session:** Manages sessions and connections.  
6. **Presentation:** Translates and formats data (encryption, encoding).  
7. **Application:** Interfaces with user applications (HTTP, FTP, SMTP).  

The TCP/IP model is a 4-layer practical model used on the Internet:  
- **Network Interface:** Combines OSI’s Physical + Data Link.  
- **Internet:** Equivalent to OSI’s Network.  
- **Transport:** Same as OSI’s Transport.  
- **Application:** Combines OSI’s Session, Presentation, Application.  

TCP/IP is simpler and widely implemented, while OSI is used for conceptual understanding.

**VI:**  
Mô hình **OSI** (Open Systems Interconnection) là mô hình lý thuyết gồm 7 tầng chuẩn hóa giao tiếp mạng:  
1. **Vật lý:** Truyền bit qua môi trường vật lý.  
2. **Liên kết dữ liệu:** Đảm bảo liên kết đáng tin cậy giữa 2 nút (MAC, phát hiện lỗi).  
3. **Mạng:** Định địa chỉ và định tuyến logic (IP).  
4. **Giao vận:** Đảm bảo truyền dữ liệu tin cậy đầu-cuối (TCP/UDP).  
5. **Phiên:** Quản lý các phiên kết nối.  
6. **Trình diễn:** Dịch và định dạng dữ liệu (mã hóa, giải mã).  
7. **Ứng dụng:** Giao diện với ứng dụng người dùng (HTTP, FTP, SMTP).  

Mô hình **TCP/IP** là mô hình thực tế với 4 tầng, được dùng rộng rãi trên Internet:  
- **Giao diện mạng:** Gộp tầng Vật lý + Liên kết dữ liệu của OSI.  
- **Internet:** Tương ứng tầng Mạng của OSI.  
- **Giao vận:** Giống tầng Giao vận OSI.  
- **Ứng dụng:** Gộp các tầng Phiên, Trình diễn, Ứng dụng của OSI.  

TCP/IP đơn giản hơn và được triển khai thực tế, OSI chủ yếu để lý giải khái niệm.

---

### 1.2 What are common TCP/IP attacks and defenses?
*(Các kiểu tấn công TCP/IP thường gặp và cách phòng thủ.)*

**EN:**  
Common TCP/IP attacks include:  
- **IP Spoofing:** Attacker forges source IP address to impersonate another host.  
- **TCP SYN Flood (DoS):** Attacker floods server with SYN packets to exhaust resources.  
- **Man-in-the-Middle (MITM):** Attacker intercepts and alters traffic between two parties.  
- **Packet Sniffing:** Attacker eavesdrops on unencrypted traffic.  
- **ICMP Flood/Smurf Attack:** Overloads the target with ICMP Echo requests.  

Defenses include:  
- Packet filtering firewalls and access control lists (ACLs).  
- SYN cookies and connection rate limiting.  
- Encryption (TLS/SSL, VPN) to prevent sniffing and MITM.  
- Intrusion Detection/Prevention Systems (IDS/IPS).  
- Disabling unused protocols/services and hardening configurations.

**VI:**  
Các kiểu tấn công **TCP/IP** thường gặp:  
- **Giả mạo IP (IP Spoofing):** Kẻ tấn công giả địa chỉ IP nguồn để mạo danh máy khác.  
- **TCP SYN Flood (DoS):** Gửi hàng loạt gói SYN làm cạn tài nguyên máy chủ.  
- **Man-in-the-Middle (MITM):** Chặn và thay đổi dữ liệu giữa 2 bên giao tiếp.  
- **Nghe trộm (Packet Sniffing):** Theo dõi lưu lượng chưa mã hóa.  
- **ICMP Flood/Smurf:** Dội hàng loạt gói ICMP làm nghẽn máy đích.  

Các biện pháp phòng thủ:  
- Dùng tường lửa lọc gói và ACL để chặn gói bất thường.  
- Áp dụng SYN cookies và giới hạn tốc độ kết nối.  
- Mã hóa (TLS/SSL, VPN) để chống nghe trộm và MITM.  
- Triển khai IDS/IPS để phát hiện/ngăn chặn xâm nhập.  
- Vô hiệu hóa dịch vụ/giao thức không dùng và cấu hình bảo mật chặt chẽ.

---

### 2. How do cookies work?
**EN:**  
Cookies are small pieces of data stored by a web browser at the request of a web server.  
They help track user sessions, store preferences, and authenticate users by sending the cookie with each request to the server.

**VI:**  
Cookie là các mẩu dữ liệu nhỏ được trình duyệt lưu lại theo yêu cầu của web server.  
Chúng giúp theo dõi phiên làm việc, lưu tùy chọn và xác thực người dùng bằng cách gửi cookie mỗi khi có request lên server.

---

### 3. How do sessions work?
**EN:**  
A session maintains state between a client and server across multiple requests.  
When a user logs in, the server creates a session and stores data (like user ID) on the server.  
The client receives a session ID, often via a cookie, and sends it with each request to identify themselves.

**VI:**  
Session là cách duy trì trạng thái giữa client và server qua nhiều request.  
Khi người dùng đăng nhập, server tạo session và lưu thông tin (ví dụ user ID) trên server, còn client nhận session ID (thường qua cookie) và gửi kèm mỗi request để xác định người dùng.

---

### 4. What is the difference between authentication vs authorization name spaces?
**EN:**  
Authentication is the process of verifying who a user is.  
Authorization determines what an authenticated user is allowed to do.

**VI:**  
Authentication (xác thực) là kiểm tra danh tính người dùng.  
Authorization (phân quyền) là xác định người dùng đã xác thực được phép làm gì.

---

### 5. Should you encrypt all data at rest?
**EN:**  
Ideally, yes. Encrypting all data at rest helps protect sensitive information from unauthorized access in case of physical theft or data breach.

**VI:**  
Lý tưởng nhất là nên mã hóa toàn bộ dữ liệu lưu trữ. Việc này giúp bảo vệ dữ liệu nhạy cảm khỏi truy cập trái phép khi bị đánh cắp thiết bị hoặc lộ dữ liệu.

---

## Intermediate Level (Trung bình)

### 6. Explain how OAuth works.
**EN:**  
OAuth is an open standard for access delegation.  
It allows users to grant a third-party app access to their resources without sharing passwords.  
The user authorizes the app, which gets an access token from the identity provider, then uses this token to access resources on the user's behalf.

**VI:**  
OAuth là chuẩn mở cho phép ủy quyền truy cập.  
Người dùng cho phép ứng dụng bên thứ ba truy cập tài nguyên mà không phải chia sẻ mật khẩu.  
Ứng dụng được cấp access token từ nhà cung cấp, dùng token này truy cập tài nguyên thay mặt người dùng.

---

### 7. Explain how JWT works.
**EN:**  
JWT (JSON Web Token) is a compact, URL-safe token containing claims between two parties.  
It has a header, payload, and signature. After authentication, the server sends a JWT to the client, who includes it with each request.  
The server verifies the signature to authenticate the user.

**VI:**  
JWT (JSON Web Token) là chuẩn mã hóa nhỏ gọn, an toàn, truyền các thông tin xác thực giữa hai bên.  
JWT gồm 3 phần: header, payload, signature. Sau xác thực, server gửi JWT cho client, client gửi kèm JWT mỗi request, server xác thực chữ ký để nhận diện người dùng.

---

### 8. What is a public key infrastructure flow and how would I diagram it?
**EN:**  
Public Key Infrastructure (PKI) is a framework for managing digital certificates and public-private key pairs.
- Certificate Authority (CA) issues a digital certificate to a user or server after verifying identity.
- The user/server presents the certificate to others to prove their identity.
- Others use the CA's public key to verify the certificate's authenticity.

**VI:**  
Hạ tầng khóa công khai (PKI) là hệ thống quản lý chứng chỉ số và cặp khóa công khai/riêng.
- CA (tổ chức chứng thực) cấp chứng chỉ cho user/server sau khi xác minh danh tính.
- User/server trình chứng chỉ để xác thực với bên khác.
- Bên nhận dùng khóa công khai của CA để xác thực chứng chỉ.

---

### 9. Describe the difference between synchronous and asynchronous encryption.
**EN:**  
Synchronous encryption typically means symmetric encryption, where the same key is used for both encryption and decryption.  
Asynchronous encryption refers to asymmetric encryption, where a public key encrypts and a private key decrypts.

**VI:**  
Mã hóa đồng bộ thường ám chỉ mã hóa đối xứng (dùng cùng 1 khóa để mã hóa và giải mã).  
Mã hóa bất đồng bộ là mã hóa bất đối xứng, dùng khóa công khai để mã hóa và khóa riêng để giải mã.

---

### 10. Describe SSL handshake.
**EN:**  
The SSL handshake is the process where a client and server establish an encrypted connection. It includes:
- Negotiating protocol version and cipher suite.
- Exchanging certificates.
- Generating session keys for encryption.
After the handshake, all data is transmitted securely.

**VI:**  
SSL handshake là quá trình client và server thiết lập kết nối mã hóa:
- Thỏa thuận phiên bản giao thức và bộ mã hóa.
- Trao đổi chứng chỉ.
- Sinh khóa phiên để mã hóa dữ liệu.
Sau handshake, dữ liệu truyền được bảo mật.

---

### 11. How does HMAC work?
**EN:**  
HMAC (Hash-based Message Authentication Code) combines a secret key with a hash function to ensure both data integrity and authenticity.  
The sender creates a hash of the message plus the secret key and sends both to the receiver, who computes the hash and checks if they match.

**VI:**  
HMAC (mã xác thực thông điệp dựa trên hàm băm) kết hợp khóa bí mật với hàm băm để đảm bảo toàn vẹn và xác thực dữ liệu.  
Người gửi tạo một mã băm từ thông điệp và khóa bí mật, gửi cho người nhận. Người nhận dùng cùng khóa tính lại mã băm để đối chiếu.

---

### 12. Why HMAC is designed in that way?
**EN:**  
HMAC is designed to resist certain attacks on plain hash functions, like length extension attacks, by mixing the secret key with the message in a specific way.  
This ensures that only someone with the secret key can generate a valid HMAC.

**VI:**  
HMAC được thiết kế để chống lại các tấn công vào hàm băm thông thường, như tấn công kéo dài độ dài (length extension), bằng cách kết hợp khóa bí mật với thông điệp theo cách đặc biệt.  
Nhờ đó, chỉ ai biết khóa bí mật mới tạo được HMAC hợp lệ.

---

### 13. What’s the difference between Diffie-Hellman and RSA?
**EN:**  
Diffie-Hellman is a key exchange protocol, mainly used to securely generate a shared secret over an insecure channel.  
RSA is an asymmetric encryption algorithm, used for both encryption and digital signatures.

**VI:**  
Diffie-Hellman là giao thức trao đổi khóa, giúp hai bên tạo ra khóa chung qua kênh không an toàn.  
RSA là thuật toán mã hóa bất đối xứng, dùng để mã hóa dữ liệu hoặc ký số.

---

### 14. If you're going to compress and encrypt a file, which do you do first and why?
**EN:**  
You should compress the file first, then encrypt it. Encryption removes patterns in the data, making compression much less effective afterward.

**VI:**  
Nên nén file trước, rồi mới mã hóa. Vì mã hóa làm mất các mẫu lặp trong dữ liệu, nếu nén sau sẽ kém hiệu quả.

---

### 15. How do I authenticate you and know you sent the message?
**EN:**  
You can use digital signatures. I sign the message with my private key, and you verify it with my public key. If verification succeeds, you know I sent it.

**VI:**  
Có thể dùng chữ ký số. Tôi ký thông điệp bằng khóa riêng, bạn xác minh bằng khóa công khai của tôi. Nếu xác thực thành công, bạn biết tôi là người gửi.

---

## Advanced Level (Nâng cao)

### 16. How does Kerberos work?
**EN:**  
Kerberos is a network authentication protocol that uses tickets to allow nodes to prove their identity securely.  
Users authenticate to a Key Distribution Center (KDC), receive a Ticket Granting Ticket (TGT), and use it to request service tickets for access to network resources.

**VI:**  
Kerberos là giao thức xác thực mạng dùng vé (ticket) để các máy chủ xác minh danh tính an toàn.  
Người dùng xác thực với Trung tâm phân phối khóa (KDC), nhận vé TGT, rồi dùng vé này để xin các vé dịch vụ truy cập tài nguyên mạng.

---

### 17. What is Perfect Forward Secrecy?
**EN:**  
Perfect Forward Secrecy (PFS) is a feature of key agreement protocols that ensures a session key cannot be compromised even if the private key of the server is compromised in the future.

**VI:**  
Perfect Forward Secrecy (PFS) là tính năng của các giao thức trao đổi khóa, đảm bảo rằng khóa phiên không bị lộ dù sau này khóa riêng của server bị lộ.

---
