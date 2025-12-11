SOC Home Lab Project Report
1. Project Title

SOC Home Lab: Security Monitoring with Wazuh

2. Introduction

A Security Operations Center (SOC) monitors network and system activity to detect and respond to cyber threats. Wazuh is an open-source SIEM tool used to collect logs, analyze events, and generate alerts.

This project demonstrates how to set up a basic SOC home lab and analyze security events.

3. Objectives

Set up a SOC home lab using Wazuh (Docker or VM)

Collect logs from Windows and Linux machines

Detect brute-force attempts and suspicious activity

Learn the basics of SIEM dashboards and alerts

4. Tools & Environment

Wazuh: Open-source SIEM (Docker version)

Windows 10/11: Log source

Ubuntu Linux: Log source

Docker Desktop: For Wazuh deployment

PC: Single machine or VM

Resources:

Wazuh Docker: https://github.com/wazuh/wazuh-docker

Wazuh Documentation: https://documentation.wazuh.com/current/

5. Methodology

Install Docker Desktop on your Windows laptop.

Pull Wazuh Docker repository:

git clone https://github.com/wazuh/wazuh-docker.git


Launch the Wazuh stack using Docker Compose:

cd wazuh-docker
docker-compose up -d


Add Windows and Linux machines as agents (optional, for beginners you can skip or simulate logs).

Review Wazuh dashboard for alerts.

Simulate brute-force or failed login attempts to generate events.

Document findings in a summary.

6. Key Tasks Performed

Deployed Wazuh via Docker

Explored the Wazuh web dashboard

Monitored system logs from Windows/Linux

Detected simulated brute-force login attempts

Practiced creating simple alert rules

7. Results & Observations

Wazuh successfully collected logs and displayed them in the dashboard

Failed login attempts were detected and alerted

Simple correlation rules helped identify potential threats

Learned how a SOC monitors systems in real time

8. Skills Learned

SIEM deployment basics (Wazuh Docker)

Log collection from multiple OS

Event monitoring and alert review

Understanding SOC workflows

9. Conclusion

This project provides hands-on experience in SOC operations, log monitoring, and alert management using Wazuh. Even as a beginner, it demonstrates how to detect and respond to basic threats in a controlled lab environment.

10. References

Wazuh Official Documentation: https://documentation.wazuh.com/current/

Wazuh Docker GitHub: https://github.com/wazuh/wazuh-docker

Intro to SOC: https://www.sans.org/white-papers/34685/
