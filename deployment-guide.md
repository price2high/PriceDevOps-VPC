# Deployment Guide

## Prerequisites

- VPC with configured subnets and route tables
- Bastion host and backend EC2 running
- S3 bucket for frontend static hosting

## Frontend

- Upload HTML files to S3
- Set permissions and hosting endpoint
- Test site via public link

## Backend

- SSH into EC2 via Bastion
- Pull backend code
- Run with `node server.js` or use `pm2`
- Ensure SG and NACL allow port 3000 access from S3 or public web server

## Optional Enhancements

- Add HTTPS via Nginx reverse proxy
- Store logs in CloudWatch
- Add email notifications via SES
