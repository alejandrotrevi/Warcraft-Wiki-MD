# API C VignetteInfo.GetVignetteInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_VignetteInfo|system=Vignette}}
Returns vignette info.
 vignetteInfo = C_VignetteInfo.GetVignetteInfo(vignetteGUID)

==Arguments==
:;vignetteGUID:{{apitype|WOWGUID}}

==Returns==
:;vignetteInfo:{{apitype|VignetteInfo?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| {{apiname|vignetteGUID}} || {{apitype|WOWGUID}} || 
|-
| {{apiname|objectGUID}} || {{apitype|WOWGUID}} || 
|-
| {{apiname|name}} || {{apitype|string}} || 
|-
| {{apiname|isDead}} || {{apitype|boolean}} || 
|-
| {{apiname|onWorldMap}} || {{apitype|boolean}} || 
|-
| {{apiname|zoneInfiniteAOI}} || {{apitype|boolean}} || <font color="green">9.0.2</font>
|-
| {{apiname|onMinimap}} || {{apitype|boolean}} || 
|-
| {{apiname|isUnique}} || {{apitype|boolean}} || 
|-
| {{apiname|inFogOfWar}} || {{apitype|boolean}} || 
|-
| {{apiname|atlasName}} || {{apitype|textureAtlas}} || 
|-
| {{apiname|hasTooltip}} || {{apitype|boolean}} || 
|-
| {{apiname|vignetteID}} || {{apitype|number}} || 
|-
| {{apiname|type}} || {{apitype|Enum.VignetteType}} || 
|-
| {{apiname|rewardQuestID}} || {{apitype|number}} || 
|-
| {{apiname|tooltipWidgetSet}} || {{apitype|number?}} || <font color="green">10.2.6</font> - Renamed from <code>widgetSetID</code>
|-
| {{apiname|iconWidgetSet}} || {{apitype|number?}} || <font color="green">10.2.6</font>
|-
| {{apiname|addPaddingAboveTooltipWidgets}} || {{apitype|boolean?}} || <font color="green">10.2.6</font> - Renamed from <code>addPaddingAboveWidgets</code>
|-
| {{apiname|mapPin}} || {{apitype|UIMapPinInfo?}} || <font color="green">11.0.7</font>
|-
| {{apiname|objectiveType}} || {{apitype|Enum.VignetteObjectiveType?}} || <font color="green">11.0.7</font>
|}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.VignetteType
! Value !! Field !! Description
|-
| 0 || {{apiname|Normal}} || 
|-
| 1 || {{apiname|PvPBounty}} || 
|-
| 2 || {{apiname|Torghast}} || <font color="green">9.0.1</font>
|-
| 3 || {{apiname|Treasure}} || <font color="green">9.0.2</font>
|-
| 4 || {{apiname|FyrakkFlight}} || <font color="green">10.1.0</font>
|}

{| class="sortable darktable zebra" style="margin-left: 3.9em"
|+ UIMapPinInfo
! Field !! Type !! Description
|-
| {{apiname|button}} || {{apitype|UIButtonInfo}} || 
|-
| {{apiname|buttonSelected}} || {{apitype|UIButtonInfo}} || 
|-
| {{apiname|underlay}} || {{apitype|textureAtlas}} || 
|}

{{:Struct UIButtonInfo}}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.VignetteObjectiveType
! Value !! Field !! Description
|-
| 0 || {{apiname|None}} || 
|-
| 1 || {{apiname|Defeat}} || 
|-
| 2 || {{apiname|DefeatShowRemainingHealth}} || 
|}

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```