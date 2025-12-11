Python Log Parser Project Report
1. Project Title

Automated Log Parsing for Suspicious IP Detection

2. Introduction

Logs from systems and applications are a crucial source of security information. Automating log analysis helps detect suspicious activity efficiently. This project demonstrates a beginner-friendly Python script that parses log files, identifies failed login attempts, and extracts suspicious IP addresses.

3. Objectives

Automate log analysis using Python

Detect repeated failed login attempts

Extract suspicious IP addresses from logs

Generate a summary report

4. Tools & Environment

Python 3 (https://www.python.org/
)

Linux auth logs (/var/log/auth.log) or Windows event logs exported to text

Text editor (VS Code, Notepad++, or GitHub Web Editor)

5. Methodology

Open a system log file in Python

Search for failed login attempts using simple pattern matching

Extract IP addresses from those entries

Count occurrences per IP to identify suspicious activity

Generate a simple report

6. Python Script

Create a file called log_parser.py inside the folder log-parser-python/:

import re

# Path to the log file
log_file = "auth.log"

# Dictionary to count failed attempts per IP
ip_count = {}

# Open and read the log file
with open(log_file, "r") as file:
    for line in file:
        if "Failed password" in line:
            # Extract IP address using regex
            ip = re.findall(r'[0-9]+(?:\.[0-9]+){3}', line)
            if ip:
                ip_address = ip[0]
                ip_count[ip_address] = ip_count.get(ip_address, 0) + 1

# Print summary report
print("Suspicious IPs and failed login attempts:")
for ip, count in ip_count.items():
    print(f"{ip}: {count} failed attempts")

7. Key Tasks Performed

Opened and parsed system logs

Extracted suspicious IP addresses

Counted failed login attempts per IP

Generated a simple summary report

8. Results & Observations

Identified IPs with repeated failed login attempts

Created a readable summary for security analysis

Demonstrated how automation reduces manual effort in log review

9. Skills Learned

Python scripting for security

Log parsing and pattern matching

Identifying suspicious activity from logs

Automating simple security tasks

10. Conclusion

This project shows how Python can be used to automate log analysis and detect suspicious activity efficiently. Even with basic scripts, security analysts can save time and respond faster to potential threats.

11. References

Python Official: https://www.python.org/

Regular Expressions: https://docs.python.org/3/library/re.html

Linux Auth Logs: https://linux.die.net/man/5/syslog
