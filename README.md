# Humanizer på svenska

**A Claude skill that rewrites or reviews Swedish text so it reads like normal Swedish, not like AI output or translated English.**

Built for emails, presentations, reports, articles and LinkedIn posts. It also works as a silent final check whenever Claude writes Swedish.

---

## Why this exists

Most humanizer tools are built for English. The ones that support Swedish usually translate English rules, which misses what actually gives Swedish AI text away: bureaucratic vocabulary ("gällande", "erhålla"), false friends ("teknologi", "massiv"), English typography (dashes, Oxford commas, "30%", curly quotes) and value-laden words that change the meaning ("förväntas", "tack vare").

This skill is written for Swedish from the start. Its rules are checked against Språkrådet's writing rules and TT-språket, and doubtful phrases can be tested against real usage in Språkbanken's corpora.

---

## Core rules

1. **Change how it is written, not what it says.** No added claims, numbers, sources or opinions. Missing facts are marked in brackets, e.g. `[källa]`, for the writer to fill in.
2. **Never invent concrete details** to make the text sound more human.
3. **Match the writer's voice.** Don't make the text sharper or more opinionated than the writer is.

---

## What it covers

| Section | Content |
|---|---|
| A. Word choice | Bureaucratic words, translated English, false friends, inflated AI vocabulary, words that say more than you mean |
| B. Sentence structure | Nominalisations, delayed "det"-openings, hidden passives, "vilket" chains, stacked hedging, comma splices, sentence length |
| C. Rhetorical AI tells | "Inte X, utan Y", staged one-liners, rule of three, landscape openings, generic closings, empty questions |
| D. Form and typography | Dashes, commas, quotation marks, %, numbers, dates, capitalisation, emojis, sa/sade |
| E. Tone | Sycophancy, knowledge disclaimers, du/ni |
| F. Frequency test | Checking a doubtful phrase against Språkbanken's Korp corpora |

Plus guidance per text type (email, presentation, report, article, LinkedIn), worked before/after examples and an eight-point final checklist.

### Modes

- **Rewrite (default):** returns the rewritten text and at most three short lines on what changed.
- **Review:** quotes the weakest phrasings, explains why and suggests fixes.
- **Silent check:** runs the checklist on Claude's own Swedish output without reporting it.

---

## Installation

**Clone into the Claude Code skills directory**

```bash
mkdir -p ~/.claude/skills
git clone https://github.com/nordefors-max/claude-humanizer-svenska.git ~/.claude/skills/humanizer-svenska
```

**Manual install**

```bash
mkdir -p ~/.claude/skills/humanizer-svenska
cp SKILL.md ~/.claude/skills/humanizer-svenska/
```

In claude.ai you can upload `SKILL.md` as a skill under Settings.

---

## Usage

```
/humanizer-svenska
```

Or ask directly:

```
Skriv om det här mejlet så att det låter som vanlig svenska:
```

```
Granska den här presentationen. Vad låter som AI?
```

The text type is inferred from the input. Section F (frequency test) needs a session with web fetch access; without it the rest of the skill works as normal.

---

## Sources

- [Språkrådet, Snabba skrivregler](https://writing.chalmers.se/wp-content/uploads/2024/06/Snabba-skrivregler-Sprakradet-1.pdf): spelling, punctuation, numbers and dates
- [TT-språket](https://tt-spraket.tt.se/): word choice, false friends, anglicisms and numbers in running text
- [Språkbanken Korp](https://spraakbanken.gu.se/korp/): how often a phrase is actually used in Swedish

TT writes news Swedish, so some of its style choices ("sade", "procent" instead of %) are deliberately not adopted for business writing.

---

## Deliberate choices

- **No dashes as pauses.** Both Språkrådet and TT allow them sparingly. The skill bans them because they are one of the clearest AI tells.
- **% and kr by default**, with a space before. Written out in speaker notes.
- **"sa", not "sade".**
- **Not purist.** Established business loanwords such as agenda, team and design are fine.

---

## Limitations

- Professional writing only. Legal, academic and scientific Swedish follow other conventions.
- Most Korp corpora are from the 2010s, so newer business jargon is underrepresented, and forums skew informal.
- AI vocabulary changes with new models. The lists need regular updates.

---

## Changelog

See [`CHANGELOG.md`](./CHANGELOG.md).

## Related

- [Wikipedia: Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing)
- [Humanizer (English)](https://github.com/blader/humanizer)
