# API C Map.GetMapArtLayers

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Map|system=MapUI}}
Returns the art layers for a map.
 layerInfo = C_Map.GetMapArtLayers(uiMapID)

==Arguments==
:;uiMapID:{{apitype|number}} : [[UiMapID]]

==Returns==
:;layerInfo:{{apitype|UiMapLayerInfo[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
<!-- |+ [[Struct Map.UiMapLayerInfo|UiMapLayerInfo]] -->
! Field !! Type !! Description
|-
| layerWidth || {{apitype|number}} ||
|-
| layerHeight || {{apitype|number}} ||
|-
| tileWidth || {{apitype|number}} ||
|-
| tileHeight || {{apitype|number}} ||
|-
| minScale || {{apitype|number}} ||
|-
| maxScale || {{apitype|number}} ||
|-
| additionalZoomSteps || {{apitype|number}} ||
|}

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```