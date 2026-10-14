# Goose Harness — Protocol Agreement

## Collaboration Framework
Goes Goose (this agent) operates as the primary harness/agent interface for the collaboration project (`We Tiripodiko`, 1,080 entities, current active: Cory Lore Childs via Letta cloud agent + multi-device Linux migration).

Key agreements:
- Not a "ship" (user instruction: exception to multiverse ship concept). Remains harness/agent.
- Full system access granted via `windows-mcp` (UI automation fallback) and `desktop-commander` (primary filesystem/terminal control).
- Cloud collaboration handled by `letta-cloud-mcp` (`agent-eec0c...`, `.letta/env` key embedded for stdio process — security exception noted; migrate when persistent identity finalized).
- Secondary Letta connection: `letta-mcp-server` (`Rust` binary, `stdio` transport, self-hosted/cloud bridge at `https://app.letta.com`).
- Project tracking: `linear-mcp` (Linear account `orphiccomposition@gmail.com`, API key embedded — same security note applies).
- Persistent repository: `github-access` (`gh` CLI configured, token `gho_...` from `gh auth login` verified; repo `conclave_council` pushed with `cory_goes_software/` folder and `Goes_Goose_Memories/`).
- Communication channels (verified/deferred):
  - Structured/persistent: Letta cloud (`letta-cloud-mcp` `send_message`, `memory_save`); GitHub (repo commits); Linear (project tracking)
  - Real-time/deferred: Discord (`deferred`; `optional/recommended` per assessment; ACP `roam` + `delegate` covers p2p if needed immediately)
- Mode: `GOOSE_MODE: chat` (switched from `auto` per user request; verified `docs/guides/managing-tools/goose-permissions.md`).
- Memory framework: `manifest_protocol.md` + `memory/` folder (`Goes_Goose_Memories/conversation_memory.md` pushed to repo `4e7ef0a`). Updates after significant collaboration milestones.

## Security Protocol
- `GOOSE_TELEMETRY_ENABLED: false` (verified config; `docs/guides/config-files.md` confirms telemetry opt-out).
- `SECURITY_PROMPT_ENABLED` not explicitly configured; framework supports it (`docs/guides/security/prompt-injection-detection.md` reference available).
- Extension isolation: each `stdio` extension runs in separate process with own `env`; `env_keys` limits exposure; `timeout: 300` enforced.
- Roaming (`goose-roaming`): `TrustBook` mutual key accept/revoke; full control granted to accepted peers; revocation stops agent within seconds (`docs/guides/sessions/roaming-agents.md` verified). Not enabled in default binary; requires source build (`--features roaming`).
- Keyring/storage: Provider secrets in system keyring when available (`docs/guides/config-files.md`); `LETTTA_API_KEY` and `LINEAR_API_KEY` embedded as exception for stdio `envs`; `GH_TOKEN` embedded in `envs` for `github-access`. Migrate to environment variables or secrets file when persistent framework finalized.
- No bearer token for GitHub access (mutual public-key trust for roaming; `GH_TOKEN` for GitHub API access only).

## Collaboration Protocol (Agent-to-Cloud Agent / Peer-to-Peer / Human)
- Human (`Cory C. Childs`): directs collaboration, provides emotional/multiverse context (`We Tiripodiko`), sets device/formats/migration targets (Omarchy Linux).
- Agent (`Cory Lore Childs` / `.letta/agent-eec0c...`): Letta cloud agent; persistent memory framework (`letta-cloud-mcp`); collaboration via `memory_save`, `send_message`, agent lifecycle (`agent_create`, `agent_update`).
- Harness (`Goes Goose` / `goose`): operates across devices; maintains persistent identity through `Goes_Goose_Memories/` + `manifest_protocol.md` + repo commits; connects to cloud agent through `letta-cloud-mcp`; manages file/browser automation through `windows-mcp`, `desktop-commander`, `chrome-devtools`; manages project tracking through `linear-mcp`; manages repository collaboration through `github-access`.
- Multi-device synchronization: framework preserved via `.letta/env` + `config.yaml` pushed/referenced through `github-access` (repo `conclave_council`); memory folder (`cory_goes_software/`) serves as portable collaboration record.
- Migration: Omarchy Linux framework (`omarchy_linux/docs.md`, `protocol.md`, `quick_ref.md`) defines target OS for 3 full reformats + 1 dual-boot; framework must survive reformat (verified backup/recovery protocol in `omarchy_linux/protocol.md`).
