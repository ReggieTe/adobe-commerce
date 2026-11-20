# 15. Target Playbook: Shopify

> Part of the *Adobe DXP Downscale Playbook* v1.0 (Review Draft). Section numbers (§) refer to the playbook's original numbering; see the root [README](../README.md) for the section map.

> Plans, limits and features change often. Verify against current Shopify documentation and the client's plan (see §1.7).

## 15.1 Fit
Strong when the client wants low operational burden, reliable checkout and fast iteration, and the business model is a standard B2C or simple B2B shop. Constrained where deep checkout, data-model or URL control is required.

## 15.2 Architecture and Hosting
Shopify hosts the platform. The client designs what sits around it: apps, middleware for ERP and 3PL, a separate content solution if content is heavy, an archive for historical data, and a backup/export routine for store data. Decide the plan tier against required features (for example B2B, checkout extensibility, markets, API limits).

## 15.3 Mapping Notes (Adobe Commerce → Shopify)
| Adobe Commerce | Shopify | Note |
|---|---|---|
| Simple product | Product with a single variant | Direct |
| Configurable product and options | Product with options and variants | Option and variant limits apply (verify current); very large option sets may need restructuring |
| Bundles and grouped products | Bundles via app or native bundles where available | App cost and behaviour vary |
| Custom attributes | Metafields and metaobjects | Define definitions before import |
| Categories | Collections (manual or automated) | Hierarchy is flat; use navigation menus for structure |
| Customer groups and tier pricing | Customer tags/segments, catalogues and price lists (B2B or markets features) | Plan and feature dependent |
| Cart price rules | Discounts and automatic discounts, Functions | Complex rule logic needs apps or custom functions |
| Multi-source inventory | Locations and inventory | Reasonable fit |
| CMS pages and blocks | Pages, blogs, sections | Limited; heavy content needs a headless CMS |
| URL rewrites | URL redirects | Platform path prefixes are fixed; redirect volume has limits (verify) |

## 15.4 Customers and Passwords
Password hashes from Adobe Commerce cannot be imported. Customers are imported through CSV or the Admin API and then invited or use the platform's sign-in flow to set access. Plan customer communications and expect a login-support spike. Avoid imports that trigger unwanted marketing or invitation emails by controlling the settings during load.

## 15.5 Orders and History
Historical orders can be created through the Admin API, but behaviour is constrained (for example around payments, fulfilment state and notifications), and API rate limits apply. Decide whether to import orders as full records or keep older history in the archive and link to it from customer service tooling. Preserve original order numbers as references.

## 15.6 Content
Pages, blogs and structured data via metaobjects cover simple content. For AEM-scale content, use a headless CMS or keep a separate content site and integrate navigation and search.

## 15.7 Integrations and Payments
Use native apps or middleware for ERP and fulfilment. Payment provider availability, fees and checkout behaviour depend on the country and plan; third-party gateways may add transaction fees. Verify which gateways support the client's market. Checkout customisation is bounded by the platform; confirm needs against its current extensibility model.

## 15.8 Limits and Gotchas
- API rate limits shape migration duration.
- Checkout, URL and data-model constraints are firm.
- App costs and app dependencies accumulate.
- Store data export routes exist but are not a full database dump; plan your own backup and archive.
- Redirect, variant and option limits can force restructuring.

## 15.9 Cutover Specifics
Connect the domain, set primary domain and redirects, verify SSL, import final deltas, check payments and tax, confirm markets and currency, test checkout end to end, and monitor order flow into ERP and fulfilment.

## 15.10 Verify List
Plan features and limits; variant and option limits; API rate limits; redirect limits; gateway availability and fees; customer account model; checkout extensibility scope; backup and export options; data location and DPA terms.
