---
name: morning-brief
description: >
  Generates a personalized morning brief for an ATP CSM. Trigger when the CSM
  says "morning brief", "good morning", "what's my day look like", "run my
  brief", or starts their session without context. Pulls from Asana if connected.
  Always addresses the CSM by their saved name — never uses a hardcoded name.
---

Generate a personalized morning brief for the CSM. Run every morning before
calls start.

## Step 1 — Load CSM profile

Check memory for `csm_profile.md`. Read their name. Use it throughout.
If not found, prompt: "Run /atp-setup first so I know who you are."

## Step 2 — Pull live data (if Asana is connected)

If Asana MCP is available:
- Fetch tasks due today assigned to this CSM
- Fetch tasks overdue (due before today, not yet complete)
- Fetch tasks completed today (to avoid flagging them as overdue)
- Fetch any tasks tagged as student calls scheduled today

If Asana is not connected, skip to Step 3 and note that connecting Asana
will unlock live data.

## Step 3 — Generate the brief

Format the brief as follows. Keep it scannable — no walls of text.

---

**Good morning, [CSM name]. Here's your day.**

**📅 TODAY — [Day, Date]**

**Calls scheduled:** [list student names + call times if available, or "Check your calendar"]

**🔴 Needs attention today:**
[List any overdue tasks or students flagged Yellow/Red. If none, say so.]

**✅ To-do today:**
[Numbered list of today's Asana tasks, or top 3 priorities if no Asana data]

**📈 This week so far:**
- Calls completed: [X of 20–25 target]
- Ascension conversations active: [list if any]

**🎯 One focus for today:**
[Pick the single most important thing — a Yellow student to turn Green, an
ascension conversation to open, or a critical task. Be specific.]

---

**Brittany's 7 call standards — check before every call:**
1. Book next call before this one ends
2. Assign specific homework (not "go through modules")
3. Your camera is on
4. Their camera is on
5. Stay 30–45 minutes
6. Talk less than the student (≤50%)
7. Explain like a teacher

---

## Step 4 — Offer next actions

After the brief, offer:
"Want me to prep for a specific call, triage your roster, or draft anything?"
