# Hosting-my-first-Ubuntu-OS-on-AWS-using-AMI
---
### I successfully launched and configured my first Ubuntu server on AWS using an Amazon Machine Image (AMI). After provisioning an EC2 instance, setting up networking and security groups, and attaching persistent storage, I connected to the server via SSH using AWS key pairs. This project gave me hands-on experience with cloud provisioning, Linux administration, and secure remote access, laying the foundation for future deployments such as containerized applications and threat intelligence platforms.

---
# 1. Project Overview
- **Objective:** Launch and configure an Ubuntu server instance on AWS using Amazon Machine Images (AMI).
- **Key Skills:** Cloud provisioning, Linux administration, networking, and security.
- **Outcome:** A fully functional Ubuntu environment hosted on AWS, accessible via SSH for direct management.
  
---
## 2. AWS Setup
- **Instance Creation:** Selected Ubuntu AMI from AWS Marketplace.
  
  ![Choose Instance](https://github.com/Div20231010/Hosting-my-first-Ubuntu-OS-on-AWS-using-AMI/blob/main/1st_os_choose.png)
- **Configured EC2 Instance:** t3.large for sufficient memory and CPU resources...
   ![Choose Instance](https://github.com/Div20231010/Hosting-my-first-Ubuntu-OS-on-AWS-using-AMI/blob/main/2nd_instance_selection.png)
- **Networking:** Configured VPC and security groups...
  - Created and configured a Virtual Private Cloud (VPC).
Configured security groups to allow SSH (port 22) access, enabling me to connect from Windows PowerShell into the EC2 instance. While AWS permits setting inbound rules to 0.0.0.0/0 for open access, I restricted the rule to my specific IP address to enhance security for this project.
![Configuring my Network security group](https://github.com/Div20231010/Hosting-my-first-Ubuntu-OS-on-AWS-using-AMI/blob/main/create-security-group-allow-ssh-traffic.png)
- **Storage:** Attached Amazon EBS volume for persistent storage.
   - Attached an Amazon EBS volume to provide persistent storage, anticipating the disk space requirements of running OpenCTI on the instance. Allocating sufficient storage during setup ensured smooth operation and avoided the need for disruptive reconfiguration later.
     ![Modified my Volume to 50GB Storage](https://github.com/Div20231010/Hosting-my-first-Ubuntu-OS-on-AWS-using-AMI/blob/main/selected_volume_adjust_80gb.png)

---
## 3. Ubuntu Configuration
- **Access:** Generated and downloaded AWS key pair (.pem file)...
   - Generated and downloaded AWS key pair (.pem file) which i used together with my public ip address to securely ssh into my instance after creating.
     ![Create A new private keypair](https://github.com/Div20231010/Hosting-my-first-Ubuntu-OS-on-AWS-using-AMI/blob/main/create-a-keypair.png)

- **SSH Connection:** Use this to securely ssh into your instance via Windows Powershell
  ```bash
  ssh -i "C:\Users\Divine\Desktop\my-key.pem" ubuntu@<Elastic-IP>

![Us Powershell To Securely SSH into your instance](https://github.com/Div20231010/Hosting-my-first-Ubuntu-OS-on-AWS-using-AMI/blob/main/ssh_via_powershell_into_my_ubuntu_instance.png)

![Successfully securely SSH into the instance](https://github.com/Div20231010/Hosting-my-first-Ubuntu-OS-on-AWS-using-AMI/blob/main/successful_ssh_into_ubuntu.png)
---
## 4. Challenges & Solutions
- Challenge: Managing secure access.
- Solution: Restricted SSH access to my IPs and used AWS key pairs.
- Challenge: Resource limitations on free-tier instances.
- Solution: Use the pay as you go (Subscription Model).
---
## 5. Results
- Successfully hosted Ubuntu OS on AWS.
- Verified access by securely connecting via SSH.
---
## 6. Key Takeaways
- Learned how to provision and manage cloud-based operating systems.
- Strengthened skills in AWS networking and security.
- Built confidence in using Linux for cloud deployments and remote administration via SSH.

