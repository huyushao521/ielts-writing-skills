---
name: ielts-task2
description: This skill should be used when the user needs help with IELTS Writing Task 2 (academic essay). It covers essay writing, structure guidance, topic brainstorming, vocabulary enhancement, grammar correction, band score estimation, and essay improvement. Triggers include requests like "写雅思大作文", "IELTS essay", "雅思Task 2", "雅思大作文批改", "雅思写作", "IELTS writing task 2", or any mention of IELTS academic essay writing.
---

# IELTS Writing Task 2 (大作文)

## Overview

This skill provides comprehensive assistance for IELTS Writing Task 2, the academic essay component worth two-thirds of the writing score. It supports essay generation, structure optimization, topic brainstorming, vocabulary upgrading, grammar correction, band score estimation, and full essay revision — targeting Band 7+ quality.

## When to Use

Trigger this skill when the user:
- Asks to write, draft, or generate an IELTS Task 2 essay on a given topic
- Requests essay evaluation, scoring, or band estimation
- Needs help brainstorming ideas or structuring an essay
- Asks for vocabulary or grammar improvement on an existing essay
- Mentions "雅思大作文", "IELTS essay", "Task 2", "雅思写作" etc.
- Provides a prompt and asks for essay-related help

## Core Capabilities

### 1. Essay Generation (写作生成)

Given a topic/prompt, generate a full Band 7+ essay following the structure in `references/essay_structure.md`.

**Workflow:**
1. Identify the essay type (see `references/essay_types.md`)
2. Generate a thesis statement and position
3. Write 4-5 paragraphs: Introduction → Body 1 → Body 2 → (Body 3) → Conclusion
4. Ensure 250+ words (target 270-300)
5. Apply Band 7+ vocabulary and grammar patterns (see `references/vocabulary_grammar.md`)

**Output format:** Present the essay in clean text, followed by a brief breakdown (word count, essay type, key vocabulary used).

### 2. Essay Evaluation & Scoring (批改评分)

Given a user's essay, evaluate and estimate a band score across all four IELTS criteria.

**Workflow:**
1. Read the full essay
2. Score each criterion using rubrics in `references/scoring_rubric.md`:
   - Task Response (TR)
   - Coherence & Cohesion (CC)
   - Lexical Resource (LR)
   - Grammatical Range & Accuracy (GRA)
3. Calculate overall estimated band (average, rounded)
4. Provide specific, actionable feedback for each criterion
5. List grammar errors with corrections
6. Suggest vocabulary upgrades

**Output format:**
```
## 评分结果 / Band Score Estimation
- Task Response (TR): X.0
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
| 原词 | 建议替换 | 说明 |
|------|----------|------|

## 修改后范文 / Improved Version
[Full revised essay]
```

### 3. Topic Brainstorming (观点构思)

Given a topic, generate structured ideas for body paragraphs.

**Workflow:**
1. Analyze the prompt to identify the core question
2. Generate 2-3 arguments for each side (if discussion type) or for the user's position
3. For each argument, provide: claim → reason → example → conclusion
4. Suggest which approach to take for the strongest essay

**Output format:** Present as a structured outline with numbered points.

### 4. Essay Structure Planning (结构规划)

Given a topic, produce a paragraph-by-paragraph plan before writing.

**Workflow:**
1. Identify essay type (see `references/essay_types.md`)
2. Map out each paragraph's purpose and key content
3. Include thesis statement, topic sentences, and concluding sentence
4. Present as an outline

### 5. Vocabulary & Grammar Enhancement (词汇语法提升)

Given an essay or paragraph, upgrade its language quality.

**Workflow:**
1. Identify plain or repetitive vocabulary → suggest Band 7+ alternatives (see `references/vocabulary_grammar.md`)
2. Identify simple sentence structures → suggest complex alternatives
3. Add collocations and less common lexical items
4. Improve sentence variety (simple, compound, complex, compound-complex)
5. Show before/after comparisons

### 6. Essay Improvement (范文改写)

Given an essay, produce an improved version targeting a higher band.

**Workflow:**
1. Identify weaknesses (weak thesis, poor paragraphing, limited vocabulary, grammar errors)
2. Rewrite the essay addressing each weakness
3. Ensure Band 7+ quality throughout
4. Add a side-by-side comparison highlighting key changes

## Essay Types Quick Reference

See `references/essay_types.md` for detailed guidance on each type:
- **Opinion (观点类)**: "Do you agree or disagree?" / "What is your opinion?"
- **Discussion (讨论类)**: "Discuss both views and give your opinion"
- **Advantage/Disadvantage (优缺点类)**: "Do the advantages outweigh the disadvantages?"
- **Problem/Solution (问题解决类)**: "What are the causes and solutions?"
- **Two-Part Question (双问题类)**: Two questions to answer

## Key References

- `references/essay_types.md` — Detailed breakdown of 5 essay types with templates and signal phrases
- `references/essay_structure.md` — Paragraph-by-paragraph structure templates and cohesion tools
- `references/scoring_rubric.md` — Full Band 1-9 scoring rubrics for all four criteria
- `references/vocabulary_grammar.md` — Band 7+ vocabulary, collocations, sentence patterns, and grammar features
- `references/essay_collection.md` — 30+ sample essays across common topics with band annotations

## Workflow Decision Tree

```
User request
├── "写一篇关于X的雅思大作文" → Essay Generation (Capability 1)
├── "帮我批改/评分这篇作文" → Essay Evaluation (Capability 2)
├── "这道题怎么想观点" → Topic Brainstorming (Capability 3)
├── "帮我列个提纲" → Essay Structure Planning (Capability 4)
├── "帮我把这段写得好一点/高级一点" → Vocabulary & Grammar Enhancement (Capability 5)
├── "帮我把这篇作文改到7分以上" → Essay Improvement (Capability 6)
└── Ambiguous → Ask user to clarify which capability they need
```

## Important Guidelines

- Always write essays in English (the essay itself), but explanations and feedback can be in Chinese if the user communicates in Chinese
- Target 270-300 words for generated essays (minimum 250)
- Use formal academic register — no contractions, no slang, no first-person singular unless the prompt explicitly asks for personal experience
- Ensure each body paragraph has a clear topic sentence
- Use a variety of cohesive devices (however, nevertheless, in addition, furthermore, consequently, etc.)
- Include less common vocabulary and complex grammatical structures for Band 7+
- When scoring, be honest and constructive — do not inflate scores
- When providing feedback, always give specific, actionable suggestions with examples
