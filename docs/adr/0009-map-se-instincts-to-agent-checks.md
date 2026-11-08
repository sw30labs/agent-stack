# ADR-0009: Map classical software-engineering instincts to agent equivalents

## Status

Accepted, retrospective, inferred 2026-11-08

## Context

The README says one purpose of the map is to reconnect old engineering habits to agent work, rather than implying those habits no longer apply.

## Decision

Encode an `instincts_mapping` cluster in the graph:

- Type safety evolves into schema plus output validation.
- Unit tests evolve into prompt and agent regression tests.
- Observability evolves into prompt, context, and decision logs.
- Code reviews evolve into critic/reviewer agents.

## Consequences

- Positive: Verification (Layer 9) is grounded in familiar controls instead of a purely novel vocabulary.
- Negative: The mappings are metaphors; they do not specify tools or thresholds.

## Alternatives considered

- Leave verification undescribed except as a layer name (rejected; the cluster exists).
- Treat evals as unrelated to classical testing (contradicted by the "evolves into" edges).

## Evidence

- `README.md` (Why I built this, item 3)
- `index.html` (nodes `instincts_mapping`, `type_safety`, `schema_validation`, `unit_tests`, `prompt_regression`, `observability`, `decision_logs`, `code_reviews`, `critic_reviewer`)
- `8f9a2fad7e6eb707f2bb9797750f2f8b531fa4cc`
