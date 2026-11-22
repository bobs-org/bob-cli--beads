# Bead: bob-cli-on.6.1 — Requirement bullets in capture (grammar 29)

[Bead Pages](../README.md) / [bob-cli-on.6](bob-cli-on.6.md) / bob-cli-on.6.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-on.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.6.md) · **Assignee:** `bob-cli-on.6.1.land`
**Created:** 2026-11-21 13:50:29 EST · **Closed:** 2026-11-22 07:12:59 EST
**Plan:** [202611/capture\_req\_bullets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_req_bullets.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/capture_req_bullets.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | [bead:bob-cli-pe][2] | Proposing bead: its land agent found this while lifting the two-level cap; the shared admission helper req_bullets::admitted_authored_lines is the place list-item child lines are classified |

_Plus 6 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_req_bullets.md
[2]: https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-pe/README.md

<!-- sase:links:end -->

## Description

Capture admits requirement bullets at every eligible position and depth, refuses the ineligible ones with taught codes, shows them as req_marker spans, expands a typed `- [` + space into `- [ ] `, and writes them into the reqs zone with the NOTES rule and the first-requirement scoop, completing phase bob-cli-on.6 (capture-reqs).

## Notes

[2026-11-22T03:03:24Z · bob-cli-on.6.1.land] LAND VERIFICATION (bob-cli-on.6.1 land agent, master 3ce97d73): all 5 phases closed; commits 1d89d95f, 7cc94933, c05deef2, 0a623b70, 3ce97d73 reviewed against plan:202611/capture_req_bullets.md and the with_first_note DECISION. Temp-vault walkthrough (dry run then commit): new task with 3 req levels + interleaved notes + drawer -> canonical reqs zone, NOTES created by the first note, REFERENCES after; first req on zero-req @work+ex with 2 loose notes -> scoop into NOTES, then a second capture appended at the end of the reqs zone and filed its note in NOTES; same-line @work+sl [ ] form with children; project-note row with nested reqs + note (## Tasks row, NOTES drawer). capture-parse req_marker depths 1/2/3/1 matched the written bytes; bob task tidy -f json reported 0 changes. Land-agent fixes (committed with this turn): existing-target inserts reported added = number of top-level groups (same-line '[ ] Handles CRLF' + nested req said 'adds 1') while new blocks count every req node — InsertWrite.added now counts every req added, at any depth, with a new reqs_existing test; json-outputs.md now lists existing-task items in requirements[]; task-requirements.md §5 attributes the Obsidian/Mac typing assists to obsidian-gestures/mac-authoring. Accepted as documented contract, not changed: human/JSON dry-run sub_bullets show authored order while the written block is canonical (docs/capture.md says so; the ⌗⌗ summary line previews the NOTES filing). Integration: no commit since the epic started duplicates or conflicts with it (other commits are ref/bank/glossary/albums docs, BOB_MAX_THREADS, and sibling bob-cli-on phases task tidy / rename-drawer / task-split, whose bob task tidy now confirms capture output is canonical). Remaining epic work: lift the TWO_LEVEL_CAP lexical helpers for lines admitted beneath req chains — on a level-3 req line capture-parse needs task_dependency for '&wo' but capture-complete returns no context (editor stuck), and '+query', '@', ',' -> '+', '.' -> '&' all stay inert; proposed as a tale that also performs this epic's closeout.

[2026-11-22T03:03:32Z · bob-cli-on.6.1.land] FOLLOW-UP TRIAGE (land agent): (1) 6.1.2 #1 Mac protocol/capture-previews sub_bullet_depths wording -> not fixable in bob-cli (bob-mac-capture-owned mount; capture-previews.md:165 still says 1 or 2); recorded as DISCOVERED ISSUE on bob-cli-on for bob-cli-on.14 (mac-nesting) / bob-cli-on.13. (2) 6.1.2 #2 TWO_LEVEL_CAP lexical helpers -> caused by this epic (plan depth-model step 3 intended them uncapped); kept as epic work in the proposed tale. (3) 6.1.2 #3 bob capture JSON lacks code for orphaned_nested_bullet / empty_child_after_markers / malformed invalid_child_line -> pre-existing, reproduced on 3ce97d73; no duplicate found; created task bob-cli-p7 (bug, small, ready). (4) 6.1.2 #4, 6.1.3 #1, 6.1.4 #2, 6.1.5 #1 stale tools/docs/tests/test_contracts.py (registry 55 vs 54, llms.txt, README sha) -> caused by bob-cli-on.1 not this epic; already recorded as DISCOVERED ISSUE note #1 on bob-cli-on; still 3 failed/5 passed on 3ce97d73; no new bead. (5) 6.1.4 #1 ^prj NOTES duplicate sections -> reproduced and widened: note captures to a req-owning ^prj write '## NOTES' with tab-indented bullets and add an empty '## NOTES' per capture, and the first-req scoop has the same shape; root cause is note_home/ensure_notes_drawer/scoop_loose_notes from ca070941 (bob-cli-on.3), which predates this epic; the plan told this epic not to change task_block_layout; recorded as DISCOVERED ISSUE on bob-cli-on. (6) Land-agent finding: just docs-check now fails at 'published URLs' on src/native/highlights_ref/podcast/feed.rs:70 (docs/1.0.md in a Podcasting 2.0 namespace literal) from 0c60af45 (bob-cli-os.7) -> recorded as DISCOVERED ISSUE on in-progress epic bob-cli-os. Also noted the numeric AuthoredDepth/LevelGate context on related task bob-cli-fi (third level for drawer notes), which is distinct and stays open. No --epic-symbol entries for bob-cli-on.6.1 or bob-cli-on.6; no just symvision recipe exists.

[2026-11-22T12:12:59Z · bob-cli-on.6.1.land] LANDED (second land agent, on master 2f4fef6d). This turn implemented the approved tale plan:202611/req_chain_lexical_helpers.md (its coder never ran) and closed out the epic.

Step 1, verify:
- All 5 phases are closed. I re-read every child note; all were addressed.
- Epic commits: 1d89d95f, 7cc94933, c05deef2, 0a623b70, 3ce97d73, plus the first lander's 536455ac (it made requirements[].added count nested requirements on existing targets).
- The first lander's walkthrough (note #1) stands.
- Re-smoked on the final binary:
  - A 3-level requirement chain with an `&work:wo` on the level-3 line wrote the canonical reqs zone, filed its note under NOTES, and added the Depends On line. `bob task tidy` reported 0 changes.
  - A complete `&work:wo` on a level-3 line writes the same task line as on level 2.

Remaining epic work, done here:
- The task-host lexical helpers now read lines admitted beneath a requirement chain at level 3+ exactly like level 2.
- New `req_bullets::admitted_authored_lines` (plus `child_bullet_cap`) shares the parsers' `LevelGate`, including the list shift. `scan_item_dependencies` was refactored onto it.
- Lifted onto the helper:
  - completion.rs child-line branch;
  - tokens.rs `parent_task_selector_tokens`;
  - item.rs target-run loops (both) and `child_seals_note` (×3), plus the editor_parse.rs `child_seals_note`;
  - type_marker.rs and directive.rs `collect_item` / `completion_at` (an item-aware bullet-prefix cap);
  - rewrite.rs `candidate_selects_plain_marker` (the separator toggle failed at level 3).
- Result: `&`, `*`, `~`, `+`, `@`, and `#` pickers; `capture-parse` needs; `,`→`+`, `.`→`&`, and `@route+id^`/`:`/`.` toggles; and leading `#type`/`%c` on deep requirement lines all match level 2. `capture-parse` needs and `capture-complete` context now agree, so the editor is no longer stuck on `&wo` at level 3.
- Kept capped, with reasons:
  - `marker_only_child_lines` — lifting it hid deep rows from refusals in ineligible hosts (`@work#Tasks` started accepting a deep `- #fix`), and changed nothing in task hosts;
  - `expand_dot_block_id_alias` (first-level move bullets only);
  - `deletion_line_context` (no failing case);
  - project-note ID helpers (IDs on nested bullets are refused);
  - editor drawer grouping and the relationship diagnostic range;
  - every notebook, record, close-log, section, and Pomodoro site.

Tests and gates:
- New tests: src/native/capture_language/tests/reqs_lexical.rs (6) and tests/cli/capture/reqs_lexical.rs (6).
- Docs: capture.md (requirement-bullets section); `capture-complete` long help; `just docs-gen` regenerated the reference.
- `just check` passed: fmt, clippy, lib 7819, cli 3991, 0 failures.
- `just docs-check`: lint, drift, strict build, published URLs, lychee, and search smoke pass. The only failures are the 3 tools/docs/tests/test_contracts.py assertions (registry 55 vs 54). They reproduce on a clean 2f4fef6d tree and are already recorded on bob-cli-on.
- Baseline-vs-new binary diff of capture-parse, `capture --dry-run`, and capture-complete/capture-rewrite at every cursor:
  - 31 refused deep drafts, 2100 outputs: byte-identical except one ineligible `@work+ex %n` draft, where `&wo` completion now matches the `needs: task_dependency` that capture-parse already reported.

Deviation from the tale's "ineligible hosts unchanged" invariant (accepted): the admission gate stays lexical and host-agnostic, as the plan's design and the parsers' own gate are. So in `%n`, `x`, `=`, notebook, and notes-list items, a deep checkbox chain the host still refuses now gets the same pickers and typing aliases as its level-2 line. Every such item still refuses at capture time; none flipped from refused to accepted across 90 host drafts.

Step 2, integrate: commits since the last landing (e5ee4a8d task-reqs §5 Obsidian table; 145b00d5 prose `((` completion; dbedc651, 900772d9, 005f4c2b, 2f4fef6d ref/podcast work) neither conflict with nor duplicate this epic. The prose `((` detector is separate from the capture child-line helpers.

Step 3, follow-ups: the first lander's triage stands (note #2: Mac protocol docs → bob-cli-on; bob-cli-p7 created; stale docs contract tests → bob-cli-on note #1; ^prj NOTES → bob-cli-on; feed URL → bob-cli-os, now passing). New this turn: task-list child lines open no `&`/`*`/`~`/`@` picker and capture-parse reports no needs, although bob capture accepts the modifier. It is pre-existing at free levels and not caused by this epic, so I created task bob-cli-pe (bug, medium, ready), linked to this bead.

No --epic-symbol entries for bob-cli-on.6.1 or bob-cli-on.6, and there is no `just symvision` recipe.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.6.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.6.1.land/README.md) | [bob-cli-on.6.1](bob-cli-on.6.1.md) | 3 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`536455a`](https://github.com/bobs-org/bob-cli/commit/536455acc9f2999bc46aeea8ec021970bdc9b9c9) | fix(capture): count nested requirements added to existing tasks | [bob-cli-on.6.1](bob-cli-on.6.1.md) | 2026-11-21 22:04:20 EST |
| bob-cli | [`ffeae19`](https://github.com/bobs-org/bob-cli/commit/ffeae199611e17eb6d8367e9a66ddee1e8c2aac4) | fix(capture): read deep requirement-chain lines like level 2 in completion, selectors, and aliases | [bob-cli-on.6.1](bob-cli-on.6.1.md) | 2026-11-22 07:14:25 EST |
| bob-cli--plans | [`bob-cli--plans@68b6574`](https://github.com/bobs-org/bob-cli--plans/commit/68b6574091c051ec55d70083c50cb0069dc17a25) | docs(plans): mark the capture requirement-bullets epic and its lexical-helpers tale done | [bob-cli-on.6.1](bob-cli-on.6.1.md) | 2026-11-22 07:15:18 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-on.6.1.1][1] | Need epic decisions and phases | 2 |
| read-by | [agent:bob-cli-on.6.1.2][2] | Need epic decisions and notes | 2 |
| read-by | [agent:bob-cli-on.6.1.3][3] | Need epic DECISIONS that bind this phase | 3 |
| read-by | [agent:bob-cli-on.6.1.4][4] | Need parent epic decisions governing this phase | 2 |
| read-by | [agent:bob-cli-on.6.1.5][5] | Need the parent epic decisions that govern phase implementation | 1 |
| read-by | [agent:bob-cli-on.6.1.land][6] | Need the epic scope, children, and linked plan file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.6.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.6.1.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.6.1.3/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.6.1.4/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.6.1.5/README.md
[6]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.6.1.land.md

<!-- sase:referenced-by:end -->
