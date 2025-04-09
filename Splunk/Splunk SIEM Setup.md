# Splunk SIEM Setup

This repository contains configuration files and queries to help you set up **Splunk** as a Security Information and Event Management (SIEM) system. Splunk is a powerful platform for searching, monitoring, and analyzing machine-generated data.

---

## Key Components:
- **Splunk Configuration Files**: Setup files for monitoring and parsing security logs.
- **Splunk Queries**: Pre-built search queries for detecting security events.
- **Splunk Dashboards**: Visualizations to monitor security incidents.

---

## Setup Instructions

# 1. Install Splunk

Follow the steps to install Splunk on your machine:
- **Splunk Download**: [Splunk Download](https://www.splunk.com/en_us/download.html)

Extract and install:

```bash
sudo tar -xvf splunk-<version>.tgz -C /opt
sudo /opt/splunk/bin/splunk start --accept-license
```

Access the Splunk UI: http://localhost:8000

## 2. Configure Splunk
Place the following configuration files in the /opt/splunk/etc/system/local/ directory:

- inputs.conf: Log files to monitor.
- props.conf: How Splunk parses the incoming logs.
- transforms.conf: Apply field extraction and masking.


After adding the files, restart Splunk:
```bash
sudo /opt/splunk/bin/splunk restart
```

## Folder Structure

### `splunk_config/`
Contains Splunk configuration files for setting up log monitoring:
- **inputs.conf**: Defines which logs to monitor.
- **props.conf**: Specifies how Splunk parses the logs.
- **transforms.conf**: Transforms data like extracting fields and masking sensitive info.

### `splunk_queries/`
Pre-built Splunk search queries to detect security events:
- **failed_logins.splunk**: Detect failed login attempts.
- **suspicious_activity.splunk**: Detect suspicious user activities.
- **brute_force_attempts.splunk**: Identify potential brute-force attacks.

### `splunk_dashboards/`
Splunk dashboards for visualizing security events:
- **failed_logins_dashboard.xml**: Shows failed login attempts.
- **suspicious_activities_dashboard.xml**: Shows suspicious activities.
- **brute_force_detection_dashboard.xml**: Displays brute-force attack data.

## Example Queries

### 1. Failed Login Detection:
```splunk
index=syslog sourcetype=syslog "failed password"
```
## 2. Suspicious User Activity:
```splunk
index=syslog sourcetype=syslog "sudo" OR "privilege escalation"
```
## 3. Brute Force Detection:
```splunk
index=syslog sourcetype=syslog "authentication failure" | stats count by src_ip
```

## References
Splunk Documentation

Splunk Security Essentials
