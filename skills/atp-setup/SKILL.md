---
name: atp-setup
description: >
  First-time setup for a new ATP CSM. Run this once on install to personalize
  all skills to your name. Trigger when a CSM says "set me up", "run setup",
  "atp setup", "I'm new", or installs the plugin for the first time. Must be
  run before any other skill works correctly.
---

Run this skill exactly once per CSM on first install. It personalizes every
other skill in the plugin to the CSM's name so nothing is hardcoded.

## Step 1 — Greet and explain

Say the following to the user (adapt tone to be warm):

"Welcome to the ATP CSM toolkit. This is your personal assistant for the
Client Success role at Abuv The Par — call prep, morning briefs, EOD
debriefs, ascension playbook, and the full EEC knowledge base are all in here.

Before we start, I need two things from you so everything is personalized to
you (not whoever set this up before you)."

## Step 2 — Collect name and email

Ask for:
1. Their first name (what they want the assistant to call them)
2. Their ATP email address (e.g. zara@abuvthepar.com)

Use AskUserQuestion with two free-text fields, or ask conversationally. Do not
proceed until both are provided.

## Step 3 — Save to memory

Save a memory file named `csm_profile.md` in the user's memory directory with
this exact format:

```markdown
---
name: csm-profile
description: "This CSM's personal profile — name and email used to personalize all ATP skills"
metadata:
  type: user
---

# CSM Profile

- **Name:** [their first name]
- **Email:** [their atp email]
- **Company:** Abuv The Par
- **Role:** Customer Success Manager
- **Setup date:** [today's date]
```

## Step 4 — Confirm and orient

After saving, tell them:

"You're set up, [their name]. Here's what you can do now:

- **Zee** — your CSM assistant. Ask for call prep, student triage, email drafts,
  ascension help, or anything ATP-related. Just say 'Zee' to activate.
- **Morning brief** — say 'morning brief' each day to see your calls, tasks, and
  student priorities.
- **EOD debrief** — say 'EOD' or 'end of day' to close out and plan tomorrow.
- **EOW report** — say 'EOW report' every Friday to build your weekly submission.

Connect your Asana and Fathom in Claude's connector settings to unlock the
full automation experience. Without them, I'll still help you plan and prep —
I just won't be able to pull live data."
