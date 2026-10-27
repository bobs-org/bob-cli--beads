# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.3 — Build a guarded stamped-PDF publication helper

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.3` · **Size:** medium
**Created:** 2026-10-26 22:51:28 EDT · **Closed:** 2026-10-26 23:41:19 EDT
**Plan:** [202610/remaining\_pdf\_write\_coordination.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/remaining_pdf_write_coordination.md)

## Description

staged-install: separate private PDF stamping from public installation and add one guarded install boundary, used by install_stamped_pdf. Recheck destination identity and marker after access, preserve presenter changes, and keep companion audio inside the granted callback. Cover the helper and PDF publication path with injected-coordinator tests.

## Notes

[2026-10-27T03:40:57Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.3] Guarded publication helper landed in highlights_ref/publish.rs and install_stamped_pdf. 16 injected-coordinator unit tests pass (unchanged-marker save, changed marker, hold, coordinator failure, late collision, missing dest, key-off, Linux pass-through, companion preservation, local-PDF stamp+install). CLI highlights_create_local_pdf_installs_and_stamps passes. cargo fmt --check and clippy --all-targets gate passed. epic-symbols: none. overwrite/execute.rs stays an already-granted scope and is not wrapped.

[2026-10-27T03:41:19Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.3] Guarded publication helper in highlights_ref/publish.rs; install_stamped_pdf snapshots dest, coordinates existing PDFs, rechecks identity/marker after access, and copies companion audio only after the grant. 16 injected-coordinator tests pass (unchanged-marker save, changed marker, hold, coordinator failure, late collision, missing dest, key-off, Linux pass-through, companion preservation, local-PDF stamp+install). CLI highlights_create_local_pdf_installs_and_stamps passes. cargo fmt --check and clippy --all-targets --all-features with the just check rustc_gate passed. No --epic-symbol leftovers. overwrite/execute.rs remains an already-granted scope.

## Dependencies

- **Depends on:** [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.1](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.1.md) ✓ · ⧖ 2026-10-26
- **Blocks:** [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.4](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.4.md) ✓ · ⧖ 2026-10-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.3.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.3](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`22882a7`](https://github.com/bobs-org/bob-cli/commit/22882a7d6557a3d2a97e12736c4d114f6bc6da50) | feat(ref): add guarded stamped-PDF publication helper | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.3](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.3.md) | 2026-10-27 00:01:32 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.3--1][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.4][2] | Need prior phase helper contract to reuse guarded publication helper | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.3.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.4/README.md

<!-- sase:referenced-by:end -->
