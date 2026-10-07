# Bead: bob-cli-4w.1 — Promote bob ref to the canonical command

[Bead Pages](../README.md) / [bob-cli-4w](README.md) / bob-cli-4w.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.3s.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.3s.linker.w0.md) · **Assignee:** `bob-cli-4w.1` · **Size:** medium
**Created:** 2026-10-06 20:15:52 EDT · **Closed:** 2026-10-06 21:03:36 EDT
**Plan:** [202610/bob\_ref\_reference\_library.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_ref_reference_library.md)

## Description

rename: make `ref` the canonical Vault command with permanent `highlights` and `highlights-ref` aliases, grouped help, canonical diagnostics, completion paths, fixtures, docs, and alias-equivalence tests.

## Notes

[2026-10-07T00:49:07Z · bob-cli-4w.1] PROPOSED FOLLOW-UP: lib test every_value_arg_has_a_decision still reports no kinds decision for create:audio (now ref create:audio); identical on clean base, known per epic plan as the bob-cli-4j failure

[2026-10-07T00:49:12Z · bob-cli-4w.1] PROPOSED FOLLOW-UP: lib test listen_filter_renders_card_and_encoded_play_link fails identically on the clean base tree (no tracker known); unrelated to the ref rename

[2026-10-07T01:03:36Z · bob-cli-4w.1] Closed by explicit `sase stitch create -B close` after create_commit landed 42a1792 ("feat(ref): promote bob ref to the canonical command"). The commit author requested bead completion after verifying the bead scope. Reopen with `sase bead open bob-cli-4w.1` if more work remains.

## Dependencies

- **Blocks:** [bob-cli-4w.4](bob-cli-4w.4.md) ◐ · ⧖ 2026-10-06
- **Blocks:** [bob-cli-4w.7](bob-cli-4w.7.md) ✓ · ⧖ 2026-10-06
- **Blocks:** [bob-cli-4w.8](bob-cli-4w.8.md) ✓ · ⧖ 2026-10-06
- **Blocks:** [bob-cli-4w.9](bob-cli-4w.9.md) ✓ · ⧖ 2026-10-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-4w.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-4w.1/README.md) | [bob-cli-4w.1](bob-cli-4w.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`42a1792`](https://github.com/bobs-org/bob-cli/commit/42a17926a9ce700634a2ed2ce51228ef4f46e0fd) | feat(ref): promote bob ref to the canonical command | [bob-cli-4w.1](bob-cli-4w.1.md) | 2026-10-06 21:02:53 EDT |
