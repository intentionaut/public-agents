# public-agents

Public-facing agent personas for the intentionaut fleet.

The split: some agents only ever touch public sources - job boards, public web pages, community surfaces. Those personas live here, in the open, because their briefs contain nothing private. Personas that need private context (code, clients, strategy) live in a private companion repo.

## Collect vs evaluate

- Cheap or free models collect. They read public sources and write structured output.
- Strong models evaluate. Judgement calls - fit, quality, priority - are made by a stronger model (or a human) on the collected material, never by the collector.
- Every collection run lands as a labeled GitHub issue, so output is reviewable and version-controlled.

## Layout

- `personas/` - small identity files: who the agent is, its current brief, which skills it uses.
- `skills/` - reusable capability definitions shared across personas: allowed and banned sources, output contracts, filing rules. Personas reference skills; they do not copy them.

## Personas

- [scout](personas/scout.md) - lead collection from public sources, using [lead-collection](skills/lead-collection.md).

## Adding a persona

1. Add a small identity file in `personas/`: name, brief, skills used.
2. Put anything reusable in `skills/` and reference it from the persona.
3. Keep briefs generic: no client names, no private filters, no personal strategy. If a brief needs those, it does not belong in this repo.
