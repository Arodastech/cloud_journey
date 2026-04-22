# Firewall (UFW) Lab

## Objective
Learn how to configure and manage firewall rules to control network access.

## Steps Performed
- Checked firewall status
- Allowed SSH (port 22)
- Enabled firewall
- Viewed firewall rules
- Added deny rule for SSH
- Removed allow rule
- Tested SSH connectivity

## Key Observations
- Firewall rules control access to services like SSH
- Rule order affects behavior
- Localhost (127.0.0.1) traffic was not blocked
- External traffic would be blocked in a real environment

## Security Impact
- Firewall adds a network-level defense layer
- Can block unauthorized access attempts
- Works alongside SSH hardening for layered security

## What I Learned
- How to enable and manage UFW
- Importance of allowing SSH before enabling firewall
- Difference between local and external traffic
- How firewall rules affect system behavior

## After Notes
- This lab demonstrated the importance of firewall rules in protecting a system from external access.
- Traffic from the localhost (127.0.0.1) is considered loopback and is typically trusted, which is why SSH connections were still allowed during testing.
- In a real-world scenario, external IP addresses would be subject to firewall rules, and unauthorized SSH attempts would be blocked.
- This shows how firewalls help control access by allowing trusted traffic while denying potentially malicious connections.