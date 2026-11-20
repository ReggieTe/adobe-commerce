
# Adobe DXP Team Training and Certification Strategy
## Building Technical Capability, Professional Competence and Operational Ownership

**Project Phase:** Cross-Phase – Discovery to Hypercare  
**Document Type:** Training, Certification and Knowledge Transfer Strategy  
**Audience:** Project Managers, Solution Architects, Technical Leads, Developers, QA Engineers, DevOps Engineers, System Administrators, Content Teams and Support Teams

---

# 1. Purpose

This document defines the training, certification and knowledge-transfer strategy for an enterprise Adobe DXP implementation or migration.

The objective is to ensure that the client has the technical knowledge, professional capabilities and operational skills required to manage the platform after the implementation consultants complete their engagement.

The strategy covers:

- Adobe product training.
- Adobe professional certification.
- Technical implementation training.
- Integration and middleware training.
- Cloud and infrastructure training.
- Security and compliance training.
- Quality assurance and testing.
- Content and business-user training.
- Application support and troubleshooting.
- Operational knowledge transfer.
- Continuous professional development.

**Core principle: The implementation team builds the platform while progressively building the client's capability to own, support and evolve it.**

---

# 2. Training Strategy

Training must be aligned with the project lifecycle and the responsibilities of each team.

The project should not wait until Hypercare to introduce knowledge transfer.

Training should be delivered through four complementary approaches.

| Training approach | Description | Expected outcome |
|---|---|---|
| Formal training | Structured courses, workshops and learning paths | Foundational knowledge |
| Professional certification | Official Adobe and technology certifications | Independently validated competence |
| Practical project training | Supervised work on the actual implementation | Applied technical capability |
| Operational knowledge transfer | Runbooks, demonstrations and support simulations | Operational readiness |

## 2.1 Training principles

1. Training must be role-based.
2. Training must reflect the selected Adobe products and deployment model.
3. Certifications must be relevant to the person's responsibilities.
4. Technical teams must receive practical implementation experience.
5. Knowledge transfer must happen continuously.
6. Training attendance alone does not demonstrate competence.
7. Practical assessments must validate operational readiness.
8. Training materials and recordings must be maintained where permitted.
9. The client must retain access to official learning resources.
10. Training progress must be tracked and reported.

---

# 3. Identify the Required Teams

The first step is to identify all teams that will interact with the Adobe DXP ecosystem.

## 3.1 Team structure

| Team | Primary responsibility |
|---|---|
| Enterprise Architecture | Overall enterprise architecture and technology governance |
| Solution Architecture | Adobe DXP solution design |
| Technical Leadership | Technical direction and engineering standards |
| Adobe Development | Adobe product customisation and implementation |
| Frontend Development | Storefront and user-interface development |
| Integration Engineering | APIs, middleware and third-party integrations |
| Cloud / Infrastructure | Hosting, networking and infrastructure operations |
| DevOps / Platform Engineering | CI/CD, environments and deployment automation |
| Database Administration | Database management and performance |
| QA / Testing | Functional, integration, regression and performance testing |
| Security | Application and infrastructure security |
| Content Management | Content creation and publishing |
| Business Operations | Business processes and operational workflows |
| Application Support | Incident management and troubleshooting |
| Service Desk | First-line support and escalation |

A person may perform multiple roles in smaller organisations. Training should be based on actual responsibilities rather than job titles alone.

---

# 4. Adobe Product Training and Certification

Adobe offers role-based learning and certification paths. The project must identify the certifications relevant to the products actually being implemented.

Not every project needs every Adobe certification.

## 4.1 Adobe Commerce

<text color="secondary" size="sm">Relevant for commerce implementation, development, administration and business operations.</text>

| Role | Recommended learning area | Certification direction |
|---|---|---|
| Adobe Commerce Developer | Architecture, modules, APIs, extension development | Adobe Commerce Developer |
| Senior Developer / Technical Lead | Architecture, customisation, integrations, performance | Adobe Commerce Developer Expert, where available |
| Frontend Developer | Themes, storefronts, frontend architecture | Adobe Commerce Front-End Developer |
| Business Analyst | Product, catalogue, promotions, pricing and business processes | Adobe Commerce Business Practitioner |
| Commerce Administrator | Store configuration, catalogue, orders and administration | Adobe Commerce administration learning |
| Solution Architect | Commerce architecture, integrations and deployment models | Relevant Adobe Commerce credentials and architecture training |

Training should cover:

- Adobe Commerce architecture.
- Module development.
- Dependency injection.
- Plugins and observers.
- Service contracts.
- REST and GraphQL APIs.
- EAV and database structure.
- Indexing and caching.
- Search architecture.
- Checkout and payment integrations.
- Multi-store and multi-website configuration.
- B2B and B2C capabilities where applicable.
- Upgrade-safe development.
- Performance optimisation.
- Application troubleshooting.

Official resources:

- [Adobe Commerce certification](https://experienceleague.adobe.com/en/docs/certification/program/overview)
- [Adobe Commerce Developer Documentation](https://developer.adobe.com/commerce/docs/)
- [Adobe Commerce learning resources](https://experienceleague.adobe.com/en/docs/commerce-learn/overview)

## 4.2 Adobe Experience Manager (AEM)

<text color="secondary" size="sm">Relevant for content management, digital experience delivery and enterprise content architecture.</text>

| Role | Recommended learning area | Certification direction |
|---|---|---|
| AEM Developer | Components, templates, services and APIs | AEM Developer |
| AEM Architect | AEM architecture and implementation | AEM Architect |
| Content Author | Content creation, workflows and publishing | AEM author training |
| Content Administrator | Permissions, workflows and content governance | AEM administration training |
| QA Engineer | Authoring, publishing and content validation | AEM testing and functional training |

Training should cover:

- AEM architecture.
- Sites and Assets.
- Components and templates.
- Content fragments.
- Experience fragments.
- Workflows.
- Author and Publish environments.
- Dispatcher and caching.
- Content delivery.
- AEM as a Cloud Service deployment concepts.
- Repository and content governance.
- API and external system integrations.

Official resources:

- [Adobe Experience Manager documentation](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service)
- [Adobe certification programme](https://experienceleague.adobe.com/en/docs/certification/program/overview)

## 4.3 Adobe Experience Platform (AEP)

<text color="secondary" size="sm">Relevant for enterprise customer data, segmentation and activation.</text>

| Role | Recommended learning area | Certification direction |
|---|---|---|
| Data Engineer | Data ingestion, schemas and datasets | Adobe Experience Platform Data Engineer |
| Data Architect | Data architecture and governance | Adobe Experience Platform Architect |
| Marketing Technology Specialist | Segmentation and activation | Relevant Adobe Experience Platform credentials |
| Data Analyst | Data exploration and reporting | Relevant analytics and platform training |

Training should cover:

- Experience Data Model (XDM).
- Schemas and datasets.
- Batch and streaming ingestion.
- Identity namespaces.
- Identity Service.
- Real-Time Customer Profile.
- Data governance.
- Audiences and segmentation.
- Data activation.
- Source and destination connectors.
- API integrations.

Official resources:

- [Adobe Experience Platform documentation](https://experienceleague.adobe.com/en/docs/experience-platform)
- [Adobe Experience Platform learning resources](https://experienceleague.adobe.com/en/docs/platform-learn/overview)

## 4.4 Other Adobe Experience Cloud products

Where applicable, include additional product-specific learning.

| Product | Training focus |
|---|---|
| Adobe Analytics | Digital analytics, implementation and reporting |
| Adobe Target | Testing, personalisation and experimentation |
| Adobe Journey Optimizer | Customer journeys and orchestration |
| Adobe Real-Time CDP | Customer data activation and segmentation |
| Adobe Campaign | Campaign management and automation |
| Adobe Marketo Engage | Marketing automation and lead management |
| Adobe Customer Journey Analytics | Cross-channel analytics |

Do not include these certifications as mandatory unless the corresponding Adobe product is within the project scope.

---

# 5. Third-Party Technology Training and Certification

Adobe DXP implementations frequently depend on external platforms.

The project should identify the third-party systems that are critical to the solution and establish training requirements for the teams responsible for them.

## 5.1 Cloud and infrastructure

| Platform | Relevant training / certification direction |
|---|---|
| AWS | AWS Solutions Architect, Developer and SysOps learning paths |
| Microsoft Azure | Azure Administrator, Solutions Architect and Developer learning paths |
| Google Cloud | Cloud Engineer, Cloud Architect and Developer learning paths |
| Linux | Linux administration and system engineering |
| Kubernetes | Kubernetes administration and application development |
| Docker | Containerisation and deployment |
| Terraform | Infrastructure as Code |
| Ansible | Configuration management and automation |

## 5.2 Integration and middleware

| Platform | Training focus |
|---|---|
| MuleSoft | API-led connectivity and integration development |
| Boomi | Integration development and administration |
| Workato | Workflow automation and enterprise integrations |
| Informatica | Data integration and data management |
| SnapLogic | Integration pipelines |
| Apache Kafka | Event-driven architecture and stream processing |
| RabbitMQ | Message queues and asynchronous processing |
| Kong | API gateway and API management |
| Apigee | API lifecycle management |
| Azure API Management | API governance and management |

## 5.3 Database and data platforms

| Platform | Training focus |
|---|---|
| MySQL | Database administration and optimisation |
| PostgreSQL | Database administration and performance |
| Microsoft SQL Server | Database administration |
| Oracle Database | Enterprise database management |
| Redis | Caching and data structures |
| OpenSearch | Search and indexing |
| Snowflake | Cloud data warehousing |
| Databricks | Data engineering and analytics |
| BigQuery | Cloud analytics |

## 5.4 Security and identity

| Platform | Training focus |
|---|---|
| Microsoft Entra ID | Identity and access management |
| Okta | Identity and access management |
| Auth0 | Application authentication |
| Ping Identity | Enterprise identity |
| CrowdStrike | Endpoint security |
| Qualys | Vulnerability management |
| Snyk | Application security |
| Wiz | Cloud security posture management |

## 5.5 Certification selection principle

Third-party certification must be driven by the technologies actually selected.

For example, if the project selects Azure as its primary infrastructure platform, Azure certifications should take priority over AWS or Google Cloud certifications.

The same applies to middleware, databases, API management and security products.

Official certification and training requirements should be checked against the vendor's current programme before setting examination targets.

---

# 6. Role-Based Training Matrix

The following matrix provides a starting point for defining training requirements.

| Role | Adobe training | Third-party training | Practical assessment |
|---|---|---|---|
| Solution Architect | Adobe product architecture | Cloud architecture, integrations | Architecture review |
| Technical Lead | Product development and extensibility | Git, CI/CD, security | Code and deployment review |
| Adobe Developer | Relevant Adobe product development | PHP, APIs, databases | Feature implementation |
| Frontend Developer | Storefront architecture | JavaScript, React, Vue or Hyvä stack | Storefront implementation |
| Integration Engineer | Adobe APIs and events | iPaaS, API management, messaging | Integration implementation |
| Cloud Engineer | Adobe deployment architecture | AWS, Azure or GCP | Environment provisioning |
| DevOps Engineer | Adobe deployment process | CI/CD, containers, IaC | Pipeline implementation |
| Database Administrator | Adobe data architecture | Selected database platform | Backup and performance assessment |
| QA Engineer | Adobe functional architecture | Automation and performance testing | Test execution |
| Security Engineer | Adobe security architecture | IAM, cloud security, OWASP | Security assessment |
| Content Author | AEM or relevant Adobe authoring tools | Content governance | Content publishing exercise |
| Application Support | Adobe troubleshooting | Monitoring and incident management | Incident simulation |
| Business Analyst | Product capabilities and workflows | Relevant enterprise systems | Business process validation |

---

# 7. Training Across the Seven Project Phases

Training must follow the implementation lifecycle.

## Phase 1 – Discovery

**Objective:** Establish the client's current technical capability.

Activities:
- Identify existing team structures.
- Assess current Adobe and third-party technology knowledge.
- Identify skills gaps.
- Review existing certifications.
- Identify key-person dependencies.
- Identify operational support requirements.
- Establish training objectives.

Deliverables:
- Team capability assessment.
- Skills-gap register.
- Initial training matrix.
- Certification baseline.

## Phase 2 – Assessment and Strategy

**Objective:** Define the skills needed for the target architecture.

Activities:
- Map target technologies to required roles.
- Identify mandatory and optional certifications.
- Establish learning paths.
- Define training budget.
- Identify training providers.
- Determine internal versus external training requirements.

Deliverables:
- Training and certification strategy.
- Role-based learning paths.
- Certification roadmap.
- Training budget and schedule.

## Phase 3 – Design

**Objective:** Align training with the target solution architecture.

Activities:
- Identify product-specific learning requirements.
- Define architecture workshops.
- Identify environment and integration training needs.
- Establish development standards.
- Plan operational knowledge transfer.
- Define practical assessment scenarios.

Deliverables:
- Technical training curriculum.
- Architecture workshop schedule.
- Knowledge-transfer plan.
- Practical assessment criteria.

## Phase 4 – Build and Development

**Objective:** Develop technical capability through practical implementation.

Activities:
- Conduct developer workshops.
- Pair client developers with consultants.
- Review implementation patterns.
- Demonstrate deployment pipelines.
- Train integration engineers.
- Conduct code reviews.
- Introduce testing and security practices.

Deliverables:
- Training attendance records.
- Practical development exercises.
- Code review records.
- Updated skills assessment.
- Certification progress report.

## Phase 5 – Content and Data Migration

**Objective:** Prepare teams to manage content and data processes.

Activities:
- Train content authors.
- Train content administrators.
- Demonstrate data migration processes.
- Explain data mapping and reconciliation.
- Train relevant data and integration engineers.
- Demonstrate migration error handling.

Deliverables:
- Content training materials.
- Data migration procedures.
- Data reconciliation training.
- Migration support documentation.

## Phase 6 – Testing and Cutover

**Objective:** Prepare technical and operational teams for production.

Activities:
- Conduct production deployment workshops.
- Train support teams on incident procedures.
- Conduct failover exercises.
- Demonstrate monitoring and alerting.
- Train teams on rollback procedures.
- Conduct operational simulations.

Deliverables:
- Cutover training records.
- Support team readiness assessment.
- Deployment runbooks.
- Incident simulation results.
- Operational readiness sign-off.

## Phase 7 – Hypercare

**Objective:** Transition responsibility to the client.

Activities:
- Conduct advanced troubleshooting sessions.
- Review production incidents.
- Complete outstanding knowledge transfer.
- Validate operational competence.
- Confirm certification progress.
- Complete formal operational acceptance.

Deliverables:
- Final training report.
- Updated skills-gap assessment.
- Operational competency sign-off.
- Final knowledge-transfer pack.
- Client operational acceptance.

---

# 8. Certification Roadmap

Certification should be planned according to the project's implementation timeline and the availability of the relevant vendor examinations.

## 8.1 Recommended sequence

| Stage | Timing | Focus |
|---|---|---|
| Baseline | Discovery | Existing knowledge and certifications |
| Foundation | Assessment | Foundational product and technology training |
| Professional | Build | Role-specific professional certification |
| Advanced | Build / Testing | Specialist and advanced learning |
| Validation | Testing / Hypercare | Practical operational competence |
| Continuous development | Post-handover | Renewal and additional certifications |

## 8.2 Certification priorities

Use three priority levels.

**Priority 1 – Essential**

Certifications or formal training directly relevant to the production platform and the person's role.

**Priority 2 – Recommended**

Certifications that improve technical depth, integration capability or operational effectiveness.

**Priority 3 – Optional**

Certifications that support future architecture expansion or career development but are not essential for the current project.

## 8.3 Certification governance

For every certification, record:

- Certification name.
- Issuing vendor.
- Relevant product.
- Target employee.
- Business justification.
- Training provider.
- Examination cost.
- Target completion date.
- Completion status.
- Expiry or renewal requirements.
- Verification details, where available.

Use official vendor certification pages to confirm the current exam names, requirements and availability.

---

# 9. Practical Knowledge Transfer

Certification alone does not establish readiness to operate the production platform.

The client team must demonstrate that it can perform the tasks required by its assigned responsibilities.

## 9.1 Developer knowledge transfer

Developers should demonstrate the ability to:

- Understand the application architecture.
- Navigate the codebase.
- Implement supported customisations.
- Build and test integrations.
- Follow coding standards.
- Troubleshoot application errors.
- Execute deployment procedures.
- Investigate performance issues.
- Maintain upgrade compatibility.

## 9.2 Infrastructure and DevOps knowledge transfer

Infrastructure teams should demonstrate the ability to:

- Understand the hosting architecture.
- Provision and configure environments.
- Manage access and secrets.
- Monitor infrastructure health.
- Manage deployments.
- Review logs and metrics.
- Execute backup procedures.
- Restore services.
- Apply security patches within the supported process.
- Execute disaster recovery procedures.

## 9.3 Support team knowledge transfer

Support teams should demonstrate the ability to:

- Classify incidents.
- Identify application versus infrastructure issues.
- Investigate failed transactions.
- Review application logs.
- Identify integration failures.
- Escalate security incidents.
- Follow incident response procedures.
- Communicate service impact.
- Document root-cause findings.

## 9.4 Content team knowledge transfer

Content teams should demonstrate the ability to:

- Create and edit content.
- Manage assets.
- Follow approval workflows.
- Preview content.
- Publish content.
- Manage permissions.
- Follow content governance standards.
- Troubleshoot publishing issues.

---

# 10. Competency Assessment Framework

The project must measure practical capability rather than simply recording course attendance.

Use the following competency levels.

| Level | Description |
|---|---|
| Level 1 – Awareness | Understands the terminology and purpose |
| Level 2 – Foundation | Can perform basic tasks with guidance |
| Level 3 – Practitioner | Can independently perform normal tasks |
| Level 4 – Advanced | Can troubleshoot complex scenarios |
| Level 5 – Specialist | Can design, optimise and guide others |

## 10.1 Example competency assessment

| Capability | Developer | Cloud Engineer | Support Engineer |
|---|---:|---:|---:|
| Architecture understanding | 3 | 3 | 2 |
| Application development | 4 | 1 | 1 |
| Infrastructure management | 1 | 4 | 2 |
| Deployment | 3 | 4 | 2 |
| Integration troubleshooting | 3 | 3 | 3 |
| Security awareness | 3 | 4 | 3 |
| Incident management | 2 | 3 | 4 |
| Disaster recovery | 1 | 4 | 2 |

Scores are illustrative. Actual target levels must be established for each role.

---

# 11. Training Governance and Ownership

Training must have clear ownership and accountability.

| Responsibility | Owner |
|---|---|
| Training strategy | Project Manager / Programme Manager |
| Technical curriculum | Solution Architect |
| Adobe training | Adobe Product Lead |
| Third-party training | Relevant Technical Lead |
| Certification planning | Training Coordinator / HR |
| Practical assessments | Technical Leads |
| Operational training | Application Support Lead |
| Training records | Project Management Office |
| Final competency approval | Client Technical Management |

## 11.1 Consultant responsibilities

The implementation consultants must:

- Identify client skills gaps.
- Recommend relevant learning paths.
- Deliver technical workshops.
- Provide practical implementation guidance.
- Conduct code walkthroughs.
- Demonstrate operational procedures.
- Prepare technical documentation.
- Mentor client technical personnel.
- Validate knowledge transfer.
- Report outstanding capability gaps.

## 11.2 Client responsibilities

The client must:

- Nominate appropriate personnel.
- Allocate time for training.
- Approve training budgets.
- Ensure access to official learning resources.
- Arrange examinations where required.
- Participate in practical exercises.
- Maintain certification records.
- Retain technical documentation.
- Ensure operational teams are available for knowledge transfer.
- Accept ownership of the platform after handover.

---

# 12. Training KPIs and Success Criteria

Training effectiveness must be measurable.

Suggested project KPIs:

| KPI | Measurement |
|---|---|
| Training completion | Percentage of planned training completed |
| Certification progress | Number of target certifications achieved |
| Skills improvement | Difference between baseline and final competency assessment |
| Practical competence | Percentage of assigned tasks passed |
| Knowledge transfer | Percentage of required KT sessions completed |
| Operational readiness | Percentage of support scenarios successfully completed |
| Documentation readiness | Percentage of required operational documents approved |
| Key-person dependency | Number of critical capabilities with only one competent person |
| Support readiness | Ability to resolve assigned incident scenarios |

Example targets should be agreed during project planning rather than treated as universal requirements.

---

# 13. Operational Handover Requirements

Before the consultants exit, the client must demonstrate operational ownership.

The handover must include:

- Approved system architecture.
- Environment and deployment documentation.
- Integration documentation.
- API and authentication documentation.
- Infrastructure and network documentation.
- Monitoring and alerting procedures.
- Backup and disaster recovery procedures.
- Security and access management procedures.
- Incident management runbooks.
- Known issues and workarounds.
- Vendor and support contact information.
- Training materials.
- Certification progress.
- Outstanding skills gaps.
- Escalation matrix.

## 13.1 Operational acceptance criteria

The client must be able to:

1. Explain the overall platform architecture.
2. Identify the major system components and dependencies.
3. Execute approved deployment procedures.
4. Monitor application and infrastructure health.
5. Investigate common incidents.
6. Escalate complex incidents appropriately.
7. Restore services using approved recovery procedures.
8. Manage user access and permissions.
9. Support business users.
10. Maintain the platform within the agreed support model.

Where a capability cannot be transferred fully during the project, it must be recorded as an outstanding risk with a named owner and mitigation plan.

---

# 14. Training Deliverables

| Deliverable | Description |
|---|---|
| Skills-gap assessment | Baseline assessment of client capabilities |
| Training strategy | Overall learning and certification approach |
| Training matrix | Training mapped to roles |
| Certification roadmap | Target certifications and dates |
| Training schedule | Planned workshops and learning sessions |
| Training materials | Slides, exercises and reference documents |
| Attendance register | Record of participation |
| Practical assessments | Evidence of applied capability |
| Certification register | Certification status and renewal details |
| Knowledge-transfer records | Completed handover sessions |
| Competency assessment | Final role-based capability assessment |
| Operational readiness report | Evidence of support readiness |
| Training completion report | Final training status and outstanding gaps |

---

# 15. Final Success Criteria

The training and certification strategy is successful when:

- The client understands the Adobe DXP architecture.
- Relevant technical personnel have completed their role-based learning.
- Required certifications have been achieved or have an approved completion plan.
- Client developers can maintain the implemented solution within their assigned scope.
- Infrastructure teams can manage the selected hosting model.
- Integration teams can support the connected systems.
- Support teams can manage normal incidents and escalations.
- Business users can operate their assigned Adobe products.
- Operational documentation has been delivered and accepted.
- Knowledge transfer has been formally signed off.

---

# 16. Conclusion

An Adobe DXP migration is not complete simply because the platform has been implemented and deployed successfully.

The organisation must also have the people, skills, processes and knowledge required to operate and evolve the platform.

Training and certification should therefore be treated as a formal workstream throughout the project lifecycle.

**The ultimate objective is to leave the client with a functioning platform and a capable team that can operate, support, maintain and continuously improve it without permanent dependency on the implementation consultants.**

**Guiding principle: Build the platform. Develop the people. Transfer ownership.**
