# humanizer-svenska

**A Claude skill for removing AI-generated writing patterns from Swedish professional text.**

Covers business writing, reports, articles, and social media posts. Detects and fixes patterns specific to Swedish AI output, going beyond generic humanizer tools by addressing the linguistic habits that AI produces specifically when writing in Swedish.

---

## What it does

The skill scans text for 16 documented AI writing patterns and rewrites them to sound like a real Swedish professional wrote them. It then runs a two-step self-critique to catch anything that still reads as AI-generated before producing a final version.

---

## Pattern coverage

| # | Pattern | Example fix |
|---|---|---|
| 1 | Significance inflation | "banbrytande verktyg" → specific metric |
| 2 | Landscape framing | "i en alltmer digitaliserad värld" → stryka, börja med poängen |
| 3 | Participle phrases as fake analysis | "bidrar till en ökad förståelse för" → skriv vad du faktiskt menar |
| 4 | Vague attributions | "experter menar" → konkret källa och datum |
| 5 | Passive voice as false formality | "det kan konstateras att" → aktivt påstående |
| 6 | Nominalization overuse | "genomförandet av" → "att genomföra" |
| 7 | Anglification | "ta ägarskap över" → "ansvara för" |
| 8 | Structural AI patterns | balanced structures, generic closings |
| 9 | Negative parallelism | "det handlar inte om X, utan Y" → direkt påstående |
| 10 | Social media patterns | consensus openers, hashtag spam, hollow CTAs |
| 11 | Sycophantic openers/closers | "Vilken bra fråga!" → stryk |
| 12 | Filler phrases | "i syfte att uppnå detta mål" → "för att" |
| 13 | Excessive hedging | stacked qualifiers → konkret osäkerhet |
| 14 | Knowledge-cutoff disclaimers | "baserat på tillgänglig information" → stryk |
| 15 | Copula avoidance | "utgör", "representerar", "fungerar som" → "är" |
| 16 | Bullet/emoji formatting as AI signal | dekorativa listor och emojis → löptext |

---

## Register support

The skill applies different editing rules depending on text type:

- **Affärsskrivande** — email, offers, presentations, internal comms
- **Rapportskrivande** — analysis, strategy, executive summaries
- **Artiklar** — thought leadership, industry commentary
- **Sociala medier** — LinkedIn and similar professional platforms

If the text type is not clear from the input, the skill will ask before editing.

---

## Process

The skill follows a structured 10-step process:

1. Ask for text type if unclear
2. Read the text
3. Identify all AI patterns
4. Apply the correct register
5. Rewrite problematic sections
6. Verify the rewrite sounds natural when read aloud in Swedish
7. Self-critique: "Vad avslöjar att det här fortfarande är AI-genererat?"
8. Answer with remaining tells
9. Self-critique: "Vad saknar texten för att låta skriven av en verklig person med en verklig åsikt?"
10. Produce final version

**Output format:** Draft rewrite → AI audit → Final version → Optional change summary

---

## What Nordic professional voice means

The skill is calibrated to Swedish professional writing norms, not generic English ones:

- **Directness without qualifiers.** Say what you mean.
- **Understatement as credibility.** Swedish readers distrust superlatives.
- **Active voice and first person.** "Vi ändrade strategin" beats "en strategiändring genomfördes."
- **Specific over general.** Not "strong results" but "30% growth in three months."
- **Acknowledge complexity honestly.** "Det här är inte enkelt" is more credible than pretending everything is resolved.

---

## Installation

This is a Claude skill. To use it, place `SKILL.md` in your skills directory and reference it in your Claude setup.

```
skills/
  humanizer-svenska/
    SKILL.md
```

---

## Compatibility

- Claude Sonnet 4.6 and later
- Works as a standalone skill or alongside the English `humanizer` skill for bilingual workflows

---

## Versions

| Version | Notes |
|---|---|
| 2.0.0 | 16 patterns, register guidance, soul demonstration, AskUserQuestion support |
| 1.0.0 | Initial release, 10 patterns |

See [CHANGELOG.md](./CHANGELOG.md) for full details.

---

## Related

- [`humanizer`](../humanizer/) — English-language equivalent (24 patterns, based on Wikipedia's Signs of AI Writing guide)
