# SOC-Home-Lab
SOC (Security Operations Center) is a centralized unit within an organization that is responsible for monitoring, detecting, responding to, and managing cybersecurity incidents and threats. It acts as the frontline defense for the organization's IT infrastructure and data.

SOC home lab is a personal, simulated environment set up for learning, practicing, and experimenting with tools and techniques used in cybersecurity operations. It replicates the tools and workflows typically found in a professional SOC.


## Main Components

1. SIEM (Security Information and Event Management):

    Tool: Wazuh
  
    Function: Collect, store, and analyze security logs from various sources.
  
    Position: Central log management and core analytics.


2. EDR (Endpoint Detection and Response):

    Tools: Velociraptor
  
    Function: Monitor endpoint activity in real-time, detect anomalous behavior, and provide an initial response.
  
    Position: At each endpoint (server, workstation).


3. IDS/IPS (Intrusion Detection/Prevention System):

    Tool: Suricata
  
    Function: Detect malicious traffic.
  
    Position: At each endpoint (server, workstation).
