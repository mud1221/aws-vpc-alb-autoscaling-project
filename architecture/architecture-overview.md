# Architecture Overview

This project implements a production-style AWS architecture with secure networking, scalability, and high availability.

## Traffic Flow
User → ALB → App Servers (ASG) → Database

## Key Highlights
- Public access only via ALB
- Application and Database in private subnets
- Bastion Host for secure administration
- Auto Scaling for high availability
