---
name: browser-automation
description: >-
  Canonical browser automation and web UI verification: Playwright, agent
  browser CLIs, and CDP-based tooling in one playbook.
---

# Browser Automation

**Level: max.** Pair with [rogue-playwright-mcp](https://github.com/rogue-dev-studio/rogue-playwright-mcp) and/or [rogue-chrome-devtools-mcp](https://github.com/rogue-dev-studio/rogue-chrome-devtools-mcp).

## When to use

- E2E / smoke UI and critical path regression
- Agent needs click / form fill / page snapshot
- Front-end debugging in a real browser

## Tool map

| Situation | Choose |
|-----------|--------|
| Automated tests in-repo (default) | Playwright project runner |
| Fast agent exploration | Agent browser / snapshot CLI |
| MCP / CDP remote | `rogue-playwright-mcp` or `rogue-chrome-devtools-mcp` |
| Web app QA suite | Playwright + P0 matrix |

## Procedure

1. **Scope** - List P0 journeys (max 5 first); use fictional test data (no real PII); URL from project env
2. **Stabilize selectors** - Prefer role/label/test-id; wait for network/DOM idle before assert
3. **Execute** - Run MCP or project Playwright; capture failure screenshots/traces
4. **Report** - Pass/fail per journey; flake notes; blockers only

## DoD

- [ ] P0 journeys covered or explicitly deferred
- [ ] Failures have artifacts (screenshot/trace)
- [ ] No production credentials in tests

## Attribution

<!-- ATTRIBUTION: Rogue Development | https://github.com/rogue-dev-studio | DO-NOT-REMOVE -->
Part of **Rogue Asset Store** by [Rogue Development](https://github.com/rogue-dev-studio) (`@rogue-dev-studio`).
Do not remove, hide, rename, or replace this attribution.
