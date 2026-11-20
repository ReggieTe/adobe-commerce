# 18. Adobe Decommissioning and Contract Exit

> Part of the *Adobe DXP Downscale Playbook* v1.0 (Review Draft). Section numbers (§) refer to the playbook's original numbering; see the root [README](../README.md) for the section map.

## 18.1 Principle
Decommissioning happens only after the fallback window closes, the business confirms stability, and required data is verified in the target or the archive. The client issues all notices and approvals; the consultant prepares the checklist and evidence.

## 18.2 Sequence
1. **Confirm** the fallback window is over and the new platform is stable (D6 evidence plus hypercare results).
2. **Take final backups** and exports of everything not otherwise preserved; verify them in the archive.
3. **Freeze** Adobe environments (read-only where possible) and block public access.
4. **Remove** Adobe tags, scripts, SDKs, webhooks and API calls from sites and applications; confirm no traffic or integrations still call Adobe.
5. **Revoke** access: admin users, IMS organisation roles, API credentials, integration keys, service accounts, SSH keys, repository access, CDN and DNS entries, certificates, and secrets held by other systems.
6. **Terminate** subscriptions per the contract: serve notice in time, confirm the end date in writing, and settle final invoices.
7. **Request data deletion**: ask for written confirmation of deletion of client data from Adobe-managed systems after the contractual retention period, and file the evidence.
8. **Delete or secure** local extracts, staging copies and temporary stores of personal data once the retention decision is applied.
9. **Update** records: vendor register, asset and licence registers, architecture documentation, DR plans and monitoring (remove Adobe checks).
10. **Close** with a signed decommissioning report.

## 18.3 Retention and Deletion
Keep records only as long as law and business need require (tax, accounting, legal claims, consent evidence). Confirm periods with counsel and finance. Document deletions with date, scope, method and approver. POPIA's retention-limitation principle applies to extracts and archives.

## 18.4 Evidence Pack
Notices and acknowledgements, final invoices, access revocation log, tag removal evidence, backup and archive verification, deletion confirmations, updated registers. Keep for the audit period set by the client.

**Deliverable:** Adobe Decommissioning Report (checklist: Appendix B.7).
