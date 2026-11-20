# Reference Diagrams (Mermaid)

> Part of the *Enterprise Adobe DXP Migration Handbook* v1.1 (Review Draft). Section numbers (§) refer to the handbook's original numbering; see the root [README](../README.md) for the section map.

## C.1 Lifecycle and gates
```mermaid
flowchart LR
  P1[1 Discovery] -->|G1| P2[2 Strategy]
  P2 -->|G2| P3[3 Design]
  P3 -->|G3| P4[4 Build]
  P4 -->|G4| P5[5 Migration]
  P5 -->|G5| P6[6 Test and Cutover]
  P6 -->|G6 + operational owner appointed| P7[7 Hypercare and Handover]
  P7 -->|G7 named owner required| X[Consultant exit]
```

## C.2 Target architecture (illustrative)
```mermaid
flowchart TB
  U[Customers and users] --> CDN[CDN / WAF]
  CDN --> AEM[AEM - content]
  CDN --> COM[Adobe Commerce - commerce]
  AEM <--> COM
  COM --> GW[API gateway / middleware]
  AEM --> GW
  GW --> ERP[ERP / finance]
  GW --> PIM[PIM / OMS / WMS]
  GW --> PAY[Payments / tax / shipping]
  COM --> AEP[Adobe Experience Platform]
  AEM --> AEP
  AEP --> MOD[Analytics / Target / AJO - where required]
  IDP[Identity provider] --- COM
  IDP --- AEM
  OBS[Monitoring, logging, alerting] -.- GW
  OBS -.- COM
  OBS -.- AEM
```

## C.3 Cutover sequence
```mermaid
sequenceDiagram
  participant B as Business
  participant C as Consultant / build team
  participant O as Operational owner
  participant S as Source platform
  participant T as Adobe DXP
  B->>C: Go-ahead for cutover window
  C->>S: Freeze changes
  C->>S: Final extract
  C->>T: Delta import
  C->>T: Reconcile and validate
  C->>B: Go / no-go checkpoint
  B->>C: Approve
  C->>T: Switch DNS and traffic
  O->>T: Monitor (first line)
  C->>O: Support during hypercare
```

---

**End of Handbook – Version 1.1 Review Draft**
