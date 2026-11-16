# Installation

## Requirements

- Minecraft Java Edition 26.3
- NeoForge 26.3.0.84 or later
- Java 25
- Realistic Trading Overhaul on both the client and the server

Single player already runs an integrated server, so installing the mod in the local profile covers
both sides. A client without RTO cannot join a server that has it.

## CurseForge App

1. Create or select a Minecraft 26.3 NeoForge profile.
2. If the current file is an alpha or beta, allow that release type for the profile. CurseForge hides
   pre-release files from profiles set to Release only.
3. Install Realistic Trading Overhaul from its CurseForge project.
4. Launch once and confirm the Mods screen lists the expected RTO version.

## Dedicated server

1. Install a NeoForge 26.3 server, build 26.3.0.84 or later.
2. Place the official RTO JAR in the server's `mods` directory.
3. Install the same JAR in every connecting client's `mods` directory.
4. Start the server once. RTO creates `config/realistictradingoverhaul-local.toml`
   (see [Configuration](Configuration)).
5. Join with a matching client and trade with one villager before opening the server publicly.

Do not download RTO from rehosting sites.
