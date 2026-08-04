# crates.io (crates-io)

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

crates.io is the official package registry for the Rust programming language, operated by the crates.io team under the Rust Foundation with infrastructure support from Amazon Web Services and Fastly. It exposes a Web API at /api/v1 used by Cargo and the website for search, publishing, yanking, and owner management, plus a sparse HTTP index at index.crates.io that has been Cargo's default registry protocol since Rust 1.70 (June 2023). The legacy git index is still mirrored. Every published version is checksummed with SHA-256 and companion documentation is auto-built on docs.rs. The crates.io source code is dual-licensed under Apache-2.0 and MIT and runs on Rust (axum, diesel) with a SvelteKit frontend.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/crates-io/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/crates-io/refs/heads/main/apis.yml)

## Scope

- **Position:** Consuming
- **Access:** 3rd-Party

## Tags

- Rust
- Package Registry
- Crates
- Cargo
- Open Source
- Developer Tools
- Rust Foundation

## Timestamps

- **Created:** 2026-05-25T00:00:00.000Z
- **Modified:** 2026-05-25

## APIs

### crates.io Web API

The crates.io Web API exposes the endpoints used by Cargo and the crates.io website to search the registry, fetch crate and version metadata, publish new versions, yank and unyank versions, and manage crate ownership. Hosted at https://crates.io/api/v1, it is the canonical implementation of the Cargo Registry Web API specification documented in the Cargo book.

- **Human URL:** [https://doc.rust-lang.org/cargo/reference/registry-web-api.html](https://doc.rust-lang.org/cargo/reference/registry-web-api.html)

#### Tags

- Crates
- Package Registry
- Rust
- Search
- Publishing

#### Properties

- [Documentation](https://doc.rust-lang.org/cargo/reference/registry-web-api.html)
- [OpenAPI](openapi/crates-io-web-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/crates-io-web-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/crates-io-web-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/crates-io-crate-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/crates-io-crate-structure.json)
- [JSON-LD](json-ld/crates-io-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Spectral Rules](rules/crates-io-rules.yml)
- [Example](examples/crates-io-search-example.json)
- [Example](examples/crates-io-get-crate-example.json)

### crates.io Sparse Index

The crates.io sparse index at https://index.crates.io serves the registry config document plus per-crate newline-delimited JSON metadata files over HTTP, replacing the legacy git index clone. Cargo uses the sparse protocol by default since Rust 1.70 (June 2023). Each index entry records a version's dependencies, features, SHA-256 checksum, and yank state.

- **Human URL:** [https://doc.rust-lang.org/cargo/reference/registry-index.html](https://doc.rust-lang.org/cargo/reference/registry-index.html)

#### Tags

- Index
- Package Registry
- Rust
- Sparse Protocol

#### Properties

- [Documentation](https://doc.rust-lang.org/cargo/reference/registry-index.html)
- [Documentation](https://blog.rust-lang.org/2023/03/09/Rust-1.68.0.html)
- [OpenAPI](openapi/crates-io-sparse-index-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/crates-io-sparse-index.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/crates-io-sparse-index.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/crates-io-index-entry-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [Example](examples/crates-io-config-example.json)
- [Example](examples/crates-io-sparse-index-example.json)

## Common Properties

- [Portal](https://crates.io)
- [Documentation](https://doc.rust-lang.org/cargo/)
- [Documentation](https://doc.rust-lang.org/cargo/reference/registry-web-api.html)
- [Documentation](https://doc.rust-lang.org/cargo/reference/registry-index.html)
- [Documentation](https://doc.rust-lang.org/cargo/reference/registries.html)
- [Documentation](https://doc.rust-lang.org/cargo/reference/registry-authentication.html)
- [Getting Started](https://doc.rust-lang.org/cargo/reference/publishing.html)
- [GitHub Organization](https://github.com/rust-lang/crates.io)
- [Source Code](https://github.com/rust-lang/crates.io-index)
- [Source Code](https://github.com/rust-lang/crates.io-index-archive)
- [Source Code](https://github.com/rust-lang/cargo)
- [Tool](https://github.com/rust-lang/crates-io-auth-action)
- [GitHub Organization](https://github.com/rust-lang/crates-io-cargo-teams)
- [Tool](https://github.com/rust-lang/crates-io-ops-bot)
- [Tool](https://github.com/rust-lang/crates_io_og_image)
- [Tool](https://github.com/rust-lang/crates-io-heroku-metrics)
- [Status Page](https://status.crates.io/)
- [Blog](https://blog.rust-lang.org/inside-rust/)
- [Changelog](https://blog.rust-lang.org/2023/03/09/Rust-1.68.0.html)
- [Documentation](https://github.com/rust-lang/crates.io/blob/main/CONTRIBUTING.md)
- [Security Policy](https://github.com/rust-lang/crates.io/blob/main/SECURITY.md)
- [Code Of Conduct](https://github.com/rust-lang/crates.io/blob/main/CODE_OF_CONDUCT.md)
- [License](https://github.com/rust-lang/crates.io/blob/main/LICENSE-APACHE)
- [License](https://github.com/rust-lang/crates.io/blob/main/LICENSE-MIT)
- [Support](mailto:help@crates.io)
- [Forum](https://rust-lang.zulipchat.com/#narrow/stream/318791-t-crates-io)
- [Forum](https://github.com/rust-lang/crates.io/discussions)
- [Documentation](https://crates.io/policies)
- [Documentation](https://crates.io/data-access)
- [Documentation](https://docs.rs)
- [Sponsor](https://foundation.rust-lang.org/)
- [Sponsor](https://aws.amazon.com/)
- [Sponsor](https://www.fastly.com/)
- [Features](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** info@apievangelist.com
**URL:** https://apievangelist.com
