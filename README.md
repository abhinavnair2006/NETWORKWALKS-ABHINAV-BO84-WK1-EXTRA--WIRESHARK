# 🦈 Wireshark Network Security Lab

<p align="center">
  <img src="https://img.shields.io/badge/Domain-Cybersecurity-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Tool-Wireshark-1679A7?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Platform-Kali%20Linux-black?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Overall%20Score-100%25-brightgreen?style=for-the-badge" />
</p>

## 📌 About This Project

This repository contains my hands-on practical exercises on **network traffic analysis and cybersecurity using Wireshark**.

Wireshark is an open-source network protocol analyser used to capture, inspect and analyse network packets. Through these exercises, I explored different network protocols, identified suspicious activities, reconstructed TCP conversations and understood common network security vulnerabilities.

## 🛠️ Tools & Technologies

| Tool / Technology | Purpose |
|---|---|
| Wireshark | Network packet capture and analysis |
| Kali Linux | Cybersecurity testing environment |
| VirtualBox | Virtual machine environment |
| TCP/IP | Network communication analysis |
| HTTP / FTP | Application protocol investigation |
| SIP / RTP | VoIP traffic analysis |

## 🎯 Objectives

- Understand packet capturing and network traffic analysis.
- Identify source and destination IP addresses.
- Analyse TCP flags and connection behaviour.
- Reconstruct TCP conversations using Follow TCP Stream.
- Identify security risks in unencrypted HTTP traffic.
- Detect suspicious FTP authentication attempts.
- Analyse SIP signalling and RTP media communication.
- Understand network security vulnerabilities and defensive techniques.

## 🔍 Wireshark Display Filters

Some useful display filters used during the practical exercises:

| Investigation | Wireshark Filter |
|---|---|
| TCP SYN packets | `tcp.flags.syn == 1 && tcp.flags.ack == 0` |
| Specific IP address | `ip.addr == 192.168.10.66` |
| HTTP requests | `http.request` |
| FTP traffic | `ftp` |
| SIP signalling | `sip` |
| RTP media | `rtp` |

## 🧪 Practical Exercises

### Lab 03 — Identify the Attacker's IP

<kbd>Score: 100%</kbd>

**Objective:** Identify the suspected attacker IP address by analysing TCP SYN packets and recognising port scanning behaviour.

**Analysis:**
- Analysed a 309-packet capture.
- Identified 73 packets matching the SYN-focused filter.
- Suspected source IP: `192.168.10.66`.
- Target IP: `192.168.10.20`.
- Identified 40 probed ports.
- Open ports: 22, 80 and 443.

**Learning Outcome:** Recognised TCP SYN scanning behaviour by analysing IP addresses, destination ports and TCP flags.

**📸 Screenshot — Lab 03**

<!-- Add your Lab 03 screenshot below -->
<p align="center">
  <img src="screenshots/lab03.png" width="85%" alt="Lab 03 - Identify the Attacker's IP" />
</p>

---

### Lab 04 — Follow TCP Stream

<kbd>Score: 100%</kbd>

**Objective:** Reconstruct and analyse application-level communication using Wireshark's Follow TCP Stream feature.

**Analysis:**
- Analysed a 246-packet capture.
- Investigated TCP port 5000.
- Identified TCP stream 5.
- Examined a 413-byte conversation between the endpoints.
- Understood how TCP communication can be reconstructed.

**Learning Outcome:** Learned to reconstruct TCP conversations and understand the confidentiality risks of unencrypted communication.

**📸 Screenshot — Lab 04**

<!-- Add your Lab 04 screenshot below -->
<p align="center">
  <img src="screenshots/lab04.png" width="85%" alt="Lab 04 - Follow TCP Stream" />
</p>

---

### Lab 05 — Follow TCP Stream, Part 2

<kbd>Score: 100%</kbd>

**Objective:** Inspect HTTP responses and identify information exposed through client-side web content.

**Analysis:**
- Investigated the `/staff.html` request.
- Identified TCP stream 7.
- Observed an HTTP 200 response.
- Examined HTML content and comments.
- Understood why sensitive information should not be stored in client-side source code.

**Learning Outcome:** Learned to inspect HTTP responses and identify information exposed through web pages.

**📸 Screenshot — Lab 05**

<!-- Add your Lab 05 screenshot below -->
<p align="center">
  <img src="screenshots/lab05.png" width="85%" alt="Lab 05 - HTTP Stream Analysis" />
</p>

---

### Lab 06 — HTTP Plain-Text Credentials

<kbd>Score: 100%</kbd>

**Objective:** Identify HTTP login submissions and understand the security risks of transmitting credentials without encryption.

**Analysis:**
- Analysed a 255-packet capture.
- Identified an HTTP POST request.
- Investigated the `/login` endpoint.
- Observed two login attempts.
- Understood how plaintext HTTP traffic can expose sensitive information.

**Learning Outcome:** Identified the risks of transmitting authentication information over unencrypted HTTP and understood the importance of HTTPS.

**📸 Screenshot — Lab 06**

<!-- Add your Lab 06 screenshot below -->
<p align="center">
  <img src="screenshots/lab06.png" width="85%" alt="Lab 06 - HTTP Plain-Text Credentials" />
</p>

---

### Lab 07 — FTP Brute-Force Detection

<kbd>Score: 100%</kbd>

**Objective:** Detect suspicious FTP authentication attempts by analysing repeated login failures and successful responses.

**Analysis:**
- Analysed a 369-packet capture.
- Identified 24 FTP authentication failure responses (530).
- Observed a subsequent successful response (230).
- Investigated FTP control-channel communication.
- Understood how repeated login failures can indicate brute-force activity.

**Learning Outcome:** Learned to identify suspicious FTP authentication patterns using response codes and packet analysis.

**📸 Screenshot — Lab 07**

<!-- Add your Lab 07 screenshot below -->
<p align="center">
  <img src="screenshots/lab07.png" width="85%" alt="Lab 07 - FTP Brute-Force Detection" />
</p>

---

### Lab 08 — VoIP Call Analysis

<kbd>Score: 100%</kbd>

**Objective:** Analyse VoIP communication by identifying SIP signalling and RTP media traffic.

**Analysis:**
- Analysed a 1,051-packet capture.
- Identified SIP signalling packets.
- Examined RTP media traffic.
- Identified the PCMU audio codec.
- Understood the difference between call signalling and media transmission.

**Learning Outcome:** Learned how SIP establishes and manages communication sessions while RTP carries real-time audio and video data.

**📸 Screenshot — Lab 08**

<!-- Add your Lab 08 screenshot below -->
<p align="center">
  <img src="screenshots/lab08.png" width="85%" alt="Lab 08 - VoIP Call Analysis" />
</p>

---

## 📊 Results Summary

| Lab | Practical Exercise | Score |
|:---:|---|:---:|
| 03 | Identify the Attacker's IP | 100% |
| 04 | Follow TCP Stream | 100% |
| 05 | Follow TCP Stream, Part 2 | 100% |
| 06 | HTTP Plain-Text Credentials | 100% |
| 07 | FTP Brute-Force Detection | 100% |
| 08 | VoIP Call Analysis | 100% |
| **Overall** | **6 Practical Exercises** | **100%** |

## 🏆 Key Learnings

- Network packet capture and inspection.
- TCP flags and port scanning detection.
- TCP stream reconstruction.
- HTTP request and response analysis.
- Plaintext credential exposure.
- FTP brute-force detection.
- SIP and RTP protocol analysis.
- Network security investigation techniques.

## 📝 Conclusion

These Wireshark practical exercises provided hands-on experience in network traffic analysis and cybersecurity investigation. By analysing different protocols such as TCP, HTTP, FTP, SIP and RTP, I developed practical skills in packet inspection, identifying suspicious activities and understanding network security vulnerabilities.

The exercises strengthened my knowledge of network protocols and the importance of securing communication through encryption and proper security practices.

---

<p align="center">
  <b>🦈 Wireshark Network Security Lab</b><br/>
  <i>Hands-on Learning | Network Analysis | Cybersecurity</i><br/><br/>
  <img src="https://img.shields.io/badge/Completed-6%20Labs-success?style=flat-square" />
  <img src="https://img.shields.io/badge/Achievement-100%25-brightgreen?style=flat-square" />
</p>
