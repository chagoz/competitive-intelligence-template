# Analysis Rules

*The canonical rulebook for how the competitive intelligence system researches, scores, and classifies signals. Read before every digest, every reality check, and every competitive mission.*

*Last updated: August 13, 2026 · Maintained by [Your name] x Claude · v1.4*

---

## 1. Tier criteria

**Gate-keeper rule:** Tier 1 is determined by one criterion only, we have lost deals to them, or they are named by prospects in active evaluations. Everything else is secondary.

**Tier 1, Direct competitors.** Always include in every digest, even if nothing happened.
**Tier 2, Adjacent.** Related problem, similar buyer, or expanding toward our territory. Include only if genuinely eventful.
**Tier 3, Partnership or ecosystem lens.** Not a threat. Influences buyers from outside, or a potential data/integration partner.
**Tier 4, Niche or emerging.** Specialist in one dimension. Watch for escalation.
**Tier 5, Systemic alternatives.** Incumbent systems used instead of us by default (SAP, Excel).

**AI-native flag (cross-cutting).** A company can be AI-native and any tier. Criteria: AI is the primary differentiator (not a feature), targets buyers wanting to reduce human involvement, no established methodology credibility comparable to Tier 1.

**Escalation rule:** Any Tier 2/4/AI-native company named in a prospect conversation triggers a human gate review before tier change.

---

## 2. Research schema, two layers

**Layer 1, What they say.** LinkedIn company page, press releases, product pages, website. Scanned weekly, feeds the digest.
**Layer 2, What they actually do.** G2, Capterra, TrustRadius, help center, job postings, employee LinkedIn posts. Scanned monthly, feeds the reality check. Source URLs live in `evidence-registry.md`, gathered once, reused every cycle.

### 2.1 Recency filter, mandatory

**Only review/comment evidence dated within the current reality-check window counts as a new signal.**

- A G2, Capterra, or employee post must carry a visible date. If the date falls inside the current cycle (the period since the last reality check), it is a new finding.
- If a review or post is undated, or dated outside the current window, it does not get presented as new. It either (a) already belongs in the standing profile as established baseline evidence, or (b) is discarded as too old to be a signal.
- Never present old evidence with fresh-sounding language ("users report...") without the date attached. Every Layer 2 citation includes its date.

Why this matters: without a recency filter, an old review can read as if it happened this week, inflating the sense of new activity and eroding trust in the reality check over time.

### 2.2 Source honesty, mandatory

**Every claim is tagged with who said it, not just how certain we are.**

Two tags, always both present:

**Origin tag:**
`[Self-declared]`, the competitor's own words: press release, website, product page, sponsored/incentivized review
`[Independent, verified]`, a third party with no incentive to make the competitor look good: organic G2/Capterra review, analyst report, journalist coverage, named customer quote outside the competitor's own site

**Link:** whenever the source is public and linkable, the citation includes the URL. If no link is available, say so explicitly rather than omitting it silently.

**Format:**
`[Independent, verified], source name, dated (URL). Claim/finding text.`
`[Self-declared], source name (dated if known). Claim/finding text.`

Why this matters: an old certainty-only scale answered "how sure are we this is true" but silently conflated a press release with a G2 review, both could land as high-confidence. Origin and certainty are different questions. A self-declared claim can still be well-sourced; an independent claim can still be thin. Both dimensions need to be visible, not merged into one number.

**Certainty grades still apply, as a second, separate signal:**
Confirmed, high confidence this is accurate, regardless of origin
Reported, credible but not fully verified
Inferred, our own read, explicitly stated as opinion

### 2.3 Talk vs implement verdict

Talk, positioning, visibility, advisory, announcement with nothing shipped
Implement, a real product or process change, evidenced

### 2.4 The reality check gap format

[Their claim], origin tag, source (linked), certainty
[What evidence shows], origin tag, source (linked), certainty
Verdict: Talk or Implement

**The five founding rules** (extracted from an early competitive mission scan):
1. Separate the claim from the evidence, never blend into one sentence
2. Tag origin and certainty for each side independently
3. Apply the talk-vs-implement verdict once both sides are gathered
4. Find the gap, that divergence is the actual insight
5. State what the gap means for your company specifically, not just that it's unverified

---

## 3. Scoring system, two independent axes

**A single relevance score conflates two different questions. They are separate and both must be visible.**

### Axis 1, Talk vs Implement (is it real?)

Talk, announced or claimed, nothing verified as shipped
Implement, verified as actually running, shipped, or live

### Axis 2, Threat level (does it matter to us?)

Independent of Axis 1. Scored against the Theme Watches (see `watch-list.md` and the nine theme watches in `about-us.md`): Transparency, Flexibility, Network effect, Ease of use, Supplier engagement, Product improvement, Lower customer effort, Visibility at scale, Regulation coverage, Industry coverage, plus AI.

High (4-5), Strikes at a core differentiator or theme watch, active deal, or ICP. Act now.
Moderate (3), Worth monitoring.
Low (1-2), Note and move on.

**The critical rule: a pure announcement (Talk) can still score 4-5 on threat level if it strikes at a core theme watch.**

Example: a competitor announcing free-for-suppliers pricing is a high threat the moment it's said, waiting to see if they actually ship it before treating it seriously would mean reacting too late. Conversely, a fully shipped (Implement) feature can stay moderate or low if it's tangential to our segment.

**Display both axes together, always:** e.g. "Talk · High 4/5" or "Implement · Moderate 3/5", never collapse into a single score. The reader must see immediately whether something is real and whether it matters, as two separate facts.

**Scoring triggers for Axis 2 (threat level):**
- Competitor moves on a theme watch (especially transparency, network effect, lowest customer effort, visibility at scale) → 4-5, regardless of talk/implement status
- Competitor publishes on a regulation we cover → 4-5
- Competitor publishes on a regulation we do not cover → 2-3 (gap signal, flag to product)
- Competitor AI move touching transparency or auditability → 4-5
- Generic AI automation claims with no evidence → 2-3
- Competitor gets analyst coverage shaping enterprise shortlists → 4-5
- General thought leadership, culture, hiring content → 1-2

**Visibility line:** [Company] was [very active / active / quiet] this [period]. They mainly talked about [theme].

**Signal classification:**

| Threat score | Classification | Flag | "So what for us" | Editorial gate | Follow-up tracker |
|---|---|---|---|---|---|
| 5 | Existential | Yes | Always (callout) | Always | Yes |
| 4 | Strategic | Yes | Always (callout) | Proposed | Yes |
| 3 | Watch | No | Never | If escalating | Yes |
| 2 | Context | No | Never | No | No |
| 1 | Noise | No | Never | No | No |

Classification is driven by Axis 2 (threat) alone. Axis 1 (talk/implement) is always displayed alongside but never determines whether something gets flagged.

**Follow-up tracker status:**
Escalating, threat score rose since last cycle, or a Talk item became Implement
Still open, no change
Resolved, signal played out

---

## 4. OKR signal tags

Max 3 per document. Only when: (1) connects to an active OKR, (2) implies a concrete action this week/month. Signal relevance only, never assign team ownership.

---

## 5. Employee list rules

**Tier 1:** top 10 scored on seniority (1-3) + LinkedIn activity (1-3), minimum combined 4. Tie-breaker: product/GTM over culture/HR.
**Tier 2 and below:** C-level only.
**Storage:** Competitor Employee List database, related to Competitor Profiles.
**Review cadence:** full rescoring every 6 months.
**Monthly use:** scan tracked employees' recent posts, dated within the current cycle only, for reality-check-relevant signals (early product hints, hiring focus, team stability, sentiment, conference/analyst engagement, credibility checks, internal tooling reveals, tone shifts). Lightweight, no rescoring, just signal scanning feeding into the profile's evidence tables. Same recency filter applies (§2.1).

---

## 6. Editorial gate, human vs AI role

**Claude owns:** all research (both layers), Axis 1 and Axis 2 scoring, signal classification, flag proposals, "So what for us" drafts, key learning/3-things candidates with reasoning, monthly reality check execution, lost deal table pull, Slack post draft, contextual closing line options.

**The human owns:** final selection of top 3 (digest) or top 3 key learnings (monthly/quarterly review), full editorial authority, no constraint. Adjusting scores when internal context changes the picture. Escalation decisions between tiers. Employee list revalidation. Any claim requiring first-hand sales/CS/product knowledge. Picking or rewriting the Slack closing line.

**The principle:** Claude scores on market signals. The human corrects based on internal reality. The gate is a context injection step, not a validation step.

---

## 7. Workflow architecture, five skills

**Weekly digest**, Layer 1 only, enriched by the latest reality check's findings as context (not restated in full, referenced and acted on). Reads: latest reality check output + previous digest's follow-up tracker. Every finding shown with both Axis 1 (talk/implement) and Axis 2 (threat) visible. Outputs: digest page, 3 Slack options, tracker entry.

**Monthly/quarterly reality check**, a job with two outputs, not a single document. It is Layer 2 research (via the Evidence Registry) run on a monthly or quarterly cadence. It reads the previous cycle's competitor profiles and HubSpot lost deal data. It applies the recency filter (§2.1) and source honesty tags (§2.2) to everything it finds. It feeds two separate consumers:
1. **Competitor Profiles database**, every profile's evidence tables and changelog block get updated immediately (per §9, the always-true rule). This is the detailed, permanent record.
2. **Monthly/Quarterly Competitor Review**, a separate, short-form document. Summarises rather than repeats: what each competitor says vs what we can verify, plus a section on where the opportunity sits for our own key lines of work. Audience: Product, Sales, C-level. Short and sweet, this is a reading document, not a research archive. Voice and structure rules live in `language-guidelines.md`, Part 3.

**Competitor profile setup**, once per new competitor. Scans both layers, fetches help center, populates the Evidence Registry, proposes employee list candidates.

**Competitive mission**, open-scope ad hoc research. If the request is vague, ask for scope clarification before researching. If comparative analysis against the company is requested without the company-side input available, flag the gap and ask whether to proceed without it or wait for input, never guess.

**Dependency chain:**
```
Profile setup → Reality check (job) → Competitor Profiles database (updated immediately)
                                    → Monthly/Quarterly Competitor Review (short-form output)
                                         ↓
                                    Weekly digest (reads reality check findings as enrichment)
```

**Status (August 13, 2026):** the Monthly/Quarterly Competitor Review template is built (Zero Edition v3). Voice and structure tested against Language Guidelines v2 (observational tone, impact-first order, altitude rule, data-sufficiency gate). Theme Watch cohesion test against the full eleven-topic list is still pending, scheduled as its own dedicated research pass rather than folded into the template build, since a first test search confirmed generic content does not clear the source-honesty bar.

---

## 8. Lost deal data, HubSpot

**Field names and connection status are workspace-specific, read them from `configuration.md`, never hardcode them here.** This section defines the method, not the exact endpoint names.

**Approach:** pull from the structured lost-reason field first, competitor-relevant values look like "Chose competitor (solution fit)" or "Chose competitor (relationship or brand)". Cross-check against the free-text reason field for competitor name extraction the structured field misses.

**Meetings/calls cross-check:** query both meetings and calls objects, filtered by creation date within the period. Sum both objects, activity-type data is often sparse on meetings alone. Dedup any scheduling-tool pairs (e.g. Calendly) by datetime and title so the same booking doesn't count twice.

**Period:** always the previous calendar month (or quarter, if cadence moves to quarterly) relative to when the reality check runs.

**Table format:** one row, competitor names as columns with counts, zero entries excluded, Unknown column always present.

**If HubSpot isn't connected, or the fields in `configuration.md` aren't set:** run the reality check without this section and say so explicitly in the output. Never fail the whole reality check over a missing lost-deal pull.

---

## 9. The always-true rule

**Every discovery updates the Competitor Profiles database entry immediately, not at the next scheduled reality check.**

This applies regardless of which skill surfaced the finding: weekly digest, monthly reality check, a competitive mission, or an ad hoc HubSpot pull. If something new is learned about a competitor, the profile page is the single source of truth and must reflect it the same session it was found.

In practice:
- Update the Changelog block at the top with what changed and when
- Update the relevant evidence table row rather than only adding a new signal history line
- Update Strategic Relevance (both axes) if the new evidence changes the picture
- Update Last Updated
- Apply recency filter and source honesty tags to any new evidence added

Why this matters: dated findings that live only in a digest or a mission page go stale and get lost. The profile is the only place guaranteed to be read every time, by the next digest, by sales, by the next reality check. If it isn't updated there, it effectively didn't happen.

---

*[Your name] x Claude · August 5, 2026 · v1.4*
*v1.2 changes: two-axis scoring model (talk/implement independent from threat level), recency filter for Layer 2 evidence, source honesty tags (self-declared vs independent, with links), reality check reframed as a job feeding both the Competitor Profiles database and a new Monthly/Quarterly Competitor Review (template pending).*
*v1.3 changes: Monthly/Quarterly Competitor Review template shipped as Zero Edition v3. Data-sufficiency gate added as a named rule (insufficient Reality Check history triggers a dedicated fresh Theme Watch search rather than a stretched trend). Open item closed.*
*v1.4 changes: §8 HubSpot field names moved out to configuration.md, this document now defines the method rather than hardcoding workspace-specific field names. No hardcoded Notion IDs or HubSpot fields should live in any source-of-truth document, that's what makes this system portable across workspaces.*
