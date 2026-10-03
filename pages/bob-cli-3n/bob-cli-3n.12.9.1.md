# Bead: bob-cli-3n.12.9.1 — Reading-view chips, recogniser alignment, and the DP29/DP30 contract

[Bead Pages](../README.md) / [bob-cli-3n.12.9](bob-cli-3n.12.9.md) / bob-cli-3n.12.9.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-3n.12.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-3n.12.land.md) · **Assignee:** `bob-cli-3n.12.9.1` · **Size:** medium
**Created:** 2026-10-03 01:27:48 EDT · **Closed:** 2026-10-03 01:53:21 EDT
**Plan:** [202610/task\_dep\_links\_landing\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_dep_links_landing_fixes.md)

## Description

chips-reading-align: settle DP29 (blockquote is not-a-line everywhere) and add DP30 in the contract and Rust DP test, give Reading view the owning-line rules and a section-derived line, make cycler/bip agree with every DP vector, stop full-document copies in Live Preview, cache the lookup index through freshnessEnsureMemo, and make the vacuous chip tests real.

## Notes

[2026-10-03T05:53:08Z · bob-cli-3n.12.9.1] PROPOSED FOLLOW-UP: note_ready::scan_excludes_r3_and_r7_paths fails intermittently under parallel cargo test (saw 2-vs-1 count once), passes in isolation and on full rerun — parallel flake distinct from the capture_pomodoros flake tracked by bob-cli-2e

[2026-10-03T05:53:21Z · bob-cli-3n.12.9.1] DP29 not-a-line everywhere + DP30 accept(1) pinned in contract and Rust DP24-DP30 rows; Reading owns rows/blockquotes/WorkLog/malformed gated with section-derived unique-or-hidden action lines and hidden emoji; Live Preview walks ancestors with doc.line (no full copy); lookup index on freshnessEnsureMemo; cycler guards all malformed, bip isMalformed excludes DP24, full DP1-DP30 tables + cycler reopen test; vacuous chip tests made real (all fail pre-fix). Verified: cargo fmt/clippy/test green (one parallel flake, passes isolation+rerun, filed as follow-up), npm test 1338/1338, validate 6/6, 3 plugins deployed.

## Dependencies

- **Blocks:** [bob-cli-3n.12.9.5](bob-cli-3n.12.9.5.md) ✓ · ⧖ 2026-10-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-3n.12.9.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3n.12.9.1/README.md) | [bob-cli-3n.12.9.1](bob-cli-3n.12.9.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`eb9d846`](https://github.com/bobs-org/bob-cli/commit/eb9d846b765f0c1172038ba147771a0d0e580836) | feat(task-deps): pin DP29 not-a-line, DP30 accept(1), cover DP24-DP30 vectors | [bob-cli-3n.12.9.1](bob-cli-3n.12.9.1.md) | 2026-10-03 01:54:55 EDT |
