# SOC L1 Alert Reporting & Escalation

## SOC L1 Alert Workflow

**Alert Reception:**
- L1 receives alerts from SIEM, EDR, or TIP
- False positives → Closed at L1 level
- Complex/threatening → Escalate to L2

## Three Key Terms

### Reporting
- Document investigation before closing or escalating
- Team standards & severity determine detail level
- Required for true positives (TP) needing escalation
- Provides evidence trail and context for L2

### Escalation
- TP requiring additional actions → L2 review
- Alert reports critical for escalation context
- Some SIEM tools have escalation features
- Alternative: Chat/Slack for immediate escalation if SIEM delay

### Communication
- Coordinate with IT, HR, management during investigation
- Follow team crisis communication procedures
- Use appropriate channels (avoid compromised systems)

---

## Alert Report Format (Who, What, When, Where, Why)

**Who** - Which user, source of action (login, command, file download)
**What** - Exact action or event sequence performed
**When** - Timestamp of suspicious activity start
**Where** - Device, IP address, website involved
**Why** - Reasoning for verdict (TP/FP/TP-Benign)

---

## Escalation Guide

### When to Escalate to L2:
- Indicator of major cyberattack requiring deeper investigation/DFIR
- Remediation needed (malware removal, host isolation, password reset)
- Communication required with customers, partners, management, law enforcement
- Alert unclear - need help from senior analyst

### Escalation Methods:
- SIEM escalation feature (primary)
- Chat/Teams message to L2 (if SIEM delay)
- Emergency contacts for critical/urgent alerts

---

## SOC Communication Cases

### Case 1: Urgent/Critical Alert
- Escalate ASAP to available L2
- If L2 unavailable → Use emergency contacts

### Case 2: Compromised Account (Slack/Teams)
- Validate login with affected user
- Do NOT contact through breached channel
- Use alternative: Phone call, email, secure messaging

### Case 3: Alert Overwhelming (Multiple Critical)
- Prioritize by workflow
- Inform L2 of situation
- Keep L2 aware of queue status

### Case 4: Misclassified Alert (Post-Investigation)
- Immediately contact L2 with concerns
- Threat actors can remain silent for weeks before impact
- Re-investigation may be needed

### Case 5: SIEM Logs Not Parsed/Searchable
- Do NOT skip alert
- Investigate what you can
- Report issue to L2 or SOC engineer
- Escalate technical issue for resolution
