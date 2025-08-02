# API SetDungeonDifficultyID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Sets the player's dungeon difficulty.
 SetDungeonDifficultyID(difficultyIndex)

==Arguments==
:;[[difficultyIndex]]:{{apitype|number}}
::: '''1''' &rarr; 5 Player
::: '''2''' &rarr; 5 Player (Heroic)
::: '''8''' &rarr; Challenge Mode

==Details==
* When the change occurs, a message will be displayed in the default chat frame.
* The above arguments are also returned from [[API GetDungeonDifficultyID|GetDungeonDifficultyID]]().

==Patch changes==
* {{Patch 5.0.4|note=Renamed from [[API SetDungeonDifficulty|SetDungeonDifficulty]](difficultyIndex). Challenge Mode added to index.}}
* {{Patch 3.2.0|note="'''3''' &rarr; Epic" removed from index. Related function added: [[API SetRaidDifficulty|SetRaidDifficulty]](difficultyIndex).}}

==See also==
* {{api|GetDungeonDifficultyID}}
* [[difficultyIndex]]
```