# Windows Security Monitoring Lab Using Sysmon

## Overview

This project demonstrates a Security Operations Center (SOC) home lab built using Windows, Sysmon, Event Viewer, and Kali Linux. The objective of the lab was to monitor, generate, and analyze security events to gain hands-on experience with endpoint monitoring, log analysis, and basic threat detection techniques.

The lab simulates common SOC activities such as process monitoring, PowerShell execution tracking, network activity analysis, and authentication event investigation.

---

## Lab Architecture

```text
Kali Linux VM
      |
Windows VM
 ├─ Sysmon
 └─ Event Viewer
```

---

## Technologies Used

* Windows 10/11
* Kali Linux
* Sysmon (Microsoft Sysinternals)
* Windows Event Viewer
* Nmap
* Command Prompt
* PowerShell

### SIEM Technologies Explored

* Splunk
* Wazuh

---

## Project Objectives

* Configure endpoint monitoring using Sysmon.
* Generate and analyze Windows security events.
* Monitor process creation and PowerShell activity.
* Investigate network connections generated from Kali Linux.
* Analyze authentication events.
* Understand SOC workflows and incident investigation fundamentals.

---

## Sysmon Configuration

Sysmon was installed to enhance Windows logging and provide detailed visibility into system activities such as:

* Process creation
* Network connections
* Process execution
* PowerShell activity
* Security monitoring events

---

## Activities Performed

### 1. Process Monitoring

Applications such as Notepad, Calculator, and Event Viewer were executed and monitored through Sysmon.

**Event ID:** 1

**Purpose:**

* Detect process creation events
* Monitor application execution
* Identify suspicious process activity

---

### 2. PowerShell Monitoring

PowerShell commands were executed and logged through Sysmon.

Example:

```powershell
Get-Process
```

**Event ID:** 1

**Purpose:**

* Monitor administrative activity
* Detect PowerShell usage
* Investigate script execution behavior

---

### 3. Network Activity Monitoring

Network activity was generated using:

```bash
ping google.com
```

and

```bash
nmap <target-ip>
```

from Kali Linux.

**Event ID:** 3

**Purpose:**

* Monitor network connections
* Identify outbound communications
* Observe network reconnaissance activity

---

### 4. Authentication Monitoring

Login activities were generated and analyzed using Windows Security Logs.

#### Successful Login

**Event ID:** 4624

#### Failed Login

**Event ID:** 4625

**Purpose:**

* Detect unauthorized access attempts
* Monitor authentication events
* Investigate account activity

---

## Key Event IDs

| Event ID | Description        |
| -------- | ------------------ |
| 1        | Process Creation   |
| 3        | Network Connection |
| 4624     | Successful Login   |
| 4625     | Failed Login       |

---

## Screenshots

The project includes screenshots demonstrating:

* Sysmon installation
* Process creation events
* PowerShell execution logs
* Network connection monitoring
* Successful login events
* Failed login events

---

## Results

Successfully:

* Installed and configured Sysmon
* Generated Windows security events
* Monitored process execution
* Investigated network activity
* Analyzed authentication logs
* Performed basic security event investigation
* Simulated SOC monitoring activities

---

## Skills Gained

* Security Monitoring
* Windows Event Analysis
* Sysmon Configuration
* Log Analysis
* Endpoint Monitoring
* Threat Detection Fundamentals
* Network Monitoring
* PowerShell Analysis
* Incident Investigation
* SOC Operations

---

## Future Enhancements

* Deploy Splunk for centralized log management
* Deploy Wazuh for endpoint detection and monitoring
* Create security dashboards
* Implement alerting and detection rules
* Expand the lab to include Active Directory monitoring

---

## Conclusion

This project provided practical experience in Windows security monitoring using Sysmon and Event Viewer. By generating and analyzing process, network, and authentication events, the lab helped develop foundational SOC and cybersecurity investigation skills. The project also introduced SIEM concepts through the exploration of Splunk and Wazuh for future enhancements.

