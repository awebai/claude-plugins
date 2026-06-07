# Provenance

This directory is a self-contained Claude Code plugin prepared for Anthropic community-marketplace review.

It was materialized from the published npm artifact:

- Package: `@awebai/claude-channel`
- Version: `1.4.12`
- Tarball: `https://registry.npmjs.org/@awebai/claude-channel/-/claude-channel-1.4.12.tgz`
- npm shasum: `104b69282be4490440e38caabb7929e33847bba2`
- npm integrity: `sha512-LOiM9Tnjr78SttnGOTlTTsXHuf+d3QOC7WyAm/81q7pq2jRi0wdd3r2YjQuf6OPmI1IYc3yNsRSh8Q7THjM8fQ==`

The source of truth for development remains `github.com/awebai/aweb`, under `channel/` and `channel-core/`. This vendored directory includes built `dist/index.js` so a git-subdir marketplace install is self-contained.

Review-prep edits after unpacking:

- Added this provenance file.
- Clarified README trust boundaries for inbound-only channel behavior and plaintext/E2EE messaging posture.
- Clarified README setup order so missing-workspace cases initialize or join through the correct team source before running channel MCP setup.
