# Wireshark Network Traffic Capture and Analysis

This repository contains the results of  capturing and analyzing network traffic using **Wireshark**.


##  Protocols Observed

- **DNS (Domain Name System)**: Resolving hostnames like `httpforever.com`, `google.com`
- **TCP (Transmission Control Protocol)**: Used for HTTP connections and reliable transmission
- **HTTP (Hypertext Transfer Protocol)**: Viewing website contents, 200 OK responses observed
- **ICMP (Internet Control Message Protocol)**: Ping requests and replies captured

##  Report

Refer to the `report.md` file for a concise explanation of:
- What protocols were captured (DNS, HTTP, TCP, ICMP)
- How the analysis was done using filters and packet inspection
- Key observations based on captured traffic

##  Learning Outcome

- Understood live packet capture
- Applied filters for protocol isolation
- Identified protocol roles and traffic patterns
- Gained hands-on experience with `.pcap` exports and analysis

##  Notes

- Packet capture was done on interface `eth0`
- Traffic includes interactions with external servers and standard web requests

---
