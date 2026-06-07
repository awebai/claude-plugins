# `aweb-skills`

Content-only Claude Code plugin packaging the five canonical aweb skills:
`aweb-bootstrap`, `aweb-coordination`, `aweb-identity`, `aweb-messaging`, and
`aweb-team-membership`.

Distinct from [`aweb-channel`](../aweb-channel/), which ships the real-time
channel runtime and requires `--dangerously-load-development-channels`. This
plugin has **no runtime**, no `bin`, and no MCP server config — just the skill
bodies. Users who only want aweb's skill catalog install this one and skip the
channel.

## Source of truth

Skill bodies are developed in [`github.com/awebai/aweb`](https://github.com/awebai/aweb)
under root `skills/`. This directory is a self-contained marketplace artifact
materialized from the published `@awebai/claude-skills` npm package; see
[`PROVENANCE.md`](./PROVENANCE.md).

## Install from the awebai marketplace

```text
/plugin marketplace add awebai/claude-plugins
/plugin install aweb-skills@awebai-marketplace
```

No `--dangerously-load-development-channels` flag is required — that flag is
only for the channel plugin.

After install, Claude Code namespaces the skills as `/aweb-skills:<name>` and
discovers them automatically.

## Included skills

- `aweb-bootstrap` — create, provision, add, or remove repo-local aweb agents with the `aw agents` lifecycle.
- `aweb-coordination` — coordinate tasks, locks, worktrees, and shared team state.
- `aweb-identity` — reason about local/global identities, keys, DIDs, and routing.
- `aweb-messaging` — use aweb mail/chat and handle channel events safely.
- `aweb-team-membership` — join teams, accept invites, fetch certificates, and diagnose active-team state.
