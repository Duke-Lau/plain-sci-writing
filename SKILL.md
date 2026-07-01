---
name: plain-sci-writing
description: Polish Chinese or English SCI manuscript prose into clear, human, non-template writing while preserving academic accuracy. Use when the user asks to remove AI tone, make SCI English natural, make Chinese academic drafts clearer, avoid jargon stacking, simplify over-polished Nature-style prose, rewrite abstracts/results/discussion/reviewer responses plainly, perform paragraph logic review, "去AI腔", "说人话", "学术中文理顺", "英文更自然", "不要模板腔", or "Nature风格但像人写的".
---

# Plain SCI Writing

Use this skill as the plain-language review layer after high-level academic polishing. The goal is not to make the prose casual. The goal is to make it readable, precise, defensible, and recognizably written by a careful human author.

## Default stance

- Preserve meaning, data, uncertainty, and scope.
- Repair logic before repairing style.
- Prefer one main idea per paragraph.
- Prefer concrete claims over grand framing.
- Say the finding first, then the meaning, then the boundary.
- Remove empty intensifiers, stock transitions, and ornamental phrasing.
- Do not invent data, mechanisms, references, novelty, study aims, statistics, or implications.
- Do not hide weak logic under fluent English.

## When to open extra files

Open [references/plainness-checklist.md](references/plainness-checklist.md) when the text is long, sounds strongly AI-generated, mixes Results and Discussion, or needs an explicit audit rather than a quick rewrite.

## Workflow

### 1. Identify the writing job

Classify the request before editing:

- `Chinese logic pass`: Chinese draft needs clearer order before translation.
- `English naturalness pass`: English is accurate but stiff, inflated, or template-like.
- `Section repair`: abstract, introduction, results, discussion, conclusion, methods, or response letter has a section-specific logic issue.
- `Human-tone pass`: prose sounds generic, over-polished, or AI-like.
- `Overclaim pass`: claims exceed the data or study design.

If the user asks only for rewriting, keep the response concise and provide a directly replaceable version. If the text has a serious logic problem, name the problem briefly before rewriting.

### 2. Stabilize the claim

For each paragraph, identify:

- the actual finding or point
- the evidence the sentence is allowed to rely on
- the intended reader takeaway
- the boundary or uncertainty that must remain visible

If any of these is missing, do not make up content. Use bracketed placeholders such as `[specify outcome]`, `[add sample size]`, or `[state comparison group]` only when needed.

### 3. Rewrite plainly

Apply these priorities in order:

1. Put the main claim early.
2. Keep one paragraph to one job.
3. Use specific nouns and active verbs where appropriate.
4. Replace vague praise with observable contribution.
5. Keep hedging proportional to the evidence.
6. Remove repeated setup phrases such as `it is worth noting that`, `in the context of`, `plays an important role`, and `provides new insights`.
7. Shorten long noun chains and stacked abstractions.
8. Preserve technical terms only when they carry necessary meaning.

### 4. Preserve SCI register

Plain writing should still sound publishable:

- Use measured verbs such as `show`, `indicate`, `suggest`, `estimate`, `compare`, and `examine`.
- Avoid hype words such as `groundbreaking`, `crucial`, `significant` when `significant` is not statistical, `profound`, `comprehensive`, and `novel` unless directly supported.
- Avoid conversational filler, jokes, rhetorical questions, and unsupported certainty.
- Keep methods and results reproducible when the sentence depends on study design.

## Output patterns

### Quick rewrite

Use this when the user asks for a cleaner version:

```markdown
Rewritten:
[directly replaceable text]
```

### Logic-first rewrite

Use this when the original text has obvious problems:

```markdown
Main issue:
[one or two concise bullets]

Rewritten:
[directly replaceable text]
```

### Chinese-to-English path

When a Chinese draft is unclear, do not translate the confusion into English. First produce a clearer Chinese logic version if useful, then the English version:

```markdown
中文逻辑版:
[clear Chinese version]

English version:
[publishable English version]
```

### Audit mode

When the user asks for review, diagnosis, or "哪里像AI", give a compact audit:

```markdown
Plainness audit:
- [specific issue]
- [specific issue]

Suggested revision:
[directly replaceable text]
```

## Boundaries

- For literature support, use `nature-citation` or another literature workflow.
- For full academic restructuring, use `nature-polishing` first, then this skill.
- For Word/PDF formatting, use `documents`.
- For statistical model choice, data cleaning, or inference validity, use R-based analysis and domain methods checks. This skill may flag overclaiming, but it does not choose models.
