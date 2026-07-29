# 🛡️ SOC Lab – Sysmon Log Ingestion and Analysis with Splunk

## 📖 Project Overview

This project demonstrates a hands-on Security Operations Center (SOC) lab focused on collecting and analysing Windows endpoint telemetry using Sysmon and Splunk.

Sysmon was used to generate detailed Windows process and system activity logs. Splunk Universal Forwarder was then configured to send the Sysmon Operational event channel to Splunk Enterprise through receiving port 9997.

The project demonstrates endpoint log collection, forwarder configuration, Windows event ingestion, XML event analysis, and basic threat-detection workflows using Splunk.
## 🎯 Objectives

The primary objectives of this lab were to:

- Install and configure Splunk Enterprise on Windows.
- Enable Splunk to receive forwarded data on TCP port **9997**.
- Install and configure the Splunk Universal Forwarder.
- Forward the Sysmon Operational event channel to Splunk Enterprise.
- Verify the connection between the Universal Forwarder and Splunk.
- Confirm that Sysmon events were successfully indexed in `index=main`.
- Analyse raw Sysmon XML events in Splunk.
- Filter and investigate Sysmon Process Create events, including Event ID **1**.
- Build practical experience with endpoint telemetry, log ingestion, and basic SOC monitoring workflows.
## 🛠️ Technologies Used

| Category | Technology |
|----------|------------|
| Host Operating System | Windows 11 |
| Endpoint Telemetry | Sysmon |
| SIEM Platform | Splunk Enterprise |
| Log Forwarding | Splunk Universal Forwarder |
| Windows Log Source | Microsoft-Windows-Sysmon/Operational |
| Transport Port | TCP 9997 |
| Configuration | `inputs.conf` |
| Search Language | Splunk Processing Language (SPL) |
<a id="lab-architecture"></a>

## 🏗️ Lab Architecture

```text
Windows 11 Endpoint
        │
        │  Sysmon generates endpoint telemetry
        ▼
Microsoft-Windows-Sysmon/Operational
        │
        │  Collected by Splunk Universal Forwarder
        ▼
Splunk Universal Forwarder
        │
        │  TCP 9997
        ▼
Splunk Enterprise
        │
        ▼
Search, Filtering and Event Analysis
```
## 🖥️ Task 1 – Splunk Enterprise Setup

### Objective

Install Splunk Enterprise on Windows 11 and verify that the SIEM platform is accessible through the Splunk web interface.

### Activities Performed

- Installed Splunk Enterprise on the Windows 11 host.
- Used the default installation directory.
- Created the Splunk administrator account.
- Confirmed that the installation completed successfully.
- Accessed the Splunk login page through `http://localhost:8000`.
- Signed in and verified that the Splunk Enterprise home page loaded correctly.

### Skills Demonstrated

- Splunk Enterprise Installation
- Windows SIEM Setup
- Administrator Account Configuration
- Splunk Web Access
- Basic Service Verification

### Screenshots

#### Splunk Enterprise Installation Completed

![Splunk Enterprise Installation Completed](images/Splunk%20Installation%20Completed.png)

#### Splunk Login Page

![Splunk Enterprise Login Page](images/Splunk%20Login%20Page.png)

#### Splunk Enterprise Home Page

![Splunk Enterprise Home Page](images/Splunk%20Home%20Page.png)
