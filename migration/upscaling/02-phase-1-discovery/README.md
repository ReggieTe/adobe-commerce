# PHASE 1: DISCOVERY

> Part of the *Enterprise Adobe DXP Migration Handbook* v1.1 (Review Draft). Section numbers (§) refer to the handbook's original numbering; see the root [README](../README.md) for the section map.

## 4. Phase 1 – Discovery

### 4.1 Objective
Establish a complete understanding of the existing business environment, platforms, architecture, infrastructure, data, integrations and operations: what exists, how it works, who depends on it and what the organisation expects. Do not assume every existing feature must be reproduced in Adobe DXP.

### 4.2 Business Discovery
Activities: identify business units and stakeholders; products and services; digital channels and customer journeys; business-critical and revenue-generating processes; acquisition and retention processes; regulatory obligations; pain points; growth plans; regional and international requirements.

Questions: What problems should migration solve? Which channels generate revenue? Which processes are critical? Which units depend on existing platforms? What are growth expectations? Are there country-specific requirements? Which capabilities must stay available during migration?

**Deliverable:** Business and Stakeholder Discovery Report.

### 4.3 Existing Platform Inventory
Platforms: custom portals and applications, WooCommerce, PrestaShop, Shopify, Adobe Commerce, other CMS, customer portals, internal admin applications, mobile apps, reporting and analytics platforms, legacy databases and services.

Per platform record: business purpose, owner, technology and version, hosting provider, deployment model, database technology, custom code and extensions, user groups, critical features, data volumes, external integrations, limitations, licensing and support, decommissioning or retention requirements.

**Deliverable:** Current Platform Inventory (template: Appendix A.1).

### 4.4 Application and Functionality Discovery
Capabilities to document: registration and authentication, customer accounts, catalogues, content management, product configuration, pricing and promotions, cart and checkout, payments and refunds, order management, customer service, search and navigation, personalisation, reporting, administration, user and role management.

Classify each: **Retain / Replace with Adobe / Rebuild as custom / Integrate with external system / Retire / Defer.** Distinguish business requirements from the technical implementation currently satisfying them.

**Deliverable:** Functional Capability Inventory.

### 4.5 Infrastructure Discovery
- **Compute:** servers, VMs, cloud instances, containers, runtimes, workers, scheduled jobs.
- **Storage:** databases, object and media storage, file systems, backups, retention.
- **Networking:** DNS, domains, certificates, firewalls, load balancers, VPNs, private networking, CDN, IP allowlisting, third-party connectivity.
- **Environments:** development, testing, staging, production, disaster recovery.
- **Operations:** monitoring, logging, deployment, backups, maintenance, capacity, patching.

Identify what can be retained, replaced, integrated or decommissioned.

**Deliverable:** Infrastructure and Hosting Inventory.

### 4.6 Middleware and Integration Discovery
Mechanisms: API gateways, ESB, iPaaS, message brokers, event streaming, custom integration services, scheduled jobs, webhooks, direct database integrations, file-based integrations. Technologies such as MuleSoft, Boomi, Azure Integration Services, Kafka, RabbitMQ, Apigee, Kong and Azure API Management are examples only.

Per integration record: source, destination, business purpose, owner, method, data exchanged, direction, frequency, authentication, error handling, retry behaviour, transformation, impact of failure, monitoring, vendor dependency.

**Deliverable:** Middleware and Integration Register (template: Appendix A.4).

### 4.7 Third-Party Systems Discovery
Categories: ERP, CRM, PIM, OMS, WMS, payment gateways, fraud detection, tax, shipping and logistics, identity providers, marketing automation, analytics, search, customer support, email and SMS, finance and accounting. Establish whether each is retained, replaced, redesigned or removed.

**Deliverable:** Third-Party Dependency Register.

### 4.8 Data Discovery
Sources: customers, addresses, products, categories, orders, payments, refunds, transactions, content, media, promotions, subscriptions, preferences, consent records, roles, audit history.

Record: source, database technology, approximate record count, volume, ownership, sensitivity, quality, retention, relationships, dependencies, duplication, historical requirements. Decide whether historical data is migrated, archived, integrated or retained in the legacy environment.

**Deliverable:** Data Source and Ownership Inventory.

### 4.9 Security and Compliance Discovery
Activities: identify authentication and authorisation mechanisms; review roles and permissions; privileged accounts; API authentication; certificate and secret management; encryption; personal and sensitive information; data residency; regulatory requirements; audit logging; security monitoring; vulnerability and patch management.

For South African operations, assess POPIA obligations, plus any other operating jurisdictions. Feed findings directly into the residency check in §2.5.

**Deliverable:** Security and Compliance Discovery Report.

### 4.10 Discovery Consolidation
Consolidate into a single current-state view: capabilities, dependencies, business-critical systems, infrastructure constraints, integration complexity, data risks, operational weaknesses, vendor dependencies, limitations, missing information, initial risks.

### 4.11 Phase 1 Exit Criteria (Gate G1)
- Business environment documented; platforms inventoried; major capabilities identified.
- Infrastructure, hosting, middleware and third-party dependencies understood.
- Major data sources identified; security and compliance considerations recorded.
- Stakeholders reviewed findings; gaps have owners and resolution plans.
- **The engagement model (§1.4) and any implementation partner are confirmed in writing.**

**Final Deliverable:** Current-State Discovery and Technical Landscape Report.
