# Bead: bob-cli-ey.1.1.6 — directive completion context, bare-# menu, initial\_selection, and grammar 2

[Bead Pages](../README.md) / [bob-cli-ey.1.1](bob-cli-ey.1.1.md) / bob-cli-ey.1.1.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ey.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ey.1.md) · **Assignee:** `bob-cli-ey.1.1.6` · **Size:** medium
**Created:** 2026-10-31 12:58:15 EDT · **Closed:** 2026-10-31 22:11:13 EDT
**Plan:** [202610/cli\_directives\_split.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/cli_directives_split.md)

## Description

directive-completion-grammar: add the `directive` completion context (`capture_complete/directives.rs`: rows c, n, t, then l on bare-URL items, bob-authored names/summaries/details/disabled reasons, no clipboard read); open the `task_type` context on a bare edge `#` with every row; emit `initial_selection: "none"` only for an empty query opened by bare `#` or `%`; add `GRAMMAR_REVISION = 2` as top-level `grammar` in capture-parse and capture-complete; zsh `%<TAB>` and bare `#<TAB>`; finish docs (Grammar at a glance), the Capture glossary strand, and the retirement grep. Commit as `feat(capture):`.

## Notes

[2026-11-01T01:56:00Z · bob-cli-ey.1.1.6--3] PROPOSED FOLLOW-UP: The retirement grep has no new text matches against HEAD. Its preserved matches are the old @template mention in docs/develop/decisions.md, generic @@ examples in scripts/web_clip/web_clip_adapter.py and tests/cli/ref_library/today.rs, and narrow negative capture rewrite/template tests; exact git grep also reports existing binary font matches. Review these baseline-only hits when the land-agent grep is finalized.

[2026-11-01T02:11:13Z · bob-cli-ey.1.1.6--4] Implemented directive and bare-# completion, initial_selection, and grammar 2; docs and Capture glossary are updated. Verified just docs-check && just check passed, the retirement sweep has no new text matches vs HEAD, and epic-symbols has no leftovers.

## Dependencies

- **Depends on:** [bob-cli-ey.1.1.4](bob-cli-ey.1.1.4.md) ✓ · ⧖ 2026-10-31
- **Depends on:** [bob-cli-ey.1.1.5](bob-cli-ey.1.1.5.md) ✓ · ⧖ 2026-10-31

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ey.1.1.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ey.1.1.6.md) | [bob-cli-ey.1.1.6](bob-cli-ey.1.1.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b290d83`](https://github.com/bobs-org/bob-cli/commit/b290d833008347581c121f72cf70b6edb3e38810) | feat(capture): add directive completion and grammar revision | [bob-cli-ey.1.1.6](bob-cli-ey.1.1.6.md) | 2026-10-31 22:12:08 EDT |
