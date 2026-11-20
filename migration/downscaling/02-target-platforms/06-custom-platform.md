# 16. Target Playbook: Custom Platform

> Part of the *Adobe DXP Downscale Playbook* v1.0 (Review Draft). Section numbers (§) refer to the playbook's original numbering; see the root [README](../README.md) for the section map.

## 16.1 Fit
Appropriate when requirements are genuinely unusual (complex B2B rules, bespoke workflows, deep ERP-driven logic) and the client has, or will fund, an engineering team for the platform's lifetime. Otherwise a packaged platform is usually cheaper and safer.

## 16.2 Build vs Compose
| Option | Description | Trade-offs |
|---|---|---|
| Custom monolith | One application (for example a PHP or other mainstream framework) | Simple deployment; all logic in one codebase; you build commerce primitives |
| Headless composition | Commerce engine or services plus a custom frontend and CMS | Flexible; more moving parts; integration and observability effort |
| Hybrid | Packaged platform with custom extensions and services | Often the best cost-risk balance |

Named products appear only as examples of commerce engines or headless CMSs; selection follows the decision matrix in §3.3.

## 16.3 Architecture Requirements
Define the MVP and keep it small. Cover: catalogue and pricing, cart and checkout, orders and fulfilment, customers and identity, content, search, promotions, tax, shipping, payments, admin tooling, reporting, audit logging, background jobs, and APIs. Use hosted payment fields or redirect gateways to avoid card-data handling. Design for observability, backups, DR and secrets from day one.

## 16.4 Migration Notes
- Design the data model first, then mapping (§17).
- The migration tooling is part of the product and should be tested like code.
- Build reconciliation and an audit trail into the import.
- Import orders as immutable historical records with original references.
- Identity: choose a standard approach (own accounts, external identity provider); handle legacy password hashes the same way as §13.4 with a security review, or force a reset.

## 16.5 Governance Requirements
Coding standards, review, CI/CD, test coverage targets, security scanning, dependency management, documentation, and an architecture decision register. Maintenance budget (typically a continuing percentage of build cost per year, agreed up front) is part of the business case.

## 16.6 Risks
Underestimated scope, key-person dependency, maintenance underfunding, security debt, and reinventing commodity features. Mitigate with a strict MVP, documented architecture, a named operational owner with engineering capability, and an agreed roadmap.

## 16.7 Cutover Specifics
Prefer phased cutover (by channel, region or catalogue slice) with traffic splitting and a strong fallback window, because bespoke platforms have less operational history than packaged ones.

## 16.8 Verify List
Chosen frameworks and component support dates; payment provider integration model; identity approach; hosting region and compliance; team capacity for the lifetime of the platform.
