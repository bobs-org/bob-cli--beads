# Bead: bob-cli-4w — bob ref: a reference library for agents and Bryan

[Bead Pages](../README.md) / bob-cli-4w

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.3s.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.3s.linker.w0.md) · **Assignee:** `bob-cli-4w.land`
**Created:** 2026-10-06 20:15:52 EDT · **Closed:** 2026-10-07 01:09:08 EDT
**Plan:** [202610/bob\_ref\_reference\_library.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_ref_reference_library.md)

## Description

`bob ref` is the canonical command for Bob's reference library. `find`, `list`, and `show` answer "is this already in my library, what am I reading or planning to read, what have I finished, and what did I note?" correctly on the real vault. Each answer comes in beautiful human output, Markdown, or versioned JSON, and is honest about coverage. The six Highlights pipeline verbs work unchanged under `bob ref` and under the permanent `bob highlights` and `bob highlights-ref` aliases. Annotations no longer carry the leaked marker mirror, and a URL that only a legacy note records can be captured again. A deployed `bob_ref` skill makes "check the library first" the default step for agents that recommend reading.

## Notes

[2026-10-07T04:32:34Z · bob-cli-4w.land] LAND TRIAGE (bob-cli-4w.land) of every PROPOSED FOLLOW-UP: (1) every_value_arg_has_a_decision ref create:audio [4w.1#1, .2#2, .3#3, .4#1, .5#1, .6#1, .8#2, .9#1, .11#7] -> duplicate of bob-cli-4j, +1 recorded (reproduced deterministic on e3e69df). (2) listen_filter_renders_card_and_encoded_play_link [4w.1#2, .3#4, .4#1, .5#2, .6#1, .8#1, .9#1, .11#7] -> duplicate of bob-cli-4u, +1 recorded (deterministic). (3) capture_pomodoros missing_note warning flake [4w.3#5, .5#3, .6#2, .9#1] -> duplicate of bob-cli-40 and its root-cause bead bob-cli-2e, +1 on both (failed in parallel just all, passed isolated); note_ready scan_excludes flake [4w.6#2] already corroborated on bob-cli-2e. (4) bash completion PTY flake [4w.9#1] -> DISCOVERED ISSUE note on active epic bob-cli-3j, which authored tests/cli/completion/bash.rs; not reproduced (cli 1107/1107) and the test name was not recorded, so no flake bead. (5) 4w.3#1 placeholder -> declined, retracted by 4w.3#2. (6) zorg reading-record migration epic [4w.11#2] -> new task bob-cli-4x (feature, xlarge). (7) decisions record 'reference reading state is derived; library verbs read-only' [4w.11#3] -> new task bob-cli-51 (memory, small). (8) library-wide annotation search [4w.11#4] -> new task bob-cli-4y (feature, large). (9) bare bob ref defaulting to list [4w.11#5] -> new task bob-cli-4z (feature, small). (10) durable ever-finished history [4w.11#6] -> new task bob-cli-50 (feature, large). Typed related links to bob-cli-4w were rejected by the pre-existing artifact-link store error (reused operation_id); each description names the proposing bead instead. Also recorded the plan's missing sync-fixes hygiene note on bob-cli-4w.8.

[2026-10-07T05:09:08Z · bob-cli-4w.land] Land verified: all 11 phases (bob-cli-4w.1-.11) closed and their notes addressed; source and commits ecabc33..e3e69df reviewed against plan:202610/bob_ref_reference_library.md; no non-epic commits landed since the epic started (nothing to integrate). Landing tale fixed epic-caused defects: list Markdown separator and summary-line breaks, list column alignment, dim pending marker, show task page labels and marks, --since overflow, bob ref -h spacing and missing example, DOI/arXiv-DOI query keys, find -i url field, invalid-YAML wikilink fallback, skipped-count, single legacy hint, dead code and new clippy warnings, missed docs/README/install-smoke updates, plus tests. just all: fmt clean, clippy zero warnings in ref_library/highlights_ref areas, lib shows only tracked bob-cli-4j/bob-cli-4u failures and the bob-cli-40 parallel flake (passes --exact); cargo test --test cli 1111/1111 green. Follow-ups triaged in the epic's LAND TRIAGE note (new bob-cli-4x, 4y, 4z, 50, 51; +1 bob-cli-4j, 4u, 40, 2e; note on bob-cli-3j). No epic-symbol entries.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-4w.1](bob-cli-4w.1.md) | Promote bob ref to the canonical command | ✓ closed | medium | 2026-10-06 | 1 | 1 |
| [bob-cli-4w.10](bob-cli-4w.10.md) | The bob\_ref agent skill | ✓ closed | small | 2026-10-06 | 1 | 0 |
| [bob-cli-4w.11](bob-cli-4w.11.md) | Live verification, install, and skill deployment on athena | ✓ closed | small | 2026-10-06 | 1 | 0 |
| [bob-cli-4w.2](bob-cli-4w.2.md) | Managed-region and note-anatomy parser | ✓ closed | small | 2026-10-06 | 1 | 1 |
| [bob-cli-4w.3](bob-cli-4w.3.md) | Read-only ref index, reading state, and identity | ✓ closed | medium | 2026-10-06 | 1 | 1 |
| [bob-cli-4w.4](bob-cli-4w.4.md) | bob ref find and the library CLI plumbing | ✓ closed | medium | 2026-10-06 | 1 | 1 |
| [bob-cli-4w.5](bob-cli-4w.5.md) | bob ref list | ✓ closed | medium | 2026-10-06 | 1 | 1 |
| [bob-cli-4w.6](bob-cli-4w.6.md) | bob ref show | ✓ closed | medium | 2026-10-06 | 1 | 1 |
| [bob-cli-4w.7](bob-cli-4w.7.md) | Library health and coverage rows in doctor | ✓ closed | small | 2026-10-06 | 1 | 1 |
| [bob-cli-4w.8](bob-cli-4w.8.md) | Remove leaked marker mirrors and stamp completion dates | ✓ closed | medium | 2026-10-06 | 1 | 1 |
| [bob-cli-4w.9](bob-cli-4w.9.md) | Capture URLs that only a legacy note records | ✓ closed | small | 2026-10-06 | 1 | 1 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-4w: bob ref: a reference library for agents and Bryan [closed]"]
    n1["bob-cli-4w.1: Promote bob ref to the canonical command [closed]"]
    n2["bob-cli-4w.10: The bob_ref agent skill [closed]"]
    n3["bob-cli-4w.11: Live verification, install, and skill deployment on athena [closed]"]
    n4["bob-cli-4w.2: Managed-region and note-anatomy parser [closed]"]
    n5["bob-cli-4w.3: Read-only ref index, reading state, and identity [closed]"]
    n6["bob-cli-4w.4: bob ref find and the library CLI plumbing [closed]"]
    n7["bob-cli-4w.5: bob ref list [closed]"]
    n8["bob-cli-4w.6: bob ref show [closed]"]
    n9["bob-cli-4w.7: Library health and coverage rows in doctor [closed]"]
    n10["bob-cli-4w.8: Remove leaked marker mirrors and stamp completion dates [closed]"]
    n11["bob-cli-4w.9: Capture URLs that only a legacy note records [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n0 --> n6
    n0 --> n7
    n0 --> n8
    n0 --> n9
    n0 --> n10
    n0 --> n11
    n1 -.-> n6
    n1 -.-> n9
    n1 -.-> n10
    n1 -.-> n11
    n2 -.-> n3
    n4 -.-> n5
    n4 -.-> n10
    n5 -.-> n6
    n5 -.-> n9
    n6 -.-> n7
    n7 -.-> n8
    n8 -.-> n2
    n9 -.-> n3
    n10 -.-> n3
    n11 -.-> n2
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-4w.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-4w.1/README.md) | [bob-cli-4w.1](bob-cli-4w.1.md) | 1 |
| [bbugyi200.athena.bob-cli-4w.10](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-4w.10/README.md) | [bob-cli-4w.10](bob-cli-4w.10.md) | 0 |
| [bbugyi200.athena.bob-cli-4w.11](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-4w.11/README.md) | [bob-cli-4w.11](bob-cli-4w.11.md) | 0 |
| [bbugyi200.athena.bob-cli-4w.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-4w.2/README.md) | [bob-cli-4w.2](bob-cli-4w.2.md) | 1 |
| [bbugyi200.athena.bob-cli-4w.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-4w.3/README.md) | [bob-cli-4w.3](bob-cli-4w.3.md) | 1 |
| [bbugyi200.athena.bob-cli-4w.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-4w.4/README.md) | [bob-cli-4w.4](bob-cli-4w.4.md) | 1 |
| [bbugyi200.athena.bob-cli-4w.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-4w.5/README.md) | [bob-cli-4w.5](bob-cli-4w.5.md) | 1 |
| [bbugyi200.athena.bob-cli-4w.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-4w.6/README.md) | [bob-cli-4w.6](bob-cli-4w.6.md) | 1 |
| [bbugyi200.athena.bob-cli-4w.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-4w.7/README.md) | [bob-cli-4w.7](bob-cli-4w.7.md) | 1 |
| [bbugyi200.athena.bob-cli-4w.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-4w.8/README.md) | [bob-cli-4w.8](bob-cli-4w.8.md) | 1 |
| [bbugyi200.athena.bob-cli-4w.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-4w.9/README.md) | [bob-cli-4w.9](bob-cli-4w.9.md) | 1 |
| [bbugyi200.athena.bob-cli-4w.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-4w.land.md) | [bob-cli-4w](README.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ecabc33`](https://github.com/bobs-org/bob-cli/commit/ecabc336ac35611458ce98004a6ece415d7314f2) | feat(highlights\_ref): add read-only managed region parser | [bob-cli-4w.2](bob-cli-4w.2.md) | 2026-10-06 20:48:52 EDT |
| bob-cli | [`42a1792`](https://github.com/bobs-org/bob-cli/commit/42a17926a9ce700634a2ed2ce51228ef4f46e0fd) | feat(ref): promote bob ref to the canonical command | [bob-cli-4w.1](bob-cli-4w.1.md) | 2026-10-06 21:02:53 EDT |
| bob-cli | [`7b60ded`](https://github.com/bobs-org/bob-cli/commit/7b60ded9f056f240f7e0d3db1ae4707a4ab9aab3) | feat(ref-library): add read-only RefRow index module with fixture vault | [bob-cli-4w.3](bob-cli-4w.3.md) | 2026-10-06 21:21:22 EDT |
| bob-cli | [`a34dc02`](https://github.com/bobs-org/bob-cli/commit/a34dc026c04ed47ae0119e6100bad774c5b2dc7d) | feat(ref): capture URLs recorded only by legacy notes with a warning | [bob-cli-4w.9](bob-cli-4w.9.md) | 2026-10-06 21:27:49 EDT |
| bob-cli | [`eaca8b1`](https://github.com/bobs-org/bob-cli/commit/eaca8b14ef506bcc48a282218eb6944561a13efd) | feat(highlights-ref): sync fixes — discard leaked marker mirrors, stamp close dates | [bob-cli-4w.8](bob-cli-4w.8.md) | 2026-10-06 21:39:57 EDT |
| bob-cli | [`e64b2df`](https://github.com/bobs-org/bob-cli/commit/e64b2df2eacf125a30b130266e4287903ce37b44) | feat(ref-doctor): add library health rows to bob ref doctor | [bob-cli-4w.7](bob-cli-4w.7.md) | 2026-10-06 22:07:39 EDT |
| bob-cli | [`87498c7`](https://github.com/bobs-org/bob-cli/commit/87498c7bd7b4da89e0a95c1a693e7aa209d4463c) | feat(ref-library): add bob ref find library-membership verdicts | [bob-cli-4w.4](bob-cli-4w.4.md) | 2026-10-06 22:20:45 EDT |
| bob-cli | [`3642b4a`](https://github.com/bobs-org/bob-cli/commit/3642b4a5c10753bd2013e12eb804a6bd4b74b36d) | feat(ref): add bob ref list reading-queue and filtered library views | [bob-cli-4w.5](bob-cli-4w.5.md) | 2026-10-06 22:56:16 EDT |
| bob-cli | [`e3e69df`](https://github.com/bobs-org/bob-cli/commit/e3e69dfd24c714ad8840ebcc3b806a3b10257848) | feat(ref): add bob ref show with exact resolution and rich row output | [bob-cli-4w.6](bob-cli-4w.6.md) | 2026-10-06 23:26:16 EDT |
| bob-cli | [`6d2911c`](https://github.com/bobs-org/bob-cli/commit/6d2911ce416ad2898f5791ea2e602eb4c40aed54) | fix(ref): land bob-cli-4w with output, identity, hygiene, and docs fixes | [bob-cli-4w](README.md) | 2026-10-07 01:12:05 EDT |
