# AWS Lab 2 – VPC and EC2 Web Application

This lab demonstrates how to create a custom VPC and deploy a web application on an Amazon EC2 instance using a user data script.

## 🎥 Lab Video



## Lab Overview

In this lab I performed the following tasks:

- Created a **custom VPC**
- Created **two public subnets**
- Configured an **Internet Gateway**
- Added a **route table for internet access**
- Created a **security group**
- Launched an **EC2 instance**
- Deployed a **web application using a user data script**


## Architecture

Components used:

- VPC (`10.0.0.0/16`)
- Public Subnet 1 (`10.0.0.0/24`)
- Public Subnet 2 (`10.0.1.0/24`)
- Internet Gateway
- Route Table
- Security Group (HTTP access)
- EC2 Instance (Amazon Linux 2023)


## EC2 Configuration

- **AMI:** Amazon Linux 2023  
- **Instance Type:** t3.micro  
- **Public IP:** Enabled  
- **Security Group:** HTTP (Port 80) allowed from anywhere  


## User Data Script

The EC2 instance runs this script automatically to install dependencies and start the application.

```bash
#!/bin/bash -ex

yum -y update

curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.0/install.sh | bash

export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"

nvm install 20

mkdir -p /var/app

wget https://aws-tc-largeobjects.s3-us-west-2.amazonaws.com/ILT-TF-100-TECESS-5/app/app.zip

unzip app.zip -d /var/app/

cd /var/app/

npm install

npm start
