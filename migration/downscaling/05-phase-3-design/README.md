# PHASE 3: DESIGN

> Part of the *Adobe DXP Downscale Playbook* v1.0 (Review Draft). Section numbers (§) refer to the playbook's original numbering; see the root [README](../README.md) for the section map.

## 8. Phase 3 – Target Design

### 8.1 Objective
Design the target platform and the migration in enough detail that build teams make no major decisions.

### 8.2 Target Solution Architecture
Components, hosting, integrations, data stores, CDN, search, payments, tax, shipping, email, analytics, backups, environments. Distinguish vendor-managed from client-managed parts.

**Deliverable:** Target Solution Architecture (diagram: Appendix C.2).

### 8.3 Data Model and Source-to-Target Mapping
Map every in-scope entity and field from Adobe to the target (§17 and the target playbooks in §13–§16). Document transformations, defaults, validation, owner, and treatment for fields with no equivalent (store as metadata, custom field, archive, or drop with sign-off).

**Deliverable:** Source-to-Target Mapping Specification.

### 8.4 URL, Redirect and SEO Design
- Map every indexed URL to a new URL or a retirement decision.
- Define canonical, hreflang, sitemap, robots and structured-data approach.
- Account for target URL constraints (for example fixed path prefixes on some platforms).
- Plan redirect implementation (server rules, plugin, platform redirects) and its limits.
- Plan image URL and media path changes.

**Deliverable:** URL Mapping and SEO Migration Design (template A.5).

### 8.5 Infrastructure and Hosting Design
Environments, hosting model, scaling, caching, CDN, WAF, backups, DR (RPO and RTO), monitoring, CI/CD, secrets. For Shopify, define what sits outside the platform (apps, middleware, archive).

**Deliverable:** Infrastructure and Hosting Specification.

### 8.6 Integration Design
Interfaces, authentication, error handling, idempotency, retries, monitoring, and cutover switching of each integration.

**Deliverable:** Integration Design.

### 8.7 Security, Privacy and Compliance Design
Roles and admin access, MFA, secrets, PCI approach (hosted payment fields), POPIA controls, consent model, data access in the archive, audit logging.

**Deliverable:** Security and Compliance Design.

### 8.8 Observability and DR Design
Uptime, checkout success, order flow, integration health, payment failures, search and error rates, SEO monitoring (crawl errors, indexation). Define alerts and owners.

**Deliverable:** Observability and DR Design.

### 8.9 Support and Operating Model Design
L1–L3 and vendor escalation (target platform, host, gateway, apps). Name the operational owner or the appointment plan.

**Deliverable:** Target Operating Model and Support Design.

### 8.10 Phase 3 Exit Criteria (Gate D3)
- Architecture, data mapping, URL and SEO design approved.
- Hosting, integration, security, observability, DR and support designs approved.
- Product-specific facts re-verified against current documentation, with dates.
- Decisions recorded in the ADR register.

**Final Deliverable:** Approved Target Design Package.
