# Phase 09 — Post-Launch & Iteration: PROMPT

## Agent Context

You are assisting with Post-Launch operations for a physical product. Your role is to help analyse performance, synthesise customer feedback, troubleshoot issues, and plan product iterations.

Before beginning, read:
- `../../PROJECT.md` for project identity and constraints
- `../08-launch-preparation/HANDOVER.md` for launch details and success metrics
- `./BRIEF.md` for this phase's sub-tasks

---

## Sub-Task Prompts

### Performance Analysis

```
Here are my product metrics for [TIME PERIOD]:

[USER INSERTS SALES DATA, TRAFFIC DATA, CONVERSION DATA, AD PERFORMANCE, ETC.]

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

[USER PASTES REVIEWS, EMAILS, SOCIAL MEDIA COMMENTS, SUPPORT TICKETS, SURVEY RESPONSES]

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

[USER INSERTS LIST OF ISSUES — defects, complaints, problems]

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

Sales data: [USER INSERTS SUMMARY]
Customer feedback: [USER INSERTS KEY THEMES]
Competitive developments: [USER INSERTS ANY CHANGES]
Team learnings: [USER INSERTS WHAT THE TEAM HAS LEARNED]

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

[USER INSERTS AD DATA, SOCIAL METRICS, EMAIL METRICS, ORGANIC TRAFFIC DATA]

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

## Ongoing Synthesis (Monthly/Quarterly)

```
It's time for a periodic review. Here's the current state:

[USER INSERTS PERFORMANCE DATA, FEEDBACK SUMMARY, INVENTORY STATUS, MARKETING RESULTS]

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

## Decision Points (Recurring)

- **Continue as-is** — performance is on track, maintain course
- **Optimise** — specific improvements needed within current product
- **Iterate** — V2 development warranted, re-enter chassis at appropriate phase
- **Expand** — add channels, markets, or SKUs
- **Sunset** — product isn't viable, plan wind-down

