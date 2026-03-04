# AWS IAM – Users, Groups and Policies Lab

This lab was done as part of AWS Technical Essentials training.  
The goal of the lab was to understand how AWS Identity and Access Management (IAM) works and how permissions are controlled using users, groups, and policies.

## What I Did

1. Opened the AWS Management Console and explored the IAM dashboard.
2. Checked the IAM users created in the lab (user-1, user-2, user-3).
3. Explored the IAM groups:
   - S3-Support
   - EC2-Support
   - EC2-Admin
4. Reviewed the policies attached to each group to understand their permissions.
5. Added users to the appropriate groups based on their job role.

User assignments:
- user-1 → S3-Support  
- user-2 → EC2-Support  
- user-3 → EC2-Admin  

## Testing Access

I used the IAM sign-in URL to log in with different users and verify their permissions.

- **user-1** was able to view Amazon S3 resources but could not access EC2.
- **user-2** could view EC2 instances but could not stop or modify them.
- **user-3** had permission to view and stop EC2 instances.

This helped demonstrate how IAM groups and policies control access to AWS services.

## Services Used

- AWS Identity and Access Management (IAM)
- Amazon EC2
- Amazon S3

## Demo

Video recording of the lab:  
(https://youtu.be/20sp1VLvic4?si=l0khm0LKqK_vpWTW)
