---
name: meeting-notes
description: Turn uploaded meeting transcripts or notes into dated Obsidian notes. Use when Caleb asks to process, summarize, or file meeting material.
---

# Meeting Transcript Notes

## Goal

Create a useful, dated Obsidian record from meeting material while preserving the source and distinguishing source content from AI summaries.

## Inputs and destination

- Input: an uploaded transcript or contemporaneous meeting notes.
- Output: one concise dated meeting note and, when a transcript is supplied, a separate preserved transcript file.
- Use the vault path supplied by Caleb for the task. Do not put the vault's private content in this hub.
- For one-on-ones, store meeting notes in `Meetings/One on ones/<Person>/`. Keep one dated note per meeting, named `YYYY-MM-DD - <meeting title>.md`. If a person's directory does not exist, create it when the destination is clear.
- Store original transcripts separately in `Meetings/Transcripts/`, named `<meeting-title>-<person>-<YYYY-MM-DD>.txt` (lowercase, hyphen-separated). Use `.txt` to preserve the supplied transcript without Markdown formatting.
- Add a link from each summary to its source transcript. Keep the summary useful on its own so routine action-item and takeaway reviews do not require reopening or reprocessing the full transcript. Use the summary as the normal source for follow-up questions; consult the transcript only when Caleb asks for source detail or the summary is insufficient.
- Use the exact Google Calendar event title as the meeting's stable identity. Match a transcript to a calendar event by date and attendees; record the title in the meeting note. If the match or target meeting is ambiguous, ask Caleb rather than guessing.
- If the meeting date, attendee, or destination is unclear, ask Caleb before filing.

## Workflow

1. Identify whether the source is a transcript or notes. Confirm the meeting date and attendees from the source or ask Caleb if they are ambiguous.
2. For a one-on-one, create a separate dated note in the attendee's folder. Read relevant existing notes for context, but do not append a new meeting to a running page.
3. Save the supplied transcript verbatim in the transcript directory and link it from the summary. Separate source material from AI-generated summaries; never replace the transcript with a summary.
4. Summarize only what the source supports. Organize useful content under topics, decisions, action items, and open questions. Include owners and due dates only when explicit. Link to existing people or project pages only when the match is clear.
5. Check the source for explicit follow-ups intended for another meeting. Put clearly targeted talking points on the agenda for the target calendar event. Add action items to the shared index when Caleb owns them, or when the source explicitly shows he needs to monitor another person's follow-through. Keep source links on every indexed item. Ask if the target meeting is unclear.
6. Maintain `hub/meeting-follow-through.md` in the Obsidian vault as the index, alongside `hub/email-index.json`. Group entries by exact Calendar event title with separate sections for agenda talking points and open action items. Keep a talking point active until a later transcript or meeting note shows it was raised; record its outcome in that meeting note. Keep an action item open until a transcript or meeting note explicitly states that it is complete. A mention or discussion alone does not close it.
7. When Caleb asks for a meeting briefing, use the calendar event title as the key. Include all open indexed action items and talking points for that title, plus a concise synopsis of the most recent prior meeting note with the same title. Do not reread or reprocess its transcript unless Caleb asks for source detail or the summary is insufficient. If the event title does not identify one meeting clearly, ask Caleb.
8. Do not generate or reconstruct a transcript from notes. If no transcript was provided, process the supplied notes as notes and label them accordingly; do not invent dialogue, quotes, speaker turns, decisions, or commitments.
9. When Caleb has asked to file the material and the destination is clear, write the note and transcript to their respective locations. Afterward, report both exact Obsidian paths and call out any uncertainties.

## Suggested meeting note structure

Follow an existing note's format when one is present. Otherwise use:

```markdown
## <Month> <day>, <year>
### <Meeting name>

**Attendees:** <known attendees>
**Source:** <uploaded notes, or link to the preserved transcript>
**Calendar event title:** <exact Google Calendar title, when matched>

### Summary
<Short factual summary>

### Topics
- <Topic and source-grounded details>

### Decisions
- <Decision, or “No decision recorded”>

### Action items
- [ ] <Owner> — <action> — <due date if explicit>

### Open questions
- <Question or unresolved point>

### Source material
<Notes, or a link to the preserved transcript file>
```

Do not add empty sections if they make the note harder to scan. Keep AI summaries and extracted action items separate from the original source material.

## Learning

If Caleb corrects the filing location, preferred structure, or extraction criteria in a way likely to recur, follow `AGENTS.md` and file or update a proposal in `inbox/requests/`. Do not silently change this skill based on one correction.
