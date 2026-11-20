
# Adobe DXP Hosting Architecture Decision Guide
## Adobe-Managed Cloud vs AWS vs Microsoft Azure vs Google Cloud vs Bare Metal

**Project Phase:** Phase 3 – Design  
**Document Type:** Architecture Decision Guide  
**Audience:** Solution Architects, Enterprise Architects, Technical Leads, Infrastructure Engineers, DevOps Engineers, Security Teams and Project Stakeholders

---

## 1. Purpose

This document establishes the hosting and infrastructure considerations when designing an Adobe Digital Experience Platform (DXP) implementation.

The objective is to select a hosting model that supports the organisation's:

- Business and technical requirements.
- Adobe product and deployment model.
- Performance and scalability expectations.
- Availability and disaster recovery requirements.
- Security, regulatory and data residency obligations.
- Integration and network architecture.
- Operational capabilities and support model.
- Budget and total cost of ownership (TCO).
- Future growth and digital transformation strategy.

The hosting decision must be made during the Design phase, following Discovery and Assessment.

**Core principle: Select the hosting architecture based on the Adobe product's supported deployment model and the organisation's operational requirements—not simply on the popularity or advertised cost of a cloud provider.**

---

# 2. Understand the Adobe DXP Hosting Landscape

Adobe DXP is an ecosystem of products and services. Not every product can be deployed using the same hosting model.

Some Adobe products are SaaS, some offer PaaS or managed-service deployment models, and others can be deployed on customer-managed infrastructure.

The first design activity is therefore to identify the hosting model of each Adobe product.

## 2.1 Adobe deployment models

| Deployment model | Description | Infrastructure responsibility |
|---|---|---|
| SaaS | Adobe operates the application and underlying infrastructure | Primarily Adobe |
| PaaS | Adobe provides and operates the hosting platform, while the customer manages application-level responsibilities | Shared |
| Managed Services | Adobe or an approved provider manages an agreed infrastructure and operational scope | Shared according to contract |
| Customer-managed cloud | Customer deploys the application on AWS, Azure or Google Cloud | Customer and cloud provider |
| On-premises | Customer operates the application in its own data centre or hosting facility | Customer |
| Dedicated bare metal | Application runs on dedicated physical servers rather than shared virtual infrastructure | Customer or hosting provider |

These models are not interchangeable. Product eligibility, licensing, support and contractual responsibilities must be confirmed before selecting an architecture.

## 2.2 Adobe product hosting considerations

| Adobe product | Typical deployment consideration |
|---|---|
| Adobe Commerce as a Cloud Service | Adobe-hosted SaaS |
| Adobe Commerce on Cloud Infrastructure | Adobe-managed PaaS, hosted on AWS or Azure |
| Adobe Commerce on-premises | Customer or hosting-provider infrastructure |
| Adobe Experience Manager as a Cloud Service | Adobe-hosted cloud service |
| AEM 6.5 | On-premises, supported cloud infrastructure or Adobe Managed Services, depending on the offering |
| Adobe Experience Platform | Adobe-managed cloud service |
| Adobe Real-Time CDP | Adobe-managed cloud service |
| Adobe Journey Optimizer | Adobe-managed cloud service |
| Adobe Target | Adobe-managed cloud service |
| Adobe Analytics | Adobe-managed cloud service |
| Adobe App Builder | Adobe extensibility platform and managed runtime |
| Adobe Commerce Optimizer | Separate Adobe service with its own architecture and integration considerations |

**Important:** Do not assume that selecting AWS, Azure, Google Cloud or bare metal means every Adobe DXP component can be hosted there. Several Adobe services remain Adobe-operated SaaS products, even when integrated with customer-managed infrastructure.

### Official Adobe references

- [Adobe Commerce deployment models](https://experienceleague.adobe.com/en/docs/commerce/information-center/explore-platforms-and-services/platform-and-services)
- [Adobe Commerce SaaS and PaaS feature comparison](https://experienceleague.adobe.com/en/docs/commerce/cloud-service/feature-comparison)
- [Adobe Commerce implementation architecture options](https://experienceleague.adobe.com/en/docs/commerce/information-center/architecture/implementation-architectures)
- [AEM as a Cloud Service overview](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/overview/introduction)

---

# 3. Hosting Option 1 – Adobe-Managed Cloud

## 3.1 Overview

Adobe-managed cloud hosting provides an environment in which Adobe operates some or most of the underlying infrastructure and platform services.

The level of responsibility retained by the customer depends on the specific Adobe product and its deployment model.

For Adobe Commerce, two important models must be distinguished:

**A. Adobe Commerce as a Cloud Service (SaaS)**

Adobe operates the Commerce platform, infrastructure and core application. The customer extends the platform through supported APIs and extensibility mechanisms.

**B. Adobe Commerce on Cloud Infrastructure (PaaS)**

Adobe provides the managed cloud platform, while the customer retains application-level responsibilities such as custom code, configuration, application patches and extension compatibility.

Adobe Commerce on Cloud Infrastructure uses AWS or Azure as its underlying infrastructure provider. The customer is consuming Adobe's PaaS offering rather than independently managing an AWS or Azure deployment.

## 3.2 Architecture characteristics

- Adobe-managed infrastructure or platform services.
- Product-specific deployment and release processes.
- Managed infrastructure services and platform components.
- Defined integration and extension mechanisms.
- Vendor-supported operational processes.
- Reduced infrastructure administration compared with self-hosting.

## 3.3 Advantages

- Reduced infrastructure management.
- Adobe-aligned platform architecture.
- Access to product-specific hosting and deployment capabilities.
- Less responsibility for physical infrastructure.
- Established platform support and maintenance processes.
- Potentially simpler operational governance.
- Reduced need for an internal infrastructure engineering team.

## 3.4 Limitations and considerations

- Less infrastructure-level control.
- Platform customisation restrictions, particularly under SaaS.
- Dependency on Adobe's supported extension mechanisms.
- Product-specific limitations around networking and infrastructure access.
- Commercial licensing and service costs.
- Dependence on Adobe release schedules and platform policies.
- Not every external integration can be installed or operated as a traditional server-side extension.

## 3.5 Best suited for

- Organisations prioritising managed operations.
- Enterprises adopting Adobe's cloud-native products.
- Businesses with limited infrastructure management capacity.
- Organisations that prefer vendor-managed platform availability and updates.
- Projects where the supported Adobe deployment model meets the required customisation and integration needs.

## 3.6 Key design questions

1. Does the required Adobe product support the selected deployment model?
2. Can all required customisations be implemented using supported extension mechanisms?
3. Are third-party integrations compatible with the Adobe environment?
4. What infrastructure and operational responsibilities remain with the customer?
5. What are the contractual uptime, support and recovery commitments?
6. What happens when Adobe introduces platform changes?
7. Are the required data residency and compliance arrangements supported?

---

# 4. Hosting Option 2 – Amazon Web Services (AWS)

## 4.1 Overview

AWS is a hyperscale cloud computing platform that provides infrastructure and managed services for customer-managed applications.

An organisation can deploy a supported Adobe Commerce on-premises installation on AWS infrastructure, subject to Adobe's system requirements and support conditions.

AWS can also host supporting components around Adobe SaaS and PaaS products, including:

- Custom middleware.
- Integration services.
- API gateways.
- Event-processing services.
- External applications.
- Data processing and analytics.
- Customer-managed storefronts.
- Custom applications and microservices.

AWS is also one of the infrastructure providers used by Adobe Commerce on Cloud Infrastructure.

## 4.2 Relevant AWS services

| Category | AWS service | Purpose |
|---|---|---|
| Compute | EC2 | Virtual servers for application workloads |
| Containers | ECS / EKS | Containerised applications and orchestration |
| Serverless | Lambda | Event-driven functions |
| Load balancing | Elastic Load Balancing | Distributes application traffic |
| Database | RDS / Aurora | Managed relational databases |
| Cache | ElastiCache | Redis or Valkey-compatible caching |
| Search | OpenSearch Service | Search and indexing |
| Storage | S3 | Object and file storage |
| CDN | CloudFront | Content delivery |
| DNS | Route 53 | DNS management |
| Networking | VPC | Network isolation and segmentation |
| Private connectivity | PrivateLink | Private service connectivity |
| Messaging | SQS / SNS | Queues and event notifications |
| Streaming | Kinesis / MSK | Event streaming |
| Security | IAM / KMS / WAF | Identity, encryption and application protection |
| Monitoring | CloudWatch | Infrastructure and application monitoring |
| Secrets | Secrets Manager | Secure credential management |

## 4.3 Advantages

- Broad infrastructure and managed-service ecosystem.
- Mature global infrastructure.
- Flexible compute and storage options.
- Strong container and serverless capabilities.
- Extensive integration and automation services.
- Flexible networking and private connectivity.
- Mature disaster recovery and backup capabilities.
- Large partner and engineering ecosystem.

## 4.4 Limitations and considerations

- Requires cloud architecture and operational expertise.
- Infrastructure configuration is the customer's responsibility for self-managed deployments.
- Costs can increase through excessive resource consumption and data transfer.
- Managed services introduce additional service-specific costs.
- Poor architecture can create unnecessary complexity.
- Security configuration and access management require continuous attention.
- Adobe support depends on using supported software versions and configurations.

## 4.5 Best suited for

- Enterprises with existing AWS investments.
- Organisations requiring infrastructure control.
- Adobe Commerce on-premises deployments.
- Custom headless storefronts and middleware.
- Complex integration architectures.
- Businesses requiring a broad range of cloud-native services.

## 4.6 South African infrastructure consideration

AWS provides an Africa (Cape Town) region:

- Region: `af-south-1`
- Location: Cape Town, South Africa
- Availability zones: Three

The availability of a regional data centre can help reduce network latency and support data-location requirements. It does not automatically guarantee that every AWS service is available in that region.

[Official AWS Regions documentation](https://docs.aws.amazon.com/global-infrastructure/latest/regions/aws-regions.html)

---

# 5. Hosting Option 3 – Microsoft Azure

## 5.1 Overview

Microsoft Azure is a hyperscale cloud platform offering infrastructure, managed databases, networking, identity, security, integration and application hosting services.

Azure is a relevant option for organisations with an established Microsoft technology ecosystem.

It can host supported customer-managed Adobe Commerce deployments and complementary DXP infrastructure, including middleware, custom applications and headless storefronts.

Azure is also one of the infrastructure providers used by Adobe Commerce on Cloud Infrastructure.

## 5.2 Relevant Azure services

| Category | Azure service | Purpose |
|---|---|---|
| Compute | Azure Virtual Machines | Virtual servers |
| Containers | Azure Kubernetes Service (AKS) | Container orchestration |
| Serverless | Azure Functions | Event-driven processing |
| App hosting | Azure App Service | Web application hosting |
| Load balancing | Azure Load Balancer / Application Gateway | Traffic distribution |
| Database | Azure Database for MySQL | Managed relational database |
| Database | Azure SQL Database | Microsoft SQL workloads |
| Cache | Azure Managed Redis | Managed caching |
| Storage | Azure Blob Storage | Object and file storage |
| CDN / edge | Azure Front Door | Global application delivery |
| Networking | Azure Virtual Network | Network isolation |
| Private connectivity | Private Link | Private service connectivity |
| Messaging | Azure Service Bus | Enterprise messaging |
| Event processing | Event Grid | Event routing |
| Streaming | Event Hubs | Event streaming |
| API management | Azure API Management | API governance and security |
| Identity | Microsoft Entra ID | Identity and access management |
| Security | Key Vault / Defender for Cloud | Secrets and security management |
| Monitoring | Azure Monitor / Application Insights | Observability |

**Technical validation:** Check the current Adobe Commerce system requirements and supported service matrix before selecting Azure managed database, cache or search services. A service being available in Azure does not automatically make it an Adobe-supported configuration.

## 5.3 Advantages

- Strong Microsoft enterprise ecosystem.
- Integration with Microsoft Entra ID.
- Established enterprise identity and access management.
- Mature hybrid cloud capabilities.
- Strong integration with Microsoft business applications.
- Managed infrastructure and database services.
- Private networking and enterprise connectivity.
- Suitable for organisations with existing Microsoft licensing and operational expertise.

## 5.4 Limitations and considerations

- Requires Azure infrastructure and DevOps expertise.
- Managed service compatibility must be validated.
- Costs can increase across networking, monitoring and managed services.
- Complex architectures require careful governance.
- Identity integration must be designed across Adobe and non-Adobe systems.
- Service availability differs by Azure region.

## 5.5 Best suited for

- Enterprises already invested in Microsoft technologies.
- Organisations using Microsoft Dynamics 365.
- Businesses with Entra ID and Microsoft security operations.
- Hybrid cloud environments.
- Enterprises requiring private connectivity to internal systems.
- Customer-managed Adobe Commerce and DXP integration workloads.

## 5.6 South African infrastructure consideration

Azure provides two South African regions:

| Region | Location | Availability zones |
|---|---|---|
| South Africa North | Johannesburg | Three |
| South Africa West | Cape Town | No availability zones listed |

The actual availability of individual Azure services and disaster recovery features must be checked for the chosen region.

[Official Azure regions documentation](https://learn.microsoft.com/en-us/azure/reliability/regions-list)

---

# 6. Hosting Option 4 – Google Cloud Platform (GCP)

## 6.1 Overview

Google Cloud Platform provides cloud infrastructure, managed databases, containers, analytics, networking, storage and AI services.

GCP is a possible infrastructure choice for customer-managed applications and supporting services around Adobe DXP.

Examples include:

- Custom Adobe Commerce integrations.
- Headless storefront applications.
- API and middleware services.
- Data engineering and analytics.
- Event processing.
- AI and machine learning workloads.
- Customer-managed applications.

GCP should not be confused with an Adobe-managed hosting option. The organisation must validate the supportability of its proposed Adobe application deployment against Adobe's published system requirements.

## 6.2 Relevant GCP services

| Category | Google Cloud service | Purpose |
|---|---|---|
| Compute | Compute Engine | Virtual machines |
| Containers | Google Kubernetes Engine (GKE) | Container orchestration |
| Serverless | Cloud Run | Container-based serverless hosting |
| Serverless | Cloud Functions | Event-driven functions |
| Load balancing | Cloud Load Balancing | Traffic distribution |
| Database | Cloud SQL | Managed relational databases |
| Database | AlloyDB | Managed PostgreSQL-compatible database |
| Cache | Memorystore | Managed caching |
| Storage | Cloud Storage | Object storage |
| CDN | Cloud CDN | Content delivery |
| Networking | VPC | Network isolation |
| Private connectivity | Private Service Connect | Private service connectivity |
| Messaging | Pub/Sub | Messaging and event distribution |
| API management | Apigee | API management |
| Identity | Cloud IAM | Identity and access management |
| Security | Cloud KMS / Secret Manager | Encryption and secrets |
| Monitoring | Cloud Monitoring | Infrastructure monitoring |
| Analytics | BigQuery | Data warehousing and analytics |

## 6.3 Advantages

- Strong data analytics ecosystem.
- Mature Kubernetes and container services.
- Strong serverless application hosting.
- Integrated data processing and AI capabilities.
- Global infrastructure.
- Managed database and storage services.
- Suitable for data-intensive and API-driven applications.

## 6.4 Limitations and considerations

- Adobe Commerce compatibility must be verified for the exact deployment.
- Requires GCP operational expertise.
- May introduce another cloud platform if the organisation already standardises on AWS or Azure.
- Costs require careful monitoring.
- Some services and capabilities differ by region.
- Integration with existing enterprise systems may require additional architecture.

## 6.5 Best suited for

- Organisations with existing GCP investments.
- Data-intensive DXP ecosystems.
- AI and analytics workloads.
- Custom applications and integration services.
- Containerised and serverless applications.
- Organisations with established Google Cloud engineering capabilities.

## 6.6 South African infrastructure consideration

GCP provides the Johannesburg region:

- Region: `africa-south1`
- Location: Johannesburg, South Africa
- Zones: `africa-south1-a`, `africa-south1-b`, `africa-south1-c`

Confirm the availability of individual services, machine types and regional features before designing the production architecture.

[Official Google Cloud regions and zones](https://cloud.google.com/compute/docs/regions-zones)

---

# 7. Hosting Option 5 – Bare Metal / Dedicated Infrastructure

## 7.1 Overview

Bare-metal hosting uses dedicated physical servers rather than relying on shared virtualised cloud infrastructure.

The infrastructure may be:

1. Owned and operated by the organisation in its own data centre.
2. Rented from a dedicated-server hosting provider.
3. Hosted in a colocation facility where the organisation supplies or leases its hardware.
4. Operated by a managed hosting provider under a contractual service agreement.

Bare metal can support a customer-managed Adobe Commerce on-premises deployment, provided that the hardware, operating system and software stack meet Adobe's published requirements.

It is important to distinguish bare metal from traditional shared hosting. Adobe Commerce is an enterprise application and requires a properly engineered infrastructure environment.

## 7.2 Typical infrastructure components

| Component | Purpose |
|---|---|
| Dedicated application servers | Execute Adobe Commerce application workloads |
| Database servers | Store transactional and application data |
| Cache servers | Support Redis or Valkey caching |
| Search servers | Run supported OpenSearch or other approved search infrastructure |
| Message queue servers | Process asynchronous application workloads |
| Load balancers | Distribute application traffic |
| Storage | Store media, backups and application files |
| Firewall | Network protection |
| CDN | Distribute static content globally |
| Backup infrastructure | Protect application and database data |
| Monitoring | Infrastructure and application observability |

## 7.3 Advantages

- Greater control over physical infrastructure.
- Dedicated hardware resources.
- Predictable hardware allocation.
- Potentially attractive economics for stable, high-utilisation workloads.
- Control over hardware and network configuration.
- Suitable for specific data residency or infrastructure policies.
- Can support legacy systems with specialised infrastructure requirements.

## 7.4 Limitations and considerations

- Hardware procurement and replacement.
- Capacity planning and provisioning.
- Physical infrastructure maintenance.
- Data centre connectivity and redundancy.
- Hardware failure and replacement procedures.
- Manual scaling unless additional infrastructure is provisioned.
- Disaster recovery requires a separate facility or recovery environment.
- Requires infrastructure engineering and system administration skills.
- Customer or provider carries more responsibility for patching, monitoring and security.
- High availability must be designed and tested rather than assumed.

## 7.5 Best suited for

- Organisations with existing data centres.
- Enterprises with strict infrastructure control requirements.
- Stable workloads with predictable capacity needs.
- Businesses with experienced infrastructure teams.
- Organisations requiring dedicated hardware.
- Workloads where a detailed TCO analysis justifies dedicated infrastructure.

## 7.6 Important design consideration

Bare metal does not automatically mean better performance, lower cost or greater security.

A poorly designed dedicated environment can be less resilient than a properly designed cloud architecture.

The architecture must account for:

- Redundant power.
- Network redundancy.
- Hardware replacement.
- Database replication.
- Backup isolation.
- Physical access control.
- Disaster recovery.
- Monitoring and alerting.
- Security patching.
- Capacity management.

---

# 8. Hosting Comparison Matrix

| Consideration | Adobe-managed cloud | AWS | Azure | Google Cloud | Bare metal |
|---|---|---|---|---|---|
| Infrastructure control | Low | High | High | High | Very high |
| Infrastructure management | Mostly Adobe | Customer | Customer | Customer | Customer/provider |
| Initial setup | Lower | Medium | Medium | Medium | High |
| Operational complexity | Lower to medium | High | High | High | Very high |
| Scalability | Product-dependent | High | High | High | Hardware-dependent |
| Managed services | Adobe-provided | Extensive | Extensive | Extensive | Provider-dependent |
| Customisation freedom | Product-dependent | High | High | High | High |
| Hardware control | Low | Low | Low | Low | Very high |
| Global reach | Product-dependent | Extensive | Extensive | Extensive | Provider-dependent |
| High availability | Product-dependent | Customer-designed | Customer-designed | Customer-designed | Customer-designed |
| Disaster recovery | Contract/product-dependent | Customer-designed | Customer-designed | Customer-designed | Customer-designed |
| Vendor lock-in | Adobe dependency | AWS dependency | Azure dependency | GCP dependency | Hardware/provider dependency |
| Infrastructure skills | Lower | Required | Required | Required | Extensive |
| Cost structure | Subscription/service fees | Consumption-based | Consumption-based | Consumption-based | Hardware and operational costs |

This matrix is a starting point. Actual costs, availability and responsibilities depend on the product, region, architecture, licensing and contract.

---

# 9. Infrastructure Architecture Considerations

The hosting decision must consider the complete DXP environment, not only the Adobe application server.

## 9.1 Application architecture

Identify where the following components will run:

- Adobe Commerce backend.
- AEM or other content platform.
- Headless storefront.
- Custom applications.
- Middleware.
- API gateway.
- Integration services.
- Scheduled jobs and background workers.
- Event consumers and producers.

For Adobe SaaS products, the Adobe-managed service remains the hosting boundary. Customer-managed applications and integrations may run in a separate cloud environment.

## 9.2 Database architecture

Determine:

- Database engine and supported version.
- Managed versus self-managed database.
- Database replication.
- Backup frequency.
- Point-in-time recovery.
- Encryption at rest.
- Network isolation.
- Database connection limits.
- Read and write workload patterns.
- Recovery time and recovery point objectives.

Do not select a managed database simply because the cloud provider offers it. Confirm that the exact engine, version and configuration are supported for the selected Adobe Commerce release.

## 9.3 Cache architecture

Evaluate:

- Redis or Valkey compatibility.
- Session storage.
- Full-page caching.
- Cache invalidation.
- Distributed cache requirements.
- Cache persistence requirements.
- Failover behaviour.

## 9.4 Search architecture

Evaluate:

- Supported OpenSearch versions.
- Indexing workload.
- Search cluster sizing.
- Cluster availability.
- Search data recovery.
- Network connectivity.
- Search service monitoring.

## 9.5 Storage architecture

Determine the appropriate storage solution for:

- Product images.
- Documents.
- Customer-uploaded files.
- Content assets.
- Application backups.
- Database backups.
- Logs and archived data.

Consider object storage where appropriate, but validate application compatibility, access controls, retention and recovery.

## 9.6 CDN and edge delivery

Evaluate:

- Global content delivery.
- Static asset caching.
- Image optimisation.
- Dynamic content caching.
- Web Application Firewall (WAF).
- DDoS protection.
- SSL/TLS certificate management.
- Cache invalidation.
- Geographic traffic distribution.

Potential services include:

- Adobe-supported CDN services.
- AWS CloudFront.
- Azure Front Door.
- Google Cloud CDN.
- Cloudflare.
- Akamai.
- Fastly.

The selected CDN must be compatible with the Adobe product's architecture and contractual requirements.

---

# 10. High Availability and Disaster Recovery

High availability and disaster recovery are separate architectural concerns.

**High availability (HA)** protects against component or infrastructure failures while keeping the application operational.

**Disaster recovery (DR)** restores services after a major incident affecting the production environment or location.

## 10.1 High availability considerations

| Layer | Design consideration |
|---|---|
| DNS | Redundant DNS resolution |
| CDN | Resilient edge delivery |
| Load balancing | Multiple application targets |
| Application | Multiple application instances |
| Database | Supported replication and failover |
| Cache | Redundant cache configuration |
| Search | Cluster availability |
| Messaging | Durable queues and recovery |
| Storage | Replication and backup |
| Network | Redundant network paths |

## 10.2 Disaster recovery considerations

The design must define:

- Recovery Point Objective (RPO).
- Recovery Time Objective (RTO).
- Backup frequency.
- Backup retention.
- Database recovery.
- File and object storage recovery.
- Infrastructure recreation.
- DNS and traffic switching.
- Integration recovery.
- Recovery testing frequency.
- Business continuity procedures.

Example requirements:

| Requirement | Example target |
|---|---|
| RPO | 15 minutes |
| RTO | 4 hours |
| Backup frequency | Continuous or scheduled, depending on data layer |
| Backup retention | Defined by business and regulatory policy |
| DR testing | At least annually, with more frequent tests where required |

These are illustrative values, not universal Adobe service commitments. The business must approve the actual targets.

## 10.3 Important Adobe consideration

For Adobe-managed SaaS and PaaS products, confirm the service-specific recovery arrangements and contractual commitments.

For customer-managed deployments, the organisation must design, implement and test its own recovery architecture.

---

# 11. Security, Compliance and Data Residency

Hosting decisions must be assessed against the organisation's regulatory and security requirements.

## 11.1 Security considerations

- Network segmentation.
- Private networking.
- Firewall and WAF configuration.
- Identity and access management.
- Privileged access management.
- Multi-factor authentication.
- Encryption at rest.
- Encryption in transit.
- Secrets management.
- Vulnerability management.
- Security patching.
- Centralised logging.
- Intrusion detection.
- Backup protection.
- Incident response.

## 11.2 Data residency

Identify where the following data will be stored and processed:

- Customer personal information.
- Customer account records.
- Payment-related information.
- Transaction records.
- Product and pricing information.
- Marketing and behavioural data.
- Content assets.
- Application logs.
- Backups and disaster recovery copies.

The location of the primary application does not necessarily determine the location of every connected service or backup.

Review the complete data flow, including Adobe SaaS services, analytics, payment providers, integrations, support access and third-party processors.

For South African deployments, assess applicable POPIA requirements and contractual obligations. Data residency and cross-border processing must be assessed at the data-flow level rather than assumed from the hosting region alone.

---

# 12. Cost and Total Cost of Ownership (TCO)

The cheapest hosting quotation is not necessarily the cheapest operating architecture.

A proper comparison must include infrastructure, operations, support, licensing, networking and disaster recovery.

## 12.1 Cost categories

| Cost category | Examples |
|---|---|
| Compute | Virtual machines, containers, dedicated servers |
| Database | Managed database, database servers, storage |
| Storage | Object storage, block storage, backups |
| Networking | Data transfer, private connectivity, load balancing |
| CDN | Bandwidth, requests, WAF and edge services |
| Search | Managed search or dedicated search clusters |
| Monitoring | Logs, metrics, tracing and alerting |
| Security | WAF, vulnerability scanning, security tools |
| Licensing | Adobe, operating systems, middleware and third-party software |
| Support | Cloud support plans, Adobe support, managed hosting |
| Engineering | DevOps, infrastructure and application maintenance |
| Disaster recovery | Secondary infrastructure, replication and testing |
| Migration | Infrastructure setup, deployment and data transfer |

## 12.2 Commercial comparison

| Model | Primary cost structure |
|---|---|
| Adobe SaaS | Adobe subscription and contracted services |
| Adobe PaaS | Adobe platform subscription and associated services |
| AWS | Infrastructure consumption and managed services |
| Azure | Infrastructure consumption and managed services |
| Google Cloud | Infrastructure consumption and managed services |
| Bare metal | Hardware, colocation or hosting fees, support and operations |

## 12.3 TCO evaluation

The project should calculate:

- Initial migration and implementation cost.
- Monthly infrastructure cost.
- Annual support and maintenance cost.
- Licensing and subscription cost.
- Infrastructure engineering cost.
- Backup and DR cost.
- Network and data transfer cost.
- Expected growth over three to five years.
- Cost of downtime and operational incidents.
- Exit and migration costs.

Use actual provider quotations and workload estimates rather than generic cloud pricing assumptions.

---

# 13. Hybrid and Multi-Cloud Architecture

An Adobe DXP implementation does not necessarily need to run entirely within one hosting environment.

A hybrid architecture can use Adobe-managed services alongside customer-managed cloud infrastructure.

Example:

```text
                    CUSTOMERS
                        |
                        v
                 CDN / WAF / DNS
                        |
                        v
               HEADLESS STOREFRONT
                        |
                        v
               API / INTEGRATION LAYER
                        |
           +------------+-------------+
           |            |             |
           v            v             v
     ADOBE COMMERCE   AEM / DXP    THIRD-PARTY
       SAAS / PAAS    SERVICES      SYSTEMS
           |            |             |
           +------------+-------------+
                        |
                        v
                ENTERPRISE SYSTEMS
                        |
          +-------------+-------------+
          |             |             |
          v             v             v
         ERP           CRM          PAYMENT
```

The diagram is conceptual. The actual integration paths depend on the Adobe product, API capabilities, network boundaries and transaction ownership.

## 13.1 Example hybrid arrangements

| Adobe services | Customer-managed infrastructure |
|---|---|
| Adobe Commerce SaaS | AWS-hosted middleware |
| AEM as a Cloud Service | Azure-hosted enterprise integration |
| Adobe Analytics | GCP data processing |
| Adobe Commerce PaaS | External payment and ERP integration services |
| Adobe Target | Customer-managed storefront |
| Adobe Experience Platform | External enterprise data platforms |

## 13.2 Benefits

- Organisations can retain existing infrastructure investments.
- Different workloads can use services best suited to their requirements.
- Adobe-managed services reduce selected operational responsibilities.
- Existing enterprise systems can remain within their current hosting environments.
- Integration services can be deployed close to the systems they connect to.

## 13.3 Risks

- Increased network complexity.
- Cross-cloud data transfer costs.
- More complex identity and access management.
- Multiple operational teams and support contracts.
- More complicated incident management.
- Additional security and compliance boundaries.
- Dependency on multiple cloud providers.

**Recommendation:** Prefer a clearly governed primary cloud strategy where possible. Introduce multi-cloud only where a measurable business, technical, regulatory or resilience requirement justifies the additional complexity.

---

# 14. Hosting Decision Framework

The project team should evaluate hosting options against business and technical requirements.

## 14.1 Decision criteria

| Criteria | Suggested weighting |
|---|---:|
| Adobe product compatibility and supportability | 15% |
| Security and compliance | 15% |
| Availability and disaster recovery | 15% |
| Total cost of ownership | 15% |
| Scalability and performance | 10% |
| Integration and networking | 10% |
| Internal technical capability | 10% |
| Infrastructure control and flexibility | 5% |
| Regional availability and data residency | 5% |
| **Total** | **100%** |

The weighting should be adjusted according to the client's priorities.

## 14.2 Hosting selection questions

### Adobe compatibility
- Which Adobe products are being implemented?
- Which deployment models are supported?
- Are the required integrations supported?
- Are the proposed infrastructure components compatible with the Adobe release?

### Business requirements
- What is the expected traffic?
- What are the transaction volumes?
- Are there seasonal peaks?
- What availability is required?
- What is the expected business growth?

### Infrastructure
- Does the organisation already use AWS, Azure or Google Cloud?
- Are there existing data centres?
- Is there a preferred hosting provider?
- Is regional hosting required?
- Is private connectivity necessary?

### Operations
- Who will manage the infrastructure?
- Is there a 24/7 support team?
- Who handles security patches?
- Who monitors application and infrastructure health?
- Who is responsible for disaster recovery?

### Financial
- What is the initial implementation budget?
- What is the monthly operational budget?
- What is the expected three-to-five-year TCO?
- Are there existing cloud commitments or enterprise agreements?

---

# 15. Proof of Concept and Infrastructure Validation

Before finalising the hosting architecture, validate the selected option through a technical proof of concept where necessary.

## 15.1 Required validation activities

| Activity | Validation objective |
|---|---|
| Environment provisioning | Confirm infrastructure can be provisioned |
| Adobe installation or onboarding | Confirm deployment eligibility |
| Software compatibility | Validate supported versions |
| Network connectivity | Validate internal and external connectivity |
| API connectivity | Test Adobe and third-party integrations |
| Database performance | Validate query and transaction performance |
| Cache performance | Validate caching behaviour |
| Search performance | Validate indexing and search |
| CDN configuration | Validate content delivery |
| Security testing | Validate security controls |
| Load testing | Validate expected traffic |
| Failover testing | Validate resilience |
| Backup testing | Validate restoration |
| DR testing | Validate recovery procedures |
| Monitoring | Confirm visibility and alerting |

## 15.2 Performance scenarios

Test realistic business scenarios:

- Normal daily traffic.
- Peak promotional traffic.
- Product catalogue imports.
- Bulk customer updates.
- Order processing.
- Checkout and payment transactions.
- Search indexing.
- ERP synchronisation.
- Scheduled jobs.
- Large content delivery.
- Recovery after a service interruption.

---

# 16. Hosting Architecture Decision Record (ADR)

Every project must document the selected hosting model.

## 16.1 ADR template

### Decision title
Adobe DXP Hosting Architecture Selection

### Business context
Describe the business requirements and the reason a hosting decision is required.

### Adobe products
List the Adobe products and their required deployment models.

### Existing infrastructure
Document existing cloud subscriptions, data centres, networking, security and operational capabilities.

### Options evaluated
- Adobe-managed cloud.
- AWS.
- Microsoft Azure.
- Google Cloud.
- Bare metal / dedicated infrastructure.
- Hybrid or multi-cloud.

### Selected hosting model
Document the approved hosting architecture.

### Decision rationale
Explain why the selected option best satisfies the business and technical requirements.

### Rejected alternatives
Document the alternatives that were considered and why they were not selected.

### Infrastructure architecture
Document:
- Compute.
- Database.
- Cache.
- Search.
- Storage.
- Networking.
- CDN.
- Security.
- Monitoring.
- Backup.
- Disaster recovery.

### Responsibility matrix
Identify the parties responsible for infrastructure, application operations, security, patching, backups and incident response.

### Financial assessment
Include implementation costs, monthly costs and projected TCO.

### Risks and mitigations
Document the main risks and their mitigation strategies.

### Approvals
Record approval from:
- Solution Architect.
- Infrastructure / Cloud Architect.
- Security Team.
- Technical Lead.
- Client IT Management.
- Project Sponsor.

---

# 17. Design Phase Deliverables

The hosting architecture decision must produce the following deliverables:

| Deliverable | Description |
|---|---|
| Hosting assessment | Comparison of viable hosting models |
| Adobe deployment assessment | Confirmation of supported Adobe deployment models |
| Cloud architecture diagram | Logical and physical hosting architecture |
| Infrastructure specification | Compute, database, cache, storage and networking requirements |
| Network architecture | Network segmentation, connectivity and traffic flow |
| Security architecture | Identity, encryption, firewall and security controls |
| HA architecture | High-availability design |
| DR strategy | Recovery objectives and procedures |
| Cost assessment | Infrastructure and operational TCO |
| Responsibility matrix | Ownership of infrastructure and operations |
| Hosting ADR | Formal hosting decision and approvals |
| POC report | Results of technical validation |

---

# 18. Recommended Design Principles

1. **Start with Adobe product compatibility.** Do not select infrastructure before confirming the product's deployment options.

2. **Distinguish Adobe PaaS from customer-managed cloud.** Adobe Commerce on Cloud Infrastructure already uses AWS or Azure as its underlying infrastructure.

3. **Do not assume every Adobe product is self-hostable.** Adobe SaaS products remain Adobe-operated services.

4. **Choose infrastructure based on business requirements.** Evaluate cost, compliance, availability, performance and operational capability.

5. **Design for failure.** High availability, backups and disaster recovery must be deliberate architectural decisions.

6. **Avoid unnecessary multi-cloud complexity.** Use multiple providers only where there is a clear business or technical justification.

7. **Validate supportability.** Confirm exact Adobe product versions, operating systems, databases, caches, search services and other dependencies.

8. **Include operational ownership.** A hosting architecture is incomplete without clear responsibility for monitoring, security, patching, backups and incident response.

9. **Evaluate total cost of ownership.** Include engineering, support, data transfer, licensing and disaster recovery—not only server costs.

10. **Document the decision.** Hosting selection must be formally approved and recorded in the solution architecture.

---

# 19. Official Technical References

## Adobe

- [Adobe Commerce deployment options](https://experienceleague.adobe.com/en/docs/commerce/information-center/explore-platforms-and-services/platform-and-services)
- [Adobe Commerce on Cloud Infrastructure](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/overview)
- [Adobe Commerce cloud architecture](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/architecture/cloud-architecture)
- [Adobe Commerce technology stack](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/architecture/tech-stack)
- [Adobe Commerce on-premises installation](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/overview)
- [Adobe Commerce system requirements](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/system-requirements)
- [Adobe Commerce shared responsibility model](https://experienceleague.adobe.com/en/docs/commerce-operations/security-and-compliance/shared-responsibility)
- [Adobe Commerce SaaS shared responsibility](https://experienceleague.adobe.com/en/docs/commerce/cloud-service/security/shared-responsibility)
- [AEM as a Cloud Service architecture](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/overview/architecture)

## AWS

- [AWS Global Infrastructure](https://aws.amazon.com/about-aws/global-infrastructure/)
- [AWS Regions and Availability Zones](https://docs.aws.amazon.com/global-infrastructure/latest/regions/aws-regions.html)
- [AWS Well-Architected Framework](https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html)

## Microsoft Azure

- [Azure Global Infrastructure](https://azure.microsoft.com/en-us/explore/global-infrastructure/)
- [Azure Regions](https://learn.microsoft.com/en-us/azure/reliability/regions-list)
- [Azure Well-Architected Framework](https://learn.microsoft.com/en-us/azure/well-architected/)

## Google Cloud

- [Google Cloud Global Infrastructure](https://cloud.google.com/about/locations)
- [Google Cloud Regions and Zones](https://cloud.google.com/compute/docs/regions-zones)
- [Google Cloud Architecture Framework](https://cloud.google.com/architecture/framework)

---

# 20. Conclusion

Hosting is a foundational design decision that influences the entire Adobe DXP implementation, including application architecture, integrations, security, performance, scalability, operational responsibilities and long-term cost.

The decision should not be reduced to choosing between AWS, Azure, Google Cloud or a dedicated server.

The project must first establish which Adobe products are being implemented, which deployment models they support, and how the client intends to operate the resulting ecosystem.

**The objective is to select a hosting architecture that is supportable, secure, resilient, scalable and commercially sustainable.**

**Design principle: Adobe manages what is contracted as an Adobe-managed service; the client owns the responsibilities retained by its chosen deployment model.**
