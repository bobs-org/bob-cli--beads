# Bead: bob-cli-7w — Bulk capture templates (@@template:)

[Bead Pages](../README.md) / bob-cli-7w

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.1j.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.1j.linker.w0.md) · **Assignee:** `bob-cli-7w.land`
**Created:** 2026-10-15 14:04:18 EDT · **Closed:** 2026-10-15 18:19:33 EDT
**Plan:** [202610/bulk\_capture\_templates.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bulk_capture_templates.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/bulk_capture_templates.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | [bead:bob-cli-82][2] | Source epic whose phases proposed this decisions strand (memory_template_decision=no auto-decision) |
| related | [bead:bob-cli-83][3] | Source epic; phase bob-cli-7w.5 proposed this action (mac_expand_action=no auto-decision) |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bulk_capture_templates.md
[2]: https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-82/README.md
[3]: https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-83/README.md

<!-- sase:links:end -->

## Description

A draft that starts with `@@template:` captures one item per row from a `{0}`-style template, exactly as if the expanded items had been typed, all or nothing; `bob capture`, the `capture-*` editor protocol, and Bob Mac Capture make templates easy to write, easy to check, and pleasant to read.

## Notes

[2026-10-15T18:23:57Z · bryanbugyi34@gmail.com] The epic lander agent should make sure that the <ctrl+j> keymap never auto-inserts a dash when the template syntax is being used (it should just insert a newline).

[2026-10-15T21:32:29Z · bob-cli-7w.land] LAND TRIAGE (bob-cli-7w.land): The PROPOSED FOLLOW-UP for the bulk-template decisions strand appears on all five phases (.1 #1, .2 #1, .3 #1, .4 #1, .5 #2). All five are one proposal, filed once as memory task bob-cli-82 (small, ready); the memory_template_decision=no auto-decision means Bryan decides. The .5 #1 'Expand template' Mac editor action (mac_expand_action=no) is filed as feature task bob-cli-83 (medium, ready). Neither has a duplicate or a causally related active epic. Pre-existing macOS CI failures that the epic did not cause (RefsPanelModelTests queued-digit, RefsInspectorScrollTests hosted-short-content) are corroborated with +1 on bob-cli-7p and bob-cli-7h, from run 38807458658. The plan's own 'Out of scope' list (slug filter, per-row bullets, pipe tables, named placeholders, saved templates, implicit templates) was not proposed by any phase, so it was not filed.

[2026-10-15T21:34:50Z · bob-cli-7w.land] LAND VERIFICATION (bob-cli-7w.land): `just check` passes on master f732097c. All 5 phases are closed. Probes against the built bob confirmed -E, execution JSON/human summary, the one-row shape, row prefixes, the equivalence oracle, capture-parse spans/items/needs, the completion gate, the rewrite no-op, the docs, and the glossary strand (the only memory note edited). Remaining epic work, planned as a landing tale that closes this epic: (1) note #1, where Mac Ctrl-J still inserts '- ' in template drafts; (2) Mac CI fails CaptureTemplatePresentationTests.testTemplateRowNeedIsQuietAndUsesBobsDiagnostic (run 38807458658, fake-bob key '@template:' vs the test's '@template:\n'); (3) capture-parse misses marker =<X>/=x session suffixes that execution refuses; (4) capture-parse falsely refuses '{0} %' URL listen templates; (5) 'template:' is offered off line 1 when the text matches; (6) the candidate label is 'Bulk template' instead of the contract's longer label; (7) '@' in a row uses the template-line prefix; (8) execution doesn't report the first issue in draft order; (9) Mac: the cachedRouteCompletion path hides bob's template: candidate; the header-only state is red-underlined; the one-row preview says '1 captures'; the one-row fake-bob key lacks a header; (10) help omits exact arity; two stale #[allow(dead_code)]. Integration: the concurrent commits (ref collections bob-cli-7v, ref rename bob-cli-7x, opaque URL stems) don't touch capture/template code, so nothing needs integrating.

[2026-10-15T22:19:33Z · bob-cli-7w.land] Verified phases .1-.5 against plan:202610/bulk_capture_templates.md and fixed the landing gaps: A1 capture-parse refuses session suffixes on markers with same predicate as execution; A2 capture-parse clipboard follows expanded instances (URL % stays Listen); A3 template: offered only on first nonblank line; A4 label is Bulk template: one capture per row below; A5 @ in row uses template row K prefix; A6 execution reports first issue in draft order with coded errors (no message-text search); A7 help requires exactly one value per placeholder and removed two stale allow(dead_code); A8 docs updated for label/first-line; B1 Ctrl-J inserts plain newline in template drafts via parsedTemplate; B2 header-only test uses @template:; B3 one-row fake-bob key includes header plus model test; B4 @ route completion skips cache so template: appears plus primed-cache test; B5 header-only calm (no underline), singular 1 capture, pickerNeed mentions template_row; B6 Mac label fixture re-recorded. just check passes (second run green after one flaky capture_text failure that passes in isolation); Mac portable-check passes on athena (1209 tests, 0 failures); mac bundle.sh succeeded but just typecheck-tests could not complete because the Mac went offline mid-run, so macOS typecheck is unverified. Follow-ups: bob-cli-82 (decision record), bob-cli-83 (Expand action); pre-existing Mac CI failures +1 on bob-cli-7p and bob-cli-7h. No integration changes were needed: the concurrent commits are ref-library work that does not touch capture.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-7w.1](bob-cli-7w.1.md) | Template language core and bob capture -E | ✓ closed | medium | 2026-10-15 | 1 | 1 |
| [bob-cli-7w.2](bob-cli-7w.2.md) | Template execution in bob capture | ✓ closed | medium | 2026-10-15 | 1 | 1 |
| [bob-cli-7w.3](bob-cli-7w.3.md) | Template-aware capture-parse | ✓ closed | medium | 2026-10-15 | 1 | 1 |
| [bob-cli-7w.4](bob-cli-7w.4.md) | Template-aware completion and rewrite | ✓ closed | small | 2026-10-15 | 1 | 1 |
| [bob-cli-7w.5](bob-cli-7w.5.md) | Bob Mac Capture template presentation | ✓ closed | medium | 2026-10-15 | 1 | 1 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-7w: Bulk capture templates (@@template:) [closed]"]
    n1["bob-cli-7w.1: Template language core and bob capture -E [closed]"]
    n2["bob-cli-7w.2: Template execution in bob capture [closed]"]
    n3["bob-cli-7w.3: Template-aware capture-parse [closed]"]
    n4["bob-cli-7w.4: Template-aware completion and rewrite [closed]"]
    n5["bob-cli-7w.5: Bob Mac Capture template presentation [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n1 -.-> n2
    n2 -.-> n3
    n2 -.-> n5
    n3 -.-> n4
    n3 -.-> n5
    n4 -.-> n5
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-7w.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-7w.1.md) | [bob-cli-7w.1](bob-cli-7w.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-7w.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-7w.2.md) | [bob-cli-7w.2](bob-cli-7w.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-7w.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-7w.3/README.md) | [bob-cli-7w.3](bob-cli-7w.3.md) | 1 |
| [bbugyi200.apollo.bob-cli-7w.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-7w.4.md) | [bob-cli-7w.4](bob-cli-7w.4.md) | 1 |
| [bbugyi200.apollo.bob-cli-7w.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-7w.5.md) | [bob-cli-7w.5](bob-cli-7w.5.md) | 1 |
| [bbugyi200.apollo.bob-cli-7w.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-7w.land.md) | [bob-cli-7w](README.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`946c9b7`](https://github.com/bobs-org/bob-cli/commit/946c9b7d166a16a24868b9929a8e552563d5ed78) | feat(capture): add template language and expansion CLI | [bob-cli-7w.1](bob-cli-7w.1.md) | 2026-10-15 14:45:00 EDT |
| bob-cli | [`8f0baa7`](https://github.com/bobs-org/bob-cli/commit/8f0baa7653714d71ed34f0399efd8a654e0cfc96) | feat(capture): execute bulk templates through planner | [bob-cli-7w.2](bob-cli-7w.2.md) | 2026-10-15 15:26:50 EDT |
| bob-cli | [`8408562`](https://github.com/bobs-org/bob-cli/commit/840856213a7eca8b6e64443eabf8159cc22d0899) | feat(capture-parse): support template drafts | [bob-cli-7w.3](bob-cli-7w.3.md) | 2026-10-15 15:57:59 EDT |
| bob-cli | [`3f2b775`](https://github.com/bobs-org/bob-cli/commit/3f2b775a1d52eba29c2300ea96e6ae2ab9c33db0) | feat(capture-complete): gate template drafts in completion and rewrite | [bob-cli-7w.4](bob-cli-7w.4.md) | 2026-10-15 16:24:58 EDT |
| bob-mac-capture | [`bob-mac-capture@e959476`](https://github.com/bobs-org/bob-mac-capture/commit/e959476fba87df548c3734f0c94311cd419fa5a9) | feat(capture): present bulk templates in Mac Capture | [bob-cli-7w.5](bob-cli-7w.5.md) | 2026-10-15 17:07:35 EDT |
| bob-cli | [`0b1bc54`](https://github.com/bobs-org/bob-cli/commit/0b1bc5416a866f8c234022117c2747d1312c6b1b) | feat(capture): finish bulk template landing gaps A1-A8 | [bob-cli-7w](README.md) | 2026-10-15 18:21:34 EDT |
