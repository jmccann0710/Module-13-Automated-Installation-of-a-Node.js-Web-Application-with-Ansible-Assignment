# Module 13 - Automated Installation of a Node.js Web Application with Ansible

## Overview
This project automates the deployment of a simple Node.js web application on an Ubuntu EC2 instance using Ansible. The application is managed with PM2.

## Files Included
- app.js
- package.json
- deploy.yml
- rollback.yml
- test.sh
- README.md

## Prerequisites
- Ubuntu EC2 instance
- SSH key pair (.pem)
- Ansible installed
- Port 3000 open in the EC2 security group

## How to Run the Deployment
```bash
ansible-playbook deploy.yml
```

## Rollback
To rollback the deployment, run:
```bash
ansible-playbook rollback.yml
```

## Accessing the Application
Once deployed, open your browser and go to:
http://<your-ec2-public-ip>:3000

## Running the Verification Script
Run the test script to verify the application:
```bash
chmod +x test.sh
./test.sh
```

## Known Issues / Limitations
- Ensure port 3000 is open in the EC2 security group
- Application may not start if PM2 is not installed