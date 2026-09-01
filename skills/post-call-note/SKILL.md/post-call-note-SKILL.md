---
name: post-call-note
description: >
  Generates a formatted post-call portal note for an ATP CSM. Trigger when the
  CSM says "post call note", "portal note", "write my call recap", "log call
  notes", or just finished a student call and needs to post to the portal.
  Output is ONE single message — never split into multiple bubbles. NPS link
  goes inline at the bottom. Always uses the CSM's saved name — never hardcoded.
---

Generate a post-call portal note ready to paste into the ATP student portal.

## Step 1 — Load CSM profile

Check memory for `csm_profile.md`. Read their name.
If not found, prompt: "Run /atp-setup first so I know who you are."

## Step 2 — Gather call details

Ask the CSM (all at once, not one by one):

1. Student name?
2. What did you cover on this call?
3. What specific homework did you assign? (be exact — not "go through modules")
4. What is the next call date and time?
5. Any wins, breakthroughs, or concerns to note?

## Step 3 — Generate the portal note

Output as ONE single message block. Never split into multiple messages.
Copy this format exactly:

---

Hey [Student Name]! 👋

Great call today! Here's a quick recap of what we covered:

[2-3 sentences summarizing what was discussed — keep it encouraging and specific]

**Your homework before our next call:**
[Specific action item 1]
[Specific action item 2 if applicable]

**Next call:** [Day, Date at Time]

You're making great progress — keep the momentum going! If you have any questions before our next call, don't hesitate to reach out. 💪

How did your call go today? We'd love your feedback:
[NPS LINK — paste the ATP NPS survey link here]

— [CSM Name]

---

## Step 4 — Remind CSM

After generating, remind:
"Copy the entire message above as ONE paste into the portal — do not split it
into separate messages. Paste the NPS link before sending."
