Wireshark Traffic Analysis Project Report
1. Project Title

Wireshark Traffic Analysis for Network Security

2. Introduction

Wireshark is a powerful network protocol analyzer used to capture and inspect network traffic. It helps cybersecurity professionals understand how data moves across networks and detect suspicious activities, such as unauthorized access attempts or scanning attacks.

This project demonstrates basic network traffic analysis using publicly available PCAP files.

3. Objectives

Capture network traffic from sample PCAP files

Apply filters to isolate key protocols (ARP, DNS, TCP, HTTP/HTTPS)

Identify network scanning attempts and abnormal traffic

Analyze and interpret results for cybersecurity awareness

4. Tools & Environment

Wireshark: Version 4.0+

Operating System: Windows 11

PCAP Files Sources:

https://wiki.wireshark.org/SampleCaptures

https://www.malware-traffic-analysis.net

5. Methodology

Downloaded sample PCAP files from online sources.

Opened the PCAPs in Wireshark.

Applied filters to analyze specific traffic:

arp for ARP requests

dns for DNS queries

tcp.port == 80 for HTTP traffic

Examined packet details to identify anomalies or suspicious behavior.

Recorded key findings in a summary report with screenshots.

6. Packet Analysis
6.1 ARP Analysis

Observed ARP request and reply packets.

Detected MAC-to-IP mapping across devices.

Checked for unusual ARP requests that may indicate ARP spoofing.

6.2 DNS Analysis

Captured DNS queries and responses.

Identified domain names requested and resolved IPs.

Noted any suspicious or unusual DNS traffic.

6.3 TCP Analysis

Inspected TCP three-way handshake (SYN, SYN-ACK, ACK).

Checked sequence numbers and port numbers.

Observed any abnormal retransmissions or connection resets.

6.4 HTTP / HTTPS Analysis

Monitored HTTP GET/POST requests.

Inspected response codes and headers.

For HTTPS, verified TLS handshake processes.

6.5 Suspicious Activity Observed

Found multiple SYN scans from a single IP address (potential reconnaissance).

Detected unusual HTTP requests to unknown domains.

Noted DNS queries for rare or suspicious domains.

7. Filters & Commands Used

arp → Analyze ARP traffic

dns → Inspect DNS queries and responses

tcp → View TCP handshake and connection patterns

http → Monitor web traffic

ip.addr == <your IP> → Filter packets related to your device

8. Results & Interpretation

Sample PCAPs show scanning attempts and normal web traffic.

TCP/HTTP analysis highlights the importance of monitoring for reconnaissance.

DNS analysis demonstrates how attackers may try to reach malicious domains.

Understanding network traffic helps detect attacks before they compromise systems.

9. Conclusion

This project enhanced my practical understanding of network traffic and packet analysis. Using Wireshark, I learned how to detect scanning, analyze protocols, and interpret network anomalies. These skills are essential for network security monitoring and cybersecurity operations.

10. References

Wireshark Sample Captures: https://wiki.wireshark.org/SampleCaptures

Malware Traffic Analysis: https://www.malware-traffic-analysis.net

Wireshark Official Documentation: https://www.wireshark.org/docs/
