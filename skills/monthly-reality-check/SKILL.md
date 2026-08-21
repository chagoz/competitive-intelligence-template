---
name: monthly-reality-check
description: "Runs your company's monthly competitive reality check: verifies competitor claims against Layer 2 evidence (G2, help centers, job postings), pulls the previous month's HubSpot lost-deal data, updates every Competitor Profiles entry, and proposes key learning candidates for the user's confirmation. Trigger phrases: 'run monthly reality check', 'run reality check for [month]'. Ad hoc, manually triggered today. Suggested cadence: monthly, first week, covering the previous calendar month."
---

# Monthly Reality Check

## Status and cadence

**Mode:** ad hoc. Runs when explicitly triggered.
**Suggested cadence:** monthly, first week, covering the previous calendar month.
**Human gate:** required. the user selects the top 3 key learnings from the candidates proposed. Never publish the Quarterly/Monthly review page before this selection happens.

## Before anything else

Read from Project knowledge: `analysis-rules.md` (§2 research schema, §2.1 recency filter, §2.2 source honesty, §8 lost deal data method, §9 the always-true rule).

Read `configuration.md` for the Evidence Registry page, Competitor Profiles database, Competitor Employee List database, and HubSpot field names. If any value is missing or unconfirmed, search Notion for it by the name given in the file, show what was found, and ask for confirmation before writing anything. Write confirmed values back into `configuration.md`.

If any edit fails with "can't edit page on block with an archived ancestor," stop and flag it, do not silently write elsewhere, this usually means the database title matched more than one page and the wrong one got confirmed.

If HubSpot fields aren't set in `configuration.md`, skip the lost-deal pull entirely and say so explicitly in the output rather than failing the whole run.

If any Evidence Registry entry is marked "to be confirmed," close that gap before scanning begins.

## Research

Layer 2 only (G2, Capterra, TrustRadius, help centers, job postings, employee LinkedIn posts). Apply the recency filter: only evidence dated inside the current cycle counts as new. Apply source honesty tags to every claim: `[Self-declared]` or `[Independent, verified]`, with a link when available.

**HubSpot lost-deal pull.** Query both meetings and calls objects, filtered by creation date for the previous calendar month (or quarter, if this cycle is quarterly). Use the structured and free-text loss-reason fields named in `configuration.md` for competitor name extraction. Sum both objects, activity-type data alone is often sparse. Dedup scheduling-tool pairs by datetime and title. Zero entries excluded, Unknown column always present. Full method: `analysis-rules.md` §8.

**Employee scan.** Light scan of tracked employees' recent posts, dated within the current cycle only, for reality-check-relevant signals. No rescoring, that happens on the 6-month cadence defined in Analysis Rules §5.

## The always-true rule

Every discovery updates the relevant Competitor Profiles entry immediately, in this same session: the 🔄 Changelog block, the 🗣️/🔧/🤷 tables, `Strategic Relevance` (both axes), `Last Updated`. Do not wait for a separate pass.

## Output

1. Update every affected Competitor Profiles entry per the always-true rule.
2. Update the Theme Watch activity matrix for the month.
3. Update the lost deal table.
4. Propose 5 key learning candidates with reasoning.
5. **Stop. Wait for the user to select the top 3.** Do not write the Monthly/Quarterly Competitor Review page until this selection happens.
6. Once selected, write or update the review page. Structure and voice live in Project knowledge, `language-guidelines.md` Part 3: observational tone, impact-first structure, altitude rule, data-sufficiency gate.

## Data-sufficiency gate

If there isn't enough Reality Check history for a genuine time-based comparison, do not stretch limited data into a trend. Run a dedicated fresh search against the topics in `watch-list.md`, topic by topic, to establish an honest current-state baseline instead. This is its own research pass, not something to compress into the same session as the rest of the reality check, flag it as a separate step if it's needed.

## What this skill does not do

Does not select the top 3 key learnings itself. Does not skip the recency filter or source honesty tags to save time. Does not run on its own schedule yet.
