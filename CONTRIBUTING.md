# Contributing to pombola

Pombola stores and presents information about public figures, particularly politicians. Useful contributions include application fixes, country-specific support, accessible presentation, reproducible tests and documentation.

## Before you start

Read [README.md](README.md), [the system overview](docs/OVERVIEW.md), [installation instructions](docs/INSTALL.md) and [testing instructions](docs/TESTING.md). Search existing issues and pull requests before proposing substantial work. Identify the affected country application and distinguish generic changes from country-specific rules.

For bugs, provide the affected version or commit, environment, minimal reproduction, expected result and observed result. For a substantial proposal, describe the use case and compatibility impact before expanding implementation scope. Use existing issue templates when offered.

## Development and validation

Use the dependency and service setup in the installation guide. Keep development databases isolated from operational systems and use sanitized fixtures. The established complete test command is:

```sh
./run-tests
```

The testing guide also documents targeted tests and country-specific settings. For example, the existing South Africa suite is:

```sh
./manage.py test --settings='pombola.settings.tests_south_africa'
```

Choose the smallest affected tests while editing and retain the full applicable integration checks. Do not reuse a test database across incompatible country settings without following the guide's database instructions.

Add regression coverage for changed behaviour and update documentation or styling notes when interfaces change. Explain migration impacts and any untested countries. Preserve the licensing and attribution of upstream code and assets; the existing project terms continue to apply.

## Pull requests

Create a focused branch from the current `master` branch and submit a pull request to this repository. Link the relevant issue or existing project task, explain the resulting behaviour, and update affected examples and documentation. Keep unrelated changes in separate pull requests.

Report executed commands, outcomes and the commit they validate. Identify unavailable checks and remaining limitations explicitly. Follow the repository's existing review and automated-check requirements; retain required gates and current ownership. Address findings and verify the final head before integration. Repository changes do not themselves authorise a release or external operational action.

## Security, rights and conduct

Follow the [security policy](https://github.com/edithatogo/.github/blob/main/SECURITY.md). Use private vulnerability reporting if available; otherwise request a private contact without publishing vulnerability details. Keep credentials, personal information and restricted source material out of issues, fixtures, logs and artifacts.

Read the [existing licence](LICENSE.txt) and preserve attribution and third-party terms. Follow the [code of conduct](https://github.com/edithatogo/.github/blob/main/CODE_OF_CONDUCT.md) and keep technical discussions respectful.

## Basis for this guide

This guide follows [GitHub's contribution-guideline guidance](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/setting-guidelines-for-repository-contributors) and the contribution-process and testing principles in [OpenSSF Best Practices](https://www.bestpractices.dev/en/criteria). It does not assert certification.
