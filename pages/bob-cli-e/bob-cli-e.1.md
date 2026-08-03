# Bead: bob-cli-e.1 — Config schema for \`values: priority\`

[Bead Pages](../README.md) / [bob-cli-e](README.md) / bob-cli-e.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.s8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.s8/README.md) · **Assignee:** `bob-cli-e.1` · **Size:** medium
**Created:** 2026-08-03 04:08:24 EDT · **Closed:** 2026-08-03 04:14:36 EDT
**Plan:** [202608/priority\_property.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/priority_property.md)

## Description

config: teach the bullet-property config loader a `values: priority` kind with a validated `levels` list (label, value, day range) and a `schedules` target, and add the `priority` entry to the chezmoi-managed bob/config.yml.

## Notes

[2026-08-03T08:14:36Z · bob-cli-e.1] Verified priority config normalization and validation with focused tests and the full bob-plugins suite (253/253 passing); npm run validate passed 6/6 manifests; managed YAML parsed with default scheduled target and P2/P3/P4 levels; both repo diffs pass git diff --check; synced bob-navigation-hotkeys and confirmed deployed main.js matches source.

## Dependencies

- **Blocks:** [bob-cli-e.2](bob-cli-e.2.md) ✓

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-e.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-e.1/README.md) | [bob-cli-e.1](bob-cli-e.1.md) | 0 |
