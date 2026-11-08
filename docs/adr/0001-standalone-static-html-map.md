# ADR-0001: Ship the Agent Stack as a standalone static HTML map

## Status

Accepted, retrospective, inferred 2026-11-08

## Context

The repo exists to make a systems mental model for reliable AI agents explorable, not to run agents. A multi-page app, build pipeline, or backend would add moving parts a teaching visualization does not need.

## Decision

Publish one self-contained HTML visualization (`index.html`, originally `mapa_agent_stack.html`) that renders a vis-network graph in the browser. No package manager, tests, CI, or server-side code are part of the tree. README describes cloning the repo and opening the HTML file locally, and says the file is static enough for GitHub Pages, GitLab Pages, or Vercel with zero configuration.

## Consequences

- Positive: Anyone with a browser can open the map; hosting is a static publish.
- Negative: There is no automated check that the graph still matches the README; offline use depends on the CDN (see ADR-0004).

## Alternatives considered

- A packaged JavaScript application with a bundler (no evidence; no `package.json`).
- A slide deck or wiki page only (the README's goal is an interactive map).

## Evidence

- `README.md` (Usage; Deployment)
- `index.html`
- `8f9a2fad7e6eb707f2bb9797750f2f8b531fa4cc` (adds `mapa_agent_stack.html`)
- `cc2862dfb9053dbd3b602472dfd88233c79aee84` (current default branch)
