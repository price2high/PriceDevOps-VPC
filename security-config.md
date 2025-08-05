# Security Configuration

## Security Groups

- Bastion: Allow SSH (22) from specific IP only
- App Server: Allow 3000 from Bastion or load balancer
- DB Server: Allow 3306 only from App Server SG

## Network ACLs

### Public Subnet

- Inbound: Allow HTTP (80), SSH (22), Ephemeral ports
- Outbound: Allow ALL

### Private Subnet

- Inbound & Outbound: Only allow traffic from 10.0.0.0/16

## Monitoring Tools

- AWS GuardDuty: Intrusion detection, port scan alerts
- AWS CloudTrail: User and service activity logging
- CloudWatch Logs: Flow Logs and custom backend logs

