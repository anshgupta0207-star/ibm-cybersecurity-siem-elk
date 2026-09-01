# SIEM Dashboard Implementation Using ELK Stack (IBM PBEL Internship)

## 📌 Project Overview
This project implements a lightweight Security Information and Event Management (SIEM) pipeline in Kali Linux using the ELK Stack (Elasticsearch, Logstash, Kibana) and Filebeat. The system captures system authentication events, monitors SSH/sudo failures, and visualizes security threats in real-time.

## 🏗️ Architecture & Data Flow
`Kali Linux Logs (/var/log/auth.log)` ➡️ `Filebeat` ➡️ `Elasticsearch` ➡️ `Kibana Dashboard`

## ⚙️ Components Used
* **Elasticsearch (v8.x):** Search and analytics database engine.
* **Filebeat:** Lightweight log shipper for system security events.
* **Kibana (v8.x):** Security Operations Center (SOC) dashboard UI.

## 🚨 Security Use Cases & Detections
1. **SSH Brute-Force Monitoring:** Tracking high-frequency failed authentication events (`event.outcome: failure`).
2. **Privilege Escalation Tracking:** Monitoring unauthorized `sudo` executions.
3. **User Activity Audit:** Visualizing top target accounts and authentication sources.

## 📊 Dashboard Preview
*(Include your screenshots here in the `/screenshots` folder)*

## 🚀 Reproduction Steps
1. Clone this repository.
2. Enable Filebeat system module: `sudo filebeat modules enable system`
3. Load Kibana assets: `sudo filebeat setup -e`
4. Access dashboard at `http://localhost:5601`.
5.
