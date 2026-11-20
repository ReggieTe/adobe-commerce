
# Adobe DXP – Third-Party Integration Directory

**Document:** Enterprise Third-Party Integration Reference  
**Platform:** Adobe Experience Cloud / Adobe Commerce  
**Purpose:** Identify major enterprise software platforms, their integration capabilities, and official developer resources for Adobe DXP implementation and migration projects.

---

## 1. Introduction

Enterprise Adobe DXP implementations commonly integrate with external business applications that already manage customers, products, pricing, inventory, orders, payments, fulfilment, marketing and analytics.

These systems may be integrated directly with Adobe Commerce, through an enterprise integration platform (iPaaS), through an API gateway, or using custom integration services.

This directory identifies commonly encountered enterprise platforms and provides links to their official API documentation, developer portals or Adobe Commerce integration modules.

### Integration implementation types

| Integration type | Description |
|---|---|
| Native Adobe integration | An integration provided and supported by Adobe for a specific Adobe product |
| Adobe Commerce extension | An installable extension that adds functionality or connects Commerce to an external platform |
| Vendor connector | An integration module supplied by the third-party software vendor |
| Middleware integration | An integration implemented through MuleSoft, Boomi, Workato or another integration platform |
| Custom API integration | A bespoke connection using REST, GraphQL, SOAP, webhooks or event messaging |
| File-based integration | Data exchange through CSV, XML, JSON, SFTP or scheduled batch processes |

**Important:** A vendor having an API does not mean it has a ready-made Adobe Commerce extension. Confirm extension availability, licensing, supported Adobe Commerce versions and compatibility with the target deployment model before selecting an implementation approach.

---

# 2. Core Enterprise Business Systems

## 2.1 CRM – Customer Relationship Management

CRM systems manage customer accounts, business relationships, sales activities, customer service and customer information.

| Platform | Integration resources |
|---|---|
| Salesforce Sales Cloud | [Salesforce REST API Developer Guide](https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/) |
| Microsoft Dynamics 365 | [Dynamics 365 Web API](https://learn.microsoft.com/en-us/power-apps/developer/data-platform/webapi/overview) |
| SAP Sales Cloud | [SAP Business Accelerator Hub](https://api.sap.com/) |
| HubSpot | [HubSpot Developer Documentation](https://developers.hubspot.com/docs/api/overview) |
| Oracle CX | [Oracle CX Developer Resources](https://docs.oracle.com/en/cloud/saas/) |
| Zoho CRM | [Zoho CRM API Documentation](https://www.zoho.com/crm/developer/docs/api/v8/) |

**Typical Adobe Commerce integration scenarios:**
- Customer account synchronisation.
- B2B company account synchronisation.
- Customer group and segmentation synchronisation.
- Lead and prospect capture.
- Customer service history.
- Customer address synchronisation.
- Order and transaction visibility.
- Customer consent and communication preferences.

**Important integration considerations:**
- Determine whether Adobe Commerce or CRM owns the customer record.
- Define customer matching rules and duplicate handling.
- Map customer IDs between systems.
- Define which system owns customer addresses and account status.
- Protect personally identifiable information during synchronisation.

## 2.2 ERP – Enterprise Resource Planning

ERP platforms manage core business operations, finance, procurement, stock, product information and order processing.

| Platform | Integration resources |
|---|---|
| SAP S/4HANA | [SAP API Business Hub](https://api.sap.com/) |
| SAP ERP / ECC | [SAP Integration Suite Documentation](https://help.sap.com/docs/integration-suite) |
| Oracle ERP Cloud | [Oracle Fusion Cloud REST API](https://docs.oracle.com/en/cloud/saas/financials/25d/farfa/index.html) |
| Microsoft Dynamics 365 Finance | [Dynamics 365 Finance and Operations APIs](https://learn.microsoft.com/en-us/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities) |
| Oracle NetSuite | [NetSuite SuiteTalk REST Web Services](https://docs.oracle.com/en/cloud/saas/netsuite/ns-online-help/chapter_1540391670.html) |
| Sage X3 | [Sage Developer Portal](https://developer.sage.com/) |

**Typical Adobe Commerce integration scenarios:**
- Product and SKU synchronisation.
- Stock and inventory availability.
- Customer account synchronisation.
- Sales order submission.
- Order status updates.
- Invoice synchronisation.
- Credit notes and refunds.
- Tax and financial data exchange.
- Customer-specific commercial terms.

**Typical data ownership:**

| Data | Common system of record |
|---|---|
| Product master | ERP or PIM |
| Inventory | ERP or WMS |
| Customer account | CRM or ERP |
| Sales order | Commerce or ERP, depending on order lifecycle |
| Invoice | ERP |
| Financial ledger | ERP |
| Payment transaction | Payment provider / payment platform |

## 2.3 Pricing Management

Pricing systems manage complex pricing rules, contracts, customer-specific prices, discounts and commercial agreements.

| Platform | Integration resources |
|---|---|
| SAP Pricing / S/4HANA | [SAP API Business Hub](https://api.sap.com/) |
| PROS | [PROS Developer Resources](https://developer.pros.com/) |
| Pricefx | [Pricefx Documentation](https://knowledge.pricefx.com/) |
| Vendavo | [Vendavo](https://www.vendavo.com/) |
| Oracle Pricing | [Oracle Cloud Documentation](https://docs.oracle.com/en/cloud/saas/) |

**Typical Adobe Commerce integration scenarios:**
- B2B customer-specific pricing.
- Contract pricing.
- Price lists.
- Discount structures.
- Volume-based pricing.
- Promotional pricing.
- Currency-based pricing.
- Quote pricing.
- Price updates and synchronisation.

**Architecture consideration:** Pricing ownership must be agreed before implementation. Adobe Commerce can calculate and display prices, but the enterprise pricing engine may remain the authoritative source.

## 2.4 PIM – Product Information Management

PIM platforms centralise product information and distribute enriched product data to commerce, marketplaces and other sales channels.

| Platform | Integration resources |
|---|---|
| Akeneo | [Akeneo API Documentation](https://api.akeneo.com/) |
| Pimcore | [Pimcore Developer Documentation](https://docs.pimcore.com/platform/) |
| Salsify | [Salsify Developer Documentation](https://developers.salsify.com/) |
| inriver | [inriver Developer Portal](https://developer.inriver.com/) |
| Stibo Systems | [Stibo Systems Developer Portal](https://doc.stibosystems.com/) |

**Typical Adobe Commerce integration scenarios:**
- Product creation and updates.
- Product attributes.
- Product categories.
- Product descriptions.
- Product variants.
- Product relationships.
- Product images and media references.
- Localised product content.
- Product enrichment and validation.

**Architecture consideration:** Define whether PIM or Adobe Commerce owns product attributes, category assignments, merchandising information and channel-specific descriptions.

## 2.5 MDM – Master Data Management

MDM platforms maintain authoritative enterprise records and enforce data consistency across applications.

| Platform | Integration resources |
|---|---|
| Informatica MDM | [Informatica Developer Documentation](https://docs.informatica.com/) |
| Reltio | [Reltio API Documentation](https://docs.reltio.com/en/developer-resources/reltio-apis) |
| SAP Master Data Governance | [SAP API Business Hub](https://api.sap.com/) |
| Semarchy xDM | [Semarchy Documentation](https://www.semarchy.com/doc/) |

**Typical Adobe Commerce integration scenarios:**
- Golden customer records.
- Product master data.
- Business account records.
- Duplicate detection.
- Master data validation.
- Cross-system identity matching.

## 2.6 OMS – Order Management System

OMS platforms coordinate order processing across digital channels, warehouses, stores and fulfilment partners.

| Platform | Integration resources |
|---|---|
| IBM Sterling Order Management | [IBM Sterling Documentation](https://www.ibm.com/docs/en/order-management) |
| Manhattan Active Omni | [Manhattan Associates Documentation](https://docs.manh.com/) |
| Fluent Commerce | [Fluent Commerce Developer Documentation](https://docs.fluentcommerce.com/) |
| Kibo Commerce | [Kibo Developer Documentation](https://docs.kibocommerce.com/) |
| Oracle Order Management | [Oracle Order Management Documentation](https://docs.oracle.com/en/cloud/saas/supply-chain-and-manufacturing/) |

**Typical Adobe Commerce integration scenarios:**
- Order submission.
- Order orchestration.
- Order allocation.
- Split shipments.
- Click and collect.
- Store fulfilment.
- Order status updates.
- Returns and exchanges.
- Fulfilment tracking.

---

# 3. Customer Experience and Commerce Systems

## 3.1 CMS – Content Management Systems

CMS platforms manage digital content, website experiences, landing pages and content delivery.

| Platform | Integration resources |
|---|---|
| Adobe Experience Manager | [AEM Developer Documentation](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/introduction/developing) |
| Contentful | [Contentful Content Management API](https://www.contentful.com/developers/docs/references/content-management-api/) |
| Sitecore | [Sitecore Developer Portal](https://developers.sitecore.com/) |
| Sanity | [Sanity API Documentation](https://www.sanity.io/docs/http-api) |
| Drupal | [Drupal REST API Documentation](https://www.drupal.org/docs/drupal-apis) |

**Typical Adobe Commerce integration scenarios:**
- Headless storefront content.
- Product landing pages.
- Editorial content.
- Category content.
- Content-driven commerce experiences.
- Shared content between websites and mobile applications.

**Important:** AEM and Adobe Commerce are separate products. Their integration architecture depends on the selected AEM deployment model and Commerce integration approach.

## 3.2 DAM – Digital Asset Management

DAM systems manage digital assets such as product images, videos, marketing material and documents.

| Platform | Integration resources |
|---|---|
| Bynder | [Bynder Developer Documentation](https://developer-docs.bynder.com/) |
| Aprimo | [Aprimo Developer Resources](https://developers.aprimo.com/) |
| Cloudinary | [Cloudinary API Documentation](https://cloudinary.com/documentation) |
| Acquia DAM | [Acquia DAM Developer Resources](https://docs.acquia.com/) |

**Typical Adobe Commerce integration scenarios:**
- Product image synchronisation.
- Image transformation and optimisation.
- Video delivery.
- Asset metadata.
- Digital asset approval workflows.
- Brand asset governance.

## 3.3 Search and Discovery

Search platforms improve product discovery, filtering, autocomplete and relevance.

| Platform | Integration resources |
|---|---|
| Algolia | [Algolia API Documentation](https://www.algolia.com/doc/) |
| Coveo | [Coveo Developer Documentation](https://docs.coveo.com/) |
| Elasticsearch | [Elasticsearch API Documentation](https://www.elastic.co/docs/api/doc/elasticsearch/) |
| OpenSearch | [OpenSearch Documentation](https://docs.opensearch.org/latest/) |
| Constructor.io | [Constructor API Documentation](https://docs.constructor.com/) |

**Adobe Commerce-specific resources:**
- [Adobe Commerce Live Search](https://experienceleague.adobe.com/en/docs/commerce/live-search/overview)
- [Adobe Commerce Product Recommendations](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/overview)
- [Adobe Commerce Marketplace](https://commercemarketplace.adobe.com/)

**Typical integration scenarios:**
- Product indexing.
- Search queries.
- Faceted navigation.
- Autocomplete.
- Search merchandising.
- Product recommendations.
- Search analytics.

## 3.4 Personalisation and Experimentation

Personalisation platforms tailor digital experiences to individual customers or audience segments.

| Platform | Integration resources |
|---|---|
| Adobe Target | [Adobe Target Developer Documentation](https://experienceleague.adobe.com/en/docs/target-dev/developer/overview) |
| Dynamic Yield | [Dynamic Yield Developer Documentation](https://docs.dynamicyield.com/) |
| Optimizely | [Optimizely Developer Documentation](https://docs.developers.optimizely.com/) |
| Bloomreach | [Bloomreach Developer Documentation](https://documentation.bloomreach.com/) |

**Typical integration scenarios:**
- Personalised product recommendations.
- A/B testing.
- Content targeting.
- Customer segmentation.
- Personalised promotions.
- Experience experimentation.

## 3.5 Marketing Automation

Marketing automation platforms manage campaigns, email, SMS, customer engagement and marketing workflows.

| Platform | Integration resources |
|---|---|
| Salesforce Marketing Cloud | [Salesforce Marketing Cloud Developer Documentation](https://developer.salesforce.com/docs/marketing/marketing-cloud/overview) |
| Braze | [Braze Developer Documentation](https://www.braze.com/docs/developer_guide/home/) |
| Klaviyo | [Klaviyo API Documentation](https://developers.klaviyo.com/en/reference/api_overview) |
| HubSpot Marketing Hub | [HubSpot API Documentation](https://developers.hubspot.com/docs/api/overview) |
| Oracle Eloqua | [Oracle Eloqua API Documentation](https://docs.oracle.com/en/cloud/saas/marketing/eloqua-rest-api/) |

**Typical integration scenarios:**
- Customer registration events.
- Abandoned cart campaigns.
- Order confirmation.
- Customer segmentation.
- Marketing consent.
- Product recommendations.
- Customer lifecycle campaigns.

## 3.6 CDP – Customer Data Platform

CDP platforms unify customer information from different channels and applications.

| Platform | Integration resources |
|---|---|
| Adobe Real-Time CDP | [Adobe Experience Platform API Documentation](https://developer.adobe.com/experience-platform-apis/) |
| Twilio Segment | [Segment Developer Documentation](https://segment.com/docs/) |
| Salesforce Data Cloud | [Salesforce Data Cloud Developer Documentation](https://developer.salesforce.com/docs/data/data-cloud/overview) |
| Tealium | [Tealium Developer Documentation](https://docs.tealium.com/) |
| mParticle | [mParticle Developer Documentation](https://docs.mparticle.com/) |

**Typical integration scenarios:**
- Customer identity resolution.
- Unified customer profiles.
- Audience creation.
- Behavioural event collection.
- Customer segmentation.
- Personalisation activation.
- Consent and data governance.

## 3.7 Loyalty and Rewards

Loyalty systems manage customer rewards, membership programmes, points and retention campaigns.

| Platform | Integration resources |
|---|---|
| LoyaltyLion | [LoyaltyLion Developer Documentation](https://developers.loyaltylion.com/) |
| Antavo | [Antavo Developer Documentation](https://docs.antavo.com/) |
| Yotpo | [Yotpo Developer Documentation](https://developers.yotpo.com/) |
| Salesforce Loyalty Management | [Salesforce Developer Documentation](https://developer.salesforce.com/docs/) |

**Typical integration scenarios:**
- Loyalty account creation.
- Points earning.
- Points redemption.
- Membership tiers.
- Reward catalogue.
- Customer rewards balance.
- Loyalty transaction history.

---

# 4. Financial and Transaction Systems

## 4.1 Payment Gateways

Payment providers process card payments, alternative payment methods, refunds and transaction settlements.

| Platform | API / Adobe Commerce integration resources |
|---|---|
| Adyen | [Adobe Commerce Plugin Documentation](https://docs.adyen.com/plugins/adobe-commerce) |
| Stripe | [Stripe API Documentation](https://docs.stripe.com/api) |
| PayPal | [PayPal Developer Documentation](https://developer.paypal.com/docs/api/overview/) |
| Worldpay | [Worldpay Developer Documentation](https://developer.worldpay.com/) |
| Checkout.com | [Checkout.com API Documentation](https://www.checkout.com/docs) |
| Braintree | [Braintree Developer Documentation](https://developer.paypal.com/braintree/docs) |

## 4.2 African Payment Providers

| Platform | API / integration resources |
|---|---|
| PayFast | [PayFast Developer Documentation](https://developers.payfast.co.za/) |
| Peach Payments | [Peach Payments Developer Documentation](https://developer.peachpayments.com/) |
| Ozow | [Ozow Developer Documentation](https://docs.ozow.com/) |
| DPO Pay | [DPO Group Developer Resources](https://dpogroup.com/) |
| Yoco | [Yoco Developer Documentation](https://developer.yoco.com/) |

**Typical Adobe Commerce integration scenarios:**
- Payment authorisation.
- Payment capture.
- Payment status updates.
- Refund processing.
- Tokenised payment methods.
- Recurring payment mandates.
- Payment reconciliation.
- Webhook processing.

**Security considerations:**
- Avoid storing raw card details in Adobe Commerce.
- Use provider-supported tokenisation.
- Verify webhook signatures.
- Implement idempotency for transaction requests.
- Protect payment credentials and API secrets.
- Understand the applicable PCI DSS responsibilities.

## 4.3 Tax Management

| Platform | Integration resources |
|---|---|
| Avalara | [Avalara Developer Documentation](https://developer.avalara.com/) |
| Vertex | [Vertex Developer Documentation](https://developer.vertexinc.com/) |
| Sovos | [Sovos Developer Resources](https://developer.sovos.com/) |
| Thomson Reuters ONESOURCE | [ONESOURCE Documentation](https://tax.thomsonreuters.com/) |

**Typical integration scenarios:**
- VAT calculation.
- Sales tax calculation.
- Tax jurisdiction determination.
- Tax exemption handling.
- Tax reporting.
- Tax transaction validation.

## 4.4 Fraud Prevention

| Platform | Integration resources |
|---|---|
| Signifyd | [Signifyd Developer Documentation](https://developer.signifyd.com/) |
| Forter | [Forter Developer Documentation](https://forter.docs.buildwithfern.com/) |
| Riskified | [Riskified Developer Documentation](https://apiref.riskified.com/) |
| Sift | [Sift Developer Documentation](https://developers.sift.com/) |

**Typical integration scenarios:**
- Transaction risk scoring.
- Fraud screening.
- Order review.
- Chargeback prevention.
- Account takeover detection.
- Automated order approval or rejection.

## 4.5 Subscription Billing

| Platform | Integration resources |
|---|---|
| Zuora | [Zuora API Documentation](https://developer.zuora.com/) |
| Chargebee | [Chargebee API Documentation](https://apidocs.chargebee.com/) |
| Recurly | [Recurly API Documentation](https://recurly.com/developers/api/) |
| Stripe Billing | [Stripe Billing Documentation](https://docs.stripe.com/billing) |

**Typical integration scenarios:**
- Subscription creation.
- Recurring billing.
- Payment mandates.
- Renewals.
- Subscription upgrades and downgrades.
- Cancellation.
- Failed payment recovery.
- Invoice generation.

## 4.6 Financial Reconciliation

| Platform | Integration resources |
|---|---|
| BlackLine | [BlackLine Developer Resources](https://developer.blackline.com/) |
| Trintech | [Trintech](https://www.trintech.com/) |
| HighRadius | [HighRadius](https://www.highradius.com/) |

**Typical integration scenarios:**
- Payment settlement matching.
- Order-to-invoice reconciliation.
- Refund reconciliation.
- General ledger posting.
- Financial exception management.

---

# 5. Logistics, Inventory and Fulfilment

## 5.1 WMS – Warehouse Management Systems

| Platform | Integration resources |
|---|---|
| Manhattan WMS | [Manhattan Associates Documentation](https://docs.manh.com/) |
| SAP Extended Warehouse Management | [SAP API Business Hub](https://api.sap.com/) |
| Blue Yonder WMS | [Blue Yonder Developer Resources](https://developer.blueyonder.com/) |
| Oracle WMS Cloud | [Oracle Supply Chain Documentation](https://docs.oracle.com/en/cloud/saas/supply-chain-and-manufacturing/) |
| Infor WMS | [Infor Developer Portal](https://developer.infor.com/) |

**Typical integration scenarios:**
- Inventory availability.
- Warehouse stock levels.
- Picking and packing.
- Shipment creation.
- Warehouse allocation.
- Order fulfilment status.

## 5.2 Inventory Management

| Platform | Integration resources |
|---|---|
| Cin7 | [Cin7 API Documentation](https://dearinventory.docs.apiary.io/) |
| Unleashed | [Unleashed API Documentation](https://apidocs.unleashedsoftware.com/) |
| NetSuite Inventory | [NetSuite SuiteTalk Documentation](https://docs.oracle.com/en/cloud/saas/netsuite/ns-online-help/chapter_1540391670.html) |
| Microsoft Dynamics 365 Supply Chain | [Dynamics 365 Documentation](https://learn.microsoft.com/en-us/dynamics365/supply-chain/) |

## 5.3 Shipping and Delivery

| Platform | Integration resources |
|---|---|
| DHL | [DHL Developer Portal](https://developer.dhl.com/) |
| FedEx | [FedEx Developer Portal](https://developer.fedex.com/) |
| UPS | [UPS Developer Portal](https://developer.ups.com/) |
| Aramex | [Aramex Developer Portal](https://www.aramex.com/) |
| ShipStation | [ShipStation API Documentation](https://docs.shipstation.com/) |
| EasyPost | [EasyPost API Documentation](https://docs.easypost.com/) |

## 5.4 Last-Mile Delivery

| Platform | Integration resources |
|---|---|
| Onfleet | [Onfleet API Documentation](https://docs.onfleet.com/) |
| Bringg | [Bringg Developer Resources](https://developers.bringg.com/) |
| FarEye | [FarEye](https://fareye.com/) |

**Typical integration scenarios:**
- Delivery booking.
- Shipping rate calculation.
- Shipment tracking.
- Delivery status updates.
- Proof of delivery.
- Delivery notifications.
- Returns collection.

---

# 6. Middleware, API Management and Integration Platforms

These technologies are particularly important in enterprise Adobe DXP implementations because they connect Adobe products to existing enterprise systems.

## 6.1 iPaaS – Integration Platform as a Service

| Platform | Integration resources |
|---|---|
| MuleSoft Anypoint Platform | [MuleSoft Developer Documentation](https://docs.mulesoft.com/) |
| Boomi | [Boomi Developer Documentation](https://developer.boomi.com/) |
| Workato | [Workato Developer Documentation](https://docs.workato.com/) |
| Informatica IDMC | [Informatica Documentation](https://docs.informatica.com/) |
| SnapLogic | [SnapLogic Developer Documentation](https://docs.snaplogic.com/) |
| Jitterbit | [Jitterbit Developer Documentation](https://docs.jitterbit.com/) |

**Typical Adobe Commerce integration scenarios:**
- ERP integration.
- CRM integration.
- PIM integration.
- Customer synchronisation.
- Product synchronisation.
- Order orchestration.
- Data transformation.
- API orchestration.
- Scheduled data exchange.

## 6.2 ESB – Enterprise Service Bus

| Platform | Integration resources |
|---|---|
| MuleSoft | [MuleSoft Documentation](https://docs.mulesoft.com/) |
| WSO2 | [WSO2 Documentation](https://apim.docs.wso2.com/) |
| IBM App Connect | [IBM App Connect Documentation](https://www.ibm.com/docs/en/app-connect) |
| Oracle Service Bus | [Oracle Service Bus Documentation](https://docs.oracle.com/en/middleware/soa-suite/service-bus/) |

## 6.3 API Management

| Platform | Integration resources |
|---|---|
| Google Apigee | [Apigee API Documentation](https://cloud.google.com/apigee/docs) |
| Azure API Management | [Azure API Management Documentation](https://learn.microsoft.com/en-us/azure/api-management/) |
| Kong Gateway | [Kong Developer Documentation](https://developer.konghq.com/) |
| AWS API Gateway | [AWS API Gateway Documentation](https://docs.aws.amazon.com/apigateway/) |
| Gravitee | [Gravitee Documentation](https://documentation.gravitee.io/) |

**Typical integration scenarios:**
- API authentication.
- OAuth 2.0.
- API key management.
- Rate limiting.
- API versioning.
- Request transformation.
- API analytics.
- Developer portal management.

## 6.4 Event Streaming and Messaging

| Platform | Integration resources |
|---|---|
| Apache Kafka | [Apache Kafka Documentation](https://kafka.apache.org/documentation/) |
| RabbitMQ | [RabbitMQ Documentation](https://www.rabbitmq.com/docs) |
| Azure Service Bus | [Azure Service Bus Documentation](https://learn.microsoft.com/en-us/azure/service-bus-messaging/) |
| Amazon SQS / SNS | [AWS Messaging Documentation](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/welcome.html) |
| Google Pub/Sub | [Google Pub/Sub Documentation](https://cloud.google.com/pubsub/docs) |

**Typical integration scenarios:**
- Asynchronous order processing.
- Inventory events.
- Product update events.
- Customer update events.
- Payment notifications.
- Fulfilment events.
- Decoupled enterprise applications.

## 6.5 Workflow and Process Automation

| Platform | Integration resources |
|---|---|
| Camunda | [Camunda Developer Documentation](https://docs.camunda.io/) |
| Temporal | [Temporal Developer Documentation](https://docs.temporal.io/) |
| n8n | [n8n API Documentation](https://docs.n8n.io/api/) |
| Microsoft Power Automate | [Power Platform Developer Documentation](https://learn.microsoft.com/en-us/power-platform/) |

---

# 7. Cloud, Infrastructure and Operations

## 7.1 Cloud Infrastructure

| Platform | Developer resources |
|---|---|
| Amazon Web Services | [AWS Developer Documentation](https://docs.aws.amazon.com/) |
| Microsoft Azure | [Azure Documentation](https://learn.microsoft.com/en-us/azure/) |
| Google Cloud Platform | [Google Cloud Documentation](https://cloud.google.com/docs) |
| OVHcloud | [OVHcloud API Documentation](https://help.ovhcloud.com/csm/en-api-documentation?id=kb_browse_cat&kb_id=) |

## 7.2 CDN, Edge and Security

| Platform | Integration resources |
|---|---|
| Cloudflare | [Cloudflare API Documentation](https://developers.cloudflare.com/api/) |
| Akamai | [Akamai Developer Documentation](https://techdocs.akamai.com/) |
| Fastly | [Fastly API Documentation](https://www.fastly.com/documentation/reference/api/) |
| AWS CloudFront | [CloudFront API Documentation](https://docs.aws.amazon.com/cloudfront/) |

## 7.3 Identity and Access Management

| Platform | Integration resources |
|---|---|
| Microsoft Entra ID | [Microsoft Identity Platform Documentation](https://learn.microsoft.com/en-us/entra/identity-platform/) |
| Okta | [Okta Developer Documentation](https://developer.okta.com/docs/) |
| Auth0 | [Auth0 Developer Documentation](https://auth0.com/docs) |
| Ping Identity | [Ping Identity Documentation](https://docs.pingidentity.com/) |

**Typical integration scenarios:**
- Single sign-on.
- Customer authentication.
- Enterprise employee authentication.
- OAuth 2.0.
- OpenID Connect.
- SAML federation.
- Multi-factor authentication.
- Role-based access control.

## 7.4 Observability and Monitoring

| Platform | Integration resources |
|---|---|
| Datadog | [Datadog API Documentation](https://docs.datadoghq.com/api/latest/) |
| Dynatrace | [Dynatrace API Documentation](https://docs.dynatrace.com/docs/dynatrace-api) |
| New Relic | [New Relic API Documentation](https://docs.newrelic.com/docs/apis/) |
| Splunk | [Splunk Developer Documentation](https://dev.splunk.com/) |
| Grafana | [Grafana API Documentation](https://grafana.com/docs/grafana/latest/developer-resources/api-reference/) |

## 7.5 Security and Vulnerability Management

| Platform | Integration resources |
|---|---|
| CrowdStrike | [CrowdStrike Developer Portal](https://developer.crowdstrike.com/) |
| Qualys | [Qualys API Documentation](https://docs.qualys.com/) |
| Snyk | [Snyk API Documentation](https://docs.snyk.io/snyk-api-info) |
| Wiz | [Wiz Developer Documentation](https://docs.wiz.io/) |

---

# 8. Analytics and Business Intelligence

## 8.1 Digital Analytics

| Platform | Integration resources |
|---|---|
| Adobe Analytics | [Adobe Analytics Developer Documentation](https://developer.adobe.com/analytics-apis/docs/2.0/) |
| Google Analytics 4 | [Google Analytics Data API](https://developers.google.com/analytics/devguides/reporting/data/v1) |
| Amplitude | [Amplitude Developer Documentation](https://amplitude.com/docs/apis) |
| Mixpanel | [Mixpanel Developer Documentation](https://developer.mixpanel.com/) |

## 8.2 Business Intelligence

| Platform | Integration resources |
|---|---|
| Microsoft Power BI | [Power BI REST API](https://learn.microsoft.com/en-us/rest/api/power-bi/) |
| Tableau | [Tableau REST API](https://help.tableau.com/current/api/rest_api/en-us/REST/rest_api.htm) |
| Qlik Sense | [Qlik Developer Portal](https://qlik.dev/) |
| Looker | [Looker API Documentation](https://cloud.google.com/looker/docs/api) |

## 8.3 Data Warehousing and Lakehouse

| Platform | Integration resources |
|---|---|
| Snowflake | [Snowflake Developer Documentation](https://docs.snowflake.com/en/developer-guide/) |
| Databricks | [Databricks API Documentation](https://docs.databricks.com/api/) |
| Google BigQuery | [BigQuery API Documentation](https://cloud.google.com/bigquery/docs/reference/rest) |
| Amazon Redshift | [Amazon Redshift API Documentation](https://docs.aws.amazon.com/redshift/) |

---

# 9. Adobe Native Integration Resources

Adobe provides its own APIs, integrations, extensions and developer services.

These are particularly important when designing an Adobe DXP architecture.

| Adobe product / capability | Developer resources |
|---|---|
| Adobe Commerce | [Adobe Commerce Developer Documentation](https://developer.adobe.com/commerce/docs/) |
| Adobe Commerce REST APIs | [Adobe Commerce REST API Reference](https://developer.adobe.com/commerce/webapi/rest/) |
| Adobe Commerce GraphQL | [Adobe Commerce GraphQL Developer Guide](https://developer.adobe.com/commerce/webapi/graphql/) |
| Adobe Commerce Marketplace | [Adobe Commerce Marketplace](https://commercemarketplace.adobe.com/) |
| Adobe App Builder | [Adobe App Builder Documentation](https://developer.adobe.com/app-builder/) |
| Adobe I/O Events | [Adobe I/O Events Documentation](https://developer.adobe.com/events/) |
| Adobe Experience Manager | [AEM Developer Documentation](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/introduction/developing) |
| Adobe Experience Platform | [Experience Platform API Documentation](https://developer.adobe.com/experience-platform-apis/) |
| Adobe Real-Time CDP | [Real-Time CDP Documentation](https://experienceleague.adobe.com/en/docs/experience-platform/rtcdp/overview) |
| Adobe Journey Optimizer | [Journey Optimizer Documentation](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/ajo-home) |
| Adobe Target | [Adobe Target Developer Documentation](https://experienceleague.adobe.com/en/docs/target-dev/developer/overview) |
| Adobe Analytics | [Adobe Analytics API Documentation](https://developer.adobe.com/analytics-apis/docs/2.0/) |
| Adobe Customer Journey Analytics | [Customer Journey Analytics Documentation](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview) |

### Adobe Commerce extension and application considerations

Adobe Commerce supports both traditional in-process PHP extensions and out-of-process applications.

- In-process extensions run inside the Commerce application.
- Out-of-process applications operate independently and communicate through APIs and events.
- Adobe App Builder can be used to develop extensions and integrations outside the Commerce application.
- Adobe Commerce Marketplace provides a directory of extensions and integration solutions.

Reference:
- [Adobe Commerce Extensions](https://experienceleague.adobe.com/en/docs/commerce-admin/start/resources/extensions)
- [Adobe Commerce Marketplace](https://experienceleague.adobe.com/en/docs/commerce-admin/start/resources/commerce-marketplace)
- [Adobe Commerce Third-Party Integrations](https://business.adobe.com/products/magento/adobe-integrations.html)

---

# 10. Adobe Commerce Extension Discovery

When evaluating an integration, first determine whether an installable Adobe Commerce extension already exists.

Recommended discovery sources:

| Source | Purpose |
|---|---|
| [Adobe Commerce Marketplace](https://commercemarketplace.adobe.com/) | Search for verified Adobe Commerce extensions |
| [Adobe Commerce Developer Documentation](https://developer.adobe.com/commerce/docs/) | Determine how to implement custom integrations |
| [Adobe Commerce GitHub](https://github.com/magento) | Review official Adobe Commerce repositories and developer resources |
| [Adobe Commerce Extension Documentation](https://experienceleague.adobe.com/en/docs/commerce-admin/start/resources/extensions) | Understand extension installation and extensibility |

### Extension assessment checklist

Before installing an extension, verify:

1. Does the extension support the target Adobe Commerce version?
2. Does it support the selected deployment model?
3. Is it compatible with the PHP version?
4. Is it compatible with the current checkout implementation?
5. Does it support the required API operations?
6. Does it support asynchronous processing?
7. Does it provide webhook support where required?
8. Does it support authentication and secure credential storage?
9. Is it actively maintained?
10. Does the vendor provide technical support?
11. Is the extension licensed per installation, environment or transaction?
12. Does it introduce dependencies that affect future upgrades?

**Do not assume that an extension listed for Magento Open Source automatically supports every Adobe Commerce edition or deployment model.**

---

# 11. Enterprise Integration Architecture

A typical Adobe Commerce enterprise integration architecture may look like this:

```text
                    DIGITAL CHANNELS
             Website | Mobile | B2B | Marketplace
                           |
                           v
                  ADOBE EXPERIENCE LAYER
             Adobe Commerce | AEM | Adobe Target
                           |
                           v
                  API / INTEGRATION LAYER
                MuleSoft | Boomi | Workato
                           |
          +----------------+----------------+
          |                |                |
          v                v                v
         CRM              ERP              PIM
     Salesforce       SAP S/4HANA         Akeneo
          |                |                |
          +----------------+----------------+
                           |
           +---------------+----------------+
           |               |                |
           v               v                v
        PRICING           OMS            INVENTORY
         SAP          Manhattan/Fluent       WMS
           |               |                |
           +---------------+----------------+
                           |
                           v
                 PAYMENT AND FULFILMENT
              Adyen | Stripe | DHL | Aramex
                           |
                           v
                 CUSTOMER EXPERIENCE DATA
              CDP | Analytics | Marketing
                           |
                           v
                  REPORTING / DATA LAKE
               Snowflake | Power BI | Tableau
```

The integration layer may not be necessary for every connection. Simple integrations can use direct APIs, while complex enterprise integrations may require middleware, event streaming and orchestration.

---

# 12. Integration Design and Data Ownership

Every integration should be documented before development begins.

## 12.1 Integration register

| Field | Description |
|---|---|
| Integration ID | Unique integration reference |
| Business capability | CRM, ERP, PIM, OMS, payment, etc. |
| Source system | System sending the data |
| Target system | System receiving the data |
| System of record | Authoritative owner of the information |
| Data objects | Customers, products, orders, inventory, etc. |
| Direction | Inbound, outbound or bidirectional |
| Integration method | REST, GraphQL, SOAP, webhook, event or file |
| Middleware | MuleSoft, Boomi, direct integration, etc. |
| Frequency | Real-time, near-real-time, scheduled or batch |
| Authentication | OAuth 2.0, API key, certificates, etc. |
| Error handling | Retry, dead-letter queue and escalation |
| Reconciliation | Method for identifying missing or inconsistent records |
| Monitoring | Logs, metrics, traces and alerts |
| Owner | Business and technical owner |
| Support model | Team responsible for ongoing operation |

## 12.2 Example integration register

| Integration | Source | Target | Direction | Method |
|---|---|---|---|---|
| Product catalogue | Akeneo | Adobe Commerce | Inbound | REST API / middleware |
| Inventory | SAP | Adobe Commerce | Inbound | API / event |
| Customer accounts | Salesforce | Adobe Commerce | Bidirectional | REST API / middleware |
| Orders | Adobe Commerce | SAP | Outbound | API / event |
| Order status | SAP / OMS | Adobe Commerce | Inbound | API / webhook |
| Payments | Adobe Commerce | Adyen | Bidirectional | Payment API / webhook |
| Shipping | Adobe Commerce | DHL | Bidirectional | Shipping API |
| Customer events | Adobe Commerce | Adobe Experience Platform | Outbound | Event / data ingestion |
| Customer journeys | Adobe Experience Platform | Adobe Journey Optimizer | Internal Adobe ecosystem | Native integration / APIs |
| Analytics | Adobe Commerce | Adobe Analytics | Outbound | Data collection |

---

# 13. Integration Failure and Operational Management

A successful integration must account for failures, not just successful API requests.

Every integration should define:

### Reliability
- Retry policies.
- Timeout handling.
- Circuit breakers.
- Idempotency.
- Duplicate message prevention.
- Dead-letter queues.

### Data quality
- Data validation.
- Mandatory field checks.
- Data transformation rules.
- Referential integrity.
- Duplicate detection.
- Reconciliation.

### Security
- Secure credential storage.
- OAuth 2.0 where supported.
- API access controls.
- Encryption in transit.
- Webhook signature verification.
- Audit logging.
- PII protection.

### Monitoring
- API availability.
- Request latency.
- Failed transactions.
- Queue depth.
- Synchronisation delays.
- Data discrepancies.
- Integration health dashboards.

### Operational ownership
- Business system owner.
- Integration technical owner.
- Support escalation.
- Vendor support arrangements.
- Incident response procedure.
- Recovery and replay procedure.

---

# 14. Final Architecture Principles

1. **Identify the system of record:** Every important business entity must have a clearly defined authoritative owner.
2. **Avoid unnecessary point-to-point integrations:** Use middleware where it reduces coupling and centralises integration governance.
3. **Use APIs and events appropriately:** Use synchronous APIs for immediate responses and asynchronous messaging for decoupled processes.
4. **Protect data consistency:** Define synchronisation, validation and reconciliation procedures.
5. **Design for failure:** Every integration needs retry, recovery, monitoring and escalation.
6. **Respect product boundaries:** Adobe Commerce, AEM, Real-Time CDP and other Adobe Experience Cloud products have different capabilities and integration models.
7. **Prefer upgrade-safe extensibility:** Avoid unnecessary modifications to Adobe Commerce core code.
8. **Document operational ownership:** The client must retain the documentation, credentials, subscriptions, vendor relationships and support procedures required to operate the integrations.

**The objective is not simply to connect Adobe Commerce to third-party systems. It is to create a governed enterprise integration architecture that remains secure, scalable, observable, maintainable and supportable after the implementation consultant exits.**
