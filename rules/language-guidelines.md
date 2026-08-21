# Language Guidelines

*How every Competitive Intelligence document is written and formatted. Apply without exception.*

*Last updated: August 19, 2026 · v2.1*

---

## PART 1, SYSTEM-WIDE

*Applies to every document type: Weekly Digest, Flash Report, Quarterly Review, Competitor Profiles.*

### Audience pool

The full readership across Competitive Intelligence outputs spans four groups: **C-level and management**, **Sustainability specialists and deeper experts**, **Product and Marketing**, and **general company readers** with less category fluency. No single document serves all four equally. Each document type states, in its own opening note, which slice of this pool it is written for and what that reader needs. That persona note lives at the top of each tier below, not here.

### The Slack message rule

The Slack post is not a teaser. It delivers the core message on its own, efficiently, so someone with thirty seconds gets the actual point of the week, not just curiosity about it. The linked document goes deeper, proof, nuance, full picture, it does not hold the headline hostage to earn a click.

Bad: "Big week for competitors. More inside."
Good: "[Competitor A]'s own users just handed us two sales talking points. Read more →"

No manufactured suspense. Short, driven, self-contained.

### Symbol system, one symbol one meaning

**Every symbol used across every document type is defined once, here, and nowhere else.** A profile, a digest, a Flash Report, or any future document type all draw from this same table. If a section needs a symbol that isn't listed, add it here first, then use it, don't improvise one locally and let a future session guess at what it meant.

| Symbol | Means | Used on |
|---|---|---|
| 🔄 | What changed since last time | Changelog |
| 🎯 | The headline, what to remember | Three things to remember, only this |
| 🖼️ | The map, establishing terms before reporting | Strategy brief, vocabulary tables |
| 🗣️ | Their words, Layer 1 | What they claim |
| 🔧 | Verified evidence, Layer 2 | What they actually do, what users say |
| 🕵️ | The gap between claim and evidence | Reality check |
| ➖ | Market white space, where nobody is playing | Gap sections |
| 📈 | Dated log | Signal history |
| 💚 | Our documented advantage | Our wins |
| ⚠️ | Our exposure, or where not to fight | Where they are ahead |
| 🧭 | Where overlap sits and where it stops | Our angle, short-form profiles |
| ⚡ | What would move a tier | Escalation trigger |
| 🤝 | Partnership or ecosystem lens | Tier 3 entries |
| 🤖 | AI | Topic section |
| 📊 | Regulation | Topic section |
| 💥 | Competitor activity roundup | Competitor pulse, what is hot elsewhere |
| 💪 | Opportunities | Content angles, sales and product signals |
| 🔍 | Still open, still tracked | Follow-up tracker, open questions |

**Inline markers, not headers:** 🔥 flame-level signal · 🔴 High 4-5, 🟡 Moderate 3, ⚪ Low 1-2 · 🗣️ Talk, 🔧 Implement (same symbols as above, same underlying meaning, self-reported vs verified) · 🚩 decision awaiting a human, ✅ decision closed · ✏️ correction after publication · 🗑️ retired.

**Two deliberate choices, worth keeping rather than splitting further:** 🔍 and 💥 each cover two labels (Follow-up tracker / Open questions, Competitor pulse / What is hot elsewhere), because those pairs are genuinely the same family of content, not two different things that happen to share a symbol. Origin tags stay as text, `[Self-declared]` and `[Independent, verified]`, never compressed into a glyph, that distinction carries too much weight to risk being misread.

**Why this lives in Part 1 and not inside a specific document's section:** a rule scoped to one document type only governs that document type. This system was originally written inside the Weekly Digest section and, predictably, never applied anywhere else, competitor profiles and other document types improvised their own symbols with no rule to check against. Every template and structure document should cross-reference this table rather than define its own.

### Notion formatting pre-flight

Run before writing any Notion content, no exceptions:

- Grey italic on all subtitles and legend lines
- "So what for us" / impact callouts use a blue callout, action-required icon
- Two-axis scores always shown together, never collapsed
- Source honesty tag on every Layer 2 claim, linked when available
- Dates on every Layer 2 citation, no evidence presented as new without its date visible
- OKR tags: blue inline text inside callouts, grey inline text outside callouts
- Flame-level sentence: highlight the key sentence only
- Quiet competitors: entire section in grey, no scoring, no bullets, one line
- Section title symbols on every header, per the master symbol system above, never improvised locally
- Visual language legend placed directly above any colour/symbol system, no exceptions
- No em dashes anywhere, scan before saving
- TOC block reminder, cannot be inserted via API in Notion

If any item is unchecked, the document is not finished.

### Four colour registers

| Colour | Meaning | Used on |
|---|---|---|
| Blue callout | Impact / action | "So what for us" and Quarterly impact statements |
| Blue inline text | OKR signal inside a callout | OKR tags inside blue callouts |
| Grey inline text | Low urgency / meta | Subtitles, quiet sections, legends |
| Yellow highlight | New signal, flag for attention | Key sentence, unverified flags |

### Visual language legend rule

Any table, matrix, or element using colour codes or symbols gets a grey italic legend directly above it, before the element, not below. Reading order: know the code, then read the table.

Example score legend: Talk (announced, not shipped) · Implement (verified, shipped) · High (4-5) · Moderate (3) · Low (1-2)

Example source legend: Self-declared = competitor's own words · Independent, verified = third party with no incentive to favour them

Example activity legend: Active this month · Minor signal · No activity · Direct threat to our positioning

Apply this rule to: tables with emoji columns, scoring matrices, follow-up tracker status columns, any custom visual language introduced in a document.

### Recency filter

Only evidence dated within the current research cycle presents as new. Older evidence stays in the standing profile, referenced, not repeated. Full rule: `analysis-rules.md` §2.1.

Bad: "Users report the setup is slow." (no date, reads as current)
Good: "A March 2026 G2 review flagged setup speed. No newer reviews raise it."

### Source honesty

Every claim tagged Self-declared (competitor's own words) or Independent, verified (third party, no incentive to favour them), dated, linked when available. Full rule: `analysis-rules.md` §2.2.

Bad: "[Competitor A] delivers 180% ROI."
Good: Self-declared, [Competitor A] website, citing an unlocated Verdantix study: "180% ROI, 8-month breakeven."

### Words to avoid

| Avoid | Use instead |
|---|---|
| Leverage | Use |
| Holistic | Specific alternative |
| End-to-end | Name the actual scope |
| Seamless | Describe what actually happens |
| Empower | Name the concrete action |
| Synergy | Avoid entirely |
| AI-powered / AI-driven | Describe what the AI actually does |
| Monitoring (with AI) | Identifies, surfaces, flags, screens |
| Game-changer | Describe the actual change |
| Leading (self-declared) | Use specific proof points |

No em dashes. Anywhere. Ever.

### AI language

Describe what the AI does. Never echo competitor hype.

Bad: "Their cutting-edge AI transforms compliance workflows."
Good: "Their AI parses bills of materials and extracts material data."

### Scoring system, two axes, always shown together

Full model: `analysis-rules.md` §3.

Axis 1, is it real? Talk (announced only) vs Implement (verified shipped).
Axis 2, does it matter? High (4-5), Moderate (3), Low (1-2). Independent of Axis 1, a pure announcement can still be High if it strikes a core theme watch.

Always displayed together, never collapsed into one number.

### OKR signal tags

Max 3 per document. Signal relevance only, never assign team ownership.

---

## PART 2, WEEKLY DIGEST

*Who this is for: three readers, each with a different failure mode.*

**C-level and management.** Reads fast, needs proof and understanding in the same glance. Fails them if the point is buried under narrative, or a signal doesn't visibly stand out from routine noise.

**Sustainability specialists and deeper experts.** Fine reading more, but organised by proof, not narrative. Fails them if a claim appears without its source and date, or gets oversimplified past what someone who already knows the category needs.

**Product and Marketing.** Enthusiastic but scans rather than reads start to finish, parsing for opportunity. Fails them if the Opportunities section isn't visually distinct enough to catch a scanning eye, or a usable insight is buried inside a competitor paragraph instead of surfaced.

### Voice and structure

Direct, fast, built for a Slack-speed read. Event and source first, "so what for us" last. This is an internal working document, the reader wants the point fast, not softened.

Example: "[Competitor A] launched a Help Center. So what for us: continuous visibility should already be part of our sales conversation."

One idea per sentence. No compound sentences. Split at commas connecting independent thoughts.

Plain regulation names. Every regulation gets a one-line plain language gloss on first use.

Short is the default. 100 words max per competitor section on a quiet week. Longer only for a direct threat.

Enrichment, not repetition. References and acts on Reality Check findings, does not re-explain them at the same depth.

Bad: restating the full gap story at reality-check depth inside the digest.
Good: "[Competitor A]'s two user-confirmed gaps (see Reality Check #1) are worth surfacing in sales conversations this week."

### Section symbols, digest-specific subset

*Drawn from the master symbol system in Part 1, this is which of those symbols apply to a Weekly Digest specifically, not a separate definition. If a digest needs a symbol not listed here, check Part 1 before inventing one.*

| Section | Symbol |
|---|---|
| This week in AI | 🤖 |
| Regulation watch | 📊 |
| Follow-up tracker | 🔍 |
| Competitor pulse | 💥 |
| Opportunities | 💪 |
| Summer / seasonal edition | 🌲 (one-off, not in the master table, this one is a seasonal exception rather than a recurring structural symbol) |

Section subtitles always grey italic.

### Competitor sections, three formats

**Active competitor:**
```
### [Company name]
[Company] was [very active / active] in [period]. They mainly talked about [theme].
Talk · High/Moderate/Low [score]/5  OR  Implement · High/Moderate/Low [score]/5
[Bullet points, 3 max, each carrying a source honesty tag if citing Layer 2 evidence]
```

**Quiet competitor:** entire section grey, one line: "No significant update in [period]."

**Flame-level signal:** highlight the key sentence, then the "So what for us" callout.

### "So what for us" block

Only on high-threat flagged signals. Fixed title, never varied. Blue callout, two to three sentences, OKR tag on the last line.

### Competitor header table

Two-row format only. Row 1: Category, Website, LinkedIn, AI-native, Tier rationale. Row 2: values. Never line-by-line key/value pairs.

### Closing

Two closing lines, grey italic, last before signature. Double divider between every Tier 1 profile.

### Slack bullet formula

Each bullet: what they did plus what it means for us, one sentence. Second part four words max.

### Flash Report

When findings consolidate around one topic with direct business consequences, the edition is renamed a Flash Report rather than numbered. Keeps the Digest's speed and directness, still Slack-bound, but given the higher stakes, holds a slightly more measured tone, closer to "here's what we found and why it matters" than a routine quick take.

Full section structure, the strategy brief rule, and the data-sufficiency gate for single-topic editions live in `flash-report-template.md`, not here. This paragraph covers when to use the format, that document covers how to build it.

---

## PART 3, QUARTERLY REVIEW

*Who this is for: two readers.*

**C-level and management, primary.** Same fast-reading need as the Digest, but the proof bar is higher since this document justifies a strategic read, not a weekly pulse check.

**Company-wide, secondary.** May be meeting a concept like a specific regulation or a Theme Watch for the first time. Needs a first-use gloss where the Digest can assume fluency. This sits in tension with the C-level need for density, a light glossary touch on first use resolves most of it without breaking the primary read.

### Voice, observation not instruction

The reader is Product, Sales, or C-level. The goal is to nurture a decision, not hand one down. No imperative verbs opening an item (Investigate, Decide, Confirm, Publish). Open with what was observed, let the implication sit there rather than stating the conclusion for the reader.

Bad: "Investigate the Buyer A and Buyer B feedback as a product signal, not a messaging problem."
Good: "Two buyers, two deals, the same doubt. Buyer A and Buyer B independently raised versions of the same concern this quarter, one on effort reduction, one on methodology reliability, both claims we lead with."

### Structure, reversed from the Digest

Impact first, proof at the close. Shape: impact statement, one or two sentences of context, then a proof line, source-honesty tagged, dated and linked.

Bad: leading with the event ("[Competitor A] hired a Chief Strategy and Innovation Officer") and ending with why it matters.
Good: leading with the implication ("Two competitors are quietly repositioning above us") and closing with the named hire and date as the proof.

### Altitude rule

Every claim answers "what does this mean for the business or buyer," not "what does the feature do." If the sentence can't complete that in one clause, it stays in the tactical record instead.

Bad: "No in-platform supplier dialogue."
Good: "Buyers are asking for something we already offer and a Tier 1 competitor doesn't, worth confirming this is said explicitly in sales conversations."

### Data-sufficiency gate

If there isn't enough Reality Check history for a genuine time comparison, don't stretch two points into a trend. Run a dedicated fresh search against the Theme Watch list itself, topic by topic, not company by company, to establish an honest current-state baseline instead.

Bad: calling two Reality Checks a "four-month view."
Good: "Two Reality Checks exist so far, not enough for a trend line. This section reflects a fresh baseline search instead."

### Opportunities section

Numbered, divider between each item. Team code-tag kept, decoupled from any directive verb. Frame as observation plus why it matters, never as an instruction.

---

*[Your name] x Claude · August 19, 2026 · v2.1*
*v2.1 changes: added a single master symbol system to Part 1 (one symbol, one meaning, applies to every document type). Fixes a real drift, the previous symbol table lived only inside Part 2 (Weekly Digest), so it never governed Competitor Profiles or any other document type, each improvised its own vocabulary with nothing to check against. Part 2's table is now explicitly a subset of Part 1's, not a separate definition.*
