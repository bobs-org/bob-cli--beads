# Bead: bob-cli-kx.2 — Archive-on-close machinery in bob-cli

[Bead Pages](../README.md) / [bob-cli-kx](README.md) / bob-cli-kx.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1bt](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1bt.md) · **Assignee:** `bob-cli-kx.2` · **Size:** large
**Created:** 2026-11-12 11:11:53 EST · **Closed:** 2026-11-13 07:51:16 EST
**Plan:** [202611/gmail\_archive\_on\_task\_close.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_archive_on_task_close.md)

## Description

core: Implement the opt-in gmail.sync.archive machinery: closed-task scan including done/, eligibility fold with one-shot journal events, the property-tested label-diff contract, the fenced per-thread batch modify apply with receipt-label crash reconcile, login -s modify, doctor rows, report rows and additive JSON, burst breaker with -c, -n, first-enable backlog confirm, docs rewrites under a feat(gmail)!: subject, the new decision record, and the bob-cli-i4 supersession.

## Notes

[2026-11-13T03:56:46Z · bob-cli-kx.2.1.7] Outer-land note: bob-cli-i4 remains READY; this phase did not touch it. The accepted plan decision bead_i4=close supersedes opt-in unlabel-after-pull because removing bob would erase archive consent; a nested-label scheme remains available for the phone-queue goal. The land agent should close bob-cli-i4 with the plan and nested-label alternative in its resolution note.

[2026-11-13T12:52:46Z · bob-cli-kx.2.1.8.land] CLOSEOUT VERIFICATION: After the final child epic bob-cli-kx.2.1 closed normally, the bead store closed this phase as delegated work landed; no force/status edit was used. The accepted bead_i4 = close decision is now fulfilled: bob-cli-i4 was closed as superseded because removing enrollment would erase live archive consent, with a nested-label phone queue retained as the alternative. Scope verification: all archive core phases and the repair child are closed; no phase symbols remain. The containing epic bob-cli-kx remains open, with bob-cli-kx.3 still in progress. Verification: 65,536 label-diff property cases, 184 Gmail integration tests, docs-gen, docs-check lint/generated/build/URL stages; just check reports only bob-cli-l2 and bob-cli-kl, and exact kl rerun passed. The known bob-cli-l7 offline link remains at docs-check lychee.

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
| read-by | [agent:bob-cli-kx.2.1.8.3][5] | Need the reviewed archive behavior decisions carried into this epic | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.2.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.2.1.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.2.1.6/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.2.1.7/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.2.1.8.3/README.md

<!-- sase:referenced-by:end -->
