# SDLC Templates

Fill-in-the-blank sprint pipeline templates for Squad Leads and VPoE.

These templates exist so that pipeline communication is **scheduled, factual, and effortless**. They fire every sprint on a fixed cadence. When the pipeline is healthy, they take 5 minutes to fill out. When it's not, they create the paper trail that protects your squads.

> The hard work is already done. These templates encode the framework. Your job is to fill in the blanks and hit send.

## How It Works

Every sprint follows a 4-milestone notification cadence. Squad Leads send operational updates. VPoE sends the cross-squad roll-up.

```
R-4 (Sprint start)     Squad Lead → PO, cc VPoE        Pipeline snapshot
R-3                     Squad Lead → PO, cc VPoE        Readiness checkpoint
R-2                     Squad Lead → PO, cc VPoE+mgr    Warning (if needed)
R-1 (Day before)        Squad Lead → PO, cc VPoE        Final status
R-1 (VPoE roll-up)      VPoE → CTO, VP Product          Cross-squad summary
```

### Data Flow

Templates feed each other in a chain. Each template notes where its data comes from and where it goes.

```
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
```

## Templates

### Squad Lead (`squad-lead/`)

| Template | When | Purpose | Feeds Into |
|----------|------|---------|------------|
| [R-4 Pipeline Status](squad-lead/R-4-pipeline-status.md) | Sprint start | Snapshot of what's ready and what's in progress | [Sprint Tracker](vpoe/sprint-tracker.md) → [R-3](squad-lead/R-3-readiness-checkpoint.md) |
| [R-3 Readiness Checkpoint](squad-lead/R-3-readiness-checkpoint.md) | R-3 | What moved, what's stalled, specific gaps | [Sprint Tracker](vpoe/sprint-tracker.md) → [R-2](squad-lead/R-2-pipeline-warning.md) |
| [R-2 Pipeline Warning](squad-lead/R-2-pipeline-warning.md) | R-2 | Formal warning if coverage < 80% | [Sprint Tracker](vpoe/sprint-tracker.md) → [R-1](squad-lead/R-1-final-status.md) |
| [R-1 Final Status](squad-lead/R-1-final-status.md) | Day before sprint | Exact loadable capacity, final call | [Sprint Tracker](vpoe/sprint-tracker.md) → [Cross-Squad Summary](vpoe/R-1-cross-squad-summary.md) |
| [Partial Definition Override](squad-lead/partial-definition-override.md) | As needed | When leadership pushes to start without full DoR | [Quarterly Override Review](vpoe/quarterly-override-review.md) |
| [Starved Sprint Scorecard Entry](squad-lead/starved-sprint-scorecard-entry.md) | Sprint close | Document the gap when a sprint ran starved | [Starved Sprint Log](vpoe/starved-sprint-log.md) |
| [Hill Street Prep](squad-lead/hill-street-prep.md) | Weekly (before Hill Street call) | Pipeline status, top risk, cross-squad flags, help needed | [Sprint Tracker](vpoe/sprint-tracker.md) |

### VPoE (`vpoe/`)

| Template | When | Purpose | Fed By |
|----------|------|---------|--------|
| [Sprint Tracker](vpoe/sprint-tracker.md) | Every sprint (R-4 through close) | Single-page checklist tracking all squad deliverables | [R-4](squad-lead/R-4-pipeline-status.md), [R-3](squad-lead/R-3-readiness-checkpoint.md), [R-2](squad-lead/R-2-pipeline-warning.md), [R-1](squad-lead/R-1-final-status.md) |
| [R-1 Cross-Squad Summary](vpoe/R-1-cross-squad-summary.md) | Day before sprint | All squads at a glance for leadership | [Sprint Tracker](vpoe/sprint-tracker.md), [R-1 Final Status](squad-lead/R-1-final-status.md) |
| [Rolling Dashboard](vpoe/rolling-dashboard.md) | Updated at sprint close | Cross-sprint squad health trends and rolling averages | [Sprint Tracker](vpoe/sprint-tracker.md), [Starved Sprint Log](vpoe/starved-sprint-log.md) |
| [Starved Sprint Log](vpoe/starved-sprint-log.md) | Ongoing | Running record of every starved sprint | [Starved Sprint Scorecard Entry](squad-lead/starved-sprint-scorecard-entry.md) |
| [Two-Sprint Escalation](vpoe/two-sprint-escalation.md) | After 2 consecutive starved sprints | Formal escalation to product leadership | [Starved Sprint Log](vpoe/starved-sprint-log.md) |
| [Quarterly Override Review](vpoe/quarterly-override-review.md) | End of quarter | Cost analysis of partial-definition overrides | [Partial Definition Override](squad-lead/partial-definition-override.md) |

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
│   │   ├── Squad B — R-4 Pipeline Status
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

### Why Confluence

- **Searchable:** Find any squad's R-2 warning from 3 months ago in seconds.
- **Commentable:** POs and managers can respond directly on the page.
- **Non-dev accessible:** Product leadership and PO managers don't need GitHub access.
- **Timestamped:** Confluence page history proves when a document was created.
- **Linkable:** Cross-reference pages. The Sprint Tracker can link directly to each squad's R-4, R-3, etc.

### Workflow

1. **R-4:** Squad Lead copies the R-4 template into the current sprint's Confluence folder. Fills it in. Sends via Slack with Confluence link. VPoE copies the Sprint Tracker into the same folder.
2. **R-3, R-2, R-1:** Same pattern. Each notification is a new Confluence page in the sprint folder.
3. **Sprint Close:** Squad Lead adds scorecard. VPoE updates Sprint Tracker close section, Rolling Dashboard, and Starved Sprint Log (if applicable).
4. **Quarterly:** VPoE creates the Quarterly Override Review page from the template.

## Rules

1. **Send on schedule.** Not when you feel like it. Not when things are bad. Every sprint, every milestone.
2. **Fill every field.** Blank fields are ambiguous. If the answer is "none" or "N/A," write that.
3. **Email from R-2 onward.** Slack is for R-4 and R-3. Email creates a searchable, timestamped record. Always include the Confluence link.
4. **Factual language only.** These are process artifacts, not personal requests. The templates are worded this way deliberately.
5. **cc VPoE on everything.** VPoE needs full visibility to produce the cross-squad summary and to maintain the Starved Sprint Log.

## Setup

1. Create the Confluence folder structure above.
2. Add R-4, R-3, R-2, R-1 as recurring calendar events for every sprint.
3. Bookmark this repo. Open the template, copy to Confluence, fill in the blanks, send.
4. VPoE: copy the [Sprint Tracker](vpoe/sprint-tracker.md) into Confluence at R-4. Check it daily during refinement week. It takes 2 minutes.
5. VPoE: maintain the [Rolling Dashboard](vpoe/rolling-dashboard.md) and [Starved Sprint Log](vpoe/starved-sprint-log.md) as living documents in the Living Documents folder. Update at every sprint close.

## Reference

These templates implement the processes defined in the [SDLC Playbook — Measure](https://rzsoftware.github.io/sdlc/metrics/) section:
- [Pipeline Health Notifications](https://rzsoftware.github.io/sdlc/metrics/#pipeline-health-notifications)
- [Starved Sprint Protocol](https://rzsoftware.github.io/sdlc/metrics/#starved-sprint-protocol)
- [Partial Definition Override](https://rzsoftware.github.io/sdlc/metrics/#partial-definition-override)
- [Roles & Sprint-Cycle Expectations](https://rzsoftware.github.io/sdlc/organization/#roles-expectations)
- [Hill Street — Weekly Leadership Sync](https://rzsoftware.github.io/sdlc/organization/#hill-street)
