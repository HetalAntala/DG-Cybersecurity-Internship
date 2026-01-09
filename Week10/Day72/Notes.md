📌 Objective
To monitor and analyze Linux system and service logs for troubleshooting and security analysis.

🛠 Tools & Environment

OS: Kali Linux
Tools: journalctl, system logs
Services monitored: cron, nginx

🔧 Commands Used
1. View System Logs
journalctl

2. View Recent Logs
journalctl -xe

3. Monitor Logs in Real-Time
journalctl -f

4. Filter Logs by Service
journalctl -u nginx
journalctl -u cron

⚙ Task Performed

Monitored cron job execution logs
Analyzed nginx service failure logs
Identified error messages related to port conflicts

⚠ Issues Faced
Problem
Nginx service failed to start.

Log Insight
bind() to 0.0.0.0:80 failed (Address already in use)

Solution
Identified conflicting service
Changed Nginx port configuration

🧠 Learning Outcome

Learned how logs help in root cause analysis
Understood importance of service-level logging
Gained troubleshooting confidence

🔐 Security Note

Logs help detect unauthorized access attempts
Regular log monitoring is essential in production systems

📝 Conclusion
Successfully monitored and analyzed Linux system logs to diagnose and resolve service issues.