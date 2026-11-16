# Bead: bob-cli-mf.1 — Quick fixes that ship before the redesign

[Bead Pages](../README.md) / [bob-cli-mf](README.md) / bob-cli-mf.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.51.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.51.linker.w0.md) · **Assignee:** `bob-cli-mf.1` · **Size:** small
**Created:** 2026-11-16 15:38:38 EST · **Closed:** 2026-11-16 15:45:50 EST
**Plan:** [202611/schema\_editor\_arrange\_and\_emoji.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/schema_editor_arrange_and_emoji.md)

## Description

quick-fixes: stop q from cancelling inside bank inputs, keep a bank category's emoji when its label is edited, make Alt+J/K work with macOS Option, and port bob's split_icon so album choice splitting matches Rust.

## Notes

[2026-11-16T20:45:50Z · bob-cli-mf.1] Implemented all four quick fixes in bob-ledger-tools: input q no longer cancels bank stages, category label edits preserve emoji, Option+J/K match KeyJ/KeyK, and album choice splitting follows Rust split_icon. Verified npm run build, npm run build:check, git diff --check, and bob plugins sync; no epic symbols remained.

## Dependencies

- **Blocks:** [bob-cli-mf.2](bob-cli-mf.2.md) ✓ · ⧖ 2026-11-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-mf.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-mf.1/README.md) | [bob-cli-mf.1](bob-cli-mf.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@e35afc1`](https://github.com/bobs-org/bob-plugins/commit/e35afc1fa0c331883ff9dc2691f1cf735be3df21) | fix(bank): preserve category emoji and editor shortcuts | [bob-cli-mf.1](bob-cli-mf.1.md) | 2026-11-16 15:46:44 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-mf.1][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-mf.1/README.md

<!-- sase:referenced-by:end -->
