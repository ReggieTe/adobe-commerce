# PHASE 6: TESTING AND CUTOVER

> Part of the *Adobe DXP Downscale Playbook* v1.0 (Review Draft). Section numbers (§) refer to the playbook's original numbering; see the root [README](../README.md) for the section map.

## 11. Phase 6 – Testing and Cutover

### 11.1 Test Strategy
Scope, environments, data, ownership, entry and exit criteria, defect severity, regression and acceptance.

### 11.2 Functional Testing
Registration, login, account, browse, search, cart, checkout, payments, refunds, orders, emails, content publishing, admin, reports and promotions. Compare behaviour against the capability matrix.

### 11.3 SEO and Redirect Testing
Crawl the old URLs and verify each redirects correctly in one hop to the right page. Check canonicals, sitemaps, robots, hreflang, structured data, metadata, mobile rendering and page speed. Check that no staging settings (noindex, blocked robots) go live.

### 11.4 Integration and Payment Testing
ERP, inventory, shipping, tax, email, CRM and analytics. Payment success, failure, 3-D Secure, refunds, partial refunds and webhooks. Test failure and retry paths.

### 11.5 Performance Testing
Normal and peak load, checkout performance, search, API throughput and caching. Test realistic journeys.

### 11.6 Security Testing
Authentication, authorisation, admin access, input validation, dependency and plugin scanning, configuration review, secrets, TLS and logging.

### 11.7 User Acceptance Testing
Business scenarios, content and merchandising processes, order handling, finance reconciliation and customer service flows. Obtain signed approval.

### 11.8 Operational Readiness
Monitoring, alerts, incident handling, backup and restore, deployment and rollback, DR and access management. **The operational owner takes part.**

### 11.9 Cutover Plan
Pre-cutover checks (approvals, backups, support cover, communications), content and catalogue freeze window, final delta extraction, final load, DNS/traffic switch with reduced TTLs set in advance, integration switchover, production validation, go-live approval, and post-cutover monitoring. Use the runbook template (up-scale A.7) with a DNS, redirect and SEO section.

**Deliverable:** Approved Cutover Runbook (diagram: Appendix C.3).

### 11.10 Rollback and Fallback
Keep Adobe running (read-only or frozen where possible) for the agreed fallback window. Define triggers, authority and time limits. Orders created on the new platform after cutover must be handled in any rollback; where reversal is impractical define forward recovery instead. Do not let the Adobe contract expire during the fallback window.

**Deliverable:** Rollback and Fallback Plan.

### 11.11 Go-Live Approval
The client decides, informed by functional, integration, data, SEO, security, performance and operational evidence, outstanding risks and fallback readiness. The consultant recommends only.

### 11.12 Phase 6 Exit Criteria (Gate D6)
- Tests passed or risks accepted; UAT signed.
- Redirect and SEO tests passed.
- Data reconciled; payments verified in production.
- Cutover completed and validated.
- **Operational owner appointed** and trained.
- Hypercare active; Adobe fallback window and its end date confirmed.

**Final Deliverable:** Go-Live and Cutover Acceptance Report.
