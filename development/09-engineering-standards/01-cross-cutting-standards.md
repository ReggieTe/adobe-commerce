# 11. Cross-Cutting Engineering Standards

> Part of the *Enterprise Adobe DXP Development Handbook* v1.0 (Review Draft). Section numbers (§) refer to the handbook's original numbering; see the README at the root of this folder for the section map.

## 11.1 Branching and Versioning
Trunk-based or short-lived branches; protected main; semantic versioning for deployable artefacts; tags per release.

## 11.2 Code Review
Review for correctness, readability, security, performance, test coverage, upgrade safety and standards. Two-person rule for production-affecting change where the risk requires it.

## 11.3 Testing Standards
Meaningful unit coverage on business logic, contract tests on integrations, deterministic automated end-to-end tests for critical journeys, stable test data.

## 11.4 Security Standards
Least privilege, vaulted secrets with rotation, dependency and container scanning, secure headers, safe handling of personal data, logging without sensitive data.

## 11.5 Performance Standards
Budgets per page and API; caching rules documented; indexing and query reviews; load tests before major releases.

## 11.6 Accessibility and Content Standards
Agreed accessibility level; semantic markup; authoring guidance; image and metadata standards.

## 11.7 Observability Standards
Structured logs with correlation identifiers, golden-signal metrics, business-transaction monitors, actionable alerts with owners.

## 11.8 Documentation Standards
Docs-as-code, versioned with the code, reviewed in pull requests.

## 11.9 Technical Debt Management
Maintain a visible register with impact and effort; reserve capacity each iteration; link debt to product lifecycle dates.

## 11.10 Product Upgrade and Lifecycle Readiness
Track vendor release notes, deprecations and end-of-support dates. Keep extensions on supported APIs so upgrades remain routine.
