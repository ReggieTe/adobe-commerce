# Reference Diagrams (Mermaid)

> Part of the *Adobe DXP Downscale Playbook* v1.0 (Review Draft). Section numbers (§) refer to the playbook's original numbering; see the root [README](../README.md) for the section map.

## C.1 Lifecycle and gates
```mermaid
flowchart LR
  P1[1 Exit discovery] -->|D1| P2[2 Target selection]
  P2 -->|D2| P3[3 Design]
  P3 -->|D3| P4[4 Build]
  P4 -->|D4| P5[5 Extraction and migration]
  P5 -->|D5| P6[6 Test and cutover]
  P6 -->|D6 + operational owner appointed| P7[7 Hypercare and decommissioning]
  P7 -->|D7 owner and Adobe exit evidenced| X[Consultant exit]
```

## C.2 Target architecture (illustrative)
```mermaid
flowchart TB
  U[Customers] --> CDN[CDN / WAF]
  CDN --> SF[Storefront on target platform]
  SF --> PAY[Payment gateway - hosted fields]
  SF --> SRCH[Search]
  SF --> CMS[Content: platform CMS or headless]
  SF --> MW[Middleware / connectors]
  MW --> ERP[ERP / finance]
  MW --> LOG[Shipping / 3PL / tax]
  SF --> EML[Email / CRM]
  SF --> AN[Replacement analytics]
  ARC[(Archive: historical orders and records)] -.- SF
  OBS[Monitoring and alerting] -.- SF
  OBS -.- MW
```

## C.3 Cutover and decommissioning sequence
```mermaid
sequenceDiagram
  participant B as Business
  participant C as Consultant / build team
  participant O as Operational owner
  participant A as Adobe estate
  participant T as Target platform
  B->>C: Approve cutover window
  C->>A: Freeze changes
  C->>A: Final delta extract
  C->>T: Load and reconcile
  C->>B: Go / no-go
  B->>C: Approve
  C->>T: Switch DNS, activate redirects and integrations
  O->>T: Monitor first line
  Note over A: Read-only fallback window
  B->>A: Confirm stability, end fallback
  B->>A: Serve notices, revoke access
  A-->>B: Deletion confirmation
```

---

**End of Playbook – Version 1.0 Review Draft**
