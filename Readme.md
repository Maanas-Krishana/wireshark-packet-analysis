# Dissecting Packets: From HTTP to TLS

A hands-on cybersecurity project focused on real-world packet analysis using Wireshark. This project explores how network communication works by capturing and analyzing HTTP traffic, DNS resolution, and TLS handshake packets.

## Project Overview

This project demonstrates practical packet inspection across multiple layers of the network stack. By analyzing live traffic, the project provides insight into:

- Application layer communication
- Domain name resolution
- Secure encrypted sessions
- Protocol behavior and packet structure

## Objectives

- Capture live network traffic
- Analyze HTTP request-response communication
- Inspect DNS query and response packets
- Observe TLS 1.3 handshake process
- Understand protocol fields across network layers

## Tools Used

- :contentReference[oaicite:0]{index=0}
- Web Browser
- System DNS Resolver

## Protocols Analyzed

### HTTP (Port 80)

Observed:

- `GET / HTTP/1.1`
- `200 OK`
- Request headers
- Host information
- Browser User-Agent

Key Learning:

HTTP transmits data in plaintext and can be inspected directly.

---

### DNS (Port 53)

Observed:

- A Records
- AAAA Records
- CNAME Records
- DNS query-response workflow

Example:

```dns
chatgpt.com → 172.64.155.209
chatgpt.com → 104.18.32.47
```

Key Learning:

DNS translates domain names into routable IP addresses.

---

### TLS 1.3 (Port 443)

Observed:

- Client Hello
- Server Hello
- Cipher negotiation
- SNI (Server Name Indication)

Example:

```tls
Client Hello (SNI=example.com)
Server Hello
```

Key Learning:

TLS enables encrypted and secure communication over HTTPS.

---

## Project Structure

```bash
wireshark-packet-analysis/
│
├── README.md
├── WiresharkProjectMaanas.pdf
│
├── captures/
│   ├── http_get.pcapng
│   ├── dns_analysis.pcapng
│   └── tls_packets.pcapng
│
└── screenshots/
    ├── http.png
    ├── dns.png
    └── tls.png
```

## Key Findings

| Protocol | Port | Purpose | Security |
|----------|------|---------|----------|
| HTTP | 80 | Web Communication | Not Encrypted |
| DNS | 53 | Domain Resolution | Not Encrypted |
| TLS | 443 | Secure Communication | Encrypted |

## Skills Demonstrated

- Network Packet Analysis
- Protocol Inspection
- Cybersecurity Fundamentals
- Traffic Analysis
- Security Monitoring
- Wireshark Filtering

## Learning Outcomes

This project improved practical understanding of:

- Packet structure and headers
- Client-server communication
- DNS resolution mechanisms
- TLS encryption negotiation
- Network troubleshooting and monitoring

## Author

**Maanas**  
Cybersecurity | Networking | Systems | AI