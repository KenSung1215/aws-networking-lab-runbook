# AWS Networking Lab Runbook (Fundamentals)

These are my personal lab notes written in a runbook/checklist style so I can repeat the setup quickly.
Hands-on notes from AWS fundamentals labs focusing on VPC basics, traffic flow, and troubleshooting.  
This repo is documentation-first (runbook style) rather than a production architecture.

## What I practiced (fundamentals)
- VPC, subnets (public/private concepts)
- Route tables (basic)
- Internet Gateway (IGW) and NAT (conceptual + basic lab use)
- Security Groups (inbound/outbound basics)
- EC2 connectivity checks (SSH/HTTP)

## How to use this repo
- Deployment steps: `docs/deployment-notes.md`
- Troubleshooting checklist: `docs/troubleshooting.md`
- Diagram/screenshots: `diagrams/` and `screenshots/`

## Validation approach
I verify changes with simple tests (e.g., SSH/HTTP reachability, ping/traceroute, basic DNS checks) and record what each result suggests.

## Notes
All work is done in legal lab environments. No production systems are targeted.
