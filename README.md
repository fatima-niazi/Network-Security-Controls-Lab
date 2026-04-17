# 🔐 Network Security Controls Lab — Module 3

## 📌 Overview
This project is part of the **Certified Network Defender (CND)** course and focuses on implementing **real-world network security controls** in a virtual lab environment.

It builds on Module 2 and introduces advanced security mechanisms including:
- Network segmentation
- Protocol hardening
- TLS security
- VPN deployment
- Intrusion Detection System (IDS)
- Centralized management
- Attack simulation & validation

---

## 👩‍💻 Author
**Bint e Fatima Niazi**  
🔗 LinkedIn: https://www.linkedin.com/in/bint-e-fatima-niazi/  
💻 GitHub: https://github.com/fatima-niazi  
📧 Email: fatimabinte4@gmail.com  

---

## 🧠 Lab Objectives
- Implement enterprise-level security controls
- Secure Active Directory environment
- Detect and prevent common cyber attacks
- Gain hands-on experience with defensive security tools

---

## 🖥️ Lab Environment

| Machine   | IP Address       | OS                  | Role |
|----------|----------------|---------------------|------|
| DC01     | 192.168.64.10  | Windows Server 2019 | Domain Controller |
| ADMIN01  | 192.168.64.20  | Windows 10 Pro      | Admin Workstation |
| CL01     | 192.168.64.30  | Windows 10 Pro      | Client Machine |
| VPN01    | 192.168.64.50  | Windows Server 2019 | VPN Server |
| IDS01    | 192.168.64.6   | Kali Linux          | IDS (Suricata) |
| ATTACK01 | 192.168.64.4   | Kali Linux          | Attack Machine |

---

## ⚙️ Implemented Security Controls

### 🔹 Network Segmentation
- Configured Windows Firewall rules on DC01
- Blocked:
  - ICMP from CL01
  - RDP access from CL01
- Allowed essential AD services only

---

### 🔹 Protocol Hardening
Disabled insecure protocols:
- SMBv1 ❌
- LLMNR ❌
- NetBIOS ❌
- mDNS ❌

---

### 🔹 TLS Hardening
- Disabled: TLS 1.0 & TLS 1.1
- Enabled: TLS 1.2 only ✅
- Disabled weak cipher: RC4

---

### 🔹 Public Key Infrastructure (PKI)
- Deployed Enterprise Root Certificate Authority
- Configured:
  - Auto-enrollment via GPO
  - Certificate lifecycle management

---

### 🔹 VPN Deployment (SoftEther)
- Configured L2TP/IPSec VPN server
- Implemented:
  - Secure authentication
  - Virtual Hub
  - SecureNAT (DHCP for VPN clients)

---

### 🔹 Intrusion Detection System (IDS)
- Installed **Suricata** on IDS01
- Configured:
  - Custom detection rules
  - Real-time alert monitoring
- Detected:
  - Port scans
  - Brute-force attempts
  - Ping sweeps

---

### 🔹 Sysmon Logging
- Installed Sysmon on:
  - DC01
  - ADMIN01
- Enabled detailed event logging for:
  - Process activity
  - Network connections
  - Threat detection

---

### 🔹 Windows Admin Center
- Installed on ADMIN01
- Enabled:
  - Remote server management
  - PowerShell execution
  - Firewall & service monitoring

---

## ⚔️ Attack Simulation & Validation

All security controls were tested using **ATTACK01 (Kali Linux)**:

### ✔️ Attacks Performed
- Network reconnaissance (Nmap)
- SMB vulnerability testing (EternalBlue)
- Brute-force attack (Hydra)
- LLMNR poisoning (Responder)
- VPN connectivity testing
- TLS version verification

---

## 📊 Key Results

| Security Control | Status |
|-----------------|--------|
| Network Segmentation | ✅ Working |
| SMBv1 Disabled | ✅ Secure |
| LLMNR Poisoning | ❌ Blocked |
| Brute Force Attack | ❌ Blocked |
| TLS Hardening | ✅ Enforced |
| VPN Access | ✅ Functional |
| IDS Detection | ✅ Active |
| Sysmon Logging | ✅ Enabled |
| WAC Management | ✅ Operational |

---

## 🔍 Key Insight
A single misconfigured machine can compromise the entire network.

During testing, LLMNR poisoning initially succeeded due to an unsecured client. Once properly hardened, the attack failed completely — highlighting the importance of **consistent security across all endpoints**.

---

## 🏁 Conclusion
This lab demonstrates a complete **defensive security architecture**, combining:

- Network-level controls  
- Host-level hardening  
- Monitoring & detection  
- Secure remote access  

It provides a strong foundation for **real-world cybersecurity roles**, especially in:
- SOC operations  
- Blue teaming  
- Network defense  

---

## 📂 Repository Contents
Full Lab Report (PDF) Containing:
- Configuration steps
- Commands & scripts
- Screenshots 

---

## ⭐ Future Improvements
- SIEM integration (Splunk / ELK)
- Automated threat response
- Log correlation & alerting
- Endpoint Detection & Response (EDR)

---
