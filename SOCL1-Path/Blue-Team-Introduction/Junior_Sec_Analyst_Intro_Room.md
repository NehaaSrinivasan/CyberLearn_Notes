
# Room 1: Junior Security Analyst Intro

**Module:** Blue Team Introduction
**Path:** SOC L1
**Platform:** TryHackMe

---

## What This Room Covers

An introduction to the SOC team structure, the responsibilities of a Junior Security Analyst, and a hands-on activity simulating real analyst work.

---

## SOC Team Hierarchy

| Role | Responsibilities |
|------|-----------------|
| **Junior SOC Analyst (L1)** | Monitors alerts 24/7, first point of contact, collects initial information, writes incident reports |
| **Senior SOC Analyst (L2)** | Investigates incidents based on L1 reports, mentors junior analysts when stuck |
| **SOC Engineer** | Configures and maintains security tools so alerts trigger correctly |
| **SOC Manager** | Manages overall SOC operations, reports to senior management |
| **Incident Responder** | Called in for major incidents — works separately from the core SOC team |

**Typical escalation flow:**
Junior Analyst → Senior Analyst → SOC Engineer → SOC Manager → Incident Responder

> Note: This flow varies by organisation.

---

## Junior Analyst — Day to Day Responsibilities

- Monitor security alerts continuously (24/7 coverage)
- Act as the first point of contact for potential incidents
- Collaborate with other teams to maintain company security
- Participate in SOC workshops and brainstorming sessions
- Stay up to date with the current threat landscape

---

## Hands-On Activity

Simulated a Junior SOC Analyst role using an interactive SIEM dashboard:

- Reviewed multiple security events in the dashboard
- Identified IP addresses linked to malicious activity
- Blocked suspicious IPs using firewall rules

### New Tools Introduced

| Tool | Purpose |
|------|---------|
| **AbuseIPDB** | Open-source platform to check the reputation and history of an IP address |
| **Cisco Talos** | Threat intelligence platform to investigate IP location and malicious activity |

---

## Key Takeaway

A clear picture of how a SOC team is structured and how incidents flow upward from a Junior Analyst to senior roles. The SIEM activity made the L1 role feel practical and realistic — not just theory.

---

*Part of the Blue Team Introduction Module — TryHackMe SOC L1 Path*
