# Bead: bob-cli-pf.2.1 — Generic bob props show and update

[Bead Pages](../README.md) / [bob-cli-pf.2](bob-cli-pf.2.md) / bob-cli-pf.2.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pf.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.2.md) · **Assignee:** `bob-cli-pf.2.1.land`
**Created:** 2026-11-22 14:47:18 EST · **Closed:** 2026-11-22 22:53:14 EST
**Plan:** [202611/props\_cli.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/props_cli.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/props_cli.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/props_cli.md

<!-- sase:links:end -->

## Description

Complete bob-cli-pf.2 with an ordered property report and guarded, reversible frontmatter edits that preserve unrelated bytes and enforce one writer per key.

## Notes

[2026-11-22T22:53:38Z · research.5y.cld] DISCOVERED ISSUE: the props role table on master (src/native/props/roles.rs @ e98c7fe9, also origin/master) classifies every area/project bookkeeping key as loose, although the plan asks to 'audit bob's frontmatter writers to complete this list'. Missing derived keys: done_tasks (written by bob task archive; on 11 areas and 42 projects); project status (bob projects sync mirrors ^prj: checked→done, canceled→canceled, reopen→wip); leftover frontmatter scheduled on projects (projects sync hoists it onto ^prj); template (written by capture_project_note.rs:562, never read); task_count/open_task_count (written by the bob-project-tasks plugin, see bob-cli-pi). Impact: =+ on any area/project note would offer free-text edits of done_tasks (breaking archive pairing) and status: done on an open project (silently reverted by the next projects sync). Evidence: research:202611/area_project_property_cards__cld.md §1.4–§1.5, §5.5 (file:explicit:a4873a8805c572a2cd19068c).

[2026-11-23T01:48:08Z · bob-cli-pf.2.1.land] LAND FOLLOW-UP TRIAGE (complete before repair proposal): Read every note on all three phases. bob-cli-pf.2.1.1 #2 (capture-related performance gate) corroborated bob-cli-bo with attributed ToolRun pass/fail evidence; no duplicate task. bob-cli-pf.2.1.2 #2 (two gcal_ack session tests using fixed sleeps) created small task bob-cli-pk and marked ready after all-status duplicate searches, the last-week task sweep, and active-epic causal review. bob-cli-pf.2.1.3 #1 (Spotify/gmail_transport ETXTBSY executable stubs) corroborated bob-cli-5l with attributed phase evidence and current source locations; no duplicate task. Declined treating ETXTBSY as the same defect as the gcal_ack timing failures: stub executable descriptor races and fixed input/journal deadlines need different remedies. No active epic has a credible causal link to these pre-existing harness defects. Reports are relayed phase observations, not fresh full-suite reproductions by this lander. The props ownership, span, semantic verification, and CLI gaps found in this audit remain epic work and are in the repair tale, not follow-up tasks. Existing bob-cli-p4 was notified about BOM ownership integration impact; its pre-existing album-discovery work remains separately tracked.

[2026-11-23T01:48:29Z · bob-cli-pf.2.1.land] LAND AUDIT at 3e480e4a (incomplete): Read the epic note, every child note, plan:202611/props_cli.md, parent plan:202611/card_owned_frontmatter.md, parent phase bob-cli-pf.2, and implementation commits e98c7fe9/fdd94725/3e480e4a. Final inherited decisions are unchanged (bank_foot=yes, drawer_memory=note, glossary-only memory scope, no decision record); this child has no plugin or memory/version changes. The inventory, six-op protocol, lock/replan/atomic runtime, props_v1 catalog handshake and completion wiring are present. Remaining epic defects: (1) note #1 is unaddressed: system-owned done_tasks/project status/scheduled and plugin task counts are still loose; template is only a creation default and needs deliberate disposition under the plan, not automatic protection. (2) PropsDocument handles BOM but roles use projects::parse_frontmatter, which rejects BOM and silently treats typed notes as ordinary notes; existing bob-cli-p4 covers upstream album discovery and has been notified of props impact. (3) rebuild_entry_with_value slices value_range.end..inline_comment.start for multiline values with a header comment; an isolated Rust harness using the exact production function and its documented ranges panics on x: |- # inline followed by an indented old value (24 > 10). (4) Exact production emit_block_scalar emits x: | for requested newline-only text and x: |+ plus only one trailing newline for a requested a plus two newlines; parsed YAML loses a newline. Leading-space text also needs an indentation indicator. verify() skips all touched keys, so it never enforces requested target semantics. (5) parse_yaml_fragment/validate_raw can admit new opaque YAML, leaving inverse operations unable to restore it; harden incoming fragments and verify undo. (6) CLI accepts human/json while the approved and published contract promises text/json; help examples use unsupported -n instead of -d. Absolute NOTE with relative -b is rejected by mixed lexical path forms. (7) Required CLI schema-change-while-lock-waiting test and complete op/stdin coverage are missing. No full bob binary or just-check gate was run during this source audit; the small harness is not a substitute for those gates. No epic-symbol entries exist. These are scoped into one medium repair tale; keep this epic and parent phase open until repaired and verified.

[2026-11-23T01:50:01Z · bob-cli-pf.2.1.land] LAND INTEGRATION: fetched origin/master; it remains 3e480e4a with no base-branch drift. Reviewed non-epic commits since the initial implementation and the two between plan baseline 96a23f50 and first implementation: c72c941d/513ec478 requirement integration; c17dd80a/9d0cbfbe requirement docs; badcd30c tick waiting/escalation; 8c019eb4 Gmail HTML; 063a8768/33f6d08d per-PDF scan dependencies/refresh; 7f104e52 dedicated-link Pomodoro history. No new property owner, competing writer, or required props consumer migration was introduced by those changes. The repair tale preserves the existing lock and scan-observation integration, and requires a fresh drift check before closing. The linked bob-plugins repository was opened read-only through sase_repo to verify task_count/open_task_count writers; no plugin changes or deployment were made.

[2026-11-23T03:53:14Z · bob-cli-pf.2.1.land] Landing repairs for generic bob props are complete and verified.

Ownership: roles.rs now classifies done_tasks (bob task archive), project status/scheduled (bob projects sync), and task_count/open_task_count (bob-project-tasks plugin) as derived; template stays loose as a creation default; created stays loose. projects::parse_frontmatter is BOM-aware so typed notes with a UTF-8 BOM keep their kind.

Writes: header-comment trivia is rebuilt from unindented blanks/comments only; yaml_text keeps the last inner line ending; empty keep-chomp bodies emit |2+ with an indented empty content line so a following --- fence cannot eat the newline; Restore wrap does not add a second blank when raw already ends with a newline. Incoming anchors/aliases/tags/merges are refused; quoted and block lookalikes stay allowed. plan::verify is per-op semantic, and inverse of set_yaml restores original bytes.

CLI: format is text|json with a hidden human alias; help says text or json; dry-run is -d; absolute NOTE plus relative -b is confined after making the vault absolute. acquire_lock_waiting keeps one lock fd open for the whole wait so schema-change-while-waiting tests can see the waiter via /proc/<pid>/fd inode compare.

Gates: cargo test --test cli props 18 passed including three lock-wait tests; props lib 53 and yaml_spans 7 passed; just docs-gen and just docs-check passed; just check (fmt, clippy, cargo test --workspace --no-fail-fast) exit 0. Read-only vault sampling under BOB_DIR=/home/bryan/bob classified zorg_* derived, album identity/card, project status/done_tasks/task counts derived, template/created loose, day parent derived and intentions card. No BOM notes at vault root. eat/1_walnut classified note.

No leftover epic-symbol entries on bob-cli-pf.2.1. Parent decisions bank_foot=yes, drawer_memory=note, memory_glossary_cards=yes, memory_decision_record=no unchanged. No memory, plugin, Cargo version, or CHANGELOG edits. Schema version stays 1. Pre-existing lander follow-ups bob-cli-bo, bob-cli-pk, bob-cli-5l, and bob-cli-p4 notification were not refiled. A denied clippy::op_ref in highlights_ref/scan_plan.rs was typed correctly so just check could pass; it is not a props behavior change.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pf.2.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.2.1.land.md) | [bob-cli-pf.2.1](bob-cli-pf.2.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`3966100`](https://github.com/bobs-org/bob-cli/commit/396610031495186d77f64f580a02a3ceb8f114ac) | feat(props): repair ownership, reversible writes, and CLI contract | [bob-cli-pf.2.1](bob-cli-pf.2.1.md) | 2026-11-22 22:55:51 EST |
| bob-cli--plans | [`bob-cli--plans@77c260f`](https://github.com/bobs-org/bob-cli--plans/commit/77c260f3fce6382df29e4d3792550c82ac6d8439) | chore(plans): mark props\_cli and landing repairs done | [bob-cli-pf.2.1](bob-cli-pf.2.1.md) | 2026-11-22 22:57:10 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pf.2.1.1--1][1] | Need epic decisions governing phase implementation and closure | 1 |
| read-by | [agent:bob-cli-pf.2.1.3][2] | Need child epic scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.2.1.1.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.2.1.3/README.md

<!-- sase:referenced-by:end -->
