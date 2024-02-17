# Born2BeRoot

##  Table of Contents
1. [Description](#description)
2. [General Instructions](#general-instructions)
3. [Project Requirements](#project-requirements)
   - [Operating System](#operating-system)
   - [SSH Configuration](#ssh-configuration)
   - [Firewall Configuration](#firewall-configuration)
   - [Hostname and Users](#hostname-and-users)
   - [Password Policy](#password-policy)
4. [Monitoring Script](#monitoring-script)
5. [Bonus](#bonus)
   - [Partitions Configuration](#partitions-configuration)
   - [WordPress Site Configuration](#wordpress-site-configuration)
   - [Additional Service Configuration](#additional-service-configuration)
6. [License](#license)


## Description
"Born to Be Root" is a project focused on setting up your first server using VirtualBox (or UTM if VirtualBox is incompatible with your machine), following a set of specific instructions. By the end of this project, you will be capable of configuring your own operating system under stringent rules, ensuring a secure and efficient server environment.

## General Instructions
VirtualBox Usage: The use of VirtualBox is mandatory for this project (UTM can be used if VirtualBox does not work on your machine).
Submission: You are only required to submit a file named signature.txt at the root of your repository. This file should contain the signature of your virtual machine's disk. See the "Submission and Evaluation" section for more details.

## Project Requirements

### Operating System
You must choose the latest stable version of Debian (not testing/unstable) or the latest stable version of Rocky as the operating system. Debian is strongly recommended if you have no experience in system administration.


###SSH Configuration
The SSH service must run on port 4242 only. It must not be possible to connect via SSH as root for security reasons.
Firewall Configuration
Configure your operating system with UFW (or firewalld in Rocky), leaving only port 4242 open.
Hostname and Users
The hostname of your virtual machine must be your login ending in 42 (e.g., wil42). You must modify this hostname during your evaluation.
Implement a strong password policy.
Install and configure sudo following strict rules.
Besides the root user, a user with your login as the name must exist and belong to the groups user42 and sudo.
Password Policy
Your password policy must meet the following criteria:

Passwords must expire every 30 days.
The minimum number of days before modifying a password must be 2.
Users must receive a warning message 7 days before their password expires.
Passwords must be at least 10 characters long, containing at least one uppercase letter and a number, and must not have more than 3 consecutive identical characters.
Passwords cannot contain the username.
For sudo group passwords: authentication with sudo must be limited to three attempts in case of an incorrect password, a custom message must be shown on incorrect password entry, and the input/output of each command executed with sudo must be logged in /var/log/sudo/. TTY mode must be enabled, and secure paths must be specified.
Monitoring Script
Develop a simple script named monitoring.sh in bash. This script, when the server starts, will display certain information (listed below) on all terminals every 10 minutes (check out wall). The script must always show the following information: OS architecture and kernel version, physical and virtual core numbers, current available RAM and its usage percentage, current disk space and its usage percentage, current CPU usage percentage, date and time of the last reboot, whether LVM is active, the number of active connections, the number of server users, the server's IPv4 address and its MAC address, and the number of commands executed with sudo.
Bonus
Correctly configure partitions to achieve a structure as shown below:
Configure a functional WordPress site with lighttpd, MariaDB, and PHP.
Configure an additional service of your choice (excluding NGINX/Apache2) that you consider useful. You must justify your choice during the defense.
License
[Specify the license here, e.g., MIT License]

