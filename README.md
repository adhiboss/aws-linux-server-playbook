# AWS Linux Server Playbook

A practical playbook repository for managing and troubleshooting Linux servers on AWS (EC2).

This repo contains real-world notes for:
- EC2 setup
- SSH access
- security hardening
- monitoring
- automation
- troubleshooting

---

## 📌 Topics Covered

### EC2
- SSH access setup
- Linux user management
- package installation and updates

### Security
- Security Groups (AWS firewall)
- Linux firewall (UFW / iptables)
- fail2ban brute-force protection

### Automation
- cron jobs
- log rotation
- scheduled monitoring scripts

### Monitoring
- systemctl + journalctl
- CPU / memory / disk monitoring
- service debugging

### Troubleshooting
- EC2 SSH connection issues
- DNS and networking failures
- port/service connectivity issues

---

## 📂 Folder Structure

```bash
aws-linux-server-playbook/
├── ec2/
├── security/
├── automation/
├── monitoring/
└── troubleshooting/
