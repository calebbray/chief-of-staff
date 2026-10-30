---
name: meeting-notes
description: Turn uploaded meeting transcripts or notes into dated Obsidian notes. Use when Caleb asks to process, summarize, reconstruct, or file a meeting transcript or notes.
---

# Meeting Transcript Notes

## Goal

Create a useful, dated Obsidian record from meeting material while preserving the source and keeping inferred content clearly labeled.

## Inputs and destination

- Input: an uploaded transcript, meeting notes, or Caleb's request to reconstruct a missing transcript from notes.
- Output: a dated note or dated section in the Obsidian page/folder for that meeting.
- Use the vault path supplied by Caleb for the task. Do not put the vault's private content in this hub.
- Search the vault for an existing page that clearly matches the meeting, attendee, or project. Follow that page's current organization and formatting.
- If the meeting date, attendee, or destination is unclear, ask Caleb before filing. If no fitting page exists, ask whether to create one and where.

## Workflow

1. Identify the source type: verbatim transcript, contemporaneous notes, or reconstruction. Confirm the meeting date and attendees from the source or ask Caleb if they are ambiguous.
2. Read the relevant existing Obsidian page and match its structure. Keep prior entries intact; add a new dated section to an established running page when that is the current convention.
3. Separate source material from AI-generated summaries. Preserve the uploaded transcript as source text or a clearly referenced adjacent file; never replace it with a summary.
4. Summarize only what the source supports. Organize useful content under topics, decisions, action items, and open questions. Include owners and due dates only when explicit. Link to existing people or project pages only when the match is clear.
5. For a reconstruction, put a prominent label at the top: **AI-generated reconstruction — not verbatim**. State which notes informed it. Never present it as a recovered recording or transcript. If Caleb explicitly asks for transcript-style dialogue, mark every speaker turn and wording as inferred; do not add decisions or commitments absent from the source. Otherwise use a narrative summary and mark missing details as not captured.
6. When Caleb has asked to file the material and the destination is clear, write the dated note there. Afterward, report the exact Obsidian path and call out any uncertainties. Ask before creating a folder/page or changing a broader people/project summary.

## Suggested meeting note structure

Follow an existing note's format when one is present. Otherwise use:

```markdown
## <Month> <day>, <year>
### <Meeting name>

**Attendees:** <known attendees>
**Source:** <transcript, notes, or labeled reconstruction>

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

### Source transcript
<Original transcript text, or a link to the preserved source file>
```

Do not add empty sections if they make the note harder to scan. For reconstructed material, keep the reconstruction separate from any original notes.

## Learning

If Caleb corrects the filing location, preferred structure, or extraction criteria in a way likely to recur, follow `AGENTS.md` and file or update a proposal in `inbox/requests/`. Do not silently change this skill based on one correction.
