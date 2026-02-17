# Starved Sprint — Scorecard Entry

> **When:** Sprint close, when the sprint ran under Starved Sprint Protocol
> **From:** Squad Lead
> **To:** VPoE
> **Channel:** Email + copy into Sprint Scorecard
> **Time to fill out:** ~5 minutes
> **Feeds into:** [Starved Sprint Log](../vpoe/starved-sprint-log.md) → [Two-Sprint Escalation](../vpoe/two-sprint-escalation.md) (if consecutive)

---

## Jira Setup

_Ensure the `starved-sprint` label was applied to all stories in this sprint at Sprint Planning (see [Jira Setup Playbook](https://rzsoftware.github.io/sdlc/metrics/#jira-setup)). This makes the sprint visible on the [VPoE Dashboard](https://rzsoftware.github.io/sdlc/metrics/#dashboard-vpoe)._

## Sprint Details

| Field | Value |
|-------|-------|
| **Sprint** | [SPRINT # — DATES] |
| **Squad** | [SQUAD NAME] |
| **Squad Lead** | [YOUR NAME] |
| **PO** | [PO NAME] |

## Capacity Gap

_Pull capacity from Velocity Chart. Pull loaded points from Sprint Report. These are in Jira — just record the numbers here for the email._

| | Points | % |
|---|---|---|
| **Available capacity** | ___ | 100% |
| **Product work loaded** | ___ | ___% |
| **Capacity gap** | ___ | ___% |

## Gap Allocation

_What engineering-owned work filled the remaining capacity? Filter your sprint board by labels `tech-debt` and `sig/sre` to pull these._

| Jira Key | Title | Points | Category |
|----------|-------|--------|----------|
| ___ | ___ | ___ | Tech debt / Reliability / Tooling / Test coverage |
| ___ | ___ | ___ | Tech debt / Reliability / Tooling / Test coverage |
| **Total** | | **___** | |

## Stories That Were Not Ready

_This is the narrative Jira can't provide — the specific DoR criteria each story failed and why._

| Jira Key | Title | Est Points | DoR Criteria Failed |
|----------|-------|-----------|-------------------|
| ___ | ___ | ___ | ___ |
| ___ | ___ | ___ | ___ |

## Root Cause

_Check all that apply:_

- [ ] Discovery incomplete — stories not yet through enablement pipeline
- [ ] Acceptance criteria missing or incomplete
- [ ] Technical design not reviewed
- [ ] PO unavailable / overcommitted
- [ ] Stakeholder decisions pending
- [ ] Dependencies on other teams not resolved
- [ ] Other: ___

**Narrative** (1-2 sentences): ___

## Notification Trail

| Milestone | Date Sent | Coverage at Time |
|-----------|-----------|-----------------|
| R-4 Pipeline Status | [DATE] | ___% |
| R-3 Readiness Checkpoint | [DATE] | ___% |
| R-2 Pipeline Warning | [DATE] or N/A | ___% |
| R-1 Final Status | [DATE] | ___% |

## Consecutive Starved Sprints

_Check the [VPoE Dashboard](https://rzsoftware.github.io/sdlc/metrics/#dashboard-vpoe) — Starved Sprint Stories gadget — to confirm consecutive count._

| | |
|---|---|
| **Is this consecutive?** | Yes / No |
| **How many in a row?** | ___ |
| **Previous starved sprints** | Sprint [#], Sprint [#] |

---

_This entry feeds into the VPoE [Starved Sprint Log](../vpoe/starved-sprint-log.md)._
