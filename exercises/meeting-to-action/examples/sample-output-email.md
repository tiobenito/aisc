# Sample Output -- Email Format

This is what the `/meeting-summary` skill produces when formatted for email, based on `samples/transcript-1.md`.

---

**Subject:** Product Standup Recap -- March 27

Hi team,

Quick recap from this morning's standup. We're two weeks out from beta launch -- here's where everything stands.

**Key Decisions**

- Notification delay investigation is the top priority this week
- Dashboard empty state: Priya will mock up two options (guided tutorial vs. minimal) for review Thursday
- Welcome email improvements moved to post-beta backlog
- Mobile responsive testing starts next Monday once breakpoints are locked

**Action Items**

| Owner | Task | Deadline |
|-------|------|----------|
| Jordan | Diagnose push notification delay (currently ~30s) | Tomorrow EOD |
| Jordan | Fix silent failure bug on collaborator invite flow | After notification diagnosis |
| Priya | Mock up 2 empty state dashboard options | Thursday |
| Priya | Finalize mobile responsive breakpoints | Friday |
| Priya | Add welcome email to backlog | Not specified |
| Priya | Review beta invite email draft | Tomorrow |
| Marcus | Set up staging environment (DB + feature flags) | Thursday (Friday AM latest) |
| Sarah | Draft beta invite email | Today |
| Lena | Start mobile responsive testing | Next Monday |

**Discussion Highlights**

- Auth/OAuth integration is complete. Just needs minor cleanup.
- Push notifications are hitting ~30s delays, likely due to an undersized worker pool. Jordan is investigating.
- Staging environment needs to be ready before beta invites go out Friday morning.

Let me know if I missed anything.

-[Your name]
