# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.4 — Route capture replacement writers through guarded publication

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.4` · **Size:** medium
**Created:** 2026-10-26 22:51:28 EDT · **Closed:** 2026-10-27 00:32:50 EDT
**Plan:** [202610/remaining\_pdf\_write\_coordination.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/remaining_pdf_write_coordination.md)

## Description

capture-writers: migrate stamp_and_install and remaining direct public PDF copies from create, clip, and collection to the shared guarded install boundary, including companion audio ordering. Preserve existing filed-overwrite coordination and all force-mode, collision, source-store, and ingest contracts.

## Notes

[2026-10-27T04:32:50Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.4] capture-writers done: all public replacement writers route through the guarded install boundary. stamp_and_install now snapshots + publishes via publish_public_pdf (no-clobber save when absent, atomic replace when present); new stamp_and_install_with(_with_listen) and publish::install_staged_pdf_with_listen keep companion/listen audio inside the grant. Migrated: create stamp_listen_and_install_pdf + markdown listen/non-listen blocks, clip listen/non-listen, collection capture_and_install (both-audio staged path), ingest listen helper. Overwrite execute/sync paths untouched (already-granted scope); force/collision/dry-run/source-store/ingest contracts preserved; holds install nothing and keep scratch with rebind hints. Evidence: 11 new injected-coordinator unit tests (grant/hold/changed-marker/late-collision/fresh/key-off/audio-inside) — 27/27 publish tests pass; full just check exit=0 (fmt, clippy rustc_gate, all 18 test binaries ok). No epic-symbols. Inventory: every public writer guarded (stamp_and_install*, install_stamped_pdf*, install_staged_pdf_with_listen) or already protected (overwrite::execute, sync external scope); private scratch writes (stamp_pdf_to_scratch, renders) stay direct.

## Dependencies

- **Depends on:** [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.3](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.3.md) ✓ · ⧖ 2026-10-26
- **Blocks:** [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.5](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.5.md) ◐ · ⧖ 2026-10-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.4/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.4](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`0971ad5`](https://github.com/bobs-org/bob-cli/commit/0971ad564b7661e2a79a076626fbbc20fad48b5a) | feat(highlights-ref): route capture replacement writers through guarded publish boundary | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.4](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.4.md) | 2026-10-27 00:34:35 EDT |
