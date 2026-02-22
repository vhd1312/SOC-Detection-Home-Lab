# SOC-Detection-Home-Lab
🔐Blue-Team Detection Engineering & Incident Response Lab

This project simulates a real-world Security Operations Center (SOC) environment built to practice threat detection, alert triage, and incident investigation using open-source SIEM and IDS tools.
The lab is designed to mirror enterprise detection workflows and strengthen hands-on blue-team skills aligned with SOC Analyst and CSIRT roles.

🎯 Objectives

1. Simulate enterprise security monitoring workflows
2. Detect reconnaissance and brute-force activity
3. Build and test / tune custom detection rules
4. Validate alerts using network traffic analysis
5. Practice SIEM log correlation and investigation workflows

🏗️ Lab Architecture

**Attacker**
1. Kali Linux (reconnaissance + attack simulation)

**Monitoring Stack**
1. Wazuh SIEM (manager)
2. Suricata IDS (manager + endpoint sensor)
   
**Endpoints**
1. Windows Server Domain Controller (Active Directory)
2. Windows endpoint joined to domain
3. Linux endpoint with Suricata agent
   
**Network**
1. NAT-based segmented lab network
2. Centralized logging to Wazuh
3. Email alert pipeline for detection validation

🛠️ Technologies Used

1. Wazuh SIEM
2. Suricata IDS
3. Kali Linux
4. Windows Server (Active Directory Domain Controller)
5. Windows & Linux endpoints
6. Wireshark / tcpdump
   
🔍 Detection Scenarios Implemented

1. SSH brute-force detection
2. Nmap reconnaissance detection
3. Suspicious TCP scan detection
4. Network anomaly validation
5. IDS → SIEM alert pipeline validation
6. Domain-joined endpoint monitoring via Wazuh agent

🧠 Investigation & Validation Workflow

1. Generated attack traffic from Kali Linux
2. Captured packets using tcpdump/Wireshark
3. Validated Suricata alerts in eve.json
4. Correlated alerts inside Wazuh
5. Tuned detection rules to reduce noise
6. Verified email alert pipeline
This workflow mirrors real SOC analyst processes:
**alert → validate → correlate → investigate → tune**

🧪 Key Learning Outcomes

1. Alert triage and investigation
2. Detection rule tuning to reduce false positives
3. Log correlation across SIEM and IDS
4. Network traffic analysis
5. SOC workflow simulation
6. IDS → SIEM integration

📬 Alerting Workflow

Suricata alerts are ingested into Wazuh and forwarded via automated email notifications to validate detection coverage and response workflow.

🚧 Project Status

**Active – Expanding Detection Coverage**

Continuously enhancing the lab by integrating additional security controls and detection sources. Upcoming improvements include firewall log ingestion and vulnerability scanning with Nessus to broaden detection visibility, improve alert correlation, and simulate more realistic enterprise SOC monitoring scenarios.
