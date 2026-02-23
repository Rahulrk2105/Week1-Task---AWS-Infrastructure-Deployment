# Week1-Task---AWS-Infrastructure-Deployment

---

# 📌 Project Overview

This project demonstrates the deployment and configuration of a complete AWS cloud infrastructure environment using core AWS services.

The objective was to:

- Create and manage IAM users and policies
- Configure secure S3 bucket access
- Deploy and configure an EC2 web server
- Resize EBS storage
- Attach a custom Elastic Network Interface (ENI)
- Create an AMI and launch replica instances

This project simulates real-world cloud infrastructure deployment and management.

---

# 🏗 AWS Services Used

- AWS IAM
- Amazon S3
- AWS CLI
- Amazon EC2
- Amazon EBS (gp3)
- Elastic Network Interface (ENI)
- Apache HTTP Server
- Amazon Machine Image (AMI)

---

# 🔐 Step 1: IAM Configuration

### ✔ Tasks Performed
- Created IAM user
- Generated access key & secret key
- Configured AWS CLI
- Created custom S3 ReadOnly policy
- Created IAM role for EC2
- Created user group with ReadOnlyAccess policy

### 📷 Screenshots

![IAM User](screenshots/01_IAM_User.png)  
![IAM Policy](screenshots/02_IAM_Policy.png)  
![IAM Role](screenshots/03_IAM_Role.png)  
![Access Key](screenshots/04_Access_Key.png)

---

# 🪣 Step 2: S3 Bucket Configuration

### ✔ Tasks Performed
- Created S3 bucket: `rahul-week1-bucket`
- Attached custom read-only policy
- Verified access using AWS CLI

### 📌 Command Used

```bash
aws s3 ls s3://rahul-week1-bucket
📷 Screenshots




🖥 Step 3: EC2 Instance Deployment
✔ Configuration

Amazon Linux 2023

Instance Type: t2.micro (initial)

Upgraded to: t2.medium

Security Group configured (Ports 22 & 80)

IAM Role attached

📷 Screenshot

💾 Step 4: EBS Volume Resize
✔ Tasks Performed

Increased root volume from 30GB → 50GB

Verified filesystem (XFS)

📌 Command Used
lsblk -f
📷 Screenshot

🌐 Step 5: Elastic Network Interface (ENI)
✔ Tasks Performed

Created custom ENI

Attached ENI to EC2 instance

Verified successful attachment

📷 Screenshots




🌍 Step 6: Apache Web Server Setup
✔ Tasks Performed

Installed Apache (httpd)

Started and enabled service

Created custom web page

Verified via browser using Public IP

📌 Commands Used
sudo yum install httpd -y
sudo systemctl start httpd
sudo systemctl enable httpd
echo "Hello from Week1 Project" | sudo tee /var/www/html/index.html
📷 Screenshots






📦 Step 7: AMI Creation & EC2 Replication
✔ Tasks Performed

Created AMI from configured EC2 instance

Launched 2 replica instances from AMI

Verified instances running successfully

📷 Screenshots




🎯 Final Outcome

Successfully deployed and validated a complete AWS infrastructure environment including:

Secure IAM setup

Controlled S3 access

EC2 web server deployment

EBS storage management

Custom networking configuration

AMI-based scaling concept

🧠 Skills Demonstrated

AWS Identity & Access Management (IAM)

S3 bucket policy configuration

AWS CLI configuration & usage

EC2 provisioning & management

Linux system administration

Apache web server deployment

EBS volume expansion

Networking using ENI

AMI creation & replication

⚠️ Security Notice

All access keys and sensitive credentials have been rotated or removed prior to publishing this repository.

📌 Conclusion

This project provides hands-on experience in AWS cloud infrastructure management and demonstrates practical knowledge in deploying and managing cloud resources securely and efficiently.
