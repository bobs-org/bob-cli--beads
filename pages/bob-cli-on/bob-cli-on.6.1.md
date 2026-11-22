# Bead: bob-cli-on.6.1 — Requirement bullets in capture (grammar 29)

[Bead Pages](../README.md) / [bob-cli-on.6](bob-cli-on.6.md) / bob-cli-on.6.1

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-on.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.6.md) · **Assignee:** `bob-cli-on.6.1.land`
**Created:** 2026-11-21 13:50:29 EST
**Plan:** [202611/capture\_req\_bullets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_req_bullets.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/capture_req_bullets.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 6 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_req_bullets.md

<!-- sase:links:end -->

## Description

Capture admits requirement bullets at every eligible position and depth, refuses the ineligible ones with taught codes, shows them as req_marker spans, expands a typed `- [` + space into `- [ ] `, and writes them into the reqs zone with the NOTES rule and the first-requirement scoop, completing phase bob-cli-on.6 (capture-reqs).

## Notes

[2026-11-22T03:03:24Z · bob-cli-on.6.1.land] LAND VERIFICATION (bob-cli-on.6.1 land agent, master 3ce97d73): all 5 phases closed; commits 1d89d95f, 7cc94933, c05deef2, 0a623b70, 3ce97d73 reviewed against plan:202611/capture_req_bullets.md and the with_first_note DECISION. Temp-vault walkthrough (dry run then commit): new task with 3 req levels + interleaved notes + drawer -> canonical reqs zone, NOTES created by the first note, REFERENCES after; first req on zero-req @work+ex with 2 loose notes -> scoop into NOTES, then a second capture appended at the end of the reqs zone and filed its note in NOTES; same-line @work+sl [ ] form with children; project-note row with nested reqs + note (## Tasks row, NOTES drawer). capture-parse req_marker depths 1/2/3/1 matched the written bytes; bob task tidy -f json reported 0 changes. Land-agent fixes (committed with this turn): existing-target inserts reported added = number of top-level groups (same-line '[ ] Handles CRLF' + nested req said 'adds 1') while new blocks count every req node — InsertWrite.added now counts every req added, at any depth, with a new reqs_existing test; json-outputs.md now lists existing-task items in requirements[]; task-requirements.md §5 attributes the Obsidian/Mac typing assists to obsidian-gestures/mac-authoring. Accepted as documented contract, not changed: human/JSON dry-run sub_bullets show authored order while the written block is canonical (docs/capture.md says so; the ⌗⌗ summary line previews the NOTES filing). Integration: no commit since the epic started duplicates or conflicts with it (other commits are ref/bank/glossary/albums docs, BOB_MAX_THREADS, and sibling bob-cli-on phases task tidy / rename-drawer / task-split, whose bob task tidy now confirms capture output is canonical). Remaining epic work: lift the TWO_LEVEL_CAP lexical helpers for lines admitted beneath req chains — on a level-3 req line capture-parse needs task_dependency for '&wo' but capture-complete returns no context (editor stuck), and '+query', '@', ',' -> '+', '.' -> '&' all stay inert; proposed as a tale that also performs this epic's closeout.

[2026-11-22T03:03:32Z · bob-cli-on.6.1.land] FOLLOW-UP TRIAGE (land agent): (1) 6.1.2 #1 Mac protocol/capture-previews sub_bullet_depths wording -> not fixable in bob-cli (bob-mac-capture-owned mount; capture-previews.md:165 still says 1 or 2); recorded as DISCOVERED ISSUE on bob-cli-on for bob-cli-on.14 (mac-nesting) / bob-cli-on.13. (2) 6.1.2 #2 TWO_LEVEL_CAP lexical helpers -> caused by this epic (plan depth-model step 3 intended them uncapped); kept as epic work in the proposed tale. (3) 6.1.2 #3 bob capture JSON lacks code for orphaned_nested_bullet / empty_child_after_markers / malformed invalid_child_line -> pre-existing, reproduced on 3ce97d73; no duplicate found; created task bob-cli-p7 (bug, small, ready). (4) 6.1.2 #4, 6.1.3 #1, 6.1.4 #2, 6.1.5 #1 stale tools/docs/tests/test_contracts.py (registry 55 vs 54, llms.txt, README sha) -> caused by bob-cli-on.1 not this epic; already recorded as DISCOVERED ISSUE note #1 on bob-cli-on; still 3 failed/5 passed on 3ce97d73; no new bead. (5) 6.1.4 #1 ^prj NOTES duplicate sections -> reproduced and widened: note captures to a req-owning ^prj write '## NOTES' with tab-indented bullets and add an empty '## NOTES' per capture, and the first-req scoop has the same shape; root cause is note_home/ensure_notes_drawer/scoop_loose_notes from ca070941 (bob-cli-on.3), which predates this epic; the plan told this epic not to change task_block_layout; recorded as DISCOVERED ISSUE on bob-cli-on. (6) Land-agent finding: just docs-check now fails at 'published URLs' on src/native/highlights_ref/podcast/feed.rs:70 (docs/1.0.md in a Podcasting 2.0 namespace literal) from 0c60af45 (bob-cli-os.7) -> recorded as DISCOVERED ISSUE on in-progress epic bob-cli-os. Also noted the numeric AuthoredDepth/LevelGate context on related task bob-cli-fi (third level for drawer notes), which is distinct and stays open. No --epic-symbol entries for bob-cli-on.6.1 or bob-cli-on.6; no just symvision recipe exists.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.6.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.6.1.land.md) | [bob-cli-on.6.1](bob-cli-on.6.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`536455a`](https://github.com/bobs-org/bob-cli/commit/536455acc9f2999bc46aeea8ec021970bdc9b9c9) | fix(capture): count nested requirements added to existing tasks | [bob-cli-on.6.1](bob-cli-on.6.1.md) | 2026-11-21 22:04:20 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-on.6.1.1][1] | Need epic decisions and phases | 2 |
| read-by | [agent:bob-cli-on.6.1.2][2] | Need epic decisions and notes | 2 |
| read-by | [agent:bob-cli-on.6.1.3][3] | Need epic DECISIONS that bind this phase | 3 |
| read-by | [agent:bob-cli-on.6.1.4][4] | Need parent epic decisions governing this phase | 2 |
| read-by | [agent:bob-cli-on.6.1.5][5] | Need the parent epic decisions that govern phase implementation | 1 |
| read-by | [agent:bob-cli-on.6.1.land][6] | Need the epic scope, children, and linked plan file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.6.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.6.1.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.6.1.3/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.6.1.4/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.6.1.5/README.md
[6]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.6.1.land.md

<!-- sase:referenced-by:end -->
