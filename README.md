# RenderDistance
RenderDistance is a Minecraft gamemode.

![2](https://github.com/IceChes/RenderDistance/assets/61756119/e0509650-d60d-4256-b0ad-737603943a44)

# How It Works
Players are confined to a tiny map. Every session, the game rules change to make the environment more hostile. Eventually, respawns are disabled, and the final player wins.

## Map Overview
The map is 12x12 chunks, or 192x192 blocks. All entities outside of the border will be deleted, including you. At the center of the map there is a spawn platform. The platform contains a level 1 beacon.

## Starting Conditions
These are the conditions and gamerules during Session 1.

- Easy difficulty
- PVP disabled
- Fire tick disabled
- Keep inventory enabled
- Spawn radius of 1

## Session-by-Session Overview
Here’s what will CHANGE from the STARTING CONDITIONS every session.

### SESSION 1:
- No change

### SESSION 2:
- Normal difficulty

### SESSION 3:
- PVP enabled
- Fire tick enabled
- Spawn radius of 20

### SESSION 4:
- Hard difficulty

### SESSION 5:
- Keep inventory disabled
- Spawn radius of 50

### SESSION 6:
- Players can no longer respawn

### SESSION 7:
- Natural regen disabled

### SESSION 8:
- Session 8 will last indefinitely, as long as 2 or more players are alive. The session will end when the victor is crowned.


## Rules
This mode does have some rules. Here they are:
- Vanilla or close-to-vanilla clients, mods, and resource packs only. If Renderdistance is being played on Java Edition, Fabric with Simple Voice Chat is required.
- No abusing exploits.
- Do not trap players in ways they reasonably can’t escape from. Examples include bed traps, portal traps, etc.
- Don’t take the game too seriously, this is a fun challenge and it’s not designed to be high-stakes. 

Here’s examples of what is allowed, for clarification:
- Tweaker packs like Vanilla Tweaks, fulbright mods, etc.
- Optimization mods like Sodium and aesthetic mods like Iris.
- Destroying bases.
- Stealing from players.
- Killing players.

# How To Use This Pack
Place this pack into your server's datapacks folder. To start pregame mode, use `/function renderdistance:pregame`. Pregame mode must be entered before the game is started.

When you want to start, run `/function renderdistance:session_1`. There is a session command for all 8 sessions that change each attribute about the game indefinitely.

The game world must be set up manually. Support for automatically setting up a game world with a world border and spawn platform may come in the future.
