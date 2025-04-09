# Splunk Dashboards

## Purpose:
This folder contains pre-configured **Splunk dashboards** that visualize security events and incidents. These dashboards are useful for monitoring security logs in real-time and gaining insights into potential security threats.

## Files:

### 1. **failed_logins_dashboard.xml**
This dashboard visualizes failed login attempts across different systems, users, and source IPs.
- **Description**: Displays a bar chart of failed login attempts, highlighting top offenders (user, host, IP).
- **Usage**: Helps monitor for brute force or unauthorized access attempts.

### 2. **suspicious_activities_dashboard.xml**
This dashboard visualizes suspicious activities such as privilege escalation and unusual user behaviors.
- **Description**: Shows alerts and visualizations of abnormal user actions and access attempts.
- **Usage**: Aids in detecting suspicious behaviors, such as attempts to gain unauthorized access to critical systems.

### 3. **brute_force_detection_dashboard.xml**
This dashboard provides a visual representation of potential brute force attempts by tracking failed login attempts across different systems.
- **Description**: A heatmap of failed logins by user or source IP, with additional alerts for excessive login attempts.
- **Usage**: Ideal for detecting brute force attacks and tracking repeated login failures.

## How to Use:
1. Navigate to **Settings** > **User Interface** > **Dashboards** in Splunk.
2. Import the XML dashboard files into Splunk.
3. Customize the dashboards as necessary to suit your environment (e.g., log source, index).
4. Use the dashboards to monitor for security events in real-time.

## Requirements:
- **Splunk Enterprise** installed.
- **Security Event Logs** (e.g., syslog, authentication logs) indexed in Splunk.
- **Splunk Dashboarding** feature enabled.
