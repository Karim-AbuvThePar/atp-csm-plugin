# ATP CSM Plugin

Personalized CSM toolkit for Abuv The Par. Includes the full EEC knowledge
base, call standards, ascension playbook, and automated daily workflows —
personalized to each CSM by name on first install.

## First-time setup

Run `/atp-setup` immediately after installing. This takes 2 minutes and
personalizes every skill to your name so nothing is hardcoded from someone else.

## Skills

| Skill | How to trigger | What it does |
|-------|---------------|-------------|
| **atp-setup** | "run setup" / "I'm new" | One-time onboarding — saves your name and personalizes everything |
| **zee** | Say "Zee" | Senior CSM assistant — call prep, student triage, ascension help, email drafts, escalation routing, course lookup |
| **morning-brief** | "morning brief" / "good morning" | Daily brief — calls, priorities, overdue tasks, 7 standards reminder |
| **eod-debrief** | "EOD" / "wrap up" | End-of-day close-out — what got done, what carries over, tomorrow's priorities |
| **eow-report** | "EOW report" / "weekly report" | Friday report builder — ready to paste into Asana EOW form |

## Knowledge base (inside Zee)

Zee has access to:
- Full EEC curriculum (115 lessons, 11 modules)
- 31-task student roadmap with stall point guidance
- Brittany's 7 call standards
- Team roster with emails and Slack channels
- Escalation paths for every scenario
- R.E.A.D.Y. ascension framework + A.E.A.C. objection handling
- 12 most common ascension objections with responses
- Student onboarding process by tier
- Downgrade and refund call frameworks

## Connect your tools

For live data in briefs and reports, connect in Claude's connector settings:
- **Asana** — pulls your tasks, calls, and student assignments
- **Fathom** — accesses your call recordings and transcripts

Without connectors, the plugin still works — you just provide context manually.

## Personalization

Every skill reads your name from memory (saved during setup). If something
still says the wrong name, run `/atp-setup` again to reset your profile.
