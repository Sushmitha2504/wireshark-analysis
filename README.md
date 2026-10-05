# Wireshark Network Analysis

A cybersecurity project demonstrating **live packet capture, network traffic analysis, protocol inspection, security monitoring, and basic network troubleshooting using Wireshark** in a controlled environment.

## 📌 Project Overview

Wireshark is a widely used open-source network protocol analyzer that allows security professionals and network administrators to capture and inspect network traffic.

This project demonstrates practical packet analysis techniques using Wireshark to understand network communication, identify protocols, analyze packets, investigate suspicious traffic patterns, and troubleshoot network issues.

## 🎯 Problem Statement

Network traffic can contain valuable information about system communication, network performance, and potential security issues.

Security professionals need the ability to:

* Capture network packets
* Identify communicating systems
* Analyze network protocols
* Understand TCP/IP communication
* Investigate unusual traffic
* Detect suspicious communication patterns
* Troubleshoot connectivity problems
* Support security monitoring and incident investigation

Wireshark provides visibility into network traffic at the packet level.

## 🎯 Objectives

The main objectives of this project are:

* Capture live network traffic using Wireshark
* Analyze captured packets
* Identify source and destination IP addresses
* Understand TCP and UDP communication
* Analyze DNS, HTTP, ARP, and ICMP traffic
* Use Wireshark display filters
* Inspect TCP flags and packet information
* Identify unusual or unexpected traffic patterns
* Troubleshoot network communication issues
* Save packet captures for further analysis

## 🛠️ Tools and Technologies

| Category          | Technology                     |
| ----------------- | ------------------------------ |
| Packet Analyzer   | Wireshark                      |
| Operating System  | Windows / Ubuntu / Kali Linux  |
| Network Protocols | TCP, UDP, DNS, HTTP, ARP, ICMP |
| Capture Format    | `.pcapng`                      |
| Command Line      | Linux Terminal                 |
| Network Tool      | Ping                           |

## 🧪 Environment

The project was performed in a controlled environment using:

* A computer/laptop
* Active network connection
* Wireshark
* Network adapter
* Optional Linux/Kali environment for additional testing

All traffic analysis should be performed only on networks and systems that are owned by you or where you have explicit authorization.

---

## 🔍 Project Methodology

The project followed these steps:

1. Install and configure Wireshark
2. Identify the active network interface
3. Start packet capture
4. Generate normal network traffic
5. Capture packets
6. Stop the capture
7. Apply Wireshark display filters
8. Analyze source and destination addresses
9. Analyze protocols and ports
10. Inspect TCP communication
11. Analyze DNS, ARP, ICMP, and HTTP traffic
12. Investigate unusual traffic patterns
13. Save the packet capture as a `.pcapng` file
14. Document observations and results

---

# 💻 Wireshark Commands & Related Commands

Wireshark is primarily a graphical packet analyzer, but several command-line utilities can be used with it.

## 1. Check Wireshark Version

```bash
wireshark --version
```

## 2. Start Wireshark

```bash
wireshark
```

## 3. List Available Capture Interfaces

Using TShark:

```bash
tshark -D
```

## 4. Capture Packets Using TShark

```bash
tshark -i <interface>
```

Example:

```bash
tshark -i eth0
```

## 5. Capture a Specific Number of Packets

```bash
tshark -i <interface> -c 50
```

## 6. Capture Traffic and Save to a File

```bash
tshark -i <interface> -w capture.pcapng
```

## 7. Read a Capture File

```bash
tshark -r capture.pcapng
```

## 8. Display Only IP Traffic

```bash
tshark -r capture.pcapng -Y "ip"
```

## 9. Display TCP Traffic

```bash
tshark -r capture.pcapng -Y "tcp"
```

## 10. Display DNS Traffic

```bash
tshark -r capture.pcapng -Y "dns"
```

## 11. Display ICMP Traffic

```bash
tshark -r capture.pcapng -Y "icmp"
```

> Replace `<interface>` with an interface available on your authorized system, such as `eth0`, `wlan0`, or the appropriate Windows capture interface.

---

# 🔎 Wireshark Display Filters

The following filters were used to analyze different types of network traffic.

### IP Traffic

```text
ip
```

### TCP Traffic

```text
tcp
```

### UDP Traffic

```text
udp
```

### DNS Traffic

```text
dns
```

### HTTP Traffic

```text
http
```

### ICMP Traffic

```text
icmp
```

### ARP Traffic

```text
arp
```

### Traffic from a Specific IP

```text
ip.addr == <IP_ADDRESS>
```

### Traffic to a Specific IP

```text
ip.dst == <IP_ADDRESS>
```

### Traffic from a Specific Source

```text
ip.src == <IP_ADDRESS>
```

### Specific TCP Port

```text
tcp.port == 80
```

### Specific UDP Port

```text
udp.port == 53
```

### TCP SYN Packets

```text
tcp.flags.syn == 1
```

### TCP SYN + ACK

```text
tcp.flags.syn == 1 && tcp.flags.ack == 1
```

---

# 📊 Packet Analysis

The captured packets were analyzed to understand:

### Source and Destination

* Source IP address
* Destination IP address
* Source port
* Destination port

### Protocol Analysis

The following protocols were examined:

* TCP
* UDP
* DNS
* HTTP
* ARP
* ICMP

### TCP Analysis

TCP packets were inspected for:

* SYN
* SYN-ACK
* ACK
* FIN
* RST
* Sequence numbers
* Acknowledgment numbers
* Retransmissions

### DNS Analysis

DNS traffic was examined to understand:

* DNS queries
* DNS responses
* Requested domain information
* DNS communication patterns

### ICMP Analysis

ICMP traffic was generated and analyzed using tools such as:

```bash
ping <target-ip>
```

This helped demonstrate request and response traffic.

---

# 🔐 Security Analysis

Wireshark can provide useful visibility during security investigations.

The captured traffic was analyzed for:

* Unexpected network connections
* Unusual protocols
* Repeated connection attempts
* Unexpected source or destination addresses
* Plaintext or insecure communication
* Abnormal packet patterns
* TCP retransmissions
* DNS communication patterns

> **Important:** An unusual packet or traffic pattern does not automatically mean that an attack has occurred. Findings should be investigated and correlated with additional evidence.

---

# 🛠️ Network Troubleshooting

Wireshark can also be used to troubleshoot network problems.

The project examined examples such as:

* Packet loss
* TCP retransmissions
* Connection failures
* DNS resolution problems
* Unexpected network behavior
* Communication delays

For example, repeated TCP retransmissions can indicate possible connectivity or network-quality problems.

---

# 🖼️ Project Preview

Add your main project images inside the `screenshots/` directory.

### Wireshark Packet Capture

![Wireshark Packet Capture](screenshots/wireshark-packet-capture.png)

### Network Traffic Analysis

![Wireshark Network Traffic Analysis](screenshots/wireshark-network-analysis.png)

### Protocol Analysis

![Wireshark Protocol Analysis](screenshots/wireshark-protocol-analysis.png)

> These images demonstrate packet capture, protocol inspection, and network traffic analysis performed during the project.

---

# 📸 Project Screenshots

The project contains screenshots documenting the practical implementation.

| Figure | Description                     |
| ------ | ------------------------------- |
| 1      | Wireshark interface             |
| 2      | Network interface selection     |
| 3      | Starting packet capture         |
| 4      | Captured network packets        |
| 5      | IP traffic analysis             |
| 6      | TCP packet analysis             |
| 7      | UDP traffic analysis            |
| 8      | DNS traffic analysis            |
| 9      | HTTP traffic analysis           |
| 10     | ICMP traffic analysis           |
| 11     | ARP traffic analysis            |
| 12     | TCP flags analysis              |
| 13     | Source and destination analysis |
| 14     | Packet filtering                |
| 15     | Network troubleshooting         |
| 16     | Suspicious traffic analysis     |
| 17     | Saved packet capture            |
| 18     | Final analysis                  |

Place the corresponding screenshots in the `screenshots/` directory.

Example:

```text
screenshots/
├── figure_01.png
├── figure_02.png
├── figure_03.png
├── figure_04.png
├── figure_05.png
├── figure_06.png
├── figure_07.png
├── figure_08.png
├── figure_09.png
├── figure_10.png
├── figure_11.png
├── figure_12.png
├── figure_13.png
├── figure_14.png
├── figure_15.png
├── figure_16.png
├── figure_17.png
└── figure_18.png
```

---

# 💾 Packet Capture File

The packet capture generated during the project can be stored as:

```text
capture.pcapng
```

The capture file can be opened using Wireshark for further analysis.

Avoid uploading captures containing sensitive or private network information.

---

# 📈 Project Outcomes

Through this project, the following outcomes were achieved:

* Successfully captured live network traffic
* Identified network protocols
* Analyzed TCP and UDP communication
* Investigated DNS queries and responses
* Analyzed ARP and ICMP packets
* Used Wireshark display filters
* Inspected TCP flags and packet details
* Identified network communication patterns
* Practiced basic security monitoring
* Used packet analysis for troubleshooting

---

# 🎓 Skills Demonstrated

* Wireshark
* Network Traffic Analysis
* Packet Capture
* Network Protocol Analysis
* TCP/IP
* TCP and UDP
* DNS Analysis
* HTTP Analysis
* ARP Analysis
* ICMP Analysis
* Network Troubleshooting
* Security Monitoring
* Basic Incident Analysis
* Linux Command Line
* TShark
* Cybersecurity Fundamentals
* Technical Documentation

---

# 📚 Learning Outcomes

This project helped develop practical understanding of:

* How network packets are transmitted
* How TCP/IP communication works
* How to capture network traffic
* How to analyze network protocols
* How to use Wireshark filters
* How to identify source and destination systems
* How to inspect TCP communication
* How to analyze DNS traffic
* How packet analysis can support security investigations
* How network analysis can assist troubleshooting

---

# 🌐 Applications / Use Cases

Wireshark can be used for:

* Network Security Monitoring
* Network Troubleshooting
* Incident Response
* Packet Analysis
* Protocol Analysis
* Network Performance Analysis
* Security Investigations
* Digital Forensics
* Cybersecurity Training
* Network Administration

---

# 🚀 Future Improvements

Possible future improvements include:

* Automated packet analysis using Python
* Build a network traffic dashboard
* Detect suspicious traffic automatically
* Integrate threat-intelligence feeds
* Add protocol-based traffic classification
* Create automated packet-analysis reports
* Develop anomaly detection using machine learning
* Integrate Wireshark/TShark with security monitoring tools

---

# ✅ Conclusion

This project demonstrated practical **network packet capture and traffic analysis using Wireshark**.

The project covered packet capture, protocol analysis, TCP/UDP communication, DNS, HTTP, ARP, ICMP, filtering, security monitoring, and network troubleshooting.

It provides a practical foundation for understanding **network security monitoring, packet analysis, troubleshooting, and cybersecurity investigation techniques**.

---

# ⚠️ Disclaimer

This project is intended **only for authorized cybersecurity testing, network analysis, and educational purposes**.

Only capture or analyze network traffic that you own or have explicit permission to monitor. Unauthorized packet capture or network monitoring may violate laws, privacy requirements, and organizational policies.

---

# 👩‍💻 Author

**Sushmitha**

GitHub: [Sushmitha2504](https://github.com/Sushmitha2504)
