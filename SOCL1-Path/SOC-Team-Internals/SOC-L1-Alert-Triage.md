
# Room 1: SOC Alert Triage

**Module:** SOC Team Internals
**Path:** SOC L1
**Platform:** TryHackMe

---

## What This Room Covers

An overview of what alerts and events are, how to prioritise them, the fields present in an alert dashboard, and the full alert triage workflow — practised through an interactive dashboard provided by TryHackMe.

---

## Events vs Alerts

| Term | Definition |
|------|-----------|
| **Event** | Any process or activity that happens in a system or network — e.g. a login, a file access, a network connection |
| **Alert** | An event that matches a specific detection rule or criteria configured in a security tool — it becomes a notification requiring attention |

> Key insight: There will always be far more events than alerts. Security tools filter events and only raise alerts when something meets a suspicious threshold.

---

## Security Tools Discussed

| Tool | Purpose |
|------|---------|
| **SIEM** | Security Information and Event Management — collects and correlates logs from across the environment |
| **EDR** | Endpoint Detection and Response — monitors endpoints for suspicious activity |
| **SOAR** | Security Orchestration, Automation and Response — automates repetitive response tasks |
| **ITSM** | IT Service Management — used for ticketing and tracking incidents |

---

## Alert Dashboard Fields

Every alert in the dashboard contains the following fields:

| Field | Purpose |
|-------|---------|
| **Name** | Title of the alert |
| **Date and Time** | When the alert was triggered |
| **Description** | Summary of what was detected |
| **Alert Severity** | How critical the alert is (High / Medium / Low) |
| **Status** | Current state — e.g. New, In Progress, Closed |
| **Verdict** | True Positive or False Positive |
| **Assignee** | Which analyst the alert is assigned to |
| **Notes** | Analyst findings and comments |

---

## How to Prioritise Alerts

1. **Filter by assignee** — only work on alerts assigned to you
2. **Sort by severity** — work high to low (Critical → High → Medium → Low)
3. **Sort by time** — within the same severity, work oldest to newest

---

## Alert Triage Workflow

The triage process is divided into three stages:

### Stage 1 — Initial Actions
- Assign the alert to yourself
- Change status to **In Progress**
- Note down basic details of the alert

### Stage 2 — Investigation
- Use a **playbook or workbook** to guide your investigation
- Follow the steps defined in the playbook to understand what happened
- Check if the alert is a known pattern (refer to past alerts/runbooks)
- Analyse findings in the SIEM

### Stage 3 — Final Actions
- Make a **verdict** — True Positive or False Positive
- Decide whether **escalation** is needed
  - If yes — assign to the right person (e.g. L2) and write a note explaining findings and reason for escalation
  - If no — document your analysis and close the alert

---

## Alert Triage Flow (from handwritten notes)

```
Alert received
    |
    v
Prioritise --> Assign to yourself --> Immediately change to In-Progress
    |
    v
Is escalation needed?
    |
   Yes --> Assign to L2 --> Change to In-Progress --> Read alert details (CIP, test, hashes used)
    |
   No --> Need escalation?
              |
             Yes --> Check playbook --> In playbook? 
                          |
                         No --> Analyse/Investigate in SIEM --> Make final verdict
              |
             No --> Alert conditions (close/mark)
```

---

## Key Takeaway

Alert triage is the core daily task of a Junior SOC Analyst. The priority order — severity first, then time — ensures the most critical threats are addressed first. Playbooks are essential guides that standardise how analysts investigate alerts, reducing errors and ensuring nothing is missed. Every alert must end with a clear verdict and documented notes regardless of outcome.

---

*Part of the SOC Team Internals Module — TryHackMe SOC L1 Path*
