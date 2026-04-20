# Linux User and Permission Security Lab

## Objective

Learn how Linux manages users, groups, and file permissions to control system access.

## Commands Practiced

whoami  
id  
groups  
useradd  
passwd  
su  
chmod  
chown  

## Why This Matters

Linux systems power most cloud infrastructure.  
Understanding users and permissions is critical for preventing unauthorized access and maintaining system security.

## Lab Steps

1. Check the current user
2. View user groups
3. Create a test user
4. Assign a password
5. Switch users
6. Modify file permissions

## Lab Results 

### Step 1 – Check current user

Command:
whoami

Output:
anthony

Explanation:
This command shows which user is currently logged into the Linux system.

---

### Step 2 – Check user ID and groups

Command:
id

Output:
uid=1000(anthony) gid=1000(anthony) groups=1000(anthony),27(sudo)

Explanation:
This command displays the user ID, group ID, and any groups the user belongs to.

---

### Step 3 – View user groups

Command:
groups

Output:
anthony sudo

Explanation:
This command shows which permission groups the current user belongs to.