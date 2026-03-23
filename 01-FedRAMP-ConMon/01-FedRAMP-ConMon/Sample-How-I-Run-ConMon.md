# How I Run a FedRAMP Continuous Monitoring (ConMon) Program

## Goal
Keep the system **audit-ready year-round** (not “audit-ready once a year”) by running a predictable operating rhythm across:
- POA&M + remediation governance
- vulnerability management evidence
- change impact discipline (avoid SSP drift)
- logging/monitoring “operational proof”
- executive reporting and risk burn-down

## Step 1 — Map the ConMon Machine (observe-first)
I start by mapping the current-state:
- **System of record**: where POA&Ms live, where evidence lives, where work is tracked (Jira/GRC tool/SharePoint/etc.)
- **RACI by lane**: who owns vuln scans, access reviews, change control, logging evidence, IR/DR evidence
- **Submission cadence**: monthly/quarterly/annual deliverables and due dates
- **Pain points**: what is consistently late or causes auditor back-and-forth

**Output:** 1-page current state map + Evidence Index (lane → owner → source → link)

## Step 2 — Establish a Repeatable Monthly Cadence
I use a lightweight monthly rhythm that avoids “meeting overload”:
- Weekly 15–30 minute POA&M hygiene sweep (aging + blockers)
- Monthly evidence collection window
- A short ConMon readiness review before submission

### Monthly deliverables I validate every cycle
- POA&M updates (status, milestones, owners, closure packages)
- monthly vulnerability scan outputs + remediation SLAs
- change log + significant change impact assessment
- proof logging/monitoring is operational (not just enabled)
- incident reporting attestation (and incident artifacts if applicable)

## Step 3 — POA&M Discipline (what makes ConMon succeed)
A POA&M program fails when closures aren’t defensible or items age forever.
My approach:
- define “closure package” minimums (implemented + validated + dated)
- track aging buckets (0–30 / 31–60 / 61–90 / 90+)
- escalate with options (reprioritize, add resources, accept risk formally)

## Step 4 — Evidence Packaging (reduce auditor friction)
I standardize evidence so it’s easy to review:
- date-stamped exports/screenshots
- links to tickets and change records
- clear mapping to control families and deliverables

**Principle:** Make evidence “reviewable in 60 seconds.”

## Step 5 — Change Impact Log (prevent SSP drift)
This is one of the biggest hidden risks in ConMon.
Every month:
- capture boundary-impacting changes (identity, infra, networking, logging, CI/CD, major app changes)
- document approvals, validation, and whether SSP narratives need updates

## Step 6 — Executive Reporting
I report program posture in business language:
- POA&M backlog + aging trend
- remediation cycle time (how fast we close findings)
- vuln SLA adherence and trendline
- “top 5 risks” + what leadership needs to decide

## Success Metrics
- on-time ConMon submissions
- declining POA&M aging (especially >90 days)
- reduced audit back-and-forth
- faster time-to-close for findings
- no surprise “significant change” issues
