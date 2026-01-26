# Deployment Notes (Lab)

## Goal
Practice AWS VPC fundamentals and basic traffic flow using a simple EC2 web instance.

## Components used
- VPC
- Public subnet (EC2 web instance)
- Private subnet (created for segmentation practice)
- Route tables (basic)
- Internet Gateway (IGW)
- NAT Gateway (created to understand private outbound concept)
- Security Groups
- EC2

## Steps (high level)
1) Created a VPC and two subnets (public + private)
2) Attached an Internet Gateway (IGW) to the VPC
3) Configured route tables:
   - Public subnet route table: 0.0.0.0/0 → IGW
   - Private subnet route table: 0.0.0.0/0 → NAT Gateway (concept practice)
4) Created a Security Group with least-privilege rules (SSH/HTTP from my IP only)
5) Launched an EC2 instance in the public subnet
6) Verified access (SSH and HTTP) and captured screenshots/notes

## Validation
- SSH reachable (yes/no): tested from my machine to EC2 public IP
- HTTP reachable (yes/no): tested by browser/curl to EC2 public IP
- If not reachable, I check in this order:
  1) Security Group rules
  2) Subnet association (public subnet) + public IP
  3) Route table target (IGW)

## Notes / Mistakes I hit
- First time SSH timed out because my SG inbound rule wasn’t limited to my current IP.
- I forgot to associate the correct route table to the public subnet, so the instance wasn’t reachable.
