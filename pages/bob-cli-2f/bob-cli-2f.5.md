# Bead: bob-cli-2f.5 — Split src/native/dataview.rs

[Bead Pages](../README.md) / [bob-cli-2f](README.md) / bob-cli-2f.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.2u](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.2u.md) · **Assignee:** `bob-cli-2f.5` · **Size:** large
**Created:** 2026-09-28 16:49:29 EDT · **Closed:** 2026-09-28 19:06:32 EDT
**Plan:** [202609/split\_largest\_rust\_files.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/split_largest_rust_files.md)

## Description

split-dataview: move the Obsidian engine, native evaluator, function library, lexer/parser, sources, errors, and CLI out of the dataview root into new files under the existing dataview directory.

## Notes

[2026-09-28T23:06:32Z · bob-cli-2f.5] Split 7088-line src/native/dataview.rs into 19 modules under src/native/dataview/ (root coordinator 131 lines; cli 546; error 241; eval 320; functions/{scalar 247, link_numeric 181, collection 388, string 328, datetime 503, compare 261}; lexer 257; native 247; obsidian 463; output 139; parser 1096; render 258; sources 617; vault 903; tests 240). All files <=1500 lines. Test count 1794 matches baseline, 9 dataview unit tests unchanged, lib 1139 + cli 515 suites green, cargo fmt clean, no new compiler/clippy warnings, bob query --help byte-identical, crate::native::dataview::DataviewError path retained. PROPOSED FOLLOW-UP: cargo clippy --all-targets fails on clean base too (deny clippy::overly_complex_bool_expr at tests/cli/capture/pomodoro_name.rs:808, untouched by this phase), so just lint stays red independent of this split.

## Dependencies

- **Depends on:** [bob-cli-2f.4](bob-cli-2f.4.md) ✓ · ⧖ 2026-09-28
- **Blocks:** [bob-cli-2f.6](bob-cli-2f.6.md) ✓ · ⧖ 2026-09-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2f.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-2f.5.md) | [bob-cli-2f.5](bob-cli-2f.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`2307179`](https://github.com/bobs-org/bob-cli/commit/2307179cd17439fc6bb2a14eecbc842189ab0199) | refactor(dataview): split query module into cohesive submodules | [bob-cli-2f.5](bob-cli-2f.5.md) | 2026-09-28 19:08:56 EDT |
