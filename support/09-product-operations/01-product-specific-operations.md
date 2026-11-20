# 11. Product-Specific Operations Guides

> Part of the *Enterprise Adobe DXP Support and Operations Handbook* v1.0 (Review Draft). Section numbers (§) refer to the handbook's original numbering; see the README at the root of this folder for the section map.

## 11.1 AEM
- **Daily:** author and publish availability, replication or publishing queue health, workflow failures, pipeline status, error logs, CDN and cache behaviour on key pages.
- **Weekly:** content and asset publishing issues, search and indexing checks, user and permission requests, certificate expiry.
- **Monthly:** access review, repository and storage trends, dispatcher and cache rule review, update planning.
- **Common incidents:** pages not updating (cache or replication), authoring slow or failing, workflow stuck, pipeline failure, misconfigured permission.

## 11.2 Adobe Commerce
- **Daily:** storefront and checkout smoke test, payment success rate, order flow into ERP, indexers and cron status, queue consumers, error and exception logs, CDN and cache health.
- **Weekly:** catalogue and price import results, search relevance spot checks, scheduled-job audit, customer-service issue patterns.
- **Monthly:** access review, extension and dependency update review, performance trends, peak-season readiness.
- **Common incidents:** stale or missing products (indexing), slow checkout, failed payment webhooks, cron stuck, cache invalidation problems, deployment regression.

## 11.3 AEP
- **Daily:** ingestion batch and streaming status, dataset health, failed flows, destination activation status.
- **Weekly:** schema and identity quality checks, segment evaluation health, consent and usage-label checks.
- **Monthly:** privacy request completion, data volume and licence usage, access review.
- **Common incidents:** ingestion failures, identity mismatches, audience not updating, destination errors.

## 11.4 Analytics, Target and Journey Optimizer
- **Daily:** tag and SDK delivery, data collection checks on key pages, active activity and journey status.
- **Weekly:** data quality checks, audience sizes, message delivery results.
- **Monthly:** tagging plan review, access review, retiring obsolete activities.
- **Common incidents:** tags not firing after release, consent misapplied, wrong audience, journey not triggering.

## 11.5 Integrations and Middleware
- **Daily:** queue depth, error rate, retries and dead-letter items, third-party status.
- **Monthly:** credential and certificate expiry, contract and rate-limit review.
- **Common incidents:** expired credentials, third-party outage, schema change by a partner, backlog build-up.
