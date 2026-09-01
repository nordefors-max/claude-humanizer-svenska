# Changelog

All notable changes to `humanizer-svenska` are documented here.

Format follows [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).  
Versioning follows [Semantic Versioning](https://semver.org/).

---

## [3.0.0] - 2026-09-01

### Summary

Aligns the skill with [blader/humanizer](https://github.com/blader/humanizer) 2.11.2. Thirteen new pattern sections (17–29), a fact-preservation rule, a false-positive guard, sample-based voice matching, and file/embedded output modes. Swedish typography (tankstreck, citattecken, rubriker) gets its own section instead of a direct port of the English dash rule.

### Added

**Fact preservation (breaking change in behaviour):**
- "Din uppgift" now has "Behåll varje påstående" and "Hitta inte på fakta": no name, number, date, quote, or source may be added unless it comes from the source text or the user. Previously the skill's own examples demonstrated inventing sources and figures.
- Process step 10: "Har omskrivningen lagt till eller tagit bort någon uppgift, ett namn, en siffra, ett datum, ett citat, en källa eller en rangordning?"
- Note above the worked examples that their figures and sources are illustrative.

**New pattern sections (13):**
- **17. Säljspråk** — "ledande", "unik", "i världsklass", "sömlös", "vi brinner för".
- **18. Överanvända AI-ord** — consolidated Swedish list: stacked "dessutom/vidare/därtill", "belysa", "robust", "landskap", "samspel", "väv", etc.
- **19. Synonymväxling och upprepade meningsstarter** — "företaget/bolaget/organisationen/aktören"; "Vi... Vi... Vi...".
- **20. Falska spann** — "från strategi till genomförande, från insikt till handling".
- **21. Tankstreck, citattecken och versaler** — em dash (—) is never Swedish typography; en dash (–) is correct but AI overuses it as parenthetical insertion; English “…” quotes and Title Case Headings are tells. Ranges and replikstreck are never touched.
- **22. Låtsad djupare sanning** — "den egentliga frågan är", "i grund och botten".
- **23. Annonsering av nästa poäng** — "låt oss dyka ner i", "här är vad du behöver veta".
- **24. Rubrik som upprepas i första meningen.**
- **25. Forcerade punchlines och dramatiska fragment.**
- **26. Formelartade talesätt** — "data är den nya oljan", "X är det nya Y".
- **27. Låtsad uppriktighet** — "Ärligt talat?", "Här är grejen:".
- **28. Svar på invändningar ingen gjort** — "jag säger inte att", "missförstå mig rätt".
- **29. Avfärdande av påhittade alternativ** — "ett frestande alternativ vore".

**New sections:**
- **Matcha skribentens röst** — analyse a writing sample first; the sample overrides the style rules, including dash rate.
- **Kontrollera falska positiva** — what not to flag (single tankstreck, Swedish curly quotes, passive voice in myndighetstext/avtal, one short sentence, real disclaimers, real alternatives, quoted text, compounds) and human details to keep.
- **Så returnerar du resultatet** — pasted-text (default), file mode (only final text written, prose only), embedded mode (final text only).

**Existing patterns extended:**
- Pattern 4: name-dropping ("uppmärksammats av DI, SvD, Breakit och Resumé") and an explicit "hitta aldrig på en källa".
- Pattern 11: chatbot leftovers ("Vill du att jag utvecklar...", "Ska jag fortsätta?").
- Pattern 14: speculative gap-fill ("hon växte troligen upp i...").

**Quick reference table:** 19 new rows.

### Changed

- Version 2.0.0 → 3.0.0.
- Intro and description rewritten around "rewrite without changing what it says".
- "Tillför röst" is now conditional: personality for articles, posts, mail, proposals; neutral for reports, contracts, myndighetstext.
- Pattern 1 and pattern 4 "Efter" examples no longer invent a percentage or a Kantar Sifo report; pattern 14 no longer invents an IARB forecast.
- Example 3's final version dropped "Det är inte en trend, det är en omfördelning", which violated the skill's own pattern 9.
- Process renumbered from 10 to 12 steps; "Utdataformat" folded into "Så returnerar du resultatet".

### Not changed

- Patterns 1–16 keep their numbers, so older references still hold.
- Register guidance, the four worked examples (apart from the one line above), and the Nordic voice principles.

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
