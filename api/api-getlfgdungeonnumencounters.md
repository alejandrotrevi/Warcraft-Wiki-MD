# API GetLFGDungeonNumEncounters

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the number of encounters and number of completed encounters for a specified dungeon ID.
 numEncounters, numCompleted = GetLFGDungeonNumEncounters(dungeonID)

==Arguments==
:;dungeonID:{{apitype|number}} : [[LfgDungeonID]]

==Returns==
:;numEncounters:{{apitype|number}} - Number of encounters in the specified dungeon.
:;numCompleted:{{apitype|number}} - Number of completed encounters in the specified dungeon.

==Patch changes==
* {{Patch 4.3.0|note=Added.}}

==See also==
* {{api|GetLFGDungeonInfo}}
* {{api|GetRFDungeonInfo}}
* {{api|GetLFGDungeonEncounterInfo}}
```