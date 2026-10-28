# Bead: bob-cli-du.2.1.4 — Verify capture edge cases and update implemented contract markers

[Bead Pages](../README.md) / [bob-cli-du.2.1](bob-cli-du.2.1.md) / bob-cli-du.2.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-du.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-du.2.md) · **Assignee:** `bob-cli-du.2.1.4` · **Size:** medium
**Created:** 2026-10-28 15:26:11 EDT · **Closed:** 2026-10-28 18:00:45 EDT
**Plan:** [202610/complete\_label\_capture.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/complete_label_capture.md)

## Description

capture-acceptance: finish the scratch-vault acceptance matrix, prove no-config and existing !/cancel compatibility, verify rollback and mixed successor selection, update capture contract documentation, and prepare evidence for the child epic land agent.

## Notes

[2026-10-28T22:00:24Z · bob-cli-du.2.1.4] PROPOSED FOLLOW-UP: Exercise inbox routing when a complete-label recovered candidate lives in an inbox note — relations_complete covers ledger strike and successor offers but never routes a recovered dependent through inbox_route

[2026-10-28T22:00:30Z · bob-cli-du.2.1.4] PROPOSED FOLLOW-UP: Cover stale disk preimage and injected commit-failure rollback for complete-label batches — relations_complete proves late-invalid-item atomicity and dry-run parity but does not drive the existing transactional harness stale-preimage or injected-failure paths for the complete path

[2026-10-28T22:00:35Z · bob-cli-du.2.1.4] PROPOSED FOLLOW-UP: Cover archived/Cancelled complete targets, || one-off complete labels, same-note S/T composition, and #ref sources — hidden/mirror/midnight/CRLF and cross-note paths are covered but these four variants have no complete-label scratch-vault assertion yet

[2026-10-28T22:00:45Z · bob-cli-du.2.1.4] relations_complete 20/20 pass (8 new acceptance tests: status matrix, relabel/unchanged/inverse, prj, subtasks, locations/mirror/hidden/midnight/CRLF, bang parity, no-config/cancel-only, reconcile+atomicity); relations_cancel 21/21 pass; cargo test workspace green (3849+2393, 0 failed); cargo fmt/clippy clean; docs-check passed; updated capture.md, json-outputs.md, and §18/CL2 markers to implemented-in-capture (nav/surface phases still named as planned)

## Dependencies

- **Depends on:** [bob-cli-du.2.1.3](bob-cli-du.2.1.3.md) ✓ · ⧖ 2026-10-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-du.2.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-du.2.1.4/README.md) | [bob-cli-du.2.1.4](bob-cli-du.2.1.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`87b6e60`](https://github.com/bobs-org/bob-cli/commit/87b6e608912bdf1c9b37e9fdbe411e9ca3974d46) | feat(capture): add relations\_complete acceptance tests and update docs | [bob-cli-du.2.1.4](bob-cli-du.2.1.4.md) | 2026-10-28 18:02:36 EDT |
