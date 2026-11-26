# Bead: bob-cli-ph.8.1 — Finish Bob Mac Capture true-case drawers

[Bead Pages](../README.md) / [bob-cli-ph.8](bob-cli-ph.8.md) / bob-cli-ph.8.1

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ph.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.8.md) · **Assignee:** `bob-cli-ph.8.1.land`
**Created:** 2026-11-25 20:55:59 EST
**Plan:** [202611/finish\_mac\_true\_case\_drawers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/finish_mac_true_case_drawers.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/finish_mac_true_case_drawers.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/finish_mac_true_case_drawers.md

<!-- sase:links:end -->

## Description

Bob Mac Capture builds green again, draws Bob-annotated drawer headers as a tray plus the verbatim title, paints draft drawer titles and delimiters from Bob's spans, and types `*`, Backspace, newline, and overtype assists on Bob's authority, completing bob-cli-ph.8.

## Notes

[2026-11-26T09:02:22Z · bob-cli-ph.8.1.land] LAND TRIAGE of PROPOSED FOLLOW-UPs: (1) bob-cli-ph.8.1.3 #2 and bob-cli-ph.8.1.4 #1 (macOS Test-step bare fatalError) DECLINED: not pre-existing; the cited 'clean base 4d9e845' is this epic's own preview-tray commit 4d9e845e, whose test target failed to compile (DrawerHeaderDesignTests.swift:59/80, run 45753263190), and run 45763712398 failed compiling CaptureDrawerPipelineTests.swift ('cannot find model'); both fixed in-epic by c2dd7fbf and a2e79f65, and run 45780151440 now executes all 5297 tests. (2) bob-cli-ph.8.1.5 #1 (CaptureDrawerPipelineTests compile errors) DECLINED as a task: caused by this epic's c561b26a, fixed by a2e79f65. (3) bob-cli-ph.8.1.6 #2 (bob-cli just check red drawer goldens) not caused by this epic (ph.10 cutover 9573ff86/46aba677): ROUTED to active epic bob-cli-ph as corroboration of its note #4 / bob-cli-ph.10 #3; reproduced independently on 1c23bce7. (4) bob-cli-ph.8.1.6 #3 (Mac push, exact-SHA CI, screenshots) is EPIC WORK, carried into the lander tale. (5) Lander-discovered: Mac drawer preview fixtures predate the cutover (grammar 31, legacy_caps): ROUTED to bob-cli-ph as a DISCOVERED ISSUE (cutover drift, related to but not a duplicate of bob-cli-ge). (6) Lander-discovered integration conflict: 631a49d5 re-added legacy_caps to docs/task-drawers.md, already corrected by ph.10's 1d6df8d1; no further edit needed. REMAINING EPIC WORK: exact-SHA macOS run 45780151440 on a2e79f65 fails 7 CaptureDrawerPipelineTests (23 assertions; first CI execution of 8.1.4/8.1.5 tests), and the Mac drawer-menu docs keep stale ALL-CAPS examples.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ph.8.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.8.1.land.md) | [bob-cli-ph.8.1](bob-cli-ph.8.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@403781d`](https://github.com/bobs-org/bob-mac-capture/commit/403781d2b3d2921584b677fae1e76b4c5bfd952b) | fix(mac-capture): land true-case drawer pipeline tests and reconcile docs | [bob-cli-ph.8.1](bob-cli-ph.8.1.md) | 2026-11-26 04:28:54 EST |
| bob-mac-capture | [`bob-mac-capture@b38c4cc`](https://github.com/bobs-org/bob-mac-capture/commit/b38c4cc3ced036c644cc230158972b819ed3fcf3) | fix(mac-capture): isolate drawer newline undo and harden old-Bob tip race | [bob-cli-ph.8.1](bob-cli-ph.8.1.md) | 2026-11-26 05:05:39 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ph.10][1] | Identify existing evidence or task tracking for baseline drawer fixture failures | 1 |
| read-by | [agent:bob-cli-ph.8.1.1--4][2] | Inspect the specified epic and its descendants before deciding whether closure is permitted | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.10.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.8.1.1.md

<!-- sase:referenced-by:end -->
