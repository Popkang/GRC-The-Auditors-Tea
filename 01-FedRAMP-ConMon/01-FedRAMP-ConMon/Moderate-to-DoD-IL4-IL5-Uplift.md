# Moderate → DoD IL4/IL5 Uplift Notes (ConMon + Readiness)

## Why the uplift is hard
A common challenge is that **FedRAMP Moderate aligns closely with DoD IL2**, while **DoD IL4/IL5** introduces additional DoD SRG requirements and operational expectations (e.g., stronger identity, additional monitoring, boundary connectivity assumptions, and DoD-specific overlays).  
- FedRAMP Moderate ↔ IL2 alignment is commonly referenced in reciprocity discussions.  
- IL4/IL5 expands requirements to support **CUI** (IL4) and **CUI + additional protections / unclassified NSS considerations** (IL5).

## Core reference documentation (start here)
**DoD / DISA**
- DoD Cloud Computing Security knowledge base: https://public.cyber.mil/dccs/
- DoD CIO Cloud Security Playbook (PDF): https://dodcio.defense.gov/Portals/0/Documents/Library/CloudSecurityPlaybookVol1.pdf
- DoD Cybersecurity Reciprocity Playbook (PDF): https://dodcio.defense.gov/Portals/0/Documents/Library/%28U%29%202024-01-02%20DoD%20Cybersecurity%20Reciprocity%20Playbook.pdf

**Cloud provider references**
- AWS DoD SRG compliance: https://aws.amazon.com/compliance/dod/
- Azure DoD IL4 overview: https://learn.microsoft.com/en-us/azure/compliance/offerings/offering-dod-il4
- Azure DoD IL5 overview: https://learn.microsoft.com/en-us/azure/compliance/offerings/offering-dod-il5

## Control families most affected in the Moderate → IL4/IL5 gap
Below are the families that usually create the most engineering + operations lift, especially when moving from a “Moderate ConMon mindset” into an **IL4/IL5 operational model**.

### Identity, Authentication, and Access
**Families:** AC, IA  
**Why it changes:** IL4/IL5 pushes stronger identity expectations and more defensible access governance (e.g., credential strength, MFA enforcement patterns, tighter privileged access controls).  
**Evidence examples:** IdP configuration exports, MFA enforcement rules, privileged access review logs, service account governance, break-glass controls.

### Audit & Accountability / Monitoring (Signal Quality)
**Families:** AU, SI (and operational monitoring expectations)  
**Why it changes:** DoD IL4/IL5 places heavier emphasis on enterprise monitoring, telemetry, and defensible evidence that monitoring is operational (not just “enabled”).  
**Evidence examples:** centralized logging architecture, retention configs, alert coverage, ticketed review workflow, monthly “monitoring review” artifacts.

### Configuration Management & Drift Control
**Families:** CM  
**Why it changes:** IL4/IL5 expects more enforceable baselines and stronger controls against drift (policy-as-code patterns, hardened images, standard builds).  
**Evidence examples:** baselines (STIG-aligned where applicable), IaC repos, change tickets, config compliance reports, exception approvals.

### Incident Response & Forensics Readiness
**Families:** IR, AU/SI (supporting)  
**Why it changes:** operational readiness matters more—playbooks, roles, testing, and proving the process works.  
**Evidence examples:** IR tabletop/exercise reports, IR runbooks, incident ticket templates, after-action reports, escalation matrices.

### Boundary / Network Protections & Encryption
**Families:** SC, AC  
**Why it changes:** tighter boundary assumptions, stronger protections for data in transit/at rest, and clearer segmentation patterns.  
**Evidence examples:** network diagrams, firewall policy exports, private connectivity notes (as applicable), key management evidence, TLS standards.

### Contingency Planning / Resilience
**Families:** CP  
**Why it changes:** restoration evidence and operational testing are heavily scrutinized in higher-impact environments.  
**Evidence examples:** DR test reports, restore test screenshots/logs, RTO/RPO targets, backup configuration evidence.

### Supply Chain / Vendor Governance
**Families:** SR, SA (and vendor risk processes)  
**Why it changes:** more scrutiny on sub-processors, integrations, and vendor access pathways—plus stronger documentation discipline.  
**Evidence examples:** vendor inventory, security reviews, data flow diagrams, contract security addenda, access pathways, offboarding evidence.

## Practical ConMon implications (what changes in your monthly rhythm)
- Stronger expectations for **POA&M discipline** (aging, closure packages, risk acceptance rigor)
- Monthly vulnerability outputs and remediation SLAs become more visible to leadership
- “Significant change” discipline matters more (keep SSP/diagrams/evidence from drifting)
- Monitoring must show **operational execution** (review artifacts, not just configs)

## Suggested artifacts to maintain (low friction)
- Evidence Index (lane → owner → source system → link)
- Change Impact Log (what changed → which controls/artifacts impacted → evidence link)
- POA&M Closure Package checklist (implemented + validated + date + validator)
