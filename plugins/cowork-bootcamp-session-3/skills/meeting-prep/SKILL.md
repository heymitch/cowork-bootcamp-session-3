---
name: meeting-prep
description: Prepare a comprehensive brief before any meeting by pulling from Gmail, Slack, Google Docs, and Fireflies. Say "Prep me for my meeting with [person]" or "Brief me on my next call".
---

# Meeting Prep

Build a complete meeting brief by pulling from your email, Slack, documents, and past meeting transcripts — all at once.

## How to Run

- "Prep me for my meeting with [person/company]"
- "Brief me on my next call"
- "What do I need to know before my 2pm?"

---

## Preflight Check (Run Every Time)

Run through this silently. Only speak up if something is missing.

### 1. Does config.md exist?
Read `config.md` from the project root.
- **If missing:** Stop. Say: "I need to know about you and your business first. Say **'Run my business blueprint'** — it takes 5 minutes."
- **If exists:** Continue.

### 2. Which connectors are available?
Check your available tools for each of these. Build a list of what's available:
- **Gmail tools** → can pull email threads AND meeting transcript emails (see Step 2 below)
- **Slack tools** → can pull channel mentions and threads
- **Google Drive/Docs tools** → can pull shared documents
- **Fireflies tools** → can pull meeting transcripts directly
- **Calendar tools** → can check meeting details

For each connector found, if config.md has it unchecked in Setup Status, update it to checked.

- **If zero connectors found:** Say: "I don't have any of your tools connected yet, so I can't pull context automatically. I can still build a brief if you paste what you know — emails, notes, or just tell me about this person. Or I can walk you through connecting Gmail — it takes two clicks and unlocks meeting history from your email."
- **If at least one found:** Continue. Note which sources are available and which aren't — only pull from what's connected.

### 3. All clear — proceed silently.

---

## What the Agent Does

Step 1: Check calendar for the meeting details (who, when, what). If no calendar tools, ask the user.

Step 2: Pull context from every connected source (skip unavailable ones silently):

- **Gmail**: Two passes:
  1. **Email threads** — recent conversations with this person/company
  2. **Meeting transcript emails** — search for emails from Fireflies, Fathom, Otter, Zoom, Google Meet, or any meeting recorder. These services email summaries after every call. Search for the person/company name in those emails to find past meeting context. Common sender patterns:
     - Fireflies: "from:fireflies.ai"
     - Fathom: "from:fathom.video"
     - Otter: "from:otter.ai"
     - Zoom: "from:zoom.us" subject contains "recording" or "transcript"
     - Google Meet: "from:meet.google.com" or meeting notes
     - Read.ai: "from:read.ai"
  This means **Gmail alone gives you meeting history** — no separate transcript connector required.

- **Slack**: Recent mentions or threads about this person/project
- **Google Docs**: Any shared documents or proposals
- **Fireflies** (if connected): Full transcripts from past meetings — richer than email summaries but not required

Step 3: Build the brief:
- **Who you're meeting**: Name, role, company, relationship summary
- **Last interaction**: When you last spoke and what was discussed
- **Open items**: Action items from past meetings that haven't been completed
- **Recent context**: What's been happening in email/Slack since your last meeting
- **Key documents**: Links to relevant shared docs
- **Suggested talking points**: Based on open items and recent context
- **Sources used**: List which connectors contributed (so user knows what's missing)

Step 4: Show the brief for review.

Step 5: Save as a file (or to Notion if connected).

## Rules

- Only pull from connectors that are actually available — skip the rest silently.
- If a connector has no relevant results, say so instead of making something up.
- Always show the brief before saving.
- Flag anything that looks urgent or time-sensitive.
- If the meeting is with someone new (no history), say so and focus on what's available.
- At the end, if key connectors are missing, mention once: "This brief would be stronger with [Gmail/Fireflies/etc] connected. Want me to walk you through it?"
