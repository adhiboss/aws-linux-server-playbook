# AWS CloudWatch Monitoring Basics

## What is CloudWatch?

Amazon CloudWatch is a monitoring and observability service for AWS resources.

It collects:
- Metrics
- Logs
- Events

---

## Default EC2 Metrics

Automatically monitored:

- CPUUtilization
- NetworkIn
- NetworkOut
- DiskReadOps
- DiskWriteOps
- StatusCheckFailed

---

## Creating a Basic Alarm

Example: CPU Utilization Alarm

1. Go to CloudWatch → Alarms
2. Create Alarm
3. Select EC2 → CPUUtilization
4. Set threshold (e.g., > 70%)
5. Configure notification (SNS)
6. Create alarm

---

## CloudWatch Logs

Used to:
- Collect application logs
- Monitor system logs
- Debug issues

CloudWatch Agent can be installed on EC2 to push logs.

---

## Why It Matters

Monitoring helps:

- Detect performance issues
- Prevent downtime
- Troubleshoot infrastructure problems
- Maintain SLA commitments
