# Bead: bob-cli-on — Task requirements (reqs)

[Bead Pages](../README.md) / bob-cli-on

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1ex](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1ex.md) · **Assignee:** `bob-cli-on.land`
**Created:** 2026-11-21 11:13:26 EST
**Plan:** [202611/task\_requirements.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_requirements.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/task_requirements.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 19 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_requirements.md

<!-- sase:links:end -->

## Description

A task can carry requirements: checkbox children without `#task`, nested as deep as the work needs, drawn as a quiet ⌗⌗ run in the task's ink. They are met when the task closes and can never be ticked early. They can be dropped with a reason or carried into their own task, and the close card audits them once. They sit in one canonical block order beside a NOTES drawer, and they promote one level at a time into project tasks. bob-cli, bob-plugins, Bob Mac Capture, and the vault agree byte for byte through shared vectors, and every legacy REQUIREMENTS drawer becomes NOTES.

## Notes

[2026-11-21T19:54:07Z · bob-cli-o6.6.1.land] DISCOVERED ISSUE: bob-cli a0961435 (bob-cli-on.1, req-contract) registered docs/task-requirements.md as a contract without updating the bob-docs contract tests, so tools/docs/tests/test_contracts.py fails 3/8 on master dfe20ca3: test_current_registry_and_generated_nav_are_complete_and_unique (registry has 55 entries, test expects 54), test_llmstxt_contracts_section_lists_exactly_registry_stems (index 46 'task-split.md' != 'task-requirements.md'), and test_readme_table_matches_original_contract_index_snapshot (README table sha f23b0e44... != pinned 34f4f8a4...). Repro: uv run --project tools/docs pytest -q tools/docs/tests/test_contracts.py. It is masked today only because just docs-check stops earlier at the reference word-budget lint. Proposed by bob-cli-o6.6.1.5 note #2 (also reproduced on clean base 250c3053 with that phase's docs stashed; evidence file:explicit:282423e57c9f033d6cf61ecc, bobcli-docs-postlint.log); re-verified on dfe20ca3 by the bob-cli-o6.6.1 land agent. Fix belongs with this epic: bump the expected count, the llms.txt list, and the README snapshot, following the precedent of bob-cli-hs.

[2026-11-22T02:50:55Z · bob-cli-on.6.1.land] DISCOVERED ISSUE (from bob-cli-on.6.1.4 PROPOSED FOLLOW-UP #1, reproduced and widened by the bob-cli-on.6.1 land agent on master 3ce97d73): NOTES routing for a req-owning ^prj task writes into an H2 '## NOTES' section with task-style tab indentation and duplicates the heading. Repro in a scratch vault: pk.md = frontmatter type [[project]] + '- [ ] #task #prj Pk root ^prj' / '\t- [ ] hand req' / '## Tasks' / '- [ ] #task Row a'. 'bob capture -- $'@pk+prj\n- first note'' appends '## NOTES\n\t- first note' at end of file (a tab-indented bullet straight under an H2 reads as an indented code block); a second note capture yields '## NOTES\n\t- first note\n\n\t- second note\n## NOTES\n' (an extra empty '## NOTES' per capture). The first-req scoop has the same shape: '@pm+prj\n- [ ] only req' on a ^prj with a loose note writes '## NOTES\n\t- loose'. Root cause predates bob-cli-on.6.1: note_home / ensure_notes_drawer / scoop_loose_notes (ca070941, bob-cli-on.3 block-layout) treat project_h2_drawers H2 sections as task drawers but write tab-indented children and mis-detect the section end. bob-cli-on.6.1 only made it reachable from requirement capture to ^prj targets (the plan said to record a follow-up rather than change task_block_layout there). Needs a decided ^prj notes home ('## Notes' H2 with column-zero bullets, matching the promotion/migration sections of plan:202611/task_requirements.md) in task_block_layout and its JS twin + RL vectors, then capture, toggle, and tidy follow it.

[2026-11-22T02:51:05Z · bob-cli-on.6.1.land] DISCOVERED ISSUE (from bob-cli-on.6.1.2 PROPOSED FOLLOW-UP #1, re-verified by the bob-cli-on.6.1 land agent): capture grammar 29 (7cc94933) lets sub_bullet_depths exceed 2 beneath requirements, but the bob-mac-capture-owned mounted docs still say otherwise: docs/capture-previews.md:165 reads 'sub_bullet_depths (1 or 2)' and docs/protocol.md:382 describes depth handling for 'sub_bullet_depths' without the deeper levels. These files live in bob-mac-capture (gitignored mount in bob-cli), so the edit belongs with the Mac phases: bob-cli-on.14 (mac-nesting, which generalizes the Mac to any authored depth) should update that wording, and bob-cli-on.13 (mac-authoring) already owns docs/protocol.md for req_marker depth. bob-cli's own docs (capture.md, json-outputs.md, capture-syntax.md) already state depths may exceed 2.

[2026-11-22T03:18:27Z · bob-cli-on.10.1.land] DISCOVERED ISSUE (corroboration from the bob-cli-on.10.1 land agent): (a) note #1's docs contract tests still fail 3/8 on master e5ee4a8d — reproduced with 'uv run --project tools/docs python -m pytest tools/docs/tests/test_contracts.py -q' (registry 55 vs pinned 54, llms.txt list, README table sha f23b0e44…); also reported by bob-cli-on.10.1.3 note #1 and bob-cli-on.10.1.5 note #1. (b) note #2's ^prj NOTES home was found independently by bob-cli-on.10.1.1 (note #1) while porting the RL twin, which mirrors it on purpose: for a ^prj task file_into_notes -> ensure_notes_drawer -> capture_drawers::ensure_drawer takes the is_prj_parent path, appends '## NOTES' at EOF, and because drawers() lists only bullet drawers an existing '## NOTES' H2 is never found, so each write appends another empty heading. bob task tidy refuses such plans through content_preserved, but the RW writers (toggle note->req first-req scoop, insert_reqs) have no such guard, and no RL/RW vector covers ^prj. Whatever home bob-cli decides needs new RL/RW vectors re-copied into the cycler and nav twins (plugins/task-status-cycler/src/196-197, nav 696-697, byte-identical; scripts/test-task-reqs-twin-copies.cjs enforces it).

[2026-11-22T09:05:24Z · bob-cli-os.land] DISCOVERED ISSUE (corroboration from the bob-cli-os land agent): the 3 tools/docs/tests/test_contracts.py failures recorded in this epic's notes still reproduce on master 2f4fef6d (test_current_registry_and_generated_nav_are_complete_and_unique, test_llmstxt_contracts_section_lists_exactly_registry_stems, test_readme_table_matches_original_contract_index_snapshot; 3 failed, 5 passed via tools/docs/.venv/bin/python -m pytest tools/docs/tests/test_contracts.py). bob-cli-os.5 (note #1), bob-cli-os.9 (note #1), and bob-cli-os.10 (note #3) also hit them during unrelated podcast work.

[2026-11-22T17:31:44Z · research.5u.final] DISCOVERED ISSUE: Mac req_marker concealment has no caret-adjacency reveal, diverging from docs/task-requirements.md §4 ('Caret adjacency reveals the raw bytes', mac-authoring/.13). Verified on bob-mac-capture master: requirementMarkerSpans() and the .clear concealment branch (CapturePanelModel.swift ~1941, ~22969) have no caret gate, so [ ] stays concealed and the caret walks invisibly across 4 transparent cells; only Backspace (consumeRequirementMarkerBackspace) inspects the caret. Found during display-redesign research (gem report file:explicit:0b89e18a8325cc0993d97840, lead verification file:explicit:5c353b4ff461108eaf7e16eb §3.4). Same research also verified wrappingOrigin counts chars with no word-wrap awareness and the ZStack overlay sits outside the editor scroll view — drift/desync risk shared with the route-emoji overlay.

[2026-11-22T17:31:51Z · research.5u.final] DISCOVERED ISSUE: capture dry-run preview shows the authored layout, not the NOTES-scooped write. cld researcher reproduction (installed bob 0.5.0, scratch vault): dry-running a task with reqs plus a loose '- note' child lists the note as a loose child in human output and sub_bullets JSON while the summary says 'files 1 note under NOTES'; the real write files it under NOTES, so the Mac preview stack renders a block that differs from what lands. Evidence: cld report file:explicit:9cb60732bf9ab7a6de1c0bf0 (Side findings §1), consolidated report file:explicit:5c353b4ff461108eaf7e16eb §4.9. A fix could also add the additive req/kind field on preview lines proposed there.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-on.1](bob-cli-on.1.md) | Requirement recognizer, shared vectors, and the contract page | ✓ closed | medium | 2026-11-21 | 1 | 1 |
| [bob-cli-on.10](bob-cli-on.10.md) | Obsidian requirement guards, toggle, drop, and typing assist | ✓ closed | large | 2026-11-21 | 1 | 0 |
| [bob-cli-on.11](bob-cli-on.11.md) | Requirements on the Obsidian successor card and carry-now | ✓ closed | large | 2026-11-21 | 1 | 0 |
| [bob-cli-on.12](bob-cli-on.12.md) | Promotion maps requirements to tasks and notes to notes | ✓ closed | medium | 2026-11-21 | 1 | 1 |
| [bob-cli-on.13](bob-cli-on.13.md) | Mac requirement typing and glyph overlay | ✓ closed | medium | 2026-11-21 | 1 | 0 |
| [bob-cli-on.14](bob-cli-on.14.md) | Mac bullet indentation beyond two levels | ✓ closed | medium | 2026-11-21 | 1 | 0 |
| [bob-cli-on.15](bob-cli-on.15.md) | Requirements on the Mac Pull-In card | ✓ closed | large | 2026-11-21 | 1 | 0 |
| [bob-cli-on.16](bob-cli-on.16.md) | Reviewed vault migration | ✓ closed | small | 2026-11-21 | 1 | 0 |
| [bob-cli-on.17](bob-cli-on.17.md) | Memory records for task requirements | ✓ closed | small | 2026-11-21 | 1 | 1 |
| [bob-cli-on.2](bob-cli-on.2.md) | Keep every task reader and outside-text writer off requirement lines | ✓ closed | medium | 2026-11-21 | 1 | 1 |
| [bob-cli-on.3](bob-cli-on.3.md) | The task block layout module and requirement line writers | ✓ closed | medium | 2026-11-21 | 1 | 1 |
| [bob-cli-on.4](bob-cli-on.4.md) | The bob task tidy command | ✓ closed | medium | 2026-11-21 | 1 | 1 |
| [bob-cli-on.5](bob-cli-on.5.md) | The bob task rename-drawer command | ✓ closed | medium | 2026-11-21 | 1 | 1 |
| [bob-cli-on.6](bob-cli-on.6.md) | Capture grammar, spans, typing rewrite, and NOTES routing for requirements | ✓ closed | large | 2026-11-21 | 1 | 0 |
| [bob-cli-on.7](bob-cli-on.7.md) | Carry a requirement branch into its own task | ✓ closed | medium | 2026-11-21 | 1 | 1 |
| [bob-cli-on.8](bob-cli-on.8.md) | Requirements on the capture successor card | ✓ closed | large | 2026-11-21 | 1 | 0 |
| [bob-cli-on.9](bob-cli-on.9.md) | Render requirements in Obsidian | ✓ closed | medium | 2026-11-21 | 1 | 1 |

## Dependencies

- **Blocks:** [bob-cli-ph.1](../bob-cli-ph/bob-cli-ph.1.md) ◐ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.1/README.md) | [bob-cli-on.1](bob-cli-on.1.md) | 1 |
| [bbugyi200.athena.bob-cli-on.10](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.10.md) | [bob-cli-on.10](bob-cli-on.10.md) | 0 |
| [bbugyi200.athena.bob-cli-on.10.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.10.1.1/README.md) | [bob-cli-on.10.1.1](bob-cli-on.10.1.1.md) | 0 |
| [bbugyi200.athena.bob-cli-on.10.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.10.1.2/README.md) | [bob-cli-on.10.1.2](bob-cli-on.10.1.2.md) | 0 |
| [bbugyi200.athena.bob-cli-on.10.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.10.1.3/README.md) | [bob-cli-on.10.1.3](bob-cli-on.10.1.3.md) | 0 |
| [bbugyi200.athena.bob-cli-on.10.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.10.1.4/README.md) | [bob-cli-on.10.1.4](bob-cli-on.10.1.4.md) | 0 |
| [bbugyi200.athena.bob-cli-on.10.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.10.1.5/README.md) | [bob-cli-on.10.1.5](bob-cli-on.10.1.5.md) | 0 |
| [bbugyi200.athena.bob-cli-on.10.1.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.10.1.6/README.md) | [bob-cli-on.10.1.6](bob-cli-on.10.1.6.md) | 1 |
| [bbugyi200.athena.bob-cli-on.10.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.10.1.land.md) | [bob-cli-on.10.1](bob-cli-on.10.1.md) | 1 |
| [bbugyi200.athena.bob-cli-on.11](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.11.md) | [bob-cli-on.11](bob-cli-on.11.md) | 0 |
| [bbugyi200.athena.bob-cli-on.11.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.11.1.1/README.md) | [bob-cli-on.11.1.1](bob-cli-on.11.1.1.md) | 0 |
| [bbugyi200.athena.bob-cli-on.11.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.11.1.2/README.md) | [bob-cli-on.11.1.2](bob-cli-on.11.1.2.md) | 0 |
| [bbugyi200.athena.bob-cli-on.11.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.11.1.3.md) | [bob-cli-on.11.1.3](bob-cli-on.11.1.3.md) | 1 |
| [bbugyi200.athena.bob-cli-on.11.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.11.1.4/README.md) | [bob-cli-on.11.1.4](bob-cli-on.11.1.4.md) | 0 |
| [bbugyi200.athena.bob-cli-on.11.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.11.1.5/README.md) | [bob-cli-on.11.1.5](bob-cli-on.11.1.5.md) | 0 |
| [bbugyi200.athena.bob-cli-on.11.1.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.11.1.6.md) | [bob-cli-on.11.1.6](bob-cli-on.11.1.6.md) | 1 |
| [bbugyi200.athena.bob-cli-on.11.1.7.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.11.1.7.1/README.md) | [bob-cli-on.11.1.7.1](bob-cli-on.11.1.7.1.md) | 0 |
| [bbugyi200.athena.bob-cli-on.11.1.7.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.11.1.7.2.md) | [bob-cli-on.11.1.7.2](bob-cli-on.11.1.7.2.md) | 1 |
| [bbugyi200.athena.bob-cli-on.11.1.7.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.11.1.7.land.md) | [bob-cli-on.11.1.7](bob-cli-on.11.1.7.md) | 2 |
| [bbugyi200.athena.bob-cli-on.11.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.11.1.land.md) | [bob-cli-on.11.1](bob-cli-on.11.1.md) | 0 |
| [bbugyi200.athena.bob-cli-on.12](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.12/README.md) | [bob-cli-on.12](bob-cli-on.12.md) | 1 |
| [bbugyi200.athena.bob-cli-on.13](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.13.md) | [bob-cli-on.13](bob-cli-on.13.md) | 0 |
| [bbugyi200.athena.bob-cli-on.14](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.14/README.md) | [bob-cli-on.14](bob-cli-on.14.md) | 0 |
| [bbugyi200.athena.bob-cli-on.15](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.15.md) | [bob-cli-on.15](bob-cli-on.15.md) | 0 |
| [bbugyi200.athena.bob-cli-on.15.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.15.1.1/README.md) | [bob-cli-on.15.1.1](bob-cli-on.15.1.1.md) | 0 |
| [bbugyi200.athena.bob-cli-on.15.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.15.1.2/README.md) | [bob-cli-on.15.1.2](bob-cli-on.15.1.2.md) | 0 |
| [bbugyi200.athena.bob-cli-on.15.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.15.1.3.md) | [bob-cli-on.15.1.3](bob-cli-on.15.1.3.md) | 0 |
| [bbugyi200.athena.bob-cli-on.15.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.15.1.4.md) | [bob-cli-on.15.1.4](bob-cli-on.15.1.4.md) | 0 |
| [bbugyi200.athena.bob-cli-on.15.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.15.1.5.md) | [bob-cli-on.15.1.5](bob-cli-on.15.1.5.md) | 1 |
| [bbugyi200.athena.bob-cli-on.15.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.15.1.land/README.md) | [bob-cli-on.15.1](bob-cli-on.15.1.md) | 2 |
| [bbugyi200.athena.bob-cli-on.16](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.16.md) | [bob-cli-on.16](bob-cli-on.16.md) | 0 |
| [bbugyi200.athena.bob-cli-on.17](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.17/README.md) | [bob-cli-on.17](bob-cli-on.17.md) | 1 |
| [bbugyi200.athena.bob-cli-on.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.2.md) | [bob-cli-on.2](bob-cli-on.2.md) | 1 |
| [bbugyi200.athena.bob-cli-on.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.3/README.md) | [bob-cli-on.3](bob-cli-on.3.md) | 1 |
| [bbugyi200.athena.bob-cli-on.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.4/README.md) | [bob-cli-on.4](bob-cli-on.4.md) | 1 |
| [bbugyi200.athena.bob-cli-on.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.5/README.md) | [bob-cli-on.5](bob-cli-on.5.md) | 1 |
| [bbugyi200.athena.bob-cli-on.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.6.md) | [bob-cli-on.6](bob-cli-on.6.md) | 0 |
| [bbugyi200.athena.bob-cli-on.6.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.6.1.1/README.md) | [bob-cli-on.6.1.1](bob-cli-on.6.1.1.md) | 1 |
| [bbugyi200.athena.bob-cli-on.6.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.6.1.2/README.md) | [bob-cli-on.6.1.2](bob-cli-on.6.1.2.md) | 1 |
| [bbugyi200.athena.bob-cli-on.6.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.6.1.3/README.md) | [bob-cli-on.6.1.3](bob-cli-on.6.1.3.md) | 1 |
| [bbugyi200.athena.bob-cli-on.6.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.6.1.4/README.md) | [bob-cli-on.6.1.4](bob-cli-on.6.1.4.md) | 1 |
| [bbugyi200.athena.bob-cli-on.6.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.6.1.5/README.md) | [bob-cli-on.6.1.5](bob-cli-on.6.1.5.md) | 1 |
| [bbugyi200.athena.bob-cli-on.6.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.6.1.land/README.md) | [bob-cli-on.6.1](bob-cli-on.6.1.md) | 3 |
| [bbugyi200.athena.bob-cli-on.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.7/README.md) | [bob-cli-on.7](bob-cli-on.7.md) | 1 |
| [bbugyi200.athena.bob-cli-on.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.8.md) | [bob-cli-on.8](bob-cli-on.8.md) | 0 |
| [bbugyi200.athena.bob-cli-on.8.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.8.1.1/README.md) | [bob-cli-on.8.1.1](bob-cli-on.8.1.1.md) | 1 |
| [bbugyi200.athena.bob-cli-on.8.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.8.1.2/README.md) | [bob-cli-on.8.1.2](bob-cli-on.8.1.2.md) | 1 |
| [bbugyi200.athena.bob-cli-on.8.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.8.1.3/README.md) | [bob-cli-on.8.1.3](bob-cli-on.8.1.3.md) | 1 |
| [bbugyi200.athena.bob-cli-on.8.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.8.1.4/README.md) | [bob-cli-on.8.1.4](bob-cli-on.8.1.4.md) | 1 |
| [bbugyi200.athena.bob-cli-on.8.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.8.1.5.md) | [bob-cli-on.8.1.5](bob-cli-on.8.1.5.md) | 1 |

… and 4 more agents

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a096143`](https://github.com/bobs-org/bob-cli/commit/a0961435506e4810841527ecd0b81505cb6d0632) | feat(task-reqs): add req forest recognizer contract | [bob-cli-on.1](bob-cli-on.1.md) | 2026-11-21 12:16:31 EST |
| bob-cli | [`ca07094`](https://github.com/bobs-org/bob-cli/commit/ca070941c05b42840a40d87f0e4f6a6e0aab6090) | feat(task-reqs): add task block layout and req line writers | [bob-cli-on.3](bob-cli-on.3.md) | 2026-11-21 13:32:20 EST |
| bob-cli | [`250c305`](https://github.com/bobs-org/bob-cli/commit/250c3053d652d1d6b48299557fc8272a809bab88) | docs(tasks): document requirement marks | [bob-cli-on.9](bob-cli-on.9.md) | 2026-11-21 13:37:40 EST |
| bob-cli | [`532df82`](https://github.com/bobs-org/bob-cli/commit/532df8259187f65b6f66864669eb80b133fcb35e) | feat(task-reqs): keep readers and writers off requirement lines | [bob-cli-on.2](bob-cli-on.2.md) | 2026-11-21 13:50:46 EST |
| bob-cli | [`f888213`](https://github.com/bobs-org/bob-cli/commit/f888213a22650dd6e33b38e9f77e7a65ca8e24e6) | feat(task): add bob task tidy to repair open task blocks | [bob-cli-on.4](bob-cli-on.4.md) | 2026-11-21 14:12:31 EST |
| bob-cli | [`2239120`](https://github.com/bobs-org/bob-cli/commit/2239120810ed5867eefc66a468cee04972aa6b45) | feat(task-split)!: carry a requirement branch into its own task | [bob-cli-on.7](bob-cli-on.7.md) | 2026-11-21 14:25:11 EST |
| bob-cli | [`1d89d95`](https://github.com/bobs-org/bob-cli/commit/1d89d95f3b2288601111965abad896eff5fd0195) | refactor(capture): make authored bullet depth a numeric level | [bob-cli-on.6.1.1](bob-cli-on.6.1.1.md) | 2026-11-21 15:12:33 EST |
| bob-cli | [`d8fae3e`](https://github.com/bobs-org/bob-cli/commit/d8fae3e5c734404864da0376818953733743ce56) | feat(task): add bob task rename-drawer to rename and merge drawers vault-wide | [bob-cli-on.5](bob-cli-on.5.md) | 2026-11-21 15:33:08 EST |
| bob-cli | [`7cc9493`](https://github.com/bobs-org/bob-cli/commit/7cc94933c2b3922e9a4c6eb80c9fc8415ce09311) | feat(capture)!: admit requirement bullets with req\_marker spans (grammar 29) | [bob-cli-on.6.1.2](bob-cli-on.6.1.2.md) | 2026-11-21 19:06:20 EST |
| bob-cli | [`c05deef`](https://github.com/bobs-org/bob-cli/commit/c05deef26b80d09c3f69181c8ab0f4dd60637168) | feat(capture): add requirement marker typing rewrite | [bob-cli-on.6.1.5](bob-cli-on.6.1.5.md) | 2026-11-21 20:14:58 EST |
| bob-cli | [`0a623b7`](https://github.com/bobs-org/bob-cli/commit/0a623b7036fbc9ccb86ebd4ef28889374affc604) | feat(capture): write new-task requirement bullets into the reqs zone | [bob-cli-on.6.1.3](bob-cli-on.6.1.3.md) | 2026-11-21 20:30:10 EST |
| bob-cli | [`3ce97d7`](https://github.com/bobs-org/bob-cli/commit/3ce97d736056fdf78ab3435badb3a03888842953) | feat(capture): write requirements to existing tasks | [bob-cli-on.6.1.4](bob-cli-on.6.1.4.md) | 2026-11-21 21:23:31 EST |
| bob-cli | [`536455a`](https://github.com/bobs-org/bob-cli/commit/536455acc9f2999bc46aeea8ec021970bdc9b9c9) | fix(capture): count nested requirements added to existing tasks | [bob-cli-on.6.1](bob-cli-on.6.1.md) | 2026-11-21 22:04:20 EST |
| bob-cli | [`e5ee4a8`](https://github.com/bobs-org/bob-cli/commit/e5ee4a8d9e942b7bbd9478ac1fa66a52d5c70ddf) | docs(task-reqs): add §5 Obsidian gestures table with exact copy and undo rule | [bob-cli-on.10.1.6](bob-cli-on.10.1.6.md) | 2026-11-21 22:08:54 EST |
| bob-cli--plans | [`bob-cli--plans@1d397b7`](https://github.com/bobs-org/bob-cli--plans/commit/1d397b783ee7e5eff90d3fc711bc5ad83054adac) | docs(plans): mark req gestures plan done | [bob-cli-on.10.1](bob-cli-on.10.1.md) | 2026-11-21 23:06:05 EST |
| bob-cli | [`ffeae19`](https://github.com/bobs-org/bob-cli/commit/ffeae199611e17eb6d8367e9a66ddee1e8c2aac4) | fix(capture): read deep requirement-chain lines like level 2 in completion, selectors, and aliases | [bob-cli-on.6.1](bob-cli-on.6.1.md) | 2026-11-22 07:14:25 EST |
| bob-cli--plans | [`bob-cli--plans@68b6574`](https://github.com/bobs-org/bob-cli--plans/commit/68b6574091c051ec55d70083c50cb0069dc17a25) | docs(plans): mark the capture requirement-bullets epic and its lexical-helpers tale done | [bob-cli-on.6.1](bob-cli-on.6.1.md) | 2026-11-22 07:15:18 EST |
| bob-cli | [`e4ee55b`](https://github.com/bobs-org/bob-cli/commit/e4ee55bdfe14f6b43ca71d2a3deaace7480b029b) | feat(task-complete): collect pre-close requirement groups and snapshot identity | [bob-cli-on.8.1.1](bob-cli-on.8.1.1.md) | 2026-11-22 08:03:26 EST |
| bob-cli | [`0a83bb1`](https://github.com/bobs-org/bob-cli/commit/0a83bb1c4f7a4466e5cd218afa7a0999556e2fbb) | feat(task-complete): add requirement verdict selection model | [bob-cli-on.8.1.2](bob-cli-on.8.1.2.md) | 2026-11-22 08:42:58 EST |
| bob-cli | [`d5e31ab`](https://github.com/bobs-org/bob-cli/commit/d5e31abcbbb19c2ca3fc14947ee03e3b9a0369fe) | feat(task-complete): add atomic carry/drop req write planning | [bob-cli-on.8.1.3](bob-cli-on.8.1.3.md) | 2026-11-22 09:35:07 EST |
| bob-cli | [`bddf386`](https://github.com/bobs-org/bob-cli/commit/bddf3868bf341287df9a5b8f0e1d5e931ac2155e) | feat(task-complete): place pulled requirement carries and resolve req jump landings | [bob-cli-on.8.1.4](bob-cli-on.8.1.4.md) | 2026-11-22 11:09:26 EST |
| bob-cli | [`7073b7c`](https://github.com/bobs-org/bob-cli/commit/7073b7c879b8cc853ee3b9a1072326dd185cba85) | feat(capture)!: publish requirement close on the successor card | [bob-cli-on.8.1.5](bob-cli-on.8.1.5.md) | 2026-11-22 13:36:38 EST |
| bob-cli | [`96a23f5`](https://github.com/bobs-org/bob-cli/commit/96a23f506f072ec577b6891b605937c47d4d82a6) | docs(task-dependencies): publish requirement close contract and RV inventory | [bob-cli-on.8.1.6](bob-cli-on.8.1.6.md) | 2026-11-22 13:58:46 EST |
| bob-cli | [`c72c941`](https://github.com/bobs-org/bob-cli/commit/c72c941deb7329e65e1899ae475a55136fe80f79) | fix(capture): land requirement-close overlap, x! pull-in, and dead-code cleanup | [bob-cli-on.8.1](bob-cli-on.8.1.md) | 2026-11-22 14:51:26 EST |
| bob-cli--plans | [`bob-cli--plans@04adcf3`](https://github.com/bobs-org/bob-cli--plans/commit/04adcf3c2e5368e1cff71509080e9b98c8106d8a) | docs(plans): mark requirement\_close\_engine done after bob-cli-on.8.1 land | [bob-cli-on.8.1](bob-cli-on.8.1.md) | 2026-11-22 14:52:27 EST |
| bob-cli | [`513ec47`](https://github.com/bobs-org/bob-cli/commit/513ec47889893245cd0aacf7f67895efcc253817) | docs(task-dependencies): mark picker v6 requirement consumer | [bob-cli-on.11.1.3](bob-cli-on.11.1.3.md) | 2026-11-22 16:04:56 EST |
| bob-cli | [`c17dd80`](https://github.com/bobs-org/bob-cli/commit/c17dd80a0b238a96c22e293badf82cdd54e4ced8) | docs(requirements): clarify managed Done close card availability | [bob-cli-on.11.1.6](bob-cli-on.11.1.6.md) | 2026-11-22 18:06:50 EST |
| bob-cli | [`9d0cbfb`](https://github.com/bobs-org/bob-cli/commit/9d0cbfbe165d56ac6f24b34d01d861d60d93f1b4) | docs(requirements): describe the Mac requirement card | [bob-cli-on.15.1.5](bob-cli-on.15.1.5.md) | 2026-11-22 19:41:54 EST |
| bob-cli | [`bf00529`](https://github.com/bobs-org/bob-cli/commit/bf005290ab7e2da5f019102b16ff81d495fe6855) | docs(task-requirements): document requirement close behavior | [bob-cli-on.11.1.7.2](bob-cli-on.11.1.7.2.md) | 2026-11-22 21:33:47 EST |
| bob-cli | [`ef640fd`](https://github.com/bobs-org/bob-cli/commit/ef640fde2f03456f3920e8402378a790ddca6858) | docs(task-dependencies): name the Mac Pull-In card as a requirement consumer | [bob-cli-on.15.1](bob-cli-on.15.1.md) | 2026-11-22 21:39:42 EST |
| bob-cli--plans | [`bob-cli--plans@d2f879c`](https://github.com/bobs-org/bob-cli--plans/commit/d2f879cd52ce4fad42f08f522d496c97a5cad6c7) | chore(plans): mark mac\_requirement\_close\_card done | [bob-cli-on.15.1](bob-cli-on.15.1.md) | 2026-11-22 21:40:41 EST |
| bob-cli | [`9c9c972`](https://github.com/bobs-org/bob-cli/commit/9c9c972c2873a23bb62ea44d89b756fd37823cbf) | docs(task-requirements): cover mixed close-card Undo in one gesture | [bob-cli-on.11.1.7](bob-cli-on.11.1.7.md) | 2026-11-23 00:56:01 EST |
| bob-cli--plans | [`bob-cli--plans@8eb9c65`](https://github.com/bobs-org/bob-cli--plans/commit/8eb9c6521c4471844f62ca84055af8dc4a205968) | docs(plans): mark req close-card mixed-undo landing done | [bob-cli-on.11.1.7](bob-cli-on.11.1.7.md) | 2026-11-23 00:58:11 EST |
| bob-cli | [`51c31c0`](https://github.com/bobs-org/bob-cli/commit/51c31c00728c0c9c649c10af87b6c983922cc56b) | docs(projects): describe requirement promotion to tasks and notes | [bob-cli-on.12](bob-cli-on.12.md) | 2026-11-23 01:15:35 EST |
| bob-cli | [`2b626d0`](https://github.com/bobs-org/bob-cli/commit/2b626d01ebf6f0f474537264e69f216ca9023285) | docs(memory): record that task requirements are met with their task | [bob-cli-on.17](bob-cli-on.17.md) | 2026-11-23 01:26:54 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-o6.6.1.5][1] | Look for existing DISCOVERED ISSUE notes about plugin fixture drift | 2 |
| read-by | [agent:bob-cli-o6.6.1.land][2] | Check active epic notes for already-recorded docs gate issues before routing landing follow-ups | 1 |
| read-by | [agent:bob-cli-oj.7][3] | Check whether the test_contracts.py walks.md failure is already tracked so I cite it instead of re-proposing | 1 |
| read-by | [agent:bob-cli-on.12][4] | Need epic and children phases | 2 |
| read-by | [agent:bob-cli-on.6.1.land][5] | Need existing notes to avoid duplicating discovered issues | 2 |
| read-by | [agent:bob-cli-on.7][6] | Check epic notes and sibling phase status for req-split | 1 |
| read-by | [agent:bob-cli-os.land][7] | Check whether the test_contracts docs-check failure is recorded on the causing epic | 1 |
| read-by | [agent:research.5u.cdx][8] | Understand the approved task requirements epic before proposing presentation-only changes | 1 |
| read-by | [agent:research.5u.cld][9] | Understand the task reqs epic scope for UX research report | 1 |
| read-by | [agent:research.5u.final][10] | Lead researcher: verify epic phase status before consolidating task-reqs display redesign research | 1 |
| read-by | [agent:research.5u.gem][11] | Understand the task reqs epic, its phases, behavior, and current display design | 1 |
| read-by | [agent:research.5u.grk][12] | Need remaining epic work and display contract before designing a display-only reqs UX | 1 |
| read-by | [agent:research.5u.mus][13] | Research task reqs UX - need epic context | 1 |
| read-by | [agent:research.5x.cdx][14] | Identify active epic scope and constraints for case-preserving drawer research | 1 |
| read-by | [agent:research.5x.cld][15] | Check that drawer-capitalization design does not conflict with the bob-cli-on epic | 1 |
| read-by | [agent:research.5x.final][16] | Verify current epic phase status to sequence the drawer-casing work against in-flight phases | 1 |
| read-by | [agent:research.5x.gem][17] | Check wip bob-cli-on epic bead so drawer design does not conflict | 1 |
| read-by | [agent:research.5x.grk][18] | Need bob-cli-on epic scope so mixed-case drawer design does not conflict | 1 |
| read-by | [agent:research.5x.mus][19] | Research drawer decapitalization vs wip epic conflict | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-o6.6.1.5/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-o6.6.1.land/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.7/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.12/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.6.1.land.md
[6]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.7/README.md
[7]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-os.land/README.md
[8]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.5u.cdx/README.md
[9]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.5u.cld/README.md
[10]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.5u.final/README.md
[11]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.5u.gem/README.md
[12]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.5u.grk/README.md
[13]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.5u.mus/README.md
[14]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.5x.cdx/README.md
[15]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.5x.cld/README.md
[16]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.5x.final/README.md
[17]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.5x.gem/README.md
[18]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.5x.grk/README.md
[19]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.5x.mus/README.md

<!-- sase:referenced-by:end -->
