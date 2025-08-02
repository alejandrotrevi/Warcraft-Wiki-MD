# API C EncounterJournal.GetDungeonEntrancesForMap

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the instance entrances for a map. Contrary to what the name implies, this includes raid instances.
 dungeonEntrances = C_EncounterJournal.GetDungeonEntrancesForMap(uiMapID)

==Arguments==
:;[[UiMapID|uiMapID]]:{{apitype|number}}

==Returns==
:;dungeonEntrances:structure - DungeonEntranceMapInfo[]

{| class="sortable darktable zebra"
|-
! Field !! Type !! Description
|-
| areaPoiID || {{apitype|number}} || Possible values listed in {{dbc|AreaPOI}}
|-
| position || {{apitype|Vector2DMixin}} || 
|-
| name || {{apitype|string}} ||
|-
| description || {{apitype|string}} ||
|-
| atlasName || {{apitype|string}} || [[AtlasID]] used as {{api|Texture:SetAtlas(atlasName)}}
|-
| journalInstanceID || {{apitype|number}} || Possible values listed in {{dbc|JournalInstance}}
|}

==Details==
Only discovered instances are returned.

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```