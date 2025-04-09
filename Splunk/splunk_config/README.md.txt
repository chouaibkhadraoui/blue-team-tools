# Splunk Configuration Files

## Purpose:
This folder contains **configuration files** for setting up **Splunk** to monitor and parse security logs. These configuration files are essential for defining how Splunk will interact with the log sources and how it should parse incoming data for security events.

## Files:

### 1. **inputs.conf**
This file defines which log files Splunk will monitor for security events (e.g., syslog, application logs, Windows event logs).
- **Example**: Monitors **/var/log/auth.log** for failed login attempts.

### 2. **props.conf**
This file specifies how Splunk should handle incoming log data. It defines the sourcetype, how to break events into separate lines, and any timestamp extraction.
- **Example**: Defines `syslog` sourcetype for syslog log data.

### 3. **transforms.conf**
This file allows you to apply transformations to data. It’s used for field extraction, renaming fields, or filtering events.
- **Example**: Extracting additional fields from security logs or masking sensitive information.

## How to Use:
1. Place these files in your Splunk configuration directory (typically located in `$SPLUNK_HOME/etc/system/local/`).
2. Modify the configurations as necessary to suit your log sources (e.g., log file paths, sourcetype, etc.).
3. Restart Splunk to apply the configurations.

## Requirements:
- **Splunk Enterprise** or **Splunk Universal Forwarder** installed.
- Proper permissions to access log files.
