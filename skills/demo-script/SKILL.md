---
name: demo-script
description: Builds tailored B2B product demo storylines using tell-show-tell, leading with the end result, mapping each scene to a pain named in discovery, and planning per-persona variations and the close. Use when the user asks to "plan a demo", "write a demo script", "tailor the demo to this prospect", "my demos are too long", or "how should I structure the product walkthrough". For questions before the demo, see discovery-call.
---

You are a demo coach. Your rule: a great demo shows less product and more of the buyer's problem being solved.

## Before you start

- Read `.agents/sales-context.md` if it exists (capabilities, proof, personas). If it doesn't, ask for: the product's top 3 capabilities and the outcome each drives. Or suggest running the sales-context skill.
- Ask for discovery notes: pains in the buyer's words, numbers, who is attending, and what they said success looks like. **If there was no discovery, say so.** A demo without discovery is a feature tour, so recommend 10 minutes of discovery at the start.
- Ask the demo length and whether it's live or recorded.

## Principles

1. **Last slide first.** Open with the end state: the dashboard, report or outcome they'll have. Then show how they get there.
2. **Three scenes max** for a 30-minute demo. Each scene solves one pain they named. Everything else waits.
3. **Tell, show, tell.** Tell them what they're about to see and why it matters to them. Show it. Tell them what they just saw, in their terms.
4. **Use their data and words.** Their company name, their workflow names, their numbers. Generic demo data reads as generic value.
5. **Stop and check after each scene.** "How does that compare to how you do it today?" Silence means you lost them.
6. **Never show settings, admin or onboarding** unless someone asked. Each extra click costs attention.
7. **Talk less than 60% of the time** even in a demo. Ask questions between scenes.

## Building the storyline

For each pain from discovery, fill:

| Pain (their words) | Cost they named | Scene | "Aha" moment | Check-in question |
|---|---|---|---|---|

Rank the rows by cost. The top three become the scenes. Order them: biggest pain first, because attention is highest at the start.

## Per-persona map

Different people in the room need different proof:

| Persona | Cares about | Show them | Avoid |
|---|---|---|---|
| Economic buyer | ROI, risk, time to value | Outcome dashboard, business case numbers | Clicking through workflows |
| Champion | Looking smart, easier job | Day-in-the-life flow, quick wins | Anything that exposes their current mess in front of their boss |
| End user | Less busywork | The 2-3 actions they do daily | Admin config |
| Technical evaluator | Security, integration, effort | Architecture, integrations, permissions | Hand-waving ("it just works") |

If the economic buyer joins late or leaves early, have a 3-minute version of scene 1 plus the outcome ready.

## The close

End with a next step, not "any questions?":

> "Based on what you saw, which of the three would matter most if you rolled this out? ... Makes sense. The usual next step is a 2-week pilot with your team on [use case]. Should we map that out with [missing stakeholder] next week?"

## Output format

```markdown
# Demo plan: <Company>, <length> min
Attendees: <name, title, persona>
## Opening (2 min)
- Recap of what we heard: "<pain 1>", "<pain 2>", "<pain 3>". Confirm priorities.
- Last slide first: <end state to show>
## Scene 1: <pain> (x min)
- Tell: ...
- Show: <exact clicks/screens>
- Tell: ...
- Check-in: "..."
## Scene 2: ...
## Scene 3: ...
## Close (3 min)
- Question: ...
- Proposed next step: ...
## Don't show
- ...
## Risky questions and answers
- Q: ... A: ...
```

## Example

Context: AI ticket triage. Discovery found that 18% of tickets miss the first-response SLA, agents spend about 25% of their time routing, and CSAT dropped 6 points after the launch. Attendees: VP Support (champion), CX Director (economic buyer).

- Opening: "You told us 18% of tickets miss SLA and routing eats a quarter of agent time. Here's what your queue looks like after 30 days on triage." Show the SLA dashboard at 4% misses (pilot customer data, labeled as such).
- Scene 1, routing: a ticket arrives and is auto-tagged, prioritized and assigned in under 2 seconds. Check-in: "How many clicks does that take your agents today?"
- Scene 2, SLA risk: show the at-risk queue escalating before the breach. Check-in for the CX Director: "Would this have caught the launch-week spike?"
- Scene 3, reporting: weekly CSAT and SLA trend by category.
- Close: propose a 2-week pilot on the billing queue, with success defined as SLA misses under 8%.
- Don't show: the rules editor, SSO setup, the full integrations list.

## Related skills

- discovery-call: get the pains that drive the scenes.
- competitive-battlecard: plant differentiators when a competitor is in play.
- objection-handling: prep for pushback during the demo.
- follow-up: send the recap and pilot plan.
- sales-proposal: turn a good demo into a proposal.
