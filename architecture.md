# Architecture Overview

The infrastructure includes:

## Network Layer

- Custom VPC with /16 CIDR block
- 2 Public Subnets (Bastion + Web Tier)
- 2 Private Subnets (App Tier + DB Tier)
- NAT Gateway in Public Subnet B
- Route tables configured for public and private routing

## Compute Layer

- EC2 (Amazon Linux 2) in Public-Subnet-A: Bastion Host
- EC2 in Private-Subnet-A: Node.js backend
- EC2 (or RDS) in Private-Subnet-B: future DB server

## Application Layer

- Static website on S3 with custom branding and appointment form
- REST API endpoint on `/api/book-appointment` for data collection

## Monitoring & Security

- VPC Flow Logs to CloudWatch
- AWS CloudTrail for API activity
- AWS GuardDuty for threat detection
- Security Groups and NACLs for layered protection

