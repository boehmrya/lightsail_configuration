# lightsail_configuration


## IP Address
52.3.221.91


## Software Installed
Installed the finger package


## Summary of Configuration Changes
Upgraded all existing packages

Changed ssh port in /etc/ssh/sshd_config file to 2200

Via the firewall (UFW) enabled SSH (port 2200), HTTP (port 80), and NTP (port 123).

Created new user grader

Added ssh public key for grader in /home/grader/.ssh/authorized_keys

Enable sudo privileges for grader via modifications to /etc/sudoers.d/grader

Turned password authentication off in /etc/ssh/sshd_config file

Configured the local timezone to UTC
