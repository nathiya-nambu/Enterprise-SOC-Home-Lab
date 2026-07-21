# MITRE ATT&CK Mapping

## Overview

The **Enterprise SOC Home Lab** leverages the **MITRE ATT&CK Framework** to classify adversary techniques observed during attack simulations. Mapping alerts to MITRE ATT&CK helps standardize incident analysis, improve threat hunting, and validate security detections.

---

## Verified MITRE ATT&CK Mappings

| Simulation | Description | Technique | Technique ID | Status |
|------------|-------------|-----------|--------------|--------|
| PowerShell Execution | PowerShell temporary file creation detected by Wazuh Rule 92205 | Ingress Tool Transfer | T1105 | ✅ Verified |
| System Information Discovery | Enumeration of system information | System Information Discovery | T1082 | ⏳ Pending Lab Verification |
| Registry Modification | Windows Registry modification activity | Modify Registry | T1112 | ⏳ Pending Lab Verification |

> **Note:** Only mappings verified through Wazuh alerts should be marked as **Verified**. Additional mappings will be added as new attack simulations are completed.

---

## Why MITRE ATT&CK?

Using the MITRE ATT&CK framework enables SOC analysts to:

- Standardize alert classification.
- Understand attacker tactics and techniques.
- Improve threat hunting activities.
- Correlate multiple security events.
- Validate detection coverage.

---

## References

- MITRE ATT&CK Framework: https://attack.mitre.org/
- Wazuh Documentation: https://documentation.wazuh.com/
- Microsoft Sysinternals Sysmon: https://learn.microsoft.com/sysinternals/downloads/sysmon
