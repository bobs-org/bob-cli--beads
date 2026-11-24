# Bead: bob-cli-pf.5.1.5 — Add YAML copy and overwrite-previewed paste

[Bead Pages](../README.md) / [bob-cli-pf.5.1](bob-cli-pf.5.1.md) / bob-cli-pf.5.1.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pf.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.5.md) · **Assignee:** `bob-cli-pf.5.1.5` · **Size:** medium
**Created:** 2026-11-23 12:39:51 EST · **Closed:** 2026-11-23 15:46:35 EST
**Plan:** [202611/property\_editor\_parity.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/property_editor_parity.md)

## Description

clipboard: wire keyboard and menu copy/paste, show ordered new/replaced/skipped keys, and apply the exact approved editable subset in one guarded undoable batch.

## Notes

[2026-11-23T20:46:35Z · bob-cli-pf.5.1.5] Implemented YAML clipboard copy/paste with ordered New/Replace/Skipped planning, dry-run probes, guarded preview/apply of one undoable batch, and stale/ownership/malformed/recovery handling. Verified 177 property-editor tests, npm run build:check, and git diff --check. epic-symbols is empty. bob plugins sync was attempted but refused to overwrite the vault's stamped uncommitted bob-ledger-tools build from another workspace; no force overwrite was performed.

## Dependencies

- **Depends on:** [bob-cli-pf.5.1.4](bob-cli-pf.5.1.4.md) ✓ · ⧖ 2026-11-23
- **Blocks:** [bob-cli-pf.5.1.6](bob-cli-pf.5.1.6.md) ✓ · ⧖ 2026-11-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pf.5.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.5.1.5/README.md) | [bob-cli-pf.5.1.5](bob-cli-pf.5.1.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@a73f70b`](https://github.com/bobs-org/bob-plugins/commit/a73f70bf4f22c0916e95546275594fd825036e9a) | feat(property-editor): add guarded YAML clipboard paste | [bob-cli-pf.5.1.5](bob-cli-pf.5.1.5.md) | 2026-11-23 15:48:09 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pf.5.1.5][1] | Need the phase scope, design file, and prior work notes before continuing this assigned phase | 3 |
| read-by | [agent:bob-cli-pf.5.1.land][2] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.5.1.5/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.5.1.land/README.md

<!-- sase:referenced-by:end -->
