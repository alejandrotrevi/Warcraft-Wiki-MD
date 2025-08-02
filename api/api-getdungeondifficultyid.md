# API GetDungeonDifficultyID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the selected dungeon difficulty.
 difficultyID = GetDungeonDifficultyID()

==Returns==
:;difficultyID:{{apitype|number}} : The player's (or group leader's) current dungeon difficulty ID preference.

==See also==
* [[DifficultyID]] (a list of possible difficultyIDs)
* {{api|GetDifficultyInfo}}
* {{api|SetDungeonDifficultyID}}
* {{api|GetRaidDifficultyID}}

==Patch changes==
* {{Patch 5.0.4|note=Renamed from <code>GetDungeonDifficulty</code>.}}
* {{Patch 3.2.0|note=Raid difficulty preferences split off to {{api|GetRaidDifficulty}}.}}
```