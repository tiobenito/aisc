# Daily Standup Prep

**Type:** Skill
**Trigger:** "prep my standup" or "what's my update today"
**Time saved:** ~10 minutes/day

## What it does

Pulls together everything you need for a quick standup update: what you did yesterday, what's on deck today, and any blockers. It reads your recent git commits, calendar events, and task list to draft a concise update you can paste into Slack or read off in a meeting.

## How it works

1. Reads today's calendar events (via Google Calendar MCP)
2. Checks recent git commits or file changes from the last 24 hours
3. Reads your task list (TASKS.md or whatever you use)
4. Drafts a 3-section update: Done / Today / Blockers
5. Keeps each section to 2-3 bullets max

## Example output

```
Done yesterday:
- Finished Q2 budget review, sent to finance
- Onboarding doc updates for new hire starting Monday

Today:
- 1:1 with Jordan at 10am - prep performance review notes
- Finalize vendor contract (waiting on legal redlines)

Blockers:
- Still waiting on headcount approval from VP - following up today
```

## Where it lives

`~/.claude/skills/standup-prep/SKILL.md`
