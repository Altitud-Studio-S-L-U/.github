```text
                  /\
                 /  \       ALTITUD STUDIO
            /\  / /\ \      Software engineering / Andorra
           /  \/ /  \ \
          /____\/____\_\
```

## Software you can inspect, run and build on

We are a software engineering studio based in Andorra. Our public tools cover data imports, API maintenance, AI-assisted code changes, compiler transformations and browser integrations. Each repository contains the source, operating contracts and instructions to run its checks.

## Choose a tool

| You need to… | Project | Interface |
| --- | --- | --- |
| Validate file records and resume interrupted imports | **[ImportKit](https://github.com/Altitud-Studio-S-L-U/importkit)** | TypeScript library · Node.js |
| Review API changes and test consumer migrations | **[Self-managed API](https://github.com/Altitud-Studio-S-L-U/self-managed-api)** | TypeScript SDK · CLI · local worker |
| Pair a code proposal with verification and a second AI reviewer | **[Forge](https://github.com/Altitud-Studio-S-L-U/forge)** | Node.js CLI · Codex + Claude Code |
| Transform selected arithmetic during native compilation | **[IRVeil](https://github.com/Altitud-Studio-S-L-U/irveil)** | C++ library · LLVM pass plugin |
| Manage listings from a Wallapop browser session | **[Wallapop Tools](https://github.com/Altitud-Studio-S-L-U/wallapop-tools)** | JavaScript · Manifest V3 extension |

## Data and API integrations

### ImportKit

Stream CSV and JSON Lines records through validation, sequential batches and local checkpoints. Batches can be limited by record count and measured bytes. Recovery preserves record IDs so the destination can deduplicate replayed writes; the application supplies its validation and persistence logic.

[Install from npm](https://www.npmjs.com/package/@altitud-studio/importkit) · [Run the recovery example](https://github.com/Altitud-Studio-S-L-U/importkit/blob/main/examples/recovery.mjs) · [API and resource limits](https://github.com/Altitud-Studio-S-L-U/importkit#limits-and-backpressure)

### Self-managed API

Compare OpenAPI, MCP and supported JSON Schema contracts, inspect affected consumers, and validate proposed migrations locally. Model use, test execution and draft PR publication have separate approvals. Available from source as an SDK, CLI and local worker; GitHub publication targets private repositories.

[Start from source](https://github.com/Altitud-Studio-S-L-U/self-managed-api#quick-start) · [Technical guide](https://github.com/Altitud-Studio-S-L-U/self-managed-api/blob/main/docs/technical-guide.pdf)

## Developer workflows

### Forge

Coordinate installed Codex and Claude Code CLIs: one proposes changes to explicitly selected files, an operator-supplied command verifies them, and the other reviews the result. Git preconditions and bounded repair keep the workflow explicit. Changes remain uncommitted for human review.

[Run Forge](https://github.com/Altitud-Studio-S-L-U/forge#run) · [Architecture](https://github.com/Altitud-Studio-S-L-U/forge#architecture) · [Trust model](https://github.com/Altitud-Studio-S-L-U/forge/blob/main/SECURITY.md)

## Compiler engineering

### IRVeil

Replace integer additions in explicitly marked C/C++ functions with equivalent boolean and arithmetic expressions. The LLVM 18 plugin provides deterministic configuration and bounded expansion on Linux x86-64. Its Ghidra and LLVM evaluation records both surviving transformations and recoverable algebra; it does not establish resistance to a skilled analyst.

[Build and integrate](https://github.com/Altitud-Studio-S-L-U/irveil#build) · [Transformation contract](https://github.com/Altitud-Studio-S-L-U/irveil/blob/main/docs/design.md) · [Ghidra and LLVM evaluation](https://github.com/Altitud-Studio-S-L-U/irveil/blob/main/docs/re-evaluation.md)

## Browser integrations

### Wallapop Tools

Reactivate listings, adjust prices, schedule actions and export CSV from an existing browser session. The extension coordinates account checks and sequential writes in its service worker. It is independent of Wallapop and uses the web application's unofficial endpoints; browser integration checks use controlled API fixtures.

[Install the latest release](https://github.com/Altitud-Studio-S-L-U/wallapop-tools/releases/latest) · [Usage and operating limits](https://github.com/Altitud-Studio-S-L-U/wallapop-tools#use) · [Data and privacy](https://github.com/Altitud-Studio-S-L-U/wallapop-tools/blob/main/PRIVACY.md)

## Explore and contribute

The five tools above are MIT licensed. Their repositories contain installation steps, examples and validation commands. This [`.github` repository](https://github.com/Altitud-Studio-S-L-U/.github) maintains the organization profile.

- Discuss changes in the relevant repository and submit a pull request.
- Include a reproducible example with synthetic data and the checks you ran.
- Follow each project's security policy for confidential vulnerability reports.

[Altitud Studio](https://altitudstudio.ad/en/) · [Public repositories](https://github.com/orgs/Altitud-Studio-S-L-U/repositories?type=public) · [Contact the studio](https://altitudstudio.ad/en/#contact)
