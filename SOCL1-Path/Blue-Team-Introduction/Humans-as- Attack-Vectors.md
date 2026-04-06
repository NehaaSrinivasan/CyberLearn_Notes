
# Room 3: Humans as Attack Vectors

**Module:** Blue Team Introduction
**Path:** SOC L1
**Platform:** TryHackMe

---

## What This Room Covers

Why humans are the easiest and most commonly exploited attack vector, how social engineering works, and the two key strategies organisations use to fight back — mitigation and detection.

---

## Why Humans Are the Weakest Link

Attackers find it far easier to manipulate a human than to break through technical defences like firewalls or networks. A human can unknowingly hand over credentials, access details, or sensitive information that gives an attacker everything they need to compromise a system.

> Key insight: Humans are the gateway to machines — exploit the person, gain access to the network.

---

## Social Engineering

Social engineering is the manipulation of human psychology to extract sensitive information or trick someone into taking a harmful action — without the victim realising it.

**Most common example:** Phishing emails
- Crafted to look legitimate
- Trick the recipient into clicking malicious links or revealing credentials
- Require no technical hacking — just deception

---

## Two Strategies to Combat Human Attack Vectors

### 1. Mitigation — Prevent or Reduce Attacks

Mitigation focuses on reducing the likelihood of an attack succeeding in the first place.

| Tool / Approach | Purpose |
|----------------|---------|
| **Anti-phishing tools** | Automatically detect and block phishing emails before they reach employees |
| **Security awareness training** | Educates employees on recognising attacks, understanding the impact, and knowing what to do |

> Goal: Make humans harder to manipulate through education and preventive technology.

### 2. Detection — Catch What Gets Through

Despite training and tools, some attacks will still succeed. This is where the SOC team steps in.

- Monitor for signs of compromise after an attack occurs
- Detect suspicious activity early to limit damage
- Prevent the attack from spreading further across systems and the network

---

## Hands-On Activity

4 real-world scenario-based exercises simulating how a SOC analyst responds when a human-triggered attack is confirmed. The key decision-making steps practised were:

| Action | When to apply |
|--------|--------------|
| **Block the IP** | Malicious external IP identified as source of attack |
| **Block the account** | Compromised user account confirmed |
| **Contain the system** | Infected machine isolated to prevent spread across the network |

> The scenarios reinforced that speed of containment is critical — the faster you act, the less damage spreads.

---

## Key Takeaway

Humans remain the easiest entry point for attackers because the information they provide is directly valuable for breaking into systems and networks. Technical defences alone are not enough — organisations need both preventive tools and well-trained people. When prevention fails, the SOC team's detection capabilities become the last line of defence.

---

*Part of the Blue Team Introduction Module — TryHackMe SOC L1 Path*
