# Skills Index

*The five workflows that run this competitive intelligence system. Each has a corresponding skill file (SKILL.md) built for use in Claude, including Cowork. Full rules referenced by each skill live in `analysis-rules.md` and `language-guidelines.md`.*

*Last updated: August 17, 2026*

---

## Status

All five are built as ad hoc skills (manually triggered), each with a suggested cadence noted inside it. A second, Cowork-scheduled version of the two cadence-based skills (Weekly Digest, Monthly Reality Check) is planned separately, using a two-phase pattern: research and draft, stop, then a second step finishes the write once reviewed. The human gate is preserved in both versions, it is never skipped.

**No skill hardcodes a Notion page ID, HubSpot field name, or Slack channel.** Every live Notion page or database is found by searching for its title, confirmed once, then written to `configuration.md` so future runs don't repeat the search. This is what makes the skills portable across Notion connections, hardcoded IDs from one workspace are meaningless in another.

## The five skills

### 1. CI System Setup

**Trigger:** "set up competitive intelligence system", "build notion workspace", "run workspace init", "continue setup"
**Mode:** five steps, in order, each tracked in `configuration.md`'s Setup Progress so a re-run resumes from the right place: (1) read existing files and connector status, (2) build the Notion structure, (3) collect company/watch-list content, skipped automatically when it already exists, (4) hand off to Competitor Profile Setup for a first evidence batch, (5) suggest cadence and walk through Cowork scheduling. Safe to re-run any time, whether resuming an interrupted setup or repairing one piece later.
**Human gate:** every step 3 question is asked, never assumed. Every step 2 item shown and confirmed before creation. Step 4 always asks which competitors before running research. Step 5 never creates a scheduled task itself, it walks the user through doing it.
**Reads:** `configuration.md` (Setup Progress and values), `competitor-profile-template.md`, `evidence-registry.md`, plus whatever exists of `about-us.md`, `competitor-list.md`, `watch-list.md` to decide whether step 3 is needed.
**Writes:** step 2, any of the five required Notion items that don't exist yet, built blank, structure only. Step 3, for a new setup only, a company's own About Us, Competitor List, Watch List, and Language Guidelines. Updates to `configuration.md`'s Setup Progress after every step. Never writes competitor data or digest content directly, step 4 delegates that to Competitor Profile Setup, and step 5 never creates a schedule on its own.

### 2. Weekly Digest

**Trigger:** "run competitive digest", "run this week's digest", or explicitly "run a flash report on [topic]"
**Mode:** ad hoc. Suggested cadence: weekly, Tuesday morning. Produces either a Weekly Digest or a single-topic Flash Report, decided by explicit request or by an emergent pattern flagged mid-research, never switched silently in either direction.
**Human gate:** required, every run, on the top 3 selection, and separately on any switch between Digest and Flash Report structure.
**Reads:** `about-us.md`, `analysis-rules.md`, `language-guidelines.md` (Parts 1 and 2), `competitor-list.md`, `watch-list.md`, `configuration.md`, the latest Reality Check, the previous digest's follow-up tracker, and `flash-report-template.md` when producing a Flash Report.
**Writes:** the digest or Flash Report page, 3 Slack post options, a digest impact tracker entry after posting.

### 3. Monthly Reality Check

**Trigger:** "run monthly reality check", "run reality check for [month]"
**Mode:** ad hoc. Suggested cadence: monthly, first week, covering the previous calendar month.
**Human gate:** required, on the top 3 key learnings selection.
**Reads:** `analysis-rules.md`, `configuration.md`, Evidence Registry, Competitor Profiles database, Competitor Employee List, HubSpot lost-deal data (if configured).
**Writes:** updates every affected Competitor Profiles entry (the always-true rule), the Theme Watch activity matrix, the lost deal table, and the Monthly/Quarterly Competitor Review page once the top 3 are selected.

### 4. Competitor Profile Setup

**Trigger:** "set up competitor profile for [name]"
**Mode:** ad hoc only, once per new competitor, never scheduled.
**Human gate:** required, on tier placement and employee list validation.
**Reads:** `about-us.md`, `analysis-rules.md`, `configuration.md`.
**Writes:** a new Competitor Profiles database entry, new Evidence Registry entries, proposed employee list candidates.

### 5. Competitive Mission

**Trigger:** open-scope, e.g. "research Competitor X for the upcoming RFI"
**Mode:** always ad hoc, on demand, never scheduled by definition.
**Human gate:** scope clarification required if the request is vague. Never fabricate the company's own side of a comparison if it isn't available, flag the gap instead.
**Reads:** `about-us.md`, `analysis-rules.md`, `configuration.md`, relevant Competitor Profiles entries.
**Writes:** a standalone page, structure determined by the mission's own needs.

---

*[Your name] x Claude · August 17, 2026*
