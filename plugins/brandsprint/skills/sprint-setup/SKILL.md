---
name: sprint-setup
description: Entry point of the AI-augmented 5-Day BrandSprint. Run once in Cowork after Onboarding and the Discovery & Clarity day. Interviews the facilitator, creates the project folder and project.md, reads the Onboarding and Discovery frames on the Miro board, tests them for gaps and contradictions, and returns the gap list as candidate research questions. Never fills a Discovery board.
---

# Sprint setup

Load `sprint-board` first; its rule, report format and placement rules apply in full.

## When

Once per sprint, after the Onboarding session and the Discovery & Clarity day, before Research Preparation. If the Discovery frames are still empty, do the interview and the folder, and tell the facilitator to come back after the Discovery day for the analysis.

## What this skill is for

Two jobs. First, it collects what no board holds and writes it down once, so the nine skills that follow never have to ask. Second, it does what the guide asks the room to do in the last 25 minutes of the Discovery day, slowly and with every board open: find every gap, every contradiction and every unproven claim, and turn each into a question research can answer. The Research Questions board is the Discovery day's main output and Research Prep starts from it; this skill makes sure nothing fell off it.

## Step 1 · The interview

Ask these in one message, as a numbered list, and accept partial answers. Fill project.md with what comes back and mark the rest "open".

1. Client and brand name. Category, in one line.
2. The brief, as the client gave it: what they want from the sprint.
3. Sprint dates, and the format: live, online, or mixed. Language of the room.
4. The Decider, by name and role.
5. Who is on the sprint team, with role (check against the five seats: the one who can say yes, marketing and creatives, product or operations, sales or support, one skeptic). Which seats are empty.
6. The brand assets that can't change (name, logo, tagline, colours) and the reason for each.
7. The Miro board URL for this sprint.
8. Which sticky colour the room uses for EVIDENCE and which for ASSUMPTION.
9. Consent agreed with the client: recording, photos of the canvases, the board the client keeps afterward, and whether the AI-assisted checks are disclosed in the proposal (the guide's line: nothing on the board is written by AI; its job is to catch what a tired room misses).
10. The folder on disk where the project should live.
11. Anything the facilitator already knows that the boards don't say: history with the client, politics in the room, a previous agency, a deadline behind the sprint.

Do not ask again for anything the facilitator answered.

## Step 2 · The folder

Inside the folder from question 10, create:

```
<Client> · 5-Day Sprint/
  00 Project/ project.md · decisions.md · sources/
  01 Before the Sprint/ Discovery/ · Research Prep/ · Research/sources/
  02 The Sprint/ Day 1/ · Day 2/ · Day 3/ · Day 4/ · Day 5/
  03 After the Sprint/
```

`project.md`, in this order, one line per item, "open" where unanswered:

```
# <Client> · 5-Day Sprint · project
Client / brand:
Category:
Brief:
Dates: · Format: · Language:
Decider:
Team: name · role · seat (one per line) · Empty seats:
Assets that can't change: asset · reason (one per line)
Board: <URL>
Colours: EVIDENCE = · ASSUMPTION = · facilitator = black
Consent: recording · photos · board handover · AI disclosure
Context from the facilitator:
Setup run: <date>
```

`decisions.md` starts with one line: `<date> · sprint-setup run · project created`.

If a file the facilitator gave in the interview belongs to no phase (the proposal, the client's brief, an old brand book), save it in `00 Project/sources/` and list it in project.md under Context.

## Step 3 · Read the boards

Through `sprint-board`, read:

Onboarding: `Welcome to the Sprint`, every `Team Roles` frame, `Expectations Mapping`, `Workshop Good Practices`.

Discovery: `Who are we?`, `Vision & Purpose`, `Objectives & Pain Points`, `Products & Services`, `Strenghts & Weaknesses`, `Competitor Landscape`, `Geographical Coverage`, `Touchpoints & Channels`, `Brand Perception`, and `Research Questions` if the board has one (the template does not yet; say so).

Report the inventory first.

## Canvas layouts

Positions as fractions of the frame. Verify on the first run against the canvas image if the items don't fit the map.

Team Roles: one slot per person: name, sprint role, objectives owned. Three frames exist on the template; read all.

Expectations Mapping: four quadrants. Top-left "Project goals from my perspective". Top-right "Unanswered questions to the project". Bottom-left "What I like to end project with". Bottom-right "Things to consider for the project".

Who are we?: three columns, left to right: what we are, what business we're in, what problem we solve.

Vision & Purpose: two areas, Vision left (or top), Purpose right (or bottom).

Objectives & Pain Points: objectives left, pain points right; connectors between them are the lines the room drew.

Products & Services: concentric. Centre is the core offer, rings outward are supporting products, then add-ons and occasional services. Read by distance from the frame centre.

Strenghts & Weaknesses: strengths left half, weaknesses right half. A proof sticky sits next to the strength it proves.

Competitor Landscape: direct competitors left, indirect right. Marked threats carry a mark or a second sticky.

Geographical Coverage: current reach left, future reach right, with timeline notes.

Touchpoints & Channels: three zones, Digital, Traditional, Direct, left to right.

Brand Perception: positive left, negative right.

## Step 4 · Tests

Run in order; record each result before the next. "Not testable" with the reason where a frame is missing or empty.

### T1 · The team
The five seats against the Team Roles frames and the interview: which seat has no name. The Decider named on the board or only in the interview. Anyone on the team not booked for all five days, from the interview. An empty seat the sprint can't run without ("the one who can say yes") is severity blocks.

### T2 · Expectations
Read across the four quadrants: where two people expect different outcomes (goals vs "what I like to end with"), quote both stickies. Unanswered questions with no owner and date. The guide's advice: the gap between people, not the overlap, is the alignment to fix before the sprint.

### T3 · Who are we, three answers
Do the three columns agree with each other? Does the "what problem we solve" column match the core offer on Products & Services? Does "what business we're in" match the category in the brief? Each mismatch is a gap, quoted.

### T4 · Vision and purpose
Count the distinct purposes written. Five people, five reasons is a research question, in the guide's words. A purpose that is a vision (where we want to be) or a vision that is a purpose (why we exist) is a finding. Is there a shared version written, or every version kept?

### T5 · Objectives against pain points
Every sharp pain point should point at an objective it blocks. Pain points with no line, objectives with no pain point. The tension the guide names: ambition high, pain points say the company can't deliver today. Quote it if it is on the board.

### T6 · The core offer
Is one thing in the centre, or several? The guide: if everything sits in the core, there is no focus. Does the core match what Brand Perception says customers see the brand for?

### T7 · Strengths without proof
Every strength needs a proof: a number, a result, something a customer said. List the strengths with no proof sticky and no assumption label. Each weakness should name what it costs (customers, margin, speed); list those that don't.

### T8 · Competitors
No indirect competitors is a finding (the guide: the ones brands usually miss). Are the three biggest threats marked, with a reason? Do the competitors named here reappear on Brand Perception or Strengths (a competitor named nowhere else is an assumption about the market).

### T9 · Reach against capacity
A large gap between current and future reach with nothing written on what it would take (people, money, partners) is a strategic risk, not an ambition, in the guide's words.

### T10 · Touchpoints
Touchpoints marked as mattering most to customers vs the ones the team spends on. Zones with nothing in them (the guide: the empty zone is often the opportunity). Touchpoints nobody inside the company owns.

### T11 · Perception
Each sticky tagged evidence (heard or read, with a source) or assumption; list the untagged. The three perceptions research should test first: marked or not. The gap between real and desired perception, if both are on the board, quoted.

### T12 · The Research Questions board
If it exists: every gap found in T2 to T11 should be on it as a question naming its source board. List the gaps that are not. Then test each question that is there: is it a question research can answer, or still a statement ("we don't agree on the audience" instead of "who buys from us today, and why?"). Are the assets that can't change on it with their reasons.
If it does not exist: say so, and treat the whole candidate list from Step 5 as what the board should hold.

## Step 5 · Candidate research questions

From every gap in T3 to T11, write one question research can answer, tagged with the board it came from, in the room's own words wherever a sticky supplies them. This is a question, not an answer, and not a finding about the brand; it is the one place in this skill where you write new text, and it stays within what the guide asks the room to produce on the Research Questions board.

Group by the five Mindmap branches: audience, competitors, market, trends, organization. Star the ones whose answer would change the strategy if it surprised the room; those get researched first.

## Step 6 · Report and placement

Write `01 Before the Sprint/Discovery/report-<date>.md` in the `sprint-board` format, with the candidate questions as section 4 (Readings) and the five-branch grouping as section 6 (Next steps: what to carry to the Mindmap).

Then the closing question, exactly: "Place the candidate research questions on the board as black stickies (on Research Questions, or in a 'Facilitator checks · Discovery' frame if the board has none)? yes / no / choose". Follow `sprint-board` for placement. Append the run to `decisions.md`.

## What this skill never does

Fill a Discovery board. Answer "who are we", write a purpose, name the core offer, or decide a competitor's threat level. Rank the room's answers against each other. Research the client on the web (that is the Research phase, with the facilitator's sources). Write to the board before the closing question is answered.
