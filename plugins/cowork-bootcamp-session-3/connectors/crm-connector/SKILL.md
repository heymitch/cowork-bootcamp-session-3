---
name: CRM Connector
description: Connect your CRM to Cowork for meeting prep and relationship tracking. Includes a Notion "Book of Names" template if you don't have a CRM yet. Say "Set up my CRM" or "Connect my Rolodex".
---

# CRM Connector

Give your agent a memory for people. Connect a CRM so Meeting Prep knows your history with every contact — and saves new context after every call.

## Do You Already Have a CRM?

### Option A: I use Notion
Notion is the default and easiest path. Your agent can read and write to a Notion database directly.

1. Connect Notion (if you haven't already — see the Notion connector from Session 2)
2. Create a new database in Notion called **"Book of Names"**
3. Add these properties:

| Property | Type | What It Tracks |
|----------|------|---------------|
| Name | Title | Contact name |
| Company | Text | Their company |
| Role | Text | Their title/role |
| Relationship | Select | Prospect / Client / Partner / Colleague / Other |
| Last Contact | Date | When you last interacted |
| Meeting Notes | Rich Text | Key outcomes from past meetings |
| Rapport Notes | Rich Text | Personal details, interests, what they care about |
| Next Steps | Rich Text | Open action items |

4. Share the database with your Cowork integration (same as any Notion page)
5. Test: tell your agent "Search my Book of Names for [any name]"

### Option B: I use HubSpot / Salesforce / Pipedrive
If you already have a CRM with an MCP server or API integration:
1. Connect it through Cowork Settings > Integrations
2. Meeting Prep will search your CRM for contact history automatically
3. After meetings, it can update contact records with new notes

### Option C: I don't have a CRM yet
No problem. Two choices:
1. **Use the Notion template above** — takes 5 minutes, gives you a real Rolodex
2. **Skip it for now** — Meeting Prep saves contact files locally to `contacts/[name].md`. You can migrate to a real CRM later.

In **Session 6 (Skill Building)**, you'll learn to build custom connectors for any tool — so if your CRM isn't listed here, you can wire it up yourself.

## What This Unlocks for Meeting Prep

Without CRM: Meeting Prep pulls from email, transcripts, and web search.
With CRM: Meeting Prep ALSO pulls your stored relationship history, rapport notes, and open action items. The brief gets dramatically better over time as you build your Book of Names.

## The Compounding Effect

| Meeting # | What Your Agent Knows |
|-----------|----------------------|
| 1st | Web research only — who they are publicly |
| 2nd | Web + email history + transcript from last call |
| 3rd+ | Web + email + transcripts + stored rapport notes + open items + personal details |

Every interaction makes the next brief better. This is the Dale Carnegie advantage — automated.

## Quick Win

After connecting, say: **"Add [person] to my Book of Names"**

Your agent creates a contact entry from whatever you know — paste a LinkedIn URL, an email signature, or just tell it what you remember.
