# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added

### Fixed

### Changed

### Removed

## [v0.4.0] - 2023-04-09

### Added

- New Secret generation and env variable reference template (#6)

## [v0.3.0] - BREAKING - 2023-04-09

### Changed

- IngressRoute values template implementation for rules matching (#5)
  - Far more robust and includes all available rules-based matching

## [v0.2.1] - 2023-04-08

### Fixed

- Reference to cache enabling flag (#4)

## [v0.2.0] - 2023-04-08

### Fixed

- Populated value for `MONGO_DATABASE` env variable in primary application deployment template ([59494f7](https://github.com/lockerstock/helm-charts/commit/59494f79872e6f37948587ba8de47b9223c5fb0b))

## [v0.1.0] - Initial Creation - 2023-04-06

### Added

- Auth0 External Secret template (#1)
- Redis Cache Deployment and Service templates (#1)
- MongoDB External Secret template (#1)
- Primary Application Deployment, Service, HPA, and IngressRoute templates (#1)
