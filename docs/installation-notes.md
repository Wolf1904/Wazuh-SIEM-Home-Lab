# Wazuh SIEM Home Lab - Installation Notes

## Project Overview

This document describes the installation and configuration process used to deploy a Wazuh SIEM Home Lab.

## Environment

| Component | Details |
|----------|----------|
| Hypervisor | VirtualBox |
| Manager OS | Ubuntu Server 22.04 LTS |
| Agent OS | Windows 10 |
| SIEM Platform | Wazuh |
| Network Mode | Bridged Adapter |

---

# Lab Architecture

```
Windows 10 (Agent)
        │
        │
        ▼
Ubuntu Server (Wazuh Manager)
        │
        ├── Wazuh Dashboard
        ├── Wazuh Manager
        └── Wazuh Indexer
```

---

# Installation Steps

## 1. Prepare Ubuntu Server

- Install Ubuntu Server 22.04
- Update packages
- Configure network connectivity
- Verify internet access

---

## 2. Install Wazuh Manager

Installed Wazuh Manager using the official installation script.

Components installed:

- Wazuh Manager
- Wazuh Dashboard
- Wazuh Indexer

---

## 3. Access Dashboard

After installation:

- Obtain Ubuntu IP address
- Open HTTPS connection
- Login using generated credentials

---

## 4. Install Windows Agent

Downloaded and installed the Wazuh Windows Agent.

Configuration included:

- Manager IP Address
- Agent Registration
- Service Startup

---

## 5. Register Agent

Registered the Windows endpoint with the Wazuh Manager.

Verification:

- Agent appears as Active
- Heartbeat communication established

---

## 6. Configure File Integrity Monitoring

Enabled real-time monitoring on a test directory.

Example monitored folder:

```
C:\Users\<User>\Test
```

---

## 7. Verification

Performed the following actions:

- Create file
- Modify file
- Delete file

Observed corresponding alerts within the Wazuh Dashboard.

---

# Skills Learned

- SIEM deployment
- Linux administration
- Windows endpoint management
- Agent onboarding
- File Integrity Monitoring
- Security event analysis
- Dashboard monitoring
- Virtual networking

---

# Future Improvements

- Deploy multiple agents
- Install Sysmon
- Configure Active Response
- Create custom detection rules
- Integrate VirusTotal
- Configure Email Alerts
- Simulate attack scenarios
