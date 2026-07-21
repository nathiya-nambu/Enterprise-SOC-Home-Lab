# PowerShell Incident Investigation

## Incident Overview

| Field | Value |
|-------|-------|
| **Alert Name** | PowerShell process created an executable file in Windows root folder |
| **Rule ID** | 92205 |
| **Severity** | 9 (Medium) |
| **Manager** | soc01 |
| **Date** | Jul 20, 2026 |
| **Time** | 17:38:49.033 |
| **Endpoint** | WIN11-HR01 |
| **Source IP** | 192.168.50.30 |
| **User** | NT AUTHORITY\SYSTEM |

---

## Event Details

| Field | Value |
|-------|-------|
| **Event Source** | Microsoft-Windows-Sysmon |
| **Event ID** | 11 (File Creation) |
| **Process** | powershell.exe |
| **Target File** | `C:\Windows\SystemTemp\__PSScriptPolicyTest_4m2qn2ol.crq.ps1` |

---

## MITRE ATT&CK Mapping

| Tactic | Technique | Technique ID |
|---------|-----------|--------------|
| Command and Control | Ingress Tool Transfer | T1105 |

---

## Investigation Summary

A Wazuh alert was generated after **PowerShell (`powershell.exe`)** created a file inside the **Windows SystemTemp** directory. The event was captured by **Sysmon Event ID 11 (File Creation)** and forwarded to the Wazuh Manager for analysis.

The investigation identified the created file:

```text
C:\Windows\SystemTemp\__PSScriptPolicyTest_4m2qn2ol.crq.ps1
```

This file is a **temporary PowerShell execution policy validation file** automatically created by Windows PowerShell during execution policy verification.

The activity was performed under the **NT AUTHORITY\SYSTEM** account, indicating that it originated from the operating system rather than an interactive user.

No evidence of malicious activity was identified during the investigation.

---

## Investigation Findings

The investigation found **no indicators** of the following malicious behaviors:

- Malware execution
- Payload download
- Privilege escalation
- Registry persistence
- Lateral movement
- Data exfiltration
- Unauthorized PowerShell script execution

---

## Impact Assessment

| Assessment | Result |
|------------|--------|
| Malware Detected | ❌ No |
| Persistence | ❌ Not Observed |
| Privilege Escalation | ❌ Not Observed |
| Lateral Movement | ❌ Not Observed |
| Data Exfiltration | ❌ Not Observed |
| System Impact | Low |

---

## Root Cause

The alert was triggered because PowerShell generated a temporary execution policy validation file.

Although the activity matched a Wazuh detection rule, further analysis confirmed that it represents normal Windows functionality and does not indicate malicious behavior.

---

## Recommendation

- Continue monitoring PowerShell activity for suspicious behavior.
- Review future PowerShell events containing encoded commands, remote downloads, execution policy bypass attempts, or unsigned script execution.
- Correlate PowerShell events with process ancestry, command-line arguments, and network activity before determining malicious intent.

---

## Analyst Conclusion

The investigation determined that the detected activity was a legitimate Windows PowerShell operation performed during execution policy validation.

No Indicators of Compromise (IOCs) or malicious behavior were identified.

The alert is classified as **Benign Activity (False Positive)**.

---

## Case Closure

| Field | Value |
|-------|-------|
| **Status** | Closed |
| **Classification** | Benign Activity (False Positive) |
| **Risk Level** | Low |
| **Analyst Decision** | No remediation required. Continue monitoring future PowerShell activity. |

---

# Evidence

## Figure 1 – Wazuh Alert


<img width="1482" height="126" alt="Image" src="https://github.com/user-attachments/assets/7a961d07-548b-47e6-88d5-c7e43b35d3a6" />

---

## Figure 2 – Event Details

<img width="1918" height="1078" alt="Image" src="https://github.com/user-attachments/assets/0ca1a5b4-6fd4-4cf6-9fa5-5c53e00db0fa" />


---

## Figure 3 – MITRE ATT&CK Mapping

<img width="898" height="352" alt="Image" src="https://github.com/user-attachments/assets/f27ebc8e-aa21-47ff-b909-060659582c2f" />

---

## Figure 4 – Threat Hunting Investigation


<img width="1918" height="1031" alt="Image" src="https://github.com/user-attachments/assets/104b1a65-3f13-460e-899e-a348cbe6af49" />

---

## Skills Demonstrated

- Wazuh SIEM Alert Investigation
- Sysmon Event Analysis
- Windows Event Log Analysis
- Threat Hunting
- MITRE ATT&CK Mapping
- Incident Response
- Root Cause Analysis
- False Positive Identification
