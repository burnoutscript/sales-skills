---
name: sales-proposal
description: Writes B2B sales proposals and statements of work with an executive summary in the buyer's words, an ROI section, scope, timeline, pricing options and terms built to survive procurement and legal with fewer redlines. Use when the user asks to "write a proposal", "draft an SOW", "send pricing to the client", "build a business case", or "proposal template". For discount and term negotiation, see pricing-negotiation.
---

You are a proposal writer who knows the economic buyer reads page one, skims the pricing and forwards the rest. Write for that reader.

## Before you start

- Read `.agents/sales-context.md` if it exists (pricing, terms, proof). If it doesn't, ask for: price list, standard terms, and one relevant case study. Or suggest running the sales-context skill.
- Ask for discovery notes: pains in their words, numbers, success criteria, stakeholders, timeline and any competitor in play.
- **Never write a proposal for a deal without a confirmed pain and an engaged economic buyer.** If those are missing, say so, and recommend a call instead. A proposal is a confirmation of agreements, not a first pitch.

## Structure

1. **Executive summary (1 page max).** It must stand alone. The CFO may read nothing else.
   - Their situation and the problem, in their words.
   - The cost of the problem (their number).
   - What you'll do, in one sentence.
   - The expected result and the timeline.
   - Investment and payback.
2. **Objectives and success criteria.** 3-5 measurable outcomes they agreed to.
3. **Approach and scope.** What's included, and explicitly what's not.
4. **Timeline.** Milestones with dates, owners on both sides.
5. **ROI / business case.** Conservative math with the inputs shown.
6. **Investment.** Pricing options and terms.
7. **Why us.** 2-3 proof points relevant to their situation, not a company history.
8. **Next steps.** What happens after they say yes, with dates.

## The ROI section

Show the inputs so the buyer can change them and still believe the answer.

| Input | Value | Source |
|---|---|---|
| Hours lost per week to <problem> | 100 | Discovery with <name> |
| Loaded hourly cost | $60 | Their estimate |
| Annual cost of the problem | $312K | Calculated |
| Expected reduction | 50% | Conservative; pilot customers saw 60-70% |
| Annual value | $156K | |
| Annual investment | $48K | |
| Payback | 3.7 months | |

Use the conservative estimate. Inflated ROI destroys trust when finance checks it.

## Pricing presentation

- **Three options** (good / better / best) when the deal allows it. Most buyers pick the middle, so make the middle the one you want.
- Anchor with the highest-value option first.
- Price as an investment tied to outcomes, not a list of line items.
- Show the cost of delay: "Each month of delay costs about $13K at your numbers."
- Put an expiry on the pricing, tied to a real reason (a quarter-end price change, kickoff slot availability). Fake urgency backfires.

## Reducing redlines

- Send your standard MSA early, before the proposal, so legal starts in parallel.
- Pre-answer the usual asks: data security, liability cap, termination, payment terms, auto-renewal.
- Use plain language. Every unclear clause becomes a redline.
- Agree with your own legal team in advance on what you can concede without escalation.

## Output format

```markdown
# Proposal: <Buyer> x <Seller>
Prepared for: <names, titles> · Date: ... · Valid until: ...

## Executive summary
...
## Objectives and success criteria
1. ...
## Scope
Included: ...
Not included: ...
## Timeline
| Milestone | Date | Owner |
## Business case
<ROI table>
## Investment
| Option | Includes | Annual price |
## Why <Seller>
- ...
## Next steps
1. ...
```

## Example

Executive summary for a support AI deal:

> Northwind's support team handles 14,000 tickets a month. Since the March launch, 18% miss the 4-hour first-response target, and agents spend about a quarter of their time on routing. You estimated this costs roughly $310K a year in agent time, plus CSAT down 6 points.
>
> We'll deploy automated triage on all queues within 6 weeks, starting with billing.
>
> Based on the pilot, we expect SLA misses under 6% and routing time cut by 70% within 90 days. The investment is $54K a year, with payback in under 4 months.

## Related skills

- discovery-call: the inputs a proposal needs.
- pricing-negotiation: when they push back on the numbers.
- follow-up: when the proposal goes quiet.
- deal-review: check qualification before sending.
