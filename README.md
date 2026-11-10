# Outlook + Teams Copilot Follow-Along Demo Session

**Classification: Public**

This repository now provides a **follow-along** session for:
1. **Microsoft 365 Copilot in Outlook (40 min)**
2. **Microsoft 365 Copilot in Teams (40 min)**

Audience: new/light Copilot users from store operations and corporate office.

This demo uses a fictional Microsoft Fake Company created for demonstration purposes. Any resemblance to real organizations, people, products, services, or data is coincidental. Do not use customer confidential information in this package.

## What changed

- Reworked from preload-heavy mailbox/channel simulation to **GA-friendly follow-along** steps.
- Designed to work in **any commercial Microsoft 365 tenant** where Outlook and Teams Copilot are available.
- Added optional sample files for attachment summarization and Analyst workflow.

## Follow-along storyline

You are preparing winter-readiness communications:
- Outlook: send a cross-functional status email with summarized attachment and schedule a follow-up meeting with agenda.
- Teams: recap a real meeting you attended (with transcript/recording), ask follow-ups, and publish a concise update.

## Session timing

1. Outlook follow-along — 40 min
2. Teams follow-along — 40 min
3. Transition/Q&A — 5 to 10 min

## Setup steps

1. Open `index.html` in this repo (or GitHub Pages URL).
2. Sign in to Outlook and Teams with Copilot available.
3. Confirm you can access at least one:
   - existing Outlook thread for a meeting/status update, and
   - Teams meeting you attended with transcript or recording.
4. Upload these optional sample files to OneDrive/SharePoint:
   - `demo/sample-data/shared/Winter-Tire-Delay-Briefing.docx`
   - `demo/sample-data/shared/Canada-Wide-Winter-Tire-Sales-Weather-2023-2026.xlsx`

## Analyst-to-Email-to-Teams flow (new)

1. Open `Canada-Wide-Winter-Tire-Sales-Weather-2023-2026.xlsx` in Excel.
2. Use Analyst (or Copilot in Excel) to generate a winter trend chart.
3. Copy chart into:
   - an Outlook update email, and
   - a Teams channel post.
4. Use Copilot in each app to rewrite for audience tone.

## Repository contents

| Path | Purpose |
|---|---|
| `index.html` | One-page runbook with tabs and copy-ready prompts |
| `demo/DEMO-INSTRUCTIONS.md` | Detailed follow-along instructor runbook |
| `demo/DEMO-INSTRUCTIONS.docx` | Same runbook in Word format |
| `demo/sample-data/shared/Winter-Tire-Delay-Briefing.docx` | Attachment used for Outlook summary/send flow |
| `demo/sample-data/shared/Canada-Wide-Winter-Tire-Sales-Weather-2023-2026.xlsx` | 3-year historical + winter prediction dataset for Analyst charts |
| `demo/sample-data/shared/Analyst-to-Outlook-Teams-Workflow.md` | Short workflow checklist |
| `AI-CONTENT-DECLARATION.md` | AI transparency |
| `manifest.json` | Package metadata |
| `LICENSE` | MIT license |

## Published links

- Repository: https://github.com/AndrewConniff/Outlook-Teams-TireDemos
- GitHub Pages: https://andrewconniff.github.io/Outlook-Teams-TireDemos/

## AI transparency

This repository contains AI-generated and human-reviewed demo content. See `AI-CONTENT-DECLARATION.md`.
