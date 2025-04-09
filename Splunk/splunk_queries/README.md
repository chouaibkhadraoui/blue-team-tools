# Splunk Search Queries

## Purpose:
This folder contains a set of **Splunk search queries** that are designed to detect common security incidents. These queries can be used to identify suspicious activities, such as unauthorized access attempts, failed logins, privilege escalation, and brute force attacks.

## Files:

### 1. **failed_logins.splunk**
Detects failed login attempts from system logs (e.g., `/var/log/auth.log`).
- **Description**: Finds occurrences of failed login attempts by searching for "failed password" in the syslog.
- **Usage**: Can be used to monitor for brute-force login attempts.

### 2. **suspicious_activity.splunk**
Detects suspicious activities, such as privilege escalation or unusual user actions.
- **Description**: Searches for anomalies like users executing high-privilege commands or accessing sensitive resources.
- **Usage**: Helps detect potential privilege escalation attempts.

### 3. **brute_force_attempts.splunk**
Detects potential brute force attacks by monitoring repeated failed login attempts.
- **Description**: Flags accounts/IPs with a high number of failed login attempts.
- **Usage**: Use it to monitor systems for brute force attacks or credential stuffing.

## How to Use:
1. Open Splunk's **Search & Reporting** app.
2. Paste the query into the search bar.
3. Modify the queries as necessary for your environment (e.g., change the log source, index name).
4. Save the queries as **Saved Searches** and schedule them to run at regular intervals.

## Requirements:
- **Splunk Search & Reporting** app.
- **Security Event Logs** (e.g., syslog, authentication logs) indexed in Splunk.
