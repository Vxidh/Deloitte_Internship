# OS_Hardening
This repository contains Ansible playbooks used for OS Hardening of openSUSE Linux servers.  

## How do I run this?
Copy the directory onto the master server using the -scp command (you can use S3 buckets if you're running everything on AWS) and make sure that the worker servers' SSH keys (.pem\.ppk files) are already present on the master server to allow for easy authentication into the client servers.  
Execute RunMe.yml in the master server (preferably openSUSE, but RHEL distributions also work) to run the entire directory of files.  

Most of the PAM modules were sourced from dev-sec/ansible-collection-hardening  

## How does this run?
Handlers is responsible for starting/stopping services which affect the system's security. All services which are not necessary for a server have been removed to reduce attack surface.  

Services which have been disabled:  
- avahi-daemon  
- bluetooth  
- CUPS 
- RPCbind  
- SMB   
- VSFTPD    
- XINET-D    
- Apache2    

Services which have been enabled:  
- cron  
- nftables  
- UFW  
- AppArmor  
- AIDE  
- auditd  
Filesystems are also remounted on initialization to avoid any vulnerabilities.  
  
Defaults and Handlers deals with patching all vulnerabilities at the user access level.   



