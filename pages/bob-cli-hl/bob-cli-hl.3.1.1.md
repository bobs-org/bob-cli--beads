# Bead: bob-cli-hl.3.1.1 — Share explicit merge planning and track capture-born targets

[Bead Pages](../README.md) / [bob-cli-hl.3.1](bob-cli-hl.3.1.md) / bob-cli-hl.3.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-hl.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hl.3.md) · **Assignee:** `bob-cli-hl.3.1.1` · **Size:** medium
**Created:** 2026-11-05 19:49:42 EST · **Closed:** 2026-11-05 20:36:16 EST
**Plan:** [202611/capture\_merge\_in\_execution.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_merge_in_execution.md)

## Description

adapter: extract the > explicit-merge adapter unchanged, share source validation and task refs, and report target.created from capture-wide task birth identity. Keep the < execution refusal until the execute phase.

## Notes

[2026-11-06T01:35:14Z · bob-cli-hl.3.1.1--2] PROPOSED FOLLOW-UP: Remove or use the stale TODAY constant blocking just check — reproduced with clean-base command `sh target/verify-clean-base-bob-cli-hl-3-1-1.sh` at base `8eecf0c4ba01712cb8a7807439c622c484f17630`: `error: constant TODAY is never used` at `tests/cli/capture/merge_in.rs:8:7` (`const TODAY: &str = "2026-11-05";`); `-D dead-code` is implied by `-D unused`, so just check exits 101.

[2026-11-06T01:36:16Z · bob-cli-hl.3.1.1--2] Completed the adapter extraction and capture-wide task birth tracking. Verified all 26 transfer tests and all 3 relation-merge tests pass, including created-target, ID-assigned existing target, moved existing target, and relation-merge regressions; just docs-check passes. just check exits 101 on the clean base commit 8eecf0c4 because TODAY is unused at tests/cli/capture/merge_in.rs:8; recorded as a proposed follow-up. epic-symbols reports no remaining entries.

## Dependencies

- **Blocks:** [bob-cli-hl.3.1.2](bob-cli-hl.3.1.2.md) ✓ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-hl.3.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hl.3.1.1.md) | [bob-cli-hl.3.1.1](bob-cli-hl.3.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`4282e71`](https://github.com/bobs-org/bob-cli/commit/4282e71222c8fcaaf76d158e7cbaa01cd0708ea7) | refactor(capture): share merge planning and track task births | [bob-cli-hl.3.1.1](bob-cli-hl.3.1.1.md) | 2026-11-05 20:37:36 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hl.3.1.1--2][1] | Confirm the phase close event and recorded verification | 4 |
| read-by | [agent:bob-cli-hl.3.1.2][2] | Check prior phase evidence | 1 |
| read-by | [agent:bob-cli-hl.3.1.land][3] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hl.3.1.1.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hl.3.1.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hl.3.1.land/README.md

<!-- sase:referenced-by:end -->
