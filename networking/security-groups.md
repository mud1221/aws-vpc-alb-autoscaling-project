# Security Groups Design

## Bastion Host SG
- Inbound: SSH (22) from admin IP
- Outbound: All

## ALB SG
- Inbound: HTTP/HTTPS from internet
- Outbound: App port to App Server SG

## App Server SG
- Inbound: App port from ALB SG
- Inbound: SSH from Bastion SG
- Outbound: DB port to DB SG

## DB Server SG
- Inbound: DB port from App Server SG
- No public access allowed
