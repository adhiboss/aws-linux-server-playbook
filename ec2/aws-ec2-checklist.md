# AWS EC2 Launch & Setup Checklist

## 1) Choose AMI
- Ubuntu / Amazon Linux 2
- Check Kernel & LTS version

## 2) Instance Type
- t3.micro (for free tier/testing)
- t3.small or larger for real workloads

## 3) Networking
- VPC: default or custom
- Subnet (public/private)
- Enable Auto-assign Public IP if needed

## 4) Security Group Rules
Allow:
- SSH (TCP 22) — YOUR_IP only
- HTTP (TCP 80)
- HTTPS (TCP 443)
Example:
SSH 22 (your.ip.here/32)
HTTP 80 0.0.0.0/0
HTTPS 443 0.0.0.0/0


## 5) Key Pair
- Create new key pair
- Download .pem and secure it
