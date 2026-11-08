# ADR-0005: Rename the map to `index.html` and host it from the GitHub Pages root

## Status

Accepted, retrospective, inferred 2026-11-08

## Context

The first visualization file was `mapa_agent_stack.html`. GitHub Pages serving `/` on `main` will not treat that name as the site homepage.

## Decision

Rename `mapa_agent_stack.html` to `index.html` so a root Pages site can serve the map at `/`. GitHub Pages is enabled on `main` with source path `/` and publishes at `https://sw30labs.github.io/agent-stack/`. The README still documents the old filename and an older `ai-agents-cybersecurity.github.io` demo URL; those drifts are assumptions A-001 and A-002, not separate decisions.

## Consequences

- Positive: The live site URL is a clean root path.
- Negative: README usage instructions are stale relative to the tree; adding a `docs/` directory later is also published by Pages because the source is the repo root (see the assumptions register). That publish is not a site-breaking deploy, but ADR markdown would become public URLs under `/docs/`.

## Alternatives considered

- Keep `mapa_agent_stack.html` and set Pages to a project subpath (not done; the rename commit is a pure mv).
- Use a `/docs` Pages source (not configured; Pages source is `/`).

## Evidence

- `84e7e063a66db47e7a5c5402b24c04d5b9061bdd` (`mapa_agent_stack.html => index.html`)
- `index.html`
- `README.md` (still names `mapa_agent_stack.html`)
- GitHub Pages API: `source.branch=main`, `source.path=/`, `html_url=https://sw30labs.github.io/agent-stack/`
