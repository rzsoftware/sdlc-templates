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

## Templates

### Squad Lead (`squad-lead/`)

| Template | When | Purpose |
|----------|------|---------|
| [R-4 Pipeline Status](squad-lead/R-4-pipeline-status.md) | Sprint start | Snapshot of what's ready and what's in progress |
| [R-3 Readiness Checkpoint](squad-lead/R-3-readiness-checkpoint.md) | R-3 | What moved, what's stalled, specific gaps |
| [R-2 Pipeline Warning](squad-lead/R-2-pipeline-warning.md) | R-2 | Formal warning if coverage < 80% |
| [R-1 Final Status](squad-lead/R-1-final-status.md) | Day before sprint | Exact loadable capacity, final call |
| [Partial Definition Override](squad-lead/partial-definition-override.md) | As needed | When leadership pushes to start without full DoR |
| [Starved Sprint Scorecard Entry](squad-lead/starved-sprint-scorecard-entry.md) | Sprint close | Document the gap when a sprint ran starved |

### VPoE (`vpoe/`)

| Template | When | Purpose |
|----------|------|---------|
| [R-1 Cross-Squad Summary](vpoe/R-1-cross-squad-summary.md) | Day before sprint | All squads at a glance for leadership |
| [Two-Sprint Escalation](vpoe/two-sprint-escalation.md) | After 2 consecutive starved sprints | Formal escalation to product leadership |
| [Starved Sprint Log](vpoe/starved-sprint-log.md) | Ongoing | Running record of every starved sprint |
| [Quarterly Override Review](vpoe/quarterly-override-review.md) | End of quarter | Cost analysis of partial-definition overrides |

## Rules

1. **Send on schedule.** Not when you feel like it. Not when things are bad. Every sprint, every milestone.
2. **Fill every field.** Blank fields are ambiguous. If the answer is "none" or "N/A," write that.
3. **Email from R-2 onward.** Slack is for R-4 and R-3. Email creates a searchable, timestamped record.
4. **Factual language only.** These are process artifacts, not personal requests. The templates are worded this way deliberately.
5. **cc VPoE on everything.** VPoE needs full visibility to produce the cross-squad summary and to maintain the Starved Sprint Log.

## Setup

1. Add R-4, R-3, R-2, R-1 as recurring calendar events for every sprint.
2. Bookmark this repo. Open the template, fill in the blanks, send.
3. VPoE: maintain the [Starved Sprint Log](vpoe/starved-sprint-log.md) as a living document (Confluence or spreadsheet).

## Reference

These templates implement the processes defined in the [SDLC Playbook — Measure](https://rzsoftware.github.io/sdlc/metrics/) section:
- [Pipeline Health Notifications](https://rzsoftware.github.io/sdlc/metrics/#pipeline-health-notifications)
- [Starved Sprint Protocol](https://rzsoftware.github.io/sdlc/metrics/#starved-sprint-protocol)
- [Partial Definition Override](https://rzsoftware.github.io/sdlc/metrics/#partial-definition-override)
