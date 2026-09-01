---
name: eod-debrief
description: >
  Generates an end-of-day debrief for an ATP CSM. Trigger when the CSM says
  "EOD", "end of day", "wrap up", "debrief", "how did I do today", or wraps
  their session. Pulls completed and open tasks from Asana if connected.
  Addresses the CSM by their saved name — never uses a hardcoded name.
---

Run the end-of-day debrief. Helps the CSM close out cleanly and set up tomorrow.

## Step 1 — Load CSM profile

Check memory for `csm_profile.md`. Read their name. Use it throughout.
If not found, prompt: "Run /atp-setup first so I know who you are."

## Step 2 — Pull live data (if Asana is connected)

If Asana MCP is available:
- Fetch tasks COMPLETED today (completed_since: start of today)
- Fetch tasks still open that were due today
- Fetch tasks due tomorrow
- IMPORTANT: Never flag a task as overdue without first checking if it was
  completed today. Always pull completed tasks before flagging anything.

If Asana is not connected, ask the CSM: "How many calls did you complete today?
Anything you want to note or flag for tomorrow?"

## Step 3 — Generate the debrief

---

**End of day, [CSM name]. Here's how today went.**

**✅ Completed today:**
[List tasks completed, or calls logged if provided manually]

**📋 Calls today:**
- Total calls: [X]
- Week total so far: [X of 20–25 target]
- Students called: [names if available]

**⚠️ Still open (carry to tomorrow):**
[List any tasks that were due today but not completed. Do NOT include tasks
completed today — double-check before listing.]

**🌅 Tomorrow's priorities:**
[Top 3 tasks or students to focus on tomorrow, based on open items + due dates]

**🔔 Ascension check:**
Any students you had an ascension conversation with today? If yes, log it:
- Student name, outcome (Soft Yes / Genuine Maybe / Soft No), follow-up date

**💬 Anything to flag for Brittany or the team?**
[Escalations, wins to post in #student-results-and-content, or issues to surface]

---

**Before you close out:**
- [ ] Call notes logged in Asana for every call today
- [ ] Next call booked with every student you spoke to
- [ ] Any Yellow students — did you increase touchpoints?
- [ ] Friday: EOW report submitted?

---

## Step 4 — Offer next actions

After the debrief, offer:
"Want me to draft any follow-up messages, flag something for Brittany, or
set your task priorities for tomorrow?"
