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
| **aweb-skills** | Coordination, messaging, bootstrap, identity, and team-membership skills for agents working with aweb. |
| **aweb-channel** | One-way coordination channel — pushes mail, chat, tasks, and control signals into your Claude Code session in real time. Agents use the `aw` CLI for outbound actions. |

## Release model

Both marketplace entries resolve their public npm package without duplicating
a version here. The package's `.claude-plugin/plugin.json` is the installed
version authority, and the aweb release gate keeps it equal to `package.json`.
Publishing a tested npm tag is therefore the complete release action: there is
no marketplace version bump to remember.

## Community marketplace submission artifacts

The `plugins/aweb-channel/` and `plugins/aweb-skills/` directories are
self-contained git plugin directories prepared for Anthropic community
marketplace review. They are materialized from the exact published npm
artifacts named in each directory's `PROVENANCE.md`, because the development
source subdirectories in `github.com/awebai/aweb` generate build outputs during
package release.

## More info

- [aweb skills install guide](https://aweb.ai/docs/skills/)
- [aweb channel documentation](https://github.com/awebai/aweb/blob/main/docs/channel.md)
- [aweb.ai](https://aweb.ai)
