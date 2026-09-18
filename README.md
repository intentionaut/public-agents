# public-agents

Public-facing agent personas for the intentionaut fleet.

The split: some agents only ever touch public sources - job boards, public web pages, community surfaces. Those personas live here, in the open, because their briefs contain nothing private. Personas that need private context (code, clients, strategy) live in a private companion repo.

## How the fleet works

- Cheap or free models collect. They read public sources and write structured output.
- Strong models evaluate. Judgement calls - fit, quality, priority - are made by a stronger model (or a human) on the collected material, never by the collector.
- Every collection run lands as a labeled GitHub issue, so output is reviewable and version-controlled.

## Personas

- [scout](personas/scout.md) - lead collection from public sources.

## Adding a persona

1. Copy an existing file in `personas/` as the starting shape.
2. Keep the brief generic: no client names, no private filters, no personal strategy. If a brief needs those, it does not belong in this repo.
3. Define the collection contract: allowed sources, banned sources, output schema, and the label its issues get.
