# crates.io (crates-io)

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
