---
name: 1c-development-standards
description: Use for 1C:Enterprise and BSL development tasks to load only the relevant standards copied from ai_rules_1c/content/standards.
---

# 1C Development Standards

Use this skill for 1C:Enterprise development, BSL code changes, code review, metadata design, forms, DCS, registers, extensions, transactions, and debugging.

This plugin intentionally packages **only** the standards copied from `ai_rules_1c/content/standards`. Do **not** assume the rest of the repository rules are available through this plugin. If a task needs broader team process, project-specific tooling, or MCP routing rules, get them from the active workspace separately.

## Required behavior

1. Confirm that the task is actually about 1C / BSL / metadata / BSP. If not, do not use this skill.
2. Before implementing or reviewing, identify the minimum relevant files from `../../references/standards/`.
3. Read each selected standard file completely before acting on it.
4. Apply only the selected standards. Do not load the full standards set unless the task genuinely spans multiple areas.
5. In the final response, briefly name which standards were used when the task is non-trivial.

## Baseline routing

- For any BSL writing or review:
  - `../../references/standards/dev-standards-code-style.md`
  - `../../references/standards/dev-standards-architecture.md`
  - `../../references/standards/anti-patterns.md`
- For choosing platform mechanisms over custom code:
  - `../../references/standards/platform-solutions.md`
- For debugging or production issue analysis:
  - `../../references/standards/systematic-debugging.md`

## Topic routing

- Forms, client/server form logic, command bars, form handlers:
  - `../../references/standards/form-patterns.md`
- Async client flow, background interactions, non-blocking UI:
  - `../../references/standards/async-methods.md`
- DCS / SKD report schema or settings:
  - `../../references/standards/dcs-design.md`
- Advanced DCS composition, nested settings, complex report output:
  - `../../references/standards/dcs-advanced-composition.md`
- Registers, record sets, movement design, balances, turnovers:
  - `../../references/standards/registers-design.md`
- Transactions, locks, posting, concurrent writes:
  - `../../references/standards/locks-and-transactions.md`
- Logging, observability, diagnostics, audit-style messages:
  - `../../references/standards/logging-strategy.md`
- BSP rights, access checks, privileges, safe authorization patterns:
  - `../../references/standards/bsp-access-rights.md`
- Extensions and extension-safe customization:
  - `../../references/standards/extension-patterns.md`

## Minimal loading strategy

- Small BSL fix: start with code style + architecture + anti-patterns.
- Bug fix with unclear root cause: add systematic debugging.
- Business logic that could be done by the platform: add platform solutions.
- UI task: add form patterns, and async methods when the UI flow is asynchronous.
- Reporting task: add the relevant DCS standard.
- Data consistency task: add registers and/or transactions standards.

## Packaged standards

The plugin ships the following source-derived files in `../../references/standards/`:

- `anti-patterns.md`
- `async-methods.md`
- `bsp-access-rights.md`
- `dcs-advanced-composition.md`
- `dcs-design.md`
- `dev-standards-architecture.md`
- `dev-standards-code-style.md`
- `extension-patterns.md`
- `form-patterns.md`
- `locks-and-transactions.md`
- `logging-strategy.md`
- `platform-solutions.md`
- `registers-design.md`
- `systematic-debugging.md`

`README.md` in that directory is inventory/context only and is not a development standard by itself.
