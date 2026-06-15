# Vendure (vendure)

Vendure is an open-source headless commerce framework built in TypeScript on top of NestJS, GraphQL, and TypeORM. A Vendure server exposes two GraphQL APIs — the Shop API (consumed by storefronts) and the Admin API (consumed by the Dashboard and back-office tooling) — plus an Asset Server REST surface for uploads and image previews, and a plugin system that extends data, services, jobs, and resolvers. The project is GPLv3-licensed Vendure Core, complemented by a commercial Vendure Platform layer of 20+ enterprise plugins, a managed Vendure Cloud offering, an official MCP server, and a starter ecosystem (Next.js, Remix, Qwik, SvelteKit, Angular, Gatsby).

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/vendure/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/vendure/refs/heads/main/apis.yml)

## Tags

- Commerce
- Headless Commerce
- eCommerce
- GraphQL
- Open Source
- TypeScript
- NestJS
- B2B
- B2C
- Storefront
- Plugins

## Timestamps

- **Created:** 2026-05-23
- **Modified:** 2026-05-25

## APIs

### Vendure Shop GraphQL API

Public GraphQL API consumed by storefronts and end-customer clients — product and collection browse, faceted search, active order / cart, checkout, eligible shipping and payment methods, customer registration, account and address management, and order lookup. Mounted by default at /shop-api on the Vendure server.

- **Human URL:** [https://docs.vendure.io/reference/graphql-api/shop/queries/](https://docs.vendure.io/reference/graphql-api/shop/queries/)
- **Base URL:** `http://localhost:3000/shop-api`

#### Tags

- GraphQL
- Storefront
- Shop
- Cart
- Checkout
- Customer

#### Properties

- [Documentation](https://docs.vendure.io/reference/graphql-api/shop/queries/)
- [OpenAPI](openapi/vendure-shop-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/vendure-shop-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/vendure-shop-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/vendure-product-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/vendure-order-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Vendure Admin GraphQL API

Privileged GraphQL API consumed by the Vendure Dashboard and back-office tooling — catalogue, channels, orders, customers, customer groups, fulfillment, promotions, tax categories and rates, zones and countries, sellers, stock locations, payment methods, shipping methods, administrators, roles, API keys, jobs and scheduled tasks, and global settings. Mounted by default at /admin-api on the Vendure server.

- **Human URL:** [https://docs.vendure.io/reference/graphql-api/admin/queries/](https://docs.vendure.io/reference/graphql-api/admin/queries/)
- **Base URL:** `http://localhost:3000/admin-api`

#### Tags

- GraphQL
- Admin
- Back-Office
- Catalog
- Orders
- Customers

#### Properties

- [Documentation](https://docs.vendure.io/reference/graphql-api/admin/queries/)
- [OpenAPI](openapi/vendure-admin-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/vendure-admin-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/vendure-admin-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/vendure-product-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/vendure-order-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/vendure-customer-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Vendure Asset Server REST API

REST surface exposed by the AssetServerPlugin. Serves images and binary assets uploaded through the Admin API; supports preview transforms via query parameters (preset, w, h, mode, format) and acts as the storage backend for product, collection, and rich-text assets.

- **Human URL:** [https://docs.vendure.io/](https://docs.vendure.io/)
- **Base URL:** `http://localhost:3000/assets`

#### Tags

- REST
- Assets
- Images
- Storage

#### Properties

- [Documentation](https://docs.vendure.io/)
- [OpenAPI](openapi/vendure-asset-server-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/vendure-asset-server.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/vendure-asset-server.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Website](https://vendure.io/)
- [Documentation](https://docs.vendure.io/)
- [Git Hub](https://github.com/vendurehq)
- [Repository](https://github.com/vendurehq/vendure)
- [Platform](https://vendure.io/platform)
- [Cloud](https://vendure.io/cloud)
- [Pricing](https://vendure.io/pricing)
- [Hub](https://vendure.io/hub)
- [LinkedIn](https://www.linkedin.com/company/vendure)
- [L L Ms Txt](https://docs.vendure.io/llms.txt)
- [M C P](https://docs.vendure.io/mcp)
- [License](https://github.com/vendurehq/vendure/blob/master/LICENSE)
- [Plans](plans/vendure-plans-pricing.yml)
- [Rate Limits](rate-limits/vendure-rate-limits.yml)
- [Fin Ops](finops/vendure-finops.yml)
- [JSON-LD](json-ld/vendure-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Vocabulary](vocabulary/vendure-vocabulary.yml)
- [Rules](rules/vendure-rules.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
