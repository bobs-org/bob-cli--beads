# Bead: bob-cli-pl.9.1.2 — Integrate the Area Card with the landed bank title and setup card

[Bead Pages](../README.md) / [bob-cli-pl.9.1](bob-cli-pl.9.1.md) / bob-cli-pl.9.1.2

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pl.9](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pl.9.md) · **Assignee:** `bob-cli-pl.9.1.2` · **Size:** medium
**Created:** 2026-11-25 19:49:46 EST
**Plan:** [202611/area\_project\_takeover.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/area_project_takeover.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:e85d653a52d90836c21d7b53 | attached via sase artifact create --bead |

_Plus 4 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

bank-arbitration: prove the bank anchor in real Obsidian, implement scope-local title/foot/frontmatter arbitration with the approved fallback ladder, and preserve the bank editor.

## Notes

[2026-11-26T02:35:19Z · bob-cli-pl.9.1.2--1] PROPOSED FOLLOW-UP: Confirmed the task-status-cycler date-boundary defect already proposed in bob-cli-pl.9.1.1 note #1 and bob-cli-pl.7 note #1: the two assertions in scripts/test-task-status-cycler-open-line.cjs expect created::2026-11-25 but produce 2026-11-26 on Nov 26; both fail identically on a clean HEAD archive. No matching task bead was found; stabilize the fixture date.

[2026-11-26T08:26:43Z · bob-cli-pl.9.1.2] RECOVERY PLAN: Audited landed plugin fixes through a0ebe63e (current plugin e82bd932; no later bank/home/editor/runner diff) and latest retained Athena run on CLI 926c9258. Real Obsidian result remains NO-GO: 38/64 passing, duplicate Bank/Area feet in both modes, nested editor timeout, second-pane Area loss, and a Bank wire-kind mismatch in the settings probe. Final passive/screenshot/console checks were unexecuted after a day screenshot timeout. Fresh focused host/frontmatter suites pass 48/48, so they do not establish real acceptance. Retained full raw report/matrix/logs/provenance, prior full-suite logs, checked transfer receipts, and the individually inspected failure PNG as file:explicit:e85d653a52d90836c21d7b53. Following the assigned-phase instruction for repeated unfinished work, authored a four-phase child epic for probe contracts, mount/foot lifecycle, editor routing, and scoped Bank acceptance/deployment; original phase remains in progress for its child land agent. No production source, memory, ancestors, or task beads changed; no epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-pl.9.1.1](bob-cli-pl.9.1.1.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-pl.9.1.3](bob-cli-pl.9.1.3.md) ◐ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pl.9.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pl.9.1.2.md) | [bob-cli-pl.9.1.2](bob-cli-pl.9.1.2.md) | 5 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@06c87a0`](https://github.com/bobs-org/bob-plugins/commit/06c87a0682d66d903017d66be98c02cfb813f379) | fix(plugins): preserve takeover timeout evidence | [bob-cli-pl.9.1.2](bob-cli-pl.9.1.2.md) | 2026-11-25 22:23:59 EST |
| bob-plugins | [`bob-plugins@8e401c6`](https://github.com/bobs-org/bob-plugins/commit/8e401c6ed34d3bc8074be904cfb983fe5d28ec17) | fix(plugins): preserve bank setup alongside area ownership | [bob-cli-pl.9.1.2](bob-cli-pl.9.1.2.md) | 2026-11-25 23:27:08 EST |
| bob-plugins | [`bob-plugins@b185579`](https://github.com/bobs-org/bob-plugins/commit/b185579f35970bceb102d301bdd11b269af54a3b) | fix(plugins): capture bank fallback adapter in widget | [bob-cli-pl.9.1.2](bob-cli-pl.9.1.2.md) | 2026-11-26 01:02:16 EST |
| bob-plugins | [`bob-plugins@5addf8c`](https://github.com/bobs-org/bob-plugins/commit/5addf8ca4b42208f7366757d449ad0d640d94ac7) | fix(plugins): refresh Bank arbitration after Area foot mounts | [bob-cli-pl.9.1.2](bob-cli-pl.9.1.2.md) | 2026-11-26 01:54:13 EST |
| bob-plugins | [`bob-plugins@a0ebe63`](https://github.com/bobs-org/bob-plugins/commit/a0ebe63eca90f814a7503a87ee570836f9876716) | fix(plugins): preserve Area foot registration during Bank arbitration | [bob-cli-pl.9.1.2](bob-cli-pl.9.1.2.md) | 2026-11-26 02:53:44 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pl.9.1.2--4][1] | Review the approved bank area arbitration scope before deciding which Athena failures require source fixes | 1 |
| read-by | [agent:bob-cli-pl.9.1.2--9][1] | Need assigned phase requirements before deciding whether Athena failures are source defects | 1 |
| read-by | [agent:bob-cli-pl.9.1.2--c][1] | Verify the assigned phase scope, previous notes, and recorded follow-ups before completing acceptance and closure | 1 |
| read-by | [agent:bob-cli-pl.9.1.2--e][1] | Verify assigned scope, required acceptance and deployment gates, phase status, and phase-only leftovers before closure decision | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pl.9.1.2.md

<!-- sase:referenced-by:end -->
