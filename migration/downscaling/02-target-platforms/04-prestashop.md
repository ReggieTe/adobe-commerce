# 14. Target Playbook: PrestaShop

> Part of the *Adobe DXP Downscale Playbook* v1.0 (Review Draft). Section numbers (§) refer to the playbook's original numbering; see the root [README](../README.md) for the section map.

> Verify against current PrestaShop documentation and module compatibility (see §1.7).

## 14.1 Fit
Good for commerce-first stores, multistore and multilingual setups, and teams with PHP skills. Content tooling is basic; content-heavy AEM sites need a separate CMS or headless content solution.

## 14.2 Architecture and Hosting
Self-managed or managed PHP hosting. Plan caching, a CDN, search (built-in or an external service), cron and background jobs, and an upgrade process for core and modules. Keep custom code in modules, not in core.

## 14.3 Mapping Notes (Adobe Commerce → PrestaShop)
| Adobe Commerce | PrestaShop | Note |
|---|---|---|
| Simple product | Standard product | Direct |
| Configurable product | Product with combinations | Attribute groups and combinations; verify scale |
| Bundle products | Pack products | Capabilities differ |
| Custom attributes | Features, custom fields via module | Decide features vs module-defined |
| Customer groups, tier pricing | Customer groups, specific prices | Reasonable fit |
| Cart price rules | Cart rules | Some rule types will not map |
| Multi-website, store views | Multistore | Map shop contexts and languages carefully |
| CMS pages and blocks | CMS pages and modules | Limited; consider an external CMS |
| URL rewrites | Friendly URLs plus redirects | Redirect handling often needs a module |

## 14.4 Customers and Passwords
Adobe password hashes are not directly usable. Use forced reset, or a vetted module that verifies the legacy hash once and rehashes. Plan communications and support load.

## 14.5 Orders and History
Import via the web service API, import tooling or scripts. Maintain order references and states; mark historical orders to avoid notifications. Map order states carefully because the target state machine differs.

## 14.6 Content
Use CMS pages for simple content. For AEM-grade content, pair PrestaShop with a headless or separate CMS and plan how URLs, menus and search combine.

## 14.7 Integrations and Payments
Use maintained modules or middleware. Confirm module compatibility with the chosen PrestaShop version before committing to a build. Use hosted payment fields or redirect gateways.

## 14.8 Limits and Gotchas
- Module ecosystem quality varies; check maintenance history.
- Major upgrades need planned effort.
- Large combination counts affect performance.
- Multistore adds complexity to imports and redirects.

## 14.9 Cutover Specifics
Same pattern as §13.9, plus verifying shop context, language-specific URLs and cart rule behaviour.

## 14.10 Verify List
Supported version and PHP requirements; module compatibility; web service limits; hash verification options; pack and combination scale; redirect handling approach.
