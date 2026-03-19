# Azure-Sentinel-Global-Honeypot
🌍 Azure Cloud Security: Global Honeypot & Threat Intelligence
🎯 Objective
I built a live cloud honeypot to capture, parse, and visualize global brute-force attacks in real-time. The goal was to understand attacker behavior, map global threat origins, and practice enterprise-grade SIEM configuration.

🛠️ Tools & Technologies Used
Cloud Infrastructure: Microsoft Azure Virtual Machines (Exposed to internet via custom Network Security Groups).

SIEM: Microsoft Sentinel & Log Analytics Workspaces (LAW).

Query Language: Kusto Query Language (KQL).

Concepts: Threat Intelligence, Log Parsing (Regex), Geo-Enrichment, Data Normalization.

📊 The Results: 72-Hour Attack Data



Using custom KQL scripts, I extracted the raw IP addresses from failed SSH login attempts, mapped them to geospatial coordinates, and visualized the attack 
density


<img width="1848" height="824" alt="Screenshot 2026-03-19 171745" src="https://github.com/user-attachments/assets/5857d860-628e-4bd8-a109-105695187d9c" />




<img width="1831" height="784" alt="Screenshot 2026-03-19 172139" src="https://github.com/user-attachments/assets/b71ac9c3-37b2-41b3-b92c-c5831323486e" />





Attacker Profiling (Username Analysis)
The "Holy Grail" (root): With over 5,100 attempts, bots overwhelmingly target the root account because it holds absolute administrative power.

Default Credentials (admin, ubuntu, user): Bots specifically scan for these to catch cloud engineers who forgot to disable default accounts during setup.

Service Discovery (oracle, ftpuser): Finding oracle suggests they are hunting for vulnerable database servers, while ftpuser indicates attempts to hijack file storage




<img width="1850" height="822" alt="Screenshot 2026-03-19 171517" src="https://github.com/user-attachments/assets/6883ef84-5d1c-415d-9766-005fe74f783a" />









##  Key Takeaways :


This project demonstrated how quickly an exposed asset is discovered by automated global botnets. It highlighted the critical importance of secure defaults, minimizing attack surfaces, and the power of SIEMs in translating raw system telemetry into actionable intelligence.
