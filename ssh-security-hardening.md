# SSH Security Hardening Guide

This guide explains how to secure SSH access on Linux servers commonly used in cloud environments such as AWS EC2.

## 1 Disable Root Login

Edit SSH configuration:

sudo nano /etc/ssh/sshd_config

Find:

PermitRootLogin yes

Change to:

PermitRootLogin no

---

## 2 Change Default SSH Port

Find:

#Port 22

Change to:

Port 2222

---

## 3 Disable Password Authentication

Find:

PasswordAuthentication yes

Change to:

PasswordAuthentication no

---

## 4 Enable Key Based Authentication

Generate SSH key:

ssh-keygen

Copy key to server:

ssh-copy-id user@server-ip

---

## 5 Restart SSH Service

sudo systemctl restart ssh

---

## 6 Verify SSH Security

Check listening ports:

ss -tulnp | grep ssh

Check login attempts:

sudo journalctl -u ssh
