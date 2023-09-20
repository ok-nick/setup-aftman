# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.4.2] - 2023-09-20
## Changed
- Disable caching by default #15

## Fixed
- Issue causing executables to not be found #14

## [0.4.1] - 2023-09-18
## Fixed
- Cache `~/.aftman/tool-storage` as well
- Only hash `aftman.toml` instead of entire directory

## [0.4.0] - 2023-09-17
## Added
- Add `cache` parameter and cache by default

## [0.3.0] - 2022-09-27
## Added
- Create `auth.toml` file with input GitHub token.

## Changed
- Cleanup installation artifacts.

## [0.2.0] - 2022-08-30
## Fixed
- PowerShell on Windows not recognizing executables.

## Removed
- Deprecate `trust-check` and `trusts` inputs as they have no use.

## [0.1.0] - 2022-07-18
### Added
- Everything

[Unreleased]: https://github.com/ok-nick/setup-aftman/compare/v0.4.2...HEAD
[0.4.2]: https://github.com/ok-nick/setup-aftman/releases/tag/v0.4.2
[0.4.1]: https://github.com/ok-nick/setup-aftman/releases/tag/v0.4.1
[0.4.0]: https://github.com/ok-nick/setup-aftman/releases/tag/v0.4.0
[0.3.0]: https://github.com/ok-nick/setup-aftman/releases/tag/v0.3.0
[0.2.0]: https://github.com/ok-nick/setup-aftman/releases/tag/v0.2.0
[0.1.0]: https://github.com/ok-nick/setup-aftman/releases/tag/v0.1.0
