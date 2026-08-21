# Configuration

*Workspace-specific values every skill reads before running. This file is empty the first time any skill runs in a new Notion connection. The setup skill searches for each item below by the name you confirm, shows what it found, and asks for confirmation before writing anything here. Once confirmed, later runs just read this file, no repeated searching or asking.*

*Fill this in during setup, most of it gets filled in for you as you answer the setup skill's questions, this is the record of what got confirmed.*

---

## Setup Progress

*Read and update this section every time the setup skill runs. It tracks which of the five setup steps are done, so a re-run resumes from the right place instead of redoing finished work or skipping ahead of unfinished work.*

| Step | Status | Notes |
|---|---|---|
| 1. Read existing files | Not started | |
| 2. Build file infrastructure | Not started | |
| 3. Content (About Us, Competitor List, Watch List, Language Guidelines) | Not started | |
| 4. First competitor evidence batch | Not started | |
| 5. Suggest cadence, walk through scheduling | Not started | |

---

## Notion, pages and databases the skills search for by title

*Type and Status get filled in during setup. Until then, treat every item below as unconfirmed.*

**Competitive Intelligence home page (title to search):**
**Type:** Markdown page
**Status:** unconfirmed

**Competitor Profiles database (title to search):**
**Type:** Database
**Status:** unconfirmed

**Competitor Employee List database (title to search):**
**Type:** Database
**Status:** unconfirmed

**Digest Impact Tracker database (title to search):**
**Type:** Database
**Status:** unconfirmed

**Evidence Registry database (title to search):**
**Type:** Database
**Status:** unconfirmed
*Live-maintained by the skills (Competitor Profile Setup adds to it, Monthly Reality Check updates "last checked" dates), not a static Project knowledge file. A template version showing its shape exists in Project knowledge as evidence-registry.md, but the working copy lives in Notion once built.*

---

## Slack

**Channel for digest posts:**
**Status:** not configured
*If not configured, the skill drafts the post and asks where to send it instead of posting.*

---

## HubSpot

**Status:** not configured

**Lost-deal reason field (structured):**
**Lost-deal reason field (free text):**
**Activity objects to query:** meetings and calls, both, summed together
**Activity type values that count:**

*If HubSpot isn't connected, or these fields aren't set, Monthly Reality Check runs without the lost-deal pull and says so in its output rather than failing.*

---

*Confirmed by: [pending first run]*
*Last confirmed: [pending]*
