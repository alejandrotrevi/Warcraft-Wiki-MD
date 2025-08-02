# API GetRaidDifficultyID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the player's currently selected raid difficulty.
 difficultyID = GetRaidDifficultyID()

==Returns==
:;difficultyID:{{apitype|number}} : The player's (or group leader's) current raid difficulty ID preference. See {{api|GetDifficultyInfo}} for a list of possible difficultyIDs.

==Details==
* You may use {{api|GetDifficultyInfo}} to retrieve information about the returned ID value.

==See also==
* {{api|SetRaidDifficultyID}}
* {{api|GetDungeonDifficultyID}}

==Patch changes==
* {{Patch 5.2.0|note=Renamed from <code>GetRaidDifficulty</code>, return values changed.}}
* {{Patch 3.2.0|note=Added; split from {{api|GetDungeonDifficulty}}.}}
```