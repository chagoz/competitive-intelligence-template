# Starter Prompt

*A copy-paste way to try a competitive research pass in a single conversation, no Skill install, no full Claude Project required. Good for a quick look before running the actual `weekly-digest` or `competitor-profile-setup` skills.*

---

## What to attach

Start a new Claude conversation and attach these four files:

- `your-workspace/about-us.md`
- `your-workspace/competitor-list.md`
- `your-workspace/watch-list.md`
- `rules/analysis-rules.md`

## The prompt

Paste this after attaching the files above:

```
I'm running a quick competitive intelligence check. I've attached my rules
and reference files, About Us, Competitor List, Watch List, and Analysis
Rules.

Research my Tier 1 competitors using public sources (their website,
LinkedIn, product pages, and if available, G2, Capterra, or another review
site). For each one, tell me:
- What they're currently claiming or positioning around
- What's actually verifiable (shipped features, real user feedback, dated
  evidence), separate from marketing claims
- A talk-vs-implement read: is this real or just announced?
- Any corporate event from the last twelve months, funding, acquisition,
  partnership, or a senior hire, even if it's not recent news, these are
  worth noting regardless of date
- How relevant this is to us, scored high/moderate/low, against the watch
  list topics I gave you

Then propose 3 things I should know this week, with your reasoning for
each, and wait for me to confirm or adjust before writing anything up in
full.

Follow analysis-rules.md for the scoring model and research approach.
Tag every claim as self-declared (their own words) or independently
verified (a third party), with a date and link when you have one. If you
can't find something, say so explicitly rather than treating silence as
an answer.
```

## What this gets you

A rough version of what the `weekly-digest` skill does automatically, run manually, in one conversation. It won't write anywhere (no Notion, no Slack), everything stays in the chat. Useful for a fast gut-check without triggering the full skill and its Notion writes.

This is deliberately a simple version. It doesn't walk through the bets pillar, the market lens, or the absence bar the way the real skills do, those need more room than a five-minute trial prompt should try to hold.

## Next step

For the real recurring workflow, Notion storage, Slack distribution, and analytics, use the actual `weekly-digest` skill.
