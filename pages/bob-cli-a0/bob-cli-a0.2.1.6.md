# Bead: bob-cli-a0.2.1.6 — Wire search and prove the complete docs gate

[Bead Pages](../README.md) / [bob-cli-a0.2.1](bob-cli-a0.2.1.md) / bob-cli-a0.2.1.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-a0.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.2.md) · **Assignee:** `bob-cli-a0.2.1.6` · **Size:** medium
**Created:** 2026-10-19 19:05:38 EDT · **Closed:** 2026-10-19 20:37:13 EDT
**Plan:** [202610/docs\_toolchain.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/docs_toolchain.md)

## Description

integration: add search smoke, compose docs-check including production mode, prove strict and fallback builds and injected-failure diagnostics, and leave complete evidence for the land agent.

## Notes

[2026-10-20T00:37:02Z · bob-cli-a0.2.1.6] Integration complete. Added bob-docs check and themed just docs-check, with one assembled source context threaded through lint, strict build, URLs, lychee, and search smoke; production --sources is forwarded once. Added the two required search cases and tests for Zensical docs and items index formats, malformed/empty/missing indexes, location boundaries, punctuation, gate order, production context reuse, and generated drift. Verification: just docs-check passed all gates and 121 tests; just docs-build-material passed. Versions: Python 3.12.13, bob-docs 0.1.0, Zensical 0.0.71, Material 9.7.7, MkDocs 1.6.1, lychee 0.24.2. Evidence: 27 contracts, 32 published pages, 352 URL mentions; live /urls.txt returned first-publish 404 warning. Injected ../missing-injected-doc.md failed strict build with vault-git-sync.md:370:26 and target; injected #missing-injected-anchor failed URLs with source line and target. Production fixture tests pass clean SHA and reject dirty, wrong SHA, missing entry, env override, and wrong bob-cli path. Follow-on CLI golden, tutorial, media gates print explicit not-implemented skips. git diff --check passed; no generated tracked drift; just check recipe remains unchanged and no Rust files changed.

[2026-10-20T00:37:13Z · bob-cli-a0.2.1.6] Verified just docs-check and 121 docs tests, strict Zensical and Material builds, search smoke, production fixture behavior, generated drift, and precise injected-link failure diagnostics; just check remains unchanged.

## Dependencies

- **Depends on:** [bob-cli-a0.2.1.3](bob-cli-a0.2.1.3.md) ✓ · ⧖ 2026-10-19
- **Depends on:** [bob-cli-a0.2.1.4](bob-cli-a0.2.1.4.md) ✓ · ⧖ 2026-10-19
- **Depends on:** [bob-cli-a0.2.1.5](bob-cli-a0.2.1.5.md) ✓ · ⧖ 2026-10-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-a0.2.1.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.2.1.6/README.md) | [bob-cli-a0.2.1.6](bob-cli-a0.2.1.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`cb42d65`](https://github.com/bobs-org/bob-cli/commit/cb42d654f9760641dbd1fce07c12c18567ae8f09) | feat(docs): wire complete documentation gate | [bob-cli-a0.2.1.6](bob-cli-a0.2.1.6.md) | 2026-10-19 20:38:11 EDT |
