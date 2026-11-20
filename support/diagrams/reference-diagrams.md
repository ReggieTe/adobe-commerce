# Reference Diagrams (Mermaid)

> Part of the *Enterprise Adobe DXP Support and Operations Handbook* v1.0 (Review Draft). Section numbers (§) refer to the handbook's original numbering; see the README at the root of this folder for the section map.

## C.1 Service lifecycle and gates
```mermaid
flowchart LR
  P1[1 Discovery] -->|S1| P2[2 Design]
  P2 -->|S2| P3[3 Transition-in]
  P3 -->|S3 owner and provider accepted| P4[4 Live operations]
  P4 --> P5[5 Improvement]
  P5 --> P6[6 Lifecycle and upgrades]
  P6 --> P4
  P4 -->|S7 review| P7[7 Renewal or transition-out]
```

## C.2 Support tiers and escalation
```mermaid
flowchart TB
  U[Users and monitoring] --> L1[L1 service desk]
  L1 --> L2[L2 application support]
  L2 --> L3[L3 technical support]
  L2 --> V[Adobe and third-party vendors]
  L3 --> V
  L3 --> DEV[Development team - fixes via change control]
  IC[Incident commander] -.- L2
  IC -.- L3
```

## C.3 Incident flow
```mermaid
flowchart LR
  D[Detect] --> L[Log and categorise]
  L --> T[Triage and diagnose]
  T --> C[Communicate]
  C --> R[Restore service]
  R --> V[Verify and close]
  V --> P[Post-incident review - Sev 1 and 2]
  P --> PR[Problem record and fix via change]
```

---

**End of Handbook – Version 1.0 Review Draft**
