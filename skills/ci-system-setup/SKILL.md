---
name: ci-system-setup
description: "Five-step setup and repair flow for the competitive intelligence system: check what exists, build the Notion structure, collect company/watch-list content, run the first competitor evidence batch, then suggest and walk through Cowork scheduling for the recurring skills. Each step is skippable if already done, tracked in configuration.md, so this is safe to re-run at any point without redoing finished work. Trigger phrases: 'set up competitive intelligence system', 'build notion workspace', 'run workspace init', 'continue setup'."
---

# Competitive Intelligence System Setup

*One skill, five steps, run in order. Each step checks whether it's already done before doing anything, so this is safe to re-run any time, whether that's resuming an interrupted setup or repairing one piece that broke later. Progress is tracked in `configuration.md`, under Setup Progress, always read and update that section first.*

## Status

**Mode:** ad hoc. Steps 1-2 run once per new Notion connection. Step 3 runs once per company, skipped automatically if content already exists. Steps 4-5 can each be re-run independently later, step 4 to add more competitors, step 5 to adjust cadence.
**Human gate:** every question in step 3 is asked, never assumed. Every item step 2 proposes to build gets shown and confirmed before creation. Step 4 never runs research without being told which competitors. Step 5 never creates a scheduled task itself, it walks the user through creating it.

---

## Before anything, read `configuration.md`'s Setup Progress section

It records which of the five steps are done, in progress, or not started. Start from the first incomplete step, don't restart finished ones, and don't skip ahead past an incomplete one, each step depends on the one before it actually being done, not just claimed to be done.

---

## STEP 1, Read existing files

Check three things and report back plainly before moving on:

1. **Project knowledge content.** Does `about-us.md`, `competitor-list.md`, and `watch-list.md` already exist with real, specific content, not placeholder templates?
2. **Notion structure.** Search for each of the five items listed in `configuration.md` (Competitive Intelligence home, Competitor Profiles, Competitor Employee List, Digest Impact Tracker, Evidence Registry). Note found, missing, or found-but-wrong-type for each.
3. **Connectors.** Confirm Notion is connected and can be searched. Confirm Slack is connected if a channel is set in `configuration.md`. Confirm HubSpot is connected if fields are set in `configuration.md`.

Write the result to Setup Progress in `configuration.md` before moving to step 2. This step never creates or writes anything except that status update.

---

## STEP 2, Build file infrastructure

*Runs after step 1, regardless of whether content exists yet. Test the plumbing before spending time on content questions, a broken connector should fail here, fast, not four questions into step 3.*

**Is:** structure only. Creates whichever of the five required Notion items step 1 found missing, blank, matching the shapes below. Writes confirmed titles back to `configuration.md`.

**Isn't:** content. Never adds a competitor, a digest, an evidence source, or any row of real data. That's step 4, and it's a separate hand-off, not something this step does itself.

### The five items, checked one at a time

For each item step 1 found missing: show the proposed shape and wait for confirmation before creating it. For each item step 1 already found: confirm it matches the expected type and move on, don't touch it.

**1. Competitive Intelligence home page**
Type: Markdown page. Shape if creating: a hub page with a short description and placeholder links to the four items below.

**2. Competitor Profiles**
Type: Database. Shape if creating, propose these fields, wait for confirmation before creating:
Name (title) · Category (text) · Website (URL) · LinkedIn (URL) · AI-native (checkbox) · Tier (select: 1-5) · Tier rationale (text) · Talk/Implement (select) · Threat score (select: 1-5) · Last updated (date) · Tracked Employees (relation to Competitor Employee List)

Zero rows on creation. The tables inside each competitor's row, What they claim, What they actually do, Signal history, are page content written per-row later by step 4 and Monthly Reality Check, not database fields, don't try to model them as properties.

If an old page or database with a similar name already exists: leave it exactly as it is, don't open it, don't read it, don't archive it. Create the new database alongside it and record the new one's title in `configuration.md`. Flag the old item's existence in the output so the user knows it's there, but do nothing to it.

**3. Competitor Employee List**
Type: Database. Shape if creating: Name (title) · Company (relation to Competitor Profiles) · Role (text) · Seniority score (select: 1-3) · LinkedIn activity score (select: 1-3) · Combined score (formula or number) · LinkedIn URL (URL) · Last reviewed (date). Zero rows on creation.

**4. Digest Impact Tracker**
Type: Database. Shape if creating: Digest (title) · Date posted (date) · Total reactions (number) · Emoji breakdown (text) · Thread replies (number) · Notion views 24h (number) · Notion views 1 week (number) · Link to digest (URL). Zero rows on creation.

**5. Evidence Registry**
Type: Database. Shape if creating: Company (relation to Competitor Profiles) · Source type (select: Help center, G2, Capterra, TrustRadius, Careers/Job board, Press/Newsroom, LinkedIn, Product pages, Pricing page) · URL (URL) · Priority (select: Critical, High, Medium) · Check frequency (select: Weekly, Monthly) · Last checked (date) · Notes (text). Zero rows on creation.

### Confirmation flow, for every item being created

1. Show the item's proposed type and full field list.
2. Wait for explicit confirmation. Never create on an assumption, even if the shape is copied directly from a template file.
3. On confirmation, create it blank.
4. Write its confirmed title, type, and status back into `configuration.md`.
5. Move to the next item. Don't batch-confirm all five at once unless explicitly asked to.

**End of step 2:** update Setup Progress in `configuration.md`. Do not proceed to step 3 until every item is either confirmed-existing or confirmed-created, an incomplete step 2 means step 4's research has nowhere reliable to write.

---

## STEP 3, Content

*Skipped automatically if step 1 already found real content in `about-us.md`, `competitor-list.md`, and `watch-list.md`, an already-established practice's case. Runs in full for a genuinely new setup.*

### The four setup questions, asked in sequence

1. **Who is your company?** Category, value drivers, differentiators, ICP, priorities. Populates About Us. Do not proceed to question 2 until this is answered, tier reasoning downstream depends on knowing what the company competes on.
2. **Who are your competitors, organised by tier?** Ask what "Tier 1" means for their business specifically (the reference definition is "we have lost deals to them, or they are named by prospects", check whether that gate-keeper rule fits their business or needs adapting). Populates the tier list.
3. **What are your watch list topics?** Two to four topic areas maximum, more creates noise. Ask what the primary competitive battleground is right now, and what external forces most affect buyers. Populates the watch list.
4. **What is your language or copy reference?** Existing brand voice docs, tone examples, words to avoid. If nothing exists yet, offer to derive a starting point from a few examples of content already liked. Populates language guidelines.

### Step 3 output

Four new reference documents, written in the structure of the existing templates but populated entirely with the user's answers, never with your company's content as a default or placeholder.

**End of step 3:** update Setup Progress. Does not guess at any answer to save time, does not run again once these documents exist and are confirmed.

---

## STEP 4, First competitor evidence batch

*Hand-off, not a rebuild. This step does not do competitor research itself, that's Competitor Profile Setup's job. This step prompts, scopes, and delegates.*

Once step 2's structure exists and step 3's competitor list is available (either freshly written or already existing): show the Tier 1 list and ask whether to run Competitor Profile Setup now, on the full Tier 1 list, or on a smaller first batch the user picks. **Never assume the full list, always ask, skipping this step silently is the most common way this setup goes wrong, structure gets built but no data ever gets requested, so be explicit here rather than defaulting quietly.**

For each competitor confirmed: trigger Competitor Profile Setup, which does the actual scanning, scoring, and Evidence Registry population. This step's job ends at the hand-off and confirming the batch completed, everything downstream, digests, reality checks, missions, reads from what Competitor Profile Setup writes here.

**End of step 4:** update Setup Progress with which competitors have been processed. This step can be re-run later for any competitor not yet covered, it doesn't have to happen all at once.

---

## STEP 5, Suggest cadence, walk through scheduling

*Only after steps 1-4 are far enough along that running the recurring skills would actually produce something real, at minimum step 2 done and at least one competitor processed in step 4.*

Suggest cadences based on what's already defined: Weekly Digest, weekly, matching the day noted in `weekly-digest`'s SKILL.md. Monthly Reality Check, monthly, first week, covering the previous calendar month. Ask if these fit or if the user wants different timing.

**This step does not create the scheduled task itself.** Walk the user through doing it: open Cowork, use the Scheduled tab or `/schedule` in a session, select the skill and the cadence just agreed on, confirm. Go one skill at a time, don't rush through both at once, this is also how the user discovers what the system can do on a recurring basis, not just a mechanical setup step.

**End of step 5:** update Setup Progress to reflect which recurring tasks are now scheduled. This step can be revisited any time cadence needs to change.

---

## What this skill never does, any step

Does not run on a schedule itself. Does not guess at content to save time. Does not touch existing Notion items it wasn't asked to build. Does not write competitor data or digest content directly, step 4 delegates that. Does not create a Cowork scheduled task on the user's behalf, step 5 walks them through it instead.
