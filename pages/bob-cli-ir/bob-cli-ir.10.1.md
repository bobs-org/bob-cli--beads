# Bead: bob-cli-ir.10.1 — Mac Record Card and guided entry

[Bead Pages](../README.md) / [bob-cli-ir.10](bob-cli-ir.10.md) / bob-cli-ir.10.1

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-ir.10](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ir.10.md) · **Assignee:** `bob-cli-ir.10.1.land`
**Created:** 2026-11-09 02:49:44 EST
**Plan:** [202611/mac\_record\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_record_card.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/mac_record_card.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_record_card.md

<!-- sase:links:end -->

## Description

Complete bob-cli-ir.10 with a thin-client Record Card, undoable guided field entry, record-aware keyboard behavior, accessible styling, and compiled Swift verified by exact-SHA macOS CI.

## Notes

[2026-11-09T12:25:22Z · bob-cli-ir.10.1.land] FOLLOW-UP TRIAGE: Read all notes on phases .1-.4. The sole PROPOSED FOLLOW-UP is bob-cli-ir.10.1.4 note #4 (optional More rows Visited/Url misalign, CI run 42611020479). Declined as a separate task because RecordCardView introduced it in this epic; retain it as required remaining epic work in the repair tale. No distinct non-epic follow-ups were found, so no new task or duplicate corroboration is warranted.

[2026-11-09T12:26:21Z · bob-cli-ir.10.1.land] LANDING AUDIT: All 8 child notes reviewed (.1 one, .2 one, .3 one, .4 five). Verified bob-cli named-field commit 5e49fa5e and Mac commits 1e6fb18, 7933c7e, 8c13ac4, 4bca5da against source, fixtures and tests. No memory, release-version or changelog changes in this child; schema 1, assist_version 1, and the existing Mac grammar gate are retained. Phase .3 macOS verification gap and .4 failed-CI fixes were resolved by CI 42611020479: snapshot 1e507e9cf9d982f8fb52e439a651437d4635dc97 has tree b9ee8b3024615983df9c95ade77cbdb4d90bdceb, identical to Mac HEAD 4bca5da; Build, Test, Bundle, Launch and Install all passed. Source confirms Bob-authored replacements, native undo, scoped metadata, optional decoding and no writes on assist. However completion presentation is incomplete: CapturePanelView prioritizes RecordCardView over the inline list; RecordCardView only projects record_value responses, so record_field and newly landed record_target rows can be keyboard-accepted invisibly. Value rows never consume selectedCompletionIndex, inlineValues drops everything after six, and More-row widths differ. footerIsRefusal treats every nonempty status including Ready as an error, suppressing the planned hints. These remain epic work; a bounded repair tale will finish the landing.

[2026-11-09T12:26:25Z · bob-cli-ir.10.1.land] INTEGRATION AUDIT: bob-cli HEAD/origin master 941ee724; first child implementation 5e49fa5e, plus contemporaneous 8cc4a754 and later non-child commits 12641768, 96196052, 1c4939b9, a729a8fd, 070d2aac, 941ee724 reviewed. Record-update landing preserves and extends -F/record.edit (current-value prefills and lossless-spelling guard), with CLI reparsing tests. Its record_target response at a create route now exposes the invisible-acceptance integration bug described in the audit. Fix visible generic completion ownership without taking over full revisit cards/current-before-after UI, which belongs to outer phase mac-record-revisits. Sized Nx close adds a separate semantic mode/diagnostic and does not require local Record Card grammar. Mac origin/master has only this child epic commits since e5b5889; no unrelated Mac drift. epic-symbols currently reports none for bob-cli-ir.10.1 or parent phase bob-cli-ir.10. Both remain open pending the repair tale; no force close, no check-full.

[2026-11-09T12:29:46Z · bob-cli-ir.10.1.land] ADDITIONAL CONTRACT CHECK: Re-read the exact card-surface section. It requires the type emoji as a presentation adornment on the editor record_route chip, preserving draft bytes and offsets. Current CaptureEditorPalette/CompletionRowContent comments explicitly put the emoji on the Record Card only; the editor has a wash but no route emoji adornment. The repair tale includes completing that original requirement with offset/copy/selection coverage.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ir.10.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ir.10.1.land.md) | [bob-cli-ir.10.1](bob-cli-ir.10.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@c09e2bc`](https://github.com/bobs-org/bob-mac-capture/commit/c09e2bcd6538e90c56030374900550a1d6053817) | fix(capture): agree Record Card completion with keyboard acceptance | [bob-cli-ir.10.1](bob-cli-ir.10.1.md) | 2026-11-09 08:28:34 EST |
| bob-mac-capture | [`bob-mac-capture@eded3b9`](https://github.com/bobs-org/bob-mac-capture/commit/eded3b9ca680244939ec9c69a71dac7484e4b683) | fix(capture): keep Record Return through last-field analysis | [bob-cli-ir.10.1](bob-cli-ir.10.1.md) | 2026-11-09 09:10:10 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ir.10.1.1][1] | Need parent epic DECISIONS and any notes about field-addressing | 2 |
| read-by | [agent:bob-cli-ir.10.1.3][2] | Need the parent epic decisions and design context governing this phase | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ir.10.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ir.10.1.3/README.md

<!-- sase:referenced-by:end -->
