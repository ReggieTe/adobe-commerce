# 12. Project Governance, Gates and Responsibilities

> Part of the *Enterprise Adobe DXP Development Handbook* v1.0 (Review Draft). Section numbers (§) refer to the handbook's original numbering; see the README at the root of this folder for the section map.

## 12.1 Roles
| Role | Responsibility |
|---|---|
| Client Sponsor | Priorities, budget, risk acceptance |
| Product Owner | Backlog, acceptance |
| Client Project Manager | Coordination |
| Consultant / Technical Lead | Design authority, standards, assurance (and build under Model A) |
| Solution Architect | Architecture |
| Developers (named employer) | Implementation |
| QA / Test Engineers | Quality engineering |
| DevOps / Platform Engineers | Pipelines, environments |
| Security | Security review |
| Business Owners | Acceptance |
| **Operational Owner** | Ongoing maintenance and operations |

## 12.2 Approval Gates
| Gate | Approval point | Required evidence |
|---|---|---|
| E1 | Requirements accepted | Backlog, NFRs, discovery pack |
| E2 | Design approved | Design package, ADRs, facts re-verified |
| E3 | Foundations ready | Pipeline demo, standards agreed |
| E4 | Release candidate complete | Quality gates green, review complete |
| E5 | Quality evidence accepted | Test, performance, security, UAT results |
| E6 | Release approved and verified | Change approval, production verification, **owner accepted release** |
| E7 | Handover accepted | **Entry: named maintaining owner**; docs, KT, roadmap |

## 12.3 Change Control
Changes to scope, architecture, cost or timeline record description, reason, technical, security, cost, timeline and operational impact, approval and decision. Architecture changes update the ADR register.

## 12.4 RACI (default Model B)
R = Responsible, A = Accountable, C = Consulted, I = Informed.

| Activity | Consultant | Client sponsor / PM | Product owner | Build team | QA | Operational owner |
|---|---|---|---|---|---|---|
| 1 Requirements | R | A | A (content) | C | C | I |
| 2 Design | A/R | A (approval) | C | C | C | C |
| 3 Foundations | A (standards) | I | I | R | C | C |
| 4 Implementation | A (review) | I | A (acceptance) | R | C | I |
| 5 Quality engineering | A (strategy) | C | R (UAT) | R | R | C |
| 6 Release approval | C | A/R | C | C | C | C |
| 6 Deployment | C | I | I | R | C | C |
| 7 Stabilisation | R (support) | I | C | R | C | R (first line) |
| 7 Handover | A/R | A (acceptance) | I | C | I | R (recipient) |

Every row has exactly one accountable party in the live RACI.

## 12.5 Commercial and Contractual Framework
The SoW states: engagement model and named partners; scope by phase and gate; acceptance criteria wording and deemed-acceptance rules; payment milestones tied to gates; assumptions and dependencies; change control and rate card; warranty and defect-liability period; IP ownership of custom code and tooling; licences for third-party components; data protection roles; closure and fallback clauses. Counsel reviews the contract.
