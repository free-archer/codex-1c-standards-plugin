# Codex 1C Standards Plugin

Plugin for Codex that adds a reusable `1c-development-standards` skill with 1C:Enterprise / BSL development standards.

The plugin is packaged as a local/repository marketplace:

- marketplace name: `1c-standart-rules`
- plugin name: `1c-standards-rules`
- display name in Codex: `1C SSL Standards`

## Install in Codex

Add this repository as a Codex plugin marketplace:

```bash
codex plugin marketplace add free-archer/codex-1c-standards-plugin
```

Install the plugin from that marketplace:

```bash
codex plugin add 1c-standards-rules@1c-standart-rules
```

Restart Codex or start a new chat after installation so the skill is loaded.

## Install from a local clone

Use this variant if you want to edit the plugin locally:

```bash
git clone https://github.com/free-archer/codex-1c-standards-plugin.git
cd codex-1c-standards-plugin
codex plugin marketplace add "$(pwd)"
codex plugin add 1c-standards-rules@1c-standart-rules
```

## Verify installation

List available plugins:

```bash
codex plugin list --available --marketplace 1c-standart-rules
```

In Codex, you can also open the plugin browser:

```text
/plugins
```

Search for `1C SSL Standards`, open it, and install it if it is not already installed.

## Usage

After installation, ask Codex to use the 1C standards when working with BSL, metadata, forms, DCS, registers, BSP rights, transactions, extensions, logging, or debugging.

Example prompts:

```text
Review this BSL change using the 1C development standards.
```

```text
Implement this 1C form change and apply only the relevant standards.
```

```text
Which packaged 1C standards apply to this register design?
```

The skill loads only the relevant files from `plugins/1c-standards-rules/references/standards/` instead of loading the full standards set for every task.

## Update

For a GitHub marketplace source, refresh the marketplace snapshot and reinstall the plugin if needed:

```bash
codex plugin marketplace upgrade
codex plugin remove 1c-standards-rules
codex plugin add 1c-standards-rules@1c-standart-rules
```
