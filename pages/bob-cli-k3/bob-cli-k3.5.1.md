# Bead: bob-cli-k3.5.1 — Keep each album's records index current

[Bead Pages](../README.md) / [bob-cli-k3.5](bob-cli-k3.5.md) / bob-cli-k3.5.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-k3.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-k3.5.md) · **Assignee:** `bob-cli-k3.5.1.land`
**Created:** 2026-11-11 13:48:49 EST · **Closed:** 2026-11-11 18:17:45 EST
**Plan:** [202611/album\_records\_index.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/album_records_index.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/album_records_index.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | file:explicit:061f2ab2ef1ce5bfc4660e3b | attached via sase artifact create --bead |
| related | file:explicit:5353c7f0e5bab132ebba1cc7 | attached via sase artifact create --bead |
| related | file:explicit:653de3c666f7c5264ea02ada | attached via sase artifact create --bead |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/album_records_index.md

<!-- sase:links:end -->

## Description

Complete bob-cli-k3.5: albums show a deterministic grouped records index, every album-backed record write updates it atomically, and albums sync plus nightly repair stale indexes with guarded writes and accurate reports.

## Notes

[2026-11-11T22:42:55Z · bob-cli-k3.5.1.land] FOLLOW-UP TRIAGE (all phase proposals): Read .1 notes #1-2, .2 notes #1-4, and .3 notes #1-2. For .1 #1 / .2 #3 / .3 #1, independently ran just docs-check on bc3983d3: only capture-panel 6265, capture-previews 6244, keyboard 6083, protocol 6294, and navigation-hotkeys 6200 exceed 6000. Added +1 evidence identifying all proposing beads to existing bob-cli-jz and bob-cli-h9; active bob-cli-kj.2 already owns their remediation, and did not cause these pre-existing failures. No duplicate task or DISCOVERED ISSUE on that remediation epic. Ledger-tools is no longer reported; added resolution evidence to existing headroom task bob-cli-il, declined stale-failure +1/new task. capture-syntax is now 6000 after bc3983d3; json-outputs is 5965 after phase .3 and subsequent trims: declined new tasks for resolved overages. .2 #2 is fixed by 6e3d8837 (vault_git tests now last; current check passed Clippy). .2 #1 is fixed by 4771047e pathspec handling; all seven named vault_sync tests passed in current check run 6a224703ed20d7ef538696dabc0c3928, so declined historical duplicate tasks. All proposals are settled; remaining defects found by this audit are epic-caused and will be repaired in the landing tale.

[2026-11-11T22:43:56Z · bob-cli-k3.5.1.land] LAND AUDIT on bc3983d3: Read every child note, both approved plans and required research; inspected source and epic commits 1f4c9457/b79ea376/6352824b. No independent DECISIONS on this child; parent decisions honored (ledger/glossary work later, albums decision memory declined). Reviewed all eight non-epic commits since 1f4c9457; origin/master fetched and equals HEAD. Partial registry refusal, generic guarded writer/rollback, catalog registration, and nightly ordering coexist correctly; bank/plugin/task-mark/keep-moving work needs no new album consumer. No epic-symbol entries, no symvision recipe. just check PASSED (run 6a224703ed20d7ef538696dabc0c3928, 599808 ms). just docs-check has only the five already-triaged mounted budgets. Isolated walkthrough PASSED: two captures + update in one batch, records new/update, index/report agreement, hand-edited index preview/repair, scoped albums commit, repeat-sync no-op, owner/unrelated bytes unchanged. Remaining epic-caused defects: (1) write planner drops damaged findings and omits member NoteRead completeness; both capture and records new succeed with a .md directory occupant and leave album unchanged, or publish fallback rows from unreadable UTF-8 members; (2) batch album_files.before is intermediate and state stale instead of original/missing, net-zero edits still reported, and original album guard can disappear on net-zero final staging; human preview prints whole album instead of promised diff; (3) raw plural/choice tally newlines produce an unquoted ## Injected heading outside the callout. Executable reproducer file:explicit:061f2ab2ef1ce5bfc4660e3b; actual results file:explicit:5353c7f0e5bab132ebba1cc7. Body-only invalid UTF-8 was also tested: sync conservatively refuses partial discovery, consistent with its guard policy, so no separate defect proposed. One medium landing-repair tale covers only these gaps and owns final closeout, including parent phase bob-cli-k3.5; keep both open until repaired.

[2026-11-11T23:17:45Z · bob-cli-k3.5.1.land] Landing repairs complete on top of audited baseline bc3983d3 (origin/master). Reviewed epic commits 1f4c9457/b79ea376/6352824b and non-epic bffbf36b/4771047e/8134d173/6e3d8837/03a0aba2/6a88d810/ee2d2cbf/bc3983d3; preserved shared renderer, route-local lookup, one folder scan per batch, notebook region bytes, JSON schema v1, guarded writer; no new commands/catalogs/plugins/migrations/memory. (1) Unsafe index refusal: new albums::write::folder_complete shared with report (folder diagnostics plus member NoteRead); AlbumWritePlan carries findings; capture stage_album_index and records plan_album_write_for_record refuse Damaged with path/reason before any dir creation or write; readable invalid YAML still counted with fallback, I/O and invalid-UTF8 refuse. (2) Batch final bytes: CaptureRecordContext::record_album_edit keeps original before/state and advances after; capture plan derives album_files from planner loaded_texts original/current, drops net-zero but guards preimage; human dry-run shows unified similar-TextDiff (context 3, a/path b/path) in print_album_files and print_album_dry_run; JSON before/after and item cards stable. (3) Tally inert: tally_text/tally_fragment apply inert_text to plural and lowered labels including empty-album; header stays one physical line; replan is no-op. Tests: new write damaged_folder_and_unreadable_member_are_damaged, index hostile_plural_and_choice_labels_stay_on_one_inert_line, 5 capture album_index tests (damaged refusal, unreadable vs malformed, later-item atomicity, missing preimage/state, net-zero guard), 3 records CLI tests (damaged new/update+dry-run, unreadable vs malformed, human diff); focused gates green (73 albums+capture, 53 capture::record, 27 albums/sync, 3 new records); sase tool run check succeeded (b80ca989, 409738ms); docs-check strict build still red on pre-existing page/anchor issues in untouched docs (no new failures; word-budget triage unchanged). Walkthrough in isolated vault: batch 2 captures plus update, records new/update, albums list agrees, sync preview, owner body.md byte-identical. Follow-up triage carried: word-budget overages (6265/6244/6083/6200) on bob-cli-jz and protocol 6294 on bob-cli-h9 owned by bob-cli-kj.2 (no duplicates); ledger-tools overage gone with evidence on bob-cli-il; capture-syntax 6000 and json-outputs 5965 resolved (declined); vault_git items_after fixed by 6e3d8837; seven vault-sync root cause fixed by 4771047e. Extension point for owner-catalog phase: albums::sync::plan_indexes / IndexSyncPlan.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-k3.5.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-k3.5.1.land.md) | [bob-cli-k3.5.1](bob-cli-k3.5.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`300a6e8`](https://github.com/bobs-org/bob-cli/commit/300a6e81005263311408fac024038a12a50fd62d) | feat(albums): finish index write safety and preview parity | [bob-cli-k3.5.1](bob-cli-k3.5.1.md) | 2026-11-11 18:19:33 EST |
| bob-cli--plans | [`bob-cli--plans@3fb7c92`](https://github.com/bobs-org/bob-cli--plans/commit/3fb7c92ac664441a58dc057714133101ec4cff40) | docs(plans): mark album index plan done | [bob-cli-k3.5.1](bob-cli-k3.5.1.md) | 2026-11-11 18:20:19 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-k3.5.1.1][1] | Need parent epic DECISIONS and child-epic constraints | 1 |
| read-by | [agent:bob-cli-k3.5.1.3][2] | Need the child epic's final decisions for this index-sync phase | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-k3.5.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-k3.5.1.3/README.md

<!-- sase:referenced-by:end -->
