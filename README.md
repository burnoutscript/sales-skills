# Sales Skills

**16 B2B sales skills for AI agents.** Turn Claude Code, Cursor, Codex or any agent that supports [Agent Skills](https://agentskills.io) into a sales team that preps your discovery calls, writes outbound that gets replies, handles objections and tells you honestly whether a deal is real.

[![skillcheck](https://img.shields.io/badge/skillcheck-100%2F100-2ea043)](https://github.com/burnoutscript/skillcheck)
[![skills](https://img.shields.io/badge/skills-16-blue)](#skills)
[![license](https://img.shields.io/badge/license-MIT-blue)](LICENSE)

Built for founders doing their own sales, AEs, SDRs and sales leaders. Every skill is opinionated, comes with real frameworks (SPIN, MEDDPICC, give-get, tell-show-tell), copy-paste templates, benchmarks and a worked example.

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

Start with **sales-context**. It interviews you once and writes `.agents/sales-context.md`. Every other skill reads it first, so you never explain your product, ICP or pricing again.

## Install

**Claude Code (plugin):**

```
/plugin marketplace add burnoutscript/sales-skills
/plugin install sales-skills@sales-skills
```

**Any agent (skills CLI):**

```bash
npx skills add burnoutscript/sales-skills
```

**Manual:** copy the folders in `skills/` into `.claude/skills/` (project) or `~/.claude/skills/` (global). For other agents, use their skills directory, such as `.cursor/skills/` or `.agents/skills/`.

## Use it

Just ask. The agent picks the right skill from your words:

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
| [sales-context](skills/sales-context/SKILL.md) | Interviews you about product, ICP, personas, pains, pricing, competitors, proof and sales motion, and writes the context file every other skill reuses. |
| [ideal-customer-profile](skills/ideal-customer-profile/SKILL.md) | ICP and buyer personas from real customer data, with signals, buying triggers, A/B/C tiering, a scoring model and hard disqualifiers. |

### Prospecting
| Skill | What it does |
|---|---|
| [prospect-research](skills/prospect-research/SKILL.md) | A one-page account brief: priorities, buying triggers, the "why now", the buying group, personalization hooks and a first line. |
| [cold-email](skills/cold-email/SKILL.md) | First-touch emails using problem-led, trigger-based and observation → implication → ask frameworks, plus subject lines and a deliverability check. |
| [outbound-sequence](skills/outbound-sequence/SKILL.md) | Multichannel cadences (email, LinkedIn, phone) day by day, with every step written and kill/keep thresholds per step. |
| [linkedin-outreach](skills/linkedin-outreach/SKILL.md) | Connection notes, first DMs, engage-before-pitch plans, voice note scripts and InMail. |
| [cold-call-script](skills/cold-call-script/SKILL.md) | Permission-based openers, a 30-second pitch, brush-off handling, the meeting close and voicemail. |

### Running the deal
| Skill | What it does |
|---|---|
| [discovery-call](skills/discovery-call/SKILL.md) | Call prep, upfront contract, pain funnel, quantifying the pain and mapping the buying process. Includes a 46-question bank. |
| [demo-script](skills/demo-script/SKILL.md) | Tailored demos: last slide first, 3 scenes mapped to real pains, tell-show-tell, a per-persona map and the close. |
| [objection-handling](skills/objection-handling/SKILL.md) | The acknowledge → clarify → respond → confirm method plus an objection library (price, timing, competitor, build, budget, brush-offs). |
| [competitive-battlecard](skills/competitive-battlecard/SKILL.md) | Honest one-page battlecards: where you win and lose, landmine questions and answers to competitor claims. |
| [follow-up](skills/follow-up/SKILL.md) | Recaps sent within 2 hours, mutual action plans and a playbook for reviving ghosted deals. |

### Closing
| Skill | What it does |
|---|---|
| [sales-proposal](skills/sales-proposal/SKILL.md) | Proposals and SOWs with an executive summary the CFO actually reads, conservative ROI math and good/better/best pricing. |
| [pricing-negotiation](skills/pricing-negotiation/SKILL.md) | Negotiation plans: anchoring, give-get trades, shrinking concessions, procurement tactics and multi-year/ramp structures. |
| [deal-review](skills/deal-review/SKILL.md) | MEDDPICC scoring on evidence only, the champion test, red flags and an honest forecast category. |
| [call-review](skills/call-review/SKILL.md) | Transcript analysis: talk ratio, questions, monologues, missed buying signals and a coaching scorecard with timestamps. |

## Example

> **You:** Review this deal. $90K, closing end of month. Champion is the Support Ops manager, very excited. We demoed and sent pricing. The VP Support was supposed to join but didn't. They're also talking to ConvoIQ.

> **Agent (deal-review):**
> **MEDDPICC: 8/24.** Metrics 1 · Economic buyer 0 · Decision criteria 1 · Decision process 1 · Paper process 0 · Pain 2 · Champion 1 · Competition 2
>
> **Red flags:** pricing sent before the economic buyer was engaged · single-threaded on a $90K deal · the close date is your month end, not their event.
>
> **Forecast: Pipeline, not Commit.**
>
> **Next best actions:**
> 1. Ask the champion to set up 30 minutes with the VP to review the business case, by Friday.
> 2. Agree on the success metric with the VP.
> 3. Ask for the security questionnaire now to start the paper process.

## Quality

Every skill is linted in CI with [skillcheck](https://github.com/burnoutscript/skillcheck) at 100/100, strict mode: no trigger collisions between skills, no broken links, every description says when to use it.

## Contributing

PRs welcome, especially new skills (renewals and expansion, partner selling, RFP responses) and better examples from real deals. Each skill needs:

- `skills/<name>/SKILL.md` with `name` and `description` frontmatter
- a "Use when the user..." trigger list that doesn't overlap other skills
- an output format and at least one realistic example
- a passing `npx skillcheck skills --strict`

## License

MIT
