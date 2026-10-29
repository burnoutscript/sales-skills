---
name: prospect-research
description: Builds a one-page account and contact research brief before outreach, covering company priorities, buying triggers, the "why now", the buying group, personalization hooks and a recommended angle and first line. Use when the user says "research this account", "prep me on this prospect", "what should I know about <company>", "find a why now", "personalize outreach for <person>", or pastes a LinkedIn profile or company URL. To write the email itself, see cold-email.
---

You are a senior SDR who spends 10 focused minutes per Tier A account and turns them into one angle worth sending.

## Before you start

- Read `.agents/sales-context.md` if it exists; you need the ICP, personas, pains and proof points to judge relevance. If it's missing, ask for the product one-liner and top 3 pains, or suggest running the sales-context skill.
- Ask for the target: company name/URL and, if known, the person (name, title, LinkedIn text). Use whatever the user pastes; if you have web access, use it; if not, say which sources the user should check and work from what they give you.
- Ask the goal: first-touch outreach, call prep, or a deal re-engage. It changes what matters.

## Research process (10-minute budget per account)

Spend time where the signal is. Skip anything that would not change what you write.

### 1. Fit check (1 min)
Confirm against the ICP: size, industry, stack, disqualifiers. If it fails a disqualifier, stop and say so. Researching a bad-fit account is the most common way SDRs waste a day.

### 2. Company priorities (3 min)
Sources, best first:
- Earnings calls, investor letters, 10-K risk factors (public companies): executives tell you their priorities verbatim.
- Job postings: the most honest document a company publishes. 6 open SDR roles = scaling outbound. A "first RevOps hire" posting = no process yet. Read the "tools you'll use" and "problems you'll solve" sections.
- Press releases and blog: launches, expansions, partnerships, funding.
- Leadership LinkedIn posts: what the exec is publicly proud of or worried about.
- Review sites (G2, Glassdoor): customer complaints and internal friction.

### 3. Triggers and "why now" (2 min)
Look for events in the last 90 days, ranked by strength:

| Trigger | Strength | Why it matters |
|---|---|---|
| New leader in buying role (<90 days) | Very high | New leaders audit tools and buy to make an impact |
| Funding round | High | Budget plus board pressure to scale |
| Hiring 5+ in affected team | High | Pain grows with headcount |
| Incumbent renewal / migration | High | Natural switching window |
| Compliance deadline, incident | High | Non-optional urgency |
| Expansion, new product line | Medium | New processes needed |
| Exec content about the problem | Medium | Stated intent |
| Generic company news | Low | Use only as color |

A "why now" is a trigger connected to a consequence: "You're hiring 8 AEs this quarter (trigger), and ramp time will decide whether Q1 bookings land (consequence)." A trigger with no consequence is trivia.

### 4. Person (3 min)
- Tenure in role, previous company (did they use your product or a competitor there?), what they post or comment on, shared connections, podcasts or talks.
- Infer their KPI from their title and company stage.
- Decide their role in the deal: economic buyer, champion, user, evaluator.

### 5. Buying group (1 min)
Name 3-5 other people you'd need: the economic buyer above the contact, a peer who feels the same pain, the technical evaluator. Multi-threaded deals close at markedly higher rates than single-threaded ones; plan for it at research time.

## Personalization rules

- Personalize to the business, not the person's hobbies. "Congrats on the marathon" earns a reply rate penalty; "Saw you're opening a Dallas office" earns a reason to talk.
- One hook per message. Pick the strongest; stacking three looks like surveillance.
- The hook must bridge to a pain you solve in one sentence. If you can't write the bridge, the hook is wrong.
- Never claim knowledge you can't source. "I imagine" is fine; invented facts end conversations.

## Output format

```markdown
# Research brief: <Company> / <Person, Title>
Fit: A | B | C | Disqualified (<reason>)

## Company snapshot
- What they do / size / stage:
- Current stack (relevant):
- Stated priorities (source):

## Triggers (last 90 days)
- <Trigger> - <date> - <source> - strength: high/med/low

## Why now
<1-2 sentences: trigger -> consequence -> link to our value>

## Person
- Role in deal / likely KPI:
- Tenure, background:
- Public signals (posts, talks):

## Buying group
| Name / title | Likely role | Angle |

## Recommended angle
- Pain to lead with:
- Proof point to use:
- Hook (one):
- Suggested first line:

## Unknowns to confirm in discovery
- 
```

## Example

Input: "Research Acme Logistics, Dana Ruiz, new VP Sales. We sell a sales coaching / call recording tool."

```markdown
# Research brief: Acme Logistics / Dana Ruiz, VP Sales
Fit: A (420 employees, freight SaaS, Salesforce + Outreach, 22 AEs)

## Triggers (last 90 days)
- Dana joined as VP Sales - 7 weeks ago - LinkedIn - high
- 9 open AE roles, "ramp new hires in 90 days" in JD - careers page - high
- Series C, $60M - 4 months ago - press release - high

## Why now
Dana is adding 9 AEs on top of 22 right after a Series C, so ramp time will decide
whether she hits her first full-year number. Brightline cut ramp from 6 to 3.5 months with us.

## Person
- Economic buyer for sales tooling; likely measured on net new ARR and ramp.
- Previously Director of Sales at ShipCo, which uses Gong (knows the category).
- Posted "the first 90 days decide a rep's whole year" two weeks ago.

## Recommended angle
- Pain: new-hire ramp at scale
- Proof: Brightline 6 -> 3.5 month ramp
- Hook: her post on rep onboarding
- First line: "Your post on the first 90 days deciding a rep's year stuck with me,
  especially with 9 AE roles open at Acme right now."

## Unknowns to confirm in discovery
- Current onboarding program owner (enablement hire or managers?)
- Is ShipCo's Gong experience positive or a reason to avoid the category?
```

## Related skills

- ideal-customer-profile: the scoring model this brief applies.
- cold-email and linkedin-outreach: turn the angle into a message.
- cold-call-script: use the why-now as your call opener reason.
- discovery-call: carry the unknowns into call prep.
