# PHASE 4: IMPLEMENTATION

> Part of the *Enterprise Adobe DXP Development Handbook* v1.0 (Review Draft). Section numbers (§) refer to the handbook's original numbering; see the README at the root of this folder for the section map.

## 7. Phase 4 – Implementation

### 7.1 Objective
Build the solution in small, reviewed, tested increments against the approved design.

### 7.2 Delivery Cadence
Short iterations with a demo and a working increment. Maintain a visible backlog, a risk and dependency log, and a technical debt register (template A.9).

### 7.3 Product Implementation Guides

#### AEM
- Follow the prescribed project structure and the product's supported build and deployment model.
- Build reusable components with clear authoring dialogs; keep business logic out of templates.
- Design content structure for authors; enforce permissions and workflows that match the governance model.
- Manage caching and Dispatcher rules as code and test invalidation behaviour.
- Treat OSGi configuration per environment as managed configuration, not manual change.

#### Adobe Commerce
- Extend through modules, plugins, observers and APIs; avoid overriding core files.
- Keep business rules testable and isolated; document custom attributes and database changes with setup scripts.
- Test indexing, cron and queue behaviour for every feature that touches catalogue, pricing, inventory or orders.
- For API-first or out-of-process extensions, design for idempotency, retries and observability.
- Manage deployment configuration in version control, with environment-specific values handled securely.

#### AEP
- Design schemas and identity namespaces before ingestion; avoid late schema changes.
- Implement data collection with the supported SDK and a governed data layer.
- Enforce consent and data-usage labels as designed; test with representative profiles.
- Monitor ingestion and dataset health from the start.

#### Analytics, Target and Journey Optimizer
- Define a data layer specification and a tagging plan; implement through the tag management approach agreed.
- Test events, attributes and consent behaviour across browsers and devices before release.
- Keep activities, audiences and journeys documented and named consistently.

### 7.4 Integration Implementation
Implement each integration to its specification with authentication, retries, idempotency, timeouts, error handling and monitoring. Test success, failure and duplicate-message paths.

### 7.5 Security in Implementation
Dependency updates, secret rotation, input validation, output encoding, access control checks, secure defaults, and fix-forward of scanner findings by severity.

### 7.6 Code Review and Quality Gates
Every change is peer reviewed (template A.4). Pipelines enforce unit-test thresholds, static analysis, security scan and licence rules before merge.

### 7.7 Definition of Done
A story is done when code is reviewed and merged, tests pass, accessibility and performance checks pass, observability is in place, configuration is documented, documentation is updated, and the product owner has accepted it.

### 7.8 Documentation During Build
Architecture decisions, component specs, API specs, configuration guides, runbooks, known limitations and troubleshooting notes updated each iteration, not at the end.

### 7.9 Phase 4 Exit Criteria (Gate E4, per release increment)
- Scope for the release is complete and accepted by the product owner.
- Quality gates are green.
- Consultant review of code and configuration complete (Models B/C), findings dispositioned.
- Documentation current.
- Release candidate ready for formal quality engineering.

**Final Deliverable:** Release Candidate with Documentation.
