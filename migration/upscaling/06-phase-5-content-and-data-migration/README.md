# PHASE 5: CONTENT AND DATA MIGRATION

> Part of the *Enterprise Adobe DXP Migration Handbook* v1.1 (Review Draft). Section numbers (§) refer to the handbook's original numbering; see the root [README](../README.md) for the section map.

## 8. Phase 5 – Content and Data Migration

### 8.1 Objective
Transfer required content, data, configuration and records into the target, preserving integrity, relationships, historical requirements and continuity. This is not a database export and import. Phase 5 begins once G4 tooling exists and runs in parallel with Phase 4 hardening and Phase 6 testing; it ends at G5 with reconciliation evidence.

### 8.2 Migration Scope Confirmation
- **Customer data:** accounts, profiles, addresses, preferences, consent, groups.
- **Commerce data:** products, categories, pricing, promotions, orders, items, payments, refunds, transactions, invoices, shipments.
- **Content:** pages, articles, assets, images, documents, metadata, relationships, navigation.
- **Configuration:** store configuration, roles, permissions, tax, shipping, payment, business rules.
- **Operational data:** audit history, reporting records, integration references, subscriptions.

Not every category belongs in Adobe; some remain authoritative externally or are archived.

**Deliverable:** Approved Migration Scope Register.

### 8.3 Source-to-Target Mapping
For every mapping: source system, entity, field; target system, entity, field; transformation rule; validation rule; default; data owner; treatment. Document fields with no target equivalent.

**Deliverable:** Source-to-Target Data Mapping Specification (template: Appendix A.3).

### 8.4 Data Cleansing and Preparation
Identify duplicates, invalid values, missing mandatory fields, orphaned relationships, inconsistent formats, obsolete records, invalid references, incorrect history. Agree treatment with business owners. Never silently discard or modify business data without an approved rule.

**Deliverable:** Data Cleansing and Preparation Report.

### 8.5 Migration Architecture and Execution
Mechanisms: direct database extraction, platform APIs, export files, ETL pipelines, custom services, middleware, batch processing, incremental synchronisation. Establish sequence, batch sizes, rate limits, error handling, retry, logging, validation and rollback or recovery.

**Deliverable:** Migration Execution Plan.

### 8.6 Content Migration
Map content types, page structures, metadata and assets; preserve relationships; review URLs and establish redirect rules; validate rendering, publishing workflows and ownership; support the governance model.

**Deliverable:** Validated Content Migration.

### 8.7 Customer and Business Data Migration
Pay attention to customer identity, account relationships, orders and transactions, payment references, history, consent and preferences, product relationships and ownership.

Passwords, payment tokens and other credentials require product-specific procedures and must not be assumed portable. Where records cannot migrate directly, define account reactivation, credential reset, archival access or integration with the authoritative system. Consent records must be migrated with their evidence, not re-assumed.

**Deliverable:** Migrated Business Data.

### 8.8 Integration Reconfiguration
Update endpoints, authentication, identifiers, webhook destinations, event subscriptions; validate synchronisation, message processing, external references and failure handling, especially for systems that continue on legacy platforms during phased migration.

**Deliverable:** Updated and Validated Integration Configuration.

### 8.9 Migration Rehearsals
Rehearse before cutover, validating extraction, transformation, import, data and relationship integrity, performance, execution duration, error handling, reconciliation and recovery. Repeat after material issues. Record durations to refine the production plan.

**Deliverable:** Migration Rehearsal Report.

### 8.10 Data Reconciliation
Compare source and target record counts (customers, products, orders), transaction totals, financial values, relationships, content and assets, and exception counts. Business owners approve material financial and business-data results.

**Deliverable:** Data Reconciliation and Acceptance Report.

### 8.11 Phase 5 Exit Criteria (Gate G5)
- Scope approved; mappings complete; data prepared.
- Processes repeatable; at least one full-volume rehearsal completed and reconciled.
- Major exceptions resolved or accepted; business owners approve migrated data.
- Production migration and rollback or recovery procedures documented.

**Final Deliverable:** Approved Migration and Reconciliation Package.

### 8.12 Source-Platform Migration Notes (new)
Each source platform has constraints that must be assessed in Discovery and confirmed in rehearsal. Treat the table as a checklist of questions, and verify details against current platform documentation.

| Source | Typical considerations |
|---|---|
| **Shopify** | Data access via export tools and APIs with rate limits; hosted platform so no database access; password hashes not exportable (plan customer reset); gift cards, discounts and apps' data may need separate extraction; order history may need archive or import-as-historical approach |
| **WooCommerce** | Database-level access usually possible; plugin-specific tables and custom post meta need mapping; multiple password hash formats; variable products and attributes map non-trivially to configurable products |
| **PrestaShop** | Database access usually possible; multistore and multilingual structures need careful mapping; module-specific data; hash format differs from Adobe Commerce |
| **Existing Adobe Commerce** | Closest model, but version differences, custom attributes, third-party extension data and deprecated APIs need assessment; consider upgrade rather than migration where the deployment model allows |
| **Custom PHP/Symfony or portals** | No standard export; schema and business rules reside in code; reverse-engineer the data model and rules; undocumented integrations are the main risk |
| **Legacy CMS** | Content in templates and shortcodes; asset metadata inconsistency; URL structure and SEO preservation; component mapping to AEM |

Common to all: customer password and payment-token portability, consent evidence, order history treatment, SEO and URL redirects, search index rebuild, and tax and currency fidelity.
