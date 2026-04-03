🛡️ Banking SOC Threat Detection Dashboard (Splunk)

This project simulates a real-world Security Operations Center (SOC) environment for a banking system using Splunk.

It focuses on detecting:

Login brute force attempts
Port scanning activity
Traffic spike anomalies
Suspicious IP behavior
🔍 Features
📊 Real-time traffic monitoring
🔴 Brute force detection (Login failures)
🟠 Port scanning detection
🔴 Traffic spike anomaly detection
📋 Suspicious IP activity tracking
📈 SOC-style visual dashboard layout

##🧠 Detection Logic
Port Scanning Detection
index=main event=PORT_SCAN
| stats count by src_ip
| sort -count

##Traffic Spike Detection
index=main event=TRAFFIC_SPIKE
| timechart count

##Top Talkers
index=main
| stats count by src_ip
| sort -count
| head 10

##Suspicious Activity
index=main
| stats count by src_ip, event
| where count > 20
| sort -count

##🏗️ Architecture

This dashboard simulates:

Network logs ingestion
Event categorization
Threat detection rules
Visualization layer in Splunk

##🚀 Tech Stack
Splunk
Security Event Simulation Logs
SOC Analytics Concepts

##🎯 Learning Outcome
SOC operations understanding
Threat detection logic
Log analysis & correlation
Dashboard design for security monitoring

##👨‍💻 Author

Built by: Samuel Kato
Web & Cybersecurity Enthusiast
