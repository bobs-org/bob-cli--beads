# Bead: bob-cli-dm.6.1 — Task-aware Link to today picker

[Bead Pages](../README.md) / [bob-cli-dm.6](bob-cli-dm.6.md) / bob-cli-dm.6.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-dm.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-dm.6.md) · **Assignee:** `bob-cli-dm.6.1.land`
**Created:** 2026-10-28 20:08:12 EDT · **Closed:** 2026-10-28 22:42:48 EDT
**Plan:** [202610/task\_theme\_link\_picker.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_theme_link_picker.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/task_theme_link_picker.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_theme_link_picker.md

<!-- sase:links:end -->

## Description

Complete bob-cli-dm.6 so the picker preselects and explains a suggested theme, remembers deliberate exceptions in guarded task edits, and supports link once.

## Notes

[2026-10-29T01:39:06Z · bob-cli-dm.6.1.land] LANDING AUDIT: Read this epic, all three child beads and every note, both linked plans, parent phase bob-cli-dm.6 and its DECISIONS. Reviewed bob-plugins implementation commits 97341c4, ea583df, 0f74920 and current source: task context/full-text one-based conversion, shared preselection, stable intent/footer, guarded writer, planner freshness, routed and partial outcomes. The selected ledger_theme_pills=yes branch is upstream of this child; seed_plex_chore remains dm.9; no memory edits occurred. All 4131 plugin tests pass; shared vectors are byte-identical. Integration: bob-plugins has no non-epic commits after bc245fc. bob-cli is at origin/master cba7c47d; reviewed drift since planning baseline 41cc4acc (387a4fc2 relation completion, 4005c613 heading parsing, 687375eb theme rename/split verifier, 38f15d3e install profile, cba7c47d reverse relation rename). Only 687375eb overlaps themes; it retains task-field coverage and byte-preserving verification and needs no picker adaptation. Three remaining epic-caused defects reproduced on the current built plugin: (1) catalog known=false to true plus refresh leaves BUILD selected, unknown_theme frozen, and no suggested New WRITE; neither snapshot.choice nor untouched initialKey adopts the eligible suggestion; (2) with a known Write create suggestion, query wri drops the normal Recent Write row, leaving only New WRI, because suggested-theme exclusion applies even when no suggested create row exists; annotation also runs before final Recent assembly; (3) a throwing caps() passes [] exemptKeys to the real Ledger Tools write planner and returns set PLAN for an ordinarily exempt destination. These require a medium repair tale, not unrelated task beads. FOLLOW-UP TRIAGE: No PROPOSED FOLLOW-UP entries exist on this epic, any of its three child phases, or parent phase dm.6. No distinct unrelated discoveries, duplicate corroborations, task creations, or declined proposals. No epic-symbol entries for dm.6.1 or dm.6. Epic and parent phase remain open pending repairs and final verification; a lander-authored tale must perform their same-turn closeout.

[2026-10-29T02:42:48Z · bob-cli-dm.6.1.land--3] Verified original phases 6.1.1–6.1.3 (closed done) plus landing repairs for catalog-knowledge refresh, typed Recent annotation, and unavailable exempt-keys skip. Monitor jqsxbkc4ee7w completed exit 0 in 11m50s on HEAD a9066b8 with dirty picker repairs: npm test 4139/4139, npm run validate 8/8, BOB_CLI_DIR docs:check passed (447 pytest + 1 skipped), vectors.json byte-identical, just check passed. Deployed with bob plugins sync --no-pull -p block-id-prompt: copied main.js +203/-51 from uncommitted a9066b8 build; backup 20261028-224151. No Obsidian desktop process (only vault inotifywait); manual suggested/default/query/Alt+Enter/one-undo verification was not performed. Integration: bob-plugins after audit 0f74920 is a9066b8 ledger-tools gtd-decided/gray-pill only (no picker overlap); dirty block-id-prompt src 076/078/085/170, generated main.js, picker-view and theme-write tests. bob-cli remains clean at cba7c47d. Inherited decisions unchanged: ledger_theme_pills=yes, seed_plex_chore=yes belongs to dm.9, both memory decisions=no. Follow-up triage: no PROPOSED FOLLOW-UP on this epic, its three children, or parent dm.6; no new task beads. epic-symbols bob-cli-dm.6.1 empty. bob-cli justfile has no symvision recipe.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-dm.6.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-dm.6.1.land.md) | [bob-cli-dm.6.1](bob-cli-dm.6.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@c59819c`](https://github.com/bobs-org/bob-plugins/commit/c59819c573c5a52d97c57d0383ca57771db141c4) | fix(block-id-prompt): refresh catalog knowledge, keep typed Recent, skip unavailable caps | [bob-cli-dm.6.1](bob-cli-dm.6.1.md) | 2026-10-28 22:45:46 EDT |
| bob-cli--plans | [`bob-cli--plans@f36de39`](https://github.com/bobs-org/bob-cli--plans/commit/f36de3992a232cfe0d698fe3f2b729b5913bd4bd) | chore(plans): mark task-theme picker epic and landing tale done | [bob-cli-dm.6.1](bob-cli-dm.6.1.md) | 2026-10-28 22:48:06 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-dm.6.1.2][1] | Need epic decisions | 1 |
| read-by | [agent:bob-cli-dm.6.1.3][2] | Need epic DECISIONS and full phase list for 6.1 | 1 |
| read-by | [agent:bob-cli-dm.6.1.land--3][3] | Need the parent link after child epic close | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-dm.6.1.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-dm.6.1.3/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-dm.6.1.land.md

<!-- sase:referenced-by:end -->
