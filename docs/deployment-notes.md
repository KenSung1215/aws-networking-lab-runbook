# Deployment Notes (Lab)

## Goal
Practice basic VPC traffic flow and access control using a simple EC2 instance.

## Components used
- VPC
- Subnets (public/private concepts)
- Route tables (basic)
- IGW / NAT (lab use)
- Security Groups
- EC2

## Steps (high level)
1) Create VPC and subnets  
2) Configure route tables (basic routes)  
3) Attach IGW (for public connectivity)  
4) Configure NAT (for private outbound, if used)  
5) Create Security Group rules (least privilege)  
6) Launch EC2 and validate SSH/HTTP access  
7) Record results and screenshots

## Validation
- SSH reachable? (yes/no)
- HTTP reachable? (yes/no)
- If not reachable: check SG → routes → subnet association in that order

