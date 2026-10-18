# Bead: bob-cli-9c.4 — bob ref scan --intake-only drain

[Bead Pages](../README.md) / [bob-cli-9c](README.md) / bob-cli-9c.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.4s.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.4s.linker.w0.md) · **Assignee:** `bob-cli-9c.4` · **Size:** medium
**Created:** 2026-10-18 14:40:04 EDT · **Closed:** 2026-10-18 15:38:59 EDT
**Plan:** [202610/ref\_ingest\_at\_birth.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_ingest_at_birth.md)

## Description

scan-intake-only: add `bob ref scan -i/--intake-only`. It drains the local xlib/ queue through the intake session, with one commit per reference, and skips the annotation pass and the pre-scan hook. It refuses `-w`, adds additive JSON fields, and exits non-zero while anything stays queued, so timers surface stuck items.

## Notes

[2026-10-18T19:38:54Z · bob-cli-9c.4] PROPOSED FOLLOW-UP: flaky lib test native::highlights_ref::fetch::tests::curl_pins_the_checked_address_with_resolve — failed once under full `just check` with "Text file busy (os error 26)" executing its fake-curl.sh (script written then exec while other threads fork); passes alone and on the clean base tree, no existing flake bead covers it

[2026-10-18T19:38:59Z · bob-cli-9c.4] Added bob ref scan -i/--intake-only: drains xlib/ through the intake session (one commit per reference, one pre-sync and one post-sync push), skips annotation pass and pre-scan hook, conflicts with -w (exit 2), exits 1 while anything stays queued/incomplete, empty queue takes no lock. Human and JSON paths (additive intake_only/queued keys at end of both envelopes, pre_sync_failed error code, hook.status skipped), --dry-run preview with local preflight, late-audio units. Docs updated (highlights-ref-sync.md, ref.md, help fixture). Verified: 10 new tests in tests/cli/highlights/scan_intake.rs plus lib unit test pass; full cli binary 1798 passed; just check green except one unrelated fetch curl 'Text file busy' flake that passes on rerun and on clean base (noted as PROPOSED FOLLOW-UP); epic-symbols empty.

## Dependencies

- **Depends on:** [bob-cli-9c.1](bob-cli-9c.1.md) ✓ · ⧖ 2026-10-18
- **Depends on:** [bob-cli-9c.2](bob-cli-9c.2.md) ✓ · ⧖ 2026-10-18
- **Blocks:** [bob-cli-9c.5](bob-cli-9c.5.md) ◐ · ⧖ 2026-10-18
- **Blocks:** [bob-cli-9c.6](bob-cli-9c.6.md) ◐ · ⧖ 2026-10-18

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-9c.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9c.4/README.md) | [bob-cli-9c.4](bob-cli-9c.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`fa7745f`](https://github.com/bobs-org/bob-cli/commit/fa7745fc71c0fe0cb2fafe4c78270e3b5d890837) | feat(ref): add scan --intake-only xlib drain | [bob-cli-9c.4](bob-cli-9c.4.md) | 2026-10-18 15:39:40 EDT |
