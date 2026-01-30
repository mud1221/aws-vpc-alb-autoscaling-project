# VPC Design

- VPC CIDR: 10.0.0.0/16
- Designed to support public and private subnets

## Subnets
- Public Subnet: ALB, Bastion Host
- Private App Subnet: Application servers
- Private DB Subnet: Database server

## Routing
- Internet Gateway attached to VPC
- Public route table routes 0.0.0.0/0 to IGW
- Private subnets have no direct internet access
