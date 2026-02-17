# SDLC Templates

Fill-in-the-blank sprint pipeline templates for Squad Leads and VPoE.

These templates handle **narrative communication and judgment calls** — the things Jira can't automate. All quantitative data (pipeline coverage, carry-over, velocity, scope adds, overrides) lives in Jira dashboards configured via the [Jira Setup Playbook](https://rzsoftware.github.io/sdlc/metrics/#jira-setup). Templates reference the dashboards for numbers and focus on context, assessment, and escalation.

> The hard work is already done. The dashboards show the numbers. These templates add the narrative. Your job is to pull the numbers, add your assessment, and hit send.

## What Jira Handles vs. What Templates Handle

| Jira (automatic) | Templates (narrative) |
|---|---|
| Pipeline depth, coverage % | Why stories aren't ready, specific DoR gaps |
| Carry-over count and rate | Root cause analysis, coaching notes |
| Scope add count | Escalation history and notification trail |
| Override count by requestor | Risk assessment, requestor acknowledgment |
| Velocity and commitment ratio | Status judgment (GREEN/AMBER/RED) |
| Blocker count and duration | Cross-squad pattern interpretation |

## How It Works

Every sprint follows a 4-milestone notification cadence. Squad Leads pull numbers from their [Squad Dashboard](https://rzsoftware.github.io/sdlc/metrics/#dashboard-squad), add narrative context, and send. VPoE pulls from the [VPoE Dashboard](https://rzsoftware.github.io/sdlc/metrics/#dashboard-vpoe) for the cross-squad roll-up.

```
R-4 (Sprint start)     Squad Lead → PO, cc VPoE        Pipeline snapshot + candidate gaps
R-3                     Squad Lead → PO, cc VPoE        Movement update + stalled stories
R-2                     Squad Lead → PO, cc VPoE+mgr    Warning (if <80% coverage)
R-1 (Day before)        Squad Lead → PO, cc VPoE        Final status + gate checklist
R-1 (VPoE roll-up)      VPoE → CTO, VP Product          Cross-squad summary
```

### Data Flow

```
                    Jira Dashboards
                    ───────────────
                    Squad Dashboard ──→ numbers for all templates
                    VPoE Dashboard  ──→ cross-squad numbers

Squad Lead                              VPoE
──────────                              ────
R-4 Pipeline Status ──────────────────→ Sprint Tracker (R-4 section)
        ↓
R-3 Readiness Checkpoint ─────────────→ Sprint Tracker (R-3 section)
        ↓
R-2 Pipeline Warning ─────────────────→ Sprint Tracker (R-2 section)
        ↓
R-1 Final Status ─────────────────────→ Sprint Tracker (R-1 section)
                                        ↓
                                   R-1 Cross-Squad Summary → CTO, VP Product
                                        ↓
                                   Rolling Dashboard (updated at sprint close)

Starved Sprint Scorecard Entry ───────→ Starved Sprint Log
                                        ↓ (after 2 consecutive)
                                   Two-Sprint Escalation → Product Leadership

Partial Definition Override ──────────→ Quarterly Override Review

Hill Street Prep (weekly) ────────────→ Hill Street action items
```

## Templates

### Squad Lead (`squad-lead/`)

| Template | When | Purpose | Feeds Into |
|----------|------|---------|------------|
| [R-4 Pipeline Status](squad-lead/R-4-pipeline-status.md) | Sprint start | Dashboard numbers + candidate DoR gaps | [Sprint Tracker](vpoe/sprint-tracker.md) → [R-3](squad-lead/R-3-readiness-checkpoint.md) |
| [R-3 Readiness Checkpoint](squad-lead/R-3-readiness-checkpoint.md) | R-3 | Movement since R-4, stalled stories, PTO status | [Sprint Tracker](vpoe/sprint-tracker.md) → [R-2](squad-lead/R-2-pipeline-warning.md) |
| [R-2 Pipeline Warning](squad-lead/R-2-pipeline-warning.md) | R-2 | Formal warning if coverage < 80% + notification history | [Sprint Tracker](vpoe/sprint-tracker.md) → [R-1](squad-lead/R-1-final-status.md) |
| [R-1 Final Status](squad-lead/R-1-final-status.md) | Day before sprint | Gate checklist + GREEN/AMBER/RED status call | [Sprint Tracker](vpoe/sprint-tracker.md) → [Cross-Squad Summary](vpoe/R-1-cross-squad-summary.md) |
| [Partial Definition Override](squad-lead/partial-definition-override.md) | As needed | DoR gap assessment + risk acceptance signature | [Quarterly Override Review](vpoe/quarterly-override-review.md) |
| [Starved Sprint Scorecard Entry](squad-lead/starved-sprint-scorecard-entry.md) | Sprint close | Root cause + notification trail for starved sprints | [Starved Sprint Log](vpoe/starved-sprint-log.md) |
| [Hill Street Prep](squad-lead/hill-street-prep.md) | Weekly | Top risk, cross-squad flags, help needed | [Sprint Tracker](vpoe/sprint-tracker.md) |

### VPoE (`vpoe/`)

| Template | When | Purpose | Fed By |
|----------|------|---------|--------|
| [Sprint Tracker](vpoe/sprint-tracker.md) | Every sprint (R-4 through close) | Process compliance checklist + execution notes | Squad Lead R-notifications + [VPoE Dashboard](https://rzsoftware.github.io/sdlc/metrics/#dashboard-vpoe) |
| [R-1 Cross-Squad Summary](vpoe/R-1-cross-squad-summary.md) | Day before sprint | GREEN/AMBER/RED per squad + RED squad narrative | [Sprint Tracker](vpoe/sprint-tracker.md) + [VPoE Dashboard](https://rzsoftware.github.io/sdlc/metrics/#dashboard-vpoe) |
| [Rolling Dashboard](vpoe/rolling-dashboard.md) | Updated at sprint close | Trend assessments, coaching notes, pattern interpretation | [Sprint Tracker](vpoe/sprint-tracker.md) + [VPoE Dashboard](https://rzsoftware.github.io/sdlc/metrics/#dashboard-vpoe) |
| [Starved Sprint Log](vpoe/starved-sprint-log.md) | Ongoing | Root cause narrative + escalation trail | [Starved Sprint Scorecard Entry](squad-lead/starved-sprint-scorecard-entry.md) |
| [Two-Sprint Escalation](vpoe/two-sprint-escalation.md) | After 2 consecutive starved sprints | Formal escalation with data + specific asks | [Starved Sprint Log](vpoe/starved-sprint-log.md) |
| [Quarterly Override Review](vpoe/quarterly-override-review.md) | End of quarter | Cost analysis + interpretation + recommendations | [Partial Definition Override](squad-lead/partial-definition-override.md) + [VPoE Dashboard](https://rzsoftware.github.io/sdlc/metrics/#dashboard-vpoe) |

## Prerequisites

Before using these templates, complete the [Jira Setup Playbook](https://rzsoftware.github.io/sdlc/metrics/#jira-setup):

1. **Custom fields** created (Engineering Ready, Original Estimate, Override Requestor, etc.)
2. **Labels** enforced (roadmap, tech-debt, sig/sre, partial-definition-override, starved-sprint, carried-over, scope-add, rework)
3. **Automation rules** deployed (scope add flagging, carry-over labeling, DoR gate reminder, etc.)
4. **Dashboards** built (Squad Dashboard per squad, VPoE Dashboard)

Without these, the templates will ask you to "pull from dashboard" and there won't be a dashboard to pull from.

## Where to Store Filled Instances

This repo is **templates only**. Never commit filled-in documents here. Filled instances go in Confluence.

### Confluence Structure

```
SDLC /
├── Sprint Records /
│   ├── Sprint 24.01 /
│   │   ├── Squad A — R-4 Pipeline Status
│   │   ├── Squad A — R-3 Readiness Checkpoint
│   │   ├── Squad A — R-2 Pipeline Warning (if sent)
│   │   ├── Squad A — R-1 Final Status
│   │   ├── Squad B — ...
│   │   ├── Squad C — ...
│   │   ├── Cross-Squad Summary
│   │   ├── Sprint Tracker (VPoE)
│   │   └── Overrides / (if any)
│   │       └── PROJ-123 — Partial Definition Override
│   ├── Sprint 24.02 /
│   │   └── ...
│   └── ...
├── Living Documents /
│   ├── Starved Sprint Log        ← one document, updated ongoing
│   └── Rolling Dashboard         ← one document, updated every sprint close
└── Quarterly Reviews /
    ├── Q1 FY25 — Override Review
    ├── Q2 FY25 — Override Review
    └── ...
```

## Rules

1. **Send on schedule.** Not when you feel like it. Not when things are bad. Every sprint, every milestone.
2. **Fill every field.** Blank fields are ambiguous. If the answer is "none" or "N/A," write that.
3. **Numbers from Jira, narrative from you.** Don't manually count points — pull from the dashboard. Add the context the dashboard can't show.
4. **Email from R-2 onward.** Slack is for R-4 and R-3. Email creates a searchable, timestamped record.
5. **cc VPoE on everything.** VPoE needs full visibility to produce the cross-squad summary.

## Setup

1. Complete the [Jira Setup Playbook](https://rzsoftware.github.io/sdlc/metrics/#jira-setup) first.
2. Create the Confluence folder structure above.
3. Add R-4, R-3, R-2, R-1 as recurring calendar events for every sprint.
4. Bookmark this repo. Open the template, copy to Confluence, fill in the blanks, send.
5. VPoE: copy the [Sprint Tracker](vpoe/sprint-tracker.md) into Confluence at R-4. Check it daily during refinement week. It takes 2 minutes.

## Reference

These templates implement the processes defined in the [SDLC Playbook — Measure](https://rzsoftware.github.io/sdlc/metrics/) section:
- [Jira Setup Playbook](https://rzsoftware.github.io/sdlc/metrics/#jira-setup) — the foundation these templates depend on
- [Pipeline Health Notifications](https://rzsoftware.github.io/sdlc/metrics/#pipeline-health-notifications)
- [Starved Sprint Protocol](https://rzsoftware.github.io/sdlc/metrics/#starved-sprint-protocol)
- [Partial Definition Override](https://rzsoftware.github.io/sdlc/metrics/#partial-definition-override)
- [Roles & Sprint-Cycle Expectations](https://rzsoftware.github.io/sdlc/organization/#roles-expectations)
- [Hill Street — Weekly Leadership Sync](https://rzsoftware.github.io/sdlc/organization/#hill-street)
