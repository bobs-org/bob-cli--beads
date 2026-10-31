# Bead: bob-cli-ex.2.1.3 — Publish project-offer contracts and finish acceptance coverage

[Bead Pages](../README.md) / [bob-cli-ex.2.1](bob-cli-ex.2.1.md) / bob-cli-ex.2.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ex.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ex.2.md) · **Assignee:** `bob-cli-ex.2.1.3` · **Size:** medium
**Created:** 2026-10-31 13:56:45 EDT · **Closed:** 2026-10-31 16:58:37 EDT
**Plan:** [202610/project\_note\_offer\_form.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/project_note_offer_form.md)

## Description

offer_contracts: update capture, project, and successor documentation and only the two glossary strands authorized by the parent epic. Verify equivalence to authored colon bullets and the remaining acceptance matrix, then provide land evidence.

## Notes

[2026-10-31T20:58:31Z · bob-cli-ex.2.1.3] PROPOSED FOLLOW-UP: a trailing #hide on a project-note task bullet (e.g. "- Private reminder #hide") is refused as a type marker (type_marker_not_applicable) for both @r^id@ and @r:id@ — authored #hide must sit mid-text today; decide whether trailing #hide should be exempt from type-marker parsing there (docs examples use "- Private #hide reminder").

[2026-10-31T20:58:37Z · bob-cli-ex.2.1.3] Published offer contracts: docs/capture.md (new 'Offer a new project's tasks' subsection, quick-reference rows, spans/modes/diagnostics, completion intent, sealed toggles, JSON + -p text, stale ^..+ prose fixed), docs/reference/capture-syntax.md (+ search_smoke case), task-dependencies.md 12/12.1/12.4/12.5/12.14, projects.md, task-types.md; glossary:successor-offer and glossary:task-successor updated per memory_glossary=yes and republished with sase memory init + just docs-gen. Acceptance audit: added tests/cli/capture/project_note_offer.rs (13 tests: byte-equal -p all vs authored colon bullets for implicit/explicit-name/typed/scheduled, none/default, eligibility + folds + placeholder/^prj, blocked project, lazy named Pomodoro, typed destinations, mint collisions, mixed Done numbering, batch suppression, human output). Fixed stray ']]' in the human 'added ^id' caption. Verified: cargo fmt --check, just lint (exit 0), cargo test --test cli capture (1195 pass), just test (4236 lib + 2584 cli pass), just docs-check passed; epic-symbols: none.

## Dependencies

- **Depends on:** [bob-cli-ex.2.1.2](bob-cli-ex.2.1.2.md) ✓ · ⧖ 2026-10-31

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ex.2.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ex.2.1.3/README.md) | [bob-cli-ex.2.1.3](bob-cli-ex.2.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e8dd3b6`](https://github.com/bobs-org/bob-cli/commit/e8dd3b650c2f50f0f312d1068641c05ce9aaaa74) | docs(capture): publish project-note offer contracts and acceptance coverage | [bob-cli-ex.2.1.3](bob-cli-ex.2.1.3.md) | 2026-10-31 16:59:34 EDT |
