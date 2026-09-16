# Builtnoble - [Community Health Files](https://help.github.com/en/github/building-a-strong-community/creating-a-default-community-health-file)

Default community health files for the `builtnoble` organization. Any **public** repository that doesn't provide its own copy of a file below automatically inherits this one.

| File | Purpose |
| --- | --- |
| [`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md) | Contributor Covenant v2.1 |
| [`CONTRIBUTING.md`](CONTRIBUTING.md) | Default contributor guide (PHP/Composer-oriented; most repos here are PHP) |
| [`SECURITY.md`](SECURITY.md) | How to privately report a vulnerability |
| [`.github/ISSUE_TEMPLATE/`](.github/ISSUE_TEMPLATE) | Default bug report / feature request forms |
| [`.github/PULL_REQUEST_TEMPLATE.md`](.github/PULL_REQUEST_TEMPLATE.md) | Default PR checklist |

A repo with its own copy of any of these files always uses its own version; this repo only fills gaps.

## Reusable CI workflows

`.github/workflows/` also hosts reusable workflows (`workflow_call`) that other repos can call directly: `php-package-tests.yml`, `php-code-style-lint.yml`, and `github-actions-security-scan.yml`. Current adopters: `currency-fieldtype`, `duration-fieldtype`.

Callers must pin to a commit SHA, not a branch or tag, e.g. `builtnoble/.github/.github/workflows/php-package-tests.yml@<sha>`. This matches the SHA-pinning already used for every third-party action in these repos, and zizmor enforces it - a tag can be moved to point somewhere else later, a commit SHA can't. Bumping a caller to pick up a change made here means updating its pinned SHA by hand.
