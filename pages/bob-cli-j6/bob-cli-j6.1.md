# Bead: bob-cli-j6.1 — bob capture-rewrite turns \`.\` into \`&\` and \`;\` into \`\*\`

[Bead Pages](../README.md) / [bob-cli-j6](README.md) / bob-cli-j6.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1aj](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1aj.md) · **Assignee:** `bob-cli-j6.1` · **Size:** medium
**Created:** 2026-11-09 11:06:45 EST · **Closed:** 2026-11-09 11:32:06 EST
**Plan:** [202611/dot\_semicolon\_modifier\_aliases.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/dot_semicolon_modifier_aliases.md)

## Description

bob-modifier-aliases: add the completion-gated `.` → `&` and `;` → `*` fallbacks after the existing `.`/`;` rules, with unit and CLI tests, help and docs inside the word budgets, and the glossary alias list.

## Notes

[2026-11-09T16:32:02Z · bob-cli-j6.1] Plan correction for phase 2 and land: the plan's literal-row `  ;` (indent-only) is not literal on master. A whole-item `;` already aliases `:` when indented, so it is now a precedence row in rewrite.rs tests. Phase 2 can rely on `  ;` -> `  :` unchanged.

[2026-11-09T16:32:06Z · bob-cli-j6.1] Added completion-gated '.'->'&' and ';'->'*' fallbacks (expand_dot_dependency_alias, expand_semicolon_blocked_task_alias via expand_modifier_fallback_alias) after the existing '.'/';' rules in capture_language/rewrite.rs. Applied leading_dot=after_text, so leading dots stay literal. Unit and CLI tests added; help text, docs/capture.md, and capture-syntax.md (6000 words, at cap) updated; just docs-gen run; glossary:capture-alias bullet added. Verified: just check exits 0 (9952 tests passed, 0 failed); just docs-check shows only the 3 baseline Mac-page budget errors (bob-cli-h9); built binary returns the exact contract JSON for '@home .' and 'Buy milk ;'.

## Dependencies

- **Blocks:** [bob-cli-j6.2](bob-cli-j6.2.md) ✓ · ⧖ 2026-11-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-j6.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-j6.1/README.md) | [bob-cli-j6.1](bob-cli-j6.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`0f31c59`](https://github.com/bobs-org/bob-cli/commit/0f31c592fc22800923e556b70066704603fad526) | feat(capture): alias . to & and ; to \* in capture drafts | [bob-cli-j6.1](bob-cli-j6.1.md) | 2026-11-09 11:32:59 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-j6.1][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-j6.1/README.md

<!-- sase:referenced-by:end -->
