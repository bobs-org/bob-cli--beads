# Bead: bob-cli-gj.2.1.2 — Note-pull batch identity and transaction semantics

[Bead Pages](../README.md) / [bob-cli-gj.2.1](bob-cli-gj.2.1.md) / bob-cli-gj.2.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-gj.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-gj.2.md) · **Assignee:** `bob-cli-gj.2.1.2` · **Size:** medium
**Created:** 2026-11-03 12:31:13 EST · **Closed:** 2026-11-03 14:53:14 EST
**Plan:** [202611/note\_pull\_cli.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/note_pull_cli.md)

## Description

batch: implement section 5, including stable pre-pick keys, earliest-item ownership, draft numbering, same-draft creation provenance, per-row net filtering, inbox routing, and transaction rollback. Cover NP13–NP20 and adversarial mixed drafts without changing existing successor-group behavior.

## Notes

[2026-11-03T19:53:10Z · bob-cli-gj.2.1.2] PROPOSED FOLLOW-UP: Project clippy gate shows 8 pre-existing nonminimal-bool errors in unrelated files plus many result_large_err warnings under -D warnings; none in batch note-pull files — verify on clean base with just lint

[2026-11-03T19:53:14Z · bob-cli-gj.2.1.2] Batch identity and transaction semantics done: earliest-item ownership across all groups with post-mint block-ID dedup, (item,0) order-key precedence for NP20 reverse-lexical, same-draft creation no-stamp via draft-start preimage, settled ordinals with line-shift-safe lookup, SL20 per-row net filtering plus refresh, inbox Ready-candidate routing, atomic rollback. Tests: 32 lib note-pull pass (NP1-NP21 incl new NP13,14,16-20, duplicate ~2, repeated-pull prune, rollback), 521 capture_language pass, 1527 capture lib pass, fmt clean, epic-symbols empty.

## Dependencies

- **Depends on:** [bob-cli-gj.2.1.1](bob-cli-gj.2.1.1.md) ✓ · ⧖ 2026-11-03
- **Blocks:** [bob-cli-gj.2.1.3](bob-cli-gj.2.1.3.md) ◐ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-gj.2.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-gj.2.1.2/README.md) | [bob-cli-gj.2.1.2](bob-cli-gj.2.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a95d5d8`](https://github.com/bobs-org/bob-cli/commit/a95d5d8f0268c9f30cf7d2ff87d1145aca519a9f) | feat(capture): batch note-pull planning with ownership and ordering | [bob-cli-gj.2.1.2](bob-cli-gj.2.1.2.md) | 2026-11-03 14:54:57 EST |
