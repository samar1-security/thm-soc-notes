# Introduction to EDR (Endpoint Detection and Response)

## What is EDR?

Endpoint Detection and Response (EDR) is a security solution designed to monitor, detect, and respond to advanced threats at the endpoint level.

### Why EDR?

With Remote Work adoption, endpoints are now outside network perimeter protection. EDR provides:
- Deep-level protection for endpoints
- Constant monitoring regardless of location
- Detection and response to advanced threats

### EDR Solutions in Market
- CrowdStrike Falcon
- SentinelOne ActiveEDR
- Microsoft Defender for Endpoint
- Open EDR
- Symantec EDR

---

## Three Pillars of EDR

### 1. Visibility
Provides impressive level of visibility into endpoint activity.

**Collected Data:**
- Process modifications
- Registry modifications
- File and folder modifications
- User actions
- Complete process tree
- Activity timeline
- Historical data for threat hunting

**Advantage:** Any detection arrives with full context.

### 2. Detection
Goes beyond traditional antivirus signature-based detection.

**Detection Techniques:**
- Signature-based detection
- Behavior-based detection (unexpected user activities)
- Machine learning baseline deviation detection
- Fileless malware detection (in-memory)
- Custom IOC feeds for threat detection

### 3. Response
Empowers analysts to take action on detected threats from central EDR console.

---

## EDR vs Antivirus

Both aim to protect endpoints but differ in:
- **Level of protection:** EDR provides deeper protection
- **Detection capabilities:** EDR includes behavioral and ML-based detection
- **Response capabilities:** EDR offers advanced response options
- **Visibility:** EDR provides detailed telemetry and context

---

## How EDR Works

### Agents (Sensors)
- Deployed on each endpoint
- Eyes and ears of EDR
- Monitor all endpoint activities
- Collect detailed telemetry

### EDR Console
- Centralized management platform
- Correlates data from all agents
- Applies complex logic and ML algorithms
- Matches threat intelligence
- Generates alerts from collected data

### Alert Process

1. Agent collects endpoint activity
2. Data sent to EDR console
3. Console analyzes with ML algorithms
4. Threat intelligence matched against data
5. Alert generated with severity level
6. SOC analyst reviews and prioritizes
7. Investigation and response taken

---

## EDR Telemetry

### What is Telemetry?
Telemetry = "black box" of endpoint with everything needed for detection and investigation.

### Collected Telemetry

**Process Executions & Terminations**
- Tracks all running/idle processes
- Identifies suspicious parent-child process relations
- Detects malware, payloads, suspicious executables

**Network Connections**
- Monitors all endpoint network connections
- Identifies C2 server connections
- Detects unusual port usage
- Flags data exfiltration attempts
- Detects lateral movement within network

**Command Line Activity**
- Captures all commands in CMD, PowerShell, etc.
- Identifies malicious command execution
- Catches obfuscated PowerShell scripts (missed by traditional AV)

**File & Folder Modifications**
- Tracks modifications during data staging
- Monitors ransomware executions
- Logs malicious file dropping
- Important for forensic investigation

**Registry Modifications**
- Registry is goldmine of Windows configuration info
- EDR monitors modifications occurring during malicious activity
- Helps identify persistence mechanisms

### Advanced Analysis
EDR uses complex logic and ML to assess activities. Advanced threats:
- Keep activities stealthy
- Use legitimate utilities
- May appear harmless individually
- Tell different story when viewed through detailed telemetry

**Benefit:** Detailed telemetry helps analysts understand full attack chain, identify root cause, and reconstruct attack timeline.

---

## Detection Capabilities

### Behavioral Detection
- Observes complete behavior of files/processes
- Catches legitimate processes abused for attacks
- Detects advanced threats that look clean

### Anomaly Detection
- EDR understands baseline endpoint behavior
- Flags any activity deviating from baseline
- Malicious activity causes behavior deviation
- Note: Can generate false positives (analyst uses context to verify)

### IOC Matching
- Strong threat intelligence field integrations
- Matches activities against known IOCs
- Effective except for zero-day attacks
- Flags matching activities

### MITRE ATT&CK Mapping
- Alerts mapped to MITRE Tactic and Technique
- Shows which attack stage was detected
- Very helpful for analysts understanding attack progression

### Machine Learning Algorithms
- Trained on large datasets of normal and malicious behaviors
- Detects complex attack patterns
- Effective for fileless attacks and multi-staged intrusions
- Catches attacks where individual actions aren't inherently malicious but pattern is malicious

---

## Response Capabilities

### Automated Response
- Teams create policies for known malicious behaviors
- Automatically block or quarantine threats

### Manual Response Options

**Isolate Host**
- Disconnect endpoint from network
- Prevents lateral movement
- Most effective for containing threats early
- Stops attacks from spreading to other endpoints

**Terminate Process**
- Kill malicious process without host isolation
- Useful for critical systems (avoid downtime)
- Neutralizes activity without major disruption
- Requires careful decision-making

**Quarantine Files**
- Move malicious files to isolated location
- Prevents execution
- Analyst can review, restore, or permanently delete
- Protects other endpoints

**Remote Access**
- Analysts access endpoint shell remotely
- Used when built-in EDR response insufficient
- Gain deeper visibility
- Execute custom actions and scripts
- Collect desired data from host

**Artifacts Collection**
- Extract data for forensic investigation or legal action
- Without physically accessing device
- Common artifacts:
  - Memory Dump
  - Event Logs
  - Specific Folder Contents
  - Registry Hives

---

## Key Advantages Over Traditional Antivirus

- Detailed visibility and context
- Advanced detection techniques (behavioral, ML-based)
- Comprehensive response options
- Threat hunting capabilities
- Historical data for investigation
- Real-time threat detection and response
