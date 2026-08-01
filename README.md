# AWS EC2 Web Server Automation

Automated deployment of an Apache Web Server on an Amazon EC2 instance using EC2 User Data. 



## Project Overview

This project showcases how to automate the deployment of a web server on AWS using Amazon EC2 and Bash scripting. By leveraging EC2 User Data, the server is fully configured during its first boot, reducing manual effort and ensuring consistent deployments.

The project also demonstrates secure access using SSH Key Pairs, Security Groups, and verification of the deployment using Linux commands and cloud-init logs.



## Features

- Launch Amazon EC2 Instance
- Configure Security Group Rules
- Secure SSH Access using Key Pair
- Automated Apache Installation
- Automated Service Start and Enable
- Automatic HTML Page Creation
- Website Accessible through Public IP
- Verification using Linux Commands
- cloud-init Log Verification
- Complete Project Documentation



## Project Architecture


User
   │
   ▼
Internet
   │
   ▼
Security Group
(SSH 22, HTTP 80, HTTPS 443)
   │
   ▼
EC2 Instance
Amazon Linux 2023
t2.micro
   │
   ▼
EC2 User Data Script
   │
   ├── Update System
   ├── Install Apache
   ├── Start Apache
   ├── Enable Apache
   └── Create index.html
   │
   ▼
Apache HTTP Server
   │
   ▼
Custom Website


## Project Structure


aws-ec2-web-server-automation/
│
├── README.md
├── architecture/
│   └── architecture-diagram.png
│
├── documentation/
│   └── AWS-EC2-WebServer-Automation.pdf
│
├── userdata/
│   └── install_apache.sh
│
└── screenshots/
    ├── 01-aws-console-home.png
    ├── 02-keypair-created.png
    ├── 03-security-group.png
    ├── 04-launch-instance.png
    ├── 05-instance-running.png
    ├── 06-webpage.png
    ├── 07-httpd-status.png
    ├── 08-index-html.png
    ├── 09-cloud-init-output.png
   

## Deployment Steps

### 1. Create an EC2 Key Pair

- RSA Key Pair
- .pem format

### 2. Create a Security Group

Inbound Rules:

- SSH (22) – Anywhere
- HTTP (80) – Anywhere
- HTTPS (443) – Anywhere

Outbound Rules:

- Allow All Traffic (Default)

### 3. Launch EC2 Instance

- Amazon Linux 2023
- t2.micro
- Existing Key Pair
- Existing Security Group
- User Data Script

### 4. Execute User Data

The User Data script automatically:

- Updates the operating system
- Installs Apache HTTP Server
- Starts Apache
- Enables Apache on boot
- Creates a custom HTML webpage

### 5. Verify Deployment

- EC2 Running
- Status Checks Passed
- Apache Running
- Apache Enabled
- Website Accessible
- cloud-init Logs Verified

---


## Verification

The deployment was verified using:

bash
systemctl status httpd

systemctl is-enabled httpd

cat /var/www/html/index.html

sudo cat /var/log/cloud-init-output.log



## Screenshots

Project screenshots are available in the **screenshots/** directory.

The documentation PDF includes all implementation screenshots with explanations.


## Skills Demonstrated

- Amazon EC2
- Linux Administration
- Amazon Linux 2023
- Apache HTTP Server
- EC2 User Data
- Bash Scripting
- Security Groups
- SSH
- Infrastructure Automation
- Cloud Deployment
- Technical Documentation
- Git & GitHub




## Documentation

Detailed project documentation is available in:


documentation/AWS-EC2-WebServer-Automation.pdf



## Author

**Ayush Nigade**

B.Tech Computer Engineering

Aspiring AWS & DevOps Engineer

GitHub: https://github.com/Ayush-Nigade


## License

This project is created for educational purposes
