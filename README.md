# Security_project
Real-Time File Integrity Using OSSEC Server


📌 Project Overview

In today's digital landscape, securing critical files and monitoring unauthorized changes is crucial. Real-Time File Integrity Using OSSEC Server is a security-focused project that leverages OSSEC (Open Source HIDS) to detect file modifications, ensuring the integrity of system files and directories.


🚀 Features


Real-Time File Monitoring: Detects unauthorized changes instantly.

Automated Alerting System: Sends notifications upon detecting file modifications.

Centralized Log Management: Stores and analyzes logs for security insights.

Cross-Platform Compatibility: Works on Linux, Windows, and Unix systems.

Customizable Configuration: Allows users to specify directories for monitoring.



🛠️ Technologies Used


OSSEC HIDS (Host-Based Intrusion Detection System)

Linux (Debian-based systems)

Python & Bash Scripting (for automation)

Syslog (for log management and alerting)

Email & SIEM Integration (for notifications)



📂 Project Structure

real-time-file-integrity-ossec/
│── configs/               # OSSEC configuration files
│── scripts/               # Automation scripts (Bash/Python)
│── logs/                  # Sample log files
│── docs/                  # Documentation & Reports
│── README.md              # Project documentation


🔧 Installation & Setup


1️⃣ Install OSSEC Server

wget -qO - https://updates.atomicorp.com/installers/atomic | sudo bash
sudo apt install ossec-hids-server -y

2️⃣ Configure OSSEC for File Integrity Monitoring

Edit the OSSEC configuration file:
sudo nano /var/ossec/etc/ossec.conf

Add directories you want to monitor:
<directories check_all="yes">/etc/</directories>
<directories check_all="yes">/var/www/html/</directories>

3️⃣ Restart OSSEC
sudo systemctl restart ossec-hids

📊 Monitoring & Alerts

Check OSSEC Alerts:
sudo cat /var/ossec/logs/alerts/alerts.log

List Active Agents:
sudo /var/ossec/bin/agent_control -l

View Log Analysis in Real-Time:
tail -f /var/ossec/logs/ossec.log

📩 Contributors

Apurva Bhavsar 

📜 License
This project is released under the MIT License.

🌟 Support & Contributions

Feel free to fork this repository, submit issues, or contribute improvements via pull requests.




