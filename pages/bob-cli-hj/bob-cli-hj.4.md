# Bead: bob-cli-hj.4 — Segment picker, dash-to-tilde rewrite, and submit guards

[Bead Pages](../README.md) / [bob-cli-hj](README.md) / bob-cli-hj.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.18s](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.18s.md) · **Assignee:** `bob-cli-hj.4` · **Size:** medium
**Created:** 2026-11-05 14:25:24 EST · **Closed:** 2026-11-05 18:49:12 EST
**Plan:** [202611/past\_pomodoro\_segment\_suffix.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/past_pomodoro_segment_suffix.md)

## Description

assists: add the pomodoro_past_segment completion context and candidates (plus zsh), the - to ~ arm of capture-rewrite, the hidden --expect-past-windows stale-preview guard, and the shell-expanded-tilde refusal, with docs and help.

## Notes

[2026-11-05T23:49:00Z · bob-cli-hj.4] PROPOSED FOLLOW-UP: Full workspace lib suite has 2 pre-existing failures unrelated to assists: native::catalog::tests::public_leaves_are_entries_or_excluded (clipboard path in both lists) and native::completion::kinds duplicate clipboard:count table entry (lines 96/540 in kinds.rs, present in HEAD). Our change fixed the third failure (added capture:expect-past-windows kinds entry). No existing task bead found for these two.

[2026-11-05T23:49:12Z · bob-cli-hj.4] Assists land: pomodoro_past_segment completion field/candidates (tail/~1..N/head, filters, zsh labels), capture-complete help, - to ~ rewrite arm (7 swaps, 8 non-swaps), hidden --expect-past-windows guard (match/mismatch/count/malformed, code pomodoro_past_windows_changed), shell-expanded-tilde guard (code shell_expanded_tilde, argv only), docs (capture.md picker/typing, json-outputs, generated cli ref), kinds entry. Verified: 6 lib + 11 CLI pomodoro_past_segment tests pass, just fmt/lint/docs-check green; full workspace has 2 pre-existing failures recorded as follow-up.

## Dependencies

- **Depends on:** [bob-cli-hj.3](bob-cli-hj.3.md) ✓ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-hj.6](bob-cli-hj.6.md) ◐ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-hj.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hj.4/README.md) | [bob-cli-hj.4](bob-cli-hj.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`35c2a42`](https://github.com/bobs-org/bob-cli/commit/35c2a426c3411a91e7825c64adf1121fe013e9ac) | feat(capture): add past-Pomodoro segment picker, dash rewrite, and submit guards | [bob-cli-hj.4](bob-cli-hj.4.md) | 2026-11-05 18:50:38 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hg.3.1.3][1] | Confirm whether the clean-base clipboard catalog test failures are already tracked | 1 |
| read-by | [agent:bob-cli-hj.4][2] | Need phase scope | 3 |
| read-by | [agent:bob-cli-hn.2][3] | Confirm the clean-base duplicate clipboard failures already have a tracker | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hg.3.1.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hj.4/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hn.2/README.md

<!-- sase:referenced-by:end -->
