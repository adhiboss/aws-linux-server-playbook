# AWS CloudWatch Monitoring Setup

This guide shows how to enable monitoring for an EC2 instance using AWS CloudWatch.

## Update System

sudo apt update
sudo apt upgrade -y

## Install CloudWatch Agent

wget https://s3.amazonaws.com/amazoncloudwatch-agent/ubuntu/amd64/latest/amazon-cloudwatch-agent.deb

sudo dpkg -i amazon-cloudwatch-agent.deb

## Configure Agent

sudo /opt/aws/amazon-cloudwatch-agent/bin/amazon-cloudwatch-agent-config-wizard

## Start CloudWatch Agent

sudo systemctl start amazon-cloudwatch-agent

## Enable Agent on Boot

sudo systemctl enable amazon-cloudwatch-agent

## Verify Status

sudo systemctl status amazon-cloudwatch-agent
