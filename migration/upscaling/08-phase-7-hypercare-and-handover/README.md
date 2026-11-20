# PHASE 7: HYPERCARE, SUPPORT AND OPERATIONAL HANDOVER

> Part of the *Enterprise Adobe DXP Migration Handbook* v1.1 (Review Draft). Section numbers (§) refer to the handbook's original numbering; see the root [README](../README.md) for the section map.

## 10. Phase 7 – Hypercare, Support and Operational Handover

### 10.1 Objective
Stabilise production, resolve implementation-related issues and transfer the knowledge and documentation required for the organisation to run its Adobe DXP environment after the engagement. The consultant is not a permanent support employee.

### 10.2 Post-Go-Live Hypercare
For an agreed period, monitor availability, performance, business transactions, middleware and APIs, and integrations; investigate failed synchronisations and production errors; resolve migration-related defects; support reconciliation; review alerts; support agreed changes; escalate vendor issues. Agree duration and hours in the engagement plan, reflecting complexity and risk.

Maintain an incident register: reference, date/time, description, business impact, severity, affected system, root cause, resolution, preventative action, status, owner.

During hypercare the **operational owner works first-line, with the consultant in a supporting role**, so that knowledge transfer happens on live incidents.

**Deliverable:** Hypercare and Stabilisation Report.

### 10.3 Support Model and Responsibilities

| Level | Responsibility |
|---|---|
| L1 – Business Support | User queries, access issues, basic process support |
| L2 – Application Support | Functional issues, configuration, integrations, operational troubleshooting |
| L3 – Technical Support | Code defects, architecture, infrastructure, complex integration |
| Vendor Support | Adobe, hosting provider and third-party escalation |

Responsibilities may be assigned to internal staff, an MSP, a specialist Adobe partner or a combination. Define ownership, incident logging, severity levels, escalation timelines, support hours, after-hours arrangements, vendor contacts and specialist Adobe expertise requirements. Never leave an undocumented assumption that the client can resolve all L2 and L3 issues internally.

**Deliverable:** Support and Escalation Matrix.

### 10.4 Technical and Operational Documentation
Documentation must allow another qualified team to understand and support the environment.

- **Solution:** overall, Adobe product, application, data and integration architecture; decisions and limitations.
- **Infrastructure:** hosting model, environments, networking, domains and certificates, dependencies, storage and databases, ownership.
- **Deployment:** source control, build, pipelines, approvals, rollback, configuration management.
- **Integration:** API specifications, middleware configuration, mappings, authentication, retry and failure handling, dependencies, vendor ownership.
- **Data:** ownership, mappings, synchronisation, migration and reconciliation procedures, retention and archival.
- **Security:** access management, roles, privileged accounts, secret and certificate ownership, procedures, audit requirements.
- **Operations:** dashboards, alert definitions, incident procedures, troubleshooting, backup, DR runbooks, maintenance.

Credentials, secrets and private keys transfer through approved secure mechanisms, never ordinary documentation.

**Deliverable:** Complete Technical and Operational Documentation Repository.

### 10.5 Knowledge Transfer and Training
Practical and demonstrable: architecture walkthrough; Adobe product administration; infrastructure and hosting; application support; middleware troubleshooting; deployment and release demonstrations; migration and reconciliation; monitoring and alerts; incident exercises; backup and restore; DR walkthrough. Receiving staff perform selected procedures under supervision.

Training records: topic, participants, date, documentation reference, practical exercise, outstanding gaps, acceptance status.

**Deliverable:** Knowledge Transfer and Training Record.

### 10.6 Operational Readiness and Formal Handover
Use the checklist in Appendix B.7 (platform and infrastructure, applications and integrations, data and security, operations, knowledge transfer, project closure).

**Deliverable:** Formal Operational Handover and Acceptance Document.

### 10.7 Future Scaling and Continuous Improvement Recommendations
Cover additional Adobe capabilities, channels, regions, performance, integration, automation, personalisation, analytics maturity, security, infrastructure optimisation, technical debt and support capability. Separate immediate, medium-term and future items, each with rationale, dependencies, indicative priority and risks.

**Deliverable:** Future Scaling and Improvement Roadmap.

### 10.8 Consultant Exit, Operational Ownership and Closure

**Hard exit condition.** The consultant cannot formally exit until the client has a **named, accountable operational owner**. This is an entry condition for Gate G7, not an item on a checklist.

An operational owner is a named internal team, managed service provider, specialist Adobe partner, infrastructure provider or defined combination, that has accepted in writing responsibility for:

- L1, L2 and L3 support (or clearly assigned parts of it) and vendor escalation.
- Stated coverage hours and after-hours arrangements.
- Monitoring, backups and DR operation.
- Release and change management.
- Custody of credentials, certificates and vendor accounts.

The handbook does not prescribe internal or MSP; it prescribes that the choice be made and evidenced.

**Timing.** The operational owner is appointed no later than G6 (go-live), so that they take part in operational readiness testing, hypercare and knowledge transfer. Appointment after go-live is a recorded risk, and the intended date is tracked from G2 (§5.11).

**Fallback if the client cannot appoint in time.** The consultant must not become the default operator. The client chooses, in writing, one of:

1. **Time-boxed extension:** a separately scoped and contracted bridging support period, with fixed end date, defined service levels and an appointment milestone. It does not form part of the original engagement deliverables.
2. **Signed risk acceptance:** the client's accountable executive accepts in writing the risk of operating without a named owner, with a stated date, and the consultant's exit proceeds on a "handover with exceptions" basis. Exceptions are recorded in the closure risk register.

Closure package: final implementation report; stabilisation report; outstanding issue and risk register; technical documentation repository; operational support handbook; knowledge-transfer records; vendor and escalation register; future improvement roadmap; signed operational handover; client acceptance of engagement deliverables.

### 10.9 Phase 7 Exit Criteria (Gate G7)
**Entry condition:** named operational owner in place (or one of the two fallback instruments executed).

- Production meets agreed stability criteria; hypercare issues resolved or formally accepted.
- Documentation delivered; knowledge transfer completed and signed.
- Access and ownership transferred; monitoring and recovery procedures available.
- Future recommendations documented; handover and closure accepted.

**Final Deliverable:** Signed Operational Handover and Consultant Engagement Closure Report.
