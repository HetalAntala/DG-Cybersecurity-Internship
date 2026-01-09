📌 Objective
To understand and implement task scheduling in Linux using cron and crontab, and verify automated execution.

🛠 Tools & Environment
OS: Kali Linux
Utility: cron / crontab
Shell: Bash

🔧 Prerequisites

User with sudo privileges
Cron service running
Check cron status:
sudo systemctl status cron

⚙ Task Performed
1. Create Output File

Created a file to store cron job output.
touch /home/kali/cron_output.txt

2. Edit Crontab

Opened crontab editor:
crontab -e


Added job:

* * * * * echo "Cron job executed on $(date)" >> /home/kali/cron_output.txt
This job runs every minute and appends output to the file.

3. Save & Install

After saving:
crontab: installing new crontab

🔍 Verification

Checked file output:
cat /home/kali/cron_output.txt


Confirmed entries were added automatically every minute.

⚠ Issue Faced
Problem:
Output file was missing initially.

Root Cause:
File was not created before scheduling the cron job.

Solution:
Manually created the file and waited for cron execution.

🧠 Learning Outcome

Learned cron time format (* * * * *)
Understood difference between system cron and user cron
Gained experience debugging silent cron failures

🔐 Security Note

Cron jobs should use absolute paths
Avoid running cron jobs as root unless necessary

📝 Conclusion
Successfully configured and verified Linux cron jobs for automated task execution.

📸 Evidence

Screenshots and terminal outputs are stored in the screenshots/ folder.