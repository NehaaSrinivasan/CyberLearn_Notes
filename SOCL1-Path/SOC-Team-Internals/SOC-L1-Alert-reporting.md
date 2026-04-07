
# Room 2: Alert Reporting

**Module:** SOC Team Internals
**Path:** SOC L1
**Platform:** TryHackMe

---

## What This Room Covers

The importance of reporting, escalation, and communication during and after a security incident. How a Junior SOC Analyst (L1) reports to seniors and escalates alerts through the SOC hierarchy.

---

## The Alert Funnel

```
Security Tools
      |
      v
   L1 Analyst
      |
      v
   L2 Analyst
      |
      v
  DFIR Experts
```

Alerts from security tools are received by L1 first. If further investigation is needed, L2 takes over. For specific major incidents, DFIR (Digital Forensics and Incident Response) experts are called in.

---

## Three Core Responsibilities

### 1. Reporting
- Write a detailed report about the alert
- Use the 5 Ws approach:
  - **Who** — which user caused the incident, compromised user details
  - **What** — what action did that person perform
  - **When** — exact date and time the incident occurred
  - **Where** — exact location, which host, PC, IP address
  - **Why** — what made the person do that activity e.g. a phishing email with an urgent subject line luring them to click a malicious link

### 2. Escalation
- Escalate the alert if it requires further investigation
- In the report, clearly mention the reason for escalation
- When escalating, L2 will only receive the alert — write your notes clearly so they have full context

### 3. Communication
- Communication is key — always use agreed channels
- Communicate with other team members to get insights about the alert
- Never work in isolation

---

## When to Escalate — Alert Escalation Guide

| Situation | Action |
|-----------|--------|
| Major cyberattack indicator | Escalate — requires deeper investigation |
| Password reset / malware removal / host isolation needed | Escalate to L2 |
| Communication needed with customers, partners, management, or law enforcement | Escalate to SOC Manager |
| L1 cannot understand the alert and needs guidance | Escalate to senior for support |

### Escalation Flow Example — Phishing Alert
```
L1 receives phishing alert
      |
      v
L1 → L2 (remind / rotate / reset password, inform affected person)
      |
      v
L2 reviews and receives only the alert from L1
```

---

## Crisis Communication Scenarios

| Scenario | What to do |
|----------|-----------|
| Urgent critical alert — L2 not available within 30 mins | Call or escalate to L3 / Manager directly |
| Slack / Teams accounts are compromised | Do NOT use Slack or Teams — use phone call instead |
| Large number of alerts — need to inform L2 | Inform L2, prioritise oldest to newest, work through them |
| Alert prioritised wrongly after a few days | Inform L2 immediately |
| Cannot complete triage due to SIEM failure | Investigate what happened, inform L2 and SOC Engineer |

---

## Tools Used in Activity

| Tool | Purpose |
|------|---------|
| **VirusTotal** | Check reputation of IP addresses, files and hashes |
| **Have I Been Pwned** | Check if an email address was involved in a known data breach |

---

## Personal Reflection

**On communication:**
Communication is the backbone of a SOC team. If an L1 analyst stays silent on an unknown alert — whether because they assumed it was a false positive or simply didn't understand it — that silence could allow a real attack to go undetected. The root cause investigation after a breach might eventually reveal that someone saw it and said nothing. That is why escalating uncertainty is just as important as escalating confirmed threats.

**On phone calls during a crisis:**
If Slack or Teams are compromised, an attacker inside the network can eavesdrop on all internal communication. Phone calls operate on a completely separate network to the organisation's infrastructure, making them impossible for the attacker to intercept. This is why falling back to phone calls is the right move when internal tools cannot be trusted.

**On VirusTotal and Have I Been Pwned:**
These two tools cover different angles of the same question — is this suspicious? VirusTotal answers that for IPs, files and hashes. Have I Been Pwned answers it for email addresses by checking if they appeared in known data breaches. Together they give an analyst a quick reputation check before going deeper.

---

## Key Takeaway

Reporting, escalation and communication are not optional — they are core duties of a Junior SOC Analyst. Always assign alerts to yourself, change status to In Progress, and follow proper reporting guidelines. Even when tools fail or communication channels are compromised, there is always a fallback — knowing those fallbacks is what separates a prepared analyst from an unprepared one.

---

*Part of the SOC Team Internals Module — TryHackMe SOC L1 Path*
