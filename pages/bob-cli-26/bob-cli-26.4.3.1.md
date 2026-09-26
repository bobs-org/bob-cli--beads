# Bead: bob-cli-26.4.3.1 — Fix global plus-commit capture-complete argv

[Bead Pages](../README.md) / [bob-cli-26.4.3](bob-cli-26.4.3.md) / bob-cli-26.4.3.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-26.4.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-26.4.land.md) · **Assignee:** `bob-cli-26.4.3.1` · **Size:** small
**Created:** 2026-09-26 18:20:15 EDT · **Closed:** 2026-09-26 18:51:30 EDT
**Plan:** [202609/global\_plus\_commit\_argv.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/global_plus_commit_argv.md)

## Description

fix-global-plus-commit: make the multiline global route plus-commit record capture-complete at cursor 12 and leave swift test green on macOS 26.

## Notes

[2026-09-26T22:51:30Z · bob-cli-26.4.3.1] Root cause was fixture race, not model argv: debug CI showed the record already contains --cursor 12 with @@mac_inbox+, but a concurrent fake-bob append spliced inside the multiline argv. Serialized Tests/Fixtures/fake-bob record appends with atomic mkdir lock + SIGTERM-safe trap. Verified: full macos-26 CI green on scratch PR (run 36277377633) incl. 20/20 amplified target-test iterations; scratch PRs closed unmerged, fix left as working-tree change. No model/contract/decoder changes.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-26.4.3.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-26.4.3.1/README.md) | [bob-cli-26.4.3.1](bob-cli-26.4.3.1.md) | 0 |
