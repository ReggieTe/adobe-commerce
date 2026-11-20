# 2. Source Landscape: What You Are Leaving

> Part of the *Adobe DXP Downscale Playbook* v1.0 (Review Draft). Section numbers (§) refer to the playbook's original numbering; see the root [README](../README.md) for the section map.

## 2.1 The Adobe estate is usually mixed

A typical estate combines several of these. Inventory each separately, because exit routes differ.

| Adobe product | Role in the estate | What is typically at stake on exit |
|---|---|---|
| Adobe Commerce | Catalogue, cart, checkout, orders, customers | Orders, customers, products, pricing, promotions, URL rewrites |
| AEM | Web content, experience pages, digital assets | Pages, fragments, assets with metadata, URL structure, templates |
| AEP | Unified customer profile, audiences | Profiles, consent, segments, event history |
| Analytics / Customer Journey Analytics | Reporting | Historical reports and raw data for trend continuity |
| Target | Personalisation and testing | Active tests, audiences, activities |
| Journey Optimizer | Orchestrated messaging | Journeys, templates, audiences, subscriptions and opt-ins |

## 2.2 Data extraction routes by product and deployment (indicative)

Verify per §1.7. "SaaS" means Adobe-managed with no infrastructure access; "PaaS" means Adobe cloud infrastructure with shared responsibility.

| Product / deployment | Typical extraction routes | Key constraints |
|---|---|---|
| Adobe Commerce on-premises | Direct database access, file system, REST/GraphQL APIs | Full control; extension-specific tables need mapping |
| Adobe Commerce on Cloud Infrastructure (PaaS) | Database and media access through supported tunnels and backups, APIs, admin exports | Access is mediated; production access procedures apply |
| Adobe Commerce as a Cloud Service (SaaS) | APIs, data-export services and admin exports only | No database access; API rate limits; plan extraction duration |
| AEM as a Cloud Service | Content packages, assets APIs, content fragment/GraphQL APIs | No direct repository access; extraction is API or package based |
| AEM 6.5-era (on-prem or managed) | Package manager, repository tooling, assets APIs | Repository structure is custom per project; needs reverse-engineering |
| AEP | Dataset export to cloud storage, query and access APIs, audience/destination exports | Depends on licence entitlements; volume and cost of export |
| Analytics | Raw data feeds, data warehouse exports, reporting APIs | Retention window; export must start early |
| Target / Journey Optimizer | Configuration exports, activity definitions, audience definitions (often documentation only) | Mostly rules, not data; capture as documentation |

**Rule:** Confirm in Phase 1 that the *entitlement to export* exists for every data class, not only the technical route. Some exports are licence-dependent.

## 2.3 Contract and entitlement review

Before technical work, the client's contract owner and counsel establish:

- Licence term end dates per product and per environment.
- **Notice period** for non-renewal and the date the notice must be served.
- Early-termination terms and any minimum commitments.
- Overlap or short-term extension options, and their cost.
- Data return, export assistance and **post-termination data retention and deletion** terms.
- Sub-processor and data-location terms relevant to POPIA.
- Support entitlements during the exit period.
- IP ownership of custom code, extensions and content.

**Deliverable:** Adobe Contract and Entitlement Register (Appendix A.1).

## 2.4 Data classes and ownership

| Data class | Examples | Usual owner | Typical treatment |
|---|---|---|---|
| Customer identity | Accounts, addresses, groups | Business (commerce) | Migrate (subject to minimisation) |
| Consent and preferences | Marketing consent, preferences, timestamps and evidence | Compliance | Migrate with evidence, or re-collect |
| Commerce records | Orders, invoices, credit memos, shipments, payments (references) | Finance | Migrate, or archive per retention rules |
| Catalogue | Products, options, categories, pricing, stock | Merchandising | Migrate and clean |
| Content | Pages, articles, fragments | Marketing | Rebuild or migrate by value |
| Assets | Images, documents, video, metadata, rights | Marketing | Migrate with metadata |
| Behavioural data | AEP events, Analytics history | Marketing and analytics | Archive summarised data; purge the rest |
| Configuration | Tax, shipping, promotions, rules | Operations | Rebuild per target |

## 2.5 Adobe-specific lock-in points to find early

- Customer IDs and external references used by other systems.
- Adobe IMS logins and API credentials used by integrations.
- Experience Cloud tags (analytics and personalisation scripts) embedded in the site.
- Content fragments and experience fragments that model content in Adobe-specific ways.
- Custom Commerce extensions holding business rules in code.
- Data in AEP that has no other home (profiles and audiences).
- Search, recommendation and CDN configuration managed in or alongside Commerce.
