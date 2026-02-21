---
name: meeting-prep
description: Never walk into a meeting cold. Prep for meetings, gather context, build briefs, track action items, write follow-ups. Say "prep me for my meeting with [person]", "brief me on [person]", "gather context", "find everything about [person]", "action items", "what's open from my meetings", "write follow-up", or "meeting recap".
user-invocable: false
---

# Meeting Prep

Your meeting command center. Pulls context from Gmail, Slack, Docs, and Fireflies, builds a brief, tracks action items, and writes follow-up emails.

## How to Run

Tell me what you need and I'll route to the right sub-skill.

## Preflight (Run Silently Every Time)

1. **config.md** — Read from project root. If missing, stop: "Say **'Run my business blueprint'** first — it takes 5 minutes."
2. **Connectors** — Scan available tools (Gmail, Slack, Drive, Fireflies, Calendar). Note what's connected. If zero: "No connectors found. I can still work with pasted notes, or I can walk you through connecting Gmail — it takes two clicks."

## Routing

| User says | Route to |
|-----------|----------|
| "Prep me for my meeting" / "Brief me on [person]" | context-gatherer then brief-builder (full flow) |
| "Gather context" / "Find everything about [person]" | context-gatherer |
| "Build a brief" / "Create brief for [person]" | brief-builder |
| "Action items" / "What's open from my meetings" | action-tracker |
| "Write follow-up" / "Meeting recap" / "Recap email" | follow-up-writer |

For the full flow ("prep me" / "brief me"), run context-gatherer first, then pass the output to brief-builder. Do not ask the user to run them separately.

## Sub-Skills

- `../context-gatherer/SKILL.md` — Pull raw context from all connected sources
- `../brief-builder/SKILL.md` — Assemble a structured meeting brief
- `../action-tracker/SKILL.md` — Find and track open action items
- `../follow-up-writer/SKILL.md` — Draft post-meeting recap emails

## References

- `references/brief-template.md` — Standard brief format and example
- `references/connector-guide.md` — How to set up each connector
- `references/transcript-search-patterns.md` — Gmail search patterns for finding meeting transcripts

## Rules

- Route based on intent. Don't ask "which sub-skill?" — figure it out from what they said.
- Always run preflight silently. Only speak up if config.md is missing or zero connectors.
- For ambiguous requests, default to the full flow (context-gatherer then brief-builder).
- Never load reference files unless a sub-skill needs them. Keep context lean.
