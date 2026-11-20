# 2. Understanding the Adobe DXP Target Environment

> Part of the *Enterprise Adobe DXP Migration Handbook* v1.1 (Review Draft). Section numbers (§) refer to the handbook's original numbering; see the root [README](../README.md) for the section map.

## 2.1 Adobe DXP Is an Ecosystem, With Three Principal Products

Adobe DXP is an ecosystem of capabilities, not a single application. For the migrations this handbook targets, three products form the **principal scope**; other Experience Cloud products are **modules included where requirements justify them**.

**Principal products**

| Product | Role in migration | Typical source platforms it replaces |
|---|---|---|
| **Adobe Experience Manager (AEM)** | Content, digital assets, page experience | Custom portals, legacy CMS, WordPress/CMS layers, content in commerce platforms |
| **Adobe Commerce** | Catalogue, cart, checkout, orders, customer accounts | WooCommerce, PrestaShop, Shopify, existing Adobe Commerce, custom commerce |
| **Adobe Experience Platform (AEP)** | Unified customer profile, data and audiences | Fragmented customer data, CRM extracts, ad-hoc analytics stores |

**Include-where-required modules**

| Module | Include when… |
|---|---|
| Adobe Analytics / Customer Journey Analytics | There is a requirement for enterprise web or cross-channel analytics beyond existing tooling |
| Adobe Target | Personalisation and experimentation are funded business goals |
| Adobe Journey Optimizer | Orchestrated cross-channel journeys are required, and AEP is in scope |
| Other Experience Cloud services (e.g. Workfront, Marketo Engage) | Specific business processes demand them |

**Capability mapping (illustrative, not mandatory)**

| Business capability | Potential target |
|---|---|
| Content management | AEM |
| Digital commerce | Adobe Commerce |
| Customer data management | AEP |
| Web analytics | Adobe Analytics or existing tooling |
| Personalisation | Adobe Target (and/or AEP-driven) |
| Journey orchestration | Adobe Journey Optimizer |
| **Customer identity** | Commerce customer accounts, or an external identity provider (CIAM). Adobe IMS governs Adobe user access and is **not** a general customer-identity solution. |
| Integration | API gateway, iPaaS, middleware or custom services |
| Search | Product-supported or third-party search |
| Payments | External payment providers |
| ERP and finance | Existing enterprise systems |

Do not select modules simply because they exist. Every module added must be justified by a requirement in the Capability Gap Assessment (§5.2).

## 2.2 Product and Deployment Assessment, and the "Verify" Convention

Adobe product names, packaging, deployment options and version lifecycles change frequently. This handbook describes **decision structure**, not a guaranteed product catalogue.

**Convention:** Any product-specific statement in this handbook or in derived product files must carry a *Last verified* date and a link to the Adobe documentation or contract used to verify it. Before design is approved (G3), the Technical Lead re-verifies every product statement the design depends on against current Adobe documentation and the client's actual licence.

The assessment must consider product, version, licensing agreement, supported architecture and available deployment options. Do not assume the whole ecosystem can run on customer-managed infrastructure because some Adobe Commerce options allow it.

## 2.3 Per-Product Deployment Matrix

Indicative only: verify per §2.2.

| Product | SaaS / Adobe-managed | PaaS (Adobe cloud infrastructure, shared responsibility) | Customer or partner-managed (incl. on-premises) | Notes |
|---|---|---|---|---|
| **Adobe Commerce** | Adobe Commerce as a Cloud Service | Adobe Commerce on Cloud Infrastructure | On-premises / self-managed (check current support and lifecycle) | Widest range of options; most deployment decisions occur here |
| **AEM** | AEM as a Cloud Service | AEM Managed Services (where still offered under contract) | AEM 6.5 on-premises (check lifecycle and support end dates) | Cloud Service imposes a prescribed architecture, pipeline and extensibility model |
| **AEP** | Adobe-managed only | Not applicable | Not applicable | No self-hosting; integration and data residency are the main levers |
| **Analytics, Target, AJO** | Adobe-managed only | Not applicable | Not applicable | Product-specific configuration and integration responsibility |

Hosting is therefore a **per-product decision**. A programme that includes AEM as a Cloud Service and AEP has no self-hosting option for those products at all, regardless of preference.

## 2.4 Deployment Decision Matrix

Score each viable deployment model for each in-scope product (e.g. 1–5, with weights agreed with the client). Record rationale, not just scores.

| Criterion | What to assess | SaaS | PaaS | Self/partner-managed |
|---|---|---|---|---|
| Total cost of ownership | Licence, hosting, ops staff, upgrades, DR | | | |
| Scalability | Peak traffic, growth, elasticity | | | |
| Performance | Latency to users and to integrated systems | | | |
| Availability and SLA | Contractual commitments, maintenance windows | | | |
| Security responsibility | Who patches, hardens, monitors | | | |
| **Data residency and POPIA** | Regions available, cross-border transfer basis (§2.5) | | | |
| Disaster recovery | RPO/RTO achievable, who owns it | | | |
| Customisation and extensibility | Custom code limits, infrastructure access | | | |
| Upgrade model | Continuous vs. controlled upgrades; effort and risk | | | |
| Version lifecycle | Support end dates, forced migrations | | | |
| Operational skills | Skills the client or MSP must hold | | | |
| Vendor dependency and portability | Lock-in, content and data export routes | | | |
| Integration fit | Network paths, private connectivity, middleware proximity | | | |

**Decision rule:** a model that fails a mandatory criterion (e.g. an unmet residency obligation) is eliminated before scoring. Mandatory criteria are agreed with the client in Phase 2.

## 2.5 Data Residency, POPIA and Cross-Border Transfer

Adobe cloud regions may not include South Africa. For South African operations, the hosting decision must include a per-product check:

1. Which regions are available for this product and licence?
2. Where will personal information be stored, processed, backed up and accessed by support staff?
3. If outside South Africa, what is the lawful basis for cross-border transfer under POPIA (e.g. adequate protection by law, binding agreement, consent, or another recognised ground)?
4. What contractual terms (data processing agreement, sub-processor lists) are in place with Adobe and other vendors?
5. Do the other jurisdictions the organisation operates in (e.g. EU or UK customers) add obligations?

Legal counsel confirms the conclusion. Record it in the Security and Compliance Strategy (§5.8) and the hosting decision record. This handbook is not legal advice.

## 2.6 Hybrid as an Integration Pattern

Hybrid is **not** a fourth deployment model. It describes the situation where Adobe-managed products are connected to customer-managed applications and external services, and it applies whichever deployment models were chosen per product.

Considerations: secure connectivity between environments, API and integration management, network latency, data transfer and synchronisation, monitoring across multiple providers, shared-responsibility boundaries, and disaster recovery across providers.
