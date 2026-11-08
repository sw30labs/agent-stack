# ADR-0002: Model agentic systems as layers 0 through 10

## Status

Accepted, retrospective, inferred 2026-11-08

## Context

Discourse about agents often collapses everything into "the model" or "the prompt." The visualization needs a vertical slice that a systems engineer can walk.

## Decision

Decompose an agentic system into eleven named layers, encoded as first-class graph nodes:

- Layer 0 Substrate
- Layer 1 Model
- Layer 2 Prompt
- Layer 3 Context
- Layer 4 Tools
- Layer 5 Agent loop
- Layer 6 Memory
- Layer 7 Subagents
- Layer 8 Orchestration
- Layer 9 Verification
- Layer 10 Interface

The README groups them as 0–1 substrate and model, 2–3 prompt and context, 4–5 tools and loop, 6–8 memory, agents and orchestration, and 9–10 verification and interface. The document title says "10-layer architecture"; the graph itself numbers Layer 0 through Layer 10 (eleven layers). That numbering mismatch is recorded as assumption A-003.

## Consequences

- Positive: Each concern has a place; later nodes can attach risks and rules per layer (ADR-0010).
- Negative: Readers may count "10 layers" and disagree with a 0–10 numbering.

## Alternatives considered

- A model-centric or prompt-centric diagram (rejected by the README rationale: agents are not magic black boxes).
- Omitting substrate (Layer 0) or interface (Layer 10) (not done; both exist as nodes).

## Evidence

- `README.md` (The Stack)
- `index.html` (nodes `layer0` … `layer10`)
- `8f9a2fad7e6eb707f2bb9797750f2f8b531fa4cc`
- `cc2862dfb9053dbd3b602472dfd88233c79aee84`
