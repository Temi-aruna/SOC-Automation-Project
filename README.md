# SOC Automation Lab for Incident Detection and Response

## Objective
This SOC Automation Lab project is all about creating a hands-on, cloud-based SOC environment for incident detection, case management, and automated response. The goal is to simulate real-world SOC workflows, from log ingestion and alert generation to automated response actions, helping to develop my practical cybersecurity skills.


### Skills Learned

- SIEM & XDR Integration - Configuring Wazuh for log collection, correlation, and threat detection.
- SOAR Implementation - Automating security workflows using Shuffle for rapid responses.
- Case Management - Using TheHive for tracking, analyzing, and managing security incidents.
- Threat Simulation & Detection - Generating security telemetry and analyzing alerts.
- Incident Response & Automation - Implementing playbooks for threat identification, containment, and eradication.

### Tools Used

- Wazuh - SIEM & XDR for log analysis, threat detection, and security monitoring.
- TheHive – Case management system for tracking security incidents and investigations.
- Shuffle - SOAR platform for automating SOC workflows and response actions.
- Cloud Services - Hosting the lab environment for accessibility and scalability.
- Windows & Linux Endpoints - Generating attack telemetry and testing security configurations.

## Steps
### Step 1: Logical Diagram & Planning
Before deploying anything, it's important to map out what components the Security Operations Center lab will contain, how they interact, and where each one lives. This usually helps ensure clarity when building and troubleshooting later.

Using Draw.io, I first created the following diagram to illustrate how logs, alerts, and responses flow through the SOC lab environment:

![Step 1](https://i.imgur.com/CkNfi3u.png)

To breakdown this data flow of how a security event is detected and responded to in regards to this lab:
- Our **Windows 10 Client** generates system logs or events (like a suspicious PowerShell script), and then these events are sent to the **Wazuh Manager**, which collects and analyzes the data. 
- If Wazuh detects a threat, it forwards an alert to **Shuffle**, which enriches the alert by gathering more context from OSINT (like checking if an IP is malicious)
- The enriched alert is sent to **TheHive**, which automatically creates an investigation case.
- Shuffle will also send an email to notify the SOC Analyst of the new alert or action taken, and the analyst will receive the alert and review it in TheHive.
- Depending on the situation, Shuffle might trigger a response, like isolating the device or killing a malicious process.
- Finally, Wazuh will perform the action on the original Windows 10 Client.

Going into further breakdown of our component roles:
- Wazuh: Acts as the main log collector and threat detector.
- TheHive: Handles investigations and tracks all ongoing security alerts.
- Shuffle: Automates the entire process of responding to threats.
- Windows/Linux Endpoints: These are the machines where simulated attacks happen.
- Cloud Hosting: The environment where all these systems live.

This planning stage ensures the rest of my lab runs efficiently and is easy to troubleshoot later.

### Step 2: Cloud & System Deployment

### Step 3: Server & Endpoint Configuration

### Step 4: Generating & Detecting Threats

### Step 5: Automating SOC Workflows
