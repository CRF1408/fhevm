# Config Files Overview

This document briefly describes common configuration files that may
appear in the FHEVM repository or in downstream projects.

## `.env` / `.env.local`

Used to store environment variables for local development. Typical
entries include:

- RPC endpoints
- API keys
- feature flags

These files **must not** be committed to version control.

## `*.toml` files

TOML files are often used for:

- Rust crate configuration (`Cargo.toml`),
- tool configuration (for example `rustfmt.toml`, `clippy.toml`).

When editing these, keep changes minimal and well-documented.

## `docker-compose.*.yml`

Docker compose files describe how local services (nodes, gateways,
databases) are started. When modifying them:

- avoid hardcoding secrets,
- document non-obvious ports or volumes.

## `*.config.*`

You may encounter additional configuration files for JavaScript or
TypeScript tooling (for example `jest.config.ts`, `tsconfig.json`).
Changes here can affect build and test behavior across the project.

This overview is not exhaustive, but should help new contributors
orient themselves among the most common config files.
