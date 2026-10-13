# Bead: bob-cli-78.1 — Sub-project cascade contract and vectors

[Bead Pages](../README.md) / [bob-cli-78](README.md) / bob-cli-78.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.71](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.71.md) · **Assignee:** `bob-cli-78.1` · **Size:** small
**Created:** 2026-10-13 03:14:27 EDT · **Closed:** 2026-10-13 03:24:00 EDT
**Plan:** [202610/subproject\_cascade.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/subproject_cascade.md)

## Description

contract: rewrite §13's residence-only rule into the cascade (parent, ancestors, inherited reasons, ^prj tag, descendant-internal targets), add §12.10 trigger (c) and a real step 3, and add the PDS, PDG, PDC and PP vectors plus doc pointers.

## Notes

[2026-10-13T07:18:54Z · bob-cli-78.1] PROPOSED FOLLOW-UP: update glossary:project-task to say sub-projects inherit their ancestors blocking (memory_glossary=no skipped it).

[2026-10-13T07:23:51Z · bob-cli-78.1] PROPOSED FOLLOW-UP: just check CLI failures capture::r#ref::percent_listen_reference_runs_existing_worker_and_installs_audio and failed_percent_listen_worker_keeps_listen_retry_guidance match the known bob-cli-6m percent-listen failures (listen worker binary missing in this env); docs-only change cannot affect them.

[2026-10-13T07:24:00Z · bob-cli-78.1] Docs-only cascade contract landed: §13 rewritten (parent/ancestors/descendants/inherited, tag ⇔ inherited, ancestor edges, descendant-internal targets, tag proxy, Task Card subtree pass, defer list), §13.19 PDS1–PDS15 added, PDB5 flipped, PDT6 amended, PDT13/PDG8–17/PDC4–6 added (PDC6 as reconcile-interval under close_recovers_subprojects=no; PDG12 cascades under schedule_cascade=yes), §12.10 trigger (c) + real step 3 + row-text rule + PP29–PP36, pointers in projects.md/task-status-hooks.md/README.md, stale no-cascade sentences fixed. just check: only the 2 known bob-cli-6m percent-listen failures; no epic-symbol entries. Coordination note left on bob-cli-75; glossary skip + check failures recorded as PROPOSED FOLLOW-UP notes.

## Dependencies

- **Blocks:** [bob-cli-78.2](bob-cli-78.2.md) ✓ · ⧖ 2026-10-13
- **Blocks:** [bob-cli-78.5](bob-cli-78.5.md) ✓ · ⧖ 2026-10-13
- **Blocks:** [bob-cli-78.7](bob-cli-78.7.md) ✓ · ⧖ 2026-10-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-78.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-78.1/README.md) | [bob-cli-78.1](bob-cli-78.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a2e92bc`](https://github.com/bobs-org/bob-cli/commit/a2e92bcb8f11c9a0d209bfa5d5afb65d13595375) | docs(tasks): cascade contract for parent/ancestors/descendants | [bob-cli-78.1](bob-cli-78.1.md) | 2026-10-13 03:25:05 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-78.1][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-78.1/README.md

<!-- sase:referenced-by:end -->
