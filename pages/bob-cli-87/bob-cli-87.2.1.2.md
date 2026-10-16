# Bead: bob-cli-87.2.1.2 — Snapshot classification and cached vault resolution

[Bead Pages](../README.md) / [bob-cli-87.2.1](bob-cli-87.2.1.md) / bob-cli-87.2.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-87.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-87.2.md) · **Assignee:** `bob-cli-87.2.1.2` · **Size:** medium
**Created:** 2026-10-16 07:26:12 EDT · **Closed:** 2026-10-16 08:53:15 EDT
**Plan:** [202610/snapshot\_view\_core.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/snapshot_view_core.md)

## Description

resolution: implement vault membership and target classification, cached source reads, note and attachment resolution, fragment indexes, and the shared Obsidian URI builder. Preserve existing audio URI behavior while extracting its helper.

## Notes

[2026-10-16T12:53:15Z · bob-cli-87.2.1.2] Resolution phase implemented and verified: classify.rs (SourceStore one-read-per-source cache incl. errors, vault membership with dot/_conflicts/xlib/lib/lit_review/shared exclusions, symlink-escape rejection, frontmatter kinds ordinary/area/project/terminal-project, typed missing/ambiguous errors, deferred default-parent) and resolve.rs (VaultNotes note resolution, FragmentIndex heading-through-shallower/list-subtree/paragraph extents skipping frontmatter/code/comments, AttachmentIndex exact/note-dir/basename precedence with dedup asset naming, shared obsidian:// percent-encode/template helpers, 640px print measure with 400px->62pct). create.rs audio URI refactored onto the shared helpers with behavior preserved (existing audio encode/precedence tests pass; snapshot URI asserted byte-identical to the audio Play-URI shape). vault_links gained only candidates/near_stems/basename_candidates/known_stems plus private levenshtein; existing resolver semantics untouched. Tests: 20 new focused tests (9 classify incl. read-once Arc sharing, 11 resolve incl. lazy-index caching), all synthetic temp vaults. just check green: fmt, clippy -D unused -D private_interfaces, 2666 lib tests + all integration suites pass. No --epic-symbol entries.

## Dependencies

- **Depends on:** [bob-cli-87.2.1.1](bob-cli-87.2.1.1.md) ✓ · ⧖ 2026-10-16
- **Blocks:** [bob-cli-87.2.1.3](bob-cli-87.2.1.3.md) ◐ · ⧖ 2026-10-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-87.2.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-87.2.1.2/README.md) | [bob-cli-87.2.1.2](bob-cli-87.2.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`29f5f4e`](https://github.com/bobs-org/bob-cli/commit/29f5f4efa0bf32f7a86fbbbce778845fed7864fa) | feat(snapshot): add classification and cached vault resolution | [bob-cli-87.2.1.2](bob-cli-87.2.1.2.md) | 2026-10-16 08:54:31 EDT |
