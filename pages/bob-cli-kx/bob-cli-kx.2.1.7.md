# Bead: bob-cli-kx.2.1.7 — Reports, doctor, documentation, and conformance audit

[Bead Pages](../README.md) / [bob-cli-kx.2.1](bob-cli-kx.2.1.md) / bob-cli-kx.2.1.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-kx.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kx.2.md) · **Assignee:** `bob-cli-kx.2.1.7` · **Size:** medium
**Created:** 2026-11-12 11:37:45 EST · **Closed:** 2026-11-12 22:57:39 EST
**Plan:** [202611/gmail\_archive\_core.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_archive_core.md)

## Description

contract: Finish quiet-breaking human and additive JSON reports, archive doctor rows, docs/help regeneration, and the complete core C1-C20 conformance audit. Record supersession evidence for the outer land agent and run the required gates. Implement section 7.

## Notes

[2026-11-13T03:56:14Z · bob-cli-kx.2.1.7] PROPOSED FOLLOW-UP: Repair the docs-gen failure: bob-docs gen rejects sase/memory/glossary/event-ack.md for missing front matter; this reproduces on clean base and is already tracked by bob-cli-l5.3.1.2 note #1.

[2026-11-13T03:56:29Z · bob-cli-kx.2.1.7] PROPOSED FOLLOW-UP: Fix native::gcal::cli::tests::sync_args_read_last_n_days_aliases_and_default_to_none, which failed identically on clean base; the existing CI task bob-cli-l2 tracks it.

[2026-11-13T03:57:39Z · bob-cli-kx.2.1.7] Implemented archive sync report/doctor rows and hints, additive JSON/config fields, receipt recovery/release handling, docs, and C1-C20 conformance coverage. Verified fmt, clippy, 83 focused integration tests, and completion-kind unit test. Full check has only the clean-base GCal alias test failure (tracked by bob-cli-l2); docs generation is blocked by the clean-base event-ack front-matter failure (tracked by bob-cli-l5.3.1.2). git diff --check passes; no epic symbols remain.

## Dependencies

- **Depends on:** [bob-cli-kx.2.1.6](bob-cli-kx.2.1.6.md) ✓ · ⧖ 2026-11-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kx.2.1.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.2.1.7/README.md) | [bob-cli-kx.2.1.7](bob-cli-kx.2.1.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`54fc8c6`](https://github.com/bobs-org/bob-cli/commit/54fc8c61870cf863710fb8051fb4d25c6f1e8117) | feat(gmail)!: complete archive reports and conformance audit | [bob-cli-kx.2.1.7](bob-cli-kx.2.1.7.md) | 2026-11-12 22:59:42 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kx.2.1.7][1] | Verify final phase state and recorded clean-base follow-ups before close | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.2.1.7/README.md

<!-- sase:referenced-by:end -->
