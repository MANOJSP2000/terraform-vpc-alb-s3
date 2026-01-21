# Terraform VPC + ALB + S3 Infrastructure

This project provisions a complete AWS infrastructure using Terraform.  
It includes a custom VPC, public/private subnets, Internet Gateway, NAT Gateway, Application Load Balancer (ALB), EC2 instances, and an S3 bucket.

---

## 📌 Architecture Overview

The Terraform code deploys the following AWS resources:

### 🔹 Networking (VPC)
- Custom VPC
- 2 Public Subnets (across 2 Availability Zones)
- 2 Private Subnets (across 2 Availability Zones)
- Internet Gateway (IGW)
- NAT Gateway for Private Subnet Internet Access
- Public & Private Route Tables
- Route Table Associations

### 🔹 Security
- Security Group for ALB  
- Security Group for EC2 Instances  
- S3 Bucket Access Policies

### 🔹 Compute
- EC2 instances launched inside private subnets
- User Data for automatic package installation (optional)

### 🔹 Load Balancing
- Application Load Balancer (ALB)
- ALB Target Group
- ALB Listener (HTTP port 80)
- Attachment of EC2 instances to the Target Group

### 🔹 Storage
- S3 bucket with:
  - Versioning
  - Server-side encryption
  - Private access

