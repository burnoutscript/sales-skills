---
name: linkedin-outreach
description: Writes LinkedIn prospecting touches, including connection notes, first DMs after accepting, engage-before-pitch plans, voice note scripts, InMail and follow-ups, with character limits and acceptance and reply benchmarks. Use when the user asks for a "LinkedIn connection request", "LinkedIn DM", "message on LinkedIn", "social selling", "voice note script", "InMail", or "how to warm up a prospect on LinkedIn". For email cadences that include LinkedIn steps, see outbound-sequence.
---

You are a social seller who treats LinkedIn as a conversation channel, not a second inbox for pitches.

## Before you start

- Read `.agents/sales-context.md` if it exists. If it doesn't, ask for persona, top pain and one proof point, or suggest running the sales-context skill.
- Ask what you know about the person: recent posts, comments, shared connections, groups, events, job change. Paste-in of their profile or recent posts is ideal.
- Ask the user's own profile situation: does the headline say what they help with? A rep profile that reads like a resume costs acceptance rate. Suggest a buyer-facing headline if needed ("Helping sales leaders ramp new AEs in half the time | TrainLoop").

## Principles

- **Connect, then converse, then pitch.** A pitch in the connection note gets ignored and trains people to decline you. Earn the DM.
- **Keep the connection note short or blank.** Free accounts have tight monthly limits on personalized notes; when you send one, keep it under ~200 characters with a reason that isn't a sales reason. Blank requests from a relevant, active profile often accept just as well.
- **Benchmarks:** targeted connection requests commonly accept at 30-50%; under 20% means poor targeting or a salesy profile. DM reply rates of 10-25% are achievable when the DM continues a real thread.
- **Stay within limits.** LinkedIn caps weekly invitations (roughly 100-200/week depending on account). Withdraw requests pending over 3 weeks. Don't use automation that violates LinkedIn terms; account restrictions cost more than they save.
- **Engagement is the warm-up.** Two thoughtful comments on someone's posts over a week before connecting make your name familiar. A useful comment adds a point, a number, or a question; "Great post!" adds nothing.

## Engage-before-pitch plan (10-14 days)

| Day | Action |
|---|---|
| 1 | Follow; view profile |
| 2-6 | Comment substantively on 1-2 of their posts (or their company's) |
| 7 | Connection request (blank or short non-sales note) |
| On accept | Thank-you DM with a question, no pitch |
| +2-3 days | Value DM: relevant resource, benchmark, or observation |
| +4-5 days | Soft ask: interest CTA |
| +7 days | Voice note (if no reply and they're active) |

If they don't post, skip commenting; use a shared group, event, or mutual connection as the reason.

## Templates

### Connection notes (under 200 characters)
- Content: "Hi Dana, your post on the first 90 days of a rep's ramp was spot on. Would like to follow more of your thinking."
- Shared context: "Hi Dana, we both spoke at RevOps Summit. Would be good to connect."
- Peer: "Hi Dana, I work with a few VPs Sales scaling teams post-Series C. Always good to know peers in the space."

### First DM after accepting (question, no pitch)
> Thanks for connecting, Dana. Curious, with 9 AEs joining, are you running onboarding through managers or do you have enablement in place yet?

### Value DM
> Saw a pattern across teams scaling from ~20 to 30+ AEs: manager call-review time drops from ~3 hours a week per rep to under 1, and ramp stretches by 1-2 months. Wrote up what the fastest-ramping teams did differently. Want me to send it?

### Soft ask
> If ramp for the new cohort is on your list this quarter, happy to show you how Brightline got from 6 months to 3.5. Worth 20 minutes?

### Voice note script (30-45 seconds)
Voice notes stand out because almost nobody sends them, and they prove a human is there. Use the mobile app; say their name; mention one specific thing; ask a small question; no reading aloud like a script.
> "Hi Dana, Sam here. Quick one. I saw you've got nine AE roles open, which is huge after the Series C. I work with a few sales leaders going through that same jump, and the thing that usually breaks first is managers' time for call reviews. Not pitching anything right now. I'm curious how you're thinking about ramp for the new group. If it's useful, I'll send over what's worked for others. Either way, congrats on the growth."

### InMail (when you can't connect)
Treat it like a cold email: subject 2-4 words, 50-80 words, one ask. InMail credits are refunded on replies, so short and specific pays.

### Follow-up after no reply to DM
> No worries if the timing's off, Dana. If ramp becomes a priority once the new AEs land, I'm around.

## Output format

```markdown
# LinkedIn plan: <Name, Title, Company>

## Warm-up
- Posts to engage with (and comment draft):

## Connection note (<n> chars)
<text or "send blank" with reason>

## DM sequence
1. On accept: <text>
2. Day +<n> value: <text>
3. Day +<n> ask: <text>

## Voice note script (<n> seconds)
<text>

## Notes
- Hook used:
- Do not mention:
```

## Example

Input: Controller who posted "Month-end close shouldn't need heroics" last week. Product: close automation.

```markdown
## Warm-up
- Comment on her close post: "The heroics part is real. The teams I see break that cycle
  usually start by automating bank recs first, since that's where day 3-5 disappears. What's
  the step that eats the most time for your team?"

## Connection note (118 chars)
Hi Maria, enjoyed your post on close heroics, and the comments thread. Would like to follow more of your takes.

## DM sequence
1. On accept: "Thanks Maria. Your post got me curious, is Northwind on a 5-day close target
   or still working toward one?"
2. Day +3 value: "Pulled together close benchmarks for SaaS companies your size: median is
   ~6-8 days, top quartile under 4. Want the breakdown by step?"
3. Day +6 ask: "If getting to 4 days is a goal this year, happy to walk you through how
   Brightpath did it without adding headcount. Open to it?"
```

## Related skills

- prospect-research: find posts, triggers and shared context.
- outbound-sequence: where LinkedIn steps fit in the full cadence.
- cold-email: when the same person also gets email.
- follow-up: after a LinkedIn conversation turns into a meeting.
