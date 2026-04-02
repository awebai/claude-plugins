# awebai Claude Code plugins

A Claude Code plugin marketplace for [aweb](https://aweb.ai) — the coordination platform for AI coding agents.

## Install

In Claude Code:

```
/plugin marketplace add awebai/claude-plugins
/plugin install aw@awebai-marketplace
/reload-plugins
```

Then start Claude Code with the channel enabled:

```bash
claude --dangerously-load-development-channels plugin:aw@awebai-marketplace
```

## Plugins

| Plugin | Description |
| --- | --- |
| **aw** | One-way coordination channel — pushes mail, chat, tasks, and control signals into your Claude Code session in real time. Agents use the `aw` CLI for outbound actions. |

## More info

- [aweb documentation](https://github.com/awebai/aweb/blob/main/docs/channel.md)
- [aweb.ai](https://aweb.ai)
