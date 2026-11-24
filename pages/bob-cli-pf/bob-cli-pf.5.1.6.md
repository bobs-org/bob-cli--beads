# Bead: bob-cli-pf.5.1.6 — Add local kind conversion and explicit vault type changes

[Bead Pages](../README.md) / [bob-cli-pf.5.1](bob-cli-pf.5.1.md) / bob-cli-pf.5.1.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pf.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.5.md) · **Assignee:** `bob-cli-pf.5.1.6` · **Size:** medium
**Created:** 2026-11-23 12:39:52 EST · **Closed:** 2026-11-23 16:18:26 EST
**Plan:** [202611/property\_editor\_parity.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/property_editor_parity.md)

## Description

kind-change: preview and apply loose-value conversions; feature-detect Obsidian's type manager and require a separate confirmation naming affected notes before changing a vault-wide property type.

## Notes

[2026-11-23T21:18:26Z · bob-cli-pf.5.1.6] Kind conversion lands in 298u: t/T and Change kind open a previewed conversion stage using existing parsers plus YAML for maps; note-local prop.set/prop.set_yaml never touches vault type. Feature-detected metadataTypeManager.setType requires a separate confirmation naming key, type, and note count; missing/throwing/async adapters and failed setters make no global change and skip property undo. 20/20 kind-change tests, 23/23 including prose-field roles, 110 related editor tests, build:check, and docs:check passed. bob-ledger-tools synced to the vault. No leftover --epic-symbol entries.

## Dependencies

- **Depends on:** [bob-cli-pf.5.1.5](bob-cli-pf.5.1.5.md) ✓ · ⧖ 2026-11-23
- **Blocks:** [bob-cli-pf.5.1.7](bob-cli-pf.5.1.7.md) ✓ · ⧖ 2026-11-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pf.5.1.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.5.1.6/README.md) | [bob-cli-pf.5.1.6](bob-cli-pf.5.1.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@d3a17f0`](https://github.com/bobs-org/bob-plugins/commit/d3a17f0c1793c742f0200cef48c130f80d6ffc1d) | feat(property-editor): preview kind conversion and confirm vault type changes | [bob-cli-pf.5.1.6](bob-cli-pf.5.1.6.md) | 2026-11-23 16:20:03 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pf.5.1.6][1] | Need the phase scope and design file | 5 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.5.1.6/README.md

<!-- sase:referenced-by:end -->
