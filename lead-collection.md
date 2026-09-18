# lead-collection

Reusable skill for personas that collect leads from public sources. A persona owns its brief (target + filters); this skill owns how a collection run works.

## Division of labour

- A cheap or free model collects. Volume and structure are its job.
- A stronger model evaluates. Scoring, fit and prioritisation happen downstream on the collected material, by a model with better judgement or by a human.
- The collector never ranks, scores, or filters by opinion. Unsure whether something fits? Include it with `confidence: low`. Dropping a real lead is worse than handing the evaluator noise.

## Sources

Allowed:

- Public job boards and careers pages
- Public web pages: company sites, portfolios, conference speaker lists
- Public community surfaces: web-indexed forum posts, public newsletters, public event listings

Banned, always:

- Logged-in scraping of any kind. If a page needs an account to view, it is out of scope.
- LinkedIn scraping, logged-in or otherwise
- Paywalled or access-controlled content
- Harvesting personal emails or phone numbers from pages

## Output contract

Each run files ONE GitHub issue with the persona's collection label (scout uses `scout-collection`) containing a table:

| name | company | why-they-fit | source link | confidence |
|------|---------|--------------|-------------|------------|

- `why-they-fit`: one line tied to the persona's brief filters
- `source link`: the exact public URL the lead was seen on. No link, no lead.
- `confidence`: high / low, whether the source actually says what the row claims

## Rules

- Cite or cut: every lead carries a working public source link.
- No fabrication: if the page does not say it, do not write it.
- Note the collection date and brief version at the top of each issue.
- Duplicates across runs are fine; the evaluator dedupes.
