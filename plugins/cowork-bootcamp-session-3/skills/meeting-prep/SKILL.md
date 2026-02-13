---
name: meeting-prep
description: Research anyone before a meeting — web search, email history, past transcripts, CRM — and walk in with a full brief plus a rapport builder. Say "Prep me for my meeting with [person]" or "Brief me on my next call".
---

# Meeting Prep

Never walk into a meeting cold. This agent researches the person, pulls your shared history from every connected source, finds a rapport builder, and gives you a brief that would take 20 minutes to build manually.

## How to Run

- "Prep me for my meeting with [person/company]"
- "Brief me on my next call"
- "What do I need to know before my 2pm?"

---

## Preflight Check (Run Silently)

### 1. Config check
Read `config.md` from project root.
- **Missing:** Stop. Say: "Say **'Run my business blueprint'** first — takes 5 minutes."
- **Exists:** Continue.

### 2. Connector inventory (silent)
Check available tools and build a source list:
- **Web search** → always available (person intelligence)
- **Gmail tools** → email threads + transcript emails from Fireflies/Fathom/Otter/Zoom
- **Fireflies tools** → full meeting transcripts
- **Notion tools** → CRM/Book of Names, project pages
- **Slack tools** → channel mentions and threads
- **Google Docs tools** → shared documents
- **Calendar tools** → meeting details

Update config.md checkboxes for any newly found connectors.
- **Zero connectors:** Still works — web research + user-provided context. Note what's missing at the end.

### 3. All clear — proceed without announcing.

---

## The Process

### Step 1: Get Meeting Details
Check calendar for who, when, what. If no calendar tools, ask: "Who are you meeting with and what's it about?"

### Step 2: Person Intelligence (Web Search)
Search the web for the person. See `references/person-research.md` for search patterns.
Build: name, title, company, career background, online presence, recent news.
This is the "never get caught not knowing who someone is" layer.

### Step 3: Relationship History (Connected Sources)
Pull from every available source — skip unavailable ones silently:
- **CRM/Notion:** Check Book of Names for stored contact profile and rapport notes
- **Gmail (two passes):** (1) email threads with this person/company, (2) meeting transcript emails from Fireflies/Fathom/Otter/Zoom/Read.ai
- **Fireflies:** Full transcripts from past meetings (richer than email summaries)
- **Slack:** Recent mentions or threads about this person/project
- **Google Docs:** Shared documents, proposals, contracts

### Step 4: Rapport Builder
Find ONE thing to open with that makes them feel known. See `references/rapport-building.md`.
- Check CRM for stored rapport notes first
- Then: shared connections, specific post they wrote, recent accomplishment, mutual interest
- If nothing found, use web research (reference a talk, article, or recent company news)

### Step 5: Compile the Brief
Use the template from `references/brief-template.md`:
Who → Shared History → Open Items → Recent Context → Rapport Builder → Talking Points → Sources Used.
Adapt for first meetings vs. recurring contacts vs. group meetings.

### Step 6: Show Brief
Present the full brief. **Do not save yet.** Wait for approval or edits.

### Step 7: Save + Rolodex Update
On approval: save brief to Notion or local file.
Prompt: "Want me to add [person] to your Book of Names for next time?" — save contact profile to CRM/Notion with rapport notes.

## Rules

- Only pull from connectors that are actually available — skip the rest silently.
- If a source returns nothing relevant, say so. Never fabricate history.
- Always show the brief before saving.
- Flag urgent or time-sensitive items.
- For new contacts: lean heavy on web research + rapport builder. For returning contacts: lean heavy on history + open items.
- At the end, if key connectors are missing, mention once: "This brief would be stronger with [source] connected."
