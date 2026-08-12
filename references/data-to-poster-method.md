# Data-to-Poster Method

## 1. Start from the evidence ledger

Each record should keep enough provenance to trace a poster mark back to the source.

Minimum fields usually include:

- `id`
- `title`
- `year` or `session`
- `theme_code`
- `source`
- optional country/site/actor fields

## 2. Build only necessary aggregates

Common aggregates:

- count by year;
- count by theme;
- year × theme matrix;
- theme × country matrix;
- theme × session matrix;
- relation links for Sankey/alluvial.

## 3. Write the visual question

Examples:

- Which themes persisted across the whole observation period?
- How did the thematic profile change from one host/session to another?
- What is the scale of the observation series?
- Which categories connect most strongly to which sessions or countries?

Do not choose a chart before writing the question.

## 4. Match question to form

- recurrence over time -> radial chronology or line/heatmap;
- category relationship -> Sankey/alluvial;
- scale -> metric summary;
- geography -> map;
- sequence -> linear timeline;
- one complex visual plus title/access -> split field.

## 5. Reduce

Poster reduction rules:

- one dominant relationship;
- one primary visual mechanism;
- 3-5 metrics maximum;
- one legend;
- one short caption;
- source/date range always visible.

Everything else belongs in the report, website, appendix or reverse side.

## 6. Verify

Before export:

- recalculate totals;
- compare visual totals with source totals;
- check missing categories;
- inspect small text at intended physical size;
- verify links/QR;
- confirm credits and source wording;
- inspect the poster at thumbnail size and at 100% zoom.
