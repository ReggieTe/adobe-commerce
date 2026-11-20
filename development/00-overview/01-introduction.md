# 1. Introduction

> Part of the *Enterprise Adobe DXP Development Handbook* v1.0 (Review Draft). Section numbers (§) refer to the handbook's original numbering; see the README at the root of this folder for the section map.

## 1.1 Purpose

This handbook gives a consultant and a delivery team a repeatable engineering method for building on Adobe DXP: requirements, architecture, environments and pipelines, implementation, quality engineering, release, and handover. It covers new builds, enhancements after a migration, and ongoing change programmes.

## 1.2 Scope

**In scope:** custom development and configuration on Adobe Experience Manager (AEM), Adobe Commerce, Adobe Experience Platform (AEP), and the Experience Cloud modules where required (Analytics, Target, Journey Optimizer); integrations and extensions; pipelines and release management; engineering standards; developer handover.

**Out of scope:** platform migration (see the migration handbooks), live operations and incident handling (see the Support handbook), product licensing and legal advice.

## 1.3 Engagement Models and Accountability

The engagement models from the up-scale handbook (§1.4) apply:

| Model | Consultant accountable for | Typical development fit |
|---|---|---|
| **A. Consultant-led delivery** | Design, build, test support, release, handover | Small or specialist scopes, tight timelines |
| **B. Lead-and-assure (default)** | Architecture, standards, code and configuration review, quality gates, release approval recommendation | Most enterprise programmes, built by client or partner teams |
| **C. Advisory only** | Quality of architecture and advice | Client has an established delivery team |

Rules for every model: the model and any build partner are named in the SoW; the client owns scope, budget, priorities and release approval; the consultant does not become the platform operator; the **operational owner** rule applies at handover (§12.7).

## 1.4 Guiding Principles

1. **Standard before custom:** Use product capabilities and supported extension points first. Custom code needs a documented reason.
2. **Architecture before code:** Agree design and non-functional targets before major build.
3. **Upgrade-safe by design:** No unsupported core modifications; extensions must survive product updates.
4. **Everything as code:** Source, configuration, pipelines and infrastructure definitions live in version control.
5. **Quality is built in:** Automated tests and quality gates run on every change.
6. **Security by design:** Secrets, access, dependencies and data handling are designed in, not added later.
7. **Small, safe releases:** Prefer frequent, reversible releases over large batches.
8. **Observable software:** Logging, metrics and tracing are part of the definition of done.
9. **Documented decisions:** Architecture decisions and known limitations are recorded.
10. **Client ownership:** The client holds the code, accounts, documentation and knowledge to continue without the consultant.

## 1.5 The "Verify" Convention

Adobe product names, deployment models, tooling, APIs and limits change often. Product-specific statements in this handbook are indicative. Before design approval (E2), the Technical Lead verifies each product fact the design depends on against current Adobe documentation and the client's licence, and records a *Last verified* date and source in the architecture decision record.
