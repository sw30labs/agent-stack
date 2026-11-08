# Architecture Decision Records

Retrospective ADRs for agent-stack, written 2026-11-08 from default branch `cc2862d` after a full read of every tracked file (LICENSE, README.md, index.html, ai-agent-security-article-diagrams.md). Format: PorterForcesAI ADR format. Open questions are in [../assumptions.md](../assumptions.md).

| ADR | Title |
|---|---|
| [0001](0001-standalone-static-html-map.md) | Ship the Agent Stack as a standalone static HTML map |
| [0002](0002-eleven-named-layers.md) | Model agentic systems as layers 0 through 10 |
| [0003](0003-llm-as-fallible-component.md) | Reframe the LLM as a fallible component inside deterministic control |
| [0004](0004-unpkg-vis-network-cdn.md) | Load vis-network from the unpkg CDN instead of vendoring it |
| [0005](0005-index-html-root-pages.md) | Rename the map to index.html and host it from the GitHub Pages root |
| [0006](0006-apache-2-0-license.md) | License the repository under Apache License 2.0 |
| [0007](0007-companion-board-article-diagrams.md) | Keep board-facing security analogies in a companion Markdown file |
| [0008](0008-client-side-physics-and-pinning.md) | Use a force-directed layout with drag-to-pin and double-click to release |
| [0009](0009-map-se-instincts-to-agent-checks.md) | Map classical software-engineering instincts to agent equivalents |
| [0010](0010-per-layer-risks-and-operating-rules.md) | Attach operating rules and risks to each layer in the graph |
