# 🖥️ Ansible System Health Monitoring

## 📘 Overview
This project automates system health monitoring using **Ansible**.  
It gathers CPU, memory, and disk usage stats from all servers in your inventory and generates a consolidated log report.

---

## ⚙️ Features
- Collects CPU, Memory, and Disk usage from remote servers  
- Saves a detailed health report at `/var/log/system_health_report.log`  
- Works across multiple nodes in parallel  
- Easily extendable for network or process checks  



## 📁 Project Structure
ansible-system-health-monitoring/
│
├── playbooks/
│ └── system_health.yml
├── inventory/
│ └── hosts.ini
└── README.md



## 🚀 Usage

Step 1 — Clone the repository
bash
git clone https://github.com/<your-username>/ansible-system-health-monitoring.git
cd ansible-system-health-monitoring
Step 2 — Update your inventory
Edit inventory/hosts.ini with your actual server IPs and SSH user credentials.

Step 3 — Run the playbook
bash

ansible-playbook -i inventory/hosts.ini playbooks/system_health.yml
🧠 Example Output
Each server will have a generated file:

lua

/var/log/system_health_report.log
containing details like:

perl

DISK USAGE:
Filesystem      Size  Used Avail Use% Mounted on
/dev/root        20G   8G   12G  40% /

MEMORY USAGE:
              total        used        free      shared  buff/cache   available
Mem:           1987         456         789          12         742        1254

CPU USAGE:
Cpu(s):  3.2%us,  1.0%sy,  0.0%ni, 95.5%id,  0.3%wa,  0.0%hi,  0.0%si,  0.0%st


🧩 Requirements
Ansible 2.9+

SSH access to target hosts

Ubuntu/Debian-based systems
