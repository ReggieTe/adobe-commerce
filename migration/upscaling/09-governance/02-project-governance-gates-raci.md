# 12. Project Governance, Responsibilities and Approval Gates

> Part of the *Enterprise Adobe DXP Migration Handbook* v1.1 (Review Draft). Section numbers (§) refer to the handbook's original numbering; see the root [README](../README.md) for the section map.

## 12.1 Key Project Roles

| Role | Primary responsibility |
|---|---|
| Client Sponsor | Business sponsorship and strategic decisions |
| Client Project Manager | Client-side coordination and governance |
| Consultant / Technical Lead | Design authority, technical direction, assurance (and build under Model A) |
| Solution Architect | Target architecture and technical design |
| Adobe Specialists | Product-specific implementation; **employer named in SoW** |
| Infrastructure Team | Hosting and infrastructure |
| Integration Team | Middleware and external systems |
| Data Team | Migration, validation and reconciliation |
| Security Team | Security and compliance |
| Business Owners | Requirements and acceptance |
| **Operational Owner** | Ongoing platform operations (internal team, MSP or partner) |

Roles may be combined in smaller engagements, but responsibilities must remain clear.

## 12.2 Approval Gates

| Gate | Approval point | Required evidence |
|---|---|---|
| G1 | Discovery acceptance | Current-state discovery report; engagement model confirmed |
| G2 | Strategy approval | Strategy, roadmap, per-product hosting decision record, intended operating model |
| G3 | Design approval | Approved design package; product facts re-verified |
| G4 | Build completion | Implemented solution; consultant review complete (Models B/C) |
| G5 | Migration readiness | Full-volume rehearsal and reconciliation evidence |
| G6 | Production go-live | Testing, UAT and cutover approvals; **operational owner appointed** |
| G7 | Operational acceptance | **Entry: named operational owner (or executed fallback).** Handover documentation, signed knowledge transfer, support readiness |

A phase is not complete merely because its activities were performed. Deliverables must be reviewed and accepted by the appropriate stakeholders.

## 12.3 Change Control
Material changes to approved scope, architecture, cost or timeline follow an agreed process recording description, reason, business, technical, security, cost and timeline impact, dependencies, approval and decision. Architecture changes go in the architecture decision register.

## 12.4 Risk and Issue Management
Maintain a central register: reference, description, category, probability, impact, severity, owner, mitigation, target date, status. Review throughout; transfer unresolved risks to the client at closure.

## 12.5 Phase-by-Phase RACI

R = Responsible, A = Accountable, C = Consulted, I = Informed. Shown for the **default Model B (lead-and-assure)**. Adjust per SoW for Models A and C. "Partner" means the named implementation partner or client build team.

| Phase / activity | Consultant | Client sponsor / PM | Business owners | Partner / build team | Operational owner |
|---|---|---|---|---|---|
| 1 Discovery | A/R | C | C | C | I |
| 2 Strategy, hosting decision | R | A (approves) | C | C | C |
| 3 Design | A/R | A for approval (sign-off) | C | C | C |
| 4 Build | A for standards and review | I | I | R | C |
| 5 Migration execution | A for approach and reconciliation method | I | A for data acceptance | R | I |
| 6 Testing | A for test strategy | C | R for UAT | R | R for readiness tests |
| 6 Go-live decision | C (recommends) | A/R | C | C | C |
| 7 Hypercare | R (supporting) | I | C | R for defect fixes | R (first-line) |
| 7 Handover and knowledge transfer | A/R | A for acceptance | I | C | R (recipient) |
| Operational owner appointment | C | A/R | I | I | – |
| Vendor contracts and subscriptions | C | A/R | I | I | C |

Where a row shows two accountabilities (for example Design), the consultant is accountable for the *quality* of the artefact and the client for its *approval*. Every activity has exactly one named accountable party in the live programme RACI.

## 12.6 Commercial and Contractual Framework (new)
The handbook assumes deliverables and acceptance. The SoW and contract must make them enforceable. At minimum:

- **Engagement model** (§1.4), named partners and subcontractors.
- **Scope by phase and gate**, with deliverables referenced to this handbook's names.
- **Acceptance criteria wording** per deliverable: who accepts, within how many business days, and what deemed acceptance means. Avoid "to the client's satisfaction" without measurable criteria.
- **Payment milestones** tied to gates, with a retention or final payment held to G7.
- **Assumptions and dependencies:** client access, data availability, decision turnaround, third-party vendor responsiveness.
- **Change control** (§12.3) with rate card.
- **Hypercare** duration, hours and what is excluded.
- **Closure and fallback** clauses per §10.8, including the extension rate and risk-acceptance form.
- **Liability, IP ownership and licence of consultant-created artefacts**, including migration tooling.
- **Data protection:** processor and operator roles, POPIA obligations, sub-processors and cross-border transfer terms.
- **Warranty or defect-liability period** and its relationship to hypercare.

Legal counsel reviews the final contract. This section is a checklist, not legal advice.
