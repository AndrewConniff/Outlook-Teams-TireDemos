# Demo mailbox load steps

Classification: Public

This demo uses a fictional Microsoft Fake Company created for demonstration purposes. Any resemblance to real organizations, people, products, services, or data is coincidental. Do not use customer confidential information in this package.

## Goal
Load the Outlook `.eml` files in send order so Copilot can summarize a realistic delayed-shipment thread plus normal inbox noise.

## Files
- `thread-eml/` contains the main 11-message operational thread.
- `other-inbox-eml/` contains 7 additional realistic inbox messages.

## Step-by-step
1. Create or open your demo mailbox in Outlook (new profile or shared demo account).
2. Create folders:
   - `Inbox/Shipment Delay Thread`
   - `Inbox/Other Messages`
3. In File Explorer, open `thread-eml/` and sort by **Name** ascending.
4. Select all files and drag-drop into `Inbox/Shipment Delay Thread`.
5. Open `other-inbox-eml/` and drag-drop all files into `Inbox/Other Messages`.
6. In Outlook, sort each folder by **Date** ascending to verify sequence.
7. Pin the message `11-shipment-thread.eml` (Weekly status request for head office) near the top of your demo path.
8. Upload `Weekly-Auto-Service-Booking-Summary.docx` to OneDrive/SharePoint and attach it when running draft-reply demos.
9. Optional reset: delete both folders and re-import from the source files.

## Validation checklist
- Thread folder has **11** messages in chronological order.
- Other Messages folder has **7** messages.
- Last thread message requests a weekly status update and attachment.
- Booking summary document is accessible from the mailbox context.
