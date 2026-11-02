# zettai.github.io

See **[AGENTS.md](./AGENTS.md)** for what this repo is, how to set it up, the
commands, and the conventions. That file is the source of truth and is read by
every agent tool used here.

Keep this file thin. Only Claude Code specifics belong below: MCP servers in
`.mcp.json` (`mcpServers` key), hooks, skills, slash commands. Anything that
would be true for another agent belongs in AGENTS.md instead.

## Claude Code specifics

<!-- Managed by 'ror apply'. Edit freely below this line; ror only checks that
     the AGENTS.md link above is still here. -->
