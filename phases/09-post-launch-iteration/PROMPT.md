# Phase 09 — Post-Launch & Iteration: PROMPT

## Agent Context

You are assisting with Post-Launch operations for a physical product. Your role is to help analyse performance, synthesise customer feedback, troubleshoot issues, and plan product iterations.

Before beginning, read:
- `../../PROJECT.md` for project identity and constraints
- `../08-launch-preparation/HANDOVER.md` for launch details and success metrics
- `./BRIEF.md` for this phase's purpose, sub-task menu and done criteria
- `./WORKBOOK.md` § Phase Plan for the approved sub-task list, once the Phase Plan prompt below has been run

Work under the Operating Policy in `../../AGENTS.md`: tag every figure, standard, supplier or competitor **Verified**, **Estimated** or **Unknown** and never invent a citation; ask before changing a recorded decision, marking a phase `complete` or committing money; run only the sub-task selected.

---

## How to Use This Prompt

Each sub-task below is a standalone prompt. Run them individually, capture outputs in WORKBOOK.md, and use the synthesis prompt at the end to pull everything together for the HANDOVER.

### Before you run a sub-task

1. Read the sub-task prompt and its inputs without carrying it out.
2. List what is unclear or missing, in at most five bullets.
3. If any item would materially change the output, ask the user one question and wait for the answer.
4. Otherwise, state your assumptions at the top of the output and proceed.

---

## Phase Plan Prompt

Run this once, at the start of the phase, before any sub-task. Sub-task selection is recorded in WORKBOOK.md, never by editing BRIEF.md.

```
Plan this phase before running any sub-task. Read:
- `../../PROJECT.md`, for identity, constraints, entry point and current status
- `../08-launch-preparation/HANDOVER.md`, for the context flowing in (if that phase is `skipped`, read Pre-existing Inputs under Entry Point in `../../PROJECT.md` instead)
- `./BRIEF.md`, for the phase purpose, the sub-task menu and the done criteria

Then propose a phase plan:
1. Which sub-tasks to run, from the Core, Conditional and Optional tiers, and in what order
2. For each: one line on why it applies to this project, and the working format you recommend (see the Best format line on each sub-task in PROMPT.md)
3. Which sub-tasks you recommend skipping, and why
4. Anything the done criteria need that the selected sub-tasks do not obviously produce
5. Anything you need from me before starting

Stop and wait for my approval. Once approved, write the agreed list under `## Phase Plan` at the top of `./WORKBOOK.md`, then start with the first sub-task.
```

---

## Sub-Task Prompts

### Performance Analysis

```
Here are my product metrics for [TIME PERIOD]:

[USER PROVIDES: sales, traffic, conversion and ad performance data — paste here, or point me to the files under library/research/; targets are in ../08-launch-preparation/HANDOVER.md § Launch Metrics & Targets]

Help me analyse:

1. **Sales performance** — units, revenue, trend. Vs. targets from Phase 08.
2. **Channel performance** — which channels are performing? Which aren't? Why?
3. **Unit economics reality** — actual COGS, actual selling price, actual margin. Vs. projections.
4. **Customer acquisition** — cost to acquire a customer by channel. Sustainable?
5. **Conversion funnel** — where are people dropping off? What's the biggest leak?
6. **Inventory position** — current stock, sell-through rate, when to reorder.
7. **Key insights** — what's the most important thing the data is telling us?
8. **Recommended actions** — prioritised list of what to do based on the data.
```

### Customer Feedback Synthesis

```
Here is customer feedback from [SOURCES]:

[USER PROVIDES: reviews, emails, social media comments, support tickets, survey responses — paste here, or point me to the files under library/research/]

Synthesise:

1. **Sentiment overview** — overall positive/negative/neutral split
2. **Top praise themes** — what do customers love? (Ranked by frequency)
3. **Top complaint themes** — what do customers dislike or want improved? (Ranked by frequency and severity)
4. **Feature requests** — what are customers asking for that doesn't exist?
5. **Surprise insights** — anything unexpected in how people are using or talking about the product?
6. **Quotes to highlight** — paraphrased customer sentiments that capture key themes (for marketing or internal use)
7. **Action items** — what should change based on this feedback? Prioritised by impact and feasibility.
8. **Cross-reference with Phase 01** — do the actual jobs-to-be-done match what we predicted?
```

### Issue Triage

```
These issues have been reported:

[FROM ./WORKBOOK.md § Issue Log — read it, or paste here if you have no file access]

Help me triage:

| Issue | Frequency | Severity | Root Cause (hypothesis) | Fix Difficulty | Priority |
|---|---|---|---|---|---|
| | | | | | |

For each high-priority issue:
1. Immediate response (what to tell affected customers)
2. Root cause investigation plan
3. Fix options with cost/timeline
4. Prevention plan (how to stop recurrence)

Classify issues:
- **Product defect** — manufacturing or design problem
- **User error** — user doesn't understand how to use it (design or documentation issue)
- **Expectation mismatch** — product works as intended but doesn't meet customer expectations (marketing or positioning issue)
- **Shipping/logistics** — damage in transit, wrong item, delayed delivery
```

### V2 / Iteration Planning

```
Based on everything we've learned post-launch:

Sales data: [FROM ./WORKBOOK.md § Performance Tracking — read it, or paste here if you have no file access]
Customer feedback: [FROM ./WORKBOOK.md § Customer Feedback Log — read it, or paste here if you have no file access]
Competitive developments: [USER PROVIDES: any competitor moves since launch]
Team learnings: [FROM ../../journal/LOG.md and ./WORKBOOK.md § Periodic Reviews — read them, or paste here if you have no file access]

Help me plan the next iteration:

1. **What's working** — elements to preserve and amplify
2. **What needs fixing** — issues to resolve in V2
3. **What's missing** — features or improvements to add
4. **What to remove** — anything that's not adding value and adds cost/complexity
5. **Priority matrix** — impact vs. effort for each proposed change
6. **V2 scope recommendation** — what should V2 include? (Minimum, ideal, stretch)
7. **Timeline and investment estimate** — rough scope of the V2 project
8. **Decision:** Is this a minor revision (tweak within current tooling/production) or a major version (back to Phase 04/05)?
```

### Marketing Optimisation

```
Here's my current marketing performance:

[USER PROVIDES: ad, social, email and organic traffic data — paste here, or point me to the files under library/research/]

Help me optimise:

1. **What's working** — best-performing channels, messages, creative, audiences
2. **What's not working** — underperforming areas to cut or fix
3. **Budget reallocation** — where should spend shift based on performance?
4. **Creative refresh** — what new angles, messages, or formats to test based on customer feedback?
5. **Organic opportunities** — SEO, content, community, PR opportunities based on traction so far
6. **Seasonal planning** — upcoming opportunities (holidays, events, trends) to plan for
7. **30-day marketing plan** — specific, prioritised actions for the next month
```

---

## Output Capture

Capture each sub-task's output in WORKBOOK.md under a heading matching the sub-task name. Every output ends with the Sub-Task Output Footer defined in `config/CONVENTIONS.md`: **Sources & confidence**, **Assumptions made**, **Open questions**, **Candidate decisions**. Keep the four headings even when one is empty; the Critique prompt checks them and the synthesis prompt reads from them.

---

## Ongoing Synthesis (Monthly/Quarterly)

```
It's time for a periodic review. Here's the current state:

[FROM ./WORKBOOK.md § Performance Tracking, § Customer Feedback Log, § Inventory Tracker and § Marketing Performance — read them, or paste here if you have no file access]

Create a state-of-the-product report:

1. **Executive summary** — one paragraph on how things are going
2. **Performance scorecard** — key metrics vs. targets
3. **Customer health** — satisfaction trends, review ratings, repeat purchase rate
4. **Financial health** — margin, cash flow, inventory value
5. **Market position** — any competitive shifts? Market changes?
6. **Top 3 priorities** — the most important things to focus on next
7. **Risks and watch items** — what could go wrong?
8. **V2 readiness** — is it time to start the next development cycle?
```

---

## Critique Prompt

Run this in a **fresh session**, not the one that produced the work. The critic reads the draft handover and the done criteria, nothing else the producer wrote unless it asks. Record disagreements between producer and critic in DECISIONS.md rather than resolving them silently.

```
You are a head of operations who inherits this product line and has to keep it profitable. You are reviewing a draft phase handover, and your job is to find what is wrong or missing, not to be encouraging.

Read:
- `./HANDOVER.md`, the draft handover for this phase
- `./BRIEF.md` § Done Criteria, what this phase was supposed to deliver
- `./WORKBOOK.md`, only where you need to check a claim against its source

Return:
1. **Gaps against the done criteria** — which criteria are not met, or met only on paper
2. **Unsupported claims** — every figure, standard, supplier, competitor or user statement in the handover that is not tagged Verified with a source you can follow. Say which should be downgraded to Estimated or Unknown.
3. **Assumptions treated as facts** — where the handover has quietly converted an assumption into a constraint
4. **What the next cycle will trip over** — the three things most likely to cause rework downstream if left as they are
5. **Your confidence rating** for this handover: High / Medium / Low, with one sentence on what drives it. Where it differs from the producer's rating, say why.

Be specific. Quote the line you are challenging. Do not rewrite the handover; that is the producer's job.
```

---

## Decision Points (Recurring)

- **Continue as-is** — performance is on track, maintain course
- **Optimise** — specific improvements needed within current product
- **Iterate** — V2 development warranted, re-enter chassis at appropriate phase
- **Expand** — add channels, markets, or SKUs
- **Sunset** — product isn't viable, plan wind-down

