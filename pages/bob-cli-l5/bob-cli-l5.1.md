# Bead: bob-cli-l5.1 — gcal.ack journal kind, ack fold, and the external classifier

[Bead Pages](../README.md) / [bob-cli-l5](README.md) / bob-cli-l5.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1c2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1c2.md) · **Assignee:** `bob-cli-l5.1` · **Size:** medium
**Created:** 2026-11-12 16:39:08 EST · **Closed:** 2026-11-12 17:36:21 EST
**Plan:** [202611/gcal\_external\_event\_ack.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gcal_external_event_ack.md)

## Description

journal: add the gcal.ack record (parse, fold into an AckBook, append), note-history ack evidence, the load_state skip, the account guard, reset/-F survival, model.rs is_external(), and the gcal.ack config kill switch.

## Notes

[2026-11-12T22:30:31Z · bob-cli-l5.1] PROPOSED FOLLOW-UP: Reconcile clean-base gate debt before the gcal epic lands. Album-index test config_backed_record_never_stages_an_album_edit fails ([] instead of ["podcasts"]); coordinate with bob-cli-l3.3, whose accepted config_backed_album_test=repurpose may own it. Full just all also reports native::gcal::cli::tests::sync_args_read_last_n_days_aliases_and_default_to_none (tracked bob-cli-l2), records_update_completion_uses_retained_type (bob-cli-k3), and the root-help snapshot (bob-cli-ix.3). docs-check’s navigation-hotkeys budget failure (6039/6000) is tracked by bob-cli-l3.3. These reproduced on clean HEAD; l2’s gcal failure is also confirmed across two machines.

[2026-11-12T22:36:21Z · bob-cli-l5.1] Implemented gcal.ack journal parsing, fold, append, note-history evidence, load_state skip, external classifier, and config kill switch. Verified all 14 journal tests, the external classifier and config tests, fmt, and Clippy. just all and docs-check failures are reproduced on clean HEAD and recorded in the PROPOSED FOLLOW-UP note.

## Dependencies

- **Blocks:** [bob-cli-l5.2](bob-cli-l5.2.md) ✓ · ⧖ 2026-11-12
- **Blocks:** [bob-cli-l5.3](bob-cli-l5.3.md) ◐ · ⧖ 2026-11-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-l5.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-l5.1/README.md) | [bob-cli-l5.1](bob-cli-l5.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b6ed0e5`](https://github.com/bobs-org/bob-cli/commit/b6ed0e597395ee22d8276d1c6063c96afec2e047) | feat(gcal): add ack journal and event classifier | [bob-cli-l5.1](bob-cli-l5.1.md) | 2026-11-12 17:38:48 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-l5.1][1] | Need the phase scope, design file, prior notes, and epic decisions before implementation | 3 |
| read-by | [agent:bob-cli-l5.2][2] | check dependency completion | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-l5.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-l5.2/README.md

<!-- sase:referenced-by:end -->
