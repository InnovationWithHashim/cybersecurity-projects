Linux Hardening Project Report
1. Project Title

Ubuntu Linux Hardening for Cybersecurity

2. Introduction

Linux hardening is the process of securing a Linux system by reducing vulnerabilities and enforcing best security practices. It is essential for protecting servers, desktops, and networked devices from attacks.

This project demonstrates basic Linux hardening techniques on an Ubuntu system.

3. Objectives

Secure an Ubuntu system by applying best practices

Configure the firewall and access restrictions

Enable intrusion prevention measures (Fail2ban)

Review and monitor system logs for anomalies

4. Tools & Environment

Operating System: Ubuntu 22.04 (VirtualBox/VM or WSL)

Terminal / Bash

UFW Firewall

Fail2ban

5. Methodology

Installed Ubuntu on VirtualBox or WSL.

Updated all packages:

sudo apt update && sudo apt upgrade -y


Disabled root login in SSH:

sudo nano /etc/ssh/sshd_config
# PermitRootLogin no
sudo systemctl restart ssh


Configured UFW firewall:

sudo ufw enable
sudo ufw allow OpenSSH
sudo ufw status


Installed Fail2ban to prevent brute-force attacks:

sudo apt install fail2ban -y
sudo systemctl enable fail2ban
sudo systemctl status fail2ban


Audited logs for anomalies:

sudo tail -f /var/log/auth.log

6. Hardening Measures Implemented

Disabled root login over SSH

Enabled and configured UFW firewall with minimal open ports

Installed Fail2ban to block repeated failed login attempts

Audited authentication logs for suspicious activity

7. Results & Observations

System is now more secure against remote brute-force attacks

Only necessary ports are open (OpenSSH for remote access)

Fail2ban automatically blocks repeated login attempts

Logs show fewer vulnerabilities after hardening

8. Skills Learned

Linux system administration basics

SSH configuration and root security

Firewall configuration (UFW)

Intrusion detection with Fail2ban

Log monitoring and anomaly detection

9. Conclusion

This project provided hands-on experience in securing an Ubuntu Linux system. It demonstrates how simple hardening steps can greatly reduce risk and protect against common cyber threats. Linux hardening is a foundational skill for cybersecurity professionals, especially those working in system security or SOC environments.

10. References

Ubuntu Hardening Guide: https://ubuntu.com/security

UFW Documentation: https://help.ubuntu.com/community/UFW

Fail2ban Official Docs: https://www.fail2ban.org/
