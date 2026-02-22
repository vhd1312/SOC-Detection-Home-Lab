# Nmap Reconnaissance Detection Investigation

## 🧪 Scenario
Simulated reconnaissance activity from a Kali attacker machine targeting a Linux endpoint in the lab environment.

**Attacker IP:** 192.168.153.131  
**Target IP:** 192.168.153.139  
**Technique:** Nmap TCP SYN Scan  
**MITRE ATT&CK:** T1046 – Network Service Discovery

---

## 🚨 Alert Triggered

Suricata generated multiple alerts indicating suspicious TCP scan behavior:

- LOCAL Possible TCP SYN Port Scan  
- LOCAL Possible TCP Connect Scan  
- LAB TCP Port Scan Detected (custom rule)

These alerts were ingested into Wazuh and correlated for validation.

---

## 📸 Detection Evidence

Below shows Suricata detecting the scan in real time from the attacker host:

![Nmap Scan Detection](screenshots/suricata_agent_logs.png)

---

## 🔍 Analysis

Observed behavior:
- High volume of TCP SYN packets from single source
- Multiple destination ports probed
- Pattern consistent with reconnaissance activity

Suricata rules triggered:
- Emerging Threats scan signatures
- Custom local rule for lab validation

Traffic verified using:
- tcpdump
- Suricata fast.log
- Wazuh alert pipeline

