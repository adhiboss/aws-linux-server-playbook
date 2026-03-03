# EC2 Troubleshooting Checklist

## 1) Cannot SSH Into EC2

Check:
- Security Group allows port 22 from your IP
- Correct key pair used
- Instance is running
- Public IP attached
- Correct username (ubuntu / ec2-user)

Test:
ssh -i key.pem ubuntu@<public-ip>

---

## 2) Website Not Loading

Check:
- Security Group allows HTTP (80) / HTTPS (443)
- Web server running (nginx / apache)
- Firewall status (ufw / firewalld)
- Application bound to correct port

Command:
sudo systemctl status nginx

---

## 3) High CPU Usage

Check:
- top
- htop
- ps aux --sort=-%cpu | head

Possible Causes:
- Infinite loop process
- High traffic
- Memory swap usage

---

## 4) Disk Full

Check:
df -h
du -sh *

Clean:
- Remove logs
- Rotate logs
- Expand EBS volume

---

## 5) Instance Status Check Failed

Check:
- AWS EC2 → Status Checks
- System vs Instance status
- Reboot instance
- Check EBS health

---

## Why This Matters

Systematic troubleshooting is critical for cloud support and customer-facing engineering roles.
