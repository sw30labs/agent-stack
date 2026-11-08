# ADR-0010: Attach operating rules and risks to each layer in the graph

## Status

Accepted, retrospective, inferred 2026-11-08

## Context

Layer names alone do not tell a builder what to do or what usually goes wrong. The product of this repo is the didactic graph, so those statements live in nodes rather than a separate spec.

## Decision

Give each layer attached concept nodes. The graph states, among other rules:

- Model: never trust directly.
- Prompt: treat prompts as code; risk prompt drift and authority leakage.
- Context: working memory; poisoning, eviction, and order sensitivity; too much context can degrade.
- Tools: determinism anchors; prefer tools for deterministic tasks; risk tool hallucination.
- Agent loop: observe → decide → act → update; the loop defines an agent.
- Memory: state persistence; write-only memory is a liability; audit and prune.
- Subagents: role decomposition that enables cross-checking; typically 2–4 agents.
- Orchestration: a graph, not a chain; retry and escalation; planner → executor → checker.
- Verification: external checks, including schema validation and human-in-the-loop.
- Interface: friction reduction via IDE plugins, commands, MCP, and LSP.
- Substrate: remains unchanged; agents are guests.

These labels are the recorded operating guidance. They are not implemented as runtime checks in this repository.

## Consequences

- Positive: The mental model is specific enough to argue with or extend (README invites PRs if a layer is missing).
- Negative: Numeric notes such as "usually 2–4 agents" are unexplained; see A-005.

## Alternatives considered

- Keep only layer titles (rejected; each layer has metaphor/risk/rule children).
- Write a long-form specification instead of graph labels (not present beyond README summaries).

## Evidence

- `index.html` (per-layer child nodes and edges listed above)
- `README.md` (The Stack grouping)
- `8f9a2fad7e6eb707f2bb9797750f2f8b531fa4cc`
