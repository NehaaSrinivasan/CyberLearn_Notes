
# Room 4: Systems as Attack Vectors

**Module:** Blue Team Introduction
**Path:** SOC L1
**Platform:** TryHackMe

---

## What This Room Covers

Even when humans are security-aware, weak systems can still be exploited by threat actors. This room covers the two main system weaknesses, how to prevent them, common attack types targeting systems, and a hands-on remediation exercise.

---

## Two Main System Weaknesses

| Weakness | Definition |
|----------|-----------|
| **Vulnerabilities** | Loopholes or weak points in a system that attackers exploit to gain access — these are bugs or flaws in software/hardware |
| **Misconfigurations** | Mistakes made while setting up or configuring systems — not a bug, but a human error in setup |

> Key distinction: Vulnerabilities are flaws in the system itself. Misconfigurations are mistakes made by the people setting it up.

---

## Preventing Vulnerabilities

| Measure | How it helps |
|---------|-------------|
| **Restrict access to trusted IDs** | Limits who can interact with sensitive systems |
| **Block known attack patterns** | Prevents recognised exploit attempts from succeeding |
| **Regular patching** | Apply vendor-released patches to fix known vulnerabilities as soon as they are available |

---

## Preventing Misconfigurations

| Measure | How it helps |
|---------|-------------|
| **Penetration testing** | Simulates real attacks to find misconfigurations before attackers do |
| **Vulnerability scanning** | Automated scanning to identify weaknesses across systems |
| **CIS Benchmark / Configuration audit** | Industry-standard guidelines to ensure systems are configured securely |

> New concept encountered: CIS Benchmark — a set of globally recognised best practice guidelines for securely configuring systems. Was not aware of this before this room.

---

## Common Attack Types on Systems

- **Vulnerability exploitation** — attackers identify and exploit known CVEs to gain access
- **Supply chain attacks** — malicious code introduced through a third-party application or update
- **Human-led attacks** — attackers leverage human error or weak credentials to compromise systems

---

## Hands-On Activity — 4 Scenarios

### Scenario 1 — CVE Exploitation
What happened: Penetration testing identified a CVE. The vulnerability was publicly known, meaning anyone could exploit it to breach the system.
Solution: Request IT to patch and update the affected system immediately.

### Scenario 2 — Brute Force Attack
What happened: Threat actors brute-forced the admin account, gained access, and replaced a webpage with malicious links.
Solution: Change the admin password to a stronger, more secure one and enforce a secure password policy.

### Scenario 3 — Outdated Firewall
What happened: A neighbouring company was hit by a cyberattack due to an old firewall vulnerability. Our organisation uses the same firewall model.
Solution: Update the firewall with the latest patch and verify there are no active CVEs against it.

### Scenario 4 — Supply Chain Attack
What happened: Malicious activity was detected originating from a third-party designed application after a recent update.
Solution: Identified as a supply chain attack — isolate the application and investigate the third-party vendor's update.

---

## Remediation Plan

| Control | Purpose |
|---------|---------|
| **Antivirus** | Detect and remove malware across all assets |
| **Patch management** | Keep all systems up to date with latest security patches |
| **Secure password policy** | Prevent brute force and credential-based attacks |
| **Security awareness training** | Ensure staff understand their role in keeping systems secure |

---

## Key Takeaway

Systems are just as exploitable as humans — and often more dangerous because vulnerabilities and misconfigurations can sit undetected for long periods. A resilient organisation patches regularly, audits configurations against standards like CIS Benchmark, and tests its own defences through penetration testing before attackers find the gaps.

---

*Part of the Blue Team Introduction Module — TryHackMe SOC L1 Path*
