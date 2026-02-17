# AWS IAM Basics (Important for EC2)

## What is IAM?
IAM (Identity and Access Management) is used to manage:
- users
- roles
- policies
- permissions

It controls who can access AWS resources.

---

## IAM Users
IAM user = a person/account inside AWS.

Example:
- admin user
- developer user

Users can have:
- password (console login)
- access keys (programmatic access)

---

## IAM Policies
A policy defines permissions in JSON format.

Example:
- allow S3 read access
- allow EC2 full access

Policies can be attached to:
- users
- groups
- roles

---

## IAM Roles (Very Important)
Role is used for AWS services.

Example:
- EC2 instance role
- Lambda role

Instead of giving access keys, you attach a role.

---

## EC2 Instance Role Example
If EC2 needs to access S3:
- create role with S3 permissions
- attach role to EC2

Then EC2 can access S3 securely without storing credentials.

---

## Best Practices
- Never use root account daily
- Use least privilege principle
- Enable MFA for important users
- Prefer roles instead of access keys

---

## Observations
- IAM is the security backbone of AWS
- Roles are safest way to give permissions to EC2
- Policies control exactly what actions are allowed
