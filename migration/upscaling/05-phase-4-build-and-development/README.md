# PHASE 4: BUILD AND DEVELOPMENT

> Part of the *Enterprise Adobe DXP Migration Handbook* v1.1 (Review Draft). Section numbers (§) refer to the handbook's original numbering; see the root [README](../README.md) for the section map.

## 7. Phase 4 – Build and Development

### 7.1 Objective
Implement the approved architecture. Under Model B the consultant directs and reviews; the named build team implements. Under Model A the consultant implements the agreed scope directly.

### 7.2 Environment Provisioning
Provision supported Adobe environments; configure customer-managed infrastructure where applicable; establish connectivity, DNS, certificates, dev and test environments, storage and databases, access, security, backups; validate connectivity. Document environment settings and ownership.

**Deliverable:** Provisioned and Validated Environments.

### 7.3 Source Control and Development Standards
Repositories, branching, coding standards, code review, dependency management, build and deployment pipelines, environment configuration, release approvals, versioning, rollback. Credentials and secrets must never be committed to source control.

**Deliverable:** Development and Release Management Standards.

### 7.4 Adobe Product Configuration
Configure the selected products per design: AEM, Adobe Commerce, AEP and any included modules (Analytics, Target, AJO), identity integration, environments and access. Follow each product's supported deployment and extension mechanisms.

**Deliverable:** Configured Adobe DXP Components.

### 7.5 Custom Development
Frontend, backend, Adobe extensions, custom APIs, business logic, workflows, UI components, authentication integration, transformation services, background processing, admin functionality. Limit custom work to genuine requirements not met by standard capabilities.

**Deliverable:** Implemented Custom Applications and Extensions.

### 7.6 Middleware Implementation
Configure API gateways; implement integration services, brokers, producers and consumers, transformation, authentication, retries, error handling, queues and dead-letter handling, logging, correlation and monitoring. Middleware should run independently of individual application deployments where appropriate.

**Deliverable:** Implemented Middleware and Integration Services.

### 7.7 Third-Party Integration Implementation
For each integration (ERP, CRM, PIM, OMS, WMS, payments, tax, shipping, identity, marketing, analytics, support): implement the interface, configure authentication, validate request and response, implement failure handling, configure monitoring, test connectivity, document dependencies.

**Deliverable:** Implemented and Technically Validated Integrations.

### 7.8 Data Migration Tooling and Preparation
**Boundary with Phase 5:** Phase 4 *builds* the tooling; Phase 5 *governs and executes* it. G4 requires tooling that runs end to end on sample data; G5 requires rehearsals on full-volume data.

Build extraction, transformation, import, validation and reconciliation processes, repeatable scripts, error reporting and migration logs, supporting rehearsal before production.

**Deliverable:** Migration Utilities and Data Processing Components.

### 7.9 Security Implementation
Identity integrations, roles and permissions, API security, service accounts, secret management, encryption, network restrictions, audit logging, other controls.

**Deliverable:** Implemented Security Controls.

### 7.10 Observability and Disaster Recovery Implementation
Dashboards, alerts, log integration, application, infrastructure and integration monitoring, backup jobs, restoration procedures, validated recovery.

**Deliverable:** Operational Monitoring and Recovery Capabilities.

### 7.11 Technical Documentation During Build
Produce continuously, not in the final week: architecture decisions, environment configuration, deployment procedures, integration specifications, API docs, data mappings, security configuration, known limitations, operational procedures, troubleshooting.

**Deliverable:** Updated Technical Documentation Repository.

### 7.12 Phase 4 Exit Criteria (Gate G4)
- Environments available; Adobe components configured; approved custom work implemented.
- Middleware operational; required integrations implemented; migration tooling runs on sample data.
- Security controls and monitoring operational; deployment procedures established.
- **Consultant code and configuration review completed (Models B/C), with findings dispositioned.**
- Documentation current; ready for formal testing.

**Final Deliverable:** Implemented Adobe DXP Solution Ready for Testing.
