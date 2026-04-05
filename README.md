# WazuhOps - Home SOC / SIEM Infrastructure

![Status](https://img.shields.io/badge/status-active-brightgreen)
![Wazuh](https://img.shields.io/badge/Wazuh-4.11.2-blue)

Personal Security Operations Center built on Wazuh, monitoring a real Ubuntu server (HomeOps) for threats, intrusions and security events in real time.

---

## Architecture
Windows 11 (Hyper-V)
├── wazuh-server VM (6GB RAM)
│   ├── Wazuh Manager    → receives and analyzes alerts
│   ├── Wazuh Indexer    → stores and indexes events
│   └── Wazuh Dashboard  → real-time visualization
│
└── homeops-server VM (2GB RAM)
└── Wazuh Agent      → monitors and forwards events

---

## Stack

| Component | Technology |
|---|---|
| Virtualization | Hyper-V (Windows 11) |
| OS | Ubuntu Server 24.04 LTS |
| SIEM | Wazuh 4.11.2 |
| Orchestration | Docker + Docker Compose |
| Agent | Wazuh Agent v4.11.2 |
| Framework | MITRE ATT&CK |

---

## What it detects

- SSH brute force and authentication failures
- Privilege escalation attempts
- File integrity monitoring
- System configuration changes
- MITRE ATT&CK technique classification

---

## Results

- 611+ security events captured in first hours
- 381 authentication failures detected
- 10 successful authentications tracked
- MITRE ATT&CK techniques identified: Password Guessing, SSH, Brute Force, Valid Accounts, Sudo
- Real-time alerting with automatic severity classification
- Active Response configured to block brute force IPs automatically
- File Integrity Monitoring active on critical system files
## Skills demonstrated

- SIEM deployment and configuration (Wazuh)
- Security event monitoring and analysis
- Docker multi-container orchestration
- Linux server administration
- Threat detection with MITRE ATT&CK framework
- Blue Team / SOC analyst workflows
- Network security monitoring
