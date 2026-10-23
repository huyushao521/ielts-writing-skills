---
name: ielts-task1
description: This skill should be used when the user needs help with IELTS Writing Task 1 (academic report). It covers chart/graph description, process diagram description, map description, vocabulary enhancement, structure guidance, band score estimation, and report improvement. Triggers include requests like "写雅思小作文", "IELTS Task 1", "雅思图表作文", "雅思流程图", "雅思地图", "雅思小作文批改", or any mention of IELTS graph/chart/process/map description writing.
---

# IELTS Writing Task 1 (小作文)

## Overview

This skill provides comprehensive assistance for IELTS Writing Task 1, the academic report component worth one-third of the writing score. It supports report generation for all chart types (line, bar, pie, table), process diagrams, and maps, along with vocabulary enhancement, structure planning, band score estimation, and full report revision — targeting Band 7+ quality.

## When to Use

Trigger this skill when the user:
- Asks to write, draft, or generate an IELTS Task 1 report for a chart, graph, table, process, or map
- Requests report evaluation, scoring, or band estimation
- Needs help with data description language and vocabulary
- Asks for structure or organization guidance for Task 1
- Mentions "雅思小作文", "IELTS Task 1", "雅思图表", "雅思流程图", "雅思地图" etc.
- Provides chart data or an image and asks for a report

## Core Capabilities

### 1. Report Generation (报告生成)

Given chart data or a described graph, generate a Band 7+ Task 1 report.

**Workflow:**
1. Identify the chart type (line/bar/pie/table/process/map)
2. Extract key features: overall trends, highest/lowest values, significant changes
3. Structure the report: Introduction → Overview → Details (1-2 paragraphs) → [Comparison]
4. Write 150+ words (target 170-200)
5. Apply appropriate vocabulary and grammar patterns (see `references/task1_vocabulary.md`)

**Chart-specific approach:**
- **Line chart** → describe trends (rise, fall, fluctuate), identify crossings and peaks
- **Bar chart** → compare categories, identify highest/lowest, note patterns
- **Pie chart** → describe proportions, compare segments, note dominant/minor shares
- **Table** → identify highest/lowest, compare rows/columns, note patterns
- **Process diagram** → describe stages sequentially, use passive voice
- **Map** → describe changes over time, compare before/after

**Output format:** Present the report in clean text, followed by a brief analysis (word count, chart type, key features identified, vocabulary used).

### 2. Report Evaluation & Scoring (批改评分)

Given a user's report, evaluate and estimate a band score.

**Workflow:**
1. Read the full report
2. Score each criterion using rubrics in `references/scoring_rubric.md`:
   - Task Achievement (TA)
   - Coherence & Cohesion (CC)
   - Lexical Resource (LR)
   - Grammatical Range & Accuracy (GRA)
3. Calculate overall estimated band
4. Provide specific feedback for each criterion
5. List grammar errors with corrections
6. Suggest vocabulary upgrades

**Output format:**
```
## 评分结果 / Band Score Estimation
- Task Achievement (TA): X.0
- Coherence & Cohesion (CC): X.0
- Lexical Resource (LR): X.0
- Grammatical Range & Accuracy (GRA): X.0
- Overall Estimated Band: X.0

## 详细反馈 / Detailed Feedback
[Criterion-by-criterion feedback]

## 语法错误 / Grammar Errors
| 原句 | 修改 | 说明 |
|------|------|------|

## 词汇升级建议 / Vocabulary Upgrades
| 原词/表达 | 建议替换 | 说明 |
|-----------|----------|------|

## 修改后范文 / Improved Version
[Full revised report]
```

### 3. Key Features Identification (关键特征提取)

Given chart data or a described chart, identify the most important features to describe.

**Workflow:**
1. Identify overall trend(s) — this goes in the overview
2. Identify highest and lowest values
3. Identify significant changes (sharp increases, sudden drops, peaks, troughs)
4. Identify crossings (where one line overtakes another)
5. Identify surprising or notable patterns
6. Rank features by importance for the 150-word report

**Output format:** Structured list of key features with suggested data points to include.

### 4. Structure Planning (结构规划)

Given a chart, produce a paragraph-by-paragraph plan.

**Standard structure:**
```
Paragraph 1 (Introduction): 1-2 sentences
  - Paraphrase the prompt (what the chart shows, time period, units)

Paragraph 2 (Overview): 2-3 sentences
  - Overall trend(s) — the "big picture"
  - No specific data/numbers in overview

Paragraph 3 (Details 1): 3-5 sentences
  - Specific data points and comparisons
  - Group related data logically

Paragraph 4 (Details 2): 3-5 sentences
  - Remaining significant data
  - Comparisons across categories/time
```

### 5. Vocabulary & Grammar Enhancement (词汇语法提升)

Given a report or description, upgrade its language quality.

**Workflow:**
1. Identify plain or repetitive vocabulary → suggest Band 7+ alternatives (see `references/task1_vocabulary.md`)
2. Improve sentence variety (simple, compound, complex)
3. Replace basic comparison structures with advanced ones
4. Add appropriate tense usage guidance
5. Show before/after comparisons

### 6. Report Improvement (范文改写)

Given a report, produce an improved version targeting a higher band.

**Workflow:**
1. Identify weaknesses (missing overview, poor data selection, limited vocabulary, grammar errors)
2. Rewrite the report addressing each weakness
3. Ensure Band 7+ quality
4. Highlight key changes with side-by-side comparison

## Chart Type Quick Reference

See `references/chart_types.md` for detailed guidance on each type:
- **Line chart (折线图)**: Trends over time
- **Bar chart (柱状图)**: Category comparison
- **Pie chart (饼图)**: Proportion/percentage
- **Table (表格)**: Multiple data dimensions
- **Process diagram (流程图)**: Sequential stages
- **Map (地图)**: Spatial change over time
- **Multiple charts (复合图)**: Two or more charts together

## Key References

- `references/chart_types.md` — Detailed chart-by-chart writing strategies with sample sentences
- `references/task1_vocabulary.md` — Band 7+ vocabulary for trends, comparisons, proportions, processes, and maps
- `references/scoring_rubric.md` — Full Band 1-9 scoring rubrics adapted for Task 1 (TA instead of TR)
- `references/sample_reports.md` — Sample reports across all chart types with band annotations

## Workflow Decision Tree

```
User request
├── "写一篇关于这个图表的小作文" → Report Generation (Capability 1)
├── "帮我批改/评分这篇小作文" → Report Evaluation (Capability 2)
├── "这个图的关键特征有哪些" → Key Features Identification (Capability 3)
├── "帮我列个提纲" → Structure Planning (Capability 4)
├── "帮我把这段写得更好" → Vocabulary & Grammar Enhancement (Capability 5)
├── "帮我把这篇改到7分以上" → Report Improvement (Capability 6)
└── Ambiguous → Ask user to clarify which capability they need
```

## Important Guidelines

- Reports are in English (the report itself); explanations and feedback can be in Chinese
- Target 170-200 words for generated reports (minimum 150)
- **Overview paragraph is critical** — without it, maximum band is 5.0 for TA
- **Do NOT include personal opinion** — Task 1 is objective data description only
- **No conclusion paragraph** — use "overview" instead; don't add new data in final paragraph
- **Select data strategically** — don't describe every single number; pick the most significant
- **Use appropriate tense** — past tense for past data, present tense for current/no-time data, future for predictions
- **Group data logically** — by trend, by category, by time period — not just chronologically
- **Paraphrase the prompt** in the introduction — don't copy the prompt wording exactly
- When scoring, be honest and constructive — do not inflate scores
