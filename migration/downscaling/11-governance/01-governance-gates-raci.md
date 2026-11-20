# 19. Project Governance, Gates and Responsibilities

> Part of the *Adobe DXP Downscale Playbook* v1.0 (Review Draft). Section numbers (§) refer to the playbook's original numbering; see the root [README](../README.md) for the section map.

## 19.1 Roles
| Role | Responsibility |
|---|---|
| Client Sponsor | Strategic decisions, accountable for notices and risk acceptance |
| Client Project Manager | Client-side coordination |
| Contract / Procurement Owner | Adobe contract, notice dates, termination |
| Consultant / Technical Lead | Design authority, assurance (and build under Model A) |
| Solution Architect | Target architecture and design |
| Build Partner / Team | Target configuration and development (named in SoW) |
| Data Team | Extraction, migration, reconciliation, archive |
| SEO / Marketing Lead | Traffic baseline, redirects, content and tracking |
| Finance Owner | Order, invoice and retention acceptance |
| Security / Compliance | POPIA, retention, access |
| Business Owners | Requirements and acceptance |
| **Operational Owner** | Ongoing platform operations |

## 19.2 Approval Gates
| Gate | Approval point | Required evidence |
|---|---|---|
| D1 | Exit discovery acceptance | Discovery report, contract timeline, extraction entitlement, baseline |
| D2 | Strategy approval | Target decision record, capability loss register, strategies, overlap budget |
| D3 | Design approval | Design package, URL and SEO design, product facts re-verified |
| D4 | Build completion | Target ready, tooling on sample data, review complete |
| D5 | Migration readiness | Full-volume rehearsal, reconciliation, archive tested |
| D6 | Go-live | Tests, UAT, redirects, **operational owner appointed**, fallback window set |
| D7 | Operational acceptance | **Entry: operational owner and Adobe termination plan evidenced**; handover, SEO recovery, documentation |

## 19.3 Change Control
Material changes (target platform, scope, data depth, dates, cost) follow the change process: description, reason, impact on business, technical, security, cost, timeline and **contract dates**, approval, decision. A target-platform change after D2 re-opens D2.

## 19.4 RACI (default Model B)
R = Responsible, A = Accountable, C = Consulted, I = Informed.

| Activity | Consultant | Client sponsor / PM | Contract owner | Build team | Business owners | Operational owner |
|---|---|---|---|---|---|---|
| 1 Exit discovery | A/R | C | R (contract) | C | C | I |
| 2 Target selection and strategy | R | A | C | C | C | C |
| 3 Design | A/R (quality) | A (approval) | I | C | C | C |
| 4 Build | A (standards, review) | I | I | R | I | C |
| 5 Extraction and migration | A (approach) | I | C | R | A (data acceptance) | I |
| 6 Testing | A (strategy) | C | I | R | R (UAT) | R (readiness) |
| 6 Go-live decision | C | A/R | C | C | C | C |
| 7 Hypercare | R (support) | I | I | R (fixes) | C | R (first line) |
| 7 Handover | A/R | A (acceptance) | I | C | I | R (recipient) |
| Adobe notices and termination | C (prepares) | A | R | I | I | I |
| Operational owner appointment | C | A/R | I | I | I | – |

Every row has exactly one accountable party in the live RACI.

## 19.5 Risk Register Seeds
| Risk | Typical mitigation |
|---|---|
| Notice date missed, contract auto-renews | Contract timeline owner; calendar alerts; early notice with a buffer |
| Extraction entitlement or volume limits | Confirm in D1; start exports early; negotiate assistance |
| SEO and traffic loss | Baseline, URL map, redirect testing, post-launch monitoring |
| Customers locked out (passwords) | Reset flow, communications, support surge plan |
| Capability loss disputes | Signed loss register; plan workarounds |
| Target platform limits found late | Verify limits in D2/D3; prototype risky flows |
| Payment gateway or token problems | Early gateway engagement; test refunds and webhooks |
| Retention or POPIA breach in extracts | Encrypted storage, access logs, deletion plan |
| Overlap cost overruns | Fixed fallback window; decision date for decommissioning |
| No operational owner | Appointment by D6; exit rule §12.7 |

## 19.6 Commercial and Contractual Framework
The SoW should state: engagement model and named partners; scope by phase and gate; acceptance criteria wording and deemed-acceptance rules; payment milestones tied to gates with a final retention at D7; assumptions (access, data availability, Adobe responsiveness, decision turnaround); change control and rate card; hypercare duration and exclusions; closure and fallback clauses; IP ownership of migration tooling and custom code; data protection roles and cross-border terms; and warranty period. The consultant has **no authority over Adobe contract actions**; those stay with the client. Counsel reviews the contract.
