---
name: email
description: Triage Gmail, summarize messages that need attention, and prepare reply drafts for Caleb to review. Use when asked to review an inbox, find important or unanswered messages, or draft email responses.
---

# Email Triage and Drafting

## Goal

Reduce the need to scan the inbox while keeping Caleb in control of responses and account changes.

## Workflow

1. Confirm which connected Gmail account and time range to review if the request does not make that clear. Do not ask Caleb to paste an email address; use the account he selected in the connection flow.
2. Review the requested inbox slice against **Known priority criteria** below. Prioritize messages that require a decision, a response, a deadline, or a promised follow-up. Judge relevance by topic and Caleb's role, not by unread status or subject wording alone.
3. Return a concise briefing grouped as:
   - **Needs your attention** — sender, subject, why it matters, and any deadline.
   - **Reply likely needed** — why a response is needed and a suggested reply draft.
   - **For awareness** — useful updates that do not appear to need action.
   - **No action apparent** — only if useful; summarize volume rather than listing every message.
4. Keep each summary grounded in the message. Mark uncertainty and distinguish explicit deadlines or asks from inferred ones.
5. Draft replies in Caleb's voice only when enough context is available. If key facts or a commitment are unclear, ask Caleb or leave a short placeholder instead of inventing them.
6. Present drafts for review. Do not send, schedule, forward, archive, label, delete, or otherwise modify messages unless Caleb explicitly approves that specific action.
7. If asked to send an approved draft, show the complete final text and recipient immediately before the send action when the interface allows review.

## Useful briefing qualities

- Filter for relevance, not inbox status or subject wording. Lead with the few items most likely to need a decision, reply, follow-through, or meaningful deadline. Omit routine confirmations, resolved notices, promotions, and low-impact FYIs. Group duplicate alerts and keep distant deadlines out unless early action is useful.
- For IT and security tickets, use bullets of no more than 20 words each.
- Include links or stable message references when the connected tool provides them.
- Combine duplicate threads and avoid repeating quoted history.
- State what was reviewed and the time range so Caleb can judge coverage.
- Do not claim continuous monitoring. This skill runs when invoked or through a separately configured schedule.

## Known priority criteria

| Category | Caleb's relevance | Handling |
| --- | --- | --- |
| UKG time-off requests that need Caleb's review | Important | Surface as an action item |
| AWS Amazon Linux AMI alerts | Not relevant; team-handled | Omit from the briefing |
| Sentry and AWS Lambda notices routed through `api-dev-us@lightcast.io` or an AWS owner address | Usually team-handled | Surface only for outages, security risks, or major service disruptions or potential disruptions; omit other notices from the briefing |
| IT and security tickets | Important | Use bullets of no more than 20 words each |

When a new or unclear recurring category's relevance is uncertain, ask Caleb before deciding how to handle it. For group-delivered Sentry and AWS Lambda notices, surface only outages, security risks, or major service disruptions or potential disruptions. Caleb can ask to investigate other group notices as needed.

## Learning

If Caleb corrects the triage criteria, preferred format, or drafting behavior in a way likely to recur, follow `AGENTS.md` and file or update a proposal in `inbox/requests/`. Do not silently change this skill based on one correction.
