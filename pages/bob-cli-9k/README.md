# Bead: bob-cli-9k — Pomodoro homes — derived area and project labels and stats

[Bead Pages](../README.md) / bob-cli-9k

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.4t.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.4t.linker.w0.md) · **Assignee:** `bob-cli-9k.land`
**Created:** 2026-10-18 16:35:49 EDT
**Plan:** [202610/pomodoro\_homes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/pomodoro_homes.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/pomodoro_homes.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | [bead:bob-cli-9n][2] | Source epic: Pomodoro homes resolver, R9 homes object, and the live-surface pattern this task extends |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/pomodoro_homes.md
[2]: https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-9n/README.md

<!-- sase:links:end -->

## Description

Every Pomodoro is labeled, on every surface, by the areas and projects of the tasks it links. The labels are derived at read time from Task Links and never written to the vault. `bob stats` and `dash_stats.md` aggregate time and task throughput by area and project. `rollup: subprojects` on `sase.md` reports every sase sub-project as `sase`. Authored names keep working exactly as they do today, but naming a session becomes optional.

## Notes

[2026-10-19T00:16:22Z · bob-cli-9k.land] LAND FOLLOW-UP TRIAGE (bob-cli-9k.land): (1) 9k.2 #2 scan_hooks.rs rustfmt: declined, already fixed (196af9b reformatted tests/cli/highlights/scan_hooks.rs; landing just check on 1933d54 passes fmt, clippy gate, and 4998 tests). (2) 9k.5 #1 / 9k.6 #1 six clean-base bob-plugins failures: already corroborated by 9k.6 on existing bob-cli-6v (unblocked glyph x4), bob-cli-6w (Keep counts once), bob-cli-7i (forward/reverse project conversion); the landing reran the full suite on bob-plugins fdc4528 (3098/3104, same six) and on a 60148ab export (same six), so no new task. (3) 9k.5 #1 stage ranker 16 ms timing miss: duplicate of bob-cli-3w, recorded +1. (4) 9k.7 #1 RefsLibraryTests/RefsNewestTests Mac test compile failure: duplicate of bob-cli-9m (filed by bob-cli-9j.land), recorded +1 with CI run 39171275522 on e5cd4e1 (Lint+Build green, Test red), so no new task; the 9k.7 macOS-only XCTests have not run on CI until 9m lands. (5) Discovered: pre-existing unnamed-session placeholders outside the plan's surfaces (x close preview, capture-complete pomodoro_name candidates, successor entry_name, Mac pickers, plugin pickers): no duplicate or causal active epic, created feature bob-cli-9n (large, ready), linked to 9k and 9j. (6) Declined: consolidating stats' two parent-chain walkers (task in: vs pomodoro pre_rollup_chain) since they agree today and docs/stats.md already promises equal rules; Reading Board using --bob-area-* tokens (optional polish, no requirement); 'unnamed' wording in close/sync error messages (low value). Remaining epic-caused gaps (R5 split remainder, rust_only vector over-marking, JS mirror parity, review_time vs GTD review row, closed zero-minute state, theme re-split without in:, catalog pruning, projects list alignment, R10 CLI caveat, review hue, stale allow(unused), bob ref today homes, human bob plan chip, 9j override-surface integration, Stats panel chart-pin refresh and view fixes, Mac Refs Today routing/toast and hollow dot, chezmoi tmux sample) go to a child epic plan.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-9k.1](bob-cli-9k.1.md) | Shared homes resolver, rollup switch, contract, and vault config | ✓ closed | medium | 2026-10-18 | 1 | 1 |
| [bob-cli-9k.2](bob-cli-9k.2.md) | Area and project parts in bob stats | ✓ closed | medium | 2026-10-18 | 1 | 1 |
| [bob-cli-9k.3](bob-cli-9k.3.md) | Pomodoro in/review filters and session drill-down data | ✓ closed | medium | 2026-10-18 | 1 | 1 |
| [bob-cli-9k.4](bob-cli-9k.4.md) | Homes on capture-pomodoros, bob plan, and bob pomodoro | ✓ closed | medium | 2026-10-18 | 1 | 1 |
| [bob-cli-9k.5](bob-cli-9k.5.md) | Obsidian ledger home chips | ✓ closed | medium | 2026-10-18 | 1 | 1 |
| [bob-cli-9k.6](bob-cli-9k.6.md) | Where the time went panel on dash\_stats.md | ✓ closed | medium | 2026-10-18 | 1 | 2 |
| [bob-cli-9k.7](bob-cli-9k.7.md) | Bob Mac Capture agenda shows homes | ✓ closed | small | 2026-10-18 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-9k: Pomodoro homes — derived area and project labels and stats [in_progress]"]
    n1["bob-cli-9k.1: Shared homes resolver, rollup switch, contract, and vault config [closed]"]
    n2["bob-cli-9k.2: Area and project parts in bob stats [closed]"]
    n3["bob-cli-9k.3: Pomodoro in/review filters and session drill-down data [closed]"]
    n4["bob-cli-9k.4: Homes on capture-pomodoros, bob plan, and bob pomodoro [closed]"]
    n5["bob-cli-9k.5: Obsidian ledger home chips [closed]"]
    n6["bob-cli-9k.6: Where the time went panel on dash_stats.md [closed]"]
    n7["bob-cli-9k.7: Bob Mac Capture agenda shows homes [closed]"]
    n8["bob-cli-9k.8: Finish Pomodoro homes — contract parity, review time, override labels, and panel fixes [in_progress]"]
    n9["bob-cli-9k.8.1: bob-cli: homes contract parity, review time, and Stats fixes [closed]"]
    n10["bob-cli-9k.8.2: bob-cli: homes on bob ref today, human bob plan, and the = override surfaces [closed]"]
    n11["bob-cli-9k.8.3: bob-plugins: JS mirror parity and Stats panel fixes [closed]"]
    n12["bob-cli-9k.8.4: Bob Mac Capture and chezmoi: no derived routing, hollow forecast dots, override labels [open]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n0 --> n6
    n0 --> n7
    n0 --> n8
    n8 --> n9
    n8 --> n10
    n8 --> n11
    n8 --> n12
    n1 -.-> n2
    n1 -.-> n4
    n1 -.-> n5
    n2 -.-> n3
    n3 -.-> n6
    n4 -.-> n7
    n5 -.-> n6
    n9 -.-> n10
    n9 -.-> n11
    n10 -.-> n12
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-9k.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-9k.1.md) | [bob-cli-9k.1](bob-cli-9k.1.md) | 1 |
| [bbugyi200.athena.bob-cli-9k.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9k.2/README.md) | [bob-cli-9k.2](bob-cli-9k.2.md) | 1 |
| [bbugyi200.athena.bob-cli-9k.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-9k.3.md) | [bob-cli-9k.3](bob-cli-9k.3.md) | 1 |
| [bbugyi200.athena.bob-cli-9k.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9k.4/README.md) | [bob-cli-9k.4](bob-cli-9k.4.md) | 1 |
| [bbugyi200.athena.bob-cli-9k.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9k.5/README.md) | [bob-cli-9k.5](bob-cli-9k.5.md) | 1 |
| [bbugyi200.athena.bob-cli-9k.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9k.6/README.md) | [bob-cli-9k.6](bob-cli-9k.6.md) | 2 |
| [bbugyi200.athena.bob-cli-9k.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9k.7/README.md) | [bob-cli-9k.7](bob-cli-9k.7.md) | 0 |
| [bbugyi200.athena.bob-cli-9k.8.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-9k.8.1.md) | [bob-cli-9k.8.1](bob-cli-9k.8.1.md) | 1 |
| [bbugyi200.athena.bob-cli-9k.8.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9k.8.2/README.md) | [bob-cli-9k.8.2](bob-cli-9k.8.2.md) | 0 |
| [bbugyi200.athena.bob-cli-9k.8.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9k.8.3/README.md) | [bob-cli-9k.8.3](bob-cli-9k.8.3.md) | 1 |
| [bbugyi200.athena.bob-cli-9k.8.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9k.8.4/README.md) | [bob-cli-9k.8.4](bob-cli-9k.8.4.md) | 0 |
| [bbugyi200.athena.bob-cli-9k.8.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9k.8.land/README.md) | [bob-cli-9k.8](bob-cli-9k.8.md) | 0 |
| [bbugyi200.athena.bob-cli-9k.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-9k.land.md) | [bob-cli-9k](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`9ec332c`](https://github.com/bobs-org/bob-cli/commit/9ec332c81def3014a559e088124ef93e3bb15ae7) | feat(homes): add shared Pomodoro home resolver and rollup contract | [bob-cli-9k.1](bob-cli-9k.1.md) | 2026-10-18 17:23:52 EDT |
| bob-plugins | [`bob-plugins@0ffb3e0`](https://github.com/bobs-org/bob-plugins/commit/0ffb3e075d48d63796391e3e89dde831f0dc7bc0) | feat(bob-ledger-tools): add pomodoro home chips | [bob-cli-9k.5](bob-cli-9k.5.md) | 2026-10-18 17:51:32 EDT |
| bob-cli | [`196af9b`](https://github.com/bobs-org/bob-cli/commit/196af9b38d9bac93e7055c599a7640e0f9eac95a) | feat(pomodoro-homes): expose derived homes on live CLI surfaces | [bob-cli-9k.4](bob-cli-9k.4.md) | 2026-10-18 17:52:36 EDT |
| bob-cli | [`81103c2`](https://github.com/bobs-org/bob-cli/commit/81103c2e2b053e6107473b81f8952966e599023c) | feat(stats): add area and project parts to bob stats | [bob-cli-9k.2](bob-cli-9k.2.md) | 2026-10-18 18:29:50 EDT |
| bob-cli | [`930b349`](https://github.com/bobs-org/bob-cli/commit/930b3495c01e1bd151ce9bdab36bcf4ad9d0dda5) | feat(stats): add pomodoro in/review filters and session drill-down | [bob-cli-9k.3](bob-cli-9k.3.md) | 2026-10-18 19:17:42 EDT |
| bob-cli | [`1933d54`](https://github.com/bobs-org/bob-cli/commit/1933d544e224e92e05ca8a94b60c9e8e08538cdb) | docs(stats): document area and project attribution | [bob-cli-9k.6](bob-cli-9k.6.md) | 2026-10-18 19:45:02 EDT |
| bob-plugins | [`bob-plugins@fdc4528`](https://github.com/bobs-org/bob-plugins/commit/fdc4528d53170b2bfd0b20ae5b609023c373fc6f) | feat(stats): add area and project attribution panel | [bob-cli-9k.6](bob-cli-9k.6.md) | 2026-10-18 19:46:01 EDT |
| bob-cli | [`77c7741`](https://github.com/bobs-org/bob-cli/commit/77c77410e32b52010ad8f0d539f466202deb30d5) | feat(stats): complete pomodoro homes parity and stats fixes | [bob-cli-9k.8.1](bob-cli-9k.8.1.md) | 2026-10-18 20:54:36 EDT |
| bob-plugins | [`bob-plugins@ed72a42`](https://github.com/bobs-org/bob-plugins/commit/ed72a4201560e53221198b503c3945b9e9606e98) | feat(ledger-tools): bring pomodoro homes JS mirror to Rust parity | [bob-cli-9k.8.3](bob-cli-9k.8.3.md) | 2026-10-18 21:32:14 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-9k.2][1] | Need epic DECISIONS, sibling phases, and overall scope for stats-parts | 1 |
| read-by | [agent:bob-cli-9k.3--1][2] | Need parent epic decisions and remaining phases | 1 |
| read-by | [agent:bob-cli-9k.4][3] | Need parent epic decisions and remaining phases | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9k.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-9k.3.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9k.4/README.md

<!-- sase:referenced-by:end -->
