# Changelog

All notable changes to `humanizer-svenska` are documented here.

Format follows [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).  
Versioning follows [Semantic Versioning](https://semver.org/).

---

## [3.1.0] - 2026-11-12

### Summary

Rules checked against TT-språket, and a frequency test against Språkbanken's Korp corpora.

### Added

- **A4: Words that say more than you mean.** Förväntas/väntas, tack vare/på grund av, bör/ska, procent/procentenheter, mindre/färre, ju ... desto, chans/risk.
- **False friends table.** Teknologi, ledarskap, massiv, familjär med, eventuellt, realisera, biljon, provisorisk.
- **English grammar imports.** Unnecessary en/ett, English plural -s on loanwords.
- **Number rules.** One to twelve in words in running text, complete ranges (500–600 kr), plural after decimals, billion = miljard.
- **B8: Sentence length.**
- **F: Frequency test.** Korp query URL, a threshold for when to replace a phrase, three measured examples and known limitations.
- **Report sentence example** and a **Sources** section.
- `WebFetch` added to `allowed-tools` for the frequency test.

### Changed

- % and kr are the default, with "procent" and "kronor" written out in speaker notes.
- The dash ban is now labelled a deliberate choice, since Språkrådet and TT allow sparing use.
- "sa", not "sade", stated explicitly.
- More entries in the A1 and A2 tables (avge, belägenhet, starta upp, maila, outsourca, pressrelease and others).
- A "not purist" note: agenda, team and design are fine in business Swedish.
- The final checklist is now eight points.

---

## [3.0.0] - 2026-10-30

### Summary

Full rewrite. The v2 examples broke the skill's own rules ("inte X, utan Y", staged one-liners) and contained invented statistics, which taught the model the patterns it was meant to remove. v3 is about half the length.

### Added

- **Three priority rules:** change form, not content; never invent details; match the writer's voice. Missing facts are marked in brackets.
- **Modes:** rewrite (default, short change note), review and silent final check.
- **Bureaucratic vocabulary table** (gällande, erhålla, tillhandahålla, huruvida and others).
- **Typography section** based on Språkrådet: dashes, Oxford comma, quotation marks, space before %, numbers, dates, capitalisation.
- **Email and presentation guidance:** subject lines, greetings, du/ni, headline as message, one point per slide.
- New examples for email and slides with no invented facts.

### Changed

- Description in Swedish and covering emails and presentations.
- Passive voice: natural s-passive is allowed; only passives that hide who did something are flagged.
- "Utgör" kept when it means a share.
- LinkedIn: 3–5 hashtags.

### Removed

- The draft, self-audit and final output steps on every run.
- Rules that changed meaning ("verkar som" → "är") or were translated from English ("-ing phrases").

---

## [2.0.0] - 2026-03-18

### Summary

Major update. Six new pattern sections, expanded tool access, a Swedish voice demonstration, and an extended quick reference table. The skill now covers the AI writing patterns that were most commonly missed in v1.0.0.

---

### Added

**New pattern sections (6):**

- **Pattern 11: Sycophantic openers and closers** — Detects and removes AI-typical praise phrases ("Vilken bra fråga!", "Hoppas det hjälper!") that immediately signal non-human origin.
- **Pattern 12: Filler phrases** — Targets phrases that add length without content: "i syfte att uppnå detta mål", "på grund av det faktum att", "i nuläget", "det är viktigt att notera att".
- **Pattern 13: Excessive hedging** — Addresses stacked qualifiers ("det kan möjligen argumenteras att detta eventuellt skulle kunna...") with guidance on expressing genuine uncertainty concisely instead.
- **Pattern 14: Knowledge-cutoff disclaimers** — Removes boilerplate like "baserat på tillgänglig information" and "inom ramen för mina kunskaper" that no human writer would include.
- **Pattern 15: Copula avoidance** — Promotes "utgör", "representerar", "fungerar som", "kan beskrivas som" to their own named section with explicit replacement guidance. Previously partially covered under Pattern 1 without a clear fix list.
- **Pattern 16: Bullet/emoji formatting as AI signal** — Addresses the pattern of AI structuring continuous reasoning as decorated bullet lists (💡 🚀 ✅) even when the content does not require list format.

**Voice section:**
- Added "Röst i praktiken: Innan och efter" — a Swedish before/after demonstrating the transformation from technically clean but voiceless text to text with an actual position. Previously the personality section stated principles without a Swedish demonstration.

**Tools:**
- Added `AskUserQuestion` to `allowed-tools`. The skill can now ask for text type when it is not clear from input, enabling correct register application before editing begins.

**Process:**
- Step 1 now explicitly prompts the skill to ask for text type if unclear, paired with the new AskUserQuestion capability.
- Self-critique loop updated to include the third question: "Vad saknar texten för att låta skriven av en verklig person med en verklig åsikt?" — carried over from a gap identified relative to the English humanizer skill.

**Quick reference table:**
- Extended with 10 new rows covering sycophancy, filler phrases, hedging, knowledge disclaimers, copula variants, and emoji/bullet patterns.

---

### Changed

- Version bumped from 1.0.0 to 2.0.0 (breaking in the sense of substantially expanded scope and changed process steps).
- Skill description updated to reflect the six new pattern categories.
- Process section renumbered from 9 steps to 10 steps.

---

### Not changed

- All 10 original patterns retained without modification.
- All four worked examples (affärsskrivande, rapportskrivande, artikel, sociala medier) retained unchanged.
- Register guidance section (four text types) retained unchanged.
- Core philosophy and Nordic voice principles unchanged.

---

## [1.0.0] - 2025-11-01

### Summary

Initial release. Swedish-specific humanizer skill covering 10 AI writing patterns common in professional Swedish text.

### Added

- Pattern 1: Significance inflation (signifikansuppblåsning)
- Pattern 2: Landscape and trend framing (landskap- och trenduppramning)
- Pattern 3: Participle phrases as fake analysis (participfraser som falsk analys)
- Pattern 4: Vague attributions (vaga attributioner)
- Pattern 5: Passive voice as false formality (passiv röst som falsk formalitet)
- Pattern 6: Nominalization overuse (nominaliseringsöverdrift)
- Pattern 7: Anglification imports (anglifieringsimporter)
- Pattern 8: Structural AI patterns (strukturella AI-mönster)
- Pattern 9: Negative parallelism, Swedish variant
- Pattern 10: Social media-specific patterns
- Register guidance for four text types: affärsskrivande, rapportskrivande, artiklar, sociala medier
- Four full worked examples with before/during/after structure
- Quick reference table with 19 swap pairs
- Nordic professional voice section
- Two-step self-critique process
