# 1. Introduction

> Part of the *Adobe DXP Downscale Playbook* v1.0 (Review Draft). Section numbers (§) refer to the playbook's original numbering; see the root [README](../README.md) for the section map.

## 1.1 Purpose

This playbook gives a consultant a repeatable method to move an organisation off Adobe DXP and onto a simpler, lower-cost or more fitting platform. Four target directions are covered:

1. **WooCommerce** (WordPress-based, self-hosted or managed hosting).
2. **PrestaShop** (PHP/Symfony, self-hosted or managed hosting).
3. **Shopify** (hosted SaaS commerce).
4. **A custom platform** (built or composed to the organisation's needs).

The playbook covers the whole lifecycle: exit discovery, target selection, design, build, extraction and migration, testing and cutover, hypercare, handover, and the formal decommissioning of the Adobe estate.

## 1.2 Scope

**In scope**
- Adobe Commerce (SaaS, PaaS and on-premises variants), AEM (Cloud Service and 6.5-era deployments), Adobe Experience Platform, and included Experience Cloud modules such as Analytics, Target and Journey Optimizer.
- Moving commerce data, content, assets, customer data, configuration and integrations to the chosen target.
- Preserving SEO value, business history and regulatory records.
- Retiring Adobe licences, environments, credentials and integrations.

**Out of scope**
- Migration *into* Adobe DXP (see the up-scale handbook).
- Migrations between the four targets themselves.
- Legal advice. Contract, POPIA and tax-retention sections are checklists for counsel.

## 1.3 Why downscaling is a different problem

Downscaling is not the up-scale process run backwards.

- **Capability goes down, not up.** The target platform will do less than Adobe DXP. The task is to decide deliberately what is dropped, replaced or rebuilt, and to get stakeholder sign-off on the losses (see §4).
- **The clock is set by Adobe's contract.** Licence terms, renewal notice periods and data-return windows set the real deadline. Missing a notice date can mean paying for another term.
- **Data extraction is the dependency.** What can be exported depends on the Adobe product, its deployment model and the licence. SaaS products give API access only, not database access.
- **Traffic and search ranking are assets that can be destroyed.** A new platform changes URLs, markup and performance. Without a redirect and SEO plan, revenue can fall.
- **Decommissioning is a deliverable.** Leaving Adobe cleanly (credentials, tags, integrations, data deletion evidence) is part of the project, not an afterthought.

## 1.4 Common drivers

Cost reduction at renewal, over-specification for the business size, loss of in-house Adobe skills, a move to a SaaS commerce model, a change in strategy, or consolidation after a merger. The driver determines the target and the acceptable loss of capability, so it must be recorded in Phase 1.

## 1.5 Engagement Models and Consultant Accountability

The engagement models from the up-scale handbook (§1.4) apply unchanged:

| Model | Consultant accountable for | Typical downscale fit |
|---|---|---|
| **A. Consultant-led delivery** | Design, build, migration execution, handover | Shopify or WooCommerce moves for small and mid-size estates |
| **B. Lead-and-assure (default)** | Design authority, standards, review, migration approach, gate evidence, handover | Most enterprise downscales; build by client team or partner |
| **C. Advisory only** | Quality of the advice and design | Client has a build partner already |

Rules for every model: the model and any build partner are named in the SoW; go-live, scope, budget and vendor-contract decisions stay with the client; the consultant never becomes the platform operator; **the client alone issues termination notices to Adobe**, and the consultant only prepares the evidence and timeline.

## 1.6 Guiding Principles

1. **Exit-first thinking:** Establish what can be extracted, and when, before choosing a target.
2. **Contract-aware scheduling:** Plan backwards from Adobe's notice and term-end dates.
3. **Deliberate capability loss:** Every dropped or reduced capability is listed, justified and signed off.
4. **Data minimisation:** Migrate what is needed, archive what must be kept, and purge the rest in line with POPIA and retention rules.
5. **Traffic preservation:** Treat URLs, content and search performance as business assets.
6. **Repeatable, reconcilable migration:** Rehearse, measure and reconcile before cutover.
7. **Safe fallback:** Keep Adobe available (read-only where possible) until the new platform is proven.
8. **Fit over fashion:** Pick the target that fits the organisation's skills and business model, not the one that is most popular.
9. **No new lock-in by accident:** Record the exit route from the new platform as well.
10. **Client ownership:** The client must hold the data, accounts, documentation and operating capability after the consultant leaves.

## 1.7 Assumptions

- The organisation's main business is commerce plus content, run on one or more Adobe products.
- Where South African operations exist, POPIA applies, plus any other relevant jurisdictions.
- All product-specific statements in this playbook carry the **"verify" convention**: confirm against current vendor documentation and the client's actual agreements, and record a *Last verified* date and source before the design gate (D3).
