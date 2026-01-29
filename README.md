# linux-access-control-auditor

# Project Overview
This project is a Linux system auditing tool designed to inspect users, groups, directories, and file permissions. It automates the process of checking for misconfigurations, logging access rights, and reporting potential security issues. The goal of this project is to demonstrate practical OS fundamentals, Linux filesystem knowledge, and scripting skills relevant to Operational Technician and system administration roles.

# Key Skills and Concepts Covered
- Linux users, groups, and permissions
- File system structure and access rights
- Bash/Python scripting for automation
- Command-line tools and file I/O in Linux
- Defensive programming and error handling
- Logging and reporting for audits
- Security awareness in system administration

# Project Tasks / Features
1. User & Group Auditing: verify users exist, list groups, detect misconfigurations
2. Directory & File Permissions: check existence, report owner/group/permissions, flag insecure settings
3. Automated Audit Script: Bash or Python script that accepts target users and directories, logs results with issues noted
4. Optional/Advanced: highlight insecure files, detect ownership mismatches, summarize results in table or CSV

# Deliverables
- Repo contains:
  - scripts/ — audit script(s)
  - sample_output/ — example log files
  - docs/permissions-explained.md — notes on OS concepts and security rationale
  - README.md — project description + instructions
- Screenshot showing audit output for demonstration



# How to Run



- Example for Bash script:
  - chmod +x audit_permissions.sh ./audit_permissions.sh --users user1,user2 --dirs /secure/data,/home/projects

- Example for Python script:
  - python3 audit_permissions.py --users user1 user2 --dirs /secure/data /home/projects

The script will produce a log file similar to:

User: user1 — EXISTS<br>

Directory/File: /secure/data — rwxr-x---<br>
Owner: user1<br>
Group: security<br>
Potential issues: None<br>

Directory/File: /secure/data/file1.txt — rw-r-----<br>
Owner: user1<br>
Group: security<br>
Potential issues: World-readable file<br>

User: user2 — MISSING<br>


# Learning Outcomes
- Learned how Linux exposes user, group, and permission information
- Practiced parsing system files and automating audits
- Gained experience handling errors, missing files, and edge cases
- Built a real-world system administration tool that could be extended for professional environments



