# Bead: bob-cli-ey.1.1.6 — directive completion context, bare-# menu, initial\_selection, and grammar 2

[Bead Pages](../README.md) / [bob-cli-ey.1.1](bob-cli-ey.1.1.md) / bob-cli-ey.1.1.6

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ey.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ey.1.md) · **Assignee:** `bob-cli-ey.1.1.6` · **Size:** medium
**Created:** 2026-10-31 12:58:15 EDT
**Plan:** [202610/cli\_directives\_split.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/cli_directives_split.md)

## Description

directive-completion-grammar: add the `directive` completion context (`capture_complete/directives.rs`: rows c, n, t, then l on bare-URL items, bob-authored names/summaries/details/disabled reasons, no clipboard read); open the `task_type` context on a bare edge `#` with every row; emit `initial_selection: "none"` only for an empty query opened by bare `#` or `%`; add `GRAMMAR_REVISION = 2` as top-level `grammar` in capture-parse and capture-complete; zsh `%<TAB>` and bare `#<TAB>`; finish docs (Grammar at a glance), the Capture glossary strand, and the retirement grep. Commit as `feat(capture):`.

## Dependencies

- **Depends on:** [bob-cli-ey.1.1.4](bob-cli-ey.1.1.4.md) ✓ · ⧖ 2026-10-31
- **Depends on:** [bob-cli-ey.1.1.5](bob-cli-ey.1.1.5.md) ✓ · ⧖ 2026-10-31

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ey.1.1.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ey.1.1.6/README.md) | [bob-cli-ey.1.1.6](bob-cli-ey.1.1.6.md) | 0 |
