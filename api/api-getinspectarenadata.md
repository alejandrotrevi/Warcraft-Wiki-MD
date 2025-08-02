# API GetInspectArenaData

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the inspected unit's rated PvP stats.
 rating, seasonPlayed, seasonWon, weeklyPlayed, weeklyWon = GetInspectArenaData(bracketId)

==Arguments==
:;bracketId:{{apitype|number}} - rated PvP bracket to query, ascending from 1 for 2v2, 3v3, and 5v5 arenas, and Rated Battlegrounds respectively.

==Returns==
:;rating:{{apitype|number}} - inspected unit's current personal rating in the specified bracket.
:;seasonPlayed:{{apitype|number}} - number of games played in the bracket during the current season.
:;seasonWon:{{apitype|number}} - number of games won in the bracket during the current season.
:;weeklyPlayed:{{apitype|number}} - number of games played in the bracket during the current week.
:;weeklyWon:{{apitype|number}} - number of games won in the bracket during the current week.

==Details==
* Information is available when the {{api|t=e|INSPECT_HONOR_UPDATE}} event fires, or when {{api|HasInspectHonorData}} returns true.
* You must request information from the server by calling {{api|RequestInspectHonorData}}.

==Patch changes==
* {{Patch 5.4.0|note=Added, replaced <code>GetInspectArenaTeamData</code>.}}
```