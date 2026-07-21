# Enterprise SOC Home Lab Architecture

## Overview

This project simulates an enterprise Security Operations Center (SOC) environment using Windows Server, Active Directory, Wazuh SIEM, Sysmon, Ubuntu Server, Windows 11, and Kali Linux.

The objective is to collect endpoint telemetry, detect suspicious activities, investigate alerts, and practice incident response in a controlled lab environment.

---

## Lab Components

| Component | Purpose |
|-----------|----------|
| VMware Workstation | Virtualization Platform |
| Windows Server 2022 | Active Directory Domain Controller |
| Ubuntu Server | Wazuh Manager |
| Windows 11 | Employee Endpoint |
| Kali Linux | Attack Simulation |
| Sysmon | Endpoint Monitoring |
| Wazuh Agent | Log Collection |
| Wazuh Dashboard | Security Monitoring |

---

## Network

- Domain: lab.local
- Windows Server: Domain Controller
- Ubuntu Server: Wazuh Manager
- Windows 11: Domain Joined Endpoint
- Kali Linux: Attacker Machine

---

## Objectives

- Build an enterprise SOC environment.
- Centralize security logs.
- Simulate cyber attacks.
- Detect malicious activity.
- Perform incident investigation.
- Map detections to MITRE ATT&CK.
