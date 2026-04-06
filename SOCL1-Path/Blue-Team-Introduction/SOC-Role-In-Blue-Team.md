
# Room 2: SOC Role in Blue Team

**Module:** Blue Team Introduction
**Path:** SOC L1
**Platform:** TryHackMe

---

## What This Room Covers

How the security team fits into a company's overall hierarchy, the different cybersecurity teams and their roles, how SOC works alongside other teams, and the difference between an internal SOC and an MSSP.

---

## Company Security Hierarchy

```
CEO
└── CISO (may also be CTO / CIO depending on organisation)
    ├── SOC Manager
    ├── Red Team Lead
    └── Team Members: SOC Analyst, SOC Engineer, GRC Specialist, Pen Tester
```

**CISO — Chief Information Security Officer**
Acts as the bridge between the CEO and the security team. Since CEOs focus on business and finance rather than technical matters, the CISO translates security risks into business language and ensures leadership understands the security posture.

---

## Cybersecurity Teams Overview

| Team | Focus | Key Roles |
|------|-------|-----------|
| **Blue Team** | Defence — detect, prevent, respond to attacks | SOC Analyst, Incident Responder, Digital Forensics |
| **Red Team** | Offence — authorised attacks to find vulnerabilities | Penetration Tester, Offensive Security Engineer |
| **GRC** | Governance, Risk & Compliance | GRC Specialist |

---

## SOC and CSIRT — How They Work Together

**SOC Team** (L1, L2 Analysts, SOC Engineer, SOC Manager):
- First to identify and contain a security incident
- Operates **24/7**
- If they cannot resolve the incident, they escalate to CSIRT

**CSIRT — Cybersecurity Incident Response Team:**
- Called in for critical or complex incidents
- Does **not** operate 24/7 — activated when needed
- Focuses on hidden threats, critical incident resolution, and deep investigation

| CSIRT Role | Responsibility |
|------------|---------------|
| Threat Intel Expert | Provides intelligence on the attack |
| Threat Hunting Expert | Proactively hunts for hidden threats |
| Malware Analyst | Analyses malicious software involved |
| Forensics Lead | Conducts deep forensic investigation |
| CSIRT Manager | Coordinates the response team |

---

## Other Supporting Teams

| Team | Role |
|------|------|
| **Digital Forensics Analyst** | Investigates incidents and produces detailed evidence-based reports |
| **Threat Intelligence Analyst** | Gathers information on emerging and active threats |
| **AppSec Engineer** | Ensures applications are built securely using best coding practices |
| **AI Security Researcher** | Handles security risks specific to AI systems |

---

## SOC vs MSSP

| | Internal SOC | MSSP (Managed Security Service Provider) |
|--|-------------|------------------------------------------|
| Scope | Handles incidents for their own organisation only | Handles hundreds of incidents across many organisations |
| Experience | Focused but limited variety | Broader exposure to diverse attack types |
| Availability | 24/7 | 24/7 |

> Key insight: MSSPs often have greater experience due to the sheer variety of incidents they handle across multiple clients.

---

## Well-Known CSIRT Teams Worldwide

- **JPCERT** — Japan
- **Mandiant** — Global (threat intelligence and incident response)
- **AWS CIRT** — Amazon Web Services incident response team

---

## Hands-On Activity

Interactive exercise to identify SOC roles and assign their corresponding responsibilities during a simulated security breach scenario.

---

## Key Takeaway

Red, Blue, and GRC teams must all cooperate to strengthen an organisation's overall security posture — no single team works in isolation. The relationship between SOC and CSIRT is particularly important: SOC handles day-to-day monitoring while CSIRT steps in for critical escalations.

---

*Part of the Blue Team Introduction Module — TryHackMe SOC L1 Path*
