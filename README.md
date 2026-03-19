# AD-Homelab-Splunk-SOC-Lab
Simple Active Directory home lab (Windows Server 2022 DC + Win10 client + Kali attacker + Splunk on Ubuntu). All VMs on NAT network. Simulated attacks from Kali → investigated in Splunk for SOC practice.

# Active Directory Home Lab with Splunk Monitoring

*Active directory project **

Built a fully functional Active Directory lab to practice domain administration, penetration testing, and log investigation in Splunk.

### Executive Summary
I created an isolated AD environment using:
- Windows Server 2022 (Domain Controller)
- Windows 10 client (domain-joined)
- Kali Linux (attacker machine)
- Ubuntu + Splunk Enterprise (SIEM)

All VMs connected via NAT network. I ran password brute-force attacks from Kali, then used Splunk to detect and investigate the activity in real time. Perfect practice for SOC Tier 1 alert triage and Helpdesk AD troubleshooting.

### Lab Architecture
Net- DIAG (NAT network – all VMs isolated from internet)

```mermaid
graph TD
    Kali[Kali Linux - Attacker] --> NAT

    Win10[Windows 10 Client - Domain joined] --> NAT
    DC[Windows Server 2022 - DC + AD DS] --> NAT
    Splunk[Ubuntu 22.04 - Splunk Enterprise] --> NAT
