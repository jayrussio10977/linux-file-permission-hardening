# linux-file-permission-hardening
Cyber security portfolio project demonstrating Linux file permission auditing, remediation, and system hardening using chmod and least-privilege principles
Linux File Permission Hardening
Cybersecurity Portfolio Project
Overview
This project demonstrates secure file permission auditing and remediation in a Linux environment. The
goal was to ensure that users and groups had only the permissions required—nothing more—following
the principle of least privilege.
Objectives
- Analyze file and directory permissions
- Identify unauthorized write or execute access
- Modify permissions to remove security risks
- Harden a hidden file to restrict access
- Restrict directory access to authorized users only
Tools & Commands Used
- ls -l – list permissions
- ls -la – list all files including hidden
- chmod – modify permissions
- chown – identify user and group ownership
- cd – navigate directories
Key Tasks Completed
1. Permission Audit
Reviewed permissions for files such as:
- project_k.txt
- project_m.txt
- .project_x.txt
- drafts/ directory
2. Fixing Incorrect Permissions
Examples of corrections performed:
chmod o-w project_k.txt
chmod go-rw project_m.txt
chmod 440 .project_x.txt
3. Hardening the Drafts Directory
Only the user researcher2 should access the directory:
chmod go-rwx drafts
Results
- No file granted unauthorized write access
- Hidden file .project_x.txt was locked down
- Draft directory restricted to the authorized user
- All permissions aligned with least-privilege principles
Author: Jason Russio
Aspiring Cloud Security Analyst
