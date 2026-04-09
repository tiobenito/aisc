# Sample Output -- Slack Format

This is what the `/meeting-summary` skill produces when formatted for Slack, based on `samples/transcript-1.md`.

---

**Product Team Standup -- March 27**
5 attendees: Sarah, Marcus, Priya, Jordan, Lena

**Key Decisions**
- Notification delay is priority one -- diagnosis needed before any other backend work
- Empty state dashboard: Priya mocking up two options (guided tutorial vs. minimal)
- Welcome email improvements deferred to post-beta backlog
- Mobile testing starts next Monday after breakpoints are locked Friday

**Action Items**
- [ ] Jordan -- Diagnose push notification delay (30s latency). Due: tomorrow EOD
- [ ] Jordan -- Fix silent failure bug in collaborator invite flow. Due: after notification investigation
- [ ] Priya -- Mock up 2 empty state options for dashboard. Due: Thursday
- [ ] Priya -- Finalize mobile responsive breakpoints. Due: Friday
- [ ] Priya -- Add welcome email improvement to backlog. Due: not specified
- [ ] Priya -- Review Sarah's beta invite email draft. Due: tomorrow
- [ ] Marcus -- Set up staging environment (database + feature flags). Due: Thursday (Friday morning latest)
- [ ] Sarah -- Draft beta invite email. Due: today
- [ ] Lena -- Begin mobile responsive testing. Due: next Monday

**Discussion Highlights**
- Auth/OAuth flow is complete, just needs cleanup
- Push notification service has a ~30s delay, likely a worker pool sizing issue
- Beta launch is in 2 weeks -- staging environment and invite emails are the critical path
