# API SetRaidDifficultyID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Sets the raid difficulty.
 SetRaidDifficultyID(difficultyIndex)

==Arguments==

:;[[difficultyIndex]]:{{apitype|number}}
:::   '''3''' &rarr; 10 Player
:::   '''4''' &rarr; 25 Player
:::   '''5''' &rarr; 10 Player (Heroic)
:::   '''6''' &rarr; 25 Player (Heroic)
:::'''14''' &rarr; Normal
:::'''15''' &rarr; Heroic
:::'''16''' &rarr; Mythic

==Details==
* When the change occurs, a message will be displayed in the default chat frame.
*Example:  /script SetRaidDifficultyID(16);  sets the raid difficulty to Mythic

==Patch changes==
* {{Patch 5.2.0|note=Renamed from <code>SetRaidDifficulty</code>}}
* {{Patch 3.2.0|note=Added; split from <code>SetDungeonDifficulty</code>.}}

==See also==
* {{api|GetRaidDifficultyID}}
* [[difficultyIndex]]
```