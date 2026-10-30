# Chief of Staff AI Hub

A version-controlled home for the instructions and workflows used in Caleb's three-month AI experiment. The aim is to find practical ways to reduce routine work and build confidence in AI as a chief-of-staff helper.

## What's here

- `AGENTS.md` — shared working instructions for agents operating in this repository.
- `.agents/skills/email/SKILL.md` — the first reusable workflow, discoverable by Codex when this repository is open.
- `.agents/skills/meeting-notes/SKILL.md` — a workflow for filing transcripts and meeting notes in Obsidian.
- `inbox/README.md` — format for agent-proposed improvements to this hub.
- `inbox/requests/` — local proposals awaiting review; request files are ignored by Git.

This repository is the authored source. Copies installed into agent-specific locations are outputs and should be updated from these files. Open this directory as the working project in Codex so it reads `AGENTS.md` and discovers the email skill.

## First experiment

Try the email skill on a small, recent slice of the inbox. Judge it by whether it helps answer: what needs my attention, what can wait, and what reply should I review? Improve the source files here based on actual friction.

## Current trust boundary

Agents may read and summarize email and prepare reply drafts. They must not send email or make other external changes unless Caleb explicitly approves the specific action. Trust can expand later by updating these instructions deliberately.

## Next steps

1. Run a small Codex inbox review and tune the instructions and email workflow from evidence.
2. Add further workflows, such as meeting minutes and action tracking, when ready.
3. Consider Claude setup after the Codex workflow is working.
