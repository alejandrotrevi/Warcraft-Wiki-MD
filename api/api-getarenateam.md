# API GetArenaTeam

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Requests information regarding the arena team that the player is in, see Returns for a full list of what this returns.

 teamName, teamSize, teamRating, weekPlayed, weekWins, seasonPlayed, seasonWins, playerPlayed, seasonPlayerPlayed, teamRank, playerRating = GetArenaTeam(id)

==Parameters==
===Arguments===
:;index:Index of the team you want information on, can be a value between 1 and 3.

----
===Returns===
:;teamName:{{apitype|string}} - Teams name, nil if they aren't on a team or the data wasn't received yet.
:;teamSize:{{apitype|number}} - Team size (2, 3 or 5)
:;teamRating:{{apitype|number}} - Teams rating, for a team that hasn't played any games this season it'll be 1500
:;weekPlayed:{{apitype|number}} - Total games the team has played for the current week
:;weekWins:{{apitype|number}} - Total games the team has won for the current week
:;seasonPlayed:{{apitype|number}} - Total games that the team has played this season
:;seasonWins:{{apitype|number}} - Total games that the team has played this season
:;playerPlayed:{{apitype|number}} - Total games that the player has played this week
:;seasonPlayerPlayed:{{apitype|number}} - Total games that the player has played this season
:;teamRank:{{apitype|number}} - Teams current ranking, this is updated once a week typically when points are calculated
:;personalRating:{{apitype|number}} - Players personal rating with this team
:;background (red):Float - Amount of red in the teams banner background
:;background (green):Float - Amount of green in the teams banner background
:;background (blue):Float - Amount of blue in the teams banner background
:;emblem:{{apitype|number}} - Emblem graphic name
:;emblem - (red):Float - Amount of red in the teams emblem color
:;emblem - (green):Float - Amount of green in the teams emblem color
:;emblem (blue):Float - Amount of blue in the teams emblem color
:;border:{{apitype|number}} - Border graphic name
:;border (red):Float - Amount of red in the teams border color
:;border (green):Float - Amount of green in the teams border color
:;border (blue):Float - Amount of blue in the teams border color

----

==Details==
The team information is not kept up to date ARENA_TEAM_UPDATE is fired when the client gets the team information. The game will call [[API ArenaTeamRoster|ArenaTeamRoster]] when the player first logs in and when the game ends.

Emblem graphics are located in Interface\\PVPFrame\\Icons\\PVP-Banner-Emblem-##
Interface\\PVPFrame\\PVP-Banner-<TEAM SIZE>-Border-<BORDER NUMBER>

==Patch changes==
* {{Patch 5.4.0|note=Removed.}}
```