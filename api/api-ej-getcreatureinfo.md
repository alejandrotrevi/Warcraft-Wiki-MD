# API EJ GetCreatureInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns encounter boss info.
 id, name, description, displayInfo, iconImage, uiModelSceneID = EJ_GetCreatureInfo(index [, encounterID])

==Arguments==
:;index:{{apitype|number}} - Creature index, up to [https://www.townlong-yak.com/framexml/8.1.5/Blizzard_EncounterJournal/Blizzard_EncounterJournal.lua#4 nine] for encounters with multiple bosses.
:;encounterID:{{apitype|number?}} : [[JournalEncounterID]] - if omitted this will default to the currently viewed encounter.

==Returns==
:;id:{{apitype|number}}  : {{dbc|journalencountercreature|JournalEncounterCreature.ID}}
:;name:{{apitype|string}}
:;description:{{apitype|string}}
:;displayInfo:{{apitype|number}} : [[CreatureDisplayID|displayID]]
:;iconImage:{{apitype|number}} : [[FileID]]
:;uiModelSceneID:{{apitype|number}} : [[ModelSceneID]]

==Example==
<syntaxhighlight lang="lua">
/dump EJ_GetCreatureInfo(1, 89)
> 358, "Glubtok", "", 37410, 522228, 9
</syntaxhighlight>

==Gallery==
<gallery>
API EJ GetCreatureInfo 01.png|description
API EJ GetCreatureInfo 02.png|iconImage
API EJ GetCreatureInfo 03a.png|Multiple creatures
</gallery>

==Patch changes==
* {{Patch 4.2.0|note=Added.}}
```