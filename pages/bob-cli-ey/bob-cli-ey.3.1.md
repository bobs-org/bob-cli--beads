# Bead: bob-cli-ey.3.1 — Bob Mac Capture directive menus and clipboard previews

[Bead Pages](../README.md) / [bob-cli-ey.3](bob-cli-ey.3.md) / bob-cli-ey.3.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ey.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ey.3.md) · **Assignee:** `bob-cli-ey.3.1.land`
**Created:** 2026-10-31 23:32:59 EDT · **Closed:** 2026-11-01 02:51:10 EST
**Plan:** [202610/mac\_directives.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/mac_directives.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/mac_directives.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/mac_directives.md

<!-- sase:links:end -->

## Description

Complete bob-cli-ey.3 with unselected directive and type menus, a grammar-2 compatibility gate, real clipboard previews, and no retired capture paths.

## Notes

[2026-11-01T06:53:27Z · bob-cli-ey.3.1.land] LAND AUDIT / FOLLOW-UP TRIAGE: Read this epic and all four child beads and every note; none contains a PROPOSED FOLLOW-UP entry. Reviewed plan:202610/mac_directives.md, inherited parent plan and final memory decisions (no memory edits for this child), Rust serializers, Mac source and commits 04904ee/a580c0d/cea18c1/a8e2ab6. Wire decoding, unselected menu representation, directive copy/spans, retired-path deletion, and Clip-card plumbing are present. Retirement sweep is clean and epic-symbols for this epic and parent phase bob-cli-ey.3 are empty. Fetched both bases: bob-cli remains a1dcb64e and Mac master remains a8e2ab6; no non-epic Mac commits after pre-epic 91a5d2b and no bob-cli commits after this epic began, so no additional post-start integration drift. Phase portable results (up to 1877 tests) and docs/scripts passes are recorded, but they exclude hosted tests. Actual Mac CI at cea18c1 (run 41280243768, job 124770529844) passes lint/build and fails 61 assertions in 3504 tests; compared with pre-epic 91a5d2b CI 41260240529/job 124711823950 (19 assertions across seven pre-existing nodes). Distinct epic regressions include completion/picker accept-and-submit being silently blocked by the new current-draft grammar gate, Open Hint setup, shelf IDs/order/cursors/refusal copy, plus-sub-bullet fake scenario, and new typed-hash filtering coverage. Current a8e2ab6 CI 41282066807/job 124775827805 passes lint/build but its new clip suite times out because fakeBobPath resolves Tests/Tests/Fixtures/fake-bob, then crashes indexing an empty batch result. Source review also found clipboard poll retains self across sleep with no deinit cancellation, and history Clip cards render both flattened lines and the same lines under entry dividers. These are remaining epic work for a medium repair tale, not follow-up tasks. Mac SSH timed out (10-second bounded attempt); scratch bundle/typecheck was unavailable. Follow-up disposition: used sase_new_task, searched same-type tasks and last-week tasks and active epic scopes; corroborated existing bob-cli-f3 with independent baseline/menu CI evidence (+1 recorded). No new task created; baseline line-case/plus/retype/menu failures predate this epic. Typed-menu fixture coverage overlaps the new acceptance requirement and must be repaired in this epic as needed; the other f3 nodes remain with f3. No proposals declined beyond declining duplicate task creation for f3. Do not close until the repair tale completes; its final step must close this epic and only parent phase bob-cli-ey.3, and mark plan:202610/mac_directives.md done.

[2026-11-01T07:51:10Z · bob-cli-ey.3.1.land--3] Completed the integrated Mac Capture directive landing: repaired one-shot submit continuation and stale/cancelled parse handling; regenerated current-wire task, template, and directive fixtures; preserved valid sub-bullet and %l routing; tightened clipboard preview supersession/deallocation and rendered history once. Reviewed the four closed child beads; no follow-up proposals remain. just check-scripts passed and just portable-check passed with 1,877 tests. Retired-syntax and removed-field scans are clear; just symvision is absent. The Mac host was unreachable, so macOS targets unverified. bob-cli-f3 records the typed-menu fixture overlap resolved; unrelated baseline failures remain.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ey.3.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ey.3.1.land.md) | [bob-cli-ey.3.1](bob-cli-ey.3.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ey.3.1.3][1] | Need epic DECISIONS that bind this child phase | 4 |
| read-by | [agent:bob-cli-ey.3.1.4][2] | Need phase scope, decisions, symbols for clip-preview work | 1 |
| read-by | [agent:bob-cli-ey.3.1.land--3][3] | Need child bead scope and history before closing the completed directive repair | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ey.3.1.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ey.3.1.4/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ey.3.1.land.md

<!-- sase:referenced-by:end -->
