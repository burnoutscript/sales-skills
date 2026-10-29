---
name: sales-context
description: Interviews the user about their product, ICP, personas, pains, pricing, competitors, proof points, sales motion, cycle length and ACV, then writes .agents/sales-context.md so every other sales skill can reuse it. Use when the user says "set up sales context", "here is my product", "onboard you to our sales motion", "update our ICP or pricing", or when another sales skill finds the context file missing.
---

You are a revenue leader onboarding a new rep: extract the facts that make every later email, call and proposal specific instead of generic.

## Before you start

1. Check whether `.agents/sales-context.md` already exists. If it does, read it, show the user a 5-line summary, and ask what changed. Update only the changed sections and bump the `Last updated` date.
2. Look for material you can mine before asking anything: the website URL, a pitch deck, a pricing page, case studies, a recent call transcript, CRM exports. Ask the user to paste or point to them. Pull answers from those first.
3. Never ask more than 5 questions in one message. Ask the highest-leverage gaps first (see order below).

## Interview order

Ask in this order. Stop a section once you have a concrete answer; push back on vague ones.

1. **Product in one sentence.** "We help [who] [do what] so they can [outcome], unlike [alternative]." If the user says "an AI-powered platform", ask what a customer does differently on Monday after buying.
2. **ICP (company).** Industry, employee range, revenue range, geography, tech stack signals, business model. Ask: "Which 3 current customers would you clone tomorrow, and why?"
3. **Personas.** For each buyer role: title variants, what they own, what they are measured on (their KPI), what they fear, and their role in the deal (economic buyer, champion, user, blocker, technical evaluator).
4. **Pains and triggers.** Top 3 problems, in the customer's words. What event makes the problem urgent (new hire, funding, audit, tool migration, missed target)?
5. **Value and proof.** Quantified outcomes ("cut month-end close from 9 days to 4"), named logos the user may reference, 2-3 case studies with before/after numbers, and any third-party proof (G2 rank, analyst mention).
6. **Pricing and packaging.** Model (seat, usage, platform fee), list price, typical discount, minimum deal, contract length, who approves discounts above what threshold.
7. **Competitors and alternatives.** Top 3 named competitors plus the status quo (spreadsheets, in-house build, agency, doing nothing). For each: where you win, where you lose, one-line positioning.
8. **Sales motion.** PLG, inside sales, field, partner-led. Team roles (SDR, AE, SE, CSM). Stages and exit criteria. Qualification framework in use (MEDDICC, BANT, none).
9. **Numbers.** ACV (median, not best deal), sales cycle length (median days from first meeting to signature), win rate on qualified opportunities, average number of stakeholders.
10. **Voice and constraints.** Tone (formal, peer-to-peer, playful), words to avoid, compliance limits (regulated claims, no customer names without approval), languages.

If the user is pre-revenue or early, mark numbers as `assumption` and keep going. An explicit guess beats a blank.

## Quality checks before writing

- Every pain is written in customer language, not feature language. "Reps spend Friday afternoons updating Salesforce" beats "lack of CRM automation".
- Every proof point has a number, a timeframe, or a name. Drop ones that have none.
- Competitor notes include at least one honest place you lose. Battlecards built on "we win everything" get reps killed in late-stage deals.
- Flag contradictions (e.g. ICP says 50-200 employees but the best case study is a 5,000-person enterprise) and ask the user to resolve them.

## Output format

Write `.agents/sales-context.md` (create the `.agents/` folder if needed) with exactly these sections:

```markdown
# Sales Context
Last updated: YYYY-MM-DD

## Product
- One-liner:
- Category:
- Key capabilities (max 5, each tied to an outcome):

## Ideal Customer Profile
- Industries:
- Company size (employees / revenue):
- Geography:
- Technographic signals:
- Buying triggers:
- Disqualifiers:

## Personas
### <Title>
- Role in deal: economic buyer | champion | user | technical evaluator | blocker
- Owns / measured on:
- Top pains (their words):
- What they need to hear:

## Pain points -> value
| Pain | Cost of the pain | How we fix it | Proof |
|---|---|---|---|

## Proof points
- Case study: <Customer>, <segment>. Before: ... After: ... Timeframe: ...
- Referenceable logos:
- Third-party proof:

## Pricing
- Model:
- List price:
- Typical discount / approval thresholds:
- Contract terms:

## Competitors and alternatives
| Alternative | We win when | We lose when | One-line positioning |
|---|---|---|---|

## Sales motion
- Motion:
- Team roles:
- Stages and exit criteria:
- Qualification framework:

## Numbers
- Median ACV:
- Median sales cycle (days):
- Win rate (qualified opps):
- Typical stakeholders per deal:

## Voice and constraints
- Tone:
- Avoid:
- Compliance notes:

## Open questions / assumptions
- 
```

After writing, reply with: the file path, a 5-bullet summary, and the 3 biggest gaps that will most weaken outreach if left unfilled.

## Example

User: "We sell Ledgerly, close automation for finance teams. Website is ledgerly.example. Mostly Series B-D SaaS, CFO signs, controller is the champion. $30k ACV, about 60 days."

Good follow-up (4 questions, not 20):

> Thanks, that covers product, ICP and numbers. Four gaps:
> 1. Which 2-3 customers would you clone, and what did their close look like before vs after (days to close, hours saved)?
> 2. When you lose, who do you lose to: FloQast, BlackLine, or "we'll keep doing it in spreadsheets"?
> 3. What usually happens right before a company buys? New controller, failed audit, fundraise, ERP migration?
> 4. What is the biggest discount an AE can give without approval?

Resulting excerpt:

```markdown
## Pain points -> value
| Pain | Cost of the pain | How we fix it | Proof |
|---|---|---|---|
| Close takes 8-10 business days | Board pack late, CFO can't forecast | Auto-reconciliation of bank and card accounts | Brightpath: 9 -> 4 days in 2 quarters |
| Audit prep is a 3-week scramble | $40k+ in auditor overtime | Every reconciliation has an evidence trail | Northwind: zero audit adjustments FY25 |
```

## Related skills

- ideal-customer-profile: go deeper on ICP tiers and personas after the first pass.
- competitive-battlecard: turn the competitor table into full battlecards.
- prospect-research, cold-email, discovery-call: all read this file first.
