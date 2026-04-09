---
name: meeting-summary
description: "Process meeting transcripts or notes into structured summaries with action items. Use when user says 'meeting summary', 'process these meeting notes', 'what were the action items', or 'summarize this meeting'."
allowed-tools: ["Read", "Write", "Glob", "Edit"]
---

# Meeting Summary

Process meeting transcripts or raw notes into a structured summary with action items, owners, and deadlines.

## Workflow

1. Read the meeting transcript or notes provided by the user (pasted text, file path, or file in the current directory).

2. Extract meeting metadata:
   - Date
   - Attendees
   - Meeting purpose/topic

3. Identify key decisions -- things that were agreed on or resolved.

4. Extract action items:
   - **Owner:** Who is responsible?
   - **Task:** What needs to happen?
   - **Deadline:** When is it due? If none stated, write "Not specified."

5. Summarize the top 2-3 discussion highlights in one sentence each.

6. Format the output for [YOUR PREFERRED DESTINATION: Slack / email / Notion / markdown file].
   <!-- Replace with your preferred format. See examples/ for Slack and email templates. -->

7. After the user reviews the output, check if they corrected anything or expressed
   a preference. If so, append a note to `~/.claude/skills/meeting-summary/learnings.md`:
   ```
   ## Learning: [short title] ([today's date])
   [one or two sentences about what to do differently next time]
   ```

## Style Notes

- Be concise. Summaries should be scannable, not a wall of text.
- Use the person's first name for action item owners, not "the team" or "someone."
- If an action item is vague in the transcript, make it specific. "Look into it" becomes "Investigate X and report findings."
- If no deadline was mentioned, don't make one up. Just say "Not specified."

## What NOT to Do

- Don't include every topic discussed -- only the important ones.
- Don't editorialize. Report what was said, not your opinion on it.
- Don't invent action items that weren't mentioned or implied.
- Don't include filler conversation or social pleasantries in the summary.
