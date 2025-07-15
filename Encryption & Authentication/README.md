# Security Engineer Interview Q&A  

---

## Encryption & Authentication Questions

### 1. What is a three-way handshake?
**EN:**  
A three-way handshake is a process used in TCP/IP networks to establish a reliable connection between a client and a server. It involves three steps:  
1. SYN: The client sends a SYN (synchronize) packet to the server.  
2. SYN-ACK: The server responds with a SYN-ACK packet.  
3. ACK: The client sends an ACK (acknowledgment) packet back to the server.  
After these steps, the connection is established.

**VI:**  
Bắt tay ba bước (three-way handshake) là quá trình dùng trong mạng TCP/IP để thiết lập kết nối đáng tin cậy giữa client và server. Gồm 3 bước:  
1. SYN: Client gửi gói SYN (đồng bộ) tới server.  
2. SYN-ACK: Server phản hồi bằng gói SYN-ACK.  
3. ACK: Client gửi gói ACK (xác nhận) lại cho server.  
Sau ba bước này, kết nối được thiết lập.

---

### 2. How do cookies work?
**EN:**  
Cookies are small pieces of data stored by a web browser at the request of a web server. They help track user sessions, store preferences, and authenticate users by sending the cookie with each request to the server.

**VI:**  
Cookie là các mẩu dữ liệu nhỏ được trình duyệt lưu lại theo yêu cầu của web server. Chúng giúp theo dõi phiên làm việc, lưu tùy chọn và xác thực người dùng bằng cách gửi cookie mỗi khi có request lên server.

---

### 3. How do sessions work?
**EN:**  
A session maintains state between a client and server across multiple requests. When a user logs in, the server creates a session and stores data (like user ID) on the server. The client receives a session ID, often via a cookie, and sends it with each request to identify themselves.

**VI:**  
Session là cách duy trì trạng thái giữa client và server qua nhiều request. Khi người dùng đăng nhập, server tạo session và lưu thông tin (ví dụ user ID) trên server, còn client nhận session ID (thường qua cookie) và gửi kèm mỗi request để xác định người dùng.

---

### 11. What is the difference between authentication vs authorization name spaces?
**EN:**  
Authentication is the process of verifying who a user is. Authorization determines what an authenticated user is allowed to do.

**VI:**  
Authentication (xác thực) là kiểm tra danh tính người dùng. Authorization (phân quyền) là xác định người dùng đã xác thực được phép làm gì.

---

## Intermediate Questions

### 4. Explain how OAuth works.
**EN:**  
OAuth is an open standard for access delegation. It allows users to grant a third-party app access to their resources without sharing passwords. The user authorizes the app, which gets an access token from the identity provider, then uses this token to access resources on the user's behalf.

**VI:**  
OAuth là chuẩn mở cho phép ủy quyền truy cập. Người dùng cho phép ứng dụng bên thứ ba truy cập tài nguyên mà không phải chia sẻ mật khẩu. Ứng dụng được cấp access token từ nhà cung cấp, dùng token này truy cập tài nguyên thay mặt người dùng.

---

### 5. Explain how JWT works.
**EN:**  
JWT (JSON Web Token) is a compact, URL-safe token containing claims between two parties. It has a header, payload, and signature. After authentication, the server sends a JWT to the client, who includes it with each request. The server verifies the signature to authenticate the user.

**VI:**  
JWT (JSON Web Token) là chuẩn mã hóa nhỏ gọn, an toàn, truyền các thông tin xác thực giữa hai bên. JWT gồm 3 phần: header, payload, signature. Sau xác thực, server gửi JWT cho client, client gửi kèm JWT mỗi request, server xác thực chữ ký để nhận diện người dùng.

---

### 6. What is a public key infrastructure flow and how would I diagram it?
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

### 7. Describe the difference between synchronous and asynchronous encryption.
**EN:**  
Synchronous encryption typically means symmetric encryption, where the same key is used for both encryption and decryption. Asynchronous encryption refers to asymmetric encryption, where a public key encrypts and a private key decrypts.

**VI:**  
Mã hóa đồng bộ thường ám chỉ mã hóa đối xứng (dùng cùng 1 khóa để mã hóa và giải mã). Mã hóa bất đồng bộ là mã hóa bất đối xứng, dùng khóa công khai để mã hóa và khóa riêng để giải mã.

---

### 8. Describe SSL handshake.
**EN:**  
The SSL handshake is the process where a client and server establish an encrypted connection. It includes:  
1. Negotiating protocol version and cipher suite.  
2. Exchanging certificates.  
3. Generating session keys for encryption.  
After the handshake, all data is transmitted securely.

**VI:**  
SSL handshake là quá trình client và server thiết lập kết nối mã hóa:  
1. Thỏa thuận phiên bản giao thức và bộ mã hóa.  
2. Trao đổi chứng chỉ.  
3. Sinh khóa phiên để mã hóa dữ liệu.  
Sau handshake, dữ liệu truyền được bảo mật.

---

### 9. How does HMAC work?
**EN:**  
HMAC (Hash-based Message Authentication Code) is a mechanism that combines a secret key with a hash function to ensure both data integrity and authenticity. The sender creates a hash of the message plus the secret key and sends both to the receiver, who computes the hash and checks if they match.

**VI:**  
HMAC (mã xác thực thông điệp dựa trên hàm băm) kết hợp khóa bí mật với hàm băm để đảm bảo toàn vẹn và xác thực dữ liệu. Người gửi tạo một mã băm từ thông điệp và khóa bí mật, gửi cho người nhận. Người nhận dùng cùng khóa tính lại mã băm để đối chiếu.

---

### 10. Why HMAC is designed in that way?
**EN:**  
HMAC is designed to resist certain attacks on plain hash functions, like length extension attacks, by mixing the secret key with the message in a specific way. This ensures that only someone with the secret key can generate a valid HMAC.

**VI:**  
HMAC được thiết kế để chống lại các tấn công vào hàm băm thông thường, như tấn công kéo dài độ dài (length extension), bằng cách kết hợp khóa bí mật với thông điệp theo cách đặc biệt. Nhờ đó, chỉ ai biết khóa bí mật mới tạo được HMAC hợp lệ.

---

### 12. What’s the difference between Diffie-Hellman and RSA?
**EN:**  
Diffie-Hellman is a key exchange protocol, mainly used to securely generate a shared secret over an insecure channel. RSA is an asymmetric encryption algorithm, used for both encryption and digital signatures.

**VI:**  
Diffie-Hellman là giao thức trao đổi khóa, giúp hai bên tạo ra khóa chung qua kênh không an toàn. RSA là thuật toán mã hóa bất đối xứng, dùng để mã hóa dữ liệu hoặc ký số.

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

### 16. Should you encrypt all data at rest?
**EN:**  
Ideally, yes. Encrypting all data at rest helps protect sensitive information from unauthorized access in case of physical theft or data breach.

**VI:**  
Lý tưởng nhất là nên mã hóa toàn bộ dữ liệu lưu trữ. Việc này giúp bảo vệ dữ liệu nhạy cảm khỏi truy cập trái phép khi bị đánh cắp thiết bị hoặc lộ dữ liệu.

---

## Advanced Questions

### 13. How does Kerberos work?
**EN:**  
Kerberos is a network authentication protocol that uses tickets to allow nodes to prove their identity securely. Users authenticate to a Key Distribution Center (KDC), receive a Ticket Granting Ticket (TGT), and use it to request service tickets for access to network resources.

**VI:**  
Kerberos là giao thức xác thực mạng dùng vé (ticket) để các máy chủ xác minh danh tính an toàn. Người dùng xác thực với Trung tâm phân phối khóa (KDC), nhận vé TGT, rồi dùng vé này để xin các vé dịch vụ truy cập tài nguyên mạng.

---

### 17. What is Perfect Forward Secrecy?
**EN:**  
Perfect Forward Secrecy (PFS) is a feature of key agreement protocols that ensures a session key cannot be compromised even if the private key of the server is compromised in the future.

**VI:**  
Perfect Forward Secrecy (PFS) là tính năng của các giao thức trao đổi khóa, đảm bảo rằng khóa phiên không bị lộ dù sau này khóa riêng của server bị lộ.

---
