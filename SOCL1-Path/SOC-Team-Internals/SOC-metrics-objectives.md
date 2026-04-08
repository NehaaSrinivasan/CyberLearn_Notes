
# Room 4: SOC Metrics and Objectives

**Module:** SOC Team Internals
**Path:** SOC L1
**Platform:** TryHackMe

---

## What This Room Covers

The core objective of a SOC team, key metrics used to measure SOC performance, what each metric indicates, thresholds for good and bad performance, and how to improve when metrics fall outside acceptable ranges.

---

## SOC Core Objective — CIA Triad

The SOC exists to protect the **Confidentiality, Integrity and Availability** of an organisation's digital assets.

> Key insight: The SOC cannot always stop a breach — but it must receive the alert, triage it and respond to the attackers as fast as possible.

---

## Key SOC Metrics

| Metric | Full Name | Formula | What it indicates |
|--------|-----------|---------|-------------------|
| **MTTD** | Mean Time To Detect | Detected / Total No. | How fast the SOC detects threats |
| **MTTR** | Mean Time To Respond | — | How fast the SOC responds to incidents |
| **MTTA** | Mean Time To Acknowledge | — | How fast an analyst picks up an alert |
| **Alert Count** | — | Total no. of alerts received | Overall load on SOC analysts |
| **False Positive Rate (FPR)** | — | False Positives / Total no. of alerts | Level of noise in alerts — capability to detect real threats |
| **Alert Escalation Rate (AER)** | — | Escalated Alerts / Total no. of alerts | Experience and independence of L1 analysts |
| **Threat Detection Rate (TDR)** | — | Detected Threats / Total no. | Reliability of the SOC team — should always be 100% |

---

## What Each Metric Tells You

### 1. Alert Count
- Good range: **5 to 30 alerts per day**
- Indicates the overall workload on SOC analysts

### 2. False Positive Rate (FPR)
- FPR over **80% is bad** for the SOC team
- Analysts become less vigilant and may start skipping true positives
- **0% is unachievable** — some false positives will always exist
- Goal: Fine tune detection rules → FP Remediation

**How to improve:**
- Exclude trusted activities like system updates
- Automate alert triage using SOAR and custom scripts

### 3. Alert Escalation Rate (AER)
- L2 relies on L1 to filter noise and escalate only actionable and threatening alerts
- Good target: **under 50%**, even better **under 20%**
- Measures the experience and independence of L1 analysts

### 4. Threat Detection Rate (TDR)
- Should **always be 100%**
- Missing a threat means ransomware or data exfiltration could go undetected

---

## SLA — Service Level Agreement

A document signed between the internal SOC team members and the office, MSSP, company management and customers. It defines expected response times and performance standards.

---

## Personal Reflection

**On MTTR in the real world:**
The ideal MTTR target given is 60 minutes. But in real world scenarios this is rarely achievable for major incidents. The WannaCry ransomware attack for example took weeks to fully respond to and contain — not 60 minutes. The 60 minute target is an ideal benchmark, not a guarantee.

What actually determines real world MTTR is how well the L1 analyst does their job at the very beginning. If L1 correctly identifies the IOCs, writes a clear report and escalates with full context, L2 can hit the ground running. If L1 misses IOCs or writes a vague report, L2 has to start the investigation from scratch — and MTTR explodes.

This means the L1 analyst, despite being the most junior role, has a direct impact on how fast the entire team responds to a threat. The quality of triage at the start determines the speed of recovery at the end.

---

## Key Takeaway

SOC metrics are not just numbers — they are health indicators for the entire security operation. A high false positive rate means analysts lose focus on real threats. A slow MTTD means attackers have more time to cause damage. Every metric points to a specific problem and has a specific fix. The goal of a SOC L1 analyst is to keep these numbers within acceptable ranges through fast, accurate and well-documented alert triage.

---

*Part of the SOC Team Internals Module — TryHackMe SOC L1 Path*
