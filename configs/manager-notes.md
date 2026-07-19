# Wazuh Manager Configuration Notes

## System Information

| Item | Value |
|------|-------|
| Operating System | Ubuntu Server 22.04 LTS |
| SIEM Platform | Wazuh |
| Hypervisor | VirtualBox |

---

# Installed Components

- Wazuh Manager
- Wazuh Dashboard
- Wazuh Indexer

---

# Agent Information

| Endpoint | Operating System |
|-----------|------------------|
| Windows 10 | Wazuh Agent |

---

# Network Configuration

Network Mode:

- Bridged Adapter

Purpose:

- Allows direct communication between the Windows Agent and the Wazuh Manager.

---

# File Integrity Monitoring

Configured real-time monitoring for a Windows directory.

Monitored Events:

- File Creation
- File Modification
- File Deletion

---

# Verification Checklist

- [x] Ubuntu Server Installed
- [x] Wazuh Installed
- [x] Dashboard Accessible
- [x] Windows Agent Installed
- [x] Agent Registered
- [x] Agent Connected
- [x] File Integrity Monitoring Enabled
- [x] Alerts Successfully Generated

---

# Common Commands

## Check Wazuh Manager

```bash
sudo systemctl status wazuh-manager
```

## Restart Manager

```bash
sudo systemctl restart wazuh-manager
```

## Check Dashboard

```bash
sudo systemctl status wazuh-dashboard
```

## Restart Dashboard

```bash
sudo systemctl restart wazuh-dashboard
```

## Check Indexer

```bash
sudo systemctl status wazuh-indexer
```

## Restart Indexer

```bash
sudo systemctl restart wazuh-indexer
```

---

# Troubleshooting

## Agent Offline

Possible causes:

- Incorrect Manager IP
- Firewall restrictions
- Agent service stopped
- Network connectivity issues

---

## Dashboard Unreachable

Possible causes:

- Dashboard service stopped
- Incorrect HTTPS URL
- SSL certificate warning
- Network configuration

---

## No FIM Alerts

Check:

- Agent is online
- Directory configured correctly
- Real-time monitoring enabled
- Agent restarted after configuration changes

---

# Future Enhancements

- Deploy Linux Agents
- Configure Sysmon
- Enable Active Response
- Integrate Threat Intelligence
- Create Custom Rules
- Add YARA Malware Detection
