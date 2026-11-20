# Reference Diagrams (Mermaid)

> Part of the *Enterprise Adobe DXP Development Handbook* v1.0 (Review Draft). Section numbers (§) refer to the handbook's original numbering; see the README at the root of this folder for the section map.

## C.1 Lifecycle and gates
```mermaid
flowchart LR
  P1[1 Requirements] -->|E1| P2[2 Design]
  P2 -->|E2| P3[3 Foundations]
  P3 -->|E3| P4[4 Implementation]
  P4 -->|E4| P5[5 Quality engineering]
  P5 -->|E5| P6[6 Release]
  P6 -->|E6 owner accepts release| P7[7 Stabilise and hand over]
  P7 -->|E7 named owner required| X[Consultant exit]
  P6 -. next increment .-> P4
```

## C.2 Solution architecture (illustrative)
```mermaid
flowchart TB
  U[Users] --> CDN[CDN / WAF]
  CDN --> AEM[AEM - content and experience]
  CDN --> COM[Adobe Commerce - commerce]
  AEM <--> COM
  AEM --> SDK[Web SDK / tags]
  COM --> EXT[Out-of-process extensions / events]
  SDK --> AEP[AEP - profile and data]
  EXT --> GW[API gateway / middleware]
  GW --> ERP[ERP and third parties]
  AEP --> MOD[Analytics / Target / AJO - where required]
  OBS[Logs, metrics, traces, alerts] -.- AEM
  OBS -.- COM
  OBS -.- GW
```

## C.3 CI/CD pipeline
```mermaid
flowchart LR
  C[Commit / PR] --> B[Build]
  B --> T[Unit tests]
  T --> S[Static and security scans]
  S --> A[Artefact]
  A --> D1[Deploy dev]
  D1 --> IT[Integration tests]
  IT --> D2[Deploy QA / stage]
  D2 --> E2E[E2E, performance, accessibility]
  E2E --> AP{Change approval}
  AP --> PR[Deploy production]
  PR --> V[Smoke tests and monitoring]
```

---

**End of Handbook – Version 1.0 Review Draft**
