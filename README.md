# Cozy Client 🦎

A custom launcher and client for **Minecraft: Java Edition**, with a cozy underwater theme.

> Not affiliated with Mojang Studios or Microsoft. Minecraft is a trademark of Mojang Studios.
> You need to own Minecraft: Java Edition to play.

## What it is

Cozy Client has two parts:

- **Cozy Launcher**: a desktop app that installs Minecraft, signs you in, and starts the game.
- **Cozy Client**: a lightweight client that adds an animated main menu, HUD elements
  (FPS, coordinates, keystrokes, CPS, ping, clock), zoom, and Discord Rich Presence.

The game itself is never modified on disk or redistributed. Official game files are
downloaded directly from Mojang's servers.

## Signing in

Cozy Launcher uses the official **Microsoft sign-in** (OAuth device code flow):

1. Click **Microsoft account** in the launcher.
2. Your browser opens `microsoft.com/link`, where you enter the code the launcher shows.
3. Sign in on Microsoft's own website. Cozy Launcher never sees your password.

**Permissions requested:** `XboxLive.signin` and `offline_access` only.

These are used for the standard Minecraft authentication flow
(Microsoft → Xbox Live → XSTS → Minecraft services), which gets your Minecraft
username and a game access token so the game can launch. Accounts that don't own
Minecraft: Java Edition cannot play.

## Privacy

- Your sign-in token is stored **only on your computer**, encrypted with your
  operating system's credential protection.
- Tokens are only ever sent to Microsoft, Xbox Live, and Minecraft services. There are
  no Cozy servers, no analytics, and no tracking.
- Signing out in the launcher deletes the stored token.

## Where game files come from

All game files are downloaded from Mojang's official servers:

- `piston-meta.mojang.com` (version info)
- `piston-data.mojang.com` (game and libraries)
- `resources.download.minecraft.net` (assets)
- Mojang's official Java runtime downloads

Files are checked against Mojang's published SHA-1 hashes.

## Supported version

Minecraft **26.2**

## Contact

Questions or issues: open an issue on this repository or contact me
[On my website](https://itzabot.dev/).
