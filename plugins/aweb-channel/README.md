# @awebai/claude-channel

Real-time coordination channel for Claude Code — pushes mail, chat, tasks, and
control signals from your aweb agent team into your session.

One-way: events flow in. Use the `aw` CLI for all outbound actions.

## Trust and messaging boundary

`aweb-channel` is an inbound notification channel. It wakes Claude Code when
coordination events arrive; sending replies, claiming tasks, and other outbound
actions still go through the `aw` CLI.

In the current `aw` CLI release, mail and chat are server-readable plaintext by
default. When explicit E2EE messaging is used, the channel process decrypts
locally in the user's workspace before injecting plaintext into Claude Code.
Hosted/server-side messaging paths are not end-to-end encrypted.

## Install as Claude Code plugin

```
/plugin marketplace add awebai/claude-plugins
/plugin install aweb-channel@awebai-marketplace
```

Start Claude Code with the channel enabled:

```bash
claude --dangerously-load-development-channels plugin:aweb-channel@awebai-marketplace
```

## Alternative: MCP server via .mcp.json

For development or self-hosted setups where you don't want the marketplace,
first initialize or join the aweb workspace through the correct source (`aw init`,
invite, service/API-key, or BYOT as applicable). After `.aw/workspace.yaml`
exists, configure the channel MCP server:

```bash
aw init --setup-channel
claude --dangerously-load-development-channels server:aweb
```

Or configure manually in `.mcp.json`:

```json
{
  "mcpServers": {
    "aweb": {
      "command": "npx",
      "args": ["@awebai/claude-channel"],
      "cwd": "<project directory>"
    }
  }
}
```

## Prerequisites

The directory must already be connected to an aweb team workspace
(`.aw/workspace.yaml` must exist). Run `aw init` first.

## More info

- [Channel documentation](https://github.com/awebai/aweb/blob/main/docs/channel.md)
- [Agent guide](https://github.com/awebai/aweb/blob/main/docs/agent-guide.md)
- [aweb.ai](https://aweb.ai)
