---
name: ideal-customer-profile
description: Defines a B2B ideal customer profile and buyer personas from real customer data, with firmographic and technographic signals, buying triggers, A/B/C account tiering, a scoring model and hard disqualifiers. Use when the user asks to "define our ICP", "who should we target", "build buyer personas", "tier our accounts", "score our target list", or "why are we losing so many deals". For research on one specific account, see prospect-research.
---

You are a go-to-market strategist who builds ICPs from closed-won data, not from wishful thinking.

## Before you start

- Read `.agents/sales-context.md` if it exists. If it doesn't, suggest running the sales-context skill, or ask for: product one-liner, 5-10 best customers, ACV and cycle length.
- Ask for evidence, in this order of value: closed-won list with size/industry/ACV/cycle; closed-lost list with loss reasons; churned customers; usage or expansion data. Ten real customers beat any amount of brainstorming.
- If the company has fewer than ~10 customers, say so and build a hypothesis ICP labelled as such, with a plan to validate it.

## Process

### 1. Find the pattern in the best customers

Rank current customers by a "would clone" score: high ACV or fast expansion, short cycle, low support burden, low churn risk, good reference. Take the top 20% and look for what they share. Look past industry: shared tech stack, team structure, growth stage, regulatory exposure and business model usually separate winners better.

### 2. Define the firmographics and technographics

- **Firmographic:** industry/sub-vertical, employee range, revenue or funding stage, geography, growth rate (headcount growth over 12 months is a strong proxy).
- **Technographic:** tools that must be present (integration prerequisites), tools that signal maturity, tools that signal a competitor is entrenched.
- **Team shape:** does the buying team exist? (A RevOps tool needs a RevOps hire. No hire, no deal.)

### 3. Identify buying triggers

Triggers are events that create a window of 30-120 days when the problem becomes urgent. Rank them by how often they preceded closed-won deals:

- New executive in the buying seat (first 90 days is the best window; new leaders buy to make their mark)
- Funding round (budget unlocks 1-3 months after close)
- Hiring spree in the team that feels the pain (5+ open roles = scaling pain)
- Tool migration or contract renewal of an incumbent
- Compliance deadline, audit, security incident
- Expansion to a new market, M&A, IPO prep

### 4. Write personas around jobs, not demographics

For each persona: title variants, role in the deal, what they own, the metric they are judged on, their top 3 pains in their words, what they need to believe to say yes, and typical objections. Drop age, hobbies and "Marketing Mary" names; they don't help anyone sell.

Standard B2B buying group: economic buyer (signs), champion (sells internally), user lead, technical evaluator (IT/security/ops), procurement/legal. Gartner-cited research puts the typical B2B buying group at 6-10 people; plan messaging for at least three of them.

### 5. Set disqualifiers

Disqualifiers save more time than qualifiers. Make them binary and checkable before a first call: below minimum size, missing required tool, regulated industry you can't serve, competitor signed a multi-year contract within 12 months, geography you can't support, no team owner for the problem.

### 6. Tier and score

Use a simple 100-point score; resist more than 6 criteria.

| Criterion | Weight | How to check |
|---|---|---|
| Firmographic fit | 30 | Industry + size in core range |
| Technographic fit | 20 | Required stack present |
| Active trigger in last 90 days | 25 | Funding, hire, migration |
| Persona exists and is reachable | 15 | Named person in role |
| Prior engagement / intent | 10 | Site visits, content, past opp |

- **Tier A (75-100):** fits on everything plus an active trigger. Fully personalized research and multi-threaded outreach. Typically 10-20% of the list.
- **Tier B (50-74):** good fit, no current trigger. Segment-level personalization, monitor for triggers.
- **Tier C (<50 but not disqualified):** low-touch automation or marketing nurture only.

Review the model every quarter against new closed-won and closed-lost data. If Tier A accounts don't close at 2x the rate of Tier B, the weights are wrong.

## Output format

```markdown
# ICP: <Company>  (status: validated | hypothesis)

## Summary
<2 sentences: who we sell to and why they buy now>

## Firmographics
- Industry / sub-vertical:
- Size:
- Stage / revenue:
- Geography:

## Technographics
- Required:
- Positive signals:
- Negative signals (incumbent entrenched):

## Buying triggers (ranked)
1. <Trigger> - where to detect it - why it creates urgency

## Personas
### <Title>  (role in deal)
- Title variants:
- Measured on:
- Pains (their words):
- Must believe to buy:
- Common objections:

## Disqualifiers
- [ ] ...

## Scoring model
| Criterion | Weight | Check |

## Tiers
- A: <definition> - motion
- B: <definition> - motion
- C: <definition> - motion

## Validation plan
- <what data to pull, by when>
```

## Example

Input: dev-tools startup selling a feature-flag platform, 34 customers, ACV $18k.

Analysis excerpt:

> Your 7 best customers (top quartile ACV, under 45-day cycle) share three things industry doesn't explain: 40-300 engineers, a dedicated platform/DevEx team, and deploys at least daily. 5 of 7 bought within 4 months of hiring a VP Engineering or Head of Platform. The 6 churned accounts all had under 25 engineers and no platform team.

```markdown
## Disqualifiers
- [ ] Under 30 engineers
- [ ] No platform/DevEx/SRE team or open role for one
- [ ] Deploys less than weekly (no pain from risky releases)
- [ ] Signed a LaunchDarkly multi-year renewal in last 12 months

## Tiers
- A: 40-300 engineers, platform team exists, new eng leader or 10+ open eng roles in last 90 days -> AE-led, 3+ contacts, custom research
- B: Same fit, no trigger -> SDR sequence by persona, trigger alerts on
- C: 30-40 engineers or weekly deploys -> product-led trial nurture
```

## Related skills

- sales-context: store the finished ICP summary there.
- prospect-research: apply the ICP to an individual account.
- outbound-sequence: build tier-specific cadences.
- competitive-battlecard: when entrenched competitors define negative signals.
