# Changelog

All the project changes should be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

Do not edit the NEW_VERSION and VERSION_DATE fields, they will be updated automatically by the Github Action script.

## [<NEW_VERSION>] - <VERSION_DATE>
### Added
### Changed
### Fixed

## [1.0.4] - 2026-07-08 (by @slazak)
### Changed
- Init payload preview console logs only when debug mode is enabled; undefined or empty user values are omitted from the init payload

## [1.0.3] - 2026-07-08 (by @slazak)
### Added
- GTM preview logs the resolved init payload to the console when the configuration tag fires successfully

## [1.0.2] - 2026-07-08 (by @slazak)
### Changed
- User data field layout and labels: format dropdowns above value fields, renamed plain/pre-hashed options, and per-field optional guidance in help text

## [1.0.1] - 2026-07-03 (by @slazak)
### Changed
- Recommended setup guidance uses Initialization — All Pages trigger

## [1.0.0] - 2026-07-03 (by @slazak)
### Added
- Optional user data on oaiq init (email, external ID, country, city, ZIP) with plain or pre-hashed SHA-256 input for hash fields

## [0.2.0] - 2026-07-02 (by @slazak)
### Changed
- Renamed template display name from OpenAI GPT Ads Configuration to OpenAI ChatGPT Ads Configuration

## [0.1.3] - 2026-07-02 (by @slazak)
### Fixed
- `LICENSE` file aligned with Apache 2.0 gallery format (full APPENDIX and copyright block)

## [0.1.2] - 2026-07-01 (by @slazak)
### Fixed
- Release workflow updates `metadata.yaml` sha only when `template.tpl` changed
- GitHub repo URLs point to [gtm-openai-gpt-ads-config](https://github.com/backona/gtm-openai-gpt-ads-config)

## [0.1.1] - 2026-07-01 (by @slazak)
### Added
### Changed
### Fixed

## [0.1.0] - 2026-07-01 (by @slazak)
### Added
- OpenAI GPT Ads Configuration GTM template to initialize the OpenAI Ads Measurement Pixel (oaiq)
- In-tag guidance for recommended trigger, Consent Mode v2 tag settings, and CSP
- Info-level console message when debug mode is enabled (with Verbose hint for SDK logs)
