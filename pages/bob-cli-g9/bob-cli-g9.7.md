# Bead: bob-cli-g9.7 — Glossary, decision record, and final config

[Bead Pages](../README.md) / [bob-cli-g9](README.md) / bob-cli-g9.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.32.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.32.linker.w0.md) · **Assignee:** `bob-cli-g9.7` · **Size:** small
**Created:** 2026-11-02 15:55:43 EST · **Closed:** 2026-11-02 21:20:27 EST
**Plan:** [202611/task\_decay\_ladder.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_decay_ladder.md)

## Description

memory-config: add the task-decay glossary strand and the task-decay-is-one-ladder decision record, correct the keep-streak, rotten-log, and task-freshness strands, mark four superseded records, regenerate the docs pages, and replace the interim chezmoi keeps with explicit per-rung allowances.

## Notes

[2026-11-03T02:20:27Z · bob-cli-g9.7] Memory-config done and verified: new glossary:task-decay strand and decisions:task-decay-is-one-ladder record; four records marked superseded-in-part with back-links (rotten-keeps-use-priority-decay, rotten-keeps-are-logged, next-keeps-ask-an-optional-rotten-reason, task-lanes-are-sticky); keep-streak/rotten-log/task-freshness strands corrected for the ladder. sase memory init clean (only pre-existing unrelated link warnings); just docs-gen exit 0 (glossary.md + decisions.md regenerated with the new entries); just docs-check 447 passed. Chezmoi interim keeps:2 replaced with final pending/next/ready_keeps:2 + enter:P1 (rolls:2 already present; YAML parses, keys match Rust parser); left uncommitted for land — needs commit + chezmoi update -a --force, and athena/Mac need the same update. No epic-symbols; no follow-ups.

## Dependencies

- **Depends on:** [bob-cli-g9.5](bob-cli-g9.5.md) ✓ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-g9.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-g9.7/README.md) | [bob-cli-g9.7](bob-cli-g9.7.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`807e181`](https://github.com/bobs-org/bob-cli/commit/807e1816560696672483eeedfbe647fca9dd8898) | docs(memory): task decay ladder glossary, decision record, and regenerated pages | [bob-cli-g9.7](bob-cli-g9.7.md) | 2026-11-02 21:22:11 EST |
| chezmoi | [`chezmoi@4854d40`](https://github.com/bbugyi200/dotfiles/commit/4854d40badff26ed110f94dd52e229e384ef7c6b) | feat(bob): final per-rung task decay allowances | [bob-cli-g9.7](bob-cli-g9.7.md) | 2026-11-02 21:23:14 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-g9.7][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-g9.7/README.md

<!-- sase:referenced-by:end -->
