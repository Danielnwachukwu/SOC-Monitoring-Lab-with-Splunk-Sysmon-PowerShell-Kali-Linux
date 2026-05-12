
# SOC Analyst Home Lab – Splunk + Sysmon + PowerShell Detection Engineering Project

---

## Project Overview

This project demonstrates the design and implementation of a functional SOC (Security Operations Center) home lab focused on:

- Windows Event Monitoring
- Sysmon Log Collection
- Splunk SIEM Ingestion
- PowerShell Activity Detection
- Network Connection Monitoring
- DNS Activity Monitoring
- Nmap Enumeration Detection
- Security Event Visualization
- Real-Time Log Analysis

The lab simulates realistic attacker and administrator behaviors while showcasing how security telemetry is collected, analyzed, and visualized inside Splunk.

---

# Lab Architecture

## Environment Components

| Component | Purpose |
|---|---|
| Windows 11 Host | Target system generating logs |
| Sysmon | Advanced Windows event logging |
| Splunk Enterprise | SIEM platform for monitoring and analytics |
| Kali Linux VM | Simulated attacker machine |
| PowerShell | Command execution and activity generation |
| Nmap | Network enumeration simulation |

---

# Key Security Monitoring Capabilities

## Sysmon Event Monitoring
- Process creation logging
- Network connection monitoring
- PowerShell execution tracking
- DNS query monitoring
- Event correlation analysis

## Splunk SIEM Analytics
- Real-time event ingestion
- Pattern analysis
- Statistical event analysis
- Timechart visualizations
- Threat activity investigation

## Detection Engineering
- Encoded PowerShell detection
- HTTP web request activity detection
- Nmap scan visibility
- Network connection tracking
- Security telemetry analysis

---

# Tools & Technologies Used

- Splunk Enterprise
- Sysmon
- Windows PowerShell
- Kali Linux
- Nmap
- Windows Event Logging
- SPL (Search Processing Language)

---

# Example SPL Queries Used

## Detect PowerShell Activity

```spl
index=* powershell.exe

Detect Sysmon Network Connections
index=* "<EventID>3</EventID>"

**Visualize Sysmon Event Frequency**
index=* "<EventID>1</EventID>" | timechart count

**Monitor Sysmon Operational Logs**
index=* source="WinEventLog:Microsoft-Windows-Sysmon/Operational"| timechart count


**Security Events Demonstrated**

PowerShell execution logging
Encoded PowerShell execution
HTTP web request activity
DNS monitoring
Network connection detection
Nmap enumeration visibility
Process enumeration
Real-time Sysmon event collection
Statistical analysis of security events


---

# Project Screenshots

---

## Core Detection & Monitoring

### Splunk Detection of Network Connection Events
![Splunk Detection of Network Connection Events](screenshots/Sysmon%20Network%20Connection%20Event%20Detection.png)

---

### PowerShell Activity Monitoring with Splunk
![PowerShell Activity Monitoring with Splunk](screenshots/PowerShell%20Activity%20Monitoring%20with%20Splunk.png)

---

### Real-Time Sysmon Operational Log Visualization
![Real-Time Sysmon Operational Log Visualization](screenshots/Sysmon%20Operational%20Log%20Timechart.png)

---

### Sysmon Log Ingestion Verification
![Sysmon Log Ingestion Verification](screenshots/Splunk%20Sysmon%20Log%20Ingestion%20Verification.png)

---

## Threat Simulation & Adversary Activity

### Encoded PowerShell Command Execution Simulation
![Encoded PowerShell Command Execution Simulation](screenshots/Encoded%20PowerShell%20Command%20Execution%20Simulation.png)

---

### HTTP Web Request Activity via PowerShell
![HTTP Web Request Activity via PowerShell](screenshots/HTTP%20Web%20Request%20Activity%20via%20PowerShell.png)

---

### Kali Linux Nmap Enumeration Against Windows Host
![Kali Linux Nmap Enumeration Against Windows Host](screenshots/Kali%20Linux%20Nmap%20Enumeration%20Against%20Windows%20Host.png)

---

### Kali Linux to Windows Host Connectivity Verification
![Kali Linux to Windows Host Connectivity Verification](screenshots/Kali%20Linux%20to%20Windows%20Host%20Connectivity%20Verification.png)

---

## Security Analytics & Event Correlation

### Sysmon Event Timechart Analysis
![Sysmon Event Timechart Analysis](screenshots/Sysmon%20Event%20Timechart%20Analysis.png)

---

### Sysmon Network Connection Event Correlation in Splunk
![Sysmon Network Connection Event Correlation in Splunk](screenshots/Sysmon%20Network%20Connection%20Event%20Correlation%20in%20Splunk.png)

---

### DNS Resolution Activity Monitoring
![DNS Resolution Activity Monitoring](screenshots/DNS%20Resolution%20Activity%20Monitoring.png)

---

### Network Traffic Trend Visualization
![Network Traffic Trend Visualization](screenshots/Network%20Traffic%20Trend%20Visualization.png)

---


**Threat Simulation**
Kali Linux Nmap Enumeration Against Windows Host
Kali Linux to Windows Host Connectivity Verification

**Security Analytics**
Sysmon Event Frequency Timechart Visualization
Sysmon Network Connection Event Detection
DNS Resolution Activity Monitoring

**Key Learning Outcomes**
Building a SOC home lab
Configuring Sysmon logging
Forwarding logs into Splunk
Writing SPL detection queries
Visualizing security telemetry
Monitoring PowerShell activity
Detecting reconnaissance behavior
Performing basic threat hunting


**Future Improvements**
Sigma rule integration
Splunk dashboards
MITRE ATT&CK mapping
Brute-force detection rules
Alert automation
Threat intelligence enrichment


**Author**
Daniel Nwachukwu

SOC Analyst | Splunk SIEM | Sysmon Monitoring | Threat Hunting | PowerShell Detection Engineering
