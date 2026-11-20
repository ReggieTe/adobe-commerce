# 11. Cross-Phase Governance and Delivery Controls

> Part of the *Enterprise Adobe DXP Migration Handbook* v1.1 (Review Draft). Section numbers (§) refer to the handbook's original numbering; see the root [README](../README.md) for the section map.

## 11.1 Infrastructure Governance

| Phase | Responsibility |
|---|---|
| Discovery | Inventory current infrastructure and hosting |
| Assessment | Compare hosting options per product and responsibilities |
| Design | Define target infrastructure and deployment architecture |
| Build | Provision and configure environments |
| Migration | Prepare infrastructure for migration execution |
| Testing and Cutover | Validate performance, availability and recovery |
| Hypercare | Monitor, document and transfer ownership |

## 11.2 Middleware and Integration Governance

| Phase | Responsibility |
|---|---|
| Discovery | Inventory existing integrations |
| Assessment | Retain, replace or redesign decisions |
| Design | Integration architecture and standards |
| Build | Implement middleware and integrations |
| Migration | Reconfigure integrations; migrate relevant data |
| Testing and Cutover | Validate end-to-end behaviour |
| Hypercare | Stabilise and transfer support documentation |

## 11.3 Third-Party Vendor Governance
Maintain a vendor register: vendor, service, business owner, technical owner, contract and subscription details, integration dependencies, support arrangements, escalation process, renewal dates, data access and ownership, exit considerations. The client retains ownership of vendor accounts and contracts.

## 11.4 Observability Governance
The organisation must be able to tell whether services are available, users can complete key journeys, APIs respond correctly, queues are processing, external integrations are failing, jobs complete, data synchronises and security events need investigation. Monitoring ownership is defined before handover.

## 11.5 Disaster Recovery Governance

| Phase | Responsibility |
|---|---|
| Discovery | Understand existing backup and recovery |
| Assessment | Establish business recovery requirements |
| Design | Define RPO, RTO and recovery architecture |
| Build | Implement backup and recovery |
| Migration | Protect source and target data |
| Testing and Cutover | Test restoration and recovery |
| Hypercare | Document, demonstrate and hand over recovery |

## 11.6 Documentation Governance
Documentation is a continuous deliverable from Discovery onward, validated during implementation and finalised at handover. The client must not receive undocumented systems.
