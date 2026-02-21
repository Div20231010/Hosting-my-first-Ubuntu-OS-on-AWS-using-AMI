# Hosting-my-first-Ubuntu-OS-on-AWS-using-AMI
---
### I successfully launched and configured my first Ubuntu server on AWS using an Amazon Machine Image (AMI)
---
# Project Overview
- **Objective:** Launch and configure an Ubuntu server instance on AWS using Amazon Machine Images (AMI).
- **Key Skills:** Cloud provisioning, Linux administration, networking, and security.
- **Outcome:** A fully functional Ubuntu environment hosted on AWS, accessible via SSH for direct management.

## 2. AWS Setup
- **Instance Creation:** Selected Ubuntu AMI from AWS Marketplace.
- **Configured EC2 Instance:** t3.large for sufficient memory and CPU resources...
- **Networking:** Configured VPC and security groups...
- **Storage:** Attached Amazon EBS volume for persistent storage...

## 3. Ubuntu Configuration
- **Access:** Generated and downloaded AWS key pair (.pem file)...
- **SSH Connection:**
  ```bash
  ssh -i "C:\Users\Divine\Desktop\my-key.pem" ubuntu@<Elastic-IP>
