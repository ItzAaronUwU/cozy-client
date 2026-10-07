Cozy Client is a custom Minecraft: Java Edition launcher and client I'm developing (Electron launcher + Java agent client). I'm requesting Minecraft API access so players can sign in with their own Microsoft accounts and launch the game they own.

Sign-in uses the OAuth device code flow with only the XboxLive.signin and offline_access scopes. The tokens are used solely for the standard Xbox Live → XSTS → login_with_xbox flow to get the player's Minecraft profile and access token, which are passed to the game at launch. Tokens are stored only on the user's PC, encrypted with the OS credential store (Electron safeStorage), and are never sent to any server other than Microsoft/Xbox/Minecraft services.

The launcher downloads official game files directly from Mojang's servers (piston-meta / piston-data / resources.download.minecraft.net) and does not redistribute any Minecraft code or assets. Accounts that don't own the game cannot launch it.
