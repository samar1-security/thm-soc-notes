# SOC Workbooks & Lookups

## Assets & Identities

### Identity Inventory
Catalogue of corporate employees, services, and their details.

**Sources:**
- **Active Directory (AD)** - Primary identity database
- **SSO Providers** - Okta, Google Workspace (cloud alternatives)
- **HR Systems** - BambooHR, SAP, HiBob (employee data only)
- **Custom Solutions** - CSV/Excel sheets (common for IT/security teams)

### Asset Inventory
List of all computing resources (servers, workstations, hardware).

**Sources:**
- **Active Directory** - Also serves as asset database
- **SIEM/EDR** - Collect host information from monitored agents
- **MDM Solutions** - MS Intune, Jamf (dedicated asset management)
- **Custom Solutions** - CSV/Excel sheets

## Network Diagrams

Essential for investigating suspicious activity.

**What to check:**
- Suspicious IPs (especially internal IPs on unusual ports)
- Services running on port numbers
- What subnet the IP belongs to
- Why would it connect to other subnets
- Possible causes: brute force, IP spoofing, CVE breach

## SOC Workbooks (Playbooks/Runbooks)

**Definition:** Structured document defining steps to investigate & remediate specific threats consistently.

**Purpose:**
- Support L1 analysts (junior specialists)
- Ensure all analysis steps followed in correct order
- Eliminate verdicts made without sufficient evidence
- Streamline alert triage process

**Typical Workbook Structure:**

1. **Enrichment** - Use Threat Intelligence & identity inventory to gather user information
2. **Investigation** - Analyze SIEM logs to make verdict on activity
3. **Escalation** - Escalate to L2 or communicate with user if necessary

**Format:**
- Detailed textual guide
- Flowchart diagrams
- Links to resources
- Step-by-step procedures

## Key Takeaway

Following workbooks in correct order guarantees high-quality alert triage and evidence-based verdicts.
