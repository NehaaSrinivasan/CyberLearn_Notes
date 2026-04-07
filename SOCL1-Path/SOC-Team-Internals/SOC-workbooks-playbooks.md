
# Room 3: SOC Workbooks and Lookups

**Module:** SOC Team Internals
**Path:** SOC L1
**Platform:** TryHackMe

---

## What This Room Covers

How SOC analysts use identity and asset inventory to understand alert context, the role of Active Directory, network diagrams, SOC workbook stages, and a detailed walkthrough of the enrichment, investigation and escalation stages.

---

## Identity Inventory

A catalogue of corporate employees including:
- User accounts and service accounts
- Machine privileges and access
- Contact details and role inside the company

**Example fields:**

| Full Name | Username | Position/Role | Email | Location | Access |
|-----------|----------|---------------|-------|----------|--------|

**Sources of Identity Inventory:**

| Source | Examples |
|--------|---------|
| **AD (Active Directory)** | Identity database for SOC |
| **SSO Providers** | Okta, Google |
| **HR Systems** | CMAD, HiBob, BambooHR |
| **Custom Solutions** | CSV, Excel sheets |

---

## Asset Inventory / Lookup

A list of all computing sources present in the organisation — software, hardware, and employees (computers, servers, workstations).

**Example fields:**

| Hostname | Location | IP Address | OS | Owner | Purpose |
|----------|----------|------------|-----|-------|---------|

**Sources of Asset Inventory:**

1. Active Directory (AD)
2. SIEM + EDR (e.g. Elastic + CrowdStrike — agents collect info about monitored hosts)
3. MDM Solution
4. Custom Solution

---

## Network Diagram

A visual schema presenting existing locations, subnets and their connections. Helps analysts understand suspicious network activity and make a verdict on whether the activity seen is legitimate or not — using identity inventory, network diagram and asset inventory together.

---

## SOC Workbook / Runbook / Playbook / Workflow

A well detailed document consisting of steps required for investigation and remediation of threats in an efficient and consistent manner.

**Three stages of a SOC Workbook:**

```
Enrichment Stage → Investigation Stage → Escalation Stage
```

---

### Enrichment Stage

```
Receive Alert
      |
      v
Use tools (e.g. BambooHR) to find out expected user location
      |
      v
Lookup login IP in threat intel services
      |
      v
Lookup login IP in anonymisation detection services
```

---

### Investigation Stage

```
Is IP malicious?
      |
     Yes → MFA check → Yes → Escalate
      |
      No → Splunk/SIEM to list user actions following the login
              |
              v
         Suspicious actions (e.g. MFA reset)?
              |
             Yes → Is it a known/contact user?
                        |
                       Yes → Escalate
                        |
                        No → Login time from atypical time?
                                  |
                                 Yes → Escalate
                                  |
                                  No → Close alert — mark as FP
              |
             No → Login from atypical location?
                        |
                       Yes → Run volume login timeline
                              Check neighbours
                              Look back 30 days
                              No base?
                                  |
                                 Yes → Contact with approval → Escalate
```

---

### Escalation Stage

```
Investigation confirms suspicious activity
      |
      v
Write a detailed report of findings
      |
      v
Escalate the alert to L2
```

---

## Personal Reflection

**On identity and asset inventory:**
When an alert comes in, knowing the context is everything. Identity and asset inventory help the SOC analyst understand who is responsible for the alert, which system it came from and which location. Without them an analyst is blind — they can see something happened but have no idea who caused it or whether it is even unusual for that user.

**On Active Directory:**
AD is the backbone repository of the entire organisation. It stores the list of users, devices and files along with their owners, permissions and location and department information. For a SOC analyst it provides the context needed to understand who is behind an alert and whether their behaviour is normal.

**On workbooks:**
Workbooks save time because if the same alert has happened before and is already documented, the analyst doesn't need to start from scratch. They follow the playbook, close the known alert faster, and have more capacity left for genuinely new threats. This is why documentation culture in a SOC is so important — every investigation completed today makes the team faster tomorrow.

---

## Key Takeaway

Context is everything in SOC work. Identity inventory, asset inventory, network diagrams and Active Directory together give analysts the background they need to make sense of alerts quickly. Workbooks ensure that experience is never lost — every past investigation becomes a guide for future ones. The three workbook stages — enrichment, investigation and escalation — show that alert analysis is a structured decision tree, not guesswork. Every step leads to either a justified escalation or a documented false positive verdict.

---

*Part of the SOC Team Internals Module — TryHackMe SOC L1 Path*
