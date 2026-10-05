Wireshark Network Analysis Project

A cybersecurity project demonstrating network packet capture and traffic analysis using Wireshark, covering protocol analysis, display filtering, network troubleshooting, and basic security observations.

Introduction

Wireshark is a widely used network protocol analyzer that enables detailed inspection of network traffic. It supports both live packet capture and offline packet analysis, helping security professionals and network administrators understand network communications, troubleshoot connectivity issues, and investigate suspicious activity.

Problem Statement

Organizations often face challenges such as:

Difficulty identifying abnormal or potentially malicious network activity
Limited visibility into internal network traffic
Difficulty diagnosing connectivity problems and packet loss
Lack of detailed information during security incidents
Objectives
Understand network packet capture
Analyze network traffic using Wireshark
Identify source and destination IP addresses
Analyze TCP, UDP, DNS, HTTP, ARP, and ICMP traffic
Use Wireshark display filters
Identify unusual or suspicious traffic patterns
Understand how Wireshark supports network troubleshooting and security monitoring
Tools Used
Wireshark
Windows / Ubuntu / Kali Linux
Active network connection
Computer/laptop with a network adapter
Wireshark Filters Used
ip      # IPv4 traffic
tcp     # TCP packets
udp     # UDP packets
dns     # DNS queries/responses
http    # HTTP packets
icmp    # ICMP (ping) packets
arp     # ARP requests/replies
Project Implementation
1. Install Wireshark

Downloaded and installed Wireshark from the official website.

2. Identify the Network Interface

Selected the active Wi-Fi or Ethernet interface.

3. Start Packet Capture

Started live packet capture on the selected network interface.

4. Generate Network Traffic

Generated normal network traffic by browsing websites, performing searches, and running commands such as:

ping google.com
5. Stop Packet Capture

Stopped the capture after collecting sufficient network packets.

6. Apply Display Filters

Applied protocol-specific filters to isolate:

IP
TCP
UDP
DNS
HTTP
ICMP
ARP
7. Analyze Packets

Examined:

Source and destination IP addresses
Source and destination ports
TCP flags
Packet details
Sequence numbers
DNS queries and responses
ICMP requests and replies
8. Save the Capture

Saved packet captures in .pcapng format for analysis and documentation.

Security Analysis

The captured traffic was examined for security-relevant observations, including:

Unexpected protocols or connections
Repeated connection attempts
Plaintext or insecure communication
Unusual communication patterns
Potential indicators requiring further investigation

A suspicious traffic pattern is treated as an observation that requires additional investigation and is not automatically considered proof of an attack.

Network Troubleshooting

Wireshark was also used to understand common network troubleshooting scenarios, including:

Packet loss
Connection failures
TCP retransmissions
DNS-related issues
Network communication problems
Simulated DHCP misconfiguration scenarios
Screenshots
Figure	Description
1	Wireshark download page
2	Wireshark launched showing available interfaces
3	Selecting the active network interface
4	Live packet capture in progress
5	Stopping the packet capture
6	IP filter applied
7	TCP filter applied
8	UDP filter applied
9	DNS filter applied
10	HTTP filter applied
11	ICMP filter applied
12	ARP filter applied
13	Examining source and destination IP addresses
14	TCP packet analysis
15	UDP packet analysis
16	DNS traffic analysis
17	ICMP / ping analysis — capture 1
18	ICMP / ping analysis — capture 2
Project Screenshots

Figure 1
Figure 2
Figure 3
Figure 4
Figure 5
Figure 6
Figure 7
Figure 8
Figure 9
Figure 10
Figure 11
Figure 12
Figure 13
Figure 14
Figure 15
Figure 16
Figure 17
Figure 18

Project Outcomes
Developed a better understanding of network traffic
Learned how to capture and inspect network packets
Gained practical experience with Wireshark display filters
Analyzed common network protocols
Improved network troubleshooting skills
Developed basic security monitoring and traffic-analysis skills
Advantages
Free and open-source
Powerful real-time packet capture and inspection
Supports a wide range of network protocols
Useful for troubleshooting and security analysis
Helpful for cybersecurity and networking education
Limitations
Large packet captures can contain a very high volume of data
Packet-level information can be difficult for beginners to interpret
Encryption can limit visibility into application-level content
Packet analysis requires understanding of networking protocols
Applications / Use Cases

Network Troubleshooting · Intrusion Detection · Threat Hunting · Incident Response · Network Monitoring · Cybersecurity Training · Protocol Analysis · Digital Forensics

Skills Demonstrated
Wireshark
Network Traffic Analysis
Packet Analysis
TCP/IP
DNS
HTTP
ARP
ICMP
Network Troubleshooting
Basic Network Security
Cybersecurity Monitoring
Conclusion

This project demonstrated the process of capturing network traffic, applying protocol-specific filters, analyzing TCP, UDP, DNS, HTTP, ARP, and ICMP traffic, and examining network communications from a security perspective.

Wireshark provides valuable network visibility for troubleshooting, security monitoring, protocol analysis, and incident investigation.

⚠️ Disclaimer

Only capture and analyze network traffic on systems and networks that you own or have explicit permission to monitor. Unauthorized packet capture or network monitoring may violate laws and organizational policies.

Author

Sushmitha

GitHub: Sushmitha2504
