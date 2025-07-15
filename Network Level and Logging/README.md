# Security Interview – Core Questions & Level Classification

---

## Beginner Level (1-24)

1. **What are common ports involving security, what are the risks and mitigations?**  
   **Answer:**  
   Common ports: 21 (FTP), 22 (SSH), 23 (Telnet), 25 (SMTP), 53 (DNS), 80 (HTTP), 443 (HTTPS), 3389 (RDP).  
   Risks: Weak authentication, brute force, unencrypted traffic, vulnerable services.  
   Mitigations: Disable unused ports, use firewalls, strong authentication, encrypt traffic, keep services patched.

2. **Which one for DNS?**  
   **Answer:**  
   DNS uses port 53 (UDP/TCP).

3. **Describe HTTPS and how it is used.**  
   **Answer:**  
   HTTPS encrypts HTTP traffic using SSL/TLS, protecting data in transit between browsers and servers. Used for secure web communications.

4. **What is the difference between HTTPS and SSL?**  
   **Answer:**  
   HTTPS is a secure protocol for web traffic that uses SSL/TLS for encryption. SSL (now replaced by TLS) is the underlying security protocol.

5. **How does threat modeling work?**  
   **Answer:**  
   Threat modeling is a process of identifying, assessing, and addressing security threats and vulnerabilities during design and development.

6. **What is a subnet and how is it useful in security?**  
   **Answer:**  
   A subnet is a segmented piece of a larger network. Subnetting improves security by isolating segments, reducing broadcast domains, and controlling access.

7. **What is subnet mask?**  
   **Answer:**  
   A subnet mask defines which portion of an IP address is network and which is host, helping to divide and organize networks.

8. **Explain what traceroute is.**  
   **Answer:**  
   Traceroute is a network diagnostic tool that traces the path packets take from source to destination, displaying each hop along the route.

9. **Draw a network, then expect them to raise an issue...**  
   **Answer:**  
   [Interviewers expect candidates to spot potential security or connectivity issues in a network diagram and suggest solutions.]

10. **Write out a Cisco ASA firewall configuration...**  
    **Answer:**  
    [Requires hands-on knowledge. Candidates should demonstrate setting up interfaces, NAT, ACLs, and security policies using CLI.]

11. **Explain TCP/IP concepts.**  
    **Answer:**  
    TCP/IP is the fundamental suite of protocols for the internet. TCP handles reliable delivery, IP handles addressing/routing.

12. **What is OSI model?**  
    **Answer:**  
    OSI (Open Systems Interconnection) model has 7 layers: Physical, Data Link, Network, Transport, Session, Presentation, Application.

13. **How does a router differ from a switch?**  
    **Answer:**  
    Routers forward packets between networks (Layer 3), switches connect devices within a network (Layer 2).

14. **Describe the Risk Management Framework process...**  
    **Answer:**  
    RMF is a structured approach to integrating security and risk management in IT systems, including steps: categorize, select, implement, assess, authorize, monitor.

15. **How does a packet travel between two hosts...**  
    **Answer:**  
    Packets move through OSI layers, are routed via routers/switches using MAC/IP addresses, with headers added/removed at each layer.

16. **Explain the difference between TCP and UDP.**  
    **Answer:**  
    TCP is connection-oriented, reliable, ensures delivery; UDP is connectionless, faster, does not guarantee delivery.

17. **Which is more secure and why?**  
    **Answer:**  
    [Depends on context. TCP is generally more secure than UDP due to reliable delivery and built-in mechanisms. Protocols like HTTPS (TCP) are more secure than HTTP (TCP) due to encryption.]

18. **What is the TCP three way handshake?**  
    **Answer:**  
    SYN (client) → SYN-ACK (server) → ACK (client). Used to establish a TCP connection reliably.

19. **What is the difference between IPSEC Phase 1 and Phase 2?**  
    **Answer:**  
    Phase 1 establishes a secure, authenticated channel (IKE SA). Phase 2 negotiates IPsec SAs for encrypting actual data.

20. **What are biggest AWS security vulnerabilities?**  
    **Answer:**  
    Examples: Public S3 buckets, overly permissive IAM roles, exposed credentials, unencrypted data, misconfigured security groups.

21. **How do web certificates for HTTPS work?**  
    **Answer:**  
    Certificates are issued by CAs to verify the server’s identity. Browsers check the certificate and use public keys for encrypted communication.

22. **What is the purpose of TLS?**  
    **Answer:**  
    TLS (Transport Layer Security) encrypts communication, ensuring confidentiality, integrity, and authenticity over networks.

23. **Is ARP UDP or TCP?**  
    **Answer:**  
    Neither. ARP is a Layer 2 protocol used for resolving IP to MAC addresses, not using UDP/TCP.

24. **Explain what information is added to a packet at each stop of the 7 layer OSI model.**  
    **Answer:**  
    Each layer adds headers (and sometimes trailers) for their functions: e.g., Application data, Presentation (format), Session (control), Transport (port), Network (IP), Data Link (MAC), Physical (bits).

## Intermediate Level (25-36)

25. **Walk through a whiteboard scenario... compromising the network...**  
    **Answer:**  
    [Describe possible attack paths: reconnaissance, exploitation, privilege escalation, lateral movement. Suggest detection and mitigation steps.]

26. **Explain how you would build a web site... secure communications...**  
    **Answer:**  
    Use HTTPS (SSL/TLS), strong authentication, input validation, proper session handling, secure headers, and follow security best practices.

27. **How does an active directory work?**  
    **Answer:**  
    Active Directory is a directory service by Microsoft for Windows domain networks. It stores info about objects, users, groups and manages authentication/authorization.

28. **Do you know how Single Sign-On works?**  
    **Answer:**  
    SSO allows users to authenticate once and gain access to multiple systems using a centralized authentication server (via SAML, OAuth, OpenID, etc.).

29. **What is a firewall?**  
    **Answer:**  
    A device or software that monitors and controls incoming and outgoing network traffic based on security rules.

30. **How does it work?**  
    **Answer:**  
    Firewalls inspect packets and permit or block them based on configured policies (stateless or stateful inspection).

31. **How does it work in cloud computing?**  
    **Answer:**  
    Cloud firewalls operate as virtual appliances, filtering traffic at the network or application level using security groups, ACLs, and firewall rules.

32. **Difference between IPS and IDS?**  
    **Answer:**  
    IDS (Intrusion Detection System) monitors and alerts on suspicious activity; IPS (Intrusion Prevention System) can also block or prevent threats in real time.

33. **How do you build a tool to protect the entire Apple infra?**  
    **Answer:**  
    [High-level: Requires scalable, automated monitoring, incident response, endpoint security, strong authentication, and continuous assessment across all assets.]

34. **How do you harden a system?**  
    **Answer:**  
    Remove unnecessary services, apply patches, enforce strong passwords, enable firewalls, use least privilege, monitor logs.

35. **How do you elevate permissions?**  
    **Answer:**  
    (Red Team) Exploit vulnerabilities, misconfigurations, weak credentials, or leverage privilege escalation techniques to gain higher access.

36. **Describe the hardening measures you've put on your home network.**  
    **Answer:**  
    Strong Wi-Fi password, disable WPS, separate guest network, firewall, updated firmware, restrict IoT, network monitoring.

## Advanced Level (37-44)

37. **What is traceroute? Explain it in details.**  
    **Answer:**  
    Traceroute sends packets with increasing TTL, recording each router (hop) that forwards the packet. Reveals network path and bottlenecks.

38. **How does HTTPS work?**  
    **Answer:**  
    HTTPS encrypts HTTP traffic using SSL/TLS. The server presents a certificate; a secure session key is negotiated for encrypted communication.

39. **What would you do if you discovered an infected host?**  
    **Answer:**  
    Isolate the host, collect forensic evidence, analyze, remove malware, patch vulnerabilities, restore from clean backup, report incident.

40. **What is SYN/ACK and how does it work?**  
    **Answer:**  
    SYN/ACK is the server's response during TCP handshake. After receiving SYN from client, server replies with SYN/ACK; client then sends ACK.

41. **You got the memory dump of a potentially compromised system, how are you going to approach its analysis?**  
    **Answer:**  
    Use forensic tools (e.g. Volatility) to analyze processes, network connections, loaded modules, search for indicators of compromise.

42. **How would you detect a DDOS attack?**  
    **Answer:**  
    Look for sudden traffic spikes, many connections from same/different IPs, degraded performance, and unusual log entries. Use monitoring tools and alerts.

43. **How does the kernel know which function to call for the user?**  
    **Answer:**  
    System calls are mapped via a syscall table; the kernel receives syscall numbers and dispatches to the corresponding handler function.

44. **How would you go about reverse-engineering a custom protocol packet?**  
    **Answer:**  
    Capture packets with Wireshark, analyze structure/patterns, document fields, use fuzzing, create parsers, and test against known behavior.

---
