---
name: Fireflies Connector
description: Connect Fireflies.ai to Cowork for meeting transcripts and notes. Use when the user mentions Fireflies, meeting transcripts, call recordings, meeting notes, or needs past meeting context for prep or follow-ups. Includes quick-win meeting recap.
---

# Fireflies Connector

Connect your agent to Fireflies.ai so it can read meeting transcripts, pull action items, and use past conversations for meeting prep and follow-ups.

## Setup
1. Get your Fireflies API key from fireflies.ai > Settings > Developer
2. Add it to Cowork Settings > Integrations > Fireflies (or configure the Fireflies MCP server)
3. Test: tell your agent "Show me my last 3 meetings from Fireflies"

## Quick Win: Meeting Recap
Tell your agent: "Recap my last meeting with [person/company]"

What it does:
- Pulls the transcript from Fireflies
- Summarizes the key points in plain language
- Lists action items and who owns them
- Flags any decisions that were made
- Notes any follow-ups that are due

## What Your Agent Can Do With Fireflies
- Search past meeting transcripts by person, company, or topic
- Pull meeting context into Meeting Prep (see [Meeting Prep](../meeting-prep/SKILL.md))
- Extract action items from any call
- Find what was discussed about a specific topic across multiple meetings
- Feed transcripts into Project Kit for proposals (see Session 4)

## Troubleshooting
- No meetings showing? Check that Fireflies is recording your calls (it needs to be invited to meetings or running as a bot)
- Wrong meetings? Fireflies API returns your account's meetings — make sure you're using the right API key
- Transcripts seem off? Fireflies transcription quality depends on audio quality
