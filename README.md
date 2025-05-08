# Week 4 – Advanced Threat Detection & Web Security Enhancements

## 🎯 Objective
To implement advanced threat detection, secure API endpoints, and strengthen web application security using tools like Fail2Ban, Logwatch, Helmet, and Express.js.

---

## ✅ Task Breakdown & Completion

### Task 1: Intrusion Detection & Monitoring
- Installed and configured **Fail2Ban** on Kali Linux to monitor SSH login attempts.
- Configured `/etc/fail2ban/jail.local`:
  - Monitored `/var/log/auth.log`
  - Set `maxretry = 2`, `bantime = 600`, and used `systemd` backend
- Simulated brute-force login using a `fakeuser` via SSH to trigger bans.
- Verified ban activity using:
  ```bash
  sudo fail2ban-client status sshd

Task 2: Log Analysis & Threat Intelligence
Installed Logwatch to generate system activity summaries.
Executed:
sudo logwatch --detail high --service sshd --range today --format text
Searched for key patterns in logs:
Failed password attempts:
sudo cat /var/log/auth.log | grep "Failed"
Sudo usage & root sessions for anomaly detection.
Verified firewall status using ufw (if enabled).
Task 3: API Security Hardening & Web Headers
Built a secure API using Express.js.
Implemented:
Rate limiting using express-rate-limit to prevent abuse.
CORS protection with the cors package.
Security headers using helmet, including:
HTTP Strict Transport Security (HSTS)
Content Security Policy (CSP)
Final server protected against brute-force, injection, and abuse attacks.
📌 Conclusion
This week’s focus on real-time threat detection, system log analysis, and API protection was successfully implemented. The knowledge and tools gained this week (Fail2Ban,
Logwatch, Express.js security practices) are essential for any cybersecurity and DevSecOps role.
This hands-on experience helped build real-world skills in intrusion prevention, API hardening, and web application security headers.



