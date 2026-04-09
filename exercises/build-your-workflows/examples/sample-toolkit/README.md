# My AI Toolkit

Personal workflows built during AI for Productivity, Week 4.

| Workflow | Type | How to trigger |
|----------|------|---------------|
| Daily Standup Prep | Skill | Say "prep my standup" or "what's my update today" |
| Expense Categorizer | Skill | Say "categorize these expenses" or paste a CSV |
| Weekly Report | Skill | Say "draft my weekly report" or "weekly update" |
| Meeting Follow-up Emails | Saved prompt | Paste meeting notes and say "draft follow-ups" |
| Inbox Triage | MCP integration | Say "triage my inbox" (requires Gmail MCP) |

## Where things live

- Skills are installed at `~/.claude/skills/[name]/SKILL.md`
- Saved prompts and templates are in this folder as markdown files
- MCP configs are in `.mcp.json` (project) or `~/.claude/.mcp.json` (global)

## What I'd build next

- Slack channel summarizer (needs Slack MCP)
- Candidate screening pipeline (resume parsing + scorecard)
- Monthly budget review automation
