# Bead: gh\_bobs-org\_\_bob-cli-5.1 — Config schema for \`values: priority\`

[Bead Pages](../README.md) / [gh\_bobs-org\_\_bob-cli-5](README.md) / gh\_bobs-org\_\_bob-cli-5.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.s8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.s8/README.md) · **Assignee:** `gh_bobs-org__bob-cli-5.1` · **Size:** medium
**Created:** 2026-08-03 08:08:24 UTC · **Closed:** 2026-08-03 08:14:36 UTC
**Plan:** [202608/priority\_property.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/priority_property.md)

## Description

config: teach the bullet-property config loader a `values: priority` kind with a validated `levels` list (label, value, day range) and a `schedules` target, and add the `priority` entry to the chezmoi-managed bob/config.yml.

## Notes

[2026-08-03T08:14:36Z · gh_bobs-org__bob-cli-5.1] Verified priority config normalization and validation with focused tests and the full bob-plugins suite (253/253 passing); npm run validate passed 6/6 manifests; managed YAML parsed with default scheduled target and P2/P3/P4 levels; both repo diffs pass git diff --check; synced bob-navigation-hotkeys and confirmed deployed main.js matches source.

## Dependencies

- **Blocks:** [gh\_bobs-org\_\_bob-cli-5.2](gh_bobs-org__bob-cli-5.2.md) ✓

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.gh\_bobs-org\_\_bob-cli-5.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.gh_bobs-org__bob-cli-5.1/README.md) | [gh\_bobs-org\_\_bob-cli-5.1](gh_bobs-org__bob-cli-5.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed (UTC) |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@8669c7e`](https://github.com/bobs-org/bob-plugins/commit/8669c7eab8fcb6a3ceb3fcba47e317e6b88004ed) | feat(navigation): validate priority property configuration | [gh\_bobs-org\_\_bob-cli-5.1](gh_bobs-org__bob-cli-5.1.md) | 2026-08-03 08:15:53 |
| chezmoi | [`chezmoi@c4d233b`](https://github.com/bbugyi200/dotfiles/commit/c4d233bb350f92377d02a1e754f992395a0947c3) | feat(bob): configure priority property levels | [gh\_bobs-org\_\_bob-cli-5.1](gh_bobs-org__bob-cli-5.1.md) | 2026-08-03 08:16:22 |
