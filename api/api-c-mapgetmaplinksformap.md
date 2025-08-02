# API C Map.GetMapLinksForMap

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Map|system=MapUI}}
Returns the map pins that link to another map.
 mapLinks = C_Map.GetMapLinksForMap(uiMapID)

==Arguments==
:;uiMapID:{{apitype|number}} : [[UiMapID]]

==Returns==
:;mapLinks:{{apitype|MapLinkInfo[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
<!-- |+ [[Struct Map.MapLinkInfo|MapLinkInfo]] -->
! Field !! Type !! Description
|-
| areaPoiID || {{apitype|number}} ||
|-
| position || {{apitype|Vector2DMixin}} ||
|-
| name || {{apitype|string}} ||
|-
| atlasName || {{apitype|string}} ||
|-
| linkedUiMapID || {{apitype|number}} ||
|}

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```