# Bead: bob-cli-db.1 — \`bob themes split\` and the reappearance fix

[Bead Pages](../README.md) / [bob-cli-db](README.md) / bob-cli-db.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.ar.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.ar.w0.md) · **Assignee:** `bob-cli-db.1` · **Size:** medium
**Created:** 2026-10-27 17:11:11 EDT · **Closed:** 2026-10-27 17:47:14 EDT
**Plan:** [202610/write\_theme\_and\_job\_split.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/write_theme_and_job_split.md)

## Description

split_cmd: add the template and map-driven per-entry theme split on the shared vault-rewrite transaction, and stop renamed_reappeared from reporting re-adopted names, with tests and docs.

## Notes

[2026-10-27T21:46:58Z · bob-cli-db.1] PROPOSED FOLLOW-UP: relation-label renamed_reappeared has the same rename-cycle false positive as themes — apply the re-adoption skip (later rename-to / color / unhide; hide does not re-adopt) in src/native/relation_labels/rename.rs

[2026-10-27T21:47:14Z · bob-cli-db.1] Added bob themes split (template TSV and map rewrite on vault_rewrite, no journal event) and skipped renamed_reappeared when a later rename-to/color/unhide re-adopts the key. Verified: cargo test --lib split_tests (4); cargo test --test cli themes (35, including split + reappearance); cargo test --test cli help (83); cargo fmt --check; clippy --all-targets --all-features with justfile rustc/clippy gates; just docs-gen; just docs-check; bob themes split --help. Cargo.toml version and CHANGELOG.md untouched. Recorded PROPOSED FOLLOW-UP for relation-label renamed_reappeared sibling. epic-symbols empty.

## Dependencies

- **Blocks:** [bob-cli-db.2](bob-cli-db.2.md) ◐ · ⧖ 2026-10-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-db.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-db.1/README.md) | [bob-cli-db.1](bob-cli-db.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a6a359b`](https://github.com/bobs-org/bob-cli/commit/a6a359b8c62c318cb82a98286cdfc72cd35c47c8) | feat(themes): add per-entry split and skip re-adopted rename reports | [bob-cli-db.1](bob-cli-db.1.md) | 2026-10-27 17:48:27 EDT |
