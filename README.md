# Vendure (vendure)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
