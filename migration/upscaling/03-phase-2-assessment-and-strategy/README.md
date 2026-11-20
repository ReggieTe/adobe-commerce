# PHASE 2: ASSESSMENT AND STRATEGY

> Part of the *Enterprise Adobe DXP Migration Handbook* v1.1 (Review Draft). Section numbers (§) refer to the handbook's original numbering; see the root [README](../README.md) for the section map.

## 5. Phase 2 – Assessment and Strategy

### 5.1 Objective
Evaluate the current environment against business objectives and determine the most appropriate migration strategy. Discovery establishes what exists; assessment determines what should change, remain, be replaced and how.

### 5.2 Business and Capability Gap Assessment
For each capability determine: native Adobe capability? Configuration sufficient? Custom development? External integration? Redesign? Retire? Cover functional, technical, data, integration, security, operational, performance and scalability gaps.

**Deliverable:** Business and Technical Gap Analysis.

### 5.3 Adobe Product Suitability Assessment
Start from the three principal products (§2.1), then justify any additional modules. Evaluate functionality, maturity, licensing, customisation, APIs, integration support, deployment model, performance, limitations, roadmap considerations and inter-product dependencies. Apply the "verify" convention (§2.2).

**Deliverable:** Adobe DXP Product and Capability Mapping.

### 5.4 Hosting and Infrastructure Strategy
Complete the per-product deployment matrix and decision matrix (§2.3–2.4) and the residency assessment (§2.5). Distinguish Adobe-managed services, Adobe cloud infrastructure, customer-managed infrastructure and external hosting.

Total cost of ownership must include: Adobe licensing, hosting, infrastructure, middleware, integration services, third-party subscriptions, development, support, monitoring, backup and DR, security and compliance, future scaling.

**Deliverable:** Hosting and Infrastructure Strategy, including the signed Hosting Decision Record.

### 5.5 Application Migration Strategy
Approaches: **Replatform, Replace, Rebuild, Integrate, Retire, Retain temporarily.** Document the selected approach per application and capability.

**Deliverable:** Application Migration Strategy and Disposition Matrix (template: Appendix A.2).

### 5.6 Data Migration Strategy
Consider full, incremental and delta migration, historical migration, archiving, cleansing, transformation, reconciliation, sequencing, ownership and cutover requirements. Identify source-to-target mappings and treatment of records without direct equivalents.

**Deliverable:** Data Migration Strategy.

### 5.7 Middleware and Integration Strategy
Assess existing middleware suitability, API management, event-driven needs, transformation, message reliability, retry and failure handling, security, monitoring and tracing, throughput, vendor support and operational ownership. Decide direct, mediated, event-driven or other patterns.

**Deliverable:** Middleware and Integration Strategy.

### 5.8 Security and Compliance Strategy
Cover identity and access management, RBAC, privileged access, API security, encryption, secrets, network security, data protection, audit logging, vulnerability management, security testing, regulatory compliance and the POPIA conclusion from §2.5. Define responsibilities among Adobe, hosting providers, vendors and the client.

**Deliverable:** Security and Compliance Strategy.

### 5.9 Migration Sequencing and Roadmap
Consider critical systems, platform and integration dependencies, data complexity, regulation, contracts, resources, budget, risk and downtime tolerance. Options: big-bang, phased, business-unit, country-by-country, channel-by-channel, capability-based. Recommend based on circumstances, not by default.

**Deliverable:** Migration Roadmap and High-Level Delivery Plan.

### 5.10 Risk, Cost and Resource Assessment
Identify technical, business, migration, security, vendor, budget, timeline, skills and operational risks. Estimate resources for architecture, development, infrastructure, data migration, integration, testing, security, business validation and operational support.

**Deliverable:** Initial Risk Register, Resource Plan and Cost Assessment.

### 5.11 Operating Model Intent (new)
Phase 2 must record the client's **intended** operating model for the live platform (internal team, MSP, specialist partner, or combination) and a date by which the operational owner will be appointed. The latest acceptable date is G6 (§10.8).

### 5.12 Phase 2 Exit Criteria (Gate G2)
- Target capabilities agreed; Adobe product suitability assessed.
- Hosting decision recorded per product, including residency conclusion.
- Application, data, integration, security strategies approved.
- Sequencing, budget, resource and risk assessments accepted.
- Intended operating model and appointment date recorded.

**Final Deliverable:** Approved Adobe DXP Migration Strategy and Programme Roadmap.
