📌 Objective
To install, configure, and troubleshoot Nginx as a reverse proxy server and understand common service-level issues.

🛠 Tools & Environment
OS: Kali Linux
Web Server: Nginx
Browser: Firefox
Service Manager: systemd

🔧 Installation
sudo apt update
sudo apt install nginx -y

⚙ Configuration Summary
1. Service Status Check
sudo systemctl status nginx

2. Port Conflict Issue
Nginx failed to start due to port 80 already in use.

Error:
bind() to 0.0.0.0:80 failed (98: Address already in use)

3. Resolution
Changed Nginx listening port from 80 → 8080.

sudo nano /etc/nginx/sites-available/default
listen 8080;

Restarted service:
sudo systemctl restart nginx

🔄 Reverse Proxy Setup

Configured Nginx to forward requests to a backend service.

location / {
    proxy_pass http://127.0.0.1:8000;
}

🔐 Security Observation
Directory listing was enabled and exposed user files.

Issue:
User home directory visible via browser

Fix:
autoindex off;
root /var/www/html;

🧪 Verification

Accessed via browser: http://localhost:8080
Confirmed Nginx service running
Verified no directory listing

⚠ Challenges Faced

Port binding conflict
Directory exposure due to misconfiguration

✅ Learning Outcome

Understood reverse proxy behavior
Learned service troubleshooting
Gained experience in secure web server configuration

📝 Conclusion
Nginx was successfully configured as a reverse proxy with proper security controls and service-level troubleshooting.