# Network Protocols Observed – Wireshark Analysis



## 1. DNS (Domain Name System)

Used to resolve domain names like `httpforever.com` and `google.com`. Both _**A (IPv4)**_ and _**AAAA (IPv6)**_ records were observed. DNS queries and responses were exchanged between local IP `192.168.128.142` and public DNS servers.
![](https://github.com/krupal-3009/wireshark-traffic-analysis/blob/f467ce5448a158ed0a2208a3d897b718258f4aad/dns.png)

## 2. TCP (Transmission Control Protocol)

TCP segments were exchanged with proper _**SYN**_ , _**ACK**_, and data transmissions. This included:
- Handshake initiation (`SYN`, `SYN-ACK`, `ACK`)
- Reassembled TCP segments forming HTTP payloads
- Connection termination (`FIN`, `ACK`)
![](https://github.com/krupal-3009/wireshark-traffic-analysis/blob/f467ce5448a158ed0a2208a3d897b718258f4aad/tcp.png)

## 3. HTTP (Hypertext Transfer Protocol)

HTTP `GET` requests and corresponding `200 OK` responses were observed.
- Content-type was `text/html`, and some parts of the webpage were captured (e.g., WiFi captive portal HTML).

![](https://github.com/krupal-3009/wireshark-traffic-analysis/blob/f467ce5448a158ed0a2208a3d897b718258f4aad/http.png)

## 4. ICMP (Internet Control Message Protocol)

A series of _**ICMP Echo (ping)**_ requests and replies between the local host and `142.250.206.78` (Google server). This validates basic reachability tests.
![](https://github.com/krupal-3009/wireshark-traffic-analysis/blob/f467ce5448a158ed0a2208a3d897b718258f4aad/icmp.png)

## 5. Specific IP address
![](https://github.com/krupal-3009/wireshark-traffic-analysis/blob/f467ce5448a158ed0a2208a3d897b718258f4aad/ip.png)

---

### 🧩 Capture Info

- Interface: `eth0`
- PCAP Export: [`network_traffic.pcap`](./network_traffic.pcap)
- Packet Count: Multiple packets across all 4 protocols
- Filtering used: `http`, `dns`, `tcp`, `icmp`, `ip.addr == 192.168.128.142`

---
