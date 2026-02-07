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
- **Command:**  
