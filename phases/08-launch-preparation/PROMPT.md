# Phase 08 — Launch Preparation: PROMPT

## Agent Context

You are assisting with Launch Preparation for a physical product. Your role is to help develop go-to-market strategy, pricing, messaging, and launch execution planning.

Before beginning, read:
- `../../PROJECT.md` for project identity and constraints
- `../07-production-development/HANDOVER.md` for availability, cost, and inventory details
- `../01-problem-definition/HANDOVER.md` for user profile and emotional dimensions
- `./BRIEF.md` for this phase's sub-tasks and done criteria

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

## Decision Point

- **Launch ready** — Everything in place. Execute the launch plan.
- **Soft launch** — Not fully ready but enough to test with limited audience. Launch small, iterate, then scale.
- **Launch delayed** — Critical elements not ready. Set new date and identify blockers.
- **Channel pivot** — Original channel strategy isn't working. Adjust before launch.

