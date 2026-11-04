# Bead: bob-cli-go.6 — Configurable merge labels in config, capture \`~\`/\`~~\`, and completion

[Bead Pages](../README.md) / [bob-cli-go](README.md) / bob-cli-go.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.36.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.36.linker.w0.md) · **Assignee:** `bob-cli-go.6` · **Size:** medium
**Created:** 2026-11-03 16:11:31 EST · **Closed:** 2026-11-04 01:33:17 EST
**Plan:** [202611/task\_move\_merge\_split.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_move_merge_split.md)

## Description

merge-label: add relations.merge_labels and LabelEffect::Merge with the four-list overlap rule, dispatch merges from capture relation commits through the engine, flag merge labels in capture-parse, capture-complete, completion, and `bob relations list`, and enable the label in chezmoi.

## Notes

[2026-11-04T05:47:07Z · bob-cli-go.6] PROPOSED FOLLOW-UP: Restore required front matter on sase/memory/glossary/task-merge.md so docs-gen and docs-check generated-drift can run; both gates stop on “memory strand has no front matter” in this unchanged base file after docs lint passes. Existing reports: bob-cli-go.8 note #1 and bob-cli-go.4.1.3 note #1.

[2026-11-04T06:33:17Z · bob-cli-go.6] Implemented relations.merge_labels and end-to-end capture merge dispatch, completion cues, relation listing, and rename/reverse warnings. Verified just check succeeded (586538 ms), targeted merge and completion-cue CLI tests passed, generated CLI snapshots updated, and git diff --check is clean. docs-check generated-drift remains blocked by the pre-existing missing front matter in sase/memory/glossary/task-merge.md; recorded as a proposed follow-up with existing bead references.

## Dependencies

- **Blocks:** [bob-cli-go.10](bob-cli-go.10.md) ◐ · ⧖ 2026-11-03
- **Depends on:** [bob-cli-go.4](bob-cli-go.4.md) ✓ · ⧖ 2026-11-03
- **Blocks:** [bob-cli-go.9](bob-cli-go.9.md) ◐ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-go.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-go.6/README.md) | [bob-cli-go.6](bob-cli-go.6.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`3741ce2`](https://github.com/bobs-org/bob-cli/commit/3741ce2e79e5341942d2ff57cc536c8bd27c0799) | feat(capture): add configurable merge relations | [bob-cli-go.6](bob-cli-go.6.md) | 2026-11-04 01:37:01 EST |
| chezmoi | [`chezmoi@5699cb0`](https://github.com/bbugyi200/dotfiles/commit/5699cb01bb5f6efd5ce7dc7e5c709316e666903d) | feat(config): enable merged-into relation defaults | [bob-cli-go.6](bob-cli-go.6.md) | 2026-11-04 01:37:42 EST |
