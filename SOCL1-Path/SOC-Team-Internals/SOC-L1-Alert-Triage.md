
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

### Stage 1 — Initial Actions
- Assign the alert to yourself
- Change status to **In Progress**
- Note down basic details of the alert

### Stage 2 — Investigation
- Use a **playbook or workbook** to guide your investigation
- Follow the steps defined in the playbook to understand what happened
- Check if the alert matches a known pattern
- Analyse findings in the SIEM

### Stage 3 — Final Actions
- Make a **verdict** — True Positive or False Positive
- Decide whether **escalation** is needed
  - If yes — assign to the right person and write a note explaining findings and reason for escalation
  - If no — document your analysis and close the alert

---

## Alert Triage Flow

```
Alert received
      |
      v
Prioritise → Assign to yourself → Change status to In Progress
      |
      v
Is escalation needed?
      |
     Yes → Assign to L2 → Write notes and reason
      |
      No → Investigate using playbook
              |
         In playbook? → Yes → Follow steps → Make verdict
              |
              No → Analyse in SIEM → Make verdict
```

---

## Personal Reflection

**On severity and time prioritisation:**
High severity alerts are worked on first because they cause the most damage to systems and networks if left unattended. A critical alert like ransomware spreading needs immediate attention — every minute of delay means more systems affected. Time ordering ensures the oldest unresolved alerts don't get forgotten. Together they help the L1 analyst focus, save time, and work efficiently through the queue.

**On playbooks:**
Playbooks save time because if the same alert has happened before and is already documented, the analyst doesn't need to spend days figuring it out from scratch. This is exactly why documentation is a must in alert triage — today's investigation becomes tomorrow's playbook.

**On true vs false positives:**
True positives are real security incidents. False positives appear to be incidents but aren't — often caused by misconfigured detection rules. For example a rule that flags 3 login attempts from different locations might trigger on someone who simply typed their password wrong 3 times from the same location. Getting this wrong matters because chasing false positives wastes time while real threats go unnoticed.

---

## Key Takeaway

Alert triage is the core daily task of a Junior SOC Analyst. The priority order — severity first, then time — ensures the most critical threats are addressed first. Playbooks are essential guides that standardise how analysts investigate alerts, reducing errors and ensuring nothing is missed. Every alert must end with a clear verdict and documented notes regardless of outcome.

---

*Part of the SOC Team Internals Module — TryHackMe SOC L1 Path*
