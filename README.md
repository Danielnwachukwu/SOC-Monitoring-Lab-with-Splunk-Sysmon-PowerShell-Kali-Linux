# SOC Analyst Home Lab – Splunk + Sysmon + PowerShell Detection Engineering Project

---

## Project Overview

This project demonstrates the design and implementation of a functional
SOC (Security Operations Center) home lab focused on:

* Windows Event Monitoring
* Sysmon Log Collection
* Splunk SIEM Ingestion
* PowerShell Activity Detection
* Network Connection Monitoring
* DNS Activity Monitoring
* Nmap Enumeration Detection
* Security Event Visualization
* Real-Time Log Analysis

The lab simulates realistic attacker and administrator behaviors while
showcasing how security telemetry is collected, analyzed, and
visualized inside Splunk.

---

# Lab Architecture

## Environment Components

| Component         | Purpose                                    |
| ----------------- | ------------------------------------------ |
| Windows 11 Host   | Target system generating logs              |
| Sysmon            | Advanced Windows event logging             |
| Splunk Enterprise | SIEM platform for monitoring and analytics |
| Kali Linux VM     | Simulated attacker machine                 |
| PowerShell        | Command execution and activity generation  |
| Nmap              | Network enumeration simulation             |

---

# Key Security Monitoring Capabilities

## Sysmon Event Monitoring

* Process creation logging
* Network connection monitoring
* PowerShell execution tracking
* DNS query monitoring
* Event correlation analysis

## Splunk SIEM Analytics

* Real-time event ingestion
* Pattern analysis
* Statistical event analysis
* Timechart visualizations
* Threat activity investigation

## Detection Engineering

* Encoded PowerShell detection
* HTTP web request activity detection
* Nmap scan visibility
* Network connection tracking
* Security telemetry analysis

---

# SOC Investigation Workflow

This lab demonstrates how a SOC analyst can investigate suspicious
activity using Splunk Enterprise, Sysmon telemetry, PowerShell logs,
and network monitoring data.

---

## Detection

Suspicious activity was identified through multiple monitoring sources
within the lab environment.

Detection sources included:

* Sysmon process creation events
* PowerShell execution monitoring
* Network connection telemetry
* DNS query activity
* Splunk correlation searches
* Security event visualizations

Alerts and anomalies were identified through Splunk searches and
Sysmon event analysis.

---

## Triage

Initial alert validation was performed to determine the legitimacy and
severity of the observed activity.

Triage activities included:

* Reviewing Splunk dashboards
* Examining process execution events
* Analyzing PowerShell command-line activity
* Identifying source and destination hosts
* Assessing potential security impact
* Determining investigation priority

---

## Investigation

A detailed investigation was conducted to understand the scope and
nature of the observed activity.

Investigation activities included:

* Correlating Sysmon events
* Reviewing PowerShell execution activity
* Investigating HTTP web requests
* Analyzing DNS resolution events
* Examining network communication patterns
* Investigating Nmap enumeration activity
* Reviewing historical event data

The collected telemetry provided visibility into endpoint activity and
enabled suspicious behavior to be reconstructed through event
correlation and timeline analysis.

---

## Threat Hunting

Additional hunting activities were performed to identify related
indicators and suspicious patterns.

Threat hunting activities included:

* Searching for related indicators
* Identifying abnormal endpoint behavior
* Reviewing historical event trends
* Correlating multiple log sources
* Mapping activity to MITRE ATT&CK techniques
* Identifying reconnaissance-related behavior

---

## Lessons Learned

This exercise demonstrated how Splunk Enterprise and Sysmon telemetry
can be leveraged to detect, investigate, and analyze suspicious
activity within a SOC environment.

Key lessons learned included:

* SOC monitoring workflows
* Splunk search and analytics
* Detection engineering concepts
* Sysmon event analysis
* Threat hunting methodologies
* Event correlation techniques
* Security telemetry visualization

---

# Tools & Technologies Used

* Splunk Enterprise
* Sysmon
* Windows PowerShell
* Kali Linux
* Nmap
* Windows Event Logging
* SPL (Search Processing Language)

---

# Example SPL Queries Used

## Detect PowerShell Activity

```spl
index=* powershell.exe
```

## Detect Sysmon Network Connections

```spl
index=* "<EventID>3</EventID>"
```

## Visualize Sysmon Event Frequency

```spl
index=* "<EventID>1</EventID>" | timechart count
```

## Monitor Sysmon Operational Logs

```spl
index=* source="WinEventLog:Microsoft-Windows-Sysmon/Operational" | timechart count
```

---

# Security Events Demonstrated

* PowerShell execution logging
* Encoded PowerShell execution
* HTTP web request activity
* DNS monitoring
* Network connection detection
* Nmap enumeration visibility
* Process enumeration
* Real-time Sysmon event collection
* Statistical analysis of security events

---

# Project Screenshots

## Core Detection & Monitoring

### Splunk Detection of Network Connection Events

### PowerShell Activity Monitoring with Splunk

### Sysmon Operational Log Timechart

### Splunk Sysmon Log Ingestion Verification

---

## Threat Simulation & Adversary Activity

### Encoded PowerShell Command Execution Simulation

### HTTP Web Request Activity via PowerShell

### Kali Linux Nmap Enumeration Against Windows Host

### Kali Linux to Windows Host Connectivity Verification

---

## Security Analytics & Event Correlation

### Sysmon Event Timechart Analysis

### Sysmon Network Connection Event Correlation in Splunk

### DNS Resolution Activity Monitoring

### Network Traffic Trend Visualization

---

# Key Learning Outcomes

* Building a SOC home lab
* Configuring Sysmon logging
* Forwarding logs into Splunk
* Writing SPL detection queries
* Visualizing security telemetry
* Monitoring PowerShell activity
* Detecting reconnaissance behavior
* Performing basic threat hunting
* Conducting SOC investigations
* Correlating security events

---

# Future Improvements

* Sigma rule integration
* Splunk dashboards
* MITRE ATT&CK mapping
* Brute-force detection rules
* Alert automation
* Threat intelligence enrichment

---

# Author

Daniel Nwachukwu

SOC Analyst | Splunk SIEM | Sysmon Monitoring |
Threat Hunting | PowerShell Detection Engineering
