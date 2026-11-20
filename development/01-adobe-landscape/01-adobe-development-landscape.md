# 2. The Adobe Development Landscape

> Part of the *Enterprise Adobe DXP Development Handbook* v1.0 (Review Draft). Section numbers (§) refer to the handbook's original numbering; see the README at the root of this folder for the section map.

## 2.1 Development models by product (indicative)

| Product | Typical development model | Key engineering concerns |
|---|---|---|
| **AEM** | Java/OSGi and Sling components, HTL templates, frontend build, Dispatcher configuration, content models, headless delivery (for example GraphQL and content fragments), and, where licensed, edge-based authoring and delivery options | Prescribed project structure and pipeline on cloud service; content model design; caching and Dispatcher rules; authoring experience |
| **Adobe Commerce** | PHP module architecture, dependency injection, plugins and observers, APIs (REST and GraphQL), theming, and, for API-first extensibility, out-of-process extensions | Upgrade safety; avoiding core overrides; indexing, cron and queue behaviour; performance of customised flows |
| **AEP** | XDM schemas, datasets, data ingestion (batch and streaming), identity design, SDK-based data collection, queries, segments and destinations | Data model and identity design; consent and data governance; ingestion monitoring |
| **Analytics / Target / Journey Optimizer** | Data collection through tags and SDKs, implementation of events and attributes, activity and journey configuration | Data layer design; tag governance; consent enforcement; testing across browsers and devices |
| **Cross-product extensibility** | Adobe's out-of-process extension framework and eventing/webhook capabilities (verify current tooling) | Authentication, rate limits, retries, observability |

## 2.2 Hosting and pipeline implications

Whether a product is Adobe-managed (SaaS), Adobe cloud infrastructure (PaaS) or customer-managed changes how code is built and deployed, how environments are provided, and what can be customised. Confirm the deployment model per product before designing the delivery pipeline (see up-scale handbook §2.3).

## 2.3 Supported extension points rule

For each product, list the supported extension points (APIs, events, plugins, components, webhooks, extension frameworks) in the architecture decision record. Anything outside that list requires an ADR with risk, upgrade impact and an approver.
