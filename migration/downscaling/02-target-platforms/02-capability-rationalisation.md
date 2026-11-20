# 4. Capability Rationalisation

> Part of the *Adobe DXP Downscale Playbook* v1.0 (Review Draft). Section numbers (§) refer to the playbook's original numbering; see the root [README](../README.md) for the section map.

## 4.1 Principle

Every Adobe capability in use is classified before design starts: **Retain, Replace, Rebuild, Reduce, Retire, or Archive.** The business accepts what is reduced or retired in writing.

## 4.2 Indicative replacement map

Examples only. Selection depends on requirements and budget.

| Adobe capability | Typical replacement options | Note |
|---|---|---|
| Commerce catalogue, cart, checkout | Target platform core | Check B2B, tiered pricing, custom options |
| Commerce promotions and rules | Target promotions plus plugins or apps | Complex rule engines may not map; rebuild or simplify |
| Commerce customer groups, shared catalogues | Target customer groups, B2B features or plugins | Confirm plan or plugin limits |
| AEM pages and templates | Target CMS pages, WordPress (for Woo), headless CMS | Content model usually simplified |
| AEM DAM and metadata | Media library, DAM service or object storage with metadata | Rights and expiry metadata need an owner |
| AEM multi-site and translation | Multistore, multilingual plugins, or separate sites | Often reduced |
| AEP profile and audiences | CRM or email platform segments, or a CDP-lite tool | Identity stitching is usually lost |
| Analytics | Alternative analytics platform; archive historical data | Plan baseline continuity |
| Target tests and personalisation | A/B testing tool or retire | Often retire |
| Journey Optimizer | Email/SMS automation tool | Rebuild key journeys only |
| Search and recommendations | Target search, plugin or third-party search | Tune relevance after migration |
| Adobe IMS single sign-on for staff | Target roles, or identity provider integration | Define admin access model |

## 4.3 Capability loss register

For each Reduce or Retire decision record: capability, business value, users affected, workaround, cost to retain, owner sign-off. Unsigned losses block gate D2.

**Deliverable:** Capability Rationalisation Matrix and Loss Register (Appendix A.2).
