# Bead: bob-cli-k3.3 — Shared host-catalog region engine extracted from notebooks

[Bead Pages](../README.md) / [bob-cli-k3](README.md) / bob-cli-k3.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.43.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.43.linker.w0.md) · **Assignee:** `bob-cli-k3.3` · **Size:** medium
**Created:** 2026-11-11 04:56:43 EST · **Closed:** 2026-11-11 05:36:57 EST
**Plan:** [202611/album\_and\_record\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/album_and_record_notes.md)

## Description

catalog-engine: extract the notebook catalog's owned-callout region, host planning, and guarded sync transaction into a shared engine parameterized by callout name, heading, head title, and placement, keeping every notebook byte and test identical, so the albums catalog and records index reuse it.

## Notes

[2026-11-11T10:36:57Z · bob-cli-k3.3] Extracted notebooks owned-callout region, host planning, and guarded sync txn into src/native/host_catalog parameterized by RegionSpec (callout, heading, head title, BeforeFirstTasks/AfterSectionThenTasks/BeforeFirstH2, optional legacy markers). Notebooks wrappers keep original tests; 18 host_catalog unit, 53 notebooks unit, 32 notebooks CLI tests, and just lint passed. No --epic-symbol leftovers.

## Dependencies

- **Blocks:** [bob-cli-k3.5](bob-cli-k3.5.md) ◐ · ⧖ 2026-11-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-k3.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-k3.3.md) | [bob-cli-k3.3](bob-cli-k3.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d0ada55`](https://github.com/bobs-org/bob-cli/commit/d0ada555a8b60c74933f9ce4eb3aa8c0469b0d64) | refactor(notebooks): extract shared host-catalog region engine | [bob-cli-k3.3](bob-cli-k3.3.md) | 2026-11-11 06:03:48 EST |
