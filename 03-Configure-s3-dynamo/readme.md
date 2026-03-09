# Lab 3 – Configure Web Application with Amazon S3 and DynamoDB

This lab demonstrates how to integrate a web application with **Amazon S3** for storing images and **Amazon DynamoDB** for storing employee data.

The employee directory application running on an EC2 instance is modified to retrieve employee photos from an S3 bucket and employee information from a DynamoDB table.

## Demo Video

YouTube Walkthrough:
https://youtu.be/6xGXl9wA2Bw

## Lab Overview

In this lab, the following tasks were performed:

* Created an **Amazon S3 bucket** to store employee images
* Configured an **S3 bucket policy** to allow the application to access the bucket
* Modified the application configuration to use the S3 bucket
* Uploaded employee images to the S3 bucket
* Created a **DynamoDB table** to store employee records
* Tested the application through the web interface
* Managed and updated items in DynamoDB using the AWS Management Console
* Added new employee records directly from DynamoDB


## Architecture Used

The lab environment already provided:

* A **VPC with two public subnets**
* An **Internet Gateway**
* A **Route Table with internet access**
* An **EC2 instance hosting the Employee Directory application**
* An **IAM role (EmployeeDirectoryAppRole)** attached to the EC2 instance

The application uses:

* **Amazon S3** → to store employee images
* **Amazon DynamoDB** → to store employee data


## Steps Performed

### 1. Created an S3 Bucket
### 2. Added an S3 Bucket Policy
### 3. Connected the Application to S3
### 4. Uploaded Employee Images
### 5. Created a DynamoDB Table
### 6. Tested the Web Application
### 7. Managed DynamoDB Items from Console
### 8. Added Items Directly in DynamoDB

This lab helped in understanding how AWS services integrate together to build a simple cloud-based application.
