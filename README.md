# IELTS Writing Skills for CodeBuddy

> 🌐 **GitHub Pages 站点**: [https://huyushao521.github.io/ielts-writing-skills/](https://huyushao521.github.io/ielts-writing-skills/)

Two CodeBuddy skills for IELTS Academic Writing: **Task 1** (图表报告) and **Task 2** (学术议论文). These skills transform CodeBuddy into a specialized IELTS writing assistant targeting Band 7+ quality.

The project also includes a **GitHub Pages study site** with IELTS Listening notes, featuring synonym/paraphrase vocabulary organized by frequency (high / medium / low).

## Features

### Task 2 — 雅思大作文 (Academic Essay)

| Capability | Description |
|-----------|-------------|
| Essay Generation | Generate a full Band 7+ essay (270-300 words) from a given prompt |
| Essay Evaluation & Scoring | Score across TR / CC / LR / GRA with detailed feedback |
| Topic Brainstorming | Generate structured arguments and evidence for any topic |
| Essay Structure Planning | Paragraph-by-paragraph outline (Intro → Body → Conclusion) |
| Vocabulary & Grammar Enhancement | Upgrade plain vocabulary and simple sentences to Band 7+ |
| Essay Improvement | Rewrite an existing essay to a higher band |

Supports all 5 essay types: Opinion, Discussion, Advantage/Disadvantage, Problem/Solution, Two-Part Question.

### Task 1 — 雅思小作文 (Academic Report)

| Capability | Description |
|-----------|-------------|
| Report Generation | Generate a Band 7+ report (170-200 words) from chart data |
| Report Evaluation & Scoring | Score across TA / CC / LR / GRA with detailed feedback |
| Key Features Identification | Identify the most significant trends and data points |
| Structure Planning | Standard structure: Intro → Overview → Details |
| Vocabulary & Grammar Enhancement | Upgrade trend/comparison vocabulary and sentence variety |
| Report Improvement | Rewrite an existing report to a higher band |

Supports all chart types: Line, Bar, Pie, Table, Process Diagram, Map, Multiple Charts.

## Installation

### Option 1: Manual Install

1. Download or clone this repository
2. Copy the `ielts-task1` and `ielts-task2` folders to `~/.codebuddy/skills/`
3. Restart CodeBuddy — the skills will be available automatically

### Option 2: Install from Zip

1. Download the latest release zip files (`ielts-task1.zip`, `ielts-task2.zip`)
2. Unzip them into `~/.codebuddy/skills/`
3. Restart CodeBuddy

## Usage

Once installed, simply ask CodeBuddy in natural language:

```
# Task 2
"帮我写一篇雅思大作文，题目是..."
"帮我批改这篇雅思作文并评分"
"这道雅思题怎么想观点"

# Task 1
"帮我写一篇雅思小作文，图表是..."
"帮我批改这篇雅思图表作文"
"这个折线图的关键特征有哪些"
```

The skills auto-trigger on keywords like: 雅思大作文, 雅思小作文, IELTS essay, IELTS Task 1, IELTS Task 2, 雅思写作, etc.

## Skill Structure

```
ielts-writing-skills/
├── ielts-task1/
│   ├── SKILL.md                          # Core skill instructions
│   └── references/
│       ├── chart_types.md                # 7 chart types with strategies & sample sentences
│       ├── task1_vocabulary.md           # Band 7+ trend/comparison/process/map vocabulary
│       ├── scoring_rubric.md             # Band 1-9 rubrics (TA/CC/LR/GRA)
│       └── sample_reports.md            # 6 sample reports (Band 7.0-8.0)
│
├── ielts-task2/
│   ├── SKILL.md                          # Core skill instructions
│   └── references/
│       ├── essay_types.md                # 5 essay types with templates & signal phrases
│       ├── essay_structure.md            # PEEL structure, cohesion tools, common mistakes
│       ├── scoring_rubric.md             # Band 1-9 rubrics (TR/CC/LR/GRA)
│       ├── vocabulary_grammar.md         # Band 7+ vocabulary, collocations, sentence patterns
│       └── essay_collection.md           # 5 sample essays (Band 7.0-8.0)
│
├── README.md
├── LICENSE
└── .gitignore
```

## Scoring Criteria Reference

Both skills use the official IELTS Writing scoring criteria:

| Criterion | Task 1 | Task 2 |
|-----------|--------|--------|
| Task Response / Achievement | TA | TR |
| Coherence & Cohesion | CC | CC |
| Lexical Resource | LR | LR |
| Grammatical Range & Accuracy | GRA | GRA |

Each criterion is scored 1-9, and the overall band is the average rounded to the nearest 0.5.

## License

MIT License — see [LICENSE](LICENSE) for details.

## Contributing

Contributions are welcome! If you'd like to add more sample essays, vocabulary, or chart-type strategies:

1. Fork this repository
2. Create a feature branch (`git checkout -b feature/new-samples`)
3. Commit your changes (`git commit -m 'Add new sample essays'`)
4. Push to the branch (`git push origin feature/new-samples`)
5. Open a Pull Request

## Acknowledgments

Built for [CodeBuddy](https://www.codebuddy.ai/) — AI coding assistant with extensible skill system.
