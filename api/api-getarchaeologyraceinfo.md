# API GetArchaeologyRaceInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the information for a specific race used in Archaeology.
 raceName, raceTexture, raceItemID, numFragmentsCollected, numFragmentsRequired, maxFragments = GetArchaeologyRaceInfo(raceIndex)

==Arguments==
:;raceIndex:{{apitype|number}} - Index of the race to query, between 1 and {{api|GetNumArchaeologyRaces}}().

==Returns==
:;raceName:{{apitype|string}} - Name of the race.
:;raceTexture:{{apitype|number}} ([[fileID]]) - The texture used by this race in the Archaeology UI.
:;raceItemID:{{apitype|number}} - Item ID of the [[Keystone]] used for the race's archaeology projects. Will be ''nil'' for [[Fossil]] as no such item exists.
:;numFragmentsCollected:{{apitype|number}} - Number of collected fragments for this race.
:;numFragmentsRequired:{{apitype|number}} - Number of fragments required to solve the current artifact
:;maxFragments:{{apitype|number}} - Maximum number of fragments that can be carried

==Example==
The snippet below prints the name of every Archaeology race.
 for i=1, GetNumArchaeologyRaces() do
  print((GetArchaeologyRaceInfo(i)))
 end

==Details==
* Returns "UNKNOWN", nil, 0, 0, 0, 0 if the <code>raceIndex</code> is out of bounds.
* The following textures are used:
{| class="darktable zebra" style="margin-left: 3.9em"
|+ Race Texture File IDs
!Texture!!Race
|-
|461831||Dwarf
|-
|461829||Draenei
|-
|461833||Fossil
|-
|461837||Night Elf
|-
|461835||Nerubian
|-
|462321||Orc
|-
|461839||Tol'vir
|-
|461841||Troll
|-
|461843||Vrykul
|-
|839111||Mantid
|-
|633002||Pandaren
|-
|633000||Mogu
|-
|1030616||Arakkoa
|-
|1030617||Draenor Clans
|-
|1030618||Ogre
|-
|1445575||Highborne
|-
|1445577||Highmountain Tauren
|-
|1445573||Demonic
|-
|2060051||Zandalari
|-
|2060049||Drust
|}

==Patch changes==
* {{Patch 8.0.1|note=Added Zandalari and Drust}}
* {{Patch 7.3.0|note=Second return value changed from a string texture path to a [[fileID]].}}
* {{Patch 4.0.6|note=Return values changed.|comment=Removed second return value (currency ID). Added numFragmentsCollected and numFragmentsRequired as 4th and 5th return values respectively.}}
* {{Patch 4.0.1|note=Added.}}

==See also==
* {{api|GetArchaeologyRaceInfoByID}}
* {{api|GetNumArchaeologyRaces}}
```