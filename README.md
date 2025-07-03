# [EC2 Instance](https://roadmap.sh/projects/ec2-instance)

Create an EC2 instance on AWS and connect to it using SSH.

The goal of this project is to create an AWS account, set up a Linux server on AWS EC2, and deploy a simple static website. This project will help you gain hands-on experience with cloud computing, specifically with Amazon Web Services (AWS).

## Requirements

You are required to complete the following tasks:

- Create an AWS account if you don’t have one already.
- Familiarize yourself with the AWS Management Console.
- Launch an EC2 instance with the following specifications:
      - Use Ubuntu Server AMI.
      - Choose a t2.micro instance type (eligible for AWS Free Tier).
      - Use the default VPC and subnet for your region.
      - Configure the security group to allow inbound traffic on ports 22 (SSH) and 80 (HTTP).
	`SSH will already be configured to port 22`
	`Add two rules with custom TCP, Port Range set as 80, 1 as IPv4 and 2 as IPv6`
      - Create a new key pair or use an existing one for SSH access.
	`Don't lose the .pem file`
      - Assign a public IP address to your instance.
	`0.0.0.0 format`
- Connect to your EC2 instance using SSH and the private key.
  `sasfsdf`
- Update the system packages and install a web server (e.g., Nginx).
- Create a simple HTML file for your static website.
- Deploy the static website to your EC2 instance.
- Access your website using the public IP address of your EC2 instance.

