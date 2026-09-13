# Competitive Intelligence System

A complete, self-contained competitive intelligence system, methodology, templates, and Claude Skills, built for any company to fork and run on their own Claude account and Notion workspace.

Version history: [`CHANGELOG.md`](CHANGELOG.md). The reasoning behind the biggest structural decisions, including what was tried and reversed: [`docs/rework-method-sept-2026.md`](docs/rework-method-sept-2026.md).

## Repo structure

Four layers, each answering a different question:

| Folder | Question it answers | Do you edit it? |
|---|---|---|
| `your-workspace/` | Who are you, and what does your workspace point to? | Yes, this is the part that's actually about your company |
| `rules/` | How does the system decide what matters? | No, reusable methodology |
| `templates/` | What shape does each output take? | No, reusable methodology |
| `docs/` | How do I set this up, and what does each skill do? | No, reference material |
| `skills/` | What are the actual Claude Skills? | No, install as-is |

### `your-workspace/`
| File | What it holds |
|---|---|
| `about-us.md` | Your category, value drivers, theme watches, ICPs, buyer archetypes, product direction, loss patterns, positioning vocabulary, regulation coverage status, who reads your outputs and what each reader needs, the lens every competitor signal gets judged through |
| `competitor-list.md` | Your Tier 1-5 competitor list, plus a corrections log |
| `watch-list.md` | The topic areas you actively monitor |
| `configuration.md` | Workspace-specific values (Notion titles, Slack channel, HubSpot fields, scheduled tasks), filled in during setup |

### `rules/`
| File | What it holds |
|---|---|
| `analysis-rules.md` | Tier criteria, research schema, corporate events, the market lens, the bets pillar, the absence bar, scoring model, editorial gate |
| `language-guidelines.md` | Voice, structure, formatting, and the master symbol system every document type follows |

### `templates/`
| File | What it holds |
|---|---|
| `digest-template-structure.md` | The weekly digest page structure |
| `slack-message-template.md` | How digest and monthly page findings get distributed to Slack |
| `competitor-profile-template.md` | The structure for a full competitor profile, both the full and medium forms |
| `flash-report-template.md` | Structure for a single-topic special edition |
| `monthly-review-template.md` | The monthly page: the review, the market lens, and the working record |
| `evidence-registry.md` | Method only, what each source type reveals and how often to check it. Addresses live in your Notion database, not this file |

### `docs/`
| File | What it holds |
|---|---|
| `skills-index.md` | What each of the five skills does, reads, and writes |
| `rework-method-sept-2026.md` | A worked example of reworking this kind of system properly: what got tried and reversed, four real errors and their one shared cause, and the rules that came out of doing the work rather than planning it. Not required reading to use the system, genuinely useful if you're about to rework your own copy |

### `skills/`
Five Claude Skills, one folder per skill, each containing a `SKILL.md`. To install one, zip the folder itself (so the zip contains `SKILL.md` at its root) and upload it in Claude's Settings.

## Who owns what

Every piece of content has exactly one home. No other file restates it, files reference each other instead. This is what makes the system forkable in the first place, a rule that broke more than once in real use before it was written down: a theme watch list drifted between two files holding different counts of the same list, brand voice rules got duplicated across two more, and a database schedule got restated in three separate files and went stale in two of them.

| Content | Owner | Everything else |
|---|---|---|
| Who the company is, category, value drivers, ICPs, buyer archetypes, product direction, loss patterns | `about-us.md` | References |
| The theme watch list | `about-us.md` | References by name, never restates |
| Your regulation or standards coverage status | `about-us.md` | References |
| Positioning vocabulary, the words that carry your position | `about-us.md` | References |
| Who reads your outputs, and what each reader needs | `about-us.md` | References |
| Who you compete with, and at what tier | `competitor-list.md` | References |
| What topics you watch, and how they're scored | `watch-list.md` | References |
| How research is done, scored and classified | `analysis-rules.md` | References |
| Writing craft, formatting, the symbol system | `language-guidelines.md` | References |
| The shape of each output | The matching template file | References |
| Where things live in your workspace, and your schedule | `configuration.md` | References, never hardcodes |

**Positioning belongs to About Us, craft belongs to Language Guidelines.** "Our AI identifies, structures, prioritises and contextualises" is a position. "Describe what the AI does rather than echoing hype" is craft. When a rule could sit in either, ask whether a different company forking this system would keep it. If yes, it's craft.

**Where a file needs content it doesn't own, it names the owner and stops.** A reader who needs the detail opens the owner. A copy is how two versions of the truth start.

## Keeping the layers in step

Four rules, all learned the hard way in real use, not designed in the abstract.

**Skill files are reconciled last, never first.** A skill describes the rules; rewriting it before the rules have settled guarantees a second pass. In one real rework, all five skills were rewritten in a single sitting and three of them were wrong within a day, because the rulebook kept changing underneath them mid-rewrite. One line was actively harmful: a skill telling a run to block on an input that had already arrived.

**A document change that names a database field isn't done until the database has the field.** In the same rework, a reference file declared several new source types and a new check cadence one morning, and the live Notion database knew nothing about it until someone checked that afternoon. The document is not the system. Changing the method and changing the store are two pieces of work, and only doing the first leaves a rule nothing can execute.

**A rule carried inline in a skill is a rule in the wrong place.** If a skill needs method the rulebook doesn't have yet, that's a signal to write it into the rulebook, not to hold it locally and mark it pending. Pending migration is exactly how a theme watch list can end up existing in two files with two different contents, each one edited without the other in view.

**One version stamp per file, in the footer, never a second one in the header.** In the same rework, most reference files had drifted between a header stamp and a footer stamp, one of them by several versions, because footers got bumped on every edit and headers never did. The footer is the stamp because it sits with the change note, and because two other rules already point at it: the one-authority-date rule in the profile template, and the version attestation the weekly digest requires before drafting.

**A status fact restated outside its owner will drift, and it doesn't matter which file does the restating.** `configuration.md` owns database detail and scheduled task cadence. In real use, three separate files each independently restated a piece of that, a skills reference file, a running-status file, and this README's own status section, and each went stale at a different time over the same underlying fact. Found three times, independently, because each fix addressed the instance rather than the pattern. Written down now so the next occurrence is recognised on sight.

## No hardcoded Notion IDs, anywhere

Every skill and every document refers to Notion pages and databases by title, never by ID. The first time any skill runs in a new Notion connection, it searches for what it needs, shows what it found, and asks for confirmation before writing.

**No skill configures itself.** Project knowledge is read-only while a skill runs, so a skill cannot write a confirmed value back into `configuration.md`. It reports the delta and asks for the file to be updated by hand. The human is the only writer, deliberately, so a configuration change is always visible.

## How these relate to each other

`about-us.md` is read first, it's the lens every competitor signal gets judged through. `analysis-rules.md` is the rulebook everything else follows. `language-guidelines.md` governs how output gets written once the rules have been applied. The template files are the concrete shapes output takes. `evidence-registry.md` defines the source types those rules get applied to, and `competitor-list.md` names who they get applied to. `skills-index.md` ties the whole thing to the five actual skill files that do the work.

## Getting started

No standalone setup guide is included in this package, this section is the walkthrough.

Create a Claude Project. Upload the reference files from `your-workspace/`, `rules/`, `templates/`, and `docs/skills-index.md` (Claude's Project knowledge is flat, folders don't carry over, grab each file regardless of which folder it sits in here). Zip and upload each folder in `skills/` under Settings. Add custom instructions telling Claude these files are the current source of truth for any competitive intelligence task, and to read `configuration.md` before touching Notion, Slack, or your CRM, never from memory.

Then run "set up competitive intelligence system." The `ci-system-setup` skill runs two phases. **Phase 1** asks who your company is, your competitors by tier, your watch list topics, and your voice, only if `about-us.md`, `competitor-list.md`, and `watch-list.md` don't already have real content, skipped automatically otherwise. **Phase 2** checks for six Notion items (the home page, and five databases including Digest Actions), shows you the proposed shape for anything missing, and builds it once you confirm. Phase 2 is safe to re-run any time, Phase 1 only runs once.

## Keeping this current

These are a snapshot, not a live mirror of Notion. When a live Notion page changes, re-export the affected file and re-upload it, replacing the old version. There's no automatic sync, a deliberate trade for keeping the system self-contained and not dependent on a private workspace.

## For a fork

Four files are specific to whoever's running this and need to be replaced with your own: `about-us.md`, `competitor-list.md`, `watch-list.md`, and `configuration.md`. The first three end with a short section on how to build your own version. Everything else defines a methodology rather than any one company's content, and travels as-is. The `ci-system-setup` skill exists specifically to walk you through that replacement.

If you find company-specific content in any other file, that's a defect in this system, not something to work around.

---

*[Your name] x Claude*
