# Starved Sprint Log

> **Owner:** VPoE
> **Updated:** After every starved sprint
> **Purpose:** Running record of every sprint that ran under Starved Sprint Protocol. This is the primary data source for escalations and quarterly reviews. The [VPoE Dashboard](https://rzsoftware.github.io/sdlc/metrics/#dashboard-vpoe) shows starved sprints automatically via the `starved-sprint` label, but this log adds the root cause narrative and notification trail that Jira can't capture.
> **Fed by:** [Starved Sprint Scorecard Entry](../squad-lead/starved-sprint-scorecard-entry.md)
> **Feeds into:** [Two-Sprint Escalation](two-sprint-escalation.md) | [Rolling Dashboard](rolling-dashboard.md)

---

## How to Use

1. Add one row per starved squad per sprint.
2. Pull data from Squad Lead's [Starved Sprint Scorecard Entry](../squad-lead/starved-sprint-scorecard-entry.md). Capacity and loaded points are also in Jira Sprint Report.
3. Reference this log in [Two-Sprint Escalations](two-sprint-escalation.md) and [Quarterly Override Reviews](quarterly-override-review.md).
4. Maintain this as a living document in Confluence. This markdown version is the template.

---

## Log

| # | Sprint | Dates | Squad | PO | Capacity (pts) | Loaded (pts) | Coverage % | Gap (pts) | Root Cause | R-2 Warning Sent | Consecutive Count | Escalation Sent |
|---|--------|-------|-------|----|---------------|-------------|-----------|----------|------------|-----------------|------------------|----------------|
| 1 | ___ | ___ | ___ | ___ | ___ | ___ | ___% | ___ | ___ | ___ | ___ | ___ |
| 2 | ___ | ___ | ___ | ___ | ___ | ___ | ___% | ___ | ___ | ___ | ___ | ___ |
| 3 | ___ | ___ | ___ | ___ | ___ | ___ | ___% | ___ | ___ | ___ | ___ | ___ |

---

## Quarterly Summary

_Complete at end of each quarter. Pull starved sprint count and override data from [VPoE Dashboard](https://rzsoftware.github.io/sdlc/metrics/#dashboard-vpoe). Root cause breakdown and escalation outcomes are narrative — only this log has them._

### Q[N] FY[YEAR]

| Metric | Value |
|--------|-------|
| **Total starved sprint instances** | ___ |
| **Squads affected** | ___ |
| **Total unrealized capacity** | ___ pts |
| **Most affected squad** | ___ (___ instances) |
| **Most common root cause** | ___ |
| **Escalations sent** | ___ |
| **Escalation outcomes** | ___ |

### Trend

| Quarter | Instances | Unrealized Capacity | Squads Affected |
|---------|-----------|-------------------|----------------|
| Q[N-2] | ___ | ___ pts | ___ |
| Q[N-1] | ___ | ___ pts | ___ |
| Q[N] | ___ | ___ pts | ___ |

---

_This log is referenced by the [SDLC Playbook — Starved Sprint Protocol](https://rzsoftware.github.io/sdlc/metrics/#starved-sprint-protocol)._
