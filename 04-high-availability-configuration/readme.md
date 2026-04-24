# AWS High Availability Setup

This project shows how I set up a highly available web application on AWS using a load balancer and auto scaling.

## 🎥 Demo Video
Watch the full implementation here:  
👉 https://your-youtube-link-here


## What I did
- Reviewed an existing EC2 web app  
- Created a target group and configured health checks  
- Set up an Application Load Balancer across multiple AZs  
- Created a launch template with user data to run the app  
- Configured an Auto Scaling Group (min: 2, max: 4)  
- Connected everything so traffic is balanced automatically  

## Testing
- Refreshed the app to see traffic shifting across AZs  
- Ran stress testing to increase load  
- Observed new EC2 instances launching automatically  

## Issue & Fix
Faced “unhealthy target” issue initially.  
Fixed it by correcting user data (S3 bucket names and region) and redeploying instances.

## Outcome
Application became scalable and remained available even under load.
