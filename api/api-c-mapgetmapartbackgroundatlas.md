# API C Map.GetMapArtBackgroundAtlas

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Map|system=MapUI}}
Returns the background atlas for a map.
 atlasName = C_Map.GetMapArtBackgroundAtlas(uiMapID)

==Arguments==
:;uiMapID:{{apitype|number}} : [[UiMapID]]

==Returns==
:;atlasName:{{apitype|string}} - [[AtlasID]]

==Values==
{| class="sortable darktable zebra"
|-
! ID !! Atlas
|-
| 993 || AdventureMap_TileBg
|-
| 994 || AdventureMap_TileBg
|-
| 1011 || AdventureMap_TileBg
|-
| 1014 || AdventureMap_TileBg
|-
| 1208 || AdventureMap_TileBg
|-
| 1209 || AdventureMap_TileBg
|-
| 1384 || AdventureMap_TileBg
|-
| 1467 || AdventureMap_TileBg
|}

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```