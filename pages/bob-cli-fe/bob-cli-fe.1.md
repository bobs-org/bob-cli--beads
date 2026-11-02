# Bead: bob-cli-fe.1 — Pure planners and shared vectors (bob-cli)

[Bead Pages](../README.md) / [bob-cli-fe](README.md) / bob-cli-fe.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.c4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.c4.md) · **Assignee:** `bob-cli-fe.1` · **Size:** medium
**Created:** 2026-11-01 16:00:42 EST · **Closed:** 2026-11-01 17:34:23 EST
**Plan:** [202611/merged\_pomodoros.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/merged_pomodoros.md)

## Description

routing-core: implement R1–R7 as pure Rust planners (land, merge_names, narrow_closed, shed, split_plan, select_by_type) with new shared vector sections and the task-types.md contract.

## Notes

[2026-11-01T22:34:23Z · bob-cli-fe.1] Implemented R1–R7 as pure planners: land (default merge, MEET and retype:true keep Set/Clear), merge_names, narrow_closed, shed, split_plan, select_by_type. Shared vectors renamed retype→land and added merge/split/narrow/shed/select (labels, exempt PLAN, MEET, prefix vs whole-key, literals, two-type implicit split, duplicates, keep-the-base). Callers pass retype:true so capture behavior is unchanged. Verified cargo fmt, project clippy gate, shared_routing_vectors plus 63 pomodoro_themes lib tests, two capture caller CLI tests, and just docs-check. No --epic-symbol leftovers.

## Dependencies

- **Blocks:** [bob-cli-fe.2](bob-cli-fe.2.md) ✓ · ⧖ 2026-11-01
- **Blocks:** [bob-cli-fe.3](bob-cli-fe.3.md) ✓ · ⧖ 2026-11-01
- **Blocks:** [bob-cli-fe.5](bob-cli-fe.5.md) ✓ · ⧖ 2026-11-01
- **Blocks:** [bob-cli-fe.6](bob-cli-fe.6.md) ✓ · ⧖ 2026-11-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-fe.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fe.1/README.md) | [bob-cli-fe.1](bob-cli-fe.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`675330d`](https://github.com/bobs-org/bob-cli/commit/675330dd5e4be39ebe920931b28a01b852bf78d5) | feat(types): add merged-Pomodoro routing planners | [bob-cli-fe.1](bob-cli-fe.1.md) | 2026-11-01 17:35:55 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-fe.1][1] | Need notes, children, and remaining work from earlier agents | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fe.1/README.md

<!-- sase:referenced-by:end -->
