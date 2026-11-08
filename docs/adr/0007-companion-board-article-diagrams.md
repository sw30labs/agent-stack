# ADR-0007: Keep board-facing security analogies in a companion Markdown file

## Status

Accepted, retrospective, inferred 2026-11-08

## Context

The interactive map teaches the internal agent stack. A later article, "How do I explain AI agent security to my board," needed governance analogies that are not the same 0–10 layer model.

## Decision

Add `ai-agent-security-article-diagrams.md` as a separate document with two Mermaid flowcharts that tell the same seven-stage governance story through different analogies:

1. Manufacture and supply chain
2. Certification and identity (FAA / KYC → non-human identities)
3. Restricted access / vault
4. Regulations and policies (bias, drift, reliability, trust and safety, HAP, IP)
5. Pre-flight inspections or stress tests → agent evals
6. ATC or fraud monitoring → AI gateway and observability, with pre-check, human escalation, and post-check
7. Emergency systems / account freeze → circuit breakers

Do not fold those diagrams into `index.html`. The map remains the stack; the Markdown file remains the board narrative.

## Consequences

- Positive: Each audience has a dedicated artifact; changing one analogy does not require editing the vis-network dataset.
- Negative: The two stories can drift from each other and from the 0–10 stack; there is no cross-link in the README.

## Alternatives considered

- Add the analogies as additional nodes in the interactive map (not done; they landed in a new Markdown file).
- Publish only one analogy (both aviation and banking were included).

## Evidence

- `ai-agent-security-article-diagrams.md`
- `cc2862dfb9053dbd3b602472dfd88233c79aee84` (commit subject names the article)
