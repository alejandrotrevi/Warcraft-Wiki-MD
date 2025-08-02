# API GetBattlefieldStatData

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|note=This is deprecated. See the [[World_of_Warcraft_API#UI_Widget_Manager|UI Widget Manager]] API.}}
Returns battlefield-specific info for a player (e.g. Warsong Gulch flag captures).
 columnData = GetBattlefieldStatData(playerIndex, slotIndex)

==Arguments==
:;playerIndex:{{apitype|number}} - Player you want to grab the data for; between 1 and {{api|GetNumBattlefieldScores}}
:;slotIndex:{{apitype|number}} - Column you want to grab the data from; between 1 and {{api|GetNumBattlefieldStats}}

==Returns==
:;columnData:{{apitype|number}} - The participant's score for the statistic

==Details==
Used to retrieve data from battleground specific scoreboard columns like flag captures in [[Warsong Gulch]]. If you want to make sure you have the most recent data you will have to call [[API RequestBattlefieldScoreData|RequestBattlefieldScoreData]] and then wait for UPDATE_BATTLEFIELD_SCORE.

==Example==
Get how many flags captures and returns a player has inside Warsong Gulch.
 for i=1, GetNumBattlefieldScores() do
 	local playerName = GetBattlefieldScore(i);
 	local flagCaptures = GetBattlefieldStatData(i, 1);
 	local flagReturns = GetBattlefieldStatData(i, 2);
 end
```