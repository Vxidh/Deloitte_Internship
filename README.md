# OS_Hardening
This repository contains Ansible playbooks used for OS Hardening of openSUSE Linux servers.  
Copy the directory onto the master server using the -scp command (you can use S3 if you're running everything on AWS) and make that the worker servers' SSH keys (.pem or .ppk file) are already present on the master server to allow for easy authentication.  
  
Please enter the names of the .pem files in the hosts.ini file otherwise it won't connect :D
