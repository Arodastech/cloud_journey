# Fail2Ban Lab

## Objective
Learn how to detect and automatically respond to brute-force SSH attacks using fail2ban.

## Steps Performed
- Installed fail2ban
- Enabled SSH monitoring (sshd jail)
- Configured retry limits and ban time
- Restarted fail2ban service
- Simulated brute-force attack using failed SSH logins
- Monitored logs using /var/log/auth.log
- Verified fail2ban status

## Key Observations
- Failed login attempts were successfully logged
- Fail2ban did not register failures or ban the IP
- SSH showed multiple authentication failures

## Issue Identified
- Running in a WSL environment prevented fail2ban from enforcing bans
- Fail2ban depends on firewall tools (iptables), which are limited in WSL

## Security Impact
- Fail2ban can automate detection and blocking of attackers in real environments
- Demonstrates the importance of system compatibility for security tools

## What I Learned
- How fail2ban detects brute-force attacks
- Difference between detection and enforcement
- Importance of logs in security monitoring
- Limitations of certain environments (WSL) in cybersecurity testing