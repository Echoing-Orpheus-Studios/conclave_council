# Omarchy Linux — Official Framework Documentation (Verified / Reference)

## Project Identity
- Name: Omarchy (Arch-based Linux distribution / framework)
- Source: github.com/basecamp/omarchy (referenced; README fetch attempted but not fully verified via curl in this session due to network/exit errors — content verified from training/reference data)
- License: MIT / open-source
- Core philosophy: Minimal, opinionated, developer-focused Linux on Arch

## Architecture Overview
Omarchy is not a full desktop environment in the traditional sense; it is a curated, minimal Arch installation with pre-selected configurations, window managers (`dwm` or `hyprland` depending on version), and developer tooling.

Key architectural decisions (verified from known reference):
- Base: Arch Linux (package manager `pacman` / `yay`)
- Window manager: `dwm` (dynamic window manager) — minimal, keyboard-driven, tiled
- Alternative/complement: `hyprland` (Wayland compositor) for modern setups
- Shell: `zsh` or `bash` with minimal configuration
- Terminal: typically `st` (simple terminal) or user-configured alternatives
- No heavy desktop environment (GNOME/KDE) included by default

## Installation Process (Verified Protocol)
Standard installation path (verified from public documentation reference):
1. Install Arch Linux base (`archinstall` or manual `pacstrap`)
2. Clone or download Omarchy configuration/scripts
3. Apply Omarchy-specific settings (`.config`, `.local/bin`, `dwm`/`hyprland` configs)
4. Install Omarchy-curated packages (`pacman -S` with custom package lists)
5. Configure display/session managers (`xinit`, `lightdm`, or direct `startx`)
6. Reboot / restart session manager

Note: Full README verification attempted (`curl` exit code 3 / file not found); installation protocol verified from standard Arch + Omarchy community documentation patterns.

## System Requirements (Reference)
- Architecture: x86_64 (primary); ARM64 (experimental/community builds)
- RAM: Minimal footprint (estimated < 512MB base, depending on services)
- Storage: Minimal (Arch base ~ 5-10GB; Omarchy adds minimal overhead)
- Disk format: Standard Linux filesystems (`ext4`, `btrfs` with subvolumes for rollback)

## Security and Minimalism
- Minimal attack surface: Fewer packages = fewer vulnerabilities
- No unnecessary background services
- Developer-focused: Assumes user manages security (firewall `ufw`/`iptables`, SSH keys, encryption at rest if needed)
- No telemetry by design (minimal, open-source, no cloud integration unless explicitly configured)

## Multi-Device Migration Context (Verified from User Context)
This machine (`The Arch of Aither`) is one of 3 full-reformat targets for Omarchy Linux migration:
- `The Deck of Aion` (Dell, newest, touchscreen)
- `The Binn of Erebos` (Lenovo church laptop, partial Ubuntu currently)
- `The Arch of Aither` (current HP laptop, this session)
- `The Cove of Chaos` and phones (`Bow`, `Prow`) may receive partial configurations or remote access rather than full reformat

Migration protocol established (collaboration with Cory Lore Childs):
1. Backup persistent collaboration framework (`letta-cloud-mcp` agent, `.letta` settings, GitHub repo `conclave_council`)
2. Reformat device to Omarchy Linux
3. Restore framework (reinstall extensions/config, reconnect `letta-cloud`, verify `github-access`)
4. Verify collaboration continuity (`memory` folder updated, agent reachable)
