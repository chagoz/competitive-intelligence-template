# Competitive Intelligence System

A complete, self-contained competitive intelligence system, methodology, templates, and Claude Skills, built for any company to fork and run on their own Claude account and Notion workspace.

License: MIT. Version history: [`CHANGELOG.md`](CHANGELOG.md).

## Try it first, no install

[`starter-prompt.md`](starter-prompt.md) runs a simplified version of the workflow in a single Claude conversation, attach a couple of files, paste a prompt, no Project or Skill setup required.

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
| `about-us.md` | Your category, value drivers, ICPs, brand voice, the lens every competitor signal gets judged through |
| `competitor-list.md` | Your Tier 1-5 competitor list |
| `watch-list.md` | The topic areas you actively monitor |
| `configuration.md` | Workspace-specific values (Notion page titles, Slack channel, HubSpot fields), filled in during setup |

### `rules/`
| File | What it holds |
|---|---|
| `analysis-rules.md` | Tier criteria, research schema, scoring model, editorial gate |
| `language-guidelines.md` | Voice, structure, formatting, and the master symbol system every document type follows |

### `templates/`
| File | What it holds |
|---|---|
| `digest-template-structure.md` | The weekly digest page structure |
| `slack-message-template.md` | How digest findings get distributed to Slack |
| `competitor-profile-template.md` | The structure for a full competitor profile |
| `flash-report-template.md` | Structure for a single-topic special edition |
| `evidence-registry.md` | Shape of the source registry each competitor profile builds up over time |

### `docs/`
| File | What it holds |
|---|---|
| `setup-guide.md` | Full step-by-step installation walkthrough |
| `skills-index.md` | What each of the five skills does, reads, and writes |

### `skills/`
Five Claude Skills, one folder per skill, each containing a `SKILL.md`. To install one, zip the folder itself (so the zip contains `SKILL.md` at its root, not nested inside another folder) and upload it in Claude's Settings.

## No hardcoded IDs

Every skill finds Notion pages and databases by searching for their title, confirmed once during setup and saved to `your-workspace/configuration.md`. Nothing here is tied to any specific Notion workspace, that's what makes it forkable.

## Getting started

Full walkthrough: [`docs/setup-guide.md`](docs/setup-guide.md).

Short version: create a Claude Project, upload the thirteen files from `your-workspace/`, `rules/`, `templates/`, and `docs/skills-index.md` (Claude's Project knowledge is flat, folders don't carry over), zip and upload each folder in `skills/`, add the custom instructions from the setup guide, then run "set up competitive intelligence system" and follow the five-step flow.
