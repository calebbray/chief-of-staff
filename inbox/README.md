# Hub improvement inbox

Agents working in any project can propose improvements to the instructions, skills, configuration, or permissions in this hub. A proposal is only a request for review; it does not authorize a change. Caleb reviews and approves each change before it is applied to the hub source.

## Request files

Save proposals in `inbox/requests/` as `<UTC timestamp>-<short-slug>.md`, for example `20261029T221500Z-email-priority.md`.

Use this format:

```markdown
---
type: instruction | skill | config | permission
target: path or named workflow
source_repo: repository or "personal"
origin: requested | observed
effort: 0
impact: 0
---

## Proposed change
Describe the change clearly.

## Why
Explain the recurring problem or benefit.

## Evidence
Quote the relevant correction or describe the repeated friction. Remove sensitive message contents and personal data.

## Suggested patch
Optional draft text or diff.
```

Use one lesson per file. Check for a matching request before creating a new one; update the existing request with additional evidence where appropriate. Score effort and impact from 0 to 10, where higher effort means more work and higher impact means greater expected benefit. Do not include email bodies, credentials, tokens, or other sensitive data in proposals.

## Review and resolution

Review pending files, merge duplicates, and present proposed changes with their rationale and exact patch. Apply only the changes Caleb approves. Keep unrelated requests pending. After an approved change is committed and installed as appropriate, remove its request file. Keep rejected requests only if Caleb wants them retained.
