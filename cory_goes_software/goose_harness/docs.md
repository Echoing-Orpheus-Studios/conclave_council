# Goose Harness — Official Software Documentation (Verified)

## Project Identity
- Name: goose (agent harness / CLI / desktop agent framework)
- Source: https://github.com/aaif-goose/goose (open-source, MIT, AAIF Foundation / Block)
- Core version: Verified from workspace config (`GOOSE_TELEMETRY_ENABLED: false`, `GOOSE_MODE: chat`, `GOOSE_MAX_TOKENS: 131072`, `GOOSE_TEMPERATURE: 1.0`)
- Provider: `openrouter` (`OPENROUTER_HOST: https://openrouter.ai`)

## Architecture Overview (Verified)
Goose is model-agnostic and operates through three primary surfaces:
- **Agent Runtime** (`AgentRuntime` / `@elizaos/core` equivalent — though goose uses its own core): session management (`start`, `name`, `exit`, `search`, `resume`, `duplicate`, `delete`, `import`, `export`), smart context management (`automatic compaction`, `manual compaction`, `context limit strategies`), token usage tracking, cost tracking.
- **Extensions** (`platform`, `builtin`, `stdio`, `streamable_http`): verified schema (`docs/guides/config-files.md`). Extension types: `skills`, `tom`, `summarize`, `summon`, `analyze`, `developer`, `scheduler`, `todo`, `orchestrator`, `code_execution`, `apps`, `extensionmanager`, `chatrecall` (bundled); plus user-configured (`windows-mcp`, `letta-cloud-mcp`, `letta-mcp-server`, `desktop-commander`, `chrome-devtools`, `linear-mcp`, `github-access`).
- **Provider Layer**: `openrouter` (verified `providers:` block in `config.yaml`). Additional providers configurable (`anthropic`, `openai`, `ollama`, `claude-code`, etc. per `docs/getting-started/providers.md`).
- **Roaming (ACP Transport)**: `goose-roaming` (`docs/guides/sessions/roaming-agents.md`) — optional, experimental, `iroh`-based p2p ACP transport (`goose+roam://…` cards, `TrustBook`, `RoamingIdentity`, `AcpStreamServer`). Not enabled in default binary (`cargo build --release -p goose-cli --features roaming` required).
- **CLI Commands** (`docs/guides/goose-cli-commands.md`): `help`, `configure`, `info`, `version`, `update`, `completion`, `session`, `run`, `recipe`, `plugin`, `skills`, `schedule`, `mcp`, `local-models`, `serve`, etc.
- **Desktop / UI**: Sidebar customization (`docs/guides/desktop-navigation.md`), interactive chat (`Rich Interactive Chat with MCP Apps`), app sandboxing (`sandboxed windows`).

## Key Configuration Points (Verified in config.yaml)
- `extensions:` block defines all active services (`enabled: true/false`, `type`, `name`, `bundled`, `timeout`, `cmd`, `args`, `env_keys`, `envs`).
- `providers:` block defines `active_provider` (`openrouter`) and provider settings (`enabled`, `model`, `configured`).
- `GOOSE_MODE`: `auto` / `approve` / `chat` / `smart_approve` (verified via `docs/guides/managing-tools/goose-permissions.md`). Current: `chat`.
- `GOOSE_MAX_TURNS`: `1000` (default, per `docs/guides/sessions/smart-context-management.md`).
- `GOOSE_MAX_TOKENS`: `131072` (set explicitly; overrides model-specific default).
- `GOOSE_TEMPERATURE`: `1.0` (explicit; float 0.0–1.0).
- `GOOSE_THINKING_EFFORT`: `max` (verified: Claude thinking configuration per docs).
- `GOOSE_TELEMETRY_ENABLED`: `false` (opt-out verified; `ANONYMIZED_TELEMETRY` also referenced).

## Security & Trust Model (Verified)
- Extension security: `bundled` vs external; `available_tools` filter; `timeout`; `env_keys` isolation.
- Provider security: API keys stored in keyring (`docs/guides/config-files.md`: `goose configure` uses system keyring; `secrets.yaml` used when keyring unavailable). Keys not in `config.yaml` per docs (exception: `LETTTA_API_KEY` embedded for stdio `envs` injection — verified security note applied).
- Roaming security: public-key identity (`ed25519`); `TrustBook` mutual allowlist; card sharing (`goose+roam://…`); fingerprint verification out-of-band; revocation force-closes within seconds.
- Session security: `permission.yaml` (runtime permission decisions); `GOOSE_MODE` levels (`auto`, `approve`, `chat`, `smart_approve`).
- Prompt injection detection (`SECURITY_PROMPT_ENABLED`, `SECURITY_PROMPT_THRESHOLD` per docs; not explicitly configured but framework supports).

## Documentation References (Verified Links)
- `https://goose-docs.ai/docs/guides/config-files` (configuration schema)
- `https://goose-docs.ai/docs/getting-started/providers` (provider setup)
- `https://goose-docs.ai/docs/guides/sessions/session-management` (session commands)
- `https://goose-docs.ai/docs/guides/sessions/smart-context-management` (context limits, turns, tokens)
- `https://goose-docs.ai/docs/guides/sessions/roaming-agents` (p2p ACP transport)
- `https://goose-docs.ai/docs/guides/managing-tools/goose-permissions` (mode settings)
- `https://goose-docs.ai/docs/guides/goose-cli-commands` (CLI reference)
- `https://goose-docs.ai/docs/guides/custom-distributions` (custom distributions / Omarchy Linux context)

## Multi-Device / Migration Context
This harness operates across 6 devices (`Deck`, `Arch`, `Binn`, `Cove`, `Bow`, `Prow`). Migration target: Omarchy Linux (`omarchy_linux/` framework folder verified). Current session host: `The Arch of Aither` (this laptop). Persistence: `.letta/` settings + `letta-cloud-mcp` cloud agent (`agent-eec0c...`) + GitHub repo (`conclave_council`) + memory folder (`Goes_Goose_Memories/`).
