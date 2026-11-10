# Altitud Studio organization defaults

This repository holds the organization profile and the defaults shared by Altitud Studio's public repositories. Tool source code, installation instructions and release assets belong to their own repositories.

| Path | Purpose |
| --- | --- |
| [profile/README.md](profile/README.md) | The organization profile shown on GitHub. |
| [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) | Contributor Covenant 2.0, used by every public repository without its own. |
| [.github/ISSUE_TEMPLATE](.github/ISSUE_TEMPLATE) | Bug report and feature request forms for repositories without their own. |
| [.github/pull_request_template.md](.github/pull_request_template.md) | Pull request template for repositories without their own. |
| [workflow-templates](workflow-templates) | The CI, CodeQL and Scorecard workflows the public repositories follow, offered under **Actions → New workflow**. |

## Workflow standard

Each public repository carries its own copy of these workflows rather than calling a shared reusable workflow. The Scorecard API checks the workflow that publishes results against [strict rules](https://github.com/ossf/scorecard-action#workflow-restrictions), and a copy keeps each repository's checks reviewable in its own history, so a change here never alters another repository's CI unannounced. The copies follow the same rules:

- Every action is pinned to a commit SHA, and Dependabot proposes updates weekly.
- Workflows start from a read-only token; a job is granted `security-events: write` or `id-token: write` only where it uploads results.
- Checkouts do not persist credentials.
- Repositories that run workflows allow only GitHub-owned actions and `ossf/scorecard-action`.
- CI runs on every pull request and on `main`. Releases are published by the maintainer, except where a repository documents a provenance-attested release workflow.
