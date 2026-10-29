# Sales Skills

16 B2B sales skills for AI agents. They turn Claude Code, Cursor, Codex or any agent that supports [Agent Skills](https://agentskills.io) into a sales assistant that preps your discovery calls, writes outbound people reply to, handles objections and tells you whether a deal is real.

[![skillcheck](https://img.shields.io/badge/skillcheck-100%2F100-2ea043)](https://github.com/burnoutscript/skillcheck)
[![skills](https://img.shields.io/badge/skills-16-blue)](#skills)
[![license](https://img.shields.io/badge/license-MIT-blue)](LICENSE)

I wrote them for founders who do their own selling, and for AEs, SDRs and sales leaders. Each skill takes a position and backs it with a named framework (SPIN, MEDDPICC, give-get, tell-show-tell), templates you can paste, benchmarks and one worked example.

## How it works

```
                        ┌─────────────────┐
                        │  sales-context  │  ← run once: product, ICP, pricing, proof
                        └────────┬────────┘
                                 │ .agents/sales-context.md
     ┌───────────────────────────┼────────────────────────────┐
     ▼                           ▼                            ▼
 PROSPECT                     SELL                         CLOSE
 ideal-customer-profile       discovery-call               sales-proposal
 prospect-research            demo-script                  pricing-negotiation
 cold-email                   objection-handling           deal-review
 outbound-sequence            competitive-battlecard       call-review
 linkedin-outreach            follow-up
 cold-call-script
```

Start with sales-context. It interviews you once and writes `.agents/sales-context.md`, and every other skill reads that file first, so you explain your product, ICP and pricing one time.

## Install

In Claude Code, as a plugin:

```
/plugin marketplace add burnoutscript/sales-skills
/plugin install sales-skills@sales-skills
```

For any agent, with the skills CLI:

```bash
npx skills add burnoutscript/sales-skills
```

Or copy the folders in `skills/` into `.claude/skills/` for one project, or `~/.claude/skills/` for all of them. Other agents have their own skills folder, such as `.cursor/skills/` or `.agents/skills/`.

## Use it

Ask in your own words and the agent picks the skill:

> "Set up my sales context. We sell close automation to finance teams."
>
> "Prep me for a discovery call tomorrow with the VP Support at Northwind."
>
> "Rewrite this cold email, nobody replies: ..."
>
> "They said it's too expensive. How do I respond?"
>
> "Review this deal. Is it really closing this month?"
>
> "Here's the transcript of my call, what did I miss?"

## Skills

### Foundation
| Skill | What it does |
|---|---|
| [sales-context](skills/sales-context/SKILL.md) | Interviews you about product, ICP, personas, pains, pricing, competitors, proof and sales motion, then writes the context file the other skills read. |
| [ideal-customer-profile](skills/ideal-customer-profile/SKILL.md) | Builds an ICP and buyer personas from real customer data, with signals, buying triggers, A/B/C tiers, a scoring model and hard disqualifiers. |

### Prospecting
| Skill | What it does |
|---|---|
| [prospect-research](skills/prospect-research/SKILL.md) | A one-page account brief: priorities, buying triggers, the "why now", the buying group, personalization hooks and a first line. |
| [cold-email](skills/cold-email/SKILL.md) | First-touch emails using problem-led, trigger-based and observation → implication → ask frameworks, plus subject lines and a deliverability check. |
| [outbound-sequence](skills/outbound-sequence/SKILL.md) | Day-by-day cadences across email, LinkedIn and phone, with the copy for every step and a kill-or-keep threshold for each. |
| [linkedin-outreach](skills/linkedin-outreach/SKILL.md) | Connection notes, first DMs, a plan for engaging before you pitch, voice note scripts and InMail. |
| [cold-call-script](skills/cold-call-script/SKILL.md) | Permission-based openers, a 30-second pitch, answers to the first brush-offs, the meeting close and a voicemail. |

### Running the deal
| Skill | What it does |
|---|---|
| [discovery-call](skills/discovery-call/SKILL.md) | Call prep, the upfront contract, the pain funnel, putting a number on the pain and mapping how they buy. Includes a 46-question bank. |
| [demo-script](skills/demo-script/SKILL.md) | Demos that open with the end result and show three scenes tied to pains the buyer named, with a map of what each persona needs to see. |
| [objection-handling](skills/objection-handling/SKILL.md) | The acknowledge → clarify → respond → confirm method and a library of answers for price, timing, competitors, build-in-house, no budget and brush-offs. |
| [competitive-battlecard](skills/competitive-battlecard/SKILL.md) | One-page battlecards that admit where you lose, with landmine questions and answers to competitor claims. |
| [follow-up](skills/follow-up/SKILL.md) | Recaps sent within two hours, mutual action plans and a playbook for deals that went quiet. |

### Closing
| Skill | What it does |
|---|---|
| [sales-proposal](skills/sales-proposal/SKILL.md) | Proposals and SOWs with a one-page executive summary for the CFO, conservative ROI math and good/better/best pricing. |
| [pricing-negotiation](skills/pricing-negotiation/SKILL.md) | Negotiation plans: anchoring, give-get trades, concessions that shrink, procurement tactics, and multi-year or ramp deals. |
| [deal-review](skills/deal-review/SKILL.md) | MEDDPICC scoring that counts only evidence, a champion test, red flags and a forecast category. |
| [call-review](skills/call-review/SKILL.md) | Reads a call transcript for talk ratio, questions, monologues and missed buying signals, and returns a coaching scorecard with timestamps. |

## Example

> You: Review this deal. $90K, closing end of month. Champion is the Support Ops manager, very excited. We demoed and sent pricing. The VP Support was supposed to join but didn't. They're also talking to ConvoIQ.

> Agent (deal-review):
> MEDDPICC: 8/24. Metrics 1 · Economic buyer 0 · Decision criteria 1 · Decision process 1 · Paper process 0 · Pain 2 · Champion 1 · Competition 2
>
> Red flags: pricing went out before the economic buyer was involved, you're single-threaded on a $90K deal, and the close date is your month end rather than anything on their side.
>
> Forecast: Pipeline. Don't commit it.
>
> Next actions:
> 1. Ask the champion to set up 30 minutes with the VP to go over the business case, by Friday.
> 2. Agree on the success metric with the VP.
> 3. Ask for the security questionnaire now so the paper process starts.

## Quality

CI lints every skill with [skillcheck](https://github.com/burnoutscript/skillcheck) in strict mode, and all 16 score 100/100. No two skills claim the same trigger phrase, no link is broken, and every description says when to use the skill.

## Contributing

PRs are welcome, especially new skills (renewals and expansion, partner selling, RFP responses) and better examples from real deals. A new skill needs:

- `skills/<name>/SKILL.md` with `name` and `description` frontmatter
- a "Use when the user..." list of triggers that no other skill uses
- an output format and at least one realistic example
- a clean run of `npx github:burnoutscript/skillcheck skills --strict`

## License

MIT
