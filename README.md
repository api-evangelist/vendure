# Vendure (vendure)

Vendure is an open-source headless commerce framework built in TypeScript on top of NestJS, GraphQL, and TypeORM. A Vendure server exposes two GraphQL APIs — the Shop API (consumed by storefronts) and the Admin API (consumed by the Dashboard and back-office tooling) — plus an Asset Server REST surface for uploads and image previews, and a plugin system that extends data, services, jobs, and resolvers. The project is GPLv3-licensed Vendure Core, complemented by a commercial Vendure Platform capability layer, a managed Vendure Cloud offering (design-partner / GA Q4 2026), an official MCP server for AI coding assistants, and a starter ecosystem (Next.js, Remix, Qwik, SvelteKit, Angular, Gatsby).

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/vendure/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=opensource-vendure&utm_content=repo)

## Tags

 - Commerce, Headless Commerce, eCommerce, GraphQL, Open Source, TypeScript, NestJS, B2B, B2C, Storefront, Plugins

## Timestamps

- **Created:** 2026-05-23
- **Modified:** 2026-05-25

## Type

`opensource` — Vendure Core is distributed under GPL-3.0. Commercial offerings (Vendure Platform, Vendure Cloud) layer on top.

## Project Snapshot

| Property | Value |
|---|---|
| GitHub org | [vendurehq](https://github.com/vendurehq) |
| Core repo | [vendurehq/vendure](https://github.com/vendurehq/vendure) |
| Latest release | v3.6.3 (May 2026) |
| License | GPL-3.0 (Core); commercial license available via Vendure Platform |
| Language | TypeScript (94%+) |
| Runtime | Node.js 20 / 22 / 24 |
| Databases | PostgreSQL, MySQL, MariaDB, SQLite |
| Framework | NestJS |
| ORM | TypeORM |
| GraphQL server | Apollo Server |
| Admin UI | React (`@vendure/dashboard`) |
| Default ports | `:3000/shop-api`, `:3000/admin-api`, `:3000/dashboard` |

## APIs

### Vendure Shop GraphQL API
Public GraphQL API consumed by storefronts and end-customer clients — product and collection browse, faceted search, active order / cart, checkout, eligible shipping and payment methods, customer registration, account and address management, and order lookup. Mounted by default at `/shop-api`.

**Human URL:** [https://docs.vendure.io/reference/graphql-api/shop/queries/](https://docs.vendure.io/reference/graphql-api/shop/queries/)

- [OpenAPI](openapi/vendure-shop-api-openapi.yml)
- [JSON Schema — Product](json-schema/vendure-product-schema.json)
- [JSON Schema — Order](json-schema/vendure-order-schema.json)
- [JSON Schema — Customer](json-schema/vendure-customer-schema.json)
- [JSON-LD](json-ld/vendure-context.jsonld)
- [Naftiko Capability — Shop Products](capabilities/shop-products.yaml)
- [Naftiko Capability — Shop Active Order](capabilities/shop-active-order.yaml)
- [Naftiko Capability — Shop Checkout](capabilities/shop-checkout.yaml)
- [Naftiko Capability — Shop Customer](capabilities/shop-customer.yaml)
- Example: [Active Order](examples/vendure-shop-active-order-example.json)
- Example: [Add Item](examples/vendure-shop-add-item-example.json)
- Example: [Search](examples/vendure-shop-search-example.json)

### Vendure Admin GraphQL API
Privileged GraphQL API consumed by the Vendure Dashboard and back-office tooling — catalogue, channels, orders, customers, customer groups, fulfillment, promotions, tax categories and rates, zones and countries, sellers, stock locations, payment methods, shipping methods, administrators, roles, API keys, jobs and scheduled tasks, and global settings. Mounted by default at `/admin-api`.

**Human URL:** [https://docs.vendure.io/reference/graphql-api/admin/queries/](https://docs.vendure.io/reference/graphql-api/admin/queries/)

- [OpenAPI](openapi/vendure-admin-api-openapi.yml)
- [Naftiko Capability — Admin Catalog](capabilities/admin-catalog.yaml)
- [Naftiko Capability — Admin Orders](capabilities/admin-orders.yaml)
- [Naftiko Capability — Admin Customers](capabilities/admin-customers.yaml)
- [Naftiko Capability — Admin Channels](capabilities/admin-channels.yaml)
- [Naftiko Capability — Admin Promotions](capabilities/admin-promotions.yaml)
- [Naftiko Capability — Admin Jobs](capabilities/admin-jobs.yaml)
- Example: [Create Product](examples/vendure-admin-create-product-example.json)

### Vendure Asset Server REST API
REST surface exposed by `@vendure/asset-server-plugin`. Serves images and binary assets uploaded through the Admin API; supports preview transforms via query parameters (`preset`, `w`, `h`, `mode`, `format`, `q`) and acts as the storage backend for product, collection, and rich-text assets.

- [OpenAPI](openapi/vendure-asset-server-openapi.yml)
- Example: [Asset Preview](examples/vendure-asset-preview-example.json)

## Tools, Packages & Surfaces

| Surface | Package / Repo | Purpose |
|---|---|---|
| Server framework | [`@vendure/core`](https://www.npmjs.com/package/@vendure/core) | The Vendure server — entities, services, GraphQL APIs, plugin system, job queue, event bus |
| Project scaffolder | [`@vendure/create`](https://www.npmjs.com/package/@vendure/create) | `npx @vendure/create` — bootstrap a new Vendure project |
| Developer CLI | [`@vendure/cli`](https://www.npmjs.com/package/@vendure/cli) | Generate plugins, entities, services, API extensions, migrations |
| Admin UI | [`@vendure/dashboard`](https://www.npmjs.com/package/@vendure/dashboard) | React-based admin dashboard against the Admin GraphQL API |
| Asset Server | [`@vendure/asset-server-plugin`](https://www.npmjs.com/package/@vendure/asset-server-plugin) | Asset storage, REST asset endpoints, image transforms |
| Email | [`@vendure/email-plugin`](https://www.npmjs.com/package/@vendure/email-plugin) | Transactional email pipeline (Handlebars/MJML) |
| Job queue | [`@vendure/job-queue-plugin`](https://www.npmjs.com/package/@vendure/job-queue-plugin) | Production job queue (BullMQ / Redis) |
| Production hardening | [`@vendure/harden-plugin`](https://www.npmjs.com/package/@vendure/harden-plugin) | Disable introspection, bound GraphQL complexity/depth |
| GraphiQL explorer | [`@vendure/graphiql-plugin`](https://www.npmjs.com/package/@vendure/graphiql-plugin) | Interactive query authoring against Shop/Admin endpoints |
| Telemetry | [`@vendure/telemetry-plugin`](https://www.npmjs.com/package/@vendure/telemetry-plugin) | OpenTelemetry instrumentation |
| Testing harness | [`@vendure/testing`](https://www.npmjs.com/package/@vendure/testing) | End-to-end testing with seeded isolated server |
| Community plugins | [vendurehq/community-plugins](https://github.com/vendurehq/community-plugins) | Braintree, Stripe, Algolia, Elasticsearch, Typesense, etc. |
| Docs MCP server | [docs.vendure.io/mcp](https://docs.vendure.io/mcp) | Remote MCP exposing Vendure docs to AI coding assistants |

## Starter Storefronts

- [Next.js](https://github.com/vendurehq/nextjs-starter-vendure) — Next.js 16 official starter
- [Remix](https://github.com/vendurehq/storefront-remix-starter) — Remix storefront kit (226+ stars)
- [Qwik](https://github.com/vendurehq/storefront-qwik-starter) — Qwik storefront kit
- [SvelteKit](https://github.com/vendurehq/storefront-sveltekit-starter)
- [Angular PWA](https://github.com/vendurehq/storefront-angular-starter)

## Commercial Layers

- **Vendure Platform** — Enterprise capability layer with 20+ enterprise plugins (advanced B2B, contract pricing, SSO, audit, governance), production-ready Next.js storefront, AI tooling, dedicated support, and a commercial license alternative to GPLv3. Sold on an annual flat fee (not GMV-priced). [Pricing](https://vendure.io/pricing)
- **Vendure Cloud** — Managed hosting for Vendure (Core or Platform) with auto-scaling, automated backups, multi-region deployments, EU data residency, and built-in observability. Available now for design partners; general availability scheduled Q4 2026.

## Governance & Operational Surfaces

- [Plans](plans/vendure-plans-pricing.yml) — Capability and commercial layer surface (API Commons Plans 0.1)
- [Rate Limits](rate-limits/vendure-rate-limits.yml) — Operator-side controls and `@vendure/harden-plugin` levers
- [FinOps](finops/vendure-finops.yml) — FinOps Foundation Framework / FOCUS 1.3 alignment
- [Vocabulary](vocabulary/vendure-vocabulary.yml) — Domain vocabulary and order/payment state machines
- [Spectral Ruleset](rules/vendure-rules.yml) — Conventions for Vendure OpenAPI specs
- [JSON-LD Context](json-ld/vendure-context.jsonld) — Linked-data mapping to schema.org

## Quick Start

```bash
# Scaffold a new Vendure project (Node 20/22/24)
npx @vendure/create my-shop

# Default endpoints after `npm run dev`:
#   Shop API:   http://localhost:3000/shop-api
#   Admin API:  http://localhost:3000/admin-api
#   Dashboard:  http://localhost:3000/dashboard
#
# Default admin credentials: superadmin / superadmin
```

## References

- Website: [vendure.io](https://vendure.io/)
- Documentation: [docs.vendure.io](https://docs.vendure.io/)
- GitHub org: [vendurehq](https://github.com/vendurehq)
- Repository: [vendurehq/vendure](https://github.com/vendurehq/vendure)
- Pricing: [vendure.io/pricing](https://vendure.io/pricing)
- LinkedIn: [linkedin.com/company/vendure](https://www.linkedin.com/company/vendure)
- LLMs.txt: [docs.vendure.io/llms.txt](https://docs.vendure.io/llms.txt)
- MCP: [docs.vendure.io/mcp](https://docs.vendure.io/mcp)
