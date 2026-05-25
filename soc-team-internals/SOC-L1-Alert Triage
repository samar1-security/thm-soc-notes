# SOC Team Internals - L1 Alert Triage

## Overview
An alert is a core concept for any SOC team. Knowing how to handle it properly ultimately decides whether a security breach is detected and prevented, or missed and devastating.

## Learning Objectives
- Familiarize with concept of SOC alert
- Explore alert fields, statuses, and classification
- Learn how to perform alert triage as an L1 analyst
- Practice with real alerts and SOC workflows

---

## From Events to Alerts

**Event Flow:**
1. Event occurs (user login, process launch, file download, etc.)
2. System logs the event (OS, firewall, cloud provider)
3. Event logs shipped to security solution (SIEM or EDR)
4. **Alert** generated when specific event/sequence occurs

**Challenge:** SOC teams receive millions of logs daily from thousands of systems. Most are expected, some require attention. Alerts highlight suspicious/anomalous events.

### Security Platforms

**SIEM Systems:**
- Splunk ES - Very solid capabilities
- Perfect choice for most SOC teams

**EDR/NDR:**
- MS Defender, CrowdStrike
- Provide their own alert dashboards

**SOAR Systems:**
- Splunk, Cortex SOAR
- Bigger SOC teams use to aggregate/centralize alerts from multiple solutions

**ITSM Systems:**
- Jira, TheHive
- Custom ticket management setups

---

## L1 Role in Alert Triage

**SOC L1** (First Line of Defense):
- Review alerts
- Distinguish bad or good
- Notify L2 in case of threat
- May receive 1-100 alerts per shift
- Each alert can reveal a cyberattack

**Full Team Involvement:**
- **L1 Analyst:** Review, classify, escalate
- **L2 Analyst:** Deep analysis and remediation
- **SOC Engineer:** Ensure alerts contain enough info for efficient triage
- **SOC Manager:** Track speed and quality to prevent missed attacks

---

## Alert Properties

**Alert Time**
- Shows creation time
- Triggers a few minutes after actual event
- Example: March 21, 15:35

**Alert Name**
- Summary of what happened
- Based on detection rule's name
- Examples: Unusual login location, Email marked as phishing, Windows RDP brute force, Potential data exfiltration

**Alert Severity**
- Defines urgency
- Set by detection engineers
- Can be altered by analysts if needed
- Levels: Low/Informational, Medium/Moderate, High/Severe, Critical/Urgent

**Alert Status**
- Informs if someone is working on alert or if triage is done
- States: New/Unassigned, In Progress/Pending, Closed/Resolved

**Alert Verdict**
- Also known as alert classification
- Explains if alert is real threat or noise
- Verdicts: True Positive (real threat), False Positive (no threat)

**Alert Assignee**
- Shows analyst assigned to review alert
- Sometimes called alert owner
- Can self-assign

**Alert Description**
- Explains what alert is about
- Usually three sections:
  1. Logic of alert generating rule
  2. Why activity indicates an attack
  3. How to triage this alert (optional)

**Alert Fields**
- Provide analyst comments and trigger values
- Examples: Affected hostname, entered cmdline, etc.

---

## Alert Prioritization

**Definition:** Process of deciding which alert to work on first. Crucial for timely threat detection, especially with many alerts in queue.

### Picking the Right Alert

Every team decides its own prioritization rules, usually automated in SIEM/EDR.

**Approaches:**

**1. Filter the Alerts**
- Don't take alerts already reviewed by other analysts
- Skip alerts already being investigated
- Only take new, unseen, unresolved alerts

**2. Sort by Severity**
- Start with critical alerts
- Then high, medium, finally low
- Detection engineers design rules so critical = much more likely real threats
- Critical alerts cause more impact than medium/low

**3. Sort by Time**
- Start with oldest alerts, end with newest
- If multiple breaches: older breach hacker likely dumping data already
- Newer breach attacker just started discovery phase

---

## Practical Exercise

Investigated alerts in TryHackMe SIEM tool:
- Assigned myself as alert owner
- Made comments regarding severity
- Closed alerts for critical, high, and low severity levels
- Completed triage workflow for each alert type

---

## Key Takeaway

Alert triage is the foundation of SOC work. L1 analysts must efficiently prioritize and classify alerts to ensure real threats aren't missed while avoiding alert fatigue from false positives.
