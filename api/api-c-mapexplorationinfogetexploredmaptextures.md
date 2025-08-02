# API C MapExplorationInfo.GetExploredMapTextures

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_MapExplorationInfo|system=MapExplorationInfo}}
Returns explored map textures for a map.
 overlayInfo = C_MapExplorationInfo.GetExploredMapTextures(uiMapID)

==Arguments==
:;uiMapID:{{apitype|number}} : [[UiMapID]]

==Returns==
:;overlayInfo:{{apitype|UiMapExplorationInfo[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| textureWidth || {{apitype|number}} || 
|-
| textureHeight || {{apitype|number}} || 
|-
| offsetX || {{apitype|number}} || 
|-
| offsetY || {{apitype|number}} || 
|-
| isShownByMouseOver || {{apitype|boolean}} || 
|-
| isDrawOnTopLayer || {{apitype|boolean}} || <font color="green">10.0.0</font>
|-
| fileDataIDs || {{apitype|number[]}} || 
|-
| hitRect || {{apitype|UiMapExplorationHitRect}} || 
|}

{| class="sortable darktable zebra" style="margin-left: 3.9em"
|+ UiMapExplorationHitRect
! Field !! Type !! Description
|-
| top || {{apitype|number}} || 
|-
| bottom || {{apitype|number}} || 
|-
| left || {{apitype|number}} || 
|-
| right || {{apitype|number}} || 
|}

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```