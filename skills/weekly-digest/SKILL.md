---
name: competitive-weekly-digest
description: "Runs your company's weekly competitive intelligence digest, or a single-topic Flash Report when findings warrant it: scans competitors, proposes the week's top signals for the user's confirmation, writes the page to Notion, drafts Slack post options, and logs analytics after posting. Trigger phrases: 'run competitive digest', 'run this week's digest', 'weekly digest for [week]', or explicitly 'run a flash report on [topic]'. Also switches to Flash Report structure mid-run if research reveals a single-topic pattern, flagged and confirmed before switching, never silently. Ad hoc, manually triggered today. Suggested cadence: weekly, Tuesday morning."
---

# Weekly Competitive Digest

## Status and cadence

**Mode:** ad hoc. This skill runs when explicitly triggered, not on a schedule. Produces either a Weekly Digest or a Flash Report, decided per the Mode selection section below.
**Suggested cadence:** weekly, Tuesday morning. If it has been more than 8 days since the last digest, mention that when starting.
**Human gate:** required, every run. Never skip Phase 1 confirmation, even if the trigger message says "just run it." Never switch from Digest to Flash Report structure, or the reverse, without asking first.

## Mode selection

Two ways this skill ends up producing a Flash Report instead of a regular digest, both require confirmation before writing, neither happens silently.

**Explicit.** The trigger message names it directly, "run a flash report on [topic]." Skip straight to the Flash Report research approach below, no need to run a regular digest scan first.

**Emergent, discovered mid-run.** Running a normal digest, the research surfaces findings that consolidate around one question with real business consequences, the exact pattern `flash-report-template.md`'s three-condition test describes. When this happens: **stop, name what's happening, and ask.** "This week's research is consolidating around [topic] rather than spreading across competitors, looks like Flash Report territory rather than a regular digest. Want me to switch structure, or keep it as a regular digest with this as the lead story?" Do not decide this unilaterally in either direction, a real finding can legitimately be a strong digest lead story instead of a full Flash Report, that's the user's call, not a scoring threshold.

If Flash Report, everything below still applies (Phase 1 research and editorial gate, the same human gate, the same "before I write the closing lines" prompt) except Phase 2's structure, which comes from `flash-report-template.md` instead of `digest-template-structure.md`.

## Before anything else

Read from Project knowledge, these are static reference files, not Notion pages, no fetch needed: `analysis-rules.md`, `language-guidelines.md` (Part 1 system-wide, Part 2 Weekly Digest, not Part 3), `competitor-list.md`, `watch-list.md`.

If the trigger is explicitly a Flash Report, also read `flash-report-template.md` before starting research, its data-sufficiency gate and strategy brief rule shape what the research pass needs to gather, not just how it gets written up afterward.

Read `configuration.md` for the Competitive Intelligence home page title and the Slack channel. If `configuration.md` is missing, empty, or any value is marked unconfirmed, search Notion for the item by the name given in the file, show what was found, and ask for confirmation before proceeding. Once confirmed, write the confirmed value back into `configuration.md` so future runs don't repeat the search. Never fetch a Notion page by a remembered ID, workspace IDs are not portable across Notion connections.

## Phase 1, Research and editorial gate

1. Search existing digests under the Competitive Intelligence home page (title confirmed in `configuration.md`) to find the correct next digest number. Skip this for a Flash Report, it is named, not numbered, per `flash-report-template.md`.
2. Read the most recent 🧪 Reality Check page for the current truth baseline (search Notion for the latest one, do not scan competitors cold if a recent reality check exists).
3. Read the previous digest's "Next week watch list" as follow-up entry points.
4. **Regular digest:** scan Tier 1 competitors (always include, even if quiet). Scan Tier 2-4 only if genuinely eventful, per the gate-keeper rule in Analysis Rules §1.
   **Flash Report (explicit trigger):** research the named topic directly, mission-depth rather than a weekly scan. Check the data-sufficiency gate in `flash-report-template.md` before treating this as viable, fewer than three independently sourced findings means this is a digest lead story, not a Flash Report, say so and offer to fold it into a regular digest instead.
5. Score every finding on both axes (Talk/Implement, Threat level) per Analysis Rules §3. Apply the recency filter (§2.1) and source honesty tags (§2.2) to every Layer 2 claim.
6. **Check for the emergent Flash Report pattern here**, per Mode selection above, before proposing candidates. If findings are consolidating around one question rather than spreading across competitors, flag it now, don't wait until after the top 3 are chosen.
7. Propose 3-5 candidate signals for "3 things to remember," each with a one-line reason, plus any follow-up threads that have escalated.
8. **Stop. Present the candidates and wait for the user to confirm, swap, or override.** Do not write the Notion page until this is confirmed.
9. Once confirmed, ask: "Before I write the closing lines, anything specific from this week I should connect to? Office mood, weather, something that happened, a running joke?"

## Phase 2, Write, once Phase 1 is confirmed

### If a regular Weekly Digest

**Page title:** `Competitive Intelligence Digest #[N] · [Date]`
**Save under:** the Competitive Intelligence home page, title confirmed in `configuration.md`

**Structure, in order:** opening subtitle → "3 things to remember" (confirmed set) → This week in AI → Regulation watch → Follow-up tracker → Competitor pulse → Opportunities (Content angles / Sales and product signals) → Next week watch list → two closing lines → credits line.

Full section-by-section structure lives in Project knowledge, `digest-template-structure.md`.

### If a Flash Report

**Page title:** named, not numbered, e.g. `Flash Report · [Topic]`
**Save under:** the Competitive Intelligence home page, title confirmed in `configuration.md`. Does not take a digest number and does not break the weekly sequence, per `flash-report-template.md`.

**Structure:** the twelve-block order defined in `flash-report-template.md`, including the strategy brief (sections 3-4), the mandatory inline markers, and section 10 (open questions and what could not be confirmed), which is never optional for a Flash Report even when it would be skippable in a regular digest.

### Both cases

Run the full formatting pre-flight checklist from `language-guidelines.md` Part 1 before writing (grey italic subtitles, two-axis scores always shown together, source honesty tags, visual legends placed above tables, no em dashes, section symbols per the master table, double dividers between Tier 1 profiles where applicable).

## Slack post options

Generate 3 options for the channel confirmed in `configuration.md`.

Format: title line (digest number or Flash Report name, matching whichever was written), then 3 bullets (what they did + what it means for us, one sentence, second part max 4 words), then `Read more → [Notion link]`, then a closing line in one of three registers (cult quote / fake kung fu master / absurdist), calibrated to the week's sharpest signal. For a Flash Report, per its own voice rule, hold the closing line one notch more measured than a routine edition. Do not auto-post. Present the 3 options and let the user choose.

## Analytics tracking, after the Slack post is live

1. Search the configured Slack channel for the digest post.
2. Pull total reactions with emoji breakdown, thread reply count, timestamp.
3. Log to the Digest Impact Tracker database, title confirmed in `configuration.md`.
4. Prompt the user to add Notion view counts at 24h and 1 week when she has them.

## What this skill does not do

Does not select the top 3 itself. Does not skip the closing-line context prompt. Does not post to Slack directly. Does not switch between Digest and Flash Report structure without asking first, in either direction. Does not treat an explicit Flash Report request as automatically viable, the data-sufficiency gate still applies even when the topic was named directly. Does not run on its own schedule yet, a Cowork-scheduled version is planned separately and will handle the gate differently.
