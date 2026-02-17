# R-2: Pipeline Warning

> **When:** R-2 — only sent when pipeline coverage is < 80% of target load
> **From:** Squad Lead
> **To:** PO
> **cc:** VPoE, PO's manager
> **Channel:** Email (paper trail required)
> **Time to fill out:** ~5 minutes
> **Previous:** [R-3 Readiness Checkpoint](R-3-readiness-checkpoint.md) | **Feeds into:** [Sprint Tracker](../vpoe/sprint-tracker.md) (R-2 section) | Next: [R-1 Final Status](R-1-final-status.md)

---

**Subject:** [SQUAD NAME] Sprint [NEXT SPRINT #] Pipeline At Risk — R-2

---

Hi [PO NAME],

This is a scheduled R-2 Pipeline Warning. Available Engineering Ready stories cover **___% of sprint capacity**. If not resolved by R-1, Sprint [NEXT SPRINT #] will run under the Starved Sprint Protocol at reduced capacity.

## The Numbers

_Pull from your [Squad Dashboard](https://rzsoftware.github.io/sdlc/metrics/#dashboard-squad) — Pipeline Depth gadget and Velocity Chart._

| | Value |
|---|---|
| **Available capacity** | ___ pts |
| **Engineering Ready stories** | ___ pts |
| **Gap** | **___ pts (___%)** |

## What's Not Ready

_This is the critical narrative section. Jira shows which stories aren't ready; this explains what each one needs and whether it's achievable by R-1._

| Jira Key | Title | Est Points | DoR Gap | What Would Need to Happen by R-1 |
|----------|-------|-----------|---------|----------------------------------|
| ___ | ___ | ___ | ___ | ___ |
| ___ | ___ | ___ | ___ | ___ |
| ___ | ___ | ___ | ___ | ___ |

## If Nothing Changes

- Sprint [NEXT SPRINT #] loads at **___% capacity**
- Remaining capacity allocated to: **[tech debt / reliability / SRE work]**
- Starved Sprint Protocol activates — gap documented in Starved Sprint Log

## Notification History

| Milestone | Date Sent | Coverage at Time |
|-----------|-----------|-----------------|
| R-4 Pipeline Status | [DATE] | ___% |
| R-3 Readiness Checkpoint | [DATE] | ___% |
| **R-2 Warning (this email)** | **[DATE]** | **___%** |

## Context

<!-- DELETE ONE: -->
This is the first time this squad has triggered an R-2 warning in [N] sprints.

<!-- OR -->
This squad has triggered R-2 warnings in [N] of the last [N] sprints. Previous warnings were sent on [DATES].

---

This is a scheduled process notification, not a request. The purpose is to provide visibility so that all parties have time to act before Sprint Planning.

_[SQUAD LEAD NAME]_
