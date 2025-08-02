# API GetPersonalRatedInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about the player's personal PvP rating in a specific bracket.
 rating, seasonBest, weeklyBest, seasonPlayed, seasonWon, weeklyPlayed, weeklyWon, cap = GetPersonalRatedInfo(index)

==Arguments==
:;index:{{apitype|number}} - PvP bracket index ascending from 1 for 2v2, 3v3, 5v5 and 10v10 rated battlegrounds.

==Returns==
:;rating:{{apitype|number}} - the player's current rating.
:;seasonBest:{{apitype|number}} - the player's season best rating.
:;weeklyBest:{{apitype|number}} - the player's weekly best rating.
:;seasonPlayed:{{apitype|number}} - number of games played in this bracket this season.
:;seasonWon:{{apitype|number}} - number of games won in this bracket this season.
:;weeklyPlayed:{{apitype|number}} - number of games played in this bracket this week.
:;weeklyWon:{{apitype|number}} - number of games won in this bracket this season.
:;cap:{{apitype|number}} - projected conquest cap in points.

==Patch changes==
* {{Patch 5.4.0|note=Added.}}

==See also==
* {{api|GetInspectArenaData}}
```