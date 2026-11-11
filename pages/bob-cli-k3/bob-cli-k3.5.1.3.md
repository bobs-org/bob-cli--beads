# Bead: bob-cli-k3.5.1.3 — Repair indexes through albums sync and nightly

[Bead Pages](../README.md) / [bob-cli-k3.5.1](bob-cli-k3.5.1.md) / bob-cli-k3.5.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-k3.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-k3.5.md) · **Assignee:** `bob-cli-k3.5.1.3` · **Size:** medium
**Created:** 2026-11-11 13:48:49 EST · **Closed:** 2026-11-11 17:20:49 EST
**Plan:** [202611/album\_records\_index.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/album_records_index.md)

## Description

index-sync: expose albums sync using host_catalog transactions, run its lock-free core after notebooks in nightly, document the command and JSON, and verify no-op, isolation, and failure behavior.

## Notes

[2026-11-11T22:20:25Z · bob-cli-k3.5.1.3] PROPOSED FOLLOW-UP: just docs-check remains red on unchanged reference pages: capture-syntax.md (6002 words), mac-capture capture-panel (6265), capture-previews (6244), keyboard (6083), protocol (6294), plugins bob-ledger-tools (6020), and bob-navigation-hotkeys (6200). Existing remediation beads cover capture-panel/previews/keyboard/navigation (bob-cli-jz), protocol (bob-cli-h9), and ledger-tools (bob-cli-il); bob-cli-k3.5.1.1 recorded the same seven-page baseline. This phase brought json-outputs.md to the 6000-word cap. Triage the untracked capture-syntax.md overage with the existing work.

[2026-11-11T22:20:49Z · bob-cli-k3.5.1.3] Implemented bob albums sync for scoped index repair with dry-run, guarded one-commit writes, per-album damage handling, JSON/human reporting, and nightly integration. Verified cargo check; album tests (27), nightly tests (8), sync unit tests (2), docs generation/reference test, command-catalog coverage and protocol tests, formatting, and git diff --check. just check exposed missing albums-sync catalog registration and stale catalog counts; fixed those, and all affected regression tests now pass. just docs-check still reports seven unchanged over-budget references, recorded as a proposed follow-up with existing trackers. epic-symbols reported none.

## Dependencies

- **Depends on:** [bob-cli-k3.5.1.1](bob-cli-k3.5.1.1.md) ✓ · ⧖ 2026-11-11
- **Depends on:** [bob-cli-k3.5.1.2](bob-cli-k3.5.1.2.md) ✓ · ⧖ 2026-11-11
- **Blocks:** [bob-cli-kd.6.1.3](../bob-cli-kd/bob-cli-kd.6.1.3.md) ◐ · ⧖ 2026-11-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-k3.5.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-k3.5.1.3/README.md) | [bob-cli-k3.5.1.3](bob-cli-k3.5.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`6352824`](https://github.com/bobs-org/bob-cli/commit/6352824bffd7db5d2d22950ed83f101c7b8ae4de) | feat(albums): sync generated record indexes | [bob-cli-k3.5.1.3](bob-cli-k3.5.1.3.md) | 2026-11-11 17:22:22 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-k3.5.1.3][1] | Need the phase scope, design file, and prior-work notes before implementation | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-k3.5.1.3/README.md

<!-- sase:referenced-by:end -->
