# Contributing

Thanks for your interest in contributing!

This is a default `CONTRIBUTING.md`, used automatically by any Builtnoble repository that doesn't provide its own. Most repositories here are PHP packages built on Composer, so the steps below reflect that common path. If the repo you're contributing to has its own `CONTRIBUTING.md`, follow that one instead; it takes precedence.

## Prerequisites

- PHP 8.3+
- Composer
- Node and npm, if the project has a JavaScript/frontend component

## Getting started

```bash
git clone git@github.com:builtnoble/<repo>.git
cd <repo>
composer install
```

If the project has a `package.json`, also run `npm install`.

## Running the test suite

```bash
composer test
```

## Code style and static analysis

Most repositories use [Pint](https://laravel.com/docs/pint) for code style and [PHPStan](https://phpstan.org/) for static analysis:

```bash
composer lint       # Pint, check only
composer format     # Pint, auto-fix
composer analyse    # PHPStan
```

Check the repo's own `composer.json` scripts section for the exact commands available; they may differ slightly from project to project.

## Branching and PR workflow

- Branch off the repository's default branch, using `feature/`, `fix/`, or `hotfix/` prefixes where practical.
- Open pull requests against the default branch unless the repo's README says otherwise.
- Keep PRs focused on a single change; large unrelated changes are harder to review and merge.

## Commit messages

Use [Conventional Commits](https://www.conventionalcommits.org/) style prefixes (`feat:`, `fix:`, `chore:`, `refactor:`, `docs:`, `test:`) where practical; it keeps history and changelogs readable.

## Reporting bugs and security issues

Use the issue templates for bug reports and feature requests. For security vulnerabilities, do **not** open a public issue - see [SECURITY.md](SECURITY.md).
