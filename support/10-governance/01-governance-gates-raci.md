# 12. Governance, Gates and Responsibilities

> Part of the *Enterprise Adobe DXP Support and Operations Handbook* v1.0 (Review Draft). Section numbers (§) refer to the handbook's original numbering; see the README at the root of this folder for the section map.

## 12.1 Roles
| Role | Responsibility |
|---|---|
| Client Sponsor | Funding, priorities, risk acceptance |
| **Service Owner (client)** | Accountable for the service and its performance |
| Service Manager | Runs processes, reporting and reviews |
| L1 Service Desk | First contact and triage |
| L2 Application Support | Operational troubleshooting and runbooks |
| L3 Technical Support / Consultant | Complex diagnosis, root cause, engineering fixes |
| Incident Commander (rotating) | Leads major incidents |
| Security Lead | Security operations and incident response |
| Vendor Manager | Adobe and third-party relationships |
| Business Owners | Priorities and acceptance |

## 12.2 Approval Gates
| Gate | Approval point | Required evidence |
|---|---|---|
| S1 | Discovery accepted | Assessment report, named service owner |
| S2 | Service design approved | Catalogue, SLA/OLAs, processes, tooling, facts re-verified |
| S3 | Transition-in complete | Runbooks tested, training, shadow success, owner and provider accepted |
| S4 | Live operations reviewed (periodic) | KPI report, incident reviews, restore tests |
| S5 | Improvement reviewed (periodic) | Trend analysis, capacity forecast, improvement register |
| S6 | Lifecycle reviewed (periodic) | Lifecycle calendar, patch and upgrade evidence |
| S7 | Review, renewal or handback | **Entry: named owner and provider**; review report, handover evidence |

## 12.3 Change Control
Changes to the service (scope, hours, severity targets, tooling, staffing) follow a recorded change process: description, reason, impact on service levels, risk, cost, approval and effective date.

## 12.4 RACI (default Model B)
R = Responsible, A = Accountable, C = Consulted, I = Informed.

| Activity | Consultant | Service owner | Service desk (L1) | L2 team | Business owners | Vendors |
|---|---|---|---|---|---|---|
| Service design | A/R | A (approval) | C | C | C | C |
| Transition-in | A (assurance) | C | R | R | I | I |
| Incident handling | C (L3) | A | R | R | I | R |
| Major incident | R (advisor/L3) | A | R | R | I | R |
| Problem management | R | A | I | R | C | C |
| Change and release acceptance | C | A | I | R | C | I |
| Patch and upgrade | C | A | I | R | C | R |
| Monthly reporting | R | A | C | C | I | I |
| Vendor escalation | C | A | R | R | I | R |
| Transition-out and handback | A/R | A (acceptance) | R | R | I | I |

Every row has exactly one accountable party in the live RACI.

## 12.5 Commercial and Contractual Framework
The contract states: engagement model and exact scope; service catalogue; hours and after-hours arrangements; severity definitions and targets with measurement rules; service credits and exclusions (for example Adobe-managed outages outside the provider's control); pricing model (retainer, time-and-materials, tiered); out-of-scope and change rates; reporting; term, renewal and termination; transition-out obligations; liability limits; data protection roles and POPIA terms; IP and tooling ownership; key-person and subcontractor rules. Counsel reviews the contract.
