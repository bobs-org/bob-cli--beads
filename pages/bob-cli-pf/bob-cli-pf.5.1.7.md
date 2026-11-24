# Bead: bob-cli-pf.5.1.7 — Verify property editor parity in Obsidian and deploy

[Bead Pages](../README.md) / [bob-cli-pf.5.1](bob-cli-pf.5.1.md) / bob-cli-pf.5.1.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pf.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.5.md) · **Assignee:** `bob-cli-pf.5.1.7` · **Size:** medium
**Created:** 2026-11-23 12:39:52 EST · **Closed:** 2026-11-23 20:03:55 EST
**Plan:** [202611/property\_editor\_parity.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/property_editor_parity.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:62ca3f23086f9033d49ae4ef | attached via sase artifact create --bead |

<!-- sase:links:end -->

## Description

acceptance: extend the existing scratch-vault real-Obsidian runner for all parity actions, review visual evidence, update the native Properties parity reference, run required gates, and sync the plugins.

## Notes

[2026-11-24T01:03:35Z · bob-cli-pf.5.1.7] PROPOSED FOLLOW-UP: Harden focusApplicationWindow fixed-coordinate clicks for narrow viewports — modal close/reopen at 390px dropped CDP in acceptance; restoring 1400/light after captures works around it, but the root trigger (click at 360,24 near the window edge vs an Electron compositor issue) is unproven

[2026-11-24T01:03:55Z · bob-cli-pf.5.1.7] Acceptance complete: real-Obsidian run PASSES (263 assertions, 0 fail, full coverage incl. all 21 new parity checks, 0 plugin errors, 0 console exceptions) on athena with pinned bob 0.6.0 built from 588c6210 plus the set_yaml fix (provenance manifest verified). Evidence: file:explicit:62ca3f23086f9033d49ae4ef (report + 28 screenshots, 24 parity + 4 standard, layout probes all pass). Reviewed marked/filter/rename/YAML/paste/convert/standard pixels across light/dark/narrow/wide: focus, marks gutter, selected-vs-marked contrast, no overlap/overflow. Root-cause fixes landed in-phase: (1) bob-cli multiline set_yaml replace dropped its trailing newline and glued lines (opaque verify fail) — fixed rebuild_entry_with_value + golden case; (2) 298p Esc filter-clear skipped repaint when a query was set, stranding the layer — now always repaints + unit test; (3) 298r source adapter dropped inter-entry comments (bob prop.move proves they belong to the following entry) — adapter now attaches leading trivia per bob model + unit test; copy/paste e2e proves source-exact copy. Also fixed 2 stale grouped-traversal assumptions the selection-filter phase outdated (core keyboard nav + surfaces visual review now click the derived row after proving keyboard moves). Docs: parity table added to property-editor.md, validation walkthrough extended, docs:check 447 pass. Gates: cargo fmt/clippy/lib(7995)/cli(4077) green; npm build/build:check/docs checks green; focused suites (197+11+37+12) green. bob plugins sync clean (0 errors, ledger-tools redeployed with fixes). Type manager probed present (setType function); vault type change confirmed inside scratch vault only. One PROPOSED FOLLOW-UP recorded (narrow-viewport focus-click hardening). No --epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-pf.5.1.6](bob-cli-pf.5.1.6.md) ✓ · ⧖ 2026-11-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pf.5.1.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.5.1.7/README.md) | [bob-cli-pf.5.1.7](bob-cli-pf.5.1.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`8d82c62`](https://github.com/bobs-org/bob-cli/commit/8d82c621b25d1595ec8a495c30f6087fbc87f524) | fix(props): keep trailing newline on multiline set\_yaml replace | [bob-cli-pf.5.1.7](bob-cli-pf.5.1.7.md) | 2026-11-23 20:05:34 EST |
