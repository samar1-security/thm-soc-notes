# Blue Team Introduction

## L1 Analyst Role
Junior security analyst is first line of defense. Monitor alerts, investigate threats, protect company from breaches.

### Daily Duties
- Monitor and investigate security alerts
- Participate in team brainstorms
- Cooperate with other teams
- Constantly learn new attacks/defenses

## SOC Team (4 Core Roles)
- **L1 Analyst:** Triage alerts, escalate complex cases
- **L2 Analyst:** Investigate advanced attacks
- **SOC Engineer:** Configure security tools
- **SOC Manager:** Oversee team, report to leadership

## Career Paths from L1
- → L2 Analyst (most common)
- → SOC Engineer
- → CIRT (incident response)
- → Manager → CISO

## Internal vs MSSP
- **Internal:** Calm shifts, few tools, deep expertise
- **MSSP:** High pressure, diverse tools, fast learning

---

# Humans as Attack Vectors

## Why Humans Are Targeted
Humans are the weakest link in cyber security. Threat actors target them because:
- Access to systems, emails, databases
- Can be manipulated to help attackers unknowingly
- Often easier than exploiting technical vulnerabilities

### Common Human-Targeted Attacks

**Social Engineering**
Manipulates victims by exploiting psychology:
- Trustworthy appearance (looks legitimate)
- Emotional triggers (urgency, fear, curiosity)

**Phishing**
- Fake emails appearing legitimate
- Trick users into clicking malicious links or entering credentials
- 3.4 billion malicious emails sent daily

**Malware Downloads**
- Fake software or infected downloads
- Techniques: fake CAPTCHAs, malicious QR codes, SEO poisoning

**Deepfakes**
- AI-generated video/audio impersonation
- Example: $25 million wire fraud via deepfake video call

**Impersonation**
- Attackers pretend to be IT, boss, or colleagues
- Phone calls requesting account takeovers for "system repairs"

**Other Attacks**
- USB drop campaigns, physical attacks, insider threats, fake job offers

## Defending Against Human Attacks

### Mitigation (Prevention)
- **Anti-phishing solution** - Blocks malicious emails before users see them
- **Antivirus/Antimalware** - Prevents malware execution
- **Security awareness training** - Teach employees to detect attacks
- **"Trust but verify" principle** - Verify suspicious requests, detect deepfakes

### Detection
SOC analysts detect attacks that slip past mitigation measures.

---

# Systems as Attack Vectors

## What Are Systems?
Physical servers, virtual machines, or cloud platforms that store critical data:
- Banks store card data
- Companies store emails
- Governments host websites

**Why Systems Matter:**
Breaching one system = compromising thousands of users/records

## How Systems Are Attacked

### 1. Human-Led Attacks
- Malicious USB insertion
- Downloading malware
- Reusing weak passwords (81% of breaches involve stolen passwords)

### 2. Vulnerabilities
- Every software has security flaws
- 40,000+ CVEs published in 2024
- Zero-day: vulnerability unknown to vendor, only attacker knows

**Responding to Vulnerabilities:**
- Apply patches/updates immediately
- Restrict access to vulnerable systems
- Apply temporary mitigations from vendor
- Block known attack patterns

### 3. Supply Chain Attacks
- Threat actors breach apps/libraries and push malicious updates
- All users of that app/library get compromised
- Famous examples: SolarWinds, 3CX breaches
- Hard to detect since you don't control all software

### 4. Misconfigurations
- IT team sets up systems insecurely
- Examples:
  - Weak passwords ("123456", "1111")
  - Unrestricted access permissions
  - Exposed databases
  - Poorly configured firewalls

**Real Examples:**
- McDonald's: "123456" password exposed 64 million job applications
- Capital One: Misconfigured firewall led to 106 million customer breach
- Smart fridges: Improperly configured, used in botnet attacks

**Responding to Misconfigurations:**
- Penetration testing (hire ethical hackers)
- Vulnerability scans (find default passwords, outdated software)
- Configuration audits (review against CIS benchmarks)

## Defending Systems

### Mitigation (Prevention)
- **Patch Management** - Track and patch vulnerable systems regularly
- **IT Training** - Teach IT team about misconfiguration risks
- **Network Protection** - Restrict access to trusted users/IP addresses
- **Antivirus Protection** - Detect and block malware

### Detection
SOC analysts detect attacks that bypass mitigation.

## Key Principle
Attackers use both human and system vulnerabilities. Protect both equally:
- Combine Mitigation (prevention) + Detection (response)
- Can't train systems like humans, but train IT department to configure securely

---

# Summary

**L1 Analyst Role:**
- First line of defense
- Monitor alerts, investigate threats
- Advance to L2, engineer, CIRT, or manager roles

**Attack Vectors:**
- Humans: Social engineering, phishing, malware, deepfakes, impersonation
- Systems: Vulnerabilities, misconfigurations, supply chain attacks

**Your Job:**
- Detect attacks that bypass mitigation
- Investigate and respond to incidents
- Recommend security improvements

**Career Path:**
Gain 1-2 years experience as L1 → Specialize in your chosen field
