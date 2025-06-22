# Network Health Checker

Automates proactive network diagnostics and daily reporting.

## 🛠 Technologies
- Python 3.x  
- ping3 (ICMP ping)  
- PyYAML (configuration parsing)  
- smtplib (email alerts)  
- Windows Task Scheduler / cron

## 📂 Structure
- **config/targets.yml** – list of hosts & ports to monitor  
- **checker.py** – pings hosts, tests TCP ports, writes timestamped CSV to `reports/`  
- **send_report.py** – finds latest CSV and emails it via SMTP  
- **schedules/cron.sh** – example cron wrapper for Linux/macOS  
- **schedules/network_health_checker.task** – exported Windows Scheduled Task XML

## 🔧 Setup

1. **Clone & install**  
   ```bash
   git clone https://github.com/YourUserName/network-health-checker.git
   cd network-health-checker
   python3 -m venv venv
   source venv/bin/activate     # or .\venv\Scripts\activate on Windows
   pip install -r requirements.txt
