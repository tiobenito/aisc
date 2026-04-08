# AI Study Camp -- Resources

Shareable materials built for [AI Study Camp](https://aistudycamp.com) students.

## What's here

### skill-builder/
A guided workshop for building your first Claude Code skill. Takes about an hour. Claude acts as an interactive instructor and walks you through the whole thing.

```bash
cd skill-builder
claude
```

### decks/
HTML slide decks used in lectures.

- `agents-vs-workflows.html` -- Week 4 lecture: when to use agents vs. simple workflows

### skills/
Installable Claude Code skills. Drop any folder into `~/.claude/skills/` and it's ready to use.

- `idea-breakdown/` — give Claude one big idea or a list of automation candidates; get back a classified, prioritized build plan with agent vs. workflow recommendations

See guide 02 in the knowledge hub for how to install a skill from this repo.

## Other tools

- **cc-level-up** -- Claude Code personal trainer plugin. Scans your setup, grades it A-F, and tells you what to improve. Install via: `/plugin marketplace add tiobenito/cc-level-up`
  - Repo: [tiobenito/cc-level-up](https://github.com/tiobenito/cc-level-up)
