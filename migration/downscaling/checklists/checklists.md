# Checklists

> Part of the *Adobe DXP Downscale Playbook* v1.0 (Review Draft). Section numbers (§) refer to the playbook's original numbering; see the root [README](../README.md) for the section map.

## B.1 Exit discovery (D1)
- [ ] Contract timeline with latest safe notice and cutover dates
- [ ] Extraction entitlement confirmed for each data class
- [ ] Estate, data, integration and tag inventories complete
- [ ] Traffic and SEO baseline captured
- [ ] Retention and compliance requirements recorded
- [ ] Driver for downscale agreed

## B.2 Strategy (D2)
- [ ] Capability loss register signed
- [ ] Target platform decision record signed
- [ ] Data migrate/archive/purge decisions approved
- [ ] Overlap period and budget approved
- [ ] Operating model intent recorded

## B.3 Design (D3)
- [ ] Data mapping complete, including fields without equivalents
- [ ] URL and SEO design approved
- [ ] Platform limits verified (variants, redirects, rate limits, order import behaviour)
- [ ] Payment, tax and shipping design confirmed for the market
- [ ] Product facts re-verified with dates

## B.4 Build (D4)
- [ ] Integrations and payments technically validated
- [ ] Migration tooling runs end to end on sample data
- [ ] Adobe tags replaced in the new site
- [ ] Monitoring, backups and restore tested
- [ ] Consultant review complete

## B.5 Migration readiness (D5)
- [ ] Full-volume rehearsal timed and reconciled
- [ ] Finance approval of order and tax reconciliation
- [ ] Customer password and consent strategy agreed and communicated
- [ ] Archive created, encrypted and retrieval-tested
- [ ] Redirect map loaded and tested in staging

## B.6 Go-live (D6)
- [ ] Functional, integration, payment, performance, security and SEO tests passed or risks accepted
- [ ] UAT signed
- [ ] DNS TTLs lowered; backups verified
- [ ] Staging noindex and robots blocks removed
- [ ] Operational owner appointed and trained
- [ ] Fallback window and Adobe end date confirmed

## B.7 Adobe decommissioning and handover (D7)
**Entry condition**
- [ ] Operational owner accepted in writing (or fallback executed)
- [ ] Adobe termination actions complete or scheduled with owners and dates

**Decommissioning**
- [ ] Final backups and exports verified
- [ ] Adobe environments frozen and public access blocked
- [ ] Adobe tags, SDKs, webhooks and API calls removed
- [ ] Admin users, IMS roles, API keys, service accounts, SSH keys revoked
- [ ] DNS, CDN, certificate and secret entries cleaned up
- [ ] Notices served and acknowledged; final invoices settled
- [ ] Written deletion confirmation received after retention period
- [ ] Local extracts and temporary copies deleted per retention decision
- [ ] Registers and monitoring updated

**Handover**
- [ ] Documentation and training complete
- [ ] SEO recovery within tolerance or plan accepted
- [ ] Archive access tested
- [ ] Outstanding defects, risks and technical debt recorded
- [ ] Client acceptance signed
