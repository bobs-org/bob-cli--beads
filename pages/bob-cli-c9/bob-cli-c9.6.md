# Bead: bob-cli-c9.6 — Decision record, glossary correction, and final docs pass

[Bead Pages](../README.md) / [bob-cli-c9](README.md) / bob-cli-c9.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.14a](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.14a.md) · **Assignee:** `bob-cli-c9.6` · **Size:** small
**Created:** 2026-10-25 14:15:32 EDT · **Closed:** 2026-10-26 12:11:48 EDT
**Plan:** [202610/ref\_create\_force\_recapture.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_create_force_recapture.md)

## Description

record: write the accepted recapture decision record and correct the Reference Task glossary strand, then republish memory. Run the final cross-page docs consistency pass and docs-check, and record proposed follow-ups.

## Notes

[2026-10-26T16:11:21Z · bob-cli-c9.6] PROPOSED FOLLOW-UP: docs-check lint fails on clean tree: BOB_TEST_FIXTURE_PDF read in src/native/highlights_ref/source_store.rs:187 is an undocumented production environment name (bob-docs lint); document it in docs/reference/configuration.md or add a reasoned exact exception

[2026-10-26T16:11:25Z · bob-cli-c9.6] PROPOSED FOLLOW-UP: SASE research file hook can dodge dedupe through hash-suffixed Markdown stems (the five ref/chat/*-<12 hex>.md duplicates); possible fix: strip the artifact id when deriving stems, and choose -f overwrite while the earlier report is unread, otherwise -f (spans bob-cli and chezmoi)

[2026-10-26T16:11:29Z · bob-cli-c9.6] PROPOSED FOLLOW-UP: Bob Mac Capture Refs panel: add a vN chip for reread families (under decisions:mac-capture-is-a-thin-client)

[2026-10-26T16:11:33Z · bob-cli-c9.6] PROPOSED FOLLOW-UP: bob-plugins reading board: add a vN chip for reread families

[2026-10-26T16:11:48Z · bob-cli-c9.6] Corrected glossary:reference-task to the v2 parent-note ^ref-<slug> model (-vN for rereads, legacy in-note ^ref still recognized) and republished via sase memory init; no decisions record per reviewer (memory_decision_record=no). Docs pass: Dedupe refusal example now shows all three hint rows with exact alignment, chip wording fixed; just docs-check assembly/validation pass, lint fails pre-existing on clean tree (BOB_TEST_FIXTURE_PDF, recorded as follow-up). Four PROPOSED FOLLOW-UP notes recorded.

## Dependencies

- **Depends on:** [bob-cli-c9.5](bob-cli-c9.5.md) ✓ · ⧖ 2026-10-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-c9.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.6/README.md) | [bob-cli-c9.6](bob-cli-c9.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`94cd2d9`](https://github.com/bobs-org/bob-cli/commit/94cd2d9528997aa490f6c984c92e26faf18486a4) | docs(ref): record-phase glossary correction and recapture docs pass | [bob-cli-c9.6](bob-cli-c9.6.md) | 2026-10-26 12:12:45 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-c9.6][1] | Need phase scope and design file | 2 |
| read-by | [agent:bob-cli-ce.6][2] | Check whether the docs-lint failure already has follow-up ownership | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.6/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ce.6/README.md

<!-- sase:referenced-by:end -->
