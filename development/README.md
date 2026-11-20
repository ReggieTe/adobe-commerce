# ENTERPRISE ADOBE DXP DEVELOPMENT HANDBOOK
## Consultant-Led Engineering Lifecycle for AEM, Adobe Commerce and Adobe Experience Platform

**Document type:** Enterprise Engineering and Delivery Handbook
**Version:** 1.0
**Status:** Proposed Baseline
**Scope:** Designing, building, testing, releasing and handing over custom solutions on Adobe DXP
**Companions:** *Enterprise Adobe DXP Migration Handbook* (up-scale), *Adobe DXP Downscale Playbook*, *Enterprise Adobe DXP Support and Operations Handbook*
**Intended audience:** Adobe Developers, Technical Leads, Solution Architects, QA Engineers, DevOps Engineers, Project Managers, Client IT Teams and Business Stakeholders

### How this handbook relates to the other handbooks

| Topic | Migration handbooks | This handbook | Support handbook |
|---|---|---|---|
| Question answered | How do we get onto or off Adobe DXP? | How do we build and change things on Adobe DXP? | How do we run it day to day? |
| Gates | G1–G7 (up-scale), D1–D7 (downscale) | **E1–E7** | S1–S7 |
| Ends with | Handover and closure | Release, stabilisation and developer handover | Service review, renewal or transition-out |
| Shared material | Engagement models, "verify" convention, operational-owner rule, template style | Reused by reference and adapted | Reused by reference and adapted |

---

## Folder structure

```
00-overview/              Introduction, lifecycle, success and closing principle
01-adobe-landscape/       Development models and extension points per Adobe product
02 ... 08-phase-*/        One folder per lifecycle phase (gates E1-E7)
09-engineering-standards/ Branching, review, testing, security, performance, debt
10-governance/            Gates, RACI, change control, commercial framework
templates/                ADR, design doc, definition of done, review checklist, and more
checklists/               Gate checklists
diagrams/                 Mermaid lifecycle, architecture and CI/CD diagrams
```

## Section map

| Handbook section | File |
|---|---|
| §1 Introduction, engagement models | [00-overview/01-introduction.md](00-overview/01-introduction.md) |
| §2 Adobe development landscape | [01-adobe-landscape/01-adobe-development-landscape.md](01-adobe-landscape/01-adobe-development-landscape.md) |
| §3 Lifecycle overview | [00-overview/02-lifecycle-overview.md](00-overview/02-lifecycle-overview.md) |
| §4 Phase 1 – Requirements and discovery | [02-phase-1-requirements-and-discovery/README.md](02-phase-1-requirements-and-discovery/README.md) |
| §5 Phase 2 – Architecture and design | [03-phase-2-architecture-and-design/README.md](03-phase-2-architecture-and-design/README.md) |
| §6 Phase 3 – Foundations | [04-phase-3-foundations/README.md](04-phase-3-foundations/README.md) |
| §7 Phase 4 – Implementation (product guides §7.3) | [05-phase-4-implementation/README.md](05-phase-4-implementation/README.md) |
| §8 Phase 5 – Quality engineering | [06-phase-5-quality-engineering/README.md](06-phase-5-quality-engineering/README.md) |
| §9 Phase 6 – Release and deployment | [07-phase-6-release-and-deployment/README.md](07-phase-6-release-and-deployment/README.md) |
| §10 Phase 7 – Stabilisation and handover | [08-phase-7-stabilisation-and-handover/README.md](08-phase-7-stabilisation-and-handover/README.md) |
| §11 Cross-cutting engineering standards | [09-engineering-standards/01-cross-cutting-standards.md](09-engineering-standards/01-cross-cutting-standards.md) |
| §12 Governance, gates, RACI | [10-governance/01-governance-gates-raci.md](10-governance/01-governance-gates-raci.md) |
| §13 Success and closing principle | [00-overview/03-success-and-closing.md](00-overview/03-success-and-closing.md) |
| Appendix B Checklists | [checklists/checklists.md](checklists/checklists.md) |
| Appendix C Diagrams | [diagrams/reference-diagrams.md](diagrams/reference-diagrams.md) |

## Templates (former Appendix A)

- [A.1](templates/a01-architecture-decision-record.md) – Architecture Decision Record
- [A.2](templates/a02-technical-design-document.md) – Technical Design Document
- [A.3](templates/a03-definition-of-ready-and-definition-of-done.md) – Definition of Ready and Definition of Done
- [A.4](templates/a04-code-review-checklist.md) – Code Review Checklist
- [A.5](templates/a05-integration-specification.md) – Integration Specification
- [A.6](templates/a06-test-plan.md) – Test Plan
- [A.7](templates/a07-release-checklist.md) – Release Checklist
- [A.8](templates/a08-component-or-module-specification.md) – Component or Module Specification
- [A.9](templates/a09-technical-debt-register.md) – Technical Debt Register
- [A.10](templates/a10-maintaining-owner-appointment-form.md) – Maintaining Owner Appointment Form

## Conventions

- Product statements follow the "verify" convention: confirm against current vendor documentation and record a *Last verified* date.
- This handbook is not legal advice. Contract and compliance sections are checklists for counsel review.
- Part of the **Adobe** repository. See the [main README](../README.md).
