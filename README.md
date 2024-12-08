# SOC-Home-Lab
SOC (Security Operations Center) is a centralized unit within an organization that is responsible for monitoring, detecting, responding to, and managing cybersecurity incidents and threats. It acts as the frontline defense for the organization's IT infrastructure and data.

SOC home lab is a personal, simulated environment set up for learning, practicing, and experimenting with tools and techniques used in cybersecurity operations. It replicates the tools and workflows typically found in a professional SOC.

# Architecture
![Untitled Diagram drawio](https://github.com/user-attachments/assets/01c0924d-9891-49d2-a128-7eb20997ccda)


# Main Components

1. SIEM (Security Information and Event Management):

Tool: Wazuh

Function: Collect, store, and analyze security logs from various sources.

Position: Central log management and core analytics.




2. EDR (Endpoint Detection and Response):

Tools: Velociraptor or OpenEDR

Function: Monitor endpoint activity in real-time, detect anomalous behavior, and provide an initial response.

Position: At each endpoint (server, workstation).




3. SOAR (Security Orchestration, Automation, and Response):

Tools: TheHive + Cortex Analyzer or Shuffle

Function: Orchestrate incident response, security process automation, and team collaboration.

Position: Coordination layer for all other tools.




4. Threat Intelligence Platform (Optional):

Tools: MISP (Malware Information Sharing Platform).

Function: Manage and share threat intelligence data to enrich incident context.

Position: Data enrichment and integration with SIEM/SOAR.






---

# Workflow

1. Data Collection:

Endpoint:

Wazuh collects endpoint activity logs from installed agents (log files, event system).

Velociraptor or OpenEDR monitors real-time behavior (files, processes, networks).


Network:

Firewall/IDS/IPS sends logs to Wazuh (example: using Suricata for IDS/IPS).


Threat Intelligence:

MISP enriches the discovered threat information.




2. Analysis & Correlation:

Wazuh as SIEM correlates logs to detect threats based on rules and anomaly detection.



3. Automated Response:

Wazuh + TheHive integration:

If there is a threat, Wazuh sends an alert to TheHive as an incident case.


TheHive + Cortex Analyzer:

Cortex runs automated analysis (e.g. IP reputation check, file hash analysis).




4. Remediation:

TheHive + Velociraptor/OpenEDR:

If the incident is confirmed, TheHive can send commands to Velociraptor or OpenEDR to take action (e.g. endpoint isolation, file/process blocking).


Automated Playbook:

Shuffle automates the response playbook (e.g. block IP at firewall, delete malicious files).

Translated with DeepL.com (free version)
