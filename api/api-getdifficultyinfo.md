# API GetDifficultyInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about a difficulty.
 name, groupType, isHeroic, isChallengeMode, displayHeroic, displayMythic, toggleDifficultyID, isLFR, minPlayers, maxPlayers = GetDifficultyInfo(id)

==Arguments==
:;id:{{apitype|number}} - difficulty ID to query, ascending from 1.

==Returns==
:;name:{{apitype|string}} - Difficulty name, e.g. "10 Player (Heroic)"
:;groupType:{{apitype|string}} - Group type appropriate for this difficulty; "party" or "raid".
:;isHeroic:{{apitype|boolean}} - true if this is a heroic difficulty, false otherwise.
:;isChallengeMode:{{apitype|boolean}} - true if this is challenge mode difficulty, false otherwise.
:;displayHeroic:{{apitype|boolean}} - display the Heroic skull icon on the instance banner of the minimap
:;displayMythic:{{apitype|boolean}} - display the Mythic skull icon on the instance banner of the minimap
:;toggleDifficultyID:{{apitype|number}} - difficulty ID of the corresponding heroic/non-heroic difficulty for 10/25-man raids, if one exists.
:;isLFR:{{apitype|boolean}} - true if this is looking for raid difficulty, false otherwise.
:;minPlayers:{{apitype|number}} - minimum players needed.
:;maxPlayers:{{apitype|number}} - maximum players allowed.

==See also==
* [[DifficultyID]] (a list of possible difficultyIDs)
* {{api|SetDungeonDifficultyID}}
* {{api|GetInstanceInfo}}
* {{api|GetRaidDifficultyID}}

==Patch changes==
* {{Patch 6.0.2|note=Now returns displayHeroic and displayMythic.}}
* {{Patch 5.2.0|note=Added.}}
```