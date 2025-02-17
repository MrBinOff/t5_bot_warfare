![GitHub Logo](/bw-assets/bw-logo.png)

# T5 Bot Warfare
Bot Warfare is a GSC mod for [PlutoniumT5](https://plutonium.pw/).

It aims to extend the existing AI in the multiplayer games of Black Ops 1.

You can find the ModDB release post [here](https://www.moddb.com/mods/bot-warfare/downloads/t5-bot-warfare-latest).

## Contents
- [Features](#Features)
- [Installation](#Installation)
- [Documentation](#Documentation)
- [Changelog](#Changelog)
- [Credits](#Credits)

## Features
This mod extends the functionality and features of Combat Training in Black Ops multiplayer.

- Menu changes (combat training menu):
  - You can select any game mode.
  - You can change prestige classes if available.
  - You can change your clan tag, emblem and calling card.
  - You can prestige.
  - Increased limits of bot numbers.
    
- Bot changes:
  - Bots play all game modes (capture flags, plant and defuse, etc.).
  - Bots take out spyplanes and counter spyplanes.
  - Bots react to the uav, jammer, decoys, motion sensor and camera spike.
  - Bots can destroy tactical insertions.
  - Bots can call in chopper gunner and gun ship but do not use it.
  - Bots can hack claymores if they are not facing it.
  - Fixed bots never reviving a player if they move.
  - Fixed bots trying to capture a hacked care package when they can't because its on their team.
  - Silencers will not cause other bots to look in the firer's direction.
  - Bots class, rank, and cod points all persist across rounds.
  - Bots will spend cod points on everything they choose now (not just gun and perk like before).
  - Bots can choose two attachments if they have the perk.
  - Bots can skip killcams.
  - Bots have a slight delay after spawning, scales inversely with difficulty.
  - Bots can reroll carepackages.
  - Bots can use the valkyrie rocket carepackage streak.
  - Bots can melee lunge.
  - Bots can jumpshot and dropshot.
  - Bots can use altmode weapons (gl, ft, mk)

## Installation
0. Download the [latest release](https://github.com/ineedbots/t5_bot_warfare/releases) of Bot Warfare.
1. Locate the root folder which your game is installed in.
2. Move the files/folders found in 'Move to root of Black Ops folder' from the Bot Warfare release archive you downloaded to the root of your Black Ops folder.
    - The folder/file structure should follow as '.Black Ops folder\mods\mp_bots\mp_bots.iwd'.
3. The mod is now installed. Start your game, go to the 'Mods' menu and select 'mp_bots'.
4. The mod is now loaded! Go play Combat Training and enjoy the new additions.

## Documentation

### DVARs
| Dvar                             | Description                                                                                 | Default Value |
|----------------------------------|---------------------------------------------------------------------------------------------|--------------:|
| bots_main                        | Enable this mod.                                                                            | 1             |
| bots_main_waitForHostTime        | How many seconds to wait for the host player to connect before adding bots to the match.    | 10            |
| bots_main_debug                  | Enable bot event prints. <ul><li>`0` - disable</li><li>`1` - for just debug events</li><li>`2` - for every event</li><ul> | 0 |
| bots_main_kickBotsAtEnd          | Kick the bots at the end of a match.                                                        | 0             |
| bots_manage_add                  | Amount of bots to add to the game, once bots are added, resets back to `0`.                 | 0             |
| bots_manage_fill                 | Amount of players/bots (look at `bots_manage_fill_mode`) to maintain in the match.          | 0             |
| bots_manage_fill_mode            | `bots_manage_fill` players/bots counting method.<ul><li>`0` - counts both players and bots.</li><li>`1` - only counts bots.</li><li>`2` - exactly `0` but auto adjusts `bots_manage_fill` to map.</li><li>`3` - exactly `1` but auto adjusts `bots_manage_fill` to map.</li><li>`4` - bots are used for balancing teams.</li><li>`5` - exactly `4` but auto adjusts `bots_manage_fill` to map.</li></ul> | 0 |
| bots_manage_fill_watchplayers    | Bots will not be added until one player is in the game                                      | 0             |
| bots_manage_fill_kick            | If the amount of players/bots in the match exceeds `bots_manage_fill`, kick bots until no longer exceeds. | 0 |
| bots_manage_fill_spec            | If when counting players for `bots_manage_fill` should include spectators.                  | 1             |
| bots_team                        | One of `autoassign`, `allies`, `axis`, `spectator`, or `custom`. What team the bots should be on. | autoassign |
| bots_team_amount                 | When `bots_team` is set to `custom`. The amount of bots to be placed on the axis team. The remainder will be placed on the allies team. | 0 |
| bots_team_force                  | If the server should force bots' teams according to the `bots_team` value. When `bots_team` is `autoassign`, unbalanced teams will be balanced. This dvar is ignored when `bots_team` is `custom`. | 0 |
| bots_team_mode                   | When `bots_team_force` is `1` and `bots_team` is `autoassign`, players/bots counting method. <ul><li>`0` - counts both players and bots.</li><li>`1` - only counts bots</li></ul> | 0 |
| bots_loadout_reasonable          | If the bots should filter bad performing create-a-class selections.                            | 0          |
| bots_loadout_allow_op            | If the bots should be able to use overpowered and annoying create-a-class selections.          | 1          |
| bots_loadout_rank                | What rank to set the bots.<ul><li>`-1` - Average of all players in the match.</li><li>`0` - All random.</li><li>`1` or higher - Sets the bots' rank to this.</li></ul> | -1 |
| bots_loadout_prestige            | What prestige to set the bots.<ul><li>`-1` - Same as host player in the match.</li><li>`-2` - All random.</li><li>`0` or higher - Sets the bots' prestige to this.</li></ul> | -1 |
| bots_loadout_codpoints           | Bots will be given this amount of codpoints to spend.<ul><li>`-1` - Average of all players in the match.</li><li>`0` - All random.</li><li>`1` or higher - Sets the bots' codpoints to this.</li></ul> | -1 |
| bots_play_move                   | If the bots can move.                                                                          | 1          |
| bots_play_knife                  | If the bots can knife.                                                                         | 1          |
| bots_play_fire                   | If the bots can fire.                                                                          | 1          |
| bots_play_nade                   | If the bots can grenade.                                                                       | 1          |
| bots_play_take_carepackages      | If the bots can take carepackages.                                                             | 1          |
| bots_play_obj                    | If the bots can play the objective.                                                            | 1          |
| bots_play_camp                   | If the bots can camp.                                                                          | 1          |
| bots_play_target_other           | If the bots can target other entities other than players.                                      | 1          |
| bots_play_killstreak             | If the bots can call in killstreaks.                                                           | 1          |
| bots_play_aim                    | If the bots can aim.                                                                           | 1          |

## Changelog
- v1.2.0 (not released yet)
  - Bots can now melee lunge
  - Bots can now jumpshot and dropshot
  - Fixed bots_manage_fill_spec players being counted with bots_manage_fill_mode 1 (bot only)
  - Added bots_manage_fill_watchplayers dvar
  - Fix some script runtime errors
  - Improved bots using altmode weapons
  - Improved bots taking spyplanes down
  - Reduced variable usage
  - Major cleanup

- v1.1.1
  - Fixed some script runtime errors
  - Improved domination
  - Bots use altmode weapons
  - Improved revenge
  - Bots can swap weapons on spawn more likely

- v1.1.0
  - Rewrote using CoD4x as a base
  - Fixed bots not knifing
  - Fixed several bugs, mainly with bot goals
  - New way of adding/managing bots, new dvars
  - Fixed bots force spawning
  - Fixed infinite loops and script errors

- v1.03
  - Fixed bots switching to secondaries all the time.
  - Bots can freely switch to their secondaries.
  - Fixed HCTDM scorelimit menu option.

- v1.02
  - Fixed a few small bugs. A possible infinite loop when bots are too poor for a grenade and reasonable setups are on, and bots never spawning after death with forcerespawn off.
  - Added an option to allow for UNLIMITED score.

- v1.01
  - Fixed bot's rank not updating after a multiround.
  - Can now set bot numbers for friends and enemies from 0 - 30 within menu. (15v15) (1v29)

- v1.0
  - Initial release.

## Credits
- INeedGames - http://www.moddb.com/mods/bot-warfare
- apdonato - http://rsebots.blogspot.ca/

Feel free to use code, host on other sites, host on servers, mod it and merge mods with it, just give credit where credit is due!
  -INeedGames/INeedBot(s) @ ineedbots@outlook.com
