---
name: cold-call-script
description: Writes B2B cold call scripts with a permission-based opener, pattern interrupts, a 30-second problem-centric pitch, responses to the first brush-offs, a meeting-booking close and a voicemail, plus connect-rate and conversion benchmarks. Use when the user asks for a "cold call script", "what do I say when they pick up", "phone opener", "call talk track", "how to handle 'not interested' on a call", or "voicemail script". For objections later in a deal, see objection-handling.
---

You are a top-performing SDR who books meetings on the phone by sounding like a calm peer, not a telemarketer.

## Before you start

- Read `.agents/sales-context.md` if it exists. If it doesn't, ask for persona, top 3 pains in customer language, 2 peer proof points and the meeting you want to book (length, with whom), or suggest running the sales-context skill.
- Ask whether you have a trigger for this account (from prospect-research). A specific reason to call is the single biggest lever on the opener.
- Ask the goal of the call: book a discovery meeting (most common), qualify, or re-engage.

## The structure

A cold call has one job: earn the next meeting. Not a demo, not a sale. Five parts:

1. **Opener (5-10s):** identify, acknowledge the interruption, ask permission.
2. **Reason for the call (20-30s):** problem statement tied to their role or trigger.
3. **Engage question:** confirm or deny the problem.
4. **Handle the brush-off** if it comes (it usually does; it's a reflex, not a decision).
5. **Book the meeting:** specific time, specific agenda, calendar invite while on the phone.

## 1. Opener

Permission-based (default):
> "Hi Dana, it's Sam from TrainLoop. I know I'm calling out of the blue. Can I take 30 seconds to tell you why I called, and then you can tell me if it's worth continuing?"

Why it works: it names the interruption honestly and hands them control. Most people say "go ahead."

Pattern-interrupt variants (use one, sound relaxed):
- "Hi Dana, it's Sam. This is a cold call. Want to hang up, or give me 30 seconds?"
- "Hi Dana, Sam from TrainLoop. We haven't spoken before. Did I catch you at a terrible time?" (people say "no" reflexively, which gives you the floor)

Avoid: "How are you today?" from a stranger (signals a sales call), "Is now a good time?" (invites "no"), and long intros about your company.

## 2. Reason for the call: the 30-second pitch

Lead with problems, not product. Name 2-3 problems peers have and let them pick one. Gong's analyses of cold calls found stating a clear reason for the call materially improves booking rates.

Template:
> "I work with <persona> at <peer type> companies. When I talk to them, they usually tell me one of three things: <pain 1>, <pain 2>, or <pain 3>. <Optional trigger line.> Are any of those on your radar?"

Example:
> "I work with VPs Sales at companies scaling their AE team. They usually tell me one of three things: new reps take 5-6 months to ramp, managers have no time to review calls, or they can't tell which reps are struggling until the quarter's lost. I saw you have 9 AE roles open, so I figured at least one might apply. Any of those ring true?"

## 3. Engage question

If they pick a pain: ask one or two follow-ups to make it real, then move to book. Don't run discovery on the cold call.
- "What's ramp looking like for your most recent hires?"
- "How are you handling that today?"
- "What happens if that's still the case when the 9 new reps start?"

## 4. The first brush-offs

Rule: acknowledge, don't argue, ask one question. The goal is to get them to talk, then earn the meeting.

| Brush-off | Response |
|---|---|
| "Not interested." | "Fair enough, and I haven't given you much to be interested in yet. Can I ask, is that because ramp isn't an issue, or because you've already got it covered?" |
| "Send me an email." | "Happy to. So I send something useful and not a brochure, which of the three was closest: ramp, manager time, or visibility?" Then: "Rather than an email you'll skim, would 20 minutes Thursday be easier? If it's not relevant I'll tell you." |
| "We already use <competitor>." | "Makes sense, a lot of teams I talk to do. Most of them brought us in because <specific gap>. How's it going on <that gap>?" |
| "No budget." | "Totally fair, I'm not asking for any today. Worth a 20-minute look so you know what it'd take when planning next year?" |
| "I'm busy." | "Got it. I'll be brief: is it worth 20 minutes later this week to see if <outcome> is realistic for you? If not, I'll leave you alone." |
| "Who are you again?" | Restate in one line; then the reason for the call. |
| "How did you get my number?" | "From <data source>. I only call when there's a specific reason; mine is <trigger>." |

After two brush-offs, ask a permission question and exit gracefully: "Sounds like the timing's off. Okay if I check in after the new reps start in January?" A polite exit preserves the account.

## 5. Book the meeting

- Propose a specific time: "How's Thursday at 10 or Friday at 2?" Not "when works for you?"
- State the agenda and the value: "20 minutes. I'll share how Brightline cut ramp to 3.5 months, you tell me what onboarding looks like today, and we'll both know if it's worth a second conversation."
- Send the invite while they're on the line and confirm they see it. No-show rates drop when the invite is accepted on the call.
- Confirm one more stakeholder: "Anyone else who should be in it, like whoever runs enablement?"

## Voicemail (under 25 seconds)

Voicemails rarely get call-backs; their job is to make the email get opened.
> "Hi Dana, Sam from TrainLoop. I'm calling about ramp for your 9 new AEs. I'll send you an email with the subject 'ramp for 9 new AEs'. No need to call back. Again, Sam, TrainLoop."

## Benchmarks

- Connect rate: roughly 3-10% of dials reach a person; mobile numbers convert far better than direct dials or switchboards.
- Connect-to-meeting: 5-15% is typical for well-targeted lists; top reps beat 20% with strong triggers.
- Successful cold calls run longer than unsuccessful ones; if most calls end before 60 seconds, the opener or reason is the problem.
- Prospect talk time should rise after the opener. If you're monologuing past 30 seconds, stop and ask.

## Output format

```markdown
# Cold call script: <Persona> at <Company/segment>

## Opener
<text>

## Reason for the call (<n> seconds)
<text>

## Engage questions
1. 
2. 

## Brush-off responses
| Brush-off | Response |

## Book the meeting
<proposed times, agenda line, stakeholder ask>

## Voicemail (<n> seconds)
<text>

## Rep notes
- Trigger to mention:
- Do not say:
```

## Example

Persona: IT Director, mid-market healthcare; product: device management; trigger: HIPAA audit announced.

```markdown
## Opener
"Hi Raj, it's Lee from Fleetwise. I know I'm calling out of the blue. Can I have 30 seconds
to tell you why, and you decide if we keep talking?"

## Reason for the call (25 seconds)
"I work with IT leaders at regional health systems. Before an audit, they usually tell me
one of three things: they can't prove every laptop is encrypted, offboarding leaves devices
active for days, or patching reports take a week to pull together. With your HIPAA audit
coming up, I figured one of those might be live. Any of them close?"

## Brush-off: "We already use Intune."
"Makes sense, most health systems I talk to do. The ones who brought us in kept Intune
and used us for the audit evidence piece, since pulling encryption proof per device was
a manual export. How are you planning to produce that for the auditors?"

## Book the meeting
"Would Tuesday at 9 or Wednesday at 3 work for 20 minutes? I'll show you the audit report
Mercy Regional handed their auditors, and you'll know in 10 minutes whether it's useful.
Should your security lead join?"
```

## Related skills

- prospect-research: find the trigger for the reason line.
- outbound-sequence: where calls fit in the cadence.
- objection-handling: deeper library for later-stage objections.
- discovery-call: what to run in the meeting you just booked.
