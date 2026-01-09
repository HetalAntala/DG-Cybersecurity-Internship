🎯 Objective
Configure and perform a full server backup for disaster recovery.

🧰 Requirements

Windows Server 2016 (VM)
Secondary disk OR virtual disk (minimum 10–20 GB)

🪜 STEP-BY-STEP
Step 1: Add Backup Feature
Open Server Manager
Click Manage → Add Roles and Features
Click Next until Features
Select ✔ Windows Server Backup
Click Install
Wait until installation completes

📸 Screenshot: Feature installation completed

Step 2: Open Windows Server Backup
Server Manager → Tools
Click Windows Server Backup

📸 Screenshot: Windows Server Backup console

Step 3: Perform Backup
Click Local Backup
Click Backup Once
Select Different options
Select Full Server
Choose backup destination:
Local drive / virtual disk
Click Next → Backup

📸 Screenshot:
Backup progress
Backup successful

📝 Conclution
Windows Server Backup is used to protect critical system data and enables recovery in case of system failure or data loss.