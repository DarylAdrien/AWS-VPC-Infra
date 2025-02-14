# AWS-VPC-Infra

## Overview

This project sets up a highly available and scalable AWS infrastructure using VPC, public and private subnets, an Application Load Balancer (ALB), and an Auto Scaling Group (ASG). The architecture ensures secure and efficient traffic distribution across multiple availability zones.

## Architecture Diagram

![AWS-vpc](./aws_vpc.png)


## Features

Virtual Private Cloud (VPC): Custom VPC with public and private subnets.

Public & Private Subnets: Public subnets host NAT gateways, and private subnets host application servers.

Application Load Balancer (ALB): Distributes incoming traffic to backend instances.

Auto Scaling Group (ASG): Automatically scales instances based on demand.

Security Groups: Configured for secure communication between resources.

NAT Gateway: Allows private instances to access the internet securely.

Multi-AZ Deployment: Ensures high availability across different availability zones.

## Prerequisites

Before deploying this infrastructure, ensure you have:

    - An AWS account with required permissions

    - Terraform installed (if using Terraform for provisioning)

    - AWS CLI configured with proper credentials

## Deployment Steps

1. Clone the Repository

        git clone <repo-url>
        cd <repo-name>

2. Configure AWS Credentials

Ensure your AWS CLI is configured properly:

    aws configure

3. Deploy Infrastructure

If using Terraform:

    terraform init
    terraform apply -auto-approve

4. Validate Deployment

Check resources in AWS:

    - VPCs in VPC Dashboard
  
    - Load Balancer in EC2 > Load Balancers
  
    - Auto Scaling Group in EC2 > Auto Scaling Groups

## Cleanup

To destroy the deployed infrastructure:

    terraform destroy -auto-approve

## License

This project is licensed under the MIT License.


