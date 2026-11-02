---
name: monday-briefing
description: Prepare a Monday overview of inbox items needing attention, the week ahead on the calendar, and upcoming actions.
---

# Monday Morning Briefing

## Goal

Help Caleb start the week with a concise view of important inbox items, calendar commitments, and actions that should happen soon.

## First-pass scope

- Review the connected Gmail inbox from the previous seven days through the briefing date. Expand the range when an older thread contains an active deadline or unresolved commitment.
- Use the private status index at `/Users/caleb.bray/notes/my thoughts/hub/email-index.json` to suppress addressed/skipped messages and carry open items forward. Keep resolved/skipped records for seven days; retain open actions until resolved. Store IDs and status only, never email content, in that file.
- Review the primary Google Calendar for Monday through Sunday in the user's timezone.
- Treat email and calendar as sources of evidence. Do not assume a separate task manager has been reviewed unless one is connected and explicitly included.
- Do not claim continuous monitoring. Run this workflow when requested or through a separately configured schedule.

## Workflow

1. State the date, timezone, inbox period, and calendar week covered.
2. Review email for decisions, replies, deadlines, promised follow-ups, approvals, and meaningful risks. Apply the email skill's known priority criteria and deduplicate threads and repeated alerts.
   - Use unread/new mail as a review signal, not as a measure of importance. Do not re-report items indexed as addressed or skippable; carry indexed open actions forward.
   - Update the status index after triage. Mark no-action or explicitly resolved messages read only when authorized and supported by the Gmail connector. If the connector cannot change read state, the index still prevents them recurring.
3. Review calendar events for the week. Surface busy or unusual days, important meetings, preparation implied by event descriptions, conflicts, and invitations still needing a response. Do not change calendar events.
4. Combine explicit email and calendar follow-ups into a prioritized action list. Give each action an owner/source and a due date when known. Distinguish stated deadlines from inferred timing; label inference clearly.
5. Return a concise briefing using this format:

   - **Top priorities** — up to three items to orient the week.
   - **Inbox** — needs a decision/reply, deadlines, and useful awareness items.
   - **Week ahead** — calendar highlights, notably dense days, and preparation points.
   - **Actions to carry forward** — concrete tasks, ordered by urgency, with source and due date if available.
   - **Coverage and gaps** — sources and date ranges reviewed; call out missing task sources or uncertain interpretations.

6. Offer reply drafts only when requested or clearly useful, and keep them for Caleb to review. Never send, archive, label, delete, or otherwise modify email beyond the authorized read-state handling above. Do not create, move, edit, or delete calendar events without confirming the specific change under the hub's calendar rule.

## Briefing qualities

- Lead with the few items most likely to need action. Omit routine confirmations, resolved threads, promotions, and low-impact FYIs.
- Keep sensitive message contents out of any saved workflow notes. Link to source messages or calendar events when connectors provide stable links.
- Group repetitive system notifications; include only items that meet the email skill's relevance criteria.
- Separate confirmed facts from inferred urgency or preparation needs.
- Keep the result short enough to scan in a few minutes. Caleb can tune the lookback, week window, amount of detail, and action thresholds after trying the first briefings.

## Inputs, output, and review

- **Inputs:** connected inbox and primary calendar, with explicit date windows.
- **Output:** a prioritized briefing and action list, with source links where available.
- **Human review:** Caleb decides what to act on, approves any reply text, and confirms any proposed external changes.
