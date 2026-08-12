---
name: heritage-data-viz-workflow
description: Use when turning dense heritage, World Heritage, HIA, observation-report, research-report, or multi-year article corpora into traceable structured data, evidence-led visualisations, and poster-grade outputs such as radial timelines, Sankey/alluvial diagrams, metric summaries, maps, timelines, and publication-ready SVG/PNG/PDF posters.
---

# Heritage Data Viz Workflow

Turn a large heritage corpus into a visual argument.

The workflow is not "make a pretty chart." It is:

**corpus -> classification -> visual question -> evidence graphic -> poster composition**

Use this skill when the source material contains many reports, articles, sessions, sites, countries, years, themes, actors, or keywords and the final output should make a pattern visible without losing traceability to the source.

## First principle

A poster is an argument, not a dashboard.

Before drawing anything, write one sentence answering:

> What relationship, pattern, change, or comparison should the reader understand after looking at this poster?

Everything on the page must support that sentence.

## What this skill solves

Use it to answer questions such as:

- How has attention shifted across years or Committee sessions?
- Which themes dominate a long-running observation series?
- How do themes connect to sessions, host countries, sites, or actors?
- Which categories recur, disappear, or emerge over time?
- What can be compressed into one visual object without turning the poster into a dashboard?
- Which records support each number, segment, or relationship shown?

The minimum useful result is:

1. one traceable dataset;
2. one documented classification spine;
3. one visual question;
4. one dominant visual mechanism;
5. one poster that can be regenerated.

## Workflow

### 1. Intake the corpus

Identify the real source material first: Excel, CSV, Word, PDF, Markdown, web pages, JSON, or images.

Preserve source identifiers whenever available:

- file or article title;
- year/date/session;
- page, sheet, URL, or source ID;
- author/institution when relevant;
- original category labels.

Do not overwrite the source files.

### 2. Build the classification spine

Create only the dimensions needed for the visual question.

Common heritage dimensions include:

- `year` / `session` / `date`;
- `country` / `host_country` / `region` / `site`;
- `theme_code` / `theme_name` / `keywords`;
- `whc_process` such as nomination, monitoring, periodic reporting, assistance, capacity building;
- `actor` such as State Party, Committee, World Heritage Centre, Advisory Body, site manager, community;
- `evidence_status` such as source fact, normalized field, AI suggestion, human-approved label.

For multi-label records, keep arrays rather than forcing one category.

If the project already has a controlled vocabulary, preserve it. Do not silently invent a new taxonomy because it looks cleaner.

### 3. Normalize and audit

Create one canonical data bundle before designing.

Recommended structure:

```json
{
  "meta": {},
  "dimensions": {},
  "records": [],
  "aggregates": {},
  "matrix": {},
  "graph": {"nodes": [], "links": []},
  "diagnostics": {},
  "warnings": []
}
```

Audit:

- total records;
- duplicates;
- missing years/categories;
- unknown codes;
- aggregate totals versus record totals;
- ambiguous classifications;
- source gaps.

AI may suggest labels or anomalies, but inferred categories must remain distinguishable from source facts and human-approved labels.

### 4. Choose one visual mechanism

Choose the form that proves the intended relationship.

#### Radial chronology

Use when the claim is about **time + recurrence + thematic density**.

Good for:

- multi-year observation series;
- session-by-session thematic coverage;
- repeated category bands around a chronological ring.

Keep year/session labels sparse. Use a stable category palette and a visible legend.

#### Sankey / alluvial

Use when the claim is about **relationship or flow between categorical dimensions**.

Examples:

- theme -> host country/year;
- source type -> theme -> output;
- country -> session -> topic.

Band width must encode a real count or weight. Never draw decorative flows that do not map to data.

#### Metric summary poster

Use when the first message is **scale**.

Select 3-5 numbers only, such as years covered, sessions observed, items published, or reports produced. Pair them with one short narrative proposition.

#### Split-field / partial radial poster

Use when one side needs a strong title, call to action, or provenance block and the other side carries a dense circular or temporal visual.

#### Context back / second side

For a two-sided poster or postcard, use the reverse side for:

- short project context;
- linear chronology;
- provenance;
- source/design credits;
- QR or report access.

Do not repeat the front-side data story.

### 5. Compose the poster

A typical poster has five levels:

1. **Series identity** - small, stable metadata.
2. **Main proposition** - the largest textual statement.
3. **Dominant evidence visual** - radial, Sankey, metric field, map, or timeline.
4. **Interpretive support** - legend, 2-4 metrics, one caption, or one note.
5. **Provenance / action** - source, date range, QR/link, credits.

Do not give every block equal visual weight.

The poster should still work as a thumbnail: the reader should identify the proposition and the visual mechanism before reading the small text.

## Visual language

The reference family uses two compatible modes.

### Dark analytical mode

Use for dense quantitative/radial compositions.

- charcoal or ink background;
- off-white primary text;
- a restrained set of semantic category colors;
- thin gray rules;
- large numerals and compact legends;
- bright colors only for data categories or key labels.

### Warm-paper editorial mode

Use for Sankey/alluvial, explanatory, or print-oriented layouts.

- warm paper background;
- ink text;
- muted but distinct category colors;
- subtle borders and rules;
- strong typographic hierarchy;
- generous margins.

### Shared rules

- Let data categories carry color; do not decorate empty space with color.
- Keep category colors stable across all outputs in one project.
- Use typography and position in addition to color; never encode meaning by color alone.
- Prefer thin rules, precise alignment, and one dominant composition.
- Avoid rounded dashboard cards, gradients, heavy shadows, generic AI imagery, and decorative heritage motifs.
- Use QR codes only when they lead to a real public destination.

## Data-to-poster grammar

Use this sequence when the user gives you a large corpus and asks for a poster:

1. **Count** - what is the scale?
2. **Classify** - which dimensions matter?
3. **Relate** - which categories connect?
4. **Compare** - what differs across time/place/theme?
5. **Select** - which one relationship deserves the poster?
6. **Visualise** - choose the visual mechanism.
7. **Compose** - arrange proposition, evidence, metrics, and provenance.
8. **Validate** - check the numbers and the exported page.

Do not skip from raw documents directly to graphic styling.

## Export standard

Prefer deterministic vector-first production:

- SVG for charts, radial systems, Sankey/alluvial, maps, and linework;
- HTML/CSS/SVG when exact typography and repeatable export matter;
- PNG for previews and social/publication delivery;
- PDF for print;
- CSV/JSON for the data behind the poster when public release is appropriate.

For print exports, verify dimensions and inspect at 100% and 200% zoom.

## Evidence and human review boundary

AI can accelerate:

- extraction;
- normalization;
- first-pass classification;
- aggregate calculation;
- chart prototyping;
- layout variants.

Human review begins before publication:

- taxonomy approval;
- ambiguous classification;
- interpretation of trends;
- claims about causality or significance;
- final wording;
- source/credit/privacy review.

Never convert an inferred pattern into a factual claim without checking the supporting records.

## Validation

Before completion:

- verify poster totals against the canonical dataset;
- confirm every visual encoding has a documented meaning;
- confirm category colors are consistent;
- inspect labels for clipping and overlap;
- verify QR/link destinations if used;
- keep source and date range visible;
- inspect both full-size and thumbnail views;
- verify final SVG/PNG/PDF opens and has the expected dimensions;
- state limitations when the source corpus is incomplete.

## Reference poster archetypes

The repository samples demonstrate four reusable archetypes:

1. **Radial chronology** - multi-year theme bands around a circular timeline.
2. **Metric summary** - a few large numbers communicate scale before detail.
3. **Partial radial / split field** - dense circular evidence paired with title and access block.
4. **Sankey / alluvial** - categorical relationships mapped as weighted flows on warm paper.

Treat them as visual grammar, not templates to copy mechanically.

## Failure signals

Revise when:

- the result looks like a generic BI dashboard;
- five different charts compete for attention;
- the poster cannot be understood at thumbnail scale;
- colors are decorative rather than semantic;
- the visual mechanism does not answer a research question;
- totals cannot be traced back to records;
- text is shrunk until it becomes texture;
- the visual is impressive but the relationship being shown is unclear.

The work is complete when the reader can answer three questions quickly:

**What am I looking at? What pattern does it show? What evidence is it based on?**
