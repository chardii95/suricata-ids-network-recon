# Network Reconnaissance Detection with Suricata IDS

## Overview
This project demonstrates the deployment and validation of a Suricata-based Intrusion Detection System (IDS) to monitor and analyze network reconnaissance activity in a NAT-based home SOC lab.

The objective was to simulate attacker reconnaissance, observe IDS behavior, analyze alerting outcomes, and document findings using SOC-standard methodology and the MITRE ATT&CK framework.

---

## Lab Architecture
- **Linux (Ubuntu 24.04 ARM64)** – Suricata IDS sensor
- **Windows 11** – Target endpoint
- **Virtual Network** – UTM shared NAT network

Suricata monitored network traffic on the Linux interface and logged events to structured JSON output (`eve.json`).

---

## Attack Simulation
- **Tool:** Nmap  
- **Technique:** SYN stealth scan  
- **Command:**  nmap -sS -p- <target-ip>

The objective was to generate reconnaissance traffic for IDS inspection and analysis.

---

## Detection Results
- Suricata successfully inspected TCP SYN traffic
- Flow and packet metadata were logged to `eve.json`
- Activity was classified as informational due to threshold-based detection logic and NAT lab constraints
- No exploitation attempts or follow-on activity were observed

This reflects realistic SOC behavior where not all reconnaissance escalates to high-severity alerts.

---

## MITRE ATT&CK Mapping
- Tactic: Discovery
- Technique: Network Service Scanning
- Technique ID: T1046

---

## Skills Demonstrated
- IDS deployment and configuration
- Rule management and validation
- Network traffic inspection
- Structured log analysis (`eve.json`)
- SOC-style incident documentation
- MITRE ATT&CK mapping
