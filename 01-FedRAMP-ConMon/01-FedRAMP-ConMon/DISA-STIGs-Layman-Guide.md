# DISA STIGs (Layman Guide for SRE / DevOps / GRC)

## What is a STIG?
A **STIG (Security Technical Implementation Guide)** is DISA’s prescriptive hardening guidance for a specific technology (e.g., Windows Server, RHEL, Ubuntu, Kubernetes, web servers, databases, browsers, network devices).

### Simple explanation
- **NIST 800-53** = *what security outcomes must be true* (high-level requirements)  
- **STIGs** = *exact secure settings to configure on a specific system*  
- **STIG checklists** = *the step-by-step “flip these switches” instructions*

If NIST is the “building code,” STIGs are the “electrical code” for a specific device or system.

---

## Why STIGs show up in DoD environments (IL4 / IL5)
As systems move toward **DoD IL4/IL5**, the expectation shifts from “you meet security outcomes” to “you meet security outcomes AND you’re hardened to a known baseline.”

STIGs are how teams demonstrate **repeatable hardening** and **defensible evidence** of secure configuration across environments.

---

## What a STIG contains (the parts)
Each STIG is made up of many individual requirements (“rules”) and each rule typically includes:
- **Rule ID** (often shown as a V-number like `V-XXXXX`)
- **Severity Category**
  - **CAT I** (high)
  - **CAT II** (medium)
  - **CAT III** (low)
- **Check Text** (how to verify whether the setting is correct)
- **Fix Text** (how to remediate if it is not correct)
- **Rationale / Discussion** (why it matters)
- Sometimes **CCI mappings** (control correlation identifiers) that align to broader control requirements

### Simple translation
Each STIG rule tells you:
1) What the secure setting should be  
2) How to check it  
3) How to fix it  
4) Why it matters  

---

## How SRE/DevOps teams implement STIGs (real-world patterns)
SRE teams struggle when STIGs are treated as manual checklists.  
They succeed when STIGs become **automated guardrails**.

### Pattern A — “Golden Images” (best for servers)
**What it is:** bake hardening into AMIs/VM images so new systems start compliant.

**Layman:** “We build secure templates so everything starts locked down.”

### Pattern B — Configuration Management (Ansible/Chef/Puppet/DSC)
**What it is:** enforce secure settings continuously; if something drifts, automation corrects it.

**Layman:** “If someone changes a setting, the system changes it back.”

### Pattern C — Policy-as-Code (cloud + Kubernetes)
**What it is:** prevent insecure configurations from being deployed in the first place.

**Layman:** “Bad setups can’t be launched.”

### Pattern D — Scanning + Drift Detection (for evidence)
**What it is:** scan periodically, track pass/fail, and remediate or document exceptions.

**Layman:** “We run safety inspections on a schedule.”

---

## What auditors usually want as evidence (STIG compliance)
If you’re auditing STIG compliance, typical evidence includes:
- STIG checklist exports (e.g., STIG Viewer output)
- Scan results from hardening/compliance tools
- Hardening scripts (Ansible/PowerShell/DSC)
- Golden image build documentation + versioning
- Exception/risk acceptance records for unmet STIG items
- Change tickets showing remediation work and validation

### A practical “STIG Evidence Checklist”
- [ ] Which STIG(s) apply to each component (OS, DB, web server, k8s, etc.)?
- [ ] How is compliance measured (tool + cadence)?
- [ ] Where are reports stored (central evidence repository)?
- [ ] How are failed items tracked (tickets/POA&M)?
- [ ] How are exceptions documented and approved?

---

## Common STIG friction points (what causes issues)
These are common reasons SRE teams push back:
- **Logging settings** (retention and volume vs cost/performance)
- **Local account/password policies** when SSO is used (rule assumes local auth)
- **Patching windows** vs uptime expectations
- **Kubernetes/container rules** that conflict with managed service defaults
- **Legacy applications** breaking with strict TLS/cipher enforcement
- Confusion about **Not Applicable** vs **Not a Finding** vs **Open**

### How to handle this cleanly
For each STIG rule, classify it as:
1) **Applicable and Compliant**
2) **Applicable but Exception Needed** (document compensating controls + approvals)
3) **Not Applicable** (write a clear reason)

The goal is “defensible decisions,” not perfection.

---

## How to explain STIGs in interviews (short script)
“STIGs are DISA’s prescriptive hardening standards for specific technologies. I’ve worked with SRE/engineering teams to translate STIG requirements into enforceable baselines using hardened templates and automation, and to produce audit-ready evidence and documented exceptions without slowing delivery.”

---

## Helpful references (official sources)
- DISA STIGs: https://public.cyber.mil/stigs/
- DoD Cloud Computing Security (DCCS): https://public.cyber.mil/dccs/
