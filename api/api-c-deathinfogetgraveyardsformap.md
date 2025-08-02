# API C DeathInfo.GetGraveyardsForMap

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_DeathInfo|system=DeathInfo}}
Returns graveyard info and location for a map.
 graveyards = C_DeathInfo.GetGraveyardsForMap(uiMapID)

==Arguments==
:;uiMapID:{{apitype|number}} : [[UiMapID]]

==Returns==
:;graveyards:{{apitype|GraveyardMapInfo[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| areaPoiID || {{apitype|number}} || {{dbc|areapoi|AreaPOI.ID}}
|-
| position || {{apitype|Vector2DMixin}} || 
|-
| name || {{apitype|string}} || 
|-
| textureIndex || {{apitype|number}} || 
|-
| graveyardID || {{apitype|number}} || 
|-
| isGraveyardSelectable || {{apitype|boolean}} || 
|}

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```