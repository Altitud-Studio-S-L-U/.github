# Altitud Studio

Software engineering studio in Andorra. We build backend and developer tools around one rule: a change that reaches a production system should be bounded, checked against evidence and approved before it has side effects.

## Tools

| Problem | Project | Status |
| --- | --- | --- |
| Resume a large CSV or JSON Lines import after a crash from the last confirmed batch, with record IDs that stay stable across retries | **[ImportKit](https://github.com/Altitud-Studio-S-L-U/importkit)**<br>TypeScript library | 1.0 on [npm](https://www.npmjs.com/package/@altitud-studio/importkit)<br>![npm downloads](https://img.shields.io/npm/dm/@altitud-studio/importkit?label=downloads) |
| Audit a website against search rules that each cite a primary source, then hand every failure to a coding agent with checks that verify the fix | **[Altimeter](https://github.com/Altitud-Studio-S-L-U/altimeter)**<br>Node.js CLI | [0.1](https://github.com/Altitud-Studio-S-L-U/altimeter/releases/latest) with build provenance |
| See which consumer calls an API or MCP contract change affects, and test the migration in Docker before a draft pull request exists | **[Self-managed API](https://github.com/Altitud-Studio-S-L-U/self-managed-api)**<br>SDK, CLI and local worker | [0.1](https://github.com/Altitud-Studio-S-L-U/self-managed-api/releases/latest), from source |
| Let one coding agent propose a change and another review it, while your own command decides whether it passes | **[Forge](https://github.com/Altitud-Studio-S-L-U/forge)**<br>Node.js CLI | [0.1](https://github.com/Altitud-Studio-S-L-U/forge/releases/latest), from source |
| Replace integer additions in marked C and C++ functions with equivalent mixed boolean-arithmetic expressions at compile time | **[IRVeil](https://github.com/Altitud-Studio-S-L-U/irveil)**<br>LLVM 18 pass plugin | [0.2 pre-release](https://github.com/Altitud-Studio-S-L-U/irveil/releases) |

## How the tools are built

- **Explicit limits.** Inputs, batches, context and deadlines have documented bounds. ImportKit [limits](https://github.com/Altitud-Studio-S-L-U/importkit/blob/main/docs/limits.md) the source, each record and each batch; Forge sends at most twelve selected files and 256 KiB of context to a model; IRVeil rewrites at most 256 additions per function by default (`max-adds`), each with at most five extra instructions.
- **Evidence before opinions.** A model's judgement never outranks a check. Altimeter drops any model claim that does not quote the collected evidence word for word; Forge never lets a review override a failed verification command; IRVeil's [evaluation](https://github.com/Altitud-Studio-S-L-U/irveil/blob/main/docs/re-evaluation.md) reports what Ghidra and LLVM still recover.
- **Approval before side effects.** Self-managed API asks separately before it uses a model, runs tests or publishes a draft pull request. Forge never commits, pushes or merges.
- **The same checks everywhere.** In each repository above, every pull request is built, tested and scanned by CodeQL in GitHub Actions. Actions are pinned by commit and kept current by Dependabot, OpenSSF Scorecard publishes the supply-chain checks, and vulnerabilities are reported privately through GitHub.

## Engineering notes

Design documents and measurements, including results that did not go our way:

- **ImportKit** · [Recovery](https://github.com/Altitud-Studio-S-L-U/importkit/blob/main/docs/recovery.md): at-least-once delivery, checkpoints in the same transaction as the records, and a PostgreSQL checkpoint store. [Performance](https://github.com/Altitud-Studio-S-L-U/importkit/blob/main/docs/performance.md): time, reads and memory measured on large files.
- **Altimeter** · [How Altimeter audits a site](https://github.com/Altitud-Studio-S-L-U/altimeter/blob/main/docs/methodology.md): five stages, each recording what it could not evaluate, so a report states how much of the catalog it covered.
- **IRVeil** · [Transformation contract](https://github.com/Altitud-Studio-S-L-U/irveil/blob/main/docs/design.md) and [reverse-engineering evaluation](https://github.com/Altitud-Studio-S-L-U/irveil/blob/main/docs/re-evaluation.md): the expressions survive native code generation and remain algebraically recoverable in Ghidra's output.
- **Forge** · [Architecture](https://github.com/Altitud-Studio-S-L-U/forge#architecture): a bounded state machine with one adapter per provider CLI and no provider SDK in the core.
- **Self-managed API** · [Technical guide](https://github.com/Altitud-Studio-S-L-U/self-managed-api/blob/main/docs/technical-guide.pdf) (Spanish): approvals, Docker validation, native services and signed updates.

## Contribute

Each repository's `CONTRIBUTING.md` lists the checks to run. Open an issue with a reproduction on synthetic data, or a pull request with the results of the checks you ran. Report vulnerabilities privately with **Report a vulnerability** on the repository's Security tab.

[altitudstudio.ad](https://altitudstudio.ad/en/) · [Open source](https://altitudstudio.ad/en/open-source/) · [Contact](https://altitudstudio.ad/en/#contact)
