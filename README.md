# Outlook + Teams Copilot Demo Session (Canadian Tire audience)

**Classification: Public**

This repository contains a combined live demo session for **Microsoft 365 Copilot in Outlook (40 min)** and **Microsoft 365 Copilot in Teams (40 min)**, designed for new/light Copilot users from stores and head office.

**Fictional Microsoft Fake Company used in all sample data:** MapleWheel Retail Group  
**Audience context:** Canadian Tire (training audience only)  
**Locale conventions:** en-CA, CAD, metric

This demo uses a fictional Microsoft Fake Company created for demonstration purposes. Any resemblance to real organizations, people, products, services, or data is coincidental. Do not use customer confidential information in this package.

## Session timing

1. **Outlook demo** — 40 minutes  
2. **Teams demo** — 40 minutes  
3. **Optional Q&A / transition** — 5 to 10 minutes

## Scenario

### Outlook scenario

A Store General Manager and Auto Service Manager are handling winter tire changeover rush conditions: delayed supplier shipment, overbooked service appointments, and a head-office weekly status request.

### Teams scenario

District weekly winter-readiness call across head office merchandising, three Store General Managers, and an Auto Service lead, plus a district Teams channel with daily posts and replies.

## Setup steps

1. Download all files in `demo/sample-data/`.
2. For Outlook:
   - Import numbered `.eml` files from `outlook/thread-eml/` in order.
   - Import additional inbox messages from `outlook/other-inbox-eml/`.
   - Use `outlook/Mailbox-Load-Steps.md` for exact load sequence.
   - Keep `outlook/Weekly-Auto-Service-Booking-Summary.docx` available for attachment demos.
3. For Teams:
   - Use `teams/Winter-Readiness-Meeting-Script.md` to record a meeting in demo tenant with transcription on.
   - If recording/transcript is unavailable, use fallback files:
     - `teams/Winter-Readiness-Transcript.vtt`
     - `teams/Winter-Readiness-Transcript-Fallback.docx`
   - Seed channel content from `teams/District-Channel-Posts-Script.md`.
4. Open `index.html` (or GitHub Pages URL) for prompt boxes with quick copy buttons.

## Prompt run order (exact text)

### Where to run each prompt (file + app)

| Prompt | Run in | Open this first | Alternative (Copilot Chat grounding) |
|---|---|---|---|
| O1 | Outlook | Folder with imported shipment thread (`thread-eml`) | In Chat, attach or paste the thread messages |
| O2 | Outlook | Draft/reply context + attach `Weekly-Auto-Service-Booking-Summary.docx` | In Chat, attach booking summary and ask for reply draft |
| O3 | Outlook | The O2 draft email body | In Chat, paste O2 draft and ask for empathy rewrite |
| O4 | Outlook | Shipment thread conversation | In Chat, use thread text and ask for invite agenda draft |
| O5 | Outlook | Inbox with both thread + other messages loaded | In Chat, summarize pasted inbox list and triage |
| T1 | Teams | District channel seeded with `District-Channel-Posts-Script.md` content | In Chat, paste channel posts and ask for catch-up |
| T2 | Teams | Recorded meeting transcript OR fallback transcript file | In Chat, attach transcript `.docx`/`.vtt` |
| T3 | Teams | Same meeting transcript/source as T2 | In Chat, ask follow-up from same transcript |
| T4 | Teams | Recap output from T2/T3 | In Chat, paste recap and ask for post rewrite |
| T5 | Teams | Live meeting with transcription on | If no live meeting, use fallback transcript in Chat |

### Outlook (40 min)

**O1 — Summarize long thread**

```text
Summarize this shipment-delay thread for me:
1) What decisions were made?
2) What is still open?
3) Who owns each open item and by when?
Return a concise status update I can send to head office in under 180 words.
```

Expected result: concise decision/open-issue summary with owners and timing.  
Pass criteria: identifies decisions, open items, and ownership correctly from thread content.

**O2 — Draft reply confirming revised appointment times**

```text
Draft a reply to affected customers confirming revised appointment times.
Reference the attached Weekly-Auto-Service-Booking-Summary.docx and include:
- confirmation of the new date/time,
- a brief apology,
- what to do if the new time does not work.
Keep it clear, professional, and in plain en-CA language.
```

Expected result: clear customer reply draft grounded in attachment context.  
Pass criteria: includes revised-time confirmation, apology, and clear next step.

**O3 — Use Copilot coaching and rewrite complaint reply empathetically**

```text
Use Copilot coaching to review this reply for tone and clarity.
Then rewrite it to sound more empathetic while staying concise and professional.
Keep all operational commitments unchanged.
```

Expected result: more empathetic version without losing commitments.  
Pass criteria: improved tone, same factual commitments, clear customer language.

**O4 — Schedule follow-up meeting + agenda**

```text
From this email thread, create a follow-up meeting invite for key owners this week.
Include:
- a 30-minute meeting title,
- required attendees,
- 4 agenda bullets focused on decisions, open risks, and next actions.
```

Expected result: complete meeting invite draft + practical agenda.  
Pass criteria: attendees and agenda align to thread decisions/open issues.

**O5 — Identify what needs action today**

```text
Based on today’s inbox and the shipment thread, tell me which messages need action today.
Group as:
1) urgent today,
2) today if time allows,
3) FYI only.
For each action item, include one suggested next step.
```

Expected result: prioritized action triage across thread + other inbox messages.  
Pass criteria: actionable prioritization with practical next steps.

Learner chat question: **Which Copilot output would you send as-is, and which would you always revise first? Why?**  
Day-one habits:
1. Ask for outputs in a **fixed structure** (decisions, open items, owners, due dates).  
2. Run **tone coaching** before sending customer-facing responses.

### Teams (40 min)

**T1 — Catch up on channel**

```text
Catch me up on this district channel for the past week.
Summarize major updates and highlight anything that needs my reply today.
Return:
- 5-7 bullet summary
- a “Needs my reply” list with who to respond to and why
```

Expected result: concise weekly digest + reply-needed list.  
Pass criteria: captures key updates and clearly flags reply-required posts.

**T2 — Recap meeting decisions and action items table**

```text
Recap this winter-readiness meeting.
Give me:
1) key decisions,
2) action items in a table with Owner | Action | Due date | Status,
3) one-sentence executive takeaway.
```

Expected result: decision recap + tabular action tracker.  
Pass criteria: owners/actions/dates correctly captured from meeting content.

**T3 — Follow-up questions on disagreement and unresolved points**

```text
From the meeting, where did people disagree and what is still unresolved?
List:
- disagreement points,
- options proposed,
- unresolved question(s),
- what input is needed to close them.
```

Expected result: conflict + unresolved analysis with closure inputs.  
Pass criteria: clearly separates resolved vs unresolved items.

**T4 — Draft then rewrite channel post**

```text
Draft a district channel post from the meeting recap for store teams.
Then rewrite it to be shorter and friendlier while keeping all critical actions and dates.
```

Expected result: two versions (full + shorter friendlier).  
Pass criteria: short version stays accurate and keeps critical owners/dates.

**T5 (Optional live) — Join late and ask what I missed**

```text
I joined this meeting a few minutes late.
What did I miss so far?
Give me:
- key points already covered,
- decisions made,
- any action assigned to me.
```

Expected result: targeted late-join summary.  
Pass criteria: practical catch-up without replaying entire meeting.

Learner reaction poll/chat question: **What Teams Copilot task saves you the most time: catch-up, meeting recap, or rewrite for audience?**  
Day-one habits:
1. Ask for **owner + date tables** in every recap.  
2. Ask for a **shorter audience rewrite** before posting to broad channels.

## Repository contents

| Path | Purpose |
|---|---|
| `index.html` | One-page demo guide with Outlook and Teams prompt boxes + copy buttons |
| `demo/DEMO-INSTRUCTIONS.md` | Combined presenter runbook (markdown) |
| `demo/DEMO-INSTRUCTIONS.docx` | Combined presenter runbook (Word) |
| `demo/sample-data/outlook/` | Outlook `.eml` thread, additional inbox messages, load steps, booking summary attachment |
| `demo/sample-data/teams/` | Teams meeting script, fallback transcripts, channel post seed script, expected recap reference |
| `AI-CONTENT-DECLARATION.md` | AI transparency statement |
| `manifest.json` | Package metadata |
| `LICENSE` | MIT license |

## Published links

- Repository: https://github.com/AndrewConniff/Outlook-Teams-TireDemos
- GitHub Pages: https://andrewconniff.github.io/Outlook-Teams-TireDemos/

## AI transparency

This repository contains AI-generated and human-reviewed demo content. See `AI-CONTENT-DECLARATION.md`.
