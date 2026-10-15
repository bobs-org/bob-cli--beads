# Bead: bob-cli-7x.1 — Stop minting opaque URL stems

[Bead Pages](../README.md) / [bob-cli-7x](README.md) / bob-cli-7x.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.1k.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.1k.linker.w0.md) · **Assignee:** `bob-cli-7x.1` · **Size:** small
**Created:** 2026-10-15 15:25:59 EDT · **Closed:** 2026-10-15 15:31:15 EDT
**Plan:** [202610/bob\_ref\_rename.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_ref_rename.md)

## Description

namer: in bob-cli, make stem_from_url return None when the last non-skipped segment is opaque (hex ID or UUID) and strip trailing opaque words, sharing collection_name's is_hex_id_word; strip a trailing .md/.txt from titles before title-derived stems; unit tests and docs.

## Notes

[2026-10-15T19:31:15Z · bob-cli-7x.1] Shared collection_name's hex-ID predicate with URL stem derivation; opaque final hex/UUID path segments now yield no URL stem, trailing opaque words are removed, and .md/.txt title suffixes are stripped before title stems. Added unit cases and docs. Verified: cargo test stem_ (11 unit tests and 6 CLI tests passed), cargo fmt, git diff --check; sase bead epic-symbols reported no leftovers.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-7x.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-7x.1/README.md) | [bob-cli-7x.1](bob-cli-7x.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`04905b3`](https://github.com/bobs-org/bob-cli/commit/04905b3999eaf0fb347cf3126fae645bbb356908) | fix(refs): avoid opaque URL stems | [bob-cli-7x.1](bob-cli-7x.1.md) | 2026-10-15 15:32:03 EDT |
