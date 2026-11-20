# Technical Checklists

> Part of the *Enterprise Adobe DXP Migration Handbook* v1.1 (Review Draft). Section numbers (§) refer to the handbook's original numbering; see the root [README](../README.md) for the section map.

## B.1 Discovery completeness
- [ ] Every platform, environment and domain inventoried
- [ ] Every integration has an owner and failure impact
- [ ] Data volumes and sensitivity recorded
- [ ] Undocumented dependencies hunted (cron jobs, direct DB links, manual processes)
- [ ] Compliance and residency obligations listed

## B.2 Design readiness (G3)
- [ ] Hosting decision recorded per product with residency conclusion
- [ ] Product facts re-verified, with dates
- [ ] Every integration has a design, auth method and failure behaviour
- [ ] Source-of-truth defined for each data domain
- [ ] RPO and RTO approved by business
- [ ] Operational owner identified

## B.3 Build readiness (G4)
- [ ] Pipelines deploy to all environments without manual steps
- [ ] No secrets in source control
- [ ] Code and configuration review complete
- [ ] Monitoring and alerts active in non-production
- [ ] Migration tooling runs on sample data

## B.4 Migration readiness (G5)
- [ ] Full-volume rehearsal completed and timed
- [ ] Reconciliation signed by business owners
- [ ] Password and token strategy agreed
- [ ] Redirect map tested
- [ ] Rollback or forward-recovery rehearsed

## B.5 Go-live readiness (G6)
- [ ] Functional, integration, security, performance tests passed or risks accepted
- [ ] UAT signed
- [ ] Backups verified by restore
- [ ] On-call and escalation contacts confirmed
- [ ] Operational owner appointed and trained
- [ ] Go / no-go meeting minuted

## B.6 Hypercare exit
- [ ] Stability criteria met for the agreed period
- [ ] No open severity 1 or 2 incidents
- [ ] Reconciliation of post-cutover transactions complete
- [ ] Operational owner resolving incidents unassisted

## B.7 Handover checklist (G7)
**Entry condition**
- [ ] Named operational owner accepted in writing (or fallback instrument executed)

**Platform and infrastructure**
- [ ] Production stable; architecture documentation complete
- [ ] Hosting and infrastructure ownership confirmed
- [ ] Environment access transferred; system and vendor accounts owned by client
- [ ] Deployment and rollback procedures documented

**Applications and integrations**
- [ ] Application, middleware and integration documentation complete
- [ ] API specifications available; integration owners identified
- [ ] Vendor dependencies documented

**Data and security**
- [ ] Data ownership and retention documented
- [ ] Migration and reconciliation reports accepted
- [ ] Security controls, access and permission ownership documented
- [ ] Secrets and credentials transferred securely

**Operations**
- [ ] Monitoring and alerting operational
- [ ] Incident procedures; support and escalation matrix approved
- [ ] Backup, recovery and DR procedures documented

**Knowledge transfer**
- [ ] Architecture walkthrough and operational training complete
- [ ] Deployment and troubleshooting demonstrated and performed by recipients
- [ ] Outstanding gaps recorded

**Project closure**
- [ ] Outstanding defects, accepted risks and technical debt documented
- [ ] Future recommendations provided
- [ ] Client handover acceptance signed
