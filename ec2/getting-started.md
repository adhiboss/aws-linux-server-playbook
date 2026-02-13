
---

## Step 4: Configure Security Group
Inbound rules (recommended):
- SSH (22) → Your IP only
- HTTP (80) → 0.0.0.0/0 (optional)
- HTTPS (443) → 0.0.0.0/0 (optional)

---

## Step 5: Connect to EC2 from WSL/Linux

### Move key into WSL
```bash
mv /mnt/c/Users/<yourname>/Downloads/mykey.pem ~/
# Getting Started with AWS Linux (EC2)

This guide explains how to launch and access a Linux server on AWS EC2.

---

## Step 1: Create AWS Account
- Go to AWS Console
- Create account
- Enable MFA for security

---

## Step 2: Launch an EC2 Instance
1. Go to **EC2 Dashboard**
2. Click **Launch Instance**
3. Choose AMI:
   - Ubuntu Server 22.04 (recommended)
4. Choose instance type:
   - `t2.micro` (free tier)

---

## Step 3: Create a Key Pair
- Create new key pair
- Download `.pem` file
- Store it safely (never share it)

Example:
---

## Step 4: Configure Security Group
Inbound rules (recommended):
- SSH (22) → Your IP only
- HTTP (80) → 0.0.0.0/0 (optional)
- HTTPS (443) → 0.0.0.0/0 (optional)

---

## Step 5: Connect to EC2 from WSL/Linux

### Move key into WSL
```bash
mv /mnt/c/Users/<yourname>/Downloads/mykey.pem ~/


---

## Step 4: Configure Security Group
Inbound rules (recommended):
- SSH (22) → Your IP only
- HTTP (80) → 0.0.0.0/0 (optional)
- HTTPS (443) → 0.0.0.0/0 (optional)

---

## Step 5: Connect to EC2 from WSL/Linux

### Move key into WSL
```bash
mv /mnt/c/Users/<yourname>/Downloads/mykey.pem ~/
