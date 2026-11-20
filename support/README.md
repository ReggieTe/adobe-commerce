# ENTERPRISE ADOBE DXP SUPPORT AND OPERATIONS HANDBOOK
## Consultant-Led Service Design, Transition and Operations for Adobe DXP

**Document type:** Enterprise Service and Operations Handbook
**Version:** 1.0
**Status:** Proposed Baseline
**Scope:** Supporting and operating Adobe DXP (AEM, Adobe Commerce, Adobe Experience Platform and included Experience Cloud modules) after go-live
**Companions:** *Enterprise Adobe DXP Migration Handbook* (up-scale), *Adobe DXP Downscale Playbook*, *Enterprise Adobe DXP Development Handbook*
**Intended audience:** Support Consultants, Service Managers, Technical Leads, Operations Teams, Managed Service Providers, Client IT Teams and Business Stakeholders

### How this handbook relates to the other handbooks

| Topic | Migration handbooks | Development handbook | This handbook |
|---|---|---|---|
| Question answered | How do we get onto or off Adobe DXP? | How do we build and change things? | How do we run it and keep it healthy? |
| Gates | G1–G7, D1–D7 | E1–E7 | **S1–S7** |
| Ends with | Handover and closure | Developer handover | Service review, renewal or transition-out |
| Shared material | Engagement models, "verify" convention, operational-owner rule, template style | Reused | Reused by reference and adapted |

---

## Folder structure

```
00-overview/              Introduction, lifecycle, success and closing principle
01-support-landscape/     Shared responsibility, support tiers, product operational concerns
02 ... 08-phase-*/        One folder per service phase (gates S1-S7)
09-product-operations/    AEM, Commerce, AEP, Experience Cloud, integrations: daily/weekly/monthly
10-governance/            Gates, RACI, change control, commercial framework
templates/                Service catalogue, SLA, runbook, incident, PIR, report and more
checklists/               Gate, routine-operations and major-incident checklists
diagrams/                 Mermaid lifecycle, tiers and incident-flow diagrams
```

## Section map

| Handbook section | File |
|---|---|
| §1 Introduction, engagement models | [00-overview/01-introduction.md](00-overview/01-introduction.md) |
| §2 Support landscape, tiers, shared responsibility | [01-support-landscape/01-adobe-support-landscape.md](01-support-landscape/01-adobe-support-landscape.md) |
| §3 Service lifecycle overview | [00-overview/02-lifecycle-overview.md](00-overview/02-lifecycle-overview.md) |
| §4 Phase 1 – Service discovery | [02-phase-1-service-discovery/README.md](02-phase-1-service-discovery/README.md) |
| §5 Phase 2 – Service design | [03-phase-2-service-design/README.md](03-phase-2-service-design/README.md) |
| §6 Phase 3 – Transition-in | [04-phase-3-transition-in/README.md](04-phase-3-transition-in/README.md) |
| §7 Phase 4 – Live operations | [05-phase-4-live-operations/README.md](05-phase-4-live-operations/README.md) |
| §8 Phase 5 – Continual improvement | [06-phase-5-continual-improvement/README.md](06-phase-5-continual-improvement/README.md) |
| §9 Phase 6 – Lifecycle and upgrades | [07-phase-6-lifecycle-and-upgrades/README.md](07-phase-6-lifecycle-and-upgrades/README.md) |
| §10 Phase 7 – Review, renewal or transition-out | [08-phase-7-review-renewal-or-transition-out/README.md](08-phase-7-review-renewal-or-transition-out/README.md) |
| §11 Product-specific operations | [09-product-operations/01-product-specific-operations.md](09-product-operations/01-product-specific-operations.md) |
| §12 Governance, gates, RACI | [10-governance/01-governance-gates-raci.md](10-governance/01-governance-gates-raci.md) |
| §13 Success and closing principle | [00-overview/03-success-and-closing.md](00-overview/03-success-and-closing.md) |
| Appendix B Checklists | [checklists/checklists.md](checklists/checklists.md) |
| Appendix C Diagrams | [diagrams/reference-diagrams.md](diagrams/reference-diagrams.md) |

## Templates (former Appendix A)

- [A.1](templates/a01-service-catalogue.md) – Service Catalogue
- [A.2](templates/a02-sla-summary.md) – SLA Summary
- [A.3](templates/a03-runbook.md) – Runbook
- [A.4](templates/a04-incident-record.md) – Incident Record
- [A.5](templates/a05-post-incident-review.md) – Post-Incident Review
- [A.6](templates/a06-problem-record.md) – Problem Record
- [A.7](templates/a07-monitoring-and-alerting-catalogue.md) – Monitoring and Alerting Catalogue
- [A.8](templates/a08-service-component-register.md) – Service Component Register
- [A.9](templates/a09-monthly-service-report.md) – Monthly Service Report
- [A.10](templates/a10-service-owner-and-provider-appointment-form.md) – Service Owner and Provider Appointment Form

## Conventions

- Product statements follow the "verify" convention: confirm against current vendor documentation and record a *Last verified* date.
- This handbook is not legal advice. Contract and compliance sections are checklists for counsel review.
- Part of the **Adobe** repository. See the [main README](../README.md).
