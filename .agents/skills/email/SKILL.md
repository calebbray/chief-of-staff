---
name: email
description: Triage Gmail, summarize messages that need attention, and prepare reply drafts for Caleb to review. Use when asked to review an inbox, find important or unanswered messages, or draft email responses.
---

# Email Triage and Drafting

## Goal

Reduce the need to scan the inbox while keeping Caleb in control of responses and account changes.

## Workflow

1. Confirm which connected Gmail account and time range to review if the request does not make that clear. Do not ask Caleb to paste an email address; use the account he selected in the connection flow.
2. Before triage, load the private email status index at `/Users/caleb.bray/notes/my thoughts/hub/email-index.json`. It contains message identifiers and triage state only; do not copy it into the repository or include message content.
3. Remove expired `addressed` and `skip` entries (seven days after their update). Keep `open` entries until resolved so an action does not disappear just because its email is older than the lookback.
4. Review the requested inbox slice against **Known priority criteria** below. Prioritize messages that require a decision, a response, a deadline, or a promised follow-up. Judge relevance by topic and Caleb's role, not by unread status or subject wording alone. Use unread/new messages as a review signal, not as a measure of importance.
5. Suppress messages whose Gmail message ID is indexed as `addressed` or `skip`. Surface indexed `open` items until they are resolved. A new message in the same thread has a different message ID and should be reviewed on its own.
6. Return a concise briefing grouped as:
   - **Needs your attention** — sender, subject, why it matters, and any deadline.
   - **Reply likely needed** — why a response is needed and a suggested reply draft.
   - **For awareness** — useful updates that do not appear to need action.
   - **No action apparent** — only if useful; summarize volume rather than listing every message.
7. Keep each summary grounded in the message. Mark uncertainty and distinguish explicit deadlines or asks from inferred ones.
8. Draft replies in Caleb's voice only when enough context is available. If key facts or a commitment are unclear, ask Caleb or leave a short placeholder instead of inventing them.
9. Update the private index after review: add `open` for actions needing follow-up, `skip` for low-value/no-action mail, and `addressed` when Caleb confirms completion. Store only `message_id`, status, `updated_at`, and the seven-day `expires_at` for resolved/skipped entries. Do not store subjects, senders, snippets, or email bodies.
10. Mark resolved or no-action messages read only when Caleb has authorized that action and the connected Gmail tools support it. If read-state changes are unavailable, say so clearly; the status index still prevents repeat triage.
11. Do not send, schedule, forward, archive, label, delete, or otherwise modify messages unless Caleb explicitly approves that specific action.
12. If asked to send an approved draft, show the complete final text and recipient immediately before the send action when the interface allows review.

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
| AWS Lambda notices routed through `api-dev-us@lightcast.io` or an AWS owner address | Usually team-handled | Surface only for outages, security risks, or major service disruptions or potential disruptions; omit other notices from the briefing |
| AWS CodeBuild runtime or image default changes | Not mission-critical when they only risk blocking future builds | Omit unless the notice indicates an outage, security risk, or major service disruption or potential disruption |
| Sentry notices | Relevant only for quota exhaustion | Surface when an error or other quota is running out or exhausted; omit individual error and QA issue alerts by default |
| Harness budget threshold alerts | Useful for early visibility; low urgency | Include spend and percentage as a low-priority awareness item; do not label as a red alert |
| IT and security tickets | Important | Use bullets of no more than 20 words each |

When a new or unclear recurring category's relevance is uncertain, ask Caleb before deciding how to handle it. For group-delivered AWS Lambda notices, surface only outages, security risks, or major service disruptions or potential disruptions. The Sentry quota rule applies regardless of routing. Caleb can ask to investigate other notices as needed.

## Learning

If Caleb corrects the triage criteria, preferred format, or drafting behavior in a way likely to recur, follow `AGENTS.md` and file or update a proposal in `inbox/requests/`. Do not silently change this skill based on one correction.
