# PHASE 2: ARCHITECTURE AND TECHNICAL DESIGN

> Part of the *Enterprise Adobe DXP Development Handbook* v1.0 (Review Draft). Section numbers (§) refer to the handbook's original numbering; see the README at the root of this folder for the section map.

## 5. Phase 2 – Architecture and Technical Design

### 5.1 Objective
Produce a design detailed enough that developers make no major architectural decisions while building. Under Models B and C this is the consultant's primary accountable output.

### 5.2 Solution Architecture
Products and services, custom components, integrations, data flows, environments, hosting responsibility boundaries (Adobe-managed vs client-managed), identity, CDN and caching, observability.

**Deliverable:** Solution Architecture and Diagram (Appendix C.2).

### 5.3 Component and Module Design
Per product, design components and modules to the supported extension points: AEM components, templates, services, workflows and Dispatcher rules; Commerce modules, plugins, observers and APIs; AEP schemas, datasets and flows; tag and data-layer design. Define interfaces, ownership and test approach for each.

**Deliverable:** Technical Design Document per component group (template A.2).

### 5.4 Data and Content Model Design
Content models and fragments, product and customer data models, XDM schemas, identity and consent models, source-of-truth rules, retention and archival.

**Deliverable:** Data and Content Model Specification.

### 5.5 API and Integration Design
Contracts, versioning, authentication, authorisation, idempotency, rate limiting, retry and dead-letter handling, error models, correlation identifiers, timeouts. Document each integration (template A.5).

**Deliverable:** API and Integration Specification.

### 5.6 Security and Privacy Design
Threat model, roles and permissions, secret management, dependency policy, input validation, data protection and consent, audit logging, POPIA alignment.

**Deliverable:** Security and Privacy Design.

### 5.7 Performance and Scalability Design
Performance budget, caching strategy (CDN, dispatcher or full-page caching, application cache), indexing strategy, query design, load model and capacity assumptions.

**Deliverable:** Performance and Capacity Design.

### 5.8 Observability Design
Log structure, metrics, traces, dashboards, alerts, business-transaction monitoring, error budgets.

### 5.9 Architecture Decision Records
Record each significant decision, its options, rationale, consequences and the product facts relied on (template A.1).

### 5.10 Phase 2 Exit Criteria (Gate E2)
- Architecture, component, data, integration, security, performance and observability designs approved.
- Product facts re-verified with dates (§1.5).
- Unsupported-extension decisions have approved ADRs.
- Estimates reviewed against the design.

**Final Deliverable:** Approved Technical Design Package.
