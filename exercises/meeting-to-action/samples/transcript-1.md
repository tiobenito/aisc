# Product Team Standup -- March 27, 2026

**Attendees:** Sarah (PM), Marcus (Engineering Lead), Priya (Designer), Jordan (Backend), Lena (QA)

---

**Sarah:** Alright, let's get going. Morning everyone. So quick recap -- we're two weeks out from the beta launch. I want to make sure we're aligned on what's left. Marcus, you want to start?

**Marcus:** Yeah sure. So the auth flow is basically done. Jordan finished the OAuth integration yesterday, just needs some cleanup. The main thing I'm worried about is the notification service. We're still seeing some delays on the push notifications -- like 30 seconds sometimes, which is way too slow.

**Sarah:** 30 seconds? That's... yeah that's not going to work for beta. What's causing it?

**Marcus:** Honestly not sure yet. Jordan's been looking into it. Jordan?

**Jordan:** Yeah so I think it's a queue issue. The worker pool might be undersized for the volume we're testing at. I haven't had time to dig in properly because I was finishing up the OAuth stuff. I can look at it today though.

**Sarah:** Okay, that needs to be priority one. Can we get that diagnosed by end of day tomorrow? Even if it's not fixed, I need to know what we're dealing with.

**Jordan:** Yeah, I'll have a diagnosis by tomorrow EOD.

**Sarah:** Perfect. Priya, where are we on the onboarding screens?

**Priya:** So the designs are done -- I shared them in Figma yesterday. The three-step flow we talked about. But I realized we never decided on the empty state for the dashboard. Like, what does a brand new user see before they've added any projects?

**Sarah:** Oh right. Yeah, we need to figure that out. Can you mock up two options? One with a guided tutorial thing and one that's more minimal -- just a "create your first project" button?

**Priya:** Sure. I can have those ready by Thursday.

**Marcus:** Actually, while we're talking about onboarding -- we should think about the welcome email too. Right now it's just a generic "thanks for signing up" thing. It would be way better if it linked to a quick start guide or something.

**Sarah:** Good call. Let's not scope creep though. Priya, can you add a note about the welcome email to the backlog? We'll tackle it after beta.

**Priya:** Yep, I'll add it.

**Sarah:** Cool. Lena, how's testing going?

**Lena:** Pretty good actually. I've been going through the test matrix for the core flows. Found a bug in the project creation flow yesterday -- when you try to add a collaborator by email and they don't have an account yet, it just fails silently. No error message, nothing.

**Marcus:** Oh that's not great. Is that on Jordan's plate?

**Jordan:** Yeah I saw the ticket. It's a simple fix -- I just need to add the invite flow fallback. I can do it after the notification investigation.

**Lena:** The other thing is I haven't started testing the mobile responsive stuff yet. Priya, are the mobile breakpoints finalized?

**Priya:** Almost. I need to adjust the nav for smaller screens. Give me until Friday and the breakpoints will be locked.

**Lena:** Works for me. I'll plan mobile testing for next Monday then.

**Sarah:** That works with the timeline. Okay, anything else? Oh wait -- Marcus, did you set up the staging environment for the beta testers?

**Marcus:** Not yet. I was going to do it this week. I need to spin up the separate database instance and configure the feature flags. Should be done by Friday.

**Sarah:** Let's aim for Thursday if possible? I want to send the beta invites Friday morning, and I need the staging URL to include in the email.

**Marcus:** Thursday's tight but I'll try. Worst case Friday morning before you send the invites.

**Sarah:** Okay. I'll draft the beta invite email today. Priya, can you review it tomorrow? Just make sure the design language matches what we've been doing.

**Priya:** Yeah, send it over whenever.

**Sarah:** Alright, I think we're good. Quick summary of what I'm hearing:
- Jordan's diagnosing the notification delay by tomorrow EOD
- Priya's got empty state mocks by Thursday and mobile breakpoints by Friday
- Lena's doing mobile testing next Monday
- Marcus is setting up staging by Thursday or Friday morning
- I'm drafting beta invites today

Anything I'm missing?

**Jordan:** Nope, I'll also fix that silent failure bug after the notification thing.

**Sarah:** Right, thanks Jordan. Okay everyone, let's have a great day. Ping me if anything comes up.

**Marcus:** Sounds good.

**Priya:** Thanks!
