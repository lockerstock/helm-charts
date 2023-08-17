# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added

### Changed

### Deprecated

### Removed

### Fixed

### Security

## [v0.7.2] - 2023-08-16

### Added

- Conditional logic to add required OpenTelemetry environment variables based on deployment environment (https://github.com/lockerstock/helm-charts/pull/23).

## [v0.7.1] - 2023-07-28

### Fixed

- Fixed broken IngressRoute Rule generation (https://github.com/lockerstock/helm-charts/pull/22).

## [v0.7.0] - 2023-07-28

### Added

- `.Values.deployment.routing` object that controls how network routing is performed. The default and only supported value for `strategy` is `loadbalancer` which expects services to direct requests with custom `Host` header at the Traefik LoadBalancer and allow it to use configured IngressRoutes to route the request. (https://github.com/lockerstock/helm-charts/pull/21).
  - The `loadbalancer` strategy appends the `LOAD_BALANCER_ADDRESS` environment variable to the deployment which can be used to make internal requests to.

### Changed

- The `.Values.ingressRoute.rules` array will now create a separate `Rule` in the final IngressRoute for each index (https://github.com/lockerstock/helm-charts/pull/21).
- Moved `.Values.ingressRoute.middlewares` to be part of `.Values.ingressRoute.rules` objects which plays better with the above change (https://github.com/lockerstock/helm-charts/pull/21).

## [v0.6.0] - 2023-05-12

### Changed

- `deployment.config.enabled` default value to `false` (https://github.com/lockerstock/helm-charts/pull/20)

## [v0.5.6] - 2023-05-07

### Added

- `deployment.config.enabled` field defaulted to `true` to allow disabling of the config block being added as environment variables to the deployment. ([#19](https://github.com/lockerstock/helm-charts/pull/19))
  - This field be updated to default as `false` once all Go microservices have migrated to explicitly setting it to `true`.

## [v0.5.5] - 2023-05-06

### Fixed

- Population of liveness/readiness probes into deployment.yaml when not provided. ([#18](https://github.com/lockerstock/helm-charts/pull/18))

## [v0.5.4] - 2023-05-04

### Fixed

- Base deployment container tag so unchanged releases can be installed (`nginx:staging` -> `nginx:latest`). ([#17](https://github.com/lockerstock/helm-charts/pull/17))

## [v0.5.3] - 2023-04-20

### Added

- `Chart.yaml` configuration information. ([#14](https://github.com/lockerstock/helm-charts/pull/14))

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
