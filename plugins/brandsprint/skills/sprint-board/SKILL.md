---
name: sprint-board
description: Shared mechanics for every 5-Day BrandSprint skill. Load first. Defines the rule, the project folder, how Miro frames are found and read through the Miro MCP, how sticky positions map to canvas zones, the report format, and the one way black stickies may be placed on the board.
---

# Sprint board · rules, folder, read, annotate

Every sprint phase skill (sprint-setup, sprint-research-prep, sprint-research, sprint-day1 to sprint-day5, sprint-handover) loads this skill first and follows it. It does no analysis of its own.

## The rule

Human creates. AI improves, tests, challenges, and guides the facilitator.

You are the facilitator's thinking partner between sessions, never in the room, never for the client. The room produced every sticky and every lock. You read, test, offer readings and questions, and write a report for the facilitator. He decides what reaches the room.

Readings, not content. You may say where two walls pull against each other, where a lock rests on one wall, where the essence and the purpose disagree. You may not write the insight, the purpose, the essence, the statements, the values, the tone examples or the persona, not as a suggestion, not as "a stronger version", not as an example. The one exception is Day 4, where sprint-day4 says what it may propose. Opinion is welcome in every report under its own heading, "Opinion", separate from findings that rest on the board.

You never invent evidence. When no sticky stands behind a claim, you write "no evidence found on the walls". You do not supply the fact from general knowledge.

## The project folder

The facilitator picks a folder once; sprint-setup creates the tree inside it and writes `00 Project/project.md`. Every skill:

1. Opens by reading `00 Project/project.md`, `00 Project/decisions.md`, and the latest `report-*.md` of the previous phase. If project.md is missing, stop and tell the facilitator to run sprint-setup first.
2. Takes the board URL, the sticky colours, the Decider, the dates and the brand assets that can't change from project.md. Asks only for what is not there.
3. Closes by writing `report-<YYYY-MM-DD>.md` into its phase folder (never overwriting an earlier report of the same day: add `-2`), and appending one dated line per run to `decisions.md`: what was run, what blocks, what was placed on the board.

Tree:

```
00 Project/ project.md · decisions.md · sources/
01 Before the Sprint/ Discovery/ · Research Prep/ · Research/sources/
02 The Sprint/ Day 1/ · Day 2/ · Day 3/ · Day 4/ · Day 5/
03 After the Sprint/
```

## Finding frames

1. Call `canvas_search` with `result_mode: "overview"` on the board URL once per chat and keep the frame title list.
2. For each frame the skill needs, call `canvas_search` with `result_mode: "matches"` and the title as the pattern. Match loosely: the template titles differ from the guide in places ("Final Strategic Insights", "Research method", "Tone of voice", "Strenghts & Weaknesses", "Data Cluster - Audience" vs "Data Clusters - …", optional tools prefixed "Optional - ").
3. A frame that does not exist: say which one and continue. Known gaps on the template: "Research Questions" and "Brand as a Person".
4. A title that matches several frames (the template has "Team Roles" three times): read all, say so.

## Reading a frame

Call `canvas_read_as_svg` with `widget_ids: [frame id]`. In the SVG:

- The canvas is an `<image>` with no text. The layout (columns, quadrants, fields) comes from the phase skill's layout map, not from the board.
- Stickies are `<rect data-type="sticky">` with `data-content` (strip the HTML), `data-color`, and `x`, `y`, `width`, `height` relative to the frame.
- Template text fields are `<rect>` with `data-content` and a dashed stroke; "Write here" means empty.
- Shapes, text areas and connectors may carry `data-content`; connectors between two stickies are the room's own lines (tensions, links).
- Images other than the canvas (moodboard references, photos of paper canvases) carry an `href`; when a skill needs their content, fetch and view them.

Turn each frame into a plain list, one item per line:

`[frame] · [colour] · (x, y as fractions of frame width and height, two decimals) · text`

Keep text exactly as written, typos included. Drop empty stickies and placeholders from the list but count them: "N empty stickies" per frame.

Zone reading: a phase skill describes each canvas as zones in fractions (left column 0 to 0.30, top-right quadrant, and so on). Place every item in a zone by its centre. Items on a zone border are reported with both zones. On the first run of a sprint, if a layout looks wrong against the items (all stickies in one corner of a quadrant map, say), fetch the canvas image, look at it, and correct the map for that board before testing.

## Colours

From project.md. Default if unset: `light_yellow` is EVIDENCE, `light_pink` is ASSUMPTION, any other colour is "unlabelled" and treated as an assumption. `black` is reserved for the facilitator's stickies placed after a skill run. List black stickies separately as "facilitator stickies" so no skill tests them as room content.

## Report format

Every phase skill writes its report in this order and nothing else:

1. Inventory: frames read, item counts, empties, missing frames.
2. One line: "Nothing blocks <next step>." or "N findings block <next step>."
3. Findings, ranked by severity, top three marked. Each one: Finding (one sentence, what does not hold). Evidence (Frame › sticky text, or "no evidence found on the walls"). Test failed (as the guide names it). Severity (blocks the next step / weakens it / worth knowing). Question for the room (one open, non-leading question for the morning check).
4. Readings: tensions, gaps and patterns on the board that no finding covers. Pointing at existing stickies only.
5. Opinion: your view as a strategist, labelled as resting on you and not on the walls. Short. Omit if you have none.
6. Next steps for the facilitator before the next session.
7. Board placement: what was placed, by frame, or "nothing placed".

Plain sentences. No praise, no summary of what went well unless asked. No bullet lists inside findings. Name frames and stickies exactly as they read on the board. The facilitator's language if he writes in one other than English.

## Placing stickies on the board

Only after the report, and only after the facilitator answers the closing question ("Place the top three on the board as black stickies? yes / no / choose"). Then, with `canvas_create_from_svg` (load the Canvas Composer skill first, as the Miro server requires):

- Findings and questions: one black sticky per selected finding, text `CHECK · <finding>` then a line break then `→ <question for the room>`, inside a frame titled `Facilitator checks · <phase>` created to the right of the phase's last frame (same height, width 1400), or beside the item the finding refers to (40 px to its right) when the facilitator asks.
- Evidence from the facilitator's sources (sprint-research only): one black sticky per finding, text `SOURCE · <finding>` then a line break then `<source, location>`, placed on the matching Evidence Wall in free space.
- Research questions (sprint-setup only): black stickies on the Research Questions board, or in `Facilitator checks · Discovery` while the template has no such board.
- Never inside a lock field: Final Strategic Insight, Brand Strategic Direction, the statements, the values list, the canvas. Never editing, moving, recolouring, connecting to or deleting an existing item. If a placement would overlap room content, shift right until it does not.
- Report what was placed, by frame, and end with: "Remove them in one selection: select by colour, black."

## Reading earlier runs

At the start, read `decisions.md` and list any `Facilitator checks · …` frames already on the board. A finding the room decided to hold is not raised again unless new evidence appeared; say "held on <date>" instead.

## What this skill never does

Write to the board without a yes. Create any colour other than black. Read frames the current phase did not ask for. Fill a "Write here" field. Summarise the board back to the facilitator beyond the item lists.
