# Bead: bob-cli-3n.12.7 — Correct the decision record and sweep stale dependency docs

[Bead Pages](../README.md) / [bob-cli-3n.12](bob-cli-3n.12.md) / bob-cli-3n.12.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-3n.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-3n.land.md) · **Assignee:** `bob-cli-3n.12.7` · **Size:** small
**Created:** 2026-10-02 23:24:09 EDT · **Closed:** 2026-10-03 01:00:45 EDT
**Plan:** [202610/task\_dep\_links\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_dep_links_fixes.md)

## Description

docs-memory-fix: add the missing rejected alternative, decided date, and plugin evidence to the decision record; fix stale docs/projects.md, freshness.md, capture.md, and today.rs wording; settle the DC7/DC8 and archive-link contract gaps.

## Notes

[2026-10-03T05:00:28Z · bob-cli-3n.12.7] PROPOSED FOLLOW-UP: capture_pomodoros missing_note_and_missing_section_are_warning_successes still flakes under parallel cargo test (passes in isolation); tracked by bead bob-cli-2e, do not fix here

[2026-10-03T05:00:45Z · bob-cli-3n.12.7] docs-memory-fix done. Decision record: added 8th rejected alternative ('!' as gesture), decided 2026-10-02, Evidence += bob-plugins 1831db4/e7baeb5/5194bc8/08d1560/82aec34/46ddd1e, vault 66c6d47c, epic fixes (bob-cli 8d54b0e/b61727a/a069239/79e39af, bob-plugins 3ffa187/330fc58/f78ffad/40e2e3a); sase memory init --check clean. Docs: projects.md Depends-On example + derived-field wording, freshness.md '!' pure-toggle + Depends on row name, capture.md recursive-close skips Depends-On lines, today.rs Depends-On comment. Contract: DC7/DC8 never block/never count (R4/R5 win), archive links keep explicit done/ path form (S3+S4.3). Code: ledger-tools waiting count excludes broken/not-task (1.20.0), nav canonicalDependencyLink keeps done/ form (1.59.0); both deployed (vault shows 1.20.0/1.59.0). Verified: cargo fmt/clippy clean, lib 1560 pass + all integration targets pass except known parallel flake capture_pomodoros (passes isolated, tracked bob-cli-2e, follow-up noted); npm test 1331/1331; validate 6/6.

## Dependencies

- **Depends on:** [bob-cli-3n.12.2](bob-cli-3n.12.2.md) ✓ · ⧖ 2026-10-02
- **Depends on:** [bob-cli-3n.12.3](bob-cli-3n.12.3.md) ✓ · ⧖ 2026-10-02
- **Depends on:** [bob-cli-3n.12.6](bob-cli-3n.12.6.md) ✓ · ⧖ 2026-10-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-3n.12.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3n.12.7/README.md) | [bob-cli-3n.12.7](bob-cli-3n.12.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`3b04a06`](https://github.com/bobs-org/bob-cli/commit/3b04a06559b7cd7c2402b3e793765bf73c4273a6) | docs(deps): correct decision record and sweep stale dependency docs | [bob-cli-3n.12.7](bob-cli-3n.12.7.md) | 2026-10-03 01:02:05 EDT |
