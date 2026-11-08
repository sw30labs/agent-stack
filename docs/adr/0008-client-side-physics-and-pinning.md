# ADR-0008: Use a force-directed layout with drag-to-pin and double-click to release

## Status

Accepted, retrospective, inferred 2026-11-08

## Context

A 50-plus-node concept graph is unreadable as a static picture. Readers need to rearrange clusters while exploring.

## Decision

Initialize vis.Network with the `forceAtlas2Based` physics solver and enable hover tooltips, multiselect, navigation buttons, and keyboard interaction. On `dragEnd`, fix the dragged node's x/y. On `doubleClick`, release that node back to physics. The toolbar text documents this: drag to organize, double-click to release, zoom to explore.

## Consequences

- Positive: A reader can pin a local view of one layer without a saved layout file.
- Negative: There is no authored canonical layout; first load is a physics stabilization (150 iterations) and can look different across sessions.

## Alternatives considered

- A hand-placed static diagram (not done; physics is enabled).
- Persist positions in localStorage (no evidence of persistence).

## Evidence

- `index.html` (toolbar copy; `options.physics`; `dragEnd` and `doubleClick` handlers)
- `README.md` ("Drag nodes to rearrange the view; they will lock in place (physics enabled).")
- `8f9a2fad7e6eb707f2bb9797750f2f8b531fa4cc`
- `6f05e810c47721bd0bf0733ba15169aabeb01e0b`
