# Bead: bob-cli-66.2 — Agenda JSON models, client call, fake-bob branch, and fixtures

[Bead Pages](../README.md) / [bob-cli-66](README.md) / bob-cli-66.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.48.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.48.linker.w0.md) · **Assignee:** `bob-cli-66.2` · **Size:** small
**Created:** 2026-10-09 17:42:23 EDT · **Closed:** 2026-10-09 18:58:05 EDT
**Plan:** [202610/idle\_capture\_pomodoro\_agenda.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/idle_capture_pomodoro_agenda.md)

## Description

mac-agenda-models: add the CaptureCore `CaptureAgendaSnapshot` decoders (decodeIfPresent everywhere), `BobProcessClient.captureAgenda(previous:)` with a byte-compare short circuit and old-bob detection, a fake-bob `--tasks` branch, and fixtures copied from bob-cli goldens, all with tests.

## Notes

[2026-10-09T22:58:05Z · bob-cli-66.2--2] Agenda models + CaptureAgendaModelsTests and BobProcessClientTests green locally; CI run https://github.com/bobs-org/bob-mac-capture/actions/runs/38000173807 green at SHA febd4dd

## Dependencies

- **Depends on:** [bob-cli-66.1](bob-cli-66.1.md) ✓ · ⧖ 2026-10-09
- **Blocks:** [bob-cli-66.3](bob-cli-66.3.md) ✓ · ⧖ 2026-10-09
- **Blocks:** [bob-cli-66.4](bob-cli-66.4.md) ✓ · ⧖ 2026-10-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-66.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-66.2.md) | [bob-cli-66.2](bob-cli-66.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@febd4dd`](https://github.com/bobs-org/bob-mac-capture/commit/febd4dde8c2956118e18dc3c35cd6c717fbd9583) | feat(agenda): JSON models, agenda client call, fake-bob branch, fixtures | [bob-cli-66.2](bob-cli-66.2.md) | 2026-10-09 18:36:55 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-66.2][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-66.3][2] | Check dependency completion state | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-66.2.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-66.3.md

<!-- sase:referenced-by:end -->
