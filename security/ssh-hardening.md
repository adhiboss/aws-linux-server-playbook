# SSH Hardening for AWS Linux Server

## 1) Disable Root Login

Edit SSH config:

sudo nano /etc/ssh/sshd_config

Set:

PermitRootLogin no

---

## 2) Disable Password Authentication

Force key-based login only:

PasswordAuthentication no

---

## 3) Change Default SSH Port (Optional)

Port 2222

After changing, update Security Group to allow new port.

---

## 4) Allow Specific Users Only

Add:

AllowUsers ubuntu ec2-user

---

## 5) Restart SSH Service

sudo systemctl restart sshd

---

## 6) Configure Security Group Properly

Allow:
SSH (port 22 or custom port)
Source: Your public IP only (x.x.x.x/32)

Never allow 0.0.0.0/0 for SSH in production.

---

## 7) Use Fail2Ban (Optional Extra Protection)

sudo apt install fail2ban
sudo systemctl enable fail2ban
