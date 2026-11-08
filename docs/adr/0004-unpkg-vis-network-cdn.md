# ADR-0004: Load vis-network from the unpkg CDN instead of vendoring it

## Status

Accepted, retrospective, inferred 2026-11-08

## Context

The map needs a graph renderer. Vendoring vis-network would make the HTML work offline and pin a version; a CDN keeps the repo to one file.

## Decision

Load `vis-network` from `https://unpkg.com/vis-network/standalone/umd/vis-network.min.js` and its stylesheet from the same host, with no version pin in the URL. The page toolbar warns that opening the file offline may not render the graph.

## Consequences

- Positive: The repository stays a single HTML file plus docs; first online load just works.
- Negative: Offline use fails; an unpinned CDN URL can change what visitors execute (supply-chain and availability risk). Whether that tradeoff was weighed is not recorded (A-004).

## Alternatives considered

- Vendor vis-network next to `index.html` (no evidence).
- Pin a concrete unpkg version in the URL (not done).

## Evidence

- `index.html` (script and stylesheet tags; toolbar `.warning`)
- `8f9a2fad7e6eb707f2bb9797750f2f8b531fa4cc`
- `6f05e810c47721bd0bf0733ba15169aabeb01e0b`
