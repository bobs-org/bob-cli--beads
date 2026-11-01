# Bead: bob-cli-ey.1.1 — cli-directives, split: % directives, bare-# type marker, %t templates, and @@ cleanup

[Bead Pages](../README.md) / [bob-cli-ey.1](bob-cli-ey.1.md) / bob-cli-ey.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ey.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ey.1.md) · **Assignee:** `bob-cli-ey.1.1.land`
**Created:** 2026-10-31 12:58:15 EDT · **Closed:** 2026-10-31 23:25:39 EDT
**Plan:** [202610/cli\_directives\_split.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/cli_directives_split.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/cli_directives_split.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 4 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/cli_directives_split.md

<!-- sase:links:end -->

## Description

Deliver phase cli-directives (bead bob-cli-ey.1) of the "Capture drawers and % directives" epic as a chain of coherent bob-cli changes, each small enough for one coding agent: delete `@@route+id`; add the `%` directive lexer with `%c`, `%n`, and `%l`; split clipboard parsing from reading; make a bare edge `#` an incomplete type marker; replace `@@template:`/`@@@` with `%t`; then add the `directive` completion context, `initial_selection`, and `grammar: 2`. The land agent closes bob-cli-ey.1.

## Notes

[2026-11-01T02:34:41Z · bob-cli-ey.1.1.land] LAND TRIAGE of PROPOSED FOLLOW-UPs: (1) bob-cli-ey.1.1.2 #2 (Mac capture-panel.md still teaches URL % listen and %N/%header clips) -> /sase_new_task found no duplicate task; it is causally part of sibling phase bob-cli-ey.3 (mac-directives, 'update the Mac docs'), recorded as a DISCOVERED ISSUE note on epic bob-cli-ey. (2) bob-cli-ey.1.1.6 #1 (review retirement-grep baseline hits) -> declined, no task: the land agent re-ran the done-when grep and every remaining hit is allowed: docs/develop/decisions.md is generated from the immutable decisions:similar-tasks-are-a-settled-heads-up record; scripts/web_clip/web_clip_adapter.py '@@' is Mermaid fixture text; tests/cli/ref_library/today.rs '-p @@' is an unrelated argument (also flagged by bob-cli-ey.1.1.5); the rest are narrow negative tests (capture_language/tests/rewrite.rs, tests/cli/capture/rewrite.rs, tests/cli/capture/parse_template.rs).

[2026-11-01T03:25:39Z · bob-cli-ey.1.1.land] All six phases (bob-cli-ey.1.1.1–.6) are closed. Their commits are 36c48075, 6ae5df00, 4c011cd7, d7f683a1, 95278934 (all feat(capture)!: with BREAKING CHANGE: footers), and b290d833 (feat(capture):).

There are no Cargo.toml version or CHANGELOG.md edits.

just check and just docs-check pass on this land-cleanup tale (fmt, clippy, 4251 lib tests plus the workspace CLI suite, then the full docs-check gates including generated drift and the first-day tutorial).

In the done-when grep (outside CHANGELOG.md and sase/), the only remaining hits are allowed:
- the generated docs/develop/decisions.md (immutable record);
- Mermaid @@ in scripts/web_clip/web_clip_adapter.py;
- -p @@ in tests/cli/ref_library/today.rs;
- narrow negative tests (capture_language/tests/rewrite.rs, tests/cli/capture/rewrite.rs, tests/cli/capture/parse_template.rs).

Scratch-vault smokes pass:
- capture-parse 'https://example.com/essay %l' emits grammar: 2, mode ref, ref_listen true, and a listen directive span;
- capture-complete 'jot idea %' names → BUILD (1400-1425) · running for a trailing-range open timed Pomodoro;
- bare '#' and '%' report initial_selection: "none" and grammar: 2;
- bob capture --dry-run 'https://example.com/article %l @work' prints would queue … → work · Listen with companion audio requested.

The Capture and Bulk Capture glossary strands match parent §7.

%t notes are on bob-cli-82, 83, 8h, 8i, and 8b.

Integration: the commits that landed in parallel left no retired forms and need none of the new machinery. Those are the project-note offers (9a30ec4c, e9b9cd1d, e8dd3b65, 42dd92bc, 86a63e84), gkeep status (efe2ebe0, 17702dca), and the glossary update (e2838ac3).

This tale deleted the dead parse_clip_markers / _with_clip_control plumbing, finished the %l / %c prose sweep, and aligned the %n detail with execution (shared select_default_pomodoro_line helper).

Follow-up triage:
- The bob-cli-ey.1.1.2 Mac-docs proposal went to epic bob-cli-ey as a DISCOVERED ISSUE for bob-cli-ey.3.
- The bob-cli-ey.1.1.6 grep-review proposal was declined: all hits are allowed.

sase bead epic-symbols bob-cli-ey.1.1 listed none. bob-cli has no just symvision recipe.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ey.1.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ey.1.1.land.md) | [bob-cli-ey.1.1](bob-cli-ey.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a1dcb64`](https://github.com/bobs-org/bob-cli/commit/a1dcb64eee30a3e7f45b0555be8cf60b940d85e1) | refactor(capture): finish cli-directives cleanup | [bob-cli-ey.1.1](bob-cli-ey.1.1.md) | 2026-10-31 23:28:06 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ey.1.1.2--3][1] | Need epic DECISIONS and phase list | 1 |
| read-by | [agent:bob-cli-ey.1.1.4--2][2] | Need epic DECISIONS for phase 4 | 2 |
| read-by | [agent:bob-cli-ey.1.1.5][3] | Need epic decisions | 1 |
| read-by | [agent:bob-cli-ey.1.1.6--4][4] | Need the parent epic's final decisions and close requirements | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ey.1.1.2.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ey.1.1.4.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ey.1.1.5/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ey.1.1.6.md

<!-- sase:referenced-by:end -->
