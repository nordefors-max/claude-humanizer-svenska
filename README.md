# 🇸🇪 Humanizer på Svenska

**A Claude skill for removing AI-generated writing patterns from Swedish professional text.**

Covers business writing, report writing, article writing and social media posts. Built on documented patterns from observed AI output in Swedish, with a focus on patterns that have no equivalent in English-language humanizer tools.

---

## Why this exists

Most AI humanizer tools are built for English. The few that support Swedish apply English detection logic translated directly, missing patterns that are specific to how LLMs generate Swedish text.

This skill is built from the ground up for Swedish, with pattern categories that reflect how AI actually writes in Swedish: nominalization overuse, passive voice as false formality, direct anglification imports, and significance inflation dressed in Swedish vocabulary.

The English [Humanizer skill](https://github.com/blader/humanizer/tree/main) covers the foundational logic. This skill inherits that logic and replaces the vocabulary and examples with Swedish-specific content.

---

## What it covers

### 10 pattern categories

| # | Pattern | Example trigger |
|---|---|---|
| 1 | Significance inflation | "banbrytande", "avgörande", "vittnar om" |
| 2 | Landscape and trend framing | "i en alltmer digitaliserad värld", "spelplanen förändras" |
| 3 | Participle phrases as fake analysis | "belyser vikten av", "understryker behovet av" |
| 4 | Vague attribution | "experter menar", "branschkällor pekar på" |
| 5 | Passive voice as false formality | "det kan konstateras att", "det bör påpekas att" |
| 6 | Nominalization overuse | "implementeringen av", "möjliggörandet av" |
| 7 | Anglification imports | "ta ägarskap över", "navigera förändringen", "holistiskt" |
| 8 | Structural AI patterns | even paragraph blocks, rule of three, formulaic closings |
| 9 | Negative parallelism | "Det är inte längre en fråga om om, utan när" |
| 10 | Social media tells | vague CTAs, landscape openings, generic hashtag stacks |

### Register guidance for 4 output types

- **Business writing** – proposals, presentations, internal comms
- **Report writing** – analysis, summaries, strategy documents, executive summaries
- **Acrticle writing** – industry commentary, thought leadership, editorial
- **Social media writing** – LinkedIn and equivalent professional channels

### 4 full before/after examples

One complete worked example per output type, each including a draft rewrite, a Swedish-language self-audit step, and a final version with change summary.

### Quick-reference substitution table

20 of the most common AI-Swedish phrases with direct replacements.

---

## Installation

**Recommended** (clone directly into Claude Code skills directory)

```bash
mkdir -p ~/.claude/skills
git clone https://github.com/humanizer-svenska.git ~/.claude/skills/humanizer-svenska
```

**Manual install** (if you already have the file)

```bash
mkdir -p ~/.claude/skills/humanizer-svenska
cp SKILL.md ~/.claude/skills/humanizer-svenska/
```

---

## Usage

In Claude Code, invoke the skill:

```
/humanizer-svenska

[klistra in din text här]
```

Or ask Claude directly:

```
Humanisera den här texten: [din text]
```

**Specify output type for best results**

The skill handles four registers with different conventions. If you specify the type upfront, the skill applies the right guidance from the start:

```
/humanizer-svenska rapport

[klistra in din text här]
```

Available types: `affärsskrivande`, `rapport`, `artikel`, `sociala medier`

If no type is specified, the skill will infer it from the text.

The skill will:
1. Identify or confirm the output type
2. Scan for the 10 pattern categories
3. Produce a draft rewrite
4. Run the Swedish self-audit ("Vad avslöjar att det här är AI-genererat?")
5. Deliver a final version with an optional change summary

---

## Examples

The [`examples/`](./examples/) folder contains input/output pairs for each output type:

| File | Type |
|---|---|
| [`examples/affarstext.md`](./examples/affarstext.md) | Business writing |
| [`examples/rapport.md`](./examples/rapport.md) | Report writing |
| [`examples/artikel.md`](./examples/artikel.md) | Article writing |
| [`examples/sociala-medier.md`](./examples/sociala-medier.md) | Social media |

---

## Design principles

**Built for Swedish, not translated from English.**
The vocabulary list, examples, and register guidance are written from scratch based on observed Swedish AI output. The structural logic from the English Humanizer skill is retained but none of the content is carried over.

**Professional writing, not academic.**
This skill is tuned for business, editorial, and professional social media output. Academic writing has different conventions and a different AI pattern profile. It is out of scope here.

**Pattern-based, not detector-based.**
The skill does not run statistical detection. It teaches Claude to recognise named patterns the same way an experienced Swedish editor would. This makes it more robust to model updates than perplexity-based approaches.

**Voice injection, not just pattern removal.**
Removing AI patterns produces clean but often flat text. The skill includes active guidance on what Swedish professional voice sounds like: direct, specific, active, grounded in Nordic communication norms. The goal is not undetectable text but genuinely better text.

---

## Limitations

- **Social media scope** is currently limited to LinkedIn and equivalent professional channels. Consumer-facing platforms (Instagram, TikTok) have different conventions not covered here.
- **Vocabulary evolves.** AI vocabulary shifts with model updates. The trigger word lists reflect patterns from GPT-4 and GPT-4o era output (2023–2025). New patterns may emerge that are not yet documented.
- **No academic writing.** Legal, scientific, and academic Swedish have different formality conventions. Applying this skill to those genres may overcorrect.
- **The skill does not source-check.** When the before/after examples in Section 4 (vague attribution) suggest replacing vague claims with specific sources, that is illustrative. The user is responsible for verifying any statistics or citations.

---

## Contributing

Contributions welcome. See [`CONTRIBUTING.md`](./CONTRIBUTING.md) for guidelines.

The most useful contributions are:

- New trigger words or phrases observed in Swedish AI output
- Additional before/after examples for any output type
- Examples from industries or contexts not currently represented
- Corrections to register guidance based on domain expertise

---

## Changelog

See [`CHANGELOG.md`](./CHANGELOG.md).

---

## License

MIT. See [`LICENSE`](./LICENSE).

---

## Related

- [Humanizer (English)](https://github.com/anthropics/claude-skills/tree/main/humanizer) – the English-language skill this is based on
- [Wikipedia: Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing) – the foundational reference for pattern documentation
- [Pedagog Malmö: Kan man upptäcka AI-genererade texter?](https://pedagog.malmo.se/bloggposter/kan-man-upptacka-ai-genererade-texter/) – Swedish-language source on AI text detection patterns
