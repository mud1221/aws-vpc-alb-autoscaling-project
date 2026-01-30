##### aws-vpc-alb-autoscaling-project 

# Production-Ready AWS VPC with ALB and Auto Scaling

## 📌 Overview
This project demonstrates the design and implementation of a secure, scalable, and production-ready AWS infrastructure for a web application using AWS best practices.

The architecture includes a custom VPC with public and private subnets, Application Load Balancer (ALB), Auto Scaling Group (ASG) using a Golden AMI, a Bastion Host for secure access, and a private database tier.

---

## 🏗 Architecture Flow
User → Application Load Balancer → Auto Scaling Group (App Servers) → Database Server

---

## 🧩 AWS Services Used
- Amazon VPC
- EC2
- Application Load Balancer (ALB)
- Auto Scaling Group (ASG)
- Launch Template
- Amazon RDS / EC2-based Database
- IAM
- CloudWatch

---

## 🌐 Network Design
- VPC CIDR: `10.0.0.0/16`
- Public Subnet: ALB and Bastion Host
- Private Subnets: Application servers and Database
- Internet Gateway for public access
- Private routing for internal communication

---

## 🔐 Security Design
- Bastion Host allows SSH access to private instances
- ALB exposes only HTTP/HTTPS to the internet
- App Servers accept traffic only from ALB
- Database accepts traffic only from App Servers
- No public IPs assigned to App or DB servers

---

## ⚙ Application Layer
- Application servers deployed in private subnets
- Golden AMI created from a configured app server
- Launch Template used for instance consistency
- Auto Scaling Group provides scalability and self-healing

---

## 📈 Auto Scaling Configuration
- Min capacity: 2
- Desired capacity: 2
- Max capacity: 5
- Health check type: ELB
- Scaling based on CPU utilization

---

## 📊 Monitoring & Reliability
- ALB health checks
- CloudWatch metrics for EC2 and ASG
- Automatic replacement of unhealthy instances

---

## 🚀 Future Enhancements
- Infrastructure as Code using Terraform
- CI/CD pipeline
- RDS Multi-AZ
- HTTPS using ACM
- Blue-Green deployments

---

## 👤 Author
**Mudasir Patel**  
Aspiring DevOps / Cloud Engineer
