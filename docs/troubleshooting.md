# Troubleshooting Checklist (Lab)

## Symptom: SSH timeout
- Check SG inbound allows SSH from my IP
- Verify instance is in the expected subnet
- Verify route table association for that subnet
- Confirm public IP / reachability (if applicable)

## Symptom: HTTP not reachable but SSH works
- Check SG inbound for port 80
- Confirm web server is running
- Confirm instance is listening on port 80

## Symptom: Private subnet cannot reach internet (outbound)
- Check NAT exists and route table points to NAT (basic)
- Confirm SG outbound allows required ports

