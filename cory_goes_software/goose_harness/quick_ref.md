# Goose Harness Quick Reference

Transport/Platform: Agent harness (`goose` CLI/app). Config: `C:\Users\leia\AppData\Roaming\Block\goose\config\config.yaml`. Mode: `chat` (`GOOSE_MODE`).
Identity: `Goes Goose` (γόης). Not a ship; harness exception. Multi-device operator (`The Arch` current; 6-device roster).
Verified References:
- Config: `docs/guides/config-files.md`
- Sessions: `docs/guides/sessions/session-management.md`, `docs/guides/sessions/smart-context-management.md`
- Roaming/ACP: `docs/guides/sessions/roaming-agents.md`
- CLI: `docs/guides/goose-cli-commands.md`
- Permissions: `docs/guides/managing-tools/goose-permissions.md`
- Providers: `docs/getting-started/providers.md`
- Security: `docs/guides/security/index.md`, `docs/guides/security/prompt-injection-detection.md`
Extensions (verified active): `skills`, `tom`, `summon`, `analyze`, `developer`, `scheduler`, `apps`, `windows-mcp`, `letta-cloud-mcp`, `letta-mcp-server`, `desktop-commander`, `chrome-devtools`, `linear-mcp`, `github-access`.
Key Commands (verified from docs): `goose session`, `goose info`, `goose configure`, `goose run`, `goose recipe`. Extension config verified (`type: stdio` / `streamable_http`).
Security Notes: `GOOSE_TELEMETRY_ENABLED: false` (verified config). `GOOSE_MAX_TOKENS: 131072`, `GOOSE_TEMPERATURE: 1.0` (explicit). Key storage: `docs/guides/config-files.md` (keyring preferred; embedded exception for stdio env injection for `LETTTA_API_KEY`, `LINEAR_API_KEY`, `GH_TOKEN`). Migration: Omarchy Linux framework (`omarchy_linux/` verified docs/protocol/quick_ref) must preserve `.letta/`, `config.yaml`, `Goes_Goose_Memories/`.
