# PHASE 6: RELEASE AND DEPLOYMENT

> Part of the *Enterprise Adobe DXP Development Handbook* v1.0 (Review Draft). Section numbers (§) refer to the handbook's original numbering; see the README at the root of this folder for the section map.

## 9. Phase 6 – Release and Deployment

### 9.1 Objective
Release safely and reversibly, with clear approvals and communication.

### 9.2 Release Planning
Scope, version, release notes, deployment window, dependencies, communications, support cover, freeze rules (template A.7).

### 9.3 Change Approval
Follow the client's change process: risk rating, approvals, emergency-change rules.

### 9.4 Deployment
Deploy through the pipeline only. Prefer techniques that reduce risk (feature flags, staged rollout, blue/green or equivalent where the platform supports them). No manual production changes except under emergency procedure with retrospective record.

### 9.5 Production Verification
Smoke tests, key journey checks, integration checks, monitoring checks, data checks. Named verifier and sign-off.

### 9.6 Rollback and Forward-Fix
Define triggers, authority, time limits and steps. Consider data changes, content changes and external side effects; where rollback is impractical, define forward-fix.

### 9.7 Release Communication
Stakeholders, support teams and, where relevant, customers or authors are informed before and after the release.

### 9.8 Phase 6 Exit Criteria (Gate E6)
- Release approved by the client change authority.
- Deployment completed through the pipeline and verified.
- Monitoring shows healthy state for the agreed observation period.
- Release notes and documentation published.
- **Operational owner has accepted the release** into support.

**Final Deliverable:** Release Record and Production Verification Report.
