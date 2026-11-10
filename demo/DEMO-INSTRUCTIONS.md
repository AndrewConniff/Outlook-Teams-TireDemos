# DEMO-INSTRUCTIONS — Combined Outlook + Teams Session

**Classification: Public**  
**Fictional Company:** MapleWheel Retail Group  
**Audience context:** Canadian Tire stores + head office (new/light Copilot users)  
**No agents**

This demo uses a fictional Microsoft Fake Company created for demonstration purposes. Any resemblance to real organizations, people, products, services, or data is coincidental. Do not use customer confidential information in this package.

## Demo title

Microsoft 365 Copilot in Outlook and Teams for winter-readiness operations (40 min + 40 min).

## Demo tool

- Copilot in Outlook (email thread summarization, drafting, coaching, scheduling, triage).
- Copilot in Teams (channel catch-up, meeting recap, follow-up analysis, post drafting).

## Files to attach / use

### Outlook

1. `demo/sample-data/outlook/thread-eml/*.eml`
2. `demo/sample-data/outlook/other-inbox-eml/*.eml`
3. `demo/sample-data/outlook/Weekly-Auto-Service-Booking-Summary.docx`
4. `demo/sample-data/outlook/Mailbox-Load-Steps.md`

### Teams

1. `demo/sample-data/teams/Winter-Readiness-Meeting-Script.md`
2. `demo/sample-data/teams/Winter-Readiness-Transcript.vtt`
3. `demo/sample-data/teams/Winter-Readiness-Transcript-Fallback.docx`
4. `demo/sample-data/teams/District-Channel-Posts-Script.md`
5. `demo/sample-data/teams/Expected-Recap-Reference.docx`

## Outlook demos (40 minutes)

### Execution context map (what to open before each prompt)

| Prompt | Run in | Open this first | Chat-grounding alternative |
|---|---|---|---|
| O1 | Outlook | Shipment thread folder loaded from `thread-eml` | Attach/paste thread in Copilot Chat |
| O2 | Outlook | Reply draft context + `Weekly-Auto-Service-Booking-Summary.docx` attached | Attach summary doc in Chat |
| O3 | Outlook | O2 draft email text | Paste O2 text in Chat |
| O4 | Outlook | Shipment thread conversation | Paste thread summary in Chat |
| O5 | Outlook | Full inbox with thread + other messages | Paste inbox list/thread in Chat |
| T1 | Teams | Seeded district channel posts | Paste channel export/posts in Chat |
| T2 | Teams | Meeting transcript (live or fallback file) | Attach transcript in Chat |
| T3 | Teams | Same transcript source as T2 | Ask follow-up in Chat from same source |
| T4 | Teams | Recap output from T2/T3 | Paste recap text in Chat |
| T5 | Teams live | Active meeting with transcription | Use fallback transcript in Chat |

### O1 — Summarize long thread

**Exact prompt text**

```text
Summarize this shipment-delay thread for me:
1) What decisions were made?
2) What is still open?
3) Who owns each open item and by when?
Return a concise status update I can send to head office in under 180 words.
```

Expected result: concise decision/open-issue summary with ownership and dates.  
Pass criteria: decisions, open items, and owners match thread evidence.

### O2 — Draft customer-facing reply from short prompt + attachment

**Exact prompt text**

```text
Draft a reply to affected customers confirming revised appointment times.
Reference the attached Weekly-Auto-Service-Booking-Summary.docx and include:
- confirmation of the new date/time,
- a brief apology,
- what to do if the new time does not work.
Keep it clear, professional, and in plain en-CA language.
```

Expected result: practical customer reply with clear next steps.  
Pass criteria: references revised time, apology, and fallback contact action.

### O3 — Coaching and empathy rewrite

**Exact prompt text**

```text
Use Copilot coaching to review this reply for tone and clarity.
Then rewrite it to sound more empathetic while staying concise and professional.
Keep all operational commitments unchanged.
```

Expected result: improved tone without changing commitments.  
Pass criteria: empathy stronger, commitments and timing preserved.

### O4 — Schedule follow-up meeting + agenda

**Exact prompt text**

```text
From this email thread, create a follow-up meeting invite for key owners this week.
Include:
- a 30-minute meeting title,
- required attendees,
- 4 agenda bullets focused on decisions, open risks, and next actions.
```

Expected result: send-ready meeting draft with useful agenda.  
Pass criteria: attendees and agenda align with thread ownership and open risks.

### O5 — Action triage for today

**Exact prompt text**

```text
Based on today’s inbox and the shipment thread, tell me which messages need action today.
Group as:
1) urgent today,
2) today if time allows,
3) FYI only.
For each action item, include one suggested next step.
```

Expected result: clear action priority list.  
Pass criteria: triage reflects message urgency and includes concrete next steps.

**Learner chat question:** Which Copilot output would you send as-is, and which would you always revise first?  
**Outlook day-one habits:**  
1. Ask for decisions/open items/owners/due dates in one output.  
2. Run tone coaching before customer-facing sends.

## Teams demos (40 minutes)

### T1 — Catch up on channel

**Exact prompt text**

```text
Catch me up on this district channel for the past week.
Summarize major updates and highlight anything that needs my reply today.
Return:
- 5-7 bullet summary
- a “Needs my reply” list with who to respond to and why
```

Expected result: concise digest and reply-needed list.  
Pass criteria: identifies key updates and reply-required posts.

### T2 — Meeting recap with action table

**Exact prompt text**

```text
Recap this winter-readiness meeting.
Give me:
1) key decisions,
2) action items in a table with Owner | Action | Due date | Status,
3) one-sentence executive takeaway.
```

Expected result: decision list + owner/date action table.  
Pass criteria: action table fields accurately populated from meeting details.

### T3 — Follow-up on disagreement and unresolved topics

**Exact prompt text**

```text
From the meeting, where did people disagree and what is still unresolved?
List:
- disagreement points,
- options proposed,
- unresolved question(s),
- what input is needed to close them.
```

Expected result: clear conflict and unresolved-items summary.  
Pass criteria: disagreement context and unresolved question are explicit and actionable.

### T4 — Draft channel post then rewrite shorter/friendlier

**Exact prompt text**

```text
Draft a district channel post from the meeting recap for store teams.
Then rewrite it to be shorter and friendlier while keeping all critical actions and dates.
```

Expected result: long + short versions of update post.  
Pass criteria: short version keeps critical owners/dates accurately.

### T5 (Optional live) — Join late, ask what I missed

**Exact prompt text**

```text
I joined this meeting a few minutes late.
What did I miss so far?
Give me:
- key points already covered,
- decisions made,
- any action assigned to me.
```

Expected result: immediate catch-up summary.  
Pass criteria: includes decisions and assigned actions relevant to attendee.

**Learner poll/chat question:** What Teams Copilot task saves you most time: catch-up, recap, or rewrite?  
**Teams day-one habits:**  
1. Always ask for owner/date action tables.  
2. Ask for shorter audience-friendly rewrites before posting.

## Build/configure

1. Load Outlook `.eml` files using `Mailbox-Load-Steps.md`.
2. Record the scripted Teams meeting with transcription on (fallback to provided transcript files as needed).
3. Seed district channel posts from script before running channel catch-up prompt.

## Validation

- Outlook prompts produce traceable decisions, ownership, and customer-ready language.
- Teams prompts produce clear recap tables, disagreement analysis, and audience-appropriate rewrites.

## Cleanup

- Remove imported demo emails/folders from mailbox if re-running with new cohorts.
