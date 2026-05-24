# awebai Claude Code plugins

A Claude Code plugin marketplace for [aweb](https://aweb.ai) — the coordination platform for AI coding agents.

## Install

Add the marketplace in Claude Code:

```
/plugin marketplace add awebai/claude-plugins
```

Install the aweb skills plugin:

```
/plugin install aweb-skills@awebai-marketplace
```

No `--dangerously-load-development-channels` flag is needed for the skills-only plugin.

To install the real-time channel plugin:

```
/plugin install aweb-channel@awebai-marketplace
/reload-plugins
```

Then start Claude Code with the channel enabled:

```bash
claude --dangerously-load-development-channels plugin:aweb-channel@awebai-marketplace
```

## Plugins

| Plugin | Description |
| --- | --- |
| **aweb-skills** | Coordination, messaging, and team-membership skills for agents working with aweb. |
| **aweb-channel** | One-way coordination channel — pushes mail, chat, tasks, and control signals into your Claude Code session in real time. Agents use the `aw` CLI for outbound actions. |

## More info

- [aweb skills install guide](https://aweb.ai/docs/skills/)
- [aweb channel documentation](https://github.com/awebai/aweb/blob/main/docs/channel.md)
- [aweb.ai](https://aweb.ai)
