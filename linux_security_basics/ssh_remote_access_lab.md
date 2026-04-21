# SSH Remote Access Lab

## Objective
Learn how to remotely access a Linux system using SSH and understand authentication and security concepts.

## Steps Performed
- Installed OpenSSH server
- Checked SSH service status using systemctl
- Started SSH service
- Found system IP address using ip a
- Connected to system using SSH
- Generated SSH key pair using ssh-keygen
- Copied public key using ssh-copy-id
- Logged in without password using SSH keys

## Key Concepts Learned
- SSH allows secure remote access to a system
- Public key is stored on server in authorized_keys
- Private key is used for authentication and must be protected
- Permissions must be strict for SSH to function properly
- Multiple sessions can be viewed using who and w

## Issues Encountered
- Mistyped commands (aptinstall instead of apt install)
- SSH service was inactive and had to be started
- Confusion between localhost (127.0.0.1) and actual IP
- Permission denied when trying to open files incorrectly

## Solutions
- Corrected command syntax
- Used systemctl start ssh
- Identified correct IP address (172.x.x.x)
- Used cat to read files instead of executing them

## Security Takeaways
- SSH keys are more secure than passwords
- If private key is compromised, attacker can impersonate user
- authorized_keys controls who can access the system
- Attackers may add their own key for persistent access