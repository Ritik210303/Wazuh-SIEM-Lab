# Wazuh-SIEM-Lab

This project demonstrates the deployment of a **Wazuh SIEM environment** integrated with an Active Directory-based lab to simulate real-world Security Operations Center (SOC) monitoring.

The lab focuses on centralized log collection, endpoint monitoring, and security event analysis across multiple systems.

---

## Lab Architecture

The environment consists of:

- Windows Server 2022 (Domain Controller)
- Windows 10 Client
- Ubuntu Client
- Wazuh Server (OVA Deployment)

All systems are connected through a VirtualBox NAT Network:

- Network: 172.16.1.0/24

---

## Key Implementations

### Wazuh Deployment
- Installed using official Wazuh OVA (v4.14.4)
- Includes:
  - Wazuh Manager
  - Wazuh Indexer
  - Wazuh Dashboard

---

### Network Configuration
- NAT Network configured in VirtualBox
- Port forwarding setup:

| Service | Host Port | Guest IP | Guest Port |
|--------|----------|---------|-----------|
| Agents | 1514 | 172.16.1.5 | 1514 |
| Auth   | 1515 | 172.16.1.5 | 1515 |
| Dashboard | 8443 | 172.16.1.5 | 443 |

---

### Agent Deployment

Wazuh agents were installed on:

- Windows Server (Domain Controller)
- Windows 10 Client
- Ubuntu Client

All agents successfully connected and started sending logs.

---

### Monitoring & Validation

- Verified agent connectivity through dashboard
- Observed real-time log collection
- Confirmed centralized monitoring

---

## Key Learnings

- Understanding SIEM architecture (Agent → Manager → Indexer → Dashboard)
- Centralized log analysis and monitoring
- Cross-platform endpoint security monitoring
- Real-world SOC workflow simulation

---

## Full Report

You can view the complete detailed report here:

 Wazuh_Setup.pdf

---

## Future Work

- Brute-force attack detection using Wazuh
- Custom rule creation and tuning
- Alert investigation and incident response
- Integration with additional endpoints

---

## Author

**Ritik Patel**  
SOC – Threat Research Intern
