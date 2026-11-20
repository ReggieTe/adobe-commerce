# PHASE 2: SERVICE DESIGN

> Part of the *Enterprise Adobe DXP Support and Operations Handbook* v1.0 (Review Draft). Section numbers (§) refer to the handbook's original numbering; see the README at the root of this folder for the section map.

## 5. Phase 2 – Service Design

### 5.1 Objective
Design a service the client can understand, fund and hold to account.

### 5.2 Service Catalogue and Scope
List the services in scope (for example incident response, user and access administration, content and catalogue support, release support, monitoring, backup operations, vendor escalation, reporting) and what is explicitly out of scope.

**Deliverable:** Service Catalogue (template A.1).

### 5.3 Service Levels
Define severity levels, response and resolution targets, support hours, after-hours arrangements, maintenance windows, availability targets (reflecting what Adobe-managed services commit to), and exclusions. Use the example matrix below as a starting point only.

| Severity | Definition (example) | Target response (example) | Target update interval (example) |
|---|---|---|---|
| Sev 1 – Critical | Revenue-critical journey down or data loss/security breach | 15–30 minutes | 30–60 minutes |
| Sev 2 – High | Major function degraded, workaround limited | 1–2 hours | 2–4 hours |
| Sev 3 – Medium | Partial or non-critical impact, workaround exists | 4 business hours | Daily |
| Sev 4 – Low | Minor issue or request | 1–2 business days | As agreed |

Targets are examples. The agreed values, measurement method and any service credits go in the SLA (template A.2).

**Deliverable:** SLA and Operational Level Agreements (OLAs).

### 5.4 Process Design
Define incident, major incident, problem, change, release, request fulfilment, access management, knowledge and vendor escalation processes, with owners and inputs and outputs.

**Deliverable:** Process Library.

### 5.5 Tooling Design
Ticketing and service desk, monitoring and alerting, on-call paging, log and trace access, status communication, knowledge base, runbook repository, secrets vault, reporting. Define access and ownership; tools and licences belong to the client where possible.

**Deliverable:** Tooling and Access Design.

### 5.6 Monitoring and Alerting Design
Cover availability, response time, error rate, checkout and order success, content publishing, integration and queue health, job success, data ingestion, certificate and secret expiry, security events and business KPIs. Every alert has an owner, severity, runbook link and escalation path.

**Deliverable:** Monitoring and Alerting Catalogue (template A.7).

### 5.7 Security Operations Design
Patching cadence, vulnerability management, access reviews, privileged access, secret and key rotation, certificate renewal, audit log review, incident handling for security events, POPIA breach procedure.

### 5.8 Backup, Recovery and DR Operations Design
Backup scope and schedule, restore tests, DR exercises, RPO and RTO, responsibilities across Adobe, host and client.

### 5.9 Governance and Reporting Design
Service review meetings, KPI set, report content and distribution, escalation governance, continual improvement register.

### 5.10 Staffing and On-Call Design
Roles, rotas, skills matrix, handover between shifts, fatigue and cover rules.

### 5.11 Phase 2 Exit Criteria (Gate S2)
- Service catalogue, SLA and OLAs agreed.
- Process library, tooling, monitoring and security operations designs approved.
- Backup and DR operations agreed.
- Adobe facts re-verified with dates.
- Staffing plan and service owner confirmed.

**Final Deliverable:** Approved Service Design Package.
