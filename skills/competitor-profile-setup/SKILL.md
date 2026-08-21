---
name: competitor-profile-setup
description: "Sets up a full initial competitor profile for a new competitor: scans both research layers, fetches the help center, populates the Evidence Registry, proposes tier placement, and proposes employee list candidates for the user's validation. Trigger phrase: 'set up competitor profile for [name]'. Ad hoc only, once per new competitor, never scheduled."
---

# Competitor Profile Setup

## Status and cadence

**Mode:** ad hoc only. Runs once per new competitor, when a new one is identified. Not a candidate for scheduling, there is nothing recurring here.
**Human gate:** required. the user confirms tier placement and validates the proposed employee list before either is saved.

## Before anything else

Read from Project knowledge: `about-us.md` (the lens every competitor gets judged through), `analysis-rules.md` (§1 tier criteria and gate-keeper rule, §2 research schema, §5 employee list rules).

Read `configuration.md` for the Competitor Profiles database and Evidence Registry page. If either is missing or unconfirmed, search Notion by the name given in the file, show what was found, and ask for confirmation before writing. Write confirmed values back into `configuration.md`.

## Research, both layers

**Layer 1, what they say.** LinkedIn company page, press releases, product pages, website.
**Layer 2, what they actually do.** Help center (mandatory: if it's documented there, it shipped), G2, Capterra, TrustRadius, job postings.

## Tier placement

Apply the gate-keeper rule: Tier 1 only if your company has lost deals to them, or they are named by prospects in active evaluations. Otherwise, place by the Tier 2-5 criteria in Analysis Rules §1. Check the AI-native flag independently, it is cross-cutting, not a separate tier. **Propose the tier and reasoning, wait for the user to confirm before saving.**

## Output

1. New row in the Competitor Profiles database (title confirmed in `configuration.md`) with a full initial scan, both layers, following the shape in Project knowledge, `competitor-profile-template.md`.
2. New entries in the Evidence Registry page (title confirmed in `configuration.md`) for every source URL found, so future reality checks don't rediscover them.
3. Propose employee list candidates for the Competitor Employee List database (title confirmed in `configuration.md`), scored per `analysis-rules.md` §5 (Tier 1: top 10 on seniority + LinkedIn activity, minimum combined 4; Tier 2 and below: C-level only). **Flag anything that can't be verified without manually browsing a profile as "pending manual validation" rather than guessing.**
4. **Stop. Wait for the user to validate the employee list before adding it.**

## What this skill does not do

Does not assign a tier without confirmation. Does not add employees without validation. Does not run on a schedule, ever, this is inherently one-time-per-competitor work.
