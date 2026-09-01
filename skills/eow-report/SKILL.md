---
name: eow-report
description: >
  Builds the weekly EOW (End of Week) report for an ATP CSM. Trigger when the
  CSM says "EOW report", "end of week report", "weekly report", "Friday report",
  or asks to submit their report. Due every Friday EOD via Asana form. Pulls
  from Asana if connected. Always uses the CSM's saved name — never hardcoded.
---

Build the CSM's End of Week report. Due every Friday before EOD.

## Step 1 — Load CSM profile

Check memory for `csm_profile.md`. Read their name and email.
If not found, prompt: "Run /atp-setup first so I know who you are."

## Step 2 — Pull weekly data (if Asana is connected)

If Asana MCP is available:
- Fetch all tasks completed this week
- Fetch calls logged this week (or tasks tagged as calls)
- Fetch any open ascension conversation tasks
- Fetch any escalation tasks from this week

If Asana is not connected, ask the CSM:
1. How many calls did you complete this week?
2. Any ascension conversations opened or closed?
3. Any student wins to highlight?
4. Any escalations or issues to flag?
5. What's your plan for next week?

## Step 3 — Draft the EOW report

Format it ready to paste into the Asana EOW form:

---

**EOW Report — [CSM Name] — Week of [Date Range]**

**CALLS THIS WEEK**
- Total calls completed: [X] (Target: 20–25)
- On track / behind / ahead: [assessment]

**STUDENT HIGHLIGHTS**
- Wins: [student name — what they achieved]
- Students moved from Yellow → Green: [names]
- Students currently Yellow: [names + intervention taken]
- Students currently Red: [names + escalation status]

**ASCENSION ACTIVITY**
- Conversations opened this week: [X]
- Outcomes: [Soft Yes / Genuine Maybe / Soft No — per student]
- Follow-ups scheduled: [dates]

**ESCALATIONS**
- Any refund requests, disputes, or flags this week: [detail or "None"]
- Escalated to Brittany: [Y/N + reason]

**WINS TO SHARE**
[1–2 student success moments worth posting in #student-results-and-content]

**NEXT WEEK PRIORITIES**
1. [Priority 1]
2. [Priority 2]
3. [Priority 3]

---

## Step 4 — Submit reminder

After drafting, remind the CSM:
"Submit this via the Asana EOW form before EOD today. Once submitted, set
your Sunday night reminder to update your CSM scorecard before the 7AM PT
Monday L10 meeting."
