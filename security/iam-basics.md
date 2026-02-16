# IAM Basics in AWS (Users, Groups, Roles, Policies)

## What is IAM?
IAM (Identity and Access Management) controls:
- Who can access AWS
- What they can access
- How they can access it

---

## IAM Components

### IAM User
A person or service account with login credentials.

### IAM Group
Collection of users with same permissions.

### IAM Policy
JSON document defining permissions.

### IAM Role
Temporary permission set assumed by AWS services (EC2, Lambda).

---

## Why IAM Roles are important
Instead of storing AWS keys in EC2,
we attach an IAM role to EC2.

This is safer because:
- No hardcoded secrets
- Temporary credentials auto-managed
- Easy to revoke

---

## Best Practices
- Never use root account for daily tasks
- Enable MFA
- Use least privilege principle
- Use roles instead of access keys in EC2
- Rotate access keys if used

---

## Example Use Case
EC2 needs to access S3:
- Create role with S3 permissions
- Attach role to EC2 instance
- EC2 can access S3 without keys
