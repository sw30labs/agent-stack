# ADR-0003: Reframe the LLM as a fallible component inside deterministic control

## Status

Accepted, retrospective, inferred 2026-11-08

## Context

A common story treats the LLM as the agent's brain. That hides the rest of the stack and invites placing trust in a stochastic component.

## Decision

The README's core reframe: the LLM is a "fallible junior colleague" or "component" within a larger deterministic system, not a brain. The graph encodes this as `core_reframe`, `model_metaphor` ("Fallible junior colleague / ∞ speed, 0 memory"), `model_risk` ("Non-deterministic & confidently wrong"), `model_rule` ("Never trust directly"), and `deterministic_control` ("Deterministic control architecture").

Deterministic control selectively invokes the model, constrains context, grounds work with tools, decomposes into subagents, verifies externally, and persists auditable memory.

## Consequences

- Positive: Design attention moves to control, tools, verification, and memory hygiene.
- Negative: The map is opinionated; teams that do treat the model as the system will find the framing confrontational.

## Alternatives considered

- Model-as-brain diagrams (explicitly rejected by the README "Why I built this" section).
- Prompt-engineering-only guidance (also rejected there).

## Evidence

- `README.md` (Why I built this)
- `index.html` (nodes `core_reframe`, `model_metaphor`, `model_risk`, `model_rule`, `deterministic_control` and their edges)
- `8f9a2fad7e6eb707f2bb9797750f2f8b531fa4cc`
- `d3fed63518b06694e12daf7e0f07f3fa8ded9643`
