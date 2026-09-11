# Phase 08 — Launch Preparation: PROMPT

## Agent Context

You are assisting with Launch Preparation for a physical product. Your role is to help develop go-to-market strategy, pricing, messaging, and launch execution planning.

Before beginning, read:
- `../../PROJECT.md` for project identity and constraints
- `../07-production-development/HANDOVER.md` for availability, cost, and inventory details
- `../01-problem-definition/HANDOVER.md` for user profile and emotional dimensions
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
- `../07-production-development/HANDOVER.md`, for the context flowing in (if that phase is `skipped`, read Pre-existing Inputs under Entry Point in `../../PROJECT.md` instead)
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

### Pricing Strategy

```
Help me set pricing for this product:

Product: [USER INSERTS DESCRIPTION]
Landed COGS: [USER INSERTS FROM PHASE 07]
Target channels: [USER INSERTS — DTC, retail, Amazon, etc.]
Competitive price landscape: [USER INSERTS FROM PHASE 02]
Positioning: [Premium / Mid-market / Value]
Target customer: [USER INSERTS FROM PHASE 01]

Develop:

1. **Retail price recommendation** — with rationale
2. **Channel pricing matrix:**
   | Channel | Selling Price | Channel Cost/Margin | Net to You | Margin % |
   |---|---|---|---|---|
3. **Promotional pricing plan** — launch discounts, bundle pricing, seasonal strategy
4. **Price sensitivity analysis** — what happens to volume at +/- 10-20%?
5. **Psychological pricing** — price point optimisation (€29.99 vs €34.99 vs €39.99)
6. **Comparison to alternatives** — does the price make sense relative to what users pay now?
7. **Margin safety check** — at the recommended price, is margin healthy across all channels?
```

### Brand Messaging & Positioning

```
Help me develop core messaging for this product:

Product: [USER INSERTS DESCRIPTION]
Target user: [USER INSERTS FROM PHASE 01]
Jobs-to-be-done: [USER INSERTS TOP 3 FROM PHASE 01]
Competitive positioning: [USER INSERTS FROM PHASE 02]
Brand personality: [USER INSERTS FROM PHASE 03]
Emotional dimension: [USER INSERTS FROM PHASE 01]

Develop:

1. **Positioning statement** — For [target user] who [need/want], [product] is [category] that [key differentiator]. Unlike [alternatives], it [unique value].
2. **Value proposition** — the core promise in one sentence
3. **Key messages** (3-5) — the main things to communicate, in priority order
4. **Tagline options** (3-5) — short, memorable, evocative
5. **Elevator pitch** — 30-second spoken description
6. **Tone of voice guidelines** — how the brand speaks (with examples of do/don't)
7. **Message-to-channel mapping** — which messages work best in which contexts (packaging, social, PR, retail)
```

### Launch Plan

```
Help me create a launch plan:

Product: [USER INSERTS DESCRIPTION]
Product availability date: [USER INSERTS FROM PHASE 07]
Channels: [USER INSERTS SELECTED CHANNELS]
Budget: [USER INSERTS MARKETING/LAUNCH BUDGET]
Team size: [USER INSERTS — likely solo or very small]

Build a launch timeline covering:

1. **Pre-launch (8-12 weeks before):**
   - Audience building activities
   - Content creation
   - Channel setup
   - PR and influencer seeding

2. **Launch week:**
   - Day-by-day activity plan
   - Announcement sequence
   - Promotional offers
   - Outreach blitz

3. **Post-launch (first 30 days):**
   - Sustained marketing activities
   - Review solicitation
   - Performance monitoring
   - Iteration based on early data

4. **Resource reality check** — is this achievable with the available team and budget?
5. **Contingency plan** — what if launch day doesn't hit targets? What levers exist?
6. **Success metrics** — what does a good launch look like? Define measurable targets for day 1, week 1, month 1.
```

### E-Commerce Setup

```
Help me plan the e-commerce presence for:

Product: [USER INSERTS DESCRIPTION]
Primary platform: [Shopify / Own site / Amazon / Other]
Budget: [USER INSERTS]

Define:

1. **Product page structure** — what sections, what information, what media
2. **Product photography shot list** — what images are needed (hero, lifestyle, detail, scale, packaging)
3. **Product description** — draft copy for the main product page
4. **SEO keywords** — target search terms for organic discovery
5. **Technical setup checklist** — payment, shipping zones, tax, analytics, email capture
6. **Trust signals** — reviews strategy, guarantees, social proof, certifications to display
7. **Conversion optimisation basics** — key principles for a high-converting product page
```

### Retail Sales Preparation

```
I'm preparing to sell this product through retail channels:

Product: [USER INSERTS DESCRIPTION AND RETAIL PRICE]
Target retailers: [USER INSERTS — specific stores or types]
Margin structure: [USER INSERTS]

Help me create:

1. **Sell sheet / line sheet** — key information a retail buyer needs: product description, wholesale price, RRP, MOQ, case pack, dimensions, weight, barcode, lead time, imagery
2. **Buyer outreach approach** — how to reach retail buyers, what to say, how to follow up
3. **Trade show preparation** — if relevant: which shows, booth requirements, what to bring
4. **Retail requirements checklist** — barcodes (UPC/EAN), retail-ready packaging, EDI capability, insurance, payment terms
5. **Consignment vs. wholesale** — pros/cons for this product at this stage
```

### Investor / Funder Communications

```
I have external funders/investors and need to keep them informed as we approach launch:

Funding type: [USER INSERTS — angel, VC, crowdfunding backers, grant body]
What was promised: [USER INSERTS — milestones, timeline, deliverables committed to]
Current status: [USER INSERTS — what's on track, what's changed]

Help me:

1. **Update template** — draft a professional investor/backer update covering:
   - Progress since last update
   - Key milestones hit
   - Timeline status (on track / adjusted — be honest)
   - Financial status (spend vs. budget)
   - Next steps and upcoming milestones
   - Any asks (introductions, advice, additional support)

2. **Reporting cadence** — recommended frequency and format for different funder types
3. **Bad news handling** — if there are delays or cost overruns, how to communicate proactively and constructively
4. **Backer-specific (crowdfunding)** — update cadence, tone, managing expectations, handling delays, stretch goal delivery status
5. **Relationship maintenance** — how to keep funders engaged and supportive beyond just reporting obligations
```

---

## Output Capture

Capture each sub-task's output in WORKBOOK.md under a heading matching the sub-task name. Every output ends with the Sub-Task Output Footer defined in `config/CONVENTIONS.md`: **Sources & confidence**, **Assumptions made**, **Open questions**, **Candidate decisions**. Keep the four headings even when one is empty; the Critique prompt checks them and the synthesis prompt reads from them.

---

## Synthesis Prompt

```
Launch preparation is complete. Here are the key outputs:

[USER PASTES PRICING, MESSAGING, LAUNCH PLAN, CHANNEL SETUP STATUS]

Synthesise into a HANDOVER for Phase 09 (Post-Launch & Iteration). Include:
1. Launch readiness summary
2. Pricing and channel summary
3. Core messaging and positioning
4. Launch timeline key dates
5. Success metrics and targets
6. Known gaps or risks for launch
7. Confidence rating
```

---

## Critique Prompt

Run this in a **fresh session**, not the one that produced the work. The critic reads the draft handover and the done criteria, nothing else the producer wrote unless it asks. Record disagreements between producer and critic in DECISIONS.md rather than resolving them silently.

```
You are a launch lead who has run go-to-market for physical products and knows where plans break on day one. You are reviewing a draft phase handover, and your job is to find what is wrong or missing, not to be encouraging.

Read:
- `./HANDOVER.md`, the draft handover for this phase
- `./BRIEF.md` § Done Criteria, what this phase was supposed to deliver
- `./WORKBOOK.md`, only where you need to check a claim against its source

Return:
1. **Gaps against the done criteria** — which criteria are not met, or met only on paper
2. **Unsupported claims** — every figure, standard, supplier, competitor or user statement in the handover that is not tagged Verified with a source you can follow. Say which should be downgraded to Estimated or Unknown.
3. **Assumptions treated as facts** — where the handover has quietly converted an assumption into a constraint
4. **What Phase 09 (Post-Launch & Iteration) will trip over** — the three things most likely to cause rework downstream if left as they are
5. **Your confidence rating** for this handover: High / Medium / Low, with one sentence on what drives it. Where it differs from the producer's rating, say why.

Be specific. Quote the line you are challenging. Do not rewrite the handover; that is the producer's job.
```

---

## Decision Point

- **Launch ready** — Everything in place. Execute the launch plan.
- **Soft launch** — Not fully ready but enough to test with limited audience. Launch small, iterate, then scale.
- **Launch delayed** — Critical elements not ready. Set new date and identify blockers.
- **Channel pivot** — Original channel strategy isn't working. Adjust before launch.

