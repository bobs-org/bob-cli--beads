# Bead: bob-cli-7r.7 — Final docs sweep, end-to-end verification, optional decision record

[Bead Pages](../README.md) / [bob-cli-7r](README.md) / bob-cli-7r.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.4g.linker.w1.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.4g.linker.w1.w0.md) · **Assignee:** `bob-cli-7r.7` · **Size:** small
**Created:** 2026-10-14 16:21:12 EDT · **Closed:** 2026-10-14 20:07:49 EDT
**Plan:** [202610/capture\_relate\_existing\_tasks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/capture_relate_existing_tasks.md)

## Description

publish: check every RX/RXC vector against the shipped binaries. Reconcile docs/capture.md, README, and help text with what landed. Run a scratch-vault walkthrough of all three authoring flows. Write the decision strand only if the memory decision says yes.

## Notes

[2026-10-15T00:07:07Z · bob-cli-7r.7] Scratch-vault walkthrough of the three authoring flows (Tasks plugin Ready/In Progress/Next/Blocked/Canceled/Done; BOB_NOW=2026-10-14 10:20:00). Seed: foo.md Buy shoes ^bar, body.md Exercise ^excercise (In Progress), job.md Do cleanup tasks ^cleanup.

1. Owner first. capture-complete -c 6 -- '@body+' → context task, picker parent_task, Exercise replacement excercise. After pick, capture-parse -- '@body+excercise &foo:bar' → mode task_dependency, existing_task body/excercise, needs []. capture --dry-run → [dry-run] ok would update  body.md / [/] → [?]  Exercise  ^excercise / ⛓ would now depend on "Buy shoes"  foo.md ^bar  [ ] Ready.

2. Relationship first. capture-parse -- '&foo:bar' → incomplete, needs [dependency_target] (Mac calm hint). capture-complete -c 10 -- '&foo:bar +' → context task_parent, picker.relationship.dependencies[0].text Buy shoes, Buy shoes disabled_reason the prerequisite itself, replacement covers only +. After inserting @body+excercise, dry-run matches flow 1.

3. Current task. capture-complete -c 1 -- '^' → context active_task, Exercise replacement body:excercise. capture-parse -- '^body:excercise &foo:bar' → mode task_dependency, existing_task. Dry-run matches flow 1.

RX/RXC vs shipped binary: RX1–RX16 and RXC1–RXC8 match docs/tests. RX8 execute was missing from relate_existing.rs; added. docs/capture.md RXC1 example had candidates: [] (false); now selected owner fields from live -c 17. Combined live '@body+excercise &foo:bar *job:cleanup' with linked In Progress owner matches the terminal example byte-for-byte (plan-budget footer omitted). Help: capture / capture-parse / capture-complete document owner rule, ^route:id, + picker, picker.relationship, owner fields. Mac README matches landed Mac fixtures (Todo status_name).

[2026-10-15T00:07:10Z · bob-cli-7r.7] PROPOSED FOLLOW-UP: skipped decisions strand existing-task-owners-relate — auto decision_record=no; record owner rule, alias-never-links, shared relationship_needs_text refusal, and closed * owner cannot block; cite bob-cli-7r phase commits; link [[decisions:capture-star-blocks-existing-tasks]] and [[decisions:mac-capture-is-a-thin-client]]

[2026-10-15T00:07:14Z · bob-cli-7r.7] PROPOSED FOLLOW-UP: Mac relationship preview fixtures freeze status_name Todo — recorded without Tasks plugin Ready settings; bob-cli with plugin settings emits Ready; re-record fixtures if Mac README should match Tasks-plugin vaults

[2026-10-15T00:07:49Z · bob-cli-7r.7] Verified RX1–RX16 and RXC1–RXC8 against the landed bob binary in a Tasks-plugin scratch vault; three authoring flows walk through capture-complete/capture-parse/capture --dry-run; docs/capture.md RXC1 JSON now matches live selected owner fields; added RX8 execute coverage; help texts and README match; decision_record=no (follow-up noted); no leftover --epic-symbol entries.

## Dependencies

- **Depends on:** [bob-cli-7r.3](bob-cli-7r.3.md) ✓ · ⧖ 2026-10-14
- **Depends on:** [bob-cli-7r.4](bob-cli-7r.4.md) ✓ · ⧖ 2026-10-14
- **Depends on:** [bob-cli-7r.6](bob-cli-7r.6.md) ✓ · ⧖ 2026-10-14

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-7r.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-7r.7.md) | [bob-cli-7r.7](bob-cli-7r.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`75a1809`](https://github.com/bobs-org/bob-cli/commit/75a180967746f23fcf22f40b5da0b8c43d2b1aad) | docs(capture): align RXC1 owner JSON and cover RX8 execute | [bob-cli-7r.7](bob-cli-7r.7.md) | 2026-10-14 20:18:31 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-7r.7--1][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-7r.7.md

<!-- sase:referenced-by:end -->
