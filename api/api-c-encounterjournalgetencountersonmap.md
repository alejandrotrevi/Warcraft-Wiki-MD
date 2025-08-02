# API C EncounterJournal.GetEncountersOnMap

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns boss pin locations for an instance map.
 encounters = C_EncounterJournal.GetEncountersOnMap(uiMapID)

==Arguments==
:;[[UiMapID|uiMapID]]:{{apitype|number}}

==Returns==
:;encounters:structure - EncounterJournalMapEncounterInfo[]

{| class="sortable darktable zebra"
|-
! Field !! Type !! Description
|-
| encounterID || {{apitype|number}} || [[JournalEncounterID]]
|-
| mapX || {{apitype|number}} ||
|-
| mapY || {{apitype|number}} ||
|}

==Patch changes==
* {{Patch 8.0.1|note=Added. Replaces {{api|C_EncounterJournal.GetCurrentMapEncounters}}.}}
```