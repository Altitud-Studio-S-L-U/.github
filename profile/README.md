# Altitud Studio

Software engineering studio based in Andorra. We build software, integrations and developer tools, and publish reusable parts of that work as open source.

[Website](https://altitudstudio.ad/en/) · [Projects and engineering cases](https://altitudstudio.ad/en/open-source/) · [Work with us](https://altitudstudio.ad/en/#contact)

## Data libraries

| Project | What it does | Get started |
| --- | --- | --- |
| [ImportKit](https://github.com/Altitud-Studio-S-L-U/importkit) | Streams CSV and JSONL into application-defined destinations, with validation, bounded batches, stable record IDs and checkpoint recovery. | [npm · v1.0.0](https://www.npmjs.com/package/@altitud-studio/importkit/v/1.0.0) · Node.js |
| [wildcsv](https://github.com/Altitud-Studio-S-L-U/wildcsv) | Reads CSV with dialect and encoding detection, configurable limits and adaptive parallel parsing. Uses only the Go standard library. | [Go module · v0.1.0](https://pkg.go.dev/github.com/Altitud-Studio-S-L-U/wildcsv@v0.1.0) |
| [ImportKit WASM](https://github.com/Altitud-Studio-S-L-U/importkit-wasm) | Adds an optional Rust/WebAssembly CSV reader to ImportKit 1.x, preserving valid records and stable IDs. | [Build from source](https://github.com/Altitud-Studio-S-L-U/importkit-wasm#install) · Node.js |

ImportKit's default delivery is at least once: destination idempotency belongs to the application. wildcsv's detection is heuristic and configurable. ImportKit WASM is not published on npm, and error precedence can differ from the standard reader when a file contains multiple errors. Performance results are tied to the documented workloads and environments.

## Developer and browser tools

| Project | What it does | Availability |
| --- | --- | --- |
| [Altimeter](https://github.com/Altitud-Studio-S-L-U/altimeter) | Audits technical SEO with evidence-linked deterministic checks, reports and optional AI analysis. Its score summarises checks, not search rankings. | [CLI · GitHub release v0.1.0](https://github.com/Altitud-Studio-S-L-U/altimeter/releases/tag/v0.1.0) |
| [self-managed-api](https://github.com/Altitud-Studio-S-L-U/self-managed-api) | Compares API contracts, inspects consumers and tests migration recipes locally, with separate approvals for model use, execution and draft PRs to private repositories. | SDK, CLI and local worker · From source |
| [Forge](https://github.com/Altitud-Studio-S-L-U/forge) | Coordinates Codex and Claude Code over selected files: proposal, operator-defined check, independent review and one repair round. Changes remain uncommitted. | CLI · From source |
| [Wallapop Tools](https://github.com/Altitud-Studio-S-L-U/wallapop-tools) | Manages listings through a Chromium extension: reactivation, price changes, scheduling and CSV export. Independent of Wallapop; depends on an unofficial web API. | [Manual installation](https://github.com/Altitud-Studio-S-L-U/wallapop-tools/releases/latest) |

## Compiler research

[**IRVeil**](https://github.com/Altitud-Studio-S-L-U/irveil) is an experimental C++17 library and LLVM 18 plugin for transforming selected integer additions into equivalent boolean and arithmetic expressions. The v0.2 pre-release targets Linux x86-64. Its [LLVM and Ghidra evaluation](https://github.com/Altitud-Studio-S-L-U/irveil/blob/main/docs/re-evaluation.md) documents recoverable algebra and does not establish resistance to reverse engineering.

## Documentation and contributions

Every project above is MIT-licensed. Installation instructions, supported environments and operating limits live in each repository. Start with the README, reproduce the relevant checks and open an issue or pull request with a concrete example.

For security reports, follow the affected repository's `SECURITY.md` or use its private vulnerability reporting channel where available.
