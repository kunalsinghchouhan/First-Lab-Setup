# First-Lab-Setup
📌 Overview

This project showcases a hands-on cybersecurity home lab built to simulate real-world Security Operations Center (SOC) workflows.

The lab replicates an attacker–target environment to practice:

Reconnaissance detection
Network traffic analysis
Host-based log investigation
Event correlation across multiple data sources

The goal is to demonstrate the ability to analyze, detect, and investigate suspicious activity in a controlled environment—core responsibilities of a SOC Analyst.

🧪 Lab Architecture

Environment Setup:

Virtualization: VirtualBox
Attacker Machine: Kali Linux
Target Machine: Windows 10
Network Type: NAT

This architecture ensures:

Safe simulation of attack scenarios
Controlled communication between systems
No exposure to external networks

Network Design:

Dedicated virtual subnet for attacker–target interaction
Promiscuous mode enabled for packet visibility
No internet access to maintain isolation
🛠️ Tools & Their Purpose
Nmap – Reconnaissance and attack surface mapping
Wireshark – Deep packet inspection and protocol-level traffic analysis
Windows Event Viewer – Host-based log monitoring and security event investigation
🔍 Practical Security Activities
1. Reconnaissance & Attack Surface Analysis (Nmap)
Performed SYN and service version scans on the target system
Identified exposed ports and running services
Evaluated potential risks associated with open services

Example:

nmap -sV 10.0.2.15

Key Insight:
Discovered active services (e.g., SMB/HTTP) and assessed how they could be leveraged during an attack phase.

2. Network Traffic Analysis (Wireshark)
Captured live traffic between attacker and target systems
Applied protocol-based filters (HTTP, DNS, TCP)
Analyzed:
TCP handshake (SYN, SYN-ACK, ACK)
DNS query/response behavior
Request–response communication patterns

Key Insight:
Mapped how reconnaissance activity appears at the packet level, improving the ability to identify suspicious traffic patterns.

3. Host-Based Log Analysis (Windows Event Viewer)
Investigated Windows Security Logs for system activity
Monitored:
Failed and successful login attempts
System-generated security events
Correlated logs with network activity

Key Insight:
Linked network scanning activity with system-level logs to simulate basic intrusion detection and investigation workflows.

🔗 Simulated SOC Workflow (End-to-End Analysis)

This lab demonstrates a simplified SOC investigation process:

Attack Simulation
Initiated reconnaissance scan using Nmap
Network Monitoring
Captured and analyzed traffic in Wireshark
Observed scan signatures and abnormal packet behavior
Log Investigation
Reviewed Windows logs for related system events
Identified login attempts and system responses
Correlation & Analysis
Mapped attacker activity → network traffic → system logs
Built a basic understanding of detection opportunities

🎯 Key Skills Demonstrated
Network traffic analysis and protocol understanding
Reconnaissance detection techniques
Log analysis and event correlation
Understanding of SOC investigation workflows
Ability to interpret real-world security data

Tech I'm Learning

**Security Tools:** Kali Linux, Nmap, Wireshark, Windows Event Viewer, VirtualBox  
**Currently Exploring:** network protocols, log analysis

📷 Screenshots
1. Nmap Scan Output
<img width="500" height="300" alt="nmap_service_scan" src="https://github.com/user-attachments/assets/24f6b9c4-b6f6-4282-bdeb-60c28e8e70d5" />

Shows open ports, services, and versions detected on the target system
➡️ Demonstrates reconnaissance and attack surface identification

2. Wireshark Packet Capture
<img width="500" height="300" alt="wireshark_traffic_capture" src="https://github.com/user-attachments/assets/a9a1178c-224f-4de0-9679-ead289bced5c" />

Shows filtered traffic (HTTP, DNS, TCP)
➡️ Highlights packet-level analysis and communication patterns

3. VirtualBox Network Configuration
<img width="500" height="300" alt="network_config_kali" src="https://github.com/user-attachments/assets/2fab0303-638d-4b4d-b735-6057234339c2" />
<img width="500" height="300" alt="network_config_windows" src="https://github.com/user-attachments/assets/b6c6038c-9d15-4ffd-9c8e-985aada74039" />

Shows isolated network setup and configuration
➡️ Explains how controlled communication is achieved

4. Windows Event Viewer Logs
<img width="500" height="300" alt="event_details_analysis" src="https://github.com/user-attachments/assets/2631d14d-c9c2-4d49-bb8f-0b09fbf9708e" />

Shows login attempts and system security events
➡️ Demonstrates host-based monitoring and investigation

🚀 Future Enhancements

1.Integrate SIEM solutions (Splunk / ELK Stack) for centralized logging

2.Simulate advanced attack scenarios:

3.Brute-force attacks

4.Lateral movement

5.Develop detection rules and alerts

6.Automate log analysis using Python

7.Expand lab to include:

8.Active Directory environment

9.Multiple endpoints and services


