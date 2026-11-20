# PHASE 4: LIVE OPERATIONS

> Part of the *Enterprise Adobe DXP Support and Operations Handbook* v1.0 (Review Draft). Section numbers (§) refer to the handbook's original numbering; see the README at the root of this folder for the section map.

## 7. Phase 4 – Live Operations

### 7.1 Objective
Run the estate reliably under the agreed processes.

### 7.2 Incident Management
1. **Detect:** monitoring or user report.
2. **Log and categorise:** service, severity, impact.
3. **Triage and diagnose:** runbooks, logs, recent changes.
4. **Communicate:** initial notice and updates at the agreed interval.
5. **Restore service:** workaround or fix; vendor escalation where needed.
6. **Verify and close** with the user or business owner.
7. **Review:** post-incident review for Sev 1 and Sev 2 (template A.5).

**Major incident procedure:** declare, assign an incident commander, open a bridge, appoint communications lead, keep a timeline, escalate to Adobe and other vendors in parallel, communicate to stakeholders, and hold a post-incident review within an agreed number of days.

### 7.3 Problem Management
Identify recurring or high-impact incidents, find root cause, record known errors and workarounds, raise fixes through change control, and track to closure (template A.6 for the problem record).

### 7.4 Change and Release Management
All production changes follow the change process: request, risk assessment, approval, scheduling, implementation, verification and review. Emergency changes are recorded retrospectively. Releases from the development team are accepted into support through the release checklist (Development handbook A.7). Align freeze periods with business peaks.

### 7.5 Request Fulfilment and Access Management
User onboarding and offboarding, role changes, content author permissions, admin access, API credentials. Perform periodic access reviews.

### 7.6 Monitoring and Event Management
Review alerts, tune thresholds, remove noise, and confirm every alert has an owner and runbook. Check dashboards daily; maintain an on-call rota.

### 7.7 Routine Operations
Daily, weekly and monthly checks per product (see Appendix B.4). Examples: job and cron health, indexing status, queue depth, replication and publishing status, ingestion health, certificate expiry, storage and capacity, backup success, error budget review.

### 7.8 Security Operations
Apply the patching cadence, track vulnerabilities by severity and due dates, rotate secrets and keys, renew certificates, review audit logs, handle security incidents and POPIA breach notifications through the agreed procedure.

### 7.9 Backup, Recovery and DR Operations
Verify backups, run scheduled restore tests, run DR exercises, record results and fix gaps. A backup that has not been restored in a test is unproven.

### 7.10 Vendor Management and Escalation
Raise Adobe and third-party tickets with: product and environment, severity and business impact, clear symptoms and timeline, steps to reproduce, logs and request identifiers, recent changes and what has been tried. Track tickets to resolution, escalate by agreed severity paths, and record vendor performance.

### 7.11 Knowledge Management
Update runbooks after every incident that exposed a gap. Maintain a searchable knowledge base with known errors and workarounds.

### 7.12 Communication
Status updates to stakeholders, planned maintenance notices, post-incident summaries.

### 7.13 Phase 4 Review Criteria (Gate S4, reviewed periodically)
- Incident and request targets met or deviations explained.
- Major incidents reviewed with actions tracked.
- Backups restored successfully in tests.
- Patch and access review obligations met.
- Runbooks current.
