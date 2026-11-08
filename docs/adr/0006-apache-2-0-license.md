# ADR-0006: License the repository under Apache License 2.0

## Status

Accepted, retrospective, inferred 2026-11-08

## Context

The repo was initialized with a license file before the map or README existed. No other license statement appears in the HTML or diagrams.

## Decision

Apply the Apache License, Version 2.0, as `LICENSE`. The initial commit added only that file.

## Consequences

- Positive: Reuse, including the interactive map and later article diagrams, has an explicit OSS license.
- Negative: The README does not point at `LICENSE`, so some visitors may miss it.

## Alternatives considered

- No license / all rights reserved (contradicted by the first commit).
- A different OSI license (no evidence another was considered).

## Evidence

- `LICENSE`
- `6a668b1ab61a3a114a930e3558b12d4cc7286609`
