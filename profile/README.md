```text
                  /\
                 /  \       ALTITUD STUDIO
            /\  / /\ \      Software engineering / Andorra
           /  \/ /  \ \
          /____\/____\_\
```

We build software, connect systems, and make the behavior of those systems easier to inspect.

Our open-source projects document their contracts, failure behavior, and limits. The code and executable examples are part of the explanation.

## Backend engineering

| Project | What it does | Start here |
| --- | --- | --- |
| **[ImportKit](https://github.com/Altitud-Studio-S-L-U/importkit)** | A TypeScript library for CSV and JSON Lines imports, bounded preflight validation, sequential batches limited by record count and measured bytes, checkpoints, and recovery with stable record IDs. The application owns validation rules and idempotent destination writes. | [API and recovery example](https://github.com/Altitud-Studio-S-L-U/importkit#readme) |
| **[Self-managed API](https://github.com/Altitud-Studio-S-L-U/self-managed-api)** | Inspect API and MCP contract changes, review their effect on consumers, and validate proposed migrations locally. Model use, test execution and draft PR publication to private destinations require separate approvals. | [Setup and operating boundaries](https://github.com/Altitud-Studio-S-L-U/self-managed-api#readme) |

## Compiler tooling

| Project | What it does | Start here |
| --- | --- | --- |
| **[IRVeil](https://github.com/Altitud-Studio-S-L-U/irveil)** | An experimental C++17 library and LLVM pass plugin for replacing selected integer additions with equivalent boolean and arithmetic expressions. Selection is explicit, expansion is bounded and configuration is deterministic. Initial support is Linux x86-64 and LLVM/Clang 18; reverse-engineering resistance is not quantified, and code generation can simplify the transformations. | [Design contract and limits](https://github.com/Altitud-Studio-S-L-U/irveil/blob/main/docs/design.md) |

## Browser integration

**[Wallapop Tools](https://github.com/Altitud-Studio-S-L-U/wallapop-tools)** is a Manifest V3 extension for listing actions, price changes, scheduling, and CSV export. It demonstrates session handling, asynchronous operations, and provider integration. It is independent of Wallapop and relies on the web application's endpoints; the [README](https://github.com/Altitud-Studio-S-L-U/wallapop-tools#readme) describes the operational limits.

## Explore or contribute

- Run the examples and checks documented in each repository.
- Use synthetic data in bug reports. Keep credentials and customer files out of public issues.
- Propose changes through pull requests; the maintainer controls integration into protected branches.
- Read each project's license and security guidance before embedding it.

[Altitud Studio](https://altitudstudio.ad/en/) · [Open-source repositories](https://github.com/orgs/Altitud-Studio-S-L-U/repositories) · [Contact the studio](https://altitudstudio.ad/en/#contact)
