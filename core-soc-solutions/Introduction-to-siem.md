# Introduction to SIEM (Security Information and Event Management)

## What is SIEM?

Security Information and Event Management (SIEM) is a core security solution that SOC analysts use in security operations centers.

It collects logs from various sources, standardizes their format, correlates them, and detects malicious activities using detection rules.

---

## The Problem: Logs Everywhere, Answers Nowhere

### Log Sources
Devices continuously generate logs of activities. These log sources are divided into two categories:

#### 1. Host-Centric Log Sources
Capture events that occur within or related to a host.

**Sources:**
- Windows machines
- Linux servers
- Application servers

**Examples of logs:**
- User accessing a file
- User attempting to authenticate
- Process execution
- Application errors

#### 2. Network-Centric Log Sources
Generated when hosts communicate with each other or access the internet.

**Sources:**
- Firewalls
- IDS/IPS
- Routers
- Proxies

**Examples of logs:**
- SSH connections
- File access via FTP
- Web traffic
- VPN access to company resources

### Challenges

Multiple log sources create numerous challenges:
1. **Numerous log sources** - Too many devices generating logs
2. **No centralization** - Logs scattered across different systems
3. **Limited context** - Individual logs don't show full picture
4. **Limited analysis** - Hard to correlate events manually
5. **Format issues** - Each source has different log format

---

## Why SIEM?

SIEM solves these challenges by:

1. **Collecting data** - Gathers logs from all sources
2. **Aggregating data** - Centralizes all logs in one place
3. **Discovering & detecting threats** - Correlates logs to find patterns
4. **Identifying breaches** - Investigates alerts and responds to incidents

---

## Key Features of SIEM

### 1. Centralized Log Collection
- Collects data from all log sources
- Centralizes logs at one location
- Single point for analysis

### 2. Normalization of Logs
- Raw logs are in different formats and sizes
- Windows logs ≠ Linux logs
- SIEM standardizes to consistent format
- Makes analysis and correlation easier

### 3. Correlation of Logs
- Individual logs are not very useful alone
- SIEM correlates logs from different sources
- Finds relationships between logs
- Identifies malicious activity by analyzing patterns

### 4. Real-Time Reporting
- SIEM detects threats based on detection rules
- Many default rules included
- Analysts create custom rules for specific threats
- Immediate alerts on suspicious activity

### 5. Dashboards and Reporting
- Most important SIEM component
- Presents normalized, ingested data for analysis
- Displays actionable insights
- Multiple dashboards for different views

#### Dashboard Information
Typical SIEM dashboards display:
- Alert highlights
- System notifications
- Health alerts
- Failed login attempts
- Events ingested count
- Rules triggered
- Top domains visited

---

## Log Sources and Ingestion

### Windows Machine Logs
- Every event recorded in Event Viewer
- Unique ID assigned to each log type
- Easy to examine and track
- Examples: authentication, process creation, service changes

### Linux Machine Logs
Logs stored in various locations:

- **/var/log/httpd** - HTTP request/response and error logs
- **/var/log/cron** - Cron job events
- **/var/log/auth.log** and **/var/log/secure** - Authentication logs
- **/var/log/kern** - Kernel-related events

### Log Ingestion Methods

How SIEM collects logs from sources:

1. **Agent/Forwarder**
   - Software installed on endpoint
   - Sends logs directly to SIEM
   - Most common method

2. **Syslog**
   - Protocol for sending logs
   - Works across network
   - Standard for many devices

3. **Manual Upload**
   - Administrator uploads log files
   - Less common for continuous monitoring
   - Useful for one-time analysis

4. **Port-Forwarding**
   - Logs forwarded to specific ports
   - Device sends logs to SIEM listening port
   - Simple but less secure

---

## Alert Detection and Analysis

### Detection Rules

SIEM has detection rules that catch threats.

**What are they?**
- Logical expressions set to be triggered
- Catch patterns indicating malicious activity
- Essential for timely threat detection
- Allow analysts to take action quickly

### Alert Investigation Process

**Where analysts spend their time:**
- Monitoring SIEM dashboards
- Dashboards display key network details in summarized form

**Investigation steps:**

1. **Alert triggered**
   - SIEM rule conditions met
   - Alert generated

2. **Examine events/flows**
   - Review events associated with alert
   - Check which rule conditions were met

3. **Determine alert type**
   - **False Positive** - Normal activity flagged incorrectly
   - **True Positive** - Actual malicious activity

4. **Actions based on findings**

#### If False Positive
- Rule may need tuning
- Adjust rule to avoid similar false positives
- Improve detection accuracy

#### If True Positive
- Perform further investigation
- Contact asset owner about activity
- Confirm suspicious activity
- **Isolate infected host** (contain threat)
- **Block suspicious IP** (prevent re-entry)

---

## SIEM Workflow Summary
Log Sources
↓
Ingestion (Agent/Syslog/Manual/Port-forward)
↓
Centralized Collection
↓
Normalization (standardize format)
↓
Correlation (relate events)
↓
Detection Rules Applied
↓
Alert Generated
↓
SOC Analyst Investigation
↓
True Positive → Respond (isolate, block, investigate)
False Positive → Tune Rules

---

## Key Takeaways

- SIEM centralizes logs from multiple sources
- Normalizes different log formats into consistent format
- Correlates logs to identify patterns
- Uses detection rules to automatically find threats
- Provides dashboards for analyst monitoring
- Enables quick response to true positives
- Requires continuous rule tuning for accuracy
