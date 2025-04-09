# Blue Team Tools

## 🛡️ Purpose of This Folder

This folder is dedicated to blue team activities and provides tools, configurations, and scripts to help **defend** against security threats. Blue teams focus on the **detection, prevention, and response** to security incidents and actively work to improve the security posture of an organization.

**Blue team responsibilities:**
- Monitoring and analyzing security events
- Setting up and managing Security Information and Event Management (SIEM) systems
- Writing and maintaining detection rules (Sigma/Snort)
- Analyzing network traffic (packet analysis)
- Parsing and investigating system logs
- Responding to detected incidents and escalating threats

This repository contains:
- **SIEM Splunk Rules**: Pre-configured detection rules and configurations for Splunk.
- **Sigma/Snort Rules**: Custom rules to detect attacks and suspicious activity.
- **Packet Analysis**: Tools for capturing and analyzing network traffic.
- **Log Parsing**: Scripts to parse various log files for indicators of compromise.

## 📚 Folder Contents:

1. **SIEM Setup (Splunk)**: Configuration files and rules for setting up a SIEM system using Splunk.
2. **Sigma/Snort Rules**: Detection rules for various attacks and security threats.
3. **Packet Analysis**: Scripts for packet capture and analysis to detect malicious network activity.
4. **Log Parsing**: Tools to parse and search through logs for security-related events.
5. **Others**: Additional utilities and information related to blue team activities.

---

## 📥 Getting Started

### 1. **SIEM Setup (Splunk)**:
- The **Splunk** folder contains configuration files and search queries for setting up Splunk to monitor security events.
- Import the provided search queries and dashboards into Splunk to detect common security issues such as failed logins, privilege escalation, and more.

### 2. **Sigma/Snort Rules**:
- The **Sigma/Snort** folder contains detection rules that can be implemented in SIEM tools or network IDS/IPS systems.
- These rules are tailored for detecting common attack patterns, such as SQL injection, buffer overflows, and privilege escalation.

### 3. **Packet Analysis**:
- **Packet capture scripts** help to capture network traffic and analyze for suspicious activity.
- Use the provided **pcap_parser.py** script to extract key details from `.pcap` files and detect anomalies.

### 4. **Log Parsing**:
- **Log parsing scripts** help identify security incidents in system logs, web server logs, authentication logs, etc.
- These tools can parse logs for keywords, failed login attempts, or unauthorized access attempts.

---

## 🔧 Prerequisites:

- **Splunk** for SIEM monitoring.
- **Snort** or **Sigma** compatible SIEM tool (e.g., Elastic Stack).
- **Wireshark/tcpdump** for packet analysis.
- **Python 3.x** for running the scripts.
- **Required Python packages**: `requests`, `pyyaml`, `scapy`.

---

## 🔎 What You’ll Find in This Repo

### 1. **SIEM Setup (Splunk)**:
   - **splunk_config/**: Configuration files for setting up Splunk for security log monitoring.
   - **splunk_queries/**: Search queries for detecting security events in Splunk.
   - **splunk_dashboards/**: Dashboards for visualizing security incidents in Splunk.

### 2. **Sigma/Snort Rules**:
   - **sigma_rules/**: Sigma rule definitions for detecting specific security events.
   - **snort_rules/**: Snort IDS/IPS rules for detecting network attacks.

### 3. **Packet Analysis**:
   - **packet_capture.py**: Python script to capture network packets in real-time.
   - **pcap_parser.py**: Script for analyzing `.pcap` files and detecting anomalies.

### 4. **Log Parsing**:
   - **syslog_parser.py**: Script to parse syslog logs for potential security threats.
   - **apache_log_parser.py**: Script to parse Apache access logs for suspicious web activity.

---

## 🧰 How to Use:

### 1. **SIEM Setup (Splunk)**:
- Import the configuration files and search queries into **Splunk** to monitor logs from your systems.
- Customize the **Splunk queries** based on your network environment and log sources.
- Use the **Splunk dashboards** to visualize security events like failed logins, unusual network traffic, and more.

### 2. **Sigma/Snort Rules**:
- Copy the **Sigma rules** to your **SIEM system** or use them with **Sigma-compatible log processing tools**.
- For **Snort IDS/IPS**, import the **Snort rules** into your Snort configuration and enable them to detect various attack types.

### 3. **Packet Analysis**:
- Run **packet_capture.py** to capture network traffic on your network.
- Use **pcap_parser.py** to analyze network traffic dumps for potential signs of compromise.

### 4. **Log Parsing**:
- Customize the **log parsing scripts** to read specific log files from your environment (e.g., `/var/log/auth.log` for Linux or Apache access logs).
- Monitor for suspicious events such as failed login attempts or unusual activity patterns.

---

## 🔒 Additional Resources:
- [Splunk Documentation](https://docs.splunk.com)
- [Sigma Rule Format](https://github.com/Neo23x0/sigma)
- [Snort IDS](https://www.snort.org)
- [Wireshark](https://www.wireshark.org)

