# Bead: bob-cli-oo — Bank row notes: Space opens a note stage on the Category card

[Bead Pages](../README.md) / bob-cli-oo

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5q.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5q.linker.w0.md) · **Assignee:** `bob-cli-oo.land`
**Created:** 2026-11-21 12:07:07 EST · **Closed:** 2026-11-21 16:40:24 EST
**Plan:** [202611/bank\_row\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_row_notes.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/bank_row_notes.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_row_notes.md

<!-- sase:links:end -->

## Description

During the ]b bank walk, Space on the Category card writes a short note into the row's inline `— note` tail and stays on the same row (no tick, no advance), and the note renders everywhere as a quiet muted-italic dash-led caption.

## Notes

[2026-11-21T19:54:14Z · bob-cli-o6.6.1.land] DISCOVERED ISSUE: bob-plugins d9fe19d (bob-cli-oo.2, bank row note captions) added a sentence to docs/bob-ledger-tools.md (wc 6580 -> 6627 words) and pushed the mounted page over the reference cap: on bob-cli dfe20ca3 + bob-plugins e6d7aed, uv run --project tools/docs bob-docs lint exits 1 with 'docs/reference/plugins/bob-ledger-tools.md:1: budget: over budget at 6042 words (cap 6000 for reference/)'. At bob-plugins 238fa91 (the previous ledger-tools docs change) lint did not report this page. Every bob-plugins and bob-cli docs gate fails lint until it is trimmed. Found by the bob-cli-o6.6.1 land agent while re-verifying docs gates; corroborated on the standing headroom task bob-cli-il.

[2026-11-21T21:40:24Z · bob-cli-oo.land] Verified all 4 phases against plan:202611/bank_row_notes.md and the epic's commits (bob-cli baca8701, dfe20ca3, fc27bf1a; bob-plugins 1731913b, d9fe19d8, 303e5dbf, 604c8a9a): note_cleaner.json is byte-identical in both repos; the Rust five-step cleaner, shared-vector test, and naming.rs payee regression are present; the plugin has disjoint noteSpan/noteMarkerSpan/noteEditable, 🔁 insertion before the flag or note, and whole-row $ protection; the caption renders in Live Preview, Reading view, and the queue card with contrast CSS. bankNoteNormalize, bankNoteWritePlan (with the round-trip self-check), and bankNoteStagePreview are in place. Space/-/Delete and restricted-Enter keys match the design (with a loading flag); bankNoteCommit applies one isolateHistory whole-line edit, reports the save outcome, keeps the cursor, re-captures context, re-anchors the walk, and counts session.notes without filing or advancing. Bank: note this row works. Docs and glossary:bank-row follow the decisions (no keymap decision record). LANDING FIXES (bob-plugins): (1) the normalizer now reports the concrete rewritten text per change ('[[people/max|Max]] → Max', deduped), matching the design's chip example (was oo.4 PROPOSED FOLLOW-UP #2), with a new note-write test and an updated stage chip assertion; (2) trimmed docs/bob-ledger-tools.md from 6033 to 5996 lint words. oo.2's caption sentence had pushed it over the 6000 cap (the epic's own DISCOVERED ISSUE note). INTEGRATION: om.10's prose-field role lint (c2e28cad) landed mid-epic, so the note-stage input now declares 'bob-text: literal' (bank fields never complete [[ per both plans); rebuilt and deployed bob-ledger-tools via bob plugins sync (no -F). No other post-start bob-cli or bob-plugins commit touches bank code. GATES: bob-cli just check passes; 133 targeted bank/prose-role tests pass; full npm test 8412/8419, with only 3 perf budgets failing at load avg 134 (all pass isolated); bob-ledger-tools docs lint is clean, and only bob-navigation-hotkeys.md (6307, bob-cli-ob, om's DISCOVERED ISSUE) still fails. Real-Obsidian bank e2e not run: no Obsidian binary on this host; the --self-test passes. FOLLOW-UPS: oo.1#1 vault-format overage was already fixed by cb9f8fad (note on bob-cli-oc), and plugin-apis is a warning tracked by bob-cli-ob. oo.2#1 deploy is resolved by later syncs and this landing. oo.2#2 and oo.4#1: ledger-tools was fixed here; nav-hotkeys +1'd on bob-cli-ob. oo.2#3, oo.3 and oo.4#3 perf flakes +1'd on bob-cli-km and bob-cli-io. oo.4#2 was fixed here. Two new DISCOVERED ISSUE notes on active epic bob-cli-om: the prose-role scanner misses bankCategoryUiAppend sites, and the R9 40 ms CPU perf gate flakes under load. No --epic-symbol entries.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-oo.1](bob-cli-oo.1.md) | Shared note cleaner, disjoint note spans, and prerequisite fixes | ✓ closed | medium | 2026-11-21 | 1 | 2 |
| [bob-cli-oo.2](bob-cli-oo.2.md) | Quiet prose caption on every row surface | ✓ closed | small | 2026-11-21 | 1 | 1 |
| [bob-cli-oo.3](bob-cli-oo.3.md) | Pure note normalizer, write planner, and stage preview model | ✓ closed | small | 2026-11-21 | 1 | 3 |
| [bob-cli-oo.4](bob-cli-oo.4.md) | Space keymap, in-card note stage, stay-on-row commit, command, and docs | ✓ closed | medium | 2026-11-21 | 1 | 2 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-oo: Bank row notes: Space opens a note stage on the Category card [closed]"]
    n1["bob-cli-oo.1: Shared note cleaner, disjoint note spans, and prerequisite fixes [closed]"]
    n2["bob-cli-oo.2: Quiet prose caption on every row surface [closed]"]
    n3["bob-cli-oo.3: Pure note normalizer, write planner, and stage preview model [closed]"]
    n4["bob-cli-oo.4: Space keymap, in-card note stage, stay-on-row commit, command, and docs [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n1 -.-> n2
    n2 -.-> n3
    n3 -.-> n4
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-oo.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-oo.1/README.md) | [bob-cli-oo.1](bob-cli-oo.1.md) | 2 |
| [bbugyi200.apollo.bob-cli-oo.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-oo.2/README.md) | [bob-cli-oo.2](bob-cli-oo.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-oo.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-oo.3.md) | [bob-cli-oo.3](bob-cli-oo.3.md) | 3 |
| [bbugyi200.apollo.bob-cli-oo.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-oo.4/README.md) | [bob-cli-oo.4](bob-cli-oo.4.md) | 2 |
| [bbugyi200.apollo.bob-cli-oo.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-oo.land/README.md) | [bob-cli-oo](README.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`baca870`](https://github.com/bobs-org/bob-cli/commit/baca8701459fb39fdeb783d5cdb95ac9f2b20b21) | feat(bank): share the five-step note cleaner and document tail order | [bob-cli-oo.1](bob-cli-oo.1.md) | 2026-11-21 12:53:38 EST |
| bob-plugins | [`bob-plugins@1731913`](https://github.com/bobs-org/bob-plugins/commit/1731913b2fa9d856cddc4ee07457f43cbd54489b) | feat(ledger-tools): parse bank notes with the shared cleaner | [bob-cli-oo.1](bob-cli-oo.1.md) | 2026-11-21 13:31:48 EST |
| bob-plugins | [`bob-plugins@d9fe19d`](https://github.com/bobs-org/bob-plugins/commit/d9fe19d8f22f73c360c30812bd5a4a1ac38ba0b8) | feat(ledger-tools): caption bank row notes as quiet prose | [bob-cli-oo.2](bob-cli-oo.2.md) | 2026-11-21 14:17:56 EST |
| bob-cli | [`dfe20ca`](https://github.com/bobs-org/bob-cli/commit/dfe20ca3040b1328b7356083fbb0f8afd4d97d80) | docs(glossary): describe bank row notes | [bob-cli-oo.3](bob-cli-oo.3.md) | 2026-11-21 14:36:44 EST |
| bob-plugins | [`bob-plugins@303e5db`](https://github.com/bobs-org/bob-plugins/commit/303e5dbf534dea3e8225b0f12941e928ddf4490d) | feat(bank): add pure row note write model | [bob-cli-oo.3](bob-cli-oo.3.md) | 2026-11-21 14:44:10 EST |
| bob-plugins | [`bob-plugins@909b30f`](https://github.com/bobs-org/bob-plugins/commit/909b30fdfa004886445f97eed1fa70ec78d103fc) | test(task-status-cycler): refresh shared successor fixture | [bob-cli-oo.3](bob-cli-oo.3.md) | 2026-11-21 14:58:31 EST |
| bob-cli | [`fc27bf1`](https://github.com/bobs-org/bob-cli/commit/fc27bf1ad8694d35bf5ce3729d7a2b3adb5f9d1e) | docs(bank): document the Category card note stage and regenerate the glossary | [bob-cli-oo.4](bob-cli-oo.4.md) | 2026-11-21 16:03:16 EST |
| bob-plugins | [`bob-plugins@604c8a9`](https://github.com/bobs-org/bob-plugins/commit/604c8a9a336cb04bc0ab6288a2b976599da42c09) | feat(bank)!: Space opens a row note stage on the Category card | [bob-cli-oo.4](bob-cli-oo.4.md) | 2026-11-21 16:09:25 EST |
| bob-plugins | [`bob-plugins@ae305a3`](https://github.com/bobs-org/bob-plugins/commit/ae305a32e43e2a94f9c2b810d197a0edfee997ff) | fix(ledger-tools): name concrete note rewrites, declare the note input literal, and trim the page under its cap | [bob-cli-oo](README.md) | 2026-11-21 16:41:28 EST |
| bob-cli--plans | [`bob-cli--plans@da069f0`](https://github.com/bobs-org/bob-cli--plans/commit/da069f05aa3f3ac1f7660cb03e88f8b50ab5b7b4) | chore(plans): mark bank\_row\_notes done after landing bob-cli-oo | [bob-cli-oo](README.md) | 2026-11-21 16:41:56 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-o6.6.1.land][1] | Check active epic notes for already-recorded docs gate issues before routing landing follow-ups | 1 |
| read-by | [agent:bob-cli-oo.4][2] | Need epic context and sibling phase notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-o6.6.1.land/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-oo.4/README.md

<!-- sase:referenced-by:end -->
