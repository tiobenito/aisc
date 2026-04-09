---
name: morning-briefing
description: "Daily morning briefing. Use when user says 'briefing', 'morning briefing', 'what does my day look like', 'catch me up', or '/briefing'."
allowed-tools: ["Bash", "Read", "Write", "Edit"]
---

# Morning Briefing

Read my email and calendar, then give me a structured daily briefing.

## Workflow

1. **Get today's calendar events**
   <!-- TODO: Use gws calendar events list to fetch today's events -->
   <!-- Include: event name, time, location, attendees -->

2. **Get recent emails**
   <!-- TODO: Use gws gmail to fetch recent unread messages -->
   <!-- Read metadata: From, Subject, Date -->
   <!-- Decide: how many emails? unread only? skip promotions? -->

3. **Synthesize into a briefing**
   <!-- TODO: Combine calendar + email into a structured summary -->
   <!-- Sections: Schedule, Email Highlights, Action Items -->

4. **Present the briefing**
   <!-- TODO: Define the output format -->
   <!-- Keep it scannable -- tables for schedule, grouped emails, numbered action items -->

## Output Format

<!-- Fill this in: what sections, what level of detail, any special formatting -->

## Notes

<!-- Add any personal preferences here: tone, length, what to skip, etc. -->
