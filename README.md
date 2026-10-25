# BrandSprint AI Skills

AI Skills for the **5-Day Brand Strategy Sprint**. A plugin for Claude that turns the AI into the facilitator's thinking partner between sprint sessions: it reads the sprint's Miro board, tests every locked decision against the evidence walls and the method's own rules, and writes a report. It never writes the brand platform.

> Human creates. AI improves, tests, challenges, and guides the facilitator.

## This plugin only works with the 5-Day Brand Strategy Sprint Framework

The skills are built on the 5-Day Brand Strategy Sprint method: its Miro template board, its canvases, its tool names and its rules. They read the board frame by frame, by the names the framework gives them, and run the tests the framework's guide asks the room to run. Without the framework there is no board to read, no canvases to map and no rules to test against, and the skills will not do anything useful.

The framework and toolkit (the Miro board with every canvas, the A0 canvases for print, the 5-Day Sprint guide, the presentation and Creative Brief templates) are sold here:

**https://www.brandsprint.com/5-day-brand-strategy-sprint-framework/**

Chapter 04 of the guide, "AI Skills", is the facilitator's manual for this plugin: requirements, setup, how each skill is run, how to read a report, the morning check, and what the client is told.

## What the plugin does

One skill per sprint phase, run by the facilitator after each session, never in the room and never by the client.

| Skill | When | What it does |
| :- | :- | :- |
| `sprint-setup` | once, after Onboarding and the Discovery day | Interviews the facilitator, creates the project folder, tests the Discovery boards for gaps and contradictions, returns candidate research questions |
| `sprint-research-prep` | after Research Preparation | Tests the Mindmap, methods, action plan and interview questions against the Discovery gaps; improves the questions |
| `sprint-research` | during the research days, and the evening before Day 1 | Extracts findings from the facilitator's own sources, offers them as sourced stickies, audits the four Evidence Walls |
| `sprint-day1` | evening of Day 1 | Stress-tests the locked Final Strategic Insight against the walls |
| `sprint-day2` | evening of Day 2 | Tests purpose, essence and the three statements against the insight and the walls |
| `sprint-day3` | evening of Day 3 | Tests values, archetype, sliders, tone and persona for coherence; returns a coherence map |
| `sprint-day4` | evening of Day 4 | Tests the prototype and the deck against the platform; may propose, labelled; rehearses Day 5 objections |
| `sprint-day5` | evening of Day 5 | Sorts the reality-check feedback into ACES as a second reading, re-tests the refined platform, checks the Brand Canvas against every lock |
| `sprint-handover` | the week after | Drafts the Brand Platform presentation, the Creative Brief, the board legend, next steps and the closing email, from locked content only |

`sprint-board` sits under all of them: the rule, the project folder, how the Miro board is read, the report format, and the one way black stickies may be placed on the board (only after the facilitator says yes, never inside a lock, removable in one selection).

Every run ends with a report for the facilitator: what was read, what blocks the next day, findings with the evidence behind each one, readings, a labelled opinion, and the questions to bring to the next morning's check. The room decides. The AI does not.

## Requirements

- A paid Claude plan (Pro, Max, Team or Enterprise). Plugins and connectors are not on the free plan.
- The Claude desktop app for macOS or Windows, open during every run.
- Cowork, the Claude mode where skills run with folders and connectors. Claude Code also works.
- A Miro account with edit access to the sprint board. The Miro connector is bundled with the plugin; sign in after install and choose the Miro team that holds the board.
- The 5-Day Brand Strategy Sprint Framework, with the sprint run on its Miro template board.
- One folder on disk where sprint projects live.

## Install

In Cowork: **Customize › Plugins › Add › Add marketplace**, paste this repository's URL, then install **brandsprint**. Open the plugin's **Connectors** tab and connect Miro.

In Claude Code:

```
claude plugin marketplace add brandsprint/5-day-brand-sprint-ai-skills
claude plugin install brandsprint@brandsprint
```

Updates arrive through the marketplace: **Check for updates** on the marketplace entry, or turn on **Sync automatically**.

## Use

One Cowork chat per sprint phase, the sprint folder connected, the Miro connector on. Run `/brandsprint:sprint-setup` after the Discovery day; it creates the project folder every later skill reads first. Then run the phase skill the evening of each session: `/brandsprint:sprint-day1`, `/brandsprint:sprint-day2`, and so on. Each skill writes its report into the project folder and asks before placing anything on the board.

The full procedure, including the morning check and what the client is told, is in chapter 04 of the guide.

## What the skills never do

Write the insight, the purpose, the essence, the statements, the values, the tone or the persona, not as a suggestion and not as an example. Fill an empty canvas. Invent evidence: when nothing on the walls supports a claim, the report says so. Write to the board without a yes. Work in the room.

## Repository layout

```
.claude-plugin/marketplace.json     the marketplace (name: brandsprint)
plugins/brandsprint/                the plugin (name: brandsprint)
  .claude-plugin/plugin.json        manifest and version
  .mcp.json                         the Miro connector
  skills/<skill>/SKILL.md           the ten skills
```

## Licence

BrandSprint™, the BrandSprint logo and the 5-Day BrandSprint™ method are trademarks of BrandSprint Europe SRL. The 5-Day Brand Strategy Sprint Framework, its guide, canvases and templates are protected by copyright. These skills are licensed to purchasers of the framework for use in their own sprints and may not be copied, modified for redistribution, or redistributed in any form without prior written permission from BrandSprint Europe SRL.

office@brandsprint.com · www.brandsprint.com
