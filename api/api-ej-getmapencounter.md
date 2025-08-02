# API EJ GetMapEncounter

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns boss pin locations on instance maps.
 x, y, instanceID, name, description, encounterID, rootSectionID, link = EJ_GetMapEncounter(uiMapID, index [, fromJournal])

==Arguments==
:;uiMapID:{{apitype|number}} : [[UiMapID]]
:;index:{{apitype|number}} - index of the boss pins.
:;fromJournal:{{apitype|boolean?}} - this function seems to only return results when passing true.

==Returns==
:;x:{{apitype|number}} - x coordinate
:;y:{{apitype|number}} - y coordinate
:;instanceID:{{apitype|number}} : {{dbc|journalinstance|JournalInstance.ID}}
:;name:{{apitype|string}}
:;description:{{apitype|string}}
:;encounterID:{{apitype|number}} : [[JournalEncounterID]]
:;rootSectionID:{{apitype|number}} : {{dbc|journalencountersection|JournalEncounterSection.ID}}
:;link:{{apitype|string}} : [[Hyperlinks#journal|journalLink]]

==Patch changes==
* {{Patch 4.2.0|note=Added.}}
```