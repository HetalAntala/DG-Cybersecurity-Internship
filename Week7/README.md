📘 Week 7 – Firewall & Security

This week focused on implementing firewall rules, blocking specific ports, testing configurations, and enabling HTTPS using SSL/TLS. The tasks were performed on a Kali Linux environment with Apache web server.

🛡️ Task 22 – Configure Firewall (UFW & IPTables)
✔ Step 1: Install UFW
sudo apt install ufw -y

✔ Step 2: Enable UFW
sudo ufw enable

✔ Step 3: Allow Required Ports
sudo ufw allow 22     # SSH
sudo ufw allow 80     # HTTP
sudo ufw allow 443    # HTTPS

✔ Step 4: Block a Specific Port (Example: 21 for FTP)
sudo ufw deny 21

📸 Screenshots Included

UFW_install.png – UFW installation

ufw_status.png – UFW status showing allowed/denied rules

deny_port.png – Denying port access

NmapScan_client.png – Nmap port scan results before/after rules

🔥 IPTables Configuration
✔ View Current IPTables Rules
sudo iptables -L

✔ Block Port Using IPTables
sudo iptables -A INPUT -p tcp --dport 21 -j DROP

📸 Screenshots Included

IpTables.png

IpTables1.png

🔒 Task 24 – Enable SSL/TLS and Configure HTTPS
✔ Step 1: Install SSL Module
sudo apt install openssl ssl-cert -y
sudo a2enmod ssl

✔ Step 2: Enable Default SSL Site
sudo a2ensite default-ssl.conf
sudo systemctl restart apache2

✔ Step 3: Test HTTPS

Open browser →
https://<server-ip>

You should see a self-signed certificate warning, which confirms SSL is active.

📸 Screenshots Included

ssl_install_enable.png – SSL module enabled

webserver_status_before.png – Apache running

https_request.png – Browser showing HTTPS secure warning

📁 Folder Structure (Week 7)
Week7/
│
├── Firewall/
│   ├── UFW_install.png
│   ├── ufw_status.png
│   ├── UFW_Rules.png
│   ├── deny_port.png
│   ├── IpTables.png
│   ├── IpTables1.png
│   └── NmapScan_client.png
│
└── HTTPS/
    ├── ssl_install_enable.png
    ├── webserver_status_before.png
    └── https_request.png