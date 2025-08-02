# API GetArchaeologyRaceInfoByID

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for an Archaeology race.
 raceName, raceTextureID, raceItemID, numFragmentsCollected, numFragmentsRequired, maxFragments = GetArchaeologyRaceInfoByID(branchID)

==Arguments==
:;branchID:{{apitype|number}} - ID of the research branch (race) to query from {{dbc|ResearchBranch}}. The following are the valid IDs:

:{| class="darktable zebra col1-center" style="margin-left: 3.9em"
! ID !! Race
|-
| 1 || Dwarf
|-
| 2 || Draenei
|-
| 3 || Fossil
|-
| 4 || Night Elf
|-
| 5 || Nerubian
|-
| 6 || Orc
|-
| 7 || Tol'vir
|-
| 8 || Troll
|-
| 27 || Vrykul
|-
| 29 || Mantid
|-
| 229 || Pandaren
|-
| 231 || Mogu
|-
| 315 || Arakkoa
|-
| 350 || Draenor Clans
|-
| 382 || Ogre
|-
| 404 || Highborne
|-
| 406 || Highmountain Tauren
|-
| 408 || Demonic
|-
| 423 || Zandalari
|-
| 424 || Drust
|}

==Returns==
:;raceName:{{apitype|string}} - Name of the race.
:;raceTextureID:{{apitype|number}} ([[fileID]]) - The texture used by this race in the Archaeology UI.
:;raceItemID:{{apitype|number}} - The itemID of the [[Keystone]] the race uses. Will be nil for [[Fossil]] because no such item exists.
:;numFragmentsCollected:{{apitype|number}} - Number of collected fragments for this race.
:;numFragmentsRequired:{{apitype|number}} - Number of fragments required to solve the current artifact
:;maxFragments:{{apitype|number}} - Maximum number of fragments that can be carried

==Details==
* The following textures are used:
{| class="darktable zebra col1-center" style="margin-left: 3.9em"
|+ Race Texture File IDs
!Texture !! Race
|-
| 461831 || Dwarf
|-
| 461829 || Draenei
|-
| 461833 || Fossil
|-
| 461837 || Night Elf
|-
| 461835 || Nerubian
|-
| 462321 || Orc
|-
| 461839 || Tol'vir
|-
| 461841 || Troll
|-
| 461843 || Vrykul
|-
| 839111 || Mantid
|-
| 633002 || Pandaren
|-
| 633000 || Mogu
|-
| 1030616 || Arakkoa
|-
| 1030617 || Draenor Clans
|-
| 1030618 || Ogre
|-
| 1445575 || Highborne
|-
| 1445577 || Highmountain Tauren
|-
| 1445573 || Demonic
|-
| 2060051 || Zandalari
|-
| 2060049 || Drust
|}

==Patch changes==
* {{Patch 8.0.1|note=Added Zandalari and Drust to branchID list}}
* {{Patch 7.3.0|note=Second return value changed from a string texture path to a [[fileID]].}}
* {{Patch 5.4.0|note=Added.}}

==See also==
* {{api|GetArchaeologyRaceInfo}}
```