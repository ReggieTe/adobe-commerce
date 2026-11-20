# 1. Introduction

> Part of the *Enterprise Adobe DXP Migration Handbook* v1.1 (Review Draft). Section numbers (§) refer to the handbook's original numbering; see the root [README](../README.md) for the section map.

## 1.1 Purpose of this Handbook

This handbook provides a structured, end-to-end methodology for helping an organisation migrate from its existing digital platforms into the Adobe Digital Experience Platform (DXP) ecosystem. It covers the complete transformation lifecycle:

- Understanding the existing digital landscape.
- Assessing business, technical and operational requirements.
- Defining the Adobe DXP architecture and selecting deployment and hosting models.
- Designing infrastructure, middleware and third-party integrations.
- Implementing the target platform.
- Migrating content, data, configurations and business capabilities.
- Testing, cutting over and stabilising.
- Transferring knowledge, documentation and operational responsibility to the client.

This is a project-level migration handbook. Migration is not a simple database transfer or application replacement. The transformation must consider the whole digital ecosystem: customer experiences, applications, data, infrastructure, integrations, security, governance, operations and future scalability.

## 1.2 Migration Direction and Scope

**Migration 1 – Scaling up:** Existing platforms → Adobe DXP.

Potential source platforms: custom enterprise portals, custom PHP/Symfony applications, WooCommerce, PrestaShop, Shopify, existing Adobe Commerce implementations, and other legacy CMS, commerce and digital experience platforms.

**Out of scope:** Migration away from Adobe DXP. A separate handbook should address decommissioning, data extraction, replacement architecture and exit strategy.

## 1.3 Consulting Engagement Model (responsibilities)

The consultant is engaged for a defined transformation programme, not permanent employment. The organisation retains ownership of its systems and long-term operations.

**Consultant responsibilities (default, see §1.4 for variants)**
- Lead technical discovery and assessment.
- Recommend and document architecture.
- Guide technology and hosting decisions.
- Set migration, testing and quality standards, and assure delivery against them.
- Guide production deployment and stabilisation.
- Prepare technical and operational documentation.
- Train and transfer knowledge to the nominated operational owner.
- Complete formal handover and engagement closure.

**Client responsibilities**
- Define business objectives and priorities.
- Provide access to systems, personnel, documentation and vendors.
- Appoint decision-makers, technical representatives and the operational owner.
- Approve architecture, budget, scope and major changes.
- Own business data, accounts, subscriptions and vendor relationships.
- Make the go-live decision and accept the completed solution.

**Joint responsibilities**
- Manage risks and dependencies.
- Agree milestones and approve scope changes.
- Validate business and technical outcomes.
- Agree operational readiness and acceptance.

## 1.4 Engagement Models and Consultant Accountability

The handbook must not leave open whether the consultant builds the solution or oversees those who do. The model is decided at engagement start, recorded in the Statement of Work (SoW) and applied in the RACI (§12.5).

| Model | Description | Consultant accountable for | Typically suits |
|---|---|---|---|
| **A. Consultant-led delivery** | Consultant leads and directly performs architecture, configuration and key build work, with client staff supporting. | Design, build quality, migration execution, testing support, handover | Small to mid-size scope; client has limited technical capacity |
| **B. Lead-and-assure (default)** | Consultant owns architecture, migration approach, quality gates and handover. Build is performed by client teams and/or specialist implementation partners, directed and reviewed by the consultant. | Design authority, standards, code and configuration review, migration approach, gate evidence, handover | Most enterprise engagements |
| **C. Advisory only** | Consultant provides assessment, strategy and design. Delivery and assurance are fully external. | Quality of advice and design documents only | Client already has a delivery partner |

Rules that apply to every model:

1. The model, and any specialist implementation partner, is named in the SoW. "Adobe Specialists" (§12.1) are always attributed to a named organisation.
2. Under Models B and C, the consultant is **not** accountable for defects in work they did not perform, but **is** accountable for the adequacy of the design, standards and review they provided.
3. In every model the consultant does not become the operator of the platform. Operations belong to the client or its appointed provider (see §10.8).
4. Go-live, scope, budget and vendor-contract decisions always remain with the client.

## 1.5 Guiding Principles

1. **Business-first transformation:** Technology decisions support measurable business outcomes.
2. **Architecture before implementation:** Agree the target architecture before major development.
3. **Platform suitability:** Select Adobe products and deployment models from actual requirements.
4. **Integration-aware design:** Treat middleware and external systems as part of the architecture.
5. **Data integrity:** Protect consistency, relationships, ownership and history.
6. **Security by design:** Apply controls across applications, infrastructure, integrations and data.
7. **Operational readiness:** Design monitoring, support and disaster recovery before production.
8. **Controlled migration:** Migration must be repeatable, testable and reconcilable.
9. **Future scalability:** Avoid unnecessary constraints and undocumented dependencies.
10. **Client ownership:** The company retains the knowledge, access and documentation to operate the solution after the consultant exits.
