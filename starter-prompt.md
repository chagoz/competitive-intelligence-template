# Starter Prompt

*A copy-paste way to try the Weekly Digest workflow in a single conversation, no Skill install, no Claude Project required. Good for a first look before committing to the full setup in `docs/setup-guide.md`.*

---

## What to attach

Start a new Claude conversation and attach these four files (from `your-workspace/` and `rules/`):

- `your-workspace/about-us.md`
- `your-workspace/competitor-list.md`
- `your-workspace/watch-list.md`
- `rules/analysis-rules.md`

If `about-us.md`, `competitor-list.md`, or `watch-list.md` are still blank templates, that's fine, the prompt below asks for that information directly instead.

## The prompt

Paste this after attaching the files above:

```
I'm trying out a competitive intelligence workflow. I've attached my rules 
and reference files.

If about-us.md, competitor-list.md, or watch-list.md are still blank 
templates rather than filled in, ask me the following before doing 
anything else, one at a time:
1. What does my company do, and what's our category?
2. Who are my direct (Tier 1) competitors, the ones I've actually lost 
   deals to or that get named in evaluations?
3. What two to four topics do I want to watch (the recurring battlegrounds 
   in my category)?

Once you have that, or if the attached files already have real answers:

Research my Tier 1 competitors using public sources (their website, 
LinkedIn, product pages, and if available, G2 or Capterra reviews). For 
each one, tell me:
- What they're currently claiming or positioning around
- What's actually verifiable (shipped features, real user feedback, dated 
  evidence), separate from marketing claims
- A talk-vs-implement read: is this real or just announced?
- How relevant this is to me, scored high/moderate/low, against the watch 
  list topics I gave you

Then propose 3 things I should know this week, with your reasoning for 
each, and wait for me to confirm or adjust before writing anything up in 
full.

Follow analysis-rules.md for the scoring model and research approach. 
Tag every claim as self-declared (their own words) or independently 
verified (a third party), with a date and link when you have one.
```

## What this gets you

A rough version of what the `weekly-digest` skill does automatically, run manually, in one conversation, with Claude asking the same questions a full setup would ask. It won't write anywhere (no Notion, no Slack), everything stays in the chat. Good for evaluating whether this system fits before setting up the full Claude Project and skills.

## Next step

If this was useful, the real setup (Project knowledge, the five skills, recurring runs, Notion storage) is in `docs/setup-guide.md`.
