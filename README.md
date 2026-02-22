# SOC-Detection-Home-Lab
🔐 Detection Engineering Lab

This project simulates a real-world security operations environment built to practice threat detection, alert triage, and incident investigation using open-source SIEM and IDS tools. The lab focuses on building practical blue-team detection skills aligned with SOC and CSIRT roles.

🎯 Objectives

1. Simulate enterprise security monitoring workflows
2. Detect reconnaissance and brute-force activity
3. Build and test custom detection rules
4. Validate alerts using network traffic analysis
5. Practice SIEM log correlation and investigation

🏗️ Lab Architecture

1. Attacker: Kali Linux
2. Target Endpoints: Linux & Windows
3. SIEM: Wazuh Manager
4. IDS: Suricata (manager + endpoint)
5. Domain Services: Windows Server Domain Controller (Active Directory) for centralized identity/authentication
6. Endpoints: Windows endpoint joined to the domain + Linux endpoint for attack simulation and monitoring
7. Monitoring: Email alerting + log correlation

🔍 Detection Scenarios Implemented

1. SSH brute-force detection
2. Nmap reconnaissance detection
3. Suspicious TCP scan detection
4. Network anomaly validation
5. IDS → SIEM alert pipeline validation

🛠️ Technologies Used

1. Wazuh SIEM
2. Suricata IDS
3. Kali Linux
4. Wireshark / tcpdump
5. Linux & Windows endpoints
6. Firewall & network logs

🧪 Key Learning Outcomes

1. Alert triage and investigation
2. Detection tuning to reduce false positives
3. Log correlation across SIEM and IDS
4. Network traffic analysis
5. SOC workflow simulation

📬 Alerting Workflow

1. Alerts generated in Suricata are ingested into Wazuh and trigger automated email notifications for validation of the detection pipeline.

🚧 Project Status

In progress — expanding detection scenarios and documentation as part of a cybersecurity capstone project
