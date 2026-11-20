# PHASE 3: FOUNDATIONS – ENVIRONMENTS, REPOSITORIES AND PIPELINES

> Part of the *Enterprise Adobe DXP Development Handbook* v1.0 (Review Draft). Section numbers (§) refer to the handbook's original numbering; see the README at the root of this folder for the section map.

## 6. Phase 3 – Foundations

### 6.1 Objective
Establish the delivery platform so that engineers can commit, build, test and deploy safely from day one.

### 6.2 Environments
Development, integration, QA, staging and production, plus sandbox or personal environments as needed. Document data policy per environment (synthetic or masked data; no production personal data in lower environments without controls). Ensure parity of configuration between staging and production.

### 6.3 Repositories and Branching
Repository layout, branching strategy, protected branches, commit and PR conventions, versioning, release tagging. No secrets in source control.

### 6.4 CI/CD Pipelines
Build, unit test, static analysis, dependency and licence scanning, security scanning, artefact storage, deployment to each environment, approvals, rollback. Use the product-supported pipeline mechanism where the product prescribes one (verify per §1.5).

### 6.5 Engineering Standards
Coding standards per language, code review rules, definition of ready and definition of done (template A.3), documentation standards, logging standards, error-handling and configuration standards, accessibility standards.

### 6.6 Tooling
Issue tracking, local development setup, mock services, test data tooling, monitoring access, secrets vault, documentation platform.

### 6.7 Team Onboarding
Access, local setup guide, architecture walkthrough, standards walkthrough, first-commit exercise.

### 6.8 Phase 3 Exit Criteria (Gate E3)
- Environments provisioned and access confirmed.
- Pipelines build, test and deploy a sample change end to end.
- Standards, definition of done and review rules agreed.
- Secrets handled through an approved mechanism.
- Team onboarded.

**Final Deliverable:** Working Delivery Platform and Engineering Standards.
