# PHASE 5: EXTRACTION AND DATA MIGRATION

> Part of the *Adobe DXP Downscale Playbook* v1.0 (Review Draft). Section numbers (§) refer to the playbook's original numbering; see the root [README](../README.md) for the section map.

## 10. Phase 5 – Extraction and Data Migration

### 10.1 Objective
Export from Adobe, transform, load, rehearse and reconcile, and archive what must be retained. Preserve integrity, history and compliance. Phase 5 starts when D4 tooling exists and ends at D5 with reconciliation evidence.

### 10.2 Extraction Execution by Source
Follow §2.2. Plan around rate limits, volume and the contract end date.

- **Commerce SaaS:** schedule API extraction early; checkpoint and resume; verify counts.
- **Commerce PaaS or on-premises:** use supported database or backup routes; extract from a snapshot to avoid load on production.
- **AEM:** export content packages and assets with metadata; keep the repository structure for mapping.
- **AEP:** export datasets and audiences to agreed storage; document the schema.
- **Analytics:** start raw data exports early because of retention windows.

Store extracts in encrypted, access-controlled storage with a record of who accessed them. Extracts of personal data are subject to POPIA and must be deleted after the migration according to the retention decision.

**Deliverable:** Extraction Log and Verified Source Extracts.

### 10.3 Transformation and Cleansing
Apply approved rules. Remove duplicates, fix invalid values, resolve orphaned records and standardise addresses and phone formats. Never silently discard business data without an approved rule.

### 10.4 Load
Load in dependency order, for example: configuration, catalogue, customers, content and assets, orders, then redirects. Use target-supported import mechanisms and respect rate limits.

### 10.5 Content and Assets
Map content types, convert structured content to the target's model, rebuild components that have no equivalent, migrate assets with metadata and alt text, regenerate image renditions and validate link integrity. Preserve rights and expiry metadata where assets have licensing limits.

### 10.6 Customers, Consent and Passwords
- Migrate only customers in scope under the data strategy.
- Migrate consent with timestamp and source, or re-collect it where evidence cannot move.
- **Passwords:** hashing formats and import support vary by source and target. Do not assume portability. Options: invite or reset on first login; support the legacy hash temporarily through a controlled mechanism and rehash on login (where the target allows it); or use an external identity provider. Plan customer communications.
- Payment tokens held by Adobe-connected gateways may or may not be portable. Confirm with the payment provider. Never export card data.

### 10.7 Orders and History
Decide import depth. Imported historical orders should be marked as historical so they do not trigger emails, stock changes or accounting events. Maintain order numbers or keep a cross-reference. Ensure refunds, invoices and credit notes are preserved or archived.

### 10.8 Rehearsals
Run at least one full-volume rehearsal covering extraction, transformation, load, redirects, reconciliation and recovery. Record durations and fix issues. Repeat after material change.

**Deliverable:** Migration Rehearsal Report.

### 10.9 Reconciliation
Compare counts and totals: customers, products, categories, orders, order values, tax totals, stock, content items, assets and redirects. Business owners and finance approve the reconciliation of financial values.

**Deliverable:** Reconciliation and Acceptance Report.

### 10.10 Archive
Create the retention archive for records not migrated: format (open and readable), storage, encryption, access controls, search capability, retention period and destruction date. Test that archived records can be retrieved.

**Deliverable:** Archive and Retrieval Plan with test evidence.

### 10.11 Phase 5 Exit Criteria (Gate D5)
- Extraction verified; mappings applied.
- Full-volume rehearsal completed and reconciled.
- Password, consent and token strategy agreed.
- Archive created and tested.
- Redirect map loaded and tested in staging.
- Business and finance approval of migrated data.
- Production migration and fallback steps documented.

**Final Deliverable:** Approved Migration and Reconciliation Package.
