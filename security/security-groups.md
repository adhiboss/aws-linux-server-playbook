# AWS Security Groups (EC2 Firewall)

## What is a Security Group?
A Security Group (SG) is a virtual firewall for AWS resources like EC2 instances.

It controls:
- inbound traffic (incoming)
- outbound traffic (outgoing)

Security Groups work at the **instance level**.

---

## Key Rules
### Inbound Rules
Defines what traffic is allowed INTO the instance.

Example:
- Allow SSH (port 22) from your IP
- Allow HTTP (port 80) from anywhere

### Outbound Rules
Defines what traffic can go OUT from the instance.

Default:
- All outbound traffic is allowed.

---

## Important Properties
### 1. Stateful Firewall
Security Groups are **stateful**:
- If inbound traffic is allowed, the return traffic is automatically allowed.
- No need to add extra outbound rule for response.

---

## Common Ports in AWS

| Service | Port | Protocol |
|--------|------|----------|
| SSH | 22 | TCP |
| HTTP | 80 | TCP |
| HTTPS | 443 | TCP |
| RDP (Windows) | 3389 | TCP |
| MySQL | 3306 | TCP |
| PostgreSQL | 5432 | TCP |

---

## Best Practices

### Allow SSH Only From Your IP
Instead of:
- `0.0.0.0/0` (anyone)

Use:
- Your public IP `/32`

Example:
203.0.113.10/32


This prevents brute-force SSH attacks.

---

## Example Security Group Setup (Web Server)

### Inbound Rules
- SSH 22 → My IP only
- HTTP 80 → 0.0.0.0/0
- HTTPS 443 → 0.0.0.0/0

### Outbound Rules
- Allow all traffic (default)

---

## Troubleshooting SSH Issues
If SSH is not connecting:
- SG inbound rule missing port 22
- wrong IP allowed (your IP changed)
- instance has no public IP
- NACL blocking traffic
- route table issues

---

## Observations
- SG only allows traffic (it cannot explicitly deny like NACL)
- Multiple SGs can be attached to one instance
- Security groups are the first thing to check in EC2 connectivity problems

