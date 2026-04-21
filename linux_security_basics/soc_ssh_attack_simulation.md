# SOC SSH Attack Simulation Lab

## Objective
Simulate and analyze SSH brute-force login attempts using system logs.

## Steps Performed
- Monitored SSH logs using `tail -f /var/log/auth.log`
- Simulated failed login attempts using SSH with invalid and valid users
- Observed log entries for failed authentication attempts
- Used grep to filter failed login attempts
- Counted total attempts using wc -l
- Extracted IP addresses from logs using awk

## Key Observations
- Multiple failed login attempts were recorded
- Logs showed both "invalid user" and "failed password for valid user"
- All attempts came from the same IP address (127.0.0.1)
- Repeated attempts in a short period indicate brute-force behavior

## Analysis
- Invalid user attempts indicate username guessing
- Valid user attempts (anthony) are more dangerous because the attacker identified a real account
- The attack pattern suggests a low-volume brute-force attempt from a single source

## Security Risks
- Brute-force attacks can eventually compromise weak passwords
- Valid usernames increase the likelihood of a successful attack
- Logs must be monitored to detect suspicious activity early

## Recommended Actions
- Block attacking IP using firewall (ufw)
- Disable password authentication for SSH
- Enforce SSH key-based authentication
- Monitor logs continuously for suspicious activity
- Use tools like fail2ban to automatically block repeated attempts

## What I Learned
- How to monitor SSH logs in real time
- How to identify brute-force attack patterns
- Difference between invalid user and valid user attacks
- Basic incident response steps for SSH attacks