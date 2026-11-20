# 13. Target Playbook: WooCommerce

> Part of the *Adobe DXP Downscale Playbook* v1.0 (Review Draft). Section numbers (§) refer to the playbook's original numbering; see the root [README](../README.md) for the section map.

> Platform facts below are indicative. Verify against current WordPress, WooCommerce and plugin documentation (see §1.7).

## 13.1 Fit
Best where content and commerce live together, WordPress skills exist, the catalogue is moderate, and the client wants full control of data and hosting. Weaker for very large catalogues or complex B2B without careful engineering and hosting.

## 13.2 Architecture and Hosting
- Self-managed or managed WordPress hosting. Choose for PHP version support, object caching, database performance, backups, WAF and staging environments.
- Use full-page caching, object cache and a CDN. Plan search separately (an external search service is common for larger catalogues).
- Keep the plugin set small and vetted. Each plugin is an upgrade and security dependency.
- Use the platform's high-performance order storage option where available; confirm plugin compatibility before enabling it.
- Separate staging and production; use a deployment pipeline and keep configuration in code where possible.

## 13.3 Mapping Notes (Adobe Commerce → WooCommerce)
| Adobe Commerce | WooCommerce | Note |
|---|---|---|
| Simple product | Simple product | Direct |
| Configurable product and options | Variable product with attributes and variations | Option combinations expand to variations; check count and performance |
| Bundle, grouped products | Grouped or bundle via plugin | Bundles typically need an extension |
| Custom attributes | Product attributes, custom fields | Define taxonomy vs meta deliberately |
| Categories | Product categories | Preserve hierarchy and slugs |
| Customer groups and tier pricing | Roles plus pricing plugin | Plugin-dependent |
| Cart price rules | Coupons and rules plugins | Complex rules need simplification or custom code |
| Inventory (single source) | Stock management | Multi-source inventory needs a plugin or an ERP |
| CMS pages and blocks | WordPress pages and blocks | Rebuild in the block editor or page builder |
| URL rewrites | Redirect rules | Export and convert (§17) |

## 13.4 Customers and Passwords
Customers become WordPress users with the customer role. Imported password hashes from Adobe Commerce are not directly usable. Use one of: forced reset with a clear customer communication; a vetted, temporary legacy-hash verification step that rehashes on first successful login; or SSO through an external identity provider. Security review any legacy-hash approach.

## 13.5 Orders and History
Import through the REST API, import tools or custom scripts. Mark historical orders so they do not send emails or alter stock. Keep original order numbers as meta and display them in admin. Very large order histories slow admin and reporting; consider importing only recent years and archiving the rest.

## 13.6 Content
WordPress is strong for content. Rebuild AEM templates as themes and blocks; convert content fragments to custom post types or structured fields. Migrate media into the media library or object storage with a CDN.

## 13.7 Integrations and Payments
Use maintained connectors for ERP, shipping and tax where they exist; otherwise middleware or custom services. Use hosted payment fields or redirect gateways to keep PCI scope low. Confirm local gateway plugins are actively maintained.

## 13.8 Limits and Gotchas
- Performance depends on hosting and plugin quality.
- Plugin conflicts and updates are the main operational risk.
- Multi-currency, B2B and multi-warehouse needs add plugins and complexity.
- WordPress admin roles are simpler than Adobe's; map them deliberately.

## 13.9 Cutover Specifics
Lower DNS TTLs in advance, freeze catalogue and content, run the delta migration, switch DNS, clear caches, verify redirects and payment webhooks, and watch error logs and checkout success.

## 13.10 Verify List
Current WordPress and WooCommerce requirements; order storage mode; supported hash handling options; payment gateway plugin status; hosting resource needs; plugin compatibility matrix.
