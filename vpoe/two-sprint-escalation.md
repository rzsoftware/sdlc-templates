# Two-Sprint Escalation

> **When:** After a squad has been starved for 2 consecutive sprints
> **From:** VPoE
> **To:** VP Product (or PO's manager)
> **cc:** CTO, affected Squad Lead
> **Channel:** Email (paper trail required)
> **Time to fill out:** ~15 minutes
> **Fed by:** [Starved Sprint Log](starved-sprint-log.md) + Squad Lead [Scorecard Entries](../squad-lead/starved-sprint-scorecard-entry.md)

---

**Subject:** Product Pipeline Gap — [SQUAD NAME] — 2 Consecutive Starved Sprints

---

Hi [VP PRODUCT / PO'S MANAGER NAME],

[SQUAD NAME] has been unable to fill engineering capacity for 2 consecutive sprints due to insufficient Engineering Ready stories. I'm flagging this per our sprint pipeline process so we can address it together.

## The Data

| | Sprint [#] | Sprint [#] |
|---|---|---|
| **Available capacity** | ___ pts | ___ pts |
| **Product work loaded** | ___ pts | ___ pts |
| **Coverage** | ___% | ___% |
| **Gap** | ___ pts | ___ pts |

**Cumulative unrealized product capacity:** ___ story points across 2 sprints.

## Notification History

Engineering flagged pipeline risk through the standard notification cadence:

### Sprint [FIRST STARVED]
| Milestone | Date | Coverage |
|-----------|------|----------|
| R-4 Pipeline Status | [DATE] | ___% |
| R-3 Readiness Checkpoint | [DATE] | ___% |
| R-2 Pipeline Warning | [DATE] | ___% |
| R-1 Final Status | [DATE] | ___% |

### Sprint [SECOND STARVED]
| Milestone | Date | Coverage |
|-----------|------|----------|
| R-4 Pipeline Status | [DATE] | ___% |
| R-3 Readiness Checkpoint | [DATE] | ___% |
| R-2 Pipeline Warning | [DATE] | ___% |
| R-1 Final Status | [DATE] | ___% |

## Stories That Were Not Ready

| Jira Key | Title | Est Points | DoR Criteria Failed | Sprint |
|----------|-------|-----------|-------------------|--------|
| ___ | ___ | ___ | ___ | ___ |
| ___ | ___ | ___ | ___ | ___ |
| ___ | ___ | ___ | ___ | ___ |

## Root Causes (from Starved Sprint Log)

_Check all that apply:_

- [ ] Discovery pipeline stalled — not enough stories entering enablement
- [ ] PO capacity — PO overcommitted, insufficient time for story writing
- [ ] AC quality — stories submitted but bounced at refinement for incomplete criteria
- [ ] Stakeholder dependencies — decisions pending from business/external teams
- [ ] Design bottleneck — UX/technical design not keeping pace
- [ ] Other: ___

**Narrative:** ___

## How Engineering Filled the Gap

| Category | Sprint [#] | Sprint [#] |
|----------|-----------|-----------|
| Tech debt | ___ pts | ___ pts |
| Reliability / SRE | ___ pts | ___ pts |
| Test coverage | ___ pts | ___ pts |
| Tooling | ___ pts | ___ pts |

This work has value but does not advance roadmap commitments.

## Impact

- **Roadmap items delayed:** ___ stories not started that were expected this quarter
- **Sprint goal achievement:** [hit/miss] for Sprint [#], [hit/miss] for Sprint [#]
- **Team morale signal:** ___ (optional — only include if relevant and factual)

## What I'm Asking For

<!-- Pick the ones that apply, delete the rest, or write your own: -->

1. **Joint pipeline review** — 30 minutes with you, [PO NAME], [SQUAD LEAD NAME], and me to identify the bottleneck and agree on a fix.

2. **More PO capacity for [SQUAD]** — [PO NAME] currently supports [describe scope]. Discovery time appears to be less than 40% of their week.

3. **Enablement pairing** — assign an enablement resource to pair with [PO NAME] on story writing and AC definition for the next sprint cycle.

4. **Scope reduction** — reduce the number of active roadmap items for [SQUAD] so the PO can focus on fewer, higher-quality stories.

5. **Other:** ___

---

I want to be clear: this is not a complaint about [PO NAME]. POs are often under-resourced, not negligent. The data shows a pipeline gap, and I'd like to work together on a systemic fix.

Happy to discuss. I'll bring the full Starved Sprint Log data.

_[VPoE NAME]_
