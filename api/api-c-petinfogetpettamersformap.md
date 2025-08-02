# API C PetInfo.GetPetTamersForMap

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_PetInfo|system=PetInfo}}
Returns the pet tamers on a map.
 petTamers = C_PetInfo.GetPetTamersForMap(uiMapID)

==Arguments==
:;uiMapID:{{apitype|number}} : [[UiMapID]]

==Returns==
:;petTamers:{{apitype|PetTamerMapInfo[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| areaPoiID || {{apitype|number}} || 
|-
| position || {{apitype|Vector2DMixin}} || 
|-
| name || {{apitype|string}} || 
|-
| atlasName || {{apitype|string?}} || 
|-
| textureIndex || {{apitype|number?}} || 
|}

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```