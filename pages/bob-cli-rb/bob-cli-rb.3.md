# Bead: bob-cli-rb.3 — Mac decodes the lead and previews it in the Task type menu

[Bead Pages](../README.md) / [bob-cli-rb](README.md) / bob-cli-rb.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1hh](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1hh.md) · **Assignee:** `bob-cli-rb.3` · **Size:** small
**Created:** 2026-11-27 15:03:21 EST · **Closed:** 2026-11-27 17:37:53 EST
**Plan:** [202611/capture\_type\_leads.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_type_leads.md)

## Description

mac_lead_preview: decode `lead` tolerantly and show it as a calm `Fix…` hint after the type pill, in the selected-row footer, and in VoiceOver, with protocol docs and CaptureCore tests.

## Notes

[2026-11-27T22:37:53Z · bob-cli-rb.3] Implemented tolerant task_type lead decoding and the menu hint, selected footer, and VoiceOver copy; added CaptureCore decoding and presentation tests and updated protocol docs. Verified Mac scratch release bundle and typecheck-tests, docs-check, and portable build. The full portable suite had one unrelated out-of-order preview test failure; its isolated rerun passed.

## Dependencies

- **Depends on:** [bob-cli-rb.2](bob-cli-rb.2.md) ✓ · ⧖ 2026-11-27
- **Blocks:** [bob-cli-rb.4](bob-cli-rb.4.md) ◐ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-rb.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-rb.3/README.md) | [bob-cli-rb.3](bob-cli-rb.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@1a5723d`](https://github.com/bobs-org/bob-mac-capture/commit/1a5723d2239eb2920483e9fa6770beacdd5911d4) | feat(capture): preview task type leads | [bob-cli-rb.3](bob-cli-rb.3.md) | 2026-11-27 17:38:38 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-rb.3][1] | Need the phase scope, notes, and design file before completing assigned work | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-rb.3/README.md

<!-- sase:referenced-by:end -->
