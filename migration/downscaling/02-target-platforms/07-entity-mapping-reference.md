# 17. Cross-Platform Entity Mapping Reference

> Part of the *Adobe DXP Downscale Playbook* v1.0 (Review Draft). Section numbers (§) refer to the playbook's original numbering; see the root [README](../README.md) for the section map.

Use as the starting point for the Source-to-Target Mapping (template A.4). Treatments: **M** migrate, **A** archive, **R** rebuild, **X** drop with sign-off.

| Source entity (Adobe) | Woo | Presta | Shopify | Custom | Notes |
|---|---|---|---|---|---|
| Customer account | M | M | M | M | Passwords not portable |
| Customer address | M | M | M | M | Validate formats |
| Customer group | M | M | M (tags/segments) | M | Pricing logic differs |
| Consent record | M | M | M (marketing consent fields, plus archive evidence) | M | Keep evidence |
| Product (simple) | M | M | M | M | |
| Product (configurable) | M | M | M | M | Variant limits and combination counts |
| Product (bundle/grouped) | R | R | R | R | Usually plugin/app/rebuild |
| Category | M | M | M (collections) | M | Hierarchy handling differs |
| Attribute / option | M | M | M (options, metafields) | M | Define before import |
| Price, special price, tier price | M | M | R | M | Tier pricing may need plan features |
| Stock / inventory | M | M | M | M | Multi-source needs care |
| Promotion / cart rule | R | R | R | R | Rebuild, don't migrate rule engines |
| Tax rule | R | R | R | R | Configure per target |
| Order | M or A | M or A | M or A | M or A | Depth decided in §7.4 |
| Invoice / credit memo | A | A | A | M or A | Retention requirement |
| Shipment / tracking | M or A | M or A | M or A | M or A | |
| Payment record | A (references only) | A | A | A | No card data |
| CMS page / block | R | R | R | R | Content model differs |
| Content fragment | R | R | R (metaobjects) | R | |
| Digital asset + metadata | M | M | M (files plus metafields) | M | Preserve rights metadata |
| URL rewrite | M (as redirects) | M | M | M | Limits per target |
| AEP profile / audience | X or A | X or A | X or A | X or A | Re-create segments in the new tool |
| Analytics history | A | A | A | A | Archive summarised data |
| Admin users and roles | R | R | R | R | Rebuild, enforce MFA |
