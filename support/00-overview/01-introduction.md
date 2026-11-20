# 1. Introduction

> Part of the *Enterprise Adobe DXP Support and Operations Handbook* v1.0 (Review Draft). Section numbers (§) refer to the handbook's original numbering; see the README at the root of this folder for the section map.

## 1.1 Purpose

This handbook gives a consultant, a managed service provider or a client operations team a structured method for designing, transitioning in, running and continually improving support for an Adobe DXP estate. It covers service design, incident, problem, change and release management, monitoring, security operations, backup and recovery operations, Adobe vendor escalation, reporting and continual improvement.

## 1.2 Scope

**In scope:** L1, L2 and L3 support models; service catalogue and service levels; operational procedures per Adobe product; vendor management; reporting; improvement; transition-in and transition-out.

**Out of scope:** platform migration (migration handbooks), feature development (Development handbook), commercial licensing negotiations and legal advice.

## 1.3 Engagement Models for Support

| Model | Consultant role | Typical fit |
|---|---|---|
| **A. Consultant-provided managed support** | The consultant (or their firm) provides defined L2/L3 support under an SLA | Small and mid-size estates, no internal team |
| **B. Lead-and-assure (default)** | Consultant designs the service, trains and assures; client team or MSP delivers L1/L2; consultant is a named L3/advisor | Most enterprise estates |
| **C. Advisory and audit only** | Consultant reviews, assesses and advises; no operational duty | Client or MSP already runs the service |

Rules for every model:
1. The model, hours, scope, response targets and exclusions are written into the contract.
2. The client owns systems, data, vendor contracts and risk acceptance.
3. The consultant does not silently become the platform operator: any support the consultant provides is defined, time-bound and chargeable under the agreed terms.
4. Unplanned, out-of-scope work follows change control.
5. A **named service owner** exists on the client side at all times (§12).

## 1.4 Guiding Principles

1. **Service, not heroics:** Defined services, owners and targets replace individual knowledge.
2. **Shared responsibility is explicit:** Adobe, the hosting provider, the MSP and the client each know what they own.
3. **Restore first, then fix:** Incident management restores service quickly; problem management removes root causes.
4. **Everything is a runbook:** Repeated tasks are documented, reviewed and tested.
5. **Change is controlled:** Changes are assessed, approved, scheduled and reversible.
6. **Observable by default:** Monitoring covers business journeys, not just servers.
7. **Evidence-based escalation:** Vendor tickets carry the evidence needed for fast resolution.
8. **Security is operational:** Patching, access review and secret rotation are scheduled work.
9. **Measure and improve:** KPIs drive improvement actions, not just reports.
10. **Client ownership:** Documentation, access and knowledge remain with the client.

## 1.5 The "Verify" Convention

Adobe support entitlements, severity definitions, service levels, release cadences, support portals, regions and product lifecycle dates change. Statements in this handbook are indicative. Before the service design is approved (S2), the Service Manager verifies each Adobe-related fact against current Adobe documentation and the client's agreements, and records a *Last verified* date and source.
