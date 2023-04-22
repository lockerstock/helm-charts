# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added

### Fixed

### Changed

### Removed

## [v0.5.2] - 2023-04-21

### Removed

- `kube-external-sync.io/top-level-domain` annotation from ingressroute.yaml template ([#13](https://github.com/lockerstock/helm-charts/pull/13))

## [v0.5.1] - 2023-04-21

### Fixed

- OpenTelemetry Gateway Service Address ([#10](https://github.com/lockerstock/helm-charts/pull/10))

## [v0.5.0] - BREAKING - 2023-04-16

> Must be deployed in tandem with [terraform-mongodb-database_user@0.2.0](https://github.com/lockerstock/terraform-mongodb-database_user/releases/tag/v0.2.0).

### Fixed

- Auth0 External Secret Key References ([#9](https://github.com/lockerstock/helm-charts/pull/9))

### Removed

- Unused MongoDB External Secret Key and primary application deployment env variables ([#9](https://github.com/lockerstock/helm-charts/pull/9))

## [v0.4.1] - 2023-04-16

> Must be deployed in tandem with [terraform-mongodb-database_user@0.2.0-pre1](https://github.com/lockerstock/terraform-mongodb-database_user/releases/tag/v0.2.0-pre1).

### Added

- MongoDB External Secret references for `db_password` and `server_domain` ([#8](https://github.com/lockerstock/helm-charts/pull/8))
- MongoDB env variables populated into primary application deployment template ([#8](https://github.com/lockerstock/helm-charts/pull/8))

### Changed

- Auth0 External Secret references to GCP Secret Manager ([#8](https://github.com/lockerstock/helm-charts/pull/8))
- Auth0 env variables populated into primary application deployment template ([#8](https://github.com/lockerstock/helm-charts/pull/8))

## [v0.4.0] - 2023-04-09

### Added

- New Secret generation and env variable reference template ([#6](https://github.com/lockerstock/helm-charts/pull/6))

## [v0.3.0] - BREAKING - 2023-04-09

### Changed

- IngressRoute values template implementation for rules matching ([#5](https://github.com/lockerstock/helm-charts/pull/5))

## [v0.2.1] - 2023-04-08

### Fixed

- Reference to cache enabling flag ([#4](https://github.com/lockerstock/helm-charts/pull/4))

## [v0.2.0] - 2023-04-08

### Fixed

- Populated value for `MONGO_DATABASE` env variable in primary application deployment template ([59494f7](https://github.com/lockerstock/helm-charts/commit/59494f79872e6f37948587ba8de47b9223c5fb0b))

## [v0.1.0] - Initial Creation - 2023-04-06

### Added

- Auth0 External Secret template ([#1](https://github.com/lockerstock/helm-charts/pull/1))
- Redis Cache Deployment and Service templates ([#1](https://github.com/lockerstock/helm-charts/pull/1))
- MongoDB External Secret template ([#1](https://github.com/lockerstock/helm-charts/pull/1))
- Primary Application Deployment, Service, HPA, and IngressRoute templates ([#1](https://github.com/lockerstock/helm-charts/pull/1))
