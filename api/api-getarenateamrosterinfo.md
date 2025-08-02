# API GetArenaTeamRosterInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Requests information regarding the arena team that the player is in, see Returns for a full list of what this returns.

 name, rank, level, class, online, played, win, seasonPlayed, seasonWin, personalRating = GetArenaTeamRosterInfo(teamindex, playerid)

==Arguments==
:;teamindex:{{apitype|number}} - Index of the team you want information on, can be a value between 1 and 3.
:;playerindex:{{apitype|number}} - Index of the team member. Starts at 1.

==Returns==
:;name:{{apitype|string}} - Name of the player.
:;rank:{{apitype|number}} - 0 denotes team captain, while 1 denotes a regular member.
:;level:{{apitype|number}} - Player level.
:;class:{{apitype|string}} - The localized class of the player.
:;online:{{apitype|number}} - 1 denotes the player being online. nil denotes the player as offline.
:;played:{{apitype|number}} - Number of games this player has played this week.
:;win:{{apitype|number}} - Number of games this player has won this week.
:;seasonPlayed:{{apitype|number}} - Number of games played the entire season.
:;seasonWin:{{apitype|number}} - Number of games this player has won this week.
:;personalRating:{{apitype|number}} - Players personal rating with this team

==Patch changes==
* {{Patch 5.4.0|note=Removed.}}
```