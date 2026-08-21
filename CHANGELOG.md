# Changelog

*What changed, when, across the whole system. Individual files also carry their own version footer, this page is the aggregate view for anyone landing on the repo cold.*

---

## Unreleased / this update

- **Repo restructured.** Flat file lists replaced with layered folders (`your-workspace/`, `rules/`, `templates/`, `docs/`, `skills/`) so it's visible at a glance what you edit versus what's fixed methodology.
- **Flash Report added.** A sixth document type, single-topic special editions, triggered explicitly or flagged mid-research by the `weekly-digest` skill. New file: `templates/flash-report-template.md`.
- **Symbol system unified.** Every symbol across every document type now traces to one master table in `rules/language-guidelines.md`. Previously the rule lived only inside the Weekly Digest section, so other document types had each improvised their own vocabulary, causing real collisions (two different sections both using the same symbol).
- **Em-dash cleanup.** The system's own "no em dashes" rule was being broken by the rule documents themselves. Fixed across every file.
- **`configuration.md` introduced.** No skill hardcodes a Notion page ID, HubSpot field name, or Slack channel anymore. Everything is found by searching for its title, confirmed once, and saved here. This is what makes the system portable across Notion workspaces.
- **`ci-system-setup` rebuilt as a five-step flow.** Read existing files, build Notion structure, collect workspace content, run a first competitor research batch, then suggest and walk through recurring schedules. Safe to re-run at any point without redoing finished work.
- **`starter-prompt.md` restored/rewritten**, a no-install way to try the workflow in a single conversation.

## Earlier

- **Two-axis scoring introduced.** Talk-vs-implement (is it real?) and threat level (does it matter?) split into independent axes, always shown together, never collapsed into one number. Previously a single relevance score conflated both questions.
- **Source honesty tags added.** Every claim tagged `[Self-declared]` or `[Independent, verified]`, dated and linked. Previously a certainty-only scale silently conflated a press release with a third-party review.
- **Recency filter added.** Only evidence dated within the current research cycle counts as new, preventing old reviews from reading as fresh findings.
- **Quarterly/Monthly Competitor Review template built**, reversed structure from the weekly digest (impact first, proof at the close), observational voice rather than directive, plus a data-sufficiency gate for when Reality Check history is too thin for a genuine trend.
- **Five-skill architecture established**: Weekly Digest, Monthly Reality Check, Competitor Profile Setup, Competitive Mission, CI System Setup.
- **Initial system**: single weekly digest workflow, one skill, tier-based competitor tracking, manual research.

---

*For the reasoning behind any specific change, the individual file's own version footer usually has more detail than this summary does.*
