# RenderDistance
RenderDistance is a Minecraft gamemode.

![2](https://github.com/IceChes/RenderDistance/assets/61756119/e0509650-d60d-4256-b0ad-737603943a44)

# How It Works
Players are confined to a tiny map. Every session, the game rules change to make the environment more hostile. Eventually, respawns are disabled, and the final player wins.

## The Session System
A session is a period when all players are online at the same time. A standard RenderDistance session lasts three hours. When the session ends, players must stop gathering resources or engaging in combat. They are allowed to finish trivial tasks they have already started like building a small base or farm. Exact details are up to mods.

## Map Overview
The map is 12x12 chunks, or 192x192 blocks. In the nether, there is a nether fortress and bastion remnant. The nether fortress may be modified to include certain things like nether wart if they are not present. 

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
- Session 8 will last indefinitely, as long as 2 or more players are alive. The session will end when the victor is crowned. Alternatively, the worldborder can be shrunk over the course of Session 8 to encourage PVP.

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
The RenderDistance datapack contains commands to preload the gameplay attributes for all 8 sessions, including hardcore mode. It will also automatically set up a worldborder, and you can also use pregame mode for starting the game.

Place this pack into your server's datapacks folder. To start pregame mode, use `/function renderdistance:pregame`. To set up without pregame mode, run `/function renderdistance:reset`. One of these two commands must be run before starting the game. If you don't know what pregame mode is, see the function reference.

When you want to start, wait for all players to join, then run `/function renderdistance:session_1`. There are commands for 8 sessions. 

To change sessions, wait until all players join, and run the `/function renderdistance:session_<session>` command to start the next session, replacing <session> with the session number from 1 to 8.

On Session 8, you have a choice. You can either run Session 8 as a normal session, OR you can run `/function renderdistance:session_8_shrink`. This will shrink the border over the course of 2 hours. 

# Funtion Reference

`tick`
Runs every tick. Checks to see if a player death count on the `deaths` scoreboard is above 0, and if so, sets their gamemode to spectator. The `deaths` scoreboard does not exist until `session_6` is run. 

`pregame`

Gives all players maximum resistance and saturation for an infinite amount of time, and runs `reset`.

`reset`

Sets all game rules affected by RenderDistance back to starting (Session 1) values. Sets the difficulty to peaceful, disables firetick, enables keepinventory, sets the spawn radius to 1, enables natural regeneration, removes the `deaths` scoreboard, sets everyone to survival, and runs `setup`.

`setup`

Sets up the worldborder to 192 blocks.

`session_1`

Clears player effects and sets the difficulty to easy. The effect clearing is because of pregame mode. Additionally, all Session commands display a title to the players.

`session_2`

Sets the difficulty to normal.

`session_3`

Enables firetick, sets the spawn radius to 20.

`session_4`

Sets the difficulty to hard.

`session_5`

Disables keep inventory. Sets spawn radius to 50.

`session_6`

Enables the `deaths` scoreboard, therefore allowing `tick` to work.

`session_7`

Disables natural regeneration.

`session_8`

Doesn't do anything, only displays titles like all the other Session functions.

`session_8_shrink`

Displays session 8's titles, and shrinks the world border to 20 over 7200 seconds.
