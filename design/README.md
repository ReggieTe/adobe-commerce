
# Adobe Commerce Frontend Architecture Decision Guide

**Document:** Frontend Architecture Design Considerations  
**Platform:** Adobe Commerce / Adobe DXP  
**Phase:** Phase 3 – Design  
**Decision:** Native Adobe Commerce Storefront vs Hyvä vs Headless  
**Audience:** Solution Architects, Technical Leads, Enterprise Architects, Developers and Project Stakeholders

---

# 1. Purpose

This document provides a framework for selecting the appropriate frontend architecture when migrating an existing digital commerce platform to Adobe Commerce.

The objective is to determine whether the organisation should:

1. Retain the native Adobe Commerce storefront architecture.
2. Adopt Hyvä as the Adobe Commerce frontend.
3. Implement a headless or decoupled storefront using a modern frontend framework.

The decision must consider more than visual design. It affects:

- Implementation cost.
- Time to market.
- Frontend performance.
- SEO and search engine indexing.
- Developer skills and availability.
- Adobe Commerce extension compatibility.
- Third-party integrations.
- Content management.
- Mobile experience.
- Hosting and infrastructure.
- Deployment and release management.
- Long-term maintenance and support.

The selected architecture must satisfy the organisation's business requirements without introducing unnecessary technical complexity.

# 2. Understanding the Three Approaches

## 2.1 Native Adobe Commerce Storefront

The native storefront is the traditional Adobe Commerce frontend architecture based on PHP templates, layouts, blocks, UI components and themes.

Adobe Commerce provides the Blank and Luma reference themes. Organisations can customise these themes or develop their own themes using the native frontend architecture.

### Architecture

```text
                 CUSTOMER BROWSER
                        |
                        v
                 WEB SERVER / NGINX
                        |
                        v
                 ADOBE COMMERCE
                        |
             +----------+----------+
             |                     |
             v                     v
        PHP APPLICATION       FRONTEND LAYER
             |                     |
             |                PHP Templates
             |                Layout XML
             |                UI Components
             |                CSS / LESS
             |                JavaScript
             |                     |
             +----------+----------+
                        |
                        v
                  DATABASE / CACHE
```

### Characteristics

- Frontend and backend are part of the same application.
- PHP is used for server-side rendering.
- Commerce functionality is closely integrated with the storefront.
- Layout XML, blocks, templates and UI components control rendering.
- Native Adobe Commerce functionality is readily available.
- Most traditional Adobe Commerce extensions are designed for this architecture.

### Advantages

- Established Adobe Commerce development model.
- Broad compatibility with traditional Adobe Commerce extensions.
- Direct access to native platform functionality.
- No separate frontend application infrastructure is required.
- Lower architectural complexity than a fully headless implementation.
- Existing Adobe Commerce developers can maintain the application.
- Suitable for organisations with established PHP and Adobe Commerce teams.

### Disadvantages

- Frontend and backend are more tightly coupled.
- Significant theme customisation can become difficult to maintain.
- Performance depends heavily on server-side rendering, caching and frontend optimisation.
- Frontend technology choices are more constrained.
- Independent frontend deployment is limited.
- A modern application-like experience may require additional custom development.

### Best suited for

- Traditional B2C commerce websites.
- B2B portals using native Adobe Commerce functionality.
- Organisations with existing Adobe Commerce frontend teams.
- Projects with limited migration budgets.
- Businesses with extensive third-party extension dependencies.
- Organisations that prioritise implementation simplicity.

### Technical considerations

- Use a custom theme rather than modifying core theme files.
- Follow Adobe Commerce layout and dependency injection conventions.
- Avoid unnecessary JavaScript and CSS dependencies.
- Implement full-page caching correctly.
- Validate compatibility with Page Builder and other installed extensions.
- Maintain upgrade-safe customisations.

Official resources:
- https://developer.adobe.com/commerce/frontend-core/
- https://developer.adobe.com/commerce/frontend-core/guide/
- https://developer.adobe.com/commerce/frontend-core/guide/themes/
- https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/design/themes

---

## 2.2 Hyvä Storefront

Hyvä is a modern frontend ecosystem for Adobe Commerce that replaces much of the traditional Luma frontend stack with a simpler and lighter implementation approach.

It uses PHP templates together with Tailwind CSS and Alpine.js.

Hyvä is not headless. It remains integrated with the Adobe Commerce application and uses its native backend capabilities.

### Architecture

```text
                 CUSTOMER BROWSER
                        |
                        v
                 WEB SERVER / NGINX
                        |
                        v
                 ADOBE COMMERCE
                        |
             +----------+----------+
             |                     |
             v                     v
        PHP APPLICATION        HYVA THEME
             |                     |
             |                 PHP Templates
             |                 Tailwind CSS
             |                 Alpine.js
             |                     |
             +----------+----------+
                        |
                        v
                  DATABASE / CACHE
```

### Characteristics

- Retains Adobe Commerce as the application and commerce backend.
- Uses PHP templates for server-side rendering.
- Uses Tailwind CSS for styling.
- Uses Alpine.js for lightweight frontend interactions.
- Replaces much of the traditional Luma frontend dependency stack.
- Does not require a separate React or Vue storefront application.

### Advantages

- Modern frontend development approach.
- Reduced frontend JavaScript complexity compared with traditional Luma implementations.
- Strong potential for improved page performance.
- Server-side rendering supports SEO requirements.
- Retains direct access to Adobe Commerce functionality.
- Less architectural separation than headless.
- Can reduce frontend development and maintenance overhead.
- Suitable for teams with PHP and frontend development experience.

### Disadvantages

- Requires a Hyvä-specific development skill set.
- Some existing Luma extensions require compatibility work or replacement.
- Extension compatibility must be checked individually.
- Certain frontend features may require additional implementation.
- Hyvä commercial licensing and product requirements must be evaluated.
- The frontend remains coupled to the Adobe Commerce application.
- Not intended to provide the complete architectural independence of headless.

### Best suited for

- Organisations migrating from Luma-based Adobe Commerce storefronts.
- Businesses seeking better frontend performance without adopting headless.
- Projects with a limited or moderate frontend development budget.
- Organisations that want to retain native Adobe Commerce functionality.
- PHP-focused development teams.
- Commerce-first websites with limited requirements for independent frontend applications.

### Technical considerations

- Verify Hyvä compatibility for all existing extensions.
- Check whether a vendor provides an official Hyvä-compatible module.
- Review checkout compatibility.
- Validate payment integrations.
- Review product configurators and custom product options.
- Confirm compatibility with B2B features.
- Validate analytics, consent management and tracking.
- Establish Tailwind CSS conventions.
- Review Alpine.js component architecture.
- Test performance using real user monitoring and Core Web Vitals.

Official resources:
- https://www.hyva.io/
- https://docs.hyva.io/
- https://www.hyva.io/compatibility

---

## 2.3 Headless / Decoupled Storefront

Headless architecture separates the frontend presentation layer from the Adobe Commerce backend.

Adobe Commerce continues to manage commerce functionality, while a separate frontend application consumes its APIs.

The frontend can be developed using technologies such as React, Next.js, Vue or an Adobe-supported storefront approach.

Headless architecture is not one specific technology. It is an architectural pattern.

### Architecture

```text
                  CUSTOMER BROWSER
                         |
                         v
                FRONTEND APPLICATION
                 React / Next.js / Vue
                         |
                         v
                  API / BFF LAYER
                         |
              +----------+----------+
              |                     |
              v                     v
       ADOBE COMMERCE          OTHER SERVICES
              |                CMS / CRM / PIM
              |                Search / CDP
              |                Marketing
              |
       +------+------+
       |      |      |
       v      v      v
    Catalog  Cart   Checkout
       |      |      |
       +------+------+
              |
              v
       ORDER MANAGEMENT
              |
              v
          DATABASE
```

### Characteristics

- Frontend and backend are independently developed.
- The frontend communicates with Commerce through APIs.
- GraphQL is commonly used for storefront operations.
- REST APIs can be used where appropriate.
- Additional API gateways or middleware may be required.
- The frontend can use a different technology stack from Adobe Commerce.
- Frontend deployment can be independent of backend deployment.

### Common frontend technologies

| Technology | Purpose |
|---|---|
| React | Component-based frontend development |
| Next.js | React framework with server rendering and routing capabilities |
| Vue.js | Component-based frontend development |
| Nuxt | Vue framework with server rendering and application capabilities |
| PWA Studio | Adobe tooling for progressive web application storefronts |
| Edge Delivery Services | Adobe storefront and content delivery approach |

### Adobe Commerce headless options

**Option A – Adobe PWA Studio**

Adobe provides PWA Studio tooling for building progressive web application storefronts.

Resources:
- https://developer.adobe.com/commerce/pwa-studio/
- https://developer.adobe.com/commerce/pwa-studio/guides/

**Option B – Custom React / Next.js / Vue**

The organisation develops its own frontend application and connects it to Adobe Commerce APIs.

Resources:
- https://developer.adobe.com/commerce/webapi/graphql/
- https://developer.adobe.com/commerce/webapi/rest/

**Option C – Commerce Storefront powered by Edge Delivery Services**

Adobe provides a storefront approach using Edge Delivery Services, storefront components and commerce APIs.

Resources:
- https://experienceleague.adobe.com/en/docs/commerce/storefront/get-started
- https://experienceleague.adobe.com/en/docs/commerce/information-center/explore-platforms-and-services/overview

### Advantages

- Complete separation between frontend and backend.
- Independent frontend deployment.
- Greater freedom in frontend technology selection.
- Suitable for omnichannel experiences.
- Supports web, mobile applications and additional customer touchpoints.
- Easier to build highly customised customer experiences.
- Can integrate multiple backend systems through API orchestration.
- Enables frontend teams to work independently from backend teams.

### Disadvantages

- Higher initial implementation complexity.
- Requires API design and management.
- Additional infrastructure may be required.
- Requires frontend and backend deployment coordination.
- More complex authentication and session management.
- Additional caching and performance architecture.
- More integration testing is required.
- Some native Adobe Commerce features may require custom frontend implementation.
- Extension compatibility cannot be assumed.
- More specialised skills may be required for long-term support.

### Best suited for

- Large enterprise commerce platforms.
- Omnichannel commerce strategies.
- Organisations with existing React, Next.js or Vue teams.
- Businesses requiring highly customised customer experiences.
- Multiple customer-facing applications consuming the same commerce services.
- Organisations with strong API governance and integration capabilities.
- Businesses planning a composable commerce architecture.

### Technical considerations

- GraphQL API coverage.
- REST API requirements.
- API gateway and middleware.
- Backend-for-Frontend (BFF) requirements.
- Authentication and customer sessions.
- Cart persistence.
- Checkout and payment integration.
- Customer account management.
- Search and product discovery.
- SEO and server-side rendering.
- CDN and caching.
- API rate limits.
- Error handling and retry strategies.
- Independent frontend and backend deployments.
- End-to-end observability.

Official resources:
- https://developer.adobe.com/commerce/webapi/graphql/
- https://developer.adobe.com/commerce/webapi/rest/
- https://developer.adobe.com/commerce/pwa-studio/
- https://experienceleague.adobe.com/en/docs/commerce/information-center/architecture/implementation-architectures

---

# 3. Architecture Comparison

| Consideration | Native Adobe Commerce | Hyvä | Headless |
|---|---|---|---|
| Architecture | Coupled | Coupled | Decoupled |
| Backend | Adobe Commerce | Adobe Commerce | Adobe Commerce |
| Frontend rendering | PHP server-side | PHP server-side | Depends on frontend stack |
| Frontend technology | PHP, JS, CSS/LESS | PHP, Alpine.js, Tailwind | React, Next.js, Vue, etc. |
| API dependency | Limited for rendering | Limited for rendering | Core requirement |
| Initial complexity | Low–Medium | Low–Medium | High |
| Initial development cost | Low–Medium | Medium | High |
| Frontend flexibility | Medium | Medium | Very High |
| Backend independence | Low | Low | High |
| Extension compatibility | Broadest traditional compatibility | Requires Hyvä compatibility | Requires API/frontend compatibility |
| SEO | Supported | Supported | Requires deliberate SSR/SEO design |
| Performance potential | Good with optimisation | High with optimisation | High with good architecture |
| Independent deployments | Limited | Limited | Yes |
| Omnichannel flexibility | Limited–Medium | Limited–Medium | High |
| API governance requirements | Low–Medium | Low–Medium | High |
| Frontend skills | Adobe Commerce/PHP | PHP, Alpine, Tailwind | Modern frontend/API skills |
| Maintenance | Theme and platform | Hyvä and platform | Separate frontend and backend |
| Best fit | Traditional commerce | Modern commerce without headless complexity | Enterprise composable experiences |

*Cost and complexity ratings are relative planning indicators, not vendor pricing or guaranteed delivery estimates.*

# 4. Business and Technical Decision Factors

The selection should be driven by business requirements, existing technology investments and future platform strategy.

## 4.1 Existing Platform Assessment

Before selecting a frontend architecture, evaluate the existing storefront.

Questions:

- Is the current platform a traditional server-rendered website?
- Is the current frontend already built using React, Vue or another modern framework?
- Does the organisation have an existing mobile application?
- Does the current platform expose APIs?
- Are there existing frontend components that can be reused?
- Does the business want to preserve the current customer experience?
- Are there complex product configurators or customer-specific workflows?
- Are there extensive third-party frontend dependencies?

**Decision consideration:**

If the existing platform already has a mature React or Next.js frontend and the organisation intends to retain it, a headless migration may be more appropriate than rebuilding the frontend using a traditional Adobe Commerce theme.

If the existing platform is a conventional PHP storefront and the organisation wants a modernised experience without a major architectural transformation, Hyvä may be appropriate.

## 4.2 Existing Adobe Commerce Extension Dependencies

Extension compatibility can materially affect the architecture decision.

Inventory all existing and required extensions.

| Extension category | Native | Hyvä | Headless |
|---|---|---|---|
| Payment | Usually broad compatibility | Verify Hyvä frontend support | Requires API/frontend integration |
| Shipping | Usually broad compatibility | Verify frontend compatibility | Requires API/frontend integration |
| Search | Usually broad compatibility | Verify frontend compatibility | API integration |
| Product configurator | Usually broad compatibility | Verify compatibility | Rebuild or integrate through APIs |
| B2B functionality | Native platform support | Validate frontend support | Build or integrate required frontend workflows |
| Customer account | Native platform support | Validate frontend support | Reimplement frontend flows |
| Loyalty | Depends on extension | Verify compatibility | API integration |
| Marketing | Depends on extension | Verify compatibility | Usually API, event or SDK integration |
| Analytics | Theme and tag integration | Theme and tag integration | Frontend instrumentation required |

Do not evaluate an extension only by whether it installs successfully.

Check whether its customer-facing functionality works correctly with the selected storefront.

## 4.3 Performance Requirements

Performance must be evaluated against the organisation's business targets.

Consider:

- Largest Contentful Paint (LCP).
- Interaction to Next Paint (INP).
- Cumulative Layout Shift (CLS).
- Time to First Byte (TTFB).
- API response times.
- Product listing performance.
- Product detail page performance.
- Checkout performance.
- Mobile network performance.
- Cache hit ratios.

A headless architecture does not automatically guarantee better performance. Poor API design, excessive frontend JavaScript, inefficient rendering and unnecessary network requests can create additional latency.

Hyvä can provide substantial frontend simplification without requiring a separate frontend application.

## 4.4 SEO Requirements

SEO must be part of the architecture decision rather than a post-development activity.

Evaluate:

- Server-side rendering.
- Metadata management.
- Canonical URLs.
- XML sitemaps.
- Structured data.
- Product schema.
- Category indexing.
- Pagination.
- Faceted navigation.
- Redirect management.
- Robots directives.
- Internationalisation and hreflang.
- URL migration.

For headless implementations, define how the frontend generates and serves crawlable HTML, metadata and structured data.

## 4.5 Content Management Requirements

Consider how marketing and content teams will manage the storefront.

Questions:

- Does the business use Adobe Experience Manager?
- Does it require Adobe Experience Manager Assets?
- Does it use Adobe Commerce Page Builder?
- Does it require visual page authoring?
- Are landing pages managed by developers or business users?
- Does content need to be distributed across multiple channels?
- Are content previews and approval workflows required?

The selected architecture must support the intended content authoring experience.

A headless frontend does not automatically provide content authoring tools. A CMS and its integration model must be designed separately.

---

# 5. Cost and Delivery Considerations

The organisation should compare total cost of ownership rather than only initial development cost.

| Cost area | Native | Hyvä | Headless |
|---|---|---|---|
| Initial development | Usually lower | Medium | Usually higher |
| Frontend licensing | Depends on extensions | Evaluate Hyvä licensing | Depends on selected technology and services |
| Backend development | Required | Required | Required |
| Frontend infrastructure | Usually shared | Usually shared | Often separate |
| API infrastructure | Limited for storefront rendering | Limited for storefront rendering | Significant |
| Extension compatibility | Broad traditional ecosystem | Additional validation | API and frontend validation |
| Developer availability | Adobe Commerce/PHP | Adobe Commerce/Hyvä | Frontend/API specialists |
| Testing complexity | Medium | Medium | High |
| Operational complexity | Lower | Lower–Medium | Higher |
| Long-term maintenance | Medium | Medium | Depends on architecture and team maturity |

### Questions for commercial assessment

1. What is the initial implementation budget?
2. What is the expected platform lifespan?
3. Does the organisation already employ frontend developers?
4. Does the organisation have API integration expertise?
5. What are the ongoing hosting and infrastructure costs?
6. Are additional licences required?
7. What is the cost of replacing incompatible extensions?
8. What are the costs of maintaining separate frontend and backend deployments?
9. Does the selected approach reduce or increase vendor dependency?
10. Can the client support the architecture after consultant handover?

---

# 6. Hosting and Infrastructure Implications

The frontend decision affects infrastructure architecture.

| Infrastructure component | Native | Hyvä | Headless |
|---|---|---|---|
| Adobe Commerce application | Required | Required | Required |
| PHP runtime | Required | Required | Required for Commerce backend |
| Web server / reverse proxy | Required | Required | Required for backend and possibly frontend routing |
| Frontend runtime | Commerce application | Commerce application | Separate frontend runtime or hosting |
| CDN | Recommended | Recommended | Recommended |
| API gateway | Optional | Optional | Often required |
| Separate frontend deployment | No | No | Yes |
| Frontend monitoring | Within application monitoring | Within application monitoring | Separate frontend monitoring |
| Cache strategy | Full-page and application cache | Full-page and application cache | CDN, frontend, API and backend caches |
| CI/CD pipelines | Usually platform pipeline | Usually platform pipeline | Frontend and backend pipelines |

### Headless infrastructure considerations

A headless architecture introduces additional operational components.

Examples:

- Frontend hosting.
- Node.js runtime, if required by the chosen framework.
- CDN and edge rendering.
- API gateway.
- BFF service.
- Frontend build pipeline.
- Separate monitoring and alerting.
- Frontend secrets and environment management.
- API rate limiting.
- Cache invalidation and coordination.

These components must be included in the infrastructure design, cost estimate and support model.

---

# 7. Adobe Commerce Deployment Model Compatibility

The frontend decision must be evaluated against the selected Adobe Commerce deployment model.

Do not assume that all storefront approaches are available across all Adobe Commerce offerings.

| Deployment model | Design consideration |
|---|---|
| Adobe Commerce on Cloud Infrastructure | Evaluate native storefront, Hyvä and supported headless approaches against the current release and service configuration |
| Adobe Commerce on-premises | Evaluate native storefront, Hyvä and API-driven storefronts against the installed version and infrastructure |
| Adobe Commerce as a Cloud Service | Use its supported storefront architecture; Luma is not supported |
| Adobe Commerce Optimizer | Treat storefront and transactional commerce responsibilities separately; validate the connected commerce backend and API architecture |

**Important:** Adobe Commerce as a Cloud Service is not simply another hosting option for the traditional Luma architecture. It has a different platform model and storefront support requirements.

Official architecture references:

- https://experienceleague.adobe.com/en/docs/commerce/information-center/architecture/implementation-architectures
- https://experienceleague.adobe.com/en/docs/commerce/cloud-service/overview

---

# 8. Decision Matrix

Use the following matrix during the Design phase.

Score each architecture from 1 to 5:

| Score | Meaning |
|---:|---|
| 1 | Poor fit |
| 2 | Limited fit |
| 3 | Acceptable fit |
| 4 | Strong fit |
| 5 | Excellent fit |

Suggested evaluation criteria:

| Evaluation criterion | Weight |
|---|---:|
| Business requirements | 15% |
| Performance requirements | 15% |
| Existing extension compatibility | 10% |
| Developer capability | 10% |
| Implementation budget | 10% |
| Time to market | 10% |
| SEO and content requirements | 10% |
| Omnichannel strategy | 10% |
| Long-term maintenance | 5% |
| Infrastructure readiness | 5% |
| **Total** | **100%** |

Calculate:

`Weighted Score = Σ (Architecture Score × Criterion Weight)`

The scoring exercise should support the architecture discussion, not replace technical validation.

### Architecture selection guidance

| Business requirement | Potentially preferred approach |
|---|---|
| Lowest architectural complexity | Native |
| Existing Luma-based implementation with modernisation goals | Hyvä |
| Improved frontend performance without full decoupling | Hyvä |
| Strong native extension dependency | Native |
| Existing React or Next.js team | Headless |
| Multiple customer-facing applications | Headless |
| Independent frontend release cycles | Headless |
| Highly customised omnichannel experience | Headless |
| Limited development budget | Native or Hyvä |
| Commerce-first website with standard customer journeys | Hyvä |
| Adobe Commerce as a Cloud Service | Supported Edge Delivery Services storefront or another supported headless approach |

---

# 9. Architecture Decision Questions

The solution architect should obtain answers to the following before recommending an architecture.

## Business

- What customer experiences must the new platform deliver?
- Is the objective to modernise the existing storefront or transform the entire digital experience?
- Is omnichannel commerce a current requirement or a future possibility?
- Does the organisation need separate B2B and B2C experiences?
- Are there complex customer journeys?

## Technical

- What frontend technologies are currently used?
- Does the organisation have a frontend engineering team?
- What third-party extensions are business-critical?
- Which integrations require frontend SDKs?
- What API capabilities are available?
- What are the performance targets?
- What are the SEO requirements?
- What are the deployment and hosting constraints?

## Operational

- Who will maintain the frontend after go-live?
- Does the client have the required skills?
- Who owns frontend releases?
- Who monitors frontend errors?
- Who handles API failures?
- What is the expected support response time?
- Does the client have a separate frontend support team?

## Commercial

- What is the initial budget?
- What are the licensing implications?
- What are the additional infrastructure costs?
- Are specialist contractors required?
- What is the estimated five-year maintenance cost?

---

# 10. Recommended Design and Validation Activities

The selected architecture should not be approved based on assumptions alone.

The project should complete the following activities.

| Activity | Description | Deliverable |
|---|---|---|
| Existing frontend assessment | Review current frontend technologies, dependencies and functionality | Frontend Assessment |
| Extension assessment | Identify compatibility and replacement requirements | Extension Compatibility Matrix |
| API assessment | Evaluate required APIs and available capabilities | API Assessment |
| UX requirements | Define customer journeys and frontend requirements | UX Requirements |
| Performance assessment | Establish baseline and target performance | Performance Requirements |
| SEO assessment | Identify SEO and URL migration requirements | SEO Architecture Requirements |
| Infrastructure assessment | Evaluate hosting, CDN, runtime and deployment requirements | Infrastructure Assessment |
| Cost assessment | Compare implementation and operational costs | TCO Comparison |
| Proof of concept | Validate critical technical assumptions | Proof of Concept Report |
| Architecture approval | Review and approve the selected approach | Architecture Decision Record |

## 10.1 Proof of Concept Requirements

Where the decision has significant financial or architectural implications, conduct a focused proof of concept.

Recommended test scenarios:

1. Homepage rendering.
2. Category listing.
3. Product detail page.
4. Product search.
5. Add to cart.
6. Cart persistence.
7. Customer login.
8. Checkout.
9. Payment gateway integration.
10. Order confirmation.
11. Customer account.
12. Mobile responsiveness.
13. SEO rendering.
14. Analytics tracking.
15. Third-party extension compatibility.

The proof of concept should validate the highest-risk areas rather than attempting to build the entire storefront.

---

# 11. Architecture Decision Record (ADR) Template

The project must formally record the selected architecture.

## ADR: Adobe Commerce Frontend Architecture

**Decision ID:** ADR-FE-001

**Project:** Adobe Commerce Migration

**Status:** Proposed / Approved / Rejected

**Date:** [Insert date]

### 1. Business Context

Describe the business objectives and frontend requirements driving the decision.

### 2. Existing Architecture

Document:

- Existing frontend technology.
- Existing backend platform.
- Current integrations.
- Existing extensions.
- Current performance.
- Current hosting model.

### 3. Options Evaluated

- Native Adobe Commerce storefront.
- Hyvä storefront.
- Headless storefront.

### 4. Selected Architecture

**Selected option:** [Insert selection]

**Frontend technology:** [Insert technology]

**Backend:** Adobe Commerce

**Rendering model:** [Server-side / Client-side / Hybrid]

**API strategy:** [REST / GraphQL / Both]

**Hosting model:** [Insert hosting model]

### 5. Reason for Selection

Explain why the selected architecture best meets the business, technical and commercial requirements.

### 6. Rejected Alternatives

Document why the other architectures were not selected.

### 7. Integration Impact

Document:

- API requirements.
- Third-party extensions.
- Payment integration.
- Search integration.
- CMS integration.
- CRM and ERP dependencies.
- Middleware dependencies.

### 8. Infrastructure Impact

Document:

- Hosting requirements.
- CDN.
- API gateway.
- Frontend runtime.
- CI/CD.
- Monitoring.
- Security.
- Disaster recovery.

### 9. Risks and Mitigation

| Risk | Impact | Mitigation | Owner |
|---|---|---|---|
| Extension incompatibility | High | Compatibility assessment and replacement planning | Technical Lead |
| Performance degradation | High | Load testing and performance optimisation | Engineering |
| API availability | High | Retry, caching and resilience strategy | Integration Lead |
| Skills shortage | Medium | Training and knowledge transfer | Project Manager |
| Higher maintenance cost | Medium | TCO review and operational planning | Solution Architect |

### 10. Approval

| Role | Name | Approval |
|---|---|---|
| Solution Architect | | |
| Technical Lead | | |
| Enterprise Architect | | |
| Business Owner | | |
| Infrastructure Lead | | |
| Project Manager | | |

---

# 12. Final Design Principles

1. Do not select headless simply because it is considered more modern.
2. Do not select native storefront development simply because it is familiar.
3. Do not select Hyvä without assessing extension compatibility and licensing.
4. Select the architecture based on business requirements, technical constraints and operational capability.
5. Consider the total cost of ownership rather than initial development cost alone.
6. Validate the most critical assumptions through a proof of concept.
7. Design SEO, performance, security and accessibility from the beginning.
8. Confirm that the client can maintain the selected architecture after consultant exit.
9. Document the decision and obtain formal stakeholder approval.
10. Keep the architecture flexible enough to support future experience and channel requirements without introducing unnecessary complexity.

**Final principle: Choose the simplest architecture that satisfies the organisation's business requirements, performance targets, integration needs and long-term digital strategy. Architectural complexity should be justified by measurable business value.**

---

# 13. Official Reference Documentation

| Topic | Documentation |
|---|---|
| Adobe Commerce storefronts | https://experienceleague.adobe.com/en/docs/commerce/information-center/explore-platforms-and-services/overview |
| Implementation architecture options | https://experienceleague.adobe.com/en/docs/commerce/information-center/architecture/implementation-architectures |
| Native frontend development | https://developer.adobe.com/commerce/frontend-core/ |
| Adobe Commerce GraphQL | https://developer.adobe.com/commerce/webapi/graphql/ |
| Adobe Commerce REST | https://developer.adobe.com/commerce/webapi/rest/ |
| PWA Studio | https://developer.adobe.com/commerce/pwa-studio/ |
| PWA Studio architecture | https://developer.adobe.com/commerce/pwa-studio/guides/storefront-architecture/ |
| Hyvä | https://www.hyva.io/ |
| Hyvä documentation | https://docs.hyva.io/ |
| Commerce Storefront | https://experienceleague.adobe.com/en/docs/commerce/storefront/get-started |
| Adobe Commerce as a Cloud Service | https://experienceleague.adobe.com/en/docs/commerce/cloud-service/overview |
| Composable Commerce | https://experienceleague.adobe.com/en/docs/commerce-learn/tutorials/getting-started/capabilities/what-is-composable-commerce |

