# ENTERPRISE ADOBE DXP MIGRATION HANDBOOK
## Consultant-Led Platform Transformation and Operational Handover

**Document type:** Enterprise Technical and Delivery Handbook
**Version:** 1.1
**Status:** Proposed Baseline
**Migration direction:** Existing platforms → Adobe Digital Experience Platform (DXP)
**Intended audience:** Adobe DXP Implementation Consultants, Technical Leads, Enterprise Architects, Project Managers, Client IT Teams and Business Stakeholders

### Change summary from v1.0

| # | Decision | Change made |
|---|---|---|
| 1 | Product scope | AEM, Adobe Commerce and AEP are now the principal products; other Experience Cloud products are "include where required" modules (§2.1). Identity guidance clarified. |
| 2 | Hosting depth | New per-product deployment decision matrices (§2.3–2.5). Hybrid reframed as an integration pattern. POPIA/data residency tied to the hosting decision. |
| 3 | Technical depth | New Appendix A (templates), Appendix B (checklists), Appendix C (reference diagrams). Core phases remain methodology. |
| 4 | Accountability | New Engagement Models (§1.4) and phase-by-phase RACI (§12.5). Consultant defined as lead-and-assure by default. |
| 5 | Closure | Named operational owner is now a hard G7 entry condition, appointed by G6, with a defined fallback (§10.8, §12.2). |
| – | Other fixes | Phase 4/5 boundary clarified (§8.1); source-platform guidance added (§8.12); commercial and contractual section added (§12.6); product facts carry a "verify" convention (§2.2). |

---

## Repository structure

```
00-overview/            Introduction, engagement models, lifecycle, success definition, closing principle
01-adobe-landscape/     Adobe products, per-product deployment matrices, hosting and POPIA decisions
02-phase-1-discovery/ … 08-phase-7-hypercare-and-handover/   One folder per lifecycle phase (gates G1–G7)
09-governance/          Cross-phase governance, gates, RACI, commercial framework, deliverables summary
templates/              Deliverable templates (former Appendix A)
checklists/             Technical checklists (former Appendix B)
diagrams/               Mermaid reference diagrams (former Appendix C)
```

## Section map

| Handbook section | File |
|---|---|
| §1 Introduction, engagement models (§1.4) | [00-overview/01-introduction.md](00-overview/01-introduction.md) |
| §2 Adobe DXP target environment, hosting, POPIA | [01-adobe-landscape/01-adobe-dxp-target-environment.md](01-adobe-landscape/01-adobe-dxp-target-environment.md) |
| §3 Lifecycle overview | [00-overview/02-lifecycle-overview.md](00-overview/02-lifecycle-overview.md) |
| §4 Phase 1 – Discovery | [02-phase-1-discovery/README.md](02-phase-1-discovery/README.md) |
| §5 Phase 2 – Assessment and Strategy | [03-phase-2-assessment-and-strategy/README.md](03-phase-2-assessment-and-strategy/README.md) |
| §6 Phase 3 – Design | [04-phase-3-design/README.md](04-phase-3-design/README.md) |
| §7 Phase 4 – Build | [05-phase-4-build-and-development/README.md](05-phase-4-build-and-development/README.md) |
| §8 Phase 5 – Migration (incl. §8.12 source-platform notes) | [06-phase-5-content-and-data-migration/README.md](06-phase-5-content-and-data-migration/README.md) |
| §9 Phase 6 – Testing and Cutover | [07-phase-6-testing-and-cutover/README.md](07-phase-6-testing-and-cutover/README.md) |
| §10 Phase 7 – Hypercare and Handover (incl. §10.8 exit rule) | [08-phase-7-hypercare-and-handover/README.md](08-phase-7-hypercare-and-handover/README.md) |
| §11 Cross-phase governance | [09-governance/01-cross-phase-governance.md](09-governance/01-cross-phase-governance.md) |
| §12 Gates, RACI (§12.5), commercial framework (§12.6) | [09-governance/02-project-governance-gates-raci.md](09-governance/02-project-governance-gates-raci.md) |
| §13 Deliverables summary | [09-governance/03-deliverables-summary.md](09-governance/03-deliverables-summary.md) |
| §14 Definition of success | [00-overview/03-definition-of-success.md](00-overview/03-definition-of-success.md) |
| §15 Closing principle | [00-overview/04-closing-principle.md](00-overview/04-closing-principle.md) |
| Appendix B Checklists | [checklists/technical-checklists.md](checklists/technical-checklists.md) |
| Appendix C Diagrams | [diagrams/reference-diagrams.md](diagrams/reference-diagrams.md) |

## Templates (former Appendix A)

- [A.1](templates/a01-current-platform-inventory.md) – Current Platform Inventory
- [A.2](templates/a02-application-disposition-matrix.md) – Application Disposition Matrix
- [A.3](templates/a03-source-to-target-mapping.md) – Source-to-Target Mapping
- [A.4](templates/a04-integration-register.md) – Integration Register
- [A.5](templates/a05-architecture-decision-record-adr.md) – Architecture Decision Record (ADR)
- [A.6](templates/a06-risk-register.md) – Risk Register
- [A.7](templates/a07-cutover-runbook.md) – Cutover Runbook
- [A.8](templates/a08-rollback-and-recovery-plan.md) – Rollback and Recovery Plan
- [A.9](templates/a09-handover-checklist.md) – Handover Checklist
- [A.10](templates/a10-raci.md) – RACI
- [A.11](templates/a11-operational-owner-appointment-form.md) – Operational Owner Appointment Form

## Conventions

- Product-specific statements must carry a *Last verified* date (see §2.2). Re-verify before G3.
- This handbook is not legal advice. The POPIA and contract sections are checklists for counsel review.
