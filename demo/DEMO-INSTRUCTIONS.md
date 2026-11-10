# DEMO-INSTRUCTIONS — Follow-Along Outlook + Teams Session

**Classification: Public**  
**Audience context:** new/light Copilot users in commercial Microsoft 365 tenants  
**Mode:** follow-along (participants can run steps in their own Outlook/Teams)

This demo uses a fictional Microsoft Fake Company created for demonstration purposes. Any resemblance to real organizations, people, products, services, or data is coincidental. Do not use customer confidential information in this package.

## Demo title

Microsoft 365 Copilot in Outlook and Teams — follow-along winter-readiness communication flow.

## Follow-along prerequisites

1. Outlook and Teams Copilot access.
2. At least one real Outlook thread for operational coordination.
3. At least one Teams meeting you attended with transcript or recording.
4. Optional sample attachments uploaded to OneDrive/SharePoint:
   - `Winter-Tire-Delay-Briefing.docx`
   - `Canada-Wide-Winter-Tire-Sales-Weather-2023-2026.xlsx`

## Execution context map (what to open before each prompt)

| Prompt | Run in | Open this first | Alternative |
|---|---|---|---|
| O1 | Outlook | Existing thread you want to update from | Use sample briefing doc and ask Copilot to draft from that |
| O2 | Outlook | New email draft + attach briefing doc | Use any internal status attachment |
| O3 | Outlook | O2 draft email body | N/A |
| O4 | Outlook | Same thread/email context as O2 | N/A |
| O5 | Outlook | Same O2 email + Analyst chart image from Excel | Use Copilot in Excel chart output pasted manually |
| T1 | Teams | Meeting recap pane for meeting with transcript/recording | Use fallback transcript doc if needed |
| T2 | Teams | Same meeting recap context | N/A |
| T3 | Teams | Same meeting recap + channel/post composer | N/A |
| T4 | Teams | O5 email summary text + chart image available | Paste from Outlook draft if needed |
| T5 | Teams | Live meeting in progress with transcript on | Optional |

## Outlook follow-along demos (40 min)

### O1 — Personalize Copilot output style (GA follow-along)

**Exact prompt text**

```text
Based on this thread, draft updates in my preferred style:
- concise first paragraph
- action items in bullets
- clear owner and due date per action
- friendly but direct tone
```

Expected result: structured draft matching personal communication style.  
Pass criteria: output is concise, actionable, and readable for direct send/edit.

### O2 — Draft and send a cross-functional update with attachment summary

**Exact prompt text**

```text
Draft an update email to store operations, auto service, and district leadership.
Summarize the attached Winter-Tire-Delay-Briefing.docx in 5 bullets, then include:
1) current status
2) risks
3) actions by owner
4) what support is needed
Use clear en-CA language.
```

Expected result: send-ready multi-recipient update grounded in attached doc.  
Pass criteria: attachment summary is accurate; owners/actions are explicit.

### O3 — Copilot coaching for clarity and tone

**Exact prompt text**

```text
Coach this draft for clarity and tone.
Then rewrite it to be slightly warmer while keeping the same commitments and dates.
```

Expected result: improved readability and tone without changing commitments.  
Pass criteria: factual content unchanged; tone clearly improved.

### O4 — Schedule follow-up meeting and generate agenda

**Exact prompt text**

```text
Create a 30-minute follow-up meeting from this thread/update.
Include required attendees and an agenda with:
- decisions needed
- risk review
- next-week milestones
- owner check-in
```

Expected result: meeting invite draft with practical agenda.  
Pass criteria: attendee list and agenda align with email actions.

### O5 — Analyst chart handoff into Outlook

**Exact prompt text**

```text
Using the summary below and the chart image I inserted from Excel,
draft a short executive email with:
- 3 key findings
- 2 actions
- 1 ask
```

Expected result: concise executive email ready to send/share.  
Pass criteria: clearly references chart insights and next actions.

Learner chat question: **Which Outlook Copilot step saved you the most time today?**  
Outlook day-one habits:
1. Ask for owner + due date formatting in every draft.
2. Run Copilot coaching before sending broad updates.

## Teams follow-along demos (40 min)

### T1 — Use a real meeting recap

**Exact prompt text**

```text
From this meeting transcript/recording, give me:
1) key decisions
2) action items with owner and due date
3) unresolved questions
```

Expected result: meeting recap with decisions/actions/open issues.  
Pass criteria: action ownership and dates are explicit.

### T2 — Ask focused follow-up questions

**Exact prompt text**

```text
Where did attendees disagree, what options were proposed, and what input is needed to close the open items?
```

Expected result: clear disagreement analysis with closure path.  
Pass criteria: unresolved items are concrete and decision-ready.

### T3 — Suggested prompts during/after Teams calls

**Exact prompt text**

```text
Create 6 follow-up prompts I can use in Teams after meetings:
2 for recap, 2 for action tracking, 2 for executive communication.
```

Expected result: reusable post-meeting prompt set.  
Pass criteria: prompts are practical and immediately reusable.

### T4 — Share Outlook/Analyst summary to Teams audience

**Exact prompt text**

```text
Draft a Teams channel post from my Outlook update and chart summary.
Then rewrite it in a shorter, friendlier style for store teams.
Keep actions and dates intact.
```

Expected result: channel-ready long + short versions.  
Pass criteria: short version remains accurate and action-complete.

### T5 (Optional) — What did I miss in a live call?

**Exact prompt text**

```text
I joined late. What did I miss so far, and do I have any assigned action?
```

Expected result: fast late-join catch-up.  
Pass criteria: assigned tasks are clearly identified.

Learner poll/chat question: **Which Teams Copilot scenario feels most useful in your daily work: recap, follow-up prompts, or channel rewrite?**  
Teams day-one habits:
1. Always request owner/date action tables.
2. Ask for audience rewrite before posting broadly.

## Analyst-to-Outlook-to-Teams workflow (new)

1. Open `Canada-Wide-Winter-Tire-Sales-Weather-2023-2026.xlsx` in Excel.
2. Use Analyst/Copilot to create weather vs sales trend chart.
3. Paste chart into Outlook update (O5).
4. Post same insight to Teams (T4) with audience rewrite.

## Cleanup

- Remove any temporary drafts/test posts if running with live users.
