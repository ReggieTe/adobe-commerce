# PHASE 4: BUILD AND CONFIGURATION

> Part of the *Adobe DXP Downscale Playbook* v1.0 (Review Draft). Section numbers (§) refer to the playbook's original numbering; see the root [README](../README.md) for the section map.

## 9. Phase 4 – Build and Configuration

### 9.1 Objective
Prepare the target platform, integrations and migration tooling. Under Model B the consultant directs and reviews; the named build team implements.

### 9.2 Environment Provisioning
Provision environments, hosting, domains (staging), certificates, CDN, backups, secrets, access. For Shopify, set up the store, markets, locations and staff roles.

### 9.3 Core Platform Configuration
Catalogue structure, attributes, taxes, currencies, shipping zones and methods, promotions, customer groups, email templates, roles and permissions, legal pages, consent mechanisms.

### 9.4 Theme and Frontend
Implement the agreed storefront design, accessibility and performance targets. Remove Adobe scripts and tags; add replacements.

### 9.5 Integrations, Payments, Tax and Shipping
Implement and test each integration. Configure payment gateways and test card, refund and failure flows. Configure tax and shipping providers.

### 9.6 Migration Tooling
Build extraction, transformation, load and reconciliation tools. Make them repeatable, logged and rate-limit aware. D4 requires the tooling to run end to end on sample data; D5 requires full-volume rehearsals.

### 9.7 Analytics and Marketing Replacement
Implement the replacement analytics, tag management, email and CRM connections. Plan baseline continuity (define how old and new metrics will be compared).

### 9.8 Security, Monitoring and Backups
Apply the security design, install monitoring, schedule and test backups, validate restore.

### 9.9 Documentation During Build
Architecture decisions, configuration, deployment steps, integration specs, mappings, runbooks, known limitations.

### 9.10 Phase 4 Exit Criteria (Gate D4)
- Environments and core configuration complete.
- Integrations and payments technically validated.
- Migration tooling runs on sample data.
- Security, monitoring and backups operational.
- Consultant review of code and configuration complete (Models B/C).
- Documentation current.

**Final Deliverable:** Target Platform Ready for Testing.
