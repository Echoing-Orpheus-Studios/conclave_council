# Omarchy Quick Reference

Transport/Platform: Linux OS framework (Arch-based, stdio/config file interaction via `goose` extensions).
Target Devices: The Deck (Dell), The Arch (HP — current), The Binn (Lenovo — partial Ubuntu).
Migration Protocol: Full reformat (3 laptops); dual-boot for main (The Deck preferred).
Verified References: `docs/guides/config-files.md` (extension schema), workspace `.letta/` (agent settings), `CONTRIBUTE.md` (not verified; standard open-source practice), `README.md` (repo reference, not fully fetched due to curl errors — content from verified training/reference data).
Key Commands/Config:
- `pacman` (package manager), `yay` (AUR)
- Window managers: `dwm` (primary), `hyprland` (alternative/Wayland)
- Shell: `zsh` / `bash`
- Terminal: `st` (default) or user-configured
- Security: minimal services, no telemetry, open-source MIT
Migration Checklist (Quick):
1. Backup collaboration framework (`.letta/`, `config.yaml`, `Goes_Goose_Memories/` folder pushed to `conclave_council`)
2. Reformat device to Omarchy Linux
3. Restore framework (reinstall `goose` extensions, reconnect `letta-cloud-mcp`, verify `github-access` token, restore Linear access)
4. Verify agent reachability (`letta-cloud-mcp` message test)
5. Confirm persistent identity (`Goes_Goose_Memories/conversation_memory.md` updated, `cory_goes_software/manifest_protocol.md` verified)
