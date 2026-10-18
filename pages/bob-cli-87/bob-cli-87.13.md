# Bead: bob-cli-87.13 — Finish note snapshots so real area and project notes match the spec

[Bead Pages](../README.md) / [bob-cli-87](README.md) / bob-cli-87.13

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-87.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-87.land.md) · **Assignee:** `bob-cli-87.13.land`
**Created:** 2026-10-17 10:11:18 EDT · **Closed:** 2026-10-17 21:42:19 EDT
**Plan:** [202610/note\_snapshot\_landing\_repairs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/note_snapshot_landing_repairs.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/note_snapshot_landing_repairs.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/note_snapshot_landing_repairs.md

<!-- sase:links:end -->

## Description

Every `bob ref create <area or project note>` snapshot matches the bob-cli-87 visual spec and content policy on the real vault: status glyphs sit on the first line of their task text, no stale status-chip row or raw `^block-id` labels appear, links to existing vault files resolve, images are framed, earlier-snapshot hints follow the plan, and the docs record what was verified on athena and the Mac.

## Notes

[2026-10-17T22:00:05Z · bob-cli-8w.land] DISCOVERED ISSUE (from bob-cli-8w.land, triaging bob-cli-8w.1 PROPOSED FOLLOW-UP #1/#2): cargo test --lib pandoc_maps_every_contract_construct_to_tex fails on bob-cli master 30bdfb89 — panic 'lifted link' at src/native/highlights_ref/note_snapshot/profile.rs:946 (the expected \hyperref[t-next]{visible link\BobTag{ᵇ}} is missing from the emitted TeX). bob-cli-87.land note #5 recorded this test passing at 5af6521; the only note_snapshot commits since are 9ef336cc (bob-cli-87.13.1) and 2ae12515 (bob-cli-87.13.2, hang-indent task rows), so this child epic's work most likely changed the emitted TeX and the expectation or projection now needs repair. Impact: just check fails for every agent at the lib-test step. Not caused by bob-cli-8w; no new task filed because it belongs to this active epic.

[2026-10-17T23:44:48Z · bob-cli-87.13.land] LAND FOLLOW-UP TRIAGE: Reviewed every phase note. bob-cli-87.13.2 #1 completion PTY flakes: +1 evidence recorded on existing bob-cli-8q for bash_readline_inserts_what_bob_returned and DISCOVERED ISSUE on causally responsible active epic bob-cli-3j covering both bash and real_zsh_first_tab_completes; declined new tasks as duplicate/active-epic-owned. bob-cli-87.13.2 #2 curl_pins_the_checked_address_with_resolve ETXTBSY: +1 on existing bob-cli-5l (same in-place stub writer race); declined duplicate. Same-type search, one-week flake sweep, active-epic sweep, and relevant 3j children reviewed. No other PROPOSED FOLLOW-UP entries in .13 children. Epic note #1 lifted-link test passes on current 860f0be: cargo test --lib pandoc_maps_every_contract_construct_to_tex -- --nocapture (1 passed). Remaining corpus-gate bugs are caused by .13.4 and stay epic work in a bounded landing tale.

[2026-10-17T23:47:06Z · bob-cli-87.13.land] LAND AUDIT at 860f0be: Read all four child scopes and every note, the approved repair plan and parent acceptance, all four epic commits (726fd48, 9ef336c, 2ae1251, 860f0be), changed projection/profile/create/gate source, synthetic goldens, and verification docs. DECISIONS honored: mac_rerun=no is explicit in docs; no packages/fonts added; no memory edits. The previously reported lifted-link contract test passes here. Fetched origin; HEAD equals origin/master. Reviewed six intervening non-epic commits: c9a5063 Highlights hotkey docs, b59af42/b5adef5 Mac keychain install reporting, 8b6ca21/4052bd7 capture open_notes, 30bdfb8 reverse Blocks contract. No snapshot integration change is required by those commits: open_notes consumes staged task locations independently; Blocks preserves the same generated dependency-line grammar snapshots already parse; install and hotkey docs do not duplicate rendering. Remaining epic-caused gate defects: find_vault_file_match incorrectly rejects old/Target and old/Target.md when notes/Target.md is the unique basename, despite 860f0be teaching the resolver this fallback. A full synthetic gate with injected missing-file warnings exits 0 and reports zero false unresolved warnings (expected exit 1). Also dry_warning_explanation runs after the loop with stale last rel, so a warning from notes/Host.md about img/chart.png can be described as genuinely missing even though notes/img/chart.png exists. Plan a medium tale limited to checker consistency, per-source warning explanations, regression coverage, athena re-gate, and this epic closeout; ancestor close is conditional on its readiness.

[2026-10-18T01:42:19Z · bob-cli-87.13.land--1] LAND CLOSE at 860f0be plus working-tree resolver, visibility, corpus-gate, synthetic tests, and docs. Read all four child phases (closed), every note, the approved repair plan, parent acceptance, and this closeout tale. DECISIONS honored: mac_rerun=no; no packages/fonts; no memory edits; decision_record=no.

Scope: find_vault_file_match uses unique basename after exact/source-relative miss (old/Target and old/Target.md); dry_warning_explanation stores origin with each warning so the failure count and report agree. scripts/dev/note_snapshot_corpus_gate_test and tests/cli/highlights/corpus_gate.rs cover basename, ambiguity, absence, source-relative attachments, and two-source origin preservation; just check-scripts runs both.

Verification: monitor 8zx7tjb24tz7 ran cargo build --release, copied CARGO_TARGET_DIR/release/bob to target/release/bob, just check, then BOB_BIN=$PWD/target/release/bob scripts/dev/note_snapshot_corpus_gate /home/bryan/bob /tmp/bob-note-snapshot-gate-closeout; exit 0. Athena 2026-10-17: 103 renders, 5,081 dry-runs, 0 render/dry-run/glyph/overfull/Type3 failures, 0 false unresolved-file warnings, 0 raw block-ID residue, 0 status-chip rows, 0 residue scan failures, vault git status unchanged. Unresolved-reference warnings 5,543, all classified; sampled origins ssh.md, define.md, cash.md, fun.md, mcp_ref.md, now_zorg.md, inbox.md match their dry-run logs; claimed-missing files have no unique basename. Residue findings: none. docs/highlights-create.md updated; Mac record stays df4e120 pre-fix.

Lifted-link: lander cargo test --lib pandoc_maps_every_contract_construct_to_tex passed on 860f0be; just check in this run includes it.

Follow-up triage (lander): bob-cli-87.13.2 PTY flakes corroborated bob-cli-8q and DISCOVERED ISSUE on bob-cli-3j (bash and zsh); curl ETXTBSY corroborated bob-cli-5l; no new tasks. Epic note #1 lifted-link does not reproduce.

Integration: fetched origin; origin/master is 30eafe2 (ahead of 860f0be). 3ec4d0d/30eafe2 Blocks docs and 54670b4/ad036f9 mermaid diagrams (profile.rs RenderFilters with diagrams: None so snapshot output stays unchanged until the wire phase) need no snapshot integration in this closeout. Earlier intervening commits (hotkey docs, keychain, capture open_notes, reverse Blocks) still need none. This tree was not rebased onto origin.

epic-symbols bob-cli-87.13: none. Parent bob-cli-87 left open: acceptance #4 live #task follow-up and image highlight still unexercised (87.12 notes #20–#24 empty attempts; docs record that path unexercised; mac_rerun=no does not waive).

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-87.13.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-87.13.land.md) | [bob-cli-87.13](bob-cli-87.13.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`724333f`](https://github.com/bobs-org/bob-cli/commit/724333f86981290f705c19a29ac723ed96e064d4) | fix(note-snapshot): resolve snapshot files and repair the corpus gate | [bob-cli-87.13](bob-cli-87.13.md) | 2026-10-17 21:46:18 EDT |
