# ADOBE DXP DOWNSCALE PLAYBOOK
## Consultant-Led Migration from Adobe DXP to WooCommerce, PrestaShop, Shopify or a Custom Platform

**Document type:** Enterprise Technical and Delivery Playbook
**Version:** 1.0
**Status:** Proposed Baseline
**Migration direction:** Adobe Digital Experience Platform (DXP) → WooCommerce | PrestaShop | Shopify | Custom platform
**Companion to:** *Enterprise Adobe DXP Migration Handbook v1.1* (the up-scale direction, see [`../upscaling`](../upscaling/README.md))
**Intended audience:** Consultants, Technical Leads, Enterprise Architects, Project Managers, Client IT Teams and Business Stakeholders

### How this playbook relates to the up-scale handbook

| Topic | Up-scale handbook v1.1 | This playbook |
|---|---|---|
| Direction | Existing platforms → Adobe DXP | Adobe DXP → simpler platform |
| Core risk | Under-designed target architecture | **Lost capability, lost data, lost traffic, and a hard Adobe contract end date** |
| Gates | G1–G7 | **D1–D7** (to avoid confusion) |
| Phases | 7, from Discovery to Handover | 7, from Exit Discovery to Handover **and Adobe decommissioning** |
| Closure rule | Named operational owner required to exit (§10.8) | Same rule applies, plus confirmed Adobe termination actions (§12.7) |
| Shared material | Engagement models, RACI approach, "verify" convention, template style | Reused by reference and adapted |

---

## Repository structure

```
00-overview/              Introduction, engagement models, lifecycle, success and closing principle
01-source-landscape/      What is being left: Adobe estate, extraction routes, contract and entitlement
02-target-platforms/      Selection framework, capability rationalisation, WooCommerce, PrestaShop,
                          Shopify, custom platform playbooks, entity mapping reference
03 … 09-phase-*/          One folder per lifecycle phase (gates D1–D7)
10-decommissioning/       Adobe decommissioning and contract exit
11-governance/            Gates, RACI, change control, risk seeds, commercial framework
templates/                Deliverable templates (former Appendix A)
checklists/               Gate and decommissioning checklists (former Appendix B)
diagrams/                 Mermaid reference diagrams (former Appendix C)
```

## Section map

| Playbook section | File |
|---|---|
| §1 Introduction, engagement models | [00-overview/01-introduction.md](00-overview/01-introduction.md) |
| §2 Source landscape | [01-source-landscape/01-adobe-source-landscape.md](01-source-landscape/01-adobe-source-landscape.md) |
| §3 Target platform selection | [02-target-platforms/01-target-selection-framework.md](02-target-platforms/01-target-selection-framework.md) |
| §4 Capability rationalisation | [02-target-platforms/02-capability-rationalisation.md](02-target-platforms/02-capability-rationalisation.md) |
| §5 Lifecycle overview | [00-overview/02-lifecycle-overview.md](00-overview/02-lifecycle-overview.md) |
| §6 Phase 1 – Exit discovery | [03-phase-1-exit-discovery/README.md](03-phase-1-exit-discovery/README.md) |
| §7 Phase 2 – Target selection and strategy | [04-phase-2-target-selection-and-strategy/README.md](04-phase-2-target-selection-and-strategy/README.md) |
| §8 Phase 3 – Design | [05-phase-3-design/README.md](05-phase-3-design/README.md) |
| §9 Phase 4 – Build | [06-phase-4-build-and-configuration/README.md](06-phase-4-build-and-configuration/README.md) |
| §10 Phase 5 – Extraction and migration | [07-phase-5-extraction-and-migration/README.md](07-phase-5-extraction-and-migration/README.md) |
| §11 Phase 6 – Testing and cutover | [08-phase-6-testing-and-cutover/README.md](08-phase-6-testing-and-cutover/README.md) |
| §12 Phase 7 – Hypercare and handover (exit rule §12.7) | [09-phase-7-hypercare-and-decommissioning/README.md](09-phase-7-hypercare-and-decommissioning/README.md) |
| §13 WooCommerce | [02-target-platforms/03-woocommerce.md](02-target-platforms/03-woocommerce.md) |
| §14 PrestaShop | [02-target-platforms/04-prestashop.md](02-target-platforms/04-prestashop.md) |
| §15 Shopify | [02-target-platforms/05-shopify.md](02-target-platforms/05-shopify.md) |
| §16 Custom platform | [02-target-platforms/06-custom-platform.md](02-target-platforms/06-custom-platform.md) |
| §17 Entity mapping reference | [02-target-platforms/07-entity-mapping-reference.md](02-target-platforms/07-entity-mapping-reference.md) |
| §18 Adobe decommissioning | [10-decommissioning/01-adobe-decommissioning.md](10-decommissioning/01-adobe-decommissioning.md) |
| §19 Governance, gates, RACI, commercial | [11-governance/01-governance-gates-raci.md](11-governance/01-governance-gates-raci.md) |
| §20 Success and closing principle | [00-overview/03-success-and-closing.md](00-overview/03-success-and-closing.md) |
| Appendix B Checklists | [checklists/checklists.md](checklists/checklists.md) |
| Appendix C Diagrams | [diagrams/reference-diagrams.md](diagrams/reference-diagrams.md) |

## Templates (former Appendix A)

- [A.1](templates/a01-adobe-contract-and-entitlement-register.md) – Adobe Contract and Entitlement Register
- [A.2](templates/a02-capability-rationalisation-matrix-and-loss-register.md) – Capability Rationalisation Matrix and Loss Register
- [A.3](templates/a03-target-platform-decision-record.md) – Target Platform Decision Record
- [A.4](templates/a04-source-to-target-mapping.md) – Source-to-Target Mapping
- [A.5](templates/a05-url-mapping-and-redirect-register.md) – URL Mapping and Redirect Register
- [A.6](templates/a06-downscale-risk-register.md) – Downscale Risk Register
- [A.7](templates/a07-data-retention-and-archive-register.md) – Data Retention and Archive Register
- [A.8](templates/a08-cutover-runbook-downscale-additions.md) – Cutover Runbook (downscale additions)
- [A.9](templates/a09-adobe-decommissioning-evidence-pack.md) – Adobe Decommissioning Evidence Pack
- [A.10](templates/a10-operational-owner-appointment-form.md) – Operational Owner Appointment Form

## Conventions

- Product and platform statements carry the "verify" convention (§1.7): confirm against current vendor documentation and record a *Last verified* date before gate D3.
- This playbook is not legal advice. Contract, POPIA and retention sections are checklists for counsel review.
- Companion handbook: [Upscaling](../upscaling/README.md). Part of the **Adobe** repository, see the [main README](../../README.md).
