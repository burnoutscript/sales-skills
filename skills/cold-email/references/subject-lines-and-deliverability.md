# Subject line patterns and deliverability checklist

## Subject line patterns

Rules: 2-4 words, lowercase, no product name, no punctuation tricks, no emojis. It should look like a colleague wrote it.

| Pattern | Template | Example |
|---|---|---|
| Trigger | `<trigger noun>` | `series c hiring` |
| Pain | `<pain in their words>` | `month-end close` |
| Company + topic | `<company> + <topic>` | `acme + audit prep` |
| Peer reference | `<peer company> <outcome>` | `brightline ramp time` |
| Question | `question on <topic>` | `question on routing` |
| Number | `<number> <noun>` | `9 new AEs` |
| Their initiative | `<initiative name>` | `dallas expansion` |
| Mutual connection | `<name> suggested i reach out` | `priya suggested i reach out` (only if true) |

Subject lines to avoid:
- Anything with the product name or "introducing"
- "Quick question" (overused, now pattern-matched as cold)
- Fake replies or forwards: "Re:", "Fwd:"
- "Partnership opportunity", "Synergies", "Following up" on email 1
- ALL CAPS, exclamation marks, "free", "guarantee", "% off"

Follow-up steps in the same thread: reply in-thread with no new subject. Threading lifts reply rates because the context stays visible.

## Deliverability checklist

Bad deliverability makes good copy irrelevant. Check these before blaming the message.

### Domain and authentication
- [ ] Send cold email from a secondary domain (e.g. `getacme.com`), never the primary corporate domain. Redirect it to the main site.
- [ ] SPF, DKIM and DMARC configured on every sending domain. Google and Yahoo have required this for bulk senders since February 2024.
- [ ] DMARC at least `p=none` with reporting; move to `quarantine` once aligned.
- [ ] Custom tracking domain if open/click tracking is used (or turn tracking off; open tracking pixels hurt placement).
- [ ] New domains aged and warmed 2-4 weeks before cold volume.

### Volume
- [ ] 30-50 cold emails per inbox per day maximum; spread across multiple inboxes rather than pushing one.
- [ ] Ramp new inboxes gradually (start around 10-20/day).
- [ ] Spread sends across business hours, not one burst.

### List hygiene
- [ ] Verify every address before sending; keep hard bounces under 2%.
- [ ] Remove role addresses (info@, sales@) and catch-alls you can't verify.
- [ ] Keep spam complaint rate under 0.1%; Google's hard ceiling is 0.3%.
- [ ] Honor opt-outs immediately and permanently. Include a plain opt-out line ("Not relevant? Just say so and I won't follow up.").

### Content
- [ ] Plain text, no images, no attachments in first touch.
- [ ] Zero or one link, and none in email 1.
- [ ] No spam-trigger phrasing: "act now", "risk-free", "100%", "click here", "guaranteed".
- [ ] Spintax or real personalization so 500 sends aren't byte-identical.
- [ ] Signature: name, title, company. No banners, no social icons.

### Compliance
- [ ] CAN-SPAM (US): truthful headers, physical address, working opt-out.
- [ ] GDPR (EU/UK): legitimate-interest basis documented, relevant to their role, easy opt-out. Some countries (e.g. Germany) are stricter on B2B cold email; check before sending.
- [ ] CASL (Canada): stricter consent rules; often treat Canada as opt-in only.

### Monitoring
- [ ] Watch Google Postmaster Tools for domain reputation and spam rate.
- [ ] Seed-test placement before launching a new campaign.
- [ ] If reply rate drops by half overnight with no copy change, suspect deliverability first: pause, check bounces and blacklists.
