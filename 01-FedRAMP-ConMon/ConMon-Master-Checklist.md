# FedRAMP Continuous Monitoring (ConMon) Master Checklist
**Purpose:** A practical checklist to keep a FedRAMP Moderate/High system audit-ready with minimal friction.  
**Use:** Treat this as an operating rhythm (owners + dates + evidence links), not a one-time project.

---

## 1) ConMon Operating Rhythm (how to run the program)
### Weekly (15–30 minutes)
- [ ] Review POA&M aging (0–30 / 31–60 / 61–90 / 90+)
- [ ] Identify overdue milestones and blockers
- [ ] Confirm remediation owners + next actions
- [ ] Validate closure packages are complete before closing items

### Monthly (core ConMon cycle)
- [ ] Collect and validate evidence for required monthly deliverables
- [ ] Update POA&M and confirm submission readiness
- [ ] Review vulnerability results and remediation SLAs
- [ ] Log boundary-impacting changes and assess SSP/control narrative impact
- [ ] Hold a ConMon readiness review (30–45 minutes) before submission

### Quarterly
- [ ] Perform access recertifications (privileged + key roles)
- [ ] Validate configuration baseline checks and drift controls
- [ ] Refresh metrics reporting (POA&M aging, SLA adherence, remediation cycle time)

### Annual (plan 60–90 days in advance)
- [ ] Execute annual testing (IR exercise, contingency/DR test as required)
- [ ] Perform policy/procedure review cycle and approvals
- [ ] Prepare for annual assessment window: evidence inventory + gap closure push

---

## 2) Monthly Deliverables (Typical)
> Exact items vary by sponsor/PMO and system boundary. This list covers common expectations.

### POA&M (Required)
- [ ] Update POA&M items (status, owners, milestones, due dates)
- [ ] Add new findings (scans, audits, incidents, assessments)
- [ ] Validate closure packages and document residual risk where applicable
- [ ] Track and report POA&M backlog + aging trends

### Vulnerability Management
- [ ] Confirm scheduled vulnerability scans executed (OS/app/web/container as applicable)
- [ ] Capture scan outputs and remediation tickets/links
- [ ] Validate remediation evidence for critical/high findings
- [ ] Document false positives and exceptions with approvals + compensating controls

### Incident Reporting / Security Events
- [ ] Monthly “no incident” attestation if applicable
- [ ] If incident occurred: document timeline, notifications, actions taken, lessons learned
- [ ] Link incident-driven improvements to POA&M/control updates

### Change Management / Significant Change Tracking
- [ ] Review changes for the month (infra, identity, logging, networking, CI/CD, major app changes)
- [ ] For each boundary-impacting change: record change ticket, approvals, testing evidence
- [ ] Determine whether SSP/control narratives need updates (yes/no)
- [ ] Maintain a simple “Change Impact Log” for audit traceability

### Logging & Monitoring Evidence
- [ ] Confirm key logs are enabled and retained (per policy)
- [ ] Capture proof of alerting/monitoring review (tickets, dashboards, on-call records)
- [ ] Validate access controls for log systems and integrity protections

---

## 3) Quarterly Deliverables (Common)
### Access Reviews
- [ ] Privileged access review (admins, break-glass, service accounts)
- [ ] Review account changes (hires/terms/transfers) sampling as required
- [ ] Validate least-privilege alignment for sensitive roles

### Configuration & Baseline Drift
- [ ] Validate secure baseline configuration checks (system hardening standards)
- [ ] Confirm security-relevant configuration monitoring is working (drift controls)
- [ ] Document deviations and remediation/exception approvals

### Metrics & Reporting
- [ ] POA&M aging distribution and top drivers
- [ ] Remediation cycle time (MTTR for findings)
- [ ] ConMon submission timeliness
- [ ] Vulnerability SLA adherence and trendline

---

## 4) Annual / Periodic Deliverables (Common)
- [ ] Incident Response tabletop/exercise + after-action report
- [ ] Contingency/DR test (restore testing) with documented results (RTO/RPO if applicable)
- [ ] Annual policy and standards review + approvals
- [ ] Security awareness / role-based training completion evidence
- [ ] Audit prep: evidence inventory, narrative validation, and gap closure sprint

---

## 5) POA&M Closure Package Checklist (use before closing)
To close a POA&M item, confirm you have:
- [ ] Proof the fix was implemented (change ticket / config evidence / deployment evidence)
- [ ] Proof the fix worked (re-scan / test result / validation output)
- [ ] Date/time + who validated
- [ ] Notes for auditor traceability (what changed, where, why)

---

## 6) “Low-Friction” Rules (to avoid fire drills)
- Keep a single Evidence Index (control lane → owner → evidence source → link)
- Require closure packages (don’t close items without validation proof)
- Run one monthly readiness review before submission (short, structured)
- Escalate with options: reprioritize, add resources, or accept risk formally
