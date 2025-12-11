Linux File Permission Hardening Project
Overview
This project demonstrates secure Linux file permission auditing, remediation, and directory hardening
to enforce least-privilege principles. Using commands such as chmod, chown, ls, and cd, permissions
were analyzed and corrected to eliminate unauthorized access.
Objectives
- Analyze file and directory permissions
- Identify unauthorized write or execute access
- Modify permissions to remove security risks
- Harden hidden files to restrict access
- Restrict directory access to authorized users only
Key Linux Commands Used
ls -l # List detailed file permissions
ls -la # List all files including hidden ones
chmod # Modify permissions
chown # Change ownership
cd # Navigate directories
Example Permission Audit
# Checking permissions
ls -l
# Sample output:
/project_k.txt rw-rw-r--
/project_m.txt rw-rw-r--
/.project_x.txt rwxrwxrwx (incorrect—should not be executable)
Fixing Incorrect Permissions
# Remove write permission for 'other'
chmod o-w project_k.txt
# Restrict hidden file to read-only for user & group
chmod 440 .project_x.txt
# Remove execute rights from drafts directory
chmod go-rwx drafts/
Project Summary
All permissions were successfully audited and hardened. Unauthorized write, read, and execute
permissions were removed. The hidden file .project_x.txt was secured, and the drafts directory was
restricted so only the appropriate owner could access it.
End of Report
