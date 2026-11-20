# 3. Target Platform Selection

> Part of the *Adobe DXP Downscale Playbook* v1.0 (Review Draft). Section numbers (§) refer to the playbook's original numbering; see the root [README](../README.md) for the section map.

## 3.1 The four targets in brief

| Target | Nature | Strength | Main trade-off |
|---|---|---|---|
| **WooCommerce** | Open-source commerce plugin on WordPress | Content plus commerce in one stack; huge ecosystem; full data control | You own hosting, security, updates and plugin quality |
| **PrestaShop** | Open-source PHP/Symfony commerce platform | Commerce-focused, multistore and multilingual, full data control | Smaller ecosystem than WooCommerce; weak content tooling; you own hosting and upgrades |
| **Shopify** | Hosted SaaS commerce | Fast to launch, low operational burden, strong checkout and reliability | Less control over data model, checkout and URLs; app and plan costs; platform limits |
| **Custom platform** | Built or composed to need (monolith or headless) | Exact fit and control | Highest build and maintenance cost; requires a capable team |

## 3.2 Fit profile

Use as a first filter, not a decision.

| Situation | Leans toward |
|---|---|
| Small team, wants low operations, standard B2C commerce | Shopify |
| Content-heavy site with commerce, WordPress skills available | WooCommerce |
| Commerce-focused, multistore or multilingual, in-house PHP skills | PrestaShop |
| Complex B2B rules, unusual pricing or workflows, strong engineering team | Custom |
| Strong requirement for data residency or self-hosting | WooCommerce, PrestaShop or Custom |
| Very high traffic spikes with minimal ops staff | Shopify (or well-run custom) |
| Heavy dependency on bespoke ERP-driven logic | Custom, or Woo/Presta with custom modules |

## 3.3 Scored decision matrix

Score 1–5 per criterion with agreed weights. Record rationale, not just the score. A mandatory-criterion failure (for example unmet residency) eliminates a target before scoring.

| Criterion | What to assess | Woo | Presta | Shopify | Custom |
|---|---|---|---|---|---|
| Functional fit | Coverage of retained capabilities (§4) | | | | |
| Data model fit | Products, options, B2B, custom attributes | | | | |
| Content capability | Fit for the content that remains | | | | |
| Total cost of ownership | Licences, apps, hosting, build, support over 3–5 years | | | | |
| Operational burden | Patching, upgrades, scaling, monitoring | | | | |
| Scalability and peak load | Traffic, catalogue size, order rate | | | | |
| Security and PCI scope | Who carries what; hosted payment fields | | | | |
| Data residency and POPIA | Regions, storage, access, sub-processors | | | | |
| Payments and local gateways | Support for required local gateways and methods | | | | |
| Integrations | ERP, CRM, 3PL, tax, shipping connectors | | | | |
| Migration complexity | Import tools, limits, data-model gaps | | | | |
| Skills availability | Local talent and partner market | | | | |
| Vendor dependency and exit | Lock-in and portability of the *new* platform | | | | |
| Time to market | Fit with Adobe term end | | | | |

## 3.4 Responsibility matrix (who carries what after migration)

| Responsibility | Woo | Presta | Shopify | Custom |
|---|---|---|---|---|
| Hosting and infrastructure | Client or host | Client or host | Shopify | Client or host |
| Application patching and upgrades | Client | Client | Shopify (platform), client (apps and theme) | Client |
| Plugin / module / app compatibility | Client | Client | Client (apps) | Client (libraries) |
| Backups and DR | Client or host | Client or host | Shopify (platform), client (exports) | Client |
| PCI scope reduction | Client (via hosted gateway) | Client (via hosted gateway) | Largely Shopify | Client (via hosted gateway) |
| Uptime commitment | Host SLA | Host SLA | Shopify | Client design and host |
| Security monitoring | Client | Client | Shared | Client |

## 3.5 Data residency, POPIA and payments

For each shortlisted target:

1. Where is personal information stored, processed, backed up and accessed by support staff?
2. If outside South Africa, what is the lawful basis for cross-border transfer under POPIA, and what agreements are in place?
3. Are the required payment gateways (including local South African ones, if relevant) supported by the target, and at what fee structure?
4. Are tax, invoicing and shipping needs met locally?

Verify availability of payment providers and features in the target country, because they vary by country and over time. Counsel confirms the POPIA conclusion.

## 3.6 Total cost of ownership

Compare 3–5 years, including: licences and plans, apps and plugins, hosting, build and migration cost, payment fees, support and managed services, monitoring, security, backups and DR, upgrades, training, and the cost of any overlap with Adobe.

## 3.7 Common selection mistakes

- Choosing the target before listing the capabilities to retain.
- Assuming "Shopify is cheaper" without costing apps, plan tier and checkout limits.
- Assuming "WooCommerce is free" without costing hosting, security and maintenance.
- Choosing a custom build to avoid trade-offs, then underfunding its maintenance.
- Ignoring that content-heavy AEM sites need a content solution as well as a commerce platform.

## 3.8 Decision rule

The client signs a **Target Platform Decision Record** (Appendix A.3) with scores, rationale, eliminated options and accepted trade-offs. Changing target after D2 is a controlled change (§19.3).
