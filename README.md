# crates.io

API Evangelist catalog entry for **crates.io** — the official package registry for the Rust programming language.

crates.io is operated by the crates.io team under the Rust Foundation with infrastructure support from Amazon Web Services (file hosting) and Fastly (CDN). The registry is the canonical implementation of the Cargo Registry Web API specification and serves the sparse HTTP index used by every recent version of Cargo. The crates.io codebase is dual-licensed under Apache-2.0 and MIT and is written in Rust (axum + diesel) with a SvelteKit/TypeScript frontend.

## APIs

| API | Description |
| --- | --- |
| [crates.io Web API](openapi/crates-io-web-api-openapi.yml) | Search, fetch crate/version metadata, publish, yank, unyank, and manage owners under `https://crates.io/api/v1`. |
| [crates.io Sparse Index](openapi/crates-io-sparse-index-openapi.yml) | HTTP-served per-crate index and `config.json` at `https://index.crates.io`. Default Cargo registry protocol since Rust 1.70 (June 2023). |

## Artifacts

- **OpenAPI** — [`openapi/`](openapi/)
  - `crates-io-web-api-openapi.yml`
  - `crates-io-sparse-index-openapi.yml`
- **JSON Schema** — [`json-schema/`](json-schema/)
  - `crates-io-crate-schema.json`
  - `crates-io-index-entry-schema.json`
- **JSON Structure** — [`json-structure/`](json-structure/)
  - `crates-io-crate-structure.json`
- **JSON-LD** — [`json-ld/crates-io-context.jsonld`](json-ld/crates-io-context.jsonld)
- **Naftiko capabilities** — [`capabilities/`](capabilities/)
  - `web-api-crates.yaml`
  - `web-api-versions.yaml`
  - `web-api-owners.yaml`
  - `sparse-index.yaml`
- **Examples** — [`examples/`](examples/)
- **Spectral rules** — [`rules/crates-io-rules.yml`](rules/crates-io-rules.yml)
- **Vocabulary** — [`vocabulary/crates-io-vocabulary.yml`](vocabulary/crates-io-vocabulary.yml)

## Key links

- Portal — https://crates.io
- Web API reference — https://doc.rust-lang.org/cargo/reference/registry-web-api.html
- Sparse index reference — https://doc.rust-lang.org/cargo/reference/registry-index.html
- Source — https://github.com/rust-lang/crates.io
- Status — https://status.crates.io
- Contact — help@crates.io / Zulip `#t-crates-io`

## Notes

- crates.io is a public good of the Rust ecosystem — there are no paid plans, so this profile omits `plans/`, `rate-limits/`, and `finops/` artifacts.
- Authentication for mutating Web API operations is a raw token in the `Authorization` header (no `Bearer` prefix), created at https://crates.io/settings/tokens.
- The Trusted Publishing flow exchanges a GitHub Actions OIDC token for a short-lived crates.io publish token via `crates-io-auth-action`.
