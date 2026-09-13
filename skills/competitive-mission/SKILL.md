---
name: competitive-mission
description: "Open-scope ad hoc competitive research for a specific question that doesn't fit the weekly or monthly cadence, e.g. 'research Competitor X for the upcoming RFI' or 'what did competitors do with AI in H1'. Produces a standalone Notion page, structure determined by the mission's own needs. Always ad hoc, on demand, never scheduled."
---

# Competitive Mission

## Status and cadence

**Mode:** ad hoc, on demand, always a live conversation. Never a candidate for scheduling; by definition the request is not known in advance.

## The defining rules

**If the request is vague, ask for scope clarification before researching.** Never guess at what good looks like for an undefined ask.

**If comparative analysis against your company is requested and the necessary input on your side is not available, flag the gap explicitly and ask whether to proceed without it or wait. Never fabricate your own side of a comparison.**

*What is available, as of September 8, 2026: about-us.md holds Product direction, three directions and five explicit non-goals, which is what the bets pillar measures distance against, and buyer archetypes for the sourcing side with their documented frictions, which are standing research questions per section 2.9. What is still missing: the investment side, which has no documented archetypes, so any investment-side reading has no roles to attach evidence to.*

*One standing constraint that changes what a mission can scope: public user voice is tested and confirmed absent in this category. Reviewer role and company size stay usable where reviews exist, but any method resting on forums, peer communities or broad public sentiment has a very low ceiling here. Scope accordingly rather than discovering it mid-run.*

*Check the file rather than trusting this note, since it will go stale.*

---

## Scoping, before any research starts

Four things get agreed in the conversation and written at the top of the output. A mission without them produces research nobody asked for.

**1. The question.** One sentence the output has to answer. Not a topic. "What did competitors do with AI in H1" is a topic; "is anyone shipping AI that a prospect could verify" is a question.

**2. Depth per company, stated as a number.** Where a request names primary and secondary companies, say what each depth actually means before starting:

- **Deep**, roughly 8 to 15 sources per company. Both layers, help centre, careers, reviews with the incentivized flag checked, press descriptor and boilerplate, public register where one exists.
- **Light**, roughly 3 to 5 sources. Layer 1 plus one Layer 2 check, usually reviews or careers.
- Go deeper on a light company only when something surfaces that earns it, and say in the output that you did.

**3. The stopping rule.** An open-scope mission has no natural end. Agree one upfront and honour it: a number of sources, a set of questions answered, or a fixed time box. State which was used, and whether it was reached or the research ran out first. Those are different outcomes and the reader should know which happened.

**4. Who reads it**, which decides voice. Part 2 for a working audience, Part 3 for Product, Sales or C-level.

---

## Before anything else

Read from Project knowledge, scoped to what the mission needs rather than all of it by default:

- about-us.md, always. It is the lens, and it owns the theme watch list, the regulation coverage status, the loss patterns, and the Product direction the bets pillar measures against
- analysis-rules.md. A mission is not exempt from the recency filter, the absence bar in 2.2.1, source honesty tags, corporate events, the market lens, the bets pillar or the archetype frictions in 2.9
- evidence-registry.md for source types and their priorities
- configuration.md for the Competitive Intelligence home page and the Competitor Profiles database

For whatever competitors the mission touches, read their Competitor Profiles entries rather than re-researching from scratch. Anything new learned is written back to the profile in the same session, per section 9, the always-true rule. That applies to a mission exactly as it applies to a scheduled run.

**Do not attempt to write to configuration.md.** Report the delta and ask the user to update it. **No skill configures itself.**

---

## The bets pillar, where a mission asks about direction

Any mission asking where competitors are going, what they are betting on, or where the market is moving uses analysis-rules.md section 2.8 rather than inventing a framing.

Three tags per company, all mandatory: evidence class, conviction, distance from us. **A bet missing any tag is excluded, not shown partial.** Where our own direction is silent on a dimension, the silence is logged for Product rather than guessed. A bet landing on one of Product's open questions is flagged, not scored.

**Report exclusions rather than omitting them.** A competitor whose bet cannot be evidenced at all is a finding about that company, and a section that silently drops it reads as an oversight.

---

## Synthesis, where the mission covers several companies

A mission across many competitors is not nine profiles stapled together. The output is organised by the question, with companies used as evidence underneath it.

**Working method.** Research company by company, then reorganise by finding before writing. If a section can only be written as "here is what each company did", the synthesis has not happened yet.

**Say how many companies support each finding.** One company is an anecdote, three is a pattern, and the reader cannot tell which unless you say.

**Where coverage is uneven, say so in the section where it appears**, not in a footnote. Absence of evidence is reported as a finding with its search trail, and it meets the bar in section 2.2.1 before it is written as confirmed: one authoritative path for a bounded claim, two named paths for an unbounded one, with the scope written into the claim.

---

## Output

A standalone Notion page under the Competitive Intelligence home page, structure determined by the mission itself rather than a fixed template.

**Where the mission consolidates around one question with a live business consequence, use the Flash Report shape** rather than inventing one: templates/flash-report-template.md. It carries a data-sufficiency gate: an answer resting on fewer than three independently sourced findings is a digest lead story, not a Flash Report.

Apply language-guidelines.md Part 1 regardless of structure: source honesty, recency, section header emoji and never an inline marker as one, visual legends above tables, no em dashes.

**Open the page with the scope block**: the question, depth per company, the stopping rule and whether it was reached, and what could not be reached. That block is what makes the rest of the page trustworthy.

**After any write, fetch the page back and inspect the returned markdown**, then run the Part 1 pre-flight against what came back and state which items passed. Rendering correctly and complying are different checks and passing one does not imply the other.

---

## What this skill does not do

- Does not assume a request is well-scoped just because it sounds specific.
- Does not invent your own side of a comparison as a data point to complete a comparison.
- Does not carry method inline. The window, the absence bar, scoring, bets and frictions live in analysis-rules.md and are referenced, never restated.
- Does not publish a partial bet, and does not omit an excluded one.
- Does not write an absence as confirmed without meeting section 2.2.1.
- Does not scope research that rests on public user voice without saying what its ceiling is.
- Does not skip the profile write-back.
- Does not write its own configuration.
- Does not run on a schedule.
