# Programming and Code

---

## Beginner Level (Cơ bản)

### 1. Tell me about a repetitive task at work that you automated away.

**EN:**  
Common examples: automating report generation, log analysis, backups, user account provisioning, vulnerability scanning, or updating dependencies using scripts or CI jobs.

**VI:**  
Ví dụ phổ biến: tự động tạo báo cáo, phân tích log, sao lưu, cấp phát tài khoản, quét lỗ hổng hoặc cập nhật thư viện bằng script hoặc công cụ CI.

---

### 2. How would you analyze a suspicious email link?

**EN:**  
- Check the link for typosquatting or strange domains.
- Hover to preview the actual URL.
- Use online scanners (e.g., VirusTotal, URLscan.io).
- Open in a safe sandbox environment (never on production).
- Look for phishing indicators (urgent language, attachments).

**VI:**  
- Kiểm tra link có lỗi chính tả hoặc domain lạ.
- Di chuột để xem trước URL thật.
- Quét với các dịch vụ trực tuyến (VirusTotal, URLscan.io).
- Nếu cần, mở trong sandbox an toàn, không dùng trên máy thật.
- Nhận diện dấu hiệu lừa đảo (ngôn từ khẩn cấp, file đính kèm bất thường).

---

## Intermediate Level (Trung bình)

### 3. How would you conduct a security code review?

**EN:**  
- Understand app architecture and data flows.
- Look for input validation, output encoding, authentication & authorization logic.
- Search for common vulnerabilities (e.g., OWASP Top 10).
- Use both manual and automated tools (e.g., SAST).
- Document findings and recommend fixes.

**VI:**  
- Hiểu kiến trúc ứng dụng, luồng dữ liệu.
- Kiểm tra kiểm soát đầu vào, mã hóa đầu ra, xác thực, phân quyền.
- Tìm các lỗi phổ biến (OWASP Top 10).
- Kết hợp kiểm tra thủ công và tự động (SAST).
- Ghi lại phát hiện, đề xuất khắc phục.

---

### 4. If I hand you a repo of source code to security audit, what’s the first few things you would do?

**EN:**  
- Identify sensitive files (config, .env, keys).
- Check for hardcoded credentials/secrets.
- Run automated scanning tools.
- Review dependencies for known vulnerabilities.
- Assess code for logic flaws and insecure patterns.

**VI:**  
- Xác định các file nhạy cảm (config, .env, key).
- Kiểm tra credential, secret hardcode.
- Chạy công cụ quét tự động.
- Soát lỗi thư viện phụ thuộc.
- Kiểm tra các lỗ hổng logic hoặc code không an toàn.

---

### 5. Can I write a tool that would search our Github repos for secrets, keys, etc.?

**EN:**  
Yes. Use or build tools like `truffleHog`, `git-secrets`, or `gitleaks` to search for exposed secrets in repositories. Integrate into CI/CD to prevent secret leaks.

**VI:**  
Có. Sử dụng hoặc tự xây công cụ như `truffleHog`, `git-secrets`, `gitleaks` để quét secret trong repo. Kết hợp vào CI/CD để ngăn rò rỉ thông tin nhạy cảm.

---

### 6. Code review a project and look for the vulnerability.

**EN:**  
During review, look for:
- Insecure input handling (lack of validation/sanitization)
- Broken authentication/authorization
- Insecure storage of data/secrets
- Use of outdated or vulnerable libraries
- Poor error handling and logging

**VI:**  
Khi review cần chú ý:
- Xử lý đầu vào không an toàn (thiếu validate/sanitize)
- Lỗi xác thực/phân quyền
- Lưu trữ dữ liệu, secret không an toàn
- Dùng thư viện lỗi thời hoặc có lỗ hổng
- Xử lý lỗi, log không chuẩn

---

## Advanced Level (Nâng cao)

### 7. How can Github webhooks be used in a malicious way?

**EN:**  
- Exfiltrate sensitive data by sending payloads to attacker-controlled endpoints.
- Trigger malicious builds/deployments in CI/CD pipelines.
- Abuse webhooks to perform DoS attacks or automate actions without consent.

**VI:**  
- Đưa dữ liệu nhạy cảm ra ngoài bằng cách gửi payload đến endpoint của kẻ xấu.
- Gây build/deploy mã độc qua CI/CD.
- Lạm dụng webhook để tấn công từ chối dịch vụ hoặc thực thi hành động trái phép.

---

### 8. Slack? (Reference: [Ars Technica - Hacking Slack Accounts as Easy as Searching Github](https://arstechnica.com/security/2016/04/hacking-slack-accounts-as-easy-as-searching-github/))

**EN:**  
Slack tokens or credentials accidentally committed to Github can be found and abused by attackers to gain access, steal data, or impersonate users.

**VI:**  
Token hoặc thông tin Slack lộ trên Github có thể bị tìm thấy, sử dụng để truy cập, đánh cắp dữ liệu hoặc giả danh người dùng.

---

### 9. AWS? (Secrets, keys in code/repos)

**EN:**  
Leaked AWS keys can allow attackers to control cloud resources, steal data, spin up expensive workloads, or disrupt services.  
Always store secrets securely, never commit to source code.

**VI:**  
Lộ key AWS sẽ khiến kẻ tấn công chiếm quyền điều khiển dịch vụ, đánh cắp dữ liệu hoặc gây tốn kém/tê liệt hệ thống.  
Phải bảo vệ key tuyệt đối, không lưu trong source code.

---

### 10. Given a CVE, walk us through it and how the solution works.

**EN:**  
- Summarize the vulnerability (impact, affected versions, attack vector).
- Explain exploitation method.
- Describe remediation (patch, config change, etc.).
- Example: **CVE-2021-44228 (Log4Shell)** - Allows remote code execution via crafted log messages. Solution: Patch Log4j to 2.17+, remove vulnerable classes.

**VI:**  
- Tóm tắt lỗ hổng (ảnh hưởng, phiên bản, cách khai thác).
- Trình bày cách khai thác.
- Giải thích cách khắc phục (vá lỗi, cấu hình lại,...).
- Ví dụ: **CVE-2021-44228 (Log4Shell)** - Cho phép thực thi mã từ xa qua log. Cách sửa: cập nhật Log4j 2.17+, xóa class lỗi.

---
