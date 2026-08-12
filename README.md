# Heritage Data Viz Workflow

**Turn dense heritage evidence into structured data, visual relationships, and poster-grade arguments.**  
**将大量遗产资料整理为结构化数据、可视化关系与可出版的 Poster。**

This Skill is for heritage and World Heritage projects where the real problem is not drawing a chart, but deciding **what to classify, what relationship matters, and how to compress a large corpus into one readable visual argument**.

它适合处理多年观察报告、文章库、世界遗产大会资料、HIA / SOC / 研究报告等信息量较大的资料：先建立分类与证据结构，再选择真正能说明问题的视觉形式，最后组成 Poster。

## Preview / 预览

All previews below are deterministic SVG examples stored in this repository, so they remain sharp and inspectable on GitHub.

下列预览均为仓库内的确定性 SVG 样例，在 GitHub 中可直接预览、放大和检查，不依赖外部图片链接。

| Radial chronology / 径向时间 | Metric summary / 关键数字 | Relationship flow / 关系流向 |
| --- | --- | --- |
| ![Radial chronology sample](examples/01-radial-wheel.svg) | ![Metric summary sample](examples/02-metric-summary.svg) | ![Relationship flow sample](examples/03-relationship-flow.svg) |

| Split field / 分栏构图 | Context back / 背面信息 |
| --- | --- |
| ![Split-field sample](examples/04-split-field.svg) | ![Context-back sample](examples/05-context-back.svg) |

## Core idea / 核心思路

**Corpus → Classification → Visual question → Evidence graphic → Poster**  
**资料库 → 分类体系 → 视觉问题 → 证据图形 → Poster**

The poster is the last step, not the first.

Poster 是最后一步，不是第一步。

## What it is for / 适用场景

- multi-year observation-report series / 多年观察报告
- heritage article or case corpora / 遗产文章与案例库
- World Heritage Committee/session analysis / 世界遗产大会与届次分析
- HIA, SOC, policy, nomination and periodic-reporting research / HIA、SOC、政策、申遗与定期报告研究
- data-heavy research communication / 数据密集型研究传播
- poster, postcard, exhibition and publication visuals / Poster、明信片、展览与出版视觉

## What it produces / 可形成的输出

The Skill prioritises a small set of visual mechanisms that each answer a distinct research question.

### 1. Radial chronology / 径向时间图

For **time + recurrence + thematic density**.

适合表现多年变化、届次节奏、不同主题在时间中的出现密度。

[Open the radial chronology sample →](examples/01-radial-wheel.svg)

### 2. Metric summary / 关键数字总览

For communicating **scale before detail** with only a few high-value numbers.

适合先让读者理解项目规模，再进入复杂信息。

[Open the metric summary sample →](examples/02-metric-summary.svg)

### 3. Sankey / alluvial / relationship flow / 桑基图、流向与关系图

For **relationships between categorical dimensions**, such as theme → year/session or theme → host country.

适合解释主题、年份、国家、来源或其他分类之间的关系，而不是只展示数量。

[Open the relationship-flow sample →](examples/03-relationship-flow.svg)

### 4. Partial radial / split field / 局部径向与分栏构图

For combining a strong title/access field with a dense circular evidence visual.

适合把项目身份、入口与复杂数据图放在同一张 Poster 中，同时保持信息层级。

[Open the split-field sample →](examples/04-split-field.svg)

## Front / back logic / 正反面逻辑

For postcard or two-sided poster formats, the front carries the visual argument; the back carries context, chronology, provenance and access.

如果是明信片或双面 Poster，正面负责“看见关系”，背面负责“理解项目”：项目简介、线性时间轴、来源、设计署名与访问入口。

[Open the context-back sample →](examples/05-context-back.svg)

## Workflow / 工作流

1. **Intake** — preserve the source corpus and provenance. / 保留原始资料与来源信息。
2. **Classify** — define only the dimensions needed for the research question. / 建立与问题有关的分类体系。
3. **Audit** — check totals, gaps, duplicates and ambiguous labels. / 检查数量、缺失、重复与歧义。
4. **Relate** — derive matrices, flows, timelines or networks. / 生成关系矩阵、流向、时间或网络结构。
5. **Select** — choose one relationship that deserves the poster. / 选择一条最值得被看见的关系。
6. **Visualise** — radial, Sankey, metric summary, map, timeline, etc. / 选择合适的证据型可视化。
7. **Compose** — proposition + dominant evidence + support + provenance. / 组合主张、核心证据、辅助信息与来源。
8. **Validate** — re-check numbers, legibility and export. / 复核数据、可读性与导出效果。

## Design principle / 设计原则

> **Do not put all the data on the poster. Put the relationship that the data proves on the poster.**
>
> **不是把所有数据放上 Poster，而是把数据能够证明的那条关系放上 Poster。**

The visual family uses two compatible modes:

- **Dark analytical mode** — charcoal field, off-white type, stable category colors, large numerals, dense radial structures.
- **Warm-paper editorial mode** — paper surface, ink typography, muted category colors, Sankey/alluvial or explanatory layouts.

Both rely on precise alignment, thin rules, stable legends, sparse captions and one dominant composition.

## Human review / 人工审核

AI can support extraction, normalization, first-pass classification, aggregation, chart prototypes and layout variants.

Publication still requires human review of:

- taxonomy and ambiguous labels;
- interpretation and trend claims;
- source traceability;
- final wording;
- credits, privacy and copyright.

## Repository structure / 仓库结构

```text
.
├── SKILL.md
├── README.md
├── README.zh-CN.md
├── SHOWCASE.md
├── agents/
│   └── openai.yaml
├── assets/
│   ├── design-tokens.css
│   └── poster-shell.html
├── references/
│   ├── data-to-poster.md
│   ├── visual-grammar.md
│   └── reference-project.md
└── examples/
    ├── README.md
    ├── 01-radial-wheel.svg
    ├── 02-metric-summary.svg
    ├── 03-relationship-flow.svg
    ├── 04-split-field.svg
    └── 05-context-back.svg
```

## Example prompts / 示例调用

```text
Use $heritage-data-viz-workflow to turn this multi-year observation-report dataset into one poster. First audit and classify the data, then identify one relationship worth visualising. Do not create a dashboard.
```

```text
使用 $heritage-data-viz-workflow 分析这批 2013–2025 年的观察报告资料。先检查数据和分类，再判断更适合用径向时间图、Sankey 还是关键数字总览，最终输出一张以证据关系为核心的 Poster。
```

## Sample-use note / 样例说明

The SVG files in `examples/` are deterministic visual-grammar samples for demonstrating how the Skill works. They are not substitutes for the original project evidence and do not fabricate project-specific data relationships.

`examples/` 中的 SVG 是用于说明 Skill 工作方式的确定性视觉语法样例，不替代原项目证据，也不虚构具体项目的数据关系。

## Completion standard / 完成标准

The poster is complete when a reader can quickly answer:

**What am I looking at? What pattern does it show? What evidence is it based on?**

一张 Poster 完成的标准是，读者可以快速回答：

**我在看什么？它说明了什么关系？这个判断基于什么证据？**
