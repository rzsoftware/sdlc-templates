# Partial Definition Override

> **When:** Any time leadership requests a story enter the sprint without passing DoR
> **From:** Squad Lead
> **To:** Override requestor
> **cc:** VPoE, PO
> **Channel:** Email + Jira comment on the story
> **Time to fill out:** ~10 minutes
> **Feeds into:** [Quarterly Override Review](../vpoe/quarterly-override-review.md)

---

**Subject:** Partial Definition Override — [JIRA-KEY] — Sprint [SPRINT #]

---

## Jira Setup

_Before filling this out, ensure the story has these fields set in Jira (see [Jira Setup Playbook](https://rzsoftware.github.io/sdlc/metrics/#jira-setup)):_

- [ ] Label `partial-definition-override` applied
- [ ] `Original Estimate` field set (points at time of override)
- [ ] `Override Requestor` field set (the person requesting the override)
- [ ] `Override Risk Estimate` field set (risk-adjusted points)

## Override Record

| Field | Value |
|-------|-------|
| **Story** | [JIRA-KEY] — [TITLE] |
| **Sprint** | [SPRINT #] |
| **Override requested by** | [NAME, TITLE] |
| **Date requested** | [DATE] |
| **Squad** | [SQUAD NAME] |
| **Squad Lead** | [YOUR NAME] |

## DoR Criteria Assessment

Check all criteria. Mark PASS or FAIL for each.

| # | DoR Criterion | Status | Gap Description (if FAIL) |
|---|--------------|--------|--------------------------|
| 1 | Acceptance criteria defined and testable | PASS / **FAIL** | ___ |
| 2 | Technical design reviewed and approved | PASS / **FAIL** | ___ |
| 3 | Dependencies identified and resolved | PASS / **FAIL** | ___ |
| 4 | Story pointed by the team | PASS / **FAIL** | ___ |
| 5 | UX/UI designs finalized (if applicable) | PASS / **FAIL** | ___ |
| 6 | Test strategy defined | PASS / **FAIL** | ___ |
| 7 | No open blockers | PASS / **FAIL** | ___ |

## Risk Assessment

| Risk | Assessment |
|------|-----------|
| **Original estimate** | ___ points (set in Jira `Original Estimate` field) |
| **Risk-adjusted estimate** | ___ points (set in Jira `Override Risk Estimate` field) |
| **Rework likelihood** | High / Medium / Low — ___ |
| **Scope change likelihood** | High / Medium / Low — ___ |
| **Carry-over likelihood** | High / Medium / Low — ___ |
| **Impact on other sprint work** | ___ |

## What Will Likely Happen

_In plain language, describe what the squad expects if this story enters the sprint without full definition. Be specific._

Example: "Without finalized AC, engineers will need to make assumptions about [X]. When the PO clarifies mid-sprint, rework is likely on [Y]. This will probably push the story from 5 points to 8-10 points and may cause [OTHER STORY] to carry over."

**Your assessment:** ___

## Requestor Acknowledgment

> I am requesting this story enter the sprint without meeting the Definition of Ready. I understand this increases the risk of rework, scope change, and carry-over. Engineering's original estimate may not hold. The outcome of this override will be tracked and reported in the Quarterly Override Review.

**Acknowledged by:** ___________________ **Date:** ___________

---

## After Sprint Close (Squad Lead completes this section)

_Jira Automation Rule 3 will prompt you when the story hits Done. Compare `Story Points` (final) to `Original Estimate` (baseline) in Jira._

| Outcome | Value |
|---------|-------|
| **Final points spent** | ___ (original estimate was ___) |
| **Scope changed mid-sprint?** | Yes / No — ___ |
| **Rework required?** | Yes / No — if yes, apply `rework` label in Jira |
| **Carried over?** | Yes / No — if yes, `carried-over` label applied automatically |
| **Impact on other stories** | ___ |

---

_Jira label applied: `partial-definition-override`_

_This override is tracked in the [Quarterly Override Review](../vpoe/quarterly-override-review.md). Jira [VPoE Dashboard](https://rzsoftware.github.io/sdlc/metrics/#dashboard-vpoe) shows all overrides automatically._
