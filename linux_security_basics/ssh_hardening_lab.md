# SSH Hardening Lab

## Objective
Secure SSH access by disabling password authentication and enforcing key-based login.

## Steps Performed
- Verified SSH key-based login was working
- Opened SSH configuration file using nano
- Modified PasswordAuthentication to no
- Restarted SSH service
- Tested access with valid user
- Simulated attacker login attempt

## Key Observations
- Valid user could still access system using SSH key
- Invalid user was immediately denied access
- No password prompt was shown

## Security Impact
- Eliminated brute-force password attack risk
- Restricted access to only trusted key holders
- Reduced attack surface significantly

## What I Learned
- How to modify SSH configuration
- Importance of verifying access before hardening
- How disabling password authentication improves security