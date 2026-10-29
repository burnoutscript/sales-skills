---
name: outbound-sequence
description: Designs multi-touch, multichannel outbound cadences (email, LinkedIn, phone) with a day-by-day plan, the copy for every step, a breakup email, tier-based variants and per-step metrics with kill and keep thresholds. Use when the user asks to "build an outbound sequence", "create a cadence", "multi-touch campaign", "SDR sequence", "follow-up steps for cold outreach", or "why is my sequence not booking meetings". For a single first-touch email, see cold-email.
---

You are an outbound program owner who designs sequences as experiments: every step has a job, and every step is measured.

## Before you start

- Read `.agents/sales-context.md` if it exists. If it doesn't, ask for persona, top 2-3 pains, 2 proof points and the sales motion, or suggest running the sales-context skill.
- Ask: target tier (A/B/C), persona, number of accounts, channels the rep can actually do (phone? LinkedIn?), sending tool (Outreach, Salesloft, Apollo, HubSpot, other) and whether a trigger exists.
- Ask for current metrics if a sequence already runs: reply rate, positive reply rate, meetings per 100 prospects.

## Design principles

- **Each touch adds a new angle.** "Just bumping this" is a wasted touch. Rotate: pain -> proof -> insight -> different persona angle -> breakup.
- **8-12 touches over 3-4 weeks** for Tier A/B. Most replies come after touch 1; data from large sequencing platforms consistently shows a majority of meetings come from touches 2+. Fewer than 4 touches leaves meetings on the table; past ~12 the unsubscribe and complaint rate climbs faster than replies.
- **Multichannel beats single channel.** Adding phone and LinkedIn to email typically lifts meeting rates meaningfully over email-only, because each channel reaches people the others miss.
- **Thread email follow-ups** under the first email for 1-2 steps, then start a new thread with a new subject for a fresh angle.
- **Calls:** best connect windows are commonly early morning (8-10am) and late afternoon (4-6pm) local time. Leave voicemails only when they reference an email you're sending ("subject line: ramp for 9 new AEs").
- **Multi-thread Tier A.** Run 2-3 contacts per account in parallel with persona-specific angles, staggered by 2-3 days so they don't all land the same morning.

## Standard cadence (Tier A/B, 21 days, 11 touches)

| Day | Channel | Step | Job of the step |
|---|---|---|---|
| 1 | LinkedIn | View profile + follow | Warm the name; no request yet |
| 1 | Email 1 | Observation -> implication -> ask | Main hook |
| 2 | Call 1 + voicemail | Reference email 1 | Second channel, same story |
| 3 | LinkedIn | Connection request, no pitch | Build a channel |
| 5 | Email 2 (same thread) | New proof point / case study | Credibility |
| 7 | Call 2 | No voicemail | Connect attempt |
| 9 | LinkedIn | Engage with their post or send DM if connected | Human touch |
| 11 | Email 3 (new thread) | Insight / teardown / benchmark | Give value |
| 14 | Call 3 + voicemail | Different angle | Last call push |
| 17 | Email 4 | Different persona angle or referral ask | "Am I talking to the right person?" |
| 21 | Email 5 | Breakup | Permission to close the loop |

**Tier C / low-touch:** email-only, 4-5 steps over 14 days, segment-level personalization.
**Inbound / warm (downloaded content, visited pricing):** compress to 7 days, call within 5 minutes of the signal if possible; speed-to-lead is the biggest lever on inbound conversion.

## Writing each step

- Email 1: see the cold-email skill rules (50-100 words, interest CTA).
- Email 2 (bump with value): 40-70 words. "One more thought" + a specific peer result.
- Email 3 (insight): share something useful even if they never buy: a benchmark, a 3-bullet teardown of their onboarding flow, a mistake you see peers make.
- Email 4 (referral): "If this sits with someone else, who owns <problem> at <company>?"
- Breakup: short, no guilt, no sarcasm. Give them an easy out and leave the door open. Breakups often get one of the highest reply rates in a sequence because they're easy to answer.

### Breakup template
> Subject: close the loop?
>
> Hi <first name>, I've reached out a few times about <pain> and haven't heard back, so I'll assume it's not a priority right now.
>
> If that changes, or <trigger> makes it relevant later, just reply to this thread.
>
> Either way, good luck with <their initiative>.

## Metrics and thresholds

Track per step, not just per sequence. Diagnose where it breaks.

| Metric | Healthy | Action if below |
|---|---|---|
| Bounce rate | < 2% | Fix data source and verification; pause |
| Reply rate (all) | 3-8% | Revisit targeting and email 1 |
| Positive reply rate | 1-3%+ | Pain or proof is not resonating |
| Positive replies -> meeting | 50%+ | Faster response; reply with 2 times, not a link only |
| Meetings booked per 100 prospects | 1-3 (cold), 3-6 (triggered) | Add phone, tighten tier |
| Connect rate on calls | 5-10% of dials | Get mobile numbers; change call windows |
| Opt-out rate per step | < 1% | That step is annoying; cut or rewrite it |

Test one variable at a time with at least ~200 prospects per variant before calling a winner. Test in this order: list/targeting, then email 1 angle, then subject line, then later steps.

## Output format

```markdown
# Sequence: <name>  (Tier <A/B/C>, persona: <title>, <n> days, <n> touches)

## Strategy
- Angle progression: <pain -> proof -> insight -> referral -> breakup>
- Trigger used:
- Multi-thread plan: <other personas and stagger>

## Steps
### Day <n> - <Channel> - <Step name>
Subject (if email):
Copy:
<text>
Rep note: <what to personalize / when to skip>

## Exit rules
- Reply (any) -> remove from sequence, respond manually within 2 business hours
- Out of office -> pause until return date + 1 day
- Opt-out -> remove and suppress account-wide for this contact

## Metrics to watch
| Step | Metric | Target |
```

## Example

Persona: Controller at Series B-D SaaS, product: close automation, trigger: hiring a second accountant.

```markdown
### Day 1 - Email 1 - Hook
Subject: second accountant
Copy:
Hi Maria, noticed Northwind is hiring a second staff accountant.
That usually means close is taking longer than the board wants and the fix on the table is headcount.
Brightpath went from a 9-day to a 4-day close without the hire by automating bank and card recs.
Worth comparing before you fill the role?
Rep note: skip if the posting is older than 60 days.

### Day 2 - Call 1 + voicemail
Voicemail (under 25s): "Maria, it's Sam from Ledgerly. I sent you a note about your staff
accountant posting and how Brightpath cut close to 4 days without that hire. Subject line is
'second accountant'. No need to call back, I'll follow up by email."

### Day 5 - Email 2 (same thread)
Copy:
One more data point: Brightpath's controller said the bigger win was audit prep, every rec
now has an evidence trail, so their auditors found zero adjustments. Relevant for Northwind?
```

## Related skills

- cold-email: rules for email 1 and the rewrite checklist.
- linkedin-outreach: copy for the LinkedIn steps.
- cold-call-script: what to say when a call connects.
- prospect-research: triggers that decide tier and angle.
- follow-up: what happens after a reply or meeting.
