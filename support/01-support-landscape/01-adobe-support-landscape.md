# 2. The Support Landscape

> Part of the *Enterprise Adobe DXP Support and Operations Handbook* v1.0 (Review Draft). Section numbers (§) refer to the handbook's original numbering; see the README at the root of this folder for the section map.

## 2.1 Shared responsibility (indicative)

| Area | Adobe | Hosting provider (if any) | MSP / consultant | Client |
|---|---|---|---|---|
| Platform availability of Adobe-managed services | ✔ (per agreement) | | Monitor and escalate | Accept SLA |
| Infrastructure (where customer or partner managed) | | ✔ | Operate (if contracted) | Own |
| Application code and configuration (custom) | | | ✔ L2/L3 (if contracted) | Own |
| Content, catalogue and business data | | | Support | ✔ Own |
| Integrations and middleware | | | ✔ (if contracted) | Own |
| Security patching and access management | Product-managed parts | Infrastructure | ✔ (custom parts) | Policy and approval |
| Backups and recovery | Per product | Per contract | ✔ Operate and test | Define RPO and RTO |
| Vendor escalation | Receives tickets | Receives tickets | ✔ Raises with evidence | Authorises |

Verify per product and deployment model (SaaS, PaaS, customer-managed).

## 2.2 What each product needs from support (indicative)

| Product | Typical operational concerns |
|---|---|
| **AEM** | Author and publish availability, content replication and delivery, Dispatcher and CDN caching and invalidation, workflows, pipeline health, content backup and restore, authoring access |
| **Adobe Commerce** | Storefront and checkout availability, indexing, cron and queues, cache and CDN behaviour, deployment health, payment and order flow, catalogue imports, search |
| **AEP** | Data ingestion health, dataset and schema health, identity and profile quality, segment and destination health, privacy request handling, data usage and consent controls |
| **Analytics / Target / Journey Optimizer** | Tag and SDK health, data collection accuracy, activity and journey status, audience health, message delivery |
| **Integrations and middleware** | Queue depth, error rates, retries, dead-letter queues, third-party availability, credential and certificate expiry |

## 2.3 Support tiers

| Tier | Responsibility |
|---|---|
| **L1 – Business and service desk** | First contact, logging, categorisation, user queries, access requests, basic business-process help, status communication |
| **L2 – Application and operations support** | Functional issues, configuration, content and catalogue issues, integration troubleshooting, job monitoring, runbook execution |
| **L3 – Technical and engineering support** | Code defects, architecture, performance, complex integration, infrastructure and pipeline issues, root cause analysis |
| **Vendor support** | Adobe, hosting provider, payment and other third parties |

Never assume L2 and L3 can be handled internally without checking skills and capacity.
