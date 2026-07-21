# Enterprise SOC Home Lab

## Project Overview

The Enterprise SOC Home Lab is a hands-on cybersecurity project built to develop practical Security Operations Center (SOC) skills.

The lab simulates a small enterprise environment using Windows Server Active Directory, Wazuh SIEM, Sysmon, and Windows endpoints. It provides a platform for learning log collection, security monitoring, attack simulation, incident investigation, and MITRE ATT&CK mapping.

This project was created for learning, portfolio development, and demonstrating foundational SOC Analyst skills.

## Objectives

- Build a realistic SOC home lab.
- Learn Windows Active Directory administration.
- Deploy and configure Wazuh SIEM.
- Collect and analyze Windows logs.
- Monitor endpoints using Sysmon.
- Simulate common attack techniques.
- Investigate security alerts.
- Document incidents professionally.
- Understand MITRE ATT&CK techniques.

  ## Lab Components

| Component | Purpose |
|----------|---------|
| VMware Workstation | Virtualization Platform |
| Windows Server 2022 | Active Directory Domain Controller |
| Ubuntu Server | Wazuh Manager, Indexer & Dashboard |
| Windows 11 | Monitored Endpoint |
| Sysmon | Endpoint Monitoring |
| Wazuh Agent | Log Collection |
| Kali Linux | Attack Simulation |



## Technologies Used

- VMware Workstation
- Windows Server 2022
- Windows 11
- Ubuntu Server
- Active Directory
- DNS
- Wazuh SIEM
- Sysmon
- PowerShell
- Linux

## Lab Architecture

> Architecture diagram coming soon.


## Documentation

The complete project documentation is available in the `docs/` directory.

| Section | Description |
|---------|-------------|
| Architecture | Lab design |
| Installation | System setup |
| Active Directory | Domain configuration |
| Wazuh | SIEM deployment |
| Sysmon | Endpoint monitoring |
| Attack Simulation | Security testing |
| Incident Response | Alert investigations |
| MITRE ATT&CK | Technique mapping |


## Attack Simulations

The following attack scenarios were simulated in the lab:

- Failed Login Attempts
- PowerShell Activity
- System Discovery
- Registry Modification
- File Creation
- EICAR Test File

## Skills Demonstrated

- SIEM Administration
- Windows Event Log Analysis
- Active Directory
- Windows Security
- Linux Administration
- Sysmon Configuration
- Threat Hunting
- Incident Response
- MITRE ATT&CK Mapping
- Security Monitoring


## Learning Outcomes

Through this project, I gained practical experience in:

- Deploying a SOC lab
- Configuring enterprise security tools
- Collecting and analyzing security logs
- Investigating alerts
- Writing incident reports
- Understanding attacker techniques

## Future Improvements

- Custom Wazuh Detection Rules
- Sigma Rule Integration
- Email Alerting
- Threat Intelligence Integration
- Active Response Automation

