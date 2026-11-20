# PHASE 3: DESIGN

> Part of the *Enterprise Adobe DXP Migration Handbook* v1.1 (Review Draft). Section numbers (§) refer to the handbook's original numbering; see the root [README](../README.md) for the section map.

## 6. Phase 3 – Architecture and Solution Design

### 6.1 Objective
Translate the strategy into a complete technical and operational design detailed enough that developers and infrastructure teams need not make major architectural decisions during build. Under Model B or C the design is the consultant's primary accountable output.

### 6.2 Target Solution Architecture
Show Adobe products and services, custom applications, external systems, data stores, middleware, API gateways, network boundaries, identity services, hosting environments, monitoring, backup and DR. Distinguish Adobe-managed from customer-managed components.

**Deliverable:** Target Solution Architecture Diagram and Description (reference diagram: Appendix C.2).

### 6.3 Application Architecture
Frontend, backend, custom services, Adobe extensions, API contracts, authentication and authorisation, business logic, configuration, scheduled tasks, background processing, error handling, dependencies. Define boundaries between Adobe capabilities and independently managed services.

**Deliverable:** Application Architecture Specification.

### 6.4 Infrastructure and Hosting Architecture
- **Environments:** development, integration test, QA, staging, production, DR.
- **Services:** compute, storage, databases, containers (where supported), networking, DNS, certificates, CDN, load balancing, firewall, backup.
- **Deployment:** CI/CD, source control, build environments, approvals, release management, rollback.

Document ownership per component, and honour the constraints of each product's deployment model (e.g. the prescribed pipeline for AEM as a Cloud Service).

**Deliverable:** Infrastructure and Hosting Architecture Specification.

### 6.5 Middleware and Integration Architecture
Define API gateway responsibilities, middleware components, brokers, event streaming, integration services, transformation, orchestration, webhooks, scheduled synchronisation and external connectivity.

Standards: API naming and versioning, authentication, authorisation, request validation, transformation, idempotency, retry policies, dead-letter handling, timeouts, rate limiting, correlation identifiers, distributed tracing, error reporting. Avoid unnecessary direct dependencies between applications.

**Deliverable:** Middleware and Integration Architecture.

### 6.6 Data Architecture
Data ownership, domains, source-of-truth systems, models, relationships, flows, retention, archival, synchronisation, access, protection. Example: Adobe Commerce manages commerce transactions while an ERP remains authoritative for financial or inventory records, depending on operating model.

**Deliverable:** Target Data Architecture and Data Ownership Matrix.

### 6.7 Security Architecture
Identity provider integration, authentication, RBAC, administrative access, API authentication, service accounts, secrets and certificates, network restrictions, encryption, audit logging, monitoring, vulnerability management, and Adobe/client responsibility boundaries.

**Deliverable:** Security Architecture and Access Control Matrix.

### 6.8 Observability Architecture
Monitor availability, response times, infrastructure and database health, API performance, middleware queues, integration failures, background jobs, synchronisation, business transactions and security events. Establish centralised logging where supported, metrics, tracing, dashboards, alert thresholds, notifications and operational reporting. Cover business-critical journeys, not just components.

**Deliverable:** Observability and Monitoring Design.

### 6.9 Disaster Recovery Architecture
Backup strategy, recovery procedures, restoration, environment recovery, regional failure, vendor outage, integration failure, business continuity and recovery testing. Define RPO and RTO from business requirements. Distinguish recovery capabilities supplied by Adobe from those the organisation or other providers must implement.

**Deliverable:** Disaster Recovery and Business Continuity Design.

### 6.10 Operational and Support Design
Support levels, responsible teams, incident management, escalation, vendor dependencies, support hours, maintenance, release responsibilities, monitoring ownership. **Identify the operational owner and confirm the appointment date (§5.11).**

**Deliverable:** Target Operating Model and Support Design.

### 6.11 Phase 3 Exit Criteria (Gate G3)
- Architecture, application, infrastructure, integration, data and security designs approved.
- Observability and DR designs documented; support responsibilities agreed.
- All product-specific assumptions re-verified against current Adobe documentation and licence (§2.2).
- Major decisions recorded in the architecture decision register (template: Appendix A.5).

**Final Deliverable:** Approved Technical and Solution Design Package.
