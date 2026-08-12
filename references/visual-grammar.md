# Visual Grammar Reference

This reference translates the Observation Report poster family into reusable data-visualisation decisions. It describes **when a visual form is appropriate**, not a requirement to reproduce one fixed style.

## 1. Radial theme wheel

### Use when

The dataset has two strong dimensions:

- repeated cycles such as year / session / edition; and
- categories that recur within each cycle.

A radial wheel can compress a long chronological series into one field while preserving periodic structure.

### Recommended mapping

- ring or angular position → period / session;
- colour → stable thematic category;
- segment length / count → defined quantity only when the dataset supports it;
- labels → selected years or periods, not every possible annotation;
- centre → optional summary or CTA, never required.

### Do not use when

- exact year-to-year magnitude comparison is the main task;
- there are too many indistinguishable categories;
- the user cannot explain what radial position or segment length means.

In those cases, a linear timeline or bar comparison is usually clearer.

---

## 2. Metric summary poster

### Use when

The story is scale and continuity rather than complex relationships.

A strong metric poster may need only four figures if they establish:

- time span;
- number of cycles / sessions;
- number of records / articles;
- number of published outputs.

### Rules

- every number needs a unit;
- every number needs an implicit or explicit time boundary;
- do not make derived numbers look source-native;
- avoid unrelated vanity metrics;
- preserve room for one title, one source line, and one action entry if needed.

---

## 3. Relationship flow (Sankey / alluvial)

### Use when

The question concerns how records connect two categorical dimensions, such as:

- theme ↔ year;
- theme ↔ session;
- theme ↔ host context;
- theme ↔ output type.

### Data requirement

Each link must be reproducible from an evidence table.

A minimal link table may look like:

```text
source_category,target_category,value
List Management,2013,4
List Management,2015,6
State of Conservation,2015,3
...
```

### Visual rules

- link width = real count or weight;
- node size = explicit count if encoded;
- stable category colours;
- order categories intentionally to reduce crossings;
- label both sides clearly;
- keep low-value links visible but subdued if they are analytically necessary;
- do not create links only to make the field look dense.

---

## 4. Timeline

### Use when

The evidence is sequence:

- project continuity;
- milestones;
- repeated committee sessions;
- publication years;
- gaps or pauses.

### Visual rules

- time spacing should be proportional when chronology is the point;
- milestone labels should be short;
- avoid decorative nodes with no data meaning;
- show missing years as gaps rather than compressing them away when the gaps matter.

---

## 5. Hybrid poster composition

A data poster may combine one major visualisation with small supporting evidence.

Recommended hierarchy:

```text
TITLE / PRIMARY CLAIM

PRIMARY EVIDENCE VISUAL

LEGEND / READING KEY

1–4 SUPPORTING METRICS OR A SMALL TIMELINE

SOURCE / PROVENANCE / OPTIONAL CTA
```

The supporting metrics must not compete with the primary evidence graphic.

---

## 6. Surface modes

### Ink field

Use for high-density, exhibition-like visualisations.

Suggested roles:

- background: charcoal / near-black;
- primary text: warm white;
- secondary text: cool grey;
- data colours: restrained categorical accents;
- rules: low-contrast grey.

### Paper field

Use for editorial explanation and relationship flow.

Suggested roles:

- background: warm off-white;
- primary text: near-black;
- secondary text: muted grey;
- data colours: restrained categorical accents;
- rules: fine grey.

---

## 7. What the reference posters teach

The strongest recurring lessons are:

1. **The visualisation is the poster's evidence core.**
2. **A long research history can be compressed through structure rather than prose.**
3. **Category colours work best when they remain stable across years and views.**
4. **Key figures are useful when they establish scale, not when they decorate.**
5. **A second explanatory page can carry institutional context, timeline, credits, and download information, leaving the front page visually focused.**

These lessons should be reused; the exact poster layout does not need to be cloned.
