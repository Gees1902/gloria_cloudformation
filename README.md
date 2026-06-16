# gloria_cloudformation

# AWS CloudFormation Project

## Project Overview

The objective was to design and deploy a custom network architecture that supports public and private resources while following AWS networking and security best practices.

This project demonstrates how to deploy a secure and scalable Virtual Private Cloud (VPC) environment in AWS using Infrastructure as Code (IaC) with AWS CloudFormation. It contains AWS CloudFormation templates used to deploy AWS infrastructure as code. 


## Architecture Components

* VPC
* Public Subnets
* Private Subnets
* Internet Gateway
* Bastion Host
* Route Tables
* Auto Scaling Group (ASG)
* Relational Database Service (RDS)
* Simple Storage Service (s3)
* Identity Access Management (IAM)
* Elastic Computing Cloud (EC2)

## Resources Deployed

The CloudFormation template deployed the following resources:

Custom VPC with a CIDR block of 10.0.0.0/16
Public Subnet for internet-facing resources
Private Application Subnet
Private Database Subnet
Additional subnets in a second Availability Zone for high availability
Internet Gateway (IGW)
Route Tables and Route Associations
Bastion Host for secure administrative access
Security Groups for controlled network access


## Files

* `vpc.yaml` - Created the VPC
* `ec2.yaml` - Created the ec2 instances
* `iam.yaml` - Created users permission
* `s3-bucket.yaml` - Creates an S3 bucket
* `igw.yaml` - Created an Internet Gateway
* `route-table.yaml` - Creates Route Tables
* `asg.yaml` - Created an Auto Scaling Group
* `rds.yaml` - Created the database


## Key Features

High Availability

Resources were distributed across multiple Availability Zones to improve fault tolerance and availability.

Network Segmentation

Public and private subnets were separated to reduce the attack surface and improve security.

Secure Administration

A Bastion Host was deployed in the public subnet to provide controlled SSH access to resources within private subnets.

Infrastructure as Code (IaC)

All networking resources were provisioned using AWS CloudFormation, enabling consistent, repeatable, and version-controlled deployments.

## Deployment Commands



Deploy a CloudFormation stack using:

```bash
aws cloudformation create-stack --stack-name my-stack --template-body file://template.yaml
```

## Deployment Validation

The deployment was validated using:

AWS CloudFormation stack status checks
AWS VPC Dashboard verification
Subnet verification
Internet Gateway attachment verification
Route Table validation
Successful SSH connection to the Bastion Host

Verify deployments in:

* AWS CloudFormation Console
* AWS VPC Dashboard
* AWS EC2 Dashboard

## Architecture Screenshot 

C:\Users\User\Documents\gloria_cloudformation\screenshots1\vpc-created.PNG
C:\Users\User\Documents\gloria_cloudformation\screenshots1\public subnet routes to the igw.PNG
C:\Users\User\Documents\gloria_cloudformation\screenshots1\iam template created.PNG
C:\Users\User\Documents\gloria_cloudformation\screenshots1\asg created.PNG
C:\Users\User\Documents\gloria_cloudformation\screenshots1\rds template created.PNG
C:\Users\User\Documents\gloria_cloudformation\screenshots1\static website bucket.PNG
screenshots1/Highly Secure VPC Architecture.PNG



## Skills Demonstrated
AWS Networking
Virtual Private Cloud (VPC) Design
Public and Private Subnets
Internet Gateways
Route Tables
Security Groups
EC2 Bastion Hosts
AWS CloudFormation
Infrastructure as Code (IaC)
Cloud Security Fundamentals

Lessons Learned

This project reinforced the importance of network segmentation, secure remote administration, and automated infrastructure deployment. Using CloudFormation simplified the deployment process while ensuring consistency and repeatability across environments.

## Author

Gloria Page
Cloud Security Engineer Apprentice
