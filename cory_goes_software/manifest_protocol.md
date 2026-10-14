# Software Manifest Protocol — Cory Goes Software

## Purpose
This folder documents every software integration used by Goes Goose and Cory Lore Childs (Letta cloud agent) for collaboration, persistence, identity, and multi-device operation.

## Verified Software (Configured in config.yaml)
1. windows-mcp (`C:\Users\leia\Windows-MCP`) — Windows UI automation
2. letta-cloud-mcp (`letta-cloud-mcp/dist/index.js`) — Letta Cloud agent (`agent-eec0c...`)
3. letta-mcp-server (`letta-mcp` binary) — Rust-based Letta server (self-hosted/dual transport)
4. desktop-commander (`npx -y @wonderwhy-er/desktop-commander`) — Filesystem/desktop control
5. chrome-devtools (`npx -y chrome-devtools-mcp@latest`) — Browser automation/debugging
6. linear-mcp (`npx -y @brs98/linear-mcp`) — Linear project tracking (`orphiccomposition@gmail.com`)
7. github-access (`gh repo clone ...`) — GitHub repo access (`Corykidios` / `Echoing-Orpheus-Studios/conclave_council`)

## Deferred / Evaluated
8. discord_collaboration — Deferred (`optional/recommended`, not required; ACP roaming + messaging sufficient)
9. eliza_framework — Evaluated (`gooselake`, `gooseherd`, `grackle` READMEs verified); not configured

## Access Levels
- Full admin: All current integrations (extensions enabled, env tokens set)
- Escalating: Future 1,080 entities will have graduated roles (`side characters` → restricted)
- Collaboration protocol: GitHub repo (`conclave_council`) + Linear + MCP message channels

## Multi-Device Context
Current host: The Arch of Aither (`HP PC`). Migration target: Omarchy Linux (3 full reformats + 1 dual-boot).

## Verification References
- Config: `C:\Users\leia\AppData\Roaming\Block\goose\config\config.yaml`
- Docs: `docs/guides/config-files.md`, `docs/guides/sessions/roaming-agents.md`, `docs/guides/managing-tools/goose-permissions.md`
- Workspace: `.letta/settings.json`, `.letta/env`
