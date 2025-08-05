# Backend Setup (Node.js API on EC2)

The backend is hosted on an EC2 instance inside a private subnet. It uses Node.js with Express to handle form submissions from the frontend.

## Setup Instructions

1. Launch EC2 instance in Private-Subnet-A
2. SSH via Bastion Host
3. Install Node.js, NPM, and PM2
4. Clone or create app in `/home/ec2-user/booking-backend`
5. Example app listens on port 3000 and writes data to `appointments.json`

## Features

- Accepts JSON and URL-encoded POST data
- Appends new appointments to local file
- Ready for upgrade to RDS (Postgres or MySQL)

