# Data-to-Poster Method

A poster should be the last layer of the workflow, not the first.

## Layer 1 — Corpus

Preserve the original material and its provenance.

Examples:

- article indexes;
- session records;
- report tables;
- publication metadata;
- manually maintained research spreadsheets.

Do not overwrite source fields with interpretation.

## Layer 2 — Structured evidence

Create one auditable record per analysis unit.

A useful pattern is:

| id | period | theme | entity | source | classification_status |
| --- | --- | --- | --- | --- | --- |
| 001 | 2025 | List Management | Session 47 | source reference | reviewed |

If a record belongs to multiple themes, choose an explicit method:

- one-to-many rows;
- primary + secondary theme fields; or
- weighted classification.

Do not double-count accidentally.

## Layer 3 — Aggregation

Document every transformation needed for the graphic.

Examples:

- count records by theme;
- count theme × year pairs;
- build source-target-value tables for Sankey;
- compute corpus totals;
- identify years with no observations.

Keep raw and derived tables separate.

## Layer 4 — Visual question

Write the intended claim before styling.

Good:

> The thematic composition of the series changes across sessions, but several themes recur throughout the observation history.

Too vague:

> Show the data beautifully.

Too broad:

> Show everything about the project.

## Layer 5 — Visual encoding

Define mappings explicitly.

Example for Sankey:

```text
left node = theme
right node = session/year
link width = number of observation records
link colour = theme category
```

Example for radial wheel:

```text
angular group = year/session
track = theme
mark = presence or count according to documented rule
colour = theme
```

If the mapping cannot be written clearly, the visual design is not ready.

## Layer 6 — Poster hierarchy

Remove data that is not necessary to understand the primary visual question.

Keep supporting data available in:

- source spreadsheet;
- appendix;
- linked report;
- repository evidence file;
- second explanatory page.

## Layer 7 — Verification

Before publication, compare visual totals against the structured data.

Recommended checks:

- total marks / links reconcile with expected counts;
- category totals reconcile;
- no duplicate records introduced by joins;
- missing values remain distinguishable from zeros;
- labels match the final taxonomy;
- visual title is supported by the data;
- source links and credits are correct.

## Human decision points

Automated workflows can accelerate parsing, grouping, calculation, and rendering, but these decisions remain human-led:

- what counts as one record;
- what taxonomy is meaningful;
- whether categories can overlap;
- what denominator answers the question;
- whether a relationship is meaningful enough to visualise;
- what interpretation is publishable.

The poster is therefore a **verified visual argument**, not an automatic chart dump.
