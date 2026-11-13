# Bead: bob-cli-kx.2 — Archive-on-close machinery in bob-cli

[Bead Pages](../README.md) / [bob-cli-kx](README.md) / bob-cli-kx.2

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1bt](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1bt.md) · **Assignee:** `bob-cli-kx.2` · **Size:** large
**Created:** 2026-11-12 11:11:53 EST
**Plan:** [202611/gmail\_archive\_on\_task\_close.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_archive_on_task_close.md)

## Description

core: Implement the opt-in gmail.sync.archive machinery: closed-task scan including done/, eligibility fold with one-shot journal events, the property-tested label-diff contract, the fenced per-thread batch modify apply with receipt-label crash reconcile, login -s modify, doctor rows, report rows and additive JSON, burst breaker with -c, -n, first-enable backlog confirm, docs rewrites under a feat(gmail)!: subject, the new decision record, and the bob-cli-i4 supersession.

## Notes

[2026-11-13T03:56:46Z · bob-cli-kx.2.1.7] Outer-land note: bob-cli-i4 remains READY; this phase did not touch it. The accepted plan decision bead_i4=close supersedes opt-in unlabel-after-pull because removing bob would erase archive consent; a nested-label scheme remains available for the phone-queue goal. The land agent should close bob-cli-i4 with the plan and nested-label alternative in its resolution note.

## Dependencies

- **Depends on:** [bob-cli-kx.1](bob-cli-kx.1.md) ✓ · ⧖ 2026-11-12
- **Blocks:** [bob-cli-kx.3](bob-cli-kx.3.md) ◐ · ⧖ 2026-11-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kx.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kx.2.md) | [bob-cli-kx.2](bob-cli-kx.2.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kx.2.1.1][1] | Need binding parent decisions and any earlier phase notes before implementing access | 1 |
| read-by | [agent:bob-cli-kx.2.1.2][2] | need assigned phase and binding decisions | 1 |
| read-by | [agent:bob-cli-kx.2.1.6][3] | Need parent decisions binding this phase | 1 |
| read-by | [agent:bob-cli-kx.2.1.7][4] | Record the phase completion and the approved outer-epic supersession evidence on the parent epic | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.2.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.2.1.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.2.1.6/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.2.1.7/README.md

<!-- sase:referenced-by:end -->
