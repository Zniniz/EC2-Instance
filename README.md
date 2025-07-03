# [EC2 Instance](https://roadmap.sh/projects/ec2-instance)

Create an EC2 instance on AWS and connect to it using SSH.

The goal of this project is to create an AWS account, set up a Linux server on AWS EC2, and deploy a simple static website. This project will help you gain hands-on experience with cloud computing, specifically with Amazon Web Services (AWS).

## Requirements

### You are required to complete the following tasks:
---

#### 1. Launch an EC2 Instance

1. **Sign in** to the AWS Management Console.  
2. Navigate to **EC2 → Instances → Launch Instance**.  
3. Configure:  
   - **AMI**: Ubuntu Server LTS  
   - **Instance Type**: t2.micro (Free Tier eligible)  
   - **Network**: default VPC/subnet  
4. **Key Pair**:  
   - Create a new key-pair (download the `.pem` file)  
   - Or select an existing one  
   - **Important:** never lose this file!  
5. **Security Group**: allow inbound:  
   - SSH (Port 22) from your IP  
   - Custom TCP (Port 80) from Anywhere-IPv4
   - Custom TCP (Port 80) from Anywhere-IPv6
6. Click on Advanced details
   - Scroll all the way down to user data
   ```bash
   sudo apt update
   sudo apt install -y nginx

   sudo systemctl start nginx
   sudo systemctl enable nginx
   ```
7. Click **Launch** and note your instance’s **Public IPv4** address (e.g. `3.95.21.79`).

---

## 2. Connect via SSH

```bash
# Ensure your .pem key is only user-readable
chmod 600 ~/Downloads/my-key.pem

# SSH in
ssh -i ~/Downloads/my-key.pem ubuntu@3.95.21.79






